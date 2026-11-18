# Bài 5 — Debug một agent bị hỏng

> **Dành cho người review (Nguyên):** bài này đưa cho intern một trace hỏng
> thật và bắt họ chẩn đoán. Đáp án ở cuối file — **chỉ người review đọc**,
> đừng đưa đáp án cho intern trước.

## Tình huống

Team có một agent "research" nhỏ: nhận một câu hỏi, dùng tool `search_web`
để tìm tài liệu, đọc vài trang bằng tool `fetch_page`, rồi trả lời kèm nguồn.
Hôm nay agent được hỏi:

> "Claude Code có hỗ trợ hook `PreToolUse` không? Nếu có, hook đó chạy khi nào?"

Agent trả lời sau 4 phút, tốn ~180.000 token:

> "Có. Hook PreToolUse chạy trước khi tool được gọi. Nguồn: tài liệu Claude Code."

Người dùng phàn nàn: câu trả lời đúng nhưng **quá chung chung, không có chi
tiết nào về hook nhận input gì, trả về gì, và khi nào thì chặn được tool** —
trong khi tài liệu chính thức có đầy đủ thông tin đó. Và 180.000 token cho một
câu hỏi tra cứu là quá nhiều.

## Trace (rút gọn, giữ nguyên thứ tự)

```
Bước 1:  search_web("Claude Code PreToolUse hook") → 10 kết quả, ~8.000 token
Bước 2:  fetch_page(kết quả #1: blog cá nhân 2025) → ~12.000 token
Bước 3:  fetch_page(kết quả #2: blog cá nhân 2024) → ~15.000 token
Bước 4:  search_web("PreToolUse hook Claude Code documentation") → 10 kết quả, ~8.000 token
Bước 5:  fetch_page(kết quả #1: trang docs chính thức) → ~20.000 token
Bước 6:  search_web("Claude Code hooks PreToolUse example") → 10 kết quả, ~8.000 token
Bước 7:  fetch_page(kết quả #3: forum thread) → ~18.000 token
Bước 8:  search_web("PreToolUse hook input output") → 10 kết quả, ~8.000 token
Bước 9:  fetch_page(kết quả #2: blog cá nhân 2025) → ~14.000 token
Bước 10: search_web("Claude Code hook block tool call") → 10 kết quả, ~8.000 token
... (lặp lại search + fetch tương tự tới bước 24)
Bước 25: trả lời (không trích dẫn cụ thể trang nào)
```

## Yêu cầu cho intern

1. **Chẩn đoán:** agent bị lỗi gì? Xếp lỗi vào bảng ở notebook chương 12B.3
   (triệu chứng → nguyên nhân gốc). Nêu ít nhất **3 vấn đề khác nhau** trong
   trace, mỗi vấn đề kèm bằng chứng là bước cụ thể nào trong trace.
2. **Thứ tự ưu tiên:** trong 3 vấn đề đó, cái nào sửa trước? Vì sao?
3. **Đề xuất sửa:** cho mỗi vấn đề, nêu cách sửa cụ thể ở đúng tầng (prompt /
   tool / harness / kiến trúc) — không được sửa mọi thứ bằng prompt.
4. **Kiểm chứng:** sau khi sửa, làm sao biết agent tốt lên thật? Thiết kế
   3–5 câu hỏi test và tiêu chí pass cho từng câu.

## Đáp án (chỉ người review)

**Vấn đề 1 — Không có tiêu chí dừng và không có tiêu chí đủ thông tin
(harness).** Agent không biết "đủ rồi" là khi nào: đã đọc docs chính thức ở
bước 5 mà vẫn search tiếp 19 bước nữa. Bằng chứng: bước 5 đã có nguồn chính
thức, bước 6–24 chỉ lặp lại cùng loại query. Sửa: harness định nghĩa tiêu chí
dừng bằng code — ví dụ: đã có ít nhất một nguồn chính thức + đã trả lời được
cả 3 phần của câu hỏi (có/không, chạy khi nào, input/output) thì dừng; hoặc
budget tối đa 8 bước. Đây là lỗi tầng harness, không phải prompt.

**Vấn đề 2 — Không ưu tiên nguồn và không lọc kết quả (tool + prompt).**
Agent fetch blog cá nhân cũ (2024, 2025) trước docs chính thức, và không có
cơ chế nào ưu tiên nguồn tin cậy. Bằng chứng: bước 2–3 fetch blog trước, bước
5 mới tới docs. Sửa: tool `search_web` trả về kèm độ tin cậy nguồn (official
docs > blog > forum), hoặc instruction yêu cầu ưu tiên docs chính thức; tốt
hơn nữa là tool result tự tóm tắt thay vì trả nguyên trang 12–20k token.

**Vấn đề 3 — Tool result quá lớn, không lọc (tool design).** Mỗi `fetch_page`
trả 12–20k token, phần lớn là nội dung không liên quan (nav, footer, bài khác).
24 bước × ~10k token trung bình ≈ 180k token. Sửa: tool chỉ trả phần liên quan
(extract theo heading/keyword) hoặc trả bản tóm tắt có trích dẫn; đặt giới
hạn token cho tool result trong harness và cắt ngắn có báo cho model biết.

**Vấn đề 4 (điểm cộng) — Không trích dẫn nguồn cụ thể.** Câu trả lời cuối
không nói lấy thông tin từ trang nào, nên người dùng không verify được. Sửa:
yêu cầu output có citation (URL + đoạn trích) và harness check citation tồn
tại trong trace trước khi trả lời.

**Chấm bài:** intern đạt nếu nêu được vấn đề 1 + một trong hai vấn đề 2/3, và
sửa đúng tầng (không sửa bằng prompt cho vấn đề 1 và 3). Intern giỏi nếu nêu
được cả 4 vấn đề, xếp đúng thứ tự ưu tiên (1 → 3 → 2 → 4, vì dừng sớm và lọc
token giảm cost ngay lập tức), và thiết kế được test có tiêu chí pass đo được
(ví dụ: "trả lời đúng cả 3 phần + ≤ 8 bước + ≤ 30k token + có citation").
