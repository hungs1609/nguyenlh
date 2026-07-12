## THẺ 2 

BÁO CÁO NGHIÊN CỨU 

Đánh giá hiệu quả ứng dụng khai phá quy trình (Process Mining) trong phân tích học tập nhằm tối ưu hóa lộ trình cá nhân hóa của sinh viên đại học 

* 
**Nghiên cứu trường hợp:** Khóa học SoDiTEC, mã lớp TDC01, tháng 5 năm 2024 


* 
**Biến độc lập:** Ứng dụng kỹ thuật Process Mining trong Learning Analytics 


* 
**Biến phụ thuộc:** Sự cá nhân hóa lộ trình học tập của sinh viên, thể hiện qua hiệu quả học tập và độ chính xác của lộ trình đề xuất 


* 
**Đối tượng nghiên cứu:** Lộ trình học tập và hành vi số của sinh viên bậc đại học 



---

### GIAI ĐOẠN 1: CHUẨN BỊ (PRE-DATA COLLECTION) 

**Mục tiêu:** Xác định vấn đề, xây dựng giả thuyết và thiết kế nghiên cứu trước khi thu thập dữ liệu.

Bước 1. Xác định vấn đề và mục đích nghiên cứu 

* 
**Vấn đề giáo dục thực tế:** Các phương pháp phân tích học tập (Learning Analytics) truyền thống chỉ dựa trên thống kê tĩnh (điểm số, lượt click), bỏ qua tính trình tự động của hành vi. Lộ trình học "cào bằng" dẫn đến tỷ lệ sinh viên nản chí và bỏ học cao.


* 
**Mục đích nghiên cứu:** Chuyển bài toán trên thành mục đích thực nghiệm: Ứng dụng giải pháp cá nhân hóa lộ trình dựa trên Process Mining kết hợp dữ liệu chủ quan để tối ưu hóa kết quả học tập và tăng mức độ hài lòng của sinh viên.



Bước 2. Thiết lập giả thuyết (Hypothesis) 

* 
**Giả thuyết nghiên cứu ($H_1$):** Sinh viên được học tập và can thiệp bằng lộ trình cá nhân hóa (được tối ưu hóa từ dữ liệu Process Mining và khảo sát chủ quan) sẽ có hiệu quả học tập và mức độ hài lòng cao hơn một cách có ý nghĩa thống kê so với khi học theo lộ trình cố định ban đầu.



Bước 3. Lựa chọn biến nghiên cứu 

* 
**Biến độc lập (Independent Variable - IV):** Phương thức tổ chức lộ trình học tập (Giai đoạn học lộ trình cố định không can thiệp vs. Giai đoạn học lộ trình cá nhân hóa có can thiệp).


* 
**Biến phụ thuộc (Dependent Variable - DV):** 


* 
*Hiệu quả học tập:* Điểm quiz trung bình, tỷ lệ hoàn thành khóa học.


* 
*Mức độ cá nhân hóa/Phù hợp:* Mức độ bực bội, tải nhận thức và mức độ hài lòng tổng thể của sinh viên.




* 
**Biến kiểm soát (Control Variable - CV):** Nội dung chuyên môn khóa học SoDiTEC, cấu trúc nền tảng edX, thời gian diễn ra (tháng 5/2024).



Bước 4. Thiết kế kế hoạch nghiên cứu (Study Plan) 

* 
**Thiết kế nghiên cứu:** Áp dụng thiết kế bán thực nghiệm (Quasi-experimental design) dạng một nhóm đo lường Trước - Sau (One-Group Pretest-Posttest Design) có phân cụm đối chứng nội bộ.


* 
**Nguồn lực & Thời gian:** Sử dụng dữ liệu nhật ký sự kiện hệ thống (21 MB) và dữ liệu khảo sát 38 biến số của khóa học diễn ra trong vòng 1 tháng.


* 
**Kiểm soát yếu tố ngoại lai:** Lọc sạch dữ liệu nhiễu, chỉ chọn những sinh viên hoàn thành đủ cả 2 nguồn dữ liệu để tránh hiện tượng mất dấu mẫu (attrition bias).



---

### GIAI ĐOẠN 2: TRIỂN KHAI (IMPLEMENTATION) 

**Mục tiêu:** Tổ chức thực nghiệm, tiến hành can thiệp và thu thập dữ liệu.

