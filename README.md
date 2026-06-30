# Day24-Track1-2A202600799- Trần Ngọc Thụy

# Lab Assignment Day 24

## Cá nhân

1. **Chọn 1 ngành từ danh sách có sẵn**
   - HR / tuyển dụng
   - Giáo dục / AI tutor
   - Y tế / symptom checker / health assistant
   - Mobility / autonomous driving
   - Media / news / social / political assistant
   - Content creator

2. Điền **Industry Risk Snapshot** cho ngành đó: chấm nhanh risk profile ở mức ngành để ước lượng harm chính, mức độ high-stakes, dữ liệu nhạy cảm, và nhu cầu human review.

3. **Tìm & phân tích 2-3 case study** AI có thật trong cùng ngành. Với mỗi case: viết Brief Case có số liệu + nguồn, rồi điền Harm Map Worksheet.

## Thảo luận nhóm

1. Mỗi thành viên share các case tìm được.
2. Thảo luận để tìm ra **pattern chung**: ngành nào high-stakes hơn, harm nào hay lặp lại, layer nào hay bắt đầu lỗi, ngành nào cần human-in-the-loop hoặc guardrail gắt hơn.
3. Chốt 1 bảng tổng hợp ngắn của cả bàn, đưa vào file cá nhân.

---

# Day 24 Lab -- Case Study Hunt và Harm Map theo Ngành

> Mỗi học viên chọn 1 ngành, tìm 2-3 case study AI có thật trong cùng ngành đó, viết brief case có số liệu và nguồn, rồi phân tích từng case bằng Harm Map Worksheet. Sau đó cả bàn share toàn bộ case và so sánh risk profile giữa các ngành.

---

## Nộp bài

- Mỗi học viên nộp `1 repo cá nhân` tên `Day24-Track1-MaHV-HoVaTen`.
- Trong repo có `1 Industry Risk Snapshot`.
- Trong repo có `2-3 Brief Case`, mỗi case đi kèm `1 Harm Map Worksheet`.
- Trong repo có `1 file tổng hợp của nhóm` chứa `1 bảng so sánh các ngành` mà nhóm đã phân tích.
- Nộp `1 link repo cá nhân`.
- Không đưa API key, token, credential, hoặc dữ liệu cá nhân nhạy cảm vào repo.

---

## Mục tiêu

- Tìm case study AI có thật và có nguồn.
- Tóm tắt được fact chính, số liệu chính, và độ tin cậy của nguồn.
- Phân tích được từng case bằng `failure mode`, `layer`, `harm`, `Severity`, `Scale`, `Probability`, `Frequency`.
- So sánh được risk profile giữa các ngành.

---

## Ngành được chọn trước

Mỗi học viên chọn `1 ngành` từ danh sách sau:

1. `HR / tuyển dụng`
2. `Giáo dục / AI tutor`
3. `Y tế / symptom checker / health assistant`
4. `Mobility / autonomous driving`
5. `Media / news / social / political assistant`
6. `Content creator`

---

## Đầu ra bắt buộc

### Cá nhân

- `1 Industry Risk Snapshot`
- `2-3 Brief Case`
- `2-3 Harm Map Worksheet`
- `1 đoạn tổng hợp ngắn` về pattern rủi ro của ngành

### Cả bàn

- share toàn bộ `2-3 case` của mỗi thành viên
- `1 bảng so sánh các ngành`
- `1 đoạn tổng hợp ngắn` về risk profile giữa các ngành

---

## Bước 1 -- Chọn ngành và chấm Risk Profile

Điền bảng này trước khi tìm case.

### Industry Risk Snapshot

| Câu hỏi | Low / Medium / High / Critical | Vì sao? |
|---|---|---|
| Nếu AI sai, có thể gây hại thể chất không? |  |  |
| AI có ảnh hưởng đến quyết định hệ trọng không? |  |  |
| Hệ thống có động tới dữ liệu nhạy cảm không? |  |  |
| Nếu sai, hậu quả có khó đảo ngược không? |  |  |
| Nếu triển khai rộng, blast radius có lớn không? |  |  |
| Có cần human review hoặc escalation không? |  |  |
| **Risk profile tổng thể của ngành** |  |  |

### Gợi ý nhanh theo ngành

