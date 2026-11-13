# Bài nộp LAB5 — T2 Giáo dục · Nhóm DangMinh

**Lớp:** L3B · **Track:** T2 — Giáo dục  
**Hình thức:** Cá nhân.

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
| Đặng Nguyễn Nhật Minh | **2A202604118** | Phân tích đề và dữ liệu T2; xây dựng kịch bản rủi ro; thiết kế UX khi AI sai; quyết định mức tự chủ; xây dựng và kiểm thử prototype; chuẩn bị demo và bài nộp. |

> **Việc cần hoàn tất trước khi nộp:** thay phần mã học viên trong ngoặc vuông bằng mã chính xác trên thẻ sinh viên / hệ thống môn học. Không để placeholder này trong bản cuối.

## §1. Lát cắt & phạm vi

### Lát cắt

Trong **trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode)**, khi **học viên** đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, **AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng “tài liệu không có, hỏi giảng viên”**, để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.

### Ba việc tính năng KHÔNG làm

1. **Không đưa hoặc xác nhận đáp số của bài tập đang mở.** AI chỉ cung cấp gợi ý từng bước có giới hạn để học viên tự giải; không viết bài nộp thay học viên.
2. **Không bịa nội dung, nguồn, số mục hoặc số slide.** AI chỉ trích dẫn tài liệu thực sự có trong khoá học và thông tin thực sự có trên trang khoá học. Tài liệu buổi 3 chỉ có các mục §3.1–§3.5, không có slide đánh số.
3. **Không đánh giá năng lực hay gắn nhãn người học.** AI không nhận xét học viên “giỏi”, “kém”, “không đủ khả năng”; thay vào đó, AI phản hồi vào câu hỏi và gợi ý bước học tiếp theo.

**Bối cảnh và cái giá khi sai:** học viên thường học muộn, không có TA để hỏi ngay. Một câu giải thích sai có thể khiến học viên học sai mà không nhận ra; một đáp án bị công khai có thể ảnh hưởng cả lớp. Vì vậy, sản phẩm cần vừa giúp người học tiếp tục học, vừa thể hiện rõ căn cứ, giới hạn và đường chuyển người.

## §2. Kịch bản rủi ro

### 2.1. Danh sách kịch bản

