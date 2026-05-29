# 02 — Group Problem Statement

> Bản nộp nhóm — Nhóm 8. Mỗi học viên copy bản cuối này vào repo cá nhân của mình.

---

## Group Convergence

Nhóm 4 người, mỗi người share top 3. Tổng cộng khoảng 12 candidates.

### Bước 3.1 — Trình bày top 3 (nhật ký pitch)

| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cảm nhận nhanh |
|---|---|---|---|---|---|
| 1 | Cường | Nghĩ hôm nay ăn gì và mua đồ ăn thiếu/thừa | Sinh viên ở trọ | Bước nghĩ món và lập danh sách mua | Workflow |
| 2 | Cường | Quản lý chi tiêu ở trọ | Sinh viên ở trọ | Ghi chép rải rác, không có cái nhìn tổng | Rule |
| 3 | Cường | Tìm việc ở trọ gần trường | Sinh viên mới | Tìm thông tin phòng trọ đáng tin cậy | Workflow |
| 4 | Minh Khánh | Smart Wake-up dựa trên chu kỳ giấc ngủ | Sinh viên/người đi làm | Set alarm không khớp chu kỳ ngủ, dậy mệt | Workflow |
| 5 | Minh Khánh | Nhắc lịch học/họp thông minh | Sinh viên | Quên lịch, không có cảnh báo trước | Rule/Workflow |
| 6 | Minh Khánh | Tìm tài liệu học tập phân tán | Sinh viên | Tài liệu rải rác nhiều nguồn, khó tìm | Workflow |
| 7 | Hoàng Nam | Viết báo cáo Dự án từ file rời rạc | Sinh viên viết báo cáo | Tổng hợp, phát hiện trùng lặp, draft đoạn nối | Workflow |
| 8 | Hoàng Nam | Tổng hợp góp ý GVHD từ nhiều buổi meeting | Nhóm làm Dự án | Góp ý nằm rải rác Zalo/file Word, dễ sót | Workflow |
| 9 | Hoàng Nam | Đọc paper tìm trích dẫn phù hợp | Người viết báo cáo học thuật | Mất 4-6 giờ đọc paper, phần lớn không dùng được | Workflow |
| 10 | Như Kiệt | Tạo khối 3D thô từ phác thảo 2D | Kỹ sư thiết kế R&D | Chuyển đổi 2D → 3D mất nhiều thời gian thủ công | Agent |
| 11 | Như Kiệt | Kiểm tra DFM (Design for Manufacturability) | Kỹ sư thiết kế | Kiểm tra DFM thủ công, dễ sót lỗi | Workflow |
| 12 | Như Kiệt | Tra cứu linh kiện CAD có sẵn | Kỹ sư R&D | Tìm linh kiện tương thích mất nhiều thời gian | Rule/Workflow |

### Bước 3.2 — Cluster (gom trùng / cụm vấn đề)

| Cluster | Candidates included | Pattern chung | Ghi chú |
|---|---|---|---|
| A — Đời sống sinh viên | Nghĩ món ăn, mua đồ thiếu/thừa, smart wake-up, quản lý chi tiêu | Các việc lặp lại hằng ngày, gần với trải nghiệm sinh viên | Dễ hiểu khi thuyết trình, có workflow rõ |
| B — Học tập | Viết báo cáo từ file rời rạc, tổng hợp góp ý GVHD, đọc paper tìm trích dẫn | Sinh viên mất thời gian tổng hợp thông tin rời rạc | AI fit tốt, nhưng cần boundary để không thành "AI viết hộ bài" |
| C — R&D / thiết kế kỹ thuật | 2D sketch to 3D, DFM check, CAD reuse | Bài toán chuyên môn sâu, impact lớn | Hay nhưng quá kỹ thuật, khó để cả nhóm trình bày dễ hiểu |

### Bước 3.3 — Shortlist

| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
|---|---|---|
| Nghĩ hôm nay ăn gì và mua đồ ăn thiếu/thừa | Actor rõ là sinh viên ở trọ; workflow dễ vẽ; bottleneck nằm ở bước nghĩ món và lập danh sách mua; metric đo được bằng thời gian, số lần mua thiếu/thừa và ngân sách | Cần kiểm tra người dùng có chịu nhập đồ đang có, ngân sách, thời gian nấu không |
| Viết báo cáo Dự án từ file rời rạc | Actor rõ là người viết chính; workflow rõ; AI hỗ trợ tổng hợp, phát hiện trùng lặp và draft đoạn nối | Dễ bị hiểu thành AI viết hộ báo cáo, cần human review rất rõ |
| Smart Wake-up | Pain phổ biến; workflow set alarm → sleep tracking → wake-up optimization rõ | Cần sensor data, wearable/mobile tracking; prediction sai có thể làm người dùng dậy muộn |
| Tạo khối 3D từ phác thảo 2D | Impact lớn, bottleneck rõ, metric thời gian mạnh | Quá chuyên môn, cần dữ liệu CAD/3D, khó làm pilot nhỏ trong lab |

### Bước 3.4 — Score để đồng thuận

Thang điểm 1-5. Tổng tối đa 35 điểm.

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Nghĩ hôm nay ăn gì và mua đồ ăn thiếu/thừa | 5 | 5 | 4 | 5 | 5 | 5 | 5 | 34 |
| Viết báo cáo Dự án từ file rời rạc | 5 | 5 | 4 | 5 | 5 | 5 | 5 | 34 |
| Smart Wake-up | 4 | 5 | 4 | 4 | 3 | 4 | 4 | 28 |
| Tạo khối 3D từ phác thảo 2D | 5 | 5 | 4 | 5 | 2 | 4 | 2 | 27 |

**Candidate nhóm chọn:**

```text
Nghĩ hôm nay ăn gì và mua đồ ăn thiếu/thừa của sinh viên ở trọ.
```

**Vì sao chọn:**

```text
- Có workflow rõ nhất, mọi thành viên đều trải qua.
- Có baseline thời gian ước lượng được (25-40 phút/lần).
- Có thể validate nhanh với sinh viên ở trọ.
- Có thể research các app/pattern có sẵn (meal planner, grocery list).
- Có thể vẽ before/after rất rõ.
- Phạm vi nhỏ, có thể pilot trong 1 tuần không cần dữ liệu phức tạp.
```

**Vì sao không chọn các candidates còn lại:**

```text
- Viết báo cáo Dự án: điểm ngang nhau nhưng dễ bị hiểu nhầm là AI viết hộ nội dung học thuật,
  cần giải thích rất kỹ human boundary khi thuyết trình. Để làm phương án dự phòng.
- Smart Wake-up: phụ thuộc sensor data và sleep-stage prediction, rủi ro kỹ thuật cao
  hơn trong phạm vi lab. Có thể bị hỏi nhiều về độ chính xác và quyền riêng tư.
- Tạo khối 3D từ phác thảo 2D: impact rất lớn nhưng quá chuyên môn, không phải thành
  viên nào cũng hiểu workflow CAD/3D đủ sâu để bảo vệ bài.
```

---

## Quick Validation

Nhóm hỏi nhanh sinh viên đang ở trọ trong lớp và qua Discord.

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Quick interview (sinh viên ở trọ) | 3 | Tất cả đều mất trên 20 phút nghĩ món + lập danh sách mua mỗi lần; hay mua thiếu hoặc thừa nguyên liệu | 1 người nói đã workaround bằng cách mua đồ theo thực đơn cố định mỗi tuần | Thu hẹp: không phải tự động hóa hoàn toàn, mà là hỗ trợ bước nghĩ món và lập danh sách tối giản |
| Mini poll trong lớp | 5 | 4/5 từng gặp cảnh mua dư đồ ăn rồi bỏ đi; tất cả đồng ý bước nghĩ món là tốn thời gian nhất | Một người nói thích tự quyết định, không muốn AI gợi ý | Thêm boundary rõ: AI chỉ gợi ý, người dùng vẫn review và quyết định cuối |

**Insight sau validation:**

```text
Pain thật không nằm ở việc "tự nấu ăn" đơn thuần. Pain nằm ở đoạn cân bằng nhiều ràng buộc
cùng lúc: đồ đang có, ngân sách, thời gian nấu, khẩu vị — để ra được danh sách mua tối giản
và thực đơn phù hợp. Đây là bài toán tối ưu nhiều biến mà AI có thể hỗ trợ tốt.
```

