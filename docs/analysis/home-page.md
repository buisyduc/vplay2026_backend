# Home Page

## Chức năng

- Hiển thị banner slider
- Hiển thị danh sách game nổi bật
- Hiển thị tin tức mới nhất

## Thành phần

### Banner

Dữ liệu:

- banner_image
- icon_image
- title
- description
- link

Entity:

- Banner

API:

GET /api/banners

### Danh mục game 

Dữ liệu:

- name
- thumbnail
- short_description

Entity:

- category_game

API:

GET api/category_game

### News Section

Dữ liệu:

- title
- thumbnail
- summary

Entity:

- News

API:

GET /api/news/latest
