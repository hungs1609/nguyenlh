## THẺ 3 

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

### PHẦN 1: MỞ ĐẦU 

#### 1.1. 

Lý do chọn đề tài 

* 
**Bối cảnh:** Sự bùng nổ của giáo dục số tạo ra khối lượng dữ liệu nhật ký (log dữ liệu) khổng lồ. Tuy nhiên, Phân tích học tập (Learning Analytics) truyền thống chỉ tập trung vào số liệu thống kê tĩnh (điểm số, lượt click), bỏ qua tính động và trình tự hành vi.


* 
**Vấn đề thực tế:** Lộ trình học tập "cào bằng" áp dụng chung cho mọi sinh viên gây ra tỷ lệ nản chí và bỏ học cao.


* 
**Giải pháp đề xuất:** Ứng dụng Khai phá quy trình (Process Mining) làm công cụ can thiệp nhằm phát hiện điểm nghẽn, hành vi lệch chuẩn để tự động điều chỉnh và cá nhân hóa lộ trình học tập.



#### 1.2. 

Mục tiêu nghiên cứu 

* 
**Mục tiêu tổng quát:** Thử nghiệm và đánh giá hiệu quả của giải pháp cá nhân hóa lộ trình học tập dựa trên kỹ thuật Process Mining.


* 
**Mục tiêu cụ thể:** 


* Xây dựng quy trình chuẩn hóa trích xuất và xử lý log dữ liệu hành vi.


* Đo lường và kiểm chứng sự cải thiện về hiệu quả học tập và độ chính xác của lộ trình đề xuất của sinh viên sau khi áp dụng can thiệp.





#### 1.3. 

Câu hỏi nghiên cứu và Giả thuyết thực nghiệm 

* 
**Câu hỏi 1:** Quy trình chuẩn hóa từ trích xuất log đến áp dụng thuật toán Process Mining được xây dựng như thế nào?


* 
**Câu hỏi 2:** Ứng dụng Process Mining giúp phát hiện những đặc trưng và sai lệch nào trong hành trình học tập thực tế của các nhóm sinh viên?


* 
**Câu hỏi 3:** Lộ trình học tập được cá nhân hóa dựa trên Process Mining kết hợp dữ liệu chủ quan có giúp nâng cao kết quả học tập và mức độ hài lòng của sinh viên hơn so với lộ trình cố định ban đầu hay không?


* 
**Giả thuyết nghiên cứu ($H_1$):** Sinh viên được học tập theo lộ trình cá nhân hóa (được tối ưu từ Process Mining và dữ liệu chủ quan) có kết quả học tập và mức độ hài lòng cao hơn ý nghĩa thống kê so với khi học theo lộ trình cố định.



---

### PHẦN 2: TỔNG QUAN TÀI LIỆU VÀ KHUNG LÝ THUYẾT 

#### 2.1. 

Tổng quan nghiên cứu (Literature Review) 

* 
**Tổng quan về Learning Analytics:** Xu hướng dịch chuyển từ thống kê tĩnh sang phân tích hành vi động (Siemens, 2013; Romero & Ventura, 2020).


* 
**Tổng quan về Educational Process Mining:** Nền tảng thuật toán của van der Aalst (2004, 2016) và các ứng dụng phát hiện hành vi lệch chuẩn (Bogarín et al., 2018).


* 
**Khoảng trống nghiên cứu (Research Gap):** Phần lớn nghiên cứu chỉ sử dụng nguồn dữ liệu đơn lẻ (hoặc log hành vi, hoặc khảo sát). Nghiên cứu này lấp đầy khoảng trống bằng quy trình phân tích hai tầng đối chiếu trực tiếp dữ liệu khách quan và chủ quan.



#### 2.2. 

Khung lý thuyết (Theoretical Framework) 

* 
**Lý thuyết Tự điều chỉnh học tập (Self-Regulated Learning - SRL) của Winne & Hadwin (1998):** Cơ sở để diễn giải các đặc trưng hành vi từ log (tính đều đặn, tính tuyến tính) thành các pha nhận thức.


* 
**Mô hình kết hợp Phân tích Quy trình và Phân cụm vệt hoạt động (Trace Clustering):** (Song, Günther, & van der Aalst, 2009).



