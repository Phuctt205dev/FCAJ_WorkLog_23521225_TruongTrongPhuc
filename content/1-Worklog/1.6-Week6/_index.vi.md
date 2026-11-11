---
title: "Worklog Tuần 6"
date: 2026-11-04
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Chuẩn bị hạ tầng và ứng dụng để triển khai thử nền tảng đăng ký sự kiện lên AWS.
* Triển khai thử ứng dụng và thu hồi tài nguyên sau khi hoàn thành.
* Cập nhật giao diện và tìm hiểu cách tự động hóa quá trình triển khai.

### Các công việc đã thực hiện trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 3 | - Rà soát kiến trúc và chuẩn bị quyền truy cập để triển khai ứng dụng lên AWS.<br>- Xây dựng cấu hình hạ tầng bằng Terraform và điều chỉnh ứng dụng để hỗ trợ môi trường AWS.<br>- Tìm hiểu cách tự động hóa việc kiểm tra và triển khai ứng dụng với GitHub Actions. | 03/11/2026 | 03/11/2026 | [AWS IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html); [Terraform](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/aws-create); [GitHub Actions](https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax) |
| 4 | - Tích hợp các cập nhật giao diện và kiểm tra khả năng đóng gói của ứng dụng.<br>- Triển khai thử ứng dụng lên AWS và thu hồi tài nguyên sau khi hoàn thành.<br>- Bổ sung công cụ hỗ trợ kiểm tra tài nguyên sau khi thu hồi. | 04/11/2026 | 04/11/2026 | [CloudFront và S3](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html); [API Gateway và Lambda](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-develop-integrations-lambda.html); [Terraform Destroy](https://developer.hashicorp.com/terraform/cli/commands/destroy) |

Một số tài liệu AWS và Terraform trong bảng được đối chiếu bổ sung sau khi thực hiện công việc.

### Kết quả đạt được tuần 6:

* Chuẩn bị tài khoản và quyền truy cập phục vụ việc triển khai ứng dụng lên AWS.
* Xây dựng cấu hình hạ tầng bằng Terraform, gồm các thành phần lưu trữ giao diện, xử lý yêu cầu và lưu dữ liệu.
* Điều chỉnh ứng dụng và công cụ quản trị để hỗ trợ chạy trên AWS bên cạnh môi trường phát triển hiện có.
* Cập nhật giao diện về màu sắc, bo góc, điều hướng và lưu tùy chọn hiển thị. Kiểm tra đóng gói giao diện thành công.
* Hoàn thành một lượt triển khai thử lên AWS, sau đó thu hồi các tài nguyên của lượt thử và bổ sung công cụ hỗ trợ kiểm kê.
* Tìm hiểu GitHub Actions để kiểm tra và triển khai ứng dụng tự động trong giai đoạn tiếp theo.

Trạng thái cuối tuần: Đã triển khai thử và thu hồi tài nguyên sau thử nghiệm. Cần tiếp tục kiểm tra các chức năng trên AWS, hoàn thiện giám sát và thực hiện kiểm thử tải.
