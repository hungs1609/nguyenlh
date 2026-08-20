# Đề tài nghiên cứu: Ứng dụng AI tạo sinh hỗ trợ giảng viên tự động tạo học liệu và thiết kế hoạt động dạy học tại Đại học Bách khoa Hà Nội

## THÔNG TIN TỔNG QUAN (THẺ ĐỀ TÀI)

* **Đề tài đề xuất:** Ứng dụng AI tạo sinh hỗ trợ giảng viên tự động tạo học liệu và thiết kế hoạt động dạy học tại Đại học Bách khoa Hà Nội
* **Luận điểm cốt lõi:** AI tạo sinh chưa thể thay thế vai trò định hướng của giảng viên, nhưng là công cụ hỗ trợ quan trọng giúp giảm tải áp lực chuẩn bị học liệu và soạn bài giảng. Bằng việc thiết kế và thử nghiệm một công cụ AI tạo sinh hỗ trợ xử lý nội dung bài giảng, nghiên cứu làm rõ khả năng ứng dụng AI trong việc tự động tạo câu hỏi kiểm tra, tóm tắt học liệu và đề xuất hoạt động học tập phù hợp với đặc thù đào tạo khối ngành kỹ thuật tại Đại học Bách khoa Hà Nội.

---

## KHUNG CẤU TRÚC ĐỀ TÀI

### 1. Mở đầu
Trong những năm gần đây, trí tuệ nhân tạo đã có những bước phát triển vượt bậc và trở thành một công cụ quen thuộc trong đời sống hằng ngày cũng như trong giáo dục. Tại các trường đại học, AI mở ra nhiều cơ hội lớn để tối ưu hóa công việc, đặc biệt là hỗ trợ giảng viên trong công tác giảng dạy. Tuy nhiên, việc chuẩn bị tài liệu, soạn slide hay thiết kế các bộ câu hỏi kiểm tra thủ công hiện nay vẫn tiêu tốn rất nhiều thời gian của người dạy. Vấn đề đặt ra là làm thế nào để tận dụng sức mạnh của AI vào quy trình chuẩn bị học liệu một cách thực chất và hiệu quả.

Trước thực tế đó, các công cụ AI tạo sinh mở ra khả năng tự động hóa nhiều tác vụ học thuật như tạo câu hỏi đánh giá, tóm tắt nội dung bài giảng và đề xuất hoạt động học tập. Nếu được thiết kế phù hợp với yêu cầu sư phạm, những công cụ này có thể hỗ trợ giảng viên giảm đáng kể thời gian chuẩn bị học liệu mà vẫn đảm bảo chất lượng giảng dạy. Để đánh giá một cách khoa học xu hướng này, việc xây dựng sản phẩm demo và phân tích nhu cầu thực tế là cần thiết nhằm xây dựng cơ sở thực nghiệm vững chắc, từ đó soi chiếu vào chính đặc thù đào tạo của Đại học Bách khoa Hà Nội.

> **Câu hỏi nghiên cứu trung tâm:** AI tạo sinh có thể hỗ trợ giảng viên tự động tạo học liệu và thiết kế hoạt động dạy học như thế nào tại ĐHBK Hà Nội?

### 2. Mục tiêu nghiên cứu
* Khảo sát và tổng hợp nhu cầu thực tế cùng những khó khăn về thời gian của giảng viên trong quy trình soạn học liệu.
* Xác định các tiêu chí sư phạm cốt lõi (như Thang đo nhận thức Bloom) làm cơ sở cho việc thiết kế chức năng tạo câu hỏi và học liệu bằng AI.
* Xây dựng sản phẩm demo dưới dạng công cụ hỗ trợ giảng viên, cho phép tải lên nội dung bài giảng hoặc tài liệu học tập và tự động sinh ra câu hỏi kiểm tra, bản tóm tắt nội dung và gợi ý hoạt động học tập.
* Đánh giá hiệu quả và khả năng ứng dụng của công cụ trong việc giảm tải thời gian chuẩn bị học liệu cho giảng viên tại ĐHBK Hà Nội.

### 3. Cơ sở lý luận
* **3.1 Khái niệm và phân định công nghệ:** Trí tuệ nhân tạo (AI), AI tạo sinh (Generative AI) và các Mô hình ngôn ngữ lớn (LLMs).
* **3.2 Nền tảng lý thuyết giáo dục ứng dụng:** Thuyết kiến tạo (hoạt động tương tác) và Thang đo nhận thức Bloom (thiết kế câu hỏi).
* **3.3 Tổng quan nghiên cứu:** Ứng dụng AI tạo sinh trong thiết kế học liệu, đánh giá học tập và hỗ trợ giảng dạy.

### 4. Khung phân tích và phát triển sản phẩm
* Khảo sát nhu cầu thực tế của giảng viên về các tác vụ thường xuyên trong quá trình chuẩn bị bài giảng như xây dựng câu hỏi kiểm tra, tóm tắt nội dung và thiết kế hoạt động học tập.
* Xây dựng các nguyên tắc thiết kế nội dung đầu ra dựa trên Thang đo nhận thức Bloom, Thuyết kiến tạo và nguyên lý Human-in-the-loop.
* Thiết kế và phát triển ứng dụng web "Không gian Học liệu số HUST" cung cấp giải pháp sinh học liệu All-in-One tự động từ tài liệu học thuật nguồn bao gồm 4 phân hệ: Sơ đồ tư duy bài giảng tương tác (Mindmap), Kịch bản Slide trình chiếu, Ngân hàng câu hỏi chuẩn Thang Bloom (MCQ & Tự luận sáng tạo), và Hệ thống Phản biện sư phạm (Pedagogical Critique System với gợi ý Preset Critics).
* Thực nghiệm triển khai và kiểm thử công cụ trên các học phần thuộc khối ngành kỹ thuật/CNTT tại ĐHBK Hà Nội; đánh giá chất lượng đầu ra và mức độ tiết kiệm thời gian của giảng viên khi sử dụng công cụ.

> **Câu hỏi đánh giá thực nghiệm:** AI tạo sinh có hỗ trợ giảm tải quy trình chuẩn bị học liệu cho giảng viên tại ĐHBK Hà Nội không? Mức độ hiệu quả của AI trong các tác vụ tự động tạo câu hỏi kiểm tra, tóm tắt nội dung và gợi ý hoạt động học tập là như thế nào?