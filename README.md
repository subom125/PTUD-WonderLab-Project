# WONDERLAB – Website thương mại điện tử đồ chơi giáo dục & sáng tạo

> Đồ án học phần **Phát triển ứng dụng WEB/TMĐT** – Chương 1: Khởi tạo đồ án và thống nhất phạm vi.

## 1. Giới thiệu

**WONDERLAB** là concept website thương mại điện tử chuyên bán đồ chơi giáo dục, đồ chơi sáng tạo, bộ STEM/DIY, trò chơi tư duy và board games cho trẻ em. Điểm nhấn của dự án là hỗ trợ người mua lựa chọn sản phẩm theo độ tuổi, sở thích, kỹ năng/loại hoạt động và ngân sách, thay vì chỉ duyệt danh mục sản phẩm.

**Wonder Finder** là công cụ tư vấn theo bộ quy tắc (*rule-based*): loại bỏ sản phẩm không phù hợp về độ tuổi/cảnh báo an toàn, sau đó gợi ý/xếp hạng theo nhu cầu và ngân sách, kèm giải thích ngắn gọn về lý do gợi ý. Phiên bản ban đầu **không cần huấn luyện mô hình AI**.

## 2. Khách hàng mục tiêu và vấn đề kinh doanh

| Nhóm khách hàng | Nhu cầu | Vấn đề giả định cần kiểm chứng |
| --- | --- | --- |
| Chính: Phụ huynh có con 4–12 tuổi | Chọn đồ chơi phù hợp độ tuổi, sở thích, hoạt động phát triển kỹ năng | Nhiều lựa chọn; khó đánh giá độ phù hợp, an toàn và giá trị sử dụng |
| Phụ: Người thân/người mua quà | Chọn quà theo dịp và ngân sách | Khó biết trẻ thích gì, mất thời gian tìm kiếm và so sánh |

## 3. Chức năng chính dự kiến

- Khám phá trang chủ, danh mục, tìm kiếm, lọc và xem chi tiết sản phẩm, bao gồm cảnh báo an toàn, thành phần hộp và hướng dẫn chơi.
- **Wonder Finder:** gợi ý sản phẩm theo độ tuổi, sở thích, hoạt động và ngân sách; trả về lý do gợi ý.
- Đăng ký, đăng nhập, quản lý thông tin khách hàng.
- Giỏ hàng, đặt hàng, lời nhắn tặng quà, thanh toán COD hoặc mô phỏng.
- Tra cứu lịch sử và trạng thái đơn hàng.
- Quản trị danh mục, sản phẩm, đơn hàng và tồn kho.

**Nâng cao nếu còn thời gian:** dashboard cơ bản, đánh giá sản phẩm, wishlist/so sánh. Chưa mặc định tích hợp thanh toán thật hoặc AI hội thoại.

## 4. Thành viên và trách nhiệm Chương 1

| Thành viên | Vai trò | Phần việc |
| --- | --- | --- |
| Trung Hiếu | Trưởng nhóm | Điều phối; phân tích ba website tương tự |
| Quang Khải | Quản lý GitHub | Tạo repository, Issues và tổng hợp tài liệu |
| Anh Thi | Phân tích bằng AI, Quy trình nghiệp vụ | Đề xuất yêu cầu qua ChatGPT, Mô tả các quy trình nghiệp vụ chính |
| Hà Giang | Phản biện bằng AI | Phản biện bằng Gemini; tổng hợp quyết định |
| Hoài | Business Analyst | Vai trò người dùng và danh sách chức năng |
| Thùy Trang | Giới thiệu đề tài | Mô tả ý tưởng, khách hàng và vấn đề kinh doanh |


## 5. Công nghệ dự kiến

- Công cụ quản lý dự án và tài liệu: **GitHub, GitHub Issues, Markdown**.
- Công cụ hỗ trợ phân tích: **ChatGPT** (AI thứ nhất), **Gemini** (AI phản biện).
- **Frontend / Backend / Database / Hosting: Chưa được chốt trong các tài liệu hiện có.** Nhóm sẽ cập nhật sau khi thống nhất stack công nghệ.
- Dữ liệu demo dự kiến: khoảng **30–50 sản phẩm** thuộc Logic & Puzzles, STEM & Science Kits, Arts & DIY, Board Games, Pretend Play.

## 6. Kế hoạch triển khai dự kiến

1. Khảo sát và xác định yêu cầu.
2. Thiết kế giao diện.
3. Xây dựng frontend.
4. Phát triển backend và cơ sở dữ liệu.
5. Tích hợp và kiểm thử.
6. Triển khai và hoàn thiện.

Chi tiết phân công và tiến độ xem [PROJECT_PLAN.md](PROJECT_PLAN.md).

## 7. Tài liệu dự án

- [Yêu cầu và phạm vi đã tổng hợp](REQUIREMENTS.md)
- [Kế hoạch và phân công](PROJECT_PLAN.md)
- [Quy tắc hỗ trợ của AI](AGENTS.md)
- [Nhật ký sử dụng AI](AI_USAGE_LOG.md)
- [Phân tích website tương tự](docs/competitor-analysis.md)
- [Vai trò người dùng](docs/user-roles.md)
- [Quy trình nghiệp vụ](docs/business-workflow.md)

