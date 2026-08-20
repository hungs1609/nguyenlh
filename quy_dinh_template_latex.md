# Quy định Kỹ thuật và Hướng dẫn Sử dụng Template LaTeX Báo cáo

Tài liệu này quy định bộ khung kỹ thuật (formatting & structural framework) cho các tài liệu báo cáo, bài luận, đồ án được biên soạn bằng LaTeX. 

> [!NOTE]
> **Lưu ý quan trọng:** Template này **không quy định cứng** nội dung báo cáo phải gồm những chương hay mục nào. Đây là bộ khung trình bày chuẩn mực về mặt kỹ thuật (geometry, typography, trang bìa, mục lục, trích dẫn), giúp người dùng dễ dàng tái sử dụng cho các dự án báo cáo khác nhau.

---

## 1. Cấu trúc Thư mục và Quản lý File Mô-đun

Để quản lý mã nguồn LaTeX sạch sẽ và dễ bảo trì, dự án áp dụng mô hình phân tách mô-đun (modular setup). Tất cả các phần của báo cáo được tách thành từng file `.tex` riêng biệt và nạp vào file chính qua lệnh `\input{...}`.

```text
latex/
├── main.tex                    # File cấu hình chính (Preamble & luồng tài liệu)
├── trang_bia.tex               # Trang bìa chuẩn của báo cáo
├── 01_abstract.tex             # File thành phần (ví dụ: Tóm tắt)
├── 02_mo_dau.tex               # File thành phần (ví dụ: Mở đầu)
├── 03_muc_tieu_nghien_cuu.tex  # File thành phần (các chương nội dung)
├── ...                         # Các file chương/mục nội dung khác
├── 07_tai_lieu_tham_khao.tex   # File thành phần (Danh mục tài liệu tham khảo)
└── quy_dinh_template_latex.md  # Tài liệu quy định & hướng dẫn sử dụng (file này)
```

---

## 2. Quy chuẩn Định dạng Trang và Font chữ (Preamble Configuration)

Các thông số kỹ thuật dưới đây được thiết lập sẵn trong `main.tex`:

### 2.1 Class và Mã hóa Ngôn ngữ
```latex
\documentclass[12pt]{article}
\usepackage[T5]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage[vietnamese]{babel}
\shorthandoff{"}
```
* **Font encoding `T5` & `utf8`**: Đảm bảo hiển thị đầy đủ ký tự tiếng Việt có dấu.
* **`babel` [vietnamese]**: Hỗ trợ ngắt từ và nhãn tiếng Việt.
* **`\shorthandoff{"}`**: Vô hiệu hóa tính năng nháy kép đặc thù của `babel` tiếng Việt để tránh xung đột cú pháp với các gói vẽ hình `tikz` hoặc chèn liên kết `hyperref`.

### 2.2 Typography (Font chữ & Cỡ chữ)
```latex
\usepackage[fontsize=13pt]{scrextend}
\usepackage{mathptmx}
```
* **Font chính**: `mathptmx` (định dạng chuẩn kiểu Times New Roman cho văn bản và công thức toán).
* **Cỡ chữ tiêu chuẩn**: `13pt` (được cấu hình qua gói `scrextend`).

### 2.3 Cấu hình Lề trang (Page Geometry)
```latex
\usepackage[top=2.5cm,bottom=2.5cm,left=3.5cm,right=2.0cm]{geometry}
```
* **Lề trên (Top)**: `2.5 cm`
* **Lề dưới (Bottom)**: `2.5 cm`
* **Lề trái (Left)**: `3.5 cm` (dành khoảng trống chuẩn cho việc gáy tập/đóng bìa)
* **Lề phải (Right)**: `2.0 cm`

### 2.4 Giãn dòng và Thụt đầu dòng (Spacing & Indentation)
```latex
\usepackage{setspace}
\setstretch{1.5}
\usepackage{indentfirst}
```
* **Giãn dòng**: `1.5` (`\setstretch{1.5}`).
* **Thụt đầu dòng**: `indentfirst` đảm bảo đoạn văn ngay sau tiêu đề section vẫn được thụt đầu dòng theo đúng quy chuẩn văn bản tiếng Việt.

