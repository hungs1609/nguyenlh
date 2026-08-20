# SoLieu_ChongLung_BanThucNghiem.xlsx - B4_KiemDinh_ANCOVA

B4. KIỂM ĐỊNH GIẢ THUYẾT (sheet lõi)
H0: A=C trên kết quả · H1: A>C. So sánh t-test thô → change-score → ANCOVA kiểm soát nền.

① T-test thô & χ² (A vs C)
| Biến | A | C | Thống kê | p | Cohen d |
| :--- | :---: | :---: | :---: | :---: | :---: |
| Điểm cuối kỳ | 66,51 | 49,45 | t=7,17 | <0,001 | 1,20 |
| Hài lòng | 2,99 | 2,33 | t=4,91 | <0,001 | 0,82 |
| Cảm nhận tiến bộ | 3,54 | 3,15 | t=3,17 | 0,002 | 0,54 |
| Ý định học tiếp | 3,12 | 2,37 | t=5,48 | <0,001 | 0,92 |
| Bỏ học | 22,4% | 46,8% | χ²=9,72 | <0,001 | — |

② Change-score self-efficacy (hậu − tiền)
| | A | C | t | p | Cohen d |
| :--- | :---: | :---: | :---: | :---: | :---: |
| Δ self-efficacy | 0,10 | -0,07 | 2,27 | 0,025 | 0,38 |

③ ANCOVA #1 — DV: self_efficacy_post | covariate: self_efficacy_pre
| Nguồn | F | p | partial η² | TB hiệu chỉnh A | TB hiệu chỉnh C |
| :--- | :---: | :---: | :---: | :---: | :---: |
| group (A vs C) | 0,24 | 0,627 | 0,002 | 2,933 | 2,897 |
| covariate self_efficacy_pre | 591,58 | <0,001 | — | — | — |
Giả định: đồng nhất độ dốc p=0,654; Levene p=0,962 (đạt)

④ ANCOVA #2 — DV: final_grade | covariates: self_efficacy_pre + prior_knowledge + SRL
| Nguồn | F | p | partial η² |
| :--- | :---: | :---: | :---: |
| group (A vs C) | 1,59 | 0,209 | 0,011 |

KẾT LUẬN: t-test thô ủng hộ H1 trên mọi biến, NHƯNG sau khi ANCOVA kiểm soát nền, hiệu ứng nhóm lên self-efficacy biến mất (p=0,63; η²=0,002) và lên điểm không có ý nghĩa (p=0,21; η²=0,011).
Nghịch lý Lord: change-score có ý nghĩa (p=0,025) nhưng ANCOVA null → bằng chứng phụ thuộc phương pháp.
Diễn giải: khác biệt kết quả A–C chủ yếu do đặc điểm SẴN CÓ, không phải do "can thiệp". Không kết luận nhân quả.