# DDoS Attack

## DDoS Attack là gì?

DDoS Attack là cuộc tấn công từ chối dịch vụ phân tán, nhằm phá vỡ lưu lượng truy cập bình thường của một server, service hoặc network. Nó làm tăng đột biến lưu lượng truy cập để làm tắc nghẽn mục tiêu và các cơ sở hạ tầng.

Để thực hiện DDoS, phải sử dụng nhiều hệ thống máy tính cùng lúc truy cập vào server để làm tăng đột biến lưu lượng. Có thể liên tưởng tấn công DDoS như một vụ ùn tắc giao thông bất ngờ làm tắc nghẽn đường phố, ngăn cản các phương tiện khác di chuyển đến đích.

![DDoS Attack](/assets/img/ddos_attack_traffic_metaphor.png "DDoS Attack")

## DDoS Attack hoạt động như thế nào?

Các cuộc tấn công DDoS thường được thực hiện với mạng lưới các máy tính được liên kết với nhau.

Các mạng này bao gồm các máy tính và các thiết bị khác (chẳng hạn như `IoT`) đã bị nhiễm phần mềm độc hại, cho phép chúng điều khiển từ xa. Những thiết bị riêng lẻ này được gọi là `bot` (hoặc `zombie`), và một nhóm bot được gọi là `botnet`.

Khi mạng botnet được thiết lập, kẻ tấn công có thể chỉ đạo một cuộc tấn công bằng cách gửi các hướng dẫn từ xa đến từng bot.

Khi máy chủ hoặc mạng của nạn nhân bị botnet nhắm làm mục tiêu, mỗi bot sẽ gửi yêu cầu đến địa chỉ IP của mục tiêu, có thể khiến máy chủ hoặc mạng bị quá tải, dẫn đến từ chối dịch vụ đối với lưu lượng truy cập thông thường (là khách hàng thực tế).

Vì mỗi bot là một thiết bị Internet hợp lệ, nên việc nhận dạng bot với các truy cập thông thường rất khó khăn.

## Cách xác định một cuộc tấn công DDoS

Biểu hiện rõ ràng nhất khi bị tấn công DDoS là trang web hoặc service trở nên chậm hoặc không khả dụng. Tuy nhiên, một số nguyên nhân khác (lưu lượng tăng đột biến một cách chính đáng như sau khi chạy quản cáo) cũng có thể gây ra vấn đề tương tự nên cần điều tra thêm. Các công cụ phân tích lưu lượng truy cập có thể giúp bạn nhận diện một cuộc tấn công DDoS.

- Lưu lượng truy cập đáng ngờ từ một địa chỉ IP hoặc một dải IP.
- Lưu lượng truy cập khổng lồ từ những người dùng có chung một hồ sơ hành vi như thiết bị, vị trí địa lý, hoặc phiên bản trình duyệt web.
- Sự gia tăng không giải thích được về số lượng request tới một page hoặc một endpoint.
- Các kiểu lưu lượng truy cập kỳ lạ như tăng vào các giờ lẻ trong ngày, hoặc các kiểu tăng không tự nhiên (Ví dụ: cứ sau 10 phút tăng đột biến).
- Những dấu hiệu cụ thể khác tuỳ thuộc vào loại tấn công.

## Các kiểu tấn công DDoS phổ biến là gì?

Các kiểu tấn công DDoS khác nhau sẽ nhằm vào các thành phần khác nhau của kết nối mạng. Để hiểu các loại tấn công DDoS khác nhau thì phải cần hiểu kết nối mạng được thực hiện như thế nào.

Một kết nối mạng bao nhiều nhiều thành phần (hoặc được gọi là lớp - `layer`) khác nhau. Giống như xây nhà, mỗi lớp sẽ có mục đích và tác dụng khác nhau.

Mô hình `OSI` được hiển thị trong hình ảnh bên dưới là một khung khái niệm để mô tả kết nối mạng theo 7 lớp riêng biệt

![OSI model](/assets/img/osi_model_7_layers.png "OSI model")

- Tầng 1: Tầng vật lý (Physical Layer)
- Tầng 2: Tầng liên kết dữ liệu (Data-Link Layer)
- Tầng 3: Tầng mạng (Network Layer)
- Tầng 4: Tầng giao vận (Transport Layer)
- Tầng 5: Tầng phiên (Session layer)
- Tầng 6: Tầng trình diễn (Presentation layer)
- Tầng 7: Tầng ứng dụng (Application layer)

