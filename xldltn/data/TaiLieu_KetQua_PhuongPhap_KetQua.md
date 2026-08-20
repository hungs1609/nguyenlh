TÀI LIỆU PHƯƠNG PHÁP & KẾT QUẢ NGHIÊN CỨU 

Đánh giá hiệu quả ứng dụng khai phá quy trình (Process Mining) trong phân tích học tập nhằm tối ưu hóa lộ trình cá nhân hóa của sinh viên đại học 

* 
**Nghiên cứu trường hợp:** Khóa SoDiTEC, mã lớp TDC01, tháng 5 năm 2024.


* 
**Thiết kế nghiên cứu:** Khung bán thực nghiệm nhóm không tương đương, tiền kiểm – hậu kiểm (NEGD).



---

PHẦN A. PHƯƠNG PHÁP NGHIÊN CỨU 

### A.1. 

Thiết kế nghiên cứu 

Nghiên cứu sử dụng thiết kế bán thực nghiệm với nhóm có sẵn, không tương đương, có tiền kiểm và hậu kiểm. Ký hiệu hai dòng quan sát của thiết kế là $O_1 (X) O_2$ cho nhóm gần thực nghiệm và $O_1 — O_2$ cho nhóm gần đối chứng, trong đó dấu gạch rời phản ánh việc hai nhóm không được phân bổ ngẫu nhiên. Đây là điểm phân biệt cốt lõi so với thực nghiệm ngẫu nhiên có đối chứng (RCT).

* 
**Lý do không phân bổ ngẫu nhiên:** Dữ liệu mang tính hồi cứu, thu thập lại từ một khóa học đã diễn ra, nên nhà nghiên cứu không thể can thiệp vào quá trình phân nhóm. Hai nhóm so sánh được xác định từ cụm lộ trình học tập hình thành tự nhiên trên nền hành vi và đặc điểm tâm lý sẵn có của học viên, chứ không phải do gán ngẫu nhiên. Việc dùng nhóm có sẵn là lựa chọn bắt buộc bởi bản chất dữ liệu, đồng thời cũng là nguồn gốc của hạn chế phương pháp luận quan trọng nhất, được lượng hóa ở Phần B.



Quy trình thực hiện gồm 5 bước chuẩn hóa, đi từ log thô đến đối chiếu chủ quan:

1. 
**Trích xuất dữ liệu:** Lấy toàn bộ sự kiện thô định dạng edX (đăng ký, xem/tua/đổi tốc độ video, điều hướng, làm quiz, xem đáp án, diễn đàn), chuẩn hóa mỗi sự kiện thành bộ ba mã ca – nhãn hoạt động – dấu thời gian.


2. 
**Trừu tượng hóa hoạt động:** Gom hàng chục loại sự kiện thô thành 8 nhãn hoạt động ở mức khái niệm học tập.


3. 
**Khai phá & kiểm định quy trình:** Dựng biểu đồ chuyển tiếp trực tiếp, thống kê biến thể trình tự, phân tích phễu tiến độ theo chương.


4. 
**Trích đặc trưng & phân khúc:** Tính 27 đặc trưng hành vi cho mỗi học viên, phân nhóm học lực và gắn cờ cảnh báo sớm.


5. 
**Đối chiếu chủ quan:** Ghép đặc trưng log với 38 biến khảo sát tâm lý – nhận thức để kiểm tra log một mình có đủ diễn giải kết quả hay không.



Trên nền mẫu 200 học viên, ba cụm lộ trình được xác lập: cụm A – có kế hoạch (**85 HV**, nhóm gần thực nghiệm), cụm C – nguy cơ (**62 HV**, nhóm gần đối chứng), và cụm B – khám phá (**53 HV**) giữ vai trò tham chiếu bổ sung trong phân tích phương sai.

### A.2. 

Đối tượng tham gia 

Tổng thể nghiên cứu là **1.531 học viên** đăng ký khóa TDC01. Từ đó, nghiên cứu áp dụng chọn mẫu có chủ đích theo tiêu chí dữ liệu đầy đủ — chỉ giữ những học viên vừa có đủ log hành vi suốt khóa, vừa hoàn thành khảo sát ở cả ba thời điểm trước, trong và sau khóa học — thu được mẫu cuối cùng **200 học viên**, trải trên 6 lớp/đợt tuyển sinh.

