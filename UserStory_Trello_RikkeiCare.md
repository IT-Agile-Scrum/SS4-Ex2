# Bài Tập: Viết User Story, Acceptance Criteria và theo dõi Trello (RikkeiCare)

## Bước 1. Viết User Story cho R5
- **User Story:** "Là một **quản lý phòng khám**, tôi muốn có thể tự cập nhật giá các gói khám trực tiếp trên phần mềm, để tôi chủ động thay đổi giá kinh doanh nhanh chóng mà không cần phải chờ đợi admin RikkeiCare hỗ trợ."
- **Giải thích chọn vai trò:** Cần chọn vai trò là "quản lý phòng khám" vì họ mới là người dùng cuối (end-user) thực sự của tính năng này và trực tiếp nhận được lợi ích (sự chủ động). Việc "admin RikkeiCare" cập nhật hộ chỉ là một quy trình thủ công tạm thời cần được loại bỏ, chứ admin không phải là đối tượng có nhu cầu tự nhiên cho tính năng này.

## Bước 2. Viết phần Then cho 2 AC của R5
- **AC 1 (thành công):** Given quản lý phòng khám đã đăng nhập, When nhập giá mới hợp lệ cho một gói khám rồi nhấn "Lưu", **Then** hệ thống lưu dữ liệu, hiển thị thông báo "Cập nhật thành công" và mức giá mới lập tức được áp dụng trên giao diện của bệnh nhân.
- **AC 2 (thất bại):** Given quản lý để trống ô giá, When nhấn "Lưu", **Then** hệ thống không lưu thay đổi, giữ nguyên mức giá cũ và hiển thị dòng chữ cảnh báo lỗi "Vui lòng nhập giá cho gói khám".

## Bước 3. Thẻ R5 đã sẵn sàng chưa?
- **Trả lời:** Thẻ R5 **CHƯA** sẵn sàng để được kéo sang cột "Ready for Sprint".
- **Lý do:** Đối chiếu với 4 tiêu chuẩn "Definition of Ready" của nhóm, thẻ R5 hiện tại mới chỉ đáp ứng 2 tiêu chuẩn đầu (đã có User Story và có Acceptance Criteria). Thẻ này **chưa được nhóm phát triển ước lượng khối lượng** (ví dụ: gán Story Point) và **chưa được đánh giá xem có đủ nhỏ** để làm xong trong 1 Sprint hay không. Do thiếu 2 điều kiện này nên không thể chuyển cột.

## Bước 4. Hoàn thiện thẻ R5 trên Trello
- **Nhãn (Label):** Gắn nhãn màu **Xanh dương** (Vì đây là một Feature/Tính năng mới).
- **Người phụ trách (Assignee):** Gán tên Lập trình viên sẽ chịu trách nhiệm phát triển thẻ này.
- **Checklist công việc (Ví dụ 3 mục):**
  1. Tạo giao diện UI form nhập giá mới cho quản lý phòng khám.
  2. Viết API cập nhật dữ liệu giá mới vào Database.
  3. Thêm logic kiểm tra (validate) không cho phép bỏ trống ô giá.
- **Hạn hoàn thành (Due date):** Gắn ngày kết thúc của Sprint hiện tại.
- **Vị trí của thẻ:** Vì R5 là công việc có độ ưu tiên cao nhất, thẻ này phải được sắp xếp nằm ở **vị trí trên cùng (đầu tiên)** của cột "Sprint Backlog" để báo hiệu cho team biết cần tập trung nguồn lực làm trước tiên.

## Bước 5. Đọc Burndown Chart
*(Thông số: Sprint 10 ngày, tổng 30 point. Tốc độ tiêu chuẩn giảm 3 point/ngày).*

**a) Ngày 6 nhóm nhanh hay chậm so với đường lý tưởng?**
- **Điểm lý tưởng ở ngày thứ 6:** 30 point - (6 ngày x 3 point) = 12 point còn lại.
- **Điểm thực tế đang còn:** 20 point (Dữ liệu đề bài cấp).
- **Kết luận:** Nhóm đang làm **CHẬM** hơn tiến độ lý tưởng, và độ lệch đang là: 20 - 12 = **8 point**.

**b) Có nên trừ luôn 3 point vào biểu đồ khi thẻ R5 "xong 80%" không?**
- **Trả lời:** **KHÔNG ĐƯỢC PHÉP TRỪ.**
- **Vì sao:** Trong nguyên tắc Scrum, không có khái niệm hoàn thành 80% hay 99%. Một User Story chỉ được tính là hoàn thành và được phép đốt point (trừ point trên Burndown Chart) khi nó đạt 100% tiêu chuẩn "Definition of Done" (đã code xong, đã test xong, không lỗi). Trừ point sớm sẽ tạo ra ảo giác rằng tiến độ đang tốt, che giấu rủi ro có thể phát sinh bọ (bug) ở 20% công đoạn cuối cùng.
