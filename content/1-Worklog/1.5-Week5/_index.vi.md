---
title: "Worklog Tuần 5"
date: 2026-10-30
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Cụ thể hóa kiến trúc serverless đã chọn thành kế hoạch triển khai ứng dụng lên AWS.
* Chuẩn bị công cụ, tài khoản làm việc và kiểm tra khả năng đóng gói ứng dụng trên máy triển khai.
* Lập dự toán, cấu hình theo dõi ngân sách và xác định cách thu hồi tài nguyên sau thử nghiệm.

### Các công việc đã thực hiện trong tuần:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 4 | - Rà soát ứng dụng local, xác định các phần cần chuẩn bị khi chuyển lên AWS và hoàn thiện kế hoạch triển khai.<br>- Thống nhất triển khai ứng dụng trước, bổ sung giám sát và cảnh báo sau; xác định các bước kiểm tra chức năng và thu hồi tài nguyên.<br>- Lập dự toán theo ngân sách học tập và hoàn thiện tài liệu kế hoạch. | 28/10/2026 | 28/10/2026 | [AWS – CloudFront với S3 riêng tư](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html); [Terraform – Plan](https://developer.hashicorp.com/terraform/cli/commands/plan) |
| 6 | - Cài đặt công cụ, thiết lập tài khoản IAM có MFA và đăng nhập AWS CLI.<br>- Kiểm tra build frontend và đóng gói backend trên máy triển khai.<br>- Điều chỉnh AWS Budgets và cập nhật hướng dẫn chuẩn bị môi trường. | 30/10/2026 | 30/10/2026 | [AWS CLI – Đăng nhập qua trình duyệt](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-sign-in.html); [AWS Budgets](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html) |

### Kết quả đạt được tuần 5:

* Hoàn thiện kế hoạch đưa nền tảng đăng ký sự kiện từ local lên AWS, xác định các bước triển khai và điều kiện kiểm tra. Thống nhất ưu tiên đưa ứng dụng lên hoạt động trước, bổ sung giám sát và cảnh báo sau.
* Chuẩn bị công cụ và tài khoản làm việc trên máy triển khai; đăng nhập AWS CLI và kiểm tra đóng gói frontend, backend thành công. Hoàn thành bước chuẩn bị môi trường để tiếp tục triển khai hạ tầng.
* Lập dự toán phù hợp với ngân sách học tập, cấu hình theo dõi ngân sách và ngưỡng cảnh báo trên AWS Budgets để hỗ trợ kiểm soát chi phí trong quá trình thử nghiệm.
* Hoàn thiện hướng dẫn chuẩn bị môi trường và quy trình kiểm tra, lưu minh chứng, thu hồi tài nguyên sau thử nghiệm; xác định cách triển khai thử mà vẫn giữ dữ liệu local.

Trạng thái cuối tuần: Hoàn thành kế hoạch và bước chuẩn bị môi trường triển khai. Cần tiếp tục hoàn thiện cấu hình ứng dụng và xác minh quyền triển khai; ứng dụng chưa được triển khai hoặc kiểm thử tải trên AWS.