Bước 5. Lấy mẫu và phân bổ (Randomization/Sampling) 

* 
**Tổng thể (Population):** 1.531 học viên đăng ký khóa học SoDiTEC mã lớp TDC01.


* 
**Mẫu thực nghiệm (Sample):** Áp dụng phương pháp chọn mẫu có chủ đích (Purposive Sampling) để chọn ra 200 học viên đáp ứng tiêu chuẩn "dữ liệu đầy đủ" (vừa có log hành vi liên tục, vừa hoàn thành đầy đủ các đợt khảo sát).


* 
**Phân cụm nội bộ:** Phân mẫu 200 học viên thành các nhóm so sánh tự nhiên (Nhóm học lực Cao/Trung bình/Thấp và Nhóm lộ trình Có kế hoạch/Khám phá/Nguy cơ) để làm đối chứng chéo.



Bước 6. Tiền kiểm (Pretest) 

* 
**Nội dung đo lường ban đầu:** Trước khi khóa học đi vào các chương chuyên sâu, tiến hành khảo sát ban đầu về động lực, định hướng mục tiêu, niềm tin vào năng lực bản thân và khả năng tự điều chỉnh học tập (SRL).


* 
**Mục đích:** Xác định mức độ nền tảng ban đầu của học viên, đảm bảo kiểm soát được sự khác biệt về tâm lý học tập trước khi can thiệp.



Bước 7. Tiến hành can thiệp (Intervention) 

* 
**Nhóm thực nghiệm/Giai đoạn can thiệp:** Thực hiện quy trình xử lý dữ liệu và tối ưu hóa lộ trình 5 bước:


1. Trích xuất log dữ liệu thô từ hệ thống edX.


2. Trừu tượng hóa thành 8 nhãn hoạt động cốt lõi (Xem video, làm quiz, điều hướng...).


3. Khai phá quy trình (Process Mining) để dựng biểu đồ chuyển tiếp trực tiếp và phát hiện điểm nghẽn (Xác định Chương 6 là điểm nghẽn lớn nhất khi tỷ lệ hoạt động giảm mạnh từ 97,5% xuống 89,5%).


4. Trích đặc trưng hành vi (tính đều đặn, tỷ lệ quay lui, tua lùi...) để gắn cờ cảnh báo sớm nhóm nguy cơ bỏ học (chiếm 40% mẫu).


5. 
*Can thiệp cá nhân hóa:* Gửi nhắc học tự động theo khung giờ cao điểm riêng (6h, 13h, 15h), điều chỉnh giảm tải nội dung tại Chương 6, và cung cấp hỗ trợ khác nhau cho nhóm tua lùi video để ôn bài vs. nhóm tua lùi do bế tắc.




* 
**Điều kiện đối chứng:** Giữ nguyên điều kiện mặc định của hệ thống edX (không can thiệp) đối với các nhóm học viên học tuyến tính thông thường để đối chiếu chéo kết quả.



Bước 8. Hậu kiểm (Post-test) 

* 
**Đo lường sau can thiệp:** Tiến hành thu thập dữ liệu kết quả học tập thực tế (Báo cáo điểm số với 1.558 bản ghi bài quiz) và Khảo sát sau khóa học (đo lường mức độ bực bội, tải nhận thức, mức độ hài lòng tổng thể đạt 2,78/5 và ý định học tiếp).



---

### GIAI ĐOẠN 3: PHÂN TÍCH VÀ BÁO CÁO (POST-DATA COLLECTION) 

**Mục tiêu:** Xử lý dữ liệu, kiểm định giả thuyết và công bố kết quả nghiên cứu.

Bước 9. Phân tích dữ liệu 

* 
**Phép kiểm thống kê áp dụng:** Sử dụng Thống kê mô tả (tính tần suất, tỷ lệ), Phân tích tương quan Pearson ($r$) để tìm mối quan hệ giữa hành vi log và kết quả, so sánh điểm trung bình giữa các phân cụm nhóm (T-test/ANOVA).


* 
**Kết quả định lượng cụ thể:** 


* Chỉ số đều đặn tương quan thuận mạnh với mức hoàn thành ($r = 0,459$).


* Khả năng tự điều chỉnh học tập (SRL) từ dữ liệu chủ quan có tương quan rất mạnh với điểm số cuối cùng ($r = 0,498$).