#### Bảng A.1. 

Cơ cấu mẫu theo lớp/đợt và ba cụm lộ trình 

| Lớp / đợt tuyển sinh | n | Hoàn thành | Ghi chú |
| --- | --- | --- | --- |
| Quy Nhơn | 125 | 45,6% | Lớp chủ lực 

 |
| Lớp tháng 7.2025 | 24 | 29,2% | Hoàn thành thấp 

 |
| BGD Hà Nội | 17 | 64,7% | Hoàn thành cao nhất 

 |
| Lớp tháng 8.2025 | 16 | 56,2%

 |  |
| HVCS HCM | 10 | 30,0%

 |  |
| Sở KHCN HN 2026 | 8 | 62,5%

 |  |
| **Tổng mẫu** | **200** | **46,0%** | <br>**A=85 · C=62** 

 |

> 
> **Lưu ý về độ lệch chọn mẫu (responder/volunteer bias):** 200 học viên có đủ log và khảo sát ba đợt vốn tích cực hơn mặt bằng 1.531 người đăng ký; do đó kết quả không thể khái quát trực tiếp cho toàn bộ học viên chưa hoạt động. Cần báo cáo khác biệt responder vs non-responder trên các biến khách quan.
> 
> 

### A.3. 

Biến nghiên cứu 

* 
**Biến độc lập ($X$):** Việc định vị học viên vào nhóm lộ trình bằng phân tích Process Mining kết hợp Learning Analytics, được thao tác hóa bằng tư cách thành viên cụm (A so với C). Đây là một biến phân loại quan sát được, không phải một can thiệp chủ động do nhà nghiên cứu bật/tắt (xem A.5 và B.2).


* 
**Biến phụ thuộc ($Y$):** Kết quả học tập và thái độ, gồm hai nhóm:


* 
*Kết quả khách quan:* Điểm cuối kỳ thang 100; tình trạng bỏ học.


* 
*Kết quả chủ quan/tâm lý:* Niềm tin năng lực bản thân sau khóa, mức hài lòng, cảm nhận tiến bộ, ý định học tiếp.




* 
**Trục thời gian đo lường:** Được tổ chức theo ba trục thời gian gồm **PRE** (đường cơ sở, đo trước khóa), **IN-SITU** (đo tức thời trong khóa bằng khảo sát vi mô gắn mốc thời gian – ESM), và **POST** (kết quả cuối khóa).



#### Bảng A.2. 

Khung biến theo trục thời gian tiền kiểm – trong khóa – hậu kiểm 

| Nhóm biến | Ví dụ biến | Thang | Thời điểm |
| --- | --- | --- | --- |
| Độc lập ($X$) | Cụm lộ trình A / C (từ PM + khảo sát) | A/B/C | — 

 |
| Đồng biến / nền | `self_efficacy_pre`, SRL tổng hợp, nền tảng, động lực | 1–5 | PRE 

 |
| Trạng thái trong khóa | tải nhận thức, bực bội, chán (ESM) | 1–9 / 1–5 | IN-SITU 

 |
| Kết quả khách quan | `final_grade`; `dropout_flag` | 0–100; 0/1 | POST 

 |
| Kết quả chủ quan | hài lòng, cảm nhận tiến bộ, `self_efficacy_post`, ý định tiếp | 1–5 | POST 

 |
| 

 |  |  |  |

### A.4. 

Công cụ đo lường 

* Bộ công cụ chủ quan kế thừa các thang đo đã được kiểm định trong tài liệu quốc tế, dịch và điều chỉnh cho bối cảnh khóa học.


* Bộ công cụ khách quan là 27 đặc trưng hành vi trích từ log edX.


* Việc dùng đồng thời hai nguồn đo bằng hai phương pháp khác nhau giúp giảm thiên lệch phương pháp chung (common-method bias).



#### Bảng A.3. 

Nguồn gốc và độ tin cậy của công cụ đo 

| Cấu trúc đo | Thang tham chiếu | Độ tin cậy | Ghi chú |
| --- | --- | --- | --- |
| SRL tổng hợp (4 tiểu mục) | OSLQ (Barnard) | Cronbach $\alpha = 0,889$ | Tính trực tiếp — đạt 

 |
