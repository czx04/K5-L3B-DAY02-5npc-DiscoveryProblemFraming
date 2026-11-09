# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: 5npc
- Candidate problem nhóm chọn (1 câu): 
- Quyết định cuối (Go / Not Yet / No-Go):

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Dư Văn Hùng | 2A202603975 | Nhóm trưởng (fork repo, merge PR); hội tụ nhóm, kiểm chứng survey, research (mục 1–3) | [czx04](https://github.com/czx04) |
| 2 | Ngô Minh Cương | 2A202603954 | Mức can thiệp AI (mục 6) | [ngominhcuong](https://github.com/ngominhcuong) |
| 3 | Đoàn Trí Hùng | 2A202603959 | Vẽ quy trình trước/sau, viết Problem Statement v0 (mục 4–5) | [hungdt31](https://github.com/hungdt31) |
| 4 | Hoàng Minh Quyền | 2A202603961 | Đề xuất candidate được chọn (#1); viết Problem Statement v1 + tiêu chí đánh giá (mục 7) | [EddyTryToCode](https://github.com/EddyTryToCode) |
| 5 | Trần Quang Hà | 2A202603962 | 4 rủi ro + quyết định Go / Not Yet / No-Go (mục 8) | [tranha1764](https://github.com/tranha1764) |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | Dư Văn Hùng | Cả nhóm (mỗi người pitch 3 candidate) | Cluster, cây OST, bảng chấm điểm |
| CP4 — Kiểm chứng | Dư Văn Hùng | | Assumption map, snapshot hoặc survey |
| CP4 — Research | Dư Văn Hùng | | Bảng research có link |
| CP5 — Quy trình trước/sau | Đoàn Trí Hùng | | Quy trình + bảng before/after |
| CP5 — Problem Statement v0 | Đoàn Trí Hùng | | Problem Statement v0 |
| CP6 — Mức can thiệp + Problem Statement v1 | Ngô Minh Cương (mức can thiệp, mục 6); Hoàng Minh Quyền (Problem Statement v1 + tiêu chí eval, mục 7) | | Ma trận, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định | Trần Quang Hà | | 4 rủi ro + Go/Not Yet/No-Go |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### HoVaTen-MSSV

**Phần việc phụ trách:**

-

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

-

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

-

**Điều mình học được từ phần nhóm:**

-

### Đoàn Trí Hùng - 2A202603959

**Phần việc phụ trách:**

- CP5: quy trình trước/sau (mục 4) và Problem Statement v0 (mục 5) của báo cáo nhóm.
- CP3: pitch 3 candidate từ báo cáo cá nhân (Card #1 là phân tích yêu cầu nghiệp vụ).

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- **4.1 Quy trình hiện tại:** sơ đồ Mermaid 7 bước, từ gửi bảng hỏi phòng ban đến bổ sung hồ sơ khi không đạt. Kèm bảng actor / input / output / thời gian cho từng bước. Chỉ ra bottleneck là bước 1–2 ("biết dữ liệu cá nhân đang đi đâu"), dựa trên câu 7 của survey.
- **4.2 Quy trình tương lai:** tách từng bước thành Rule, AI hay con người. Có 2 điểm con người kiểm tra (HITL): DPO duyệt từng dòng danh mục do AI trích, luật sư/DPO ký trước khi nộp. Có 4 boundary AI không được làm, và phương án quay về làm tay bằng Excel khi AI sai.
- **4.3 Before/after:** so sánh số bước, tổng thời gian, số bước thủ công, chỗ bottleneck dịch chuyển và 4 rủi ro mới kèm cách giảm.
- **Mục 5 Problem Statement v0:** soạn đủ 6 trường theo các lựa chọn nhóm đã chốt (actor doanh nghiệp 50–200 người, metric tổng thời gian lập hồ sơ, đo bằng sheet log của DPO). Đưa v0 cho AI phản biện, ghi lại 5 điểm yếu và cách xử lý cho v1 / mục 8.
- **Cập nhật số liệu:** khi survey tăng từ 9 lên 14 người, đối chiếu lại toàn bộ mục 4–5 với ảnh kết quả survey và gắn mỗi con số với câu hỏi và ảnh tương ứng.
- Có dùng AI (Claude) để chuyển mô tả sang Mermaid và phản biện v0. Nội dung đã tự kiểm tra từng bước; chi tiết ghi ở bảng "Dùng AI" trong báo cáo cá nhân.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/team/group_report.md`: mục 4.1, 4.2, 4.3 và mục 5 (gồm bảng "Phản biện nhận được").
- Commit `ba4acf3` trên nhánh `group_report_4_5`, merge qua PR #8: viết mục 4–5 lần đầu.
- Commit `2790f2d` trên nhánh `hotfix/group_report_4_5`, merge qua PR #10: sửa nội dung mục 4–5 bị lệch số liệu sau khi survey tăng từ 9 lên 14 người, gắn từng con số với câu hỏi và ảnh survey, tô màu bottleneck trên sơ đồ 4.1.
- Nguồn số liệu dẫn link trong mục 4–5: ảnh survey `report/assets/image.png`, `image-1.png`, `image-2.png`, `image-3.png` (do nhóm trưởng tải lên).

**Điều mình học được từ phần nhóm:**

- Mỗi con số trong quy trình phải trỏ về được nguồn cụ thể. Khi survey tăng từ 9 lên 14 người, mục 4–5 của mình bị lệch với mục 3.2 mà mình không biết. Từ đó mình ghi rõ số câu hỏi và ảnh cạnh từng con số, để khi nguồn đổi thì biết chỗ nào cần sửa.
- Vẽ quy trình tương lai xong mới thấy AI chỉ làm 1 trong 7 bước, và bottleneck chuyển sang khâu chờ phòng ban trả lời. Nghĩa là metric "tổng thời gian" có thể không giảm dù AI làm tốt. Trước đó mình nghĩ cứ thêm AI vào bước nghẽn là đủ.
- Thu hẹp actor nghe đơn giản nhưng kéo theo nhiều việc. Khi chỉ còn doanh nghiệp 50–200 người, baseline tính trên cả nhóm 200–1.000 người không còn đúng, và actor có thể rơi vào diện được miễn lập hồ sơ. Mỗi lần đổi phạm vi phải kiểm lại cả dữ liệu lẫn luật.