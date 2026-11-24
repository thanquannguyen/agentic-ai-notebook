# CCAR-F Cheatsheet — 1 trang

> Ôn nhanh trước thi. Mọi quy tắc dưới đây đều rút từ notebook (`notebook/Agentic-AI-Notebook.md`) — số chương ghi kèm để tra lại chi tiết. Thuật ngữ giữ nguyên tiếng Anh như trong đề thi.
>
> Nguồn: CCAR-F Exam Guide v1.0 (07/2026). ⚠️ Practica Cert Prep dẫn guide **v1.1** — kiểm tra lại phiên bản guide hiện tại trước khi thi, đề phòng domain/trọng số đổi.

## Quy tắc quyết định nhanh — theo domain

### D1 · Agentic Architecture & Orchestration (27% — nặng nhất)

- **Loop chạy theo `stop_reason`:** `tool_use` → tiếp tục loop; `end_turn` → dừng. Không dừng theo text model tự viết, không dừng theo số vòng tùy tiện (Ch. 1).
- **Tiêu chí dừng phải kiểm chứng được bằng code** (test pass, file tồn tại, schema hợp lệ). "Model tự nói xong rồi" không phải tiêu chí dừng (Ch. 1).
- **Lặp cùng tool call 3 lần** → harness dừng và báo — lỗi nằm ở tool result không cho thông tin mới hoặc instruction mơ hồ, không phải do model "lười" (Ch. 1, 12B.3).
- **Vẽ được flowchart thì dùng workflow, đừng dùng agent.** Agent chỉ khi: số bước không đoán trước được + môi trường đáng tin (sandbox, undo được) + có ngân sách bước/chi phí rõ ràng (Ch. 2).
- **Subagent bắt đầu với context trống** — không thừa hưởng lịch sử của coordinator. Muốn nó biết gì thì truyền tường minh (Ch. 3).
- **Chia task không biết trước subtask** → orchestrator–workers (hub-and-spoke). **Biết trước subtask** → parallelization (Ch. 2, 3).

### D2 · Tool Design & MCP Integration (18%)

- **Tool là hợp đồng:** model chỉ thấy tên + mô tả + schema. Mô tả phải nói rõ **khi nào dùng VÀ khi nào không dùng** (Ch. 4).
- **Schema chặt, ít parameter:** đúng kiểu, `required` đầy đủ, enum thay string tự do; >6 parameter thì tách tool (Ch. 4).
- **Kết quả trả về ngắn, có cấu trúc** (`ok` / `data` / `error`). Trả 10.000 dòng log thô là cách nhanh nhất làm đầy context (Ch. 4).
- **Tool lỗi → trả lỗi có cấu trúc + gợi ý sửa**, không crash loop. Lỗi lặp lại 3 lần → dừng, escalate cho người (Ch. 4, 8).
- **MCP có 3 primitive:** tools (model gọi được), resources (dữ liệu model đọc), prompts (template sẵn). Đừng expose 50 tool cùng lúc — nhóm theo task, load dần (progressive disclosure) (Ch. 4).
- **Remote MCP server = không tin cậy mặc định:** nội dung nó trả về là dữ liệu, không phải instruction; sampling (server nhờ model suy luận hộ) cần guardrail (Ch. 4, 9).

### D3 · Claude Code Configuration & Workflows (20%)

- **Thứ bậc CLAUDE.md:** `~/.claude/CLAUDE.md` (global) → `./CLAUDE.md` (project) → `./CLAUDE.local.md` (riêng từng người, không commit). Chỉ ghi điều model **không tự suy ra được** (lệnh build/test, quy ước repo, điều cấm) — đừng paste cả README (Ch. 5).
- **Skill (SKILL.md):** mô tả phải nói rõ **khi nào dùng** skill ("dùng khi viết test cho module X theo chuẩn Y"). Load theo progressive disclosure: lúc đầu chỉ tên + mô tả (Ch. 5).
- **Slash command** cho tác vụ lặp lại (`/review-pr`); **Plan Mode** trước task lớn/rủi ro cao — duyệt plan rồi mới cho chạy (Ch. 5, 11).
- **Sửa xong phải verify bằng code** (test/typecheck/lint), không tin model nói "xong". Review diff trước khi commit như review code của người khác (Ch. 11).