---

## Research Giải Pháp

Nhóm tìm các hướng đã có sẵn, không giả định phải tự build từ đầu.

| Nguồn / tool / case | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| Mealime (meal planning app) | https://www.mealime.com | Gợi ý thực đơn tuần + tạo grocery list tự động | Tốt cho bước gợi ý món và lập danh sách mua | Không tính đến đồ đang có trong nhà, không tối ưu ngân sách sinh viên | Rule + Workflow đã đủ cho bước gợi ý cơ bản; điểm khác biệt là phải tính đồ đang có |
| Paprika Recipe Manager | https://www.paprikaapp.com | Quản lý công thức + tạo grocery list từ thực đơn chọn | Tốt cho người có sẵn thực đơn cố định | Phải tự chọn công thức trước, không AI hỗ trợ gợi ý từ nguyên liệu có sẵn | Pattern tốt: lấy input từ người dùng → tạo list; cần thêm bước AI xử lý nguyên liệu đang có |
| ChatGPT / Gemini (dùng tự do) | https://chat.openai.com | Draft menu gợi ý từ nguyên liệu người dùng nhập | Rất linh hoạt, hiểu context tốt | Không có memory, phải nhập lại mỗi lần; không tích hợp ngân sách | AI draft cần người review; workflow hợp lý là: nhập nguyên liệu + ngân sách → AI gợi ý → người review |

**Research takeaway:**

```text
Không nên build một agent tự lên kế hoạch bữa ăn cả tuần và tự mua đồ.
Hướng hợp lý hơn là Workflow: người dùng nhập đồ đang có + ngân sách + thời gian nấu +
món không ăn → AI gợi ý 2-3 món phù hợp + danh sách mua tối giản → người dùng review và quyết định.
```

---

## Workflow Before/After

### Current State — 6 bước, 25-40 phút/lần

```text
CURRENT STATE — 6 bước, khoảng 25-40 phút/lần

[1 Nghĩ hôm nay ăn gì: 15-20']   <-- bottleneck chính
    (cân bằng khẩu vị, ngân sách, thời gian nấu, đồ đang có)
→ [2 Kiểm tra đồ trong nhà: 5']
→ [3 Lập danh sách mua: 5-10']
→ [4 Đi mua đồ: biến thiên]
→ [5 Nấu/ăn]
→ [6 Xử lý đồ thừa (nếu mua dư)]
```

| Bước | Actor | Input | Output | Thời gian/tần suất | Ghi chú |
|---|---|---|---|---|---|
| 1 Nghĩ ăn gì | Sinh viên | Khẩu vị, ngân sách, thời gian | Quyết định món ăn | 15-20 phút, 3-5 lần/tuần | **Bottleneck chính** |
| 2 Kiểm tra đồ trong nhà | Sinh viên | Đồ đang có trong tủ/tủ lạnh | Danh sách đồ có | 5 phút | Thường bỏ qua, hay quên |
| 3 Lập danh sách mua | Sinh viên | Công thức món, đồ đang có | Danh sách đi mua | 5-10 phút | Hay mua thiếu hoặc thừa |
| 4 Đi mua đồ | Sinh viên | Danh sách mua | Nguyên liệu mua về | Biến thiên | |
| 5 Nấu / ăn | Sinh viên | Nguyên liệu, công thức | Bữa ăn | Biến thiên | |
| 6 Xử lý đồ thừa | Sinh viên | Đồ mua dư | — | 5-10 phút | Tốn tiền, lãng phí |

**Bottleneck chính:**

```text
Bước 1 — Nghĩ hôm nay ăn gì: mất 15-20 phút mỗi lần vì phải cân bằng nhiều ràng buộc
cùng lúc (khẩu vị, ngân sách, thời gian nấu, đồ đang có). Kết quả là hay mua thiếu/thừa
hoặc bỏ cuộc đặt đồ ăn ngoài (tốn tiền hơn).
```

### Future State — 4 bước, dưới 10 phút/lần

