# Day 24-Track 1-2A202600799-Trần Ngọc Thụy

# Mobility / Autonomous Driving - AI Harm Map

## 1. Chọn ngành

Ngành tôi chọn là **Mobility / autonomous driving**. Đây là nhóm hệ thống AI được dùng trong xe tự hành, robotaxi hoặc các tính năng hỗ trợ lái như giữ làn, tự điều chỉnh tốc độ, nhận diện vật thể, dự đoán hành vi người đi đường và hỗ trợ quyết định phanh/tránh.

Tôi chọn ngành này vì đây là một ngành **high-stakes**: AI không chỉ tạo nội dung hoặc đưa ra gợi ý, mà có thể tác động trực tiếp tới phương tiện đang di chuyển trong thế giới thật. Nếu hệ thống nhận diện sai, phản ứng chậm, thiết kế UX gây hiểu nhầm, hoặc quy trình vận hành không escalation kịp, hậu quả có thể là tai nạn, thương tích hoặc tử vong.

Các stakeholder chính gồm: tài xế, hành khách, người đi bộ, người đi xe máy/xe đạp, các xe khác trên đường, công ty triển khai, cơ quan quản lý và cộng đồng sống trong khu vực thử nghiệm/triển khai. Điểm đặc biệt của mobility là nhiều người bị ảnh hưởng **không chủ động chọn dùng sản phẩm**, ví dụ người đi bộ hoặc người tham gia giao thông bình thường.

## 2. Industry Risk Snapshot

| Câu hỏi | Low / Medium / High / Critical | Vì sao? |
|---|---|---|
| Nếu AI sai, có thể gây hại thể chất không? | Critical | Xe tự hành hoặc hệ thống hỗ trợ lái có thể trực tiếp gây va chạm, thương tích hoặc tử vong cho người đi bộ, hành khách, tài xế và người tham gia giao thông khác. |
| AI có ảnh hưởng đến quyết định hệ trọng không? | Critical | Hệ thống quyết định phanh, giữ làn, tránh vật cản, dừng xe hoặc tiếp tục di chuyển trong môi trường giao thông thật. |
| Hệ thống có đụng tới dữ liệu nhạy cảm không? | Medium | Hệ thống có thể thu thập video đường phố, vị trí, hành vi lái xe và dữ liệu cảm biến; mức nhạy cảm thấp hơn y tế nhưng vẫn có rủi ro riêng tư. |
| Nếu sai, hậu quả có khó đảo ngược không? | Critical | Tai nạn giao thông, thương tích, tử vong hoặc mất niềm tin công chúng rất khó khắc phục sau khi xảy ra. |
| Nếu triển khai rộng, blast radius có lớn không? | High | Một lỗi phần mềm hoặc thiết kế UX có thể ảnh hưởng tới hàng nghìn đến hàng triệu xe đang hoạt động trên đường. |
| Có cần human review hoặc escalation không? | Critical | Cần safety driver, giám sát vận hành, quy trình dừng khẩn cấp, báo cáo sự cố và cơ chế regulator review trước khi mở rộng. |
| **Risk profile tổng thể của ngành** | **Critical** | Mobility là ngành high-stakes vì AI tương tác trực tiếp với thế giới vật lý, trong môi trường phức tạp, tốc độ cao và có nhiều stakeholder không tự nguyện tham gia. |

## 3. Brief Case + Harm Map

### Case 1: Uber ATG self-driving crash ở Tempe, Arizona

| Field | Nội dung |
|---|---|
| Tên case | Uber ATG Tempe fatal crash |
| Ngành | Mobility / autonomous driving |
| Tổ chức / sản phẩm | Uber Advanced Technologies Group; xe thử nghiệm Volvo XC90 gắn hệ thống automated driving system |
| Use case AI | Xe thử nghiệm tự lái nhận diện môi trường, dự đoán vật thể, lập kế hoạch chuyển động và điều khiển xe trên đường công cộng. |
| Thời điểm | 18/03/2018; báo cáo NTSB được adopted ngày 19/11/2019 |
| Case xảy ra chuyện gì? | Một xe thử nghiệm tự lái của Uber đang chạy ở Tempe, Arizona đã va chạm với một người đi bộ đang băng qua đường ngoài vạch sang đường. NTSB kết luận sự cố liên quan đến giám sát không đầy đủ của operator, hạn chế trong thiết kế hệ thống và safety culture chưa đủ mạnh. |
| Stakeholder bị ảnh hưởng | Người đi bộ, safety driver, người tham gia giao thông, Uber ATG, cơ quan quản lý và cộng đồng đang sống gần khu thử nghiệm. |
| Số liệu chính | 1 người đi bộ 49 tuổi tử vong; operator đã vận hành xe khoảng 19 phút trước va chạm; NTSB phát hành báo cáo NTSB/HAR-19/03 dài 78 trang. |
| Trích nguồn ngắn | NTSB mô tả xe thử nghiệm tự động đã đâm và gây tử vong cho một người đi bộ 49 tuổi tại Tempe, Arizona. |
| Nguồn 1 | NTSB, `Collision Between Vehicle Controlled by Developmental Automated Driving System and Pedestrian, Tempe, Arizona, March 18, 2018`, NTSB/HAR-19/03: https://www.ntsb.gov/investigations/AccidentReports/Reports/HAR1903.pdf |
| Nguồn 2 | NTSB accident ID HWY18MH010, được dẫn trong báo cáo NTSB/HAR-19/03. |
| Ghi chú độ tin cậy | Primary source. Đây là báo cáo điều tra chính thức của cơ quan an toàn giao thông Hoa Kỳ. |

