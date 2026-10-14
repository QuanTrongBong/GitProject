# Thực hành cài đặt và sử dụng Sass CLI

## Kiểm tra công cụ

Node.js và npm đã được kiểm tra trong môi trường phát triển:

```text
node -v  → v24.19.0
npm -v   → 11.17.0
```

Sass CLI được cài cục bộ trong dự án để có phiên bản nhất quán, không cần quyền quản trị:

```powershell
npm install
npx sass --version
```

## Biên dịch một tệp SCSS

```powershell
npx sass scss/styles.scss css/styles.css
```

Lệnh đọc `scss/styles.scss`, biên dịch SCSS và ghi CSS ra `css/styles.css`.

## Theo dõi thay đổi

```powershell
npx sass --watch scss/:css/
```

Sass theo dõi thư mục nguồn và biên dịch lại các tệp khi nội dung SCSS thay đổi. Dừng chế độ watch bằng `Ctrl+C`.

## Biên dịch nhiều tệp

```powershell
npx sass scss/:css/
```

Tất cả SCSS không phải partial trong `scss/` được biên dịch sang `css/` với tên tương ứng. Tệp partial `_tokens.scss` chỉ cung cấp biến/mixin cho `@use`, không tạo CSS đầu ra riêng.

Các lệnh tương đương qua npm scripts:

```powershell
npm run build
npm run watch
```

## Cấu trúc

- `scss/_tokens.scss`: biến màu và mixin dùng chung.
- `scss/styles.scss`, `scss/components.scss`: hai entry point SCSS.
- `css/styles.css`, `css/components.css`: CSS được sinh ra và dùng bởi trang mẫu.
- `index.html`: minh họa kết quả.

## Ghi chú cài đặt

Không cần chạy `Set-ExecutionPolicy Unrestricted`. Nếu PowerShell chặn script shim npm, hãy dùng `npm.cmd` thay cho `npm` hoặc mở Command Prompt; tránh nới lỏng Execution Policy toàn hệ thống.
