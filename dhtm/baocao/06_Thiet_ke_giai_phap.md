# 06. THIẾT KẾ GIẢI PHÁP KIẾN TRÚC VÀ DỊCH VỤ

## 1. Sơ đồ kiến trúc tổng thể sáu lớp
Vận dụng khung kiến trúc hệ sinh thái Đại học thông minh được tổng hợp từ Uskov và cộng sự (2018), Tổ chức Hợp tác và Phát triển Kinh tế (OECD, 2023) cùng nội dung bài giảng chuyên đề, giải pháp Dịch vụ Cố vấn học tập và Hỗ trợ sớm thông minh tại Đại học Bách khoa Hà Nội được thiết kế theo cấu trúc sáu lớp đồng bộ. Kiến trúc này bảo đảm tính truy vết giá trị xuyên suốt: mọi quyết định công nghệ và hạ tầng ở các lớp dưới đều hướng tới việc phục vụ quy trình, dịch vụ và giá trị giáo dục ở các lớp phía trên.

```mermaid
flowchart TD
    subgraph L1 [LỚP 1: GIÁ TRỊ VÀ CHỦ THỂ]
        V1["Sinh viên: Được hỗ trợ kịp thời, bảo mật, không bị dán nhãn"]
        V2["Cố vấn học tập: Có thông tin bối cảnh, giảm thủ tục hành chính"]
        V3["Nhà trường: Giảm tỷ lệ thôi học, minh bạch trách nhiệm giải trình"]
    end

    subgraph L2 [LỚP 2: DỊCH VỤ]
        S1["Dịch vụ Nhận diện Nguy cơ Sớm từ tuần thứ 3 đến tuần thứ 5"]
        S2["Dịch vụ Điều phối và Can thiệp Cá nhân hóa"]
        S3["Dịch vụ Đánh giá và Khép kín Vòng lặp"]
    end

    subgraph L3 [LỚP 3: QUY TRÌNH]
        P1["Kích hoạt Tín hiệu Dữ liệu"] --> P2["Cố vấn Đánh giá Bối cảnh"]
        P2 --> P3["Thiết lập Kế hoạch Can thiệp"]
        P3 --> P4["Theo dõi Tiến độ Phục hồi"]
        P4 --> P5["Đánh giá và Tinh chỉnh Thuật toán"]
    end

    subgraph L4 [LỚP 4: DỮ LIỆU]
        D1["Dữ liệu Học vụ Lịch sử từ SIS"]
        D2["Dữ liệu Tiến trình Thực tế từ LMS"]
        D3["Dữ liệu Bối cảnh và Nhật ký Can thiệp"]
        D4["Nền tảng Dữ liệu Tập trung Data Lakehouse"]
    end

    subgraph L5 [LỚP 5: ỨNG DỤNG VÀ NĂNG LỰC SỐ]
        A1["Động cơ Phân tích Rủi ro Sớm"]
        A2["Cổng Cố vấn Bối cảnh hóa"]
        A3["Trung tâm Thông báo Đa kênh"]
        A4["Phân hệ Quản lý Hồ sơ Can thiệp"]
    end

    subgraph L6 [LỚP 6: HẠ TẦNG VÀ AN TOÀN]
        I1["Hạ tầng Định danh Tập trung SSO"]
        I2["Phân quyền Truy cập Dựa trên Vai trò RBAC"]
        I3["Mã hóa Dữ liệu và Nhật ký Giám sát"]
        I4["Hạ tầng Đám mây Lai"]
    end

    L1 === L2
    L2 === L3
    L3 === L4
    L4 === L5
    L5 === L6
```

### Phân tích chi tiết sáu lớp kiến trúc
Xét ở Lớp 1 là Giá trị và Chủ thể, kiến trúc định vị rõ người thụ hưởng và các giá trị cốt lõi được cam kết. Mọi giải pháp công nghệ bên dưới đều quy tụ về mục tiêu giúp sinh viên được nhận diện khó khăn kịp thời để phục hồi học kỳ, hỗ trợ cố vấn học tập có đủ bức tranh bối cảnh sư phạm, và nâng cao hiệu quả đào tạo chung của nhà trường.

