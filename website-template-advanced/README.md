# Website Template nâng cao với Sass

Website mẫu responsive được xây dựng theo yêu cầu thực hành: hero có hình nền và lớp phủ, menu cố định, lưới card dịch vụ, hiệu ứng hover và footer hai cột.

## Cấu trúc

```text
website-template-advanced/
├── images/
│   ├── banner.svg
│   ├── service-design.svg
│   ├── service-growth.svg
│   └── service-support.svg
├── scss/
│   ├── abstracts/
│   ├── base/
│   ├── components/
│   ├── layout/
│   └── main.scss
├── css/style.css
├── index.html
└── package.json
```

- `scss/abstracts/`: variables, mixins và breakpoint dùng chung.
- `scss/layout/` và `scss/components/`: style được chia theo vùng giao diện; selectors được lồng bằng nesting.
- `css/style.css`: CSS biên dịch, được trang HTML sử dụng.
- `images/`: hình minh họa SVG cục bộ, không cần tải ảnh từ dịch vụ ngoài.

## Cài đặt và biên dịch

Trong Terminal, mở thư mục này rồi chạy:

```powershell
npm install
npm run build
```

Để Sass tự biên dịch mỗi khi có thay đổi:

```powershell
npm run watch
```

Mở `index.html` trong trình duyệt để xem website.
