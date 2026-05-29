# 01 — Individual Problem Scan

Case ví dụ: **Gym Buddy — AI hỗ trợ newbie kiểm tra form khi tập gym**

Nhân vật ví dụ: Thảo, 23 tuổi, mới đi gym được vài tháng. Mỗi buổi Thảo phải tự nhớ mình đã tập bao nhiêu set, rep, mức tạ và nghỉ bao lâu.

## Scan rộng

Bối cảnh tôi quan sát là người mới đi gym, người tập không có PT theo sát, và private trainer đang quản lý nhiều học viên cùng lúc. Những vấn đề dưới đây đều xuất phát từ workflow tập luyện và theo dõi tiến độ thật.

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Mỗi buổi tập phải ghi lại số set, số rep, mức tạ, thời gian nghỉ | Người tập gym, PT | Nhiều người ghi thủ công trên note/app hoặc quên ghi |
| 2 | Tốn thời gian | PT phải theo dõi tiến độ nhiều học viên cùng lúc, gồm lịch tập, mức tạ, cân nặng, body measurement | Private trainer | Dễ bỏ sót tiến độ nếu quản lý bằng Excel, note hoặc chat |
| 3 | AI có thể tốt hơn | AI có thể tạo báo cáo tiến độ hằng tuần: số buổi tập, mức tạ tăng, nhóm cơ bỏ sót, mức độ tuân thủ | Người tập, PT | PT phải tổng hợp thủ công khi muốn review tiến độ |
| 4 | Pain từ người khác | Người mới không biết form squat, deadlift, bench press đúng hay sai trong lúc tập nên hoặc tập sai, hoặc né bài compound | Newbie tự tập, sinh viên, người không có PT | Hay soi gương, quay video, hỏi bạn cùng tập hoặc bỏ qua bài vì sợ chấn thương |
| 5 | Tốn thời gian | Khi máy bị chiếm hoặc phòng gym đông, người mới không biết đổi sang bài nào tương đương nên mất thời gian tìm bài thay thế giữa buổi tập | Newbie tự tập | Đứng chờ máy, mở TikTok/YouTube tìm bài thay thế, buổi tập bị ngắt mạch |


Vì sao phần scan này mạnh:

- Có actor cụ thể: người mới đi gym, sinh viên, người không có PT.
- Có workflow lặp lại hằng tuần và hằng buổi tập.
- Có pain thật: sợ sai form, sợ chấn thương, không biết bắt đầu từ đâu.
- Có dấu hiệu đo được: thời gian tìm bài, thời gian xem video, số lần phải tự tra cứu.
- Không bắt đầu bằng “làm app AI”, mà bắt đầu từ khó khăn trong quy trình tự tập.

---

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Check form squat, deadlift, bench press cho newbie trong lúc tập | Pain rõ, actor rõ, rủi ro chấn thương cao, workflow dễ vẽ, AI value nổi bật hơn app fitness thông thường | Camera đặt sai góc có làm feedback kém tin cậy không |
| 2 | Tự động tổng hợp tiến độ tập luyện hằng tuần cho người tập và PT | Có workflow lặp lại, dữ liệu tương đối rõ, impact đo được bằng thời gian tổng hợp và độ đầy đủ report | Nếu dữ liệu đầu vào ghi thiếu hoặc sai thì report có còn hữu ích không |
| 3 | Gợi ý bài tập thay thế khi máy bị chiếm hoặc thiếu dụng cụ | Xảy ra rất thường xuyên ở phòng gym đông, giúp buổi tập không bị ngắt mạch | Cần dữ liệu đủ tốt về nhóm cơ, thiết bị và mức độ khó để gợi ý hợp lý |

## Problem Card #1 — Check form khi tập gym

**Problem 1 câu:**  
Người mới đi gym không biết form squat, deadlift hoặc bench press của mình đúng hay sai trong lúc thực hiện động tác, nên hoặc tập sai mà không biết, hoặc né các bài compound vì sợ chấn thương.

