# 03 — Individual Reflection

> Học viên: Ngô Minh Khánh - Mã học viên: 2A202600953
> Nhóm: 8

---

## Đóng góp của tôi trong nhóm

| Hoạt động                    | Tôi đã làm gì?                                                                                                                                                | Kết quả / ảnh hưởng                                                                     |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| Scan cá nhân                 | Scan nhiều problems liên quan đến giấc ngủ, báo thức và sức khỏe của sinh viên ở trọ như: thức dậy mệt, snooze nhiều lần, ngủ đủ giờ nhưng vẫn thiếu tỉnh táo | Nhóm có thêm cluster về health-tech và hành vi sinh hoạt hằng ngày của sinh viên        |
| Pitch Problem Card           | Pitch idea “Smart Wake-up System” — hệ thống báo thức thông minh đánh thức người dùng theo trạng thái ngủ thay vì giờ cố định                                 | Candidate được shortlist vì workflow rõ và có measurable impact tới chất lượng thức dậy |
| Workflow analysis            | Phân tích current workflow của alarm truyền thống và future workflow có sleep-stage prediction                                                                | Nhóm nhìn rõ bottleneck nằm ở việc alarm không biết trạng thái ngủ realtime             |
| Rule / Workflow / Agent      | Chủ động lập luận vì sao bài toán phù hợp với Workflow + ML hơn là Full AI Agent                                                                              | Nhóm thống nhất hướng tiếp cận practical hơn thay vì “AI-first”                         |
| Research / validation        | Tìm hiểu cách hoạt động của các app như Sleep Cycle, Apple Sleep, Fitbit Sleep Tracking                                                                       | Xác nhận pain là có thật và đã có market validation từ các sản phẩm hiện tại            |
| Problem Statement refinement | Điều chỉnh problem statement từ “AI alarm” sang “wake-up optimization problem”                                                                                | Problem rõ workflow hơn và tránh bị solution-first                                      |

---

## Bảng dùng AI trong lab

| Phase                   | Tôi dùng AI để làm gì?                                                          | AI hữu ích ở đâu?                                                                    | AI sai / hời hợt ở đâu?                                                                                          | Tôi sửa gì bằng nhận định của mình?                                                    |
| ----------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Scan cá nhân            | Nhờ AI gợi ý thêm problems liên quan đến giấc ngủ và sinh hoạt sinh viên        | AI giúp mở rộng thêm góc nhìn về sleep tracking, fatigue và snooze behavior          | Một số ý AI đưa ra quá rộng hoặc quá “startup sounding” như “AI health assistant” nhưng không có workflow cụ thể | Chỉ giữ lại các problems có actor rõ, pain thật và xảy ra hằng ngày                    |
| Problem Card            | Nhờ AI phản biện idea Smart Wake-up System theo góc nhìn skeptical PM           | AI chỉ ra assumption “90 phút/cycle” không đúng với mọi người và cần personalization | AI nhiều lần đề xuất dùng Full AI Agent dù workflow chưa cần mức autonomy đó                                     | Kéo lại hướng Workflow + ML prediction vì practical và deterministic hơn               |
| Workflow                | Dùng AI để format lại current/future workflow và xác định AI intervention point | AI giúp tách rõ các bước: tracking → prediction → wake decision → alarm              | AI có xu hướng merge nhiều bước thành “AI agent xử lý toàn bộ” khiến boundary không rõ                           | Tách rõ human boundary và fallback alarm để workflow dễ explain hơn                    |
| Problem Statement       | Dùng AI để refine metric và boundary                                            | AI giúp bổ sung metric như wake freshness, snooze count và oversleep rate            | AI đề xuất thêm nhiều metric khó đo như “daily productivity score” hoặc “mood improvement”                       | Giữ lại các metric có thể đo đơn giản trong MVP như số lần snooze và wake satisfaction |
| Rule / Workflow / Agent | Dùng AI để so sánh 3 hướng triển khai                                           | AI giúp nhìn rõ trade-off giữa Rule, Workflow và Agent                               | AI thường bias sang Agent như một giải pháp “cao cấp hơn”                                                        | Tôi tự chốt rằng Workflow là phù hợp nhất với bài toán hiện tại                        |

