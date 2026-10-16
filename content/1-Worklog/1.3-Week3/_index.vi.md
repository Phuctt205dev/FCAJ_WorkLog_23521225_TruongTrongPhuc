---
title: "Worklog Tuần 3"
date: 2026-10-16
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Bổ sung giao diện chọn vai trò và luồng đăng nhập, quản lý phiên, đăng xuất cho quản trị viên.
* Hoàn thiện giao diện quản lý sự kiện, phối hợp tích hợp API và thống nhất các quy tắc bảo vệ dữ liệu đăng ký.
* Kiểm tra chức năng, giao diện responsive và kết quả tích hợp trên môi trường local; cập nhật tài liệu dự án.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 3 | - Phân tích luồng Người tham gia và Quản trị viên; xác định các thao tác cần đăng nhập và kiểm tra quyền.<br>- Thống nhất thông tin trong form quản trị, quy tắc mở/đóng đăng ký, chặn xóa sự kiện đã có chỗ dùng và không giảm sức chứa dưới số chỗ đã dùng.<br>- Thiết kế giao diện chọn vai trò, đăng nhập và bố cục quản trị, tái sử dụng hệ thống giao diện hiện có. | 13/10/2026 | 13/10/2026 | [OWASP – Authorization](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html); [Schema.org – Event](https://schema.org/Event) |
| 5 | - Hoàn thiện giao diện danh sách, tìm kiếm, thêm/sửa sự kiện, xác nhận xóa và mở/đóng đăng ký.<br>- Tích hợp đăng nhập, kiểm tra phiên và đăng xuất; cấu hình frontend gọi API qua Vite proxy, xử lý trạng thái tải và thông báo lỗi.<br>- Phối hợp phía backend cập nhật API contract, kiểm tra quyền, bảo vệ phiên và xử lý xung đột khi sửa/xóa sự kiện. | 15/10/2026 | 15/10/2026 | [OWASP – Session Management](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html); [OWASP – CSRF Prevention](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html); [OWASP – Authentication](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html) |
| 6 | - Kiểm tra luồng chọn vai trò, đăng nhập/tải lại/đăng xuất, quản lý sự kiện và luồng đăng ký của người tham gia trên local.<br>- Rà soát responsive, cách hiển thị nội dung sự kiện và các tình huống không đủ quyền, xung đột dữ liệu, chặn xóa khi có chỗ dùng.<br>- Đối chiếu kết quả kiểm thử, build/lint; cập nhật tài liệu và dùng thử lại môi trường local để xác nhận kết quả. | 16/10/2026 | 16/10/2026 | [AWS SAM – Validate](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/sam-cli-command-reference-sam-validate.html); [Python – unittest](https://docs.python.org/3/library/unittest.html); [Vite – Build](https://vite.dev/guide/build.html) |

### Kết quả đạt được tuần 3:

* Bổ sung trang chọn vai trò và các màn hình đăng nhập, quản lý sự kiện cho quản trị viên; giữ luồng người tham gia xem, tìm kiếm và đăng ký sự kiện mà không cần tài khoản.
* Hoàn thiện giao diện danh sách, tìm kiếm, thêm/sửa/xóa và mở/đóng đăng ký. Form quản trị hỗ trợ tên, danh mục, thời gian theo giờ Việt Nam, địa điểm, đơn vị tổ chức, sức chứa và nội dung sự kiện; giữ nhất quán với thiết kế có sẵn.
* Phối hợp tích hợp frontend với các API quản trị và cập nhật API contract phiên bản 2. Luồng đăng nhập giữ được phiên khi tải lại và thu hồi phiên khi đăng xuất; chọn vai trò trên giao diện không tự cấp quyền quản trị.
* Nắm được cách phối hợp giữa giao diện và backend để kiểm tra quyền, bảo vệ phiên bằng cookie HttpOnly/SameSite và kiểm tra CSRF/Origin. Các quy tắc chặn xóa khi có chỗ dùng, bảo toàn số chỗ đã dùng và phát hiện xung đột phiên bản đã được kiểm tra trong đợt nâng cấp.
* Kết quả kiểm thử chung của đợt nâng cấp được ghi nhận trong nhật ký: 45 unit test và 2 integration test đạt. Các tình huống tranh chỗ cuối, trùng email, quyền truy cập, quản lý phiên và cập nhật đồng thời đã được kiểm tra.
* Frontend build/lint và SAM build/validate đạt; frontend còn hai cảnh báo Fast Refresh cũ tại Button và Badge. Kiểm tra Edge headless ghi nhận các luồng chính hoạt động; các trang mới không tràn ngang tại chiều rộng 320, 375, 414, 768 và 1280 px. Nội dung script thử nghiệm hiển thị như văn bản, không thực thi.
* Cập nhật tài liệu chạy local, API contract, mô hình dữ liệu và quy tắc bảo mật. Dùng thử lại ứng dụng với tài khoản quản trị, kiểm tra trạng thái backend và phân biệt số chỗ mô phỏng trong dữ liệu mẫu với bản ghi đăng ký thực tế.

Trạng thái cuối tuần: Hoàn thành đợt nâng cấp vai trò và quản trị sự kiện trên môi trường local. Hạ tầng ứng dụng chưa triển khai lên AWS; các phương án cấp tài khoản quản trị trên production mới ở mức trao đổi.
