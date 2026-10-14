# Tối ưu CSS bằng Sass Variables và Mixins

## Cấu trúc dự án

```text
sass-mixins/
├── abstracts/
│   ├── _mixins.scss
│   └── _variables.scss
├── base/
│   └── _typography.scss
├── components/
│   ├── _buttons.scss
│   └── _cards.scss
├── index.html
├── main.scss
├── main.css
└── original.css
```

- `abstracts/_variables.scss` tập trung màu sắc, cỡ chữ, khoảng đệm, bo góc và bóng đổ.
- `abstracts/_mixins.scss` định nghĩa `button-style` và `box-style` để dùng lại.
- `base/_typography.scss` áp dụng biến cho tiêu đề.
- `components/_buttons.scss` và `_cards.scss` dùng mixins để tạo component.
- `main.scss` nạp các partial bằng cú pháp `@use` hiện đại.
- `original.css` lưu CSS ban đầu để đối chiếu; `main.css` là CSS được biên dịch.

## Cài đặt và chạy

Mở Terminal trong thư mục này rồi chạy:

```powershell
npm install
npm run build
```

Lệnh Sass CLI tương đương:

```powershell
npx sass main.scss main.css
```

Để tự biên dịch lại khi SCSS thay đổi:

```powershell
npm run watch
```

Mở `index.html` trong trình duyệt để xem kết quả. Dùng `Ctrl+C` để dừng chế độ watch.
