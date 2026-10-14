# Chuyển CSS có sẵn sang Sass/SCSS

## Cấu trúc thư mục

```text
sass-conversion/
├── abstracts/
│   ├── _mixins.scss
│   └── _variables.scss
├── base/
│   └── _global.scss
├── components/
│   ├── _buttons.scss
│   └── _cards.scss
├── layout/
│   └── _container.scss
├── index.html
├── main.scss
├── main.css
└── original.css
```

- `abstracts/_variables.scss`: màu sắc, bóng đổ và thông số dùng chung.
- `abstracts/_mixins.scss`: mixin cấu hình nút và box-shadow.
- `base/_global.scss`: kiểu chữ, màu chữ và nền trang.
- `layout/_container.scss`: bố cục container, có nesting media query cho màn hình nhỏ.
- `components/_buttons.scss`: nút sử dụng mixin và nested `&:hover`.
- `components/_cards.scss`: card sử dụng biến và mixin.
- `main.scss`: entry point nạp các partial bằng `@use` của Dart Sass hiện đại.
- `original.css`: stylesheet ban đầu để đối chiếu.
- `main.css`: CSS được Sass CLI biên dịch.

## Cài đặt và chạy

Node.js và npm cần được cài đặt trước. Từ Terminal, mở thư mục `sass-conversion` rồi chạy:

```powershell
npm install
npm run build
```

`npm run build` tương đương lệnh:

```powershell
npx sass main.scss main.css
```

Để tự biên dịch khi SCSS thay đổi:

```powershell
npm run watch
```

Sau đó mở `index.html` trong trình duyệt để xem kết quả. Dùng `Ctrl+C` để dừng watch.