Gần như tất cả các cuộc tấn công DDoS đều liên quan đến việc áp đảo lưu lượng truy cập vào server hoặc network, nhưng có thể chia làm 3 loại. Kẻ tấn công có thể sử dụng một hoặc nhiều vector tấn công khác nhau, hoặc sử dụng vector chu kỳ tấn công để khắc chế lại các biện pháp phòng chống của mục tiêu.

#### Application Layer Attack

###### Mục tiêu tấn công

Còn được gọi là tấn công DDoS layer 7 (do liên quan đến layer thứ 7 của mô hình OSI), mục tiêu của loại tấn công này là làm cạn kiệt tài nguyên của mục tiêu để xảy ra tình trạng từ chối phục vụ (truy cập không khả dụng).

Các cuộc tấn công nhằm vào layer nơi các web pages được tạo ra trên máy chủ và phân phối để phản hồi lại các HTTP request. Một HTTP request có thể tốn ít chi phí ở phía client, nhưng lại tốn nhiều chi phí ở server để có thể phản hồi, vì server thường phải tải nhiều file cũng như truy vấn cơ sở dữ liệu để có thể tạo ra trang web.

Các cuộc tấn công layer 7 thường rất khó chống vì khó có thể phân biệt được lưu lượng truy cập thông thường và lưu lượng truy cập của kẻ tấn công.

![DDoS Attack layer 7](/assets/img/application_layer_ddos_example.png "DDoS Attack layer 7")

###### HTTP Flood

Đây là một dạng tấn công của DDoS Attack Layer 7, nó tương tự như việc nhấn `refresh` liên tục trên trình duyệt, trên nhiều máy tính khác nhau cùng lúc, số lượng request HTTP tràn ngập máy chủ, dẫn đến từ chối dịch vụ.

Kiểu tấn công này có phạm vi từ đơn giản đến phức tạp.

Đơn giản nhất là truy cập vào cùng 1 URL với cùng 1 dải địa chỉ IP, referrer hoặc user agent. Phức tạp hơn là có thể sử dụng một số lượng lớn địa chỉ IP, và các URL mục tiêu ngẫu nhiên bằng cách sử dụng referrer hoặc user agent ngẫu nhiên.

#### Protocal Attack

###### Mục tiêu tấn công

Protocol attack là loại tấn công nhắm vào tập trung vào việc khai thác nguồn tài nguyên của máy chủ. Tấn công này tập trung vào các lỗ hổng ở Layer 3 hoặc Layer 4 của mô hình Kết nối hệ thống mở (OSI). Điều đó có nghĩa là chúng sẽ sử dụng hết bộ nhớ, các lõi xử lý, hoặc làm quá tải nguồn thiết bị hoặc các mạng lưới giữa hệ thống bị nhắm đến và người dùng ở đầu kia. Protocol attack bao gồm các phương thức tấn công phổ biến như: SYN floods, Ping of death, Smurf, Teardrop...

![DDoS Attack Protocol](/assets/img/syn_flood_ddos_example.png "DDoS Attack Protocol")

###### SYN flood

_(Đang cập nhật)_

#### Volume-based Attack

###### Mục tiêu tấn công

Volume-based attack là kiểu tấn công DDoS phổ biến nhất và hoạt động bằng cách áp đảo khả năng của máy chủ với một lượng lớn yêu cầu dữ liệu sai. Kẻ tấn công thường sẽ vận dụng các kỹ thuật khuếch đại để sinh ra các request mà không cần dùng đến một lượng lớn tài nguyên. Trong khi máy chủ bận rộn với việc kiểm tra các yêu cầu dữ liệu độc hại này, các lưu lượng truy cập hợp lệ không thể đi qua. Volume-base attack bao gồm các phương thức tấn công phổ biến như: UDP flood, ICMP flood,...

![DDoS Volume-based Attack ](/assets/img/amplification_ddos_example.png "DDoS Volume-based Attack ")

###### DNS Amplification

_(Đang cập nhật)_

**Còn một số khái niệm khác chưa tìm hiểu thêm. Có thể tham khảo tại: _https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/_**
