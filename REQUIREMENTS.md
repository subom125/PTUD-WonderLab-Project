# Requirements – WONDERLAB


## 1. Mục tiêu dự án

Xây dựng website thương mại điện tử đồ chơi giáo dục/sáng tạo dành cho phụ huynh có con 4–12 tuổi và người mua quà; hỗ trợ tìm sản phẩm an toàn, phù hợp với độ tuổi, sở thích và ngân sách, và hoàn thành quy trình mua hàng, quản trị cơ bản.

Điểm khác biệt là **Wonder Finder**: tư vấn dựa trên quy tắc và thuộc tính sản phẩm, cung cấp lý do gợi ý, không phụ thuộc mô hình AI học máy trong MVP.

## 2. Phạm vi

### 2.1. Trong phạm vi dự kiến (MVP)

- Danh mục, trang chủ, sản phẩm nổi bật, tìm kiếm/lọc/sắp xếp, chi tiết sản phẩm.
- Wonder Finder: lọc an toàn/độ tuổi; tư vấn theo sở thích, hoạt động, ngân sách; giải thích lý do gợi ý.
- Đăng ký/đăng nhập, quản lý hồ sơ khách hàng.
- Giỏ hàng, đặt hàng, lời nhắn tặng quà, COD hoặc thanh toán mô phỏng và mã giảm giá cơ bản.
- Tra cứu trạng thái/lịch sử đơn hàng; quản trị danh mục, sản phẩm, đơn hàng và tồn kho.
- Dữ liệu demo dự kiến 30–50 sản phẩm thuộc năm nhóm sản phẩm đã lựa chọn.

### 2.2. Ngoài phạm vi mặc định / ưu tiên sau

- Thanh toán trực tuyến thật và tích hợp vận chuyển tự động.
- Cá nhân hóa từ lịch sử hành vi, AI hội thoại/phức tạp.
- Dịch vụ gói quà tính phí, hệ thống thành viên phức tạp, ứng dụng di động riêng.
- Dashboard nâng cao, wishlist, so sánh và đánh giá chỉ phát triển khi luồng chính ổn định.

## 3. Người dùng và quyền hạn

| Vai trò | Nhiệm vụ | Quyền hạn dự kiến |
| --- | --- | --- |
| Guest – Khách chưa đăng nhập | Xem, tìm kiếm, nhận tư vấn | Xem trang chủ/danh mục/chi tiết, dùng tìm kiếm/lọc/Wonder Finder, thêm vào giỏ |
| Customer – Khách hàng | Mua hàng, theo dõi đơn và quản lý hồ sơ | Quyền Guest + đăng ký/đăng nhập, địa chỉ, đặt hàng, thanh toán, lịch sử đơn |
| Admin – Quản trị viên | Quản lý sản phẩm, danh mục, đơn hàng, tồn kho | Đăng nhập quản trị, thêm/sửa/ẩn, xem và cập nhật trạng thái đơn, xem thống kê cơ bản nếu triển khai |

Chi tiết tại [docs/user-roles.md](docs/user-roles.md).

## 4. Yêu cầu chức năng

Bảng sau sử dụng **mã F01–F15** của tài liệu Nhiệm vụ 5, không đồng nhất với mã FR-xx trong tài liệu AI ban đầu.

| Mã | Chức năng | Người sử dụng | Ưu tiên |
| --- | --- | --- | --- |
| F01 | Trang chủ, danh mục và sản phẩm nổi bật | Guest, Customer | Bắt buộc |
| F02 | Chi tiết sản phẩm: tên, ảnh, giá, mô tả, cảnh báo an toàn, thành phần hộp, hướng dẫn chơi | Guest, Customer | Bắt buộc |
| F03 | Tìm kiếm, lọc, sắp xếp sản phẩm | Guest, Customer | Bắt buộc |
| F04 | Wonder Finder: gợi ý theo tuổi, sở thích, ngân sách và giải thích lý do | Guest, Customer | Bắt buộc |
| F05 | Đăng ký, đăng nhập và hồ sơ cá nhân | Customer | Bắt buộc |
| F06 | Giỏ hàng: thêm/sửa số lượng/xóa | Guest, Customer | Bắt buộc |
| F07 | Đặt hàng: giao hàng, lời nhắn tặng quà, tổng tiền, tồn kho | Customer | Bắt buộc |
| F08 | COD/thanh toán mô phỏng; mã giảm giá cơ bản | Customer | Bắt buộc |
| F09 | Lịch sử mua hàng, trạng thái đơn và tra cứu bằng mã đơn + số điện thoại | Customer | Bắt buộc |
| F10 | Quản lý danh mục: thêm, sửa, ẩn | Admin | Bắt buộc |
| F11 | Quản lý sản phẩm: thêm, sửa, ẩn; giữ toàn vẹn đơn hàng cũ | Admin | Bắt buộc |
| F12 | Quản lý đơn: cập nhật trạng thái, trừ/hoàn tồn kho | Admin | Bắt buộc |
| F13 | Dashboard: tổng số đơn, tổng doanh thu | Admin | Nâng cao |
| F14 | Đánh giá sản phẩm chỉ với người đã mua | Customer | Nâng cao |
| F15 | Wishlist và so sánh sản phẩm | Customer | Nâng cao |

### 4.1. Quy tắc nghiệp vụ và tiêu chí nghiệm thu quan trọng

