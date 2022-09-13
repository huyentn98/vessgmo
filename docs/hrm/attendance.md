# Giới thiệu chức năng Chấm công - Đăng ký công

Chấm công, Đăng ký công là 2 phân hệ con mở rộng của phân hệ Nhân sự. Đây là nơi lưu trữ, tổng hợp tất cả dữ liệu đăng ký chấm công và chấm công của các nhân viên trong công ty. Hai phân hệ cung cấp cái nhìn toàn cảnh, bao quát và trực quan về thông tin chấm công của nhân viên; từ đó giúp các công ty/ doanh nghiệp quản lý chấm công một cách hiệu quả và chuẩn xác.

Để sử dụng được các nghiệp vụ này, người dùng cần cài đặt ứng dụng Chấm công - Đăng ký công; ngoài ra nếu Khách hàng có hệ thống chấm công camera AI thì cài thêm ứng dụng **Camera AI** hỗ trợ sử dụng dữ liệu chấm công từ camera để tổng hợp công. 

Phân hệ Chấm công - Đăng ký công đáp ứng được các yêu cầu nghiệp vụ như:

- Quản lý hiệu quả kế hoạch nghỉ phép cho tất cả nhân viên bằng cách tự động tính toán số ngày nghỉ phép theo Luật lao động hiện hành.
- Quản lý ngày nghỉ phép, làm thêm giờ của nhân viên linh hoạt.
- Công cụ báo cáo, thống đơn giản và trực quan
- Tự động đồng bộ, chấm công cho nhân viên trên hệ thống dựa theo đơn đăng ký nghỉ, đăng ký làm thêm giờ.
- Hỗ trợ tổng hợp công dựa trên dữ liệu lịch sử vào/ ra, import công từ file excel,...

## Mô tả nghiệp vụ

Phân hệ Chấm công - Đăng ký công cho phép người dùng thực hiện đăng ký chấm công - tổng hợp bảng công theo quy trình như sau

![image-20210930154213758](images/image-20210930154213758.png)

Các luồng quy trình:

