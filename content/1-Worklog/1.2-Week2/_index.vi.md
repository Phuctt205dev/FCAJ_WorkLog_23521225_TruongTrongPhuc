---
title: "Worklog Tuần 2"
date: 2026-10-09
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Điều chỉnh kiến trúc nền tảng đăng ký sự kiện để phù hợp với ngân sách học tập.
* Hoàn thiện kế hoạch thực hiện dự án trong 8 tuần và các kịch bản kiểm thử.
* Chuẩn bị môi trường local và bộ khung project để bắt đầu phát triển ứng dụng.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 5 | - Đánh giá chi phí phương án container và lựa chọn kiến trúc serverless.<br>- Xác định các thành phần S3, CloudFront, API Gateway, Lambda và DynamoDB; làm rõ luồng frontend–backend và hướng xử lý đăng ký đồng thời.<br>- Xây dựng kế hoạch 8 tuần, các kịch bản kiểm thử và phương án giảm thời gian duy trì tài nguyên AWS. | 08/10/2026 | 08/10/2026 | [AWS Fargate Pricing](https://aws.amazon.com/fargate/pricing/); [Elastic Load Balancing Pricing](https://aws.amazon.com/elasticloadbalancing/pricing/); [CloudFront Documentation](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html); [DynamoDB Transactions](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/transaction-apis.html) |
| 6 | - Hoàn thiện checklist setup và giới hạn thử tải để kiểm soát số request, thời gian chạy và chi phí.<br>- Chuẩn bị công cụ, môi trường Python, cấu trúc project và repository trên GitHub.<br>- Chạy DynamoDB Local bằng Docker Compose, kiểm tra đọc/ghi và lưu dữ liệu sau khi khởi động lại.<br>- Chạy API mẫu bằng AWS SAM CLI, kiểm tra /health, kết nối frontend mẫu và hoàn thiện hướng dẫn chạy local. | 09/10/2026 | 09/10/2026 | [Python – venv](https://docs.python.org/3/library/venv.html); [Docker Compose](https://docs.docker.com/reference/cli/docker/compose/up/); [DynamoDB Local](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.html); [AWS SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/using-sam-cli-local-start-api.html) |

### Kết quả đạt được tuần 2:

* Chốt hướng kiến trúc serverless phù hợp với ngân sách học tập: frontend trên S3 và CloudFront, API qua API Gateway HTTP API, xử lý bằng Lambda On-Demand và lưu dữ liệu trên DynamoDB On-Demand. Xác định Terraform để quản lý hạ tầng, CloudWatch và SNS để giám sát, cảnh báo; định hướng CI/CD với GitHub Actions và OIDC.
* Làm rõ luồng xử lý giữa frontend, API và database; xác định hướng dùng transaction để cập nhật bộ đếm và tạo bản đăng ký cùng nhau, nhằm tránh đăng ký vượt số chỗ. Frontend không trực tiếp truy cập database hoặc quyết định còn chỗ.
* Xây dựng kế hoạch thực hiện dự án trong 8 tuần, từ setup và phát triển local đến triển khai AWS, kiểm thử, hoàn thiện tài liệu, demo và dọn tài nguyên. Ưu tiên phát triển trên laptop trong giai đoạn đầu để kiểm soát chi phí.
* Thiết kế 5 kịch bản kiểm thử: tranh những chỗ cuối cùng, gửi lại yêu cầu đăng ký, lưu lượng tăng rồi giảm, truy cập API quản trị khi không có quyền và triển khai phiên bản lỗi rồi quay lại bản tốt. Các kịch bản đã có hướng thực hiện và tiêu chí đánh giá, chưa được thực thi.
* Xác định giới hạn cho bài thử tải dự kiến: từ 1 đến 5 request/giây, mỗi lượt kéo dài 2 phút; hai phần đọc và đăng ký dự kiến khoảng 600 request, chưa tính yêu cầu chuẩn bị. Yêu cầu script có thời hạn, điều kiện dừng và không tự retry trong lượt đo đầu; kết quả chỉ phản ánh mức tải đã thử.
* Hoàn thành môi trường local và bộ khung project trên Windows 11: môi trường Python riêng, cấu trúc thư mục, repository trên GitHub, DynamoDB Local, API mẫu và frontend mẫu. Kiểm tra đọc/ghi, khả năng giữ dữ liệu sau khi khởi động lại, API /health và kết nối frontend–backend; hoàn thiện hướng dẫn chạy.

Trạng thái cuối tuần: Môi trường local và bộ khung project đã sẵn sàng. Các chức năng nghiệp vụ đăng ký sự kiện chưa hoàn thành; các bài kiểm thử hệ thống mới ở mức kế hoạch; hạ tầng ứng dụng trên AWS chưa được triển khai.

Bước tiếp theo: Xây dựng frontend với dữ liệu mẫu theo kế hoạch tuần thứ 2 của dự án, chuẩn bị cho giai đoạn phát triển backend và tích hợp local.
