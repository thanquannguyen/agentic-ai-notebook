# CCAO-F — Claude Certified Associate: Foundations

> Nguồn: Anthropic CCAO-F Exam Guide v1.0 (hiệu lực 07/2026). Kiểm tra lại
> exam guide trước khi đăng ký — Anthropic ghi rõ nội dung có thể thay đổi.

## Exam facts

| | |
|---|---|
| Mã thi | CCAO-F |
| Đối tượng | Người dùng Claude trong công việc (operations, marketing, PM, giáo dục, truyền thông) — **không cần biết code** |
| Số câu | 60 (trắc nghiệm + trả lời nhiều đáp án) |
| Thời gian | 120 phút |
| Phí | $99 |
| Đậu | 720 / 1.000 (thang điểm, không phải 72% số câu) |
| Hiệu lực | 12 tháng, gia hạn miễn phí nếu đúng hạn |
| Điều kiện đăng ký | Email công ty thuộc Claude Partner Network |

## Bảy domain và trọng số

| # | Domain | Trọng số | ~Số câu | Thi cái gì |
|---|---|---|---|---|
| 1 | Prompting and Task Execution | 14% | ~8 | Viết prompt cho task công việc, chia task phức tạp thành bước, lặp lại và cải thiện prompt |
| 2 | **Output Evaluation and Validation** | **21%** | ~13 | Kiểm tra độ chính xác/đầy đủ, phát hiện hallucination và bias, fact-check, biết khi nào cần người review, chọn format output |
| 3 | Product and Model Selection | 12% | ~7 | Chọn giữa chat, Projects, research mode, artifacts; chọn Haiku/Sonnet/Opus theo cost–speed–quality; quản lý context và memory |
| 4 | Workflow Integration and Solution Design | 16% | ~10 | Phân tích yêu cầu, đưa Claude vào workflow có sẵn, giải thích giá trị và giới hạn cho stakeholder |
| 5 | Configuration and Knowledge Management | 12% | ~7 | Lập Projects với instructions và knowledge, quản lý uploads và connectors (Google Drive, Gmail), giữ knowledge luôn mới |
| 6 | Governance, Risk, and Responsible Use | 15% | ~9 | Phân biệt dùng đúng/sai, quy tắc dữ liệu nhạy cảm và privacy, tuân thủ chính sách AI của tổ chức |
| 7 | Troubleshooting and Optimization | 10% | ~6 | Chẩn đoán prompt/output yếu, chỉnh từ feedback, làm workflow hiệu quả hơn |

**Điểm mấu chốt:** domain nặng nhất là **đánh giá output (21%)**, không phải viết
prompt (14%). Người học chỉ chăm chăm luyện prompt là học sai trọng tâm.

## Học gì

- **Anthropic Academy (miễn phí):** *Claude 101*, *AI Fluency* — hai khóa nền
  tảng cho track Associate.
- **Notebook này:** chương 5 (instructions), chương 9 (guardrails — phần
  governance), chương 10 (evals — phần output evaluation). Chương 6 (context)
  giúp phần Configuration & Knowledge Management.
- **Luyện đề:** làm nhiều câu scenario — đề thi hỏi "trong tình huống này thì
  làm gì", không hỏi thuộc lòng định nghĩa.

## Tài liệu public cho CCAO-F

| Nguồn | Nội dung |
|---|---|
| [ravnhq/claude-certified-architect](https://github.com/ravnhq/claude-certified-architect) | Study guide + practice exam cho cả 4 chứng chỉ; riêng Associate có ngân hàng 770 câu hỏi |
| [claude.termidy.com/ccao-f](https://claude.termidy.com/ccao-f/) | Community site: guide + ngân hàng 360 câu hỏi viết mới (không phải đề thật), chia theo domain |
| [rubricedu.com — CCAO-F guide](https://www.rubricedu.com/certifications/ccao-f) | 30 objectives theo 7 domain, mỗi objective link tới bài học |

## Kế hoạch gợi ý (1–2 tuần)

- **Tuần 1:** Claude 101 + AI Fluency (Academy). Đọc kỹ phần Output Evaluation
  và Governance trong notebook (chương 9, 10).
- **Tuần 2:** Làm 100–200 câu practice theo domain, tập trung vào 3 domain
  nặng nhất (Output Evaluation 21% + Workflow Integration 16% + Governance
  15% = 52% đề thi). Ôn lại các lỗi hay gặp: tin mù output, không fact-check,
  đưa dữ liệu nhạy cảm vào prompt.

## Liên hệ với các chứng chỉ khác

- CCAO-F là **dễ nhất và rẻ nhất** trong 4 cái — phù hợp làm bài khởi động
  (warm-up) trước khi vào CCAR-F, hoặc thi cuối cùng để hoàn thành bộ sưu tập.
- Kiến thức CCAO-F (prompting, output evaluation, governance) là nền tảng cho
  cả 3 chứng chỉ còn lại — học chắc phần này thì các chứng chỉ sau nhẹ hơn.
