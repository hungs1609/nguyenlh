# 09. HỆ THỐNG KPI VÀ PHƯƠNG ÁN ĐÁNH GIÁ KIỂM CHỨNG

## 1. Bảng ma trận KPI kiểm chứng được
Để bảo đảm tính khả thi, minh bạch và có thể kiểm chứng được, hệ thống chỉ số đo lường hiệu quả của Dịch vụ Cố vấn học tập và Hỗ trợ sớm tại Đại học Bách khoa Hà Nội được xây dựng bao gồm cả nhóm chỉ số dẫn dắt đo lường quá trình vận hành và nhóm chỉ số kết quả đo lường giá trị giáo dục thực chất tạo ra.

**Bảng 9.1. Ma trận chỉ số hiệu quả cho Dịch vụ Cố vấn học tập và Hỗ trợ sớm**

| Phân nhóm chỉ số | Mã chỉ số | Tên chỉ số đo lường | Đường cơ sở hiện trạng | Mục tiêu Giai đoạn 1 (12 tháng) | Mục tiêu Giai đoạn 2 (24 tháng) | Mục tiêu Giai đoạn 3 (36 tháng) | Nguồn dữ liệu kiểm chứng | Tần suất đo lường | Đơn vị chủ sở hữu chỉ số |
| :--- | :---: | :--- | :---: | :---: | :---: | :---: | :--- | :---: | :--- |
| **Chỉ số Quá trình** | **KPI-01** | **Thời điểm nhận diện nguy cơ sớm** | Tuần thứ 17 đến 19 sau khi có điểm thi | Tuần thứ 5 đến 6 | Tuần thứ 4 | Tuần thứ 3 đến 4 | Nhật ký hệ thống của động cơ phân tích rủi ro | Hàng tuần | Bộ phận Kỹ thuật Dữ liệu |
| | **KPI-02** | **Thời gian phản hồi của cố vấn học tập** | Không có quy định cụ thể | Dưới 120 giờ | Dưới 72 giờ | Dưới 48 giờ | Nhật ký truy cập cổng cố vấn và phân hệ hồ sơ | Hàng tháng | Trưởng Khoa Viện Đào tạo |
| | **KPI-03** | **Tỷ lệ cảnh báo sai** | Không đo lường được | Dưới 20% | Dưới 15% | Dưới 10% | Báo cáo đối soát giữa cố vấn và điểm giữa kỳ | Từng học kỳ | Hội đồng Đánh giá Sư phạm |
| | **KPI-04** | **Tỷ lệ sinh viên chấp nhận hỗ trợ** | Dưới 20% | Đạt từ 60% | Đạt từ 75% | Đạt từ 85% | Nhật ký các phiên tư vấn trên hệ thống hồ sơ | Hàng học kỳ | Ban Công tác Sinh viên |
| **Chỉ số Kết quả** | **KPI-05** | **Tỷ lệ sinh viên thoát diện cảnh báo học vụ** | Ước tính khoảng 30% | Đạt từ 45% | Đạt từ 60% | Đạt từ 70% | Cơ sở dữ liệu điểm chính thức trên SIS | Hàng học kỳ | Ban Đào tạo |
| | **KPI-06** | **Mức độ cải thiện điểm trung bình học kỳ** | Không có sự cải thiện rõ rệt | Tăng trung bình 0.2 điểm | Tăng trung bình 0.35 điểm | Tăng trung bình 0.5 điểm | Bảng điểm đối chứng trước và sau can thiệp | Hàng học kỳ | Ban Đào tạo |
| | **KPI-07** | **Tỷ lệ sinh viên bị buộc thôi học hàng năm** | Khoảng 4.5% đến 5.5% | Giảm 5% so với hiện trạng | Giảm 15% so với hiện trạng | Giảm 25% so với hiện trạng | Quyết định xử lý học vụ chính thức của Đại học | Hàng năm | Ban Giám đốc Đại học |
| | **KPI-08** | **Mức độ hài lòng của sinh viên** | Chưa từng khảo sát | Đạt từ 70% | Đạt từ 80% | Đạt từ 90% | Khảo sát ẩn danh của Trung tâm Đảm bảo Chất lượng | Hàng năm | Trung tâm Đảm bảo Chất lượng |

## 2. Phương pháp Kiểm định và Đo lường Hiệu quả Can thiệp
Để khẳng định sự cải thiện kết quả học tập của sinh viên là do tác động thực tế của dịch vụ hỗ trợ sớm chứ không phải do các yếu tố ngẫu nhiên bên ngoài, nhà trường áp dụng thiết kế nghiên cứu bán thực nghiệm kết hợp kỹ thuật ghép cặp điểm xu hướng Propensity Score Matching.

