# 01 — Individual Problem Scan

Case thực tế: **Chuyển đổi quy trình thiết kế xe từ phác thảo 2D sang Khối 3D thô** 
## Scan rộng

Hệ thống scan 13 problems thực tế trong quy trình R&D và vận hành thiết kế phương tiện:



| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Khi phát triển model xe mới, kỹ sư phải tra cứu thủ công và copy-paste lại các điểm kỹ thuật cố định (Hardpoints) như: bình xăng, bình điện, gá động cơ từ khung gầm xe cũ sang bản vẽ mới. | Kỹ sư CAD | Mất trên 5 tiếng mỗi khi bắt đầu một dáng xe mới cùng phân khúc. |
| 2 | Lặp lại | Đo đạc và đối chiếu thủ công kích thước lốp, vành, phanh đĩa để kiểm tra có bị vi phạm khoảng cách an toàn tối thiểu khi vận hành hay cạ dè xe không. | Kỹ sư kết cấu | Lặp lại mỗi tuần khi bản vẽ 2D thay đổi nét vẽ. |
| 3 | Tốn thời gian | Sau khi có bản vẽ 2D cho thiết kế mẫu xe mới, kỹ sư phải nắn chỉnh thủ công từng bề mặt (Surfacing) hoặc kéo lưới (Mesh) từ ảnh phác thảo và thông số để tạo khối 3D thô ban đầu. | Kỹ sư tạo khối | Mất từ 3 đến 5 ngày làm việc thực tế cho mỗi bản dựng thô. |
| 4 | Tốn thời gian | Viết meeting notes tổng hợp ý kiến sửa đổi thiết kế sau các buổi họp chéo giữa team Thiết kế kiểu dáng và team Kỹ thuật cơ khí. | PM dự án, Team member | 30 phút/buổi họp. |
| 5 | AI có thể tốt hơn | Phần mềm lưu trữ tài liệu (Notion/Excel) không tự động gợi ý thứ tự ưu tiên các linh kiện cần thiết kế trước dựa trên deadline kiểm thử linh kiện (Context/Dependency). | PM, Team member | Task nhiều nhưng thứ tự ưu tiên phân rã linh kiện bị mơ hồ. |
| 6 | AI có thể tốt hơn | Tra cứu lại bản vẽ cũ hoặc quyết định kỹ thuật cũ (Ví dụ: "Tìm cụm đèn pha LED của các đời xe ga từ 2020-2025") rất khó do lưu trữ file CAD phân tán. | Cả team R&D | Mất 30-45 phút/lần tìm, phải mở từng file CAD lớn ra để xem bằng mắt. |
| 7 | Pain từ người khác | Kỹ sư CAD phải dừng việc để hỏi lại bộ phận tạo dáng 2D vì nét vẽ phác thảo bị che khuất ở các góc khuất kỹ thuật (Mặt sau ổ khóa, gầm dè xe). | Kỹ sư CAD, Designer 2D | Hỏi đi hỏi lại 2-3 lần/mẫu spec vẽ phác thảo. |
| 8 | Pain từ người khác | Giám đốc thiết kế yêu cầu sửa đổi nhưng đưa ra nhận xét cảm tính ("cho đuôi xe thể thao hơn", "nhìn ngầu hơn"), kỹ sư CAD phải tự mò mẫm dịch sang số đo milimet. | Giám đốc thiết kế, Kỹ sư CAD | Sửa đi sửa lại (Feedback loop) từ 7-10 lần mới chốt được một chi tiết nhỏ. |
| 9 | Tốn thời gian | Tổng hợp và kết xuất dữ liệu thử nghiệm độ bền vật liệu (Monthly KPI/Testing Report) từ nhiều thiết bị đo lường khác nhau. | Kỹ sư thử nghiệm, Manager | Lặp lại mệt mỏi vào cuối mỗi tháng. |
| 10 | Lặp lại | Viết báo cáo tiến độ tiến trình gia công khuôn mẫu thử nghiệm mỗi sáng theo đúng một format mẫu gửi cho cấp quản lý. | Kỹ sư xưởng mẫu | 10-15 phút/ngày. |
| 11 | AI có thể tốt hơn | Phần mềm CAD không tự dự đoán được tọa độ trọng tâm (Center of Gravity) dựa trên vật liệu và độ dày khối vỏ thô để cảnh báo lệch cân bằng. | Kỹ sư kết cấu | Mất 2 ngày tính toán sơ bộ bằng tay cho mỗi form dáng mới. |
| 12 | Tốn thời gian | Đo đạc và đối chiếu thủ công từng kích thước đèn, góc biển số trên file 3D với hàng trăm trang tài liệu luật đăng kiểm (TCVN/Euro 5) của các nước. | Kỹ sư đăng kiểm | Mất ít nhất 12 tiếng kiểm tra thủ công cho một bộ vỏ xe đầy đủ. |
| 13 | Pain từ người khác | Kỹ sư khuôn mẫu trả lại file 3D vì Designer vẽ góc vuốt bề mặt quá gắt, không thể làm khuôn dập tấm kim loại hoặc ép nhựa được (Lỗi DFM). | Kỹ sư khuôn, 3D Modeler | File bị trả đi trả lại 4-5 lần; xưởng khuôn phải đợi có file chuẩn mới gia công được.


