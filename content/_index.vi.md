+++
title = "AI/ML"
date = 2025
weight = 1
chapter = false
+++

# Bedrock Series: Ảnh tạo sinh với Stability AI

#### Tổng quan

Trong thời đại của trí tuệ nhân tạo (AI) và điện toán đám mây, việc tạo ra các ứng dụng thông minh và tự động hóa đã trở nên dễ dàng hơn bao giờ hết. Workshop này sẽ đưa bạn vào một hành trình thú vị, nơi chúng ta sẽ xây dựng một hệ thống tạo ảnh tự động sử dụng **Stable Diffusion** – một trong những mô hình tạo ảnh tiên tiến nhất hiện nay.

Bạn sẽ tiếp cận chủ đề **Generative AI** với dịch vụ Amazon Bedrock làm chủ đạo, sử dụng model **Stability AI** để tự động sinh ảnh dựa trên prompt được cung cấp. Kết hợp với **Lambda và API Gateway** để tạo REST API từ đó có thể request bằng **Postman** hay các công cụ khác, bất kì đâu (localhost, frontend-websites...) tới Bedrock để nhận lại một hình ảnh độc đáo được tạo ra bởi AI.

#### Sơ đồ kiến trúc

![Image](/images/capture_ws2/ArchitectureImage.png?width=90pc)

#### Mục tiêu

Sau khi xong workshop này, chúng ta sẽ xây dựng được một hệ thống tạo ảnh tự động sử dụng Stable Diffusion thông qua AWS Bedrock, kết hợp với các dịch vụ AWS Lambda, API Gateway, và S3. Hệ thống này cho phép người dùng gửi một prompt (yêu cầu văn bản) và nhận lại một hình ảnh được tạo ra bởi AI. Hình ảnh sau khi tạo sẽ được lưu trữ trên S3 và người dùng có thể truy cập thông qua một Pre-signed URL. Hiểu và có thể ứng dụng trong thực tế các website hoặc nâng cấp mở rộng các tính năng nâng cao hơn từ các dịch vụ AWS hay model AI khác.

{{% notice note %}}
Tài khoản AWS của bạn phải được tạo ít nhất 24 giờ trước khi thực hiện workshop. Điều này đảm bảo rằng tài khoản của bạn đã được kích hoạt đầy đủ và có thể sử dụng các dịch vụ như Bedrock
{{% /notice %}}

#### Nội dung chính

Workshop sẽ được chia thành 6 phần chính:

1. [Model Access và yêu cầu cần thiết](1-Model-Access_Prerequites/): Thiết lập quyền truy cập vào mô hình Stable Diffusion trên AWS Bedrock.
2. [Tạo S3 Bucket và set up hàm Lambda](2-Creation-S3-Bucket_ConfigureLambda/): Tạo S3 bucket để lưu trữ ảnh và thiết lập Lambda function để xử lý yêu cầu.
3. [Tích hợp Lambda với Bedrock & Test Event](3-Integration-Bedrock-&Test-Event/): Kết nối Lambda với Bedrock và kiểm tra việc tạo ảnh.
4. [Kết nối Lambda với API Gateway](4-Map-Lambda-With-APIGateway/): Tạo API Gateway để người dùng có thể gửi yêu cầu qua HTTP.
5. [Test ảnh tạo sinh trên Postman](5-Test-Image-Generation-On-Postman/): Kiểm tra toàn bộ hệ thống bằng cách gửi yêu cầu qua Postman.
6. [Dọn dẹp tài nguyên](6-Clean-up-resources): Xóa các tài nguyên đã tạo để tránh phát sinh chi phí.
