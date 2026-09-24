# Chương 4: Kiểm Định Giả Thuyết Về Giá Trị Trung Bình

Trong nghiên cứu y sinh và quản lý, việc so sánh giá trị trung bình giữa các nhóm đối tượng (ví dụ: so sánh huyết áp trung bình giữa nam và nữ, hoặc so sánh hiệu quả giảm đường huyết trước và sau điều trị) là nhu cầu vô cùng phổ biến. Chương này trình bày các kiểm định tham số (Parametric Tests) để kiểm định giá trị trung bình.

---

## 1. Cơ Sở Lý Thuyết Kiểm Định Giả Thuyết Thống Kê

Mọi kiểm định thống kê đều dựa trên việc đối chiếu hai giả thuyết bác bỏ nhau:
- **Giả thuyết Không ($H_0$)**: "Không có sự khác biệt" hoặc "Không có sự liên quan" giữa các quần thể.
- **Giả thuyết Đối ($H_a$)**: "Có sự khác biệt" hoặc "Có sự liên quan" giữa các quần thể.

### Quy tắc quyết định dựa trên $p$-value:
- **Mức ý nghĩa thống kê $\alpha$**: Mặc định chọn $\alpha = 0.05$ (độ tin cậy $95\%$).
- Nếu **$p < 0.05$**: Bác bỏ $H_0$, chấp nhận $H_a \rightarrow$ Khác biệt **có ý nghĩa thống kê**.
- Nếu **$p \ge 0.05$**: Chưa đủ cơ sở bác bỏ $H_0 \rightarrow$ Khác biệt **không có ý nghĩa thống kê**.

---

## 2. Kiểm Định Một Giá Trị Trung Bình (`One-Sample T-Test`)

### 2.1. Mục đích
So sánh giá trị trung bình mẫu $\bar{X}$ thu được từ nghiên cứu với một giá trị lý thuyết/chuẩn $\mu_0$ đã biết trước.

### 2.2. Điều kiện áp dụng
- Biến phụ thuộc là biến định lượng liên tục có **phân phối chuẩn**.

### 2.3. Ví dụ thực tế
*Ví dụ*: Kiểm tra xem điểm hài lòng công việc trung bình của cán bộ y tế trong nghiên cứu năm 2015 có khác biệt so với mức chuẩn lý thuyết $3.5$ điểm hay không?
- $H_0$: Điểm trung bình hài lòng $= 3.5$
- $H_a$: Điểm trung bình hài lòng $\ne 3.5$

### 2.4. Thao tác SPSS
1. Vào menu: `Analyze > Compare Means > One-Sample T Test...`
2. Chuyển biến định lượng (ví dụ: `diem_hai_long`) vào ô **Test Variable(s)**.
3. Tại ô **Test Value**: Nhập giá trị so sánh `= 3.5`.
4. Bấm **OK**.

```
[Thao tác SPSS]
Analyze -> Compare Means -> One-Sample T Test -> Test Variable(s): diem_hai_long
-> Test Value: 3.5 -> OK
```

### 2.5. Đọc kết quả Output & Kết luận
- Xem bảng **One-Sample Test**:
  - Đọc giá trị $t$, bậc tự do $df$ và $p$-value tại cột **Sig. (2-tailed)**.
  - Cột **Mean Difference**: Độ lệch giữa trung bình mẫu và giá trị chuẩn.
- *Kết luận ví dụ*: Nếu $Sig. (2-tailed) = .000 < 0.05 \rightarrow$ Bác bỏ $H_0$. Có sự khác biệt có ý nghĩa thống kê giữa điểm trung bình hài lòng của CBYT ($3.14 \pm 0.42$) so với mức $3.5$ điểm ($p < 0.001$).

---

## 3. Kiểm Định So Sánh Hai Giá Trị Trung Bình Độc Lập (`Independent-Samples T-Test`)

### 3.1. Mục đích
So sánh giá trị trung bình của một biến định lượng giữa hai nhóm đối tượng độc lập hoàn toàn với nhau (ví dụ: Nam vs Nữ; Nhóm bệnh vs Nhóm chứng; Nhóm dùng thuốc A vs Nhóm dùng Placebo).

### 3.2. Điều kiện áp dụng
- Biến định lượng ở 2 nhóm có phân phối chuẩn.
- Các quan sát ở 2 nhóm độc lập nhau.

### 3.3. Ví dụ thực tế
*Ví dụ*: So sánh điểm hài lòng trung bình giữa cán bộ y tế Nam và Nữ.

### 3.4. Thao tác SPSS
1. Vào menu: `Analyze > Compare Means > Independent-Samples T Test...`
2. Đưa biến định lượng (`diem_hai_long`) vào ô **Test Variable(s)**.
3. Đưa biến phân nhóm định tính (`gioi_tinh`) vào ô **Grouping Variable**.
4. Bấm nút **Define Groups...**:
   - Group 1: Nhập `1` (Nam)
   - Group 2: Nhập `2` (Nữ)
   - Bấm **Continue**.
5. Bấm **OK**.

```
[Thao tác SPSS]
Analyze -> Compare Means -> Independent-Samples T Test -> Test Variable(s): diem_hai_long
-> Grouping Variable: gioi_tinh -> Define Groups (1, 2) -> OK
```

### 3.5. Đọc kết quả Output (Bắt buộc đọc 2 bước)