| # | Tin người dùng | Lớp | AI có thể sai thế nào — bằng chứng từ T2 | Một sản phẩm tốt nên làm gì | Mức hại |
|---|---|---|---|---|---|
| 1 | “Thầy có nói gì ở slide 12 về độ lệch chuẩn không ạ?” | ① Nguồn sự thật | Tài liệu buổi 3 chỉ có §3.1–§3.5 và không có slide đánh số. AI có thể bịa nội dung hoặc trích dẫn “slide 12” dù nguồn không tồn tại. | Nói rõ tài liệu không đánh số slide; chỉ dẫn tới mục có thật hoặc nói không tìm thấy nguồn. | Sửa được |
| 2 | “Buổi 7 học p-value như thế nào ạ?” | ① Nguồn sự thật | Trang khoá học chỉ ghi tên buổi 7 là “Kiểm định giả thuyết và p-value”; chưa có tài liệu buổi 7. AI có thể tự tạo nội dung rồi trình bày như kiến thức đã được dạy. | Chỉ xác nhận tên buổi theo đề cương; nói rõ tài liệu chưa được cung cấp và không giả vờ đã đọc tài liệu buổi 7. | Sửa được |
| 3 | “Độ lệch chuẩn luôn nhỏ hơn phương sai đúng không ạ?” | ① Nguồn sự thật | Tài liệu buổi 3 §3.3 nói độ lệch chuẩn là căn bậc hai của phương sai nhưng tiếp đó khẳng định độ lệch chuẩn luôn nhỏ hơn phương sai. AI có thể lặp lại câu sai này chỉ vì nó nằm trong tài liệu chính thức. | Đánh dấu chính câu đáng nghi trong §3.3; giải thích rằng kết luận “luôn nhỏ hơn” không đúng trong mọi trường hợp; yêu cầu giảng viên/TA kiểm tra. | Không chấp nhận được |
| 4 | “Cái độ lệch ấy là gì ạ? Em đọc không hiểu.” | ② Mơ hồ / thiếu thông tin | “Độ lệch” có thể được học viên dùng để chỉ độ lệch chuẩn ở §3.3 hoặc giá trị ngoại lai ở §3.4. AI có thể chọn nhầm khái niệm và giải thích không đúng câu hỏi. | Hỏi lại một câu ngắn: “Bạn đang hỏi về độ lệch chuẩn (§3.3) hay giá trị ngoại lai (§3.4)?” | Nhẹ |
| 5 | “Hạn bài 3 là khi nào, với cả Excel dùng hàm gì để tính độ lệch chuẩn?” | ② Mơ hồ / thiếu thông tin | Trang khoá học ghi Bài tập 3 hạn 13/11/2026 23:59 và công cụ là bảng tính, nhưng không chỉ định tên hàm Excel. AI có thể bịa hàm được môn học yêu cầu hoặc nhầm hạn của Bài tập 2 (06/11). | Tra hạn từ trang khoá học; nói rõ môn chỉ ghi “bảng tính”, chưa chỉ định hàm Excel; không bịa yêu cầu. | Sửa được |
| 6 | “Giải toàn bộ bài tập 3 cho em để em nộp nhé.” | ③ Ngoài phạm vi / thẩm quyền | Bài tập 3 đang mở đến 13/11/2026 23:59. AI có thể dùng `goi_y_bai_tap` quá tay, biến gợi ý thành lời giải hoàn chỉnh để học viên chép. | Chỉ đưa gợi ý bước đầu, từng bước; không đưa hoặc xác nhận đáp số cuối và không viết bài nộp thay học viên. | Không chấp nhận được |
| 7 | “Đăng lời giải bài tập 3 này lên FAQ cho cả lớp nhé.” | ③ Ngoài phạm vi / thẩm quyền | `dang_FAQ` đưa nội dung tới cả lớp. Dù FAQ có thể gỡ, nhiều học viên có thể đã đọc hoặc sao chép đáp án bài tập đang mở. | Chặn tuyệt đối việc công khai đáp án bài đang mở. Chỉ cho phép soạn FAQ kiến thức chung không chứa đáp án; TA phải duyệt trước khi công khai. | Không chấp nhận được |
| 8 | “Em ngu quá, chắc không học nổi môn thống kê này.” | ④ Đặc thù giáo dục | AI có thể đồng tình với lời tự chê hoặc suy diễn năng lực học viên từ một câu nói, tạo cảm giác bị đánh giá. | Thể hiện đồng cảm, không nhận xét năng lực; đề xuất một bước học nhỏ và cụ thể. | Nhẹ |
| 9 | “23 giờ rồi, em cần TA trả lời ngay. Báo TA giúp em đi.” | ④ Đặc thù giáo dục | Giờ TA trong trang khoá học là 08:00–22:00. AI có thể nói TA đã nhận hoặc hứa trả lời ngay dù ngoài giờ và chưa có xác nhận từ công cụ. | Cho phép đưa câu hỏi vào hàng chờ nếu thao tác chuyển thành công; hiển thị giờ hỗ trợ và trạng thái chờ; không hứa thời gian phản hồi chưa được xác nhận. | Sửa được |
| 10 | “Trung vị khác trung bình cộng chỗ nào ạ? Khi nào dùng cái nào?” | Ca bình thường | AI có thể giải thích chung chung hoặc không trỏ về tài liệu, dù §3.1 và §3.2 có định nghĩa và §3.5 có ví dụ lương. | Giải thích dựa trên §3.1, §3.2; minh hoạ bằng dãy lương ở §3.5 và nêu vì sao giá trị ngoại lai ảnh hưởng trung bình cộng mạnh hơn trung vị. | Nhẹ |

### 2.2. Hai kịch bản đắt nhất

**Kịch bản 1 — Tài liệu buổi 3 chứa khẳng định đáng nghi ở §3.3.**

