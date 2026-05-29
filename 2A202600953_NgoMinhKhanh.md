# Smart Wake-up System dựa trên chu kỳ giấc ngủ

> Case: Smart Wake-up System / AI Alarm dựa trên trạng thái giấc ngủ realtime.

Nhân vật: Khánh, sinh viên đại học thường xuyên ngủ không đều do học và làm project ban đêm. Dù đặt báo thức đúng giờ, Khánh thường thức dậy trong trạng thái mệt, choáng hoặc rất khó tỉnh táo.

---

# 01 — Individual Problem Scan

## Scan rộng

| #  | Lăng kính          | Problem quan sát được                                       | Ai đang đau?                   | Dấu hiệu thật                 |
| -- | ------------------ | ----------------------------------------------------------- | ------------------------------ | ----------------------------- |
| 1  | Lặp lại            | Báo thức reo đúng giờ nhưng vẫn thức dậy rất mệt            | Sinh viên, người đi làm        | Xảy ra gần như mỗi ngày       |
| 2  | Tốn thời gian      | Người dùng snooze nhiều lần rồi ngủ quên                    | Người đi làm                   | Trễ học/trễ làm               |
| 3  | AI có thể tốt hơn  | Báo thức hiện tại không xét trạng thái ngủ thực tế          | Người dùng smartphone          | Alarm cố định theo giờ        |
| 4  | Pain từ người khác | Smartwatch có tracking nhưng không tối ưu thời điểm wake-up | Người dùng wearable            | Data có nhưng chưa action     |
| 5  | Tốn thời gian      | Người dùng ngủ đủ giờ nhưng vẫn mệt                         | Sinh viên, nhân viên văn phòng | Sleep quality thấp            |
| 6  | AI có thể tốt hơn  | Người dùng không biết chu kỳ ngủ của mình                   | Người dùng smartwatch          | Không có personalized insight |
| 7  | Pain từ người khác | Alarm đánh thức lúc deep sleep gây khó chịu                 | Người ngủ không sâu            | Khó tỉnh táo 30-60 phút đầu   |
| 8  | Lặp lại            | Người dùng thức khuya nhưng vẫn đặt alarm cố định           | Sinh viên                      | Sleep debt tích tụ            |
| 9  | AI có thể tốt hơn  | App alarm hiện tại không học thói quen cá nhân              | Người dùng mobile              | Wake-up không cá nhân hóa     |
| 10 | Pain từ người khác | Người dùng muốn ngủ thêm 5 phút nhưng lại oversleep         | Người đi làm                   | Snooze loop                   |

---

## Top 3

| Rank | Problem                    | Vì sao chọn                              | Điều còn chưa chắc                           |
| ---- | -------------------------- | ---------------------------------------- | -------------------------------------------- |
| 1    | Smart Wake-up              | Workflow rõ, AI fit mạnh, impact đo được | Sleep-stage prediction có đủ chính xác không |
| 2    | Snooze Loop                | Pain phổ biến                            | Có thể chỉ cần behavioral design             |
| 3    | Personalized Sleep Insight | Có long-term value                       | Scope dễ quá rộng                            |

---

# Problem Card #1 — Smart Wake-up

## Problem 1 câu

Người dùng thường thức dậy trong trạng thái mệt do báo thức cố định không xét trạng thái giấc ngủ thực tế.

---

## Actor

Sinh viên hoặc người đi làm sử dụng điện thoại/smartwatch để đặt báo thức hằng ngày.

---

## Thời điểm / bối cảnh

Ban đêm đến sáng hôm sau, trước giờ người dùng muốn thức dậy.

---

## Current workflow

```text
1. Người dùng đặt giờ báo thức cố định
2. Người dùng đi ngủ
3. Alarm reo đúng giờ đã đặt
4. Người dùng bị đánh thức bất kể đang deep sleep hay light sleep
5. Người dùng snooze hoặc thức dậy trong trạng thái mệt
```

