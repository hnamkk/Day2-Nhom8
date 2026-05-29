# 03 — Individual Reflection

> Học viên: Bùi Như Kiệt - Mã học viên: 2A202600895
> Nhóm 8

---

## Đóng góp của tôi trong nhóm

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| Scan cá nhân | Scan 13 problems từ quy trình R&D thiết kế phương tiện, đa dạng 4 lăng kính (Lặp lại, Tốn thời gian, AI có thể tốt hơn, Pain từ người khác) | Nhóm có thêm cluster chuyên biệt về quy trình kỹ thuật/công nghiệp với nhiều candidates rõ actor và dấu hiệu thật |
| Pitch Problem Card | Pitch "Tạo khối 3D thô từ phác thảo 2D" với workflow 7 bước và baseline 3–5 ngày làm việc (16–24 giờ thực tế tại bottleneck) | Candidate vào shortlist với metric rõ ràng: giảm từ 3 ngày xuống dưới 30 phút, độ chính xác >80% |
| Gom trùng / cluster | Phân tách rõ 3 nhóm vấn đề: lặp lại hành chính, lỗi hình học kỹ thuật, và tra cứu dữ liệu CAD | Nhóm tránh gộp nhầm các problem có actor và bottleneck khác nhau vào cùng một cluster |
| Chọn candidate problem | Tự lập luận Top 3 và chỉ ra lý do chưa chọn #2, #3 làm ưu tiên đầu | Nhóm có cơ sở rõ để so sánh trade-off giữa các candidates thay vì chọn theo cảm tính |
| Research | Khảo sát nhanh quy trình thực tế tại phòng R&D, đối chiếu timeline với kỹ sư tạo khối | Xác nhận bottleneck thật nằm ở bước kéo lưới (bước 4–5), không phải bước review hay xuất file |
| Rule / Workflow / Agent | Lập luận chọn Rule + Deep Learning Model (Workflow), không chọn Agent thuần | Nhóm thống nhất không "AI-first": AI sinh khối thô, kỹ sư vẫn giữ vai trò kiểm duyệt và vá lỗi |

---