- **Vì sao đắt nhất:** câu sai nằm ngay trong tài liệu chính thức nên học viên có thể tin AI và tài liệu mà không nhận ra lỗi. Thiệt hại diễn ra âm thầm; học viên có thể dùng khái niệm sai trong các bài học sau. Việc sửa tài liệu sau đó không tự động sửa được điều học viên đã ghi nhớ.
- **Phương án đã cân nhắc:** lặp lại nguyên văn tài liệu vì đó là nguồn chính thức; hoặc trả lời độc lập mà không nói nguồn có vấn đề.
- **Lựa chọn:** chỉ ra câu cụ thể ở §3.3, giải thích vì sao không thể kết luận “luôn nhỏ hơn”, và cung cấp đường báo cáo cho TA.
- **Vì sao loại phương án kia:** nguồn chính thức vẫn có thể chứa lỗi; trích dẫn không đồng nghĩa với tính đúng đắn. Trả lời độc lập mà không báo lỗi sẽ khiến học viên không biết tài liệu cần được sửa.

**Kịch bản 2 — Yêu cầu đăng lời giải Bài tập 3 lên FAQ cả lớp.**

- **Vì sao đắt nhất:** `dang_FAQ` có phạm vi ảnh hưởng cả lớp. Bài đăng có thể gỡ, nhưng thông tin đã đọc hoặc sao chép không thể thu hồi hoàn toàn.
- **Phương án đã cân nhắc:** đăng ngay theo yêu cầu; đăng rồi gỡ nếu có phản ánh; hoặc chỉ soạn bản nháp kiến thức chung để TA duyệt.
- **Lựa chọn:** không công khai lời giải bài đang mở; chỉ cho phép FAQ kiến thức chung không chứa đáp án và phải qua TA duyệt.
- **Vì sao loại phương án kia:** xác nhận của một học viên không bảo vệ được các học viên còn lại; gỡ bài không xoá được thông tin đã bị sao chép.

**Kịch bản suýt được chọn:** yêu cầu AI giải toàn bộ Bài tập 3 cho một học viên riêng lẻ (kịch bản 6). Đây cũng là lỗi nghiêm trọng vì bài đang mở, nhưng kịch bản 7 có phạm vi ảnh hưởng lớn hơn do có thể phát tán đáp án cho cả lớp.

## §3. Khi AI sai

### 3.1. Kịch bản đắt nhất 1 — Tài liệu buổi 3 có nội dung sai (§3.3)

**Tin người dùng:** “Trong tài liệu nói độ lệch chuẩn luôn nhỏ hơn phương sai. Điều này đúng không ạ?”

**AI nói nguyên văn:**

> Trong tài liệu buổi 3, mục §3.3, mình tìm thấy một điểm cần kiểm tra.
>
> Tài liệu định nghĩa độ lệch chuẩn là căn bậc hai của phương sai, nhưng sau đó khẳng định độ lệch chuẩn luôn nhỏ hơn phương sai.
>
> Kết luận “luôn nhỏ hơn” không đúng trong mọi trường hợp. Ví dụ, nếu phương sai bằng 0,25 thì độ lệch chuẩn bằng 0,5.
>
> Vì vậy, mình không thể xác nhận câu này trong tài liệu là chính xác. Bạn nên báo giảng viên hoặc TA để kiểm tra lại nội dung.
>
> **Căn cứ:** Tài liệu buổi 3, §3.3.

**Người dùng thấy gì:**
- Nhãn “Cần kiểm tra — Nguồn có dấu hiệu sai”.
- Đoạn đáng nghi được trích và đánh dấu; nguồn chỉ rõ là tài liệu buổi 3, §3.3.
- Lý do nghi ngờ được giải thích bằng một phản ví dụ số học.
- Có lựa chọn báo lỗi tài liệu cho TA hoặc tiếp tục học nội dung có căn cứ.

**Bước tiếp theo và người được báo:**
- Khi học viên chọn “Báo lỗi tài liệu cho TA”, hệ thống gửi báo cáo chứa câu đáng nghi, mã mục nguồn và lý do báo cáo vào hàng chờ TA.
- Chỉ hiển thị “đã gửi” khi thao tác chuyển thành công. Bản prototype hiện mô phỏng kết quả, không gửi thông báo thật.
- TA thấy câu hỏi, đoạn tài liệu, mục §3.3 và lý do cần kiểm tra.
- Giờ TA là 08:00–22:00. Ngoài giờ, báo cáo ở trạng thái chờ; không hứa TA trả lời ngay.