- `HR / tuyển dụng`: fairness, opportunity loss, dignity, legal exposure
- `Giáo dục / AI tutor`: misinformation, over-reliance, chất lượng học, unequal support
- `Y tế / symptom checker / health assistant`: injury, harmful advice, delayed intervention, dữ liệu sức khỏe
- `Mobility / autonomous driving`: physical safety, fail-safe, escalation, system reliability
- `Media / news / social / political assistant`: misinformation, manipulation, public trust, social impact at scale
- `Content creator`: copyright, misinformation, reputation, bias, synthetic media misuse

---

## Bước 2 -- Tìm 2-3 case study có thật trong cùng ngành

Tìm khoảng `5-8 case` sơ bộ rồi lọc xuống `2-3 case` mạnh nhất.

### Tiêu chí chọn case

Mỗi case nên trả lời được các câu hỏi sau:

- AI được dùng để làm gì?
- Chuyện gì đã xảy ra?
- Ai bị ảnh hưởng?
- Có ít nhất `1 số liệu` không?
- Có đủ dữ kiện để điền worksheet không?

Nếu case thiếu số liệu hoặc nguồn yếu, đổi case khác.

### Dùng công cụ tìm

Bạn có thể dùng:

- `search engine` để tìm báo, report, paper, filing, notice, audit, benchmark
- `AI assistant có web/search` để shortlist case ban đầu và gợi ý nguồn
- `nguồn chính thức / nguồn học thuật` để lấy bằng chứng mạnh hơn

### Ưu tiên nguồn

1. `Primary source` court filing, regulator notice, benchmark paper, audit report, official announcement, transparency report, company report
2. `High-quality secondary source` bài điều tra, newsroom có fact-check, tổ chức nghiên cứu có trích nguồn rõ
3. `Nguồn phụ để đối chiếu` blog kỹ thuật, bài tổng hợp, explainer article

### Gợi ý prompt

Thay `[NGÀNH]` hoặc `[TÊN CASE]` bằng nội dung bạn đang làm.

- `Tìm cho tôi 5-8 case study AI có thật trong ngành [NGÀNH]. Chỉ giữ case có ít nhất 1 số liệu và ít nhất 1 nguồn đáng tin.`
- `Từ danh sách trên, chọn 3 case phù hợp nhất để làm harm map. Với mỗi case, gợi ý sơ bộ harm lens, failure mode, layer có thể liên quan, và fact nào tôi cần tự verify.`
- `Với case [TÊN CASE], giúp tôi tóm tắt: AI được dùng để làm gì, chuyện gì đã xảy ra, stakeholder nào bị ảnh hưởng, số liệu chính là gì, và nên đọc nguồn nào trước.`

Không copy thẳng output của AI vào bài. Luôn tự mở nguồn và kiểm lại fact.

### Checklist kiểm nguồn

Trước khi chốt case, kiểm lại:

- đã mở nguồn thật chưa?
- số liệu nằm ở đâu trong nguồn?
- mốc thời gian có đúng không?
- đây là nguồn gốc hay nguồn trích lại?
- nếu có 2 nguồn, chúng có mâu thuẫn nhau không?

Không được ghi `ChatGPT`, `Claude`, `Perplexity` làm nguồn của case.

---

## Bước 3 -- Viết Brief Case cho từng case

Với mỗi case, điền một bảng ngắn để lưu fact chính, số liệu, và nguồn.

### Template Brief Case

| Field | Bạn điền gì |
|---|---|
| Tên case | Tên ngắn gọn, dễ gọi lại |
| Ngành | Một trong 6 ngành của bài |
| Tổ chức / sản phẩm | Ai liên quan đến case này |
| Use case AI | AI đang được dùng để làm gì |
| Thời điểm | Năm hoặc mốc thời gian chính |
| Case xảy ra chuyện gì? | Tóm tắt 2-3 câu, chỉ viết fact chính |
| Stakeholder bị ảnh hưởng | User, ứng viên, người bệnh, người đi đường, cử tri, nhà sáng tạo... |
| Số liệu chính | Ít nhất 1 con số có ý nghĩa |
| Trích nguồn ngắn | 1 câu fact ngắn hoặc paraphrase có dẫn nguồn |
| Nguồn 1 | Tên nguồn + ngày + link hoặc citation |
| Nguồn 2 | Nguồn đối chiếu nếu có |
| Ghi chú độ tin cậy | Primary / secondary / có conflict không? |

