# **Module 02 - Lab: 000003**

## Link: https://000003.awsstudygroup.com/vi/
- Khởi tạo VPC
    + Cấu hình tường lửa VPC 
    + Thực hành tạo 1 VPC
    + Cấu hình Site to Site VPN

### 1. Các bước thực hành
#### 1.1 Tạo VPC.
- Tạo môi trường mạng ảo riêng biệt trong AWS
- Thiết lập không gian địa chỉ IP cho VPC
- Cấu hình các tính năng DNS cơ bản

        Step 1: Truy cập VPC -> Your VPCs -> Nhấn Crete VPC
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
- Subnet là phân đoạn mạng con trong VPC
- Cho phép phân phối tài nguyên theo vùng sẵn sàng (AZ)
- Hỗ trợ phân loại mạng public và private

        Step 1: Truy cập VPC -> Subnets -> Nhấn Create Subnet
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

***Khi tạo Subnet***
- Sự khác biệt giữa các IP ở mỗi Subnet là khác nhau, và AZ,  nếu không để ý thì dễ bị nhầm lẫn

***Lưu ý về Availability Zone AWS sử dụng hai khái niệm:***

- **Availability Zone (AZ):** Tên hiển thị (ví dụ: ap-southeast-1a)
- **AZ ID:** Định danh thực tế của AZ AWS ánh xạ ngẫu nhiên AZ với AZ ID giữa các tài khoản để đảm bảo phân phối tài nguyên đồng đều.

#### 1.3 Tạo Internet Gateway
- Internet Gateway (IGW) là thành phần VPC cho phép kết nối internet
- Cung cấp điểm kết nối giữa VPC và internet
- Hỗ trợ giao tiếp hai chiều cho các tài nguyên trong VPC

        Step 1: Truy cập VPC -> Internet Gateway -> Nhấn Crete Internet Gateway
        |
        Step 2: Cấu hình Internet Gateway
        |       + Name tag: Nhập Internet Gateway
        |       + Click Create internet gateway
        Step 3: Kết nối với VPC 
        |       + Click Actions trong Internet Gateway
        |       + Chọn Attach to VPC
        |       + Chọn VPC ASG từ danh sách (VPC ID sẽ tự động điền)
        |       + Click Attach internet gateway.

***Xác nhận trạng thái sau khi gắn thành công:***

- State của Internet Gateway sẽ chuyển sang Attached
- IGW đã sẵn sàng định tuyến lưu lượng internet cho VPC

#### 1.4 Tạo Route Table
- Route Table là thành phần định tuyến lưu lượng mạng trong VPC
- Xác định đường đi cho các gói tin giữa các subnet và internet
- Cho phép kiểm soát luồng dữ liệu vào/ra VPC

        Step 1: Truy cập VPC -> Route tables -> Crete route table
        |
        Step 2: Cấu hình Route Table
        |       + Name: Nhập Route table-Public
        |       + VPC: Chọn VPC ASG (VPC ID sẽ tự động điền)
        |       + Click Create route table
        |
        Step 3: Cấu hình định tuyến -> Thêm route cho Internet Gateway
        |       + Click Actions -> Trong Route table
        |       + Chọn Edit routes
        |
        Step 4: Cấu hình route mới
        |       + Click Add route
        |       + Destination: Nhập 0.0.0.0/0 (đại diện cho internet)
        |       + Target: Chọn Internet Gateway và chọn IGW đã tạo
        |       + Click Save changes
        |
        Step 5: Liên kết với Subnet -> Thiết lập subnet associations
        |       + Chọn tab Subnet associations
        |       + Click Edit subnet associations
        |
        Step 6: Chọn các public subnet
        |       + Mở rộng cột Subnet ID để xem chi tiết
        |       + Chọn cả 2 public subnet đã tạo
        |       + Click Save associations

#### 1.5 Tạo Security Group
- Security Group là tường lửa ảo cho các tài nguyên AWS
- Hoạt động như danh sách kiểm soát truy cập (ACL) ở cấp instance
- Cho phép kiểm soát lưu lượng vào/ra theo port và protocol

***Tạo Security Group cho Public Subnet***

        Step 1: Truy cập VPC -> Security Group -> Crete Security Group
        |
        Step 2: Cấu hình Security Group
        |       + Security Group name: Nhập Public subnet - SG
        |       + Description: Nhập Allow SSH and Ping for servers in public subnet
        |       + VPC: Chọn VPC ASG
        |
        Step 3: Thiết lập Inbound Rules
        |       + Click Add rule
        |       + Rule 1:
        |               Type: SSH
        |               Source: My IP (địa chỉ IPv4 public của bạn)
        |       + Rule 2:
        |               Type: All ICMP - IPv4
        |               Source: Anywhere (cho phép ping từ mọi nơi)
        | 
        Step 4: Xác nhận Outbound Rules và tạo Security Group
        |
        Step 5: Kiểm tra Security Group đã tạo

***Tạo Security Group cho Public Subnet***


### 2. Các vấn đề gặp phải và cách giải quyết vấn đề.




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

