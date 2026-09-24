# Giáo Trình Thống Kê Và Phân Tích Số Liệu Nghiên Cứu Bằng SPSS

> Tài liệu hướng dẫn thực hành và lý thuyết thống kê ứng dụng trong nghiên cứu Y - Dược học và Quản lý
> Tổng hợp và chuẩn hóa theo chương trình giảng dạy Thống kê Y học - Tin học ứng dụng và Giáo trình Phân tích Thống kê Cơ bản trong Quản lý bằng SPSS.

---

## Mục Mục Toàn Bộ Giáo Trình

### [Chương 1: Tổng quan về SPSS và Quản lý Nhập dữ liệu Nghiên cứu](1-tong-quan-va-nhap-lieu-spss.md)
1. Tổng quan về SPSS Statistics trong nghiên cứu khoa học
2. Giao diện làm việc của SPSS: Data View và Variable View
3. Định nghĩa các thuộc tính biến số trong Variable View (Name, Type, Width, Decimals, Label, Values, Missing, Columns, Align, Measure, Role)
4. Quy trình khai báo bộ biến số và nhập dữ liệu nghiên cứu
5. Nhập dữ liệu từ các nguồn bên ngoài (Excel, CSV, Stata)

---

### [Chương 2: Quản lý và Biến đổi Dữ liệu trong SPSS](2-quan-ly-va-bien-doi-du-lieu.md)
1. Lọc và chọn lọc bản ghi nghiên cứu: Lệnh Data > Select Cases
2. Sắp xếp dữ liệu: Lệnh Data > Sort Cases
3. Tạo biến mới dựa trên công thức toán học: Lệnh Transform > Compute Variable (Tính BMI, tính tuổi từ ngày sinh, tính điểm tổng...)
4. Mã hóa và phân nhóm biến số: Lệnh Transform > Recode into Different Variables & Recode into Same Variables
5. Tách và ghép file dữ liệu: Data > Split File, Data > Merge Files (Add Cases / Add Variables)

---

### [Chương 3: Thống kê Mô tả và Trình bày Dữ liệu Nghiên cứu](3-thong-ke-mo-ta-va-trinh-bay-du-lieu.md)
1. Phân loại biến số: Biến định tính (Nominal, Ordinal) và Biến định lượng (Continuous, Discrete)
2. Thống kê mô tả biến định tính: Tần số (Frequency), Tỷ lệ % (Percent, Valid Percent), Vẽ biểu đồ Cột (Bar chart) & Hình tròn (Pie chart)
3. Thống kê mô tả biến định lượng:
   - Khảo sát phân phối chuẩn (Góc độ lý thuyết, Skewness, Kurtosis, kiểm định Kolmogorov-Smirnov / Shapiro-Wilk)
   - Báo cáo phân phối chuẩn: Giá trị trung bình (Mean), Độ lệch chuẩn (SD)
   - Báo cáo phân phối không chuẩn: Trung vị (Median), Khoảng tứ phân vị (IQR), Min - Max
   - Biểu đồ mô tả: Histogram, Boxplot
4. Mô tả mối quan hệ giữa 2 biến số:
   - Biến định tính x Biến định tính: Lệnh Crosstabs, Bảng 2x2 & n xm, Biểu đồ Stacked Bar
   - Biến định tính x Biến định lượng: Lệnh Case Summaries, Biểu đồ Boxplot theo nhóm
   - Hai biến định lượng: Hệ số tương quan, Biểu đồ phân tán Scatterplot

---

### [Chương 4: Kiểm định Giả thuyết về Giá trị Trung bình](4-kiem-dinh-gia-thiet-trung-binh.md)
1. Cơ sở lý thuyết kiểm định giả thuyết thống kê: Giả thuyết H0, Ha, Mức ý nghĩa alpha, Giá trị p-value
2. Kiểm định giả thuyết cho 1 giá trị trung bình: One-Sample T-Test
3. Kiểm định so sánh 2 giá trị trung bình độc lập: Independent-Samples T-Test
   - Đọc và giải thích kiểm định bình đẳng phương sai Levene (Levene's Test for Equality of Variances)
   - Đọc kết quả p-value trong 2 trường hợp: Equal variances assumed & Equal variances not assumed
4. Kiểm định so sánh 2 giá trị trung bình ghép cặp: Paired-Samples T-Test (Trước - Sau can thiệp)
5. Kiểm định so sánh nhiều giá trị trung bình (ANOVA 1 yếu tố): One-Way ANOVA
   - Kiểm định đồng nhất phương sai (Homogeneity of Variance)
   - So sánh bội cặp Post-Hoc (LSD, Bonferroni, Tukey, Games-Howell)

---

### [Chương 5: Kiểm định Giả thuyết cho Biến Định tính và Tỷ lệ](5-kiem-dinh-ty-le-va-bien-dinh-tinh.md)
1. Kiểm định giả thuyết cho 1 giá trị tỷ lệ: Kiểm định nhị thức Binomial Test
2. Kiểm định mối liên quan giữa 2 biến định tính độc lập: Chi-Square Test (Chi bình phương)
   - Bảng 2x2: Đọc kết quả Pearson Chi-Square, Continuity Correction, hoặc Fisher's Exact Test
   - Bảng n xm: Điều kiện số ô có tần số kỳ vọng (Expected Count) < 5 không vượt quá 20%
3. Đánh giá mức độ liên quan và nguy cơ:
   - Tỷ số chênh (Odds Ratio - OR) và Nguy cơ tương đối (Relative Risk - RR)
   - Khoảng tin cậy 95% (95% CI)
4. Kiểm định giả thuyết cho 2 tỷ lệ ghép cặp: Kiểm định McNemar Test

---

### [Chương 6: Phân tích Tương quan và Hồi quy Thống kê](6-tuong-quan-va-hoi-quy.md)
1. Phân tích tương quan tuyến tính:
   - Hệ số tương quan Pearson (r) cho biến phân phối chuẩn
   - Hệ số tương quan Spearman (rho) cho biến phân phối không chuẩn / thứ tự
   - Đánh giá chiều hướng và độ mạnh của mối tương quan
2. Phân tích hồi quy tuyến tính đơn và bội (Linear Regression):
   - Dạng phương trình hồi quy: Y = beta_0 + beta_1 * X + epsilon
   - Hệ số xác định R^2, kiểm định ANOVA mô hình, đọc hệ số B, giá trị p và khoảng tin cậy 95%
3. Phân tích hồi quy Logistic nhị phân (Binary Logistic Regression):
   - Ứng dụng trong phân tích yếu tố nguy cơ với biến đầu ra nhị phân (0/1)
   - Đọc hệ số B, hệ số Exp(B) (Odds Ratio hiệu chỉnh - Adjusted OR) và giá trị p

---

## Nguồn Dữ Liệu Thực Hành & Đề Cương Ôn Tập

- Bộ số liệu ví dụ bao gồm: ungthu.sav, daithaoduong.sav, dieutriyhct.sav, staff-satisfaction.sav, so-lieu-nghien-cuu-tang-huyet-ap.sav.
- Tham khảo các câu hỏi ôn tập thi lý thuyết và thực hành SPSS dành cho sinh viên và học viên Chuyên khoa 1 (CK1) Y Dược.
