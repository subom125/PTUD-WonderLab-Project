
# AI Usage Log – WONDERLAB

## Lần sử dụng 1

### Công cụ
**ChatGPT (OpenAI)**

### Mục đích
Phân tích yêu cầu nghiệp vụ cho dự án WONDERLAB – Website thương mại điện tử đồ chơi giáo dục và sáng tạo, từ đó xác định phạm vi, chức năng, nhóm người dùng và kế hoạch phát triển phù hợp với học phần.

### Prompt
Yêu cầu ChatGPT đóng vai trò chuyên gia phân tích nghiệp vụ cho dự án thương mại điện tử với các thông tin:

- **Tên dự án:** WONDERLAB.
- **Sản phẩm:** Đồ chơi giáo dục, STEM, DIY, board games và đồ chơi sáng tạo.
- **Khách hàng mục tiêu:** Phụ huynh có con 4–12 tuổi và người mua quà.
- **Vấn đề kinh doanh:** Khó lựa chọn đồ chơi phù hợp với độ tuổi, sở thích, mục tiêu học tập và ngân sách.
- **Giải pháp:** Website bán đồ chơi tích hợp Wonder Finder.
- **Website tham khảo:** MyKingdom, LEGO và OpenSTEM.
- **Quy mô:** 7 thành viên, khoảng 30–50 sản phẩm mẫu.

Yêu cầu AI đề xuất mục tiêu, phạm vi, nhóm người dùng, chức năng, quy trình nghiệp vụ, yêu cầu phi chức năng, MVP, chức năng nâng cao và rủi ro triển khai; phân biệt yêu cầu bắt buộc với yêu cầu có thể phát triển sau.

### Kết quả đề xuất
ChatGPT đề xuất:

1. **Nhóm người dùng:** Khách vãng lai (Guest), khách hàng (Customer) và quản trị viên (Admin).
2. **Chức năng chính:** Trang chủ, danh mục, tìm kiếm, lọc, chi tiết sản phẩm, giỏ hàng, đặt hàng, quản lý sản phẩm và đơn hàng.
3. **Wonder Finder:** Gợi ý đồ chơi theo độ tuổi, sở thích, hoạt động và ngân sách bằng quy tắc (rule-based), không cần huấn luyện AI.
4. **Yêu cầu phi chức năng:** Responsive, bảo mật, phân quyền, kiểm tra dữ liệu đầu vào và bảo đảm toàn vẹn dữ liệu.
5. **MVP:** Ưu tiên quy trình mua hàng hoàn chỉnh và Wonder Finder cơ bản.
6. **Chức năng mở rộng:** Thanh toán trực tuyến, chatbot AI, đánh giá sản phẩm, wishlist và dashboard.
7. **Rủi ro:** Vượt phạm vi dự án, dữ liệu không nhất quán, lỗi nghiệp vụ, bảo mật và chậm tiến độ.

Kết quả: https://chatgpt.com/s/t_6ad5029795608191a514a4d467862373

### Phản biện
Nhóm sử dụng Gemini để đánh giá độc lập kết quả ChatGPT.

Gemini nhận xét rằng một số yêu cầu chưa đáp ứng đầy đủ vấn đề kinh doanh, đặc biệt là giải thích lý do gợi ý, thông tin an toàn của đồ chơi, quản lý tồn kho và đăng ký tài khoản.

Ngoài ra, Gemini đề xuất làm rõ bảo mật API quản trị, quy tắc xếp hạng Wonder Finder và giới hạn những chức năng vượt quá phạm vi học phần.

### Quyết định của nhóm
- Giữ các chức năng thương mại điện tử cơ bản và Wonder Finder rule-based.
- Nâng tính năng giải thích lý do gợi ý lên mức bắt buộc.
- Bổ sung thông tin an toàn, thành phần hộp và hướng dẫn chơi.
- Bổ sung đăng ký/đăng nhập, quản lý danh mục và tồn kho.
- Ưu tiên COD hoặc thanh toán mô phỏng.
- Chuyển cá nhân hóa theo lịch sử, thanh toán trực tuyến thực tế và các tính năng phức tạp sang giai đoạn phát triển sau.

Các yêu cầu sau điều chỉnh được tổng hợp trong `REQUIREMENTS.md`.

