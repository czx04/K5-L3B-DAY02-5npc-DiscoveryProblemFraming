# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: 5npc
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu): Khi doanh nghiệp phải lập hồ sơ đánh giá tác động xử lý dữ liệu cá nhân theo luật mới, chuyên viên pháp chế/DPO mất 2–4 tuần chủ yếu để đi hỏi từng phòng ban đang thu thập dữ liệu gì, lưu ở đâu, chia sẻ cho ai, trong khi hồ sơ phải đạt ngay lần nộp đầu và cập nhật định kỳ.
- Quyết định cuối: 

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Hoàng Minh Quyền | Khi phải lập hồ sơ đánh giá tác động dữ liệu cá nhân theo luật mới, tôi muốn biết mọi phòng ban thu dữ liệu gì, lưu đâu, chia sẻ cho ai, để nộp đạt ngay lần đầu | Pháp chế / DPO doanh nghiệp lớn (bán lẻ, bảo hiểm, fintech, bệnh viện) | Hỏi và gom thông tin từ các phòng ban: 7–11 ngày công | Doanh nghiệp tự làm hay thuê trọn gói tư vấn? AI hiểu sai luật thì ai chịu? () |
| 2 | Hoàng Minh Quyền | Khi tới kỳ kiểm kê khí nhà kính / báo cáo CBAM, tôi muốn có đủ số liệu điện, nhiên liệu cả năm, để báo cáo đúng, không nộp lại | Cán bộ ESG nhà máy, DN xuất khẩu sang EU | Xin và nhập tay số liệu từ kế toán, kho, kỹ thuật: 2–4 tuần | FPT VertZéro và nền tảng khác đã làm chưa? () |
| 3 | Ngô Minh Cương | Khi bàn giao ca trực, tôi muốn nắm nhanh sự cố chưa đóng, để ca sau không sót việc | Kỹ sư on-call | Viết tóm tắt bàn giao: 10–15'/ca, hay sót thread Slack | Checklist bắt buộc đã đủ chưa? PagerDuty/incident.io có sẵn tính năng chưa? () |
| 4 | Ngô Minh Cương | Khi bị khách khiếu nại thiếu hàng trên sàn, tôi muốn tìm nhanh video đóng gói của đơn đó, để nộp bằng chứng trong 24h | Chủ shop, trưởng ca kho TMĐT | Tua camera tìm đúng lúc đóng đơn: 8–12'/đơn | Quét mã vạch + camera (Rule) đã giải được chưa? () |
| 5 | Đoàn Trí Hùng | Khi nhận task mới, tôi muốn hiểu rõ yêu cầu nghiệp vụ và phạm vi code cần sửa, để làm đúng ngay từ đầu | Developer dự án Nhật, leader | Đối chiếu BD/DD với source code: 10–20', gây hỏi lại leader | Tài liệu không được đưa ra AI ngoài, checklist đã đủ chưa? () |
| 6 | Dư Văn Hùng | Mỗi tuần, tôi muốn biết game nào trong portfolio bị review xấu tăng đột biến và vì sao, để xử lý trước khi rating tụt | Team ASO, Product/LiveOps nhà phát hành 100+ game | Đọc, dịch, phân loại review đa ngôn ngữ: 15–20'/game/tuần | AppFollow, AppTweak đã giải chưa? () |
| 7 | Trần Quang Hà | Khi tự luyện IELTS Speaking/Writing, tôi muốn nhận ra lỗi diễn đạt lặp lại, để sửa dứt điểm trước khi thi | Người ôn thi IELTS | Tự tra và rà lỗi: 2–3 giờ/lần | ChatGPT / app chấm IELTS có sẵn đã đủ chưa? Ai trả tiền? () |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A. Hồ sơ tuân thủ bắt buộc | #1 Hồ sơ dữ liệu cá nhân, #2 Kiểm kê khí nhà kính / CBAM | Luật ép phải làm, sai thì bị phạt hoặc nộp lại; nghẽn ở bước đi gom thông tin từ nhiều phòng ban |
| B. Tổng hợp thông tin rải rác để chuyển giao | #3 Bàn giao ca trực, #5 Phân tích yêu cầu nghiệp vụ, #6 ReviewRadar | Thông tin nằm ở nhiều nguồn (Slack, Jira, tài liệu, review); người làm phải đọc và tóm tắt cho người sau |
| C. Tìm bằng chứng / lỗi trong khối dữ liệu lớn | #4 Video đóng gói TMĐT, #7 Lỗi luyện IELTS | Phải dò tay trong nhiều dữ liệu (video, bài viết) để tìm đúng chỗ cần |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Giảm thời gian lập hồ sơ đánh giá tác động xử lý dữ liệu cá nhân lần đầu
         từ 2–4 tuần công xuống dưới 1 tuần, và hồ sơ đạt ngay lần nộp đầu
