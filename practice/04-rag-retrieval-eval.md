# Practice 04 — RAG mini + retrieval eval

**Sau chương 6B của notebook. Thời gian: ~1.5 giờ.**

## Mục tiêu

Xây một RAG tối thiểu trên 20–30 tài liệu ngắn và đo **retrieval riêng**,
không chỉ chấm câu trả lời cuối.

## Bài làm

1. **Chuẩn bị dữ liệu:** lấy 20 đoạn văn ngắn (mỗi đoạn 3–5 câu) về một chủ đề
   bạn rành, mỗi đoạn nói về một ý khác nhau. Đánh số đoạn 1–20.
2. **Viết 10 câu hỏi**, mỗi câu có đáp án nằm trong **đúng 1 đoạn** đã định
   trước (golden passage). Ghi lại: câu hỏi → đoạn đúng.
3. **Xây RAG tối thiểu:** chunk (mỗi đoạn là 1 chunk), embed bằng một
   embedding API bất kỳ, lưu vector vào list trong Python, retrieve bằng
   cosine similarity (không cần vector DB).
4. **Đo retrieval:** với mỗi câu hỏi, kiểm tra đoạn đúng có nằm trong top-3
   không. Tính recall@3 = số câu có đoạn đúng trong top-3 / 10.
5. **Thử 2 cải tiến, đo lại sau mỗi lần (chỉ đổi 1 thứ mỗi lần):**
   - (a) Viết lại câu hỏi dài hơn, rõ ràng hơn (query rewriting).
   - (b) Tăng top-k lên 5 rồi rerank bằng tay (đọc 5 đoạn, chọn lại top-3).

## Tiêu chí đạt

- [ ] Có bảng: câu hỏi, đoạn đúng, top-3 retrieve được, đúng/sai.
- [ ] recall@3 baseline được ghi lại bằng số, không phải cảm nhận.
- [ ] Sau mỗi cải tiến, recall@3 thay đổi thế nào — và bạn kết luận được
      cải tiến nào đáng giữ.

## Câu hỏi tự kiểm tra

1. recall@3 = 40% nhưng câu trả lời cuối "nghe đúng" 90% — tin số nào?
2. Một câu hỏi có đáp án nằm ở **2 đoạn** khác nhau — golden set ghi thế nào?
3. Thêm 1.000 tài liệu nữa vào index thì recall sẽ tăng hay giảm, vì sao?