### Gợi ý cho ô `Số liệu chính`

Viết theo kiểu:

- `X người bị ảnh hưởng`
- `Y USD tiền phạt hoặc settlement`
- `tỉ lệ false positive cao hơn Z lần`
- `N complaint hoặc incident`
- `mốc thời gian cụ thể`

Nếu không có được ít nhất một con số có nghĩa, nên đổi case.

---

## Bước 4 -- Điền Harm Map Worksheet cho từng case

Với mỗi case, điền `1 worksheet`.

### Template Harm Map Worksheet

| High-risk moment | Stakeholder bị ảnh hưởng | Failure mode | Layer bắt đầu lỗi | Harm xảy ra là gì? | Harm lens | Severity | Scale | Probability | Frequency | Vì sao? |
|---|---|---|---|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |  |  |  |  |

### Label gợi ý

#### `Failure mode`

- `Hallucination`
- `Bias / fairness`
- `Sycophancy`
- `Over-reliance`
- `Harmful advice`
- `Privacy leak`
- `Escalation failure`
- `Misuse / jailbreak`

#### `Layer bắt đầu lỗi`

- `UX`
- `Grounding`
- `Safety`
- `Model`

#### `Harm lens`

- `Misinformation`
- `Opportunity loss`
- `Injury`
- `Privacy loss`
- `Dignity loss`

### Cách chấm 4 yếu tố

#### `Severity`

Nếu harm này xảy ra, nó nặng đến đâu?

- `Low`: phiền toái nhẹ, dễ sửa
- `Medium`: có hại thật nhưng còn khôi phục được
- `High`: mất tiền, mất cơ hội, rủi ro công bằng / pháp lý / dữ liệu đáng kể
- `Critical`: có thể gây hại thể chất, chậm can thiệp, hoặc hậu quả khó đảo ngược

#### `Scale`

Harm này ảnh hưởng rộng đến bao nhiêu người hoặc nhóm?

- `Low`
- `Medium`
- `High`

#### `Probability`

Harm này có dễ xảy ra không?

- `Low`
- `Medium`
- `High`

#### `Frequency`

Harm này nếu có, nó lặp lại thường xuyên đến mức nào?

- `Low`
- `Medium`
- `High`

### Lưu ý

- `Severity` không phải `Probability`
- `Probability` không phải `Frequency`
- `Scale` không phải `Severity`

---

## Bước 5 -- Share toàn bộ case với cả bàn

Mỗi học viên share `toàn bộ 2-3 case` của mình trong `4-5 phút`.

Flow share:

1. Ngành tôi chọn là gì?
2. Tôi đã tìm được những case nào?
3. Với từng case: AI dùng để làm gì, chuyện gì đã xảy ra, số liệu chính là gì?
4. Với từng case: failure mode, layer, harm chính là gì?
5. Nhìn cả 2-3 case, pattern rủi ro của ngành là gì?
6. Nếu là team sản phẩm, tôi sẽ sửa gì trước?

---

## Bước 6 -- So sánh risk profile giữa các ngành

Sau khi mọi người share xong, cả bàn điền bảng sau:

| Ngành | Harm dễ gặp nhất | Failure mode hay lặp lại | Layer hay bắt đầu lỗi | Risk profile tổng thể | Vì sao? |
|---|---|---|---|---|---|
| HR / tuyển dụng |  |  |  |  |  |
| Giáo dục / AI tutor |  |  |  |  |  |
| Y tế / symptom checker / health assistant |  |  |  |  |  |
| Mobility / autonomous driving |  |  |  |  |  |
| Media / news / social / political assistant |  |  |  |  |  |
| Content creator |  |  |  |  |  |

### Câu hỏi thảo luận

- Ngành nào có `Severity` tiềm năng cao nhất?
- Ngành nào có `Scale` tiềm năng lớn nhất?
- Ngành nào có `Probability` hoặc `Frequency` cao nhất?
- Ngành nào xử lý dữ liệu nhạy cảm rõ nhất?
- Ngành nào cần human-in-the-loop rõ nhất?
- Ngành nào cần bar "được ship" cao nhất?
