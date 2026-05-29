# 01 - Individual Problem Scan

## 1. Candidate problems (10 problems)

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Mỗi lần mua sắm phải mở từng app/website siêu thị rồi duyệt danh mục giống nhau | Người nội trợ chuẩn bị mua sắm theo tuần | Mất 15-20 phút mỗi lần kiểm tra giá trên 3-4 nền tảng khác nhau |
| 2 | Tốn thời gian | Phải đi tới vài trung tâm thương mại để tìm giá tốt nhất | Người mua hàng cần mua gấp | Mất 1-2 giờ di chuyển + tìm kiếm; bị phàn nàn "tại sao không mua chỗ rẻ hơn" |
| 3 | Lặp lại | Phải lặp lại việc tóm tắt và ghi chú khi chuyển từ bài báo này sang bài báo khác | Nghiên cứu sinh / học viên đang đọc nhiều paper | Viết note cho mỗi tài liệu mất 30-45 phút, nhiều nội dung trùng nhưng vẫn phải tái viết |
| 4 | Tốn thời gian | Mất nhiều thời gian để so sánh và đối chiếu các điểm giống nhau giữa nhiều nguồn | Nghiên cứu sinh cần tổng hợp literature review | Mất 3-5 giờ để tạo bảng so sánh 5 paper; phải quay lại đọc lại vài lần |
| 5 | AI có thể tốt hơn | Không có công cụ tự động cảnh báo khi sản phẩm thường mua giảm giá sâu | Người nội trợ muốn tiết kiệm và tránh bỏ lỡ sale | Bỏ lỡ khuyến mãi tốt 2-3 lần/tuần; không có thông báo chủ động |
| 6 | AI có thể tốt hơn | Phân loại nhanh ý chính / ý quan trọng và loại bỏ phần nền không cần thiết | Nghiên cứu sinh cần kết quả nhanh từ tài liệu dày đặc | Đọc 30-50 trang paper mất 2-3 giờ để lấy ra 5-6 điểm chính |
| 7 | Pain từ người khác | Người thân phàn nàn "mua đắt", không biết chỗ nào rẻ hơn khi bị so sánh | Người nội trợ bị so sánh giá | Bị hỏi "tại sao không mua chỗ rẻ hơn" 1-2 lần/tuần |
| 8 | Pain từ người khác | Thầy hướng dẫn hoặc đồng nghiệp muốn thấy "điểm mới" nhưng mình chỉ có đống note rời rạc | Nghiên cứu sinh trình bày literature review cho giáo viên | Thầy yêu cầu giải thích lại điểm tương đồng 2-3 lần; feedback "gap nghiên cứu chưa rõ" |
| 9 | Lặp lại | Mỗi tuần phải gửi form/email xin báo cáo từ các team thành viên rồi hỏi lại chi tiết | Người tổng hợp báo cáo tuần cho quản lý | Gửi email follow-up 2-3 lần/tuần để xin chi tiết; mất 20 phút chỉ để hỏi lại |
| 10 | Tốn thời gian | Phải dành nhiều giờ để đọc tài liệu dài, slide, email để lấy ra những điểm chính | Người chuẩn bị meeting recap hoặc review tài liệu gấp | Mất 3-4 giờ để review 50 trang tài liệu + viết summary; phải quay lại đọc 2-3 lần |

## 2. Top 3 Problem Cards

### Problem Card #1: Trích xuất ý chính từ tài liệu dài

Problem 1 câu:
Nghiên cứu sinh mất 2-3 giờ để đọc paper 30-50 trang rồi trích xuất 5-6 ý chính, trong khi nội dung thực sự cần thiết chỉ 15% của tài liệu.

Actor:
Nghiên cứu sinh / học viên đang làm khóa luận.

Thời điểm / bối cảnh:
Hằng tuần cần review 5-10 paper liên quan, deadline gấp.

Current workflow 7 bước:
1. Mở PDF / paper.
2. Đọc abstract + kết luận (10 phút).
3. Scan phần liên quan + phương pháp (40 phút).
4. Đọc kết quả và discussion (30 phút).
5. Ghi chú bằng tay những ý chính (20 phút).
6. Viết tóm tắt 3-5 dòng vào note (15 phút).
7. Quay lại kiểm tra để lấy chi tiết (10 phút).

Bottleneck:
Bước 2-4 (80 phút) — mất thời gian lọc thông tin; bước 5-6 (35 phút) — phải viết lại theo cách hiểu của mình.

Impact:
- Đọc 1 paper = 2.5 giờ → 5 paper/tuần = 12.5 giờ.
- Bỏ lỡ chi tiết quan trọng, note không consistent.

Success metric:
- Giảm 50% thời gian đọc.
- Tỷ lệ ý chính bị bỏ sót < 5%.
- Note tự động có format chuẩn.

Non-AI alternative:
Tạo template ghi chú chuẩn; nhưng vẫn phải đọc và ghi chú thủ công.

AI hypothesis:
Input: PDF/paper.
AI trích xuất: methodology, findings, limitations, key insight.
Output: structured note.

