# Proxy

## Proxy Server (Forward Proxy) là gì?

#### Định nghĩa

Một `forward proxy`, thường được gọi là proxy, proxy server hay web proxy là một server được đặt trước một nhóm các thiết bị của client. Khi những máy tính này gửi request đến các website và services trên internet, proxy server sẽ chặn những request này lại và nó sẽ tương tác với web servers thay cho các máy tính client. Nó hoạt động như một người trung gian.

Ví dụ, đặt tên cho 3 máy tính có liên quan đến một giao tiếp với forward proxy như sau:

- A: Tên của máy tính ở client
- B: Là một forward proxy server
- C: Đây là web server (nơi lưu trữ data của website)

<h4 style="text-align: center;">Forward Proxy Flow</h4>

![Forward Proxy (Proxy server)](/assets/img/forward_proxy_flow.png "Forward Proxy (Proxy server)")

Trong một giao tiếp Internet tiêu chuẩn, máy tính A sẽ tiếp cận trực tiếp đến máy tính C, với các request được gửi thẳng từ client đế `origin server` và server sẽ gửi các phản hồi đến client. Khi một forward proxy được thêm vào, A sẽ gửi request đến B và B sẽ forward các request đến C. Sau đó, C sẽ gửi phản hồi đến B, và nó lại forward trở về cho A.

#### Lợi ích của Forward Proxy

Tại sao lại cần phải thêm một bước trung gian trong các hoạt động Internet. Sau đây là một số lý do mà chúng ta cần sử dụng `forward Proxy`:

- Để hạn chế duyệt web: Một số chính phủ, trường học và các tổ chức khác sử dụng tường lửa để cung cấp cho người dùng quyền truy cập vào Internet một cách giới hạn. Sử dụng một proxy có thể khắc phục được những hạn chế này, vì chúng cho phép người dùng kết nối đến proxy thay vì các trang web họ đang truy cập.

- Để chặn quyền truy cập vào một số nội dung nhất định: proxy cũng có thể được thiết lập để chặn một nhóm người dùng truy cập các trang web nhất định. Ví dụ: trường học có thể cấu hình kết nối web thông qua proxy cho phép các quy tắc lọc nội dung, từ chối chuyển tiếp phản hồi từ Facebook và các trang mạng xã hội khác.

- Để bảo vệ danh tính người dùng: Ẩn địa chỉ IP của client khi truy cập tới các website trên internet do phía các website chỉ có thể biết được địa chỉ của forward proxy server.

## Reserve Proxy

#### Định nghĩa

Một `reserve proxy` là một server được đặt trước một hoặc nhiều web server, chặn các request từ client. Đây là điểm khác biệt so với `forward proxy`, khi được đặt trước các thiết bị ở client. Với một reserve proxy, khi client gửi các request lên web server, những request này sẽ bị chặn lại ở `edge computing (điện toán ngoại vi / điện toán biên)` của reserve Proxy. Reserve Proxy sẽ gửi các request và nhận về response từ `origin server`.

Sử khác biệt giữa forward proxy và reserve proxy khá nhỏ nhưng quan trọng. Một cách hiểu đơn giản là:

- Forward Proxy: nằm trước client và đảm bảo không có bất cứ server nào được giao tiếp trực tiếp với một số client cụ thể.
- Reserve Proxy: nằm trước origin server và đảm bảo không có bất cứ client nào có thể giao tiếp trực tiếp đến origin server.

Một lần nữa, để minh hoạ chúng ta đặt tên cho các máy tính có liên quan như sau:

- D: các máy tính ở Client
- E: Reserve Proxy server
- F: một hoặc nhiều origin server

<h4 style="text-align: center;">Forward Proxy Flow</h4>

![Reserve Proxy](/assets/img/reserve_proxy_flow.png "Reserve Proxy")

Thông thường, tất cả các request từ D sẽ gửi trực tiếp đến F, và F sẽ gửi các phản hồi ngược lại cho D. Với một reserve proxy, tất cả các request từ D sẽ gửi đến E, E sẽ gửi các request đến F và nhận các response từ F. E sẽ chuyển các response về lại cho D.

#### Lợi ích của Reserve Proxy

Dưới đây là một số lợi ích khi sử dụng reserve proxy:

- `Load balancing`: cân bằng tải - một website phổ biến với có hàng triệu lượt truy cập mỗi ngày có thể không xử lý được lưu lượng truy cập nếu chỉ có một server duy nhất. Thay vào đó nó có thể phân phối tài nguyên vào một nhóm nhiều server khác nhau để xử lý tất cả các request cho cùng một website. Trong trường hợp này, reserve proxy có thể cung cấp một giải pháp cân bằng tải bằng cách phân phối các request vào những server khác nhau để tránh tình trạng quá tải ở một server nào đó. Trong trường hợp một server bị lỗi, thì các server khác có thể thay thế để xử lý.

- Bảo vệ server trước các cuộc tấn công: với reserve proxy, một website hoặc service sẽ không bao giờ cần tiết lộ địa chỉ IP của origin server. Điều này khiến hacker sẽ gặp nhiều khó khăn hơn trong việc tấn công một server như `tấn công DDoS`. Thay vào đó, hacker chỉ có thể tấn công vào `reserve proxy`, ví dụ như Cloudfare CDN, những CDN này sẽ có bảo mật chặt chẽ hơn và nhiều nguồn lực hơn để chống lại các cuộc tấn công mạng.

- `Global server load balancing`: là một dạng cân bằng tải, một website có thể được phân bố trên nhiều server khắp toàn cầu và reserve proxy sẽ gửi request của client đến với server gần với vị trí địa lý của client nhất. Điều này giúp giảm khoảng cách để gửi request và nhận response, từ đó tối ưu được thời gian.

- `Caching`: một reserve proxy còn có khả năng cache content, trả về kết quả với hiệu suất nhanh hơn. Ví dụ, một user tại Paris vào một website có origin server đặt tại LA. User này phải kết nối với reserve proxy tại Paris, sau đó reserve proxy này sẽ kết nối với origin server tại LA. Proxy server có thể cache lại data của user này. Những user khác tại Paris nếu truy cập vào web sẽ nhận được data cache tại reserve proxy ở Paris, nhanh hơn nhiều so với user đầu tiên.

- `SSL encryption`: mã hoá và giải mã SSL (hoặc TLS) các giao tiếp cho mỗi client rất đắt đỏ nếu thực hiện trên origin server. Một reserve proxy có thể được cấu hình để giải mã tất cả các request từ client và mã hoá các response. Giải phòng các tài nguyên đắt tiền trên origin server.

#### Cách tích hợp một Reserve Proxy

Một số công ty tự xây dựng `reserve proxy` cho chính họ, nhưng việc này tốn rất nhiều nguồn nhân lực từ kỹ sư phần cứng đến phần mềm, cũng như chi phí đầu tư cho máy móc thiết bị. Một trong những cách dễ dàng và tốn ít chi phí nhất mà vẫn tận dụng được các lợi ích của reserve proxy đó là đăng ký một `CDN service`.

Ví dụ, `Cloudfare CDN` cung cấp tất cả những tính năng bảo mật và hiệu năng ở trên, cũng như một số tính năng khác.
