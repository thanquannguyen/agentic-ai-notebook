# CCAR-P — Claude Certified Architect: Professional

> Nguồn: Anthropic CCAR-P Exam Guide v1.0 (hiệu lực 07/2026). Kiểm tra lại
> exam guide trước khi đăng ký — Anthropic ghi rõ nội dung có thể thay đổi.
>
> Đây là bậc **sau CCAR-F**: dành cho architect senior sở hữu hệ thống
> production end-to-end. Không nên thi trước khi có CCAR-F + kinh nghiệm
> triển khai thật.

## Exam facts

| | |
|---|---|
| Mã thi | CCAR-P |
| Đối tượng | Tech lead / architect senior sở hữu hệ thống Claude production end-to-end |
| Số câu | 63 (trắc nghiệm + trả lời nhiều đáp án, theo tình huống production) |
| Thời gian | 120 phút |
| Phí | $175 |
| Đậu | 720 / 1.000 (thang điểm, không phải 72% số câu) |
| Hiệu lực | 12 tháng, gia hạn miễn phí nếu đúng hạn |
| Điều kiện đăng ký | Email công ty thuộc Claude Partner Network |

## Bảy domain và trọng số

| # | Domain | Trọng số | ~Số câu | Thi cái gì |
|---|---|---|---|---|
| 1 | Solution Design & Architecture | 17% | ~11 | Biến bài toán kinh doanh thành giải pháp Claude, chọn giữa workflow / agent / augmented LLM, multi-agent orchestration |
| 2 | Claude Models, Prompting & Context Engineering | 13% | ~8 | Chọn model theo trade-off, system prompt và guardrails, context window, prompt caching, modular prompts và Skills |
| 3 | **Integration** | **19%** | ~12 | Capability bloat và least privilege, authentication gaps, **RAG pipelines và retrieval strategy**, MCP vs API vs CLI vs agent-to-agent, monitoring at scale |
| 4 | Evaluation, Testing & Optimization | 16% | ~10 | Metrics, evaluation datasets, A/B tests, chẩn đoán hallucination và model mismatch, trade-off cost–latency |
| 5 | Governance, Safety & Risk Management | 14% | ~9 | Guardrails, failure modes, human-in-the-loop validation, quy định (GDPR, HIPAA, FedRAMP), bias và transparency |
| 6 | Stakeholder Communication & Lifecycle Management | 14% | ~9 | Discovery, giải thích trade-off, kỳ vọng và SLA, documentation, handoff và iteration |
| 7 | Developer Productivity & Operational Enablement | 7% | ~4 | Cấu hình Claude Code và tool cho team, AI-assisted workflows, operational debugging |

**Điểm mấu chốt:** **28% đề thi (D5 + D6) là phi kỹ thuật** — governance và
làm việc với stakeholder. Đây là điểm khác biệt lớn nhất so với CCAR-F: thi
Professional là thi **quyết định và trách nhiệm**, không chỉ thi kỹ thuật.
Ba domain không có trong CCAR-F: Evaluation/Testing/Optimization (D4),
Governance/Safety/Risk (D5), Stakeholder/Lifecycle (D6).

## Học gì

- **Anthropic Academy (miễn phí):** 5-course Professional prep path (~12 giờ,
  733 phút), bắt đầu từ *Claude Platform & Solution Design*.
- **Notebook này:** toàn bộ 13 chương là nền tảng (đặc biệt chương 6B về RAG
  cho domain Integration, chương 8–10 về HIML/evals cho D4–D5). Phần còn thiếu
  so với CCAR-F: governance theo quy định (GDPR/HIPAA/FedRAMP), stakeholder
  management, SLA và lifecycle — học từ khóa prep chính thức, không có trong
  notebook này.
- **Kinh nghiệm thật:** CCAR-P hỏi về hệ thống đã triển khai (monitoring,
  incident, handoff, SLA) — không có kinh nghiệm vận hành thì khó trả lời
  đúng các câu scenario.

## Tài liệu public cho CCAR-P

| Nguồn | Nội dung |
|---|---|
| [girishr/ClaudeCertifiedArchitect-Professional-Prep](https://github.com/girishr/ClaudeCertifiedArchitect-Professional-Prep) | 5 module cô đọng từ khóa chính thức, 75 câu scenario, 8 hands-on lab, RAG chunking/indexing, web hub luyện đề |
| [ravnhq/claude-certified-architect](https://github.com/ravnhq/claude-certified-architect) | Study guide + practice exam 63 câu cho track Professional |
| [MoBRUEC — CCAR-P guide](https://github.com/mobruec/mobruec/blob/HEAD/claude-certified-architect/readme.md) | Guide theo đúng exam guide v1.0, cảnh báo về các bản tóm tắt bịa số liệu |
| [claudeexpert.avinashai.com — CCAR-P Study Guide](https://claudeexpert.avinashai.com/00_exam_scope_and_study_plan.html) | Study plan + câu hỏi practice tự viết (không phải đề thật), map scope theo exam guide |

## Kế hoạch gợi ý (sau khi có CCAR-F)

- **Giai đoạn 1:** Học 5-course Professional prep path (~12h). Đối chiếu từng
  module với 7 domain trong bảng trên.
- **Giai đoạn 2:** Học sâu 3 domain mới so với CCAR-F (D4 evals, D5 governance,
  D6 stakeholder) — đây là 44% đề thi.
- **Giai đoạn 3:** Làm 75 câu scenario của girishr + mock exam của ravnhq.
  Tự chấm theo domain, yếu domain nào thì quay lại học domain đó.

## Liên hệ với các chứng chỉ khác

- **Lộ trình khuyên dùng:** CCAR-F → (kinh nghiệm triển khai) → CCAR-P.
  Thi CCAR-P ngay sau CCAR-F mà chưa từng vận hành hệ thống production thì
  phần scenario về incident/SLA/handoff sẽ rất khó.
- CCDV-F giúp phần Integration (D3) của CCAR-P nếu đã học kỹ về API và MCP.