├── Opportunity A: Thông tin dữ liệu nằm rải rác ở nhiều phòng ban; DPO phải đi hỏi từng nơi,
│                  chờ trả lời và hỏi lại nhiều vòng (bước 1, ~5–8 ngày công)
│   └── Phòng ban không biết mình đang "xử lý dữ liệu cá nhân" gì, trả lời bảng hỏi thiếu hoặc
│       sai thuật ngữ pháp lý
├── Opportunity B: Không biết bên thứ ba nào đang nhận dữ liệu; hợp đồng với bên xử lý nằm ở nhiều
│                  nơi, phải đọc từng hợp đồng để tìm điều khoản chia sẻ (bước 2, ~2–3 ngày công)
└── Opportunity C: Không chắc hồ sơ đã đủ và đúng Mẫu 09/10 trước khi nộp; sợ bị đánh giá
                   "không đạt" rồi phải bổ sung trong 30 ngày
    └── Mỗi 6 tháng hoặc khi có mục đích xử lý mới lại phải gom lại từ đầu vì không biết
        cái gì đã thay đổi
     ✗ "Chatbot hỏi đáp Luật 91/2025"            ← solution, gạch khỏi tầng này
     ✗ "AI đọc hợp đồng, tự soạn danh mục dữ liệu" ← solution, gạch khỏi tầng này
     ✗ "Phần mềm data mapping (OneTrust, …)"     ← tên công cụ, gạch khỏi tầng này
     ✗ "Bộ template + checklist Mẫu 09"          ← solution (dù không dùng AI), gạch khỏi tầng này
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- "Chatbot hỏi đáp Luật 91/2025": là công cụ; nhu cầu thật phía sau là "phòng ban không hiểu mình xử lý dữ liệu gì" → đã gộp vào nhánh con của Opportunity A.
- "AI đọc hợp đồng, tự soạn danh mục dữ liệu": là giả thuyết giải pháp cho Opportunity B, để dành cho CP6 (mức can thiệp AI).
- "Phần mềm data mapping kiểu OneTrust": là tên công cụ; đưa sang mục 3.3 Research giải pháp đã có.
- "Bộ template + checklist theo Mẫu 09/10": là phương án No AI cho Opportunity C, đưa sang bảng so sánh 4 mức ở 6.2.

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| #1 Hồ sơ đánh giá tác động dữ liệu cá nhân | 5 | 5 | 3 | 5 | 3 | 5 | 2 | **28** |
| #6 ReviewRadar (review xấu tăng đột biến) | 4 | 4 | 3 | 3 | 5 | 3 | 4 | 26 |
| #2 Kiểm kê khí nhà kính / CBAM | 4 | 4 | 4 | 4 | 3 | 4 | 2 | 25 |

