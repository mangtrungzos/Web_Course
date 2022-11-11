# Hệ Thống Lưới
- Lưới nhiều cột (Multicolumn grid)
- Lưới một cột (Single column grid)
- lưới module (Modular grid)
- Lưới đường cơ sở (Baseline grid)

# Ứng dụng
- Lưới trong thiết kế UI / UX: vai tro đặc biệt quan trọng trong Responsive Web Design

# Responsive Web Design
- Grid: Thành phần cha
- Row: Dòng 
- Column: Cột 
- Gutter: khoảng cách 2 phía của column 

/*===============Thành phần lý thuyết==================*/

# Column
- Độ rộng sử dụng đơn vị %(tương đối) giúp linh động, dễ dàng tương thích với độ rộng khác nhau của các thiết bị. Số lượng cột trong grid system được xác định trước. 
(VD: PC 12|16 cột, Tablet 8 cột, mobile 4 cột)

# Gutter - Đường ngăn cách 
- Khoảng cách 2 phía của 1 cột, tạo nên rãnh ngăn giữa các cột. Độ rộng rãnh ngăn có thể thay đổi cho phù hợp với thiết kế hoặc độ rộng màn hình.
(VD: PC/Tablet 24px, Mobile 16px)

# margin - Phần lề
- Khoảng cách 2 bên trái/phải của bố cục chính của website. Độ rộng phần lề thay đổi để phù hợp với các kích thước màn hình. 
(VD: Phần lề lớn thích hợp cho màn hình lớn như PC, phần lề nhỏ thích hợp cho màn hình nhỏ như Tablet, mobile)

# Thành phần chính làm việc với CSS
1. Grid - Lưới (Thường là phần cha, chứa Row và Column)
2. Row - Dòng (Dòng - chiều ngang, chứa Column)
3. Column - Cột (Chứa nội dung / thành phần trên website)


# Tạo Column

/*===Tablet / PC Low Resolution===*/
@media (min-width: 740px) and (max-width: 1023px){
}


/*===PC Low Resolution===*/
@media(min-width: 1024px) and (max-width: 1239px){
}

# Tạo Row
## Vai trò
1. Chứa các Columns, giúp các Columns nằm theo chiều ngang
2. Khi tổng chiều ngang columns vượt quá kích thước Row, cho columns xuống hàng 
3. Loại bỏ khoảng thừa do gutters tạo ra ở 2 phía


## CSS:
@media (min-width: 740px){
    .row{
        margin-left: -8px;
        margin-right: -8px;
    }
}

@media (min-width: 1113px){
    .row{
        margin-left: -12px;
        margin-right: -12px;
    }
}

@media (min-width: 1024px) and (max-width: 1239px){
    .wide.row{
        margin-left: -12px;
        margin-right: -12px;
    }
}

# Shorthand
## flex-row, shrink, basis

.c-1{
    flex: 0 0 8.33333%; /*8.33333% set chiều ngang hoặc dọc tùy vào thẻ chứa nó có flex-direction: row or column*/ 
    max-width: 8.33333%; /*Giới hạn kích thước tối đa*/
}

## Cách tính 8.33333% = 100% / 12 cột -> muốn hiện thị mấy cột thì lấy 8.33333% x số cột muốn hiển thị

## c: moblie / m: tablet / l: PC

# Column offset : Vị trí của column
.c-o-1 : o là offset(vị trí của nó)