| Động lực & self-efficacy | MSLQ (Pintrich) | Thang đã kiểm định | Chưa có dữ liệu tiểu mục 

 |
| Định hướng mục tiêu | Elliot Achievement Goal | Thang đã kiểm định | Mastery / Performance 

 |
| Cảm xúc học tập | AEQ (Pekrun) | Thang đã kiểm định | Đo in-situ (ESM) 

 |
| Hài lòng / tiến bộ / ý định | Satisfaction; Perceived Learning; Behavioral Intention | Thang đã kiểm định | Outcome hậu kiểm 

 |
| 27 đặc trưng hành vi | Trích từ log edX | Khách quan | Đối chiếu chéo 

 |

* 
**Về độ tin cậy:** Hệ số nhất quán nội tại Cronbach $\alpha$ của thang SRL tổng hợp (bốn tiểu mục gồm lập kế hoạch, giám sát siêu nhận thức, điều tiết nỗ lực, sắp xếp môi trường) đạt **0,889**, vượt ngưỡng 0,8 thường được coi là tốt. Với các thang còn lại, dữ liệu hiện chỉ lưu điểm cấu trúc (đã tổng hợp) chứ chưa lưu điểm từng tiểu mục, nên chưa thể tính $\alpha$ tại chỗ ; giá trị nội dung dựa trên tính đã kiểm định của thang gốc.


* 
**Về giá trị (validity):** Cần bổ sung kiểm định bất biến đo lường (measurement invariance) trên mẫu Việt trước khi so sánh xuyên nhóm ở quy mô lớn hơn.



### A.5. 

Vấn đề đạo đức 

* 
**Đồng thuận & ẩn danh:** Dữ liệu phân tích dùng mã ẩn danh (`learner_id`), không chứa tên hay email ; danh sách định danh thật và username đã băm được lưu tách biệt. Vì là dữ liệu LMS hồi cứu, cần có phê duyệt sử dụng dữ liệu của đơn vị và/hoặc đồng thuận cho mục đích nghiên cứu; đây là điều kiện tiên quyết khi mở rộng.


* 
**Rủi ro cho người tham gia:** Nghiên cứu quan sát lại quá trình học tự nhiên, không áp đặt can thiệp chủ động, nên không có nguy cơ gây hại trực tiếp và không có tình huống "giữ lại lợi ích" của nhóm đối chứng.


* 
**Yếu tố có thể làm sai lệch kết quả:** 1. Hai nhóm không tương đương ở đường cơ sở — thiên lệch chọn lọc, đe dọa hiệu lực nội tại;
2. Thiên lệch tự báo cáo và hồi cố ở khảo sát;
3. Thiên lệch responder/volunteer;
4. Chỉ khảo sát một khóa/một thời điểm — giới hạn hiệu lực ngoại;
5. Tương quan chỉ đo quan hệ tuyến tính.



> 
> **Biện pháp kiểm soát:** Điểm (1) được kiểm soát định lượng bằng ANCOVA ở phần B.4 ; các điểm còn lại được nêu rõ như một giới hạn của nghiên cứu.
> 
> 

---

PHẦN B. KẾT QUẢ NGHIÊN CỨU 

### B.1. 

Quá trình và kết quả phân tích tiền kiểm 

Trước khi khóa học diễn ra, hai biến đường cơ sở — niềm tin năng lực bản thân (self-efficacy tiền kiểm) và mức tự điều chỉnh học tập tổng hợp — được so sánh giữa hai nhóm bằng kiểm định $t$ Welch nhằm đánh giá mức độ tương đương. Kết quả bác bỏ giả định tương đương.

#### Bảng B.1. 

Tiền kiểm A vs C — hai nhóm KHÔNG tương đương ở đường cơ sở 