Về phương diện Lớp 2 là Dịch vụ, hệ thống chuyển dịch từ việc cung cấp các phần mềm rời rạc sang ba gói dịch vụ liên thông gồm Dịch vụ nhận diện nguy cơ sớm ở giai đoạn giữa kỳ, Dịch vụ điều phối can thiệp đa bên và Dịch vụ theo dõi phục hồi kết hợp đánh giá sau can thiệp.

Đối với Lớp 3 là Quy trình, thiết kế xác lập chu trình năm bước với trách nhiệm bàn giao rõ ràng. Thời hạn cam kết xử lý dịch vụ được quy định nghiêm ngặt: kể từ khi xuất hiện tín hiệu rủi ro đến khi cố vấn học tập tiếp cận người học không được vượt quá 72 giờ.

Về mặt Lớp 4 là Dữ liệu, kiến trúc phá vỡ các ốc đảo thông tin bằng việc tích hợp hai nguồn dữ liệu thẩm quyền gồm dữ liệu học vụ lịch sử từ hệ thống SIS và dữ liệu tiến trình học tập thời gian thực từ hệ thống LMS, lưu trữ tập trung tại nền tảng dữ liệu chung của trường.

Ở Lớp 5 là Ứng dụng và Năng lực số, hệ thống tích hợp động cơ phân tích rủi ro học tập ứng dụng mô hình học máy có khả năng giải thích, Cổng cố vấn học tập trực quan và phân hệ quản lý hồ sơ can thiệp giúp lưu trữ lịch sử tư vấn an toàn.

Cuối cùng, Lớp 6 là Hạ tầng và An toàn bảo đảm tính sẵn sàng cao và tuân thủ pháp lý thông qua hệ thống định danh tập trung của Đại học Bách khoa Hà Nội, cơ chế phân quyền dựa trên vai trò nghiêm ngặt, mã hóa cơ sở dữ liệu và lưu vết toàn bộ nhật ký truy cập theo quy định pháp luật.

## 2. Service Blueprint và Luồng dữ liệu can thiệp
Bản đồ dịch vụ Service Blueprint trực quan hóa toàn bộ hành trình trải nghiệm, phân định ranh giới giữa tương tác trực tiếp của người dùng, hoạt động nghiệp vụ hậu trường và các luồng công nghệ hỗ trợ bên dưới.

```mermaid
sequenceDiagram
    autonumber
    actor SinhVien as Sinh viên
    participant LMS_SIS as LMS và SIS
    participant EWE as Động cơ Phân tích Rủi ro
    actor CoVan as Cố vấn Học tập
    participant Portal as Cổng Cố vấn và Hồ sơ
    actor GiangVien as Giảng viên và Đơn vị Hỗ trợ

    Note over SinhVien,LMS_SIS: GIAI ĐOẠN 1: CẢM NHẬN TÍN HIỆU (TUẦN 1 ĐẾN 4)
    SinhVien->>LMS_SIS: Tương tác học tập (vắng 2 buổi, không nộp bài tập tuần 3)
    LMS_SIS->>EWE: Đồng bộ dữ liệu nhật ký và điểm quá trình qua API

    Note over EWE,CoVan: GIAI ĐOẠN 2: SUY DIỄN VÀ ĐÁNH GIÁ BỐI CẢNH (TUẦN 4 ĐẾN 5)
    EWE->>EWE: Tính toán chỉ số nguy cơ học tập mức cao
    EWE->>Portal: Chuyển thông tin bối cảnh vào danh sách chờ của Cố vấn
    Portal->>CoVan: Thông báo bảo mật về sinh viên cần xem xét bối cảnh
    CoVan->>Portal: Kiểm tra hồ sơ đa chiều gồm điểm tích lũy và ghi chú liên quan

    Note over CoVan,SinhVien: GIAI ĐOẠN 3: CAN THIỆP CÓ TRÁCH NHIỆM (TRONG VÒNG 72 GIỜ)
    CoVan->>SinhVien: Gửi lời mời trao đổi trực tiếp bằng ngôn ngữ khích lệ
    SinhVien->>CoVan: Tham gia buổi tư vấn và chia sẻ khó khăn thực tế
    CoVan->>Portal: Lập Kế hoạch Phục hồi Học tập cá nhân hóa
    CoVan->>GiangVien: Kết nối sinh viên với lớp phụ đạo của Trợ giảng môn học

    Note over SinhVien,EWE: GIAI ĐOẠN 4: ĐÁNH GIÁ VÀ KHÉP KÍN VÒNG LẶP (SAU 14 NGÀY)
    SinhVien->>LMS_SIS: Tăng cường tương tác và hoàn thành bài tập bổ sung
    LMS_SIS->>EWE: Ghi nhận sự phục hồi của các chỉ số học tập
    EWE->>Portal: Cập nhật trạng thái nguy cơ đã được giải tỏa
    CoVan->>Portal: Đóng hồ sơ can thiệp và gửi phản hồi tinh chỉnh thuật toán
```

