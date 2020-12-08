***GET( Yêu cầu server đưa lại resource. vd: vuốt newfeed),  
PUT(Yêu cầu server cho sửa / thêm vào resource đã có trên hệ thống. Ví dụ: Edit 1 post ở trên fb.),  
POST(Yêu cầu server cho tạo ra 1 resource mới. vd:đặt chuyến đi mới),  
DELETE(Yêu cầu server cho xóa 1 resourse)***  

**Tạo Một requuest (POST) trên Postman**  
**Tương tự như gửi request bằng phương thức GET, ở đây ta chỉ cần thay phương thức nhập là POST**  
- Method: POST  
- URL: Địa chỉ URL  
- Headers: Nhập theo thông tin đã có  
- Body: Các bạn nhấp vào tab Body, chọn RAW và nhập thông tin muốn insert vào database.
- Sau khi nhập đầy đủ các thông tin, chọn Send để xem kết quả trả về.
  
 KHi chọn POST, sẽ thấy ở Body có các option khác nhau để gửi dữ liệu bên trong body là:  
- ***Form-data***: được sử dụng để gửi dữ liệu mà đang gói bên trong biểu mẫu giống như các chi tiết được nhập khi điền vào biểu mẫu. Các chi tiết này được gửi bằng cách viết chúng dưới dạng cặp KEY-VALUE trong đó khóa là "name" của mục đang gửi và value là giá trị của nó. các bước:  
           1. Chọn Form-data  
           2. Thêm cặp KEY-VALUE  
- ***X-www-form-urlencoded***: Form data và x-www-form-urlencoded rất giống nhau. Cả 2 đều được sử dụng với mục đích hầu như giống nhau. Khác nhau là **URL sẽ được mã hóa khi gửi qua x-www-form-urlencoded**  
- ***Raw***: Raw là option hay được dùng nhất. Raw nghĩa là body message để chỉ ra một luồng các bit biểu diễn phần request body. Các bit này sẽ được hiểu là một string server  
1. Click vào drop down bên cạnh binary và ta có thể nhìn thấy tất cả các option bạn có thể gửi request  2. Chọn JSON(application/json)  
3. Nhập vào ô nhập dữ liệu  
- ***Binary***: Binary được thiết kế để gửi thông tin theo định dạng không thể nhập theo cách thủ công. Vì mọi thứ trong máy tính được chuyển thành nhị phân, ta sử dụng các tùy chọn này khi không thể được viết theo cách thủ công như hình ảnh, tệp, v.v. Để sử dụng tùy chọn này:
1. Click vào binary, chọn CHOOSE FILES
2. Chọn file bất kỳ như 1 file ảnh chẳng hạn
 
