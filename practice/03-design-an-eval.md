# Practice 03 — Design an eval

**Sau chương 10 của notebook. Thời gian: ~1.5 giờ.**

## Mục tiêu

Thiết kế một eval nhỏ (10 task) cho một agent viết unit test, và chạy thử
baseline bằng tay.

## Bài làm

1. **Chọn task thật:** lấy 10 function từ một repo bạn quen, mỗi function cần
   1 test file. Ghi lại: input (code của function), expected outcome
   (test chạy pass + cover ít nhất 1 case biên).
2. **Tiêu chí chấm (bằng code, không chấm bằng cảm tính):**
   - Test file được tạo ra, pytest chạy pass.
   - Test cover được case biên đã định trước (kiểm tra bằng coverage hoặc
     bằng tay).
3. **Chạy baseline:** cho agent (Claude Code hoặc loop ở bài 01) làm 10 task,
   ghi lại: pass mấy/10, trung bình mấy bước, lỗi thuộc loại nào
   (chọn sai tool? thiếu context? test sai logic?).
4. **Phân loại lỗi:** với mỗi task fail, viết một dòng: nguyên nhân gốc là gì.

## Tiêu chí đạt

- [ ] Có bảng kết quả: task, pass/fail, số bước, loại lỗi.
- [ ] Ít nhất 1 task fail được phân loại đúng nguyên nhân (không đổ chung
      cho "model dở").
- [ ] Đề xuất được **một** thay đổi cụ thể (prompt/tool/quy trình) để thử
      ở vòng sau — và nói rõ sẽ đo lại bằng metric nào.

## Câu hỏi tự kiểm tra

1. Vì sao 10 task là đủ để bắt đầu nhưng không đủ để kết luận "agent tốt"?
2. Task set lấy từ repo bạn quen — có nguy cơ gì về độ đại diện?
3. Nếu dùng LLM-as-judge để chấm test thì cần calibrate thế nào?
