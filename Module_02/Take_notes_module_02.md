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

![Kiến trúc VPC cơ bản](https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_02/1.%20VPC%20basic.png)

***Một số tính chất chính và khái niệm của VPC cần nhớ:***
- VPC nằm trong 1 **Region**, khi tạo VPC cần khai báo 1 lớp mạng **CIDR** IPPv4 (bắt buộc) và IPv6 (tùy chọn).
- **Limit** của AWS: -> **5 VPC** -> trên **1 AWS Region** -> trên **1 AWS account**
- Mục đích chính sử dụng VPC *trong thực tế* thường dùng để **phân tách** các môi trường, trong **software development life cycle**, thì nó sẽ chia ra nhiều môi trường như **(Production/Dev/Test/Staging)**. -> Mỗi môi trường chúng ta có thể tạo ra 1 VPC
- Lưu ý: **Isolate** (Cô lập) giữa các **VPC** chỉ là mức các **Network**. Nếu như chúng ta có yêu cầu của người dùng
    + Vd: User không thể nhìn thấy một tài nguyên nguyên cụ thể thì cần tách nhiều AWS Account, nhiều VPC không giải quyết vấn đề này.

***Kiến trúc phân tách các môi trường VPC riêng biệt:***

![Kiến trúc VPC phân tách](https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_02/1.%20VPC%20ph%C3%A2n%20t%C3%A1ch.png)

### 1.1 VPC - Subnets
- **Subnets** được gọi là mạng con, Amazon VPC cho phép -> tạo nhiều mạng ảo và chia các mạng ảo này thành các mạng con **(Subnet)**.
- VPC Subnet sẽ nằm trong 1 AZ (Availability Zone) cụ thể.
- Khi tạo Subnet, chúng ta chỉ định CIDR cho mạng con đó và đây là một **tập hợp con của khối VPC CIDR**
    + Vd: Cho mỗi **Quận** trong thành phố Hồ Chí Minh được gọi là mỗi **VPC**, thì trong mỗi **Quận** thì sẽ gồm nhiều **Phường** khác nhau thì đó được gọi là **Subnets** của từng **Quận** đó. => Đó còn được gọi là **tập hợp con của khối VPC CIDR**
- Trong mỗi Subnet, AWS sẽ giữ **5 địa chỉ IP**. Ví dụ nếu Subnet có CIDR là 10.10.1.0/24
    + Địa chỉ network (10.10.1.0)
    + Địa chỉ broadcast (10.10.1.255)
    + Địa chỉ cho bộ định tuyến (10.10.1.1)
    + Địa chỉ cho DNS (10.10.1.2)
    + Địa chỉ cho tính toán tương lai (10.10.1.3)

- Phân loại VPC - Subnets
    + Public subnet
    + Private subnet 

    => Bản chất của hai cái này là như nhau, tuy nhiên có quy ước riêng.
    + Nếu đặt tên **"Public Subnet"**, cấu hình như **Public Subnet**, thì nếu đặt các máy chủ ảo vào vùng **Public** này thì nó sẽ được cho phép đi ra **ngoài Internet**
    + Private thì ngược lại -> Không được đưa ra ngoài Internet.
***Kiến trúc cấu hình VPC khi đặt Subnet vào:***

![Kiến trúc VPC - Subnets](https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_02/1.1%20VPC%20subnets.png)
- Mỗi Subnets riêng biệt chỉ nằm trong 1 AZ riêng biệt.

***Làm sao để chúng ta tạo một cái Public Subnet, khi nào chúng ta gọi nó là Public Subnet và khi nào chúng ta gọi đó là Private Subnet? Phần 1.2 sẽ giải thích.*** 

### 1.2 VPC - Route Table
- Route Table (Bảng định tuyến), tập hợp các Route để xác định đường đi bên trong mạng của mình.
- Khi tạo VPC, AWS sẽ tạo một -> **Default Route table**, Default Route table không thể bị xóa bà chỉ chứa **1 Route duy nhất** là Route cho phép tất cả các Subnet trong VPC **liên lạc với nhau**.

***Hình ảnh minh họa***

![Minh họa Default Route table](https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_02/1.2%20Default%20Route%20table.jpg)

- Route table sẽ được gán vào Subnet. 
- Để tạo được Public Subnet, Subnets mà bên trong máy chủ có thể đi ra ngoài Internet, thì chúng ta phải tạo Custom Route table (Bảng định tuyến tùy chỉnh), tuy nhiên không thể xóa Default Route (VPC CIDR - Local), chỉ được thêm subnet chứ không xóa được Default Route. 
### 1.3 VPC - Elastic Network Interface (ENI)
- **Elastics Network Interface (ENI)** là một card ảo, chúng ta có thể chuyển sang các EC2 Instance khác.
- Mỗi máy chủ ảo của chúng ta, khi bật máy chủ lên chúng ta tạo máy chủ ở trong VPC, thì máy chủ của chúng ta sẽ được **cấp một địa chỉ IP**, các địa chỉ IP này không được gán vào tài nguyên máy chủ, mà nó gán vào các card mạng ảo (Elastic Network Interface).
- Tạo ra một máy chủ ảo thì đồng nghĩa chúng ta tạo ra một -> Elastics Network Interface
- Nhưng cái máy chủ này có thể linh hoạt gắn vào những các mạng ảo khác, khá là thông dụng. 
- Giải thích ví dụ dễ hiểu hơn: 
    + Máy chủ ảo: Căn nhà của bạn 
    + Card ảo: Số nhà của bạn. 
    + Thì số nhà của bạn có thể tháo hoặc thay thế bằng một cái số nhà khác, hoặc cái số nhà cũ của bạn sẽ chuyển qua căn nhà khác. 
- Khi chuyển sang một máy chủ mới, thì một card mạng ảo sẽ vẫn **duy trì**.
    + Địa chỉ IP Private
    + Địa chỉ Elastic IP address -> Là một địa chỉ public
    + Địa chỉ MAC -> Là địa chỉ vật lí
- **Elastic IP address (EIP)** là một địa chỉ public IPv4 tĩnh, có thể liên kết với một Elastic Networl Interface. 
    + Khi không sử dụng, sẽ bị charge phí. (Để tránh lãng phí).

***Kiến trúc VPC nâng cao***

![VPC nâng cao gồm EC2](https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_02/1.3%20VPC%20n%C3%A2ng%20cao%20g%E1%BB%93m%20EC2.png)

***Giải thích ảnh trên: ***
- Trong này chúng ta tạo ra một máy chủ EC2 -> Máy chủ EC2 này sẽ được gán Elastic Network Interface -> ... Ở dưới
- VPC này sẽ cấp: 
    + VPC Private IP
    + Địa chỉ Private IPv4 trong subnet CIDR (Không gian mạng)
    + Giả sử gán cho nó 1 cái địa chỉ IP Private 10.10.1.6
- Để cái EC2 này đi ra ngoài Internet thì nó sẽ được gán vào một cái IP Public
    + Thì nó gán Elastic IP address 
    + Nó là địa chỉ Public IPv4 tĩnh, không thay đổi khi máy ảo restart
    + Địa chỉ gán vào là 134.23.42.15
## **II. VPC Peering & Transit Gateway**
## **III. VPN & Direct Connect**
## **IV. Elastic Load Balancing**