## Top 3


| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Tạo khối 3D thô từ phác thảo 2D | Workflow đầu vào/đầu ra cực rõ. Chiếm nhiều thời gian nhất trong quy trình. Tiết kiệm thời gian là metric nhìn thấy rõ bằng mắt. | Khái niệm khối 3D "đủ tốt" để kỹ sư dùng tiếp rất khó đo. AI dễ sinh lưới bị lỗi bề mặt hoặc méo hình học không gian. |
| 2 | 	Tự động quét và phát hiện lỗi thoát khuôn/dập tấm (DFM Check) | Cực kỳ tốn chi phí nếu làm sai. Bài toán có tập luật hình học rõ ràng (độ vát góc, độ dày thành), rất phù hợp để AI/Rule kiểm tra chéo tự động thay vì đợi kỹ sư xưởng check bằng mắt. | Cần thuật toán xử lý không gian (Spatial AI) đủ mạnh để đọc và bóc tách các vùng bề mặt phức tạp trên file 3D thô. |
| 3 | Tra cứu/Tái sử dụng linh kiện từ đời xe cũ | Nhiều người đau, giảm chi phí sản xuất khuôn lớn cho công ty. | Bản quyền và bảo mật dữ liệu file CAD của hãng cực cao. Phạm vi hệ thống RAG cho dữ liệu không gian 3D quá rộng. |

## Problem Card #1 — 2D Sketch to Digital Clay (Concept 3D)

**Problem 1 câu:**  
Mỗi khi có dáng xe mới, Kỹ sư dựng hình mất từ 3 đến 5 ngày kéo lưới (mesh) thủ công từ ảnh phác thảo 2D để tạo khối đất sét kỹ thuật số thô, làm chậm tiến độ duyệt thiết kế tổng thể.

**Actor:**  
Kỹ sư tạo dáng khối 3D (3D Modeler / Digital Sculptor) tại phòng R&D xe máy.

**Thời điểm / bối cảnh:**  
Giai đoạn đầu của dự án R&D (Concept Design Phase), ngay sau khi bản phác thảo kiểu dáng và bảng thông số kích thước bao (Dài x Rộng x Cao) được duyệt sơ bộ.

**Current workflow:**
```text
1. Nhận ảnh phác thảo 2D ba góc (Trước, Ngang, Sau) + Bảng kích thước (D x R x C)
2. Import ảnh vào môi trường phần mềm 3D (Autodesk Alias / Blender) làm hình nền
3. Tạo các khối hộp (Bounding Box) bao quanh theo kích thước giới hạn tối đa
4. Kéo lưới (Mesh), nắn khối polymer/clay kỹ thuật số thủ công theo các nét nét vẽ 2D
5. Xử lý mịn các bề mặt giao cắt thô (Basic Surfacing) để tạo khối liền mạch
6. Self-review tỷ lệ hình học xem có bị méo hay sai lệch phác thảo không
7. Xuất file định dạng thô (.obj/.stl) gửi cho Trưởng nhóm duyệt dáng xe
```

**Bottleneck:**  
Bước 4 & 5 — Việc nắn chỉnh từng đa giác (polygon) để biến các nét vẽ phẳng 2D thành hình khối không gian 3 chiều đối ứng mất khoảng 16 - 24 giờ làm việc thực tế và phụ thuộc hoàn toàn vào kỹ năng kéo tay của kỹ sư.