```mermaid
graph TD
    A[Tổng số Sinh viên có Nguy cơ Học tập<br>Phát hiện ở Tuần 4] --> B[Ghép cặp tương đương Propensity Score Matching]
    B --> C[NHÓM CAN THIỆP<br>Nhận hỗ trợ từ Cố vấn học tập và Phụ đạo]
    B --> D[NHÓM ĐỐI CHỨNG<br>Chỉ nhận thông báo nhắc nhở thông thường]
    
    C --> E[Đánh giá Kết quả Cuối kỳ<br>Điểm GPA và Tỷ lệ Cảnh báo Học vụ]
    D --> E
    
    E --> F{Phân tích Đối sánh Tác động Ròng<br>Net Treatment Effect}
    F --> G[Kết luận Giá trị Giáo dục Thực chất]
```

Phương pháp được tiến hành bằng việc chia đối tượng nghiên cứu thành hai nhóm có đặc điểm tương đồng. Nhóm can thiệp gồm các sinh viên thuộc diện nguy cơ nhận được đầy đủ gói dịch vụ gồm tư vấn trực tiếp với cố vấn học tập, tham gia lớp phụ đạo của trợ giảng và điều chỉnh kế hoạch học tập cá nhân. Nhóm đối chứng gồm các sinh viên có cùng mức điểm tuyển sinh đầu vào, cùng ngành học và có mức độ sụt giảm tương tác tương đương ở tuần thứ tư nhưng học tập tại các đơn vị chưa triển khai thí điểm dịch vụ. 

Bằng việc phân tích đối sánh mức độ cải thiện điểm trung bình học kỳ và tỷ lệ trượt môn giữa hai nhóm sau khi kết thúc học kỳ, nhà trường có thể bóc tách tác động ròng của dịch vụ, khẳng định giá trị gia tăng thực chất mà giải pháp mang lại cho chất lượng đào tạo.

## 3. Chu trình Cải tiến Liên tục
Dữ liệu chỉ số hiệu quả không chỉ dùng để lập báo cáo thành tích mà đóng vai trò là nguồn thông tin phản hồi sống động để vận hành chu trình cải tiến chất lượng liên tục PDCA cho toàn bộ hệ sinh thái dịch vụ.

```mermaid
flowchart TD
    subgraph PLAN [1. KẾ HOẠCH]
        P1[Xác định mục tiêu chỉ số học kỳ]
        P2[Cập nhật trọng số thuật toán phân tích]
        P3[Phân công chỉ tiêu cố vấn học tập phụ trách]
    end

    subgraph DO [2. THỰC HIỆN]
        D1[Thu thập nhật ký tương tác thời gian thực]
        D2[Kích hoạt cảnh báo tuần 3 đến 5]
        D3[Cố vấn học tập tổ chức các phiên tư vấn bối cảnh]
    end

    subgraph CHECK [3. KIỂM TRA]
        C1[Rà soát tỷ lệ cảnh báo sai định kỳ]
        C2[Đo lường thời gian phản hồi của cố vấn]
        C3[Khảo sát trải nghiệm sinh viên ẩn danh]
    end

    subgraph ACT [4. ĐIỀU CHỈNH]
        A1[Tự động tinh chỉnh ngưỡng cảnh báo thuật toán]
        A2[Tái phân bổ nguồn lực trợ giảng cho môn khó]
        A3[Khen thưởng cố vấn có đóng góp xuất sắc]
    end

    PLAN --> DO --> CHECK --> ACT --> PLAN
```

Ở khía cạnh công nghệ, nếu tỷ lệ cảnh báo sai vượt quá ngưỡng 15%, hội đồng chuyên môn sẽ tiến hành rà soát lại các trọng số cấu thành chỉ số tham gia học tập; chẳng hạn như giảm bớt tỷ trọng của việc xem bài giảng trực tuyến nếu học phần đó chủ yếu giảng dạy trên lớp. 

Ở khía cạnh sư phạm, nếu dữ liệu ghi nhận trên 40% sinh viên trong một lớp học phần đồng loạt rơi vào diện nguy cơ cao, hệ thống sẽ tự động gửi tín hiệu đến trưởng bộ môn để rà soát lại phương pháp giảng dạy hoặc độ khó của bài kiểm tra quá trình, bảo đảm việc can thiệp được thực hiện hai chiều giữa người học và người dạy.
