# K5-L3B-Day05-T2-DangMinh — LAB5 T2 Giáo dục

Bài nộp cho LAB5 — Thiết kế sản phẩm AI: UX và mức độ tự chủ, lớp L3B, track T2 (Giáo dục).

## Các tệp trong dự án

- `spec.md` — Bài nộp gồm §1–§7: phạm vi sản phẩm, kịch bản rủi ro, trải nghiệm khi AI sai, mức độ tự chủ, thiết kế prototype, tiêu chí đánh giá và nội dung demo.
- `prototype/index.html` — Prototype StudySpace AI có thể mở và tương tác trực tiếp trên trình duyệt.
- `prototype/01-student-source-warning.png` — Ảnh chụp màn hình 1: AI phát hiện nội dung cần kiểm tra trong tài liệu buổi 3, mục §3.3.
- `prototype/02-student-active-assignment-block.png` — Ảnh chụp màn hình 2: AI chặn yêu cầu công khai đáp án của bài tập đang mở.
- `prototype/README.md` — Hướng dẫn mở prototype, mô tả chức năng và các giới hạn của bản mô phỏng.

## Cách mở prototype

Không cần cài đặt phần mềm, chạy máy chủ, có API key hoặc kết nối Internet. Mở tệp `prototype/index.html` bằng Microsoft Edge hoặc Google Chrome.

Dùng các nút chọn tình huống để chuyển giữa trường hợp tài liệu có nội dung cần kiểm tra, trường hợp yêu cầu công khai đáp án bài tập đang mở và một câu hỏi học tập thông thường. Chọn **Hàng chờ TA** để xem các báo cáo và bản nháp FAQ được mô phỏng.

## Phạm vi và giới hạn

Đây là prototype phục vụ bài tập thiết kế, sử dụng dữ liệu khóa học giả lập. Câu trả lời của AI, hàng chờ TA, báo cáo và thao tác duyệt đều được mô phỏng ngay trong trình duyệt. Prototype không gọi mô hình AI thật, không kết nối với trang khóa học thật hoặc tài khoản TA thật, không gửi thông báo thật và không xuất bản FAQ thật. Dự án không sử dụng dữ liệu cá nhân của học viên thật.

## Việc cần kiểm tra trước khi nộp

1. Đảm bảo mã học viên trong `spec.md` chính xác.
2. Sau buổi demo trực tiếp, cập nhật §7.2 trong `spec.md` bằng tình huống lạ thực tế mà TA, giảng viên hoặc nhóm khác đưa ra và cách thiết kế xử lý. Không ghi tình huống luyện tập thành kết quả demo thực tế.
3. Tạo một repository GitHub **mới, công khai và ban đầu để trống**, đặt tên chính xác là `K5-L3B-Day05-T2-DangMinh`. Không fork repository đề bài.
4. Đưa toàn bộ nội dung trong thư mục này lên nhánh `main` của repository mới.
5. Mở repository bằng cửa sổ riêng tư/ẩn danh để kiểm tra quyền truy cập công khai, sau đó nộp URL theo kênh giảng viên thông báo.
