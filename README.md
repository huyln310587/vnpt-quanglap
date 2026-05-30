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
