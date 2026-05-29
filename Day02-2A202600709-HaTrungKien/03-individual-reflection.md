## 03 — Individual Reflection

### Đóng góp cá nhân trong nhóm

| Hoạt động | Em đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| **Scan cá nhân** | Brainstorm và đưa ra 8 problems xoay quanh trải nghiệm thực tế của newbie khi mới bắt đầu đi tập gym. | Nhóm có danh sách vấn đề ban đầu để thảo luận và chọn được hướng chính là "Form dáng". |
| **Pitching** | Tham gia pitching ý tưởng của nhóm và trả lời một số câu hỏi phản biện từ các nhóm khác. | Giúp nhóm làm rõ hơn lý do chọn vấn đề này và sản phẩm được hiểu đúng hơn. |
| **Problem Statement** | Viết nháp phần Problem Statement v0 và chỉnh tiếp sang v1 theo góp ý của nhóm. | Giúp nhóm xác định rõ hơn Actor, Bottleneck và Metric cơ bản cho bài toán. |
| **Rule / Workflow / Agent** | Đưa ra lý do chọn **Agent** thay vì chỉ dừng ở Workflow. | Nhóm thống nhất được decision: bài toán check form cần phản hồi Real-time Agent vì nếu người tập sai động tác thì cần cảnh báo ngay lúc đó, còn feedback sau set (Workflow) chỉ phù hợp để xem lại chứ khó giúp tránh chấn thương kịp thời. |

### Bảng dùng AI trong quá trình làm lab

| Phase | Em dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| **Scan** | Nhờ AI gợi ý thêm các vấn đề mà người mới đi tập gym có thể gặp. | Giúp mở rộng nhanh các pain point như lịch tập, dinh dưỡng, ghi log, thời gian nghỉ và tập sai form. | Một số gợi ý còn khá chung, giống các app fitness phổ biến như đếm rep hoặc đếm calo. | Em lọc lại và chọn ý "ảnh hưởng sức khỏe do sai form" vì đây là vấn đề rõ ràng hơn và có hậu quả thực tế hơn. |
| **Problem Statement** | Nhờ AI hỗ trợ sắp xếp ý và viết lại các trường trong Statement v0, v1. | Giúp câu chữ gọn hơn và bám đúng format yêu cầu của lab. | Metric AI đưa ra còn cảm tính, ví dụ như "giúp người dùng tập tốt hơn" hoặc "giảm nguy cơ chấn thương". | Em tự chỉnh lại Success Metric theo hướng cụ thể hơn như phát hiện lỗi form, phản hồi nhanh và người dùng hiểu được cảnh báo. |
| **Rule / Workflow / Agent** | Nhờ AI so sánh các hướng Rule, Workflow và Agent cho bài toán check form. | Giúp chỉ ra rằng trước khi dùng Agent vẫn cần một số rule cơ bản như căn góc camera và chọn bài tập. | AI có lúc đề xuất hướng an toàn quá mức, nghiêng về Workflow kiểu quay video rồi phân tích sau. | Em giữ hướng Agent vì bài toán sửa dáng cần phản hồi real-time, nhưng bổ sung bước Rule để kiểm tra góc máy trước khi Agent chạy. |
| **Hoàn thiện** | Nhờ AI rà soát lại logic và cách diễn đạt trong báo cáo trước khi nộp. | Giúp phát hiện vài đoạn chuyển ý chưa mượt và một số chỗ bị lặp ý. | Đôi khi AI tự mở rộng thêm nhiều tính năng ngoài scope như gợi ý lịch tập, dinh dưỡng hoặc tracking tiến độ. | Em xóa bớt các phần thừa và giữ phạm vi nhóm tập trung vào một vấn đề chính: Check form lúc tập. |

### Bài học cá nhân

* **Problem tốt nên xuất phát từ tình huống thật:** Ban đầu em nghĩ app cá nhân hóa lịch tập là hướng đáng làm, nhưng sau khi phân tích kỹ hơn, em thấy việc tập sai form đáng ưu tiên hơn vì nó có thể gây đau hoặc chấn thương thật, nhất là với người mới chưa có PT.
* **AI chỉ nên đóng vai trò hỗ trợ, không nên thay mình quyết định:** AI giúp brainstorm, phản biện và viết lại nội dung nhanh hơn, nhưng nhiều gợi ý vẫn khá chung chung. Người làm sản phẩm vẫn phải tự chọn vấn đề, tự giới hạn scope và bảo vệ quyết định của mình.

* **Nếu làm lại:** Em sẽ hỏi thử 3-5 bạn sinh viên hoặc người mới đi tập gym để kiểm chứng xem họ có thật sự gặp những bottleneck mà nhóm đã chọn không.