```text
FUTURE STATE — 4 bước, dưới 10 phút/lần

[1 Nhập input: 2']
    (đồ đang có + ngân sách + thời gian nấu + món không ăn)
→ [2 AI gợi ý 2-3 món + danh sách mua tối giản: 1']   -- Workflow step
→ [3 Sinh viên review và sửa: 5']                       -- Human boundary
→ [4 Đi mua đồ và nấu]

Fallback:
AI gợi ý không phù hợp → sinh viên tự chọn món quen + nhập thủ công vào danh sách.

Bottleneck mới:
Bước nhập input. Đây là bottleneck chấp nhận được vì người dùng kiểm soát và quyết định.
```

**Before/after impact:**

| Metric | Trước | Sau kỳ vọng | Ghi chú |
|---|---:|---:|---|
| Thời gian nghĩ món + lập danh sách | 25-40 phút | Dưới 10 phút | Target chính |
| Số bước thủ công tốn công nhất | Bước 1 (20 phút) | Bước 3 review (5 phút) | Human boundary rõ hơn |
| Tần suất mua thiếu/thừa | 2-3 lần/tuần | 0-1 lần/tuần | AI tối ưu danh sách theo đồ có sẵn |
| Tần suất đặt đồ ăn ngoài vì không nghĩ ra | Thường xuyên | Giảm rõ | Có gợi ý nhanh, ít lý do bỏ cuộc |
| Risk mới | Không có | Hallucination / gợi ý không phù hợp | Cần review trước khi đi mua |

---

## Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Sinh viên ở trọ, tự lo bữa ăn 3-5 lần mỗi tuần. |
| **Workflow** | Nghĩ món → kiểm tra đồ đang có → lập danh sách mua → đi mua → nấu/ăn → xử lý đồ thừa. |
| **Bottleneck** | Bước nghĩ món mất 15-20 phút vì phải cân bằng khẩu vị, ngân sách, thời gian nấu và nguyên liệu đang có cùng lúc. |
| **Impact** | Mua thiếu/thừa đồ ăn, dễ đặt đồ ăn ngoài (tốn tiền hơn), khó kiểm soát chi tiêu ăn uống. |
| **Success Metric** | Giảm thời gian nghĩ món + lập danh sách từ khoảng 35 phút xuống dưới 10 phút/lần. |
| **Boundary** | AI không tự quyết định người dùng phải ăn gì; người dùng phải review danh sách trước khi mua. |

---

## Rule / Workflow / Agent

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **Rule** | Template thực đơn cố định theo tuần, checklist mua đồ có sẵn | Đủ nếu sinh viên ăn thực đơn giống nhau mỗi tuần và không cần cá nhân hóa | Không giải quyết bài toán cân bằng nhiều ràng buộc linh hoạt; người dùng vẫn phải tự điều chỉnh | Không chọn làm toàn bộ, nhưng dùng cho fallback |
| **Workflow** | Người dùng nhập input → AI gợi ý 2-3 món + danh sách mua tối giản → người dùng review | Hợp vì workflow tuyến tính, AI chỉ hỗ trợ bước tối ưu nhiều ràng buộc | Gợi ý sai/không phù hợp khẩu vị; cần người review | **Chọn** |
| **Agent** | Agent tự theo dõi kho đồ ăn, tự gợi ý thực đơn cả tuần, tự tạo đơn đặt hàng | Chỉ cần nếu sinh viên muốn lên kế hoạch cả tuần tự động và tích hợp app mua sắm | Quá rộng cho lab; cần nhiều quyền và tích hợp phức tạp; hallucination nguy hiểm hơn nếu AI tự đặt hàng | Chưa chọn |

**Mức chọn:**

```text
Workflow.
```

**Vì sao chọn Workflow, không chọn Rule:**

```text
Rule (template cố định) không giải quyết được bài toán cân bằng linh hoạt giữa đồ đang có,
ngân sách thay đổi mỗi tuần, và khẩu vị. AI ở mức Workflow giúp xử lý đúng phần này.
```

**Vì sao không chọn Agent:**

