# Quy trình nghiệp vụ chính – WONDERLAB

## Mục tiêu và nguyên tắc mô hình hóa quy trình To-Be
Các quy trình To-Be được mô tả từ lúc khách phát sinh nhu cầu tìm đồ chơi đến khi đơn hàng được giao hoàn tất, đồng thời bao quát các nghiệp vụ hỗ trợ gồm quản lý sản phẩm/danh mục, tài khoản và đánh giá. Mỗi quy trình xác định tác nhân, điều kiện bắt đầu, luồng chính, điểm quyết định, nhánh ngoại lệ và kết quả đầu ra. Tìm kiếm theo từ khóa, danh mục và các bộ lọc như độ tuổi, giá, sở thích hoặc loại hoạt động là các thao tác tiêu chuẩn trong quy trình khám phá sản phẩm; không phải một tính năng độc lập hay công cụ tư vấn/xếp hạng riêng.

Nguyên tắc áp dụng xuyên suốt: (1) chỉ đưa sản phẩm đang kinh doanh vào danh sách có thể mua; (2) thuộc tính dùng để lọc phải được chuẩn hóa trong dữ liệu sản phẩm; (3) máy chủ xác thực quyền, giá, số lượng, tồn kho và tổng tiền; (4) khách được duyệt sản phẩm và tạo giỏ khi chưa đăng nhập nhưng phải đăng nhập trước khi đặt hàng; (5) chỉ thông báo tạo đơn thành công sau khi đơn và chi tiết đơn được lưu thành công; (6) kiểm tra tồn kho tại checkout và kiểm tra lại trước khi Admin xác nhận, chỉ trừ kho khi xác nhận thành công; (7) thao tác quản trị phải được xác thực và phân quyền ở máy chủ; (8) sản phẩm bị ẩn/ngừng kinh doanh không được mua mới và bị loại khỏi giỏ đang lưu, nhưng dữ liệu sản phẩm trong đơn hàng lịch sử được giữ nguyên; (9) lỗi xử lý phải có thông báo rõ ràng và không làm thay đổi một phần trạng thái đơn hoặc tồn kho; (10) đơn hàng hỗ trợ hai phương thức thanh toán: COD và chuyển khoản ngân hàng bằng QR.

![Sơ đồ quy trình nghiệp vụ tổng quát To-Be của WONDERLAB](images/workflow/Sơ đồ tổng quát.png)

## Mô tả quy trình nghiệp vụ của hệ thống
### Quy trình tổng quát: Từ khám phá sản phẩm đến hoàn tất đơn hàng
Bước 1 - Phát sinh nhu cầu và khám phá: Khách truy cập website, duyệt danh mục hoặc nhập từ khóa. Khách có thể kết hợp các bộ lọc mà hệ thống hỗ trợ như độ tuổi, khoảng giá, sở thích và loại hoạt động; các tiêu chí được kết hợp đồng thời theo dữ liệu đã chuẩn hóa.

Bước 2 - Trả kết quả và xem chi tiết: Hệ thống chỉ truy vấn sản phẩm đang kinh doanh, hiển thị danh sách phù hợp và thông tin tóm tắt. Khách mở chi tiết để xem tên, giá hiện hành, mô tả, độ tuổi phù hợp, hoạt động/kỹ năng, thành phần hộp, hướng dẫn sử dụng và cảnh báo an toàn nếu các trường này có dữ liệu. Nếu không có kết quả, hệ thống thông báo và cho khách điều chỉnh hoặc xóa bộ lọc; không tự ý thay đổi tiêu chí.

Bước 3 - Chọn sản phẩm và quản lý giỏ: Khách chọn số lượng, thêm sản phẩm vào giỏ hoặc thay đổi số lượng/xóa sản phẩm. Hệ thống kiểm tra trạng thái kinh doanh và số lượng hợp lệ, cập nhật tạm tính. Nếu sản phẩm đã bị ẩn/ngừng kinh doanh hoặc số lượng không hợp lệ, hệ thống thông báo và yêu cầu khách chọn lại; việc có sản phẩm trong giỏ không đồng nghĩa hàng đã được giữ chỗ.

