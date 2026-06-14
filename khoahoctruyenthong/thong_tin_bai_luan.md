# TỔNG HỢP KIẾN THỨC VÀ CƠ SỞ LÝ THUYẾT CHO BÀI LUẬN
## Đề tài: Thiết kế lại hệ thống truyền thông tích hợp cho nền tảng đào tạo số daotao.ai

Tài liệu này hệ thống hóa toàn bộ thông tin thực tế của học viên và các cơ sở lý thuyết truyền thông áp dụng trực tiếp vào bài luận cuối kỳ.

---

## 1. Thông tin thực tế về daotao.ai tại EdTech Centre

### 1.1. Bối cảnh tác giả bài luận
* **Vai trò:** Chuyên viên trực tiếp vận hành tại Trung tâm Công nghệ và Giải pháp Chuyển đổi số trong giáo dục (**EdTech Centre**) – Đại học Bách khoa Hà Nội.
* **Nhiệm vụ đảm nhận:** Toàn bộ quy trình vận hành bao gồm đăng tải khóa học, trực tiếp trả lời/hỗ trợ giải đáp thắc mắc của học viên, đối soát dữ liệu và làm báo cáo tiến độ học tập.

### 1.2. Các nhóm đối tượng tham gia (Stakeholders)
* **Người gửi (Sender):** Ban quản trị EdTech Centre (trong đó có chuyên viên hỗ trợ).
* **Người nhận (Receiver):** Học viên (sinh viên HUST, cán bộ công chức thuộc Đề án 06, học viên cộng đồng tự do).
* **Đối tác liên kết (Partners):** Giảng viên tham gia biên soạn bài giảng, các cơ quan cử cán bộ đi học.

### 1.3. Kênh truyền thông hiện tại
* **Nội bộ & Đối tác:** Sử dụng phần lớn qua ứng dụng nhắn tin **Zalo** và tổ chức **họp trực tiếp**.
* **Với Học viên:** Tiếp nhận hỗ trợ và thông báo qua 3 kênh chính:
  1. **Fanpage Facebook**
  2. **Form hỗ trợ trên website daotao.ai**
  3. **Kênh Zalo OA (Official Account)**

---

## 2. Phân tích hiện trạng & Điểm nhiễu (Noise) thực tế

Dựa trên thực tế vận hành, hệ thống truyền thông hiện tại đang bộc lộ những điểm nghẽn và rào cản truyền thông rõ rệt:

| Mối quan hệ | Kênh truyền thông | Điểm nhiễu (Noise) / Bất cập thực tế | Hậu quả |
| :--- | :--- | :--- | :--- |
| **Nội bộ & Đối tác** | Zalo chat | Tin nhắn trao đổi công việc dễ bị trôi; không có hệ thống lưu trữ/phân loại yêu cầu. | Các yêu cầu kỹ thuật/nội dung dễ bị bỏ sót hoặc phản hồi trễ. |
| **Nội bộ & Đối tác** | Giao tiếp ngôn ngữ | Các thông tin yêu cầu về mặt kỹ thuật/hệ thống bị hiểu sai lệch giữa các bên. | Triển khai tính năng hoặc cập nhật khóa học bị sai lệch so với yêu cầu ban đầu. |
| **Với Học viên** | Website daotao.ai | Nút đăng ký khóa học khó tìm thấy (giao diện chưa tối ưu). | Học viên gặp khó khăn ngay từ bước tiếp cận đầu tiên. |
| **Với Học viên** | Hệ thống Đăng nhập | Lỗi đăng nhập thường xuyên xảy ra nhưng học viên không biết cách tự xử lý. | Quá tải yêu cầu hỗ trợ gửi về Trung tâm EdTech. |
| **Với Học viên** | Form hỗ trợ web / Zalo OA | Thời gian phản hồi từ trung tâm bị chậm do khối lượng câu hỏi thủ công quá lớn. | Học viên mất kiên nhẫn, giảm động lực học tập, dễ bỏ cuộc. |
| **Đặc trưng Người nhận** | Toàn bộ các kênh | Học viên (đặc biệt là cán bộ công chức lớn tuổi) có kỹ năng công nghệ kém. | Rào cản nhận thức lớn, khó thao tác theo các tài liệu hướng dẫn thông thường. |

---

## 3. Các Lý thuyết Truyền thông Áp dụng vào Bài luận