---

## Bottleneck

Alarm không biết trạng thái ngủ realtime của người dùng trước khi đánh thức.

---

## Impact

* Người dùng tỉnh dậy mệt dù ngủ đủ giờ
* Giảm tỉnh táo buổi sáng
* Snooze nhiều lần
* Dễ trễ học/trễ làm

---

## Success metric

* Giảm số lần snooze
* Tăng wake-up satisfaction score
* Giảm thời gian “uể oải” sau khi thức dậy
* Người dùng thức dậy đúng hoặc gần đúng giờ mục tiêu

---

## Non-AI alternative

* Alarm window cố định
* Heuristic 90 phút/cycle
* Sleep hygiene recommendations

---

## AI hypothesis

Sử dụng dữ liệu từ:

* smartwatch
* accelerometer
* heart rate
* HRV
* screen off time

để dự đoán:

* light sleep
* deep sleep
* REM

sau đó chọn thời điểm tối ưu để đánh thức người dùng trong khoảng thời gian cho phép.

---

## Quick gut

Workflow.

---

# Draft current workflow

```text
CURRENT STATE

[User đặt alarm cố định]
→ [User ngủ]
→ [Alarm reo đúng giờ]
→ [Wake-up regardless of sleep stage]
→ [Mệt / snooze / oversleep]
```

---

# Draft future workflow

```text
FUTURE STATE

[User đặt giờ muốn thức dậy]
→ [System tracking sleep data]
→ [ML predict sleep stage]
→ [Decision engine chọn thời điểm wake tối ưu]
→ [Smart alarm đánh thức]
→ [User wake trong light sleep]

Fallback:
Nếu prediction fail → alarm vẫn reo ở giờ cuối cùng user yêu cầu.
```

---

# 02 — Group Problem Statement

## Group convergence

| Cluster      | Candidate examples                 | Pattern chung                |
| ------------ | ---------------------------------- | ---------------------------- |
| Productivity | Smart Wake-up, Smart Reminder      | Tối ưu trạng thái người dùng |
| Health-tech  | Sleep tracking, Fatigue prediction | Dùng biometric data          |
| Behavioral   | Snooze loop, Sleep habit           | Người dùng khó tự kiểm soát  |

Nhóm chọn:
Smart Wake-up System.

---

## Vì sao chọn

* Workflow rõ
* Pain phổ biến
* Có measurable metric
* Có thể so sánh Rule / Workflow / Agent
* Có wearable/mobile data available

---

## Quick validation

### Quick interview

Nhóm hỏi nhanh 5 sinh viên/người đi làm:

| Nguồn           | Số người | Tín hiệu xác nhận                               | Tín hiệu phản bác               | Nhóm sửa problem thế nào                                                   |
| --------------- | -------: | ----------------------------------------------- | ------------------------------- | -------------------------------------------------------------------------- |
| Quick interview |        5 | 4/5 nói thường xuyên thức dậy mệt dù ngủ đủ giờ | 1 người nói chỉ cần ngủ sớm hơn | Thu hẹp problem vào “wake timing optimization” thay vì “sleep improvement” |

---

## Research giải pháp

| Tool / Case     | Họ giải quyết phần nào? | Điểm mạnh        | Khoảng trống                  |
| --------------- | ----------------------- | ---------------- | ----------------------------- |
| Sleep Cycle App | Smart alarm window      | Dễ dùng          | Không cá nhân hóa mạnh        |
| Fitbit Sleep    | Sleep tracking          | Có wearable data | Wake optimization còn hạn chế |
| Apple Sleep     | Sleep analytics         | Ecosystem mạnh   | Không fully adaptive          |

---

## Research takeaway

```text
Pain thật không nằm ở việc đặt báo thức, mà nằm ở việc alarm hiện tại không biết trạng thái ngủ thực tế của người dùng.
```

---

# Workflow before/after

## CURRENT STATE

