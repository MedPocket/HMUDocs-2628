# Chương 6: Phân Tích Tương Quan Và Hồi Quy Thống Kê

Trong nghiên cứu khoa học, bên cạnh việc so sánh trung bình hay tỷ lệ, việc tìm hiểu mối liên hệ tuyến tính và xây dựng mô hình dự báo giữa các biến số đóng vai trò then chốt. Chương này trình bày hai công cụ phân tích nâng cao: **Phân tích tương quan (Correlation)** và **Phân tích hồi quy (Regression)**.

---

## 1. Phân Tích Tương Quan Tuyến Tính

Phân tích tương quan đánh giá mức độ chặt chẽ và chiều hướng mối liên hệ tuyến tính giữa hai biến định lượng.

### 1.1. Hệ số tương quan Pearson ($r$) và Spearman ($\rho$)
- **Hệ số tương quan Pearson ($r$)**: Áp dụng khi hai biến định lượng đều có **phân phối chuẩn**.
- **Hệ số tương quan Spearman ($\rho$)**: Áp dụng khi ít nhất một trong hai biến định lượng có **phân phối không chuẩn** hoặc là biến **thứ tự (Ordinal)**.

### 1.2. Giá trị và chiều hướng của Hệ số tương quan
Hệ số tương quan $r$ (hoặc $\rho$) luôn nằm trong khoảng từ $-1.0$ đến $+1.0$:
- **$r > 0$**: Tương quan thuận (biến $X$ tăng thì biến $Y$ tăng).
- **$r < 0$**: Tương quan nghịch (biến $X$ tăng thì biến $Y$ giảm).
- **$r = 0$**: Không có tương quan tuyến tính.

### Mức độ chặt chẽ của mối tương quan ($|r|$):
- $|r| < 0.3$: Tương quan yếu.
- $0.3 \le |r| < 0.5$: Tương quan trung bình.
- $0.5 \le |r| < 0.7$: Tương quan chặt chẽ.
- $|r| \ge 0.7$: Tương quan rất chặt chẽ.

### 1.3. Thao tác SPSS
1. Vào menu: `Analyze > Correlate > Bivariate...`
2. Chuyển hai biến định lượng (ví dụ: `tuoi` và `diem_hai_long`) vào ô **Variables**.
3. Tại mục **Correlation Coefficients**:
   - Tích chọn $\checkmark$ **Pearson** (nếu phân phối chuẩn).
   - Tích chọn $\checkmark$ **Spearman** (nếu phân phối không chuẩn).
4. Bấm **OK**.

```
[Thao tác SPSS]
Analyze -> Correlate -> Bivariate -> Variables: [tuoi, diem_hai_long]
-> [x] Pearson / [x] Spearman -> OK
```

---

## 2. Phân Tích Hồi Quy Tuyến Tính (Linear Regression)

Hồi quy tuyến tính biểu diễn mối quan hệ phụ thuộc giữa một biến phụ thuộc định lượng liên tục ($Y$) theo một hoặc nhiều biến độc lập ($X_1, X_2, \dots$).

### 2.1. Phương trình hồi quy tuyến tính đơn
$$Y = \beta_0 + \beta_1 X + \epsilon$$
Trong đó:
- $Y$: Biến phụ thuộc (biến đầu ra định lượng).
- $X$: Biến độc lập (yếu tố dự báo/dự đoán).
- $\beta_0$: Hằng số tự do (Giao điểm với trục tung Constant).
- $\beta_1$: Hệ số hồi quy góc (độ dốc). Thể hiện mức độ thay đổi của $Y$ khi $X$ tăng lên $1$ đơn vị.
- $\epsilon$: Sai số ngẫu nhiên.

### 2.2. Các chỉ số quan trọng trong kết quả SPSS
1. **Hệ số xác định $R^2$ (R Square)**: Cho biết tỷ lệ phần trăm sự biến thiên của $Y$ được giải thích bởi mô hình các biến độc lập $X$. (Ví dụ: $R^2 = 0.35 \rightarrow X$ giải thích được $35\%$ sự biến thiên của $Y$).
2. **Kiểm định ANOVA của mô hình**: Kiểm định giả thuyết xem toàn bộ mô hình hồi quy có ý nghĩa thống kê hay không ($p < 0.05$).
3. **Bảng Coefficients (Các hệ số)**:
   - Cột **B**: Giá trị hệ số hồi quy thực tế $\beta_0$ và $\beta_1$.
   - Cột **Sig.**: Giá trị $p$-value kiểm định ý nghĩa của từng hệ số $B$.