---

## Bài học cá nhân

### Điều tôi nhận ra về cách chọn problem

**Problem tốt là problem có workflow và bottleneck rõ, không phải problem nghe “AI” nhất.** Ban đầu tôi nghĩ về “AI Alarm Agent” như một sản phẩm AI phức tạp, nhưng sau khi phân tích workflow thì nhận ra pain thật nằm ở việc alarm hiện tại không biết trạng thái ngủ của người dùng trước khi đánh thức.

**Problem càng gần trải nghiệm thật càng dễ phân tích.** Vì bản thân là sinh viên ở trọ và thường xuyên ngủ muộn, tôi dễ nhìn thấy:

* hành vi snooze
* thức dậy mệt
* ngủ đủ giờ nhưng vẫn uể oải

Những problem này có dấu hiệu thật và lặp lại hằng ngày nên dễ viết workflow và metric hơn các idea quá xa trải nghiệm cá nhân.

### Điều tôi nhận ra về AI

**AI hữu ích nhất ở bước phản biện và structure thinking.** Khi dùng AI để challenge Problem Statement hoặc workflow, AI giúp tôi nhìn ra:

* boundary chưa rõ
* metric chưa cụ thể
* assumption chưa chắc chắn

Điều này hữu ích hơn nhiều so với việc để AI “nghĩ idea thay”.

**AI thường đề xuất Agent quá sớm.** Trong nhiều lần hỏi, AI có xu hướng:

* biến workflow thành autonomous agent
* thêm reasoning không cần thiết
* over-engineering solution

Điều này làm tôi hiểu rõ hơn rằng:

* Agent không phải level “cao hơn”
* nhiều bài toán chỉ cần Workflow + ML là đủ

### Điều tôi nhận ra về workflow thinking

**Workflow là phần quan trọng nhất để xác định AI fit.** Khi vẽ current workflow của alarm truyền thống, tôi thấy rõ:

* bottleneck nằm ở wake timing
* AI chỉ cần can thiệp ở sleep-stage prediction
* không cần tự động hóa toàn bộ hệ thống

Điều này giúp tôi xác định:

* Rule-based đủ cho MVP rất nhỏ
* Workflow + ML phù hợp production
* Full Agent là overkill ở giai đoạn đầu

### Điều tôi nhận ra về làm việc nhóm

**Pitch bằng workflow và metric dễ thuyết phục hơn pitch bằng công nghệ.** Khi tôi nói:

* “alarm hiện tại wake user ở random sleep stage”
* “user snooze 3-4 lần”
* “wake freshness thấp”

mọi người hiểu problem nhanh hơn nhiều so với việc chỉ nói:

* “mình muốn build AI sleep agent”.

**Giải thích vì sao KHÔNG chọn Agent cũng quan trọng như giải thích vì sao chọn Workflow.** Khi nhóm tranh luận giữa Workflow và Agent, việc phân tích:

* latency
* realtime requirement
* deterministic behavior
* fallback

giúp nhóm quyết định rõ ràng hơn thay vì chọn theo cảm giác “Agent nghe advanced hơn”.

---

## Nếu làm lại

```text
Nếu làm lại, tôi sẽ validate problem kỹ hơn bằng cách khảo sát
nhiều sinh viên/người đi làm hơn để đo:
- số lần snooze trung bình
- mức độ mệt sau khi thức dậy
- tỷ lệ người ngủ đủ giờ nhưng vẫn thiếu tỉnh táo

Hiện tại phần validation chủ yếu vẫn ở mức qualitative và dựa trên
trải nghiệm cá nhân hoặc người xung quanh.

Tôi cũng sẽ định nghĩa rõ hơn cách đo “wake freshness”.
Ví dụ:
- user tự chấm điểm tỉnh táo sau khi thức dậy
- số phút để rời khỏi giường
- số lần snooze
- thời gian sử dụng điện thoại sau khi alarm reo

Điều này sẽ giúp success metric cụ thể và dễ đánh giá hơn trong MVP.
```