- Thiết lập và khai báo ban đầu. Xem hướng dẫn chi tiết [Tại đây](#Thiết lập và khai báo ban đầu)
- Thiết lập kế hoạch nghỉ phép cho nhân viên. Xem hướng dẫn chi tiết [Tại đây](#Thiết lập kế hoạch nghỉ phép cho nhân viên)

- Nhân viên đăng ký công. Xem hướng dẫn chi tiết [Tại đây](#Đăng ký chấm công)

- Quản lý trực tiếp của nhân viên phê duyệt/ từ chối đăng ký công. Xem hướng dẫn chi tiết [Tại đây](#Phê duyệt/ Từ chối đăng ký công)

- Cán bộ chấm công tổng hợp công. Xem hướng dẫn chi tiết [Tại đây](#Tổng hợp công)


## Thiết lập và khai báo ban đầu

Việc thiết lập và khai báo ban đầu của phân hệ chấm công -  đăng ký công nên được thực hiện ngay khi lần đầu cài đặt hệ thống, giúp khởi tạo dữ liệu và bắt đầu sử dụng nghiệp vụ chấm công. 

### Thiết lập phân quyền người dùng

***Đối tượng thực hiện: Người quản trị hệ thống***

Để đảm bảo tất cả người dùng đăng nhập vào miền ứng dụng của doanh nghiệp đảm nhận đúng vai trò, quản trị viên hệ thống cần thiết lập phân quyền phù hợp. Cụ thể như sau:

  - Đối với phân hệ Chấm công, gồm 4 mức phân quyền:
    - Không chọn gì (bỏ trống): Người dùng không có phân sự gì với phân hệ chấm công
    - Chọn "Điểm danh thủ công": Người dùng chỉ có quyền điểm danh thủ công trên mobile hoặc máy chấm công. Có thể hiểu phân quyền này cho nhân viên bình thường trong công ty.
    - Chọn "Cán bộ": Người dùng là cán bộ chấm công, có quyền tổng hợp và theo dõi báo cáo công của tất cả các nhân viên
    - Chọn "Người quản trị": Người quản trị phân hệ Chấm công, có quyền *Tổng hợp công* và cấu hình thiết lập mục chấm công Camera AI (nếu đã cài đặt) cũng như xem dữ liệu chấm công qua camera.

  - Đối với phân hệ Đăng ký công, phân hệ này dùng để nhân viên đăng ký, quản lý trực tiếp của nhân viên phê duyệt/ từ chối đăng ký, cán bộ nhân sự phê duyệt/ từ chối và theo dõi báo cáo đăng ký công. Có 3 mức phân quyền cho phân hệ này như sau:
    - Không chọn gì (bỏ trống): Người dùng nội bộ (nhân viên) có thể đăng ký công (đăng ký nghỉ/OT)
    - Chọn "Người phụ trách": Thiết lập cho người dùng là quản lý của nhân viên, có quyền đăng ký công và chỉ phê duyệt/ từ chối đơn đăng ký công của nhân viên mình phụ trách, quản lý.
    - Chọn "Quản lý công": Thiết lập cho người dùng là cán bộ duyệt công, có quyền đăng ký công, xem và phê duyệt/ từ chối tất cả các đơn đăng ký công, KHÔNG có quyền tự phê duyệt/ từ chối đơn đăng ký của cá nhân người dùng đó.
    - Chọn "Người quản trị": Thiết lập cho người quản trị phân hệ Đăng ký công, có quyền xem và phê duyệt tất cả các đơn đăng ký công bao gồm cả đơn của bản thân. 

### Thiết lập ký hiệu công

***Đối tượng thực hiện: Người quản trị hệ thống hoặc người quản trị phân hệ Chấm công*** 

Ký hiệu công (hay còn gọi là "Loại ngày làm"), là danh sách các ký hiệu hiển thị lên bảng chấm công tương ứng cho các loại ngày làm, ví dụ như công đi làm (X), công nghỉ phép (P), công làm tăng ca (OT),...

Dữ liệu ký hiệu công (loại ngày làm) này được sử dụng để thiết lập các loại đăng ký công thì thiết lập tương ứng. 

Hiện tại, khi người dùng cài đặt thành công phân hệ Chấm công, hệ thống đã tạo sẵn bộ dữ liệu các ký hiệu công phổ biến, thường dùng cho tất cả các doanh nghiệp. Người dùng kiểm tra dữ liệu trên hệ thống và điều chỉnh dữ liệu phù hợp bằng cách thao tác như sau:

- Vào menu **Chấm công** >> Chọn **Cấu hình** >> Ký hiệu công. Hệ thống hiển thị màn hình sau

![image-20210930181238919](images/image-20210930181238919.png)

*Lưu ý: Các dữ liệu có sẵn này không được phép xoá. Người dùng có thể tạo thêm ký hiệu công mới bằng cách bấm **Tạo** và nhập dữ liệu phù hợp, sau đó thực hiện **Lưu**.*

### Thiết lập hình thức chấm công

***Đối tượng thực hiện: Người quản trị phân hệ Chấm công và có quyền quản trị ở các phân hệ khác trong mục thiết lập***

***Mục đích:*** Lựa chọn hình thức chấm công/ tổng hợp công cho công ty, thiết lập thời gian cho phép đi muộn/ về sớm (nếu có)

***Thực hiện trên hệ thống:*** Người dùng vào menu **Chấm công** >> **Cấu hình** >> **Thiết lập**, giao diện hiển thị 

![image-20211026151256067](images/image-20211026151256067.png)

- Nếu người dùng không tích chọn vào "Chấm công dựa vào lịch sử vào - ra": hệ thống sẽ hiểu là tổng hợp công dựa trên các đơn đăng ký nghỉ/ OT ; còn lại sẽ tự động chấm công X: công đi làm

- Nếu người dùng tích chọn vào "Chấm công dựa vào lịch sử vào - ra", nhập số phút cho phép nhân viên đi muộn/ về sớm: hệ thống hiểu là tổng hợp công dựa trên các đơn đăng ký nghỉ/ OT; thời gian còn lại nhân viên được chấm công (hiển thị trên bảng tổng hợp công) chỉ khi nhân viên đó có dữ liệu vào/ ra trong ngày. 

### Thiết lập loại đăng ký công

***Đối tượng thực hiện: Người quản lý công hoặc Người quản trị phân hệ Đăng ký công.*** 

***Mục đích:*** Thiết lập các loại đăng ký công tương ứng với các ký hiệu công, để khi nhân viên đăng ký công thuộc loại đăng ký công nào thì khi cán bộ chấm công tổng hợp công, hệ thống tự động hiển thị đúng loại ký hiệu công tương ứng lên bảng công.

***Thực hiện trên hệ thống:*** Người dùng vào menu **Đăng ký công** >> Chọn **Cấu hình** >> **Loại đăng ký**. Hệ thống hiển thị màn hình sau

![image-20210930184045094](images/image-20210930184045094.png)

Ngay khi người dùng cài đặt thành công phân hệ "Đăng ký công", hệ thống tự động tạo sẵn bộ dữ liệu các loại đăng ký với bộ ký hiệu công khởi tạo. Người dùng có thể thêm loại đăng ký mới bằng cách bấm nút **Tạo**, nhập các thông tin yêu cầu, bấm **Lưu** để hoàn tất.

![image-20210930184609554](images/image-20210930184609554.png)

***Lưu ý 1:** Các thông tin cần nhập*

- Loại ngày làm: Chọn 1 trong số các loại ngày làm đã khai báo ở bước **Thiết lập đăng ký công**
- Ngày xác nhận: Nhập khoảng thời gian cho phép đăng ký công với loại đăng ký này
- Công trong: Chọn Ngày/Nửa ngày/Giờ tương ứng với đơn vị thời gian nghỉ cho loại đăng ký này. Ví dụ như hình trên, thì với loại đăng ký công là "Nghỉ dưỡng năm 2021", nhân viên được phép đăng ký nghỉ theo ngày (1 ngày, 2 ngày, ...)
- Đăng ký phân bổ: Tích chọn chế độ đăng ký phân bổ phù hợp, cụ thể
  - Không giới hạn: Tức là với phân bổ kế hoạch đăng ký công thuộc loại đăng ký này thì không cần người phê duyệt. Có thể hiểu là nhân viên có thể tuỳ ý đăng ký kế hoạch cho loại đăng ký này.
  - Thiết lập bởi người quản lý công: Tức là người quản lý công mới có quyền cấp phát phân bổ thời gian cho loại đăng ký công này
- Đăng ký công: Tích chọn chế độ phê duyệt đăng ký công phù hợp, cụ thể
  - Không phê duyệt: Tức là các đơn đăng ký công thuộc loại đăng ký công này thì không cần phê duyệt, đơn có hiệu lực được duyệt ngay tại thời điểm nhân viên đăng ký
  - Người quản lý công: Tức là đơn đăng ký công thuộc loại này phải được phê duyệt bởi người quản lý công mới có tính hiệu lực
  - Quản lý nhân viên: Tức là đơn đăng ký công thuộc loại này phải được phê duyệt bởi quản lý cấp trên trực tiếp của nhân viên
  - Quản lý nhân viên và quản lý công: Tức là đơn đăng ký công thuộc loại này phải được phê duyệt lần 1 bởi quản lý nhân viên, và phê duyệt lần 2 bởi người quản lý công mới có hiệu lực.

***Lưu ý 2:** Các loại đăng ký có sẵn trên hệ thống thì không cho phép người dùng xoá.*  

### Thiết lập loại hợp đồng tính phép

***Đối tượng thực hiện: Người quản lý công hoặc người quản trị phân hệ Đăng ký công*** 

- Theo quy định của Luật lao động nói chung và quy định của công ty nói riêng, để tính và quản lý số ngày phép cho nhân viên thì cần xác định được danh sách hợp đồng được hưởng phép và danh sách loại hợp đồng được tính thời gian là thời gian làm việc trong năm.

- Các bước thực hiện trên hệ thống: Người dùng vào menu **Đăng ký công** >> Chọn **Cấu hình** >> Chọn **Thiết lập**

![image-20211001102029639](images/image-20211001102029639.png)

Người dùng điều chỉnh dữ liệu phù hợp với doanh nghiệp, bấm **Lưu** để hoàn tất.

### Thiết lập loại hoạt động

***Đối tượng thực hiện: Người quản lý công hoặc người quản trị phân hệ Đăng ký công***

- Tại bước này, người dùng thiết lập các hoạt động để định nghĩa rằng: loại hoạt động này bắt buộc phải thực hiện hành động gì? Người mặc định thực hiện là ai? Hoạt động này có là tiền điều kiện có hoạt động nào khác không? Sau hoạt động này thì nên thực hiện hoạt động nào? Thời gian dự kiến phải hoàn thành hoạt động trong bao lâu?

- Việc thiết lập này chính là định nghĩa cho các thông báo cảnh báo khi quá thời gian thực hiện cho phép.

- Các bước thực hiện trên hệ thống: 

  - Người dùng vào menu **Đăng ký công** >> Chọn **Cấu hình** >> **Hoạt động**. Hệ thống hiển thị lên màn hình danh sách các hoạt động được định nghĩa sẵn. 
- Người dùng có thể thiết lập thêm hoạt động bằng cách bấm nút **Tạo**, nhập các thông tin yêu cầu và bấm **Lưu** để hoàn tất.
  

*Lưu ý: Các bản ghi hệ thống tạo sẵn thì không được phép xoá.*

### Cấu hình chấm công Camera AI

***Đối tượng thực hiện: Người quản trị phân hệ Chấm công***

Quy trình: Kích hoạt tích hợp >> Tạo bộ dữ liệu ảnh nhận diện cho tất cả nhân viên

- **Kích hoạt tích hợp**: Phân hệ Chấm công vESS hỗ trợ tự động cấu hình tích hợp với Camera AI, sau khi cài đặt ứng dụng người quản trị cần kích hoạt việc cấu hình này bằng cách: Vào menu **Chấm công** >> **Camera AI** >> **Cấu hình**, giao diện hiển thị như hình sau

![image-20211026142048376](images/image-20211026142048376.png)

Tại đây, người dùng bấm nút **Cấu hình**, hệ thống tự động thiết lập và hiển thị thông báo thiết lập thành công.

![image-20211026142134700](images/image-20211026142134700.png)

- **Tạo bộ dữ liệu ảnh nhận diện cho tất cả nhân viên**: Tại bước này, người quản trị tải lên ảnh nhận diện cho nhân viên. 

Người dùng vào menu **Chấm công** >> **Camera AI** >> **Cấu hình nhân viên**, giao diện hiện lên danh sách nhân viên. Những nhân viên ở trạng thái "Chưa đồng bộ", người dùng bấm chọn nhân viên để tải ảnh lên. (Lưu ý: Người dùng cũng có thể bấm chọn nhân viên "Đã đồng bộ" để chỉnh sửa ảnh), giao diện hiển thị như sau

![image-20211026143450617](images/image-20211026143450617.png)

Người dùng bấm **Sửa**,  giao diện hiển thị cho phép người dùng thêm ảnh 

![image-20211026144816912](images/image-20211026144816912.png)

Người dùng thực hiện tải lên và đồng bộ ảnh cho tất cả nhân viên. 

## Thiết lập kế hoạch nghỉ phép cho nhân viên

Tiền điều kiện: Quản trị viên hệ thống đã thiết lập loại hợp đồng tính phép ở bước [này](#Thiết lập loai hợp đồng tính phép)

***Đối tượng thực hiện: cán bộ quản lý công hoặc người quản trị phân hệ Đăng ký công***

- Thường hàng kỳ, hàng năm hoặc khi nhân viên có sự thay đổi liên quan đến tính tổng số ngày được phép đăng ký nghỉ phép trong năm (ví dụ như khi nhân viên thay đổi diện đối tượng từ thử việc lên hợp đồng lao động, khi nhân viên nghỉ việc,...), cán bộ quản lý công sẽ thực hiện tính toán lại tổng số ngày phép cho nhân viên. 

  Mục đích của bước này là để cấp phát số ngày phép cho nhân viên theo đúng quy định.

- Hướng dẫn thực hiện trên hệ thống: 

  - ***Tính toán số ngày phép***: Khi cần tính lại số ngày phép cho nhân viên, người dùng vào menu **Đăng ký công** >> Chọn **Quản lý** >> Chọn **Quản lý nghỉ phép** >> Bấm nút **Lấy dữ liệu** >> Tại đây người dùng bấm **Thêm một dòng** để tìm kiếm và tích chọn 1 hoặc nhiều nhân viên cần tính phép >> Bấm **Chọn** để tiếp tục

  ![image-20211001103353709](images/image-20211001103353709.png)

   Người dùng bấm **Tạo** để thực hiện tính toán số ngày phép

  ![image-20211001103440578](images/image-20211001103440578.png)
  Hệ thống tự động tính toán, hiển thị dữ liệu lên danh sách Quản lý nghỉ phép

  ![image-20211001103924333](images/image-20211001103924333.png)

  Đối với những dòng dữ liệu vừa được tính toán, chưa được phê duyệt (tức là ở trạng thái **Nháp**) thì người dùng có thể nhập thêm số liệu vào cột Số ngày phép công thêm (Tức là ví dụ theo quy định riêng của công ty, nhân viên Hoài được cộng thêm 1 ngày phép vì có thành tích xuất sắc thì người dùng nhập dữ liệu như trên ảnh), Số ngày kỳ trước (Tức là số ngày phép của năm trước còn dư được phép cộng thêm vào tổng số ngày phép cho năm sau) phù hợp. 

  - ***Phê duyệt dữ liệu***: Đối với các dòng dữ liệu hiển thị ở trạng thái **Nháp** thì nhân viên đó chưa được đăng ký nghỉ phép. Để hệ thống tự động cấp phát số ngày nghỉ phép này tới nhân viên tương ứng, người dùng cần thực hiện Phê duyệt để dữ liệu có hiệu lực bằng cách bấm **Phê duyệt** cho từng dòng hoặc tích chọn nhiều nhân viên để phê duyệt 1 lần

  ![image-20211001104849106](images/image-20211001104849106.png)

## Đăng ký chấm công

**Đối tượng thực hiện:** Nhân viên trong công ty

### Nhân viên chấm công thủ công

**Tiền điều kiện:** Nhân viên đã có tài khoản để đăng nhập vào hệ thống

Trong trường hợp công ty [thiết lập hình thức chấm công](#Thiết lập hình thức chấm công) là "Chấm công dựa vào lịch sử vào - ra", nhân viên của công ty bắt buộc phải chấm công thủ công để được ghi nhận công. Nhân viên của công ty có thể thực hiện chấm công trên ứng dụng vESS hoặc chấm công trên web.

*Cách 1: Chấm công trên web*

Nhân viên vào menu Chấm công >> Hệ thống hiển thị trang giao diện để chấm công. 

![image-20220620111217045](images/image-20220620111217045.png)

Nhân viên bấm để chấm công vào > Hệ thống hiển thị màn hình thông báo chấm công thành công 

![image-20220620111303978](images/image-20220620111303978.png)

Trước giờ nhân viên ra về, nhân viên vào màn hình Chấm công, thực hiện tương tự để chấm công ra.

*Cách 2: Chấm công trên ứng dụng vESS*

Nhân viên đăng nhập trên ứng dụng vESS, chọn menu Chấm công >> Thực hiện bấm Chấm công vào/ra tương tự trên web

![image-20220620112050661](images/image-20220620112050661.png) ![image-20220620112138863](images/image-20220620112138863.png) 

Người dùng có thể bấm vào "Tổng hợp công" để xem dữ liệu chấm công trong tháng của mình.

![image-20220620112256093](images/image-20220620112256093.png)

### Nhân viên đăng ký công nghỉ, công làm thêm

***Hệ thống chỉ cho phép đăng ký công cho tháng hiện tại hoặc thời điểm trong tương lai.***

Luồng thực hiện đăng ký chấm công được chia thành 2 trường hợp:

***Trường hợp 1***: *Nhân viên* chủ động đăng ký chấm công trên app mobile (trên điện thoại), hoặc trên ứng dụng web (trên máy tính)

Khi nhân viên có yêu cầu đăng ký chấm công (có thể là đăng ký nghỉ, đăng ký công tác, hoặc đăng ký làm thêm giờ) thì sẽ chủ động tạo đơn đăng ký lên hệ thống theo 2 cách:

- *Cách 1: Đăng ký trên ứng dụng web*

Nhân viên vào menu **Đăng ký công** >> Hệ thống hiển thị bảng lịch có các ngày đăng ký nghỉ/OT. Nhân viên bấm **Đăng ký công** >> Nhập thông tin theo yêu cầu >> Bấm **Lưu** để hoàn tất. Lúc này hệ thống ghi nhận đăng ký công ở trạng thái *Chờ duyệt.* 

![image-20211001135700337](images/image-20211001135700337.png)

![image-20211001134701698](images/image-20211001134701698.png)

Hoặc nhân viên vào menu Đăng ký công >> Chọn **Cá nhân** >> Chọn **Đăng ký công** >> Hệ thống hiển thị lên màn hình danh sách đăng ký công >> Nhân viên bấm **Tạo**, nhập các thông tin yêu cầu và bấm **Lưu** để hoàn tất việc gửi đơn đăng ký công. 

***Lưu ý:*** 

- Nhân viên không thể tạo nhiều đơn đăng ký công trong cùng thời gian. Trong trường hợp nhân viên tạo đơn đăng ký nhưng chưa muốn trình cấp trên duyệt ngay thì có thể thực hiện lưu đơn nháp bằng cách bấm *Tạo bản nháp*. Khi muốn trình cấp trên duyệt, nhân viên vào đơn đăng ký công ở trạng thái "Nháp" (Để trình) >> Chỉnh sửa thông tin phù hợp và bấm **Xác nhận** để hoàn tất
- Đối với các đơn đăng ký nghỉ phép: nhân viên chỉ được đăng ký trong số ngày được cho phép (Người quản lý công đã tính cho nhân viên tại bước trên)

![image-20211001143922470](images/image-20211001143922470.png)

![image-20211001144009268](images/image-20211001144009268.png)

- Thời lượng nghỉ được tính dựa trên lịch làm việc, tức là không tính thời lượng nghỉ cho các ngày nghỉ (Thứ 7, Chủ nhật) của nhân viên và không tính thời lượng làm thêm giờ đối với các khoảng thời gian thuộc khung làm việc cố định. (*Khung giờ làm việc của nhân viên được thiết lập trong hồ sơ nhân viên*)

- *Cách 2: Đăng ký trên app mobile*

Để thuận tiện hơn cho nhân viên, hệ thống hỗ trợ đăng ký công trên app mobile (sử dụng điện thoại smartphone). Nhân viên truy cập app, đăng nhập tài khoản cá nhân, bấm vào menu **Đăng ký công** >> Chọn **Yêu cầu chấm công của tôi** >> Chọn "Yêu cầu Bấm nút "+" để tạo đơn đăng ký công >> Nhân viên nhập đầy đủ thông tin và bấm **Hoàn tất** để trình cấp trên duyệt (hiển thị với trạng thái Chờ duyệt) hoặc bấm **Lưu nháp** để lưu đơn đăng ký ở trạng thái Nháp.

![image-20211011161637099](images/image-20211011161637099.png) ![image-20211011162431230](images/image-20211011162431230.png) ![image-20211011162527449](images/image-20211011162527449.png) 

![image-20211011162604060](images/image-20211011162604060.png) ![image-20211011162657413](images/image-20211011162657413.png) 

Ở trên app mobile, muốn chuyển đơn đăng ký từ trạng thái Nháp thành Chờ duyệt, nhân viên bấm vào đơn đăng ký, kiểm tra lại thông tin, chỉnh sửa nếu cần và bấm **Hoàn tất**.

***Trường hợp 2***: Nhân viên có vấn đề về kỹ thuật, hoặc sức khoẻ không thể tự đăng ký được, nhờ *cán bộ quản lý công* thực hiện đăng ký công cho nhân viên

Người quản lý công vào menu **Đăng ký công** >> Chọn **Quản lý** >> Chọn **Đăng ký công** >> Bấm **Tạo**, nhập liệu và bấm **Lưu** để hoàn tất (chờ người có thẩm quyền duyệt) hoặc bấm **Tạo bản nháp** để lưu đơn với trạng thái Nháp

![image-20211001144306068](images/image-20211001144306068.png)

*Lưu ý: Người quản lý công có thể thực hiện tạo đơn đăng ký công cho từng nhân viên, cả công ty, cả 1 phòng/ban, theo nhóm nhân viên chung nhãn bằng cách lựa chọn phù hợp chế độ đăng ký ở hình trên.*

## Phê duyệt/ Từ chối đăng ký công

Đối với các loại đăng ký công cần phê duyệt thì quản lý của nhân viên hoặc quản lý công hoặc người quản trị phân hệ Đăng ký công có quyền vào duyệt tương ứng. 

Hướng dẫn các bước thực hiện trên hệ thống theo các đối tượng như sau:

- Người phụ trách: Đối tượng này được phép duyệt đơn đăng ký công của nhân viên mình quản lý

  ***Cách 1: Thực hiện trên web***

  - Người dùng vào menu **Đăng ký công** >> Chọn **Quản lý** >> Chọn **Đăng ký công** >> Hệ thống hiển thị danh sách đơn đăng ký công của nhân viên do người dùng phụ trách quản lý trực tiếp
  - Người dùng tìm thực hiện bấm **Duyệt** nếu chấp thuận đơn đăng ký công, hoặc ngược lại thì bấm **Từ chối**. Người dùng có thể tích chọn nhiều đơn để duyệt/ từ chối 1 lần

  ![image-20211001151206263](images/image-20211001151206263.png)

- Quản lý công: Đối tượng này được phép duyệt tất cả đơn đăng ký công của nhân viên trừ đơn của bản thân

  - Người dùng vào menu **Đăng ký công** >> Chọn **Quản lý** >> Chọn **Đăng ký công** >> Hệ thống hiển thị mặc danh sách đơn đăng ký công của nhân viên do người dùng phụ trách quản lý trực tiếp, người dùng có thể xoá bộ lọc trên thanh tìm kiếm để xem đơn đăng ký của tất cả các nhân viên trong công ty
  - Người dùng tìm thực hiện bấm **Duyệt** nếu chấp thuận đơn đăng ký công, hoặc ngược lại thì bấm **Từ chối**

- Người quản trị phân hệ Đăng ký công: Đối tượng này được duyệt tất cả đơn đăng ký công, kể cả đơn của bản thân

  - Người dùng vào menu **Đăng ký công** >> Chọn **Quản lý** >> Chọn **Đăng ký công** >> Hệ thống hiển thị mặc danh sách đơn đăng ký công của nhân viên do người dùng phụ trách quản lý trực tiếp, người dùng có thể xoá bộ lọc trên thanh tìm kiếm để xem đơn đăng ký của tất cả các nhân viên trong công ty
  - Người dùng tìm thực hiện bấm **Duyệt** nếu chấp thuận đơn đăng ký công, hoặc ngược lại thì bấm **Từ chối**
  - Ngoài ra, người quản trị phân hệ Đăng ký công có thể chuyển 1 đơn đăng ký ở trạng thái từ "Bị từ chối" về "Nháp" để nhân viên đó có thể kiểm tra, chỉnh sửa lại thông tin và trình người có thẩm quyền duyệt lại. Thực hiện bằng cách bấm **Tạo bản nháp** tại màn hình chi tiết đơn đăng ký công có trạng thái *Bị từ chối*.

***Cách 2: Thực hiện trên ứng dụng mobile***

Người sử dụng đăng nhập vào ứng dụng mobile trên điện thoại, chọn menu **Yêu cầu chấm công** >> Chọn **Phê duyệt yêu cầu chấm công** >> Chọn yêu cầu chấm công cần duyệt để thực hiện **Duyệt/ Từ chối**. Người sử dụng có thể thao tác nhanh bằng cách bấm vào dấu ![image-20211011163041070](images/image-20211011163041070.png) tại đơn đăng ký cần duyệt, chọn **Duyệt/ Từ chối**  phù hợp

![image-20211011163211631](images/image-20211011163211631.png) ![image-20211011163231180](images/image-20211011163231180.png) 

## Tổng hợp công

***Đối tượng thực hiện: Người quản trị phân hệ Chấm công (Cán bộ chấm công)*** 

### Chấm công nhanh

Hằng ngày, hệ thống sẽ tự động đồng bộ và chấm công cho nhân viên dựa dựa theo hình thức chấm công đã được thiết lập ở bước [này](#Thiết lập hình thức chấm công) và các dữ liệu lịch sử vào/ra, lịch sử đăng ký công nghỉ, công làm thêm của nhân viên đã được duyệt. Thông tin chấm công sẽ hiển thị lên bảng công cho tất cả nhân viên. 

Người dùng xem bảng tổng hợp công trên hệ thống bằng cách vào menu **Chấm công** >> Chọn **Tổng hợp công** >> Hệ thống hiển thị dữ liệu chấm công của tất cả nhân viên tại tháng hiện tại như hình sau:

![image-20220620114651541](images/image-20220620114651541.png)

***Lưu ý:*** 

- *Để chấm công được cho nhân viên, thì bắt buộc cán bộ nhân sự phải thiết lập quá trình làm việc cho nhân viên tại bước Quản lý hồ sơ nhân viên.*

- *Hệ thống tự động chấm công hàng đêm, nên nhân viên bắt đầu làm việc ngày n thì ngày n + 1 có dữ liệu chấm công.*

- *Trong trường hợp ngày n, cán bộ chấm công muốn chốt công luôn; để lấy được cả dữ liệu chấm công ngày hiện tại, người dùng thực hiện đồng bộ công bằng cách bấm **Đồng bộ** >> Chọn thời gian cần đồng bộ >> Hệ thống hiển thị cảnh báo sẽ xoá toàn bộ dữ liệu trên bảng công trong khoảng thời gian được chọn và tự động đồng bộ lại >> Người dùng xác nhận **Đồng ý** >> Hệ thống thực hiện đồng bộ và hiển thị lại bảng công.*

- *Cán bộ chấm công có thể thực hiện xuất dữ liệu bảng công bằng cách bấm **Xuất báo cáo***

- *Trường hợp cán bộ chấm công muốn kiểm tra dữ liệu vào ra của nhân viên, người dùng vào menu Chấm công >> Người quản lý >> Chấm công để xem dữ liệu vào/ ra theo điểm danh trên web, hoặc Chấm công >> Camera AI >> Lịch sử Check In để xem dữ liệu vào/ra theo camera*

### [Chấm công thủ công]()

Vào menu **Chấm công** >> Chọn **Tổng hợp công** >> Màn hình hiển thị bảng tổng hợp công. Cán bộ chấm công có thể sửa, hoặc thêm mới công cho nhân viên bằng cách click đúp vào ô công của nhân viên, màn hình hiện ra như sau:

![image-20220620114903383](images/image-20220620114903383.png)

Cán bộ chấm công thực hiện nhập/ sửa công vào ô **Thời gian làm** theo quy tắc: **[Ký hiệu công 1]:[Số giờ công]; [Ký hiệu công 2]: [Số giờ công]** và bấm **Lưu & Đóng**

Trong trường hợp muốn xoá công của nhân viên, cán bộ chấm công click vào ô công của nhân viên, chọn biểu tượng "x" để xoá công.

Ví dụ: CB chấm công chấm cho đ/c Trần Bảo Châu đi làm thêm giờ (Ký hiệu: OT), cả ngày 14/05/2022 (8 tiếng). CB chấm công nhập OT:8, cụ thể:

![image-1](images/image-1.jpeg)

Sau khi bấm **Lưu & Đóng**, màn hình sẽ hiển thị DS như dưới và ghi nhận thành công.

![image-2](images/image-2.jpeg)

### Import công từ file excel

**Mục đích sử dụng**: Công ty không sử dụng quy trình chấm công theo quy trình hướng dẫn ở trên, nhưng muốn Import dữ liệu chấm công quản lý từ file excel lên hệ thống, phục vụ làm dữ liệu đầu vào để tính lương.

**Các bước thực hiện:** 

Bước 1: Tải file mẫu import

Trên màn hình tổng hợp công, người dùng bấm vào nút **Nhập dữ liệu** để mở ra hộp thoại import công >> Bấm **Xuất biểu mẫu** để tải file mẫu dữ liệu chấm công

![image-20220620134510207](images/image-20220620134510207.png)

Bước 2: Nhập dữ liệu vào file excel

Người dùng thực hiện nhập liệu công vào file excel theo mẫu vừa tải xuống ở bước 1, ví dụ minh hoạ ở ảnh sau

Lưu ý: Bắt buộc nhập Tháng, Năm, Mã nhân viên và dữ liệu chấm công.

![image-20220620135504543](images/image-20220620135504543.png)

Bước 3: Nhập file lên hệ thống

Trên màn hình ở bước 1, người dùng bấm **Tải lên tập tin của bạn**, chọn file excel cần nhập, bấm **Nhập tệp** để xác nhận >> Hệ thống kiểm tra dữ liệu trên file excel

+ Nếu có lỗi: Hệ thống hiển thị màn hình thông báo lỗi như minh hoạ

  ![image-20220620135847264](images/image-20220620135847264.png)

+ Nếu không có lỗi: Hệ thống thực hiện import, và tự tải lại trang màn hình tổng hợp công sau khi đã ghi nhận dữ liệu trên file excel

- Người dùng bắt buộc nhập mã nhân viên (dạng text), nhập dữ liệu chấm công; tên nhân viên không bắt buộc nhập. 

**Một số cảnh báo lỗi nhập tệp thường gặp và cách xử lý**

  - "Nhân viên không hợp lệ"
    - Nguyên nhân: Mã nhân viên không tồn tại, hoặc không thuộc quyền quản lý của người dùng đang thao tác hoặc nhân viên chưa có quá trình làm việc tại ngày chấm công.
    - Xử lý: Kiểm tra lại mã nhân viên tại dòng cảnh báo, điều chỉnh phù hợp. 

  - "Thời gian làm việc không hợp lệ"

    - Nguyên nhân: Dữ liệu chấm công sai quy tắc hoặc sai ký hiệu công, hoặc tổng số giờ làm trong ngày vượt quá giờ công chuẩn theo cấu hình lịch làm việc cho nhân viên

    - Xử lý: Kiểm tra lại dữ liệu chấm công theo dòng và cột, đảm bảo đúng ký hiệu công, đúng quy tắc. Tiếp đến kiểm tra thêm tổng số giờ công làm việc (Bao gồm loại công Nghỉ có lương & Nghỉ không lương & Chấm công) và số giờ làm việc chuẩn trên lịch làm việc của nhân việc.

      Xem lịch làm việc của nhân viên: Vào menu **Nhân viên**, bấm xem chi tiết 1 nhân viên, tab **Thông tin công việc**, trường **Giờ làm việc**

      ![image-20220620144844948](images/image-20220620144844948.png)

      ![image-20220620144916389](images/image-20220620144916389.png)

      Ví dụ ngày thứ 2, theo lịch làm việc, tổng số giờ làm chuẩn là 8h. Nếu người dùng nhập dữ liệu chấm công ngày thứ 2 cho nhân viên có tổng công nghỉ có lương + nghỉ không lương + chấm công vượt quá 8h thì hệ thống cảnh báo. Người dùng thực hiện điều chỉnh dữ liệu chấm công hoặc điều chỉnh giờ làm việc phù hợp. 

  - "Tháng ... không có ngày ..."
    - Nguyên nhân: Nhập thừa dữ liệu chấm công. Ví dụ tháng 6 chỉ có 30 ngày nhưng lại nhập cả dữ liệu chấm công của ngày 31.
    - Xử lý: Xoá bỏ dữ liệu chấm công không hợp lệ, và import lại file.

## Chấm công phân ca

Chức năng này phục vụ cho các công ty, đơn vị có nhiều ca làm việc, và phân bổ ca làm việc khác nhau cho các nhân viên. 

### **Thiết lập phân ca**

**Đối tượng sử dụng:** Cán bộ Nhân sự, Cán bộ chấm công

**Mục đích sử dụng:** 

* Người dùng tạo ca làm việc, chi tiết phân ca, đổi ca làm việc cho nhân viên để phù hợp với tình hình hoạt động của công ty.

* Nhân viên có hình thức làm việc theo ca thì người dùng mới có thể phân ca cho nhân viên đó. Hình thức làm việc của nhân viên được thiết lập trong mục **Người quản lý** >> **Nhân viên** >> **Thông tin công việc** >> **Lịch làm việc** >> **Hình thức làm việc**

  ![image-20220630172021350](images/image-20220630172021350.png)

### **Thiết lập ký hiệu công**

Kí hiệu công là kí hiệu hiển thị trong bảng tổng hợp công, qua kí hiệu đó người dùng biết được loại ngày làm việc của các nhân viên để dễ dàng tổng hợp theo loại công và tính lương, ví dụ: ký hiệu **X** thể hiện công ngày thường, kí hiệu **OT**: công tăng ca.

***Các bước thực hiện:***

*Bước 1:* Người dùng truy cập vào ứng dụng **Chấm công** > Chọn mục **Cấu hình** > Nhấn chọn **Ký hiệu công**: Hiển thị danh sách kí hiệu công > Nhấn nút **Tạo**

![image-20220630172006579](images/image-20220630172006579.png)

*Bước 2:* Nhập tên công, mã công, loại công > Nhấn **Lưu**

![image-20220630172100570](images/image-20220630172100570.png)

### **Thiết lập ca làm việc**

*Bước 1:* Người dùng truy cập vào ứng dụng **Chấm công** > Chọn mục **Ca làm việc** > Nhấn chọn **Ca làm việc**: Hiển thị danh sách ca làm việc > Nhấn nút **Tạo**

![image-20220630172139806](images/image-20220630172139806.png)

*Bước 2:* Điền đầy đủ thông tin vào các trường bắt buộc > Nhấn **Lưu**

![image-20220630172203579](images/image-20220630172203579.png)

Tại màn hình Danh sách ca làm việc, thêm mới một bản ghi Ca làm việc vừa tạo

**Lưu ý:** *Các ca làm việc khác nhau, nhưng cùng tính chất thì người dùng có thể thiết lập chung 1 ký hiệu công*

![image-20220630172228714](images/image-20220630172228714.png)

*Tuỳ vào mục đích người sử dụng muốn hiển thị lên bảng tổng hợp chấm công là ký hiệu công gì, tương ứng với ca làm việc nào, thì người dùng chọn Ký hiệu công tương ứng tại trường "Ký hiệu". Ví dụ, nếu muốn nhân viên đi làm "Ca 3" khi hiển thị lên bảng tổng hợp công với ký hiệu công là "Tăng ca  3 (TC3)" thì thực hiện thiết lập như sau*: 

- Thiết lập kí hiệu công với tên: ***Tăng ca 3***, mã: ***TC3***, loại công: ***Chấm công***.

  ![image-20220704094921831](images/image-20220704094921831.png)

- Thiết lập ca làm việc với tên: ***Ca 3***, mã: ***TC3***, kí hiệu: ***TC3***

  ![image-20220704100524336](images/image-20220704100524336.png)

  *Sau đó thực hiện phân ca như các bước dưới đây*.

### Phân ca chi tiết cho các phòng/ban, nhân viên

**Đối tượng sử dụng:** Cán bộ nhân sự.

**Các bước thực hiện:**

*Bước 1:* Người dùng truy cập vào ứng dụng **Chấm công** > Chọn mục **Ca làm việc** > Nhấn chọn **Phân ca chi tiết:** Hiển thị danh sách chi tiết phân ca > Nhấn nút **Tạo**

![image-20220630172252742](images/image-20220630172252742.png)

*Bước 2:* Điền đầy đủ thông tin Chi tiết phân ca vào các trường bắt buộc:

![image-20220630172342982](images/image-20220630172342982.png)

***Lưu ý:*** 

* *Nếu chọn phòng ban áp dụng, hệ thống sẽ hiển thị tất cả nhân viên trong phòng ban đó và áp dụng ca làm việc này (người dùng có thể xoá nhân viên không áp dụng ca làm việc):*

  ![image-20220630172405997](images/image-20220630172405997.png)

* *Người dùng cũng có thể chọn nhân viên từ các đơn vị khác nhau để phân ca bằng cách không chọn phòng ban áp dụng mà chọn cụ thể từng nhân viên:*

  ![image-20220630172439423](images/image-20220630172439423.png)

* *Người dùng không thể Tạo chi tiết phân ca với các ca làm việc có thời gian trùng nhau. Trường hợp người dùng chưa muốn duyệt Chi tiết phân ca thì nhấn Lưu để Lưu bản nháp.*
* *Phải có ít nhất 1 nhân viên được phân ca làm việc mới có thể Duyệt Chi tiết phân ca*

*Bước 3:* 

Bấm nút **Duyệt** ![2022-06-29_10h57_28](images/2022-06-29_10h57_28.png) để duyệt Chi tiết phân ca. Chi tiết phân ca sau khi được duyệt sẽ xuất hiện tại Bảng tổng hợp phân ca. 

Người dùng xem Bảng tổng hợp phân ca bằng cách vào mục **Ca làm việc** >> **Bảng tổng hợp phân ca**		

## **Đề nghị đổi ca**

### **Thiết lập đổi ca**

**Mục đích sử dụng:** Nhân viên đã được phân ca có thể tạo đề nghị đổi ca để đổi sang ca làm việc khác.

**Đối tượng sử dụng:** Nhân viên được phân ca làm việc 

*Bước 1:*  Người dùng truy cập vào ứng dụng **Chấm công** > Chọn mục **Ca làm việc** > Nhấn chọn **Đề nghị đổi ca**: Hiển thị danh sách Đề nghị đổi ca > Nhấn nút **Tạo**

![image-20220630172544999](images/image-20220630172544999.png)

*Bước 2:* Điền thông tin vào các trường bắt buộc

![image-20220630172608741](images/image-20220630172608741.png)

Sau đó nhấn **Lưu**, bản ghi ở trạng thái Nháp, chờ duyệt.

### **Phê duyệt/Từ chối đổi ca**

**Mục đích sử dụng:** Các yêu cầu đổi ca được tạo phải được phê duyệt mới có thể đổi ca trên Bảng tổng hợp phân ca. Người có quyền duyệt có thể phê duyệt hoặc từ chối yêu cầu đổi ca.

**Đối tượng sử dụng:** 

Quản lý của nhân viên, quản lý phân ca hoặc người quản trị phân hệ chấm công 

Với mỗi yêu cầu đổi ca, người được chọn duyệt trong yêu cầu đổi ca mới có thể phê duyệt yêu cầu đổi ca đó.

**Cách thực hiện:**

- Tại tài khoản của người duyệt, màn hình hiển thị 02 nút: Duyệt và Từ chối

  ![2022-06-30_14h27_00](images/2022-06-30_14h27_00.png)

* Người dùng chấp thuận đề nghị đổi ca thì nhấn **Duyệt**, bản ghi chuyển về trạng thái Duyệt. Tại Bảng tổng hợp phân ca, ca của hai nhân viên đó sẽ được thay đổi cho nhau:

  ![2022-06-30_14h29_01](images/2022-06-30_14h29_01.png)

* Ngược lại, người dùng nhấn **Từ chối**, bản ghi chuyển về trạng thái Từ chối. Không có sự thay đổi nào ở Bảng tổng hợp phân ca. Người duyệt có thể chuyển bản ghi về trạng thái Nháp bằng cách nhấn vào **Chuyển về Nháp** để người đề nghị đổi ca có thể chỉnh sửa.

  ![2022-06-29_14h51_16](images/2022-06-29_14h51_16.png)



## **Tổng hợp công phân ca**

Các nghiệp vụ, lưu ý trên bảng tổng hợp công, người dùng xem thêm tại [đây](#Tổng hợp công)

Người dùng xem bảng tổng hợp công trên hệ thống bằng cách vào menu **Chấm công** >> Chọn **Tổng hợp công**: Hệ thống hiển thị dữ liệu chấm công của tất cả nhân viên (bao gồm cả nhân viên làm theo giờ hành chính, và các nhân viên làm theo ca) tại tháng hiện tại như hình sau: 

![image-20220704135832272](images/image-20220704135832272.png)



## Chốt dữ liệu tổng hợp công

**Mục đích sử dụng:** Dữ liệu tại bảng tổng hợp công vẫn có thể sửa, xoá, thay đổi, nhập dữ liệu từ file excel. Do đó, khi tới kì chốt công, sau khi nhân viên rà soát dữ liệu công đúng với số công thực tế, người dùng thực hiện chốt dữ liệu. Việc chốt dữ liệu sẽ là kết quả tổng hợp công cuối cùng, bảng dữ liệu công sẽ bị khoá và không thể thay đổi để đảm bảo dữ liệu đầu vào cho việc tính lương.

**Đối tượng sử dụng:** Cán bộ chấm công.

**Các bước thực hiện:** 

* Người dùng truy cập vào ứng dụng **Thiết lập** > Chọn **Chấm công** > Tích chọn ô **Chốt công**: Hiển thị Ngày chốt công > Chọn ngày chốt công.

  ![image-20220701111813406](images/image-20220701111813406.png)

* Sau khi chọn ngày chốt công, người dùng nhấn **Lưu** ![image-20220701094320279](images/image-20220701094320279.png). Khi đó, dữ liệu trên bảng tổng hợp công từ ngày được chọn là ngày chốt trở về trước được khoá dữ liệu, người dùng không thể can thiệp sửa, xoá, nhập dữ liệu công từ file excel.

   ![image-20220701104118965](images/image-20220701104118965.png)

  

