# Báo cáo cá nhân — 2A202603954_NgoMinhCuong

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Ngô Minh Cương
- MSSV: 2A202603954
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: 5npc
- Link repo nhóm: https://github.com/czx04/K5-L3B-DAY02-5npc-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi đến giờ bàn giao ca trực vận hành kỹ thuật (on-call handover), tôi muốn nắm nhanh danh sách sự cố chưa đóng và trạng thái các ticket treo, để ca sau không bị sót việc và không hỏi lại từ đầu. | Kỹ sư On-call, Incident Manager, Đội trực vận hành | 2 lần/ngày (đầu mỗi ca trực), mất 25–35 phút/lần đọc lướt thread Slack và Jira; tuần trước có 1 ticket P2 bị bỏ quên 4 tiếng do ca trước quên nhắc (log trên Jira Service Desk). |
| 2 | Lặp lại | Khi kết thúc tuần làm việc, tôi muốn đối soát nhanh số giờ log task thực tế trên Jira/GitHub với bảng đăng ký làm thêm (OT) của các thành viên, để duyệt bảng công trước hạn nộp cho kế toán. | Team Lead, Kế toán nội bộ, Nhân sự dự án | Hàng tuần sáng thứ Hai; mất 45–60 phút mở 3 tab đối chiếu chéo; tháng trước có 2 lần tính lệch giờ OT dẫn đến khiếu nại (bằng chứng từ email phản ánh). |
| 3 | Tốn thời gian | Khi nhận được hồ sơ yêu cầu thầu/báo giá kỹ thuật (RFP) dài hơn 60 trang từ khách hàng doanh nghiệp, tôi muốn bóc tách nhanh các yêu cầu kỹ thuật bắt buộc và điều khoản phạt trễ hạn, để đội kỹ thuật phản hồi khả năng đáp ứng trước buổi họp thẩm định. | Solution Architect, Bidding Lead, Account Manager | 2–3 hồ sơ/tháng; mất 3–4 tiếng đọc lướt và bôi vàng thủ công từng trang; 1 lần gửi báo giá muộn 24h khiến công ty mất quyền mở thầu dự án 300 triệu. |
| 4 | Tốn thời gian | Khi tiếp nhận phản ánh khách hàng báo thiếu hàng/hỏng hàng trên sàn TMĐT, tôi muốn tìm đúng đoạn video đóng gói của mã đơn đó trong kho lưu trữ, để xác định lỗi thuộc về khâu đóng hàng hay đơn vị vận chuyển. | Trưởng ca kho, Nhân viên CSKH sàn TMĐT, Quản lý shop | Trung bình 8–12 khiếu nại/ngày; nhân viên mất 15–20 phút/đơn tua xem lại camera theo mốc thời gian in trên phiếu gửi; tổng tốn ~2.5 giờ/ngày chỉ để xác minh đơn khiếu nại. |
| 5 | Cần đọc, tổng hợp nhiều thông tin | Khi hệ thống phân tán (microservices) báo lỗi 500 hàng loạt vào giờ cao điểm, tôi muốn liên kết các log lỗi rời rạc từ các cụm server khác nhau về cùng một luồng giao dịch, để xác định đúng dịch vụ gây nghẽn đầu tiên mà không phải tải từng file log thô. | Backend Dev, SRE/DevOps, Tech Lead | 2–3 lần/tuần; mỗi lần mất 40–50 phút đào sâu 4 nguồn log (AWS CloudWatch, Datadog, log server, Sentry); thời gian gián đoạn hệ thống trung bình 45 phút/sự cố. |
| 6 | Cần đọc, tổng hợp nhiều thông tin | Khi nhà cung cấp dịch vụ hạ tầng thông báo cập nhật điều khoản bảo mật và chính sách tính phí mới, tôi muốn biết chính xác các dịch vụ công ty đang thuê bị ảnh hưởng ở mục nào, để dự toán chi phí phát sinh trước kỳ thanh toán tháng tới. | Giám đốc kỹ thuật (CTO), Kế toán quản trị, DevOps Lead | 1–2 lần/quý; tài liệu cập nhật dài 20–30 trang pháp lý/kỹ thuật; CTO mất trọn 1 buổi chiều (~3 tiếng) đọc và tính nhẩm; tháng trước bị bất ngờ vì hóa đơn cloud tăng thêm $450 do thay đổi cách tính bandwidth. |
| 7 | Cần đọc, tổng hợp nhiều thông tin | Khi làm nghiên cứu khoa học hoặc chuẩn bị tài liệu kỹ thuật (literature review), tôi muốn trích xuất và đối chiếu bảng thông số benchmark (dataset, metric, baseline SOTA) từ 15 bài báo liên quan, để tìm ra khoảng trống nghiên cứu cho đề tài. | Sinh viên nghiên cứu (Lab AI), Nghiên cứu viên R&D | Mỗi đợt làm đồ án/paper mất 2–3 tuần; trung bình 60–90 phút cho mỗi bài báo để vẽ ma trận so sánh; hay bị sót các bài có cấu trúc bảng biểu không chuẩn. |
| 8 | Pain từ người khác | Khi trợ giảng (TA) nhận bài nộp bài tập lớn/lab từ 80 sinh viên, TA muốn phát hiện ngay các bài nộp sai cấu trúc thư mục, thiếu file bắt buộc hoặc sai quy cách đặt tên, để nhắc sinh viên sửa ngay trước khi chốt hạn chấm điểm. | Trợ giảng (TA), Giảng viên, Sinh viên lớp lab | 1 đợt/tuần; TA mất 2–3 tiếng giải nén từng file kiểm tra thủ công; trung bình 15–20% sinh viên nộp sai định dạng dẫn đến tranh cãi khi bị trừ điểm oan (tin nhắn khiếu nại trong kênh Discord/Zalo). |
| 9 | Pain từ người khác | Khi đội kiểm thử (Tester) gửi báo cáo lỗi (Bug Ticket) nhưng thiếu các bước tái hiện chi tiết và thông tin phiên bản thiết bị, lập trình viên (Developer) muốn có đủ ngữ cảnh lỗi ngay lần đầu mở ticket, để không phải ping hỏi qua lại làm đứt quãng mạch làm việc. | Lập trình viên, Tester, Project Manager | 5–7 bug/sprint bị gắn nhãn "Cannot Reproduce"; Dev mất 15–20 phút nhắn tin hỏi lại hoặc gọi video để Tester thao tác lại; làm trễ tiến độ release 1–2 ngày (log trên Jira board). |
| 10 | Lặp lại | Khi có nhân sự thực tập sinh/kỹ sư mới gia nhập dự án (onboarding), người hướng dẫn (Mentor) muốn cung cấp một checklist cài đặt môi trường code chuẩn theo đúng phiên bản thư viện hiện hành của dự án, để nhân sự mới có thể chạy được code mẫu trong ngày đầu tiên mà không làm phiền đồng nghiệp xung quanh. | Mentor kỹ thuật, Nhân sự mới (Intern/Junior) | Diễn ra mỗi khi có đợt tuyển intern (khoảng 3–4 lần/năm); mỗi nhân sự mới mất 1.5–2 ngày vật lộn với lỗi lệch phiên bản phần mềm; Mentor tốn 3–4 tiếng debug hộ (ghi nhận qua ghi chú phỏng vấn nội bộ). |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- **Ý AI gợi ý mà tôi giữ lại:** Ban đầu tôi tự scan được các vấn đề kỹ thuật và nghiên cứu học tập (#1, #2, #5, #7, #8, #9, #10). Sau đó tôi dùng AI để mở rộng góc nhìn vận hành thực tế và giữ lại ý #4 (tìm video đóng hàng TMĐT để xử lý khiếu nại) và #6 (đối chiếu điều khoản thay đổi cách tính phí dịch vụ hạ tầng cloud) vì hai vấn đề này có quy trình cụ thể, đo lường được bằng số phút hao phí thực tế và có tác động tài chính rõ ràng.
- **Ý AI gợi ý mà tôi loại bỏ:** Tôi đã loại bỏ gợi ý của AI về *"Trợ lý AI quản lý toàn bộ công việc cá nhân"* và *"Hệ thống tự động phát hiện gian lận thi cử"*. Lý do: Ý thứ nhất là solution trá hình, mơ hồ và không có quy trình cụ thể; ý thứ hai có phạm vi quá rộng, đụng chạm chính sách bảo mật/quyền riêng tư phức tạp, không khả thi để giải quyết trong một buổi lab Discovery.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Bàn giao ca trực sự cố kỹ thuật (Ý #1) | Quy trình lặp lại đều đặn mỗi ngày, actor rõ ràng, bottleneck đo được bằng phút rất cụ thể (40 phút/ca), dễ so sánh giữa No AI/Rule/Workflow/Agent. | Liệu kỹ sư ca sau có tin tưởng bản tóm tắt tự động không hay vẫn vào đọc lại từng thread chat? |
| 2 | TA kiểm tra định dạng và tính hợp lệ bài nộp lab (Ý #8) | Nỗi đau thực tế trong trường học, dễ kiểm chứng ngay với trợ giảng/bạn học, tác động trực tiếp tới điểm số sinh viên. | Có cần AI không hay chỉ cần script Python/Bash đơn giản (Rule-based) đã giải quyết được 90%? |
| 3 | Đối soát video đóng gói xử lý khiếu nại TMĐT (Ý #4) | Tác động kinh tế rõ ràng (mất tiền phạt và tiền hàng), tần suất xảy ra hàng ngày ở các shop bán lẻ. | Giải pháp quét mã vạch thủ công (No AI/Rule) có thể đã đủ tốt mà không cần AI can thiệp? |

### Problem Card #1 — Bàn giao ca trực sự cố kỹ thuật (On-call Handover)

| Trường | Nội dung |
|---|---|
| Job Story | Khi đến giờ bàn giao ca trực vận hành kỹ thuật (on-call handover), tôi muốn nắm nhanh danh sách sự cố chưa đóng và trạng thái các ticket treo, để ca sau không bị sót việc và không hỏi lại từ đầu. |
| Actor | Kỹ sư trực ca vận hành (On-call Engineer), Incident Manager |
| Thời điểm / bối cảnh | 8h00 sáng và 20h00 tối hàng ngày tại thời điểm chuyển giao giữa 2 ca trực |
| Quy trình hiện tại (3–7 bước) | 1. Đọc lại kênh Slack sự cố trong ca (10') · 2. Lọc Jira Service Desk các ticket chưa đóng (10') · 3. Kiểm tra dashboard Grafana xem còn cảnh báo treo không (5') · 4. Tự viết tin nhắn tóm tắt bàn giao vào kênh Slack chung (10') · 5. Gọi sync nhanh 5 phút giải thích cho ca sau (5') |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4 — Viết tóm tắt bàn giao: mất 10–15 phút, người trực mệt mỏi sau ca trực dài nên hay viết sơ sài hoặc sót các thảo luận ngầm trong thread Slack |
| Impact (nếu không giải thì sao) | Mất 40 phút/ca (80 phút/ngày cho cả 2 ca); tuần trước có 1 sự cố P2 bị bỏ quên suốt 4 tiếng do ca trước quên bàn giao, vi phạm cam kết SLA với khách hàng |
| Success metric (baseline → target) | Tổng thời gian giao ca từ 40 phút xuống dưới 10 phút/ca; tỷ lệ sự cố bị bỏ sót giữa 2 ca giảm về 0% (đo qua log Jira 4 tuần) |
| Phương án không dùng AI | Dùng template cố định trong Google Docs + checklist 5 mục bắt buộc phải tick trước khi out ca |
| Giả thuyết về AI (nếu có) | AI gom dữ liệu ticket Jira + tóm tắt các thread thảo luận trong ca để soạn sẵn bản nháp bàn giao; kỹ sư chỉ cần rà soát lại |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 40 phút / ca trực

[1 Đọc kênh Slack: 10'] → [2 Lọc Jira ticket: 10'] → [3 Kiểm tra Grafana: 5']
→ [4 Viết tóm tắt bàn giao: 10'] ← BOTTLENECK (dễ sót sự cố)
→ [5 Gọi sync giải thích: 5']
```

### Problem Card #2 — Kiểm tra định dạng và tính hợp lệ bài nộp lab (Lab Submission Integrity)

| Trường | Nội dung |
|---|---|
| Job Story | Khi trợ giảng (TA) nhận bài nộp bài tập lớn/lab từ 80 sinh viên, TA muốn phát hiện ngay các bài nộp sai cấu trúc thư mục, thiếu file bắt buộc hoặc link demo không mở được, để nhắc sinh viên sửa ngay trước khi chốt hạn chấm điểm. |
| Actor | Trợ giảng (TA), Giảng viên bộ môn, Sinh viên lớp lab |
| Thời điểm / bối cảnh | Sáng thứ Hai sau khi hệ thống đóng hạn nộp bài tập lúc 23h59 Chủ nhật |
| Quy trình hiện tại (3–7 bước) | 1. Tải toàn bộ file ZIP bài nộp từ LMS về máy (10') · 2. Giải nén từng folder sinh viên (15') · 3. Mở từng bài kiểm tra: đúng tên file, có file PDF báo cáo, có link video demo không và link có mở được quyền công khai không (60') · 4. Ghi danh sách sinh viên vi phạm vào Excel (20') · 5. Gửi thông báo cảnh báo lên Discord/Zalo lớp (15') |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 — Mở từng folder kiểm tra thủ công: mất 60–75 phút cho 80 sinh viên; thao tác lặp lại dễ mỏi mắt và bỏ sót link video bị khoá quyền riêng tư |
| Impact (nếu không giải thì sao) | Mất 120 phút/tuần của TA; 15–20% sinh viên bị trừ điểm oan hoặc nhận điểm 0 vì lỗi hình thức ngớ ngẩn (quên share quyền link Drive); sinh viên khiếu nại kéo dài làm chậm tiến độ công bố điểm |
| Success metric (baseline → target) | Thời gian kiểm tra giảm từ 120 phút xuống dưới 15 phút; 100% sinh viên nộp sai định dạng được cảnh báo tự động trong vòng 2 giờ sau khi nộp bài |
| Phương án không dùng AI | Viết script Python quét cấu trúc folder, kiểm tra định dạng đuôi file và ping thử link video Drive xem có public không (Rule-based 100%) |
| Giả thuyết về AI (nếu có) | Rule kiểm tra cấu trúc file và link; AI chỉ đọc lướt trang đầu file PDF để kiểm tra xem có đủ thông tin MSSV, họ tên và đề bài theo mẫu không |
| Cảm nhận nhanh | Rule (kết hợp Workflow rất nhẹ) |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 120 phút / đợt nộp bài

[1 Tải ZIP từ LMS: 10'] → [2 Giải nén 80 folder: 15']
→ [3 Mở từng bài kiểm tra file + link Drive: 60'] ← BOTTLENECK
→ [4 Ghi danh sách lỗi vào Excel: 20'] → [5 Thông báo lên Discord/Zalo: 15']
```

### Problem Card #3 — Đối soát video đóng gói xử lý khiếu nại sàn TMĐT (E-commerce Packing Verification)

| Trường | Nội dung |
|---|---|
| Job Story | Khi tiếp nhận phản ánh khách hàng báo thiếu hàng/hỏng hàng trên sàn TMĐT, tôi muốn tìm đúng đoạn video đóng gói của mã đơn đó trong kho lưu trữ, để xác định lỗi thuộc về khâu đóng hàng hay đơn vị vận chuyển. |
| Actor | Trưởng ca kho, Nhân viên chăm sóc khách hàng (CSKH), Chủ shop TMĐT |
| Thời điểm / bối cảnh | Hàng ngày khi sàn TMĐT gửi thông báo yêu cầu cung cấp bằng chứng cho đơn khiếu nại |
| Quy trình hiện tại (3–7 bước) | 1. Đọc mã vận đơn và lý do khiếu nại trên portal sàn (2') · 2. Tra cứu thời gian in phiếu đóng gói trên phần mềm quản lý kho (3') · 3. Mở phần mềm camera đầu ghi kho (2') · 4. Tua xem lại video tại bàn đóng gói quanh khung giờ đó để tìm đúng lúc nhân viên đóng đơn hàng này (10') · 5. Cắt đoạn clip 30 giây rõ nét (3') · 6. Tải clip lên portal sàn TMĐT để khiếu nại (2') |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4 — Tua video camera: mất 8–12 phút/đơn vì phải tua đi tua lại ở tốc độ 4x/8x để nhận diện đúng tờ phiếu gửi và sản phẩm được nhét vào hộp |
| Impact (nếu không giải thì sao) | Mất 22 phút/đơn $\times$ 8–12 đơn = 2.5–3.5 tiếng/ngày; nếu quá hạn 24h không cung cấp được video, sàn tự động xử thua và trừ tiền shop (thiệt hại 2–4 triệu/tháng tiền oan) |
| Success metric (baseline → target) | Thời gian tìm và xuất video giảm từ 22 phút xuống dưới 3 phút/đơn; tỷ lệ khiếu nại được cung cấp bằng chứng đúng hạn đạt 100% |
| Phương án không dùng AI | Nhân viên kho quét mã vạch đơn hàng trước máy quét kết nối webcam tại bàn đóng gói để phần mềm tự cắt sẵn clip theo mã đơn (Rule / Hardware Sync) |
| Giả thuyết về AI (nếu có) | Dùng computer vision nhận diện mã vận đơn trên tay nhân viên từ camera trên cao và tự động đánh dấu (tag) mốc thời gian trong video lưu trữ |
| Cảm nhận nhanh | Rule hoặc Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 22 phút / đơn khiếu nại (Tổng ~2.5 - 3.5 tiếng/ngày)

[1 Đọc mã đơn trên sàn: 2'] → [2 Tra cứu giờ in phiếu: 3'] → [3 Mở app camera: 2']
→ [4 Tua camera tìm lúc đóng gói: 10'] ← BOTTLENECK (tua mỏi mắt)
→ [5 Cắt clip 30s: 3'] → [6 Tải video lên sàn: 2']
```

### Card muốn pitch nhất

- Card số: **Problem Card #1 — Bàn giao ca trực sự cố kỹ thuật (On-call Handover)**
- Vì sao: Bài toán có quy trình lặp lại hàng ngày, actor rõ ràng, số liệu thời gian đo lường bằng phút rất thuyết phục (40 phút/ca). Đây là bài toán mẫu mực để nhóm mang vào thảo luận so sánh giữa No AI (template), Rule (script lấy ticket) và Workflow (AI tóm tắt ngữ cảnh sự cố).
- Câu hỏi muốn nhóm phản biện: *"Nếu công ty áp dụng một template checklist bắt buộc (No AI/Rule) cho người rời ca, liệu có đủ để giải quyết việc quên sự cố không, hay nhất thiết phải cần AI tóm tắt các thread chat phân tán trong Slack?"*

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Baseline 40 phút/ca chỉ phản ánh những ngày nhiều sự cố, vào ngày hệ thống chạy êm đềm thì thời gian giao ca có thể ngắn hơn nhiều. | Đồng ý | Đã làm rõ trong phần Impact: con số 40 phút là mức trung bình tính toán trên log 14 ngày làm việc (gồm cả ngày cao điểm và ngày êm đềm), có dẫn chứng ticket P2 bị bỏ quên tuần trước. |
| Đề xuất ban đầu định để AI tự động gửi tin bàn giao cho ca sau mà không cần người duyệt (Agentic). | Không đồng ý | Giữ vững ranh giới an toàn (Boundary): Bắt buộc kỹ sư rời ca phải đọc bản nháp, xác nhận độ chuẩn xác của trạng thái ticket rồi mới bấm gửi, không cho AI tự ý gửi để tránh báo sai ngữ cảnh kỹ thuật. |
| Success metric ban đầu chỉ đo thời gian (giảm từ 40' xuống 10') mà chưa đo lường chất lượng bàn giao (bàn giao nhanh nhưng thiếu sót thì sao?). | Đồng ý | Đã bổ sung thêm chỉ số đo lường chất lượng: "Tỷ lệ sự cố bị bỏ sót giữa 2 ca trực giảm về 0% trong 4 tuần pilot". |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | |
| Nhận phản biện | Câu hỏi tôi nhận được: | Tôi đã sửa gì: |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | | | | |
| CP2 Problem Card | | | | |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
