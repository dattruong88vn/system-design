# CDN

## CDN là gì?

CDN là cụm từ viết tắt của `content delivery network` (mạng phân phối nội dung). CDN là một nhóm máy chủ (server) được phân bố theo vị trí địa lý, có nhiệm vụ cache content gần với vị trí của user. Một CDN cho phép trung chuyển các loại dữ liệu cần thiết của một website một cách nhanh chóng như HTML page, Javascript file, stylesheet (CSS file), hình ảnh và video.

Sự phổ biến của các service CND ngày càng được mở rộng, và ngày nay phần lớn các truy cập website đều được quản lý thông qua CDN, kể cả những website lớn như Facebook, Netflix hay Amazone.

CDN nếu được cấu hình đúng cách còn giúp ngăn chặn các cuộc tấn công mạng phổ biế, ví dụ như cuộc tấn công từ chối dịch vụ phân tán (`DDoS`) nhắm mục tiêu vào các website và máy chủ qua việc gây gián đoạn các dịch vụ mạng.

## CDN có giống với một Web Host?

Mặc dù CDN không lưu trữ nội dung và không thể thay thế web host, nhưng nó giúp cache content (lưu trữ nội dung) ở `network edge`, tăng hiệu suất trang web. Nhiều trang web gặp khó khăn trong việc đáp ứng nhu cầu hiệu suất khi sử dụng các host service truyền thống, đó là lý do họ chọn CDN.

Bằng cách sử dụng cache (bộ nhớ đệm) để giảm băng thông lưu trữ, giúp ngăn chặn sự gián đoạn dịch vụ và cải thiện bảo mật, CDN là một lựa chọn phổ biến để hạn chế những điểm yếu của các dịch vụ lưu trữ truyền thống.

## Những lợi ích khi sử dụng CDN

Mặc dù các lợi ích khi sử dụng CDN phụ thuộc vào kích thước và nhu cầu của các yếu tố Internet, thì những lợi ích hàng đầu cho phần lớn người dùng có thể chia ra như sau:

- Giảm thời gian tải trang web

- Giảm chi phí băng thông: bằng việc giảm số lượng request lên web server, thay vào đó sử dụng cache từ CDN sẽ giảm chi phí băng thông cho request gửi lên server.

- Tăng tính khả dụng và dự phòng của web: sử dụng CDN hạn chế server bị quá tải (do phân bố ra nhiều CDN khác nhau gần với vị trí của user), đồng thời hạn chế bị gián đoạn khi có một server bị lỗi (các server khác sẵn sàng thay thế).

- Tăng bảo mật cho website: ngăn chặn các cuộc tấn công mạng vì hacker không lấy được địa chỉ IP của server, thay vào đó là IP của CDN.

## CDN hoạt động như thế nào?

Theo định nghĩa, CDN là một mạng lưới nhiều server được liên kết với nhau với mục đích truyền tại nội dung một cách nhanh chóng, giá rẻ, đáng tin cậy và bảo mật cao nhất có thể. Để nâng cao tốc độ và khả năng kết nối, một CDN sẽ đặt các máy chụ tại điểm giao của các network khác nhau (được gọi là `Internet Exchange Point - IXPs`).

Những IXPs này là những vị trí chính để các nhà cung cấp Internet kết nối với nhau, từ đó cung cấp cho nhau các quyền truy cập đến các nguồn truy cập trong các mạng khác nhau của họ. Bằng cách kết nối đến các vị trí có tốc độ và tính kết nối cao này, một nhà cung cấp CDN có thể giảm chi phí và thời gian khi phân phối dữ liệu ở tốc độ cao.

![Reserve Proxy](/assets/img/cdn_distributed_server_map.png "Reserve Proxy")

Ngoài đặt máy chủ tại các IXPs, CDN còn thực hiện một số tối ưu hoá trong việc truyền dữ liệu tiêu chuẩn giữa clien và server. CDN đặt các trung tâm dữ liệu (Data Center) tại các vị trí chiến lược trên toàn cầu, tăng cường bảo mật, được thiết kế để tồn tại khi xuất hiện nhiều loại lỗi cũng như bị tắc nghẽn internet.

**_Link refer: (https://www.cloudflare.com/learning/cdn/what-is-a-cdn/)_**
