# CCAR-F — Checklist ngày thi

> **Nguồn thông tin trong file này:** tổng hợp từ Exam Guide v1.0 (07/2026) mà repo này đang dùng + các thông tin thủ tục (đăng ký, thi lại, đổi lịch, phí theo tier, gia hạn) theo Practica Cert Prep, trang này cho biết họ đối chiếu nguồn chính thức ngày **21/11/2026** (xem link ở `resources.md`). Một số mục đã được một nguồn độc lập thứ hai (dsprep.com) xác nhận trùng khớp (phí, luật thi lại, điều kiện Partner Network).
>
> ⚠️ **Kiểm tra lại exam guide + Certification FAQ chính thức trước khi đăng ký** — Anthropic ghi rõ nội dung có thể thay đổi, và các thông tin thủ tục dưới đây mình chưa đọc trực tiếp từ văn bản chính thức của Anthropic. Repo này xây theo guide **v1.0 (07/2026)**; Practica dẫn guide **v1.1** — nên xác nhận phiên bản guide hiện tại trước khi thi. Lưu ý: theo Practica, **CCAR-F không nằm trong nhóm chứng chỉ đổi nội dung từ 07/12/2026** (nhóm đó là CCAO-F, CCDV-F, CCAR-P).

## 1. Trước khi đăng ký — đủ điều kiện chưa?

- [ ] Đang làm việc tại một tổ chức thuộc **Claude Partner Network** (đây là cửa bắt buộc — không có công ty partner thì không đăng ký được).
- [ ] Có **email công ty** thuộc partner đó (email cá nhân bị từ chối).
- [ ] Đủ **18 tuổi** trở lên.
- [ ] Đang ở một quốc gia Anthropic hỗ trợ thi — **Việt Nam được hỗ trợ**.
- [ ] Đã đọc hết exam guide (domain, trọng số, câu hỏi mẫu) và tự chấm mình trên từng task statement.
- [ ] Đã làm bài thi thử có tính giờ và điểm ổn định ở mức tự tin (không chỉ làm một lần rồi đăng ký).

## 2. Các bước đăng ký

1. Đăng nhập **Anthropic Partner Academy** bằng email công ty, mở trang chứng chỉ CCAR-F.
2. Bấm **Register** và xác nhận **tên đúng như trên giấy tờ tùy thân** (CMND/CCCD/hộ chiếu) — lưu ý: tên chỉ tự đổi được **một lần mỗi năm**, nên kiểm tra kỹ trước khi xác nhận.
3. Chuyển sang **Pearson VUE**: chọn hình thức **OnVUE (thi online)** hoặc **test centre**, chọn ngôn ngữ, ngày và giờ thi, rồi thanh toán.
4. **Giá được khóa tại thời điểm đặt lịch** — đặt càng sớm càng chắc giá.
5. Chạy **system test của Pearson** sớm, trên đúng máy + mạng sẽ dùng để thi (đặc biệt quan trọng với OnVUE trên laptop công ty).

## 3. Phí và giảm giá theo tier đối tác

| Tier của công ty | Phí CCAR-F |
|---|---|
| Registered | $125 (giá đầy đủ) |
| Select / Preferred / Global Premier | Giảm 50% tại lúc thanh toán qua Pearson |
| Global Premier | **Miễn phí tới 31/12/2026** |

- **Kiểm tra tier của công ty mình trước khi trả tiền** — mức giảm áp dụng tự động theo tier tại lúc checkout, không cần nhập mã.
- Thi lại cũng trả **đủ phí** như lần đầu (không có giá thi lại).
- Phí trên là giá niêm yết trước giảm giá; xác nhận lại trên trang Partner Academy vì có thể đổi.

## 4. Hình thức thi — biết trước để khỏi bỡ ngỡ

- **60 câu**, trắc nghiệm + trả lời nhiều đáp án, trong **120 phút** (~2 phút/câu). Tính cả thời gian làm thủ tục thì cần chừa khoảng **135 phút** ngồi thi.
- **4 scenario** rút ngẫu nhiên từ ngân hàng **6 scenario production** có sẵn: customer support agent, Claude Code viết code, hệ thống research đa agent, developer productivity tools, Claude Code trong CI, và trích xuất dữ liệu có cấu trúc. Mỗi scenario là một bối cảnh, các câu hỏi trong đó hỏi quyết định kiến trúc đúng trong bối cảnh đó.
- **Thang điểm 100–1.000, đậu từ 720** — không phải 72% số câu. Kết quả hiện ngay trên màn hình khi xong; báo cáo điểm có thêm **% đúng theo từng domain** (chỉ để tham khảo, không ảnh hưởng đậu/rớt). Đậu thì nhận badge qua **Credly** — nên thêm email cá nhân vào tài khoản Credly để khỏi mất badge khi đổi công ty.
- **Closed-book:** không được dùng Claude, tài liệu, hay công cụ hỗ trợ. Thi bằng **tiếng Anh hoặc tiếng Nhật** — nếu tiếng Anh không phải tiếng mẹ đẻ, có thể **xin thêm giờ từ Pearson trước khi đặt lịch**.
- **Không có câu hỏi không tính điểm nào được công bố cho CCAR-F** (các chứng chỉ khác từ 07/12/2026 có 10 câu thử không tính điểm — CCAR-F không nằm trong nhóm đổi đó).

## 5. Chiến thuật làm bài (120 phút / 60 câu)