### 3.1. Mô hình Shannon–Weaver (Mô hình tuyến tính)
* **Phân tích:** 
  * Quá trình gửi chỉ thị/hướng dẫn đăng ký từ EdTech Centre (Sender) qua Email/Website đến học viên (Receiver) gặp rất nhiều **Nhiễu (Noise) kỹ thuật** (giao diện khó nhìn thấy nút đăng ký, lỗi chức năng đăng nhập).
  * Trong giao tiếp nội bộ qua Zalo, nhiễu vật lý (tin nhắn trôi nhanh) làm gián đoạn việc truyền đạt thông điệp chính xác giữa chuyên viên và giảng viên/kỹ thuật viên.

### 3.2. Mô hình Truyền thông Giao dịch/Tương tác (Transactional/Interactive Model)
* **Phân tích:**
  * Mô hình này nhấn mạnh vào **vòng phản hồi (Feedback loop)** và **Trường kinh nghiệm (Field of Experience)**.
  * Hiện tại, phản hồi hỗ trợ qua Zalo OA và Form web bị chậm $\rightarrow$ làm đứt gãy vòng phản hồi, học viên cảm thấy không được tương tác trực tiếp.
  * Sự khác biệt lớn về "Trường kinh nghiệm công nghệ" giữa Đội ngũ phát triển (EdTech Centre - trình độ CNTT cao) và Học viên (kỹ năng công nghệ kém) dẫn đến việc biên soạn tài liệu hướng dẫn bị quá chuyên môn, khó hiểu đối với học viên.

### 3.3. Thuyết Phong phú Truyền thông (Media Richness Theory)
* **Phân tích:**
  * Việc giải quyết lỗi đăng nhập hoặc hướng dẫn sử dụng tính năng là những vấn đề có độ mơ hồ cao đối với người kém công nghệ. 
  * Nếu chỉ dùng kênh "nghèo nàn" (Lean Media) như văn bản chữ trên website hoặc form hỗ trợ sẽ không hiệu quả. Cần nâng cấp lên kênh "phong phú" (Rich Media) hơn như chatbot tương tác trực quan hoặc video mô phỏng thao tác ngắn.

### 3.4. Thuyết Tải nhận thức (Cognitive Load Theory)
* **Phân tích:**
  * Học viên có kỹ năng công nghệ kém sẽ chịu **Tải nhận thức ngoại lai (Extraneous Cognitive Load)** cực kỳ lớn nếu giao diện rườm rà (không tìm thấy nút đăng ký) hoặc thông điệp hướng dẫn không rõ ràng.
  * Cần thiết kế lại giao diện truyền thông và chuẩn hóa các thông điệp phản hồi để tối giản hóa tải nhận thức ngoại lai, giúp họ tập trung hoàn toàn vào việc học tập chuyên môn (**Germane Load**).

---

## 4. Giải pháp cải tiến đề xuất (02 Sản phẩm cụ thể)

### 4.1. Sản phẩm 1: Hệ thống Chatbot hỗ trợ tự động (Automated Support Chatbot)
* **Cơ sở lý thuyết:** Áp dụng *Interactive Model* để tạo vòng phản hồi ngay lập tức, và *Media Richness Theory* để cung cấp hướng dẫn dạng tương tác thay thế văn bản tĩnh.
* **Cách thực hiện:** Thu thập toàn bộ dữ liệu lịch sử chat hỗ trợ từ Facebook, Form web, Zalo OA trước đây $\rightarrow$ Phân loại các nhóm lỗi phổ biến (lỗi đăng nhập, tìm nút đăng ký, nộp bài) $\rightarrow$ Thiết lập kịch bản trả lời tự động thông minh bằng Chatbot để giải quyết 80% câu hỏi lặp lại của học viên.

### 4.2. Sản phẩm 2: Bộ Template Email mới trực quan (Visual Email Templates)
* **Cơ sở lý thuyết:** Áp dụng *Cognitive Load Theory* để giảm tải nhận thức ngoại lai.
* **Cách thực hiện:** Thiết kế lại toàn bộ hệ thống email thông báo tiến trình học, hướng dẫn mở tài khoản với định dạng trực quan (kèm hình vẽ hướng dẫn từng bước click chuột, ngôn từ tối giản hóa thuật ngữ kỹ thuật) phù hợp với người dùng kém công nghệ.