| Biến tiền kiểm | A (TB±ĐLC) | C (TB±ĐLC) | $t$ | $p$ | $d$ |
| --- | --- | --- | --- | --- | --- |
| Self-efficacy (tiền) | 3,09±0,67 | 2,62±0,64 | 4,25 | <0,001 | 0,70 |
| SRL tổng hợp | 3,69±0,51 | 2,28±0,56 | 15,57 | <0,001 | 2,64 |
| Động lực nội tại | 3,26±0,93 | 2,08±0,77 | 8,37 | <0,001 | 1,36 |
| Nền tảng tự đánh giá | 2,94±0,93 | 3,21±0,99 | −1,66 | 0,099 | −0,28 |
| Định hướng làm chủ | 3,06±0,84 | 3,02±1,19 | 0,24 | 0,810 | 0,04 |

* 
**Phân tích chi tiết:** Nhóm A xuất phát cao hơn nhóm C có ý nghĩa thống kê ở self-efficacy ($d=0,70$) và đặc biệt ở SRL ($d=2,64$ — chênh lệch rất lớn). Ngược lại, định hướng làm chủ và nền tảng tự đánh giá không khác biệt, cho thấy khác biệt nền tập trung ở năng lực tự điều chỉnh và niềm tin, chứ không phải ở kiến thức đầu vào hay động cơ mục tiêu.


* 
**Hệ quả trực tiếp:** Mọi so sánh hậu kiểm phải kiểm soát đường cơ sở, nếu không sẽ nhầm chênh lệch sẵn có thành "hiệu ứng".



### B.2. 

Quá trình và kết quả can thiệp — ghi chú về tính trung thực (fidelity) 

* 
**Tính minh bạch:** Nghiên cứu **KHÔNG** triển khai một chương trình can thiệp chủ động do nhà nghiên cứu thiết kế (chẳng hạn bật tính năng gợi ý lộ trình cá nhân hóa cho nhóm thực nghiệm và tắt cho nhóm đối chứng). "Can thiệp" ở đây là quá trình học tập tự nhiên mà hai nhóm đã trải qua, được quan sát lại qua log. Đây là can thiệp quan sát được theo nghĩa hồi cứu. Vì không có tác động chủ động, khái niệm trung thực can thiệp (treatment fidelity) theo nghĩa cổ điển không áp dụng.


* 
Đảm bảo tính trung thực ở 3 lớp có thể kiểm chứng:


* 
*Trung thực quy trình phân tích:* Cùng một pipeline 5 bước được áp dụng đồng nhất cho toàn bộ 200 học viên, không tùy biến theo nhóm.


* 
*Trung thực tiêu chí mẫu:* Tiêu chí dữ liệu đầy đủ (đủ log + khảo sát ba đợt) áp dụng như nhau cho mọi học viên.


* 
*Trung thực thao tác hóa nhóm:* Quy tắc gán cụm dựa trên điểm tổng hợp hành vi/tâm lý là xác định và tái lập được.




* **Bối cảnh mô tả:** Tổng cộng khoảng **46.000 sự kiện chính** được ghi nhận; hoạt động chủ đạo là xem video và điều hướng; **40% học viên** rơi vào diện cảnh báo sớm; điểm nghẽn tiến độ rõ nhất ở Chương 6. Đây là bối cảnh của "can thiệp quan sát được", không phải bằng chứng về một tác động do nghiên cứu tạo ra.



### B.3. 

Quá trình và kết quả phân tích hậu kiểm 

Sau khóa học, các biến hậu kiểm được so sánh giữa hai nhóm bằng cùng công cụ tương đương tiền kiểm (với self-efficacy) và bằng công cụ hậu kiểm chuyên biệt (với các outcome còn lại). Ở mức so sánh thô, nhóm A vượt nhóm C trên mọi chỉ số.

#### Bảng B.2. 

Hậu kiểm A vs C (t-test Welch; bỏ học bằng $\chi^2$) — khác biệt thô rõ rệt 

| Biến hậu kiểm | A | C | Thống kê | $p$ | $d$ |
| --- | --- | --- | --- | --- | --- |
| Điểm cuối kỳ /100 | 66,51 | 49,45 | $t=7,17$ | <0,001 | 1,20 |
| Ý định học tiếp | 3,12 | 2,37 | $t=5,48$ | <0,001 | 0,92 |
| Hài lòng | 2,99 | 2,33 | $t=4,91$ | <0,001 | 0,82 |
| Self-efficacy (hậu) | 3,19 | 2,55 | $t=4,02$ | <0,001 | 0,67 |
| Cảm nhận tiến bộ | 3,54 | 3,15 | $t=3,17$ | 0,002 | 0,54 |
| Bỏ học | 22,4% | 46,8% | $\chi^2=9,72$ | 0,002 | — |


