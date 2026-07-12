## THẺ 1 

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

## Mở đầu 

1. Lý do chọn đề tài 

* Sự bùng nổ của các hệ thống quản lý học tập trực tuyến và giáo dục số tại các trường đại học đã tạo ra một khối lượng dữ liệu nhật ký khổng lồ về hành vi của người học.


* Tuy nhiên, các phương pháp phân tích học tập truyền thống chủ yếu tập trung vào những số liệu thống kê tĩnh như thời gian truy cập, số lần click hay điểm số, mà bỏ qua khía cạnh động, tức là trình tự, tần suất và cách thức sinh viên thực hiện các hoạt động học tập theo thời gian.


* Bên cạnh đó, mô hình đào tạo truyền thống với các lộ trình học tập cào bằng, áp dụng chung cho mọi sinh viên, không còn đáp ứng được nhu cầu, năng lực và tốc độ học tập riêng biệt của từng người, dẫn đến tỷ lệ nản chí hoặc bỏ học cao.


* Trong bối cảnh đó, khai phá quy trình nổi lên như một cầu nối giữa khoa học dữ liệu và quản lý quy trình, cho phép trực quan hóa, kiểm định và tối ưu hóa các quy trình thực tế dựa trên nhật ký sự kiện.


* Việc ứng dụng Process Mining vào Learning Analytics giúp phác họa lại bản đồ hành trình học tập thực tế của sinh viên, từ đó phát hiện các điểm nghẽn và những hành vi học tập lệch chuẩn hoặc kém hiệu quả, làm cơ sở để xây dựng và điều chỉnh lộ trình học tập cá nhân hóa một cách tự động và chính xác hơn.



2. Mục tiêu nghiên cứu 

* Nghiên cứu này nhằm thiết kế, thử nghiệm và đánh giá một khung giải pháp ứng dụng kỹ thuật Process Mining vào phân tích học tập.


* Từ đó, nghiên cứu hướng tới việc phát hiện các mô hình hành vi học tập thực tế và đề xuất giải pháp cá nhân hóa lộ trình học tập cho sinh viên một cách tự động, đồng thời kiểm chứng xem giải pháp này có cải thiện độ chính xác của lộ trình và hiệu quả học tập của sinh viên so với các phương pháp định hướng thông thường hay không.



3. Câu hỏi nghiên cứu 

* 
**Câu hỏi 1:** Làm thế nào để xây dựng một quy trình chuẩn hóa, đi từ việc trích xuất dữ liệu nhật ký trên hệ thống quản lý học tập đến việc áp dụng các thuật toán khai phá quy trình phục vụ phân tích học tập?


* 
**Câu hỏi 2:** Việc ứng dụng Process Mining giúp phát hiện những đặc trưng và sai lệch nào trong hành trình học tập thực tế của các nhóm sinh viên có học lực khác nhau?


* 
**Câu hỏi 3:** Lộ trình học tập được cá nhân hóa dựa trên kết quả phân tích Process Mining có giúp cải thiện kết quả học tập và mức độ hài lòng của sinh viên so với lộ trình cố định ban đầu hay không?



---

## Phần 2. Tổng quan nghiên cứu và phương pháp nghiên cứu 

#### 2.1. 

Tổng quan các nghiên cứu trước và lý do lựa chọn hướng tiếp cận 

* Phân tích học tập, hiểu theo nghĩa là việc đo lường, thu thập và phân tích dữ liệu về người học nhằm cải thiện quá trình dạy và học, đã được xác lập như một lĩnh vực nghiên cứu độc lập từ đầu những năm 2010, khi các hệ thống quản lý học tập trở nên phổ biến ở bậc đại học (Siemens, 2013).


* Đa số các công trình theo hướng này, cũng như các công trình thuộc lĩnh vực khai phá dữ liệu giáo dục nói chung, tập trung khai thác các chỉ số tổng hợp ở cấp độ kết quả, chẳng hạn điểm số, thời lượng truy cập hay số lần tương tác, mà ít đi sâu vào trình tự và tính động của hành vi học tập theo thời gian (Romero và Ventura, 2020).


* Khai phá quy trình là một hướng tiếp cận ra đời trong lĩnh vực quản lý quy trình nghiệp vụ, với nền tảng thuật toán được đặt ra từ công trình của van der Aalst và cộng sự về khai phá luồng công việc từ nhật ký sự kiện (van der Aalst, Weijters, và Maruster, 2004) , sau đó được hệ thống hóa toàn diện trong chuyên khảo của van der Aalst (2016).


* Khi được đưa vào lĩnh vực giáo dục, hướng tiếp cận này hình thành một nhánh nghiên cứu riêng gọi là khai phá quy trình giáo dục.


* Bogarín, Cerezo và Romero (2018), trong một tổng quan hệ thống về khai phá quy trình giáo dục, đã chỉ ra rằng phần lớn các nghiên cứu ứng dụng kỹ thuật này để khám phá lại quy trình học tập thực tế của sinh viên trên các hệ thống quản lý học tập, phát hiện những trình tự học tập lệch chuẩn so với thiết kế ban đầu của khóa học, tuy nhiên phần lớn các nghiên cứu này vẫn dừng lại ở mô tả hành vi mà chưa gắn kết chặt chẽ với các đặc điểm tâm lý và nhận thức của người học.


