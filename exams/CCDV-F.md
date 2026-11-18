# CCDV-F — Claude Certified Developer: Foundations

> Nguồn: Anthropic CCDV-F Exam Guide v1.0 (hiệu lực 07/2026). Kiểm tra lại
> exam guide trước khi đăng ký — Anthropic ghi rõ nội dung có thể thay đổi.
>
> ⚠️ **Lưu ý quan trọng:** Pearson VUE thông báo exam CCDV-F sẽ có nội dung
> cập nhật từ **07/12/2026**, domain weights có thể thay đổi. Nếu thi sau ngày
> này, đọc exam guide bản mới nhất trước khi ôn.

## Exam facts

| | |
|---|---|
| Mã thi | CCDV-F |
| Đối tượng | Engineer build, tích hợp, bảo mật và tối ưu ứng dụng production trên Claude API |
| Số câu | 53 (trắc nghiệm + trả lời nhiều đáp án) |
| Thời gian | 120 phút |
| Phí | $125 |
| Đậu | 720 / 1.000 (thang điểm, không phải 72% số câu) |
| Hiệu lực | 12 tháng, gia hạn miễn phí nếu đúng hạn |
| Điều kiện đăng ký | Email công ty thuộc Claude Partner Network |

## Tám domain và trọng số

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

**Điểm mấu chốt:** một mình domain **Applications and Integration (33.1%)** đã
bằng 1/3 đề thi — nặng hơn Claude Code + Eval cộng lại gấp 3 lần. Top 3 domain
(Applications 33.1% + Model Selection 16.8% + Agents 14.7%) = ~65% đề thi.
Guide này chi tiết tới từng **skill** (25 skill có trọng số riêng tới 1 chữ số
thập phân) — đây là blueprint chi tiết nhất trong 4 chứng chỉ.

## Học gì

- **Anthropic Academy (miễn phí):** *Building with the Claude API*, *Claude Code
  in Action*, *Introduction to MCP*, *MCP: Advanced Topics*, *Introduction to
  agent skills*, *Introduction to subagents*.
- **Notebook này:** chương 1 (loop & harness), 2 (patterns), 3 (orchestrator),
  4 (tools & MCP), 6 (context), 6B (RAG), 9 (guardrails), 10 (evals).
  Riêng domain Applications & Integration cần thêm kiến thức software
  engineering căn bản (REST, async, JSON schema) — notebook không cover phần
  này, học từ docs của Claude API.
- **Thực hành code thật:** viết một app nhỏ gọi Messages API + tool use +
  streaming, rồi viết MCP server tối thiểu — đề thi hỏi scenario code rất nhiều.

## Tài liệu public cho CCDV-F

| Nguồn | Nội dung |
|---|---|
| [natsh/claude-developer-foundations-prep](https://github.com/natsh/claude-developer-foundations-prep) | Tài liệu từ khóa prep Skilljar (5 module); quiz 100 câu theo domain; mock exam 53 câu (đậu khi ≥ 40/53); kèm 2 Claude Code skill chạy thi thử có chấm điểm |
| [datacertlab/DataCertLab-Notes](https://github.com/datacertlab/datacertlab-notes) | Notes theo từng domain, đối chiếu kỹ với exam guide v1.0, ghi rõ chỗ guide và docs hiện tại khác nhau |
| [andymdh/claude_developer_foundations](https://github.com/andymdh/claude_developer_foundations) | Study guide tĩnh theo domain, kèm review aids và practice questions |
| [cemendes/anthropic-claude-certifications](https://github.com/cemendes/anthropic-claude-certifications) | Track CCDV-F với domain guides, cheat sheets, slide deck. ⚠️ Blueprint trong README repo này khác với exam guide chính thức — chỉ dùng phần guides/cheat sheets, đối chiếu domain weights với guide gốc |

## Kế hoạch gợi ý (2–3 tuần)

- **Tuần 1:** *Building with the Claude API* + viết app nhỏ (Messages API,
  tool use, streaming, token counting). Học domain Applications & Integration
  trước vì nó chiếm 1/3 đề.
- **Tuần 2:** *Intro to MCP* + *MCP Advanced* + viết MCP server tối thiểu.
  Học Agents & Workflows (notebook chương 1–3) và Model Selection (caching,
  cost).
- **Tuần 3:** Làm quiz 100 câu của natsh theo module, sau đó làm mock 53 câu
  (mục tiêu ≥ 40/53). Ôn Security (injection, hooks) và Prompt/Context
  Engineering.

## Liên hệ với các chứng chỉ khác

- CCDV-F và CCAR-F **chồng chéo mạnh** ở agents, tools/MCP, context, evals —
  ôn một cái thì cái còn lại nhẹ đi rất nhiều. Khác biệt lớn nhất: CCDV-F
  nặng về **code và tích hợp ứng dụng** (33.1%), CCAR-F nặng về **thiết kế
  kiến trúc và Claude Code** (27% + 20%).
- Nếu đã có CCAR-F, CCDV-F chủ yếu cần bổ sung domain Applications &
  Integration và kỹ năng code API thực tế.
