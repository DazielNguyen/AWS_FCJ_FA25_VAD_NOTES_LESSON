# **Module 2 - Các dịch vụ mạng trên AWS**
## **III. VPN & Direct Connect**
### 1. Giới thiệu về VPN & và Direct Connet

- Đây là tính năng dùng để kết nối giữa môi trường on-premises và môi trường trên Cloud. Hay người ta thường hay gọi là môi trường Hybrid. 

- Hybrid ở đây là gì? Là có nghĩa rằng chúng ta chạy một phần dịch vụ ở local hay được gọi là on-premises và một phần dịch vụ trên chạy trên điện toán đám mây ở trên AWS. 
### 2. VPN Site to Site

- **VPN Site to Site** dùng trong mô hình hybrid để thiết lập kết nối liên tục giữa môi trường trung tâm dữ liệu truyền thống tới môi trường VPC của AWS. 

- Việc thiết lập kết nối sẽ cần 2 đầu endpoint ở phía AWS và phía khách hàng: 

    + **Virtual Private Gateway** Được quản lí hoàn toàn AWS (chia 2 endpoint ở 2 đầu 2 AZ)

    + **Customer Gateway**: Đầu endpoint phía khách hàng, có thể là thiết bị phần cứng hoặc software appliance. 

***Link hướng dẫn tất cả những thiết bị, software application...***: [https://docs.aws.amazon.com/vpn/latest/s2svpn/your-cgw.html]

### 3. VPN Client to Site
-
-
-
### 4. AWS Direct Connect
-
-
-

## **IV. Elastic Load Balancing**
### 1. Tổng quan về Elastic Load Balancing
### 2. ELB - Application Load Balancer
### 3. ELB - Network Load Balancer
### 4. ELB - Classic Load Balancer
### 5. ELB - Gateway Load Balancer

