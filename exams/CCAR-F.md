# CCAR-F — Claude Certified Architect: Foundations

> Nguồn: Anthropic CCAR-F Exam Guide v1.0 (hiệu lực 07/2026). Kiểm tra lại
> exam guide trước khi đăng ký — Anthropic ghi rõ nội dung có thể thay đổi.
>
> Đây là chứng chỉ **mục tiêu chính** của repo này — notebook được viết để
> cover toàn bộ 5 domain của nó.

## Exam facts

| | |
|---|---|
| Mã thi | CCAR-F |
| Đối tượng | Solution architect làm việc với Claude Code, MCP và agents |
| Số câu | 60 (trắc nghiệm + trả lời nhiều đáp án, theo tình huống production) |
| Thời gian | 120 phút |
| Phí | $125 |
| Đậu | 720 / 1.000 (thang điểm, không phải 72% số câu) |
| Hiệu lực | 12 tháng, gia hạn miễn phí nếu đúng hạn |
| Điều kiện đăng ký | Email công ty thuộc Claude Partner Network |

## Năm domain và trọng số

| # | Domain | Trọng số | ~Số câu | Thi cái gì | Chương notebook |
|---|---|---|---|---|---|
| 1 | **Agentic Architecture & Orchestration** | **27%** | ~16 | Agent loop, Agent SDK, multi-agent orchestration (hub-and-spoke), lifecycle hooks, task decomposition, session management | Ch. 1, 2, 3 |
| 2 | Tool Design & MCP Integration | 18% | ~11 | MCP primitives (tools, resources, prompts), mô tả tool, structured error responses, transports, sampling/notifications, built-in tools | Ch. 4 |
| 3 | Claude Code Configuration & Workflows | 20% | ~12 | CLAUDE.md hierarchy, Agent Skills (SKILL.md), custom slash commands, plan mode, iterative refinement, CI/CD & batch runs | Ch. 5, 11 |
| 4 | Prompt Engineering & Structured Output | 20% | ~12 | Tiêu chí thành công rõ ràng, few-shot, tool_use, JSON-schema, validation-and-retry loops, multi-pass review | Ch. 5, 10 |
| 5 | Context Management & Reliability | 15% | ~9 | Long context & compaction, progressive summarisation, prompt caching, token budgeting, multi-agent handoffs, error propagation, escalation, human review, provenance | Ch. 6, 6B, 7, 8, 9 |

**Điểm mấu chốt:** đề thi theo **tình huống production** (agent loop hỏng, tool
schema sai, hệ thống quá tải) — hỏi quyết định kiến trúc đúng, không hỏi thuộc
lòng. Câu hỏi về anti-pattern thường nặng điểm hơn câu hỏi kiến thức thuần.
Mỗi kỳ thi rút 4 trong 6 production scenario có sẵn.

**Lưu ý về RAG:** RAG không có domain riêng — nó nằm trong D1 (retrieval của
augmented LLM) và D5 (context strategies). Xem chương 6B của notebook.

## Học gì

- **Anthropic Academy (miễn phí):** *Claude Code 101*, *Claude Code in Action*,
  *Building with the Claude API*, *Introduction to MCP*, *MCP: Advanced Topics*,
  *Introduction to agent skills*, *Introduction to subagents*.
- **Notebook này:** đọc toàn bộ 13 chương — mỗi chương đều map tới một domain
  trong bảng trên. Làm 4 bài `practice/` để biến lý thuyết thành kỹ năng.
- **Đọc gốc:** *Building Effective Agents* và *How we built our multi-agent
  research system* (link trong `resources.md`).

## Tài liệu public cho CCAR-F

| Nguồn | Nội dung |
|---|---|
| [ravnhq/claude-certified-architect](https://github.com/ravnhq/claude-certified-architect) | Study guide + practice exam (EN/ES/PT), preflight checklist |
| [timothywarner-org/claude-architect](https://github.com/timothywarner-org/claude-architect) | O'Reilly live training: 5 file theo 5 domain, practice scenarios, ngân hàng 60 câu hỏi |
| [parmar-m/claude-architect-certification-prep](https://github.com/parmar-m/claude-architect-certification-prep) | Study notebook + bảng tổng hợp các repo prep cộng đồng |
| [luongnv89/claude-howto](https://github.com/luongnv89/claude-howto) (MIT) | 10 module Claude Code kèm template (skills, subagents, MCP, hooks, plugins) — thực hành cho D3 |

## Kế hoạch gợi ý (3 tuần — xem chi tiết ở chương 13 của notebook)

- **Tuần 1 — Nền tảng (D1 + D4):** đọc *Building Effective Agents* + bài
  multi-agent research. Làm lại ví dụ chương 1–2 bằng tay.
- **Tuần 2 — Công cụ (D2 + D3):** học các khóa Academy; thực hành: viết 1 skill
  + 1 slash command + 1 MCP server nhỏ.
- **Tuần 3 — Vận hành (D5 + tổng ôn):** đọc *Building with the Claude API*.
  Làm câu hỏi mẫu trong exam guide, tự chấm theo domain. Ôn anti-pattern.

## Liên hệ với các chứng chỉ khác

- CCAR-F là **nền tảng** cho CCAR-P: 3 domain của CCAR-P (Evaluation,
  Governance, Stakeholder) không có trong CCAR-F — muốn lên Professional thì
  học thêm 3 domain đó + kinh nghiệm triển khai thật.
- Với CCDV-F: chồng chéo mạnh ở agents, tools/MCP, context, evals. CCAR-F
  nặng kiến trúc + Claude Code; CCDV-F nặng code + tích hợp ứng dụng.
