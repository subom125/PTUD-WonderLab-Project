# Requirements – WONDERLAB

## 1. Mục tiêu dự án

Xây dựng website thương mại điện tử đồ chơi giáo dục/sáng tạo dành cho phụ huynh có con 4–12 tuổi và người mua quà; hỗ trợ tìm sản phẩm an toàn, phù hợp với độ tuổi, sở thích và ngân sách, và hoàn thành quy trình mua hàng, quản trị cơ bản.

Điểm khác biệt là **Wonder Finder**: tư vấn dựa trên quy tắc và thuộc tính sản phẩm, cung cấp lý do gợi ý, không phụ thuộc mô hình AI học máy trong MVP.

## 2. Phạm vi

### 2.1. Trong phạm vi dự kiến (MVP)

- Danh mục, trang chủ, sản phẩm nổi bật, tìm kiếm/lọc/sắp xếp, chi tiết sản phẩm.
- Wonder Finder: lọc an toàn/độ tuổi; tư vấn theo sở thích, hoạt động, ngân sách; giải thích lý do gợi ý.
- Đăng ký/đăng nhập, quản lý hồ sơ khách hàng.
- Giỏ hàng và đặt hàng dành cho khách hàng đã đăng nhập; COD hoặc thanh toán mô phỏng. Lời nhắn tặng quà và mã giảm giá đơn giản được ưu tiên nếu đủ thời gian.
- Tra cứu trạng thái/lịch sử đơn hàng; quản trị danh mục, sản phẩm, đơn hàng và tồn kho.
- Dữ liệu demo dự kiến 30–50 sản phẩm thuộc năm nhóm sản phẩm đã lựa chọn.

### 2.2. Ngoài phạm vi mặc định / ưu tiên sau

- Thanh toán trực tuyến thật và tích hợp vận chuyển tự động.
- Cá nhân hóa từ lịch sử hành vi, AI hội thoại/phức tạp.
- Dịch vụ gói quà tính phí, hệ thống thành viên phức tạp, ứng dụng di động riêng.
- Dashboard nâng cao chỉ phát triển khi luồng chính ổn định; wishlist, so sánh và đánh giá chưa nằm trong danh sách F01–F41 được cập nhật.

## 3. Người dùng và quyền hạn

| **Vai trò**            | **Nhiệm vụ chính**                                                                | **Quyền hạn dự kiến**                                                                                                                                                                                                                                             |
| ---------------------- | --------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Khách vãng lai (Guest) | Khám phá sản phẩm, tìm kiếm đồ chơi phù hợp và tham khảo thông tin trước khi mua. | Xem danh sách và chi tiết sản phẩm; tìm kiếm, lọc theo độ tuổi, danh mục và giá; sử dụng Wonder Finder; xem lý do gợi ý và cảnh báo an toàn; đăng ký tài khoản, đăng nhập. Chưa được đặt hàng theo phạm vi nhóm đã thống nhất.                                    |
| Khách hàng (Customer)  | Mua hàng, quản lý thông tin cá nhân và theo dõi đơn hàng.                         | Thực hiện các chức năng của khách vãng lai; quản lý hồ sơ cá nhân; thêm, sửa số lượng và xóa sản phẩm trong giỏ hàng; đặt hàng bằng COD hoặc phương thức thanh toán mô phỏng; gửi lời nhắn tặng quà; xem lịch sử và trạng thái đơn hàng của chính mình.           |
| Quản trị viên (Admin)  | Quản lý dữ liệu sản phẩm, danh mục, tồn kho và xử lý đơn hàng.                    | Đăng nhập khu vực quản trị; thêm, sửa, ẩn sản phẩm; thêm, sửa, ẩn hoặc ngừng sử dụng danh mục; quản lý số lượng tồn kho; xem chi tiết đơn hàng và cập nhật trạng thái theo quy tắc nghiệp vụ; xem số liệu tổng hợp cơ bản nếu chức năng thống kê được triển khai. |

Lưu ý về phạm vi quyền hạn: Theo phạm vi nhóm đã thống nhất, WONDERLAB cần có chức năng đăng ký, đăng nhập khách hàng và yêu cầu khách hàng đăng nhập trước khi đặt hàng. Khách vãng lai vẫn được sử dụng các chức năng khám phá sản phẩm và Wonder Finder. Trong phiên bản đầu tiên, nhóm chỉ cần triển khai một vai trò quản trị viên, chưa cần phân chia thành nhân viên bán hàng hay nhân viên xử lý đơn hàng riêng biệt.

