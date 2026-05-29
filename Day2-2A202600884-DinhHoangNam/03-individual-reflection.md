# 03 — Individual Reflection

> Học viên: Đinh Hoàng Nam - Mã học viên: 2A202600884
> Nhóm 8

---

## Đóng góp của tôi trong nhóm

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| Scan cá nhân | Scan 11 problems từ trải nghiệm làm báo cáo Dự án, đa dạng 4 lăng kính | Nhóm có thêm cluster B (Học tập) với 3 candidates rõ ràng |
| Pitch Problem Card | Pitch "Viết báo cáo Dự án từ file rời rạc" với workflow 7 bước và baseline 1-2 ngày | Candidate vào shortlist, điểm ngang với problem ăn uống (34/35) |
| Gom trùng / cluster | Đề xuất tạo cluster B (Học tập) để tách khỏi cluster Đời sống | Nhóm có thêm clusters, tránh bỏ sót domain quan trọng |
| Chọn candidate problem | Đồng thuận chọn problem ăn uống thay vì problem Dự án của mình | Thực hành được tinh thần "problem first": bài tốt hơn không phải bài của mình |
| Research | Hỏi nhanh 3 sinh viên ở trọ | Nhóm thấy không cần build agent; xác nhận pain ở bước nghĩ món là thật |
| Rule / Workflow / Agent | Lập luận chọn Workflow, không chọn Agent | Nhóm thống nhất decision, tránh "AI-first" |

---

## Bảng dùng AI trong lab

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan cá nhân | Hỏi AI gợi ý thêm problem theo role sinh viên làm báo cáo sau khi tự scan trước | Giúp nhớ thêm "Báo cáo văn phong không nhất quán" (problem #11) và gợi ý lăng kính "Pain từ người khác" | AI gợi ý một số ý quá chung chung như "quản lý dự án phức tạp" không có actor rõ | Bỏ các ý không có dấu hiệu thật; chỉ giữ ý có workflow và người gặp vấn đề cụ thể |
| Problem Card | Dùng AI phản biện Problem Card #1 theo prompt skeptical PM | Chỉ ra metric "đủ tốt về nội dung" chưa đo được; hỏi boundary giữa AI hỗ trợ và AI viết hộ | AI đề xuất luôn sang Agent (tự gom file, tự phát hiện trùng, tự viết) trước khi nhóm chọn level | Kéo lại về Workflow; nhấn mạnh người viết chính vẫn phải review và chịu trách nhiệm nội dung |
| Workflow | Nhờ AI vẽ lại current/future workflow từ mô tả text | Nhanh hơn khi format ASCII, gợi ý thêm bước "Fallback" | AI gộp bước "phát hiện trùng lặp" và "viết lại nối mạch" thành 1 bước, che khuất bottleneck thật | Tách lại vì bottleneck nằm đúng ở bước nối mạch, không phải bước phát hiện trùng |
| Problem Statement | Nhờ AI phản biện field còn mơ hồ trong PS v0 | Chỉ ra success metric "giảm mua thiếu/thừa" chưa có baseline rõ | AI đề xuất thêm metric "user satisfaction score" - quá rộng cho pilot nhỏ | Nhóm giữ metric đơn giản: thời gian + số lần mua thiếu/thừa, đo được trong 1 tuần pilot |

---

## Bài học cá nhân

### Điều tôi nhận ra về cách chọn problem

**Problem tốt không phải problem nghe "AI" nhất.** Candidate "Viết báo cáo Dự án" và candidate "Nghĩ món ăn" có điểm bằng nhau (34/35), nhưng nhóm chọn bài ăn uống vì dễ trình bày hơn và ít rủi ro diễn giải hơn. Tôi học được rằng ngoài chất lượng kỹ thuật, còn cần nghĩ đến khả năng giải thích và defend bài trước người nghe.

**Bắt đầu từ trải nghiệm thật giúp tìm bottleneck nhanh hơn.** Vì tôi trực tiếp làm báo cáo Dự án, tôi scan được 11 problems với dấu hiệu thật (giờ cụ thể, hành động cụ thể). Những problem này dễ viết workflow hơn nhiều so với problem nghe qua.

### Điều tôi nhận ra về AI

**AI hữu ích nhất ở bước phản biện, không phải bước tạo ra.** Khi dùng AI để phản biện Problem Card, AI chỉ ra điểm yếu trong metric và boundary rất nhanh. Nhưng khi để AI "gợi ý problem", kết quả hay quá chung chung và không có dấu hiệu thật.

**Phải tự scan trước, AI sau.** Nếu mở AI ngay từ đầu, rất dễ bị kéo theo ý của AI mà không có trải nghiệm thật để kiểm chứng. Scan tay trước giúp tôi biết ý nào của AI là thật và ý nào là lý thuyết.

**AI hay đề xuất Agent quá sớm.** Trong cả hai lần dùng AI (phản biện Problem Card và research), AI đều gợi ý sang Agent dù bài toán chưa cần. Đây là dấu hiệu cần tự đặt câu hỏi: "Workflow có giải được không?" trước khi nghĩ đến Agent.

### Điều tôi nhận ra về làm việc nhóm

**Pitch ngắn, rõ bottleneck giúp nhóm quyết định nhanh hơn.** Khi tôi pitch "Viết báo cáo - bottleneck tại bước nối mạch - mất 4-6 tiếng", nhóm hiểu ngay và có thể đặt câu hỏi trúng. Các pitch mơ hồ hơn mất nhiều thời gian giải thích hơn.

**Challenge đúng trọng tâm quan trọng hơn challenge nhiều.** Câu hỏi về sensor data của Smart Wake-up giúp nhóm thấy rủi ro kỹ thuật thật, dẫn đến quyết định không chọn. Một câu hỏi đúng chỗ có giá trị hơn nhiều câu hỏi chung chung.

---

## Nếu làm lại

```text
Tôi sẽ validate thêm với 3-5 sinh viên ở trọ thực tế trước khi chốt baseline
"25-40 phút/lần nghĩ món", vì con số này hiện chủ yếu đến từ phỏng vấn nhanh trong lớp.
Baseline chắc hơn sẽ giúp success metric (giảm xuống dưới 10 phút) thuyết phục hơn.

Tôi cũng sẽ thử vẽ workflow tay trên giấy trước khi số hóa, vì bước vẽ tay
ép tôi nghĩ rõ từng bước thay vì để AI format thay. Lần này tôi đã số hóa ngay
và suýt bỏ sót bottleneck thật khi AI gộp bước.
```

