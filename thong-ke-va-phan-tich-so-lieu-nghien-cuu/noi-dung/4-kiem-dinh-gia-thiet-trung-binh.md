# Chương 4: Kiểm Định Giả Thuyết Về Giá Trị Trung Bình

Kiểm định giả thuyết về giá trị trung bình thuộc nhóm kiểm định tham số (Parametric Tests), áp dụng cho các biến phụ thuộc định lượng có phân phối chuẩn.

---

## 1. Kiểm Định Một Giá Trị Trung Bình (One-Sample T-Test)

So sánh giá trị trung bình $\bar{X}$ thu được từ mẫu nghiên cứu với một giá trị lý thuyết / chuẩn $\mu_0$ đã biết trước.

Đường dẫn thực hiện lệnh:

```text
Analyze > Compare Means > One-Sample T Test...
```

> **Đọc kết quả:** Nhìn cột `Sig. (2-tailed)`. Nếu $p < 0.05 \rightarrow$ Bác bỏ $H_0$, trung bình mẫu khác biệt có ý nghĩa thống kê so với giá trị chuẩn.

---

## 2. Kiểm Định So Sánh Hai Giá Trị Trung Bình Độc Lập (Independent-Samples T-Test)

So sánh trung bình của 2 nhóm đối tượng độc lập (ví dụ: Nam vs Nữ, Bệnh vs Chứng).

Đường dẫn thực hiện lệnh:

```text
Analyze > Compare Means > Independent-Samples T Test...
```

> **Quy trình đọc kết quả bắt buộc 2 bước:**
> 1. **Bước 1**: Đọc kiểm định phương sai Levene (`Levene's Test for Equality of Variances` - cột `Sig.`):
>    - Nếu $Sig. \ge 0.05$: Phương sai 2 nhóm đồng nhất -> Đọc kết quả T-Test ở hàng trên (`Equal variances assumed`).
>    - Nếu $Sig. < 0.05$: Phương sai 2 nhóm không đồng nhất -> Đọc kết quả T-Test ở hàng dưới (`Equal variances not assumed`).
> 2. **Bước 2**: Đọc giá trị $p$-value tại cột `Sig. (2-tailed)` của hàng tương ứng. Nếu $p < 0.05 \rightarrow$ Sự khác biệt trung bình giữa 2 nhóm có ý nghĩa thống kê.

---

## 3. Kiểm Định So Sánh Hai Giá Trị Trung Bình Ghép Cặp (Paired-Samples T-Test)

So sánh trung bình của cùng một nhóm đối tượng được đo lường tại 2 thời điểm khác nhau (Trước vs Sau can thiệp).

Đường dẫn thực hiện lệnh:

```text
Analyze > Compare Means > Paired-Samples T Test...
```

---

## 4. Kiểm Định So Sánh Nhiều Giá Trị Trung Bình (One-Way ANOVA)

So sánh giá trị trung bình trên $\ge 3$ nhóm độc lập (ví dụ: So sánh điểm hài lòng giữa CBYT ở 6 tỉnh thành).

Đường dẫn thực hiện lệnh:

```text
Analyze > Compare Means > One-Way ANOVA... > Post Hoc... > [x] Tukey
```

> **Cách đọc kết quả ANOVA:**
> 1. Đọc kiểm định đồng nhất phương sai `Test of Homogeneity of Variances` ($Sig. \ge 0.05$).
> 2. Đọc bảng `ANOVA`: Nếu $Sig. < 0.05 \rightarrow$ Có ít nhất một cặp nhóm khác biệt nhau về trung bình.
> 3. Đọc bảng `Multiple Comparisons (Post-Hoc)`: Tìm chính xác từng cặp nhóm nào khác biệt nhau ($p < 0.05$).

---

## Điều Hướng Bài Học

[< Chương Trước: Thống kê mô tả](3-thong-ke-mo-ta-va-trinh-bay-du-lieu.md) | [Mục lục](0-muc-luc.md) | [Chương Sau: Kiểm định tỷ lệ & biến định tính >](5-kiem-dinh-ty-le-va-bien-dinh-tinh.md)
