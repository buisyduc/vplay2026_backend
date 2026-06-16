# Game_page
## Chức năng
- Hiển thị 3 game mới nhất
- Bộ lọc theo danh mục game 
- thanh tìm kiếm theo tên game
- list game hien thị theo danh mục
## Thành phần 
## Game_latest
Dữ liệu : 
- truy vấn 3 game mới nhất được thêm vào db (limit 3)
- tên
- danh mục 
- hình ảnh

Entity:
- game
- category_game
API 
GET /api/games?featured=true&limit=3

## Bộ lọc danh mục 
Dữ liêu :
-name
Entity:
- category_game
- game
API
GET /api/games?category={slug}&limit=6

## Thanh tìm kiếm 
Dữ liệu :
- name
Entity :
-game:
API
GET /api/games?search={keyword}&limit=6
## list game 
Dữ liệu : 
- name 
- danh mục
- hình ảnh 

API 
- Get api/game