Chi tiết tại [docs/user-roles.md](docs/user-roles.md).

## 4. Yêu cầu chức năng

Danh sách chức năng cập nhật sử dụng **mã F01–F41** theo phân công và phạm vi mới của nhóm; các mã này thay thế bảng F01–F15 cũ và không đồng nhất với mã FR-xx trong bản yêu cầu kỹ thuật trước đó.

| **Mã** | **Chức năng**                                                                                 | **Người sử dụng**          | **Mức độ ưu tiên** |
| ------ | --------------------------------------------------------------------------------------------- | -------------------------- | ------------------ |
| F01    | Xem trang chủ và các nhóm sản phẩm nổi bật                                                    | Khách vãng lai, Khách hàng | Bắt buộc           |
| F02    | Xem danh sách sản phẩm theo danh mục                                                          | Khách vãng lai, Khách hàng | Bắt buộc           |
| F03    | Xem chi tiết sản phẩm, gồm tên, hình ảnh, giá, mô tả, độ tuổi, kỹ năng hoặc hoạt động phù hợp | Khách vãng lai, Khách hàng | Bắt buộc           |
| F04    | Hiển thị thành phần hộp đồ chơi, cảnh báo an toàn và hướng dẫn chơi hoặc lắp ráp              | Khách vãng lai, Khách hàng | Bắt buộc           |
| F05    | Tìm kiếm sản phẩm theo tên hoặc từ khóa                                                       | Khách vãng lai, Khách hàng | Bắt buộc           |
| F06    | Lọc sản phẩm theo độ tuổi, danh mục và khoảng giá                                             | Khách vãng lai, Khách hàng | Bắt buộc           |
| F07    | Sắp xếp sản phẩm theo giá tăng dần hoặc giảm dần                                              | Khách vãng lai, Khách hàng | Nên có             |
| F08    | Đăng ký tài khoản khách hàng                                                                  | Khách vãng lai             | Bắt buộc           |
| F09    | Đăng nhập và đăng xuất tài khoản khách hàng                                                   | Khách vãng lai, Khách hàng | Bắt buộc           |
| F10    | Quản lý hồ sơ và thông tin cá nhân                                                            | Khách hàng                 | Bắt buộc           |
| F11    | Sử dụng Wonder Finder để chọn độ tuổi, sở thích, loại hoạt động và ngân sách                  | Khách vãng lai, Khách hàng | Bắt buộc           |
| F12    | Gợi ý danh sách sản phẩm phù hợp dựa trên các tiêu chí đã chọn                                | Khách vãng lai, Khách hàng | Bắt buộc           |
| F13    | Hiển thị lý do gợi ý cho từng sản phẩm                                                        | Khách vãng lai, Khách hàng | Bắt buộc           |
| F14    | Xếp hạng sản phẩm gợi ý theo quy tắc chấm điểm đã xác định                                    | Khách vãng lai, Khách hàng | Nên có             |
| F15    | Thông báo khi không có sản phẩm phù hợp và cho phép điều chỉnh tiêu chí                       | Khách vãng lai, Khách hàng | Bắt buộc           |
| F16    | Thêm sản phẩm vào giỏ hàng                                                                    | Khách hàng                 | Bắt buộc           |
| F17    | Thay đổi số lượng hoặc xóa sản phẩm khỏi giỏ hàng                                             | Khách hàng                 | Bắt buộc           |
| F18    | Tính và hiển thị tổng tiền theo giá sản phẩm và số lượng                                      | Khách hàng                 | Bắt buộc           |
| F19    | Nhập thông tin nhận hàng gồm họ tên, số điện thoại, địa chỉ và ghi chú tùy chọn               | Khách hàng                 | Bắt buộc           |
| F20    | Gửi lời nhắn tặng quà trong đơn hàng                                                          | Khách hàng                 | Nên có             |
| F21    | Kiểm tra tính hợp lệ của thông tin đặt hàng và số lượng sản phẩm                              | Khách hàng, Hệ thống       | Bắt buộc           |
| F22    | Kiểm tra tồn kho trước khi tạo đơn và trừ tồn kho khi đơn được xác nhận                       | Hệ thống, Admin            | Bắt buộc           |
| F23    | Đặt hàng bằng COD hoặc phương thức thanh toán mô phỏng                                        | Khách hàng                 | Bắt buộc           |
| F24    | Tạo mã đơn hàng, lưu đơn hàng và chi tiết đơn hàng vào cơ sở dữ liệu                          | Hệ thống                   | Bắt buộc           |
| F25    | Hiển thị thông báo đặt hàng thành công và mã đơn hàng                                         | Khách hàng                 | Bắt buộc           |
| F26    | Xem lịch sử đơn hàng và trạng thái các đơn của bản thân                                       | Khách hàng                 | Bắt buộc           |
| F27    | Tra cứu đơn hàng bằng mã đơn và số điện thoại đặt hàng                                        | Khách hàng                 | Bắt buộc           |
| F28    | Áp dụng một mã giảm giá cố định với quy tắc đơn giản                                          | Khách hàng                 | Nên có             |
| F29    | Đăng nhập vào khu vực quản trị và kiểm soát quyền truy cập                                    | Admin                      | Bắt buộc           |
| F30    | Thêm, sửa và ẩn hoặc ngừng kinh doanh sản phẩm                                                | Admin                      | Bắt buộc           |
| F31    | Thêm, sửa và ẩn hoặc ngừng sử dụng danh mục sản phẩm                                          | Admin                      | Bắt buộc           |
| F32    | Quản lý số lượng tồn kho của sản phẩm                                                         | Admin                      | Bắt buộc           |
| F33    | Xem danh sách và chi tiết đơn hàng                                                            | Admin                      | Bắt buộc           |
| F34    | Cập nhật trạng thái đơn hàng theo quy tắc nghiệp vụ                                           | Admin                      | Bắt buộc           |
| F35    | Tìm kiếm hoặc lọc đơn hàng theo mã đơn và trạng thái                                          | Admin                      | Nên có             |
| F36    | Bảo vệ các chức năng quản trị bằng xác thực và phân quyền ở phía máy chủ                      | Hệ thống                   | Bắt buộc           |
| F37    | Hiển thị số liệu tổng hợp cơ bản về số đơn hàng, doanh thu và đơn chờ xử lý                   | Admin                      | Nâng cao           |
| F38    | Hỗ trợ gói quà có phí, kèm quy trình xử lý gói quà                                            | Khách hàng, Admin          | Phát triển sau     |
| F39    | Cá nhân hóa gợi ý theo lịch sử tìm kiếm hoặc mua hàng                                         | Hệ thống                   | Phát triển sau     |
| F40    | Tích hợp cổng thanh toán trực tuyến thật và dịch vụ vận chuyển                                | Khách hàng, Hệ thống       | Phát triển sau     |
| F41    | Xây dựng AI tư vấn hội thoại hoặc hệ thống gợi ý học máy                                      | Khách vãng lai, Khách hàng | Phát triển sau     |