#### Harm Map Worksheet

| High-risk moment | Stakeholder bị ảnh hưởng | Failure mode | Layer bắt đầu lỗi | Harm xảy ra là gì? | Harm lens | Severity | Scale | Probability | Frequency | Vì sao? |
|---|---|---|---|---|---|---|---|---|---|---|
| Xe tự lái gặp người đi bộ băng qua đường trong điều kiện tối và cần quyết định phanh/tránh | Người đi bộ, safety driver, người đi đường | Escalation failure; over-reliance; harmful automation behavior | Model; Safety; UX | Hệ thống không phản ứng đủ an toàn, safety driver không can thiệp kịp, dẫn đến va chạm chết người | Injury | Critical | Medium | Medium | Low | Mức độ rất nặng vì có tử vong. Scale ở mức medium vì là thử nghiệm giới hạn, nhưng nếu cách thiết kế tương tự được nhân rộng thì blast radius tăng mạnh. |

### Case 2: Cruise robotaxi bị California DMV đình chỉ permit

| Field | Nội dung |
|---|---|
| Tên case | Cruise California permit suspension |
| Ngành | Mobility / autonomous driving |
| Tổ chức / sản phẩm | Cruise LLC, robotaxi tự hành tại California |
| Use case AI | Robotaxi không có tài xế an toàn vận hành trên đường công cộng, chở khách và tương tác với người đi bộ, xe khác, xe cứu hộ và cơ quan giao thông. |
| Thời điểm | 24/10/2023 |
| Case xảy ra chuyện gì? | California DMV đình chỉ ngay lập tức deployment permit và driverless testing permit của Cruise. DMV nêu rằng xe của Cruise không an toàn cho public operation, Cruise đã misrepresent thông tin liên quan đến an toàn công nghệ tự hành, và hoạt động thử nghiệm tạo unreasonable risk cho công chúng. |
| Stakeholder bị ảnh hưởng | Người đi bộ, hành khách robotaxi, người tham gia giao thông, cơ quan quản lý, Cruise/GM và người dân tại khu vực triển khai. |
| Số liệu chính | 2 loại permit bị đình chỉ ngay lập tức: autonomous vehicle deployment permit và driverless testing permit. |
| Trích nguồn ngắn | California DMV thông báo đình chỉ permit vì public safety là ưu tiên chính và có thể đình chỉ khi có unreasonable risk. |
| Nguồn 1 | California DMV, `DMV Statement on Cruise LLC Suspension`, 24/10/2023: https://www.dmv.ca.gov/portal/news-and-media/dmv-statement-on-cruise-llc-suspension/ |
| Nguồn 2 | AP News, `California regulators suspend recently approved San Francisco robotaxi service for safety reasons`, 24/10/2023: https://apnews.com/article/8aa872f6b87bbff59e9c86471e87b0e7 |
| Ghi chú độ tin cậy | Nguồn 1 là primary source từ regulator; nguồn 2 là secondary source dùng để đối chiếu bối cảnh. |

#### Harm Map Worksheet

| High-risk moment | Stakeholder bị ảnh hưởng | Failure mode | Layer bắt đầu lỗi | Harm xảy ra là gì? | Harm lens | Severity | Scale | Probability | Frequency | Vì sao? |
|---|---|---|---|---|---|---|---|---|---|---|
| Robotaxi không người lái hoạt động trên đường công cộng khi regulator cho rằng hệ thống chưa an toàn | Người đi bộ, hành khách, người đi đường, cơ quan quản lý | Escalation failure; safety governance failure; over-reliance | Safety; UX | Xe có thể gây rủi ro cho công chúng, đồng thời việc báo cáo/diễn giải thông tin an toàn không đầy đủ làm regulator và cộng đồng khó đánh giá nguy cơ thật | Injury; dignity loss; public trust loss | Critical | High | Medium | Medium | Severity critical vì tai nạn trên đường có thể gây thương tích nặng. Scale high vì robotaxi hoạt động trong không gian công cộng, ảnh hưởng cả người không chọn dùng dịch vụ. |

