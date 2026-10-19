# Project Plan – WONDERLAB

## 1. Thành viên và vai trò (phân công Chương 1)

| Thành viên | Vai trò | Trách nhiệm | Đầu ra |
| --- | --- | --- | --- |
| Trung Hiếu | Trưởng nhóm, nghiên cứu đối thủ | Điều phối; phân tích ba website | `docs/competitor-analysis.md` |
| Quang Khải | Quản lý GitHub | Tạo repo, Issues, quản lý và tổng hợp tài liệu | Repository, README, Project Plan, AGENTS, Issues |
| Anh Thi | Phân tích yêu cầu bằng AI, Phân tích nghiệp vụ | Lưu prompt ChatGPT, kết quả đề xuất, Quy trình mua hàng, quản trị và tài khoản | Phần ChatGPT của `AI_USAGE_LOG.md`, `docs/business-workflow.md` |
| Hà Giang | Phản biện bằng AI | Lưu prompt Gemini, phản biện, quyết định nhóm | Phần Gemini của `AI_USAGE_LOG.md` |
| Hoài | Business Analyst | Vai trò người dùng, danh sách chức năng | `docs/user-roles.md`, `REQUIREMENTS.md` |
| Thùy Trang | Giới thiệu đề tài | Vấn đề kinh doanh và khách hàng mục tiêu | Nội dung `README.md`, `REQUIREMENTS.md` |


## 2. Các giai đoạn của đồ án

1. **Khảo sát – xác định yêu cầu:** ý tưởng, 3 website tham khảo, AI phân tích/phản biện, người dùng/chức năng, quy trình.
2. **Thiết kế giao diện:** user flow, wireframe, bố cục responsive.
3. **Phát triển frontend:** trang chủ, sản phẩm, bộ lọc, Wonder Finder, giỏ hàng, checkout.
4. **Backend và cơ sở dữ liệu:** tài khoản, sản phẩm, đơn hàng, tồn kho, quy tắc gợi ý, API.
5. **Tích hợp và kiểm thử:** kết nối các phần; kiểm tra nghiệp vụ và bảo mật.
6. **Triển khai – hoàn thiện:** chạy demo, sửa lỗi, cập nhật tài liệu và bàn giao.

## 3. Backlog công việc Chương 1

| Mã | Công việc | Người phụ trách | Kết quả | Hạn | Trạng thái |
| --- | --- | --- | --- | --- | --- |
| T01 | Chốt đề tài và vấn đề kinh doanh | Thùy Trang | Nội dung giới thiệu | 11pm 17/10/2026 | Đã có tài liệu Word |
| T02 | Phân tích 3 website | Trung Hiếu | Bảng/nhận xét 3 website | 11am 18/10/2026 | Đã có tài liệu Word |
| T03 | Phân tích yêu cầu bằng ChatGPT | Anh Thi | Prompt và phân tích đầu tiên | 13pm 18/10/2026 | Đã có tài liệu Word |
| T04 | Phản biện bằng Gemini | Hà Giang | Prompt, phản biện, quyết định nhóm | 15pm 18/10/2026 | Đã có tài liệu Word |
| T05 | Vai trò và chức năng | Hoài | Bảng vai trò và chức năng F01–F15 | 17pm 18/10/2026 | Đã có tài liệu Word |
| T06 | Quy trình nghiệp vụ | Anh Thi | Bốn quy trình | 11pm 18/10/2026 | Đã có tài liệu Word |
| T07 | Khởi tạo và tổng hợp GitHub | Quang Khải | Repo, 7 file bắt buộc, Issues | 11pm 19/10/2026 | Đang hoàn thiện |


## 4. Rủi ro và biện pháp xử lý

| Rủi ro | Biện pháp xử lý |
| --- | --- |
| Phạm vi tính năng quá lớn | Khóa danh sách MVP trước khi code; chuyển phần nâng cao sang backlog |
| Chưa thống nhất công nghệ | Chốt frontend, backend, database, hosting và cấu trúc dự án sớm |
| Dữ liệu sản phẩm thiếu chuẩn | Chuẩn hóa thuộc tính, độ tuổi, cảnh báo, giá, tồn kho |
| Wonder Finder gợi ý không phù hợp | Loại trừ tuổi/an toàn trước; kiểm thử tình huống có/không có kết quả |
| Trùng/chỉnh sửa ghi đè tài liệu | Mỗi tài liệu có người chủ trì; review Pull Request nếu cần |
| Thao tác quản trị không an toàn | Xác thực và phân quyền ở backend/API |
| Chậm tích hợp và kiểm thử | Issue có đầu ra và tiêu chí hoàn thành rõ ràng; review định kỳ |
| Lộ thông tin bí mật | Không commit token, secret, mật khẩu, dữ liệu khách hàng thật |

## 5. Quy trình cộng tác GitHub (chỉ qua trình duyệt cũng được)

1. Nhận GitHub Issue có **Assignee**, đầu ra và tiêu chí hoàn thành.
2. Mở file `.md` tương ứng, chọn **Edit this file**.
3. Sửa nội dung; với tài liệu có nhiều người chỉnh sửa, tạo branch/PR để review trước.
4. Ghi commit message rõ ràng, ví dụ `docs: add WonderLab business workflows`.
5. Reviewer đối chiếu nội dung với `REQUIREMENTS.md`, sau đó Merge Pull Request.
6. Đóng Issue khi đạt tiêu chí hoàn thành và cập nhật tiến độ.

## 6. Các quyết định còn cần chốt

- Công nghệ frontend/backend/database/hosting.
- Ngày bắt đầu, hạn nộp và mốc triển khai từng giai đoạn.
- Người phụ trách kỹ thuật ở những buổi tiếp theo.
- Quy tắc trừ tồn kho và chuyển trạng thái đơn hàng.
- Phạm vi thực tế của mã giảm giá, chatbot và thanh toán mô phỏng.