> Hình B.1. So sánh kết quả hậu kiểm và tỷ lệ bỏ học giữa hai nhóm có sẵn. 
> 
> 
![So sánh kết quả hậu kiểm và tỷ lệ bỏ học giữa hai nhóm có sẵn.](sosanhketquahaukiem.jpg)

### B.4. 

Kết quả kiểm định giả thuyết 

* **Giả thuyết:** $H_0$ — không có khác biệt kết quả học tập giữa nhóm có kế hoạch (A) và nhóm nguy cơ (C); $H_1$ — có khác biệt, theo hướng A tốt hơn C. Quy trình kiểm định đi từ so sánh thô, đến kiểm soát nội bộ bằng change-score, đến ANCOVA kiểm soát đường cơ sở.


* **So sánh thô:** Cả 4 biến hậu kiểm độc lập (Bảng B.2) đều khác biệt có ý nghĩa theo hướng $H_1$; ở mức này $H_0$ bị bác bỏ. Tuy nhiên do lệch nền nên so sánh thô chưa đủ kết luận.


* 
**Change-score self-efficacy (hậu − tiền):** Nhóm A tăng trung bình **+0,10**, nhóm C giảm **−0,07**; khác biệt có ý nghĩa ($t=2,27$; $p=0,025$; $d=0,38$). Trong nội bộ, thay đổi của A tiệm cận ngưỡng ($t=1,98$; $p=0,051$) còn C không đổi có ý nghĩa ($p=0,205$). Tức là chiều biến thiên của hai nhóm khác nhau, chứ không chỉ là chênh lệch sẵn có được kéo dài.


* 
**ANCOVA #1 — kiểm soát đường cơ sở:** Với biến phụ thuộc self-efficacy hậu kiểm và đồng biến là self-efficacy tiền kiểm, hiệu ứng nhóm A/C **không còn ý nghĩa thống kê** ($F=0,24$; $p=0,627$; partial $\eta^2=0,002$). Trung bình hiệu chỉnh gần như trùng nhau ($A=2,93$ vs $C=2,90$). Giả định ANCOVA đạt: đồng nhất độ dốc hồi quy $p=0,654$; đồng nhất phương sai Levene $p=0,962$. Gần như toàn bộ khoảng cách self-efficacy hậu kiểm được giải thích bởi khác biệt tiền kiểm, không phải bởi nhóm.


* 
**ANCOVA #2 - điểm cuối kỳ:** Kiểm soát đồng thời self-efficacy tiền, nền tảng và SRL, hiệu ứng nhóm lên điểm cuối kỳ cũng **không có ý nghĩa** ($F=1,59$; $p=0,209$; partial $\eta^2=0,011$ - nhóm chỉ giải thích thêm ~1% phương sai điểm sau khi trừ nền). Khoảng cách 17 điểm ở so sánh thô phần lớn bị hấp thụ bởi các đồng biến đường cơ sở.



> Hình B.2. Kiểm định giả thuyết self-efficacy: chênh lệch thô (trái) biến mất sau khi ANCOVA hiệu chỉnh đường cơ sở (phải). 
> 
> 

| Phương pháp kiểm soát nền | Diễn giải & Kết luận chi tiết |
| --- | --- |
| **Diễn giải tổng hợp (Nghịch lý Lord)** | Change-score cho khác biệt có ý nghĩa ($p=0,025$) trong khi ANCOVA cho kết quả null ($p=0,63$). Hai phương pháp kiểm soát nền có thể cho kết luận trái chiều trên cùng dữ liệu quan sát — đây chính là nghịch lý Lord. Vì vậy bằng chứng phụ thuộc lựa chọn phương pháp và không thể xem là chắc chắn.

 |
| **Kết luận thận trọng** | <br>$H_0$ bị bác bỏ ở mức so sánh thô, nhưng sau khi kiểm soát đường cơ sở, hiệu ứng của tư cách nhóm lên self-efficacy và điểm là không đáng kể. Khác biệt kết quả A–C chủ yếu phản ánh **ĐẶC ĐIỂM SẴN CÓ** của học viên, không phải một tác động do việc phân nhóm/PM tạo ra. Không được kết luận nhân quả từ thiết kế này.

 |

