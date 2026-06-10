# VNPT địa bàn Quảng Lập - Bộ web PWA

Bộ này dùng để chạy website như ứng dụng trên điện thoại và chuẩn bị đóng gói thành app Android bằng TWA/Bubblewrap.

## File trong gói

- `index.html`: website chính.
- `manifest.webmanifest`: khai báo PWA.
- `sw.js`: service worker.
- `icon-192.png`: icon PWA 192x192.
- `icon-512.png`: icon PWA 512x512.
- `offline.html`: trang mất kết nối.
- `privacy.html`: chính sách quyền riêng tư.
- `TWA-HUONG-DAN.md`: hướng dẫn đóng gói TWA.
- `.well-known/assetlinks.template.json`: mẫu Digital Asset Links cho TWA.

## Cách upload lên GitHub/Vercel

Upload toàn bộ các file và thư mục trong gói này lên repository GitHub đang kết nối Vercel.

Sau khi Vercel deploy xong, kiểm tra các link:

- https://www.vnpt-quanglap.vn/manifest.webmanifest
- https://www.vnpt-quanglap.vn/sw.js
- https://www.vnpt-quanglap.vn/privacy.html
- https://www.vnpt-quanglap.vn/icon-512.png

## Kiểm tra PWA trên điện thoại Android

1. Mở Chrome trên điện thoại.
2. Vào https://www.vnpt-quanglap.vn/
3. Bấm menu dấu ba chấm.
4. Chọn `Thêm vào màn hình chính` hoặc `Cài đặt ứng dụng`.
5. Mở icon VNPT địa bàn Quảng Lập trên màn hình điện thoại.


## Cập nhật icon

- Đã đổi nội dung icon thành `QUANG LAP`
- Thêm họa tiết hoa phượng rơi ở hai bên viền icon


## Chức năng gửi vị trí

Website đã thêm mục `Gửi vị trí hỗ trợ kỹ thuật`.

Khách hàng có thể:
- Bấm `Lấy vị trí hiện tại`.
- Sao chép link Google Maps.
- Gửi link qua Zalo cho nhân viên phụ trách khu vực.

Chức năng này dùng Geolocation API của trình duyệt, cần khách hàng bấm cho phép quyền vị trí.


## Bản không có thư mục .well-known

Bản ZIP này đã bỏ thư mục `.well-known` để dễ upload lên GitHub bằng giao diện web.

Hiện tại để chạy PWA trên điện thoại chỉ cần các file:

- index.html
- manifest.webmanifest
- sw.js
- icon-192.png
- icon-512.png
- offline.html
- privacy.html

File `assetlinks-template-for-later.json` chỉ dùng sau này khi làm TWA/CH Play.


## Cập nhật vị trí mục gửi tọa độ

- Đã chuyển mục `Gửi vị trí cho nhân viên phụ trách` xuống ngay bên dưới 4 ô khu vực liên hệ.
- Khách hàng xem nhân viên phụ trách trước, sau đó mới dùng chức năng lấy vị trí và gửi Google Maps qua Zalo.


## Đổi vị trí phần hướng dẫn và gửi vị trí

- Đã đưa mục `Gửi vị trí cho nhân viên phụ trách` lên ngay sau danh sách 4 khu vực.
- Đã chuyển phần `Khách hàng cần sửa chữa / Khách hàng cần đăng ký mới / Cần hỗ trợ ngay` xuống dưới mục gửi vị trí.


## Cập nhật phần gửi vị trí dễ dùng hơn

Phần gửi vị trí đã được làm lại theo quy trình đơn giản:

1. Chọn khu vực.
2. Chọn Kỹ Thuật Địa Bàn hoặc Kinh Doanh Địa Bàn.
3. Bấm `Lấy vị trí & mở Zalo`.
4. Website tự sao chép link Google Maps và mở Zalo đúng nhân viên phụ trách.
5. Khách hàng chỉ cần dán nội dung vào Zalo và gửi.


## Mẫu câu gửi tọa độ

Phần gửi vị trí đã thêm sẵn mẫu câu. Khi khách bấm nút, website sẽ:

1. Lấy tọa độ hiện tại.
2. Tạo link Google Maps.
3. Tạo sẵn nội dung tin nhắn.
4. Sao chép nội dung vào bộ nhớ tạm.
5. Mở Zalo đúng nhân viên phụ trách để khách dán và gửi.


## Đổi vị trí khu vực và gửi tọa độ

- Đã đưa phần `4 khu vực nhân viên địa bàn` lên trên.
- Đã chuyển phần `Gửi tọa độ hỗ trợ kỹ thuật` xuống ngay bên dưới 4 khu vực.


## Đổi vị trí gửi tọa độ lên trên

- Đã đưa phần `Gửi tọa độ hỗ trợ kỹ thuật` lên trên.
- Phần `4 khu vực nhân viên địa bàn` nằm ngay bên dưới phần gửi tọa độ.


## Bỏ Zalo Mr.Tri Toàn

- Đã bỏ nút Zalo của nhân viên Mr.Tri Toàn thuộc khu vực Ka Đô.
- Vẫn giữ số điện thoại và nút Gọi: 0916270682.
- Trong phần gửi tọa độ, nếu chọn Kinh Doanh Địa Bàn Ka Đô thì không mở Zalo sai.


## Cập nhật số Zalo Mr.Tri Toàn

- Đã đổi số Mr.Tri Toàn thành `0916290682`.
- Đã thêm lại nút Zalo đúng theo số `0916290682`.
- Nút gọi và Zalo đều dùng số mới.


## Hiện lại Zalo Mr.Tri Toàn

- Đã sửa trực tiếp thẻ nhân viên Mr.Tri Toàn để hiện đủ 2 nút:
  - Gọi: 0916290682
  - Zalo: https://zalo.me/0916290682


## Bản sửa lỗi mất ảnh nhân viên

- Dựng lại từ bản ổn định có đủ ảnh nhân viên.
- Giữ số/Zalo Mr.Tri Toàn: 0916290682.
- Thêm lại phần tăng tương tác nhưng không thay đổi cấu trúc thẻ ảnh nhân viên.


## Đăng ký lắp mạng thêm kỹ thuật

- Phần `Đăng ký lắp đặt nhanh` đã thêm lựa chọn người nhận:
  - Kinh Doanh Địa Bàn
  - Kỹ Thuật Địa Bàn
  - Cả Kinh Doanh + Kỹ Thuật
- Toàn bộ số điện thoại/Zalo nhân viên giữ nguyên theo danh sách đã chốt 100%.