* Một số công trình gần đây đã bắt đầu kết hợp khai phá quy trình với các lý thuyết về tự điều chỉnh học tập.


* Cerezo, Bogarín, Esteban và Romero (2020) áp dụng thuật toán Inductive Miner trên dữ liệu tương tác của sinh viên đại học để khám phá mô hình tự điều chỉnh học tập, và cho thấy quy trình học tập của nhóm đạt và nhóm không đạt có sự khác biệt rõ rệt về cấu trúc trình tự.


* Winne và Hadwin (1998) trước đó đã đặt nền tảng lý thuyết cho việc xem học tập tự điều chỉnh như một chuỗi các pha lập kế hoạch, giám sát và điều chỉnh, đây chính là cơ sở lý thuyết để diễn giải các đặc trưng hành vi trích xuất từ log, chẳng hạn mức độ đều đặn hay tính tuyến tính khi điều hướng nội dung, như những biểu hiện quan sát được của quá trình tự điều chỉnh học tập.


* Điểm chung của các nghiên cứu nêu trên là hầu hết chỉ sử dụng một nguồn dữ liệu duy nhất, hoặc log hành vi hoặc khảo sát tâm lý, mà ít khi đối chiếu trực tiếp cả hai nguồn trên cùng một nhóm người học để kiểm tra xem log một mình có đủ để diễn giải đúng ý nghĩa hành vi hay không. Đây chính là khoảng trống mà nghiên cứu này hướng tới lấp đầy.


* Kế thừa nền tảng thuật toán khai phá quy trình của van der Aalst và cộng sự, cũng như hướng tiếp cận kết hợp với lý thuyết tự điều chỉnh học tập của Cerezo và cộng sự, nghiên cứu lựa chọn thiết kế một quy trình phân tích hai tầng. Trong đó, kết quả khai phá quy trình từ log khách quan được đối chiếu trực tiếp với dữ liệu khảo sát chủ quan trên cùng một nhóm 200 học viên, nhằm kiểm định xem những phát hiện thuần túy từ hành vi có được diễn giải đúng hay không, và từ đó đề xuất một cách tiếp cận cá nhân hóa lộ trình học tập toàn diện hơn.



#### 2.2. 

Bối cảnh và nguồn dữ liệu 

Để trả lời các câu hỏi nghiên cứu, đề tài triển khai một nghiên cứu trường hợp trên khóa học trực tuyến SoDiTEC, mã lớp TDC01, diễn ra trong tháng 5 năm 2024, với 200 học viên tham gia. Bốn nguồn dữ liệu được thu thập và đối chiếu song song, bao gồm dữ liệu hành vi khách quan trích xuất trực tiếp từ hệ thống quản lý học tập, và dữ liệu chủ quan thu thập qua khảo sát tâm lý và nhận thức của học viên.

| STT | Nguồn dữ liệu | Quy mô | Vai trò trong nghiên cứu |
| --- | --- | --- | --- |
| 1 | Nhật ký sự kiện gốc trích xuất từ hệ thống, định dạng edX | Khoảng 21 MB, hàng trăm nghìn sự kiện của 200 học viên trong tháng 5 năm 2024 | Dữ liệu thô đầu vào cho quá trình khai phá quy trình |
| 2 | Báo cáo điểm số của nền tảng | 1.558 bản ghi, 42 cột dữ liệu điểm từng câu hỏi video và bài quiz | Bổ sung biến kết quả học tập theo từng học viên |
| 3 | Danh sách học viên đăng ký khóa học | 1.531 học viên | Đối chiếu định danh và nhóm lớp |
| 4 | Bảng đặc trưng hành vi đã trích xuất từ log | 200 học viên với 27 đặc trưng hành vi | Dùng để phân khúc học lực và tính tương quan |
| 5 | Khảo sát chủ quan trước, trong và sau khóa học | 200 học viên với 38 biến số | Đo động lực, định hướng mục tiêu, khả năng tự điều chỉnh học tập, tải nhận thức, cảm xúc và mức độ hài lòng, những khía cạnh mà log hệ thống không thể quan sát trực tiếp |

(Nguồn dữ liệu tổng hợp dựa trên bối cảnh nghiên cứu) 

#### 2.3. 

Phương pháp chọn mẫu 

* Tổng thể nghiên cứu là toàn bộ học viên đăng ký khóa học SoDiTEC mã lớp TDC01, với quy mô 1.531 người theo danh sách của nền tảng.


* Từ tổng thể này, nghiên cứu áp dụng phương pháp chọn mẫu có chủ đích theo tiêu chí dữ liệu đầy đủ, tức là chỉ giữ lại những học viên vừa có đầy đủ log hành vi trong suốt khóa học, vừa hoàn thành khảo sát ở cả ba thời điểm trước, trong và sau khóa học.


* Sau khi lọc theo tiêu chí này, mẫu nghiên cứu cuối cùng gồm 200 học viên, được sử dụng xuyên suốt cho toàn bộ các phân tích trong Phần 3.