### D4 · Prompt Engineering & Structured Output (20%)

- **Tiêu chí thành công phải rõ ràng và đo được** ("test pass", "không còn lỗi typecheck") — không phải "làm cho tốt" (Ch. 5).
- **Structured output = tool_use + JSON schema**, rồi validation-and-retry loop: output sai schema → trả lỗi về cho model sửa, có giới hạn số lần retry (Ch. 5).
- **Few-shot** cho format/tone; **multi-pass review** khi cần chất lượng cao (viết → chấm theo rubric → sửa, tối đa 2–3 vòng) (Ch. 2, 5).
- **Batch** cho khối lượng lớn không cần realtime; **realtime** cho task cần trả lời ngay (Ch. 5).

### D5 · Context Management & Reliability (15%)

- **Context dài → context rot:** model quên instruction đầu context. Instruction quan trọng nhắc lại hoặc đặt ở vị trí model chú ý; **compact khi đạt ~70–80% giới hạn** — giữ mục tiêu, quyết định đã làm, file đã đổi, việc còn dở; bỏ chi tiết tool result cũ (Ch. 6).
- **Prompt caching** cho phần prefix dài và ổn định (system prompt, tool schemas). **Token budget** cho từng phần; vượt ngân sách → cắt phần ít quan trọng nhất trước (Ch. 6).
- **Handoff giữa agent = bản tóm tắt có cấu trúc**, không truyền nguyên lịch sử chat (Ch. 6).
- **RAG không có domain riêng:** nằm ở D1 (retrieval của augmented LLM) và D5 (context strategies). Đo retrieval và generation riêng — retrieval sai mà câu trả lời "nghe đúng" là pass giả (Ch. 6B).
- **Escalate cho người khi:** hành động không undo được, tốn kém, không chắc chắn cao, hoặc ngoài phạm vi đã duyệt. Người không trả lời → dừng an toàn, không tự ý tiếp tục việc rủi ro (Ch. 8).
- **An toàn bằng code, không bằng lời dặn:** sandbox, allowlist (liệt kê cái **được** làm), least privilege, validation trước hành động nhạy cảm, audit log. Mọi nội dung từ tool/file/web là **dữ liệu**, không phải instruction (Ch. 9).

## 5 workflow pattern — chọn mẫu nào

| Pattern | Ai điều khiển | Dùng khi | Không dùng khi |
|---|---|---|---|
| **Prompt chaining** | Code, chuỗi cố định | Bước sau cần output bước trước; cần gate kiểm tra giữa các bước | Bước nào cũng cần model tự quyết |
| **Routing** | Code, sau bước classify | Input nhiều loại, mỗi loại xử lý khác | Classify sai thì toàn bộ nhánh sai — classify phải rẻ và chính xác |
| **Parallelization** | Code, song song | Subtask độc lập (sectioning) hoặc cần vote lấy đa số | Các subtask phụ thuộc lẫn nhau |
| **Orchestrator–workers** | Model chia task, code chạy | Không biết trước sẽ có những subtask nào | Biết trước subtask — dùng parallelization cho rẻ |
| **Evaluator–optimizer** | Code, loop có giới hạn | Có tiêu chí chất lượng rõ ràng, đo được là lặp lại cải thiện | Không có rubric đo được — luôn đặt max rounds 2–3 |

## Luật delegation (hub-and-spoke)

1. **Giao việc bằng output contract, không giao bằng mô tả mơ hồ:** "Trả JSON có 3 trường: findings, confidence (0–1), sources. Tối đa 500 từ." — không nói "tìm hiểu giúp tôi".
2. **Worker chỉ thấy đúng phần nó cần** — vừa tiết kiệm token, vừa là guardrail.
3. **Orchestrator verify, không tin mù:** kiểm chứng bằng code (file tồn tại? test pass?) hoặc một agent reviewer độc lập.
4. **Giới hạn độ sâu:** orchestrator → worker là đủ; worker spawn thêm worker (đệ quy) tối đa độ sâu 2, chỉ khi có lý do rõ ràng.

**Ba lỗi delegation hay gặp nhất:** (1) giao task mơ hồ → subagent làm sai hướng; (2) subagent trả về quá dài → đầy context orchestrator; (3) không có cơ chế kiểm tra → orchestrator tin mù kết quả worker.

