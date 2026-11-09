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
| 3 | Hoàng Minh Quyền | Khi nhận hồ sơ mời thầu mới, tôi muốn có ngay danh sách yêu cầu năng lực, giấy tờ kèm tài liệu mình đã có, để không bị loại vì thiếu hồ sơ | Chuyên viên đấu thầu công ty CNTT, thiết bị y tế, xây lắp | Đọc hồ sơ mời thầu + tìm tài liệu năng lực trong kho: 6–8 giờ/gói | Tỉ lệ bị loại vì thiếu hồ sơ có thật sự cao không? () |
| 4 | Ngô Minh Cương | Khi bàn giao ca trực, tôi muốn nắm nhanh sự cố chưa đóng, để ca sau không sót việc | Kỹ sư on-call, Incident Manager | Viết tóm tắt bàn giao: 10–15'/ca, hay sót thread Slack | Checklist bắt buộc đã đủ chưa? PagerDuty/incident.io có sẵn tính năng chưa? () |
| 5 | Ngô Minh Cương | Khi nhận bài nộp lab của 80 sinh viên, tôi muốn phát hiện ngay bài sai cấu trúc, thiếu file, link demo hỏng, để nhắc sửa trước hạn chấm | Trợ giảng (TA), giảng viên | Mở từng folder kiểm tra tay: 60–75'/80 bài | Script Python/Bash (Rule) đã giải được 90% chưa, cần gì AI? () |
| 6 | Ngô Minh Cương | Khi bị khách khiếu nại thiếu hàng trên sàn, tôi muốn tìm nhanh video đóng gói của đơn đó, để nộp bằng chứng trong 24h | Chủ shop, trưởng ca kho TMĐT | Tua camera tìm đúng lúc đóng đơn: 8–12'/đơn | Quét mã vạch + camera (Rule) đã giải được chưa? () |
| 7 | Đoàn Trí Hùng | Khi nhận task mới, tôi muốn hiểu rõ yêu cầu nghiệp vụ và phạm vi code cần sửa, để làm đúng ngay từ đầu | Developer dự án Nhật, leader | Đối chiếu BD/DD với source code: 10–20', gây hỏi lại leader | Tài liệu không được đưa ra AI ngoài, checklist đã đủ chưa? () |
| 8 | Đoàn Trí Hùng | Khi bắt đầu học một chủ đề ML mới, tôi muốn đi được từ toán, lý thuyết đến code ví dụ, để hiểu và áp dụng nhanh | Học viên mới học ML (chương trình AI VinUni) | Nối lý thuyết với code thực tế: 60–120'/chủ đề | Người học khác có cùng khó khăn không? Khó nhất ở chủ đề nào? () |
| 9 | Đoàn Trí Hùng | Khi gặp lỗi trong ứng dụng Intra-mart, tôi muốn nhanh chóng xác định nguyên nhân và hướng xử lý, để không mất quá nhiều thời gian debug | Developer Java/Intra-mart mới làm quen framework | Đọc source framework/dự án tìm module lỗi: 30–60'/lỗi | Ngoài hệ sinh thái Intra-mart có ai gặp không? Đã đo thời gian debug thật chưa? () |
| 10 | Dư Văn Hùng | Mỗi tuần, tôi muốn biết game nào trong portfolio bị review xấu tăng đột biến và vì sao, để xử lý trước khi rating tụt | Team ASO; Product/LiveOps nhận kết quả (nhà phát hành 100+ game) | Đọc, dịch, phân loại review đa ngôn ngữ: 15–20'/game/tuần | AppFollow, AppTweak đã giải chưa? () |
| 11 | Dư Văn Hùng | Khi nhận bug report từ người chơi, tôi muốn có đủ bước tái hiện, để dev sửa mà không phải hỏi lại | QA / dev team game indie | Hỏi lại và chờ trả lời: ~10' + chờ vài giờ đến 1 ngày/bug | Form/template bắt buộc có đủ không, cần gì AI? () |
| 12 | Dư Văn Hùng | Khi người chơi hỏi trên Discord, tôi muốn trả lời nhanh các câu lặp lại, để mod không trả lời mãi một câu | Mod Discord (tình nguyện viên), người chơi mới | Chờ mod thấy tin: 30'–vài giờ khi mod offline | Discord AutoMod / bot FAQ có sẵn đã giải chưa? () |
| 13 | Trần Quang Hà | Khi tự luyện IELTS Speaking/Writing, tôi muốn nhận ra lỗi diễn đạt lặp lại, để sửa dứt điểm trước khi thi | Người ôn thi IELTS | Tự tra và rà lỗi: 2–3 giờ/lần | ChatGPT / app chấm IELTS có sẵn đã đủ chưa? Ai trả tiền? () |
| 14 | Trần Quang Hà | Khi chuẩn bị bài dạy tiếng Anh cuối tuần cho 2 em nhỏ, tôi muốn có sẵn khung từ vựng và câu hỏi game, để không mất công soạn lại mà các bé không chán | Gia sư, học sinh lớp 2–3 | Tự soạn game trên Baamboozle: 1–2 giờ/tuần | Có kho game/bộ đề mẫu sẵn chưa? Actor chỉ 1 người thì impact bao nhiêu? () |
| 15 | Trần Quang Hà | Khi nghiên cứu công nghệ backend mới (Kafka KRaft, Microservices), tôi muốn nắm ngay kiến trúc cốt lõi, để bắt tay vào code thay vì chìm trong tài liệu dài | Backend developer | Đọc tài liệu, sách: 2–3 giờ/công nghệ, có lần 3 ngày | Khác gì đọc quick-start / hỏi ChatGPT? Đo "đã nắm kiến trúc" bằng gì? () |


### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A. Hồ sơ tuân thủ / thủ tục bắt buộc | #1 Hồ sơ dữ liệu cá nhân, #2 Kiểm kê khí nhà kính / CBAM, #3 Hồ sơ dự thầu | Quy định hoặc bên mời thầu ép phải nộp đủ; sai thì bị phạt, nộp lại hoặc bị loại. Nghẽn ở bước đi gom thông tin/tài liệu từ nhiều phòng ban |
| B. Tổng hợp thông tin rải rác để chuyển giao | #4 Bàn giao ca trực, #7 Phân tích yêu cầu nghiệp vụ, #10 ReviewRadar, #11 Bug report thiếu bước tái hiện | Thông tin nằm ở nhiều nguồn (Slack, Jira, tài liệu, review, tin nhắn người chơi); người làm phải đọc, tóm tắt hoặc hỏi lại cho người sau |
| C. Dò tìm bằng chứng / lỗi trong khối dữ liệu lớn | #5 Kiểm tra bài nộp lab, #6 Video đóng gói TMĐT, #9 Debug Intra-mart | Phải dò tay trong nhiều dữ liệu (folder bài nộp, video, log + source code) để tìm đúng chỗ sai |
| D. Học / truyền đạt kiến thức lặp lại | #8 Học ML, #12 Câu hỏi lặp trên Discord, #13 Lỗi luyện IELTS, #14 Soạn bài dạy tiếng Anh, #15 Nghiên cứu công nghệ backend | Actor chủ yếu là cá nhân; pain là thời gian tự tra cứu, soạn hoặc trả lời lại cùng một kiến thức |

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
| #10 ReviewRadar (review xấu tăng đột biến) | 4 | 4 | 3 | 3 | 5 | 3 | 4 | 26 |
| #2 Kiểm kê khí nhà kính / CBAM | 4 | 4 | 4 | 4 | 3 | 4 | 2 | 25 |

**Candidate được chọn:** #1, hồ sơ đánh giá tác động xử lý dữ liệu cá nhân.

**Vì sao chọn:** Tổng điểm cao nhất. Nghĩa vụ mới có hiệu lực từ 1/1/2026, chuyển sang tiền kiểm (đạt/không đạt), phải cập nhật 6 tháng/lần, nên nhu cầu bắt buộc và lặp lại. Quy trình theo mẫu cố định nên dễ chỉ ra bottleneck (bước 1–2: gom thông tin từ phòng ban, đọc hợp đồng bên thứ ba). Chọn kèm rủi ro đã biết: pain chưa có số đo và nhóm yếu domain. Hai điểm này chuyển thành giả định ưu tiên kiểm chứng ở CP4.