* Việc chọn mẫu theo tiêu chí dữ liệu đầy đủ, thay vì chọn mẫu ngẫu nhiên, giúp bảo đảm tính nhất quán khi đối chiếu song song hai nguồn dữ liệu khách quan và chủ quan trên cùng một người học. Tuy nhiên điều này cũng có thể tạo ra một độ lệch nhất định, vì những học viên hoàn thành đầy đủ cả log lẫn khảo sát có xu hướng là những người tham gia tích cực hơn so với mặt bằng chung của 1.531 học viên đăng ký. Hạn chế này được trình bày lại ở Phần 5.3 của báo cáo.


* Về cơ cấu, mẫu 200 học viên trải rộng trên sáu lớp hoặc đợt tuyển sinh khác nhau, được trình bày chi tiết ở mục 3.3.4, cho phép quan sát phần nào sự khác biệt giữa các nhóm học viên theo bối cảnh tổ chức.



#### 2.4. 

Quy trình xử lý và khai phá quy trình 

Quy trình chuẩn hóa được xây dựng và áp dụng trong nghiên cứu gồm năm bước, trực tiếp trả lời câu hỏi nghiên cứu thứ nhất:

1. 
**Bước 1 - Trích xuất dữ liệu:** Lấy toàn bộ sự kiện thô từ hệ thống, bao gồm đăng ký khóa học, xem video, tua video, thay đổi tốc độ phát, điều hướng nội dung, làm bài quiz, xem đáp án và tham gia diễn đàn, gắn với từng học viên và khóa học cụ thể. Mỗi sự kiện được chuẩn hóa thành ba thành phần cơ bản theo đúng cấu trúc dữ liệu tiêu chuẩn của khai phá quy trình, gồm mã định danh học viên đóng vai trò mã ca, nhãn hoạt động, và thời điểm xảy ra sự kiện (van der Aalst, 2016).


2. 
**Bước 2 - Trừu tượng hóa hoạt động:** Gom nhóm hàng chục loại sự kiện thô thành tám nhãn hoạt động ở mức khái niệm học tập, gồm xem video, điều hướng, hoàn thành, làm quiz, đóng nội dung, tham gia diễn đàn, đăng ký và xem đáp án, giúp việc phát hiện quy trình không bị nhiễu bởi các chi tiết kỹ thuật.


3. 
**Bước 3 - Khai phá và kiểm định quy trình:** Dựng biểu đồ chuyển tiếp giữa các hoạt động, thống kê các biến thể trình tự học tập, phân tích phễu tiến độ theo từng chương, xác định phân bố thời điểm học tập cao điểm, và gán hồ sơ quy trình điển hình cho mỗi học viên dựa trên trình tự thực tế của họ. Chi tiết kỹ thuật của bước này được trình bày riêng ở mục 2.5.


4. 
**Bước 4 - Trích đặc trưng hành vi và phân khúc học viên:** Tính toán 27 đặc trưng cho mỗi học viên như số sự kiện, số phiên học, số ngày học, mức độ đều đặn, thời gian không hoạt động gần nhất, độ tuyến tính khi điều hướng, tỷ lệ quay lui, số lần tua video, số lần thay đổi tốc độ, số lần kiểm tra đáp án, chuỗi trả lời sai liên tiếp dài nhất và mức độ tham gia diễn đàn. Dựa trên các đặc trưng này, học viên được phân vào ba nhóm học lực là cao, trung bình và thấp, đồng thời được gắn cờ cảnh báo sớm nếu có nguy cơ bỏ học.


5. 
**Bước 5 - Đối chiếu với dữ liệu chủ quan:** Ghép các đặc trưng hành vi từ log với các biến khảo sát tâm lý và nhận thức theo từng học viên, nhằm kiểm tra xem log một mình có đủ để giải thích kết quả học tập hay không, phục vụ trả lời câu hỏi nghiên cứu thứ hai và thứ ba.



#### 2.5. 

Kỹ thuật khai phá quy trình được áp dụng 

* Để dựng biểu đồ chuyển tiếp giữa các hoạt động, còn gọi là biểu đồ chuyển tiếp trực tiếp, nghiên cứu áp dụng nguyên lý nền tảng của các thuật toán khai phá quy trình dựa trên quan hệ chuyển tiếp trực tiếp, do van der Aalst và cộng sự đề xuất (van der Aalst, Weijters, và Maruster, 2004). Với mỗi học viên, chuỗi sự kiện được sắp xếp theo đúng thứ tự thời gian, sau đó mỗi cặp hoạt động liền kề nhau trong chuỗi được ghi nhận là một quan hệ chuyển tiếp trực tiếp. Toàn bộ quan hệ này được tổng hợp trên 200 học viên để tính tần suất xuất hiện của từng cặp chuyển tiếp, từ đó dựng nên biểu đồ mạng lưới hoạt động với các cạnh được gán trọng số theo tần suất, cho phép nhận diện những luồng chuyển tiếp chủ đạo trong toàn khóa học.


* Để phân tích biến thể trình tự, mỗi học viên được biểu diễn bằng một chuỗi ký tự ghép nối toàn bộ các hoạt động mà học viên đó thực hiện theo đúng thứ tự thời gian, gọi là một vệt hoạt động. Những học viên có vệt hoạt động giống hệt nhau được gộp vào cùng một biến thể, sau đó các biến thể được xếp hạng theo số lượng học viên sở hữu (van der Aalst, 2016).


