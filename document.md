# CSS inn HTML
1. Internal (Sử dụng 1 cặp thẻ style{} trong chính file HTML)
2. External (CSS bằng cách link tới 1 file ở bên ngoài)
3. inline (Bằng cách sử dụng attribute style trong chính các thẻ để CSS
    style="")

# reset css
// Ex: 
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        ...
# font-family:
- sans-serif: chủng (tập hợp những phông chữ không có chân)

# inherit
- Kế thừa 
    # Ex:         
                *{
                    box-sizing: inherit;
                }

                html{
                    box-sizing: border-box;
                }
- Cho tất cả các thẻ có box-sizing sẽ kế thừa lại thuộc tính box-sizing của HTML.
# Transparent
- Màu trong suốt

# Transform / thủ thuật căn giữa các vạch ngăn và nhiều thứ khác
    content: "";
    position: absolute;
    top: 50%; /*top: 50% là 50% của thẻ chứa nó*/
    left: 0;
    height: 60%;
    border-left: 1px solid #e5e5e5;
    transform: translateY(-50%);/*50% chiều cao của chính nó*/

# Độ tương thích đối với các trình duyệt web
- https://caniuse.com/?search=animation

# Line-height
// Có nghĩa là chiều cao của một dòng

# min-width
- Chiều dài tối thiểu 

# Khi đối tượng con vượt quá đối tượng cha trong muốn ẩn thằng con đi
// overflow: hidden

# overflow-x Làm thanh scroll kéo ngang
- Khi đối tượng con vượt quá đối tượng cha theo chiều ngang sẽ auto tự động nó sẽ sinh ra thanh scroll để kéo ngang
# margin
// margin: 2px 16px 0 (trên, trái phải , dưới)
// margin: 0 12px 0 8px (trên phải dưới trái)

# padding
// 0 0 8px 0: up, right, down, left

# Để thêm bóng vào 1 khối màu trắng 
// box-shadow // Tạo ra 1 bóng đổ cho đối tượng

# CSS selectors
// Cách css tới các phần tử

# Tổ hợp phím CSS các phần tử giống nhau
// Ctrl + Shift + L

# Thẻ p
// Có tính chất display: block

# Thẻ a
// Khi set width không được / Do chưa có thuộc tính display: block
// Thẻ a được hiểu là thẻ chứa chữ / nên mặc định bị ảnh hưởng bởi thuộc tính line-height
# Thẻ span
// Thẻ span mặc định không apply thuộc tính css / nên có thể css cho thẻ cha để các thẻ con chứa span được kế thừa

# default div ul
// have padding-left: 40px

# card <h>
// Có khoảng margin mặc định lên trên và dưới 

# transition
// Thêm thuộc tính transition vào đối tượng muốn thay đổi 

// /*Làm chuyển động sang phải*/ 
    1. transition: right linear 0.1s;
       right: 0;
    2. Hover
       right: -4px;
    Ex: 
            .category-item__link{
                position: relative;
                color: var(--text-color);
                text-decoration: none;
                font-size: 1.6rem;
                padding: 8px 16px;
                display: block;
                transition: right linear 0.1s;
                right: 0;
            }

            .category-item__link:hover{
                right: -4px;
                color: var(--primary-color);
            }

# text-overflow: ellipses
// Tạo dấu 3 chấm sau dòng chữ đối với những chữ quá dài và chỉ áp dụng được khi có white-space

// Khi sử dụng text-overflow: ellipses phải thêm 1 thuộc tính nữa  white-space: nowrap

// white-space: nowrap / không cho chữ xuống dòng nữa 

# text-decoration
// line-through: gạch ngang giữa chữ
// underline: gạch dưới chân chữ

# align-items
// baseline: căn thẳng hàng dưới chân chữ 

# Căn items về một hướng
// margin-left / right : auto / Sẽ đẩy item về một hướng cho tới khi chạm phải vào item tiếp theo

# border radius về 1 hướng
// border-top-right-radius
// ...

# box-shadow
// box-shadow: 0 0.0625rem 0.125rem 0 rgba(0,0,0,.1);
    1. 0: unset x , không di chuyển chiều ngang
    2. 

# CSS chữ in
//  text-transform: uppercase;

# pagination
// Phần phân trang

# Thuộc tính Fillter
// giảm độ sáng của item xuống 
    filter: brightness(...%)

# object-fit
// Đối với những ảnh bị ăn theo trục cross axis ta có thể sử dụng 
    object-fit: contain

# Cách chọn 1 đối tượng có thể css hết tất cả
- ctrl shift L

# Cách fix lỗi hở viền dọc bên phải
- overflow: hidden set cho thẻ cha lớn chứa tất cả các item trong đó
- khi những đối tượng bên trong bị đẩy ra ngoài hoặc bị hở ra ngoài so với layout thì ẩn đi là được 

# nav : navigation : thẻ điều hướng

# display: block
- Sử dụng display: block để set chiều ngang khi thẻ không ăn thuộc tính width height

# : nth-of-type(3n)

# Cách set dấu 3 chấm đối với những dòng chữ dài 
    display: block;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    overflow: hidden;

# Thanh scroll 
- Xuất hiện ở thẻ ul chính là cái thẻ cho phép overflow: hidden
    EX: Web_Shopee
            .mobile-category__list::-webkit-scrollbar{
                display: none;
            }

# Cách bỏ hight light của thẻ khi ấn vào 
    -webkit-tap-hightlight-color: transparent