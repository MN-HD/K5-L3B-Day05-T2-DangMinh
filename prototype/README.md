# Prototype T2 — StudySpace AI

## Các tệp

- `index.html` — Prototype có thể tương tác, được đóng gói trong một tệp HTML. Không cần cài đặt, chạy máy chủ, API key hoặc kết nối Internet.
- `01-student-source-warning.png` — Ảnh chụp màn hình 1: trợ lý đánh dấu khẳng định cần kiểm tra trong tài liệu buổi 3, mục §3.3, đồng thời hiển thị nguồn và cách báo cáo.
- `02-student-active-assignment-block.png` — Ảnh chụp màn hình 2: trợ lý chặn yêu cầu công khai lời giải của bài tập đang mở và đưa ra gợi ý bước đầu có giới hạn.

## Cách mở và sử dụng

1. Mở `index.html` bằng Microsoft Edge hoặc Google Chrome.
2. Dùng các nút chọn tình huống để chuyển giữa hai trường hợp rủi ro cao và một câu hỏi học tập thông thường.
3. Trong tình huống tài liệu có nội dung cần kiểm tra, chọn **Báo lỗi tài liệu cho TA**, sau đó mở **Hàng chờ TA** để xem thao tác chuyển báo cáo được mô phỏng.
4. Trong tình huống bài tập đang mở, chọn **Nhận gợi ý bước đầu** để xem gợi ý có giới hạn, hoặc **Soạn FAQ kiến thức chung** để tạo bản nháp an toàn.
5. Mở **Hàng chờ TA** để xem xét, duyệt hoặc từ chối bản nháp FAQ kiến thức chung.
6. Thử tình huống câu hỏi thông thường để xem trợ lý giải thích kiến thức kèm nguồn mà không cần TA duyệt.

## Phạm vi và giới hạn

Đây là prototype thiết kế sử dụng dữ liệu giả lập. Prototype không kết nối với trang khóa học thật, mô hình AI thật, tài khoản TA, dịch vụ thông báo hoặc hệ thống xuất bản. Tất cả thao tác tạo hàng chờ, chuyển báo cáo, xem xét và duyệt đều được mô phỏng trong trình duyệt. Prototype không đăng FAQ thật và không gửi tin nhắn thật.

## Chú thích HAX / PAIR

1. **HAX G2** — Nhãn trạng thái "Cần kiểm tra" giúp người học nhận biết câu trả lời cần được xác minh.
2. **HAX G11** — Trích dẫn nguồn và đánh dấu khẳng định đáng nghi trong tài liệu buổi 3, mục §3.3.
3. **PAIR Errors + Graceful Failure** — Chức năng báo lỗi cho TA và đường xử lý an toàn khi trợ lý không thể xác nhận nguồn.
4. **HAX G10** — Chặn yêu cầu công khai đáp án của bài tập đang mở.
5. **Quyền kiểm soát của học viên** — Học viên chủ động chọn có nhận gợi ý bước đầu hay không.
6. **Kiểm duyệt của TA** — Hàng chờ TA yêu cầu xem xét trước khi bản nháp FAQ kiến thức chung được duyệt.

Prototype thể hiện các mức tự chủ đã đề xuất cho bốn tool gốc của T2, công cụ tra cứu trang khóa học chỉ đọc và thao tác soạn FAQ được tách riêng khỏi thao tác đăng FAQ.
