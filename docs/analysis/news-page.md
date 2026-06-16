## news page
## chức năng
- Hiển thị tin tức mớiu nhất
- bộ lọc danh mục 
- thanh tìm kiếm theo name 
- list tin tức hiên thị theo bộ lọc 
## Thành phần 
## Tin tức mới nhất 
Dữ liệu :
- hình ảnh 
- danh mục 
- name 
Entity 
- news
API 
GET api/news


## bộ lọc danh mục 
Dữ liệu :
- name
Entity 
- category_news
-new
API 
GET api/news?category={slug}


## thanh tìm kiếm 
Dữ liệu :
-  name 
Entity 
- news
API 
GET api/news?search={keyword}


## list news hiên thị theo bộ lọc 
Dữ liệu :
- name
- hình ảnh 
Entity 
- news
- category_news
 

 API
 - GET api/news