---

### PHẦN 3: PHƯƠNG PHÁP NGHIÊN CỨU THỰC NGHIỆM 

#### 3.1. 

Thiết kế thực nghiệm (Experimental Design) 

Do đặc thù triển khai trên lớp học có sẵn (mã lớp TDC01), nghiên cứu áp dụng Thiết kế bán thực nghiệm (Quasi-experimental Design) dạng So sánh các nhóm tự hình thành (Static-Group Comparison) hoặc Thiết kế thực nghiệm một nhóm đo lường Trước - Sau (One-Group Pretest-Posttest Design) kết hợp đối chứng chéo theo phân cụm nội bộ.

#### 3.2. 

Biến số nghiên cứu (Variables) 

* 
**Biến độc lập (IV):** Phương thức tổ chức lộ trình học tập (Giai đoạn 1: Lộ trình cố định truyền thống; Giai đoạn 2: Can thiệp bằng Lộ trình cá nhân hóa dựa trên Process Mining).


* 
**Biến phụ thuộc (DV):** 


* Hiệu quả học tập (Điểm quiz, Tỷ lệ hoàn thành).


* Độ chính xác và phù hợp của lộ trình (Mức độ bực bội, Tải nhận thức, Mức độ hài lòng).




* 
**Biến kiểm soát (CV):** Giảng viên, nội dung khóa học SoDiTEC, nền tảng edX.



#### 3.3. 

Khách thể và Phương pháp chọn mẫu 

* 
**Tổng thể:** 1.531 học viên đăng ký khóa học SoDiTEC.


* 
**Mẫu thực nghiệm:** $N = 200$ học viên được lựa chọn theo phương pháp chọn mẫu có chủ đích (Purposive Sampling), đáp ứng tiêu chí có dữ liệu đầy đủ (gồm cả log hành vi và 3 đợt khảo sát).



#### 3.4. 

Công cụ thu thập dữ liệu và Quy trình can thiệp 

* 
**Công cụ khách quan:** Nhật ký sự kiện gốc (21 MB, định dạng edX), Báo cáo điểm số (1.558 bản ghi).


* 
**Công cụ chủ quan (Tiền kiểm & Hậu kiểm):** Bộ câu hỏi 38 biến số đo lường Động lực, SRL (Trước), Tải nhận thức, Cảm xúc (Trong), và Mức độ hài lòng (Sau).


* 
**[Quy trình xử lý 5 bước]**:



$$\text{Bước 1: Trích xuất log edX} \rightarrow \text{Bước 2: Trừu tượng hóa (8 nhãn)} \rightarrow \text{Bước 3: Khai phá quy trình} \rightarrow \text{Bước 4: Trích đặc trưng \& Phân khúc} \rightarrow \text{Bước 5: Đối chiếu dữ liệu chủ quan}$$






---

### PHẦN 4: KẾT QUẢ NGHIÊN CỨU VÀ PHÂN TÍCH THỰC NGHIỆM 

#### 4.1. 

Kết quả Khai phá Quy trình từ dữ liệu khách quan (Log dữ liệu) 

* 
**Phân bố hoạt động:** Xem video (43%) và Điều hướng (36.4%) chiếm chủ đạo.


* 
**Mức độ phân tán quy trình:** Phát hiện 156 biến thể trình tự trên 200 học viên (quy trình phân tán cao, chiếm 78%).


* 
**Bốn hồ sơ quy trình cốt lõi:** 


* Xem nhiều video, trình tự tuyến tính (52%).


* Xem nhiều video, nhảy cóc nội dung (46%).


* Làm nhiều quiz, nhảy cóc nội dung (1.5%).


* Làm nhiều quiz, trình tự tuyến tính (0.5%).




* 
**Điểm nghẽn (Bottleneck):** Phễu tiến độ giảm mạnh nhất ở Chương 6 (từ 97.5% xuống 89.5%).


* 
**Giờ cao điểm:** 6h, 13h, 15h.



#### 4.2. 

Kết quả phân khúc học lực và Cảnh báo sớm 

* 
**So sánh các phân khúc (Thống kê mô tả nhóm):** Nhóm học lực Thấp (54 SV) có mức đều đặn rất thấp (0.075), tỷ lệ quay lui cao (0.319), và 79.6% rơi vào diện nguy cơ bỏ học.


