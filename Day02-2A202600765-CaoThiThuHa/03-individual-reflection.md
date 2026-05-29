# 03 — Individual Reflection

Case nhóm chọn: **Gym Buddy — AI hỗ trợ newbie kiểm tra form khi tập gym**

Học viên thực hiện: **Cao Thị Thu Hà**  
Mã học viên: **2A202600765**

---

## Đóng góp của Hà trong nhóm

Trong suốt 4 tiếng làm việc nhóm của Day 02 Lab, tôi đã tích cực tham gia vào tất cả các giai đoạn thảo luận, phản biện và xây dựng giải pháp chung từ bài toán cá nhân cho đến đề xuất của nhóm. Dưới đây là bảng chi tiết đóng góp của tôi:

| Hoạt động | Tôi đã làm gì? | Kết quả / Ảnh hưởng đối với nhóm |
|---|---|---|
| **Scan cá nhân** | Thực hiện scan rộng 15 vấn đề khác nhau từ thực tế tự tập gym, phân tích sâu các lăng kính lặp đi lặp lại và pain từ người tập khác. | Cung cấp cho nhóm nhiều dữ liệu thực tế và góc nhìn đa chiều về các khó khăn của newbie tự tập. |
| **Pitch Problem Card** | Trình bày và làm rõ 2 bài toán cá nhân: Lịch tập thiếu cá nhân hóa động (#9) và sự thiếu hỗ trợ 24/7 từ PT ngoài phòng tập (#14). | Giúp nhóm mở rộng bối cảnh ngoài việc sửa tư thế tập luyện (form), nhìn nhận toàn diện bức tranh sinh hoạt của học viên gym. |
| **Challenge bài của bạn khác** | Khi bạn Quỳnh pitch bài check form, tôi đã đặt câu hỏi phản biện cực kỳ thực tế: *"Phòng gym giờ cao điểm rất đông và ồn, người tập làm sao đặt camera điện thoại quay toàn thân mà không bị người khác che khuất hoặc gây phiền hà?"* | Thảo luận này giúp nhóm bổ sung bước rule/checklist hướng dẫn đặt camera trong workflow tương lai và xây dựng guardrail/fallback chặt chẽ khi confidence nhận diện của AI bị giảm sút. |
| **Gom trùng / Cluster** | Đồng hành cùng nhóm phân loại các ý tưởng cá nhân thành 10 cluster rõ ràng (Dinh dưỡng, Nhắc nhở, Check form, Cá nhân hóa...). | Tạo tiền đề sạch sẽ để nhóm thực hiện chấm điểm và đưa ra lựa chọn khoa học nhất. |
| **Chọn candidate problem** | Cùng cả nhóm chấm điểm ma trận chọn bài toán check form và cảnh báo lỗi động tác trực tiếp (đạt 34/35 điểm). | Đồng thuận cao về việc tập trung giải quyết bài toán cốt lõi liên quan trực tiếp đến an toàn chấn thương. |
| **Validation / Research** | Trực tiếp hỗ trợ tìm kiếm tài liệu về các giải pháp Pose Estimation hiện có (Peloton Guide, Google MediaPipe, BlazePose) và hỗ trợ phỏng vấn nhanh 1 học viên từng thuê PT. | Rút ra bài học quan trọng: AI không nên ôm đồm cả app fitness mà chỉ nên can thiệp vào bottleneck hẹp là cảnh báo lỗi động tác tức thời. |
| **Workflow nhóm** | Đồng thiết kế current state và future state workflow. Định vị rõ các bước nào dùng Rule, bước nào dùng AI Agent và giới hạn Human Boundary. | Bản thiết kế workflow trực quan, logic được nhóm nộp kèm và áp dụng làm baseline cho dự án. |
| **Problem Statement** | Tham gia viết và tinh chỉnh Problem Statement từ v0 lên v1, làm rõ success metric về thời gian nhận feedback phản hồi dưới 1 giây. | Có một Problem Statement chặt chẽ, đo lường được và định rõ ranh giới hoạt động của AI. |
| **Rule / Workflow / Agent & Decision** | Lập luận mạnh mẽ để nhóm quyết định nâng lên mức **Agent** cho tính năng realtime alert trong lúc đang tập, đồng thời thống nhất quyết định **Go** với scope thí điểm (pilot) nhỏ. | Nhóm đi đến quyết định cuối cùng mang tính thực tiễn cao, có lộ trình rollback an toàn nếu AI hoạt động không tốt. |

---

## Bảng dùng AI trong reflection

Trong quá trình thực hiện bài tập cá nhân và thảo luận nhóm, tôi đã sử dụng các mô hình AI làm trợ lý tư duy. Dưới đây là cách tôi phối hợp và phản biện lại AI để đảm bảo tính thực tế của bài nộp:

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| **Scan cá nhân** | Hỏi AI gợi ý thêm các vấn đề thực tế ở phòng gym theo 4 lăng kính sau khi tôi tự viết được 5 ý ban đầu. | Gợi ý cho tôi các ý tưởng thú vị như việc tự đọc chỉ số InBody mập mờ (#8) hay điều chỉnh volume tập theo chỉ số RPE sinh lý (#12). | Đưa ra các đề xuất chung chung, mang tính vĩ mô kiểu "Người tập thiếu động lực tinh thần cần AI động viên" hoặc "AI tự thiết lập thực đơn y khoa". | Tôi loại bỏ hoàn toàn các ý tưởng thiếu workflow thực tế, tập trung viết lại các problem gắn liền với hành vi thật và đo lường được. |
| **Problem Card** | Nhờ AI đóng vai trò skeptical PM để phản biện tính khả thi và độ chặt chẽ của Problem Card #1. | Chỉ ra điểm yếu của Success Metric ban đầu của tôi khi viết "giúp người tập đỡ đau lưng hơn" là quá mơ hồ và khó đo lường khách quan. | AI liên tục khuyên tôi chuyển hướng sang một app fitness tổng thể, tích hợp cả ăn uống, ngủ nghỉ, social network để tối đa hóa doanh thu. | Tôi kiên định giữ nguyên scope hẹp là check form squat/bench press realtime, sửa success metric thành "độ trễ cảnh báo dưới 1 giây" và "giảm tỉ lệ sai form ở set tiếp theo". |
| **Workflow nhóm** | Nhờ AI hỗ trợ cấu trúc lại sơ đồ workflow ASCII để dán vào file báo cáo cho trực quan và sạch sẽ. | Căn chỉnh các khối bước logic thẳng hàng, phân chia rõ ràng giữa Action của Người và Bước xử lý của AI. | AI tự động gộp bước "đặt camera đúng góc" vào chung một bước "thực hiện set tập", bỏ qua rủi ro camera bị nghiêng hoặc khuất khớp. | Tôi tách riêng bước "App hướng dẫn setup camera (Rule)" thành một bước tiền kiểm an toàn bắt buộc trước khi AI Agent kích hoạt. |
| **Research giải pháp** | Nhờ AI hỗ trợ tìm hiểu nhanh cơ chế hoạt động của Peloton Guide và Google MediaPipe Pose. | Tổng hợp nhanh các ưu nhược điểm kỹ thuật và chỉ ra khoảng trống (gap) về logic đánh giá lỗi biomechanics của các thư viện mã nguồn mở. | Đưa ra một số số liệu thống kê về độ chính xác và tỷ lệ chấn thương phòng gym không rõ nguồn gốc (hallucination). | Tôi tự mình kiểm chứng lại các thông tin kỹ thuật chính thống từ trang tài liệu Google MediaPipe và loại bỏ các số liệu thống kê trôi nổi không được xác thực. |

---

## Bài học của Hà

Trải qua lab học này, tôi đã rút ra được 4 bài học đắt giá trong tư duy làm sản phẩm AI:

1. **Problem-First là chìa khóa tránh lãng phí:** Trước khi nghĩ đến việc dùng AI ngầu thế nào, phải vẽ được workflow hiện tại của người dùng và chỉ ra đúng bước nghẽn (bottleneck). Nếu bottleneck không rõ ràng hoặc có thể giải quyết bằng các quy tắc tĩnh (Rule/Dashboard) với chi phí rẻ hơn, thì không nên đưa AI vào.
2. **Agent không phải là cây đũa thần vô điều kiện:** Agent cực kỳ mạnh mẽ cho các tác vụ mang tính động, tự quan sát và tự ra quyết định như giám sát form realtime qua camera. Tuy nhiên, nó đi kèm rủi ro cực lớn về độ chính xác (hallucination/false alert). Do đó, Agent bắt buộc phải đi kèm **Human Boundary** (người tập tự quyết định việc nâng tạ, AI không thay thế) và **Guardrails/Fallback** rất chặt chẽ (camera lỗi thì dừng phân tích và khuyên hỏi PT thật).
3. **Giá trị của việc phản biện (Challenge):** Việc đặt mình vào vị trí hoài nghi giúp sản phẩm thực tế hơn. Câu hỏi của tôi về "góc đặt camera trong phòng tập đông người" đã biến một giải pháp AI lý thuyết trong phòng lab thành một workflow thực tiễn, có tính đến sự bất tiện của người dùng ngoài đời thực.
4. **Research để đứng trên vai người khổng lồ:** Không cần phát minh lại bánh xe. Nhìn vào các giải pháp như MediaPipe hay Freeletics giúp nhóm tôi định vị rõ sản phẩm của mình không phải là một thư viện nhận diện pose cơ thể, mà là một **AI Agent ứng dụng** dịch pose thành feedback biomechanics dễ hiểu cho newbie.

### Nếu được làm lại:
> [!TIP]
> Tôi muốn thực hiện một cuộc phỏng vấn trực tiếp (user interview) sâu hơn với 2-3 chủ phòng gym/PT chuyên nghiệp để hiểu rõ hơn cách họ quan sát và sửa lỗi form cho học viên ngoài đời thực. Từ đó, tôi có thể cung cấp các tập luật biomechanics chính xác hơn cho mô hình AI Agent, đồng thời thiết kế cách phản hồi (âm thanh/hình ảnh) tinh tế hơn để không làm người tập bị giật mình hoặc mất tập trung khi đang nâng tạ nặng.