```text
Bài toán chưa cần AI tự lập kế hoạch dài hạn, tự gọi công cụ hoặc tự mua đồ.
Workflow tuyến tính: nhập input → AI gợi ý → người review là đủ và ít rủi ro hơn.
```

---

## Problem Statement v1

| Field | Nội dung |
|---|---|
| **Actor** | Sinh viên ở trọ, tự lo bữa ăn 3-5 lần mỗi tuần. |
| **Workflow** | Nghĩ món → kiểm tra đồ đang có → lập danh sách mua → đi mua → nấu/ăn → xử lý đồ thừa. |
| **Bottleneck** | Bước nghĩ món và lập danh sách mua mất 25-40 phút/lần vì phải cân bằng khẩu vị, ngân sách, thời gian nấu và nguyên liệu đang có cùng lúc. |
| **Impact** | Mất thời gian, mua thiếu/thừa đồ ăn, dễ đặt đồ ăn ngoài, khó kiểm soát chi tiêu ăn uống. |
| **Success Metric** | Giảm thời gian nghĩ món + lập danh sách từ khoảng 35 phút xuống dưới 10 phút/lần; giảm mua thiếu/thừa xuống 0-1 lần/tuần. |
| **Boundary** | AI không tự quyết định người dùng phải ăn gì; không tự mua đồ; không tự giả định dị ứng/kiêng ăn; người dùng phải review danh sách trước khi mua. |
| **AI intervention point** | Sau khi người dùng nhập đồ đang có, ngân sách, thời gian nấu và món không ăn; trước khi đi mua đồ. |
| **Mức chọn** | Workflow: người dùng nhập input, AI gợi ý 2-3 món + danh sách mua tối giản, người dùng review. |
| **Rủi ro & người thật kiểm tra** | Risk: AI gợi ý không phù hợp khẩu vị, hallucination nguyên liệu. Người thật review: sinh viên phải kiểm tra danh sách và sửa trước khi đi mua. |

---

## Final Decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú |
|---|---|---|
| Actor và workflow đã rõ chưa? | Yes | Sinh viên ở trọ, workflow 6 bước rõ |
| Baseline và success metric đã đo được chưa? | Yes | Baseline ~35 phút, target < 10 phút, đo bằng thời gian thực |
| Có data/input đủ dùng chưa? | Yes | Input là đồ đang có + ngân sách + thời gian nấu, người dùng tự nhập |
| Nếu AI sai, hậu quả có chấp nhận được không? | Yes | Gợi ý sai → người dùng review và sửa trước khi mua; không nguy hiểm |
| Có người review/owner vận hành không? | Yes | Chính sinh viên là người review cuối |
| Có cách non-AI đơn giản hơn không? | Yes | Template thực đơn cố định, nhưng không giải quyết cân bằng linh hoạt |

**Decision:**

```text
Go với scope nhỏ.
```

**Lý do:**

```text
- Problem rõ: sinh viên ở trọ, workflow 6 bước, bottleneck tại bước nghĩ món.
- Workflow rõ: tuyến tính, AI chỉ hỗ trợ bước tối ưu nhiều ràng buộc.
- Metric rõ: đo được thời gian, số lần mua thiếu/thừa.
- Human review rõ: sinh viên review danh sách trước khi mua.
- Có non-AI alternative: template cố định (fallback nếu AI gợi ý tệ).
- Rủi ro thấp: nếu AI gợi ý sai, hậu quả không nghiêm trọng.
```

**Pilot nhỏ nhất:**

```text
- Dùng ChatGPT / Gemini với prompt chuẩn.
- Sinh viên nhập: đồ đang có + ngân sách + thời gian nấu + món không ăn.
- AI gợi ý 2-3 món + danh sách mua tối giản.
- Sinh viên đo thời gian từ lúc nhập đến lúc có danh sách đã review.
- Chạy thử 3-5 bữa trong 1 tuần, ghi lại thời gian và số lần phải sửa danh sách.
```

**Exit / rollback:**

```text
- Nếu sinh viên phải sửa hơn 50% danh sách trong 3 lần liên tiếp, hạ xuống template + checklist thủ công.
- Nếu AI gợi ý món không phù hợp dị ứng/kiêng ăn dù đã nhập, không dùng trực tiếp.
```