* 
**Tương quan tuyến tính (Pearson r):** Mức đều đặn tương quan thuận với mức hoàn thành ($r = 0.459$); tỷ lệ quay lui tương quan nghịch với điểm quiz ($r = -0.301$).



#### 4.3. 

Kết quả đối chiếu Thực nghiệm: Khắc phục "Điểm mù" của Log bằng Dữ liệu chủ quan 

Đây là phần trọng tâm chứng minh hiệu quả của mô hình can thiệp:

* 
**Trường hợp 1 (Tua lùi video):** Top 40% tua lùi nhiều có điểm số trải rộng từ 0 đến 1 ($\sigma = 0.263$). Log không phân biệt được SV đang "ôn tập" hay đang "bế tắc".


* 
**Trường hợp 2 (Xem lại nhiều lần):** Kết hợp định hướng mục tiêu (SRL) phân tách rõ: Nhóm có định hướng làm chủ kiến thức đạt điểm 54.6 vs. Nhóm định hướng thấp chỉ đạt 46.0.



#### 4.4. 

Đánh giá hiệu quả tối ưu hóa lộ trình cá nhân hóa (Trả lời câu hỏi 3) 

So sánh các nhóm lộ trình hình thành tự nhiên để chứng minh giả thuyết: Nhóm có kế hoạch (lộ trình tối ưu) có tỷ lệ bỏ học thấp (22.4%), điểm trung bình cao (66.51), mức độ hài lòng cao (2.99). Ngược lại, nhóm nguy cơ có tỷ lệ bỏ học lên tới 46.8% và điểm số chỉ đạt 49.45.

---

### PHẦN 5: THẢO LUẬN 

* 
**Ý nghĩa của quy trình 5 bước:** Chứng minh tính khả thi của việc chuyển đổi dữ liệu thô thành tri thức giáo dục có thể hành động (Actionable Insights).


* 
**Biện giải kết quả thực nghiệm:** Giải thích tại sao log hành vi một mình là "điều kiện cần nhưng chưa đủ". Việc cá nhân hóa bắt buộc phải tích hợp dữ liệu SRL và Cảm xúc (sự bực bội, tải nhận thức).


* 
**Yếu tố nhiễu bối cảnh (Contextual Factors):** Phân tích sự chênh lệch tỷ lệ hoàn thành giữa các lớp (Ban Giám đốc Hà Nội đạt 64.7% vs. Lớp tháng 7/2025 chỉ đạt 29.2%), cho thấy bối cảnh tổ chức là một biến nhiễu cần kiểm soát trong thực nghiệm giáo dục.



---

### PHẦN 6: KẾT LUẬN, HẠN CHẾ VÀ HƯỚNG PHÁT TRIỂN 

#### 6.1. 

Kết luận và Hàm ý thực tiễn 

* Khẳng định giải pháp kết hợp Process Mining và dữ liệu chủ quan giải quyết được bài toán cá nhân hóa lộ trình.


* 
**Hành động sư phạm:** Thiết kế can thiệp tự động (nhắc học giờ cao điểm, cấu trúc lại Chương 6, giảm tải nhận thức cho nhóm nguy cơ).



#### 6.2. 

Hạn chế của nghiên cứu (Đặc thù môn Thực nghiệm) 

* Mẫu nghiên cứu ($N=200$) trong 1 khóa học tháng 5/2024 làm hạn chế tính khái quát hóa (External Validity).


* 
**Hạn chế lớn nhất về mặt thực nghiệm:** Chưa triển khai thiết kế thực nghiệm ngẫu nhiên có đối chứng hoàn chỉnh (Randomized Controlled Trial - RCT) ở giai đoạn này để so sánh trực tiếp, các nhóm so sánh hiện tại là các nhóm hình thành tự nhiên (Static groups).



#### 6.3. 

Hướng phát triển tiếp theo 

Triển khai một nghiên cứu thực nghiệm có đối chứng đầy đủ (A/B Testing trên hệ thống): Nhóm A (Học lộ trình cố định) vs. Nhóm B (Học lộ trình cá nhân hóa bằng Process Mining) để kiểm định triệt để quan hệ nhân quả.

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