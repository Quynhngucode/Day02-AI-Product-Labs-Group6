# 02 — Group Problem Statement

Case nhóm chọn: **Gym Buddy — AI hỗ trợ newbie kiểm tra form khi tập gym**

Bối cảnh: nhóm đang đánh giá các problem liên quan đến người mới đi gym, đặc biệt là nhóm người tự tập, không có private trainer hoặc không đủ chi phí thuê PT lâu dài.

---

## Group convergence

Nhóm gom các problem scan được thành các cluster sau:

| Cluster | Candidate examples | Pattern chung |
|---|---|---|
| Lên lịch / kế hoạch tập luyện | Weekly workout plan, lịch tập theo nhóm cơ, lịch tăng cơ/giảm mỡ, lịch tập theo thời gian rảnh | Tạo kế hoạch tập phù hợp với mục tiêu, thể trạng, kinh nghiệm và lịch sinh hoạt của người tập |
| Theo dõi / tổng hợp tiến độ | Workout log, số set/rep/mức tạ, cân nặng, body measurement, weekly progress report | Gom dữ liệu tập luyện theo thời gian rồi tổng hợp để biết người tập có tiến bộ hay không |
| Tư vấn / hỏi đáp tập luyện | Hôm nay tập gì, tập bao nhiêu set, có nên tăng tạ không, đau cơ có nên tập tiếp không | Trả lời các câu hỏi lặp lại của người tập dựa trên mục tiêu, lịch tập và tình trạng hiện tại |
| Điều chỉnh bài tập / thay thế bài | Máy bị chiếm, không có dụng cụ, đau nhẹ, quá mệt, không đủ thời gian tập | Đề xuất phương án thay thế phù hợp khi điều kiện thực tế thay đổi |
| Cá nhân hóa giáo án | Lịch tập theo chiều cao/cân nặng, mục tiêu giảm mỡ/tăng cơ, người mới/người đã tập lâu, giới hạn chấn thương | Biến một giáo án chung thành kế hoạch riêng cho từng người |
| Nhắc nhở / duy trì thói quen | Nhắc lịch tập, nhắc uống nước, nhắc nghỉ ngơi, nhắc ghi log, nhắc quay lại sau khi bỏ buổi | Giúp người tập không quên việc cần làm và duy trì consistency |
| Review / feedback kỹ thuật | Check form squat, deadlift, bench press, nhận xét video tập, cảnh báo lỗi động tác | Quan sát bài tập và chỉ ra lỗi kỹ thuật hoặc điểm cần sửa |
| Quản lý học viên cho PT | Dashboard học viên, báo cáo tiến độ, cảnh báo học viên bỏ buổi, summary từng người | Giúp private trainer theo dõi nhiều học viên cùng lúc thay vì quản lý thủ công |
| Dinh dưỡng / phục hồi cơ bản | Ăn gì trước/sau tập, protein bao nhiêu, ngủ nghỉ thế nào, ngày nghỉ nên làm gì | Hỗ trợ các lời khuyên cơ bản liên quan đến tập luyện, ăn uống và phục hồi |
| Chuyển người thật / kiểm soát rủi ro | Đau bất thường, nghi chấn thương, bệnh nền, giảm cân quá nhanh, bài tập nguy hiểm | Khi vấn đề vượt quá mức tư vấn đơn giản, cần chuyển sang PT thật hoặc chuyên gia y tế |

Insight từ phần convergence:

```text
Các problem về lịch tập, nhắc nhở và workout log đều hữu ích, nhưng dễ bị xem như app fitness thông thường.
Problem “check form và cảnh báo lỗi động tác” có pain rõ hơn vì nó chạm trực tiếp vào nỗi sợ tập sai, chấn thương và thiếu feedback realtime khi không có PT.
```

---

## Shortlist và score

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **Check form squat, deadlift, bench press, nhận xét video tập, cảnh báo lỗi động tác** | **5** | **5** | **5** | **5** | **4** | **5** | **5** | **34** |
| Tạo lịch tập tuần theo mục tiêu tăng cơ/giảm mỡ | 4 | 4 | 3 | 3 | 4 | 3 | 5 | 26 |
| Gợi ý bài tập thay thế khi máy bị chiếm/thiếu dụng cụ | 4 | 4 | 3 | 2 | 4 | 3 | 5 | 25 |

