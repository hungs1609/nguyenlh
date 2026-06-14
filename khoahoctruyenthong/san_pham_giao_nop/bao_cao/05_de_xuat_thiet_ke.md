# 5. Thiết kế lại hệ thống truyền thông

Để khắc phục các điểm đứt gãy và rào cản truyền thông đã phân tích, chương này đề xuất giải pháp thiết kế lại hệ thống truyền thông tích hợp tại Trung tâm Công nghệ Giáo dục (daotao.ai). Trọng tâm cải tiến hướng tới việc tối ưu hóa hiệu suất truyền tin nội bộ và chuyển dịch các kênh giao tiếp với học viên theo mô hình tương tác lấy người học làm trung tâm.

## 5.1. Chiến lược truyền thông tích hợp mới

Chiến lược truyền thông mới phân tách rõ ràng vai trò của từng kênh truyền thông theo thuyết phong phú truyền thông:
*   Website daotao.ai: Được định vị là kênh truyền tải chính có độ phong phú cao nhờ tích hợp chatbot tự động và tối ưu hóa giao diện bằng cách đưa nút đăng ký ra màn hình chủ, bổ sung hướng dẫn thao tác nhanh.
*   Hệ thống email tự động: Đóng vai trò là kênh chỉ thị được tinh giản tối đa cấu trúc thông tin để giảm tải nhận thức ngoại lai cho học viên lớn tuổi.
*   Trang Zalo và Facebook Fanpage: Chuyển đổi công năng từ tiếp nhận đại trà sang kênh hỗ trợ chuyên sâu để giải quyết các ca phức tạp không thể tự động hóa, đòi hỏi sự can thiệp trực tiếp của chuyên viên.

## 5.2. Tích hợp chatbot tự động trên website

Để tối ưu hóa vòng phản hồi và giảm tải công việc hỗ trợ thủ công, hệ thống chatbot tương tác được phát triển dựa trên dữ liệu hội thoại lịch sử và tích hợp trực tiếp ở góc phải giao diện website daotao.ai.

### 5.2.1. Kịch bản phân nhánh của chatbot

Chatbot được lập trình phân luồng xử lý thông tin dựa trên các nhóm câu hỏi lặp lại phổ biến nhất của học viên:

```mermaid
graph TD
    Start[Học viên nhấp vào Chatbot] --> Greeting[Chatbot hiển thị lời chào & Menu chính]
    Greeting --> Opt1[1. Hướng dẫn đăng ký khóa học]
    Greeting --> Opt2[2. Khắc phục lỗi đăng nhập]
    Greeting --> Opt3[3. Hỗ trợ kỹ thuật khác / Gặp chuyên viên]

    Opt1 --> Answer1[Hiển thị ảnh GIF minh họa nút đăng ký và 3 bước thực hiện ngắn gọn]
    
    Opt2 --> SubMenu{Lớp học Đề án 06 hay Tự do?}
    SubMenu --> SubOpt1[Lớp Đề án 06]
    SubMenu --> SubOpt2[Tài khoản Tự do]
    
    SubOpt1 --> Answer2A[Username: Số CCCD<br>Mật khẩu mặc định: Daotao@123<br>Click nút bên dưới để đối soát danh sách CCCD nếu báo lỗi]
    SubOpt2 --> Answer2B[Nhấp chọn 'Quên mật khẩu' để nhận lại mã xác thực qua Email]
    
    Opt3 --> Answer3[Chuyển tiếp hội thoại kèm toàn bộ lịch sử chat sang Chuyên viên trực ban]
```

