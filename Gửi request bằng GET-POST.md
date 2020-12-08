*Trước khi thực hiện việc test API thì cần phải có đầy đủ thông tin của API cần test như:*   
 - URL: Đây là địa chỉ URL mà request sẽ gửi đi  
- Method: Phương thức của request, phương thức được gửi đi ở đây là phương thức GET
- URL Params: Tham số truyền thêm vào URL, Có thể có hoặc không 
- Header: Thông tin về headers của một request, hiện tại chúng ta có 2 khoá là “Content-Type” và “Authorization”
- Data Params: Chúng ta không cần data parameters trong phương thức GET
- Success Response: Kết quả khi request được gởi thành công (gồm code và content/body)
- Error Response: Kết quả khi request được gởi thất bại (response code khi gặp lỗi)    


**Tạo Một requuest (GET) trên Postman**
Trên Header Bar, chọn New/Request.  
Nhập các thông tin về Request:
- Request name: Tên của request  
- Request description (Optional): Mô tả hoặc chú thích cho request, phần này không bắt buộc.  
- “+ Create Collection”: nên tạo một collection để lưu trữ các request, một collection giống như một test suite / folder lưu trữ các request nhỏ bên trong để dễ quản lý. Chọn vào Create Collection đặt tên cho collection vừa tạo. Sau khi đặt tên, click vào collection vừa tạo để chọn, lúc này nút Save sẽ được sáng lên để có thể lưu request vào “Employees API”.  

Sau khi tạo mới một request, chuyển qua phần Builder để nhập các thông tin cần thiết:  
- Method: mặc định sẽ chọn phương thức GET  
- Nhập địa chỉ API cần gửi
Chọn tab Headers, nhập thông tin về header bao gồm Content-Type, Authorization và giá trị của các khoá như trong yêu cầu.
- Chọn Send để gởi request.
*Kết quả*  
- Có thể xem kết quả ở mục Status. Hiện tại **Status: 200 OK** cho thấy request đã được gởi thành công. Ngoài ra có thể kiểm tra thêm ở phần response body để xem kết quả, danh sách dữ liệu trả về.  
- Nếu **không thành công** thì Kết quả trả về là 401 Unauthorized (không thành công) và có thông báo “Please check the authorization“
  
  
**Tạo Một requuest (POST) trên Postman**  
(*GET( Yêu cầu server đưa lại resource. vd: vuốt newfeed),  

PUT(Yêu cầu server cho sửa / thêm vào resource đã có trên hệ thống. Ví dụ: Edit 1 post ở trên fb.),  

POST(Yêu cầu server cho tạo ra 1 resource mới. vd:đặt chuyến đi mới),  

DELETE(Yêu cầu server cho xóa 1 resourse) *) 
**Tương tự như gửi request bằng phương thức GET, ở đây ta chỉ cần thay phương thức nhập là POST**  
- Method: POST  
- URL: Địa chỉ URL  
- Headers: Nhập theo thông tin đã có  
- Body: Các bạn nhấp vào tab Body, chọn RAW và nhập thông tin muốn insert vào database.
- Sau khi nhập đầy đủ các thông tin, chọn Send để xem kết quả trả về.

