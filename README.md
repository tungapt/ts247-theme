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

