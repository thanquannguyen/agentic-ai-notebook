# Agentic AI — Notebook & Practice

Tài liệu học agentic AI từ tầng "biết dùng" tới tầng "biết thiết kế và vận hành",
dùng cho hai việc:

1. **Review thực tập sinh AI** — phân biệt người biết dùng tool với người biết
   thiết kế hệ thống agentic (xem `notebook/Agentic-AI-Notebook.md`, chương 12).
2. **Ôn thi cả 4 chứng chỉ Claude** (xem `exams/`) — trọng tâm là CCAR-F,
   sau đó mở rộng lên CCDV-F, CCAR-P và CCAO-F khi cần.

## Cấu trúc

```
├── notebook/
│   └── Agentic-AI-Notebook.md   # Notebook chính (13 chương + phụ lục)
├── exams/
│   ├── CCAO-F.md                # Associate: Foundations ($99, 60 câu)
│   ├── CCDV-F.md                # Developer: Foundations ($125, 53 câu)
│   ├── CCAR-F.md                # Architect: Foundations ($125, 60 câu) ← mục tiêu chính
│   └── CCAR-P.md                # Architect: Professional ($175, 63 câu)
├── resources.md                 # Link tài liệu chính thức + repo public chọn lọc
└── practice/
    ├── 01-minimal-agent-loop.md # Xây vòng lặp agent tối thiểu bằng Python
    ├── 02-write-a-skill.md      # Viết một SKILL.md đúng chuẩn
    ├── 03-design-an-eval.md     # Thiết kế eval cho một agent nhỏ
    ├── 04-rag-retrieval-eval.md # RAG mini + đo recall@k và faithfulness
    └── 05-debug-a-broken-agent.md # Chẩn đoán một agent hỏng từ trace thật (kèm đáp án cho người review)
```

## Lộ trình thi khuyên dùng

| Thứ tự | Chứng chỉ | Vì sao ở vị trí này |
|---|---|---|
| 1 | **CCAR-F** | Mục tiêu chính: thiết kế hệ thống agentic, review intern, mentor. Notebook này cover toàn bộ 5 domain của nó. |
| 2 | **CCDV-F** | Bổ sung phần code + tích hợp ứng dụng (Applications & Integration 33.1%). Chồng chéo mạnh với CCAR-F nên học nhanh. ⚠️ Nội dung thi cập nhật từ 07/12/2026 — đọc exam guide mới trước khi ôn. |
| 3 | **CCAR-P** | Bậc sau CCAR-F, cần thêm kinh nghiệm vận hành production thật (governance, SLA, incident, handoff). |
| 4 | CCAO-F | Dễ nhất, rẻ nhất — thi cuối để hoàn thành bộ 4, hoặc thi đầu làm warm-up nếu muốn. |

Tổng phí cả 4: $524. Mỗi chứng chỉ hiệu lực 12 tháng, gia hạn miễn phí nếu
đúng hạn. Đăng ký thi cần email công ty thuộc Claude Partner Network.

## Cách dùng

- **Tự học:** đọc notebook theo thứ tự, làm bài `practice/` sau mỗi cụm chương
  tương ứng (01 sau chương 1, 02 sau chương 5, 03 sau chương 10, 04 sau chương 6B,
  05 sau chương 12B).
- **Review intern:** dùng rubric và bộ câu hỏi ở chương 12 của notebook.
  Hỏi theo tầng — đừng hỏi câu tầng 3 khi người ta chưa qua tầng 1.
- **Ôn thi:** đọc file `exams/<mã-thi>.md` tương ứng để biết domain weights
  và tài liệu riêng cho từng chứng chỉ, sau đó làm đề thử trong các repo ở
  `resources.md`.

## Nguồn

Nội dung gốc trong repo này (notebook + bài practice + file exams) là ghi chú tự
soạn từ các nguồn công khai, chủ yếu là tài liệu của Anthropic và exam guide
v1.0 (07/2026). Các repo và tài liệu bên ngoài chỉ được **link tham khảo**,
không copy nội dung — xem `resources.md`.

Tài liệu chính thức nên đọc trước mọi thứ khác:

- Anthropic, "Building Effective Agents" — https://www.anthropic.com/engineering/building-effective-agents
- Anthropic, "How we built our multi-agent research system" — https://www.anthropic.com/engineering/multi-agent-research-system
- Exam guides v1.0 (07/2026) — tải từ Partner Academy (clau.de/CCAF)

## License

Nội dung gốc trong repo này: MIT. Tài liệu và repo được link tới thuộc về
tác giả của chúng, theo license riêng của từng nguồn.
