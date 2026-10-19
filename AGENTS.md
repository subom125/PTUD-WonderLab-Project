# Project Instructions for AI – WONDERLAB

## 1. Project context

Dự án học phần Phát triển ứng dụng WEB/TMĐT: website đồ chơi giáo dục/sáng tạo **WONDERLAB**, hướng đến phụ huynh có con 4–12 tuổi và người mua quà. Điểm khác biệt chính là **Wonder Finder theo quy tắc (rule-based)**.

## 2. Scope

- Trước khi đề xuất hoặc chỉnh sửa chức năng, đọc `README.md` và `REQUIREMENTS.md`.
- Chỉ triển khai những yêu cầu đã được nhóm xác nhận trong `REQUIREMENTS.md`.
- Phân biệt **bắt buộc**, **nâng cao**, **chưa thống nhất**; không tự biến ý tưởng AI thành yêu cầu dự án.
- Wonder Finder cần lọc theo độ tuổi và an toàn trước khi xếp hạng; không mặc định tích hợp AI học máy/chatbot.

## 3. Coding principles

- Viết mã dễ đọc, có tổ chức, dễ bảo trì và kiểm thử.
- Không thay đổi kiến trúc lớn hoặc tự ý xóa tính năng đang hoạt động.
- Ưu tiên thay đổi nhỏ, kiểm tra được, giảm phụ thuộc không cần thiết.
- Tôn trọng toàn vẹn đơn hàng, giá ở thời điểm mua, kiểm tra tồn kho, phân quyền Admin ở phía server.
- Nếu công nghệ chưa được nhóm chốt, chỉ đưa ra đề xuất; không tự khẳng định đã chọn stack.

## 4. Workflow

### Trước khi thay đổi

1. Đọc tài liệu và xác định yêu cầu/Issue liên quan.
2. Mô tả hiện trạng và tác động.
3. Đề xuất hướng giải quyết, tiêu chí kiểm thử và rủi ro.
4. Chờ xác nhận nếu thay đổi phạm vi hoặc quy tắc nghiệp vụ.

### Sau khi thay đổi

1. Tóm tắt thay đổi.
2. Liệt kê file liên quan.
3. Nêu cách chạy, kiểm thử và kết quả (nếu đã thực hiện).
4. Nêu giới hạn chưa xử lý, không khẳng định đã kiểm thử khi chưa chạy.

## 5. Security

- Không đưa API key, mật khẩu, token, thông tin đăng nhập hoặc `.env` lên repository công khai.
- Không công khai dữ liệu khách hàng thật; ưu tiên dữ liệu giả khi demo.
- Không vô hiệu hóa xác thực, phân quyền và các kiểm tra dữ liệu.
- Không tiết lộ thông tin đơn hàng chỉ bằng mã đơn dễ đoán.

## 6. Communication

Nếu yêu cầu chưa rõ, có mâu thuẫn giữa các file hoặc ảnh hưởng đến nghiệp vụ, phải nêu điểm chưa rõ và hỏi nhóm trước khi triển khai. Nội dung AI tạo ra phải được người phụ trách kiểm tra và ghi lại trong `AI_USAGE_LOG.md` khi dùng cho quyết định dự án.