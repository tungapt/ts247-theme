# Hướng Dẫn Sử Dụng Các Component

Thư viện SCSS cung cấp một số component giao diện phổ biến, được tối ưu hóa và dễ sử dụng trong HTML. Dưới đây là hướng dẫn chi tiết cách sử dụng từng component:

---

## 1. Buttons
Buttons là thành phần cơ bản, có nhiều kiểu dáng và trạng thái để sử dụng.

### Cách sử dụng
```html
<button class="btn btn-primary">Primary Button</button>
<button class="btn btn-secondary">Secondary Button</button>
<button class="btn btn-outline">Outline Button</button>
```

### Các class hỗ trợ
- `btn-primary`: Nút màu chính.
- `btn-secondary`: Nút màu phụ.
- `btn-outline`: Nút viền, không nền.
- `btn-lg`, `btn-sm`: Điều chỉnh kích thước lớn hoặc nhỏ.

---

## 2. Navbar
Navbar là thành phần thanh điều hướng, hỗ trợ responsive.

### Cách sử dụng
```html
<nav class="navbar">
  <div class="navbar-brand">Brand</div>
  <ul class="navbar-nav">
    <li class="nav-item"><a href="#" class="nav-link">Home</a></li>
    <li class="nav-item"><a href="#" class="nav-link">About</a></li>
    <li class="nav-item"><a href="#" class="nav-link">Contact</a></li>
  </ul>
</nav>
```

### Các class hỗ trợ
- `navbar`: Phần tử gốc.
- `navbar-brand`: Thương hiệu hoặc logo.
- `navbar-nav`: Danh sách điều hướng.
- `nav-item`: Mỗi mục trong danh sách.
- `nav-link`: Liên kết trong điều hướng.

---

## 3. Cards
Cards là thành phần giao diện dùng để hiển thị thông tin theo bố cục hộp.

### Cách sử dụng
```html
<div class="card">
  <div class="card-header">Card Header</div>
  <div class="card-body">This is the card body.</div>
  <div class="card-footer">Card Footer</div>
</div>
```

### Các class hỗ trợ
- `card`: Phần tử gốc của card.
- `card-header`: Phần đầu của card.
- `card-body`: Nội dung chính của card.
- `card-footer`: Phần chân của card.

---

## 4. Modals
Modals là hộp thoại xuất hiện trên giao diện để hiển thị thông tin hoặc yêu cầu người dùng thực hiện hành động.

### Cách sử dụng
```html
<div class="modal">
  <div class="modal-header">
    <h5 class="modal-title">Modal Title</h5>
    <button class="modal-close">&times;</button>
  </div>
  <div class="modal-body">
    This is the content of the modal.
  </div>
  <div class="modal-footer">
    <button class="btn btn-secondary">Close</button>
    <button class="btn btn-primary">Save changes</button>
  </div>
</div>
```

### Các class hỗ trợ
- `modal`: Phần tử gốc của modal.
- `modal-header`: Phần đầu của modal.
- `modal-title`: Tiêu đề modal.
- `modal-close`: Nút đóng modal.
- `modal-body`: Nội dung chính của modal.
- `modal-footer`: Phần chân của modal.

---

## 5. Grid
Grid là hệ thống lưới giúp sắp xếp nội dung theo hàng và cột.

### Cách sử dụng
```html
<div class="row">
  <div class="col col-4">Column 1</div>
  <div class="col col-4">Column 2</div>
  <div class="col col-4">Column 3</div>
</div>
```

### Các class hỗ trợ
- `row`: Phần tử gốc của hàng.
- `col`: Phần tử gốc của cột.
- `col-1` đến `col-12`: Định nghĩa độ rộng của cột theo tỷ lệ 12.

---

## 6. Utilities
Utilities là các class nhỏ giúp bạn áp dụng style nhanh chóng mà không cần viết CSS.

### Cách sử dụng
```html
<div class="m-3 p-2 bg-primary text-white">Utility Example</div>
```

### Các class phổ biến
- Khoảng cách:
  - `m-{n}`: Margin, ví dụ: `m-3`.
  - `p-{n}`: Padding, ví dụ: `p-2`.
- Màu sắc:
  - `bg-primary`, `bg-secondary`, `bg-light`, `bg-dark`.
  - `text-white`, `text-dark`, `text-muted`.
- Hiển thị:
  - `d-block`, `d-inline`, `d-flex`, `d-none`.

---

## Kết luận
Các component trên giúp bạn nhanh chóng xây dựng giao diện thống nhất và hiện đại. Tùy chỉnh thêm bằng cách override các class hoặc biến trong SCSS nếu cần thiết.