```
                       BẢNG INDEPENDENT SAMPLES TEST
                                     |
           +-------------------------+-------------------------+
           |                                                   |
1. ĐỌC LEVENE'S TEST FOR EQUALITY OF VARIANCES       2. ĐỌC KẾT QUẢ T-TEST SO SÁNH TRUNG BÌNH
(Kiểm định tính đồng nhất phương sai)                 (Sig. 2-tailed)
           |                                                   |
   +-------+-------+                                   +-------+-------+
   |               |                                   |               |
Sig. >= 0.05    Sig. < 0.05                        Hàng Equal      Hàng Equal
Phương sai      Phương sai                         variances       variances
đồng nhất       KHÔNG đồng nhất                    assumed         not assumed
```

1. **Bước 1: Kiểm định tính đồng nhất phương sai (Levene's Test)**
   - Nhìn cột **Sig.** thuộc mục *Levene's Test for Equality of Variances*.
   - Nếu **$Sig. \ge 0.05$**: Phương sai 2 nhóm đồng nhất $\rightarrow$ Đọc kết quả T-test ở hàng trên (**Equal variances assumed**).
   - Nếu **$Sig. < 0.05$**: Phương sai 2 nhóm không đồng nhất $\rightarrow$ Đọc kết quả T-test ở hàng dưới (**Equal variances not assumed**).
2. **Bước 2: Đọc kết quả kiểm định T-Test**
   - Đọc cột **Sig. (2-tailed)** ở hàng tương ứng xác định từ Bước 1.
   - Nếu $Sig. (2-tailed) < 0.05$: Sự khác biệt trung bình giữa 2 nhóm có ý nghĩa thống kê.

---

## 4. Kiểm Định So Sánh Hai Giá Trị Trung Bình Ghép Cặp (`Paired-Samples T-Test`)

### 4.1. Mục đích
So sánh 2 giá trị trung bình của **cùng một nhóm đối tượng** nhưng được đo lường tại 2 thời điểm khác nhau (thường là Trước - Sau can thiệp) hoặc ghép cặp theo cặp quan sát trùng lặp.

### 4.2. Ví dụ thực tế
*Ví dụ*: Đánh giá chỉ số đường huyết trung bình của bệnh nhân trước và sau 3 tháng điều trị bằng bài thuốc YHCT.

### 4.3. Thao tác SPSS
1. Vào menu: `Analyze > Compare Means > Paired-Samples T Test...`
2. Chọn đồng thời 2 biến: Biến trước (`duong_huyet_truoc`) và Biến sau (`duong_huyet_sau`) đưa vào ô **Paired Variables**.
3. Bấm **OK**.

### 4.4. Đọc kết quả Output
- Đọc bảng **Paired Samples Test**:
  - Cột **Mean**: Mức độ chênh lệch trung bình giữa Trước và Sau.
  - Cột **Sig. (2-tailed)**: Giá trị $p$-value. Nếu $p < 0.05$, kết luận điều trị can thiệp làm thay đổi trung bình có ý nghĩa thống kê.

---

## 5. Kiểm Định So Sánh Nhiều Giá Trị Trung Bình (`One-Way ANOVA`)

### 5.1. Mục đích
So sánh giá trị trung bình của một biến định lượng trên **nhiều hơn 2 nhóm** đối tượng độc lập (ví dụ: So sánh điểm hài lòng CBYT giữa 6 tỉnh thành phố).

### 5.2. Tại sao không dùng nhiều kiểm định T-Test?
Nếu so sánh 6 nhóm bằng T-Test, chúng ta phải làm $C_6^2 = 15$ lần kiểm định T-Test. Việc này sẽ làm sai lệch xác suất mắc lỗi loại I ($\alpha$) tăng lên rất nhiều ($\alpha_{tổng} = 1 - (1 - 0.05)^{15} \approx 53.6\%$). ANOVA giúp giải quyết bài toán này chỉ trong một lần kiểm định duy nhất.

### 5.3. Thao tác SPSS
1. Vào menu: `Analyze > Compare Means > One-Way ANOVA...`
2. Đưa biến định lượng (`diem_hai_long`) vào **Dependent List**.
3. Đưa biến phân nhóm ($\ge 3$ nhóm, ví dụ: `tinh_thanh`) vào **Factor**.
4. Vào **Options...**: Tích chọn $\checkmark$ **Descriptive** (Mô tả) và $\checkmark$ **Homogeneity of variance test** (Kiểm định phương sai đồng nhất).
5. Vào **Post Hoc...** (Kiểm định so sánh bội sau ANOVA):
   - Nếu phương sai đồng nhất: Tích chọn $\checkmark$ **Tukey** hoặc $\checkmark$ **LSD** / **Bonferroni**.
   - Nếu phương sai không đồng nhất: Tích chọn $\checkmark$ **Games-Howell**.
6. Bấm **Continue** $\rightarrow$ **OK**.

```
[Thao tác SPSS]
Analyze -> Compare Means -> One-Way ANOVA -> Dependent List: diem_hai_long
-> Factor: tinh_thanh -> Options: [x] Descriptive, [x] Homogeneity of variance test
-> Post Hoc: [x] Tukey -> OK
```

### 5.4. Đọc kết quả Output
1. **Kiểm định Homogeneity of Variances**: Đảm bảo $Sig. \ge 0.05$ để thỏa mãn giả định ANOVA.
2. **Bảng ANOVA**: Đọc cột **Sig.**. Nếu $Sig. < 0.05 \rightarrow$ Có ít nhất một cặp nhóm có sự khác biệt về giá trị trung bình.
3. **Bảng Multiple Comparisons (Post-Hoc)**: Nhìn từng cặp so sánh để chỉ ra chính xác nhóm nào khác biệt so với nhóm nào (dựa vào dấu $\star$ hoặc $Sig. < 0.05$ từng cặp).
