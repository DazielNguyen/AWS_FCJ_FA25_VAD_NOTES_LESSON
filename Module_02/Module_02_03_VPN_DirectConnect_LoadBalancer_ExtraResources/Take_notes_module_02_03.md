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
- **VPN Client to Site**: Cho phép một host truy cập tới tài nguyên trong VPC. 

- Chi phí dịch vụ khá cao, cho nên thường khi sử dụng Client to Site thì thường sẽ dùng qua dịch vụ **Third Party** của AWS cung cấp. 

- Khuyến khích sử dụng VPN Client to Site trong **AWS Market Place**.

### 4. AWS Direct Connect

- **AWS Direct Connect** là dịch vụ cho phép tạo kết nối riêng tư từ trung tâm dữ liệu truyền thống tới AWS.

- Độ trễ khoảng **20ms - 30ms**. 

- **AWS Direct Connect** ở Việt Nam hiện tại sẽ thông qua AWS Direct Connect partners và hoạt động dưới dạng ***Hosted Connections***. (Nếu trực tiếp tới AWS thì là ***Dedicated Connections***)

    + Băng thông Direct Connect có thể thay đổi lên/xuống tùy nhu cầu.   

- Trong thực tế khi đi làm Cloud Engineer thì mình không bao giờ được cấu hình **Direct Connect** này, hầu hết sẽ có đội ngũ Partner sẽ làm thay.

- **Direct Connect** là đường kết nối ở mức thấp không có thực hiện mã hóa dữ liệu, sau khi đấu nối thực hiện Direct Connect xong thì chúng ta phải sử dụng thêm VPN Site to Site.

## **IV. Elastic Load Balancing**

### 1. Tổng quan về Elastic Load Balancing.
- **Elastic Load Balancing** (ELB) là một dịch vụ cân bằng tải được quản lí bởi AWS, có chức năng phân phối lưu lượng cho nhiều EC2 Instance hoặc Container.

- Sử dụng giao thức **HTTP, HTTPS, TCP và SSL (TCP bảo mật).**

- Có thể nằm ở -> **Public** hoặc **Private** Subnet.

- Mỗi ELB sẽ được cấp tên DNS và kết nối thông qua DNS. Chỉ có Network Load Balancer hỗ trợ gán IP tĩnh. 

- ELB không kết nối qua địa chỉ IP, chỉ kết nối qua DNS trừ ELB - Network Load Balancer.

- ELB có tính năng **health check**, không gửi lưu lượng đến các Instance không đạt **health check**.

- Bao gồm 4 loại: 
    + **Application Load Balancer**
    + **Network Load Balancer** -> Hỗ trợ gán IP tĩnh
    + **Classic Load Balancer** -> Giá cao
    + **Gateway Load Balancer** -> Mới nhất

- **Sticky session (session affinity):** Tính năng cho phép các kết nối được gán vào một target nhất định. Việc này đảm bảo các requests từ một user trong một session sẽ được gửi tới cùng một target. 

- **Sticky session** là cần thiết trong trường hợp các máy chủ ứng dụng lưu trữ thông tin trạng thái của người dùng tại server. 

    + Hoạt động trên **Network Load Balancer, Application Load Balancer, Classic Load Balancer.**

- ELB cung cấp tính năng lưu trữ logs truy cập **(access logs)** chugns ta có thể sử dụng access logs để phân tích truy cập, trouble shoot. Logs truy cập sẽ được lưu trữ vào một dịch vụ lưu trữ đối tượng là **Amazon S3** (Simple Storage Service).


### 2. ELB - Application Load Balancer

### 3. ELB - Network Load Balancer
### 4. ELB - Classic Load Balancer
### 5. ELB - Gateway Load Balancer

