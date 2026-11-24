# CCDV-F — Claude Certified Developer: Foundations

> Nguồn: Anthropic CCDV-F Exam Guide v1.0 (hiệu lực 07/2026) + Exam Guide
> **v1.1** (thi từ 07/12/2026). Kiểm tra lại exam guide trước khi đăng ký —
> Anthropic ghi rõ nội dung có thể thay đổi.
>
> ⚠️ **Đề thi đổi từ 07/12/2026 — file này giữ cả 2 bản.** Phiên bản đề tùy
> thuộc **ngày thi**, không tùy ngày đăng ký: thi tới 06/12/2026 thì theo bản
> cũ (53 câu), thi từ 07/12/2026 thì theo bản mới v1.1 (70 câu). Nếu có thể
> thi trước ngày đổi thì ôn theo bản cũ. Chi tiết bản mới theo Practica Cert
> Prep (đối chiếu exam guide v1.1 chính thức ngày 21/11/2026).

## Exam facts

| | |
|---|---|
| Mã thi | CCDV-F |
| Đối tượng | Engineer build, tích hợp, bảo mật và tối ưu ứng dụng production trên Claude API |
| Số câu | **53** (bản cũ, thi tới 06/12/2026) · **70, trong đó 60 tính điểm + 10 câu thử không tính điểm** (bản mới v1.1, từ 07/12/2026) |
| Thời gian | 120 phút (cả 2 bản) |
| Phí | $125 |
| Đậu | 720 / 1.000 (thang điểm, không phải 72% số câu) |
| Hiệu lực | 12 tháng, gia hạn miễn phí nếu đúng hạn |
| Điều kiện đăng ký | Email công ty thuộc Claude Partner Network |

## Tám domain và trọng số — 2 phiên bản

### Bản cũ — thi tới 06/12/2026 (53 câu)

| # | Domain | Trọng số | ~Số câu | Thi cái gì |
|---|---|---|---|---|
| 1 | Agents and Workflows | 14.7% | ~8 | Agent architecture, khi nào dùng workflow vs agent, manager/supervisor hierarchies, subagents, patterns và frameworks (Agent SDK, LangGraph, PydanticAI, Strands) |
| 2 | **Applications and Integration** | **33.1%** | ~18 | Requirements, lifecycle, API mechanics, software engineering foundations (REST, JSON, async, version control, SDLC), application design, configuration |
| 3 | Claude Code | 3.1% | ~2 | Vận hành Claude Code: rules, skills, commands, sessions, headless mode, CLAUDE.md |
| 4 | Eval, Testing, and Debugging | 2.6% | ~1 | Error handling, recovery, debugging, trace failure analysis |
| 5 | Model Selection and Optimisation | 16.8% | ~9 | LLM fundamentals, trade-off giữa các model, cost và token management, prompt caching |
| 6 | Prompt and Context Engineering | 11.0% | ~6 | Context management, prompting (XML, structured), output handling, context pruning |
| 7 | Security and Safety | 8.1% | ~4 | Prompt injection, guardrails, hooks, identity và secrets |
| 8 | Tools and MCPs | 10.6% | ~6 | Tool implementation, MCP server development, schemas, error handling |

**Điểm mấu chốt (bản cũ):** một mình domain **Applications and Integration
(33.1%)** đã bằng 1/3 đề thi — nặng hơn Claude Code + Eval cộng lại gấp 3
lần. Top 3 domain (Applications 33.1% + Model Selection 16.8% + Agents
14.7%) = ~65% đề thi. Guide này chi tiết tới từng **skill** (25 skill có
trọng số riêng tới 1 chữ số thập phân) — đây là blueprint chi tiết nhất trong
4 chứng chỉ.

### Bản mới v1.1 — thi từ 07/12/2026 (70 câu, 60 tính điểm)

| # | Domain | Trọng số | ~Số câu* | Thi cái gì |
|---|---|---|---|---|
| 1 | Agents and Workflows | 17% | ~10 | Workflow vs agent, định nghĩa Agent SDK, harness và hooks, chẩn đoán agent trace |
| 2 | **Applications and Integration** | **20%** | ~12 | Messages API mechanics, surface behaviour, configuration và SDLC, xử lý lỗi theo từng loại lỗi |
| 3 | Claude Code | 8% | ~5 | Vận hành Claude Code trên mọi bề mặt (CLI, desktop, IDE, web, mobile), thứ bậc CLAUDE.md, permission modes, Skills, plugins, hooks, subagents |
| 4 | Eval, Testing, and Debugging | 10% | ~6 | Golden set, LLM-as-judge đã calibrate, chẩn đoán failure mode |
| 5 | Model Selection and Optimization | 12% | ~7 | Token và sampling, adaptive thinking/effort, model tier, cost và caching |
| 6 | Prompt and Context Engineering | 15% | ~9 | Long session, sửa prompt, structured output, grounding và citations |
| 7 | Security and Safety | 8% | ~5 | Prompt injection, guardrail xác định (deterministic), least privilege, quản lý API key |
| 8 | Tools and MCP | 10% | ~6 | Thiết kế tool, MCP server và transport, chọn giữa tool / Skill / MCP |