### 2.5 Header, Footer và Đánh số trang
```latex
\usepackage{fancyhdr}
\pagestyle{fancy}
\fancyhf{}
\fancyfoot[R]{\thepage}
\renewcommand{\headrulewidth}{0pt}
\renewcommand{\footrulewidth}{0pt}
```
* **Vị trí số trang**: Góc dưới bên phải (`\fancyfoot[R]{\thepage}`).
* **Đường kẻ ngang**: Ẩn đường kẻ ở cả header và footer (`headrulewidth` và `footrulewidth` bằng `0pt`).
* **Đánh số trang**: Bắt đầu đánh số dạng chữ số Ả Rập (`1, 2, 3...`) từ trang ngay sau bìa:
  ```latex
  \newpage
  \pagenumbering{arabic}
  \setcounter{page}{1}
  ```

### 2.6 Đồ họa và Liên kết
* `graphicx`: Chèn hình ảnh (`.png`, `.jpg`, `.pdf`).
* `tikz`: Vẽ sơ đồ, đồ thị và vẽ viền trang bìa (`\usetikzlibrary{calc,shapes.geometric,arrows}`).
* `hyperref`: Chèn liên kết web/nội bộ với tùy chọn `[hidelinks]` để không hiển thị khung màu quanh link khi xuất ra PDF:
  ```latex
  \usepackage{url}
  \usepackage[hidelinks]{hyperref}
  ```

---

## 3. Quy chuẩn Thiết kế Trang Bìa (`trang_bia.tex`)

Trang bìa được xây dựng độc lập trong môi trường `titlepage` với các quy chuẩn về kích thước font và bố cục như sau:

### 3.1 Viền bìa tự động (TikZ Overlay Border)
Khung viền bìa đơn mảnh (bề dày `1.5pt`), tự động căn chỉnh lùi vào từ lề giấy:
```latex
\begin{tikzpicture}[overlay,remember picture]
    \draw [line width=1.5pt] ($ (current page.north west) + (3cm,-2cm) $) rectangle ($ (current page.south east) + (-2cm,1.5cm) $);
\end{tikzpicture}
```

### 3.2 Bố cục và Font chữ trên Trang Bìa
1. **Tên Cơ quan / Trường**: Căn giữa, cỡ `14pt`, in đậm, IN HOA (`{\fontsize{14}{16}\selectfont\textbf{ĐẠI HỌC BÁCH KHOA HÀ NỘI}\\}`).
2. **Tên Khoa / Viện**: Căn giữa, cỡ `12pt`, in đậm, IN HOA (`{\fontsize{12}{14}\selectfont\textbf{KHOA KHOA HỌC VÀ CÔNG NGHỆ GIÁO DỤC}\\}`).
3. **Khoảng cách**: `\vspace{1.5cm}`.
4. **Logo Trường**: Chiều cao `4.5 cm` (`\includegraphics[height=4.5cm]{hust_logo.png}`).
5. **Khoảng cách**: `\vspace{1.5cm}`.
6. **Loại hình tài liệu**: Cỡ `16pt`, in đậm, màu đỏ (`{\fontsize{16}{18}\selectfont\textbf{\color{red}BÁO CÁO BÀI LUẬN}\\}`).
7. **Khoảng cách**: `\vspace{0.8cm}`.
8. **Tên đề tài / Báo cáo**: Cỡ `14pt`, in đậm, căn giữa (`{\fontsize{14}{18}\selectfont\textbf{...}\\}`).
9. **Đường kẻ phân cách**: `\vspace{0.4cm}\noindent\rule{0.65\textwidth}{0.6pt}\vspace{0.6cm}`.
10. **Tên Học phần**: Cỡ `12pt`, in nghiêng + in đậm (`{\fontsize{12}{14}\selectfont\textit{\textbf{Học phần:} ...}\\}`).
11. **Khoảng cách**: `\vspace{2.0cm}`.
12. **Khối thông tin Học viên & Giảng viên**: Căn trái (`flushleft`), lùi lề `2.5 cm`, sử dụng môi trường `tabular{ll}`.
13. **Chân trang**: Khoảng trống co giãn `\vfill`, địa điểm – năm xuất bản cỡ `12pt` in đậm (`{\fontsize{12}{14}\selectfont\textbf{Hà Nội – 2026}\\}\vspace*{0.4cm}`).

