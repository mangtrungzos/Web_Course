/*==========CSS FlexBox==========*/
    Training skill flex
    https://codepen.io/enxaneta/full/adLPwv/
    https://codingfantasy.com/games/flexboxadventure/play
    https://flexboxfroggy.com/
    http://www.flexboxdefense.com/
# display: flex | inline-flex
// decide whether to use flex box layout or not
# flex-direction: row | column | row-reverse
// Change direction of main axis
// When use display: flex / flex-item default: row / then main axis nằm ngang
// or when use flex-direction: column / main axis: nằm dọc song song với cross aixs
# flex-wrap: nowrap | wrap | wrap-reverse
// Tùy chọn flex-item có thể xuống dòng hay không

// wrap-reverse: đổi chiều của cross start và cross end
# flex-basis: <legnth>
// Set kích thước của main size
// Phụ thuộc vào main axis nằm ở hướng nào thì sẽ set chiều ngang hoặc dọc tướng ứng với main size
# justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly
// Dành cho flex container
// Căn flex-item theo main axis
# justify-self: flex-start | -end | center
// Dành cho flex item
# align-content: flex-start | -end | center
// the same justify-content 
// Set theo phương hướng của trục cross axis
# align-self: flex-start | -end | center
// set cho flex-item
# align-items: center
// Set theo cross axis
# flex-grow: <number>
// Tăng kích thước của main size theo main aixs
# flex-shrink: <number>
// Thu nhỏ lại
# flex: <number>
// shorthand của flex-basis | -grow | -shrink

// Có giá trị từ 1 trở lên / sẽ cố chiếm hết khoảng không gian mà flex-item có thể chiếm được theo chiều main aixs
# order: <number>



# Để căn giữa 1 đối tượng ở trong 1 đối tượng có Display: flex
// Thẻ cha có thuộc tính display: flex
// Thẻ con có thuộc tính margin: auto

# text-align
// Căn theo main axis / Căn giữa chữ