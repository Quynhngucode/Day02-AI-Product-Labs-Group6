# 01 — Individual Problem Scan

Case cá nhân: **Gym Buddy — AI hỗ trợ người mới đi gym tự tập an toàn hơn**

Nhân vật quan sát: Quỳnh, sinh viên mới bắt đầu đi gym, chưa có nhiều kinh nghiệm và không đủ tài chính để thuê private trainer dài hạn. Khi đi tập, Quỳnh thường tự xem video trên TikTok/YouTube, tự chọn bài tập và tự chỉnh form bằng cách soi gương.

---

## Scan rộng

Tôi chọn các ý **1, 6, 12, 16** từ bảng scan nhóm và phát triển thêm **2 problem mới** để làm phần scan cá nhân. Các problem đều đi từ quan sát workflow thật của người mới đi gym, chưa bắt đầu bằng giải pháp AI.

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Mỗi tuần phải tự lên lịch tập cho từng nhóm cơ: ngực, lưng, chân, vai, tay, core | Người mới đi gym, người tập không có PT | Mất 20–30 phút/tuần để tìm bài và sắp lịch |
| 2 | Tốn thời gian | Không biết máy nào dùng cho nhóm cơ nào, phải hỏi người khác hoặc tự tra cứu | Người mới đi gym | Đứng lâu trong phòng gym nhưng không biết bắt đầu từ đâu |
| 3 | AI có thể tốt hơn | AI có thể tạo báo cáo tiến độ hằng tuần: số buổi tập, mức tạ tăng, nhóm cơ bỏ sót, mức độ tuân thủ | Người tập, PT | PT phải tổng hợp thủ công khi muốn review tiến độ |
| 4 | Pain từ người khác | Người mới sợ tập sai form, sợ chấn thương, ngại hỏi người trong phòng gym | Người mới đi gym | Tập dè dặt, chỉ dùng máy quen thuộc, tránh bài compound |
| 5 | Tốn thời gian | Người mới phải xem nhiều video hướng dẫn nhưng vẫn không biết video nào phù hợp với thể trạng và trình độ của mình | Người mới đi gym | Mất 30–60 phút xem video trước buổi tập nhưng vào phòng gym vẫn bối rối |
| 6 | AI có thể tốt hơn | Người tập không biết sau mỗi set mình sai ở đâu và cần sửa gì cho set tiếp theo | Người mới đi gym, người tự tập không có PT | Quay video lại nhưng chỉ xem bằng cảm tính, không biết lưng/gối/tay có sai kỹ thuật không |

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
| 1 | Người mới sợ tập sai form, sợ chấn thương, không biết mình sai ở đâu khi đang tập | Pain mạnh nhất, impact rõ nhất, khác biệt AI cao nếu có thể nhận xét form hoặc cảnh báo lỗi | Cần xác định phạm vi bài tập nào đủ an toàn để demo trong lab |
| 2 | Không biết máy nào dùng cho nhóm cơ nào, không biết bắt đầu từ đâu trong phòng gym | Workflow rất thật với newbie, dễ validate bằng phỏng vấn nhanh | Có thể giải quyết bằng hướng dẫn tĩnh hoặc checklist, chưa chắc cần AI mạnh |
| 3 | Mỗi tuần phải tự lên lịch tập cho từng nhóm cơ | Lặp lại thường xuyên, dễ làm trong lab, có thể đo thời gian tiết kiệm | Dễ bị giống app fitness thông thường nếu không cá nhân hóa đủ tốt |

---

## Problem Card #1 — Check form khi tự tập gym

**Problem 1 câu:**  
Người mới đi gym tự tập không có PT thường không biết mình đang sai form trong lúc tập, dẫn đến sợ chấn thương, tập dè dặt hoặc tập sai mà không nhận ra.

**Actor:**  
Sinh viên/người mới bắt đầu đi gym, chưa có nhiều kinh nghiệm, không thuê private trainer thường xuyên.

**Thời điểm / bối cảnh:**  
Trong buổi tập tại phòng gym, đặc biệt khi thực hiện các bài dễ sai kỹ thuật như squat, deadlift, bench press hoặc các bài dùng máy lần đầu.

**Current workflow:**

```text
1. Xem video hướng dẫn trên TikTok/YouTube/Google
2. Đến phòng gym và chọn bài/máy tập theo video đã xem
3. Setup tạ hoặc máy tập
4. Tập theo trí nhớ hoặc nhìn người khác tập
5. Tự soi gương hoặc quay video để xem lại
6. Không chắc form đúng hay sai
7. Tiếp tục tập với rủi ro sai động tác hoặc sai nhóm cơ
```

**Bottleneck:**  
Bước 5–6 — người mới không thể tự đánh giá form chính xác trong lúc đang tập. Họ có thể soi gương hoặc xem lại video, nhưng không đủ kiến thức để biết lỗi nằm ở đâu và sửa thế nào.

**Impact:**  

