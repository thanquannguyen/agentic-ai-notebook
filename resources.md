# Resources — tài liệu chọn lọc

> Quy tắc: chỉ link, không copy nội dung. Đọc tài liệu chính thức của Anthropic
> trước, repo cộng đồng chỉ để tham khảo và luyện đề. Kiểm tra lần cuối 19/11/2026;
> link Practica Cert Prep thêm ngày 24/11/2026.
> Chi tiết từng chứng chỉ (domain, trọng số, kế hoạch học) xem thư mục `exams/`.

## Chính thức (đọc trước)

| Nguồn | Dùng cho |
|---|---|
| [Building Effective Agents — Anthropic Engineering](https://www.anthropic.com/engineering/building-effective-agents) | Taxonomy chuẩn: augmented LLM, 5 workflow, agent loop. Nền tảng của notebook. |
| [How we built our multi-agent research system — Anthropic Engineering](https://www.anthropic.com/engineering/multi-agent-research-system) | Orchestrator–workers trong thực tế, bài học delegation, số liệu 90.2%. |
| [Claude Code docs](https://code.claude.com/docs) | Skills, subagents, hooks, settings, sandbox — nguồn chính xác nhất cho CCAR-F D3. |
| [MCP docs](https://modelcontextprotocol.io) | Spec đầy đủ: tools, resources, prompts, transports, sampling. |
| [Anthropic Academy (Skilljar)](https://anthropic.skilljar.com) | Khóa miễn phí: Claude 101, AI Fluency, Claude Code 101, Claude Code in Action, Building with the Claude API, Intro to MCP, MCP Advanced, Intro to agent skills, Intro to subagents, 5-course Professional prep path. |
| Exam guides v1.0 (07/2026) | Syllabus chính thức + câu hỏi mẫu cho cả 4 chứng chỉ. Tải từ Partner Academy certifications page (clau.de/CCAF). |

## Repo chính thức (hands-on)

| Repo | Nội dung | Dùng cho |
|---|---|---|
| [anthropics/claude-cookbooks](https://github.com/anthropics/claude-cookbooks) | Notebook/recipe chính thức: agent SDK, patterns, tool_use, tool evaluation, evals, observability, skills, managed_agents, RAG recipes | Hands-on theo từng domain, đặc biệt RAG + evals |

## Luyện thi — tất cả 4 chứng chỉ

| Repo | Nội dung | Dùng cho |
|---|---|---|
| [ravnhq/claude-certified-architect](https://github.com/ravnhq/claude-certified-architect) | Study guide + practice exam cho cả 4 chứng chỉ (EN/ES/PT), preflight checklist; riêng Associate có ngân hàng 770 câu | Ôn thi trực tiếp, làm đề thử |
| [parmar-m/claude-architect-certification-prep](https://github.com/parmar-m/claude-architect-certification-prep) | Study notebook + bảng tổng hợp các repo prep cộng đồng | Tham khảo thêm, đối chiếu nguồn |
| [Practica Cert Prep — tất cả 4 chứng chỉ](https://certprep.practica.asia/certifications) | Miễn phí, song ngữ Anh–Việt, không cần đăng nhập; mỗi chứng chỉ có overview, knowledge theo domain, cheatsheet, mock tính giờ — CCAR-F 287 câu, CCAR-P 140 câu, CCAO-F 100 câu, CCDV-F 101 câu (câu hỏi của họ, không phải của repo này) | Ôn thi trực tiếp, làm đề thử theo domain |

## Luyện thi — CCAR-F (Architect Foundations)

| Repo | Nội dung |
|---|---|
| [timothywarner-org/claude-architect](https://github.com/timothywarner-org/claude-architect) | O'Reilly live training: 5 file theo 5 domain, practice scenarios, ngân hàng 60 câu hỏi |
| [Practica — CCAR-F](https://certprep.practica.asia/ccar-f) | 67 nguyên tắc theo 5 domain + 287 câu hỏi (tiếng Anh, có dịch tiếng Việt) + mock tính giờ; miễn phí, không cần đăng nhập |

## Luyện thi — CCAR-P (Architect Professional)

| Repo | Nội dung |
|---|---|
| [girishr/ClaudeCertifiedArchitect-Professional-Prep](https://github.com/girishr/ClaudeCertifiedArchitect-Professional-Prep) | 5 module cô đọng từ khóa chính thức, 75 câu scenario, 8 hands-on lab, RAG chunking/indexing |
| [MoBRUEC — CCAR-P guide](https://github.com/mobruec/mobruec/blob/HEAD/claude-certified-architect/readme.md) | Guide theo đúng exam guide v1.0, cảnh báo về các bản tóm tắt bịa số liệu |
| [claudeexpert.avinashai.com — CCAR-P Study Guide](https://claudeexpert.avinashai.com/00_exam_scope_and_study_plan.html) | Study plan + câu hỏi practice tự viết, map scope theo exam guide |
| [Practica — CCAR-P](https://certprep.practica.asia/ccar-p) | 39 nguyên tắc theo 7 domain + 140 câu hỏi + mock tính giờ (70 câu/120 phút theo guide v1.1 từ 07/12/2026); miễn phí, không cần đăng nhập |

## Luyện thi — CCDV-F (Developer Foundations)

| Repo | Nội dung |
|---|---|
| [natsh/claude-developer-foundations-prep](https://github.com/natsh/claude-developer-foundations-prep) | Tài liệu từ khóa prep Skilljar (5 module); quiz 100 câu theo domain; mock exam 53 câu (đậu khi ≥ 40/53); kèm 2 Claude Code skill chạy thi thử có chấm điểm |
| [datacertlab/DataCertLab-Notes](https://github.com/datacertlab/datacertlab-notes) | Notes theo từng domain CCDV-F, đối chiếu kỹ với exam guide v1.0 |
| [andymdh/claude_developer_foundations](https://github.com/andymdh/claude_developer_foundations) | Study guide tĩnh theo domain, kèm review aids và practice questions |
| [Practica — CCDV-F](https://certprep.practica.asia/ccdv-f) | 24 nguyên tắc theo 8 domain + 101 câu hỏi + mock tính giờ; lưu ý guide v1.1 từ 07/12/2026: 70 câu (60 câu tính điểm), 8 domain cân bằng lại |

## Luyện thi — CCAO-F (Associate Foundations)

| Nguồn | Nội dung |
|---|---|
| [claude.termidy.com/ccao-f](https://claude.termidy.com/ccao-f/) | Community site: guide + ngân hàng 360 câu hỏi viết mới theo domain |
| [rubricedu.com — CCAO-F guide](https://www.rubricedu.com/certifications/ccao-f) | 30 objectives theo 7 domain, mỗi objective link tới bài học |
| [Practica — CCAO-F](https://certprep.practica.asia/ccao-f) | 21 nguyên tắc theo 6 domain + 100 câu hỏi + mock tính giờ; lưu ý guide v1.1 từ 07/12/2026: 70 câu (60 câu tính điểm), 6 domain |

## Repo thực hành (cho intern + hiểu harness)

| Repo | Nội dung | Dùng cho |
|---|---|---|
| [luongnv89/claude-howto](https://github.com/luongnv89/claude-howto) (MIT) | 10 module hướng dẫn Claude Code kèm template: slash commands, memory, skills, subagents, MCP, hooks, plugins (11–13h) | Intern học Claude Code hands-on |
| [shareAI-lab/learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) (MIT) | 20 bài học xây harness kiểu Claude Code từ đầu bằng Python: loop, permissions, hooks, subagents, compaction, memory, MCP | Hiểu harness ở tầng code |
| [traversaal-ai/agent-engineering-leidos](https://github.com/traversaal-ai/agent-engineering-leidos) | Module 5: skills/subagents/multi-agent — subagent vs agent team, quy tắc 9/10, chọn model | Khi review: khi nào dùng subagent, khi nào cần agent team |
