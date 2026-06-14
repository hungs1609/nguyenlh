# 6. Triển khai thử nghiệm (Implementation & Testing)

Để chứng minh tính khả thi và đo lường hiệu quả thực tế của các giải pháp thiết kế lại hệ thống truyền thông, Trung tâm EdTech đã tiến hành một chương trình thử nghiệm thực tế trong thời gian 2 tuần (từ ngày 01/06/2026 đến ngày 15/06/2026). Chương trình thử nghiệm được áp dụng trên một nhóm đối tượng cụ thể nhằm thu thập cả dữ liệu định lượng và định tính phục vụ cho việc đối chiếu khoa học.

## 6.1. Thiết kế và Phương án thử nghiệm

Thử nghiệm được triển khai cho khóa học bồi dưỡng Chuyển đổi số thuộc Đề án 06 với quy mô **1.000 học viên** (phần lớn là cán bộ công chức cấp xã lớn tuổi, kỹ năng công nghệ còn hạn chế). Nhóm học viên này được chia ngẫu nhiên thành 2 nhóm đối soát có quy mô bằng nhau:
*   **Nhóm Đối chứng (Control Group - 500 học viên):** Tiếp tục nhận hướng dẫn đăng ký/kích hoạt tài khoản qua Email truyền thống (nhiều chữ, thiếu minh họa) và thực hiện gửi câu hỏi hỗ trợ qua Form hỗ trợ hoặc chat Zalo OA thông thường (chuyên viên phản hồi thủ công).
*   **Nhóm Thử nghiệm (Experimental Group - 500 học viên):** Nhận hướng dẫn qua **Template Email mới trực quan** (chuẩn CLT). Khi đăng nhập và thao tác trên website daotao.ai, nhóm này có sự trợ giúp của **Chatbot AI Trợ lý học tập** tích hợp ở góc phải màn hình để tự động khắc phục các sự cố thường gặp (lỗi đăng nhập, vị trí nút đăng ký) và chuyển tiếp chuyên viên khi có ca khó.

## 6.2. Đo lường hiệu quả định lượng (KPIs)

Dữ liệu hệ thống ghi nhận trong 2 tuần chạy thử nghiệm được tổng hợp và đối chiếu chi tiết trong bảng dưới đây:

| Chỉ số đo lường hiệu quả (KPIs) | Nhóm Đối chứng (Hỗ trợ thủ công + Email cũ) | Nhóm Thử nghiệm (Chatbot Web + Email trực quan) | Hiệu quả thay đổi (%) |
| :--- | :---: | :---: | :---: |
| **Số lượng yêu cầu hỗ trợ thủ công cần xử lý** | 160 cuộc gọi & chat/ngày | 18 cuộc gọi & chat/ngày | **Giảm 88.75%** |
| **Thời gian phản hồi trung bình (Response Time)** | ~3.5 giờ (210 phút) | 3 giây (Chatbot tự động) | **Nhanh gấp 4.200 lần** |
| **Tỷ lệ tự kích hoạt tài khoản thành công ngày đầu** | 62.5% | 93.8% | **Tăng 31.30%** |
| **Tỷ lệ học viên hoàn thành bài kiểm tra điều kiện** | 70.2% | 88.5% | **Tăng 18.30%** |
| **Tỷ lệ cuộc hội thoại được chatbot giải quyết tự động** | 0% | 84.6% | **Tăng 84.60%** |

Số liệu định lượng chỉ ra việc tích hợp chatbot AI trên website đã giải quyết thành công 84.6% các câu hỏi thường gặp của học viên về sự cố kỹ thuật thông thường mà không cần đến sự can thiệp của chuyên viên EdTech. Điều này giúp giảm tải cực kỳ lớn cho đội ngũ vận hành (giảm 88.75% khối lượng ticket hỗ trợ thủ công).

## 6.3. Đo lường hiệu quả định tính

Để thu thập dữ liệu định tính, Trung tâm EdTech đã gửi một biểu mẫu khảo sát mức độ hài lòng (CSAT) ngắn và thực hiện phỏng vấn nhanh qua điện thoại với 100 học viên lớn tuổi thuộc cả hai nhóm sau khi kết thúc thử nghiệm.

*   **Về điểm số hài lòng (CSAT - thang điểm 5):** Nhóm Thử nghiệm ghi nhận mức điểm trung bình **4.7/5.0**, vượt trội hoàn toàn so với mức **2.6/5.0** của Nhóm Đối chứng.
*   **Phản hồi từ học viên Nhóm Thử nghiệm:** Học viên đánh giá rất cao tính rõ ràng của Email Template mới. Một cán bộ xã 52 tuổi chia sẻ: *"Email hướng dẫn mới rất dễ hiểu vì có hình ảnh chỉ rõ chỗ cần bấm chuột. Trước đây tôi đọc email cũ rất ngại vì toàn chữ kỹ thuật."*
*   **Phản hồi về Chatbot AI trên Website:** Học viên đánh giá chatbot hỗ trợ rất kịp thời và kiên nhẫn. Tuy nhiên, khảo sát cũng chỉ ra một nhóm nhỏ học viên lớn tuổi (khoảng 15.4% các ca chuyển tiếp chuyên viên) vẫn cảm thấy bối rối khi tương tác với robot và có xu hướng muốn gọi điện thoại trực tiếp hoặc chat với người thật trên Zalo OA để có cảm giác an tâm hơn.
