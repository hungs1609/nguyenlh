# Phần 2. CƠ SỞ LÝ THUYẾT VÀ TỔNG QUAN TÀI LIỆU

## 2.1. Tổng quan nghiên cứu

### Xu hướng dịch chuyển trong phân tích học tập
Phân tích học tập đã phát triển nhanh chóng từ đầu những năm 2010 (Siemens, 2013). Tuy nhiên, Romero và Ventura (2020) chỉ ra rằng đa số các công trình nghiên cứu thuộc lĩnh vực này vẫn chủ yếu khai thác các chỉ số tổng hợp tĩnh (như tổng thời lượng truy cập, tần suất click chuột, hoặc tổng số bài tập đã làm) để dự báo kết quả học tập mà bỏ qua tính trình tự và động học của quá trình học tập theo thời gian.

### Ứng dụng khai phá quy trình giáo dục (Educational Process Mining)
Khai phá quy trình (Process Mining) ban đầu được phát triển bởi Wil van der Aalst trong khoa học dịch vụ và quản lý quy trình nghiệp vụ (van der Aalst, Weijters, & Maruster, 2004; van der Aalst, 2016). Khi được ứng dụng vào giáo dục, hướng tiếp cận này tạo thành phân nhánh Educational Process Mining (EPM). 

Bogarín, Cerezo và Romero (2018) đã thực hiện tổng quan hệ thống và chỉ ra rằng Process Mining cho phép chuyển dịch từ phân tích dữ liệu tĩnh sang trực quan hóa toàn bộ dòng chảy hành vi thực tế của người học dưới dạng biểu đồ chuyển tiếp (Directly-Follows Graph) hoặc các mô hình quy trình có cấu trúc (như Petri nets hay Process trees). Điều này giúp phát hiện hành vi lệch chuẩn (conformance checking) so với thiết kế sư phạm ban đầu của khóa học.

### Khoảng trống nghiên cứu
Mặc dù EPM mang lại nhiều giá trị thực tiễn, đa số các công trình hiện nay vẫn đối mặt với hai khoảng trống nghiên cứu lớn. Khoảng trống thứ nhất liên quan đến sự thiên lệch nguồn dữ liệu đơn lẻ (single-source bias). Hầu hết nghiên cứu chỉ phân tích độc lập dữ liệu nhật ký hệ thống hoặc khảo sát tự báo cáo. Việc thiếu đối chiếu song song hai nguồn này dẫn đến nguy cơ diễn giải sai lệch hành vi số, chẳng hạn như hành vi xem lặp lại video bài giảng có thể phản ánh sự chủ động ôn tập của học viên nhưng cũng có thể do cản trở nhận thức khi bài giảng quá phức tạp. Khoảng trống thứ hai nằm ở việc thiếu kiểm soát đường cơ sở khi đánh giá hiệu quả can thiệp. Nhiều nghiên cứu quy kết kết quả tích cực đầu ra cho can thiệp công nghệ mà bỏ qua các yếu tố nền tảng của người học như động lực hay kỹ năng SRL sẵn có ở đường cơ sở (baseline equivalence) chưa được kiểm soát thống kê.

Nghiên cứu này hướng tới lấp đầy khoảng trống bằng quy trình phân tích hai tầng đối chiếu log hành vi với khảo sát tâm lý, đồng thời sử dụng kiểm định ANCOVA để đánh giá hiệu quả can thiệp.

## 2.2. Khung lý thuyết

Nghiên cứu này dựa trên hai trụ cột lý thuyết cốt lõi để thiết kế và biện giải kết quả:

### Lý thuyết Tự điều chỉnh học tập (SRL)
Theo mô hình của Winne và Hadwin (1998), học tập tự điều chỉnh là một tiến trình nhận thức động gồm bốn pha diễn ra liên tục: (1) định nghĩa nhiệm vụ, (2) thiết lập mục tiêu và lập kế hoạch, (3) thực hiện các chiến thuật học tập, và (4) thích ứng siêu nhận thức. Mô hình này cung cấp cơ sở lý luận quan trọng giúp thao tác hóa và giải nghĩa các chỉ số hành vi số từ log LMS (như tính đều đặn, tính tuần tự trong điều hướng, hay tỷ lệ quay lui) thành các biểu hiện quan sát được của các pha nhận thức và điều chỉnh hành vi của sinh viên.

### Mô hình phân cụm vệt hoạt động (Trace Clustering)
Để xử lý sự phân tán của quy trình học tập trực tuyến đại trà, nghiên cứu ứng dụng mô hình Phân cụm vệt hoạt động (Trace Clustering) do Song, Günther và van der Aalst (2009) đề xuất. Kỹ thuật này giúp phân rã tập dữ liệu quy trình lớn và phức tạp thành các cụm lộ trình học tập có cấu trúc hành vi đồng nhất hơn. Từ đó, nghiên cứu có thể xây dựng các hồ sơ quy trình đại diện và thiết lập các chiến lược can thiệp sư phạm cá nhân hóa phù hợp cho từng nhóm học viên.