- **Đọc scenario trước, đọc câu hỏi sau.** Câu hỏi nào cũng gắn với bối cảnh production — đáp án đúng là đáp án đứng vững trong production, không phải đáp án "nghe hay nhất".
- **Loại trừ trước, chọn sau:** bỏ ngay các đáp án vi phạm nguyên tắc nền tảng — dựa vào prompt để enforce điều bắt buộc, thêm tool khi chưa có task cần nó, tin mù kết quả subagent, để user input ghi đè system instruction. Đề CCAR-F thích cài anti-pattern làm đáp án nhử.
- **Câu multiple-response:** đề ghi rõ cần chọn mấy đáp án — đếm đủ số đáp án rồi mới sang câu khác. Chọn thiếu cũng sai như chọn sai.
- **Câu khó thì flag rồi đi tiếp**, quay lại sau khi xong vòng 1. Đừng đốt 5 phút cho một câu khi còn 20 câu chưa đọc — mỗi câu có trọng số ngang nhau trong thang điểm.
- **Chừa 10 phút cuối** để rà lại các câu đã flag và các câu multiple-response (dễ sót đáp án nhất).
- **Khi phân vân giữa hai đáp án đều "đúng":** chọn đáp án nào **enforce bằng code** thay vì dựa vào prompt, **đơn giản hơn** thay vì phức tạp hơn, và **kiểm chứng được** thay vì tin mù — đó là "khẩu vị" xuyên suốt của guide.
- **Không bỏ trống câu nào** — trắc nghiệm thì câu bỏ trống chắc chắn không điểm, câu đoán còn có cơ hội.

## 6. Đổi lịch, hủy, thi lại

- **Đổi lịch / hủy:** được tới **1 giờ trước giờ thi** với OnVUE, **48 giờ trước** với test centre. Muộn hơn hoặc vắng thi (no-show) thì **mất phí**.
- Pearson hoàn tiền hủy trong **7–10 ngày làm việc**.
- **Thi lại (nếu trượt):** chờ **14 ngày** sau lần trượt thứ nhất, **30 ngày** sau lần thứ hai, **90 ngày** sau lần thứ ba; tối đa **4 lần trong 12 tháng** liên tục.
- Dùng thời gian chờ để ôn lại đúng domain yếu theo báo cáo % từng domain — đừng đăng ký thi lại ngay khi chưa biết mình yếu ở đâu.

## 7. Không thi cái gì (out-of-scope — theo exam guide)

Đừng tốn thời gian ôn những thứ này cho CCAR-F — guide ghi rõ **ngoài phạm vi thi**:

- Fine-tuning
- API billing và authentication
- Hosting MCP server
- Vision, computer use
- Streaming
- Rate limits và pricing

(Nếu gặp câu hỏi về mấy chủ đề này trong tài liệu ôn bên ngoài, đó là tài liệu sai scope.)

## 8. Gia hạn (sau khi đậu)

- Chứng chỉ có hiệu lực **12 tháng** kể từ ngày đậu.
- **Gia hạn đúng hạn thì miễn phí:** xem lại những gì thay đổi từ lúc thi, rồi làm một bài **assessment không giám sát** trên Partner Academy — không cần thi lại toàn bộ.
- **Để quá hạn:** phải thi lại toàn bộ kỳ thi có giám sát với đủ phí.
- **Nếu kỳ thi thay đổi lớn**, Anthropic có thể yêu cầu thi lại toàn bộ thay vì assessment gia hạn.
- Anthropic cho biết chi tiết về thời gian mở cửa sổ gia hạn sẽ công bố trước khi các chứng chỉ đầu tiên hết hạn — **kiểm tra FAQ trước ngày hết hạn của mình**, đừng đợi tới sát ngày.

## 9. Checklist cuối cùng

### Một tuần trước thi

- [ ] Đã đọc lại exam guide một lần nữa (domain weights có thể đổi).
- [ ] Đã làm ít nhất một bài mock 60 câu / 120 phút trong điều kiện như thi thật.
- [ ] Đã ôn lại cheatsheet (`CCAR-F-cheatsheet.md`) + các anti-pattern (notebook Ch. 9.4, 11.3, 12B.4).
- [ ] Đã chạy system test của Pearson trên đúng máy sẽ thi.
- [ ] Đã xác nhận tier giảm giá của công ty (nếu có).

### Hôm trước thi

- [ ] Xác nhận lại giờ thi, múi giờ, và link/phòng thi (OnVUE) hoặc địa chỉ test centre.
- [ ] Chuẩn bị giấy tờ tùy thân trùng tên đã đăng ký.
- [ ] OnVUE: dọn bàn làm việc, chuẩn bị phòng kín, yên tĩnh; kiểm tra webcam + mic.
- [ ] Ngủ đủ — đừng thức khuya nhồi thêm.

### Sáng ngày thi

- [ ] Tới sớm / đăng nhập sớm 15–30 phút để làm thủ tục check-in.
- [ ] Mang theo giấy tờ tùy thân; không mang tài liệu, điện thoại vào khu vực thi (theo quy định của Pearson).
- [ ] Nhắc lại chiến thuật: 2 phút/câu, flag câu khó, chừa 10 phút cuối rà lại.

---
*Checklist soạn 24/11/2026. Thông tin thủ tục theo Practica Cert Prep (đối chiếu nguồn chính thức 21/11/2026) — kiểm tra lại exam guide + Certification FAQ chính thức trước khi đăng ký, vì phí, điều kiện và quy định có thể thay đổi.*