```text
[Set fixed alarm]
→ [Sleep]
→ [Alarm rings]
→ [Wake during random sleep stage]
→ [Fatigue / snooze]
```

---

## FUTURE STATE

```text
[Set desired wake-up time]
→ [Collect sensor data]
→ [Sleep-stage prediction]
→ [Wake-up optimization]
→ [Smart alarm wake-up]

Fallback:
Nếu model không chắc chắn → wake ở deadline cuối cùng.
```

---

## Before/after impact

| Metric                |    Trước | Sau kỳ vọng |
| --------------------- | -------: | ----------: |
| Snooze count          |  3-4 lần |      <1 lần |
| Wake freshness        |     Thấp |     Cao hơn |
| Oversleep rate        |      Cao |    Thấp hơn |
| Sleep-stage awareness | Không có |          Có |

---

# Problem Statement v0

| Field          | Nội dung                          |
| -------------- | --------------------------------- |
| Actor          | Người dùng smartphone/smartwatch  |
| Workflow       | Set alarm → sleep → fixed wake-up |
| Bottleneck     | Alarm không biết sleep stage      |
| Impact         | Mệt sau khi thức dậy              |
| Success Metric | Giảm snooze, tăng wake freshness  |
| Boundary       | Không thay thế thiết bị y tế      |

---

# Rule / Workflow / Agent

| Mức      | Phương án                           | Khi nào đủ              | Rủi ro            | Chọn?             |
| -------- | ----------------------------------- | ----------------------- | ----------------- | ----------------- |
| Rule     | 90 phút/cycle heuristic             | MVP đơn giản            | Không cá nhân hóa | Dùng cho fallback |
| Workflow | Sensor → prediction → wake decision | Workflow rõ và realtime | Prediction sai    | Chọn              |
| Agent    | Tự học habit dài hạn                | Future personalization  | Over-engineering  | Chưa chọn         |

---

## Mức chọn

Workflow.

---

## Vì sao

* Pipeline khá rõ:

  * tracking
  * prediction
  * decision
  * alarm
* Không cần planning phức tạp kiểu autonomous agent
* Realtime system cần deterministic hơn LLM agent

---

# Problem Statement v1

| Field                   | Nội dung                                                                       |
| ----------------------- | ------------------------------------------------------------------------------ |
| Actor                   | Người dùng smartphone/smartwatch                                               |
| Workflow                | Set wake-up time → sleep tracking → sleep-stage prediction → optimized wake-up |
| Bottleneck              | Alarm không biết trạng thái ngủ realtime                                       |
| Impact                  | Fatigue, snooze, oversleep                                                     |
| Success Metric          | Giảm snooze, tăng wake freshness                                               |
| Boundary                | Không thay thế chẩn đoán y tế; không wake quá giờ user cho phép                |
| AI intervention point   | Sleep-stage prediction + wake timing                                           |
| Mức chọn                | Workflow                                                                       |
| Rủi ro & human boundary | Prediction sai → fallback alarm cố định                                        |

---

# Final decision

## Decision

Go với MVP nhỏ.

---

## Pilot nhỏ nhất

* Flutter mobile app
* User nhập:

  * giờ muốn dậy
  * giờ đi ngủ
* Dùng:

  * accelerometer
  * screen-off time
* Wake trong khoảng 15-30 phút trước deadline

---

## Nếu MVP tốt

Phase tiếp theo:

* smartwatch integration
* HR/HRV prediction
* personalized sleep profile

---

## Exit / rollback

Nếu:

* prediction không tốt hơn alarm thường
* user vẫn snooze nhiều
* sensor data quá noisy

thì rollback về:

* smart alarm window heuristic
* non-AI optimization

---

## Decision rationale

* Problem rõ
* Workflow rõ
* Có measurable metrics
* Có non-AI fallback
* Workflow phù hợp hơn Agent
* Có thể build MVP tương đối nhanh
