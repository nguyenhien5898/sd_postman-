***1. Khái Niệm***  
  API (Application Programming Interface) ta có thể hiểu đơn giản nó là phần mềm trung gian giữa Client và Server cho phép chúng có thể nói chuyện được với nhau.
Trong API, thường sử dụng giao thức để Client và server giao tiếp với nhau. Trong đó giao thức chính là HTTP. Và API được xây dựng trên chính 2 thành phần: Request và Reponse.

Một request thường sử dụng 4 phương thức chính đó là:
- GET để truy vấn object
- POST để tạo object mới
- PUT để sửa đổi hoặc thay thế một object
- DELETE để loại bỏ một object

Mỗi phương thức trên phải được API call thông qua để gửi chỉ thị cho server phải làm gì.  

***Vì sao phải test API?***
- Trong quá trình triển khai dự án, phần server và client làm độc lập với nhau nên có nhiều chỗ client chưa làm xong, mình không thể chờ client làm xong để test được dữ liệu mà test API bằng công cụ khác luôn –> Lúc này việc test hoàn toàn không phụ thuộc gì vào client.
- Kể cả khi client làm xong rồi, nếu mình test trên client mà thấy lỗi liên quan đến logic và dữ liệu thì cũng cần test thêm cả API để biết chính xác là server sai hay client sai –> fix lỗi sẽ nhanh hơn.
- Khi làm hệ thống web services, dự án của mình chỉ viết API cho bên khác dùng, mình sẽ không có client để test giống như các dự án khác –> phải test API hoàn toàn.
