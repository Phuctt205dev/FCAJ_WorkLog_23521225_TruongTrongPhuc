# Worklog tuần 2 – Điều chỉnh kiến trúc và chuẩn bị môi trường dự án

**Thời gian: 08/10/2026–09/10/2026**

## 1. Mục tiêu

- Điều chỉnh kiến trúc nền tảng đăng ký sự kiện để phù hợp với ngân sách học tập.
- Chốt kế hoạch thực hiện trong 8 tuần và các kịch bản kiểm thử.
- Hoàn thành môi trường local và bộ khung project để bắt đầu phát triển.

**Tuần 2 thực tập** đồng thời là **tuần đầu thực hiện dự án**, tập trung vào thiết kế và setup.

## 2. Các công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|---|---|---|---|---|
| Thứ Năm | Đánh giá chi phí, điều chỉnh kiến trúc sang serverless; làm rõ luồng frontend–backend; xây dựng kế hoạch 8 tuần và phương án kiểm thử | 08/10/2026 | 08/10/2026 | AWS Pricing; CloudFront Documentation; DynamoDB Transactions; API Gateway Documentation |
| Thứ Sáu | Hoàn thiện checklist setup và giới hạn thử tải; chuẩn bị công cụ, repository, DynamoDB Local, API mẫu và frontend local; kiểm tra lại bộ khung project | 09/10/2026 | 09/10/2026 | Python Documentation; Git Documentation; Docker Compose Documentation; DynamoDB Local; AWS SAM CLI |

## 3. Nội dung chi tiết

### Thứ Năm – 08/10/2026: Điều chỉnh kiến trúc và lập kế hoạch

#### Đánh giá chi phí và lựa chọn kiến trúc

Đã xem xét các khoản phí của phương án container sử dụng ECS Fargate, ALB và các kết nối mạng. Qua phân tích, xác định rằng task, ALB và interface endpoint vẫn có thể phát sinh phí khi được duy trì dù ít người truy cập.

Đã lựa chọn hướng serverless để giảm nhu cầu giữ tài nguyên ứng dụng chạy liên tục.

| Thành phần dự kiến | Vai trò |
|---|---|
| S3 và CloudFront | Lưu và cung cấp giao diện website qua HTTPS |
| API Gateway HTTP API | Nhận yêu cầu từ frontend |
| Lambda On-Demand | Xử lý yêu cầu và kiểm tra quyền |
| DynamoDB On-Demand | Lưu sự kiện và lượt đăng ký |
| CloudWatch và SNS | Theo dõi hệ thống và gửi cảnh báo |
| Terraform | Quản lý hạ tầng AWS |
| GitHub Actions và OIDC | Kiểm thử, triển khai bằng quyền AWS tạm thời |

Đã làm rõ luồng xử lý: trình duyệt tải giao diện từ CloudFront, gọi HTTP API, sau đó Lambda đọc hoặc ghi DynamoDB và trả kết quả.

Đối với đăng ký, đã xác định hướng dùng transaction để tăng bộ đếm và tạo bản đăng ký cùng nhau. Frontend không trực tiếp quyết định còn chỗ hoặc truy cập database.

#### Chốt kế hoạch thực hiện

Đã xây dựng kế hoạch 8 tuần:

| Tuần dự án | Nội dung |
|---|---|
| 1 | Setup môi trường, đặt tên đề tài và tạo bộ khung project |
| 2 | Xây dựng frontend với dữ liệu mẫu |
| 3 | Xây dựng backend, database local và tích hợp frontend |
| 4 | Xử lý đăng ký đồng thời, chống trùng và quyền quản trị |
| 5 | Hoàn thiện local, chuẩn bị Terraform và CI |
| 6 | Triển khai AWS |
| 7 | Kiểm thử, giám sát và thu minh chứng |
| 8 | Hoàn thiện tài liệu, demo và dọn tài nguyên |

Phương án tiết kiệm được xác định là phát triển trên laptop trong giai đoạn đầu, chỉ sử dụng AWS khi cần tích hợp, kiểm thử và demo.

#### Xác định các kịch bản kiểm thử

Đã xây dựng năm kịch bản:

- Nhiều người tranh những chỗ cuối cùng.
- Gửi lại yêu cầu sau khi bấm nhiều lần hoặc mất phản hồi.
- Lưu lượng tăng rồi giảm.
- Gọi API quản trị khi không có quyền.
- Triển khai phiên bản lỗi, phát hiện và quay lại bản tốt.

Mỗi kịch bản đã có hướng thực hiện, công cụ dự kiến và tiêu chí đánh giá. Các nội dung này mới ở mức thiết kế, chưa phải kết quả kiểm thử.

**Kết quả ngày:**

- Chốt hướng kiến trúc serverless và luồng xử lý.
- Xác định cơ chế chống đăng ký vượt số chỗ.
- Có kế hoạch 8 tuần và các kịch bản kiểm thử.
- Xác định cách giảm thời gian duy trì tài nguyên AWS.

