# 01 — Individual Problem Scan

Case cá nhân: **Gym Buddy — AI hỗ trợ người mới đi gym tự tập an toàn và hiệu quả**

Nhân vật quan sát: Hà, một người mới bắt đầu đi gym, tự tập không có PT hoặc không đủ chi phí thuê PT lâu dài. Trong quá trình tự tập, Hà gặp nhiều khó khăn từ việc duy trì kỷ luật, lên kế hoạch ăn tập cho đến việc lo sợ chấn thương khi tập sai động tác mà không có ai chỉ dẫn.

---

## Scan rộng

Tôi tiến hành scan rộng 15 problems dựa trên chính trải nghiệm thực tế của bản thân và những người xung quanh tại phòng tập gym, sử dụng đa dạng 4 lăng kính. Các vấn đề được ghi nhận với actor cụ thể và dấu hiệu thực tế rõ ràng, không đi trước từ giải pháp AI.

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật | Người quan sát |
|---|---|---|---|---|---|
| 1 | Tốn thời gian | Tự ước lượng và tính toán macro dinh dưỡng (calo, protein, carb, fat) cho mỗi bữa ăn hằng ngày. | Người mới tập gym muốn tăng cơ/giảm mỡ | Mất 15–20 phút mỗi ngày ghi chép và tra cứu calo thực phẩm trên Google/app, dễ tính sai hoặc bỏ ngang. | Hà |
| 2 | Lặp lại | Ghi chép (log) tay số set, rep, và mức tạ sau mỗi bài tập để theo dõi tiến độ. | Người tập gym tự theo dõi | Phải mang sổ bút hoặc mở app note bấm liên tục khi tay đang mồ hôi, dễ quên ghi chép dẫn đến buổi sau không nhớ mức tạ cũ. | Hà |
| 3 | Pain từ người khác | Người tập tại nhà không biết bố trí không gian tập và setup dụng cụ (thảm, tạ đơn) thế nào cho an toàn và đủ biên độ động tác. | Người tập gym tại nhà | Thường xuyên va quệt vào đồ đạc xung quanh, đặt camera quay bị khuất, không thực hiện trọn vẹn động tác. | Hà |
| **4** | **Lặp lại** | **Nhắc lịch tập, nhắc uống nước, nhắc nghỉ ngơi, nhắc ăn uống theo mục tiêu** | **Người tập, PT** | **Người tập dễ bỏ buổi nếu không có ai nhắc** | **Hà** |
| 5 | Tốn thời gian | Tìm bài tập thay thế tương đương khi máy tập chính trong phòng gym bị người khác chiếm mất vào giờ cao điểm. | Người tập gym giờ cao điểm | Đứng chờ máy mất 5–10 phút hoặc đi loanh quanh tìm máy khác mà không biết bài nào thay thế có cùng tác động cơ. | Hà |
| 6 | AI có thể tốt hơn | Phân biệt cảm giác đau mỏi cơ lành mạnh sau tập (DOMS) so với đau khớp chấn thương nguy hiểm. | Người mới tự tập | Lo sợ thái quá khi bị đau cơ sau buổi tập đầu, hoặc ngược lại cố tập tiếp khi khớp bị đau dẫn đến chấn thương nặng hơn. | Hà |
| 7 | Pain từ người khác | Học viên online phàn nàn PT phản hồi video tập quá trễ (sau 1–2 ngày), làm họ không sửa được form ngay cho buổi tập kế tiếp. | Học viên gym online | Phải nhắn tin giục giã PT liên tục trên Zalo, buổi tập sau vẫn lặp lại lỗi sai form cũ vì chưa được sửa kịp thời. | Hà |
| 8 | Tốn thời gian | Đọc và hiểu các thông số chỉ số cơ thể (InBody) để tự điều chỉnh chế độ tập và ăn uống phù hợp. | Người tập gym | Nhận tờ kết quả InBody với hàng chục chỉ số nhưng không biết ý nghĩa và hành động tiếp theo là gì, phải chờ PT giải thích. | Hà |
| **9** | **AI có thể tốt hơn** | **App gym hiện tại thường chỉ cho lịch tập cố định, chưa cá nhân hóa theo thể trạng, mục tiêu, lịch rảnh và tiến độ thật** | **Người tập gym** | **Người dùng bỏ app vì lịch tập không phù hợp thực tế** | **Hà** |
| 10 | Lặp lại | Tính toán tỷ lệ tăng tạ tịnh tiến (Progressive Overload) hằng tuần để đảm bảo cơ bắp phát triển liên tục. | Người tập gym tự học | Không biết khi nào nên tăng tạ, tăng bao nhiêu kg, dẫn đến tập mãi một mức tạ suốt nhiều tháng không có tiến bộ. | Hà |
| 11 | Tốn thời gian | Lọc các video hướng dẫn kỹ thuật tập trên mạng để tìm biến thể động tác phù hợp với hạn chế khớp cơ thể (vd: cứng khớp cổ chân). | Người mới tập gym | Mất cả tiếng xem video hướng dẫn squat nhưng thử làm theo vẫn thấy đau gối vì video chỉ hướng dẫn cho người có cơ địa bình thường. | Hà |
| 12 | AI có thể tốt hơn | Điều chỉnh khối lượng tập (Volume) thời gian thực dựa trên mức độ mệt mỏi sinh lý hằng ngày (chỉ số RPE/RIR) thay vì giáo án cứng nhắc. | Người tập tự lập kế hoạch | Hôm nào mệt mỏi vì áp lực công việc vẫn cố tập nặng dẫn đến quá tải/kiệt sức, hôm nào sung sức lại tập quá nhẹ do rập khuôn giáo án. | Hà |
| 13 | Lặp lại | Theo dõi và duy trì nhịp tim trong vùng tối ưu (Fat Burn Zone) khi tập cardio để giảm mỡ hiệu quả nhất. | Người tập cardio/giảm mỡ | Phải liên tục nhìn đồng hồ thông minh hoặc đo tay, khó duy trì cường độ chạy/đạp xe ổn định đúng vùng nhịp tim mục tiêu. | Hà |
| **14** | **Pain từ người khác** | **Người tập phàn nàn rằng PT chỉ hỗ trợ trong buổi tập, ngoài giờ phải tự xoay xở** | **Người tập gym** | **Có thắc mắc về ăn uống/tập luyện nhưng phải chờ PT trả lời** | **Hà** |
| 15 | AI có thể tốt hơn | Tự động đếm số lần thực hiện (rep) và đo thời gian nghỉ giữa các set (rest time) để người tập tập trung hoàn toàn vào kỹ thuật. | Người tập gym tự lực | Thường xuyên quên mất mình đã tập được bao nhiêu rep khi mệt mỏi ở cuối set, hoặc nghỉ quá thời gian quy định do mải lướt điện thoại. | Hà |

