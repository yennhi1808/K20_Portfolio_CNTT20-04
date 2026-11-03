# RELEASE_NOTES

## v7 - Bàn giao portfolio

- **Ngày cập nhật:** 2026-11-03
- **Tác giả:** Nguyễn Yến Nhi
- **Mã nguồn:** [Repository](https://github.com/yennhi1808/K20_Portfolio_CNTT20-04), nhánh `main`
- **Commit ứng dụng liên quan:** [`fc2808358c26b82c75159e519ff80099c9087c2c`](https://github.com/yennhi1808/K20_Portfolio_CNTT20-04/commit/fc2808358c26b82c75159e519ff80099c9087c2c)
- **URL xuất bản:** [GitHub Pages](https://yennhi1808.github.io/K20_Portfolio_CNTT20-04/)

### Thay đổi chính

- Hoàn thiện portfolio CV tĩnh bằng HTML và CSS, gồm giới thiệu, kỹ năng, dự án, học tập và liên hệ.
- Bổ sung trang kết quả cho biểu mẫu liên hệ thực hành.
- Bản bàn giao tài liệu gồm README, nhật ký sử dụng AI và ghi chú phát hành.

### Lỗi đã sửa

Đường dẫn CSS tuyệt đối theo máy Windows khiến stylesheet không phù hợp khi chạy trên GitHub Pages. `index.html` và `ket-qua.html` hiện tham chiếu stylesheet bằng đường dẫn tương đối `css/style.css`. Trong lần kiểm tra ghi nhận ở `AI_LOG.md`, trang chủ và request CSS trên Pages trả về HTTP 200.

### Hạn chế còn lại

- Biểu mẫu chỉ kiểm tra dữ liệu bằng HTML5 và chuyển tới `ket-qua.html` bằng GET; không gửi email, không lưu dữ liệu, và dữ liệu có thể xuất hiện trên URL.
- Font Inter được tải từ Google Fonts; nếu không có kết nối tới dịch vụ này, trang dùng font dự phòng trong CSS.
- Cấu hình nhánh/thư mục nguồn GitHub Pages cần được xác nhận trực tiếp tại **Settings → Pages** của repository.

### Tiếp tục kiểm tra và bàn giao

1. Mở [website](https://yennhi1808.github.io/K20_Portfolio_CNTT20-04/) và kiểm tra điều hướng, hình ảnh, responsive, biểu mẫu và trang kết quả theo [README](./README.md).
2. Trong Developer Tools → **Network**, tải lại trang và xác nhận `css/style.css` được tải thành công.
3. Nếu cần xác nhận cấu hình xuất bản, xem **Settings → Pages** trong [repository](https://github.com/yennhi1808/K20_Portfolio_CNTT20-04).
4. Mã ứng dụng được tham chiếu để đối chiếu là commit [`fc2808358c26b82c75159e519ff80099c9087c2c`](https://github.com/yennhi1808/K20_Portfolio_CNTT20-04/commit/fc2808358c26b82c75159e519ff80099c9087c2c). Tài liệu bàn giao mới cần được đưa vào commit nộp cùng mã nguồn.
