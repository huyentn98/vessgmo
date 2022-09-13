# Quy trình nghiệp vụ

Khách hàng đăng nhập tài khoản trên ứng dụng CloudERP bằng tài khoản theo công ty đã cung cấp để thực hiện xem, cập nhật thông tin cá nhân, xem thông báo, tin tức và các nội dung khác.

**Quy trình**

![](picture/PIC_DW_Mobile_DangNhap-QuyTrinh.jpg)

**Các luồng quy trình**

* Đăng nhập. Chi tiết nghiệp vụ <u>[tại đây](#ang-nhap)</u>.

**Mô tả nghiệp vụ**

Khi người sử dụng muốn đăng nhập vào ứng dụng CloudERP thì quy trình thực hiện như sau:

1. Mở app trên thiết bị 

2. Thực hiện nhập domain hoặc quét QR code domain để cung cấp thông tin 

3. Thực hiện đăng nhập bằng thông tin tài khoản mật khẩu đã được công ty cung cấp

4. Nhập mã OTP được gửi đến để xác nhận và đăng nhập thành công.


**Luồng chức năng chính**


* Đăng nhập. Chi tiết nghiệp vụ <u>[tại đây](#ang-nhap)</u>.


**Video hướng dẫn**


## **Đăng nhập**

Khách hàng đăng nhập tài khoản trên ứng dụng CloudERP bằng tài khoản theo công ty đã cung cấp

**Đối tượng thực hiện:** Người dùng

Điều kiện trước: Công ty của người dùng đã được đăng ký trên hệ thống, người dùng đã có tài khoản.
Ngoài ra, hệ thống cần cài đặt các chức năng: Nhân viên, Tài liệu.

Điều kiện sau: Đăng nhập thành công và vào màn hình Danh sách ứng dụng hoặc onbroading

1. Mở app trên thiết bị 

2. Thực hiện nhập domain hoặc quét QR code domain để cung cấp thông tin: 

    ![](picture/PIC_DW_Mobile_DangNhap-Domain.jpg)
    
    * Trường hợp ứng dụng kiểm tra chưa có domain mới thực hiện nhập domain hoặc quét QR code domain
    
        * Nếu người dùng chọn nhập mã domain, sẽ khai báo thông tin Đường dẫn của công ty 
        
        * Nếu người dùng chọn quét QR code domain, ứng dụng sẽ hiển thị màn hình quét QR code domain
        
    ![](picture/PIC_DW_Mobile_DangNhap-QRCode.jpg)
    
    * Trường hợp ứng dụng kiểm tra đã có domain, người dùng sẽ thực hiện đăng nhập luôn
    
3. Nhấn **Tiếp tục**, ứng dụng sẽ thực hiện kiểm tra xem thông tin domain có tồn tại hay không.
    
    * Nếu thông tin domain chính xác, người dùng sẽ tiến hành đăng nhập 
    
    * Nếu thông tin domain không chính xác, người dùng sẽ tiếp tục nhập thông tin domain 
   
4. Thực hiện đăng nhập bằng thông tin tài khoản mật khẩu đã được công ty cung cấp

    ![](picture/PIC_DW_Mobile_DangNhap-DangNhap.jpg)

    * Khai báo thông tin Tài khoản và Mật khẩu đã được công ty cung cấp 
    
    * Chọn **Nhớ mật khẩu** để lưu mật khẩu cho lần đăng nhập tiếp theo 
    
    * Nhấn **Nhập lại tên miền** để nhập lại domain 
    
    * Nhấn **Đăng nhập** hoặc chọn đăng nhập bằng vân tay 
        
        * Nếu thông tin đăng nhập đúng, hệ thống gửi SMS OTP vào số điện thoại của người dùng
    
        * Nếu thông tin đăng nhập không chính xác, người dùng sẽ thực hiện lại việc đăng nhập

5. Tại màn hình nhập mã OTP, nhấn **Gửi lại** nếu không nhận được mã OTP hoặc mã OTP bị quá thời hạn cho phép

6. Người dùng nhập mã OTP được gửi đến

![](picture/PIC_DW_Mobile_DangNhap-NhapOTP.jpg)

7. Nhấn **Xác nhận** 

    * Nếu mã OTP chính xác, người dùng đăng nhập thành công
    
    * Nếu mã OTP không chính xác, người dùng nhập lại mã OTP
