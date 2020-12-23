## status code  
- 1xx (100 – 199): Information responses / Phản hồi thông tin – Yêu cầu đã được chấp nhận và quá trình xử lý yêu cầu của bạn đang được tiếp tục.  
- 2xx (200 – 299): Successful responses / Phản hồi thành công – Yêu cầu của bạn đã được máy chủ tiếp nhận, hiểu và xử lý thành công.

- 3xx (300 – 399): Redirects / Điều hướng – Phía client cần thực hiện hành động bổ sung để hoàn tất yêu cầu  

- 4xx (400 – 499): Client errors / Lỗi phía client – Yêu cầu không thể hoàn tất hoặc yêu cầu chứa cú pháp không chính xác. 4xx sẽ hiện ra khi có lỗi từ phía client do không đưa ra yêu cầu hợp lệ.

-  5xx (500 – 599): Server errors / Lỗi phía máy chủ – Máy chủ không thể hoàn thành yêu cầu được cho là hợp lệ. Khi 5xx xảy ra, chỉ có thể đợi để bên hệ thống máy chủ xử lý xong. 

**Cụ Thể**  
1. Information responses / Phản hồi thông tin:  

- 100 Continue: Phản hồi tạm thời này cho biết rằng mọi thứ tới hiện tại vẫn ổn và phía client nên tiếp tục yêu cầu hay bỏ qua phản hồi nếu yêu cầu đã hoàn tất.

- 101 Switching Protocol: Code này được gửi để phản hồi header yêu cầu Upgrade từ phía client và cho biết giao thức máy chủ đang chuyển sang.

- 102 Processing (WebDAV): Code này cho biết rằng máy chủ đã nhận và đang xử lý yêu cầu, nhưng phản hồi vẫn chưa có hiệu lực.

- 103 Early Hints: Được sử dụng để trả về một số tiêu đề phản hồi trước message HTTP cuối cùng.  
2. Successful responses / Phản hồi thành công:
- 200 OK: Yêu cầu đã thành công. Ý nghĩa của thành công còn phụ thuộc vào phương thức HTTP là gì:

      - GET: Tài nguyên đã được tìm nạp và được truyền trong nội dung thông điệp.  
      - HEAD: Các header thực thể nằm trong nội dung thông điệp.  
      - PUT hoặc POST: Tài nguyên mô tả kết quả của hành động được truyền trong nội dung thông điệp.  
      - TRACE: Nội dung thông điệp chứa thông báo yêu cầu khi máy chủ nhận được.

- 201 Created: Yêu cầu đã thành công và kết quả là một tài nguyên mới đã được tạo. Đây thường là phản hồi được gửi sau các yêu cầu POST hoặc một số yêu cầu PUT.

- 202 Accepted: Yêu cầu đã được nhận nhưng chưa được thực hiện. Yêu cầu này là non-committal, vì không có cách nào trong HTTP để gửi sau đó một phản hồi không đồng bộ cho biết kết quả của yêu cầu. Nó dành cho các trường hợp trong đó 1 quá trình / máy chủ khác xử lý yêu cầu hoặc để xử lý hàng loạt.

- 203 Non-Authoritative Information: Code phản hồi này có nghĩa là siêu thông tin được trả về không hoàn toàn giống với thông tin có sẵn từ máy chủ gốc, nhưng được thu thập từ phần copy local hay của bên phía thứ 3. Code này chủ yếu được sử dụng để phản chiếu hoặc sao lưu tài nguyên khác. Ngoại trừ trường hợp cụ thể đó, thông thường phản hồi “200 OK” được ưu tiên cho trạng thái này.

- 204 No Content: Không có nội dung để gửi cho yêu cầu này, nhưng các header có thể hữu dụng. User-agent có thể cập nhật các header đã lưu trong bộ nhớ cache cho tài nguyên này bằng các header mới.

- 205 Reset Content: Cho user-agent biết để reset document đã gửi yêu cầu này.

- 206 Partial Content: Code phản hồi này được dùng khi Range header được gửi từ client để yêu cầu chỉ 1 phần của nguồn tài nguyên.

- 207 Multi-Status (WebDAV): Truyền tải thông tin về nhiều nguồn tài nguyên, đối với các trường hợp mà nhiều status code có thể đều thích hợp.

- 208 Already Reported (WebDAV): Được sử dụng trong 1 phần tử phản hồi <dav:propstat> để tránh liệt kê nhiều lần các thành viên nội tại của nhiều liên kết vào cùng 1 tập hợp.

- 226 IM Used (HTTP Delta encoding): Máy chủ đã hoàn thành yêu cầu GET cho nguồn tài nguyên và phản hồi là sự trình bày kết quả của 1 hoặc nhiều thao tác instance được áp dụng cho instance hiện tại.

4. Client errors / Lỗi phía client:
– 400 Bad Request: Máy chủ không thể hiểu yêu cầu do cú pháp không hợp lệ.

