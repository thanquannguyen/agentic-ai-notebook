# Resources — tài liệu chọn lọc

> Quy tắc: chỉ link, không copy nội dung. Đọc tài liệu chính thức của Anthropic
> trước, repo cộng đồng chỉ để tham khảo và luyện đề. Kiểm tra lần cuối 19/11/2026.

## Chính thức (đọc trước)

| Nguồn | Dùng cho |
|---|---|
| [Building Effective Agents — Anthropic Engineering](https://www.anthropic.com/engineering/building-effective-agents) | Taxonomy chuẩn: augmented LLM, 5 workflow, agent loop. Nền tảng của notebook. |
| [How we built our multi-agent research system — Anthropic Engineering](https://www.anthropic.com/engineering/multi-agent-research-system) | Orchestrator–workers trong thực tế, bài học delegation, số liệu 90.2%. |
| [Claude Code docs](https://code.claude.com/docs) | Skills, subagents, hooks, settings, sandbox — nguồn chính xác nhất cho D3. |
| [MCP docs](https://modelcontextprotocol.io) | Spec đầy đủ: tools, resources, prompts, transports, sampling. |
| [Anthropic Academy (Skilljar)](https://anthropic.skilljar.com) | Khóa miễn phí: Claude Code 101, Claude Code in Action, Building with the Claude API, Intro to MCP, MCP Advanced, Intro to agent skills, Intro to subagents. |
| CCAR-F Exam Guide v1.0 (07/2026) | Syllabus chính thức + câu hỏi mẫu. Tải từ Partner Academy certifications page (clau.de/CCAF). |

## Repo chính thức (hands-on)

| Repo | Nội dung | Dùng cho |
|---|---|---|
| [anthropics/claude-cookbooks](https://github.com/anthropics/claude-cookbooks) | Notebook/recipe chính thức: agent SDK, patterns, tool_use, tool evaluation, evals, observability, skills, managed_agents, RAG recipes | Hands-on theo từng domain, đặc biệt RAG + evals |

## Repo luyện thi CCAR-F / CCAR-P

| Repo | Nội dung | Dùng cho |
|---|---|---|
| [ravnhq/claude-certified-architect](https://github.com/ravnhq/claude-certified-architect) | Study guide + practice exam cho cả 4 chứng chỉ (EN/ES/PT), preflight checklist | Ôn thi trực tiếp, làm đề thử |
| [timothywarner-org/claude-architect](https://github.com/timothywarner-org/claude-architect) | O'Reilly live training: 5 file theo 5 domain CCAR-F, practice scenarios, ngân hàng 60 câu hỏi | Ôn theo domain + luyện đề |
| [girishr/ClaudeCertifiedArchitect-Professional-Prep](https://github.com/girishr/ClaudeCertifiedArchitect-Professional-Prep) | CCAR-P prep: 5 module cô đọng, 75 câu scenario, 8 hands-on lab, RAG chunking/indexing | Sau CCAR-F lên CCAR-P; phần RAG sâu |
| [parmar-m/claude-architect-certification-prep](https://github.com/parmar-m/claude-architect-certification-prep) | Study notebook + bảng tổng hợp các repo prep cộng đồng | Tham khảo thêm, đối chiếu nguồn |
| [Stephen-Data-Engineer-Public/Claude-Certified-Architect-exam-prep](https://github.com/Stephen-Data-Engineer-Public/Claude-Certified-Architect-exam-prep) | Kế hoạch học 90 giờ theo phase Beginner → Advanced | Người cần lộ trình chi tiết từng giờ |

## Repo thực hành (cho intern + hiểu harness)

| Repo | Nội dung | Dùng cho |
|---|---|---|
| [luongnv89/claude-howto](https://github.com/luongnv89/claude-howto) (MIT) | 10 module hướng dẫn Claude Code kèm template: slash commands, memory, skills, subagents, MCP, hooks, plugins (11–13h) | Intern học Claude Code hands-on |
| [shareAI-lab/learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) (MIT) | 20 bài học xây harness kiểu Claude Code từ đầu bằng Python: loop, permissions, hooks, subagents, compaction, memory, MCP | Hiểu harness ở tầng code |
| [traversaal-ai/agent-engineering-leidos](https://github.com/traversaal-ai/agent-engineering-leidos) | Module 5: skills/subagents/multi-agent — subagent vs agent team, quy tắc 9/10, chọn model | Khi review: khi nào dùng subagent, khi nào cần agent team |
