# CCAR-P — Claude Certified Architect: Professional

> Nguồn: Anthropic CCAR-P Exam Guide v1.0 (hiệu lực 07/2026) + Exam Guide
> **v1.1** (thi từ 07/12/2026). Kiểm tra lại exam guide trước khi đăng ký —
> Anthropic ghi rõ nội dung có thể thay đổi.
>
> Đây là bậc **sau CCAR-F**: dành cho architect senior sở hữu hệ thống
> production end-to-end. Không nên thi trước khi có CCAR-F + kinh nghiệm
> triển khai thật.
>
> ⚠️ **Đề thi đổi từ 07/12/2026 — file này giữ cả 2 bản.** Phiên bản đề tùy
> thuộc **ngày thi**, không tùy ngày đăng ký: thi tới 06/12/2026 thì theo bản
> cũ (63 câu), thi từ 07/12/2026 thì theo bản mới v1.1 (70 câu). Nếu có thể
> thi trước ngày đổi thì ôn theo bản cũ. Chi tiết bản mới theo Practica Cert
> Prep (đối chiếu exam guide v1.1 chính thức ngày 21/11/2026).

## Exam facts

| | |
|---|---|
| Mã thi | CCAR-P |
| Đối tượng | Tech lead / architect senior sở hữu hệ thống Claude production end-to-end |
| Số câu | **63** (bản cũ, thi tới 06/12/2026) · **70, trong đó 60 tính điểm + 10 câu thử không tính điểm** (bản mới v1.1, từ 07/12/2026) |
| Thời gian | 120 phút (cả 2 bản — bản mới ít thời gian hơn mỗi câu) |
| Phí | $175 |
| Đậu | 720 / 1.000 (thang điểm, không phải 72% số câu) |
| Hiệu lực | 12 tháng, gia hạn miễn phí nếu đúng hạn |
| Điều kiện đăng ký | Email công ty thuộc Claude Partner Network |

## Bảy domain và trọng số — 2 phiên bản

### Bản cũ — thi tới 06/12/2026 (63 câu)

| # | Domain | Trọng số | ~Số câu | Thi cái gì |
|---|---|---|---|---|
| 1 | Solution Design & Architecture | 17% | ~11 | Biến bài toán kinh doanh thành giải pháp Claude, chọn giữa workflow / agent / augmented LLM, multi-agent orchestration |
| 2 | Claude Models, Prompting & Context Engineering | 13% | ~8 | Chọn model theo trade-off, system prompt và guardrails, context window, prompt caching, modular prompts và Skills |
| 3 | **Integration** | **19%** | ~12 | Capability bloat và least privilege, authentication gaps, **RAG pipelines và retrieval strategy**, MCP vs API vs CLI vs agent-to-agent, monitoring at scale |
| 4 | Evaluation, Testing & Optimization | 16% | ~10 | Metrics, evaluation datasets, A/B tests, chẩn đoán hallucination và model mismatch, trade-off cost–latency |
| 5 | Governance, Safety & Risk Management | 14% | ~9 | Guardrails, failure modes, human-in-the-loop validation, quy định (GDPR, HIPAA, FedRAMP), bias và transparency |
| 6 | Stakeholder Communication & Lifecycle Management | 14% | ~9 | Discovery, giải thích trade-off, kỳ vọng và SLA, documentation, handoff và iteration |
| 7 | Developer Productivity & Operational Enablement | 7% | ~4 | Cấu hình Claude Code và tool cho team, AI-assisted workflows, operational debugging |

**Điểm mấu chốt (bản cũ):** **28% đề thi (D5 + D6) là phi kỹ thuật** —
governance và làm việc với stakeholder. Đây là điểm khác biệt lớn nhất so
với CCAR-F: thi Professional là thi **quyết định và trách nhiệm**, không chỉ
thi kỹ thuật. Ba domain không có trong CCAR-F: Evaluation/Testing/Optimization
(D4), Governance/Safety/Risk (D5), Stakeholder/Lifecycle (D6) = **44%** đề thi.

### Bản mới v1.1 — thi từ 07/12/2026 (70 câu, 60 tính điểm)