**Actor:**  
Sinh viên, người mới đi gym, tự tập không có PT theo sát.

**Thời điểm / bối cảnh:**  
Trong buổi tập, đặc biệt ở các bài compound cần phối hợp nhiều khớp và dễ sai kỹ thuật.

**Current workflow:**

```text
1. Chọn bài tập trên app/TikTok/YouTube
2. Xem video mẫu và cố nhớ kỹ thuật
3. Setup tạ hoặc máy
4. Thực hiện 1 set thử
5. Tự soi gương hoặc tự cảm nhận xem có sai không
6. Nếu vẫn không chắc thì quay video hoặc hỏi người khác
7. Sửa lại hoặc bỏ qua bài tập đó
```

**Bottleneck:**  
Bước 5-6. Người mới không thể vừa nâng tạ vừa tự đánh giá chính xác lưng, gối, tay và biên độ động tác.

**Impact:**  
Tập sai có thể gây đau lưng, đau khớp, không vào đúng nhóm cơ, tốn thời gian và làm người tập mất tự tin với các bài quan trọng.

**Success metric:**  
Giảm số lần user phải dừng set để xem lại video hoặc hỏi người khác; phát hiện được lỗi form cơ bản trong lúc tập; tăng tỷ lệ user sửa đúng lỗi ở set tiếp theo.

**Non-AI alternative:**  
Checklist form đúng/sai, gương tập, biển hướng dẫn ở máy, hoặc nhờ PT/nhân viên phòng gym quan sát.

**AI hypothesis:**  
AI dùng camera để theo dõi pose và cảnh báo khi phát hiện lỗi form cơ bản hoặc góc đặt máy không phù hợp.

**Quick gut:**  
Agent.

### Draft current workflow

```text
CURRENT STATE

[1 Xem video mẫu: 3-5']
→ [2 Setup tạ/máy: 2']
→ [3 Tập set thử: 1']
→ [4 Tự soi gương / tự cảm nhận: 1-2']  <-- bottleneck
→ [5 Quay lại hoặc hỏi người khác nếu không chắc: 2-5']
→ [6 Sửa hoặc bỏ bài]
```

### Draft future workflow

```text
FUTURE STATE

[1 Đặt điện thoại ở góc chuẩn]
→ [2 App kiểm tra khung hình và ánh sáng]
→ [3 User bấm Start và thực hiện set]
→ [4 AI theo dõi realtime, cảnh báo lỗi form cơ bản]
→ [5 Sau set, app tóm tắt 1-2 lỗi chính và cách sửa]

Fallback: nếu góc quay xấu hoặc confidence thấp, app dừng đánh giá và khuyên hỏi PT/người có kinh nghiệm.
```

## Problem Card #2 — Tổng hợp tiến độ tập luyện hằng tuần

**Problem 1 câu:**  
PT và người tập mất thời gian gom workout log, cân nặng và body measurement để biết tuần này có tiến bộ thật hay không.

**Actor:**  
Private trainer đang quản lý nhiều học viên, và người tập muốn theo dõi tiến độ của chính mình.

**Thời điểm / bối cảnh:**  
Cuối tuần hoặc trước buổi review giáo án, khi cần nhìn lại số buổi tập, mức tạ tăng và mức độ tuân thủ.

**Current workflow:**

```text
1. Mỗi buổi người tập ghi set/rep/mức tạ bằng note hoặc app
2. PT hỏi lại lịch tập, cân nặng, cảm giác buổi tập qua chat
3. Cuối tuần PT mở nhiều nguồn dữ liệu khác nhau
4. PT tự tổng hợp xem học viên có tập đủ không, có tăng tạ không
5. PT viết nhận xét và điều chỉnh giáo án tuần sau
```

**Bottleneck:**  
Bước 3-4. Dữ liệu nằm rải rác và dễ thiếu, nên PT phải ghép thủ công trước khi ra được insight.

**Impact:**  
PT dễ bỏ sót học viên tụt tiến độ, người tập không thấy rõ mình đang cải thiện ở đâu, và việc review trở nên chậm, cảm tính.