#### Bảng B.3. 

Hiệu ứng thô so với hiệu ứng sau khi kiểm soát đường cơ sở 

| Kết quả | Cohen d (thô) | partial $\eta^2$ (ANCOVA) | Ý nghĩa nhóm còn lại |
| --- | --- | --- | --- |
| Self-efficacy hậu | 0,67 | 0,002 | Biến mất 

 |
| Điểm cuối kỳ | 1,20 | 0,011 | Không ý nghĩa 

 |
| $\Delta$ self-efficacy (change) | 0,38 | — | Nhỏ, có ý nghĩa 

 |
| 

 |  |  |  |

* 
**Hướng tiếp theo:** Kết quả ANCOVA lượng hóa đúng cảnh báo rằng phần lớn khác biệt hậu kiểm phản ánh sự kết hợp giữa đặc điểm sẵn có và quá trình học. Để chuyển từ tương quan có định hướng sang bằng chứng nhân quả, bước tiếp theo cần một thực nghiệm có phân ngẫu nhiên thực thụ, với một chương trình can thiệp (bật gợi ý lộ trình cá nhân hóa) được thiết kế và ghi nhận đầy đủ tài liệu vận hành, phân tích bằng ANCOVA/mô hình hồi quy đa biến kiểm soát đồng biến đường cơ sở.



---

PHẦN C. KẾT LUẬN 

Kết quả kiểm định giả thuyết được tổng hợp theo trình tự tiền nghiệm – hậu nghiệm trên ba cụm lộ trình học tập: có kế hoạch (A), khám phá (B) và nguy cơ (C).

* 
**Kết quả tiền nghiệm:** So sánh ba cụm cho thấy khác biệt về niềm tin năng lực bản thân ở đường cơ sở: cụm khám phá (B) có $TB = 3,32, ĐLC = 0,68$; cụm có kế hoạch (A) có $TB = 3,09, ĐLC = 0,67$; cụm nguy cơ (C) có $TB = 2,62, ĐLC = 0,64$. Kiểm định ANOVA ($F(2, 197) = 16,77, p < 0,001$) cho thấy có khác biệt ý nghĩa về niềm tin năng lực bản thân giữa cụm khám phá và cụm nguy cơ (chênh lệch $TB = 0,70, p < 0,001$) và giữa cụm có kế hoạch và cụm nguy cơ (chênh lệch $TB = 0,46, p < 0,001$). Không có khác biệt ý nghĩa giữa cụm có kế hoạch và cụm khám phá (chênh lệch $TB = 0,23, p = 0,119$). Chênh lệch nền thể hiện đậm hơn ở mức tự điều chỉnh học tập ($F(2, 197) = 156,24, p < 0,001$).


* 
**Kết quả hậu nghiệm:** Sau khóa học, khác biệt về điểm số cuối kỳ giữa ba cụm tiếp tục rõ rệt: cụm A có $TB = 66,51, ĐLC = 14,14$; cụm B có $TB = 58,11, ĐLC = 14,39$; cụm C có $TB = 49,45, ĐLC = 14,30$. Kiểm định ANOVA ($F(2, 197) = 25,79, p < 0,001$) cho thấy khác biệt ý nghĩa ở cả ba cặp: cụm A vs cụm C (chênh lệch $TB = 17,05, p < 0,001$), cụm B vs cụm C (chênh lệch $TB = 8,66, p = 0,004$) và cụm A vs cụm B (chênh lệch $TB = 8,39, p = 0,003$). Xu hướng tương tự xuất hiện ở self-efficacy hậu nghiệm ($F(2, 197) = 12,54, p < 0,001$) với khác biệt ý nghĩa giữa cụm C và hai cụm còn lại, nhưng không có ý nghĩa giữa cụm A và cụm B (chênh lệch $TB = 0,20, p = 0,457$). Về tỷ lệ bỏ học, cụm nguy cơ (46,8%) cao hơn cụm có kế hoạch (22,4%) một cách có ý nghĩa ($\chi^2 = 9,72, p = 0,002$).


