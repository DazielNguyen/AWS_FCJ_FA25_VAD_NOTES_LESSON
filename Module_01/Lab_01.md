# **Module 01 - Lab 01**
## 1. Tạo tài khoản AWS: 
- Tạo tài khoản để truy cập và sử dụng các dịch vụ của AWS, mỗi tài khoản là -> root user
- Root user có toàn quyền với tài khoản AWS của mình, quyền hạn của root user không bị giới hạn. 
- Các điểm lưu ý khi tạo tài khoản: 
    + Cần một tài khoản email: 
    + Một tài khoản ngân hàng có thể dùng quốc tế như Visa. Mastercard để đăng kí được Free Tier của AWS. 
## 2. MFA cho tài khoản AWS. 
- MFA là gì? 
    + MFA (Multi-factor Authentication): Là một chức năng bảo mật có thể thông qua một ứng dụng, cung cấp mã số như OTP để xác thực mỗi lần đăng nhập để an toàn bảo mật
    + OTP(One-time Password): Gồm 6 chữ số và mỗi OTP chỉ có giá trị trong 60 giây.
    + Có thể cài thẳng lên trình duyệt như Microsoft Authentication. 
    + Có thể tham khảo thêm thiết bị MFA Cứng
- Lưu ý: Không nên xóa khóa MFA, khi mất tài khoản rất khó để lấy lại, phải cần đến đội ngũ AWS Support hỗ trợ
## 3. Tạo Admin Group và Admin User
Hướng dẫn tạo Admin Group và Admin User

- IAM Group: là một tool quản lý người dùng (IAM User), IAM Group -> Chứa nhiều IAM User, Các IAM User ở trong IAM Group đều hưởng chung quyền hạn mà IAM Group gán cho. 
- IAM User: là đơn vị người dùng của AWS, có thể tạo nhiều IAM User để cho phép người khác truy cập dài hạn vào tài nguyên AWS trong tài khoản root AWS.
## 4. Hỗ trợ xác thực tài khoản
- AWS Support là đơn vị cung cấp các dịch vụ hỗ trợ khách hàng.