**Success metric:**  
Giảm thời gian tổng hợp tiến độ cho mỗi học viên; tăng tỷ lệ log được điền đầy đủ; giúp PT phát hiện sớm học viên bỏ buổi hoặc chững mức tạ.

**Non-AI alternative:**  
Mẫu Excel/Google Sheet chuẩn hoặc app log tập cơ bản với dashboard cố định.

**AI hypothesis:**  
AI tự gom log, tóm tắt xu hướng chính trong tuần và gợi ý điểm cần chú ý cho PT hoặc người tập.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE

[1 Thu log từ note/app/chat]
→ [2 Mở từng học viên hoặc từng buổi tập]
→ [3 So sánh số buổi, mức tạ, cân nặng]  <-- bottleneck
→ [4 Viết nhận xét thủ công]
→ [5 Gửi review hoặc chỉnh giáo án]
```

### Draft future workflow

```text
FUTURE STATE

[1 Log được nhập hoặc đồng bộ sau mỗi buổi]
→ [2 Hệ thống gom dữ liệu theo tuần]
→ [3 AI tạo summary: số buổi tập, mức tạ tăng, nhóm cơ bỏ sót]
→ [4 PT review và chỉnh khuyến nghị trước khi gửi]

Fallback: nếu log thiếu nhiều hoặc bất thường, hệ thống chỉ báo "dữ liệu chưa đủ để kết luận".
```

## Problem Card #3 — Gợi ý bài tập thay thế khi máy bị chiếm

**Problem 1 câu:**  
Khi máy bị chiếm hoặc thiếu dụng cụ, người mới đi gym không biết nên đổi sang bài nào tương đương nên buổi tập bị ngắt mạch hoặc bỏ luôn bài đó.

**Actor:**  
Người mới đi gym, chưa quen nhiều biến thể bài tập.

**Thời điểm / bối cảnh:**  
Giờ cao điểm ở phòng gym, khi thiết bị phổ biến như cable, smith machine hoặc bench thường kín người.

**Current workflow:**

```text
1. Đến khu vực máy theo lịch tập
2. Thấy máy đang có người dùng
3. Chờ máy trống hoặc đi loanh quanh
4. Tự search TikTok/YouTube/xem app để tìm bài thay thế
5. Chọn đại một bài hoặc bỏ qua nhóm cơ đó
```

**Bottleneck:**  
Bước 3-4. Người tập không biết bài nào thay được mà vẫn đúng nhóm cơ, đúng mức độ khó và đúng thiết bị còn trống.

**Impact:**  
Buổi tập bị kéo dài, mất nhịp, dễ bỏ bài quan trọng và giảm động lực quay lại phòng gym đông.

**Success metric:**  
Giảm thời gian đứng chờ hoặc tìm bài thay thế; giảm số bài bị bỏ qua vì thiếu thiết bị; tăng độ liền mạch của buổi tập.

**Non-AI alternative:**  
Danh sách bài thay thế cố định theo từng máy hoặc poster gắn ở phòng gym.

**AI hypothesis:**  
AI gợi ý bài thay thế theo mục tiêu buổi tập, nhóm cơ, thiết bị còn trống và kinh nghiệm của user.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE

[1 Theo lịch đến máy]
→ [2 Máy bị chiếm]
→ [3 Chờ hoặc đi tìm máy khác]
→ [4 Search bài thay thế: 3-8']  <-- bottleneck
→ [5 Tập tiếp hoặc bỏ qua]
```

### Draft future workflow

```text
FUTURE STATE

[1 User báo máy bị chiếm hoặc chụp nhanh khu vực thiết bị]
→ [2 App hỏi mục tiêu bài tập hiện tại]
→ [3 Hệ thống gợi ý 2-3 bài thay thế phù hợp]
→ [4 User chọn bài và tiếp tục buổi tập]

Fallback: nếu không có bài thay thế đủ an toàn cho newbie, app khuyên đổi thứ tự bài tập thay vì cố chọn đại.
```