**Bảng 6.1. Ma trận chi tiết Service Blueprint dịch vụ hỗ trợ sớm**

| Tầng kiến trúc dịch vụ | Bước 1: Phát hiện tín hiệu | Bước 2: Đánh giá bối cảnh | Bước 3: Tiếp cận và Tư vấn | Bước 4: Thực hiện can thiệp | Bước 5: Đánh giá phục hồi |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Bằng chứng vật lý và số** | Giao diện nộp bài tập; Bảng điểm danh lớp học. | Bảng điều khiển bối cảnh trên Cổng cố vấn học tập. | Thông điệp mời gặp gỡ; Phòng tư vấn trực tiếp hoặc trực tuyến. | Bản cam kết kế hoạch học tập cá nhân; Lịch phụ đạo. | Biểu đồ phục hồi học tập; Kết quả bài thi giữa kỳ. |
| **Hành động của Sinh viên** | Vắng học không phép hoặc chậm nộp bài tập quá trình. | Chưa nhận thông báo rủi ro để tránh áp lực tâm lý. | Nhận thông điệp đồng hành; Xác nhận lịch hẹn với cố vấn. | Tham gia buổi tư vấn; Chia sẻ khó khăn và tham gia lớp phụ đạo. | Hoàn thành bài tập bổ sung; Cải thiện kết quả học tập. |
| **Tương tác trực tiếp** | Giảng viên ghi nhận vắng mặt trên hệ thống. | Không có tương tác trực tiếp. | Cố vấn học tập trực tiếp lắng nghe và thấu cảm khó khăn. | Giảng viên bộ môn hoặc trợ giảng hỗ trợ bù đắp kiến thức rỗng. | Cố vấn học tập gửi thông điệp biểu dương sự tiến bộ. |
| **Hành động hậu trường** | Hệ thống tự động tổng hợp dữ liệu vi mô vào kho dữ liệu. | Cố vấn học tập tra cứu lịch sử học tập và chuẩn bị phương án. | Cố vấn học tập lựa chọn gói can thiệp học thuật hoặc tâm lý. | Ban Đào tạo phân bổ trợ giảng; Ban Công tác Sinh viên hỗ trợ thủ tục. | Cố vấn học tập xác nhận đóng hồ sơ can thiệp trên hệ thống. |
| **Hệ thống hỗ trợ và Luồng dữ liệu** | Đường ống dữ liệu tự động đồng bộ dữ liệu lúc 00:00 hàng ngày. | Động cơ phân tích tính toán điểm số nguy cơ học tập. | Phân hệ thông báo bảo mật gửi thư điện tử mã hóa. | Phân hệ quản lý hồ sơ ghi nhận kế hoạch hành động. | Thuật toán so sánh chỉ số trước và sau can thiệp để tự học. |

## 3. Quy trình Can thiệp Sư phạm và Ma trận Phân tầng Nguy cơ
Để bảo đảm tính công bằng và cá nhân hóa, hệ thống phân loại rủi ro thành ba cấp độ với các kịch bản can thiệp tương ứng.