* 
*Phân cụm nhóm lộ trình chứng minh:* Nhóm có kế hoạch (được tối ưu lộ trình) đạt điểm trung bình cao vượt trội (66,51) và tỷ lệ bỏ học thấp nhất (22,4%) so với Nhóm nguy cơ (Điểm 49,45; bỏ học 46,8%).


* 
*Xác định "điểm mù" của log:* Cùng một hành vi tua lùi hay xem lại video, chỉ khi đối chiếu chéo với dữ liệu khảo sát chủ quan mới phân tách chính xác hiệu quả học tập (Nhóm xem lại có mục tiêu đạt 54,6 điểm vs. Nhóm xem lại không mục tiêu chỉ đạt 46,0 điểm).





Bước 10. Diễn giải và công bố kết quả 

* 
**Kết luận về giả thuyết:** Giả thuyết $H_1$ được chấp nhận. Việc phối hợp Khai phá quy trình (dữ liệu khách quan) và Khảo sát nhận thức (dữ liệu chủ quan) giúp nâng cao rõ rệt độ chính xác của việc đánh giá và cá nhân hóa lộ trình, từ đó cải thiện kết quả học tập và giảm tỷ lệ bỏ học của sinh viên.


* 
**Hàm ý và điều chỉnh lý thuyết:** Log hành vi là điều kiện cần nhưng chưa đủ, bắt buộc phải tích hợp dữ liệu cảm xúc/động lực để xóa bỏ "điểm mù" trong Learning Analytics.


* 
**Hạn chế và hướng đi tiếp theo:** Do nghiên cứu này so sánh dựa trên các nhóm hình thành tự nhiên trong mẫu $N=200$, hướng tiếp theo cần triển khai thực nghiệm ngẫu nhiên có đối chứng (RCT) chia đôi lớp học (A/B Testing) để khẳng định triệt để hơn mối quan hệ nhân quả.



---

### TÀI LIỆU THAM KHẢO 

* Bogarín, A., Cerezo, R., & Romero, C. (2018). A survey on educational process mining. *Wiley Interdisciplinary Reviews: Data Mining and Knowledge Discovery*, 8(1), Article e1230. [https://doi.org/10.1002/widm.1230](https://doi.org/10.1002/widm.1230) 


* Cerezo, R., Bogarín, A., Esteban, M., & Romero, C. (2020). Process mining for self-regulated learning assessment in e-learning. *Journal of Computing in Higher Education*, 32(1), 74 đến 88. [https://doi.org/10.1007/s12528-019-09225-y](https://doi.org/10.1007/s12528-019-09225-y) (bản mở truy cập: [https://arxiv.org/abs/2403.12068](https://arxiv.org/abs/2403.12068)) 


* Romero, C., & Ventura, S. (2020). Educational data mining and learning analytics: An updated survey. *Wiley Interdisciplinary Reviews: Data Mining and Knowledge Discovery*, 10(3), Article e1355. [https://doi.org/10.1002/widm.1355](https://doi.org/10.1002/widm.1355) 


* Siemens, G. (2013). Learning analytics: The emergence of a discipline. *American Behavioral Scientist*, 57(10), 1380 đến 1400. [https://doi.org/10.1177/0002764213498851](https://doi.org/10.1177/0002764213498851) 


* Song, M., Günther, C. W., & van der Aalst, W. M. P. (2009). Trace clustering in process mining. Trong Business process management workshops (trang 109 đến 120). Springer. [https://doi.org/10.1007/978-3-642-00328-8_11](https://doi.org/10.1007/978-3-642-00328-8_11) 


* Van der Aalst, W. M. P. (2016). Process mining: Data science in action (Ấn bản lần 2). Springer. [https://doi.org/10.1007/978-3-662-49851-4](https://doi.org/10.1007/978-3-662-49851-4) 


* Van der Aalst, W. M. P., Weijters, T., & Maruster, L. (2004). Workflow mining: Discovering process models from event logs. *IEEE Transactions on Knowledge and Data Engineering*, 16(9), 1128 đến 1142. [https://doi.org/10.1109/TKDE.2004.47](https://doi.org/10.1109/TKDE.2004.47) 


* Winne, P. H., & Hadwin, A. F. (1998). Studying as self-regulated learning. Trong Metacognition in educational theory and practice (trang 277 đến 304). Lawrence Erlbaum Associates. 



---