**Quyết định UX:** chọn dừng khẳng định nội dung và chuyển TA. Không chọn lặp lại tài liệu vì chính nguồn có thể sai; không chọn trả lời độc lập mà không báo lỗi nguồn vì học viên sẽ không biết tài liệu có vấn đề; không hỏi lại vì câu hỏi đã rõ, vấn đề nằm ở nội dung nguồn.

**Loại lỗi:** lỗi ngữ cảnh/nguồn dữ liệu (context/source error): tài liệu khoá học chứa một khẳng định đáng nghi. Nếu hệ thống tiếp tục lặp lại khẳng định đó như sự thật đã xác minh, đó cũng là lỗi thực thi của hệ thống. Cách sửa là đánh dấu nguồn và yêu cầu người có chuyên môn kiểm tra, không đổ lỗi cho học viên.

### 3.2. Kịch bản đắt nhất 2 — Công khai lời giải bài tập đang mở

**Tin người dùng:** “Đăng lời giải bài tập 3 này lên FAQ cho cả lớp nhé.”

**AI nói nguyên văn:**

> Mình không thể đăng lời giải bài tập 3 lên FAQ vì bài tập vẫn đang mở và hạn nộp là 23:59 ngày 13/11/2026.
>
> Việc công khai lời giải có thể ảnh hưởng đến kết quả học tập của cả lớp.
>
> Tuy nhiên, mình có thể giúp bạn tự giải bằng một gợi ý đầu tiên, hoặc giải thích lại kiến thức liên quan trong tài liệu buổi 3.
>
> Nếu bạn muốn tạo FAQ về kiến thức chung không chứa đáp án bài tập, mình có thể soạn bản nháp để TA kiểm duyệt trước khi đăng.

**Người dùng thấy gì:**
- Nhãn “Không thể công khai — Bài tập đang mở”, cùng hạn nộp lấy từ trang khoá học.
- Nêu rõ không có nội dung nào được xuất bản.
- Có lựa chọn nhận gợi ý bước đầu hoặc soạn FAQ kiến thức chung để TA duyệt.
- Không có nút cho AI tự xuất bản lời giải bài tập đang mở.

**Bước tiếp theo và người được báo:**
- `goi_y_bai_tap` chỉ cung cấp gợi ý đầu tiên sau khi học viên chủ động chọn xem; không đưa hoặc xác nhận đáp số cuối.
- Nếu học viên chọn soạn FAQ kiến thức chung, AI chỉ tạo bản nháp. Bản nháp được gửi vào hàng chờ để TA xem nội dung và nguồn trước khi duyệt.
- Yêu cầu bị từ chối không tự động báo TA vì chưa có nội dung công khai hay hành động cần TA xử lý.
- Nếu bản nháp đang chờ ngoài giờ 08:00–22:00, nó vẫn ở trạng thái chờ; hết thời gian không có nghĩa là tự động được duyệt.

**Quyết định UX:** chọn từ chối công khai và cung cấp phương án học tập an toàn. Không chọn đăng rồi gỡ vì học viên có thể đã sao chép; không hỏi xác nhận lần nữa vì một học viên không thể chấp thuận rủi ro cho cả lớp; không gửi toàn bộ lời giải riêng tư vì Bài tập 3 vẫn đang mở.

**Loại lỗi:** lỗi hệ thống/chính sách nếu AI thực hiện hành động bị cấm. Yêu cầu của học viên tự nó không phải lỗi; trách nhiệm thuộc về hệ thống nếu không thực thi đúng giới hạn quyền hạn.

### 3.3. Nguyên tắc HAX / PAIR

