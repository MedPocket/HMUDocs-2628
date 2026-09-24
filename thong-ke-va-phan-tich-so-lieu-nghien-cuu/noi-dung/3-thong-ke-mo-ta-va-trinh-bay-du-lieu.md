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

Đường dẫn thực hiện lệnh bảng tần số và tỷ lệ phần trăm:

```text
Analyze > Descriptive Statistics > Frequencies...
```

> **Chỉ số báo cáo:** Tần số ($n$) và tỷ lệ phần trăm hợp lệ (`Valid Percent`).
> **Biểu đồ phù hợp:** Biểu đồ cột rời (`Bar Chart`) hoặc biểu đồ hình tròn (`Pie Chart`).

---

## 3. Thống Kê Mô Tả Biến Định Lượng Và Khảo Sát Phân Phối Chuẩn

Để báo cáo biến định lượng chuẩn xác, bắt buộc phải khảo sát xem biến số có tuân theo **Phân phối chuẩn (Normal Distribution)** hay không.

Đường dẫn thực hiện lệnh khảo sát phân phối chuẩn:

```text
Analyze > Descriptive Statistics > Explore... > Plots... > [x] Histogram [x] Normality plots with tests
```

### Quy tắc trình bày chỉ số thống kê trong báo cáo y học:

| Phân phối dữ liệu | Chỉ số tập trung | Chỉ số phân tán | Trình bày chuẩn bài báo khoa học |
| :--- | :--- | :--- | :--- |
| **Phân phối Chuẩn** | Trung bình (`Mean`) | Độ lệch chuẩn (`SD`) | $\bar{X} \pm SD$ (Ví dụ: $45.2 \pm 8.6$ tuổi) |
| **Phân phối Không chuẩn** | Trung vị (`Median`) | Khoảng tứ phân vị (`IQR`) | $Median (IQR)$ (Ví dụ: $5.8 (4.2 - 8.1) \text{ mg/dL}$) |

---

## 4. Mô Tả Mối Quan Hệ Giữa Hai Biến Số

- **Biến Định tính x Biến Định tính**: Bảng chéo `Crosstabs`.
  ```text
  Analyze > Descriptive Statistics > Crosstabs... > Cells... > [x] Row
  ```
- **Biến Định tính x Biến Định lượng**: `Case Summaries`.
  ```text
  Analyze > Reports > Case Summaries...
  ```
- **Hai Biến Định lượng**: Hệ số tương quan `Bivariate` và biểu đồ phân tán `Scatterplot`.
  ```text
  Analyze > Correlate > Bivariate...
  ```

---

## Điều Hướng Bài Học

[< Chương Trước: Quản lý dữ liệu](2-quan-ly-va-bien-doi-du-lieu.md) | [Mục lục](0-muc-luc.md) | [Chương Sau: Kiểm định giá trị trung bình >](4-kiem-dinh-gia-thiet-trung-binh.md)
