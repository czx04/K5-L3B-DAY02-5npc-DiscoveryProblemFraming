# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm:
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu):
- Quyết định cuối: Go / Not Yet / No-Go

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |
| 7 | | | | | |
| 8 | | | | | |
| 9 | | | | | |
| 10 | | | | | |
| 11 | | | | | |
| 12 | | | | | |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A | | |
| B | | |
| C | | |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: 
├── Opportunity A: 
├── Opportunity B: 
└── Opportunity C: 
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

-

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| | | | | | | | | |
| | | | | | | | | |
| | | | | | | | | |

**Candidate được chọn:**

**Vì sao chọn:**

**Vì sao loại các candidate còn lại:**

**Xử lý bất đồng (nếu có):**

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |

*Điền 4–6 giả định; xóa dòng thừa.*

Giả định nhóm kiểm chứng trong buổi này:

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn / Survey / Log, ticket, review

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong `report/assets/cp4-interview-snapshot-N.md`):

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | |
| Câu nói đáng nhớ nhất (nguyên văn) | |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | |
| Hiện đang xử lý bằng cách nào (workaround)? | |
| Mất bao lâu, bao lần? | |
| Insight / opportunity rút ra | |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| | | | |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text

```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

**Bottleneck chính:**

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text

```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | | | |
| Tổng thời gian | | | |
| Số bước thủ công | | | |
| Bottleneck chính | | | |
| Rủi ro mới phát sinh | | | |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

-

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô: **Độ mơ hồ Trung bình (Medium Ambiguity) × Độ phức tạp Cao (High Complexity)**.

```text
Độ phức tạp
    ▲
Cao │              [ BÀI CỦA NHÓM: DPIA WORKFLOW ]
    │              (Hàng chục hợp đồng cloud/agency, schema IT chằng chéo
    │               nhưng biểu mẫu đầu ra Mẫu 09/10 cố định)
    │
    │  [Rule: Phân loại file]
Thấp│
    └────────────────────────────────────────► Độ mơ hồ
       Thấp                             Cao
```

**Vì sao (Dựa trên số liệu khảo sát thực tế):**
- **Độ phức tạp cao**: Khảo sát thực tế từ 14 doanh nghiệp (50% Công nghệ/Phần mềm, 42.9% Ngân hàng/Fintech; 57.1% quy mô 50–200 người) cho thấy dữ liệu đầu vào phân tán ở nhiều định dạng phi cấu trúc. Hai khâu mất nhiều thời gian nhất theo khảo sát là: **Gom hợp đồng bên thứ ba (cloud, vận chuyển, agency...) — 71.4% (10/14)** và **Hỏi các phòng ban về thu thập, lưu trữ dữ liệu — 71.4% (10/14)**, theo sau là **Vẽ sơ đồ luồng dữ liệu — 57.1% (8/14)**. Việc đối soát chéo giữa hợp đồng nhà cung cấp và kiến trúc kỹ thuật có độ phức tạp nghiệp vụ rất cao.
- **Độ mơ hồ trung bình (không quá cao)**: Biểu mẫu đầu ra là **hoàn toàn xác định** theo quy định pháp luật tại Nghị định 356/2025/NĐ-CP (Mẫu số 09: Đánh giá tác động xử lý dữ liệu và Mẫu số 10: Chuyển dữ liệu ra nước ngoài). Các trường dữ liệu cần điền đã có phân loại pháp lý rõ ràng theo Điều 3 & Điều 4 Luật 91/2025/QH15. Mục tiêu đầu ra rất rõ: điền đúng, đủ và có bằng chứng đối chiếu.

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | Ban hành biểu mẫu bảng hỏi Excel/Word gửi các phòng ban tự điền; tổ chức họp đối soát dữ liệu định kỳ. | Đủ nếu công ty siêu nhỏ, dưới 3 đối tác dịch vụ và luồng dữ liệu tĩnh. | **Khảo sát phản ánh sự thất bại của No AI**: 71.4% đang dùng Google Form và 50.0% dùng Excel/Word thủ công khiến **64.3% mất từ 2 tuần đến trên 1 tháng** (42.9% mất > 1 tháng); **71.4% đánh giá độ khó ở mức 4–5/5**. | ❌ Không chọn |
| **Rule** (Regex / Form logic) | Dùng các bộ lọc từ khóa (CCCD, SĐT, AWS, Cloud) và form bắt buộc điền theo cấu trúc sẵn. | Đủ nếu mọi hợp đồng và tài liệu IT đều viết theo một khuôn mẫu chuẩn duy nhất. | **Rào cản ngôn ngữ tự nhiên**: 71.4% người tham gia khảo sát kẹt ở khâu gom và đọc hợp đồng bên thứ ba (DPA/Vendor contract). Hợp đồng đa dạng cách hành văn, tiếng Việt/tiếng Anh, regex không thể hiểu ngữ cảnh pháp lý và quan hệ chuyển giao dữ liệu. | ❌ Không chọn |
| **Workflow** (Pipeline AI đa bước có Human-in-the-loop) | Pipeline: Rule tiền xử lý & lọc PII thật → LLM trích xuất thực thể luồng dữ liệu & mapping Mẫu 09/10 → Tạo dự thảo có Citation nguồn → DPO/IT rà soát và bấm duyệt. | Đủ khi đầu vào là văn bản phi cấu trúc đa dạng, đầu ra là biểu mẫu pháp lý cố định, đòi hỏi độ chính xác cao và có con người chịu trách nhiệm pháp lý. | Rủi ro ảo giác (Hallucination) điều khoản hợp đồng; được kiểm soát triệt để bằng cơ chế bắt buộc trích dẫn Citation đối chiếu song song và giao diện thẩm định HITL cho DPO. | ✅ **CHỌN** |
| **Agent** (Autonomous AI Agent tự ra quyết định) | Agent tự động quét mạng nội bộ, tự trao đổi qua email với các phòng ban, tự ký số và tự nộp hồ sơ lên Bộ Công an. | Chỉ áp dụng khi hệ thống pháp luật cho phép AI đại diện pháp nhân và hệ thống có toàn quyền can thiệp vào vận hành công ty. | **Cực kỳ nguy hiểm và bất khả thi về mặt pháp lý**: Khảo sát cho thấy người làm chính là DPO/Compliance (42.9%) và IT/An toàn thông tin (42.9%). AI tự nộp hồ sơ sai có thể khiến doanh nghiệp bị phạt tới 5% doanh thu; không cơ quan quản lý nào chấp nhận hồ sơ do Agent tự nộp. | ❌ Không chọn |