**Nguồn tham khảo:**

- [AWS Fargate Pricing](https://aws.amazon.com/fargate/pricing/)
- [Elastic Load Balancing Pricing](https://aws.amazon.com/elasticloadbalancing/pricing/)
- [AWS PrivateLink Pricing](https://aws.amazon.com/privatelink/pricing/)
- [AWS Lambda Pricing](https://aws.amazon.com/lambda/pricing/)
- [Amazon API Gateway Pricing](https://aws.amazon.com/api-gateway/pricing/)
- [CloudFront – Restrict access to an S3 origin](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html)
- [DynamoDB Transactions](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/transaction-apis.html)

### Thứ Sáu – 09/10/2026: Hoàn thiện kế hoạch và setup local

#### Giới hạn bài thử tải

Đã điều chỉnh bài thử tải để kiểm soát lượng request và chi phí:

| Giai đoạn | Tải | Thời gian |
|---|---:|---:|
| Khởi động | 1 request/giây | 30 giây |
| Tăng tải | 3 request/giây | 30 giây |
| Cao điểm nhỏ | 5 request/giây | 30 giây |
| Giảm tải | 1 request/giây | 30 giây |

Mỗi phần dự kiến khoảng 300 request; phần đọc và phần đăng ký khoảng 600 request, chưa tính yêu cầu chuẩn bị. Đã xác định script phải có thời hạn, điều kiện dừng và không tự retry trong lượt đo đầu.

Đã hiểu rằng bài test này chỉ chứng minh hành vi ở mức tải đã thử. Cảnh báo ngân sách không thay thế cho giới hạn trong script.

#### Hoàn thành môi trường phát triển

Đã hoàn thành setup bộ khung project trên Windows 11 tại thư mục `D:\aws-workshop\event-registration`.

Các công việc gồm:

- Chuẩn bị công cụ phát triển và môi trường Python riêng.
- Tổ chức thư mục frontend, backend, kiểm thử, hạ tầng và tài liệu.
- Chuẩn bị repository và lưu mã nguồn trên GitHub.
- Chạy DynamoDB Local bằng Docker Compose.
- Kiểm tra đọc/ghi và khả năng giữ dữ liệu sau khi khởi động lại.
- Chạy Lambda local bằng AWS SAM CLI, kiểm tra API `/health`.
- Kết nối frontend mẫu với API và hiển thị trạng thái backend.
- Hoàn thiện hướng dẫn chạy và kiểm tra lại môi trường.

Trong quá trình chạy database, đã sử dụng `docker compose config --quiet` để kiểm tra cấu hình và `docker compose up -d` để khởi động container.

Đã bổ sung yêu cầu đặt tên đề tài bằng tiếng Việt và tiếng Anh. Báo cáo chưa ghi tên cụ thể do chưa có nội dung xác nhận tên đã chọn.

**Kết quả ngày:**

- Hoàn thành giai đoạn setup của tuần đầu thực hiện dự án.
- Database local, API mẫu và frontend mẫu đã hoạt động.
- Có bộ khung project và hướng dẫn để tiếp tục phát triển.
- Có giới hạn rõ ràng cho bài thử tải dự kiến.

**Nguồn tham khảo:**

- [Python – venv](https://docs.python.org/3/library/venv.html)
- [Git Documentation](https://git-scm.com/doc)
- [DynamoDB Local](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.html)
- [Docker Compose – config](https://docs.docker.com/reference/cli/docker/compose/config/)
- [Docker Compose – up](https://docs.docker.com/reference/cli/docker/compose/up/)
- [AWS SAM CLI – Local API testing](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/using-sam-cli-local-start-api.html)
- [Grafana k6 – Thresholds](https://grafana.com/docs/k6/latest/using-k6/thresholds/)
- [AWS Budgets](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html)

## 4. Kết quả đạt được trong tuần

Đã hoàn thành việc điều chỉnh định hướng kiến trúc, lập kế hoạch 8 tuần, thiết kế các kịch bản kiểm thử và setup bộ khung project trên laptop.

So với tuần trước, dự án đã chuyển từ nghiên cứu phương án ban đầu sang lựa chọn kiến trúc cụ thể và chuẩn bị được môi trường để phát triển.

**Trạng thái cuối tuần:**

- Môi trường local và bộ khung project đã sẵn sàng.
- Các chức năng nghiệp vụ đăng ký sự kiện chưa thuộc phạm vi hoàn thành của giai đoạn setup.
- Các bài kiểm thử hệ thống mới ở mức kế hoạch.
- Hạ tầng ứng dụng trên AWS chưa được triển khai.

## 5. Tài liệu tham khảo chung

Các nguồn kỹ thuật được liệt kê theo từng ngày ở mục 3. Yêu cầu trình bày kiến trúc, demo và chi phí được đối chiếu với [Tiêu chí chấm Workshop FCAJ](https://hcm-rules.awsfcaj.com/5-scoring/).