# **Module 02 - Lab: 000003**

## Link: https://000003.awsstudygroup.com/vi/
- Khởi tạo VPC
    + Cấu hình tường lửa VPC 
    + Thực hành tạo 1 VPC
    + Cấu hình Site to Site VPN

### 1. Các bước thực hành
#### 1.1 Tạo VPC.
    Step 1: Tìm VPC -> Your VPCs -> Nhấn Crete VPC
    |
    Step 2: Cấu hình VPC
            + Resources: Chọn VPC only
            + Name tag: Nhập ASG
            + IPv4 CIDR: Nhập 10.10.0.0/16
    |
    Step 3: Kích hoạt DNS cho VPC
            + Chọn Edit VPC settings
            + Mở tab DNS settings
            + Bật Enable DNS resolution
            + Bật Enable DNS hostnames
            + Bật Enable Network Address Usage metrics
            + Lưu thay đổi
    
#### 1.2 Tạo Subnets.
    Step 1: Tìm VPC -> Subnets -> Nhấn Create Subnet
    |
    Step 2: Chọn VPC ASG đã tạo trước đó. 
    |
    Step 3: Cấu hình Subnet đầu tiên - Public Subnet 1
    |       + Subnet name: Nhập Public Subnet 1
    |       + Availability Zone: Chọn ap-southeast-1a
    |       + IPv4 Subnet CIDR: Nhập 10.10.1.0/24
    |       + Click Create subnet
    |
    Step 4: Tạo Public Subnet 2
    |       + Subnet name: Nhập Public Subnet 2
    |       + Availability Zone: Chọn ap-southeast-1b
    |       + IPv4 Subnet CIDR: Nhập 10.10.2.0/24
    |       + Click Create subnet
    |
    Step 5: Tạo Private Subnet 1
    |       + Subnet name: Nhập Private Subnet 1
    |       + Availability Zone: Chọn ap-southeast-1a
    |       + IPv4 Subnet CIDR: Nhập 10.10.3.0/24
    |       + Click Create subnet
    |
    Step 6: Tạo Private Subnet 2
    |       + Subnet name: Nhập Private Subnet 2
    |       + Availability Zone: Chọn ap-southeast-1b
    |       + IPv4 Subnet CIDR: Nhập 10.10.4.0/24
    |       + Click Create subnet
    |
    Step 7: Cấu hình Auto-assign Public IP -> Mục đích: Cho phép tự động cấp phát địa chỉ IP công cộng cho các instance trong public subnet.
    |       + Chọn subnet từ danh sách -> Set up từng cái Subnet theo các bước dưới
    |       + Click Actions
    |       + Chọn Edit subnet settings
    |       + Bật Enable auto-assign public IPv4 address
    |       + Click Save

#### 1.3 Tạo Internet Gateway

### 2. Điểm cần lưu ý: 
- Sự khác biệt giữa các IP ở mỗi Subnet là khác nhau, và AZ,  nếu không để ý thì dễ bị nhầm lẫn

***Lưu ý về Availability Zone AWS sử dụng hai khái niệm:***

- **Availability Zone (AZ):** Tên hiển thị (ví dụ: ap-southeast-1a)
- **AZ ID:** Định danh thực tế của AZ AWS ánh xạ ngẫu nhiên AZ với AZ ID giữa các tài khoản để đảm bảo phân phối tài nguyên đồng đều.

### 3. Các vấn đề gặp phải và cách giải quyết vấn đề.




# **Module 02 - Lab: 000058**
## Link: https://000058.awsstudygroup.com/vi/
 - System Manager - Session Manager 
    + Tạo kết nối đến máy chủ EC2
    + Quản lí sessioin logs
    + Sử tính năng Port Forwarding
### 1. Các bước thực hành
### 2. Điểm cần lưu ý: 
### 3. Các vấn đề gặp phải và cách giải quyết vấn đề.




# **Module 02 - Lab: 000019**
## Link: https://0000019.awsstudygroup.com/vi/
### 1. Các bước thực hành
### 2. Điểm cần lưu ý: 
### 3. Các vấn đề gặp phải và cách giải quyết vấn đề.
 - Thiết lập VPC Peering
    + Cập nhật Network ACL 
    + Tạo kết nối Peering 
    + Cấu hình Route tables 
    + Kích hoạt Cross-Peer DNS. 

# **Module 02 - Lab: 000020**
## Link: https://000020.awsstudygroup.com/vi/
### 1. Các bước thực hành
### 2. Điểm cần lưu ý: 
### 3. Các vấn đề gặp phải và cách giải quyết vấn đề.
 - Thiết lập Transit Gateway
    + Thiết lập hạ tầng
    + Tạo Transit Gateway -> Nối nhiều VPC lại với nhau
    + Transit Gateway Attachments
    + Tạo Route Table cho TGW
    + Thêm Gateway vào Route Tables & Kiểm tra kết quả

# **Module 02 - Lab: 000010**
## Link: https://000010.awsstudygroup.com/vi/
### 1. Các bước thực hành
### 2. Điểm cần lưu ý: 
### 3. Các vấn đề gặp phải và cách giải quyết vấn đề.
 - Hybrid DNS
    + Thiết lập Hybrid DNS
    + Tạo Outbound Endpoint
    + Tạo Route 53 Resolver Rule
    + Tạo Inbound Endpoint.