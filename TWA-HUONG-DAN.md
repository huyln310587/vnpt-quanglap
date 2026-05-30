# Hướng dẫn đóng gói PWA thành Android TWA

## 1. Cài công cụ

Cài:

- Node.js
- Java JDK
- Android Studio

Sau đó mở Terminal/CMD và chạy:

```bash
npm install -g @bubblewrap/cli
```

## 2. Khởi tạo project TWA

Sau khi website đã deploy xong và link manifest mở được, chạy:

```bash
bubblewrap init --manifest https://www.vnpt-quanglap.vn/manifest.webmanifest
```

Gợi ý thông tin khi Bubblewrap hỏi:

- Application name: `VNPT địa bàn Quảng Lập`
- Short name: `VNPT ĐB QL`
- Package name: `com.vnptdiabanquanglap.app`
- Host: `www.vnpt-quanglap.vn`
- Start URL: `/`
- Theme color: `#005baa`

## 3. Build thử

```bash
bubblewrap build
```

Sau khi build, Bubblewrap sẽ tạo project Android và thông tin signing key.

## 4. Tạo Digital Asset Links

Lấy SHA-256 fingerprint từ Bubblewrap, rồi tạo file:

```text
.well-known/assetlinks.json
```

Nội dung theo mẫu:

```json
[
  {
    "relation": ["delegate_permission/common.handle_all_urls"],
    "target": {
      "namespace": "android_app",
      "package_name": "com.vnptdiabanquanglap.app",
      "sha256_cert_fingerprints": [
        "DÁN_SHA256_FINGERPRINT_THẬT_VÀO_ĐÂY"
      ]
    }
  }
]
```

Upload file này lên GitHub đúng đường dẫn:

```text
.well-known/assetlinks.json
```

Chờ Vercel deploy rồi kiểm tra:

```text
https://www.vnpt-quanglap.vn/.well-known/assetlinks.json
```

## 5. Build file AAB để đưa lên CH Play

Sau khi Digital Asset Links hợp lệ, chạy lại:

```bash
bubblewrap build
```

File cần upload lên Google Play Console là file `.aab`.

## 6. Thông tin nên dùng khi tạo app trên CH Play

- Tên app: `VNPT địa bàn Quảng Lập`
- Mô tả ngắn: `Cung cấp dịch vụ và sửa chữa kỹ thuật VNPT địa bàn Quảng Lập`
- Link chính sách quyền riêng tư: `https://www.vnpt-quanglap.vn/privacy.html`
