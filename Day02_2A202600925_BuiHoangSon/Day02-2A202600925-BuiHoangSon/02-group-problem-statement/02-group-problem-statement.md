# 02 - Group Problem Statement

## 1. Candidate problem đã chọn

### Problem candidate

Problem 1 câu:
Nghiên cứu sinh mất 2-3 giờ để đọc paper 30-50 trang rồi trích xuất 5-6 ý chính, trong khi nội dung thực sự cần thiết chỉ 15% của tài liệu.

Actor:
Nghiên cứu sinh / học viên làm khóa luận.

Thời điểm / bối cảnh:
Hằng tuần review literature trước deadline, cần viết literature review và gap research.

Current workflow:
1. Mở paper.
2. Đọc abstract + conclusion.
3. Scan phần liên quan + methodology.
4. Đọc kết quả + discussion.
5. Ghi chú tay.
6. Viết tóm tắt.
7. Kiểm tra lại chi tiết.

Bottleneck:
- Quá nhiều nội dung phải lọc thủ công.
- Ghi chú không đồng bộ.
- Phải đọc nhiều lần để tránh bỏ sót.

Impact:
- Mất 2.5 giờ cho 1 paper.
- 5 paper/tuần = 12.5 giờ.
- Dễ bỏ lỡ "gap nghiên cứu" và mất nhiều thời gian tổng hợp.

Success metric:
- Giảm 50% thời gian đọc/rút gọn.
- Đưa ra note dạng structured với tỷ lệ chính xác ≥ 95% trên ý chính.
- Thời gian review 1 paper ≤ 30 phút.

Boundary (phạm vi làm):
- Chỉ giải quyết trường hợp có paper/technical document bằng text có thể đọc được.
- Không xử lý bài toán dịch thuật hoặc đọc PDF scan không OCR.
- Không xây hệ thống gợi ý toàn bộ literature; chỉ tập trung vào extraction và cấu trúc lại nội dung.

Non-AI alternative:
- Thực thi template note bắt buộc.
- Đào tạo researcher đọc paper theo checklist.
- Ưu điểm: rủi ro thấp. Hạn chế: vẫn tốn nhiều thời gian.

AI/Workflow/Rule so sánh:
- No AI: đọc và ghi chú thủ công.
- Rule: dùng checklist, template cố định.
- Workflow: AI hỗ trợ trích xuất ý chính, human review.
- Agent: nếu mở rộng ra hệ thống quản lý paper, có thể dùng agent để theo dõi paper hiện tại; nhưng prototype ban đầu chỉ cần workflow.

Giải thích lựa chọn:
Workflow là lựa chọn phù hợp vì bài toán cần xử lý ngôn ngữ phức tạp và trích xuất thông tin từ văn bản. AI hỗ trợ phần này, còn người dùng vẫn giữ vai trò xác nhận, chỉnh sửa, và định hướng nội dung.

Quyết định:
- Mức phù hợp: Workflow.
- Nếu đầu tư thêm: Agent có thể dùng khi mở rộng thành hệ thống review literature.

## 2. Phân tích nhanh theo lab

### Tại sao chọn problem này?
- Actor rõ: nghiên cứu sinh.
- Workflow rõ: có các bước đọc, scan, ghi chú, tổng hợp.
- Bottleneck cụ thể: bước đọc/scan và ghi chú.
- Metric rõ: giờ hiện tại và mục tiêu giảm.
- Boundary rõ: chỉ tập trung vào paper/document summarization.

### Điều chưa chắc / câu hỏi cần validation
- Paper dạng gì: academic paper, report, hay cả slide?
- Người dùng cần output ở dạng text hay note trong công cụ học tập?
- Có sẵn transcript/metadata hay chỉ PDF?

### Quick validation (đã thực hiện)
- Pain có thật từ kinh nghiệm cá nhân: đọc tài liệu dài luôn tốn thời gian và hay mất trọng tâm.
- Các gợi ý từ worksheet: 4 lăng kính đã dùng để mở rộng problem.
- Research sơ bộ: nhiều công cụ summarization hiện tại vẫn cần review do thiếu độ chính xác.

### Rule / Workflow / Agent
- Rule: checklist và template.
- Workflow: AI extract + human review.
- Agent: khả năng mở rộng sau này, nhưng không cần cho giải pháp ban đầu.

### Quyết định cuối
- Chọn candidate problem: Trích xuất ý chính từ tài liệu dài.
- Chọn phương án: Workflow.
- Tại sao: nó giải quyết đúng bottleneck nhất mà vẫn giữ được rủi ro thấp bằng review của người dùng.