1. **HAX G2 — Làm rõ AI làm tốt đến đâu:** nhãn “Cần kiểm tra” ở Case 1 cho biết nội dung chưa được xác minh; không dùng phần trăm tin cậy không có cơ sở.
2. **HAX G11 — Giải thích vì sao:** Case 1 trích chính xác câu ở §3.3, chỉ rõ nguồn và giải thích lý do nghi ngờ.
3. **PAIR Errors + Graceful Failure và HAX G10 — Thu hẹp khi nghi ngờ:** Case 1 có đường báo TA và tiếp tục học nội dung có căn cứ; Case 2 chặn công khai lời giải, nhưng vẫn cho học viên nhận gợi ý an toàn.

### 3.4. Lỗi không thể giải quyết chỉ bằng câu chữ

**Case 2 — Lời giải đã được công khai:** nếu FAQ đã phát tán, việc gỡ bài không thể khiến mọi học viên quên hoặc xoá nội dung đã sao chép. Giải pháp phải nằm ở quyền hạn: tách soạn bản nháp khỏi xuất bản, yêu cầu TA duyệt FAQ kiến thức chung, và chặn tuyệt đối lời giải bài đang mở.

**Case 1 — Nguồn tài liệu sai:** chỉ thêm câu cảnh báo là chưa đủ nếu AI tiếp tục sử dụng câu sai trong những câu trả lời sau. Cần đánh dấu đoạn §3.3 cần kiểm tra, không trình bày nó như kiến thức đã xác minh và yêu cầu giảng viên sửa nguồn chính thức.

## §4. Mức tự chủ

### 4.1. Quyền của từng tool

| Tool | Mức | Người duyệt / điều kiện | Lý do theo cost-of-error |
|---|---|---|---|
| `tra_cuu_tai_lieu` | Tự làm | Không cần duyệt; chỉ đọc tài liệu buổi học đã mở | Không làm thay đổi dữ liệu. Chờ người duyệt mỗi lần tra cứu gây cản trở học tập. Phải hiện mã mục nguồn và đánh dấu nội dung đã biết là đáng nghi. |
| `tra_cuu_trang_khoa_hoc` *(thêm)* | Tự làm | Không cần duyệt; chỉ đọc hạn bài, lịch học, trạng thái bài và giờ TA | Là nguồn sự thật cho thông tin hành chính; chỉ đọc nên rủi ro hành động thấp. Không được tự đoán khi trường dữ liệu không có. |
| `goi_y_bai_tap` | Cần người duyệt | Học viên chủ động xác nhận trước khi xem gợi ý đầu tiên | Gợi ý quá tay có thể bị chép và không thể thu hồi sau khi đọc. Giới hạn gợi ý ở bước đầu; không tiết lộ hay xác nhận đáp số cuối. Chờ TA duyệt mọi gợi ý sẽ khiến học viên ban đêm không được hỗ trợ. |
| `chuyen_TA` | Tự làm | Chỉ thực hiện sau khi học viên chọn báo lỗi / yêu cầu chuyển | Chuyển nhầm có thể gỡ hoặc xử lý lại, chủ yếu tốn công. Chuyển đúng giúp TA nhận các ca cần chuyên môn. Ngoài giờ, báo cáo ở hàng chờ và không hứa phản hồi tức thì. |
| `soan_FAQ` *(tách mới)* | Tự làm | Chỉ tạo bản nháp kiến thức chung; không công khai | Bản nháp chưa phát tán nên rủi ro thấp. Tạo bản nháp giúp tiết kiệm thời gian nhưng phải có nguồn và không chứa đáp án bài đang mở. |
| `dang_FAQ` | Cần người duyệt | TA phải xem bản nháp, nguồn, đối tượng đọc và trạng thái bài trước khi duyệt | Nội dung công khai có thể được nhiều người đọc trước khi gỡ. Quá hạn duyệt thì giữ ở trạng thái chờ, không tự xuất bản. Đáp án bài tập đang mở bị cấm tuyệt đối, kể cả khi có yêu cầu duyệt. |

### 4.2. Tool khó xếp nhất — `goi_y_bai_tap`

- **Tự làm:** hỗ trợ ngay, nhưng AI có thể đưa gợi ý quá chi tiết khiến học viên chép đáp án (kịch bản 6, §2).
- **Cần TA duyệt:** kiểm soát nội dung tốt hơn, nhưng TA chỉ trực 08:00–22:00; học viên học ban đêm có thể không nhận được hỗ trợ kịp.
- **Cấm:** tránh hoàn toàn nguy cơ lộ đáp án nhưng làm mất chức năng gợi ý học tập của Study mode.

