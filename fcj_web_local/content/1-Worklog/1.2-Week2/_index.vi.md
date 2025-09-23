---
title: "Worklog Tuần 2"
date: "2025-09-09"
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

- Kết nối, làm quen với các thành viên trong First Cloud Journey.
- Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ 	| Công việc 	| Ngày bắt đầu 	| Ngày kết thúc 	| Nguồn tài liệu và ghi chú học tập 	|
|---	|---	|---	|---	|---	|
| 2 	| - Tìm hiểu về AWS Virtual Private Cloud (VPC)<br>   + VPC là gì? <br>   + Cấu trúc của VPC được hoạt động như thế nào?<br>- Tìm hiểu về VPC-Subnets và kiến trúc của Subnet?<br>- Tìm hiểu về VPC-Route Table?<br>- Tìm hiểu về VPC-ENI và kiến trúc của VPC-ENI?<br>- Tìm hiểu về VPC-Endpoint và kiến trúc của VPC-Endpoint?<br>- Tìm hiểu về VPC-Internet Gateway và kiến trúc của VPC-Internet Gateway?<br>- Tìm hiểu về VPC-NAT Gateway và kiến trúc của VPC-NAT Gateway?<br>- Tìm hiểu về VPC-Security Group và kiến trúc của VPC-Security Group?<br>- Tìm hiểu về VPC-NACL và kiên trúc của VPC-NACL?<br>- Tìm hiểu về VPC-Flow Logs 	| 15/09/2025 	| 15/09 	| Tài liệu: https://cloudjourney.awsstudygroup.com/<br>Youtube: https://youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&si=W80Cdf_fSc6sjOV_<br>Ghi chú: https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_02/Module_02_01_VPC/Take_notes_module_02_01.md 	|
| 3 	| - Tìm hiểu về các dịch vụ mạng trên AWS?<br>- Tìm hiểu về VPC Peering và kiến trúc của VPC Peering?<br>- Tìm hiểu về Transit Gateway và kiến trúc của Transit Gateway?<br>- Nắm rõ các khái niệm về dịch vụ VPN & Direct Connect?<br>- VPN Site to Site là gì? Việc thiết lập nó như thế nào?<br>- Tìm hiểu về VPN Client to Site?<br>- AWS Direct Connect là gì? 	| 16/09/2025 	|  	| Tài liệu: https://cloudjourney.awsstudygroup.com/<br>Youtube: https://youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&si=W80Cdf_fSc6sjOV_<br>Ghi chú: https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_02/Module_02_01_VPC/Take_notes_module_02_01.md 	|
| 4 	| - Tìm hiểu về các khái niệm và tổng quan về Elastic Load Balancing? Và các loại ELB hiện nay?<br>- Tìm hiểu về ELB - Application Load Balancer và kiến trúc của nó?<br>- Tìm hiểu về ELB - Network Load Balancer và nắm rõ khái niệm?<br>- Tìm hiểu về ELB - Classic Load Balancer và nắm rõ khái niệm?<br>- Tìm hiểu về ELB - ELB - Gateway Load Balancer và kiến trúc của nó? 	| 17/09/2025 	|  	| Tài liệu: https://cloudjourney.awsstudygroup.com/<br>Youtube: https://youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&si=W80Cdf_fSc6sjOV_<br>Ghi chú: https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_02/Module_02_01_VPC/Take_notes_module_02_01.md 	|
| 5 	| - Thực hành Lab 03<br>- Thực hành Lab 58<br>- Thực hành Lab 19 	| 18/09/2025 	|  	| Tài liệu: https://cloudjourney.awsstudygroup.com/<br>Youtube: https://youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&si=W80Cdf_fSc6sjOV_<br>Ghi chú: https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_02/Module_02_01_VPC/Take_notes_module_02_01.md 	|
| 6 	| - Thực hành Lab 20<br>- Thực hành Lab 10<br>- Nghiên cứu bổ sung về AWS Advanced Networking - Specialty Study Guide 	| 19/09/2025 	|  	| Tài liệu: https://cloudjourney.awsstudygroup.com/<br>Youtube: https://youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&si=W80Cdf_fSc6sjOV_<br>Ghi chú: https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_02/Module_02_01_VPC/Take_notes_module_02_01.md 	|

### Kết quả đạt được tuần 2:

- Hiểu AWS là gì và nắm được các nhóm dịch vụ cơ bản:

  - Compute
  - Storage
  - Networking
  - Database
  - ...

- Đã tạo và cấu hình AWS Free Tier account thành công.

- Làm quen với AWS Management Console và biết cách tìm, truy cập, sử dụng dịch vụ từ giao diện web.

- Cài đặt và cấu hình AWS CLI trên máy tính bao gồm:

  - Access Key
  - Secret Key
  - Region mặc định
  - ...

- Sử dụng AWS CLI để thực hiện các thao tác cơ bản như:

  - Kiểm tra thông tin tài khoản & cấu hình
  - Lấy danh sách region
  - Xem dịch vụ EC2
  - Tạo và quản lý key pair
  - Kiểm tra thông tin dịch vụ đang chạy
  - ...

- Có khả năng kết nối giữa giao diện web và CLI để quản lý tài nguyên AWS song song.
- ...