**Vì sao loại các candidate còn lại:**

- #10: điểm khá nhưng công cụ thương mại đã giải phần lớn; nếu làm dễ thành "làm lại AppFollow". Ghi vào hướng tiếp theo.
- #2: pain thật nhưng không lấy được dữ liệu mẫu trong lab, và đã có nền tảng trong nước làm.
- #3: cùng cluster A với #1 nhưng chưa có bằng chứng tỉ lệ bị loại vì thiếu hồ sơ.
- #4, #7, #11: #4 trùng tính năng PagerDuty/incident.io; #7 vướng quy định không đưa tài liệu khách hàng Nhật ra AI ngoài; #11 form/template bắt buộc có thể đã đủ.

**Xử lý bất đồng (nếu có):**

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | Lập hồ sơ lần đầu mất từ 2 tuần công trở lên, và phần lớn thời gian nằm ở bước gom thông tin từ phòng ban và hợp đồng bên thứ ba | Value | 5 | 2 | **Có** |
| 2 | Doanh nghiệp tự làm, hoặc ít nhất tự gom thông tin nội bộ, chứ không giao trọn gói cho công ty tư vấn | Viability | 5 | 1 | **Có** |
| 3 | Hồ sơ phải cập nhật định kỳ, nên đây là việc lặp lại chứ không phải làm một lần rồi thôi | Value | 4 | 3 (Nghị định 356) | **Có** |
| 4 | Công cụ đang dùng chủ yếu là Excel/Word và bảng hỏi gửi phòng ban; chưa có phần mềm làm theo mẫu Việt Nam | Value | 4 | 2 | **Có** |
| 5 | Có thể lấy được nguồn đầu vào (hợp đồng, chính sách quyền riêng tư, danh sách hệ thống) để thử trong lab mà không lộ dữ liệu thật | Feasibility | 4 | 1 |  |
| 6 | DPO/luật sư chấp nhận rà soát bản nháp do máy soạn thay vì tự viết từ đầu | Usability | 4 | 1 | |

Giả định nhóm kiểm chứng trong buổi này: **#1, #2, #3, #4**, bằng micro survey.

### 3.2. Kiểm chứng

Cách đã dùng: **Survey** (Google Form, 10 câu, ẩn danh). 

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong report/assets/cp4-interview-snapshot-N.md):

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Survey: thời gian | 9 | 5/9 mất từ 2 tuần trở lên, trong đó 4/9 mất trên 1 tháng | **4/9 chỉ mất 1–2 tuần**, ít hơn mức 2–4 tuần nhóm giả định |
| Survey: bước tốn thời gian nhất | 9 | Gom hợp đồng bên thứ ba 7/9, hỏi phòng ban 6/9; khớp đúng bottleneck bước 1–2 | Luật sư/DPO rà soát cũng được chọn 5/9, nên bottleneck không chỉ nằm ở khâu gom |
| Survey: ai làm | 9 | 4/9 tự làm nội bộ, 2/9 nội bộ gom rồi tư vấn rà soát → 6/9 vẫn phải tự gom thông tin | **3/9 thuê tư vấn làm trọn gói**. Với nhóm này, phần mềm cho DPO không có chỗ đứng |
| Survey: công cụ | 9 | Google Form/bảng hỏi 6/9, Excel/Word 4/9: làm thủ công là chủ yếu | 4/9 nói đã dùng "phần mềm chuyên dụng" nhưng không ghi tên, cần hỏi lại |
| Survey: cập nhật | 9 | 7/9 cập nhật định kỳ → việc lặp lại, khớp Nghị định 356 | 1 người chưa cập nhật lần nào, 1 người không rõ |
| Survey: mức khó | 9 | 8/9 chấm 4, 1/9 chấm 5 | Không ai chấm 5 ngoài 1 người; khó nhưng chưa phải "cực kỳ đau" |

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
