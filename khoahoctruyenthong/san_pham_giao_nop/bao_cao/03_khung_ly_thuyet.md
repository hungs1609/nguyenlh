# 3. Khung lý thuyết (Theoretical Framework)

Để xây dựng một nền tảng khoa học vững chắc cho việc phân tích và thiết kế lại hệ thống truyền thông tại Trung tâm EdTech (daotao.ai), báo cáo này áp dụng bốn lý thuyết và mô hình truyền thông cốt lõi. Sự kết hợp giữa các mô hình truyền thống (tuyến tính) và hiện đại (giao dịch, nhận thức) giúp nhận diện toàn diện từ các lỗi truyền tín hiệu kỹ thuật cho đến các rào cản tâm lý - nhận thức của người học.

## 3.1. Mô hình Shannon–Weaver (Mô hình truyền thông tuyến tính)

Được đề xuất bởi Claude Shannon và Warren Weaver (1949), kế thừa nền tảng từ công thức truyền thông tuyến tính nổi tiếng của Lasswell (1948), mô hình này ban đầu được thiết kế để tối ưu hóa hiệu suất truyền tín hiệu kỹ thuật. Mô hình mô tả truyền thông là một tiến trình tuyến tính một chiều bao gồm các thành phần: **Nguồn phát (Sender)** $\rightarrow$ **Mã hóa (Encoder)** $\rightarrow$ **Thông điệp (Message)** $\rightarrow$ **Kênh (Channel)** $\rightarrow$ **Giải mã (Decoder)** $\rightarrow$ **Người nhận (Receiver)**. Yếu tố cốt lõi của mô hình này là sự xuất hiện của **Nhiễu (Noise)** - bất kỳ tác nhân nào làm biến dạng hoặc cản trước thông điệp từ nguồn phát đến người nhận.

Trong bối cảnh giáo dục số tại EdTech Centre, mô hình Shannon–Weaver được áp dụng để phân tích các đứt gãy mang tính kỹ thuật và vật lý:
*   **Kênh truyền thông nội bộ (Zalo chat):** Thông điệp kỹ thuật từ chuyên viên EdTech (Sender) được mã hóa bằng văn bản gửi đến Giảng viên (Receiver). Tuy nhiên, mật độ thông tin quá cao trong nhóm chat Zalo tạo ra "nhiễu vật lý" (tin nhắn trôi nhanh), làm suy hao và biến dạng thông điệp ban đầu, dẫn đến việc giải mã sai lệch các yêu cầu kỹ thuật.
*   **Kênh truyền thông với học viên (Website/Email):** Giao diện daotao.ai đóng vai trò là kênh truyền tải thông điệp hướng dẫn đăng ký/đăng nhập. Các lỗi kỹ thuật của hệ thống và việc che khuất các nút tương tác (như nút đăng ký) được định nghĩa là "nhiễu kỹ thuật", trực tiếp ngăn cản học viên giải mã và thực hiện hành vi mong muốn.

## 3.2. Mô hình Truyền thông Giao dịch và Tương tác (Transactional & Interactive Model)

Khác với mô hình tuyến tính, Mô hình tương tác của Schramm (1954) và Mô hình giao dịch của Barnlund (1970) nhìn nhận truyền thông là một quá trình hai chiều đồng thời, nơi các bên tham gia đều đóng vai trò là Người truyền thông (Communicators), vừa gửi vừa nhận thông điệp. Mô hình này nhấn mạnh hai yếu tố:
1.  **Vòng phản hồi (Feedback loop):** Dòng thông tin phản hồi từ người nhận ngược trở lại người gửi để điều chỉnh thông điệp.
2.  **Trường kinh nghiệm (Field of Experience):** Toàn bộ nền tảng kiến thức, văn hóa, thái độ và kỹ năng của mỗi cá nhân. Truyền thông chỉ thành công khi trường kinh nghiệm của người gửi và người nhận có phần giao thoa đủ lớn.