* Do số lượng biến thể chi tiết quá lớn để diễn giải trực tiếp, nghiên cứu thực hiện thêm một bước gộp nhóm theo hai chiều đặc trưng hành vi nổi bật nhất của mỗi học viên, gồm loại hoạt động chiếm ưu thế trong vệt hoạt động là xem video hay làm quiz, và kiểu điều hướng là tuyến tính hay nhảy cóc, được xác định dựa trên chỉ số độ tuyến tính điều hướng. Việc gộp nhóm theo hai chiều đặc trưng này tạo thành bốn hồ sơ quy trình ở mục 3.2.2, và về bản chất là một hình thức đơn giản hóa của kỹ thuật phân cụm vệt hoạt động (Song, Günther, và van der Aalst, 2009).


* Đối với phân tích phễu tiến độ, mỗi chương được gán một sự kiện mốc là lần đầu tiên học viên tương tác với nội dung của chương đó. Số học viên có sự kiện mốc tại một chương, chia cho tổng số học viên ban đầu, cho ra tỷ lệ phần trăm còn hoạt động tại chương đó.


* Để xác định ngưỡng cảnh báo sớm (ví dụ: ngưỡng số lần tua lùi hay số lần xem lại video được coi là cao), nghiên cứu sử dụng ngưỡng phân vị thứ 60 của toàn bộ mẫu, tức là nhóm 40% học viên có giá trị cao nhất trên chỉ số tương ứng được coi là nhóm cao. Đây là một kỹ thuật phổ biến trong các hệ thống cảnh báo sớm dựa trên phân tích học tập, cho phép xác định nhóm cần chú ý mà không cần giả định trước về phân phối của dữ liệu.


* Việc phân khúc học lực thành ba nhóm cao, trung bình và thấp, cũng như việc phân nhóm lộ trình thành ba cụm (có kế hoạch, khám phá và nguy cơ) dựa trên dữ liệu khảo sát, được thực hiện bằng cách kết hợp điểm số tổng hợp từ nhiều đặc trưng hành vi hoặc tâm lý có liên quan đến kết quả học tập, sau đó chia nhóm theo các mức phân vị của điểm tổng hợp này. Cách tiếp cận này là một dạng đơn giản hóa của các phương pháp phân cụm nhằm tạo ra các nhóm người học có đặc điểm tương đồng để thiết kế can thiệp phù hợp.



#### 2.6. 

Phương pháp phân tích 

Nghiên cứu sử dụng kết hợp thống kê mô tả để tính tần suất và tỷ lệ phần trăm của các hoạt động, phân tích biến thể quy trình và biểu đồ chuyển tiếp trực tiếp là hai kỹ thuật lõi của khai phá quy trình đã trình bày ở mục 2.5, phân tích tương quan Pearson giữa các cặp biến hành vi và kết quả cũng như giữa các biến chủ quan và kết quả, phân khúc và so sánh nhóm để đối chiếu chéo hai nguồn dữ liệu, và phân tích phễu theo tiến trình nội dung khóa học để phát hiện các điểm rơi rớt học viên.

---

## Phần 3. Kết quả nghiên cứu 

#### 3.1. 

Tổng quan mẫu và hành vi học tập chung 

Trên tổng số 200 học viên khóa TDC01, bức tranh tổng quan cho thấy một khóa học có tỷ lệ hoàn thành thấp và tỷ lệ nguy cơ bỏ học cao ngay từ dữ liệu hành vi log.

| Chỉ số từ log | Giá trị |
| --- | --- |
| Số học viên | 200 |
| Tỷ lệ cảnh báo nguy cơ bỏ học | 40% |
| Mức độ hoàn thành trung bình | 0,294, tương đương 29,4% |
| Điểm quiz trung bình | 0,438, tương đương 43,8% |
| Mức độ học đều đặn trung bình | 0,155 |
| Số phiên học trung bình mỗi học viên | 11,9 phiên |

(Bảng số liệu tổng quan hành vi học tập từ log khách quan) 

Số liệu từ báo cáo điểm số của nền tảng, với 1.558 bản ghi chấm điểm, và danh sách 1.531 học viên đăng ký cho thấy quy mô lớp thực tế lớn hơn nhóm 200 học viên được lấy mẫu sâu để phân tích hành vi. Nhóm 200 học viên này được chọn làm mẫu đại diện vì có đầy đủ dữ liệu log và khảo sát song song.

#### 3.2. 

Kết quả khai phá quy trình từ log khách quan 

##### 3.2.1. 

Tần suất hoạt động và chuyển tiếp giữa các hoạt động 

Sau khi trừu tượng hóa, tổng cộng có khoảng 46.000 sự kiện học tập chính được ghi nhận. Hoạt động chiếm ưu thế tuyệt đối là xem video (43%) và điều hướng nội dung (36,4%).

| Hoạt động | Số sự kiện | Tỷ lệ phần trăm |
| --- | --- | --- |
| Xem video | 19.785 | 43,0% |
| Điều hướng | 16.756 | 36,4% |
| Hoàn thành | 3.425 | 7,4% |
| Làm quiz | 2.938 | 6,4% |
| Đóng nội dung | 2.375 | 5,2% |
| Tham gia diễn đàn | 475 | 1,0% |
| Đăng ký khóa học | 200 | 0,4% |
| Xem đáp án | 102 | 0,2% |