### 5.2.2. Kịch bản hội thoại mẫu
*   Học viên: "Tôi không biết cách đăng nhập để vào học."
*   Chatbot (Phản hồi sau 1 giây):
    > "Xin chào Anh/Chị! Để đăng nhập nhanh nhất vào lớp học Chuyển đổi số (Đề án 06), vui lòng áp dụng thông tin sau:
    > *   Tên đăng nhập (Username): Nhập chính xác số căn cước công dân của Anh/Chị.
    > *   Mật khẩu mặc định: Daotao@123 (Lưu ý chữ D viết hoa).
    >
    > Nếu hệ thống báo lỗi 'Tài khoản không tồn tại', rất có thể số căn cước công dân trong danh sách đăng ký ban đầu của đơn vị bị sai lệch. Anh/Chị vui lòng nhấp vào nút Yêu cầu đối soát CCCD bên dưới để chuyên viên kiểm tra và sửa đổi."

## 5.3. Mẫu email hướng dẫn trực quan

Thiết kế lại hệ thống email thông báo để giảm thiểu tải nhận thức ngoại lai dựa trên thuyết tải nhận thức. Email mới loại bỏ các văn bản kỹ thuật dài dòng, thay thế bằng định dạng tối giản, cấu trúc phân cấp thông tin rõ ràng và có các chỉ dẫn thị giác.

*   Tiêu đề Email: `[daotao.ai] Hướng dẫn kích hoạt tài khoản học tập Đề án 06 (Chỉ với 3 bước)`
*   Khung nội dung:
    > Kính gửi Anh/Chị học viên,
    >
    > Để bắt đầu khóa học trên nền tảng daotao.ai, Anh/Chị vui lòng thực hiện 3 bước kích hoạt tài khoản đơn giản sau đây:
    >
    > * BƯỚC 1: Truy cập trang học tập
    >   * Nhấp chuột vào đường dẫn: https://daotao.ai/login
    >
    > * BƯỚC 2: Nhập thông tin đăng nhập
    >   * Tên đăng nhập (Username): [Điền Số căn cước công dân của Anh/Chị]
    >   * Mật khẩu mặc định: Daotao@123 (Lưu ý chữ D viết hoa).
    >
    > * BƯỚC 3: Đổi mật khẩu mới
    >   * Ngay sau khi đăng nhập thành công, hệ thống sẽ yêu cầu Anh/Chị đặt mật khẩu mới dễ nhớ của riêng mình để bảo mật thông tin.
    >
    > (Có kèm hình ảnh minh họa chụp màn hình thực tế, khoanh tròn đỏ vị trí điền thông tin đăng nhập)
    >
    > ---
    > Cần hỗ trợ ngay? Anh/Chị chỉ cần sử dụng tính năng Chatbot Trợ lý học tập tích hợp sẵn ở góc dưới bên phải website daotao.ai để được hỗ trợ 24/7.
    >
    > Trung tâm Công nghệ Giáo dục, Đại học Bách khoa Hà Nội

## 5.4. Quy trình truyền thông nội bộ

Để giải quyết vấn đề trôi tin nhắn và hiểu sai thông số kỹ thuật trên nhóm chat Zalo, Trung tâm Công nghệ Giáo dục thực hiện các cải tiến giao tiếp nội bộ:
1.  Chuyển đổi công cụ: Thay thế việc bàn giao yêu cầu kỹ thuật qua nhóm chat bằng việc sử dụng một bảng Kanban quản trị công việc chung trên hệ thống dùng chung được phân quyền.
2.  Chuẩn hóa thông điệp phối hợp: Quy định giảng viên và chuyên viên khi bàn giao học liệu bắt buộc phải điền đầy đủ thông tin theo biểu mẫu chuẩn:
    *   Mã khóa học và tên bài giảng
    *   Yêu cầu định dạng bài giảng (học liệu chuẩn SCORM hoặc video MP4 nén H.264)
    *   Độ phân giải yêu cầu (1080p)
    *   Người chịu trách nhiệm duyệt nội dung
3.  Quy trình phê duyệt: Mọi thay đổi kỹ thuật chỉ được kích hoạt khi trạng thái công việc trên bảng quản trị chuyển sang "Đã duyệt" bởi người có thẩm quyền, loại bỏ hoàn toàn các thông báo bằng lời nói hoặc tin nhắn chat tự phát.