Nhóm chọn: **Check form squat, deadlift, bench press, nhận xét video tập, cảnh báo lỗi động tác**.

Vì sao chọn:

- Có actor rõ: newbie tự tập gym, sinh viên, người không có PT, người sợ tập sai form.
- Có workflow rõ: chuẩn bị bài tập → setup tạ/máy → thực hiện động tác → tự soi gương/cảm nhận → sửa sai hoặc tiếp tục tập.
- Có pain thật: người mới thường không biết mình đang sai form, ngại hỏi người khác, sợ chấn thương và dễ tránh các bài compound.
- Có impact đo được: số lỗi form phát hiện được, thời gian nhận feedback, tỷ lệ sửa đúng sau feedback, số lần phải dừng set vì cảnh báo nguy hiểm.
- Có thể làm trong lab ở mức prototype: dùng video/ảnh mẫu để demo nhận xét form, hoặc mô phỏng logic check lỗi dựa trên pose/keypoints.
- Có thể so sánh Rule / Workflow / Agent rõ ràng.

Vì sao không chọn các bài khác:

- **Tạo lịch tập tuần:** workflow rõ và dễ làm, nhưng dễ trùng với app fitness thông thường; AI value chưa nổi bật nếu chỉ tạo plan.
- **Gợi ý bài tập thay thế:** thực tế và hữu ích, nhưng impact thấp hơn vì chưa giải quyết pain lớn nhất là tập sai form và nguy cơ chấn thương.

---

## Quick validation

Nhóm có thể validate nhanh với 3 nhóm người: newbie tự tập, người đã từng thuê PT và người có kinh nghiệm tập gym.

| Nguồn | Số người | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Newbie tự tập gym | 3 | Thường không chắc form đúng hay sai, hay nhìn video/TikTok rồi bắt chước | Một số bài máy đơn giản ít cần check form realtime | Thu hẹp scope vào bài có rủi ro kỹ thuật cao như squat, deadlift, bench press |
| Người từng thuê PT | 2 | Lý do thuê PT thường là cần người sửa form trực tiếp | PT còn giúp tạo động lực và giáo án, AI không thay thế hoàn toàn | Định vị sản phẩm là trợ lý sửa form cơ bản, không thay thế PT |
| Người tập lâu hơn / có kinh nghiệm | 2 | Feedback realtime hữu ích nếu cảnh báo đúng lỗi nguy hiểm | Nếu camera đặt sai góc thì feedback có thể nhiễu | Thêm bước rule kiểm tra góc camera trước khi bắt đầu phân tích |

Insight sau validation:

```text
Pain thật không chỉ là “không biết tập bài gì”, mà là “không biết mình đang tập đúng hay sai trong lúc thực hiện động tác”.
Vì lỗi form xảy ra ngay trong set tập, feedback sau buổi tập có thể quá muộn với các lỗi nguy hiểm.
```

---

## Research giải pháp

Nhóm tìm các hướng đã có sẵn, không giả định phải tự build toàn bộ từ đầu.

| Nguồn / tool / case | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|
| Freeletics Coach | Cá nhân hóa chương trình tập luyện và hướng dẫn thực hiện bài tập | Kế hoạch tập được điều chỉnh theo mục tiêu người dùng | Chưa tập trung mạnh vào phân tích kỹ thuật động tác theo thời gian thực | AI có thể thay thế một phần vai trò hướng dẫn cơ bản của PT |
| Peloton Guide | Nhận diện cơ thể và theo dõi quá trình tập | Trải nghiệm đơn giản, dễ sử dụng tại nhà | Phản hồi kỹ thuật còn ở mức cơ bản | AI phù hợp cho việc theo dõi và nhắc nhở thường xuyên |
| Google MediaPipe Pose | Nhận diện các keypoints trên cơ thể người | Mã nguồn mở, hỗ trợ nhiều nền tảng | Chỉ cung cấp dữ liệu tư thế, không tự đánh giá đúng/sai | Có thể dùng làm nền tảng xây dựng hệ thống kiểm tra form |
| BlazePose / Human Pose Estimation Research | Trích xuất tư thế cơ thể từ video hoặc camera | Có thể nhận diện khớp cơ thể từ hình ảnh/video | Cần thêm logic để chuyển dữ liệu thành feedback cho người tập | AI cần kết hợp pose estimation và luật đánh giá kỹ thuật |