(Bảng thống kê số lượng và tỷ lệ hoạt động của học viên) 

* 
**Vòng lặp chủ đạo:** Chuyển tiếp từ làm quiz sang xem video và ngược lại chiếm ưu thế với khoảng 784 và 783 lượt, phản ánh mô hình học xem rồi kiểm tra lặp lại nhiều lần.


* 
**Các phát hiện đáng chú ý khác:** Chuyển tiếp từ xem video sang diễn đàn đạt 263 lượt, và từ diễn đàn quay lại video đạt 133 lượt. Chuyển tiếp từ làm quiz sang xem đáp án ghi nhận 89 lượt, phản ánh hành vi tìm đáp án khi gặp khó khăn.



##### 3.2.2. 

Mức độ đa dạng của trình tự học tập 

* Một phát hiện quan trọng mà thống kê tĩnh không thể thấy được là trong 200 học viên, có tới 156 trình tự học khác nhau, tức khoảng 78% học viên có một đường đi riêng biệt. Đây là một quy trình học tập rất phân tán và thiếu chuẩn hóa. Trình tự phổ biến nhất cũng chỉ chiếm 3,5% số học viên.


* Để dễ đọc và ứng dụng, nghiên cứu gộp thành bốn hồ sơ quy trình khái quát:



| Hồ sơ quy trình | Số học viên | Tỷ lệ phần trăm |
| --- | --- | --- |
| Xem nhiều video, đi theo trình tự tuyến tính | 104 | 52,0% |
| Xem nhiều video, nhảy giữa các nội dung | 92 | 46,0% |
| Làm nhiều quiz, nhảy giữa các nội dung | 3 | 1,5% |
| Làm nhiều quiz, đi theo trình tự tuyến tính | 1 | 0,5% |

(Bảng phân bố nhóm hồ sơ quy trình học tập) 

Gần một nửa số học viên (46%) thuộc nhóm nhảy giữa các nội dung thay vì đi theo trình tự chương tuyến tính, đây là một tín hiệu hành vi quan trọng để cá nhân hóa việc gợi ý nội dung tiếp theo.

##### 3.2.3. 

Phễu tiến độ theo chương và giờ học cao điểm 

| Chương | Tỷ lệ học viên còn hoạt động |
| --- | --- |
| Chương 1 | 100% |
| Chương 2 | 99,5% |
| Chương 3 | 99,5% |
| Chương 4 | 98,5% |
| Chương 5 | 97,5% |
| Chương 6 | 89,5% |

(Bảng phễu tiến độ học tập qua các chương) 

Phân tích phễu theo sáu chương nội dung cho thấy tỷ lệ học viên còn hoạt động giảm dần đều, và giảm mạnh nhất ở Chương 6 (từ 97,5% xuống còn 89,5%). Đây là điểm nghẽn rõ rệt nhất cần được can thiệp. Về mặt thời gian, giờ học cao điểm của học viên tập trung vào khoảng 6 giờ sáng, 13 giờ và 15 giờ chiều. Dữ liệu này giúp ích cho việc thiết lập nhắc học tự động theo khung giờ phù hợp cá nhân.

##### 3.2.4. 

Phân khúc theo học lực và nhóm cảnh báo sớm 

| Phân khúc | Số học viên | Hoàn thành trung bình | Điểm quiz trung bình | Mức đều đặn trung bình | Mức quay lui trung bình | Tỷ lệ nguy cơ bỏ học |
| --- | --- | --- | --- | --- | --- | --- |
| Cao | 63 | 0,364 | 0,448 | 0,233 | 0,242 | 12,7% |
| Trung bình | 83 | 0,296 | 0,460 | 0,147 | 0,302 | 35,0% |
| Thấp | 54 | 0,209 | 0,391 | 0,075 | 0,319 | 79,6% |

(Bảng thống kê chi tiết theo phân khúc học lực) 

* Kết quả phân khúc cho thấy nhóm học lực thấp có mức hoàn thành, điểm quiz, và chỉ số đều đặn thấp hơn hẳn, trong khi chỉ số quay lui lại cao hơn.


* Có tới 79,6% học viên nhóm này rơi vào diện cảnh báo nguy cơ. Riêng với 80 học viên được gắn cờ cảnh báo (chiếm 40%), mức hoàn thành trung bình chỉ đạt 0,254 và thời gian không hoạt động gần nhất trung bình lên tới 43 ngày. Đây là tín hiệu cảnh báo sớm hữu ích phát hiện từ log trước khi có điểm số cuối kỳ.



##### 3.2.5. 

Tương quan giữa hành vi log và kết quả học tập 

| Cặp biến số | Hệ số tương quan | Diễn giải |
| --- | --- | --- |
| Mức đều đặn và mức hoàn thành | 0,459 | Học đều dự báo mức hoàn thành cao, đây là một chỉ báo khách quan khá mạnh |
| Số ngày học và mức hoàn thành | 0,459 | Số ngày xuất hiện gắn liền với tiến độ hoàn thành |
| Độ tuyến tính điều hướng và điểm quiz | 0,328 | Điều hướng có kế hoạch, đi theo trình tự thường cho điểm tốt hơn |
| Tỷ lệ quay lui và điểm quiz | -0,301 | Quay lui nhiều thường gắn với điểm thấp hơn, có thể là dấu hiệu dò dẫm hoặc bí bài |
| Chuỗi trả lời sai dài nhất và mức hoàn thành | 0,067 | Tương quan yếu và nhiễu, cần đặt trong bối cảnh chủ quan để diễn giải đúng |
| Tỷ lệ tua lùi và điểm quiz | -0,110 | Tua lùi nhiều là tín hiệu mơ hồ, có thể là đang ôn bài hoặc đang bí bài |