### 4.1. Quy tắc nghiệp vụ và tiêu chí nghiệm thu quan trọng

| **Yêu cầu** | **Quy tắc / kết quả mong đợi** |
| --- | --- |
| F03–F04 | Hiển thị thông tin sản phẩm, thành phần hộp, cảnh báo an toàn và hướng dẫn khi có dữ liệu. |
| F11–F15 | Wonder Finder loại sản phẩm không phù hợp độ tuổi hoặc yêu cầu an toàn trước khi gợi ý; nêu lý do, thông báo nếu không có kết quả. |
| F16–F18 | Chỉ khách hàng đăng nhập mới quản lý giỏ hàng; thay đổi số lượng phải cập nhật tổng tiền chính xác. |
| F19, F21–F25 | Kiểm tra thông tin giao hàng và tồn kho; tạo mã đơn duy nhất; lưu đơn và chi tiết đơn nhất quán trước khi thông báo thành công. |
| F22, F34 | Kiểm tra tồn kho trước khi tạo đơn; trừ tồn kho khi đơn được xác nhận theo quy trình nghiệp vụ đã thống nhất. |
| F26–F27 | Chỉ cho phép xem đơn hàng thuộc quyền truy cập; tra cứu bằng mã đơn và số điện thoại đặt hàng. |
| F30–F31 | Khi ẩn sản phẩm hoặc danh mục, bảo toàn dữ liệu tham chiếu và thông tin của những đơn hàng đã tạo. |
| F29, F36 | Xác thực và phân quyền quản trị ở phía máy chủ, không chỉ ẩn nút trên giao diện. |

**Điểm cần thống nhất khi lập trình:** Xác định chính xác sự kiện chuyển đơn sang trạng thái xác nhận để trừ kho (ví dụ `CONFIRMED`), cách hoàn kho khi hủy và khả năng đặt đồng thời; tài liệu cập nhật chỉ nêu nguyên tắc “trừ tồn kho khi đơn được xác nhận”.