Quick gut:
- Rule: không đủ.
- Workflow: phù hợp.
- Agent: có thể là nâng cấp, nhưng không cần cho prototype đầu.

### Problem Card #2: Cảnh báo khuyến mãi sản phẩm thường mua

Problem 1 câu:
Người nội trợ mỗi tuần phải vào 3-4 app siêu thị để kiểm tra giá và khuyến mãi, mất 20-30 phút, và vẫn hay bỏ lỡ sale tốt.

Actor:
Người nội trợ quản lý chi tiêu gia đình.

Thời điểm / bối cảnh:
Hằng tuần chuẩn bị danh sách mua sắm + kiểm tra giá.

Current workflow 6 bước:
1. Mở app BigC, Aeon, Lotte.
2. Tìm sản phẩm thường mua (8 phút/app).
3. Xem khuyến mãi, ghi chép giá.
4. Quay lại để so sánh nếu bỏ sót.
5. Quyết định mua ở đâu.
6. Bỏ lỡ sale mới.

Bottleneck:
Bước 2-3 (30 phút) — kiểm tra từng cửa hàng thủ công.

Impact:
- Mất 30 phút/tuần.
- Bỏ lỡ sale 2-3 lần/tuần.
- Bị phàn nàn "mua đắt".

Success metric:
- Giảm 80% thời gian.
- Phát hiện 90% khuyến mãi tốt.
- Tiết kiệm ≥ 300k/tháng.

Non-AI alternative:
Spreadsheet track giá và checklist.

AI hypothesis:
Hệ thống track giá tự động và cảnh báo khi giảm > 15%.

Quick gut:
- Rule + Workflow phù hợp.
- Agent chưa cần ngay.

### Problem Card #3: Trích xuất action items từ meeting recap

Problem 1 câu:
Nhân viên mất 3-4 giờ để ghi chú meeting, tổng hợp action items, deadline, người phụ trách → recap thường bị sai hoặc chậm trễ.

Actor:
Nhân viên chuẩn bị meeting recap cho team.

Thời điểm / bối cảnh:
Sau mỗi meeting công ty, cần gửi recap trước 2 giờ.

Current workflow 7 bước:
1. Dự meeting (60 phút).
2. Ghi chú toàn bộ + sơ đồ lại những quyết định (20 phút).
3. Xem lại Slack/email để lấy context (10 phút).
4. Ghi vào doc: decision, action, person, deadline (20 phút).
5. Đọc lại để chắc action items đúng (10 phút).
6. Viết narrative: background → decision → action items (20 phút).
7. Review + gửi cho manager (10 phút).

Bottleneck:
Bước 2-6 (80 phút) — phải tái xử lý thông tin nhiều lần.

Impact:
- Một meeting = 130 phút tổng.
- 2 meeting/tuần = 4.3 giờ/tuần.
- Recap thiếu chi tiết → phải sửa lại.

Success metric:
- Giảm 70% thời gian tạo recap.
- Trích xuất chính xác ≥ 95% action items.
- Recap gửi đúng hạn.

Non-AI alternative:
Standardize format recap + training.

AI hypothesis:
Input: transcript/recording.
AI trích xuất decision/action/owner/deadline.
Output: structured recap.

Quick gut:
- Workflow phù hợp.
- Agent có thể là bước tiếp theo.

## 3. Draft workflows cho top 3

### Workflow #1: Trích xuất ý chính từ tài liệu dài

Current state (2.5 giờ/paper):
- Mở PDF: 2'.
- Đọc abstract + conclusion: 10'.
- Scan Methodology/Results: 40'.
- Đọc Discussion: 30'.
- Ghi chú tay: 35'.
- Kiểm tra lại: 10'.

Future state (25 phút/paper):
- Upload PDF: 1'.
- AI extract structured note: 2'.
- Review note: 15'.
- Edit + save: 7'.

Fallback:
- PDF scan ảnh → chuyển sang text version.
- AI sai → review + sửa.

### Workflow #2: Cảnh báo khuyến mãi

Current state (30 phút/tuần):
- Mở app BigC: 1'.
- Tìm 10 sản phẩm: 15'.
- Xem giá + ghi chép: 5'.
- Mở Aeon + Lotte: 18'.
- So sánh: 5'.

Future state (5-8 phút/tuần):
- Nhập danh sách 10 sản phẩm: 5' (once).
- System track giá auto: 0'.
- Nhận alert khi giảm > 15%: 1'.
- Quyết định mua: 2'.

Fallback:
- API không có → web scraping.
- Alert nhiều sai → điều chỉnh threshold.

### Workflow #3: Trích xuất action items từ meeting recap

Current state (130 phút/meeting):
- Dự meeting: 60'.
- Ghi chú: 20'.
- Tổng hợp vào doc: 20'.
- Viết narrative: 20'.
- Review + gửi: 10'.

Future state (79 phút/meeting):
- Meeting + transcript: 60'.
- AI parse transcript: 2'.
- PM review recap: 10'.
- Edit + send: 7'.

Fallback:
- Không có transcript → dùng audio-to-text.
- AI thiếu owner/deadline → PM kiểm soát.