(Bảng hệ số tương quan Pearson giữa hành vi log và kết quả học tập) 

Hai dòng cuối trong bảng trên chỉ ra một số hành vi log như chuỗi trả lời sai liên tiếp hay tua lùi video có tương quan yếu hoặc mơ hồ với kết quả học tập. Log ghi nhận được điều gì đang xảy ra, nhưng không giải thích được vì sao nó xảy ra, đặt ra nhu cầu đối chiếu với dữ liệu chủ quan ở phần tiếp theo.

#### 3.3. 

Kết quả khảo sát chủ quan về nhận thức và tâm lý người học 

Song song với log hành vi, 200 học viên được khảo sát ở ba thời điểm : trước khóa học (đo động lực, năng lực bản thân, SRL) , trong lúc học (đo tải nhận thức, cảm xúc) , và sau khóa học (đo mức độ hài lòng, ý định học tiếp).

##### 3.3.1. 

Tổng quan kết quả đầu ra 

| Chỉ số | Giá trị |
| --- | --- |
| Tổng số học viên khảo sát | 200 |
| Tỷ lệ hoàn thành theo khảo sát | 46,0% |
| Tỷ lệ bỏ học | 32,0% |
| Điểm tổng kết trung bình trên thang 100 | 58,995 |
| Mức độ hài lòng trung bình trên thang 5 | 2,78 |

(Bảng tổng hợp chỉ số đầu ra từ khảo sát) 

##### 3.3.2. 

Tương quan giữa yếu tố chủ quan và kết quả 

| Cặp biến số | Hệ số tương quan | Ý nghĩa |
| --- | --- | --- |
| Khả năng tự điều chỉnh học tập và điểm số | 0,498 | Tương quan dương, ở mức vừa đến mạnh, cho thấy khả năng tự điều chỉnh học tập là một chỉ báo tốt cho kết quả |
| Mức độ bực bội hoặc bí bài và tỷ lệ bỏ học | 0,304 | Tương quan dương, cho thấy sự khó chịu về cảm xúc dự báo được khả năng bỏ học, điều mà log không quan sát được |
| Tải nhận thức và mức độ hài lòng | âm 0,276 | Tương quan âm, cho thấy quá tải nhận thức làm giảm sự hài lòng |
| Điểm số và mức độ hài lòng | 0,370 | Tương quan chỉ ở mức vừa, cho thấy điểm số và sự hài lòng là hai khái niệm khác nhau, cần đo lường riêng |
| Mức tăng niềm tin vào năng lực bản thân và cảm nhận học được | 0,687 | Tương quan dương và khá mạnh, cho thấy sự tiến bộ về niềm tin gắn chặt với cảm nhận học được |

(Bảng hệ số tương quan giữa yếu tố tâm lý chủ quan và kết quả học tập) 

So với các tương quan tính từ log, yếu tố chủ quan về khả năng tự điều chỉnh học tập có sức giải thích kết quả học tập mạnh hơn hầu hết các đặc trưng hành vi log. Đặc biệt, mức độ bực bội hoặc bí bài dự báo được khả năng bỏ học, đây là một tín hiệu cảnh báo sớm hoàn toàn nằm ngoài khả năng quan sát của log hệ thống.

##### 3.3.3. 

Ba nhóm lộ trình học tập 

Dựa trên dữ liệu khảo sát, học viên được phân thành ba cụm lộ trình: nhóm có kế hoạch, nhóm khám phá tự do, và nhóm thuộc diện nguy cơ cao.

| Nhóm lộ trình | Số học viên | Tỷ lệ bỏ học | Điểm trung bình | Hài lòng trung bình | Mức bực bội trung bình |
| --- | --- | --- | --- | --- | --- |
| Nhóm có kế hoạch | 85 | 22,4% | 66,51 | 2,99 | 3,26 |
| Nhóm khám phá | 53 | 30,2% | 58,11 | 2,97 | 3,26 |
| Nhóm nguy cơ | 62 | 46,8% | 49,45 | 2,33 | 3,36 |

(Bảng so sánh chi tiết giữa ba nhóm lộ trình tự nhiên) 

Nhóm nguy cơ (chiếm khoảng 31%) có tỷ lệ bỏ học cao gấp đôi nhóm có kế hoạch, điểm số thấp hơn rõ rệt và mức độ hài lòng thấp nhất. Đây chính là nhóm mục tiêu ưu tiên cho các can thiệp cá nhân hóa.

##### 3.3.4. 

Tỷ lệ hoàn thành theo lớp học 