## Bảng dùng AI trong lab

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan cá nhân | Hỏi AI gợi ý thêm problem theo role kỹ sư R&D thiết kế xe sau khi tự scan trước | Giúp nhớ thêm lăng kính "Pain từ người khác" (problem #7, #8, #13) — những người bị ảnh hưởng gián tiếp bởi bottleneck của người khác | AI gợi ý một số ý quá chung chung như "quản lý dự án phức tạp" không có actor rõ, không có dấu hiệu thật đo được | Bỏ các ý không có workflow cụ thể hoặc không có con số thời gian; chỉ giữ ý có người gặp vấn đề và hành động lặp lại rõ ràng |
| Problem Card | Dùng AI phản biện Problem Card #1 theo prompt skeptical PM | Chỉ ra khái niệm "đủ tốt" của file 3D thô chưa định nghĩa được; hỏi ranh giới giữa AI sinh khối và kỹ sư vá lỗi ở đâu | AI đề xuất luôn sang Agent tự động hoàn toàn (tự nhận ảnh, tự xuất file chuẩn gửi duyệt, không cần kỹ sư review) trước khi nhóm xác định level phù hợp | Kéo lại về Workflow có human-in-the-loop; nhấn mạnh kỹ sư vẫn là người chịu trách nhiệm chất lượng hình học cuối cùng |
| Workflow | Nhờ AI format lại current/future workflow từ mô tả text dạng thô | Nhanh hơn khi trình bày ASCII, AI gợi ý thêm bước "Fallback" khi AI sinh khối bị biến dạng nặng | AI gộp bước "Mesh Generation" và "Basic Surfacing" thành 1 bước, che khuất bottleneck thật (bước nắn từng polygon mới là nơi mất 16–24 giờ) | Tách lại thành hai bước riêng vì bottleneck nằm đúng ở bước kéo lưới thủ công, không phải bước xử lý mịn bề mặt sau đó |
| Problem Statement | Nhờ AI phản biện field còn mơ hồ trong Problem Card v0 | Chỉ ra success metric ">80% độ chính xác" chưa có phương pháp đo cụ thể; hỏi so sánh với cái gì | AI đề xuất thêm metric "user satisfaction score của kỹ sư review" — quá rộng và chủ quan cho giai đoạn pilot đầu tiên | Nhóm giữ metric cụ thể và đo được: thời gian tạo khối (phút) + tỷ lệ sai lệch kích thước bao so với bảng thông số đầu vào |

---

## Bài học cá nhân

### Điều tôi nhận ra về cách chọn problem

**Problem tốt không phải problem nghe "AI" hoặc "công nghệ cao" nhất.** Problem DFM Check (#2) và Problem tra cứu linh kiện (#3) đều nghe có vẻ phức tạp và thú vị về mặt kỹ thuật, nhưng cả hai đều bị loại khỏi vị trí #1 vì scope quá rộng và rủi ro dữ liệu quá cao để làm MVP. Problem #1 — tạo khối 3D thô — thắng vì input/output rõ ràng và metric tiết kiệm thời gian nhìn thấy được ngay bằng mắt.

**Bắt đầu từ quy trình thật, không phải từ công nghệ.** Vì tôi có trải nghiệm thực tế trong môi trường R&D thiết kế xe, tôi scan được 13 problems với dấu hiệu thật (giờ cụ thể, hành động lặp đi lặp lại). Những problem này dễ viết workflow hơn nhiều so với problem nghe qua hoặc tưởng tượng từ lý thuyết.

### Điều tôi nhận ra về AI

**AI hữu ích nhất ở bước phản biện, không phải bước tạo ra.** Khi dùng AI để phản biện Problem Card, AI chỉ ra điểm yếu trong metric và ranh giới human/AI rất nhanh. Nhưng khi để AI "gợi ý problem từ đầu", kết quả hay thiếu actor cụ thể và không có dấu hiệu thật đo được.

**Phải tự scan trước, AI sau.** Nếu mở AI ngay từ đầu, rất dễ bị kéo theo khung tư duy của AI — đặc biệt trong domain kỹ thuật chuyên biệt như CAD/R&D, AI thường không biết cụ thể bottleneck nằm ở bước nào. Scan tay trước giúp tôi biết ý nào của AI chạm đúng thực tế và ý nào chỉ là lý thuyết nghe có vẻ hợp lý.

**AI hay đề xuất Agent quá sớm và quá rộng.** Trong cả hai lần dùng AI (phản biện Problem Card và gợi ý workflow), AI đều nhảy thẳng sang giải pháp Agent tự động hoàn toàn dù bài toán chưa cần và chưa có dữ liệu huấn luyện rõ. Đây là dấu hiệu cần tự hỏi: "Workflow + Rule có giải được chưa?" trước khi leo thang lên Agent.

### Điều tôi nhận ra về làm việc nhóm

**Pitch rõ bottleneck bằng con số giúp nhóm quyết định nhanh hơn.** Khi tôi pitch "Tạo khối 3D thô — bottleneck tại bước kéo lưới — mất 16–24 giờ/phương án, một mẫu xe cần 5 phương án", nhóm hiểu ngay và đặt câu hỏi trúng thay vì hỏi vòng vo về công nghệ.

**Giải thích lý do không chọn quan trọng không kém lý do chọn.** Việc tôi chủ động ghi rõ tại sao Problem #2 và #3 chưa được chọn làm ưu tiên đầu (scope rộng, bảo mật dữ liệu CAD, khó đo metric) giúp nhóm không phải tranh luận lại từ đầu và tập trung vào phân tích Problem #1 sâu hơn.

---

## Nếu làm lại

```text
Tôi sẽ validate thêm baseline "3–5 ngày/phương án" bằng cách phỏng vấn
ít nhất 2–3 kỹ sư tạo khối từ các công ty R&D xe khác nhau (không chỉ
một môi trường), vì con số này hiện chủ yếu đến từ trải nghiệm nội bộ
một hãng. Baseline chắc hơn sẽ giúp success metric (giảm xuống dưới 30 phút)
thuyết phục hơn khi present.

Tôi cũng sẽ định nghĩa rõ hơn "độ chính xác >80%" ngay từ Problem Card v0
thay vì để mơ hồ: đo bằng gì (sai lệch mm so với bảng kích thước bao),
đo ở đâu (chiều dài tổng thể, chiều rộng tối đa, chiều cao yên), và ai là
người đo (kỹ sư review hay công cụ tự động). Không có phương pháp đo,
metric chỉ là con số cho có.
```
