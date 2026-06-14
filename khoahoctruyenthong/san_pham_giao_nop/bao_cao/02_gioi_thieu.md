# 2. Giới thiệu (Introduction)

Trong kỷ nguyên số, giáo dục trực tuyến quy mô lớn (MOOCs - Massive Open Online Courses) đã trở thành trụ cột quan trọng trong việc xây dựng một xã hội học tập suốt đời. Tuy nhiên, sự thành công của một nền tảng MOOC không chỉ phụ thuộc vào chất lượng học liệu số mà còn chịu sự chi phối sâu sắc bởi hiệu suất của hệ thống truyền thông hỗ trợ học tập (Student Support Communication System). 

## 2.1. Bối cảnh nền tảng daotao.ai và Trung tâm EdTech

Nền tảng học trực tuyến daotao.ai được phát triển và vận hành bởi Trung tâm Công nghệ Giáo dục (EdTech Centre) thuộc Trường Công nghệ Thông tin và Truyền thông – Đại học Bách khoa Hà Nội. Nền tảng ra đời với sứ mệnh cung cấp các khóa học đại trà miễn phí phục vụ cộng đồng, đồng thời chịu trách nhiệm đào tạo và bồi dưỡng kỹ năng số cho hàng chục ngàn cán bộ công chức trên toàn quốc theo Đề án 06 của Chính phủ. Với quy mô người học lớn và có sự phân hóa sâu sắc về nhân khẩu học cũng như trình độ công nghệ, Trung tâm EdTech phải đối mặt với áp lực vận hành hệ thống hỗ trợ kỹ thuật cực kỳ lớn.

## 2.2. Tầm quan trọng của truyền thông tích hợp trong EdTech

Truyền thông trong giáo dục số không đơn thuần là hoạt động gửi - nhận thông tin kỹ thuật, mà thực chất là quá trình thiết kế truyền thông có mục tiêu nhằm duy trì sự tương tác ba chiều (Giảng viên - Học viên - Học liệu). Một hệ thống truyền thông tích hợp (Integrated Communication System) hiệu quả sẽ:
*   Bảo đảm sự phối hợp nhịp nhàng và chính xác tuyệt đối trong khâu số hóa học liệu giữa bộ phận kỹ thuật (EdTech Centre) và giảng viên chuyên môn (HUST).
*   Giúp người học nhanh chóng tiếp cận hướng dẫn học tập, vượt qua các rào cản thao tác kỹ thuật ban đầu để tập trung hoàn toàn vào việc tiếp thu tri thức.
*   Cung cấp vòng phản hồi nhanh chóng nhằm nâng cao trải nghiệm học tập trực tuyến, củng cố lòng tin và giảm thiểu tỷ lệ học viên bỏ học giữa chừng.

## 2.3. Vấn đề đặt ra và Mục tiêu của báo cáo

Mặc dù có nhiều nỗ lực cải tiến, hệ thống truyền thông hiện tại của daotao.ai vẫn bộc lộ những nút thắt cổ chai nghiêm trọng:
*   *Trong nội bộ và đối tác:* Sự lệ thuộc vào nhóm chat Zalo tự phát để phối hợp thông số kỹ thuật học liệu dẫn đến hiện tượng trôi tin nhắn và hiểu sai thông điệp, gây lãng phí nguồn lực biên soạn slide và SCORM.
*   *Trong tương tác với học viên:* Tình trạng học viên (đặc biệt là cán bộ Đề án 06 lớn tuổi) không tìm thấy nút đăng ký học, không tự khắc phục được sự cố đăng nhập thông thường kết hợp với tốc độ phản hồi thủ công chậm trễ của trung tâm đã tạo ra rào cản tâm lý nhận thức nặng nề cho người học.

Nhằm giải quyết triệt để các tồn tại trên, báo cáo này thực hiện phân tích hệ thống truyền thông hiện tại của daotao.ai dưới lăng kính của bốn lý thuyết truyền thông khoa học (Shannon–Weaver, Mô hình Giao dịch, Thuyết Phong phú Truyền thông, Thuyết Tải nhận thức). Từ đó, báo cáo đề xuất và kiểm chứng thực nghiệm hai giải pháp cải tiến thực tiễn: tích hợp **Chatbot AI tự động trợ giúp trên website** và thiết kế **Bộ Template Email trực quan**, hướng tới tối ưu hóa hiệu suất vận hành giáo dục số của Trung tâm EdTech.