- 401 Unauthorized: Cho dù quy chuẩn HTTP chỉ định “unauthorized” (không có thẩm quyền), nhưng nó có nghĩa phản hồi này là “unauthenticated” (chưa được xác thực). Có nghĩa là, client phải các tự xác thực chính mình để nhận được phản hồi đã yêu cầu.

- 402 Payment Required: Code phản hồi này được dành cho những lần sử dụng trong tương lai. Mục đích ban đầu của việc tạo mã này là sử dụng nó cho các hệ thống thanh toán kỹ thuật số, tuy nhiên status code này rất hiếm khi được sử dụng và không tồn tại quy ước tiêu chuẩn nào.

- 403 Forbidden: Client không có quyền truy cập vào phần nội dung, nghĩa là nó không được phép, vì vậy máy chủ từ chối cung cấp tài nguyên được yêu cầu. Không giống như 401, danh tính của client đã được máy chủ nhận biết.  
- 404 Not Found:
– 405 Method Not Allowed: Phương thức yêu cầu được máy chủ nhận biết nhưng đã bị vô hiệu hóa và không thể sử dụng được. Ví dụ: 1 API có thể cấm XÓA 1 nguồn tài nguyên. 2 phương thức bắt buộc, GET và HEAD, không bao giờ được vô hiệu hóa và không được trả về code lỗi này.

- 406 Not Acceptable: Phản hồi này được gửi khi máy chủ web, sau khi thực hiện server-driven content negotiation, không tìm thấy bất kỳ nội dung nào phù hợp với các tiêu chí do user-agent đưa ra.

- 407 Proxy Authentication Required: Code này tương tự như 401 nhưng việc xác thực là cần thiết để được thực hiện bởi proxy.

- 408 Request Timeout: Phản hồi này được gửi trên 1 kết nối idle bởi 1 số máy chủ, ngay cả khi không có bất kỳ yêu cầu nào trước đó của client. Có nghĩa là máy chủ muốn tắt kết nối không sử dụng này. Phản hồi này được sử dụng nhiều hơn vì 1 số trình duyệt như Chrome, Firefox 27+ hoặc IE9, sử dụng cơ chế  tiền kết nối HTTP để tăng tốc độ lướt web. Cũng lưu ý rằng 1 số máy chủ chỉ tắt kết nối luôn mà không hề gửi thông báo này.

- 409 Conflict: Phản hồi này được gửi khi 1 yêu cầu xung đột với trạng thái hiện tại của máy chủ.

- 410 Gone: Phản hồi này được gửi khi nội dung được yêu cầu đã bị xóa vĩnh viễn khỏi máy chủ, không có địa chỉ chuyển tiếp. Client phải xóa bộ nhớ cache và liên kết của mình tới nguồn tài nguyên. HTTP spectication dự định status code này được sử dụng cho “các dịch vụ khuyến mại, có thời hạn”. Các API không nên bắt buộc phải chỉ ra các tài nguyên đã bị xóa bằng status code này.

- 411 Length Required: Máy chủ đã từ chối yêu cầu vì trường header Content-Lenghth không được xác định và máy chủ thì yêu cầu chuyện đó.

- 412 Precondition Failed: Client đã chỉ ra các điều kiện tiên quyết trong các header của nó mà máy chủ không đáp ứng được.

- 413 Payload Too Large: Thực thể yêu cầu lớn hơn giới hạn do máy chủ xác định, máy chủ có thể đóng kết nối hoặc trả về trường header Retry-After.

- 414 URI Too Long: URI được yêu cầu bởi client dài hơn mức máy chủ muốn thông dịch.

- 415 Unsupported Media Type: Định dạng phương tiện của dữ liệu được yêu cầu không được máy chủ hỗ trợ, do đó máy chủ đang từ chối yêu cầu.

- 416 Range Not Satisfiable: Client yêu cầu một phần của tập tin nhưng máy chủ không thể cung cấp nó. Trước đây được gọi là “Requested Range Not Satisfiable”.

- 417 Expectation Failed: Máy chủ không thể đáp ứng các yêu cầu của trường Expect trong header.  
5. Server errors / Lỗi phía máy chủ:
- 500 Internal Server Error: Một thông báo chung, được đưa ra khi máy chủ gặp phải một trường hợp bất ngờ, message cụ thể không phù hợp.

- 501 Not Implemented: Máy chủ không công nhận các phương thức yêu cầu hoặc không có khả năng xử lý nó.

- 502 Bad Gateway: Máy chủ đã hoạt động như một gateway hoặc proxy và nhận được một phản hồi không hợp lệ từ máy chủ nguồn.

- 503 Service Unavailable: Máy chủ hiện tại không có sẵn (hiện đang quá tải hoặc bị down để bảo trì). Đây chỉ là trạng thái tạm thời.

- 504 Gateway Timeout: Máy chủ đã hoạt động như một gateway hoặc proxy và không nhận được một phản hồi từ máy chủ nguồn.

- 505 HTTP Version Not Supported: Máy chủ không hỗ trợ phiên bản “giao thức HTTP”.
