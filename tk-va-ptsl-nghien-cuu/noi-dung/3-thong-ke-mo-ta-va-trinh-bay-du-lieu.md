# Chương 3: Thống Kê Mô Tả Và Trình Bày Dữ Liệu Nghiên Cứu

Thống kê mô tả (Descriptive Statistics) tóm tắt, mô tả và trình bày các đặc tính cơ bản của bộ dữ liệu nghiên cứu thông qua bảng biểu, các số đo đại diện và biểu đồ trực quan.

---

## 1. Phân Loại Biến Số Trong Nghiên Cứu

- **Biến định tính (Categorical)**:
  - *Danh nghĩa (Nominal)*: Giới tính, Nhóm máu, Tỉnh thành.
  - *Thứ tự (Ordinal)*: Giai đoạn ung thư, Mức độ đau (Nhẹ < Vừa < Nặng).
- **Biến định lượng (Quantitative)**:
  - *Rời rạc (Discrete)*: Số con, Số ngày nằm viện.
  - *Liên tục (Continuous)*: Tuổi, Cân nặng, Huyết áp tâm thu.

---

## 2. Thống Kê Mô Tả Biến Định Tính

![Frequencies Output](_images/img-3-thong-ke-1.png)

### 2.1. Chỉ số báo cáo
- Tần số ($n$): Số lượng quan sát ở từng biểu hiện.
- Tỷ lệ phần trăm ($\%$): Báo cáo giá trị `Valid Percent` (tỷ lệ trên các bản ghi hợp lệ sau khi loại trừ missing).

### 2.2. Lệnh SPSS
```text
Analyze > Descriptive Statistics > Frequencies...
```
> **Thao tác vẽ biểu đồ:** Trong cửa sổ `Frequencies`, bấm `Charts...` -> Chọn `Bar charts` hoặc `Pie charts` -> Chọn `Percentages` -> Bấm `OK`.

---

## 3. Thống Kê Mô Tả Biến Định Lượng Và Khảo Sát Phân Phối Chuẩn

Để báo cáo biến định lượng chuẩn xác, bắt buộc phải khảo sát xem biến số có tuân theo **Phân phối chuẩn (Normal Distribution)** hay không.

![Histogram Output](_images/img-3-thong-ke-2.png)

### 3.1. Các tiêu chí đánh giá phân phối chuẩn
1. **Chỉ số thống kê**: `Mean` và `Median` xấp xỉ bằng nhau; `Skewness` và `Kurtosis` nằm trong khoảng $[-1.0, +1.0]$.
2. **Biểu đồ**: Histogram có dạng hình chuông đối xứng.
3. **Kiểm định giả thuyết**: Kiểm định Kolmogorov-Smirnov ($N \ge 50$) hoặc Shapiro-Wilk ($N < 50$).
   - Nếu $p > 0.05$: Biến có phân phối chuẩn.
   - Nếu $p \le 0.05$: Biến có phân phối không chuẩn.

### 3.2. Quy tắc trình bày chỉ số thống kê trong báo cáo y học

| Phân phối dữ liệu | Chỉ số tập trung | Chỉ số phân tán | Trình bày chuẩn bài báo khoa học |
| :--- | :--- | :--- | :--- |
| **Phân phối Chuẩn** | Trung bình (`Mean`) | Độ lệch chuẩn (`SD`) | $\bar{X} \pm SD$ (Ví dụ: $45.2 \pm 8.6$ tuổi) |
| **Phân phối Không chuẩn** | Trung vị (`Median`) | Khoảng tứ phân vị (`IQR`) | $Median (IQR)$ (Ví dụ: $5.8 (4.2 - 8.1) \text{ mg/dL}$) |

![Boxplot Output](_images/img-3-thong-ke-3.png)

```text
Analyze > Descriptive Statistics > Explore... > Plots... > [x] Histogram [x] Normality plots with tests
```

---

## 4. Mô Tả Mối Quan Hệ Giữa Hai Biến Số

- **Biến Định tính x Biến Định tính**: Dùng bảng chéo `Crosstabs`.
  ```text
  Analyze > Descriptive Statistics > Crosstabs... > Cells... > [x] Row
  ```
- **Biến Định tính x Biến Định lượng**: Dùng `Case Summaries`.
  ```text
  Analyze > Reports > Case Summaries...
  ```
- **Hai Biến Định lượng**: Dùng tương quan `Bivariate` và biểu đồ phân tán `Scatterplot`.
  ```text
  Analyze > Correlate > Bivariate...
  ```

---

## Điều Hướng Bài Học

[< Chương Trước: Quản lý dữ liệu](2-quan-ly-va-bien-doi-du-lieu.md) | [Mục lục](0-muc-luc.md) | [Chương Sau: Kiểm định giá trị trung bình >](4-kiem-dinh-gia-thiet-trung-binh.md)