* 
**Lưu ý diễn giải:** Vì ba cụm đã khác biệt ngay từ tiền nghiệm (đặc biệt ở SRL), các khác biệt hậu nghiệm phản ánh khác biệt giữa các nhóm có sẵn. Khi kiểm soát đường cơ sở bằng ANCOVA, hiệu ứng của tư cách cụm lên niềm tin năng lực bản thân ($F = 0,24, p = 0,63$) và lên điểm số ($F = 1,59, p = 0,21$) giảm mạnh và không còn ý nghĩa thống kê. Do đó, kết quả nên được diễn giải như bằng chứng tương quan có định hướng, chưa phải bằng chứng nhân quả ; việc khẳng định hiệu quả của cá nhân hóa lộ trình cần một thực nghiệm có phân ngẫu nhiên ở giai đoạn tiếp theo.

### 1. Biến tiền kiểm và hậu kiểm

**Biến tiền kiểm:**

| Biến tiền kiểm | A (TB±ĐLC) | C (TB±ĐLC) | t | p |
| --- | --- | --- | --- | --- |
| Self-efficacy (tiền) | 3,09±0,67 | 2,62±0,64 | 4,25 | <0,001 |

**Biến hậu kiểm:**

| Biến hậu kiểm | A (TB) | C (TB) | t | p |
| --- | --- | --- | --- | --- |
| Self-efficacy (hậu) | 3,19 | 2,55 | 4,02 | <0,001 |

---

### ② Change-score self-efficacy (hậu – tiền)

| Chỉ số | A | C | t | p |
| --- | --- | --- | --- | --- |
| Δ self-efficacy | 0,10 | -0,07 | 2,27 | 0,025 |

* 
**Nhóm A:** Nhóm có kế hoạch học tập ($N=85$).


* 
**Nhóm C:** Nhóm không có kế hoạch học tập ($N=62$).



### 1. Phân tích biến thiên nội bộ từng nhóm

* 
**Nhóm A:** Có sự thay đổi về mức độ Self-efficacy từ thời điểm tiền kiểm ($M_1 = 3,09, SD_1 = 0,67$) sang thời điểm hậu kiểm ($M_2 = 3,19$). Điểm đánh giá Self-efficacy sau can thiệp của Nhóm A cao hơn so với trước can thiệp một khoảng là $M_2 - M_1 = 0,10$.


* 
**Nhóm C:** Có sự thay đổi về mức độ Self-efficacy từ thời điểm tiền kiểm ($M_1 = 2,62, SD_1 = 0,64$) sang thời điểm hậu kiểm ($M_2 = 2,55$). Điểm đánh giá Self-efficacy hậu kiểm của Nhóm C giảm so với trước can thiệp một khoảng là $M_2 - M_1 = -0,07$.



### 2. Kết quả đối chiếu giữa hai nhóm

* 
**Tại thời điểm Tiền kiểm:** Kết quả kiểm định ($t = 4,25, p < 0,001$) cho thấy có sự khác biệt có ý nghĩa thống kê giữa điểm số của Nhóm A so với Nhóm C. Điểm số ban đầu của Nhóm A cao hơn Nhóm C ($M_A - M_C = 0,47$), tạo ra sự lệch nền rất lớn (Cohen's $d = 0,70$) và là nguồn gây nhiễu chính cho mọi so sánh hậu kiểm.


* 
**Tại thời điểm Hậu kiểm (t-test thô chưa kiểm soát nền):** Kết quả kiểm định ($t = 4,02, p < 0,001$) cho thấy có sự khác biệt có ý nghĩa thống kê giữa điểm Self-efficacy hậu kiểm của Nhóm A so với Nhóm C. Điểm hậu kiểm của Nhóm A vẫn cao hơn Nhóm C ($M_A - M_C = 0,64$, Cohen's $d = 0,67$). Tuy nhiên kết quả thô này chưa phản ánh chính xác hiệu quả can thiệp do ảnh hưởng từ sự lệch nền gốc.


* 
**Đối với mức độ thay đổi điểm số (Change-score):** Kết quả kiểm định ($t = 2,27, p = 0,025$) cho thấy có sự khác biệt có ý nghĩa thống kê về mức độ biến thiên điểm số giữa Nhóm A ($+0,10$) so với Nhóm C ($-0,07$).