# How to use XML

XML được sử dụng ở nhiều khía cạnh khác nhau của Web development.
XML thường được sử dụng để phần tách dữ liệu ra khỏi bản trình bày (presentation).

### XML tách dữ liệu khỏi presentation

XML không quan tâm đến việc dữ liệu sẽ được hiển thị như thế nào.
Cũng một dữ liệu XML thì có thể sử dụng với nhiều cách trình chiếu khác nhau.
Vì lý do này, với XML, đó là một sự tách biệt hoàn toàn giữa data và presentation.

### XML là một phần bổ sung cho HTML

Trong nhiều ứng dụng HTML, XML được sử dụng để lưu trữ và truyền tải dữ liệu. Trong khi HTML được sử dụng để định dạng và hiển thị dữ liệu.

### XML tách biệt dữ liệu khỏi HTML

Khi hiển thị dữ liệu trong HTML, bạn không nên edit file HTML khi dữ liệu thay đổi.

Với XML, data sẽ được lưu trữ trong một file riêng biệt. Và với một vài dòng code Javascript, bạn có thể đọc được dữ liệu từ file XML và update nội dung lên bất cứ page HTML nào.

Ví dụ về một file `.xml`:

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
    <title lang="en">XQuery Kick Start</title>
    <author>James McGovern</author>
    <author>Per Bothner</author>
    <author>Kurt Cagle</author>
    <author>James Linn</author>
    <author>Vaidyanathan Nagarajan</author>
    <year>2003</year>
    <price>49.99</price>
  </book>

  <book category="web" cover="paperback">
    <title lang="en">Learning XML</title>
    <author>Erik T. Ray</author>
    <year>2003</year>
    <price>39.95</price>
  </book>

</bookstore>
```

### Transaction Data

Hiện nay đã có rất nhiều định dạng XML đã ra đời, tương ứng với nhiều ngành nghề khác nhau để mô tả những dữ liệu hàng ngày.

- Cổ phiếu
- Giao dịch tài chính
- Dữ liệu Y tế
- Dữ liệu toán học
- Đo lường khoa học
- Thông tin, tin tức
- Dịch vụ thời tiết

###### Ví dụ XML tin tức

```
<?xml version="1.0" encoding="UTF-8"?>
<nitf>
  <head>
    <title>Colombia Earthquake</title>
  </head>
  <body>
    <headline>
      <hl1>143 Dead in Colombia Earthquake</hl1>
    </headline>
    <byline>
      <bytag>By Jared Kotler, Associated Press Writer</bytag>
    </byline>
    <dateline>
      <location>Bogota, Colombia</location>
      <date>Monday January 25 1999 7:28 ET</date>
    </dateline>
  </body>
</nitf>
```

###### Ví dụ XML thời tiết

```
<?xml version="1.0" encoding="UTF-8"?>
<current_observation>

<credit>NOAA's National Weather Service</credit>
<credit_URL>http://weather.gov/</credit_URL>

<image>
  <url>http://weather.gov/images/xml_logo.gif</url>
  <title>NOAA's National Weather Service</title>
  <link>http://weather.gov</link>
</image>

<location>New York/John F. Kennedy Intl Airport, NY</location>
<station_id>KJFK</station_id>
<latitude>40.66</latitude>
<longitude>-73.78</longitude>
<observation_time_rfc822>Mon, 11 Feb 2008 06:51:00 -0500 EST
</observation_time_rfc822>

<weather>A Few Clouds</weather>
<temp_f>11</temp_f>
<temp_c>-12</temp_c>
<relative_humidity>36</relative_humidity>
<wind_dir>West</wind_dir>
<wind_degrees>280</wind_degrees>
<wind_mph>18.4</wind_mph>
<wind_gust_mph>29</wind_gust_mph>
<pressure_mb>1023.6</pressure_mb>
<pressure_in>30.23</pressure_in>
<dewpoint_f>-11</dewpoint_f>
<dewpoint_c>-24</dewpoint_c>
<windchill_f>-7</windchill_f>
<windchill_c>-22</windchill_c>
<visibility_mi>10.00</visibility_mi>

<icon_url_base>http://weather.gov/weather/images/fcicons/</icon_url_base>
<icon_url_name>nfew.jpg</icon_url_name>
<disclaimer_url>http://weather.gov/disclaimer.html</disclaimer_url>
<copyright_url>http://weather.gov/disclaimer.html</copyright_url>

</current_observation>
```