**Mức chọn:** **AI Workflow (kết hợp Human-in-the-loop)**.

**Vì sao không chọn mức đơn giản hơn (No AI / Rule):**
- Bằng chứng từ khảo sát: Dù 71.4% doanh nghiệp đã dùng Google Form và 50% dùng Excel/Word (No AI), quá trình vẫn kéo dài trên 1 tháng ở 42.9% doanh nghiệp và 71.4% người làm thấy rất khó khăn (mức 4–5/5). Khâu đọc và gom hợp đồng bên thứ ba (71.4% gặp khó) đòi hỏi khả năng hiểu ngôn ngữ tự nhiên phi cấu trúc mà chỉ LLM trong AI Workflow mới xử lý được.

**Vì sao không chọn mức phức tạp hơn (Autonomous Agent):**
- Khảo sát ghi nhận 78.6% doanh nghiệp có nhu cầu cập nhật hồ sơ định kỳ hoặc khi có thay đổi hệ thống. Hồ sơ pháp lý bắt buộc phải gắn liền với trách nhiệm cá nhân của DPO và người đại diện pháp luật (chữ ký số, con dấu pháp nhân). Trao quyền tự trị hoàn toàn cho Agent là vi phạm nguyên tắc quản trị rủi ro cơ bản trong lĩnh vực tuân thủ pháp lý.

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | Trích xuất các thực thể dữ liệu (Loại dữ liệu cá nhân cơ bản/nhạy cảm, bên nhận dữ liệu, mục đích xử lý, thời gian lưu trữ, biện pháp bảo mật) từ tài liệu thô và dự thảo nội dung các trường thông tin của Mẫu số 09/10 kèm chỉ mục trích dẫn (Citation). |
| **Judgment** — con người cân nhắc, quyết định gì? | Chuyên viên DPO / Compliance / IT đánh giá tính chính xác của dữ liệu trích xuất, đối chiếu trích dẫn nguồn, xử lý các cảnh báo mâu thuẫn (Conflict Flags) giữa hợp đồng và thực tế hệ thống, quyết định bấm duyệt. |
| **Action** — hành động cuối cùng là gì, ai làm? | Xuất hồ sơ Mẫu 09/10 hoàn chỉnh (file .docx/.pdf); Đại diện pháp luật của doanh nghiệp ký số điện tử và nộp chính thức lên Cổng dịch vụ công Bộ Công an. |
| **Outcome** — đo kết quả bằng gì? | - Rút ngắn thời gian làm hồ sơ từ **trên 1 tháng (42.9% khảo sát)** hoặc **2–4 tuần (21.4% khảo sát)** xuống **dưới 4 ngày làm việc**.<br>- Giảm mức độ khó khăn từ **mức 4–5/5 (71.4% khảo sát)** xuống mức dễ quản lý.<br>- Hỗ trợ cập nhật định kỳ nhanh chóng cho **64.3% doanh nghiệp có nhu cầu cập nhật định kỳ**. |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | - Hợp đồng bên thứ ba: Cloud, cổng thanh toán, agency marketing, vận chuyển (PDF/Docx) — nguồn gây nghẽn số 1 (71.4% survey).<br>- Metadata/Schema hệ thống IT (Docx/JSON) — nguồn dữ liệu các phòng ban (71.4% survey).<br>- Chính sách bảo mật nội bộ. *(Đã được làm sạch và che PII thật)*. |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | Các thao tác chỉnh sửa, xác nhận hoặc loại bỏ trường dữ liệu của DPO trên giao diện đối soát được ghi nhận để cải thiện độ chính xác trích xuất cho các kỳ cập nhật định kỳ 6 tháng tiếp theo. |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng:
  - **Người dùng dứt khoát muốn ĐƯỢC HỖ TRỢ (Augment)**.
  - **Bằng chứng từ khảo sát**: 
    + 85.8% người trực tiếp phụ trách là chuyên sự chuyên môn cao: **DPO / Compliance (42.9%)** và **IT / An toàn thông tin (42.9%)**.
    + 57.1% doanh nghiệp tự làm nội bộ (35.7%) hoặc kết hợp nội bộ gom thông tin và tư vấn rà soát (21.4%).
    + Họ là người trực tiếp chịu trách nhiệm giải trình trước Cục A05 Bộ Công an. Do đó, họ cần một **AI** giúp tự động hóa 80% thời gian gom thông tin và bóc tách hợp đồng đối tác, nhưng quyền kiểm duyệt và ra quyết định cuối cùng (20%) bắt buộc phải thuộc về con người.
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào:
  - **BỎ SÓT (False Negative) TỆ HƠN RẤT NHIỀU**.
  - **Vì sao (Bằng chứng từ khảo sát)**: 
    + Khảo sát cho thấy **28.6% (4/14) doanh nghiệp gặp khó khăn ở bước "Sửa và bổ sung sau khi bị yêu cầu"**. 
    + Nếu AI bỏ sót một loại dữ liệu nhạy cảm (như CCCD, vị trí, tài khoản) hoặc bỏ sót một bên thứ ba (cloud nước ngoài), hồ sơ nộp lên sẽ bị Cục A05 đánh giá **Không đạt**, yêu cầu sửa đổi bổ sung kéo dài, hoặc nghiêm trọng hơn là bị xử phạt vi phạm hành chính tới **5% doanh thu** theo Nghị định 356. Ngược lại, nếu AI "báo nhầm", DPO chỉ mất 2 giây click chuột để gạt bỏ trường đó trên giao diện đối soát.
  - **Thiết kế đã xử lý thế nào**:
    1. Cấu hình Prompt và Extraction Engine ưu tiên tối đa **Độ bao phủ (High Recall)** hơn là Độ chính xác tuyệt đối (Precision).
    2. Bất cứ trường dữ liệu nào có dấu hiệu nghi vấn (Confidence score từ 60%–85%) đều được đưa vào danh sách **"Cần chuyên viên xác nhận lại" (Review Flag)** thay vì tự ý bỏ qua.
    3. Cung cấp cơ chế **Citation song song** giúp DPO bấm vào trường thông tin là xem ngay văn bản gốc để kiểm tra trong 5 giây.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** | |
| **AI intervention point** | |
| **Mức chọn** | No AI / Rule / Workflow / Agent |
| **Rủi ro & người kiểm tra** | |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| | | | |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | | |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | | |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | | |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | | |

### 8.2. Kết luận

**Quyết định:** Go / Not Yet / No-Go

**Lý do:**

**Nếu Go — pilot nhỏ nhất:**

**Nếu Not Yet — cần kiểm chứng gì trước:**

**Nếu No-Go — nên làm gì thay AI:**

**Ngưỡng dừng** (nếu sau … mà … thì quay về …):

---

## 9. Hạn chế và hướng tiếp theo

-

## 10. Tài liệu tham khảo

-
