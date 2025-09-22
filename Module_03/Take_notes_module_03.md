# **Module 3 - Dịch vụ Compute VM trên AWS**
## **I. Amazon Elastic Compute Cloud (EC2)**
### 1. Giới thiệu về EC2
- **EC2** giống máy chủ ảo hoặc máy chủ vật lí truyền thống
- **EC2** có khả năng *khởi tạo nhanh, khả năng co giãn tài nguyên mạnh mẽ, linh hoạt.*
- **EC2** có thể hỗ trợ các workload như lưu trữ web, ứng dụng, cơ sở dữ liệu, dịch vụ xác thực và bất cứ công việc nào khác mà máy chủ thông thường có thể đáp ứng.

### 2. EC2 - Instance Type

***Link tham khảo:***
(https://aws.amazon.com/ec2/instance-types/?ncl=h_ls)

- Cấu hình của Amazon EC2 không được tùy chọn tùy ý, mà lựa chọn cấu hình thông qua việc
lựa chọn các EC2 Instance type. 

***Sơ đồ kiến trúc của máy chủ ảo EC2***

![Module 3.1 EC2 Architec](https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_03/Image_module_03/Module%203.1%20EC2%20Architec.png)
- Instance type quyết định các yếu tố :
    + CPU (Intel / AMD / ARM ( Graviton 1/ 2/3) / GPU)
    + Memory
    + Network
    + Storage

### 3. EC2 - AMI /Backup /Key Pair
- Sử dụng **AMI (Amazon Machine Image)** có thể **provision** ra -> **một hoặc nhiều EC2 Instances** cùng lúc. 
    + AMI có sẵn của AWS, trên AWS Market Place và custom AMI tự tạo từ EC2 Instances.
- **AMI** bao gồm:
    + Root OS volumes 
    + Quyền sử dụng **AMI** quy định tài khoản AWS được sử dụng 
    + **Mapping EBS volume** sẽ được tạo và gán vào EC2 Instances.
- EC2 instance có thể được **backup** bằng cách tạo **snapshot**.

***Kiến trúc EC2 AMI*** 

![Module 3.3 EC2 AMI](https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_03/Image_module_03/Module%203.3%20EC2%20AMI%20Architec.png)

- **Key pair** (public key và private key) dùng để mã hóa thông tin đăng nhập cho EC2 Instance.

***Kiến trúc EC2 Key Pair*** 

![Module 3.3 EC2 Key Pair](https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/Module_03/Image_module_03/Module%203.3%20EC2%20Key%20Pair.png)

### 4. EC2 - Elastic Block Store 

## **II. Amazon Lighsail**
## **III. Amazon EFS/FSX**
## **IV. AWS Application Migration Service (MGN)**