| Yêu cầu | Quy tắc / kết quả mong đợi |
| --- | --- |
| F02 | Hiển thị đầy đủ cảnh báo an toàn, thành phần hộp, hướng dẫn chơi khi có dữ liệu |
| F04 | Loại sản phẩm không phù hợp độ tuổi/cảnh báo an toàn **trước** khi xếp hạng; hiển thị lý do gợi ý; nếu không có kết quả phải thông báo rõ |
| F06 | Khi thay đổi số lượng giỏ, tổng tiền được cập nhật chính xác; không đặt vượt tồn kho |
| F07 | Kiểm tra dữ liệu giao hàng và tồn kho; xác nhận đơn trả về mã đơn; lưu đơn và chi tiết đơn nhất quán |
| F08 | COD/thanh toán mô phỏng; mã giảm giá ở mức đơn giản, không mặc định xử lý cổng thật |
| F09 | Tra cứu bằng mã đơn + số điện thoại đặt hàng; người đăng nhập chỉ xem đơn của chính mình; không để lộ dữ liệu |
| F11 | Khi ẩn sản phẩm, loại khỏi hiển thị/giỏ chưa đặt nhưng vẫn giữ thông tin tên/giá của các đơn hàng đã tạo |
| F12 | Kiểm tra tồn kho trước tạo đơn; **trừ kho khi đơn chuyển CONFIRMED** theo quyết định sau phản biện; hoàn kho khi hủy nếu hỗ trợ hủy đơn |

**Điểm cần thống nhất:** Tài liệu quy trình nghiệp vụ đang mô tả trừ tồn kho ngay khi xác nhận đặt thành công, còn bảng phản biện chốt trừ khi chuyển `CONFIRMED`. Cần thống nhất một thời điểm trước khi lập trình; bảng trên thể hiện kết luận của phần phản biện.

## 5. Yêu cầu phi chức năng

| Mã | Yêu cầu | Tiêu chí đánh giá dự kiến |
| --- | --- | --- |
| NFR-01 | Dễ sử dụng | Thực hiện được hành trình tìm và đặt hàng |
| NFR-02 | Responsive | Không tràn giao diện, mất nút chính ở mobile/desktop |
| NFR-03 | Hiệu năng | Mục tiêu đề xuất: tải trang chính dưới 3 giây trong điều kiện thử nghiệm ổn định |
| NFR-04 | Xác thực và bảo vệ bí mật | Băm mật khẩu, không đưa secret vào repository |
| NFR-05 | Phân quyền phía server | Người không có quyền bị từ chối khi gọi trực tiếp API quản trị |
| NFR-06 | Toàn vẹn dữ liệu | Tổng tiền tính ở server; đơn/chi tiết đơn lưu nhất quán |
| NFR-07 | Kiểm tra đầu vào | Kiểm tra dữ liệu bắt buộc, kiểu dữ liệu, số lượng |
| NFR-08 | Dễ bảo trì/kiểm thử | Chia module, có kịch bản test nghiệp vụ quan trọng |
| NFR-09 | Có thể cài đặt và triển khai | Thành viên khác có thể chạy theo tài liệu |
| NFR-10 | Bảo vệ dữ liệu cá nhân | Không công khai thông tin khách hàng, chỉ thu thập tối thiểu |
| NFR-11 | Mở rộng/sao lưu | Có phương án mở rộng dữ liệu và sao lưu khi cần |

### 5.1. Kịch bản kiểm thử tham khảo

- **AT-01:** Tìm sản phẩm có trong dữ liệu → hiển thị đúng.
- **AT-02:** Lọc tuổi/ngân sách → trả về sản phẩm hợp lệ.
- **AT-03:** Wonder Finder không có kết quả → thông báo và hướng điều chỉnh.
- **AT-04:** Đổi số lượng giỏ → tổng tiền đúng.
- **AT-05:** Đặt hàng hợp lệ → lưu đơn, sinh mã đơn.
- **AT-06:** Đặt hàng không hợp lệ → báo lỗi và không tạo đơn sai.
- **AT-07:** Gọi API admin khi không có quyền → bị từ chối.
- **AT-08:** Admin đổi trạng thái → trạng thái mới được lưu.
- **AT-09:** Dùng trên điện thoại → hành trình mua hàng không bị cản trở.

## 6. Giới hạn, giả định và nội dung cần xác minh

- Là một cửa hàng bán đồ chơi, không phải sàn đa người bán.
- Nhóm chưa chốt **frontend, backend, database, hosting** trong các tài liệu được cung cấp.
- Dữ liệu minh họa khoảng 30–50 sản phẩm; cần xác minh nguồn hình ảnh và người tạo dữ liệu.
- Cần xác nhận thời gian biểu, khả năng lập trình và phạm vi tích hợp thanh toán theo yêu cầu giảng viên.
- Cần thống nhất rõ thuật toán xếp hạng Wonder Finder; tiêu chí tuổi/an toàn phải là điều kiện loại trừ.
- Cần thống nhất **lúc trừ kho** và tính năng hủy đơn; phân biệt mã ưu đãi cơ bản trong F08 với thanh toán thật ngoài phạm vi.
- Phần **chatbot** có trong ý tưởng ban đầu nhưng không nằm trong danh sách F01–F15; nên để ở ý tưởng mở rộng, chưa cam kết trong MVP.

## 7. Quy trình và cơ sở quyết định

- [Quy trình nghiệp vụ](docs/business-workflow.md)
- [Bảng vai trò và chức năng](docs/user-roles.md)
- [Nhật ký ChatGPT + Gemini và quyết định sau phản biện](AI_USAGE_LOG.md)

