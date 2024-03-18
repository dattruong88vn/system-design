# Giới thiệu XML

### XML là gì?gì

- XML là viết tắt của từ eXtensible Markup Language.
- XML cũng là một markup language tương tự như HTML.
- XML được thiết kế để lưu trữ và truyền tải dữ liệu.
- XML được thiết kế để `tự mô tả chính nó`. (Chỗ này chưa hiểu lắm, sẽ bổ sung sau).
- XML được khuyến cáo sử dụng từ [W3C](https://viblo.asia/p/tim-hieu-ve-thiet-ke-web-chuan-w3c-924lJPVXKPM).

### XML thực sự ko làm gì cả (XML Does Not DO Anything)

Điều này có thể gây một chút khó hiểu, nhưng thực tế thì XML ko làm bất cứ điều gì.

Lưu ý sau là một lưu ý được gửi từ Jani cho Tove, được lưu trữ dưới dạng XML:

```
<note>
  <to>Tove</to>
  <from>Jani</from>
  <heading>Reminder</heading>
  <body>Don't forget me this weekend!</body>
</note>
```

Thông tin của đoạn XML trên mô tả chính nó:

- Nó có thông tin người gửi, người nhận
- Nó có heading
- Nó có mesage body

Thực tế XML ko làm gì cả, nó chỉ là thông tin được bọc trong các tags khác nhau.

Một số người có thể viết thêm các phần mềm để gửi, nhận lưu trữ và hiển thị nó.

### Sự khác nhau giữa XML và HTML

XML và HTML được tạo ra với những mục đích riêng:

- XML được thiết kế để mang theo dữ liệu, nó tập trung vào dữ liệu là gì.
- HTML được thiết kế để hiển thị dữ liệu, nó tập trung vào dữ liệu sẽ trông như thế nào.
- Các thẻ XML ko được định nghĩa trước như các thẻ HTML.

### XML KHÔNG sử dụng các thẻ được định nghĩa trước

Ngôn ngữ XML ko có các thẻ được định nghĩa trước.

Các thẻ trong ví dụ ở trên (như `<to>` hay `<from>`) không được định nghĩa theo bất kỳ tiêu chuẩn XML nào. Những thẻ này được phát minh bởi tác giả của văn bản XML đó.

HTML làm việc với các thẻ được định nghĩa sẵn. Trong khi đó với XML, tác giả sẽ phải định nghĩa các thẻ cũng như cấu trúc của văn bản.

### XML có thể mở rộng

Phần lớn các ứng dụng XML vẫn có thể hoạt động tốt ngay cả khi data được thêm hoặc xoá bớt khỏi văn bản.

Thử tưởng tượng, thiết kế một ứng dụng để hiển thị phiên bản gốc của file `note.xml` (<to>, <from>, <heading>, <body>).

Sau đó tưởng tưởng ra một phiên bản mới hơn của `note.xml` với các phần tử được thêm vào <date>, <hour> và bỏ ra phần tử <heading>.

Với cách XML được xây dựng, phiên bản cũ vẫn có thể hoạt động được.

```
<note>
  <date>2015-09-01</date>
  <hour>08:30</hour>
  <to>Tove</to>
  <from>Jani</from>
  <body>Don't forget me this weekend!</body>
</note>
```

### XML đơn giản hoá mọi thứ

- XML đơn giản hoá việc chia sẻ dữ liệu
- XML đơn giản hoá việc truyền tải dữ liệu
- XML đơn giản hoá việc thay đổi nền tảng
- XML đơn giản hoá tính sẵn có của dữ liệu

4 món này từ từ bổ sung thêm.

Nhiều hệ thống máy tính lưu trữ dữ liệu dưới các định dạng không tương thích với nhau. Trao đổi dữ liệu giữa các hệ thống không tương thích là một công việc tốn nhiều thời gian của Web Developer. Với số lượng lớn data cần phải chuyển đổi (convert), và data không tương thích thường xuyên bị mất.

XML lưu trữ dữ liệu dưới dạng văn bản thô (plain text). Điều này giúp cho phần cứng và phần mềm có thể độc lập trong cách lưu trữ, truyền tải và chia sẻ dữ liêụ.

XML cũng giúp quá trình nâng cấp lên các hệ điều hành, phiên bản ứng dụng hoặc trình duyệt mới một cách dễ dàng mà không làm mất dữ liệu.

Với XML, dữ liệu có thể dễ dàng truy xuất cho tất cả các loại "máy đọc" như con người, máy tính, máy thoại...

### XML được đề xuất sử dụng theo tiều chuẩn web W3C

XML được W3C đưa vào danh sách đề xuất sử dụng từ tháng 2 năm 1998.