| Lớp học | Số học viên | Tỷ lệ hoàn thành |
| --- | --- | --- |
| Quy Nhơn | 125 | 45,6% |
| Lớp tháng 7 năm 2025 | 24 | 29,2% |
| Ban Giám đốc tại Hà Nội | 17 | 64,7% |
| Học viện cơ sở tại thành phố Hồ Chí Minh | 10 | 30,0% |
| Lớp tháng 8 năm 2025 | 16 | 56,3% |
| Sở Khoa học Công nghệ Hà Nội năm 2026 | 8 | 62,5% |

(Bảng tỷ lệ hoàn thành phân bổ theo từng lớp học bối cảnh) 

Sự chênh lệch khá lớn giữa các lớp (dao động từ 29,2% đến 64,7%) cho thấy các yếu tố bối cảnh tổ chức và lớp học cũng ảnh hưởng đáng kể đến kết quả và cần được kiểm soát khi xây dựng mô hình.

#### 3.4. 

Đối chiếu dữ liệu khách quan và chủ quan 

Đóng góp cốt lõi của nghiên cứu nằm ở việc chỉ ra rằng dữ liệu log khách quan vẫn tồn tại những điểm mù cần được bổ khuyết bằng dữ liệu chủ quan. Hai trường hợp sau đây minh chứng rõ nét cho điều này:

* 
**Trường hợp 1 - Tua lùi video nhiều lần:** Với nhóm học viên có số lần tua lùi thuộc top 40% cao nhất, điểm quiz trung bình chỉ đạt 0,413 nhưng độ lệch chuẩn lên tới 0,263, với điểm số trải rộng từ 0 đến 1. Bản thân log không thể phân biệt được đây là hành vi ôn tập chủ động hay là dấu hiệu bế tắc trong học tập.


* 
**Trường hợp 2 - Xem lại video nhiều lần:** Trong nhóm học viên có tỷ lệ xem lại video cao, khi tách theo định hướng mục tiêu từ khảo sát, nhóm xem lại nhiều và có định hướng làm chủ kiến thức đạt điểm trung bình 54,6, trong khi nhóm định hướng thấp chỉ đạt 46,0. Cùng một hành vi trên log, nhưng chỉ có dữ liệu chủ quan về định hướng mục tiêu mới tách được hai nhóm có kết cục học tập khác nhau để đưa ra khuyến nghị can thiệp phù hợp.



Khai phá quy trình trên log hành vi là điều kiện cần nhưng chưa đủ để cá nhân hóa chính xác lộ trình học tập; bắt buộc phải ghép thêm dữ liệu chủ quan về định hướng mục tiêu, khả năng tự điều chỉnh học tập và cảm xúc để diễn giải đúng hành vi.

---

## Phần 4. Thảo luận và trả lời câu hỏi nghiên cứu 

#### 4.1. 

Về quy trình chuẩn hóa từ log đến khai phá quy trình 

Nghiên cứu đã xây dựng và kiểm chứng thành công một quy trình năm bước áp dụng trên log thực tế của 200 học viên. Quy trình này tạo ra các sản phẩm phân tích tiêu chuẩn của Process Mining (tần suất hoạt động, biểu đồ chuyển tiếp, phân tích biến thể và phễu tiến độ) có thể tái sử dụng cho các khóa học khác trên cùng nền tảng.

#### 4.2. 

Về đặc trưng và sai lệch hành vi giữa các nhóm học lực 

Khai phá quy trình phát hiện được các đặc trưng và sai lệch rõ rệt giữa các nhóm học lực:

1. Độ đa dạng trình tự học rất cao (156 biến thể trên 200 học viên), và gần một nửa học viên đi theo lối nhảy cóc thay vì tuyến tính.


2. Nhóm học lực thấp có mức độ học không đều đặn hơn hẳn và quay lui nhiều hơn, với gần 80% rơi vào diện cảnh báo nguy cơ.


3. Điểm nghẽn tiến độ rõ rệt nhất nằm ở Chương 6, khi tỷ lệ học viên còn hoạt động giảm gần 10 điểm phần trăm chỉ trong một chương.



Tuy nhiên, nghiên cứu cũng chỉ ra giới hạn của cách tiếp cận này khi một số hành vi log riêng lẻ như tua lùi video hay chuỗi trả lời sai không có tương quan đủ mạnh và rõ ràng nếu không đặt trong bối cảnh chủ quan.

#### 4.3. 

Về khả năng cải thiện kết quả và sự hài lòng nhờ cá nhân hóa 

Dữ liệu hiện có thu thập sau khi triển khai lộ trình ban đầu và chưa có nhóm đối chứng dùng lộ trình cá nhân hóa hoàn chỉnh, cho phép trả lời một phần câu hỏi thông qua so sánh giữa các nhóm lộ trình đã hình thành tự nhiên. Nhóm có kế hoạch đạt điểm trung bình 66,5 và tỷ lệ bỏ học 22,4%, trong khi nhóm nguy cơ chỉ đạt 49,5 điểm với tỷ lệ bỏ học 46,8%. Chênh lệch 17 điểm và gấp đôi tỷ lệ bỏ học giữa hai nhóm là bằng chứng gián tiếp thuyết phục rằng việc phát hiện sớm và can thiệp cá nhân hóa kịp thời có tiềm năng cải thiện đáng kể kết quả học tập và sự hài lòng. Để khẳng định chắc chắn quan hệ nhân quả, cần một thực nghiệm có đối chứng ở giai đoạn nghiên cứu tiếp theo.

---