Research takeaway:

```text
Không nên bắt đầu bằng một app fitness tổng quát. Hướng hợp lý hơn là tập trung vào một workflow rất cụ thể: người mới thực hiện một bài tập có rủi ro kỹ thuật cao, AI quan sát form và cảnh báo lỗi nguy hiểm.
```

---

## Workflow before/after

File nhóm nộp kèm:

```text
02-group-problem-statement-workflow.png/pdf/md
```

Nội dung workflow:

```text
CURRENT STATE — Newbie tự tập gym không có PT

[1 Newbie muốn tập gym nhưng không đủ tài chính thuê PT]
→ [2 Tự tìm lịch tập và động tác trên TikTok/YouTube/Google]
→ [3 Đến phòng gym, nhìn nhiều máy tập nhưng không biết nên chọn máy nào]
→ [4 Tự chọn bài tập theo cảm tính, không chắc bài đó có phù hợp với mình không]
→ [5 Tập theo video hoặc nhìn người khác tập nhưng không biết form đúng hay sai]  <-- bottleneck
→ [6 Nghỉ giữa set để soi gương, xem lại video hoặc chỉnh máy/tư thế]
→ [7 Tiếp tục tập nhưng vẫn có nguy cơ sai động tác, sai nhóm cơ hoặc dễ chấn thương]
```

```text
FUTURE STATE — Gym Buddy hỗ trợ sửa form realtime

[1 Newbie mở app Gym Buddy trước buổi tập]
→ [2 App hỏi mục tiêu, trình độ, tình trạng đau/chấn thương và bài tập muốn thực hiện]  -- Workflow step
→ [3 App hướng dẫn user đặt camera đúng góc]  -- Rule/checklist step
→ [4 User thực hiện bài tập trước camera]  -- Human action
→ [5 AI theo dõi realtime qua camera và phát hiện lỗi form: lưng cong, gối lệch, tay đặt sai, biên độ sai]  -- Agent step
→ [6 AI cảnh báo lỗi nguy hiểm ngay lập tức bằng âm thanh/visual cue]  -- Agent step
→ [7 Sau set, app tóm tắt lỗi chính và gợi ý cách sửa cho set sau]  -- Workflow step
```

Fallback:

```text
Nếu AI không nhận diện rõ cơ thể, góc camera bị che, ánh sáng kém, có nhiều người đi qua khung hình hoặc user có dấu hiệu đau/chóng mặt/chấn thương:
→ App dừng feedback chi tiết.
→ App báo “Không đủ dữ liệu để đánh giá an toàn”.
→ App khuyên user hỏi PT/nhân viên phòng gym/người có chuyên môn.
```

Bottleneck mới:

```text
User cần đặt camera đúng góc và làm theo cảnh báo của AI.
Đây là bottleneck chấp nhận được vì nó tạo một điểm kiểm soát an toàn trước khi AI đưa feedback kỹ thuật.
```

Before/after impact:

| Metric | Trước | Sau kỳ vọng | Ghi chú |
|---|---|---|---|
| Khả năng biết mình tập đúng hay sai | Thấp, chủ yếu tự soi gương hoặc đoán theo video | Cao hơn nhờ AI cảnh báo realtime | Target chính |
| Khả năng chọn bài/máy phù hợp | Dễ chọn theo cảm tính hoặc theo trend | AI gợi ý bài/máy phù hợp với trình độ newbie | Giảm quá tải thông tin |
| Cách sửa lỗi động tác | Xem video một chiều, khó biết mình sai ở đâu | AI chỉ ra lỗi cụ thể và hướng dẫn sửa ngay | Phản hồi hai chiều |
| Mức độ phụ thuộc vào PT | Cao nếu muốn được sửa form trực tiếp | Giảm ở các bài beginner và máy tập cơ bản | Không thay thế hoàn toàn PT |
| Chi phí hướng dẫn ban đầu | Cao nếu thuê PT cá nhân | Thấp hơn khi dùng app AI | Yếu tố pricing quan trọng |
| Bottleneck chính | Không biết form đúng hay sai trong lúc tập | Đặt camera đúng góc và làm theo cảnh báo AI | Human/self boundary |
| Rủi ro chấn thương | Có thể cao do tập sai mà không biết | Giảm ở các lỗi form cơ bản | AI chỉ hỗ trợ giảm rủi ro, không đảm bảo an toàn tuyệt đối |
| Risk mới | Tự tập sai mà không có ai nhắc | AI có thể nhận diện sai nếu camera/góc quay kém | Cần fallback sang PT/người thật khi không chắc |

---

## Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Học sinh, sinh viên, người mới bắt đầu đi tập gym, tự tập không có PT. |
| **Workflow** | Xem video/ảnh hướng dẫn động tác → setup tạ/máy → thực hiện set tập bằng cách bắt chước → tự cảm nhận cơ thể → nghỉ và tự chỉnh lại nếu thấy sai. |
| **Bottleneck** | Bước “thực hiện set tập” và “tự cảm nhận”. Người mới chưa có kinh nghiệm nên không biết lưng có cong, gối có lệch, tay có sai góc hoặc biên độ có đúng không. |
| **Impact** | Tập sai có thể gây đau lưng, đau khớp, tập không vào đúng nhóm cơ, mất thời gian mà không thấy hiệu quả và dễ bỏ cuộc sau một thời gian ngắn. |
| **Success Metric** | Phát hiện được các lỗi form nguy hiểm trong lúc tập; tỷ lệ user sửa đúng lỗi sau feedback tăng; giảm số lần user phải tự dừng để xem lại video hoặc hỏi người khác. |
| **Boundary** | Chỉ đánh giá và cảnh báo về tư thế/form; không chẩn đoán bệnh, không kê đơn điều trị, không thay thế PT/bác sĩ trong trường hợp đau bất thường hoặc có bệnh nền. |

---

## Rule / Workflow / Agent

| Mức | Phương án | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **Rule** | Checklist ảnh/video minh họa form đúng/sai; hướng dẫn góc đặt camera; cảnh báo chung trước khi tập | Đủ nếu user chỉ cần tài liệu tham khảo hoặc bài tập đơn giản, ít rủi ro | User khó tự quan sát bản thân khi đang nâng tạ; dễ bỏ qua checklist | Không chọn làm toàn bộ, nhưng dùng làm baseline và bước căn chỉnh camera |
| **Workflow** | User quay video set tập → upload → AI phân tích sau set → trả feedback lỗi sai → user sửa ở set sau | Hợp lý cho MVP hoặc khi chưa đủ tài nguyên realtime | Feedback bị trễ; nếu lỗi form nghiêm trọng xảy ra ngay trong set thì đã có rủi ro chấn thương | Có thể dùng làm pilot nhỏ nhất |
| **Agent** | Bật camera → hệ thống liên tục track chuyển động → tự phát hiện lỗi form nguy hiểm → cảnh báo ngay bằng âm thanh/visual cue | Cần thiết khi lỗi form cần được sửa ngay trong lúc tập | Nhận diện sai do góc quay, ánh sáng, người đi qua khung hình; cảnh báo sai có thể làm phiền user | **Chọn cho hướng sản phẩm chính** |

Mức chọn:

```text
Agent — Real-time Form Monitoring & Alert.
```

Vì sao:

- Lỗi form trong bài tập tạ có thể gây rủi ro ngay trong lúc thực hiện động tác.
- Workflow phân tích sau set giúp cải thiện kỹ thuật nhưng không chặn được lỗi nguy hiểm tức thời.
- Agent phù hợp hơn vì có thể quan sát liên tục và cảnh báo ngay khi phát hiện dấu hiệu nguy hiểm.
- Tuy nhiên, agent cần guardrail: chỉ cảnh báo trong scope bài tập đã hỗ trợ, không chẩn đoán chấn thương và cần fallback sang người thật khi không chắc.