Shortlist lấy đại diện mạnh nhất của cluster A (#1, #2) và cluster B (#6). Cluster C bị loại sớm: #4 đã có giải pháp quét mã vạch + camera; #7 actor là cá nhân, khó trả lời câu "ai trả tiền".

Giải thích điểm:

- **#1:** Actor rõ (DPO ở doanh nghiệp không được miễn trừ). Quy trình đã có khung pháp lý cố định (Mẫu 09/10, nộp A05, bổ sung trong 30 ngày). Impact đo được bằng ngày công và kết quả đạt/không đạt. Có đủ 4 mức để so sánh: template/checklist (No AI) → Rule → Workflow → Agent. **Pain chỉ 3** vì 2–4 tuần công vẫn là giả định R&D. **Domain chỉ 2** vì cả nhóm chưa ai làm pháp chế.
- **#6:** Vừa sức lab nhất (review công khai, lấy được ngay) và Dư Văn Hùng hiểu domain. Nhưng AppFollow/AppTweak đã có gắn tag và phân tích cảm xúc review, nên khoảng trống còn lại hẹp. Impact (15–20'/game/tuần) nhỏ hơn #1.
- **#2:** Có bằng chứng pain mạnh nhất (Tuổi Trẻ 25/6/2026: có doanh nghiệp gửi 3 lần, 3 bộ số liệu khác nhau). Nhưng dữ liệu nằm trong hóa đơn và phiếu kho nội bộ, khó có mẫu thật trong lab. Đã có FPT IS VertZéro và các nền tảng khác.

**Candidate được chọn:** #1, hồ sơ đánh giá tác động xử lý dữ liệu cá nhân.

**Vì sao chọn:** Tổng điểm cao nhất. Nghĩa vụ mới có hiệu lực từ 1/1/2026, chuyển sang tiền kiểm (đạt/không đạt), phải cập nhật 6 tháng/lần, nên nhu cầu bắt buộc và lặp lại. Quy trình theo mẫu cố định nên dễ chỉ ra bottleneck (bước 1–2: gom thông tin từ phòng ban, đọc hợp đồng bên thứ ba). Chọn kèm rủi ro đã biết: pain chưa có số đo và nhóm yếu domain. Hai điểm này chuyển thành giả định ưu tiên kiểm chứng ở CP4.

**Vì sao loại các candidate còn lại:**

- #6: điểm khá nhưng công cụ thương mại đã giải phần lớn; nếu làm dễ thành "làm lại AppFollow". Ghi vào hướng tiếp theo.
- #2: pain thật nhưng không lấy được dữ liệu mẫu trong lab, và đã có nền tảng trong nước làm.
- #3, #5: #3 trùng tính năng PagerDuty/incident.io; #5 vướng quy định không đưa tài liệu khách hàng Nhật ra AI ngoài.

**Xử lý bất đồng (nếu có):** *(nhóm điền: ai muốn chọn candidate khác, lý do, nhóm chốt thế nào)*

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | Lập hồ sơ lần đầu mất từ 2 tuần công trở lên, và phần lớn thời gian nằm ở bước gom thông tin từ phòng ban và hợp đồng bên thứ ba | Value | 5 | 2 | **Có** |
| 2 | Doanh nghiệp tự làm, hoặc ít nhất tự gom thông tin nội bộ, chứ không giao trọn gói cho công ty tư vấn | Viability | 5 | 1 | **Có** |
| 3 | Hồ sơ phải cập nhật định kỳ, nên đây là việc lặp lại chứ không phải làm một lần rồi thôi | Value | 4 | 3 (Nghị định 356) | **Có** |
| 4 | Công cụ đang dùng chủ yếu là Excel/Word và bảng hỏi gửi phòng ban; chưa có phần mềm làm theo mẫu Việt Nam | Value | 4 | 2 | **Có** |
| 5 | Có thể lấy được nguồn đầu vào (hợp đồng, chính sách quyền riêng tư, danh sách hệ thống) để thử trong lab mà không lộ dữ liệu thật | Feasibility | 4 | 1 | Chưa, để CP5–6 |
| 6 | DPO/luật sư chấp nhận rà soát bản nháp do máy soạn thay vì tự viết từ đầu | Usability | 4 | 1 | Chưa, để CP6 |

Giả định nhóm kiểm chứng trong buổi này: **#1, #2, #3, #4**, bằng micro survey.

### 3.2. Kiểm chứng

Cách đã dùng: **Survey** (Google Form, 10 câu, ẩn danh). Kết quả tổng hợp: [report/assets/cp4-survey-result.md](../assets/cp4-survey-result.md).

- **Mẫu:** 14 phản hồi, gồm 6 DPO/Compliance, 6 IT/An toàn thông tin, 2 HR.
  - Lĩnh vực: 7 công nghệ/phần mềm, 6 ngân hàng/tài chính/fintech, 1 vận tải.
  - Quy mô: 8 công ty 50–200 người, 5 công ty 200–1.000 người.
- **Nhóm "đã thực sự làm":** 9/14 người vừa trả lời đã làm xong hoặc đang làm, vừa không chọn "chưa làm lần nào". Các số về thời gian và cách làm bên dưới tính trên 9 người này.
- **Lưu ý chất lượng dữ liệu:**
  - Cả 14 phản hồi đến trong 26 phút, nhiều khả năng từ cùng một vòng quen biết, nên mẫu không đại diện cho thị trường.
  - Câu 7 ghi "chọn tối đa 2" nhưng form không chặn; 11/13 người chọn từ 3 bước trở lên, nên chỉ đọc được thứ tự tương đối.
  - Có 2 phản hồi mâu thuẫn: "chưa làm" nhưng vẫn ghi thời gian.
  - 6 người chọn "phần mềm chuyên dụng" nhưng không ai ghi tên phần mềm.

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Survey: thời gian (câu 6) | 9 | 5/9 mất từ 2 tuần trở lên, trong đó 4/9 mất trên 1 tháng | **4/9 chỉ mất 1–2 tuần**, ít hơn mức 2–4 tuần nhóm giả định |
| Survey: bước tốn thời gian nhất (câu 7) | 9 | Gom hợp đồng bên thứ ba 7/9, hỏi phòng ban 6/9; khớp đúng bottleneck bước 1–2 | Luật sư/DPO rà soát cũng được chọn 5/9, nên bottleneck không chỉ nằm ở khâu gom |
| Survey: ai làm (câu 5) | 9 | 4/9 tự làm nội bộ, 2/9 nội bộ gom rồi tư vấn rà soát → 6/9 vẫn phải tự gom thông tin | **3/9 thuê tư vấn làm trọn gói**. Với nhóm này, phần mềm cho DPO không có chỗ đứng |
| Survey: công cụ (câu 8) | 9 | Google Form/bảng hỏi 6/9, Excel/Word 4/9: làm thủ công là chủ yếu | 4/9 nói đã dùng "phần mềm chuyên dụng" nhưng không ghi tên, cần hỏi lại |
| Survey: cập nhật (câu 9) | 9 | 7/9 cập nhật định kỳ → việc lặp lại, khớp Nghị định 356 | 1 người chưa cập nhật lần nào, 1 người không rõ |
| Survey: mức khó (câu 10, thang 1–5) | 9 | 8/9 chấm 4, 1/9 chấm 5 | Không ai chấm 5 ngoài 1 người; khó nhưng chưa phải "cực kỳ đau" |

Kết luận cho từng giả định:

| Giả định | Kết quả |
|---|---|
| #1 Thời gian + bottleneck | **Xác nhận một phần.** Bottleneck đúng ở khâu gom thông tin, nhưng thời gian dao động lớn (1–2 tuần đến trên 1 tháng) |
| #2 Tự làm hay thuê | **Xác nhận một phần.** 2/3 vẫn tự gom thông tin, 1/3 thuê trọn gói |
| #3 Lặp lại | **Xác nhận** (7/9 cập nhật định kỳ) |
| #4 Công cụ thủ công | **Xác nhận phần lớn.** Còn mở câu hỏi "phần mềm chuyên dụng" là gì |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

- **Thu hẹp actor:** từ "DPO doanh nghiệp lớn" thành "DPO/IT ở doanh nghiệp **tự gom thông tin nội bộ**, gồm cả khi có tư vấn rà soát", chủ yếu là công ty công nghệ và fintech 50–1.000 người. Loại nhóm thuê tư vấn trọn gói khỏi phạm vi.
- **Sửa baseline:** từ "2–4 tuần" thành "**1 tuần đến trên 1 tháng**, trung vị khoảng 2 tuần"; target vẫn là dưới 1 tuần.
- **Mở rộng bottleneck:** bước gom hợp đồng bên thứ ba được nhắc nhiều nhất (7/9), ngang hoặc hơn bước hỏi phòng ban. Hai bước này gộp thành một bottleneck: "biết dữ liệu đi đâu".
- **Ghi rủi ro:** khâu luật sư/DPO rà soát cũng tốn thời gian (5/9). Nếu bản nháp kém, thời gian rà soát có thể tăng chứ không giảm.
- **Việc tiếp theo:** phỏng vấn 1–2 người đã chọn "phần mềm chuyên dụng" để biết đó là công cụ gì, giải được bước nào.

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| OneTrust: Data Mapping Automation + module PIA/DPIA | https://www.onetrust.com/news/iapp-data-mapping-automation/ | Bước 1–3: bảng hỏi gửi phòng ban, kiểm kê hệ thống và luồng dữ liệu, sơ đồ luồng; có module DPIA riêng | Nền tảng lớn nhất ngành, có tự động phát hiện và phân loại dữ liệu trên hệ thống | Chưa thấy nguồn chính thức xác nhận hỗ trợ mẫu hồ sơ theo Nghị định 356; giá doanh nghiệp, nặng với công ty 50–200 người | Pattern "bảng hỏi chuẩn gửi từng phòng ban → kiểm kê → sơ đồ luồng" đã là chuẩn; nhóm không cần phát minh lại, khoảng trống là **mẫu Việt Nam + giá vừa sức SME** |
| AesirX Compliance One: quy trình DPIA cho Luật 91/2025 | https://aesirx.io/blog/aesirx/the-dpia-triage-pipeline-from-trigger-to-dossier-without-a-separate-documentation-project | Từ phân loại khi nào cần DPIA đến hồ sơ; data mapping | Có nói rõ khung pháp lý Việt Nam (Luật 91/2025, Nghị định 356) | Nội dung marketing của nhà cung cấp, nhóm chưa kiểm được trích dẫn điều luật; chưa rõ có điền đúng mẫu hồ sơ không | Đã có đối thủ nhắm đúng thị trường Việt Nam → cần kiểm tra kỹ trước khi kết luận "chưa có phần mềm" |
| Dịch vụ tư vấn trong nước (Luật Việt An, CyStack, DPO.VN…) | https://luatvietan.vn/tu-van-danh-gia-tac-dong-xu-ly-du-lieu-ca-nhan.html · https://cystack.net/solutions/giai-phap-tuan-thu-nghi-dinh-13-cho-doanh-nghiep/pricing | Bước 4–5: điền mẫu, rà soát pháp lý; có nơi làm trọn gói | Chịu trách nhiệm pháp lý, đúng thứ 3/9 người trong survey chọn | Doanh nghiệp vẫn phải tự cung cấp thông tin nội bộ; không công bố giá; phải trả phí lại mỗi lần cập nhật | Đối thủ thật là **thuê tư vấn**, không phải phần mềm. Giải pháp nên giúp khâu gom nội bộ và xuất ra bộ hồ sơ để tư vấn rà soát nhanh hơn, không thay luật sư |



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

Bài của nhóm nằm ở ô:

Vì sao:

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | | | | |
| **Rule** | | | | |
| **Workflow** | | | | |
| **Agent** | | | | |

**Mức chọn:**

**Vì sao không chọn mức đơn giản hơn:**

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | |
| **Judgment** — con người cân nhắc, quyết định gì? | |
| **Action** — hành động cuối cùng là gì, ai làm? | |
| **Outcome** — đo kết quả bằng gì? | |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng:
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào:

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
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | Trung bình | Survey xác nhận nghẽn ở khâu gom thông tin (hợp đồng bên thứ ba 7/9, hỏi phòng ban 6/9) và việc lặp lại (7/9 cập nhật định kỳ). Nhưng 4/9 chỉ mất 1–2 tuần, 3/9 thuê tư vấn trọn gói, mẫu nhỏ và cùng vòng quen biết |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | Trung bình | Phòng ban chỉ cần xác nhận Đúng/Sai/Bổ sung. Chưa có bằng chứng DPO chấp nhận rà bản nháp do máy soạn (giả định #6) |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | Trung bình | Phần bảng hỏi + checklist làm được ngay bằng Google Form/Sheet. Phần AI đọc hợp đồng chưa có tài liệu thật để thử (giả định #5) |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | **Cao** | OneTrust và AesirX (theo bài giới thiệu của họ) có thể đã làm được việc này; nhóm chưa kiểm. Chưa biết doanh nghiệp có cho đưa hợp đồng, tài liệu nội bộ vào công cụ AI bên ngoài không |

### 8.2. Kết luận

**Quyết định:** **Not Yet**

**Lý do:** Viability ở mức Cao nhưng kiểm được nhanh trong 2 tuần. Ba rủi ro còn lại ở mức Trung bình.

**Nếu Not Yet — cần kiểm chứng gì trước:**

- Dùng thử hoặc xin demo OneTrust, AesirX: có xuất được hồ sơ theo mẫu Nghị định 356 không, giá bao nhiêu.
- Phỏng vấn 2–3 DPO/IT: công ty có cho đưa hợp đồng, tài liệu nội bộ vào công cụ AI không; rà bản nháp có nhanh hơn tự viết không.

**Ngưỡng dừng** (nếu sau … mà … thì quay về …):

- Nếu sau 2 tuần, OneTrust hoặc AesirX đã làm đúng mẫu Nghị định 356 với giá chấp nhận được → No-Go, dùng công cụ có sẵn.
- Nếu từ 2/3 DPO được hỏi không cho đưa tài liệu vào AI → bỏ bước AI, chỉ làm bảng hỏi chuẩn + checklist.
- Nếu pilot bảng hỏi chuẩn ở 1 doanh nghiệp không giảm được ít nhất 30% thời gian gom thông tin → quay về cách làm hiện tại.

---

## 9. Hạn chế và hướng tiếp theo

- 

## 10. Tài liệu tham khảo

- Nghị định 356/2025/NĐ-CP (EY tóm tắt): https://www.ey.com/vi_vn/technical/tax/tax-and-law-updates/nghi-dinh-so-356-2025-nd-cp-quy-dinh-chi-tiet-mot-so-dieu-va-bien-phap-thi-hanh-luat-bao-ve-du-lieu-ca-nhan
- Mức phạt 5% doanh thu (Báo Đầu tư): https://baodautu.vn/to-chuc-vi-pham-quy-dinh-chuyen-du-lieu-ca-nhan-xuyen-bien-gioi-bi-phat-5-doanh-thu-d314379.html
- Kiểm kê khí nhà kính, bằng chứng cho candidate #2 (Tuổi Trẻ, 25/6/2026): https://tuoitre.vn/kiem-ke-khi-nha-kinh-co-doanh-nghiep-gui-3-lan-3-bo-so-lieu-khac-nhau-100260625163229417.htm
- Kết quả survey CP4: [report/assets/cp4-survey-result.md](../assets/cp4-survey-result.md)
- Link các công cụ và dịch vụ đã có: xem bảng 3.3.