### Case 3: Tesla Autopilot / Autosteer recall năm 2023

| Field | Nội dung |
|---|---|
| Tên case | Tesla Autosteer recall 23V838 |
| Ngành | Mobility / autonomous driving |
| Tổ chức / sản phẩm | Tesla Autopilot / Autosteer trên Model S, Model X, Model 3 và Model Y |
| Use case AI | Hệ thống hỗ trợ lái Level 2 giữ làn, điều khiển tốc độ và hỗ trợ tài xế, nhưng vẫn yêu cầu con người giám sát liên tục. |
| Thời điểm | 12/2023 |
| Case xảy ra chuyện gì? | Tesla recall gần như toàn bộ xe có Autosteer tại Hoa Kỳ để cập nhật phần mềm. Vấn đề chính là kiểm soát hệ thống có thể không đủ để ngăn tài xế misuse Autosteer hoặc không duy trì trách nhiệm giám sát khi hệ thống đang bật. |
| Stakeholder bị ảnh hưởng | Tài xế Tesla, hành khách, người đi đường, người đi bộ, cơ quan quản lý và Tesla. |
| Số liệu chính | Khoảng 2,031,220 xe bị ảnh hưởng trong recall 23V838. |
| Trích nguồn ngắn | NHTSA/Tesla recall mô tả Autosteer cần remedy vì driver engagement controls có thể không đủ trong một số điều kiện. |
| Nguồn 1 | NHTSA, Part 573 Safety Recall Report 23V838, Tesla Autosteer: https://static.nhtsa.gov/odi/rcl/2023/RCLRPT-23V838-3326.PDF |
| Nguồn 2 | AP News, `Tesla recalls nearly all vehicles sold in US to fix system that monitors drivers using Autopilot`, 13/12/2023: https://apnews.com/article/8060508627a34e6af889feca46eb3002 |
| Ghi chú độ tin cậy | Nguồn 1 là recall report chính thức; nguồn 2 là secondary source giúp đối chiếu số lượng và bối cảnh điều tra NHTSA. |

#### Harm Map Worksheet

| High-risk moment | Stakeholder bị ảnh hưởng | Failure mode | Layer bắt đầu lỗi | Harm xảy ra là gì? | Harm lens | Severity | Scale | Probability | Frequency | Vì sao? |
|---|---|---|---|---|---|---|---|---|---|---|
| Tài xế bật Autosteer trong điều kiện không phù hợp hoặc mất tập trung vì tin hệ thống tự lái được nhiều hơn thực tế | Tài xế, hành khách, người đi đường, người đi bộ | Over-reliance; escalation failure; misuse | UX; Safety | Tài xế không giám sát liên tục, hệ thống không buộc can thiệp đủ mạnh, làm tăng nguy cơ va chạm | Injury | High | High | Medium | Medium | Severity high vì có nguy cơ tai nạn nghiêm trọng. Scale high vì hơn 2 triệu xe bị ảnh hưởng, dù không phải mọi xe đều gặp harm. |

## 4. Pattern rủi ro của ngành Mobility

Các case mobility có pattern chung là lỗi không chỉ nằm ở model nhận diện đường hay vật thể, mà còn nằm ở toàn bộ hệ thống: UX làm người dùng over-rely, safety layer không escalation đủ nhanh, quy trình vận hành chưa dừng triển khai kịp thời, và báo cáo an toàn chưa tạo đủ niềm tin cho regulator. Điểm nguy hiểm nhất là AI hoạt động trong thế giới vật lý, nơi một quyết định sai trong vài giây có thể gây thương tích hoặc tử vong. Vì vậy ngành này cần bar ship rất cao: kiểm thử theo kịch bản hiếm nhưng nguy hiểm, giám sát human-in-the-loop rõ ràng, log sự cố minh bạch, giới hạn operational design domain và cơ chế fail-safe trước khi mở rộng.

Nếu là team sản phẩm, việc cần sửa trước là giới hạn nơi/tình huống hệ thống được phép hoạt động, tăng driver/operator monitoring, thiết kế cảnh báo không gây hiểu nhầm về năng lực tự lái, và tạo quy trình dừng xe/dừng rollout khi xuất hiện incident nghiêm trọng.

## 5. Bảng so sánh nhóm

