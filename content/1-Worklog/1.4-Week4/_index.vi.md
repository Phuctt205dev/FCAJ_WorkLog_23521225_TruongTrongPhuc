---
title: "Worklog Tuần 4"
date: 2026-10-24
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Bổ sung tài khoản người tham gia, luồng đặt vé và trang Vé của tôi; đảm bảo việc đăng ký đúng thời gian và không bị trùng.
* Thống nhất đăng nhập, điều hướng theo vai trò và bố cục ứng dụng; mở rộng giao diện quản lý sự kiện và tài khoản User.
* Rà soát các chức năng và giao diện trên môi trường local; hoàn thiện tài liệu phục vụ bàn giao.
* Tiếp thu kiến thức từ mentor về ứng dụng AI trong phỏng vấn ứng viên, xây dựng sản phẩm cùng Kiro Crew và AWS AI PenTesting.

### Các công việc đã thực hiện trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 4 | - Bổ sung giao diện đăng ký, đăng nhập và trang Vé của tôi cho người tham gia.<br>- Phối hợp tích hợp API đặt vé, gắn vé với tài khoản và giới hạn quyền xem vé.<br>- Hoàn thiện xử lý giờ mở bán, hết chỗ và chống tạo vé trùng khi gửi lại yêu cầu. | 21/10/2026 | 21/10/2026 | [OWASP – Authorization](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html); [OWASP – Password Storage](https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html); [DynamoDB Transactions](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/transaction-apis.html); [AWS – Idempotent APIs](https://aws.amazon.com/builders-library/making-retries-safe-with-idempotent-APIs/) |
| 6 | - Thống nhất form đăng nhập chung, quản lý phiên và điều hướng theo vai trò User/Admin.<br>- Hoàn thiện sidebar, navbar và bố cục hiển thị trên máy tính, điện thoại.<br>- Bổ sung tìm kiếm, chỉnh sửa và xóa User; phối hợp xử lý dữ liệu vé và số chỗ khi xóa tài khoản hoặc sự kiện. | 23/10/2026 | 23/10/2026 | [OWASP – Session Management](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html); [OWASP – CSRF Prevention](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html); [OWASP – Authorization](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html); [DynamoDB Transactions](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/transaction-apis.html) |
| 7 | - Tham gia buổi meeting cùng các mentor: xem demo ứng dụng AI trong phỏng vấn ứng viên, tìm hiểu xây dựng sản phẩm cùng Kiro Crew và AWS AI PenTesting.<br>- Dùng thử các luồng tài khoản, đặt/xem vé và quản trị trên môi trường local; rà soát giao diện và xử lý các lỗi phát hiện.<br>- Cập nhật tài liệu API, mô hình dữ liệu và hướng dẫn bàn giao; phối hợp hợp nhất mã nguồn và đồng bộ các nhánh. | 24/10/2026 | 24/10/2026 | Chia sẻ từ mentor; tài liệu bổ sung: [Kiro – Kiro Crew](https://kiro.dev/blog/introducing-kiro-crew/); [AWS – AI PenTesting](https://aws.amazon.com/about-aws/whats-new/2026/03/aws-security-agent-ondemand-penetration/); [Git – Worktree](https://git-scm.com/docs/git-worktree) |

### Kết quả đạt được tuần 4:

* Hoàn thiện tài khoản người tham gia với các chức năng đăng ký, đăng nhập, đăng xuất và xem vé đã đặt; phối hợp tích hợp frontend với backend và phân quyền truy cập.
* Hoàn thiện luồng đặt vé gắn với tài khoản, kiểm tra giờ mở bán và số chỗ còn lại. Bổ sung cơ chế chống đăng ký trùng và xử lý gửi lại yêu cầu khi kết nối gián đoạn.
* Thống nhất đăng nhập và điều hướng theo vai trò User/Admin. Bổ sung sidebar thu gọn, navbar và cải thiện bố cục để sử dụng thuận tiện trên máy tính, điện thoại.
* Mở rộng chức năng quản trị với tìm kiếm, chỉnh sửa và xóa User; cho phép xóa sự kiện đã có người đăng ký. Phối hợp xử lý vé và hoàn chỗ khi cần, bảo toàn dữ liệu không liên quan.
* Rà soát các luồng sử dụng chính trên môi trường local, kiểm tra quyền truy cập và giao diện responsive. Xử lý các lỗi về thao tác giao diện, thông báo và cập nhật dữ liệu được phát hiện trong quá trình dùng thử.
* Cập nhật tài liệu API, mô hình dữ liệu và hướng dẫn bàn giao; phối hợp hợp nhất mã nguồn và đồng bộ các nhánh.
* Quan sát sản phẩm demo ứng dụng AI trong phỏng vấn ứng viên qua phần chia sẻ của mentor; có thêm góc nhìn về cách đưa AI vào bài toán thực tế.
* Được giới thiệu cách xây dựng sản phẩm cùng Kiro Crew, hiểu khái quát cách phối hợp các AI agent để hỗ trợ công việc phát triển phần mềm.
* Tiếp cận kiến thức về AWS AI PenTesting, hiểu vai trò của AI trong hỗ trợ phát hiện, xác minh lỗ hổng và đề xuất khắc phục khi đánh giá bảo mật ứng dụng.

Trạng thái cuối tuần: Hoàn thành đợt nâng cấp tài khoản, đặt vé và quản trị trên môi trường local. Hạ tầng ứng dụng chưa triển khai lên AWS; chức năng đặt vé chưa bao gồm thanh toán.