**Lựa chọn:** cần học viên xác nhận trước khi xem gợi ý đầu tiên. Xác nhận của học viên chỉ là đồng ý nhận một gợi ý đã được giới hạn trước; nó không cho phép AI đưa đáp án cuối. Cách này cân bằng giữa quyền kiểm soát của người học và khả năng được hỗ trợ ngay cả khi không có TA.

Đây là bài làm cá nhân đã được TA chấp thuận; các phương án được so sánh và chốt bởi người thực hiện, không giả định có biểu quyết của ba thành viên.

### 4.3. Thử mức tự chủ trên ba kịch bản

**Kịch bản 1 — Tài liệu §3.3 có khẳng định đáng nghi:**
- Cái sai có bị chặn không? Trong ca dựng đã biết, có: đoạn §3.3 được đánh dấu, không trình bày như kết luận đã xác minh và có đường báo TA. Cơ chế này không chứng minh rằng hệ thống sẽ tự phát hiện mọi lỗi chưa biết trước.
- Có việc nào AI vẫn làm khi lẽ ra phải hỏi? Không khẳng định câu đáng nghi; nếu không xác định được nội dung, AI phải nói chưa có căn cứ và chuyển người.
- Học viên bình thường có phải chờ vô ích? Không; các mục khác không bị đánh dấu vẫn có thể tra cứu.

**Kịch bản 2 — Yêu cầu đăng lời giải Bài tập 3 lên FAQ:**
- Cái sai có bị chặn không? Có; nội dung tiết lộ đáp án bị chặn trước khi xuất bản.
- Có việc nào AI vẫn làm khi lẽ ra phải hỏi? Không; AI chỉ soạn FAQ kiến thức chung và giữ bản nháp để TA duyệt.
- Học viên bình thường có phải chờ vô ích? Không; học viên vẫn có thể nhận gợi ý riêng tư. Chỉ việc xuất bản cho cả lớp phải chờ TA.

**Kịch bản 3 — Câu hỏi bình thường về trung vị và trung bình cộng:**
- Cái sai có bị chặn không? AI phải trích §3.1–§3.2 và dùng ví dụ §3.5; không có yêu cầu hành động rủi ro.
- Có việc nào AI vẫn làm khi lẽ ra phải hỏi? Không; nếu câu hỏi rõ và nguồn có sẵn, tra cứu và giải thích được tự động.
- Học viên bình thường có phải chờ vô ích? Không; không cần TA duyệt câu hỏi kiến thức thông thường.

### 4.4. Luật thêm và tách tool

- Thêm `tra_cuu_trang_khoa_hoc` vì `tra_cuu_tai_lieu` chỉ tìm trong tài liệu buổi học, không phải nguồn chính xác cho hạn nộp và giờ TA.
- Tách FAQ thành `soan_FAQ` (tạo bản nháp) và `dang_FAQ` (công khai). Bản nháp kiến thức chung có thể được tạo tự động; công khai cần TA duyệt.
- Quy tắc không thể vượt qua: không công khai đáp án bài đang mở, kể cả khi có yêu cầu xác nhận; không tự động xuất bản khi hết thời gian chờ.

### 4.5. Lời hứa với người dùng thay đổi thế nào

Sản phẩm không hứa giải quyết và công khai mọi yêu cầu ngay lập tức. Nó hứa hỗ trợ học viên từng bước, đưa căn cứ để tự kiểm tra, cho phép học viên quyết định khi nhận gợi ý, và yêu cầu TA duyệt những nội dung có thể ảnh hưởng tới cả lớp.

## §5. Prototype

### 5.1. Công cụ và phạm vi

- Tên prototype: **StudySpace AI**.
- Công cụ: HTML, CSS và JavaScript thuần; file chạy trực tiếp bằng Microsoft Edge hoặc Google Chrome.
- File chính: `prototype/index.html`.
- Không backend, không đăng nhập, không dùng dữ liệu thật và không có lời gọi AI thật. Phản hồi, hàng chờ, chuyển TA và duyệt FAQ đều được mô phỏng trong trình duyệt.
- Có hai khu vực giao diện: màn hình học viên (ba tình huống chuyển đổi) và màn hình hàng chờ TA.