| # | Domain | Trọng số | ~Số câu* | Thi cái gì |
|---|---|---|---|---|
| 1 | Solution Design and Architecture | 18% | ~11 | Giao việc cho người vs Claude, chọn pattern, thiết kế orchestrator/subagent, chọn deployment surface và agent runtime |
| 2 | Claude Models, Prompting, and Context Engineering | 13% | ~8 | Chọn model tier, chẩn đoán system prompt, caching, reasoning effort, vòng đời context |
| 3 | **Integration** | **21%** | ~13 | Tool least-privilege, auth posture, kiến trúc retrieval, MCP vs API vs agent-to-agent, kiểm soát độ tin cậy |
| 4 | Evaluation, Testing, and Optimization | 17% | ~10 | Độ phủ eval, bias của LLM-as-judge, thiết kế experiment, tìm nguyên nhân gốc từ trace, migration model |
| 5 | Governance, Safety, and Risk Management | 16% | ~10 | Guardrail, prompt injection, cổng human-in-the-loop, kiểm soát compliance, bias |
| 6 | Stakeholder Communication and Lifecycle Management | 7% | ~4 | SLA không giữ được, decision record, gói handoff |
| 7 | Developer Productivity and Operational Enablement | 8% | ~5 | Đóng gói workflow Claude Code, permission mode, trách nhiệm với code do AI sinh ra |

\* ~Số câu tính trên 60 câu tính điểm, làm tròn.

**Điểm mấu chốt (bản mới):** domain Stakeholder tụt mạnh **14% → 7%**,
trong khi Integration lên **19% → 21%** và Governance lên **14% → 16%**.
Phần phi kỹ thuật (D5 + D6) còn **23%** (bản cũ 28%); ba domain mới so với
CCAR-F (D4 + D5 + D6) còn **40%** (bản cũ 44%). Objectives bản mới cụ thể
hơn và yêu cầu **suy luận từ artifact**: log, trace, config, diagram, kết quả
eval — không chỉ hỏi lý thuyết. Bản mới cũng kỳ vọng thí sinh làm việc hàng
ngày với Claude Developer Platform, Agent Skills, Claude Code, Agent SDK, MCP
và Claude Managed Agents, và phân biệt được API của Anthropic với Amazon
Bedrock, Google Vertex AI và Microsoft Foundry.

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
  đúng các câu scenario. **Bản mới** càng nặng phần này: luyện đọc artifact
  thật (log, trace, eval table, config) và hỏi "cái gì hỏng trước, vì sao".

## Tài liệu public cho CCAR-P

| Nguồn | Nội dung |
|---|---|
| [girishr/ClaudeCertifiedArchitect-Professional-Prep](https://github.com/girishr/ClaudeCertifiedArchitect-Professional-Prep) | 5 module cô đọng từ khóa chính thức, 75 câu scenario, 8 hands-on lab, RAG chunking/indexing, web hub luyện đề — dùng được cho cả 2 bản |
| [ravnhq/claude-certified-architect](https://github.com/ravnhq/claude-certified-architect) | **Bản cũ:** study guide + practice exam 63 câu cho track Professional |
| [MoBRUEC — CCAR-P guide](https://github.com/mobruec/mobruec/blob/HEAD/claude-certified-architect/readme.md) | **Bản cũ:** guide theo đúng exam guide v1.0, cảnh báo về các bản tóm tắt bịa số liệu |
| [claudeexpert.avinashai.com — CCAR-P Study Guide](https://claudeexpert.avinashai.com/00_exam_scope_and_study_plan.html) | Study plan + câu hỏi practice tự viết (không phải đề thật), map scope theo exam guide |
| [Practica Cert Prep — CCAR-P](https://certprep.practica.asia/ccar-p) | **Bản mới v1.1:** miễn phí, song ngữ Anh–Việt, 140 câu hỏi theo 7 domain bản mới + mock 70 câu tính giờ |

## Kế hoạch gợi ý (sau khi có CCAR-F)

- **Giai đoạn 1:** Học 5-course Professional prep path (~12h). Đối chiếu từng
  module với 7 domain trong bảng trên — nhớ chọn bảng đúng với ngày thi của
  mình (bản cũ hay bản mới).
- **Giai đoạn 2:** Học sâu 3 domain mới so với CCAR-F (D4 evals, D5 governance,
  D6 stakeholder) — đây là **44% đề thi bản cũ / 40% đề thi bản mới**.
- **Giai đoạn 3:** Làm 75 câu scenario của girishr + mock exam theo đúng bản
  mình thi: **mock 63 câu của ravnhq** nếu thi bản cũ, **mock 70 câu trong
  120 phút** (Practica) nếu thi bản mới. Tự chấm theo domain, yếu domain nào
  thì quay lại học domain đó.

## Liên hệ với các chứng chỉ khác

- **Lộ trình khuyên dùng:** CCAR-F → (kinh nghiệm triển khai) → CCAR-P.
  Thi CCAR-P ngay sau CCAR-F mà chưa từng vận hành hệ thống production thì
  phần scenario về incident/SLA/handoff sẽ rất khó.
- CCDV-F giúp phần Integration (D3) của CCAR-P nếu đã học kỹ về API và MCP.
