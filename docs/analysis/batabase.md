## language

| Trường (cột) | Kiểu dữ liệu | Mô tả |
| :--- | :--- | :--- |
| id | INT(5) | PK |
| icon | VARCHAR(255) | icon hiển thị quốc kỳ của ngôn ngữ |
| language_code | VARCHAR(10) | Ký tự viết tắt (vi, en, jp...) |
| language_name | VARCHAR(255) | Tên của ngôn ngữ |
| created_at | TIMESTAMPTZ | |
| created_by | TIMESTAMPTZ | |
| updated_at | TIMESTAMPTZ | |
| deleted_at | TIMESTAMPTZ | |

---

## banner

| Trường (cột) | Kiểu dữ liệu | Mô tả |
| :--- | :--- | :--- |
| id | INT(5) | PK |
| banner_image | VARCHAR(255) | hình ảnh banner lớn |
| icon_image | VARCHAR(255) | hình ảnh icon |
| name | VARCHAR(255) | tên của game tương ứng với banner |
| is_active | BOOLEAN | Trạng thái của dữ liệu |
| created_at | TIMESTAMPTZ | |
| created_by | TIMESTAMPTZ | |
| updated_at | TIMESTAMPTZ | |
| deleted_at | TIMESTAMPTZ | |

---

## user

| Trường (cột) | Kiểu dữ liệu | Mô tả |
| :--- | :--- | :--- |
| id | INT(5) | PK |
| name | VARCHAR(255) | tên của người dùng |
| email | VARCHAR(255) | email dùng để đăng nhập |
| password | VARCHAR(255) | mật khẩu đã mã hóa |
| phone | VARCHAR(255) | số điện thoại |
| is_active | BOOLEAN | Trạng thái tài khoản |
| created_at | TIMESTAMPTZ | |
| created_by | TIMESTAMPTZ | |
| updated_at | TIMESTAMPTZ | |
| deleted_at | TIMESTAMPTZ | |

---

## role

| Trường (cột) | Kiểu dữ liệu | Mô tả |
| :--- | :--- | :--- |
| id | INT(5) | PK |
| role | VARCHAR(255) | tên quyền (admin, editor...) |
| is_active | BOOLEAN | Trạng thái của dữ liệu |
| created_at | TIMESTAMPTZ | |
| created_by | TIMESTAMPTZ | |
| updated_at | TIMESTAMPTZ | |
| deleted_at | TIMESTAMPTZ | |

---

## user_role

| Trường (cột) | Kiểu dữ liệu | Mô tả |
| :--- | :--- | :--- |
| id | INT(5) | PK |
| role_id | INT(5) | id của quyền {FK} |
| user_id | INT(5) | id của người dùng {FK} |
| created_at | TIMESTAMPTZ | |
| created_by | TIMESTAMPTZ | |
| updated_at | TIMESTAMPTZ | |
| deleted_at | TIMESTAMPTZ | |

---

## category_game

| Trường (cột) | Kiểu dữ liệu | Mô tả |
| :--- | :--- | :--- |
| id | INT(5) | PK |
| name | VARCHAR(255) | tên danh mục |
| image | VARCHAR(255) | hình ảnh danh mục |
| description | VARCHAR(255) | nội dung mô tả danh mục |
| is_active | BOOLEAN | Trạng thái của dữ liệu |
| created_at | TIMESTAMPTZ | |
| created_by | TIMESTAMPTZ | |
| updated_at | TIMESTAMPTZ | |
| deleted_at | TIMESTAMPTZ | |

---

## game

| Trường (cột) | Kiểu dữ liệu | Mô tả |
| :--- | :--- | :--- |
| id | INT(5) | PK |
| category_id | INT(5) | id của danh mục {FK} |
| name | VARCHAR(255) | tên game |
| image | VARCHAR(255) | hình ảnh game |
| website_url | VARCHAR(255) | đường dẫn tới nội dung game |
| download_url | VARCHAR(255) | đường dẫn tới nội dung cài đặt game |
| is_featured | BOOLEAN | xác định mức độ nổi bật |
| is_active | BOOLEAN | Trạng thái của dữ liệu |
| created_at | TIMESTAMPTZ | |
| created_by | TIMESTAMPTZ | |
| updated_at | TIMESTAMPTZ | |
| deleted_at | TIMESTAMPTZ | |

---

## category_news

| Trường (cột) | Kiểu dữ liệu | Mô tả |
| :--- | :--- | :--- |
| id | INT(5) | PK |
| name | VARCHAR(255) | tên danh mục |
| is_active | BOOLEAN | Trạng thái của dữ liệu |
| created_at | TIMESTAMPTZ | |
| created_by | TIMESTAMPTZ | |
| updated_at | TIMESTAMPTZ | |
| deleted_at | TIMESTAMPTZ | |

---

## news

| Trường (cột) | Kiểu dữ liệu | Mô tả |
| :--- | :--- | :--- |
| id | INT(5) | PK |
| category_id | INT(5) | id của danh mục {FK} |
| name | VARCHAR(255) | tên tin tức |
| image | VARCHAR(255) | hình ảnh tin tức |
| slug | VARCHAR(255) | đường dẫn url nội dung tin tức |
| description | TEXT | nội dung tin tức |
| is_featured | BOOLEAN | xác định mức độ nổi bật |
| published_at | TIMESTAMPTZ | thời gian tạo tin tức |
| is_active | BOOLEAN | Trạng thái của dữ liệu |
| created_at | TIMESTAMPTZ | |
| created_by | TIMESTAMPTZ | |
| updated_at | TIMESTAMPTZ | |
| deleted_at | TIMESTAMPTZ | |

## translation

| Trường (cột) | Kiểu dữ liệu | Mô tả |
| :--- | :--- | :--- |
| id | INT(5) | PK |
| natable_nameme | VARCHAR(255) | tên bảng cần dịch |
| record_id | INT(5) | id của bản ghi trong bảng cần dịch |
| language_id | INTG(5) | id của ngôn ngữ |
| key | VARCHAR(255) | tên trường cần dịch |
| value | TEXT | nội dung  đã dịch |
| created_at | TIMESTAMPTZ | |
| created_by | TIMESTAMPTZ | |
| updated_at | TIMESTAMPTZ | |
| deleted_at | TIMESTAMPTZ | |