```mermaid
graph TD
    A[Dữ liệu học tập tuần 1 đến 4] --> B{Động cơ phân tích đánh giá nguy cơ}
    B -- "Điểm số dưới 0.4 (Nguy cơ Thấp)" --> C[GÓI 1: TỰ THÍCH ỨNG<br>Gửi tài liệu bổ trợ và hướng dẫn tự học qua LMS]
    B -- "Điểm số từ 0.4 đến 0.7 (Nguy cơ Vừa)" --> D[GÓI 2: ĐỒNG ĐẲNG<br>Kết nối Trợ giảng và nhóm học tập sinh viên]
    B -- "Điểm số trên 0.7 (Nguy cơ Cao)" --> E[GÓI 3: CAN THIỆP CHUYÊN SÂU<br>Cố vấn trực tiếp tư vấn và phối hợp đa bên]
```

Đối với nhóm sinh viên có mức độ nguy cơ thấp tương ứng với điểm rủi ro dưới 0.4 do chỉ quên nộp một bài tập hoặc vắng một buổi học, hệ thống tự động gửi thông báo nhắc nhở nhẹ nhàng trên hệ thống quản trị học tập kèm tài liệu hướng dẫn tự học mà không làm phiền đến cố vấn học tập. 

Đối với nhóm sinh viên có mức độ nguy cơ trung bình tương ứng với điểm rủi ro từ 0.4 đến 0.7 khi có dấu hiệu vắng hai buổi học và điểm kiểm tra nhanh dưới trung bình, hệ thống đề xuất sinh viên tham gia nhóm hỗ trợ học tập đồng đẳng do các trợ giảng sinh viên khóa trên phụ trách. 

Đối với nhóm sinh viên có mức độ nguy cơ cao tương ứng với điểm rủi ro từ 0.7 trở lên do vắng trên 30% thời lượng hoặc không tương tác liên tục trong hai tuần, hệ thống lập tức kích hoạt cảnh báo gửi đến cố vấn học tập. Cố vấn học tập bắt buộc phải tổ chức phiên tư vấn trực tiếp trong vòng 72 giờ và phối hợp cùng ban đào tạo để thiết lập kế hoạch can thiệp cá nhân hóa.

Để trực quan hóa cơ chế vận hành của động cơ phân tích rủi ro trong môi trường thực tế của Đại học Bách khoa Hà Nội, Bảng 6.2 mô phỏng hồ sơ bối cảnh và kịch bản kích hoạt can thiệp đối với ba trường hợp sinh viên điển hình.

**Bảng 6.2. Ma trận hồ sơ phân tích rủi ro học tập của ba sinh viên Bách khoa mẫu (Case Student Profiles)**

| Thuộc tính phân tích | Trường hợp 1: Sinh viên Nguyễn Văn A | Trường hợp 2: Sinh viên Trần Thị B | Trường hợp 3: Sinh viên Lê Văn C |
| :--- | :--- | :--- | :--- |
| **Thông tin học vụ (SIS)** | K68 Trường Cơ khí (SME), CPA kỳ trước: Chưa có | K68 Trường CNTT&TT (SoICT), Điểm chuẩn đầu vào: 27.5 | K68 Trường Điện - Điện tử (SEEE), CPA tích lũy: 3.12 |
| **Tần suất truy cập LMS Moodle** | **1 lần/tuần** (sụt giảm 80% từ tuần 2) | **3 lần/tuần** (đều đặn nhưng thời lượng ngắn) | **6 lần/tuần** (tương tác liên tục) |
| **Thời gian học liệu số** | **12 phút/tuần** trên hệ thống | **45 phút/tuần** | **85 phút/tuần** |
| **Tiến độ nộp bài tập tuần** | Nợ bài tập tuần 2 và tuần 3 học phần **Giải tích I** | Nộp trễ 1 bài tập **Tin học đại cương**, nợ 1 bài quiz | Hoàn thành 100% bài tập đúng hạn |
| **Chuyên cần lớp học phần** | Vắng **2 buổi học** không phép học phần Giải tích I | Đi học đầy đủ | Đi học đầy đủ |
| **Điểm kiểm tra nhanh** | Điểm quiz tuần 3: **2.5/10** (Nguy cơ ĐQT < 3.0) | Điểm quiz tuần 3: **5.0/10** | Điểm quiz tuần 3: **8.0/10** |
| **Điểm số rủi ro tính toán ($R$)** | **$R = 0.78$ (Nguy cơ Cao - Cấp độ 3)** | **$R = 0.46$ (Nguy cơ Vừa - Cấp độ 2)** | **$R = 0.12$ (Nguy cơ Thấp - Cấp độ 1)** |
| **Gói dịch vụ kích hoạt** | **GÓI 3: CAN THIỆP CHUYÊN SÂU** | **GÓI 2: HỖ TRỢ ĐỒNG ĐẲNG** | **GÓI 1: TỰ THÍCH ỨNG** |
| **Hành động can thiệp cụ thể** | Hệ thống chuyển hồ sơ bảo mật sang Cổng CVHT. Cố vấn gửi lời mời tư vấn riêng trong 72h; phát hiện sinh viên làm thêm ban đêm và hổng kiến thức vi phân; kết nối Trợ giảng phụ đạo và Ban CTSV hỗ trợ. | Hệ thống tự động gửi thông báo gợi ý sinh viên đăng ký nhóm trợ giảng đồng đẳng sinh viên khóa trên (K66) để hướng dẫn sửa bài tập lập trình C++. | Hệ thống tự động gửi thông điệp biểu dương tiến độ học tập kèm tài liệu tham khảo nâng cao qua ứng dụng eHUST. |

