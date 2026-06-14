# 11. Phụ lục (Appendix)

## Phụ lục A. Sơ đồ hệ sinh thái truyền thông đề xuất tại daotao.ai

Dưới đây là sơ đồ chi tiết biểu diễn luồng truyền thông hỗ trợ học viên đa kênh sau cải tiến, minh họa cho mô hình lai (Hybrid System) kết hợp Chatbot AI tự động và chuyên viên hỗ trợ thủ công:

```mermaid
graph TD
    A[Học viên gặp lỗi kỹ thuật] --> B{Kênh tiếp nhận}
    B -- Truy cập daotao.ai --> C[Chatbot AI trợ giúp tự động]
    B -- Gửi liên hệ/Form/Zalo OA --> D[Chuyên viên EdTech Centre]
    
    C --> E{AI tự phân loại lỗi}
    E -- Lỗi đăng nhập/kích hoạt tài khoản --> F[Chatbot tự động hướng dẫn thao tác]
    E -- Lỗi phức tạp/ngoài kịch bản --> G[Hệ thống tự động chuyển tiếp Zalo OA/Fanpage]
    
    F --> H{Học viên phản hồi}
    H -- Đã giải quyết xong --> I[Đóng ticket & Đo lường CSAT tự động]
    H -- Vẫn chưa thực hiện được --> G
    
    G --> D
    D --> J[Chuyên viên hỗ trợ trực tiếp/Gọi điện]
    J --> I
```

---

## Phụ lục B. Kịch bản hội thoại phân nhánh chi tiết của Chatbot AI trên Website

Mô phỏng luồng kịch bản hội thoại (Dialogue Flow) của Chatbot AI khi tiếp cận học viên gặp sự cố đăng nhập trên daotao.ai:

```text
[Hệ thống]: Chào mừng bạn đến với daotao.ai! Tôi là Trợ lý ảo EdTech. Tôi có thể giúp gì cho bạn?
    ├── [Option 1: Tôi không đăng nhập được tài khoản]
    │     └── [Hệ thống]: Bạn đang đăng nhập bằng phương thức nào?
    │               ├── [Option 1.1: Đăng nhập bằng tài khoản nội bộ HUST]
    │               │     └── [Hệ thống]: Đối với sinh viên/giảng viên HUST, vui lòng sử dụng tài khoản email @hust.edu.vn và chọn đăng nhập qua cổng CAS của trường. 
    │               │           └── [Hệ thống]: Bạn đã đăng nhập được chưa? (Có / Chưa)
    │               └── [Option 1.2: Đăng nhập bằng tài khoản Đề án 06]
    │                     └── [Hệ thống]: Vui lòng kiểm tra email kích hoạt từ EdTech Centre. Bạn có nhận được mã kích hoạt tài khoản không?
    │                               ├── [Có, tôi có mã]: Nhập mã vào ô kích hoạt tại trang đăng nhập. Hướng dẫn chi tiết: [Xem tại đây]
    │                               └── [Không, tôi không nhận được]: Hãy cung cấp Email/Số điện thoại để tôi kiểm tra trạng thái trên hệ thống LMS.
    └── [Option 2: Tôi muốn đăng ký khóa học mới]
          └── [Hệ thống]: Bạn hãy di chuột lên góc phải màn hình, click vào nút màu cam "ĐĂNG KÝ NGAY". Hướng dẫn từng bước bằng hình ảnh tại đây: [Xem link]
```

---

## Phụ lục C. Bản phác thảo cấu trúc Email hướng dẫn kích hoạt tài khoản tối giản (CLT-oriented)

Bản phác thảo (Wireframe) của template email mới được thiết kế nhằm tối thiểu hóa tải nhận thức ngoại lai:

```text
+-----------------------------------------------------------------------+
|  [Logo Bách khoa Hà Nội - EdTech Centre]                              |
+-----------------------------------------------------------------------+
|  Chào anh/chị [Tên học viên],                                         |
|  Chúc mừng anh/chị đã tham gia lớp bồi dưỡng Đề án 06.                |
|  Để bắt đầu học tập ngay, anh/chị chỉ cần hoàn thành 3 bước sau:      |
|                                                                       |
|  [BƯỚC 1: NHẬN THÔNG TIN ĐĂNG NHẬP]                                    |
|  * Tài khoản: [Địa chỉ email của học viên]                            |
|  * Mật khẩu tạm thời: [Mật khẩu ngẫu nhiên]                           |
|                                                                       |
|  [BƯỚC 2: TRUY CẬP WEBSITE]                                           |
|  * Anh/chị click vào nút lớn bên dưới để mở trang học:                |
|    =========================================                          |
|    ||        NÚT: TRUY CẬP TRANG HỌC TẬP      || (Màu cam nổi bật)    |
|    =========================================                          |
|                                                                       |
|  [BƯỚC 3: ĐỔI MẬT KHẨU MỚI]                                           |
|  * Nhập mật khẩu tạm thời ở trên, sau đó hệ thống sẽ tự động hiện ra  |
|    ô nhập mật khẩu mới. Hãy nhập mật khẩu anh/chị dễ nhớ nhất.        |
|                                                                       |
|  * Lưu ý: Nếu gặp bất kỳ khó khăn nào, anh/chị chỉ cần bấm vào        |
|    biểu tượng Chatbox ở góc dưới bên phải màn hình daotao.ai để được  |
|    hỗ trợ tự động 24/7.                                               |
+-----------------------------------------------------------------------+
```

---

## Phụ lục D. Bảng phân tích chi tiết dữ liệu khảo sát CSAT định tính trước và sau cải tiến

Phân loại các phản hồi định tính của học viên Đề án 06 lớn tuổi qua các kênh Form phản hồi và Zalo OA:

| Kênh khảo sát | Nội dung phản hồi trước cải tiến (Email cũ & Hỗ trợ Zalo OA) | Nội dung phản hồi sau cải tiến (Email trực quan & Chatbot Website) |
| :--- | :--- | :--- |
| **Email hướng dẫn** | "Email quá dài, có nhiều từ chuyên ngành như 'LMS', 'SCORM' làm tôi không biết phải click vào đâu." (Học viên 52 tuổi) | "Email rất rõ ràng, có 3 bước lớn chữ to nên tôi đọc và tự làm theo được ngay." (Học viên 48 tuổi) |
| **Tốc độ phản hồi** | "Tôi gửi yêu cầu lấy lại mật khẩu từ sáng nhưng đến chiều muộn mới nhận được câu trả lời từ chuyên viên." (Học viên 45 tuổi) | "Hỏi chatbot trên web trả lời ngay lập tức, hướng dẫn đúng chỗ tôi đang bị kẹt nên tôi tự làm được." (Học viên 50 tuổi) |
| **Trải nghiệm sử dụng**| "Tìm mãi không thấy nút đăng ký ở đâu trên điện thoại vì giao diện quá nhiều chữ." (Học viên 55 tuổi) | "Tôi bấm vào hỗ trợ là chatbot chỉ ngay nút đăng ký màu cam ở góc màn hình, rất dễ tìm." (Học viên 53 tuổi) |
