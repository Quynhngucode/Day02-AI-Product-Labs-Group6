# 03 — Individual Reflection

Case nhóm chọn: **Gym Buddy — AI hỗ trợ newbie kiểm tra form khi tập gym**

## Đóng góp của tôi trong nhóm

| Hoạt động | Tôi đã làm gì? | Kết quả |
|---|---|---|
| Scan cá nhân | Brainstorm 5 problems xoay quanh trải nghiệm đi gym của người mới và góc nhìn của PT | Nhóm có đủ candidate để so sánh |
| Pitch | Pitch 3 hướng nổi bật là check form khi tập, tổng hợp tiến độ tập luyện và gợi ý bài thay thế khi máy bị chiếm | Problem check form được đưa vào shortlist vì pain rõ và impact lớn |
| Làm slide | Tổng hợp ý chính của nhóm lên slide, sắp xếp lại flow problem → workflow → metric → Rule / Workflow / Agent | Nhóm trình bày mạch lạc hơn, dễ thống nhất decision cuối |
| Group convergence | Cùng nhóm gom các ý thành các cluster như plan tập, progress tracking, form feedback, bài thay thế | Nhóm nhìn rõ bài nào chỉ là app fitness thông thường, bài nào có AI value rõ hơn |
| Workflow / Problem Statement | Cùng chỉnh lại actor, bottleneck, boundary và before/after workflow cho case check form | Problem Statement cuối rõ hơn ở điểm can thiệp của AI và ranh giới với PT thật |
| Decision | Tham gia lập luận vì sao hướng sản phẩm chính là Agent realtime nhưng pilot nhỏ nhất nên đi từ Workflow sau set | Nhóm có decision hợp lý hơn thay vì cố làm realtime ngay từ đầu |

## Bảng dùng AI trong quá trình làm bài

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì |
|---|---|---|---|---|
| Scan problem | Nhờ GPT gợi ý thêm các problem quanh người mới đi gym, PT và workout tracking | Giúp tôi mở rộng từ 1 ý ban đầu sang đủ 5 problem có thể đem đi pitch | Một số gợi ý quá rộng kiểu app fitness toàn diện hoặc meal plan chung chung | Tôi chỉ giữ các problem có workflow thật và pain tôi quan sát được |
| Top 3 / pitch | Nhờ GPT giúp viết lại problem thành câu ngắn, dễ pitch hơn | Nhanh hơn khi biến ý thô thành Problem Card rõ actor và bottleneck | AI có xu hướng làm câu chữ nghe hay nhưng làm pain bị chung chung | Tôi sửa lại để giữ đúng bối cảnh gym newbie và thêm dấu hiệu thật |
| Workflow | Dùng GPT để gợi ý cách tách current workflow và future workflow | Hữu ích khi nhìn ra bước nào là human action, bước nào là AI intervention | AI có lúc nhảy thẳng sang solution mà chưa làm rõ bottleneck | Tôi kéo lại bằng cách vẽ current state trước rồi mới cho AI tham gia ở bước phù hợp |
| Research | Nhờ GPT liệt kê các tool/case liên quan như pose estimation, fitness coach app, camera tracking | Tiết kiệm thời gian tìm keyword và nhóm các hướng giải pháp đã có | Có chỗ AI gợi ý tool đúng tên nhưng diễn giải khá chung, chưa đủ để dùng làm lập luận | Tôi chỉ giữ những ý nhóm kiểm lại được và dùng research như pattern tham khảo |
| Problem Statement / Decision | Nhờ GPT phản biện xem boundary, metric và mức chọn Rule / Workflow / Agent đã chặt chưa | Hữu ích ở bước chỉ ra rủi ro như góc camera, confidence thấp và fallback sang người thật | AI có xu hướng đẩy lên Agent rất nhanh vì nghe “hay” hơn | Nhóm giữ logic problem-first, chấp nhận Agent là hướng chính nhưng pilot bắt đầu từ scope nhỏ |

## Bài học tôi rút ra

- Problem tốt không phải problem nghe hiện đại nhất, mà là problem có actor rõ, workflow rõ và pain đủ thật để đo được.
- Lúc đầu nhóm dễ trượt sang hướng làm một app gym quá rộng. Chỉ khi gom lại theo workflow, nhóm mới thấy “check form trong lúc tập” là pain sắc nhất.
- Việc vẽ before/after workflow giúp tôi hiểu rõ AI nên đứng ở đâu. Nếu chưa có bottleneck rõ thì nói Agent hay Workflow vẫn còn cảm tính.
- Rule không hề “kém” AI. Trong case này, rule như hướng dẫn đặt camera, checklist form cơ bản và fallback an toàn là phần rất quan trọng, cũng như là giới hạn các tư thế có thể hỗ trợ.
- AI giúp tôi đi nhanh hơn ở bước brainstorm, cấu trúc ý và phản biện, nhưng nếu tin ngay output đầu tiên thì rất dễ bị solution-first hoặc scope quá rộng.

Nếu làm lại:

```text
Tôi sẽ dành thêm thời gian validate trực tiếp với nhiều người mới đi gym hơn, vì hiện tại insight đúng nhưng số lượng tín hiệu thực tế vẫn còn ít. Tôi cũng sẽ chốt pilot nhỏ sớm hơn để tránh sa đà vào việc tưởng tượng sản phẩm realtime quá lớn ngay từ đầu.
```

