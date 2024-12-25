# Tài Liệu Hướng Dẫn Sử Dụng Thư Viện SCSS

## 1. Giới thiệu
Thư viện SCSS này được xây dựng nhằm cung cấp một tập hợp các tiện ích và thành phần giao diện thường dùng, lấy cảm hứng từ Bootstrap. File `main.scss` là tệp gốc, nơi các tệp SCSS thành phần khác được import để biên dịch thành CSS cuối cùng.

Thư viện này giúp bạn nhanh chóng xây dựng giao diện người dùng hiện đại với các tiện ích được tổ chức tốt, dễ tùy chỉnh và mở rộng.

---

## 2. Cài đặt
### Yêu cầu
- Trình biên dịch SCSS (Ví dụ: Dart Sass, Node Sass).

### Cách biên dịch
- Biên dịch `main.scss` thành CSS bằng câu lệnh:
  ```bash
  sass main.scss main.css
  ```

---

## 3. Cấu trúc thư viện
Thư viện được chia thành các module SCSS sau, mỗi module xử lý một nhóm tính năng cụ thể:

| **Module**       | **Chức năng**                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| `variables`       | Định nghĩa các biến màu sắc, font, khoảng cách, breakpoint, v.v.                              |
| `mixins`          | Chứa các mixin để tái sử dụng, như mixin cho responsive, text-shadow, hay button hover.       |
| `reset`           | Đặt lại các quy tắc mặc định của trình duyệt để đảm bảo sự đồng nhất trên các nền tảng.       |
| `typography`      | Định dạng văn bản, các kích thước font, khoảng cách dòng, và các tiện ích liên quan.          |
| `buttons`         | Tạo các kiểu nút với màu sắc, trạng thái (hover, active) và kích thước đa dạng.              |
| `forms`           | Cung cấp các style cho input, textarea, checkbox, radio button, v.v.                         |
| `grid`            | Hệ thống lưới 12 cột tương tự Bootstrap, hỗ trợ responsive.                                  |
| `flex`            | Cung cấp các tiện ích sử dụng Flexbox như căn chỉnh, sắp xếp, và sắp đặt layout.              |
| `navbar`          | Tạo thanh điều hướng với các tùy chọn responsive.                                             |
| `cards`           | Style cho card với header, body, footer.                                                     |
| `modals`          | Cung cấp các style cơ bản cho modal, hỗ trợ animation.                                        |
| `utilities`       | Bao gồm các tiện ích nhỏ như khoảng cách, hiển thị, màu sắc, v.v.                             |

---

## 4. Chi tiết từng module

### 4.1. Variables
- Định nghĩa các biến màu sắc, khoảng cách, breakpoint, font-family.
- Ví dụ:
  ```scss
  $primary-color: #007bff;
  $secondary-color: #6c757d;
  $spacing-unit: 1rem;
  ```

### 4.2. Mixins
- Tái sử dụng các đoạn mã CSS lặp lại.
- Ví dụ:
  ```scss
  @mixin center-flex {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  ```

### 4.3. Reset
- Đặt lại các thuộc tính mặc định của trình duyệt.
- Ví dụ:
  ```scss
  *,
  *::before,
  *::after {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  ```

### 4.4. Typography
- Style cho văn bản như font-size, line-height, text-align.
- Ví dụ:
  ```scss
  h1 {
    font-size: 2.5rem;
    font-weight: bold;
  }
  ```

### 4.5. Buttons
- Tạo các kiểu nút với trạng thái hover, focus.
- Ví dụ:
  ```scss
  .btn {
    padding: 0.5rem 1rem;
    border: none;
    background-color: $primary-color;
    color: #fff;
    &:hover {
      background-color: darken($primary-color, 10%);
    }
  }
  ```

### 4.6. Forms
- Style cho input, textarea, checkbox, radio button.
- Ví dụ:
  ```scss
  input {
    padding: 0.5rem;
    border: 1px solid $secondary-color;
    border-radius: 4px;
  }
  ```

### 4.7. Grid
- Hệ thống lưới 12 cột linh hoạt.
- Ví dụ:
  ```scss
  .row {
    display: flex;
    flex-wrap: wrap;
  }
  .col {
    flex: 1;
    padding: $spacing-unit;
  }
  ```

### 4.8. Flex
- Tiện ích cho Flexbox.
- Ví dụ:
  ```scss
  .d-flex {
    display: flex;
  }
  .justify-center {
    justify-content: center;
  }
  ```

### 4.9. Navbar
- Style cho thanh điều hướng.
- Ví dụ:
  ```scss
  .navbar {
    display: flex;
    background-color: $primary-color;
    padding: $spacing-unit;
  }
  ```

### 4.10. Cards
- Style cho card với các phần header, body, footer.
- Ví dụ:
  ```scss
  .card {
    border: 1px solid $secondary-color;
    border-radius: 4px;
    padding: $spacing-unit;
  }
  ```

### 4.11. Modals
- Style cơ bản cho modal.
- Ví dụ:
  ```scss
  .modal {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: #fff;
    padding: $spacing-unit;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  ```

### 4.12. Utilities
- Các tiện ích nhỏ như margin, padding, visibility.
- Ví dụ:
  ```scss
  .m-1 {
    margin: $spacing-unit;
  }
  .p-1 {
    padding: $spacing-unit;
  }
  .d-none {
    display: none;
  }
  ```

---

## 5. Hướng dẫn sử dụng

### Import thư viện
- Đảm bảo file `main.scss` đã được liên kết với dự án của bạn.
- Chèn file CSS biên dịch vào tệp HTML:
  ```html
  <link rel="stylesheet" href="main.css">
  ```

### Sử dụng các class có sẵn
- Áp dụng style bằng các class có sẵn trong thư viện.
- Ví dụ:
  ```html
  <div class="btn btn-primary">Click Me</div>
  <div class="d-flex justify-center">Centered Content</div>
  ```

### Tùy chỉnh
- Nếu cần tùy chỉnh thêm, bạn có thể override các biến trong file `variables.scss` hoặc thêm các class của riêng bạn.

---

## 6. Mở rộng và tùy chỉnh
- Thay đổi các biến trong `variables.scss` để tùy chỉnh màu sắc, font, hoặc kích thước.
- Thêm các thành phần hoặc tiện ích mới trong các module tương ứng.

---

## 7. Kết luận
Thư viện SCSS này cung cấp một bộ công cụ mạnh mẽ và linh hoạt để xây dựng giao diện người dùng hiện đại. Hãy mở rộng và tùy chỉnh để phù hợp với dự án của bạn!




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