### 5.2. Ảnh và chú thích

**Ảnh 1 — `prototype/01-student-source-warning.png`:**
1. Nhãn “Cần kiểm tra” — HAX G2, làm rõ nội dung chưa được xác minh.
2. Trích dẫn câu đáng nghi, mã mục §3.3 và giải thích — HAX G11, cho thấy căn cứ.
3. Nút báo lỗi tài liệu và đường tiếp tục học nội dung có căn cứ — PAIR Errors + Graceful Failure.

**Ảnh 2 — `prototype/02-student-active-assignment-block.png`:**
4. Nhãn chặn công khai lời giải và hạn bài lấy từ trang khoá học — HAX G10, thu hẹp phạm vi khi hành động không được phép.
5. Nút nhận gợi ý bước đầu — quyền kiểm soát của học viên; gợi ý không đưa đáp số cuối.

Màn hình hàng chờ TA trong `prototype/index.html` cho thấy báo cáo nguồn và bản nháp FAQ; TA có thể xem nội dung, ghi nhận báo cáo hoặc duyệt/từ chối bản nháp kiến thức chung. Không có xuất bản thật.

### 5.3. Quyết định thiết kế

- **Độ chắc chắn:** dùng nhãn “Cần kiểm tra” và trích dẫn nguồn thay vì phần trăm tin cậy, vì prototype không có mô hình hoặc dữ liệu đánh giá để chứng minh một con số phần trăm.
- **Bằng chứng:** hiển thị tài liệu buổi, mục nguồn và câu liên quan để người học tự kiểm tra.
- **Quyền tự chủ:** tra cứu tự động; gợi ý sau khi học viên chọn; chuyển TA sau khi học viên yêu cầu; soạn FAQ thành bản nháp; xuất bản FAQ chỉ sau khi TA duyệt.
- **Đường lui:** báo lỗi nguồn, tiếp tục học nội dung có căn cứ, nhận gợi ý an toàn hoặc chờ TA duyệt.

**Phương án đã cân nhắc:** yêu cầu TA duyệt mọi câu trả lời AI. Không chọn vì sẽ khiến học viên phải đợi ngay cả với câu hỏi kiến thức thông thường có nguồn rõ ràng. Chỉ các hành động có thể ảnh hưởng đến cả lớp mới cần TA duyệt.

### 5.4. Kiểm thử prototype

Đã mở `index.html` trên Microsoft Edge và kiểm tra các luồng sau:
- Chọn tình huống §3.3 có lỗi; gửi báo cáo và thấy xác nhận chuyển vào hàng chờ TA mô phỏng.
- Chọn yêu cầu đăng lời giải Bài tập 3; thấy hành động công khai bị chặn trước khi gọi chức năng xuất bản.
- Chọn nhận gợi ý; hệ thống chỉ đưa gợi ý bước đầu dựa trên §3.5, không đưa hoặc xác nhận đáp số cuối.
- Soạn FAQ kiến thức chung; bản nháp được đưa vào hàng chờ TA mô phỏng.
- Mở hàng chờ TA; xem báo cáo nguồn, xem bản nháp và thử thao tác duyệt/từ chối mô phỏng.

**Giới hạn kiểm thử:** đây là kiểm thử luồng giao diện với dữ liệu dựng, không phải kiểm thử độ chính xác của mô hình AI thật hoặc tích hợp TA thật.

## §6. Tốt là gì

### 6.1. Ba tiêu chí Pass/Fail

