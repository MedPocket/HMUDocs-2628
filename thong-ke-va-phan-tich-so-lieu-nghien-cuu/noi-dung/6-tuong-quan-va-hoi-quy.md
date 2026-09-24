# Chương 6: Phân Tích Tương Quan Và Hồi Quy Thống Kê

Chương này trình bày các phương pháp đánh giá mối liên hệ tuyến tính và xây dựng mô hình dự báo trong SPSS.

---

## 1. Phân Tích Tương Quan Tuyến Tính (Correlation)

### 1.1. Hệ số tương quan Pearson ($r$) và Spearman ($\rho$)
- **Pearson ($r$)**: Hai biến định lượng phân phối chuẩn.
- **Spearman ($\rho$)**: Biến phân phối không chuẩn hoặc biến thứ tự (Ordinal).

### 1.2. Mức độ tương quan
- $|r| < 0.3$: Tương quan yếu.
- $0.3 \le |r| < 0.5$: Tương quan trung bình.
- $0.5 \le |r| < 0.7$: Tương quan chặt chẽ.
- $|r| \ge 0.7$: Tương quan rất chặt chẽ.

Đường dẫn thực hiện lệnh:

```text
Analyze > Correlate > Bivariate...
```

---

## 2. Phân Tích Hồi Quy Tuyến Tính (Linear Regression)

Biểu diễn mối quan hệ phụ thuộc của biến phụ thuộc định lượng $Y$ theo các biến độc lập $X$:

$$Y = \beta_0 + \beta_1 X + \epsilon$$

Đường dẫn thực hiện lệnh:

```text
Analyze > Regression > Linear...
```

> **Các chỉ số chính trong Output:**
> - $R^2$ (`R Square`): Tỷ lệ phần trăm sự biến thiên của $Y$ được giải thích bởi mô hình $X$.
> - Bảng `Coefficients`: Hệ số $B$ (độ dốc) và giá trị $p$-value (`Sig.`).

---

## 3. Phân Tích Hồi Quy Logistic Nhị Phân (Binary Logistic Regression)

Ứng dụng cho biến đầu ra nhị phân ($0/1$: Mắc bệnh / Không mắc bệnh; Tử vong / Sống sót).

$$\text{logit}(P) = \ln\left(\frac{P}{1 - P}\right) = \beta_0 + \beta_1 X_1 + \beta_2 X_2 + \dots$$

Đường dẫn thực hiện lệnh:

```text
Analyze > Regression > Binary Logistic... > Options... > [x] CI for exp(B): 95%
```

> **Ý nghĩa của $\text{Exp}(B)$:**
> Lấy mũ $e^B = \text{Exp}(B)$ chính là chỉ số **Odds Ratio hiệu chỉnh ($\text{Adjusted OR}$)** đánh giá nguy cơ sau khi đã khống chế ảnh hưởng của các yếu tố nhiễu.

---

## Điều Hướng Bài Học

[< Chương Trước: Kiểm định tỷ lệ & biến định tính](5-kiem-dinh-ty-le-va-bien-dinh-tinh.md) | [Mục lục](0-muc-luc.md)