## Phần 5. Kết luận, hạn chế và hướng phát triển 

#### 5.1. 

Kết luận 

Nghiên cứu đã chứng minh tính khả thi và giá trị của việc ứng dụng khai phá quy trình trong phân tích học tập thông qua trường hợp thực tế của khóa học TDC01. Dữ liệu chủ quan về động lực, khả năng tự điều chỉnh học tập và cảm xúc là thành phần cần thiết để cá nhân hóa chính xác hơn, khắc phục những điểm mù của log dữ liệu hành vi. Nghiên cứu cũng đề xuất một mô hình phân nhóm ba lộ trình học tập làm cơ sở thiết kế can thiệp phù hợp.

#### 5.2. 

Hàm ý thực tiễn 

* Nên ưu tiên can thiệp tại điểm nghẽn Chương 6 và gửi nhắc học vào các khung giờ cao điểm riêng biệt của từng học viên.


* Triển khai cảnh báo sớm nguy cơ bỏ học dựa trên mức độ học đều đặn và thời gian không hoạt động gần nhất từ log, kết hợp đo mức độ bực bội định kỳ.


* Thiết kế can thiệp khác nhau theo từng nhóm lộ trình (duy trì nhịp độ nhóm có kế hoạch, định hướng nhóm khám phá, hỗ trợ tích cực và giảm tải nhận thức cho nhóm nguy cơ).


* Tích hợp thêm một số câu hỏi khảo sát ngắn về định hướng mục tiêu và cảm xúc vào hệ thống để bổ khuyết dữ liệu hành vi.



#### 5.3. 

Hạn chế của nghiên cứu 

Nghiên cứu còn một số hạn chế bao gồm: dữ liệu chỉ đến từ một khóa học với 200 học viên làm hạn chế tính khái quát hóa ; chưa có nhóm đối chứng thực nghiệm ngẫu nhiên để so sánh trực tiếp ; các hệ số tương quan sử dụng chỉ phản ánh quan hệ tuyến tính; và dữ liệu khảo sát phụ thuộc vào tính tự nhận thức của học viên.

#### 5.4. 

Hướng phát triển tiếp theo 

* Triển khai một thực nghiệm có đối chứng, so sánh trực tiếp giữa lộ trình cố định và lộ trình cá nhân hóa tự động.


* Mở rộng dữ liệu sang nhiều khóa học và lớp học khác nhau để tăng tính khái quát.


* Áp dụng các kỹ thuật khai phá quy trình nâng cao hơn để dự báo sớm hơn nữa nguy cơ bỏ học ngay từ những phiên học đầu tiên, xây dựng hệ thống gợi ý theo thời gian thực.



---

## Tài liệu tham khảo 

* Bogarín, A., Cerezo, R., & Romero, C. (2018). A survey on educational process mining. *Wiley Interdisciplinary Reviews: Data Mining and Knowledge Discovery*, 8(1), Article e1230. [https://doi.org/10.1002/widm.1230](https://doi.org/10.1002/widm.1230) 


* Cerezo, R., Bogarín, A., Esteban, M., & Romero, C. (2020). Process mining for self-regulated learning assessment in e-learning. *Journal of Computing in Higher Education*, 32(1), 74 đến 88. [https://doi.org/10.1007/s12528-019-09225-y](https://doi.org/10.1007/s12528-019-09225-y) (bản mở truy cập: [https://arxiv.org/abs/2403.12068](https://arxiv.org/abs/2403.12068)) 


* Romero, C., & Ventura, S. (2020). Educational data mining and learning analytics: An updated survey. *Wiley Interdisciplinary Reviews: Data Mining and Knowledge Discovery*, 10(3), Article e1355. [https://doi.org/10.1002/widm.1355](https://doi.org/10.1002/widm.1355) 


* Siemens, G. (2013). Learning analytics: The emergence of a discipline. *American Behavioral Scientist*, 57(10), 1380 đến 1400. [https://doi.org/10.1177/0002764213498851](https://doi.org/10.1177/0002764213498851) 


* Song, M., Günther, C. W., & van der Aalst, W. M. P. (2009). Trace clustering in process mining. Trong D. Ardagna, M. Mecella, & J. Yang (Chủ biên), *Business process management workshops* (trang 109 đến 120). Springer. [https://doi.org/10.1007/978-3-642-00328-8_11](https://doi.org/10.1007/978-3-642-00328-8_11) 


* Van der Aalst, W. M. P. (2016). *Process mining: Data science in action* (Ấn bản lần 2). Springer. [https://doi.org/10.1007/978-3-662-49851-4](https://doi.org/10.1007/978-3-662-49851-4) 


* Van der Aalst, W. M. P., Weijters, T., & Maruster, L. (2004). Workflow mining: Discovering process models from event logs. *IEEE Transactions on Knowledge and Data Engineering*, 16(9), 1128 đến 1142. [https://doi.org/10.1109/TKDE.2004.47](https://doi.org/10.1109/TKDE.2004.47) 


* Winne, P. H., & Hadwin, A. F. (1998). Studying as self-regulated learning. Trong D. J. Hacker, J. Dunlosky, & A. C. Graesser (Chủ biên), *Metacognition in educational theory and practice* (trang 277 đến 304). Lawrence Erlbaum Associates. 



---