---

## 4. Quy chuẩn Mục lục và Đánh số Section

### 4.1 Tạo Mục lục (Table of Contents)
```latex
\renewcommand{\contentsname}{Mục lục}
\tableofcontents
\newpage
```

### 4.2 Xử lý Các phần Tiền đề (Abstract, Lời mở đầu...)
Với các phần tiền đề không muốn tăng chỉ số chương chính thức, sử dụng tiêu đề không đánh số `\section*{...}` và thêm thủ công vào Mục lục:
```latex
\section*{1. Tóm tắt}
\addcontentsline{toc}{section}{1. Tóm tắt}
```

### 4.3 Quản lý Chỉ số Section cho Các chương chính
Để tự động điều chỉnh số thứ tự section giữa phần tiền đề và các chương chính, thiết lập lại bộ đếm:
```latex
\setcounter{section}{1} % Để chương tiếp theo tự động đánh số bắt đầu từ 2 (hoặc số mong muốn)
```

---

## 5. Quy chuẩn Trích dẫn và Tài liệu Tham khảo

### 5.1 Cấu hình Gói trích dẫn (`natbib`)
```latex
\usepackage[round]{natbib}
\newcommand{\parencite}{\citep} % Alias tương thích cú pháp biblatex
```

### 5.2 Trình bày File `07_tai_lieu_tham_khao.tex`
```latex
\renewcommand{\refname}{7. Tài liệu tham khảo}
\addcontentsline{toc}{section}{7. Tài liệu tham khảo}

\begin{thebibliography}{9}
\bibitem[Anderson \& Krathwohl(2001)]{anderson2001}
Anderson, L. W., \& Krathwohl, D. R. (Eds.). (2001). \textit{A taxonomy for learning, teaching, and assessing: A revision of Bloom's taxonomy of educational objectives}. Longman.
\end{thebibliography}
```

---

## 6. Hướng dẫn Quy trình Tái sử dụng Template cho Báo cáo Mới

1. Sao chép thư mục template sang dự án mới.
2. Cập nhật các trường thông tin trên `trang_bia.tex`.
3. Tạo/Chỉnh sửa các file nội dung `.tex` thành phần.
4. Cập nhật danh sách `\input{...}` trong `main.tex`.
5. Cập nhật danh mục `\bibitem` trong file tài liệu tham khảo.
6. Biên dịch bằng XeLaTeX / PDFLaTeX.

---

## 7. Mã nguồn Mẫu Hoàn chỉnh (Complete Skeleton Source Code)

Dưới đây là mã nguồn đầy đủ 100% của 2 file cốt lõi (`main.tex` và `trang_bia.tex`) để có thể tái tạo chính xác tuyệt đối hình thức của tài liệu gốc mà không cần tham chiếu file ngoại vi khác:

