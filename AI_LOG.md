# Nhật ký sử dụng AI

## Hiện tượng và dữ kiện ban đầu

- Trang portfolio trên GitHub Pages không hiển thị CSS; request trang chủ được ghi nhận có trạng thái `304`.
- Khi kiểm tra HTML ban đầu, cả `index.html` và `ket-qua.html` trỏ stylesheet tới đường dẫn Windows tuyệt đối `D:\CNTT20-04\portfolio\css\style.css`.
- Repository có stylesheet tại `css/style.css`. Trạng thái `304` của trang chủ chỉ cho biết tài nguyên được phục vụ từ cache khi không thay đổi; không xác định được kết quả request CSS.

## Nhận định trước khi hỏi AI

Em nghi ngờ CSS không hiển thị do đường dẫn stylesheet sai. Đây là giả thuyết cần kiểm tra riêng request CSS, không phải kết luận dựa trên trạng thái `304`.

## Công cụ và trao đổi với AI

- **Công cụ:** Copilot trong VS Code; kiểm tra mã nguồn và URL bằng trình duyệt/công cụ HTTP.
- **Yêu cầu đã hỏi:** nêu giả thuyết, dữ kiện cần kiểm tra và bản sửa tối thiểu cho trang GitHub Pages.
- **Phản hồi AI (tóm tắt):** đường dẫn ổ đĩa Windows không dùng được trên GitHub Pages; thay bằng đường dẫn tương đối `css/style.css` ở cả trang chính và trang kết quả. Kiểm tra request CSS riêng vì `304` của trang HTML không chứng minh CSS đã tải hay chưa.

## Quyết định và lý do

Em chọn dùng `css/style.css` vì HTML và thư mục `css` nằm cùng cấp trong repository, nên đường dẫn tương đối hoạt động trên cả trang chủ và trang kết quả, không phụ thuộc đường dẫn máy cá nhân. Thay đổi này được ghi nhận trong commit `fc2808358c26b82c75159e519ff80099c9087c2c`.

## Phần sửa

- Trong `index.html`, đổi đường dẫn stylesheet từ đường dẫn Windows tuyệt đối sang `css/style.css`.
- Trong `ket-qua.html`, thực hiện đổi tương tự để trang kết quả dùng cùng stylesheet.

## Thử lại và kết quả

Sau thay đổi, mã nguồn hiện tại dùng `css/style.css` ở cả hai trang. Kiểm tra HTTP trực tiếp trong phiên làm tài liệu này cho kết quả: URL trang chủ trả `200`, HTML chứa liên kết `css/style.css`, và URL stylesheet trên GitHub Pages trả `200` với Content-Type `text/css`.

Đây là kết quả kiểm tra tại thời điểm ghi nhật ký; trạng thái `304` ban đầu không được xem là bằng chứng sửa lỗi. Có thể kiểm tra lại trong Developer Tools → **Network** sau khi tải lại trang, xem riêng request `css/style.css`.