---

## Problem Statement v1

| Field | Nội dung |
|---|---|
| **Actor** | Sinh viên, người mới đi gym, tự tập không có PT hoặc không đủ chi phí thuê PT lâu dài. |
| **Workflow** | Setup điện thoại ở góc chuẩn → bật camera tracking → thực hiện động tác → nghe cảnh báo nếu có lỗi nguy hiểm → sửa ngay trong set hoặc dừng set → xem lại summary sau khi tập. |
| **Bottleneck** | Người mới không thể vừa nâng tạ vừa quan sát chính xác toàn bộ tư thế của mình ở nhiều góc; vì vậy họ khó biết mình đang sai form trong thời gian thực. |
| **Impact** | Tập sai có thể dẫn đến đau lưng, đau khớp, sai nhóm cơ, không đạt kết quả và giảm động lực đi tập. |
| **Success Metric** | App phát hiện và cảnh báo đúng phần lớn các lỗi form nguy hiểm trong thời gian thực; độ trễ cảnh báo đủ thấp để user sửa ngay; user hiểu được lỗi chính sau mỗi set. |
| **Boundary** | Chỉ theo dõi khi user chủ động bấm Start; chỉ cảnh báo tư thế/form; không ép user phải dừng set; không tư vấn y tế; không dùng cho người có chấn thương/bệnh nền nếu không có chuyên gia theo dõi. |
| **AI intervention point** | Can thiệp trực tiếp vào bước “thực hiện set tập” thông qua camera để đóng vai trò PT ảo giám sát form realtime. |
| **Mức chọn** | Agent: hệ thống tự quan sát qua camera, tự đánh giá pose/form theo logic đã định nghĩa, tự quyết định thời điểm và loại cảnh báo cần phát ra. |
| **Rủi ro & người thật kiểm tra** | Risk: góc đặt điện thoại sai, ánh sáng kém, người khác đi qua khung hình, AI nhận diện khớp sai và cảnh báo nhầm. Kiểm tra: có bước rule để căn chỉnh khung hình trước khi tập; nếu confidence thấp thì dừng feedback và khuyên hỏi PT/nhân viên phòng gym. |

---

## Final decision

Decision:

```text
Go với scope nhỏ.
```

Pilot nhỏ nhất:

- Chỉ chọn 1–2 bài tập phổ biến và có form dễ quan sát, ví dụ squat và bench press.
- Dùng video mẫu hoặc video tự quay trong điều kiện cố định.
- MVP ban đầu có thể chạy theo hướng Workflow: upload video sau set rồi nhận feedback.
- Sau khi logic feedback ổn hơn, mở rộng sang Agent realtime.
- Đo các chỉ số: thời gian nhận feedback, số lỗi form phát hiện, số feedback sai, mức độ user hiểu được lỗi và sửa được ở set sau.

Exit / rollback:

- Nếu AI thường xuyên không nhận diện được pose do góc quay hoặc môi trường phòng gym, hạ xuống chế độ phân tích video sau set.
- Nếu feedback sai quá nhiều hoặc user không hiểu cách sửa, quay về checklist form + video minh họa + hướng dẫn đặt camera.
- Nếu user báo đau bất thường hoặc nghi chấn thương, dừng hướng dẫn và chuyển sang khuyến nghị hỏi PT/bác sĩ.

Decision rationale:

- Problem rõ: newbie không biết mình tập đúng hay sai trong lúc tập.
- Workflow rõ: setup camera → tập → AI quan sát → cảnh báo → xem lại feedback.
- Metric có thể đo: số lỗi phát hiện, độ trễ feedback, tỷ lệ sửa lỗi sau feedback.
- Có non-AI baseline: checklist form, video mẫu, rule căn chỉnh camera.
- AI nằm ở điểm can thiệp cụ thể: quan sát và cảnh báo lỗi form trong lúc thực hiện động tác.
- Human boundary rõ: AI không thay thế PT/bác sĩ, chỉ hỗ trợ feedback form cơ bản và chuyển người thật khi không chắc.