### Người kiểm tra
**Anh Thi** – Phụ trách phân tích yêu cầu bằng AI.

---

## Lần sử dụng 2

### Công cụ
**Gemini (Google)**

### Mục đích
Phản biện độc lập kết quả phân tích yêu cầu của ChatGPT nhằm phát hiện yêu cầu thiếu, trùng lặp, chưa rõ ràng hoặc vượt quá khả năng triển khai của nhóm.

### Prompt
Yêu cầu Gemini đóng vai trò người phản biện độc lập cho dự án WONDERLAB.

Cung cấp:
- Mô tả đề tài và vấn đề kinh doanh.
- Khách hàng mục tiêu.
- Kết quả phân tích MyKingdom, LEGO và OpenSTEM.
- Danh sách yêu cầu do ChatGPT đề xuất.

Yêu cầu Gemini đánh giá:
1. Mức độ giải quyết vấn đề kinh doanh.
2. Các yêu cầu trùng lặp hoặc không cần thiết.
3. Những chức năng vượt phạm vi.
4. Chức năng và quy trình còn thiếu.
5. Rủi ro dữ liệu, bảo mật và quyền riêng tư.
6. Những yêu cầu chưa rõ để lập trình và kiểm thử.

### Kết quả đề xuất
Gemini đưa ra các đề xuất chính:

- Nâng giải thích lý do gợi ý trong Wonder Finder lên mức MUST.
- Bổ sung cảnh báo an toàn, thành phần hộp và hướng dẫn chơi.
- Bổ sung lời nhắn hoặc tùy chọn quà tặng.
- Loại bỏ cá nhân hóa theo lịch sử khỏi phạm vi hiện tại.
- Bổ sung đăng ký, đăng nhập khách hàng.
- Ưu tiên COD hoặc thanh toán mô phỏng.
- Bổ sung quản lý danh mục, kiểm tra và trừ tồn kho.
- Tăng bảo mật tra cứu đơn hàng và API Admin.
- Xác định quy tắc chấm điểm Wonder Finder.
- Bảo toàn dữ liệu đơn hàng khi sản phẩm bị ẩn.

Kết quả: https://share.gemini.google/7GDuEBX3CXEi

### Phản biện
Nhóm đối chiếu các đề xuất của Gemini với kết quả ChatGPT, vấn đề kinh doanh và phạm vi học phần.

Một số ý kiến cần điều chỉnh:
- Gemini cho rằng không cần tài khoản khách hàng, nhưng đăng ký/đăng nhập là chức năng cốt lõi mà nhóm lựa chọn.
- Yêu cầu bảo mật API Admin đã được ChatGPT đề cập trong NFR-05 nên không cần tạo yêu cầu trùng lặp.
- Độ tuổi và cảnh báo an toàn phải là điều kiện loại trừ trong Wonder Finder, không chỉ dùng để cộng điểm phù hợp.
- Một số tính năng như thanh toán thật, dashboard phức tạp và dịch vụ gói quà có phí chưa phù hợp với MVP.

### Quyết định của nhóm
**Giữ lại:**
- Website thương mại điện tử với các chức năng mua hàng cơ bản.
- Wonder Finder dựa trên quy tắc.
- Các yêu cầu bảo mật và phân quyền.
- Dashboard ở mức nâng cao, triển khai sau khi chức năng chính ổn định.

**Điều chỉnh, bổ sung:**
- Giải thích lý do gợi ý và thông tin an toàn sản phẩm.
- Đăng ký/đăng nhập khách hàng.
- Lời nhắn tặng quà ở mức SHOULD.
- Quản lý danh mục và tồn kho.
- Tra cứu đơn bằng mã đơn kết hợp số điện thoại.
- Quy tắc xếp hạng và xử lý sản phẩm bị ẩn.

**Loại khỏi phạm vi MVP:**
- Cá nhân hóa theo lịch sử mua hàng.
- Thanh toán trực tuyến thực tế.
- Tính năng AI tư vấn phức tạp.
- Dịch vụ gói quà có phí.

Các quyết định được sử dụng để hoàn thiện `REQUIREMENTS.md` và xác định phạm vi dự án.

### Người kiểm tra
**Hà Giang** – Phụ trách phản biện yêu cầu bằng AI Gemini.
