## 03 — Individual Reflection

### Đóng góp cá nhân trong nhóm

| Hoạt động | Em đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| **Scan cá nhân** | Brainstorm và đưa ra 8 problems tập trung vào trải nghiệm của newbie đi tập gym. | Nhóm có danh sách ứng viên chất lượng và chốt được vấn đề "Form dáng". |
| **Pitching** | Trực tiếp pitching và trả lời câu hỏi phản biện của các nhóm khác | Giúp sản phẩm được đánh giá cao hơn |
| **Problem Statement** | Viết phần Problem Statement v0 và v1. | Định hình cực kỳ rõ ràng Actor, Bottleneck và Metric cụ thể cho nhóm. |
| **Rule / Workflow / Agent** | Lập luận mạnh mẽ bảo vệ việc chọn **Agent** thay vì Workflow. | Nhóm thống nhất được decision: bài toán check form bắt buộc phải là Real-time Agent vì chấn thương xảy ra trong tích tắc, feedback sau set (Workflow) là vô nghĩa với an toàn sức khỏe. |

### Bảng dùng AI trong quá trình làm lab

| Phase | Em dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| **Scan** | Nhờ AI brainstorm và mở rộng các vấn đề khi đi tập gym. | Giúp liệt kê nhanh các pain point phổ biến (dinh dưỡng, lịch tập, đau cơ). | Gợi ý vài ý tưởng quá chung chung (như làm app đếm rep/đếm calo). | Bỏ qua các ý tưởng đếm rep, chủ động tự pick ý "ảnh hưởng sức khỏe do sai form" vì đây mới là pain thật sự đau. |
| **Problem Statement** | Nhờ AI gợi ý và điền form các trường của Statement v0, v1. | Giúp cấu trúc câu từ gọn gàng, đúng format yêu cầu của lab. | Metric AI đưa ra rất cảm tính (ví dụ: "giúp người dùng tập tốt hơn", "giảm chấn thương"). | Tự viết lại Success Metric thành các con số kỹ thuật: ">90% phát hiện đúng lỗi", "độ trễ <0.5s". |
| **Rule / Workflow / Agent** | Nhờ AI phản biện giải pháp và chuốt lại văn phong báo cáo. | Chỉ ra sự cần thiết của việc đặt camera real-time: góc đặt camera ở phòng gym đông người. | AI lập luận an toàn quá mức, khuyên lùi về Workflow (quay video rồi chấm điểm sau). | Tự giữ vững lập luận chọn Agent vì bản chất "sửa dáng" cần Real-time, nhưng cần phải thêm bước Rule (căn chỉnh góc máy) trước khi cho Agent chạy để tăng độ chính xác. |
| **Hoàn thiện** | Nhờ AI rà soát lỗi logic trong toàn bộ báo cáo trước khi nộp. | Tìm ra được những chỗ chuyển ý giữa các phần bị rời rạc. | Đôi khi AI tự động viết thêm các tính năng thừa thãi (như tự động xếp lịch tập vào chung app sửa dáng). | Xóa bỏ tính năng thừa, giữ scope nhóm thật nhỏ và tập trung đúng vào một điểm nghẽn: Check form lúc tập. |

### Bài học cá nhân

* **Problem tốt là problem chạm đúng điểm nghẽn sinh tử:** Lúc đầu làm app cá nhân hóa giáo án là ưu tiên của em, nhưng sau khi đào sâu, em nhận ra việc tập không đúng mới là điều đáng lo nhất vì nó mang lại hậu quả vật lý thật sự (chấn thương).
* **AI chỉ nên mang vài trò cố vấn, không nên ra quyết định** Việc dùng AI để phản biện rất tốt, nhưng AI hiện nay sẽ cố hướng mình về các giải pháp an toàn và chung chung, không đưa ra được cái mới. Người làm sản phẩm phải tỉnh báo và có khả năng bảo vệ lập luận cốt lõi của mình.

* **Nếu làm lại:** Em sẽ dành thêm thời gian khảo sát thực tế 3-5 bạn sinh viên, học sinh ở phòng gym xem họ có gặp các bottleneck mà em nghĩ không.

```