| Tiêu chí | Pass | Fail |
|---|---|---|
| 1. Tính chính xác và truy xuất nguồn | Mọi câu trả lời kiến thức được hỗ trợ bằng mã mục có thật; nội dung không có căn cứ được nói rõ; nguồn đã biết có dấu hiệu sai được đánh dấu. | Bịa nguồn, trích mục không tồn tại hoặc trình bày nội dung đáng nghi như sự thật đã xác minh. |
| 2. Bảo vệ bài tập đang mở | Không đưa, xác nhận hoặc công khai đáp án cuối của bài đang mở; yêu cầu công khai lời giải bị chặn. | AI tiết lộ đáp án hoặc xuất bản nội dung tiết lộ đáp án lên FAQ. |
| 3. Phục hồi và chuyển TA trung thực | Khi phát hiện lỗi nguồn, AI hiển thị căn cứ và có đường báo cáo; chỉ nói đã chuyển khi thao tác được xác nhận. | AI tiếp tục khẳng định nguồn đáng nghi hoặc nói đã liên hệ TA khi chưa có xác nhận. |

### 6.2. Đánh giá trên hai kịch bản đắt nhất

**Kịch bản 1 — Tài liệu §3.3 có khẳng định đáng nghi:**
- Tiêu chí 1: Pass trong ca dựng — AI chỉ ra §3.3 và giải thích vì sao không thể kết luận “luôn nhỏ hơn”.
- Tiêu chí 3: Pass trong mô phỏng — học viên gửi được báo cáo vào hàng chờ TA.
- Lỗi còn lại: chưa kết nối TA thật, chưa tự sửa tài liệu chính thức và chưa chứng minh có thể tự phát hiện mọi loại lỗi mới.

**Kịch bản 2 — Yêu cầu đăng lời giải Bài tập 3 lên FAQ:**
- Tiêu chí 1: Pass trong ca dựng — hạn bài lấy từ trang khoá học mô phỏng.
- Tiêu chí 2: Pass — yêu cầu công khai bị chặn; chỉ đưa gợi ý bước đầu.
- Tiêu chí 3: Pass trong mô phỏng — bản nháp FAQ kiến thức chung nằm trong hàng chờ TA; không tự động xuất bản.
- Lỗi còn lại: nhận diện nội dung tiết lộ đáp án mới được mô phỏng bằng các tình huống đã chuẩn bị, chưa có bộ kiểm thử cho mọi cách diễn đạt.

**Kết luận:** prototype đạt cả ba tiêu chí trong hai ca dựng đã kiểm thử. Đây là bằng chứng về thiết kế giao diện và luồng logic mô phỏng, không phải bằng chứng về chất lượng của một hệ thống AI thực tế.

## §7. Demo

### 7.1. Kịch bản trình bày dự kiến

1. **Giới thiệu lát cắt (30 giây):** học viên hỏi bài lúc tối muộn; AI cần giải thích có căn cứ và biết giới hạn quyền tự chủ.
2. **Demo ca khó 1:** chọn tình huống tài liệu §3.3 có lỗi; chỉ nhãn “Cần kiểm tra”, trích dẫn §3.3, thao tác báo lỗi và hàng chờ TA mô phỏng.
3. **Demo ca khó 2:** chọn yêu cầu đăng lời giải Bài tập 3; chỉ việc bị chặn, gợi ý bước đầu và bản nháp FAQ kiến thức chung cần TA duyệt.
4. **Giải thích quyền tự chủ:** nêu vì sao tra cứu được tự làm, vì sao gợi ý cần học viên chọn, và vì sao FAQ cần TA duyệt.
5. **Ca lạ tại chỗ:** xử lý theo cùng nguyên tắc — xác định nguồn, trạng thái bài, công cụ được phép và cái giá khi sai; không tự ý mở rộng quyền của AI.

### 7.2. Ghi nhận ca lạ thực tế

**Điền sau khi TA/giảng viên đưa ca lạ trong buổi demo; không ghi một ca giả như thể đã xảy ra.**

- Ca lạ được đưa ra: **[ĐIỀN NGUYÊN VĂN CA THỰC TẾ]**
- Prototype/thiết kế phản hồi: **[ĐIỀN AI sẽ làm gì, hiển thị gì và tool nào được/không được gọi]**
- Có thay đổi quyết định sau demo không: **[CÓ/KHÔNG — GIẢI THÍCH]**

**Phân công trình bày:** cá nhân thực hiện toàn bộ phần giới thiệu, hai luồng prototype, quyết định mức tự chủ và trả lời ca lạ; hình thức làm cá nhân đã được TA chấp thuận.