\* ~Số câu tính trên 60 câu tính điểm, làm tròn.

**Điểm mấu chốt (bản mới):** đề thi cân bằng lại mạnh — Applications &
Integration tụt từ **33.1% → 20%**, trong khi Claude Code tăng **3.1% →
8%** và Eval tăng **2.6% → 10%**. Top 3 domain mới (Applications 20% +
Agents 17% + Prompt/Context 15%) = 52% đề thi. Bản mới kỳ vọng thí sinh dùng
thường xuyên Messages API, Agent SDK và Claude Managed Agents, Claude Code
trên mọi bề mặt, cộng Git và CI (ví dụ GitHub Actions) — không còn là kỳ thi
nặng software engineering tổng quát nữa.

## Học gì

- **Anthropic Academy (miễn phí):** *Building with the Claude API*, *Claude Code
  in Action*, *Introduction to MCP*, *MCP: Advanced Topics*, *Introduction to
  agent skills*, *Introduction to subagents*.
- **Notebook này:** chương 1 (loop & harness), 2 (patterns), 3 (orchestrator),
  4 (tools & MCP), 6 (context), 6B (RAG), 9 (guardrails), 10 (evals).
  Riêng domain Applications & Integration cần thêm kiến thức software
  engineering căn bản (REST, async, JSON schema) — notebook không cover phần
  này, học từ docs của Claude API. Phần này nặng ở bản cũ (33.1%), nhẹ hơn ở
  bản mới (20%).
- **Thực hành code thật:** viết một app nhỏ gọi Messages API + tool use +
  streaming, rồi viết MCP server tối thiểu — đề thi hỏi scenario code rất nhiều.
  Bản mới hỏi nhiều hơn về Claude Code trên mọi bề mặt và về eval (golden set,
  calibrate LLM-as-judge).

## Tài liệu public cho CCDV-F

| Nguồn | Nội dung |
|---|---|
| [natsh/claude-developer-foundations-prep](https://github.com/natsh/claude-developer-foundations-prep) | **Bản cũ:** tài liệu từ khóa prep Skilljar (5 module); quiz 100 câu theo domain; mock exam 53 câu (đậu khi ≥ 40/53); kèm 2 Claude Code skill chạy thi thử có chấm điểm |
| [datacertlab/DataCertLab-Notes](https://github.com/datacertlab/datacertlab-notes) | **Bản cũ:** notes theo từng domain, đối chiếu kỹ với exam guide v1.0, ghi rõ chỗ guide và docs hiện tại khác nhau |
| [andymdh/claude_developer_foundations](https://github.com/andymdh/claude_developer_foundations) | Study guide tĩnh theo domain, kèm review aids và practice questions |
| [cemendes/anthropic-claude-certifications](https://github.com/cemendes/anthropic-claude-certifications) | Track CCDV-F với domain guides, cheat sheets, slide deck. ⚠️ Blueprint trong README repo này khác với exam guide chính thức — chỉ dùng phần guides/cheat sheets, đối chiếu domain weights với guide gốc |
| [Practica Cert Prep — CCDV-F](https://certprep.practica.asia/ccdv-f) | **Bản mới v1.1:** miễn phí, song ngữ Anh–Việt, 101 câu hỏi theo 8 domain bản mới + mock 70 câu tính giờ |

## Kế hoạch gợi ý (2–3 tuần)

- **Tuần 1:** *Building with the Claude API* + viết app nhỏ (Messages API,
  tool use, streaming, token counting). **Bản cũ:** học domain Applications &
  Integration trước vì nó chiếm 1/3 đề. **Bản mới:** học Agents &
  Workflows + Applications + Prompt/Context trước (17% + 20% + 15% = 52% đề).
- **Tuần 2:** *Intro to MCP* + *MCP Advanced* + viết MCP server tối thiểu.
  Học Agents & Workflows (notebook chương 1–3) và Model Selection (caching,
  cost). **Bản mới:** dành thêm thời gian cho Claude Code (8%) và Eval (10%)
  — hai domain tăng mạnh nhất.
- **Tuần 3:** Làm quiz 100 câu của natsh theo module, sau đó làm mock exam
  theo đúng bản mình thi: **mock 53 câu (mục tiêu ≥ 40/53)** nếu thi bản cũ,
  **mock 70 câu trong 120 phút** (Practica) nếu thi bản mới. Ôn Security
  (injection, hooks) và Prompt/Context Engineering.

## Liên hệ với các chứng chỉ khác

- CCDV-F và CCAR-F **chồng chéo mạnh** ở agents, tools/MCP, context, evals —
  ôn một cái thì cái còn lại nhẹ đi rất nhiều. Khác biệt lớn nhất: **bản cũ**
  CCDV-F nặng về **code và tích hợp ứng dụng** (33.1%), CCAR-F nặng về
  **thiết kế kiến trúc và Claude Code** (27% + 20%). Ở **bản mới**, CCDV-F
  cân bằng hơn (Applications chỉ còn 20%) nên khoảng cách với CCAR-F thu hẹp.
- Nếu đã có CCAR-F, CCDV-F chủ yếu cần bổ sung domain Applications &
  Integration và kỹ năng code API thực tế.
