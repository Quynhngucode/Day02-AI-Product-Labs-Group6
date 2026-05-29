# 03 — Individual Reflection

## Đóng góp của Quỳnh trong nhóm

| Hoạt động | Quỳnh đã làm gì? | Kết quả |
|---|---|---|
| Scan cá nhân | Đưa ra các problem liên quan đến người mới đi gym như tự lên lịch tập, không biết dùng máy nào, thiếu feedback khi tập sai form | Nhóm có thêm nhiều candidate xoay quanh workflow tự tập gym không có PT |
| Pitch problem | Pitch bài toán “người mới sợ tập sai form, sợ chấn thương, ngại hỏi người khác trong phòng gym” | Bài toán check form được đưa vào shortlist và có điểm cao nhất |
| Before/after | Tham gia xây dựng future workflow cho Gym Buddy: user chọn bài → đặt camera → AI theo dõi form → cảnh báo lỗi → user sửa động tác | Nhóm có before/after workflow rõ để so sánh tác động |
| Risk & fallback | Nêu rủi ro như camera sai góc, phòng gym đông, ánh sáng kém, AI nhận diện nhầm hoặc user có dấu hiệu đau/chấn thương | Nhóm thêm được boundary: khi AI không chắc hoặc có rủi ro sức khỏe thì chuyển sang PT/người thật |

---

## Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì |
|---|---|---|---|---|
| Scan problem | Nhờ AI gợi ý các pain point của người mới đi gym theo 4 lăng kính: lặp lại, tốn thời gian, AI có thể tốt hơn, pain từ người khác | AI giúp mở rộng danh sách problem và không chỉ nghĩ đến “làm app tập gym” ngay từ đầu | Một số gợi ý ban đầu còn chung chung, giống tính năng app hơn là problem thật | Tôi chọn lại các ý có actor rõ, workflow rõ và dấu hiệu thật |
| Grouping | Nhờ AI nhóm các problem thành cluster như planning, tracking, check form, hỏi đáp, nhắc nhở | AI giúp nhìn ra pattern chung giữa nhiều ý tưởng khác nhau | Có lúc nhóm quá nhiều cluster, làm bài bị rộng | Tôi giữ lại các cluster liên quan trực tiếp đến newbie tự tập gym |
| Problem Statement | Nhờ AI chuyển ý tưởng thành Problem Card và Problem Statement | AI giúp viết rõ actor, workflow, bottleneck, impact, success metric, boundary | AI đôi lúc nhảy sang solution quá sớm như app real-time hoặc agent hoàn chỉnh | Tôi chỉnh lại theo hướng problem-first: bắt đầu từ workflow tự tập của newbie trước |
| Workflow before/after | Nhờ AI hỗ trợ viết current state và future state | AI giúp trình bày workflow mạch lạc, dễ đưa vào deliverable | Future workflow ban đầu hơi tham vọng, bao gồm quá nhiều chức năng | Tôi thu hẹp MVP: ưu tiên check form và feedback lỗi cơ bản |
| Risk & boundary | Nhờ AI liệt kê các rủi ro khi dùng AI trong gym | AI giúp nhớ các rủi ro như camera sai góc, nhận diện sai, chấn thương, bệnh nền | Một số rủi ro bị viết quá rộng sang y tế/dinh dưỡng | Tôi giữ boundary rõ: chỉ nhận xét form cơ bản, không chẩn đoán bệnh hay thay PT/bác sĩ |

---

## Bài học của Quỳnh

Qua bài Lab Day 02, tôi nhận ra một problem tốt không phải là problem nghe “AI” nhất, mà là problem có actor cụ thể, workflow thật, bottleneck rõ và có cách đo impact. Ban đầu, tôi dễ nghĩ theo hướng “làm app AI tập gym”, nhưng sau khi phân tích lại thì vấn đề cốt lõi không phải là app, mà là việc người mới đi gym không biết mình đang tập đúng hay sai trong lúc thực hiện động tác.

Việc vẽ workflow giúp tôi thấy rõ pain nằm ở bước tự đánh giá form. Người mới có thể xem rất nhiều video, nhưng khi vào phòng gym thì vẫn không biết lưng, gối, tay hoặc biên độ chuyển động của mình có đúng không. Đây là điểm khiến họ sợ chấn thương, tập dè dặt hoặc chỉ dùng các máy quen thuộc.

Tôi cũng học được rằng không nên chọn Agent chỉ vì Agent nghe mạnh hơn. Với scope lab, hướng hợp lý hơn là bắt đầu bằng Workflow: người dùng quay video hoặc gửi ảnh bài tập, AI phân tích lỗi form cơ bản, sau đó người dùng sửa ở set tiếp theo. Nếu sau này cần cảnh báo ngay trong lúc tập thì mới phát triển lên Agent real-time.

Một bài học khác là AI không nên thay thế hoàn toàn private trainer. Trong bài toán này, AI phù hợp để hỗ trợ newbie ở các lỗi cơ bản và giúp họ tự tin hơn khi tập. Tuy nhiên, khi có dấu hiệu đau, chấn thương, bệnh nền hoặc AI không chắc chắn, hệ thống cần khuyên người dùng hỏi PT, nhân viên phòng gym hoặc chuyên gia y tế.

Nếu làm lại, tôi sẽ validate sớm hơn bằng cách hỏi 3–5 người mới đi gym xem họ sợ nhất điều gì khi tự tập: không biết lịch tập, không biết dùng máy, hay không biết form đúng/sai. Tôi cũng sẽ chọn trước 1–2 bài tập cụ thể, ví dụ squat và bench press, để problem statement không bị quá rộng.

---

## Tôi sẽ sửa gì nếu tiếp tục làm bài này

```text
Tôi sẽ thu hẹp MVP thành:
User quay video một set squat hoặc bench press
→ AI nhận diện một số lỗi form cơ bản
→ AI trả feedback ngắn: lỗi gì, vì sao nguy hiểm, sửa thế nào ở set tiếp theo
→ Nếu video không đủ rõ hoặc có dấu hiệu đau/chấn thương, AI không kết luận và khuyên hỏi người thật.
```

Lý do là scope này đủ nhỏ để làm trong lab, vẫn thể hiện được giá trị AI, đồng thời tránh việc bài toán bị biến thành một app fitness quá lớn.
