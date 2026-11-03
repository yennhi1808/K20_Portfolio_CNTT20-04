# Portfolio CV - Nguyễn Yến Nhi

## Thông tin sản phẩm

- **Tên:** Portfolio CV cá nhân
- **Tác giả:** Nguyễn Yến Nhi
- **Mô tả:** Trang portfolio tĩnh giới thiệu bản thân, kỹ năng, dự án, học tập và thông tin liên hệ; có biểu mẫu thực hành chuyển đến trang kết quả.
- **Mã nguồn:** [GitHub repository](https://github.com/yennhi1808/K20_Portfolio_CNTT20-04)
- **Sản phẩm trực tuyến:** [GitHub Pages](https://yennhi1808.github.io/K20_Portfolio_CNTT20-04/)
- **Hồ sơ tác giả:** [github.com/yennhi1808](https://github.com/yennhi1808)

## Cấu trúc thư mục

```text
.
├── index.html          # Trang portfolio chính
├── ket-qua.html        # Trang kết quả của biểu mẫu
├── css/
│   └── style.css       # Giao diện và responsive
├── assets/
│   ├── avatar.svg
│   ├── nhiiiii.jpg
│   ├── du-an-1.svg
│   ├── du-an-2.svg
│   └── du-an-3.svg
├── README.md
├── AI_LOG.md           # Ghi nhận việc dùng AI và quyết định
└── RELEASE_NOTES.md    # Ghi chú bàn giao v7
```

## Chạy trên máy

Đây là website tĩnh, không cần cài thư viện. Từ thư mục gốc của repository, chạy:

```bash
python -m http.server 8000
```

Mở <http://localhost:8000/> trong trình duyệt. Nếu máy không có Python, có thể mở thư mục bằng VS Code và chạy extension Live Server. Mở trực tiếp `index.html` cũng được, nhưng dùng máy chủ local giúp kiểm tra gần với cách website được xuất bản hơn.

## Nguồn xuất bản

Sản phẩm được phục vụ qua GitHub Pages tại URL ở trên. Mã nguồn hiện có trong nhánh `main`, với các trang HTML và thư mục `css/`, `assets/` ở thư mục gốc. Nội dung trang chủ và stylesheet đã được kiểm tra trả về HTTP 200. Cấu hình nhánh/thư mục xuất bản cụ thể chưa xác minh được qua API; có thể xác nhận tại **Settings → Pages** của repository.

## Cách kiểm tra

1. Mở trang chủ, kiểm tra ảnh, bố cục và các mục Giới thiệu, Kỹ năng, Dự án, Học tập, Liên hệ.
2. Dùng menu hoặc nút **Xem dự án** để kiểm tra các liên kết neo trong trang.
3. Thu nhỏ cửa sổ trình duyệt để kiểm tra bố cục responsive.
4. Trong phần Liên hệ, thử gửi biểu mẫu với dữ liệu hợp lệ; trường họ tên yêu cầu tối thiểu 2 ký tự, email cần đúng định dạng, lời nhắn từ 10 đến 500 ký tự. Kiểm tra trang `ket-qua.html` và liên kết quay lại.
5. Mở Developer Tools → **Network**, tải lại trang và kiểm tra request `css/style.css`. Khi chạy local, request dự kiến là `http://localhost:8000/css/style.css`; trên Pages, request dự kiến là `https://yennhi1808.github.io/K20_Portfolio_CNTT20-04/css/style.css`.

Biểu mẫu chỉ là bài thực hành: không gửi email, không lưu dữ liệu lên máy chủ; dữ liệu gửi bằng GET có thể xuất hiện trên URL.

## Liên kết và minh chứng

- [Hồ sơ GitHub của tác giả](https://github.com/yennhi1808)
- [Mã nguồn repository](https://github.com/yennhi1808/K20_Portfolio_CNTT20-04)
- [Commit sửa đường dẫn CSS](https://github.com/yennhi1808/K20_Portfolio_CNTT20-04/commit/fc2808358c26b82c75159e519ff80099c9087c2c)
- [Ghi nhận sử dụng AI](./AI_LOG.md)
- [Ghi chú phát hành v7](./RELEASE_NOTES.md)
