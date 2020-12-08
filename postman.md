__postman là gì?__  
-Postman là một công cụ cho phép chúng ta làm việc với API, nhất là REST. Với Postman, ta có thể gọi Rest API mà không cần viết dòng code nào.     
_restAPI là gì?_ là 1 phương thức tạo API với những nguyên lý tổ chức nhất định.các nguyên lý này hướng dẫn lập trình viên tạo môi trường xử lý API request được toàn diện.  
__cách sử dụng postman__
- chọn method, điền URL, thêm các thông tin cho body, header trong những trường hợp cần thiết, rồi nhấn SEND.  
- đợi và Postman cho kết quả   
nhìn có 2 dòng, cơ mà hiểu được có tý   
__*các chức năng cơ bản*__  
- cho phép gửi yêu cầu với các phương thức:   
GET( Yêu cầu server đưa lại resource. vd: vuốt newfeed),  
PUT(Yêu cầu server cho sửa / thêm vào resource đã có trên hệ thống. Ví dụ: Edit 1 post ở trên fb.),  
POST(Yêu cầu server cho tạo ra 1 resource mới. vd:đặt chuyến đi mới),  
DELETE(Yêu cầu server cho xóa 1 resourse)  
- Cho phép post dữ liệu dưới dạng form (key-value), text, json.  
- Hiện kết quả trả về dạng text, hình ảnh, XML, JSON. 

[__Tạo một request trên Postman__]    

[__Gởi request với phương thức POST__]( 

[__Export và Import Collections__]  

 **Export Collections**  
  Để export một test collection, nhấp vào biểu tượng dấu 3 chấm kế bên tên collection, sau đó chọn Export. Tại cửa sổ tiếp theo sẽ chọn định dạng mặc định là Collection v2.1 và chọn Export. Lúc này sẽ có được một file với định dạng .json dùng để lưu trữ hoặc gửi cho người khác sử dụng.  
 **Import Collections**  
 Để import, chọn vào biểu tượng Import trên thanh Header Bar. Chọn Tab “Import File” và tìm đến file .json đã được export ra.  
 Sau khi import thành công thì sẽ thấy được một Collection và các request bên trong.
 
[__viết test kiểm tra kết quả__](https://sangbui.com/postman-07-viet-tests-kiem-tra-ket-qua/#comments)  