- Có thể gây chấn thương do sai tư thế ở lưng, gối, vai, cổ tay.
- Tập không vào đúng nhóm cơ, làm giảm hiệu quả.
- Người mới dễ nản vì tập nhiều nhưng không thấy tiến bộ.
- Người không có PT thiếu phản hồi trực tiếp trong lúc tập.

**Success metric:**  

- Người dùng nhận được feedback form trong vòng dưới 5 giây sau khi thực hiện set hoặc trong thời gian thực nếu có thể.
- Giảm số lỗi form cơ bản như lưng cong, gối lệch, biên độ sai, tay đặt sai.
- Người dùng biết ít nhất 1–2 lỗi cụ thể cần sửa sau mỗi set.
- Trong demo lab, hệ thống phân loại được form “ổn / cần sửa / nguy hiểm” cho một số bài tập mẫu.

**Non-AI alternative:**  

- Checklist form đúng/sai bằng ảnh minh họa.
- Video hướng dẫn từng bài tập.
- Poster hướng dẫn trên máy tập.
- Hỏi PT hoặc nhân viên phòng gym.

Các cách này có ích nhưng vẫn thiếu feedback cá nhân hóa cho chính động tác của người dùng.

**AI hypothesis:**  
AI có thể hỗ trợ phân tích ảnh/video hoặc camera để nhận diện tư thế cơ thể, chỉ ra lỗi form cơ bản và gợi ý cách sửa. Người dùng vẫn cần tự quyết định dừng/tập tiếp, và các tình huống đau/chấn thương cần chuyển cho người thật.

**Quick gut:**  
Workflow hoặc Agent.

- Nếu chỉ phân tích video sau set: **Workflow**.
- Nếu theo dõi và cảnh báo trong lúc tập: **Agent có kiểm soát**.

---

### Draft current workflow

```text
CURRENT STATE — Newbie tự tập không có PT

[1 Xem video hướng dẫn: 20–30']
→ [2 Đến phòng gym, chọn bài/máy: 10']
→ [3 Setup tạ/máy: 5']
→ [4 Tập theo video/trí nhớ] 
→ [5 Soi gương hoặc quay video]  <-- bottleneck
→ [6 Không biết form đúng hay sai]
→ [7 Tiếp tục tập, vẫn có nguy cơ sai form/chấn thương]
```

---

### Draft future workflow

```text
FUTURE STATE — Gym Buddy hỗ trợ check form

[1 User chọn bài tập muốn thực hiện]
→ [2 App hiển thị checklist form ngắn]        -- Rule
→ [3 User quay video hoặc bật camera]         -- Human action
→ [4 AI phân tích tư thế/form]                -- AI step
→ [5 App chỉ ra lỗi cụ thể và cách sửa]       -- Workflow step
→ [6 User sửa ở set tiếp theo]                -- Human action
→ [7 Nếu nghi rủi ro/chấn thương → hỏi PT]    -- Human boundary

Fallback:
Nếu video mờ, góc quay sai, nhiều người che camera hoặc AI không đủ tự tin,
app không đưa kết luận chắc chắn mà yêu cầu quay lại/gợi ý hỏi PT.
```

---

## Problem Cards #2 và #3 — tóm tắt

| Card | Actor | Bottleneck | Metric | Quick gut | Vì sao chưa chọn làm #1 |
|---|---|---|---|---|---|
| Không biết máy nào dùng cho nhóm cơ nào | Người mới đi gym | Đứng trong phòng gym nhưng không biết chọn máy/bài phù hợp | Giảm thời gian chọn bài/máy từ 10–15 phút xuống dưới 3 phút | Rule / Workflow | Pain rõ nhưng có thể giải quyết bằng hướng dẫn tĩnh, bản đồ máy hoặc checklist; AI không khác biệt bằng check form |
| Tự lên lịch tập tuần | Người mới đi gym, người không có PT | Mất thời gian chia nhóm cơ, chọn bài, set/rep, lịch nghỉ | Giảm thời gian lập lịch từ 20–30 phút xuống dưới 5 phút | Workflow | Dễ làm nhưng khá giống các app fitness hiện có; impact về an toàn thấp hơn bài toán sai form |

---

## Kết luận cá nhân

Sau khi scan các problem, tôi chọn **Check form khi tự tập gym** làm bài toán chính vì đây là pain mạnh nhất của người mới đi gym. Vấn đề không chỉ là “không biết tập bài gì”, mà là **không biết mình đang tập đúng hay sai trong lúc thực hiện động tác**. Đây là bottleneck có impact lớn vì liên quan đến hiệu quả tập luyện và rủi ro chấn thương.

Hướng tiếp cận phù hợp nhất là không bắt đầu bằng một app AI quá lớn, mà bắt đầu từ scope nhỏ:

```text
User gửi video/ảnh bài tập → hệ thống nhận xét lỗi form cơ bản → user sửa ở set tiếp theo.
```

Nếu MVP này hoạt động tốt, có thể phát triển tiếp lên real-time monitoring cho một số bài tập nguy cơ cao.
