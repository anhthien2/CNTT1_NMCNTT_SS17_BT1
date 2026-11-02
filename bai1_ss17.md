# Phần 1: Báo cáo phân tích (I/O) - Dùng tab Computed

Vào trang bị đè > F12 > chọn mũi tên `Inspect` > click vào khung **"Nội dung bài học"**

**Bước 1: Mở Computed để soi Box Model thật**  
Đừng nhìn tab `Styles` vì nó đang bị ghi đè lộn xộn. Qua tab **Computed** ở bên phải, kéo xuống dưới cùng sẽ thấy sơ đồ Box Model màu sắc:

-   **Content (xanh):** Là kích thước thực của text/video. Ví dụ nó đang hiện `632 x 400px` nhưng thực tế bị co lại.
-   **Padding (xanh lá):** Khoảng đệm trong. Đang dính `padding: 20px` ở cả 4 phía làm khung to ra thêm 40px.
-   **Border (vàng):** Viền. Đang là `border: 1px solid #ddd` - đây là thứ làm 2 khung chạm nhau.
-   **Margin (cam):** Lề ngoài. Hiện tại đang là `margin: 0` nên 2 khung mới bị đè lên nhau.


# Phần 2: Thiết kế giải pháp

```
.lesson-content {
  margin-right: 24px; /* Thay vì margin: 0 -> tạo khoảng thở */
  padding: 16px; /* Giảm từ 20px xuống để gọn */
  width: calc(70% - 24px); /* Đảm bảo không quá 100% */
}

.video-list {
  width: 30%;
  margin-left: 0;
  float: none; /* Bỏ float nếu đang dùng */
}
```