Bước 4 - Checkout và chọn thanh toán: Khách chọn tiến hành đặt hàng. Nếu chưa đăng nhập, hệ thống yêu cầu đăng nhập hoặc đăng ký; sau khi xác thực thành công, khách nhập họ tên người nhận, số điện thoại, địa chỉ giao hàng và ghi chú tùy chọn. Khách chọn một trong hai phương thức: COD (thanh toán khi nhận hàng) hoặc chuyển khoản ngân hàng bằng QR. Với COD, đơn được tạo ở trạng thái thanh toán “Chưa thanh toán”. Với chuyển khoản QR, hệ thống tạo mã QR chứa thông tin chuyển khoản theo mã đơn và số tiền cần trả; đơn ở trạng thái thanh toán “Chờ xác nhận thanh toán” cho đến khi Admin đối soát giao dịch.

Bước 5 - Kiểm tra và tạo đơn: Máy chủ kiểm tra phiên đăng nhập, trường bắt buộc, sản phẩm còn kinh doanh, giá hiện hành, số lượng và tồn kho; đồng thời tự tính lại tổng tiền. Nếu có dữ liệu sai, giá thay đổi hoặc không đủ hàng, hệ thống trả lỗi để khách kiểm tra giỏ/thông tin và gửi lại. Nếu hợp lệ, hệ thống lưu đơn cùng các dòng chi tiết theo một giao dịch nhất quán, gán mã đơn duy nhất và đặt trạng thái đơn “Chờ xác nhận”. Hệ thống đồng thời lưu phương thức thanh toán và trạng thái thanh toán ban đầu tương ứng.

Bước 6 - Phản hồi kết quả và xử lý thanh toán: Chỉ sau khi lưu đơn thành công, hệ thống mới hiển thị mã đơn và thông tin xác nhận. Nếu chọn COD, hệ thống hiển thị số tiền cần trả khi nhận hàng. Nếu chọn chuyển khoản QR, hệ thống hiển thị mã QR, tên ngân hàng, số tài khoản nhận, số tiền và nội dung chuyển khoản có chứa mã đơn; khách thực hiện chuyển khoản qua ứng dụng ngân hàng. Ở phiên bản MVP, Admin đối soát giao dịch với thông tin tài khoản nhận và cập nhật “Đã thanh toán” khi xác nhận nhận đủ tiền; trước đó trạng thái vẫn là “Chờ xác nhận thanh toán”. Nếu lưu đơn thất bại, hệ thống không hiển thị thành công và không tạo mã đơn giả. Tồn kho chưa bị trừ tại bước checkout.

Bước 7 - Admin xử lý đơn: Admin đăng nhập và được hệ thống kiểm tra quyền trước khi mở danh sách đơn “Chờ xác nhận”. Admin kiểm tra thông tin đơn và tồn kho lần cuối. Với đơn COD, nếu đủ hàng và hợp lệ, Admin xác nhận; hệ thống chuyển sang “Đã xác nhận” và trừ tồn kho đúng một lần. Với đơn chuyển khoản QR, Admin chỉ xác nhận giao hàng sau khi đối soát tiền thành công và đủ hàng; hệ thống cập nhật trạng thái thanh toán “Đã thanh toán”, trạng thái đơn “Đã xác nhận” và trừ tồn kho đúng một lần. Nếu chưa nhận được tiền hoặc giao dịch không khớp, đơn giữ trạng thái chờ thanh toán, không xác nhận giao hàng và không trừ tồn kho. Nếu không đủ hàng hoặc có vấn đề, Admin hủy đơn và ghi lý do; nếu tiền đã nhận trước khi hủy, Admin thực hiện hoàn tiền ngoài hệ thống và lưu ghi chú xử lý.

Bước 8 - Giao hàng, hoàn tất và tra cứu: Khi bàn giao đơn cho đơn vị vận chuyển, Admin cập nhật “Đang giao”; khi xác nhận giao thành công, Admin cập nhật “Hoàn thành”. Hệ thống lưu lịch sử thay đổi trạng thái. Khách chỉ được xem chi tiết các đơn thuộc tài khoản của mình. Các ngoại lệ xuyên suốt gồm không có kết quả tìm kiếm, sản phẩm hết khả dụng, giỏ rỗng, chưa đăng nhập, dữ liệu giao hàng sai, giá/tồn kho thay đổi, lỗi lưu đơn, Admin từ chối xác nhận và truy cập quản trị không đủ quyền.



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
