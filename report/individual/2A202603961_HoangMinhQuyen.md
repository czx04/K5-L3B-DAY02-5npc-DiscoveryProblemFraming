# Báo cáo cá nhân — 2A202603961_HoangMinhQuyen

> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).

## 1. Thông tin học viên

- Họ tên: Hoàng Minh Quyền
- MSSV: 2A202603961
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: 5npc
- Link repo nhóm: https://github.com/czx04/K5-L3B-DAY02-5npc-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

Tôi scan 5 problem, đóng vai phòng nghiên cứu sản phẩm của một công ty phần mềm B2B (hư cấu), tìm bài toán mà doanh nghiệp sẵn sàng trả tiền. Số liệu ghi "Giả định R&D" là chưa đo, sẽ kiểm ở CP4.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Cần đọc, tổng hợp nhiều thông tin | Khi công ty phải lập hồ sơ đánh giá tác động xử lý dữ liệu cá nhân theo luật mới, tôi muốn biết mọi phòng ban đang thu thập dữ liệu gì, lưu ở đâu, chia sẻ cho ai, để nộp hồ sơ đạt ngay lần đầu | Pháp chế/DPO, CNTT, các phòng ban có dữ liệu khách hàng | Luật 91/2025/QH15 và Nghị định 356/2025 có hiệu lực từ 1/1/2026; hồ sơ được Bộ Công an đánh giá đạt/không đạt. Giả định R&D: 2–4 tuần công để gom thông tin từ các phòng ban |
| 2 | Tốn thời gian | Khi tới kỳ kiểm kê khí nhà kính, tôi muốn có đủ số liệu điện, nhiên liệu, nguyên liệu đã dùng trong năm, để lập báo cáo đúng và không phải nộp lại | Cán bộ môi trường/ESG ở nhà máy, kế toán, kho | Tuổi Trẻ (25/6/2026) dẫn lời Cục Biến đổi khí hậu: "Có doanh nghiệp gửi ba lần, ba bộ số liệu khác nhau". Giả định R&D: 3–6 tuần công/kỳ để gom số liệu |
| 3 | Lặp lại | Khi nhận một hồ sơ mời thầu mới, tôi muốn có ngay danh sách mọi yêu cầu về năng lực, kinh nghiệm và giấy tờ cùng tài liệu mình đã có để đáp ứng, để không bị loại vì thiếu hồ sơ | Chuyên viên đấu thầu, trưởng phòng kinh doanh | Giả định R&D: 5–15 gói thầu/tháng ở công ty CNTT/thiết bị; 1–2 ngày công/gói để đọc và lập checklist |
| 4 | Pain từ người khác | Khi bảo hiểm xã hội từ chối thanh toán một phần hồ sơ bảo hiểm y tế, phòng tài chính bệnh viện muốn biết trước lỗi nằm ở chỉ định nào, để sửa trước khi gửi | Phòng tài chính – kế hoạch bệnh viện, bác sĩ | Một nghiên cứu ở phòng khám Đắk Lắk (2024): chỉ định kỹ thuật sai quy định chiếm 92,7% khoản bị từ chối (cần tự mở nguồn) |
| 5 | Lặp lại | Khi chuẩn bị bộ chứng từ xuất khẩu thanh toán bằng L/C, tôi muốn biết hóa đơn, vận đơn, C/O và packing list đã khớp nhau và khớp L/C chưa, để ngân hàng không báo sai lệch | Nhân viên xuất nhập khẩu, kế toán | Giả định R&D: mỗi lần sai lệch bị tính phí và nhận tiền chậm vài ngày |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- Giữ lại #1 và #2 vì đến từ quy định mới có hiệu lực 2026: nhu cầu bắt buộc, công cụ chưa theo kịp.
- #4 giữ trong scan nhưng không chọn vào top 3: đã có phần mềm rà soát hồ sơ bảo hiểm y tế (ví dụ MDinsight Adaptor).
- Bỏ ý "trợ lý vận hành toàn doanh nghiệp" vì quá rộng, không có actor và quy trình cụ thể.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Hồ sơ đánh giá tác động xử lý dữ liệu cá nhân (#1) | Quy định mới bắt buộc, phạt cao, hồ sơ phải cập nhật định kỳ; mới thấy dịch vụ tư vấn, chưa thấy phần mềm làm theo mẫu Việt Nam | Doanh nghiệp tự làm hay thuê trọn gói công ty tư vấn? |
| 2 | Gom số liệu kiểm kê khí nhà kính (#2) | Có bằng chứng số liệu không nhất quán; dữ liệu điện, nhiên liệu đã nằm sẵn trên hóa đơn điện tử | FPT IS VertZéro hoặc nền tảng khác đã lấy dữ liệu từ hóa đơn chưa? |
| 3 | Hồ sơ dự thầu không bị loại vì thiếu giấy tờ (#3) | Mất một gói thầu là mất tiền rõ; chưa thấy công cụ giúp phía nhà thầu | Tỉ lệ bị loại vì thiếu hồ sơ/lỗi hình thức có thật sự cao không? |

### Problem Card #1 — Hồ sơ đánh giá tác động xử lý dữ liệu cá nhân

| Trường | Nội dung |
|---|---|
| Job Story | Khi công ty phải lập hồ sơ đánh giá tác động xử lý dữ liệu cá nhân theo luật mới, tôi muốn biết mọi phòng ban đang thu thập dữ liệu gì, lưu ở đâu, chia sẻ cho ai, để nộp hồ sơ đạt ngay lần đầu |
| Actor | Chuyên viên pháp chế hoặc nhân sự bảo vệ dữ liệu (DPO) ở doanh nghiệp không được miễn trừ: xử lý dữ liệu nhạy cảm hoặc có từ 100.000 chủ thể dữ liệu trở lên (bán lẻ, bảo hiểm, fintech, bệnh viện tư) |
| Thời điểm / bối cảnh | Lần đầu lập hồ sơ sau khi luật có hiệu lực 1/1/2026; sau đó cập nhật định kỳ 6 tháng khi có mục đích xử lý mới hoặc đổi bên xử lý |
| Quy trình hiện tại (3–7 bước) | 1. Gửi bảng hỏi/phỏng vấn từng phòng ban · 2. Gom hợp đồng với bên xử lý, bên thứ ba · 3. Vẽ sơ đồ luồng dữ liệu · 4. Điền báo cáo theo Mẫu số 10 (và Mẫu số 09 nếu chuyển dữ liệu ra nước ngoài) · 5. Luật sư/DPO rà soát · 6. Gửi cơ quan chuyên trách bảo vệ dữ liệu cá nhân thuộc Bộ Công an · 7. Nếu không đạt: bổ sung trong 30 ngày |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 1–2: gom và đối chiếu thông tin dữ liệu từ nhiều phòng ban, khoảng 7–11 ngày công (Giả định R&D) |
| Impact (nếu không giải thì sao) | 2–4 tuần công cho lần đầu; hồ sơ không đạt phải bổ sung trong 30 ngày, nếu không có thể bị xử phạt; phạt tối đa tới 5% doanh thu với vi phạm chuyển dữ liệu xuyên biên giới |
| Success metric (baseline → target) | Thời gian lập hồ sơ lần đầu từ 2–4 tuần xuống dưới 1 tuần; hồ sơ đạt ngay lần nộp đầu |
| Phương án không dùng AI | Bộ biểu mẫu + checklist theo Mẫu số 10, bảng hỏi chuẩn cho từng phòng ban; hoặc thuê công ty tư vấn trọn gói |
| Giả thuyết về AI (nếu có) | AI đọc hợp đồng, chính sách quyền riêng tư, danh sách hệ thống để soạn nháp danh mục dữ liệu và sơ đồ luồng; DPO/luật sư duyệt trước khi nộp |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — lần đầu khoảng 2–4 tuần công (Giả định R&D)

[1 Bảng hỏi/phỏng vấn từng phòng ban: 5–8 ngày] ← BOTTLENECK
→ [2 Gom hợp đồng bên xử lý, bên thứ ba: 2–3 ngày] ← BOTTLENECK
→ [3 Vẽ sơ đồ luồng dữ liệu: 2 ngày]
→ [4 Điền Mẫu số 10: 2 ngày] → [5 Luật sư/DPO rà soát: 2 ngày]
→ [6 Gửi Bộ Công an: kết quả trong 15 ngày] → [7 Không đạt → bổ sung trong 30 ngày]
```

### Problem Card #2 — Gom số liệu kiểm kê khí nhà kính

| Trường | Nội dung |
|---|---|
| Job Story | Khi tới kỳ kiểm kê khí nhà kính, tôi muốn có đủ số liệu điện, nhiên liệu, nguyên liệu đã dùng trong năm, để lập báo cáo đúng và không phải nộp lại |
| Actor | Cán bộ môi trường/ESG ở nhà máy thuộc danh mục bắt buộc kiểm kê, hoặc doanh nghiệp xuất khẩu thép, xi măng sang EU chịu CBAM |
| Thời điểm / bối cảnh | Kỳ kiểm kê định kỳ; báo cáo phát thải cho khách hàng EU theo CBAM (thu phí từ 1/1/2026) |
| Quy trình hiện tại (3–7 bước) | 1. Xin số liệu điện, dầu, than, khí từ kế toán, kho, kỹ thuật · 2. Gom hóa đơn/phiếu xuất kho, nhập tay vào Excel · 3. Quy đổi đơn vị · 4. Nhân hệ số phát thải · 5. Lập báo cáo theo mẫu · 6. Giải trình khi số liệu lệch |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 1–2: gom dữ liệu hoạt động từ nhiều phòng ban, mỗi nơi một con số, khoảng 2–4 tuần (Giả định R&D) |
| Impact (nếu không giải thì sao) | Báo cáo bị yêu cầu làm lại (có doanh nghiệp gửi 3 lần, 3 bộ số liệu); với CBAM, thiếu số liệu thật thì phải dùng giá trị mặc định của EU |
| Success metric (baseline → target) | Thời gian gom số liệu từ 3–6 tuần xuống dưới 1 tuần; báo cáo không phải nộp lại |
| Phương án không dùng AI | Rule: lọc hóa đơn điện, xăng dầu theo mã số thuế người bán và mã hàng; template Excel chuẩn |
| Giả thuyết về AI (nếu có) | AI phân loại các dòng hàng ghi tên lộn xộn trên hóa đơn đầu vào vào đúng nhóm nguồn phát thải; người phụ trách duyệt |
| Cảm nhận nhanh | Rule + Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — khoảng 3–6 tuần công/kỳ (Giả định R&D)

[1 Xin số liệu từ kế toán, kho, kỹ thuật: 1–2 tuần] ← BOTTLENECK
→ [2 Gom hóa đơn, nhập tay Excel: 1–2 tuần] ← BOTTLENECK
→ [3 Quy đổi đơn vị: 2 ngày] → [4 Nhân hệ số phát thải: 1 ngày]
→ [5 Lập báo cáo: 3 ngày] → [6 Giải trình số liệu lệch: vài ngày]
```

### Problem Card #3 — Hồ sơ dự thầu không bị loại vì thiếu giấy tờ

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhận một hồ sơ mời thầu mới, tôi muốn có ngay danh sách mọi yêu cầu về năng lực, kinh nghiệm và giấy tờ cùng tài liệu mình đã có để đáp ứng, để không bị loại vì thiếu hồ sơ |
| Actor | Chuyên viên đấu thầu ở công ty CNTT, thiết bị y tế, xây lắp dự 5–15 gói thầu qua mạng/tháng |
| Thời điểm / bối cảnh | Từ lúc hồ sơ mời thầu được đăng trên Hệ thống mạng đấu thầu quốc gia đến hạn đóng thầu, thường 1–3 tuần |
| Quy trình hiện tại (3–7 bước) | 1. Tải hồ sơ mời thầu · 2. Đọc tiêu chuẩn đánh giá năng lực, kinh nghiệm · 3. Lập checklist yêu cầu · 4. Tìm hợp đồng tương tự, biên bản nghiệm thu, báo cáo tài chính trong kho tài liệu · 5. Soạn hồ sơ dự thầu · 6. Rà lần cuối và nộp |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2 và 4: đọc hồ sơ mời thầu và tìm tài liệu năng lực tương ứng, khoảng 6–8 giờ/gói (Giả định R&D) |
| Impact (nếu không giải thì sao) | Thiếu một giấy tờ có thể bị đánh giá không đạt, mất cả gói thầu; chuyên viên chỉ kịp dự ít gói hơn |
| Success metric (baseline → target) | Thời gian từ nhận hồ sơ mời thầu đến có checklist đầy đủ từ 1–2 ngày xuống dưới 2 giờ; số gói bị loại vì thiếu hồ sơ = 0 |
| Phương án không dùng AI | Checklist mẫu theo loại gói thầu + kho hồ sơ năng lực được đặt tên chuẩn |
| Giả thuyết về AI (nếu có) | AI trích yêu cầu từ hồ sơ mời thầu và ghép mỗi yêu cầu với tài liệu năng lực trong kho; chuyên viên duyệt |
| Cảm nhận nhanh | Rule + Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — khoảng 1–2 ngày công/gói (Giả định R&D)

[1 Tải hồ sơ mời thầu: 15'] → [2 Đọc tiêu chuẩn đánh giá: 3–4 giờ] ← BOTTLENECK
→ [3 Lập checklist: 1–2 giờ] → [4 Tìm tài liệu năng lực trong kho: 3–4 giờ] ← BOTTLENECK
→ [5 Soạn hồ sơ dự thầu: 1–3 ngày] → [6 Rà lần cuối + nộp: 1 giờ]
```

### Card muốn pitch nhất

- Card số: 1
- Vì sao: Quy định mới có hiệu lực 1/1/2026 và chuyển sang tiền kiểm (Bộ Công an đánh giá đạt/không đạt), mức phạt cao, hồ sơ phải cập nhật 6 tháng/lần; research mới thấy dịch vụ tư vấn, chưa thấy phần mềm làm theo mẫu Việt Nam.
- Câu hỏi muốn nhóm phản biện: "Doanh nghiệp sẽ tự làm hồ sơ bằng công cụ, hay thuê trọn gói công ty tư vấn? Nếu thuê tư vấn thì bài toán có còn đáng làm không?"

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Lập hồ sơ là việc theo đợt, không lặp hằng tuần | Đồng ý một phần | Nghị định 356 yêu cầu cập nhật 6 tháng/lần; thêm vào "Thời điểm / bối cảnh" |
| AI có thể diễn giải luật sai | Đồng ý | Giả thuyết AI chỉ soạn nháp danh mục dữ liệu; DPO/luật sư duyệt trước khi nộp |
| Gợi ý cho AI tự nộp hồ sơ lên Bộ Công an | Không đồng ý | Nộp hồ sơ là hành động pháp lý của doanh nghiệp; giữ người có thẩm quyền ký và nộp |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả |
|---|---|---|
| Pitch Problem Card | Pitch 3 card: hồ sơ đánh giá tác động dữ liệu cá nhân, kiểm kê khí nhà kính, hồ sơ dự thầu | Card hồ sơ dữ liệu cá nhân được chọn (28 điểm); card khí nhà kính vào shortlist |
| Phản biện bài bạn khác | Hỏi …: "…" | … |
| Nhận phản biện | Bị hỏi: "Doanh nghiệp tự làm hay thuê trọn gói tư vấn?" | Đưa thành giả định #2 ở CP4; survey cho thấy 3/9 thuê trọn gói nên nhóm thu hẹp actor về doanh nghiệp tự gom thông tin nội bộ |
| Kiểm chứng / research | Đọc toàn văn Nghị định 356 để kiểm thông tin nhóm đang dùng | Phát hiện hồ sơ đánh giá tác động dùng Mẫu số 10, không phải Mẫu số 09 như nhóm ghi |
| Quyết định | Soạn mục 8, 9, 10 của báo cáo nhóm | Nhóm có quyết định Not Yet kèm 3 ngưỡng dừng |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Dùng Claude soạn nháp bảng scan và search xem mỗi problem đã có ai làm chưa | Phát hiện cả 5 problem vòng đầu (đối soát hóa đơn, đối chiếu chuyển khoản, phân loại bảo hành, so sánh báo giá, rà hợp đồng) đều đã có công cụ làm, ví dụ MISA AVA đã đối chiếu hóa đơn với PO | Vòng đầu chọn problem theo "dễ thấy ROI" mà chưa kiểm đối thủ; nhiều số liệu là ước lượng | Thay toàn bộ 5 problem bằng các bài toán từ quy định mới 2026; gắn nhãn "Giả định R&D" cho số chưa đo |
| CP2 Problem Card | Dùng Claude soạn nháp 3 card và đóng vai PM hoài nghi phản biện card #1 | Chỉ ra rủi ro "việc theo đợt" và rủi ro diễn giải luật sai | Gợi ý cho AI tự nộp hồ sơ lên Bộ Công an; đoán sai Mẫu số 09 là mẫu hồ sơ đánh giá tác động | Giữ người có thẩm quyền ký và nộp; đọc văn bản gốc và sửa thành Mẫu số 10 |
| CP4 Research | Dùng Claude tìm văn bản Nghị định 356 và kiểm các link trong báo cáo có mở được không | Tìm được toàn văn để đối chiếu, không chỉ dựa vào bản tóm tắt của EY | Nhiều kết quả tìm kiếm là bài marketing của nhà cung cấp | Chỉ giữ link đã tự mở; ghi rõ AesirX, OneTrust là "theo bài giới thiệu của họ, chưa kiểm" |
| CP5 Quy trình | Dùng Claude vẽ workflow hiện tại và tương lai cho card #1 | Tách rõ bước Rule, bước AI, bước con người kiểm tra và phương án quay về | Phạm vi ban đầu quá rộng: nhiều ngành, hai loại hồ sơ, cả 7 bước | Thu hẹp còn bước gom thông tin dữ liệu khách hàng, người dùng là nhân viên không chuyên luật |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | Dùng Claude soạn nháp mục 8 (4 rủi ro, quyết định, ngưỡng dừng) | Đưa đúng số liệu survey vào từng rủi ro | Bản đầu quá dài và có nhận định pháp lý không có nguồn ("đưa hợp đồng vào AI là chuyển dữ liệu ra nước ngoài") | Rút gọn theo bài mẫu; đổi nhận định đó thành câu hỏi mở cần kiểm chứng |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
- Học thêm về góc nhìn và cách đặt vấn đề của các bạn khác nhau phản biện bảo vệ quan điểm và cùng nhau tìm ra tiếng nói chung cho bài lab
**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
- Có. Nhóm từng quá tập trung vào cách giải quyết bài toán khi chưa thật sự hiểu rõ vấn đề và chưa biết được actor chính trong trường hợp đó thật sự cần gì và muốn gì cũng như bài toán cụ thể ra sao. Nhóm nhận ra khi các giải pháp cso vẻ tiến triển gần như "đi vào bế tắc" vừa không thực sự giải quyết được bài toán vừa làm mất thời gian và chi phí vận hành. Sau đó cùng nhau ngồi lại đặt ra các vấn đề chính và tìm nguồn gốc vấn đề sau đó đưa ra các giải pháp triệt để.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
- Thật sự là có nhưng không phải đổi ý mà chỉ lưỡng lự khi chưa đủ kiến thức bảo vệ quan điểm, cụ thể là trong best card được tôi chọn phần topic nó khá vĩ mô khi liên quan đến nhiều ngành như luật pháp, an ninh và hộ kinh doanh, khi nhận được nhiều câu hỏi phản biện về chủ đề và cách làm tôi đã phải dành thêm thời gian nghiên cứu và cùng các bạn trong nhóm tìm hiểu kĩ hơn trước khi chọn lựa và tiếp tục đi theo

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
- Có. Mặc dù số lượng survey không quá nhiều nhưng đủ để cho thấy một thực trạng rằng bộ luật mới bên cạnh các doanh nghiệp đã hiểu và vận hành thành công hoặc ít nhất là có biết đến và bắt đầu vận hành thì còn nhiều doanh nghiệp nhỏ chưa bắt đầu hoặc thậm chí còn chưa biết về điều luật này

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

- Domain pháp lý còn lạ, cả nhóm chưa ai làm pháp chế (domain chỉ được chấm 2/5)
- Ví dụ cụ thể: tưởng hồ sơ đánh giá tác động dùng Mẫu 09, đến khi đọc văn bản gốc mới biết là Mẫu 10
- Cách xử lý: đọc Điều 18, 19, 20 của Nghị định 356 rồi sửa lại

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

- Đổi: đọc văn bản gốc ngay từ đầu, không tin bản tóm tắt của EY.
- Phản biện mạnh hơn: chất lượng survey.
    - Nhóm nhận 14 phản hồi trong 26 phút, phần lớn từ cùng một vòng quen biết.
    - Chỉ 9 người thật sự đã làm hồ sơ.
    - Vậy mà nhóm vẫn dùng các con số 7/9, 3/9 để ra quyết định.
- Lẽ ra nên đề xuất: hỏi thêm người ngoài vòng quen, hoặc phỏng vấn 2–3 DPO.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

DPO hoặc nhân viên IT ở doanh nghiệp mất nhiều ngày để tự lập hồ sơ đánh giá tác động dữ liệu cá nhân theo Nghị định 356. Đây là việc không thể làm qua loa, vì Bộ Công an chấm đạt hoặc không đạt, hồ sơ không đạt có thể bị phạt, và hồ sơ phải cập nhật 6 tháng một lần. Chỗ nghẽn không nằm ở bước điền mẫu mà ở việc biết dữ liệu đang đi đâu: hỏi từng phòng ban và gom hợp đồng với bên thứ ba. Thước đo thành công là thời gian lập hồ sơ lần đầu, giảm từ khoảng 2 tuần xuống dưới 1 tuần. Công cụ không kết luận về pháp lý và không tự nộp hồ sơ, DPO hoặc luật sư luôn duyệt trước. Nhóm đang nghiêng về Rule (bảng hỏi cộng checklist) và chỉ thêm AI ở bước đọc hợp đồng khi có bằng chứng Rule chưa đủ. Quyết định là Not Yet: còn phải kiểm OneTrust và AesirX đã làm được mẫu Việt Nam chưa, và doanh nghiệp có cho đưa tài liệu nội bộ vào AI không.
---

## 7. Tài liệu tham khảo

- Nghị định 356/2025/NĐ-CP, toàn văn (Điều 18, 19, 20, 42): https://thuvienphapluat.vn/van-ban/Quyen-dan-su/Nghi-dinh-356-2025-ND-CP-huong-dan-Luat-Bao-ve-du-lieu-ca-nhan-687428.aspx
- EY Việt Nam — tóm tắt Nghị định 356/2025/NĐ-CP (đã tự mở): https://www.ey.com/vi_vn/technical/tax/tax-and-law-updates/nghi-dinh-so-356-2025-nd-cp-quy-dinh-chi-tiet-mot-so-dieu-va-bien-phap-thi-hanh-luat-bao-ve-du-lieu-ca-nhan
- Tuổi Trẻ (25/6/2026) — Kiểm kê khí nhà kính: có doanh nghiệp gửi 3 lần, 3 bộ số liệu khác nhau (đã tự mở): https://tuoitre.vn/kiem-ke-khi-nha-kinh-co-doanh-nghiep-gui-3-lan-3-bo-so-lieu-khac-nhau-100260625163229417.htm
- MISA AMIS — AI Agent kiểm soát hóa đơn và chứng từ tự động (đã tự mở): https://amis.misa.vn/259621/ai-agent-kiem-soat-hoa-don-va-chung-tu-tu-dong/
- Báo Đầu tư — phạt 5% doanh thu khi vi phạm chuyển dữ liệu xuyên biên giới (cần tự mở): https://baodautu.vn/to-chuc-vi-pham-quy-dinh-chuyen-du-lieu-ca-nhan-xuyen-bien-gioi-bi-phat-5-doanh-thu-d314379.html
- FPT IS VertZéro (cần tự mở): https://baodauthau.vn/giai-phap-made-by-fpt-is-tao-cu-hich-trong-chuyen-doi-xanh-post154145.html
- Sở Y tế Đồng Nai — phần mềm rà soát dữ liệu thanh toán BHYT (cần tự mở): https://syt.dongnai.gov.vn/Lists/Vn%20bn/Attachments/9430/419%20TTTTYTQG.pdf
