# 3. Khung lý thuyết

Để xây dựng nền tảng vững chắc cho việc phân tích và thiết kế lại hệ thống truyền thông tại Trung tâm Công nghệ Giáo dục, báo cáo này áp dụng bốn lý thuyết và mô hình truyền thông cốt lõi. Sự kết hợp giữa các mô hình truyền thống và hiện đại giúp nhận diện toàn diện từ các lỗi truyền tín hiệu kỹ thuật cho đến các rào cản tâm lý, nhận thức của người học.

## 3.1. Mô hình truyền thông tuyến tính Shannon–Weaver

Mô hình Shannon và Weaver (1949), kế thừa nền tảng từ công thức truyền thông tuyến tính của Lasswell (1948), ban đầu được thiết kế để tối ưu hóa hiệu suất truyền tín hiệu kỹ thuật. Mô hình mô tả truyền thông là một tiến trình tuyến tính một chiều bao gồm các thành phần: Nguồn phát $\rightarrow$ Mã hóa $\rightarrow$ Thông điệp $\rightarrow$ Kênh $\rightarrow$ Giải mã $\rightarrow$ Người nhận. Yếu tố cốt lõi của mô hình này là sự xuất hiện của nhiễu - bất kỳ tác nhân nào làm biến dạng hoặc cản trở thông điệp từ nguồn phát đến người nhận.

Trong bối cảnh giáo dục trực tuyến tại trung tâm, mô hình Shannon–Weaver được áp dụng để phân tích các đứt gãy mang tính kỹ thuật và vật lý:
*   Kênh truyền thông nội bộ qua nhóm chat: Thông điệp kỹ thuật từ chuyên viên được mã hóa bằng văn bản gửi đến giảng viên. Tuy nhiên, mật độ thông tin quá cao trong nhóm chat tạo ra nhiễu vật lý do tin nhắn trôi nhanh, làm suy hao và biến dạng thông điệp ban đầu, dẫn đến việc giải mã sai lệch các yêu cầu kỹ thuật.
*   Kênh truyền thông với học viên qua website và email: Giao diện daotao.ai đóng vai trò là kênh truyền tải thông điệp hướng dẫn đăng ký hoặc đăng nhập. Các lỗi kỹ thuật của hệ thống và việc che khuất các nút tương tác, chẳng hạn như nút đăng ký, được xem là nhiễu kỹ thuật, trực tiếp ngăn cản học viên giải mã và thực hiện hành vi mong muốn.

## 3.2. Mô hình truyền thông giao dịch và tương tác

Khác với mô hình tuyến tính, mô hình tương tác của Schramm (1954) và mô hình giao dịch của Barnlund (1970) nhìn nhận truyền thông là một quá trình hai chiều đồng thời, nơi các bên tham gia đều đóng vai trò là người truyền thông, vừa gửi vừa nhận thông điệp. Mô hình này nhấn mạnh hai yếu tố:
1.  Vòng phản hồi: Dòng thông tin phản hồi từ người nhận ngược trở lại người gửi để điều chỉnh thông điệp.
2.  Trường kinh nghiệm: Toàn bộ nền tảng kiến thức, văn hóa, thái độ và kỹ năng của mỗi cá nhân. Truyền thông đạt hiệu quả khi trường kinh nghiệm của người gửi và người nhận có phần giao thoa đủ lớn.

Ứng dụng mô hình giao dịch vào hệ thống hỗ trợ của daotao.ai chỉ ra hai vấn đề:
*   Đứt gãy vòng phản hồi: Khối lượng yêu cầu hỗ trợ lớn khiến chuyên viên không thể phản hồi kịp thời qua biểu mẫu web hay Zalo. Sự chậm trễ này làm đứt gãy vòng phản hồi tức thì, khiến học viên lớn tuổi cảm thấy bị cô lập trong môi trường số, dẫn đến mất động lực học tập.
*   Sự lệch pha về trường kinh nghiệm: Chuyên viên vận hành có trình độ công nghệ cao thường mã hóa thông điệp hướng dẫn bằng các thuật ngữ chuyên môn. Trong khi đó, học viên lớn tuổi thuộc Đề án 06 có trường kinh nghiệm công nghệ hạn chế nên không thể giải mã được các hướng dẫn này, gây ra sự bất đối xứng thông tin.

## 3.3. Thuyết phong phú truyền thông

Thuyết phong phú truyền thông của Daft và Lengel (1986) lập luận rằng các kênh truyền thông có khả năng truyền tải lượng thông tin khác nhau tùy thuộc vào mức độ phong phú của chúng. Độ phong phú được đo lường bằng khả năng cung cấp phản hồi tức thì, khả năng truyền tải các tín hiệu phi ngôn ngữ như hình ảnh, âm thanh, mức độ cá nhân hóa và sự đa dạng ngôn ngữ. Kênh được chia từ phong phú như giao tiếp trực tiếp, video, chatbot tương tác, đến nghèo nàn như văn bản tĩnh, biểu mẫu điền thông tin.

Lý thuyết này chỉ ra rằng đối với các nhiệm vụ có độ mơ hồ cao như khắc phục lỗi đăng nhập hệ thống hoặc thao tác đăng ký lớp học đối với người kém công nghệ, việc sử dụng kênh truyền thông nghèo nàn như gửi biểu mẫu hỗ trợ bằng chữ sẽ gặp khó khăn:
*   Học viên kém công nghệ cần các kênh giàu thông tin gồm hình ảnh trực quan và tương tác từng bước để hiểu cách xử lý lỗi.
*   Việc tích hợp chatbot trực quan trên website daotao.ai và xây dựng video hướng dẫn ngắn sẽ nâng cấp kênh truyền từ nghèo nàn lên phong phú, giúp tối ưu hóa việc truyền tải các thông điệp kỹ thuật phức tạp.

## 3.4. Thuyết tải nhận thức

Thuyết tải nhận thức của John Sweller (1988) giải thích cách bộ nhớ làm việc xử lý thông tin. Bộ nhớ làm việc có giới hạn về dung lượng và phải điều phối cho ba loại tải nhận thức:
1.  Tải nhận thức bản chất: Độ khó tự thân của nội dung kiến thức bài học.
2.  Tải nhận thức ngoại lai: Lượng năng lượng trí tuệ tiêu tốn do cách trình bày thông tin hoặc thiết kế giao diện không tối ưu.
3.  Tải nhận thức hữu ích: Nỗ lực trí tuệ được sử dụng để kiến tạo sơ đồ nhận thức và ghi nhớ kiến thức vào bộ nhớ dài hạn.

Nguyên lý cốt lõi trong công nghệ giáo dục là tối thiểu hóa tải nhận thức ngoại lai để giải phóng bộ nhớ làm việc, nhường chỗ cho tải nhận thức hữu ích:
*   Giao diện phức tạp, nút đăng ký bị ẩn và các email hướng dẫn dài dòng chứa đầy thuật ngữ kỹ thuật đang tạo ra một lượng tải nhận thức ngoại lai lớn cho học viên lớn tuổi.
*   Để giải quyết, bộ mẫu email mới trực quan và chatbot phân nhánh sẽ đơn giản hóa cấu trúc thông tin. Bằng cách giảm tải nhận thức ngoại lai, học viên sẽ dễ dàng tự khắc phục lỗi kỹ thuật và tập trung năng lượng trí tuệ vào việc tiếp thu bài học.
