# Template Web Page — tái cấu trúc bằng Sass

Trang HTML/CSS template được tổ chức lại thành SCSS với variables, mixins, nesting và partials.

## Cấu trúc

```text
template-page-sass/
├── abstracts/
│   ├── _mixins.scss
│   └── _variables.scss
├── assets/
│   ├── laptop.svg
│   └── logo.svg
├── base/
│   └── _reset.scss
├── components/
│   └── _buttons.scss
├── layout/
│   ├── _footer.scss
│   ├── _navigation.scss
│   └── _sections.scss
├── index.html
├── main.scss
└── main.css
```

- `abstracts/_variables.scss`: màu sắc, font và kích thước giao diện.
- `abstracts/_mixins.scss`: kiểu căn giữa Flexbox và nút dùng lại.
- `layout/` và `components/`: style theo từng vùng và component; selector con được lồng bằng nesting.
- `main.scss`: entry point nạp partials bằng `@use`.
- `main.css`: CSS biên dịch để trang HTML sử dụng.

## Build

```powershell
npm install
npm run build
```

Để tự biên dịch khi thay đổi SCSS:

```powershell
npm run watch
```

Mở `index.html` trong trình duyệt để xem trang.
