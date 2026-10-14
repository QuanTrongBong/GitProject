# Responsive Grid — tái cấu trúc CSS sang Sass

Bài thực hành lấy cấu trúc mẫu từ [codegym-vn/responsive-grid](https://github.com/codegym-vn/responsive-grid) và chuyển style inline/CSS thành SCSS có tổ chức.

## Cấu trúc

```text
responsive-grid-sass/
├── abstracts/
│   ├── _mixins.scss
│   └── _variables.scss
├── base/
│   └── _reset.scss
├── layout/
│   └── _grid.scss
├── css/
│   └── main.css
├── main.scss
├── responsive_grid.html
└── package.json
```

- `abstracts/_variables.scss`: bảng màu, số cột, kích thước và opacity.
- `abstracts/_mixins.scss`: mixins cho hàng, cột, dải màu và đường kẻ grid.
- `base/_reset.scss`: box sizing, khoảng lề và font cơ bản.
- `layout/_grid.scss`: các class layout, component con bằng nesting, cùng breakpoint mobile.
- `main.scss`: entry point, nạp partial bằng `@use`.
- `responsive_grid.html`: HTML không còn style inline; stylesheet được biên dịch đặt tại `css/main.css`.

## Cài đặt, build và watch

Mở Terminal ở thư mục này:

```powershell
npm install
npm run build
```

Biên dịch tự động khi SCSS đổi:

```powershell
npm run watch
```

Lệnh Sass CLI tương đương:

```powershell
npx sass main.scss css/main.css
```

Mở `responsive_grid.html` trong trình duyệt và thay đổi kích thước cửa sổ để kiểm tra lưới.