## 5. Yêu cầu phi chức năng

| **Mã** | **Yêu cầu**                  | **Tiêu chí đánh giá dự kiến**                                                    |
| ------ | ---------------------------- | -------------------------------------------------------------------------------- |
| NFR-01 | Dễ sử dụng                   | Thực hiện được hành trình tìm và đặt hàng                                        |
| NFR-02 | Responsive                   | Không tràn giao diện, mất nút chính ở mobile/desktop                             |
| NFR-03 | Hiệu năng                    | Mục tiêu đề xuất: tải trang chính dưới 3 giây trong điều kiện thử nghiệm ổn định |
| NFR-04 | Xác thực và bảo vệ bí mật    | Băm mật khẩu, không đưa secret vào repository                                    |
| NFR-05 | Phân quyền phía server       | Người không có quyền bị từ chối khi gọi trực tiếp API quản trị                   |
| NFR-06 | Toàn vẹn dữ liệu             | Tổng tiền tính ở server; đơn/chi tiết đơn lưu nhất quán                          |
| NFR-07 | Kiểm tra đầu vào             | Kiểm tra dữ liệu bắt buộc, kiểu dữ liệu, số lượng                                |
| NFR-08 | Dễ bảo trì/kiểm thử          | Chia module, có kịch bản test nghiệp vụ quan trọng                               |
| NFR-09 | Có thể cài đặt và triển khai | Thành viên khác có thể chạy theo tài liệu                                        |
| NFR-10 | Bảo vệ dữ liệu cá nhân       | Không công khai thông tin khách hàng, chỉ thu thập tối thiểu                     |
| NFR-11 | Mở rộng/sao lưu              | Có phương án mở rộng dữ liệu và sao lưu khi cần                                  |

### 5.1. Kịch bản kiểm thử tham khảo

- **AT-01:** Tìm sản phẩm có trong dữ liệu → hiển thị đúng.
- **AT-02:** Lọc tuổi/ngân sách → trả về sản phẩm hợp lệ.
- **AT-03:** Wonder Finder không có kết quả → thông báo và hướng điều chỉnh.
- **AT-04:** Khách hàng đăng nhập đổi số lượng giỏ → tổng tiền đúng; khách vãng lai không thực hiện được chức năng giỏ hàng.
- **AT-05:** Đặt hàng hợp lệ → lưu đơn, sinh mã đơn.
- **AT-06:** Đặt hàng không hợp lệ → báo lỗi và không tạo đơn sai.
- **AT-07:** Gọi API admin khi không có quyền → bị từ chối.
- **AT-08:** Admin đổi trạng thái → trạng thái mới được lưu.
- **AT-09:** Dùng trên điện thoại → hành trình mua hàng không bị cản trở.

## 6. Giới hạn, giả định và nội dung cần xác minh

- Là một cửa hàng bán đồ chơi, không phải sàn đa người bán.
- Nhóm đã dự kiến **HTML/CSS/JavaScript/Bootstrap**, **ASP.NET Core MVC (C#)** và **SQL Server** theo bảng yêu cầu kỹ thuật mới; cần chốt môi trường hosting và cấu hình triển khai.
- Dữ liệu minh họa khoảng 30–50 sản phẩm; cần xác minh nguồn hình ảnh và người tạo dữ liệu.
- Cần xác nhận thời gian biểu, khả năng lập trình và phạm vi tích hợp thanh toán theo yêu cầu giảng viên.
- Cần thống nhất rõ thuật toán xếp hạng Wonder Finder; tiêu chí tuổi/an toàn phải là điều kiện loại trừ.
- Cần thống nhất **lúc trừ kho** và tính năng hủy đơn; phân biệt mã ưu đãi đơn giản (F28, nên có) với thanh toán trực tuyến thật (F40, phát triển sau).
- **Chatbot/AI tư vấn hội thoại** thuộc F41 (phát triển sau), chưa cam kết trong MVP.

## 7. Quy trình và cơ sở quyết định

- [Quy trình nghiệp vụ](https://github.com/subom125/PTUD-WonderLab-Project/blob/main/docs/business-workflow.md)
- [Bảng vai trò và chức năng](https://github.com/subom125/PTUD-WonderLab-Project/blob/main/docs/user-roles.md)
- [Nhật ký ChatGPT + Gemini và quyết định sau phản biện](https://github.com/subom125/PTUD-WonderLab-Project/blob/main/AI_USAGE_LOG.md)
