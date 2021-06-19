# JavaScript Code Search Engine

Đồ án môn học Truy Tìm Thông Tin 2021

## Các bước chạy project

### 1. Index

Data được crawl bằng Scrapy, source code có thể được tìm thấy
tại [đây](https://github.com/ecin-tpk/CodeGrepperCrawler.git)  
Làm theo hướng dẫn trong file README để có thể crawl dữ liệu và index dữ liệu

### 2. Cấu hình CORS cho elasticsearch

Phiên bản elasticsearch đã sử dụng 7.12 hoặc 7.13  
Thêm những dòng sau vào file config/elasticsearch.yml

```
http.cors.enabled: true
http.cors.allow-origin: "*"
http.cors.allow-methods: OPTIONS,HEAD,GET,POST,PUT,DELETE
http.cors.allow-headers: "X-Requested-With,X-Auth-Token,Content-Type,Content-Length,Authorization"
```

Chạy elasticsearch server bằng cách mở file elasticsearch.bat

### 3. Cài đặt các thư viện

`yarn install` hoặc `npm install`

### 4. Chạy project React

`yarn start` hoặc `npm start`

Mở trình duyệt và truy cập [http://localhost:3000](http://localhost:3000).

## Các chức năng

1. Tìm kiếm câu hỏi javascript
2. Lọc nội dung tìm kiếm theo framework
3. Sắp xếp kết quả theo ngày đăng
4. Gợi ý kết quả tìm kiếm
5. Highlight đối với những từ giống với nội dung tìm kiếm
6. Phân trang
7. Xem nội dung sau khi tìm kiếm bao gồm: code javascript, ngày đăng, người đăng, các thẻ đánh dấu theo framework hoặc
   ngôn ngữ, nguồn liên kết cung cấp có thể nhấn vào để mở