*(Ghi chú: Dữ liệu mô phỏng tham số hóa của nhóm nghiên cứu nhằm minh họa trực quan quy tắc suy diễn của động cơ phân tích rủi ro).*

Dựa trên thuật toán phân tầng rủi ro, khối lượng công việc hỗ trợ sinh viên tại Đại học Bách khoa Hà Nội được phân bổ tối ưu theo nguyên tắc hình phễu, bảo đảm tính khả thi và không gây quá tải cho đội ngũ giảng viên kiêm nhiệm cố vấn học tập.

**Bảng 6.3. Dự phóng phân bổ tải công việc can thiệp cho một khóa 8.000 sinh viên tại Đại học Bách khoa Hà Nội**

| Phân tầng nguy cơ | Tỷ lệ sinh viên ước tính | Số lượng sinh viên ước tính (Khóa 8.000 SV) | Kênh thực hiện can thiệp chính | Khối lượng phụ trách trung bình trên 1 CVHT | Tác động tải công việc lên đội ngũ CVHT |
| :--- | :---: | :---: | :--- | :---: | :--- |
| **Cấp 1: Nguy cơ thấp** | **~15%** | **~1.200 sinh viên** | Tự động hóa 100% qua thông báo LMS Moodle và app eHUST | 12 – 15 SV/CVHT | **0 giờ** (Hệ thống tự động điều phối học liệu bổ trợ). |
| **Cấp 2: Nguy cơ vừa** | **~8%** | **~640 sinh viên** | Mạng lưới Trợ giảng sinh viên (TA) và Nhóm học tập đồng đẳng | 6 – 8 SV/CVHT | **~1 giờ/kỳ** (CVHT chỉ duyệt danh sách ghép nhóm). |
| **Cấp 3: Nguy cơ cao** | **~4%** | **~320 sinh viên** | **Cố vấn học tập trực tiếp tư vấn chuyên sâu 1-1** | **3 – 5 SV/CVHT** | **~6–10 giờ/kỳ** (Mỗi ca tư vấn 2 phiên $\times$ 45–60 phút). |

*(Ghi chú: Phân bổ tham số hóa dựa trên quy mô tuyển sinh khóa mới của ĐHBK Hà Nội và tỷ lệ trượt môn thực tế của khối kỹ thuật).*

Bảng 6.3 mang lại một luận cứ then chốt bảo vệ tính khả thi của giải pháp: Mặc dù mỗi cố vấn học tập quản lý danh nghĩa từ 80 đến 120 sinh viên, nhưng nhờ cơ chế sàng lọc thông minh ba cấp độ, người thầy chỉ phải tập trung nguồn lực tư vấn chuyên sâu cho **3 đến 5 sinh viên thực sự rơi vào khủng hoảng nặng nhất**. Điều này giải quyết triệt để nỗi lo ngại về tình trạng quá tải và "trơ lì cảnh báo" của giảng viên.