### Vì sao phần scan này mạnh:
1. **Có scan rộng và sâu:** Đạt 15 problems cụ thể, khai thác toàn diện cả 4 lăng kính để mở rộng tối đa không gian bài toán trước khi đưa ra lựa chọn hội tụ.
2. **Actor cụ thể và gần gũi:** Tập trung vào người mới tập gym, người tự tập không có PT hoặc học viên tập gym online/hybrid.
3. **Dấu hiệu thực tế rõ ràng:** Mọi vấn đề đều đi kèm thời gian bị lãng phí, rủi ro cụ thể, phản hồi tiêu cực từ người tập thật hoặc các hành vi bỏ cuộc, nản chí dễ đo lường.
4. **Tránh solution-first:** Không bắt đầu bằng "Tôi muốn build app AI chăm sóc khách hàng", mà đi thẳng vào những điểm nghẽn thực sự trong workflow sinh hoạt và tập luyện của người tập.

---

## Top 3

Từ 15 problems trên, tôi sàng lọc ra Top 3 bài toán có pain-point mạnh nhất, workflow rõ ràng và có tiềm năng ứng dụng AI mang lại giá trị vượt trội so với các giải pháp thông thường.

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | **Người tự tập không biết mình đang sai form kỹ thuật trong lúc tập, sợ chấn thương và không có phản hồi sửa lỗi tức thì (Problem #6, #7)** | Pain cực lớn liên quan đến an toàn chấn thương và hiệu quả tập luyện. Khả năng can thiệp realtime của AI mang lại khác biệt lớn so với tài liệu tĩnh. | Cách tối ưu hóa góc đặt camera trong không gian phòng tập gym đông đúc để AI nhận diện chuẩn xác mà không bị che khuất. |
| 2 | **Lịch tập cố định từ các app hiện tại chưa cá nhân hóa và linh hoạt theo tiến độ thực tế, thể trạng và lịch rảnh động của người tập (Problem #9)** | Vấn đề lặp lại hằng tuần và có tỉ lệ bỏ app (churn rate) cực kỳ cao. Cá nhân hóa động là điểm mạnh cốt lõi của AI. | Làm sao thu thập đủ dữ liệu thể trạng ban đầu và cập nhật tiến độ tự động mà không bắt người dùng nhập liệu quá phức tạp. |
| 3 | **Người tập thiếu sự hỗ trợ và giải đáp thắc mắc 24/7 ngoài giờ tập về ăn uống, phục hồi và thay thế bài tập (Problem #14)** | Pain-point rất thật từ cả phía người tập lẫn PT. Giải quyết khoảng trống lớn trong dịch vụ huấn luyện hiện tại. | Cách kiểm soát rủi ro thông tin y tế/dinh dưỡng nhạy cảm để AI không đưa ra lời khuyên sai lệch gây ảnh hưởng sức khỏe. |

---

## Problem Card #1 — Giám sát form kỹ thuật và cảnh báo lỗi realtime khi tự tập gym

**Problem 1 câu:**  
Người mới tự tập gym không có PT thường không biết mình đang sai form ngay trong lúc thực hiện động tác, dẫn đến tập sai nhóm cơ, thiếu hiệu quả và đối mặt với rủi ro chấn thương nghiêm trọng.

**Actor:**  
Sinh viên, người đi làm mới bắt đầu tập gym tự tập một mình, không đủ tài chính thuê PT riêng lâu dài hoặc tập theo mô hình online/hybrid.

**Thời điểm / bối cảnh:**  
Thực hiện các set tập chính tại phòng gym, đặc biệt với các bài tập compound có rủi ro kỹ thuật và nguy cơ chấn thương cao (Squat, Deadlift, Bench Press).

**Current workflow:**
1. Xem video hướng dẫn động tác chuẩn trên YouTube hoặc TikTok trước buổi tập.
2. Đến phòng gym, setup tạ/máy tập và chuẩn bị thực hiện.
3. Thực hiện set tập bằng cách bắt chước theo trí nhớ.
4. Tự soi gương ở góc nghiêng (nếu có gương) hoặc dùng điện thoại quay video lại set tập.
5. Sau khi kết thúc set, nghỉ ngơi và mở video đã quay ra xem lại bằng cảm tính.
6. Không chắc chắn mình có bị gù lưng, lệch gối, lệch khớp vai hay không do thiếu kiến thức chuyên môn.
7. Tiếp tục tập các set tiếp theo với sự hoang mang hoặc giữ nguyên tư thế sai.

**Bottleneck:**  
Bước 4, 5, 6 — Người tập không thể vừa thực hiện động tác nặng vừa quan sát chính xác tư thế của mình ở mọi góc độ trong thời gian thực. Việc xem lại video sau set tập cũng chỉ mang tính cảm tính và phản hồi bị trễ, lỗi form nghiêm trọng đã xảy ra và rủi ro chấn thương đã xuất hiện.

**Impact:**  
- Gây chấn thương khớp, cột sống, dây chằng (đặc biệt nguy hiểm với bài Squat/Deadlift).
- Tập sai nhóm cơ mục tiêu làm tốn thời gian, công sức mà không thấy cơ thể thay đổi.
- Tạo thói quen vận động sai lệch (bad motor pattern) cực kỳ khó sửa về sau.
- Người tập hoang mang, mất động lực và dễ dàng từ bỏ việc tập luyện chỉ sau 1–2 tháng đầu.

**Success metric:**  
- AI phát hiện và phát ra tín hiệu cảnh báo (âm thanh/hình ảnh) các lỗi form nghiêm trọng (gù lưng, lệch gối) với độ trễ cực thấp (dưới 1 giây) ngay trong set tập.
- Giảm tỷ lệ thực hiện sai form cơ bản ở các set tập sau xuống dưới 20% nhờ feedback sửa đổi trực quan cụ thể ngay sau set.
- Thời gian người tập phải dừng lại loay hoay tự kiểm tra form giảm từ 5–7 phút xuống dưới 1 phút.

**Non-AI alternative:**  
- Nhìn gương phòng gym để tự chỉnh: Chỉ quan sát được một góc, gây mất tập trung và dễ chấn thương cổ khi cố ngoảnh đầu nhìn gương lúc nâng tạ nặng.
- Thuê PT trực tiếp: Chi phí cực kỳ đắt đỏ (5-10 triệu/tháng), không phù hợp với số đông newbie hoặc sinh viên.
- Nhờ bạn tập xem hộ: Bạn tập cũng là newbie nên không đủ kiến thức chuyên môn để nhận xét đúng/sai.

**AI hypothesis:**  
Hệ thống AI ứng dụng Pose Estimation (nhận diện khớp cơ thể qua camera) kết hợp các luật biomechanics để giám sát chuyển động của người tập trong thời gian thực, phát cảnh báo tức thì khi tư thế vượt ngưỡng an toàn và tóm tắt lỗi sai kèm hướng dẫn sửa sau set.

**Quick gut:**  
Agent. AI cần liên tục quan sát, đánh giá trạng thái động tác theo thời gian thực và tự động đưa ra quyết định cảnh báo thích hợp mà không cần người dùng thao tác bấm nút trong lúc đang nâng tạ.

---

### Draft current workflow

```text
CURRENT STATE — Tự mò form thủ công (Mất nhiều thời gian & rủi ro cao)

[1 Xem video hướng dẫn trên mạng: 15']
→ [2 Đến phòng gym, setup tạ/máy: 5']
→ [3 Thực hiện bài tập theo trí nhớ]
→ [4 Tự soi gương hoặc đặt điện thoại tự quay phim set tập]  <-- bottleneck (không quan sát được realtime toàn diện)
→ [5 Kết thúc set, mở video xem lại và tự đoán lỗi bằng cảm tính: 5']  <-- bottleneck (đánh giá mơ hồ)
→ [6 Tiếp tục tập set sau với form sai hoặc dè dặt vì sợ chấn thương]
```

---

### Draft future workflow

```text
FUTURE STATE — Gym Buddy hỗ trợ check form & cảnh báo realtime

[1 User chọn bài tập trên app (vd: Squat)]
→ [2 App hiển thị checklist góc đặt camera & hướng dẫn setup]    -- Rule
→ [3 User đặt điện thoại, căn chỉnh khung hình trước camera]      -- Human action
→ [4 Thực hiện động tác, AI track pose & phân tích realtime]     -- AI Agent step
→ [5 Phát âm thanh/visual cảnh báo NGAY LẬP TỨC nếu sai form]    -- AI Agent step
→ [6 Kết thúc set, app hiển thị summary lỗi chính & cách sửa]    -- Workflow step
→ [7 User sửa lỗi ở set tiếp theo hoặc bấm trợ giúp từ PT thật]   -- Human / Fallback step

Fallback:
Nếu góc quay kém, ánh sáng tối hoặc có người đi qua che khuất camera:
-> App dừng phân tích kỹ thuật, phát cảnh báo "Góc quay không đủ điều kiện an toàn".
-> Gợi ý user tự tập với mức tạ nhẹ hơn hoặc hỏi người có chuyên môn trực tiếp tại phòng gym.
```

---

## Problem Cards #2 và #3 — tóm tắt

| Card | Actor | Bottleneck | Metric | Quick gut | Vì sao chưa chọn làm #1 |
|---|---|---|---|---|---|
| **Problem Card #2:** Cá nhân hóa giáo án tập và dinh dưỡng động theo tiến trình thực tế | Người tập gym tự tập | Giáo án cứng nhắc, không tự động co giãn theo thể trạng thực tế hằng ngày và lịch rảnh thay đổi liên tục của user. | Giảm tỷ lệ người dùng bỏ dở giáo án tập luyện sau 1 tháng từ 60% xuống dưới 15%. | Workflow (AI đóng vai trò lập lịch động) | Mặc dù pain lớn và mang tính lặp lại cao, nhưng mức độ đe dọa an toàn sức khỏe tức thời không cao bằng lỗi sai form động tác. Dễ bị nhầm lẫn với các app fitness thông thường nếu không giải quyết được tính realtime kỹ thuật. |
| **Problem Card #3:** PT ảo hỗ trợ giải đáp thắc mắc 24/7 ngoài giờ tập | Học viên gym tự tập / Học viên hybrid | Phải chờ đợi PT trả lời các thắc mắc vụn vặt về ăn uống, phục hồi hoặc thay thế bài tập ngoài giờ tập trực tiếp. | Giảm thời gian chờ đợi phản hồi từ 12–24 tiếng xuống dưới 1 phút; tỷ lệ thắc mắc được giải quyết đúng đắn > 90%. | Workflow / Agent | Đây là bài toán hỗ trợ thông tin (QA/Copilot), có tính ứng dụng cao nhưng giá trị trải nghiệm tại phòng gym và sự "WOW" công nghệ không trực quan, mạnh mẽ bằng việc check form realtime qua camera. |

---

## Kết luận cá nhân

Sau khi trải qua quá trình scan rộng 15 vấn đề và đào sâu phân tích Top 3, tôi nhận thấy **vấn đề người tự tập sai form kỹ thuật mà không biết** (Top 1) là bài toán nhức nhối nhất, mang lại giá trị cao nhất cho người tập gym. 

Bản chất của việc tập gym là sự lặp đi lặp lại của các động tác vật lý dưới áp lực tạ. Điểm can thiệp đắt giá nhất của AI chính là đóng vai trò như một **"mắt thần" giám sát thời gian thực** (Real-time AI Agent). Nó giải quyết triệt để điểm nghẽn của việc tự soi gương hay quay video xem lại sau set tập vốn bị trễ và thiếu chính xác.

Tôi đề xuất hướng đi tập trung, tinh gọn cho MVP ban đầu:
- Tập trung phân tích form của **1–2 bài tập compound cốt lõi** và có tần suất tập cao nhất là **Squat** và **Bench Press**.
- Ứng dụng mô hình AI Agent quan sát trực tiếp qua camera điện thoại, phát hiện các lỗi form nguy hiểm ảnh hưởng trực tiếp đến khớp gối và cột sống để cảnh báo tức thì, đảm bảo an toàn tối đa cho newbie trước khi hướng đến việc tối ưu hóa hiệu suất cơ bắp.
