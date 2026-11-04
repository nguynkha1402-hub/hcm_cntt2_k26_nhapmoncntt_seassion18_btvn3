### Phần 1. Phân tích

-Dùng Inspect Element chọn khung "Danh sách trạm".   

-Vào tab Computed kiểm tra 4 lớp Box Model. Lỗi chồng lấn thường do lớp ngoài cùng  đang bị âm hoặc bằng 0.

### Phần 2. Triển khai
Vào tab Styles của phần tử lỗi, áp dụng 1 trong 2 cách:

- Nếu dùng layout tĩnh: Thêm` margin-top: 50px;` (điều chỉnh số cho phù hợp).

- Nếu dùng `position: absolute`: Tăng giá trị `top` để đẩy khung xuống.

### Phần 3. Kiểm thử
Nếu đổi `margin` mà khung không di chuyển, nguyên nhân do Browser Engine đang ưu tiên các thuộc tính ghi đè:

- Phần tử đang bị gán `position: absolute` (bứt khỏi luồng HTML, không nhận margin đẩy).

- Phần tử đang là `display: inline` (không nhận margin dọc).