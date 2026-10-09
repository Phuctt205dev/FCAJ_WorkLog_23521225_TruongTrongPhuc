---
title: "Worklog Tuần 1"
date: 2026-10-02
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1:

* Làm quen với môi trường thực tập tại văn phòng AWS, nội quy và chương trình First Cloud AI Journey (FCAJ).
* Tìm hiểu các nguồn học tập, cách ghi Worklog và cấu trúc trình bày Workshop.
* Phân tích bài toán và xây dựng Proposal cho đề tài Online Event Registration Platform trên AWS, xác định kiến trúc và kế hoạch triển khai ban đầu.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 4 | - Làm quen với môi trường thực tập, nội quy và chương trình FCAJ.<br>- Tham khảo Worklog, Workshop mẫu và các nguồn học tập.<br>- Phân tích bài toán đăng ký sự kiện, xác định phạm vi ứng dụng và xây dựng kiến trúc sơ bộ.<br>- Tìm hiểu tính sẵn sàng cao, Application Load Balancer, Auto Scaling và cơ chế tự phục hồi. | 30/09/2026 | 30/09/2026 | [FCAJ](https://cloudjourney.awsstudygroup.com/); [Worklog mẫu](https://workshop-sample.awsfcaj.com/1-worklog/); [Application Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html); [Auto Scaling Health Checks](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-health-checks.html); [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) |
| 5 | - Tiếp tục xây dựng Proposal; điều chỉnh kiến trúc theo hướng tách frontend trên Vercel và backend trên AWS.<br>- Tìm hiểu RDS PostgreSQL, giới hạn của Auto Scaling khi lượng truy cập tăng đột biến và yêu cầu tránh đăng ký vượt số chỗ.<br>- Xác định phương án kiểm soát chi phí và sử dụng Terraform để quản lý vòng đời hạ tầng. | 01/10/2026 | 01/10/2026 | [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html); [Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html); [Vercel Documentation](https://vercel.com/docs/git); [Terraform Documentation](https://developer.hashicorp.com/terraform/docs); [AWS Pricing](https://aws.amazon.com/pricing/) |
| 6 | - Tìm hiểu giám sát, cảnh báo và bảo mật với CloudWatch, SNS, IAM, Systems Manager và Secrets Manager.<br>- Nghiên cứu CI/CD, Blue/Green Deployment và Rollback.<br>- Hoàn thiện định hướng kỹ thuật cho Proposal; lập lộ trình triển khai, các kịch bản kiểm thử và luồng demo Workshop. | 02/10/2026 | 02/10/2026 | [CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html); [SNS](https://docs.aws.amazon.com/sns/latest/dg/welcome.html); [IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html); [Systems Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager.html); [Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html); [CodePipeline](https://docs.aws.amazon.com/codepipeline/latest/userguide/welcome.html); [CodeBuild](https://docs.aws.amazon.com/codebuild/latest/userguide/welcome.html); [CodeDeploy](https://docs.aws.amazon.com/codedeploy/latest/userguide/welcome.html) |

### Kết quả đạt được tuần 1:

* Nắm được nội quy, cách tổ chức chương trình FCAJ và các nguồn tài liệu phục vụ quá trình thực tập; hiểu cách ghi Worklog và trình bày Workshop.
* Xác định được bài toán Online Event Registration Platform và phạm vi chức năng chính: xem sự kiện, đăng ký, quản lý sự kiện và số lượng chỗ. Định hướng giữ ứng dụng đơn giản để tập trung vào hạ tầng AWS và DevOps.
* Xây dựng Proposal và kiến trúc đề xuất: frontend trên Vercel, backend trên EC2 qua Application Load Balancer, kết hợp Auto Scaling Group và RDS PostgreSQL. Tìm hiểu phương án triển khai tầng ứng dụng trên nhiều Availability Zone để tăng tính sẵn sàng và hỗ trợ tự phục hồi.
* Nhận biết các vấn đề cần kiểm chứng khi triển khai: độ trễ mở rộng của Auto Scaling khi lượng truy cập tăng đột biến và tính nhất quán dữ liệu khi nhiều người cùng đăng ký những chỗ cuối cùng.
* Xác định phương án kiểm soát chi phí: phát triển ứng dụng trên môi trường local, dùng RDS Single-AZ cho Workshop và sử dụng Terraform để tạo, dọn dẹp hạ tầng phục vụ kiểm thử hoặc demo.
* Định hướng sử dụng CloudWatch và SNS để giám sát, cảnh báo; nghiên cứu IAM, Systems Manager và Secrets Manager phục vụ bảo mật, quản trị hệ thống. Tìm hiểu phương án CI/CD với CodePipeline, CodeBuild và CodeDeploy, bao gồm Blue/Green Deployment và Rollback.
* Lập lộ trình triển khai và các kịch bản kiểm thử: hoạt động bình thường, lượng truy cập tăng đột biến, lỗi EC2 hoặc ứng dụng, đăng ký đồng thời, triển khai phiên bản mới và xử lý triển khai thất bại; xây dựng luồng demo tương ứng.

Trạng thái cuối tuần: Hoàn thành giai đoạn làm quen, nghiên cứu và lập kế hoạch; chưa triển khai hạ tầng AWS thực tế.

Bước tiếp theo: Xây dựng phiên bản ứng dụng tối thiểu (MVP) trên môi trường local, sau đó triển khai từng thành phần của kiến trúc AWS theo lộ trình đã lập.
