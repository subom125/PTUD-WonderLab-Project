# Quy trình nghiệp vụ chính – WONDERLAB

## Quy trình 1. Mua hàng và tư vấn bằng Wonder Finder

1. Khách hàng truy cập website WONDERLAB.
2. Khách hàng mở **Wonder Finder**, chọn độ tuổi của bé, sở thích/kỹ năng cần phát triển và mức ngân sách.
3. Hệ thống lọc/chấm điểm và trả danh sách sản phẩm phù hợp, kèm **giải thích lý do gợi ý**.
4. Khách hàng xem chi tiết sản phẩm để đọc cảnh báo an toàn, thành phần hộp và hướng dẫn chơi.
5. Khách thêm sản phẩm vào giỏ và tiếp tục đặt hàng (Checkout).
6. Khách đăng nhập hoặc đăng ký tài khoản nếu chưa có.
7. Khách nhập thông tin giao hàng và lời nhắn tặng quà nếu cần.
8. Hệ thống kiểm tra số lượng tồn kho hợp lệ.
9. Khách xác nhận đơn; hệ thống lưu đơn và hiển thị mã đơn/thông báo thành công.
10. Khách theo dõi trạng thái; Admin tiếp nhận và cập nhật trạng thái giao hàng.


## Quy trình 2. Quản lý và xử lý đơn hàng (Admin)

1. Khách hàng hoàn tất đặt hàng.
2. Admin đăng nhập vào hệ thống quản trị.
3. Admin xem đơn hàng mới ở trạng thái **Chờ xác nhận**.
4. Admin kiểm tra khách hàng, sản phẩm, thanh toán.
5. Admin xác nhận và cập nhật đơn sang trạng thái **Đang giao** theo quy trình tài liệu gốc.
6. Hệ thống lưu lịch sử cập nhật, đồng bộ trạng thái trang tra cứu khách hàng.
7. Khi giao thành công, Admin chuyển đơn sang **Hoàn thành**.

**Trạng thái đề xuất trong phân tích AI:** `PENDING → CONFIRMED → SHIPPING → COMPLETED`; có thể thêm `CANCELLED` nếu triển khai hủy đơn. **Tài liệu quy trình hiện bỏ qua bước CONFIRMED riêng**: cần thống nhất trước khi code.

## Quy trình 3. Quản lý sản phẩm và ràng buộc toàn vẹn (Admin)

1. Admin đăng nhập vào hệ thống quản trị.
2. Vào **Quản lý sản phẩm** và tìm sản phẩm cần cập nhật.
3. Chọn **Ẩn/ngừng kinh doanh**.
4. Hệ thống xử lý sản phẩm không còn hợp lệ trong các giỏ hàng chưa đặt mua theo nghiệp vụ dự kiến.
5. Hệ thống **giữ nguyên thông tin tên, giá mua và hình ảnh** trong các đơn hàng đã tạo trước đó.
6. Thông báo cập nhật thành công; sản phẩm bị ẩn không còn xuất hiện ở trang chủ/danh mục.

## Quy trình 4. Đăng ký tài khoản và đánh giá sản phẩm

1. Guest truy cập website, chọn **Đăng ký**.
2. Nhập họ tên, số điện thoại, email, mật khẩu và gửi yêu cầu.
3. Hệ thống tạo tài khoản và đăng nhập tự động.
4. Khách đặt mua sản phẩm; đơn hoàn thành sau khi giao thành công.
5. Khách đăng nhập, xem lịch sử mua hàng.
6. Chọn sản phẩm đã mua và viết đánh giá/nhận xét.
7. Hệ thống lưu và hiển thị đánh giá tại trang chi tiết.

> **Phân loại phạm vi:** Đăng ký tài khoản là chức năng bắt buộc F05; **đánh giá sản phẩm là chức năng nâng cao F14**, không được hiểu là bắt buộc chỉ vì có mô tả quy trình.

## Ghi chú kiểm thử và trường hợp ngoại lệ

- Không có sản phẩm Wonder Finder phù hợp → thông báo rõ và cho phép chỉnh tiêu chí.
- Dữ liệu Checkout thiếu hoặc không hợp lệ → không tạo đơn.
- Hết hàng hoặc không đủ hàng → thông báo, không cho hoàn tất đơn không hợp lệ.
- Giao dịch lưu đơn thất bại → không hiển thị đặt hàng thành công.
- Khách không được xem đơn của người khác; thao tác quản trị phải qua xác thực/phân quyền.

> Nguồn: `Xác định quy trình nghiệp vụ chính.docx`; tham chiếu quyết định và phân loại chức năng ở [`REQUIREMENTS.md`](../REQUIREMENTS.md).