| Ngành | Harm dễ gặp nhất | Failure mode hay lặp lại | Layer hay bắt đầu lỗi | Risk profile tổng thể | Vì sao? |
|---|---|---|---|---|---|
| HR / tuyển dụng | Opportunity loss, bias/fairness, dignity loss, rủi ro pháp lý | Bias, automation bias, over-reliance, thiếu human review | Model, Grounding, UX | High | AI có thể loại ứng viên sai, khuếch đại bias trong dữ liệu tuyển dụng và làm mất cơ hội việc làm. Hậu quả thường không gây hại thể chất nhưng ảnh hưởng lớn đến công bằng, thu nhập và danh dự cá nhân. |
| Giáo dục / AI tutor | Opportunity loss (giảm tư duy), Misinformation (học sai), Dignity loss (kỷ luật oan) | Over-reliance, Hallucination, Bias | UX, Model, Grounding | High | Đối tượng nhạy cảm, dễ bị tổn thương danh dự và nợ tư duy lâu dài nếu phụ thuộc AI hoặc AI đánh giá sai. |
| Y tế / symptom checker / health assistant | Injury, harmful advice, delayed intervention, privacy loss | Hallucination, harmful advice, over-reliance, escalation failure | Safety, Grounding, Model, UX | Critical | Nếu AI tư vấn sai hoặc không khuyên người bệnh đi khám kịp thời, hậu quả có thể là chậm điều trị, tổn hại sức khỏe hoặc tử vong. Dữ liệu y tế cũng rất nhạy cảm nên cần guardrail và human review mạnh. |
| Mobility / autonomous driving | Injury, tử vong, mất niềm tin công chúng, rủi ro pháp lý | Escalation failure, over-reliance, safety governance failure | Safety, UX, Model | Critical | AI điều khiển hoặc hỗ trợ điều khiển xe trong môi trường vật lý phức tạp. Sai sót có thể gây hại cho cả người dùng và người không tự nguyện tham gia hệ thống. |
| Media / news / social / political assistant | Misinformation diện rộng, mất uy tín (Dignity loss) | Hallucination nặng, bóp méo sự thật, automation bias | Model sinh ảo giác, UX lừa dối người dùng | High | AI sản xuất và phát tán tin giả với tốc độ/quy mô không giới hạn, như mạng lưới BeeUp hay Apple AI. Rất khó thu hồi và đính chính, gây khủng hoảng truyền thông. |
| Content creator | Copyright risk, misinformation, reputation loss, bias, synthetic media misuse | Hallucination, misuse/jailbreak, plagiarism, bias | Model, Grounding, Safety, UX | Medium | AI tạo nội dung có thể sao chép phong cách/tác phẩm, tạo thông tin sai hoặc deepfake làm hại danh tiếng. Severity thường thấp hơn mobility/y tế, nhưng scale cao vì nội dung có thể phát tán rất nhanh. |

## 6. Kết luận chung

Nhìn chung, các ngành AI đều có rủi ro nhưng khác nhau về **mức độ nghiêm trọng**, **quy mô ảnh hưởng** và **khả năng đảo ngược hậu quả**. Mobility và y tế có risk profile cao nhất vì lỗi AI có thể gây hại trực tiếp đến sức khỏe, tính mạng hoặc làm chậm can thiệp cần thiết. Media và giáo dục có severity vật lý thấp hơn, nhưng scale và frequency có thể rất lớn vì thông tin sai hoặc phụ thuộc AI có thể lan rộng và lặp lại hằng ngày. HR và content creator thường không gây hại thể chất, nhưng ảnh hưởng mạnh đến cơ hội, danh dự, quyền lợi và niềm tin xã hội.

Pattern chung của bảng so sánh là lỗi AI hiếm khi chỉ nằm ở model. Nhiều harm bắt đầu từ cách hệ thống được thiết kế, dữ liệu grounding không đủ tốt, UX làm người dùng quá tin tưởng, hoặc thiếu human review khi gặp tình huống high-stakes. Vì vậy, khi triển khai AI trong các ngành này, cần xác định rõ mức rủi ro của từng use case, đặt guardrail phù hợp, có cơ chế escalation cho con người và không nên scale rộng trước khi chứng minh được độ an toàn trong các tình huống khó.

Riêng với **Mobility / autonomous driving**, kết luận của tôi là ngành này cần tiêu chuẩn triển khai nghiêm ngặt nhất: giới hạn điều kiện vận hành, kiểm thử kỹ các edge case ngoài đường thật, giám sát tài xế/operator, fail-safe rõ ràng, báo cáo sự cố minh bạch và phối hợp chặt với regulator. Lý do là một lỗi nhỏ trong vài giây có thể tạo hậu quả không thể đảo ngược cho cả người dùng lẫn người không chọn tham gia hệ thống.