### 7.1 File `main.tex` hoàn chỉnh
```latex
\documentclass[12pt]{article}
\usepackage[T5]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage[vietnamese]{babel}
\shorthandoff{"}
\usepackage[fontsize=13pt]{scrextend}
\usepackage{mathptmx}
\usepackage[top=2.5cm,bottom=2.5cm,left=3.5cm,right=2.0cm]{geometry}
\usepackage{setspace}
\setstretch{1.5}
\usepackage{indentfirst}
\usepackage{fancyhdr}
\usepackage{graphicx}
\usepackage{xcolor}
\usepackage{tikz}
\usetikzlibrary{calc,shapes.geometric,arrows}
\usepackage{url}
\usepackage[hidelinks]{hyperref}

% Cấu hình đánh số trang ở góc dưới bên phải
\pagestyle{fancy}
\fancyhf{}
\fancyfoot[R]{\thepage}
\renewcommand{\headrulewidth}{0pt}
\renewcommand{\footrulewidth}{0pt}

% Cấu hình trích dẫn theo chuẩn APA bằng natbib
\usepackage[round]{natbib}
\newcommand{\parencite}{\citep}

\begin{document}

% Trang bìa
\input{trang_bia}

\newpage
\pagenumbering{arabic}
\setcounter{page}{1}

% Phần tiền đề (Abstract)
\input{01_abstract}
\addcontentsline{toc}{section}{1. Tóm tắt}
\newpage

% Trang mục lục
\renewcommand{\contentsname}{Mục lục}
\tableofcontents
\newpage

\setcounter{section}{1} % Để chương tiếp theo tự động đánh số 2
% Các chương nội dung chính (ví dụ)
\input{02_mo_dau}
\newpage

\input{03_muc_tieu_nghien_cuu}
\newpage

\input{04_co_so_ly_thuyet}
\newpage

\input{05_thiet_ke_san_pham}
\newpage

\input{06_ket_luan}
\newpage

% Tài liệu tham khảo
\input{07_tai_lieu_tham_khao}
\newpage

\end{document}
```

### 7.2 File `trang_bia.tex` hoàn chỉnh
```latex
\begin{titlepage}
    % Khung viền đơn mảnh bám theo lề giấy 
    \begin{tikzpicture}[overlay,remember picture]
        \draw [line width=1.5pt] ($ (current page.north west) + (3cm,-2cm) $) rectangle ($ (current page.south east) + (-2cm,1.5cm) $);
    \end{tikzpicture}
    
    \centering
    
    % Tên Trường & Khoa chủ quản
    {\fontsize{14}{16}\selectfont\textbf{ĐẠI HỌC BÁCH KHOA HÀ NỘI}\\} 
    {\fontsize{12}{14}\selectfont\textbf{KHOA KHOA HỌC VÀ CÔNG NGHỆ GIÁO DỤC}\\} 
    
    \vspace{1.5cm}
    
    % Khối định vị LOGO Trường
    \includegraphics[height=4.5cm]{hust_logo.png}
    
    \vspace{1.5cm}
    
    % Loại hình tài liệu (Màu đỏ, in hoa đậm)
    {\fontsize{16}{18}\selectfont\textbf{\color{red}BÁO CÁO BÀI LUẬN}\\} 
    
    \vspace{0.8cm}
    
    % Tên đề tài/báo cáo phân tích
    {\fontsize{14}{18}\selectfont\textbf{TÊN ĐỀ TÀI BÁO CÁO BAO GỒM CÁC DÒNG\\ TIÊU ĐỀ ĐƯỢC NGẮT DÒNG HỢP LÝ}\\} 
    
    \vspace{0.4cm}
    \noindent\rule{0.65\textwidth}{0.6pt} % Đường kẻ ngang phân cách tiêu đề
    \vspace{0.6cm}
    
    % Tên Học phần tương ứng
    {\fontsize{12}{14}\selectfont\textit{\textbf{Học phần:} Tên Học Phần Tương Ứng}\\} 
    
    \vspace{2.0cm}
    
    % Khối thông tin Học viên & Giảng viên hướng dẫn
    \begin{flushleft}
        \hspace{2.5cm} 
        \begin{tabular}{ll}
            \fontsize{12}{14}\selectfont\textbf{Học viên thực hiện:} & \fontsize{12}{14}\selectfont Họ và Tên - Mã số sinh viên \\
            \fontsize{12}{14}\selectfont\textbf{Giảng viên hướng dẫn:} & \fontsize{12}{14}\selectfont TS. Nguyễn Văn A
        \end{tabular}
    \end{flushleft}
    
    \vfill
    
    % Địa điểm và thời gian xuất bản ở cuối trang
    {\fontsize{12}{14}\selectfont\textbf{Hà Nội – 2026}\\}
    \vspace*{0.4cm}
    
\end{titlepage}
```
