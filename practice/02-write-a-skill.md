# Practice 02 — Write a SKILL.md

**Sau chương 5 của notebook. Thời gian: ~45 phút.**

## Mục tiêu

Viết một skill hoàn chỉnh cho một quy trình thật của team mình, sao cho một
người (hoặc agent) chưa từng làm quy trình đó vẫn làm đúng.

## Bài làm

Chọn một quy trình thật, ví dụ: "viết unit test cho module mới", "review PR",
"viết commit message", "tạo bug report". Viết file `SKILL.md` gồm:

```markdown
---
name: ten-skill
description: Dùng khi <tình huống cụ thể>. Không dùng khi <tình huống loại trừ>.
---

# Tên skill

## Khi nào dùng
...

## Quy trình (từng bước)
1. ...
2. ...

## Ví dụ input/output
...

## Lỗi hay gặp
- ...
```

## Tiêu chí đạt

- [ ] Đọc riêng phần `description` đã biết **khi nào** dùng skill (một người lạ
      đọc xong không hỏi lại "cái này dùng lúc nào?").
- [ ] Quy trình có bước kiểm chứng cuối (test pass, checklist, output mẫu).
- [ ] Có ít nhất 1 ví dụ input/output cụ thể, không chỉ mô tả chung chung.
- [ ] Liệt kê ít nhất 2 lỗi hay gặp và cách tránh.

## Câu hỏi tự kiểm tra

1. Skill của bạn dài 200 dòng — có vấn đề gì với progressive disclosure?
2. Một phần kiến thức trong skill đã lỗi thời (tool đổi tên) — ai phát hiện,
   sửa ở đâu?
3. Skill này khác gì với việc paste cùng nội dung vào chat mỗi lần?
