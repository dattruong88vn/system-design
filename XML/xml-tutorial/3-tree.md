# XML Tree

Các văn bản XML đề có dạng sơ đồ cây, bắt đầu từ gốc (root) và phần nhánh.

### Cấu trúc XML tree

![XML tree](/XML/nodetree.gif "XML tree")

### Một ví dụ về XML Document

Hình ảnh trên thể hiện những cuốn sách nằm trong file sau:

```
<?xml version="1.0" encoding="UTF-8"?>
<bookstore>
  <book category="cooking">
    <title lang="en">Everyday Italian</title>
    <author>Giada De Laurentiis</author>
    <year>2005</year>
    <price>30.00</price>
  </book>
  <book category="children">
    <title lang="en">Harry Potter</title>
    <author>J K. Rowling</author>
    <year>2005</year>
    <price>29.99</price>
  </book>
  <book category="web">
    <title lang="en">Learning XML</title>
    <author>Erik T. Ray</author>
    <year>2003</year>
    <price>39.95</price>
  </book>
</bookstore>
```

### Cấu trúc của một file XML

Các văn bản XML được định dạng theo một sơ đồ cây các phần tử. Nó được bắt đầu từ `root element` và phân nhánh từ root đến các `child elements`.

Tất cả các phần tử đều có thể có phần tử con bên trong nó.

```
<root>
  <child>
    <subchild>.....</subchild>
  </child>
</root>
```

Các thuật ngữ "parent", "child", "sibling" dùng để mô tả mối quan hệ giữa các phần tử.

Tất cả các phần tử đều có thể có `text content` và các thuộc tính (ví dụ như categories).

### Self Describing Syntax

XML sử dụng cú pháp tự mô tả khá nhiều.

Một prolog xác định phiên bản XML và mã hoá ký tự: `<?xml version="1.0" encoding="UTF-8"?>`

Dòng tiếp theo sẽ là root element: `<bookstore>`. Tiếp theo là các phần tử con.