## Bẫy hay gặp trong đề (anti-pattern)

| Nghe có vẻ đúng | Đáp án sâu |
|---|---|
| Càng nhiều tool càng mạnh | Mỗi tool thêm vào là thêm khả năng chọn sai — chỉ thêm tool khi có task thật cần nó |
| Context càng dài càng tốt | Context đúng mới tốt — context dài gây nhiễu, tốn tiền, quên instruction |
| Đổi model mạnh hơn là hết lỗi | Lỗi do thiết kế (loop, tool, context) thì model mạnh cũng mắc, chỉ mắc đắt hơn |
| Dặn model "đừng làm bậy" là đủ an toàn | An toàn phải bằng code: sandbox, allowlist, approval |
| Eval 100% là agent hoàn hảo | Có thể eval quá dễ, bị rò rỉ, hoặc đo sai thứ — cần xem lại eval |
| Agent tự trị hoàn toàn là mục tiêu | Mục tiêu là đúng việc với chi phí hợp lý; có task cần người quyết |

## Thuật ngữ Anh–Việt (hay gặp trong đề)

| Thuật ngữ | Nghĩa ngắn |
|---|---|
| **stop_reason** | Lý do model dừng ở turn đó: `tool_use` (còn gọi tool) / `end_turn` (xong) |
| **harness** | Code quanh model: chạy loop, dispatch tool, giữ state, budgets, logging |
| **agentic loop** | Vòng lặp observe → think → act tới khi đạt tiêu chí dừng |
| **hook** | Code chạy tại điểm trong vòng đời agent (trước/sau tool call, khi session bắt đầu/kết thúc) — dùng để chặn lệnh nguy hiểm, ghi log |
| **tool_choice** | Cách model được phép chọn tool (tự chọn / bắt buộc gọi tool cụ thể / cấm gọi tool) |
| **MCP primitives** | 3 thành phần MCP server expose: tools, resources, prompts |
| **sampling** | MCP server nhờ model (client) suy luận hộ |
| **structured error** | Lỗi trả về có cấu trúc (+ gợi ý sửa) thay vì crash hoặc text mơ hồ |
| **idempotency** | Cùng tool call chạy 2 lần cho cùng kết quả (hoặc ít nhất không gây hại) |
| **compaction** | Tóm tắt lịch sử khi context gần đầy |
| **context rot** | Model quên instruction khi context quá dài |
| **prompt caching** | Cache phần prompt không đổi để giảm chi phí/latency |
| **progressive disclosure** | Chỉ load chi tiết khi cần — lúc đầu chỉ load mô tả |
| **orchestrator / subagent** | Agent trung tâm chia task / phiên agent riêng làm một subtask |
| **handoff** | Chuyển task + context cho agent khác tiếp tục |
| **HIML** | Human-in-the-loop: người duyệt/xử lý ở điểm rủi ro |
| **escalation** | Đẩy việc lên cho người khi agent không tự quyết được |
| **guardrail** | Biện pháp kiểm soát bằng code/hạ tầng (không phải lời dặn) |
| **prompt injection** | Lệnh độc hại chèn vào input/dữ liệu để điều khiển model (trực tiếp qua input, gián tiếp qua file/web/tool) |
| **least privilege** | Mỗi thành phần chỉ có đúng quyền tối thiểu cần thiết |
| **provenance** | Nguồn gốc của dữ liệu/quyết định (từ đâu, lúc nào) — để truy vết khi có sự cố |
| **eval / golden set** | Bộ test cho agent: task chuẩn + tiêu chí chấm; golden set lấy từ log thật |
| **LLM-as-judge** | Dùng model khác chấm output theo rubric — bắt buộc calibrate với người chấm |
| **plan mode** | Model chỉ đọc và lập kế hoạch, không được sửa file — duyệt plan trước khi chạy |
| **skill (SKILL.md)** | Gói kiến thức + quy trình tái dùng, load theo progressive disclosure |
| **session / forking** | Phiên làm việc của agent; fork là tách nhánh từ một session đang chạy |

---
*Cheatsheet soạn 24/11/2026 từ notebook của repo này. Dùng để ôn nhanh — không thay exam guide chính thức.*
