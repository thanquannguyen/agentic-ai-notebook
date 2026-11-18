# Practice 01 — Minimal agent loop

**Sau chương 1 của notebook. Thời gian: ~1 giờ. Cần: Python + Anthropic API key.**

## Mục tiêu

Viết một vòng lặp agent tối thiểu (dưới 100 dòng) gọi Claude API, cho model dùng
một tool `read_file`, và tự dừng đúng lúc. Hiểu bằng tay thì mới review được
người khác.

## Bài làm

1. Viết loop theo pseudocode ở chương 1.1: gửi message → nếu `stop_reason`
   là `tool_use` thì chạy tool, append kết quả, lặp lại.
2. Thêm **3 giới hạn bắt buộc**: max 10 bước, timeout 30s cho mỗi tool call,
   và dừng khi model trả về text (không còn tool call).
3. Thêm **phát hiện lặp**: nếu cùng một tool call với cùng argument lặp lại
   3 lần → dừng và in lý do.
4. Chạy thử với task: "Đọc file README.md trong thư mục hiện tại và tóm tắt
   trong 3 câu."

## Tiêu chí đạt

- [ ] Loop dừng sau tối đa 10 bước trong mọi trường hợp (kể cả khi model lặp).
- [ ] Tool lỗi (ví dụ: file không tồn tại) không crash loop — lỗi được trả
      về cho model dưới dạng text.
- [ ] Log ra được: số bước đã chạy, tên tool đã gọi, tổng token (nếu API trả về).

## Câu hỏi tự kiểm tra

1. Bỏ giới hạn max bước đi thì chuyện gì xảy ra khi model bị kẹt?
2. Vì sao phải append cả tool call *và* tool result vào history, không chỉ
   append result?
3. Muốn thêm tool thứ hai (`list_directory`) thì phải sửa những chỗ nào?
