# Vai trò người dùng và chức năng – WONDERLAB

## 1. Bảng vai trò người dùng

| Vai trò | Nhiệm vụ chính | Quyền hạn dự kiến |
| --- | --- | --- |
| Guest – Khách chưa đăng nhập | Khám phá, tìm kiếm đồ chơi và nhận tư vấn từ Wonder Finder | Xem trang chủ, danh mục, chi tiết; tìm kiếm, lọc; dùng Wonder Finder; thêm sản phẩm vào giỏ |
| Customer – Khách hàng | Mua hàng, theo dõi đơn hàng và cá nhân hóa trải nghiệm | Quyền Guest; đăng ký/đăng nhập; quản lý hồ sơ/địa chỉ; đặt hàng có lời nhắn tặng quà; thanh toán; tra cứu lịch sử đơn |
| Admin – Quản trị viên | Quản lý danh mục, sản phẩm, đơn hàng và tồn kho | Đăng nhập hệ thống quản trị; thêm/sửa/ẩn sản phẩm, danh mục; quản lý đơn; xem thống kê cơ bản nếu triển khai |

## 2. Danh sách chức năng đã phân loại

| Mã | Chức năng | Người dùng | Ưu tiên |
| --- | --- | --- | --- |
| F01 | Trang chủ, danh mục, sản phẩm nổi bật | Guest, Customer | Bắt buộc |
| F02 | Chi tiết sản phẩm: giá, ảnh, mô tả, cảnh báo, thành phần hộp, hướng dẫn chơi | Guest, Customer | Bắt buộc |
| F03 | Tìm kiếm, lọc, sắp xếp | Guest, Customer | Bắt buộc |
| F04 | Wonder Finder theo tuổi/sở thích/ngân sách và lý do gợi ý | Guest, Customer | Bắt buộc |
| F05 | Đăng ký, đăng nhập, hồ sơ | Customer | Bắt buộc |
| F06 | Giỏ hàng: thêm, sửa số lượng, xóa | Guest, Customer | Bắt buộc |
| F07 | Đặt hàng: thông tin, lời nhắn, tổng tiền, tồn kho | Customer | Bắt buộc |
| F08 | COD/thanh toán mô phỏng và mã giảm giá cơ bản | Customer | Bắt buộc |
| F09 | Lịch sử và tra cứu trạng thái đơn (mã đơn + số điện thoại) | Customer | Bắt buộc |
| F10 | Quản lý danh mục: thêm, sửa, ẩn | Admin | Bắt buộc |
| F11 | Quản lý sản phẩm: thêm, sửa, ẩn và toàn vẹn dữ liệu đơn cũ | Admin | Bắt buộc |
| F12 | Quản lý đơn và tồn kho: cập nhật trạng thái, trừ/hoàn kho | Admin | Bắt buộc |
| F13 | Dashboard tổng đơn, doanh thu | Admin | Nâng cao |
| F14 | Đánh giá/nhận xét chỉ dành cho người đã mua | Customer | Nâng cao |
| F15 | Wishlist và so sánh sản phẩm | Customer | Nâng cao |

## 3. Ràng buộc chính

- Guest được sử dụng Wonder Finder và giỏ hàng nhưng cần tài khoản để hoàn tất đặt hàng theo quy trình nhóm đã mô tả.
- Khách hàng chỉ xem thông tin cá nhân và đơn hàng của mình; tra cứu đơn yêu cầu mã đơn + số điện thoại xác minh.
- Quyền Admin phải được kiểm tra ở tầng xử lý dữ liệu/API, không chỉ ẩn nút ở giao diện.
- Chức năng nâng cao không được mặc định là sản phẩm bắt buộc của phiên bản đầu tiên.