**Impact:**  
Mất 3 - 5 ngày làm việc cho mỗi một phương án thiết kế dáng xe. Một mẫu xe cần thử nghiệm ít nhất 5 phương án ngoại hình, gây nghẽn tiến độ R&D toàn dự án từ 3 đến 4 tuần. Ban giám đốc không có mô hình trực quan để duyệt nhanh.

**Success metric:**  
Giảm tổng thời gian tạo khối 3D thô đầu tiên từ **3 ngày xuống dưới 30 phút**. File khối 3D do hệ thống sinh ra đạt độ chính xác hình học **>80%** khi đối chiếu với bảng thông số kích thước bao đầu vào.

**Non-AI alternative:**  
Mua hoặc tận dụng các bộ khung gầm/vỏ xe mẫu (3D Templates) có sẵn của hãng rồi kéo bóp lại. Cách này giảm được 20% thời gian nhưng làm mất đi "DNA thiết kế" đặc trưng và các đường dập nổi độc quyền của dòng xe mới.

**AI hypothesis:**  
Mô hình Deep Learning (Image-to-3D) tự động phân tích ảnh phác thảo nhiều góc độ kết hợp với tham số kích thước dạng bảng để sinh ra lưới 3D thô đối xứng hoàn hảo trong vài phút. Kỹ sư chỉ đóng vai trò kiểm duyệt và vá lỗi bề mặt nhỏ.

**Quick gut:**  
Rule + Deep Learning Model (Workflow).

### Draft current workflow

```text
CURRENT STATE — 3 ngày (Khoảng 24 giờ làm việc thực tế)

[1 Nhận & phân tích spec: 60']
→ [2 Setup môi trường & ảnh nền: 30']
→ [3 Tạo khung bounding box giới hạn: 30']
→ [4 Kéo lưới nắn khối thô thủ công: 16 giờ]  <-- bottleneck
→ [5 Xử lý mịn bề mặt giao cắt: 5 giờ]        <-- bottleneck
→ [6 Self-review tỷ lệ hình học: 60']
→ [7 Xuất file gửi duyệt: 15']
```

### Draft future workflow

```text
FUTURE STATE — 25 phút

[1 Nhập ảnh 2D + thông số kích thước bao vào hệ thống: 2']
→ [2 AI phân tích luật kích thước (Rule-check): 1']
→ [3 AI sinh mô hình hình khối 3D thô (Mesh Generation): 2']
→ [4 Kỹ sư review + vá lỗi bề mặt (Sửa lỗ thủng, lệch đối xứng bằng tay): 20'] <-- human boundary
Hoàn thành: Xuất file 3D thô chuẩn sang bước tiếp theo.

Fallback: AI sinh khối bị biến dạng nặng hoặc sai tỷ lệ kích thước bao → Kỹ sư quay lại dùng workflow thủ công cũ.
```

## Problem Cards #2 và #3 — tóm tắt


| Card | Actor | Bottleneck | Metric | Quick gut | Vì sao chưa chọn làm #1 |
|---|---|---|---|---|---|
| **#2: RLHF Prompt-to-CAD (Dịch feedback sếp)** | Kỹ sư CAD & Giám đốc thiết kế | Dịch từ ngữ nhận xét cảm tính, trừu tượng của sếp thành thông số cơ khí số học chính xác để sửa đổi trực tiếp trên file 3D. | **7-10 vòng lặp** sửa đổi → **2-3 vòng lặp** chốt thiết kế. | AI Agent | Gu thẩm mỹ của mỗi sếp là khác nhau và mang tính chủ quan cao, rất khó để thiết kế các metric đo lường chất lượng kỹ thuật một cách tự động. |
| **#3: Tra cứu/Tái sử dụng linh kiện từ đời xe cũ** | Toàn bộ kỹ sư team R&D và CAD | Phải l lục tìm, mở từng file CAD cũ lớn để đo đạc xem linh kiện cũ có vừa vặn với khoảng trống trên xe mới hay không. | **45 phút/lần tìm** → **dưới 3 phút** có ngay đề xuất linh kiện phù hợp nhất kèm tọa độ đặt. | Agent / Workflow | Quyền truy cập dữ liệu (Data Access) là bài toán cực khó do chính sách bảo mật thông tin tuyệt mật của các hãng xe lớn; scope xử lý RAG trên dữ liệu hình học CAD 3D quá rộng để làm MVP đầu tiên. |