Ứng dụng mô hình giao dịch vào hệ thống hỗ trợ của daotao.ai chỉ ra hai vấn đề nghiêm trọng:
*   **Đứt gãy vòng phản hồi:** Khối lượng yêu cầu hỗ trợ lớn khiến chuyên viên EdTech không thể phản hồi kịp thời qua Web Form hay Zalo OA. Sự chậm trễ này làm đứt gãy vòng phản hồi tức thì, khiến học viên (đặc biệt là học viên lớn tuổi) cảm thấy bị cô lập trong môi trường số, dẫn đến mất động lực học tập.
*   **Sự lệch pha về Trường kinh nghiệm:** Chuyên viên EdTech (trình độ công nghệ cao) mã hóa thông điệp hướng dẫn bằng các thuật ngữ chuyên môn. Trong khi đó, học viên lớn tuổi thuộc Đề án 06 (trường kinh nghiệm công nghệ rất hạn chế) không thể giải mã được các hướng dẫn này, gây ra sự bất đối xứng thông tin nghiêm trọng.

## 3.3. Thuyết Phong phú Truyền thông (Media Richness Theory)

Thuyết Phong phú Truyền thông của Daft và Lengel (1986) lập luận rằng các kênh truyền thông có khả năng truyền tải lượng thông tin khác nhau tùy thuộc vào mức độ "phong phú" của chúng. Độ phong phú được đo lường bằng: khả năng cung cấp phản hồi tức thì, khả năng truyền tải các tín hiệu phi ngôn ngữ (hình ảnh, âm thanh), cá nhân hóa và sự đa dạng ngôn ngữ. Kênh được chia từ **Phong phú (Rich Media)** như giao tiếp trực tiếp, video, chatbot tương tác, đến **Nghèo nàn (Lean Media)** như văn bản tĩnh, form điền thông tin.

Lý thuyết này chỉ ra rằng đối với các nhiệm vụ có độ mơ hồ cao (như khắc phục lỗi đăng nhập hệ thống hoặc thao tác đăng ký lớp học đối với người kém công nghệ), việc sử dụng kênh truyền thông nghèo nàn (như gửi form hỗ trợ bằng text) sẽ thất bại:
*   Học viên kém công nghệ cần các kênh giàu thông tin (hình ảnh trực quan, tương tác từng bước) để hiểu cách xử lý lỗi.
*   Việc tích hợp Chatbot AI trực quan trên website daotao.ai và xây dựng video hướng dẫn ngắn sẽ nâng cấp kênh truyền từ "nghèo nàn" lên "phong phú", giúp tối ưu hóa việc truyền tải các thông điệp kỹ thuật phức tạp.

## 3.4. Thuyết Tải nhận thức (Cognitive Load Theory)

Được phát triển bởi John Sweller (1988), Thuyết Tải nhận thức giải thích cách bộ nhớ làm việc (working memory) xử lý thông tin. Bộ nhớ làm việc có giới hạn về dung lượng và phải điều phối cho ba loại tải nhận thức:
1.  **Tải nhận thức bản chất (Intrinsic Cognitive Load):** Độ khó tự thân của nội dung kiến thức bài học.
2.  **Tải nhận thức ngoại lai (Extraneous Cognitive Load):** Lượng năng lượng trí tuệ tiêu tốn do cách trình bày thông tin hoặc thiết kế giao diện không tối ưu.
3.  **Tải nhận thức hữu ích (Germane Cognitive Load):** Nỗ lực trí tuệ được sử dụng để kiến tạo sơ đồ nhận thức và ghi nhớ kiến thức vào bộ nhớ dài hạn.

Nguyên lý cốt lõi trong EdTech là **tối thiểu hóa tải nhận thức ngoại lai** để giải phóng bộ nhớ làm việc, nhường chỗ cho tải nhận thức hữu ích (Germane Load):
*   Giao diện phức tạp, nút đăng ký bị ẩn và các email hướng dẫn dài dòng chứa đầy thuật ngữ kỹ thuật đang tạo ra một lượng **tải nhận thức ngoại lai khổng lồ** cho học viên lớn tuổi.
*   Để giải quyết, bộ Template Email mới trực quan (Visual-centric) và Chatbot AI phân nhánh sẽ đơn giản hóa tối đa cấu trúc thông tin. Bằng cách giảm tải nhận thức ngoại lai, học viên sẽ dễ dàng tự khắc phục lỗi kỹ thuật và tập trung toàn bộ năng lượng trí tuệ vào việc tiếp thu bài học.
