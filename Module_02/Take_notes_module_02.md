# **Module 2 - Dịch vụ mạng trên AWS**
## **I. AWS Virtual Private Cloud (VPC)**
### 1. Giới thiệu về Amazon VPC 
- Là một dịch vụ cung cấp môi trường mạng ảo riêng tư, nó được cô lập về mặt logic khỏi các mạng khác ở AWS Cloud, nó hoàn toàn tách biệt với thế giới bên ngoài.
- Amazon VPC cho phép khởi chạy và tạo các tài nguyên AWS vào một mạng ảo mà bạn đã xác định. 
- Giả sử chúng ta tạo ra một lớp mạng ảo: 
    + VPC 10.10.0.0/16 : Trong này có những gì?
    + Các tài nguyên, các máy chủ, các cơ sở dữ liệu, các thiết bị cân bằng tải sẽ được đặt ở đâu trong lớp mạng ảo này?
    + Lớp mạng ảo này liên quan gì đến Availability Zone trong Module 1?
- Mô hình trình bày mạng ảo: 

            AWS Cloud - Account: 3345-2334-1232 "Tài khoản có Unique ID gồm 12 số"
            |
            Region Singapore: ap-southeast-1 (tối thiểu gồm 3 AZ)
            |
            Availability Zone: ap-southest-1b

- VPC nó nằm trong -> **Region** -> thì **VPC** sẽ chạy nhiều máy chủ, các cơ sở dữ liệu trên nhiều **Availability** khác nhau. => Đây là practice cơ bản nhất để triển khai ứng dụng và dịch vụ ở trên cloud, triển khai mô hình ở **multi AZ** để đảm bảo độ ổn định cao.
- AZ (Availability Zone): một cụm trung tâm dữ liệu
- Môi trường truyền thống việc triển khai ứng dụng ở 2 AZ, thì nó giống hai mô hình triển khai ở DC (Data Center) và DR (Disaster Recovery) -> Ở môi trường On-premise thường được gọi là DC/DR 


***Kiến trúc cơ bản của VPC:***

![Kiến trúc VPC cơ bản](https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_02/VPC%20basic.png)

***Một số tính chất chính và khái niệm của VPC cần nhớ:***
- VPC nằm trong 1 **Region**, khi tạo VPC cần khai báo 1 lớp mạng **CIDR** IPPv4 (bắt buộc) và IPv6 (tùy chọn).
- **Limit** của AWS: -> **5 VPC** -> trên **1 AWS Region** -> trên **1 AWS account**
- Mục đích chính sử dụng VPC *trong thực tế* thường dùng để **phân tách** các môi trường, trong **software development life cycle**, thì nó sẽ chia ra nhiều môi trường như (Production/Dev/Test/Staging). -> Mỗi môi trường chúng ta có thể tạo ra 1 VPC









## **II. VPC Peering & Transit Gateway**
## **III. VPN & Direct Connect**
## **IV. Elastic Load Balancing**