### 2.3. Thao tác SPSS
1. Vào menu: `Analyze > Regression > Linear...`
2. Đưa biến phụ thuộc định lượng vào **Dependent**.
3. Đưa biến độc lập vào **Independent(s)**.
4. Bấm **OK**.

```
[Thao tác SPSS]
Analyze -> Regression -> Linear -> Dependent: diem_hai_long -> Independent(s): tuoi -> OK
```

---

## 3. Phân Tích Hồi Quy Logistic Nhị Phân (Binary Logistic Regression)

Trong nghiên cứu y tế, biến kết cục quan tâm thường là biến nhị phân ($0/1$ hoặc $No/Yes$: Mắc bệnh / Không mắc bệnh; Tử vong / Sống sót; Hài lòng / Không hài lòng). Khi đó, hồi quy tuyến tính không còn phù hợp mà phải sử dụng **Hồi quy Logistic nhị phân**.

### 3.1. Phương trình Hồi quy Logistic
Hồi quy Logistic mô hình hóa xác suất xảy ra biến cố $P(Y = 1)$ thông qua hàm Logit:
$$\text{logit}(P) = \ln\left(\frac{P}{1 - P}\right) = \beta_0 + \beta_1 X_1 + \beta_2 X_2 + \dots + \beta_k X_k$$

Một đặc tính rất quan trọng của Hồi quy Logistic là khi lấy mũ thừa cơ số $e$ của hệ số hồi quy $B$, ta thu được ngay **Odds Ratio hiệu chỉnh (Adjusted Odds Ratio)**:
$$\text{Adjusted OR} = e^B = \text{Exp}(B)$$

### 3.2. Ưu điểm của Hồi quy Logistic đa biến
Hồi quy Logistic đa biến cho phép đánh giá tác động độc lập của một yếu tố nguy cơ lên bệnh lý sau khi đã **khống chế/hiệu chỉnh (control/adjust)** ảnh hưởng của các yếu tố nhiễu (Confounders) khác như Tuổi, Giới tính, Tiền sử gia đình...

### 3.3. Thao tác SPSS
1. Vào menu: `Analyze > Regression > Binary Logistic...`
2. Đưa biến phụ thuộc nhị phân ($0/1$) vào ô **Dependent**.
3. Đưa các biến độc lập (định lượng hoặc định tính) vào ô **Covariates**.
4. Nếu biến độc lập là biến định tính phân nhóm $\rightarrow$ Bấm **Categorical...**:
   - Đưa biến định tính vào **Categorical Covariates**.
   - Chọn nhóm tham chiếu (**Reference Category**): `First` hoặc `Last` $\rightarrow$ Bấm **Change** $\rightarrow$ **Continue**.
5. Bấm **Options...**: Tích chọn $\checkmark$ **CI for exp(B): 95%**.
6. Bấm **Continue** $\rightarrow$ **OK**.

```
[Thao tác SPSS]
Analyze -> Regression -> Binary Logistic -> Dependent: mac_benh_tang_ha
-> Covariates: [tuoi, bmi, bmi_group, hut_thuoc]
-> Categorical: [bmi_group, hut_thuoc] -> Options: [x] CI for exp(B): 95% -> OK
```

### 3.4. Đọc kết quả Output
Nhìn bảng **Variables in the Equation**:
- Cột **B**: Hệ số hồi quy Logistic.
- Cột **Sig.**: Giá trị $p$-value kiểm định ý nghĩa thống kê của biến độc lập.
- Cột **Exp(B)**: Tỷ số chênh Odds Ratio hiệu chỉnh ($\text{OR}_{\text{adjusted}}$).
- Cột **95% C.I. for EXP(B)**: Khoảng tin cậy 95% của OR hiệu chỉnh.

*Phiên giải ví dụ*: Bệnh nhân có hút thuốc lá có nguy cơ mắc bệnh tăng huyết áp cao gấp $2.85$ lần so với nhóm không hút thuốc sau khi đã hiệu chỉnh theo tuổi và chỉ số BMI ($\text{Adjusted OR} = 2.85$; $95\% \text{ CI}: 1.42 - 5.71$; $p = 0.003 < 0.05$).
