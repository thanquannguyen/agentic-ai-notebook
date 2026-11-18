# Agentic AI — Notebook & Practice

Tài liệu học agentic AI từ tầng "biết dùng" tới tầng "biết thiết kế và vận hành",
dùng cho hai việc:

1. **Review thực tập sinh AI** — phân biệt người biết dùng tool với người biết
   thiết kế hệ thống agentic (xem `notebook/Agentic-AI-Notebook.md`, chương 12).
2. **Ôn thi Claude Certified Architect – Foundations (CCAR-F)** — chứng chỉ
   Claude for Partner (xem chương 13 của notebook để map domain và kế hoạch ôn).

## Cấu trúc

```
├── notebook/
│   └── Agentic-AI-Notebook.md   # Notebook chính (13 chương + phụ lục)
├── resources.md                 # Link tài liệu chính thức + repo public chọn lọc
└── practice/
    ├── 01-minimal-agent-loop.md # Xây vòng lặp agent tối thiểu bằng Python
    ├── 02-write-a-skill.md      # Viết một SKILL.md đúng chuẩn
    ├── 03-design-an-eval.md     # Thiết kế eval cho một agent nhỏ
    └── 04-rag-retrieval-eval.md # RAG mini + đo recall@k và faithfulness
```

## Cách dùng

- **Tự học:** đọc notebook theo thứ tự, làm bài `practice/` sau mỗi cụm chương
  tương ứng (01 sau chương 1, 02 sau chương 5, 03 sau chương 10, 04 sau chương 6B).
- **Review intern:** dùng rubric và bộ câu hỏi ở chương 12 của notebook.
  Hỏi theo tầng — đừng hỏi câu tầng 3 khi người ta chưa qua tầng 1.
- **Ôn thi:** học theo map domain ở chương 13, sau đó làm đề thử trong các repo
  ở `resources.md`.

## Nguồn

Nội dung gốc trong repo này (notebook + bài practice) là ghi chú tự soạn từ các
nguồn công khai, chủ yếu là tài liệu của Anthropic. Các repo và tài liệu bên
ngoài chỉ được **link tham khảo**, không copy nội dung — xem `resources.md`.

Tài liệu chính thức nên đọc trước mọi thứ khác:

- Anthropic, "Building Effective Agents" — https://www.anthropic.com/engineering/building-effective-agents
- Anthropic, "How we built our multi-agent research system" — https://www.anthropic.com/engineering/multi-agent-research-system
- CCAR-F Exam Guide v1.0 (07/2026) — tải từ Partner Academy (clau.de/CCAF)

## License

Nội dung gốc trong repo này: MIT. Tài liệu và repo được link tới thuộc về
tác giả của chúng, theo license riêng của từng nguồn.
