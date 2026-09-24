# Chương 5: Kiểm Định Giả Thuyết Cho Biến Định Tính Và Tỷ Lệ

Chương này trình bày các kiểm định phi tham số (Non-parametric Tests) để so sánh tỷ lệ và đánh giá mối liên quan giữa các biến định tính.

---

## 1. Kiểm Định Một Giá Trị Tỷ Lệ (Binomial Test)

So sánh tỷ lệ quan sát được từ mẫu nghiên cứu với một tỷ lệ chuẩn/lý thuyết $p_0$ đã cho trước.

```text
Analyze > Nonparametric Tests > Legacy Dialogs > Binomial...
```

---

## 2. Kiểm Định Mối Liên Quan Giữa Hai Biến Định Tính (Chi-Square Test - $\chi^2$)

![Chi-Square Test Output](_images/img-5-ty-le-1.png)

Đường dẫn thực hiện lệnh:

```text
Analyze > Descriptive Statistics > Crosstabs...
```

> **Quy tắc chọn kết quả Khi bình phương trong Bảng $2 \times 2$:**
> - Nếu $N > 40$ và tất cả $E_{ij} \ge 5$: Đọc `Pearson Chi-Square`.
> - Nếu $N \le 40$ và tất cả $E_{ij} \ge 5$: Đọc `Continuity Correction` (hiệu chỉnh Yates).
> - Nếu có ít nhất $1$ ô có $E_{ij} < 5$: Đọc `Fisher's Exact Test` (Kiểm định chính xác Fisher).
>
> **Quy tắc cho Bảng $n \times m$:**
> Không quá $20\%$ số ô có tần số kỳ vọng $E_{ij} < 5$ và không có ô nào có $E_{ij} < 1$. Đọc hàng `Pearson Chi-Square`.

---

## 3. Tỷ Số Chênh (Odds Ratio - OR) Và Nguy Cơ Tương Đối (Relative Risk - RR)

- **Odds Ratio (OR)**: Thích hợp cho nghiên cứu bệnh - chứng (Case-Control Study).
- **Relative Risk (RR)**: Thích hợp cho nghiên cứu đoàn hệ (Cohort Study) và can thiệp.

> **Quy tắc đọc Khoảng tin cậy $95\% \text{ CI}$:**
> - Nếu $95\% \text{ CI}$ **KHÔNG chứa giá trị 1.0**: Mối liên quan có ý nghĩa thống kê ($p < 0.05$).
> - Nếu $95\% \text{ CI}$ **chứa giá trị 1.0**: Mối liên quan không có ý nghĩa thống kê ($p \ge 0.05$).

---

## 4. Kiểm Định Hai Tỷ Lệ Ghép Cặp (McNemar Test)

So sánh tỷ lệ mắc bệnh / đạt tiêu chuẩn của cùng một nhóm đối tượng tại 2 thời điểm (Trước vs Sau can thiệp).

![McNemar Test Output](_images/img-5-ty-le-2.png)

Đường dẫn thực hiện lệnh:

```text
Analyze > Descriptive Statistics > Crosstabs... > Statistics... > [x] McNemar
```

---

## Điều Hướng Bài Học

[< Chương Trước: Kiểm định giá trị trung bình](4-kiem-dinh-gia-thiet-trung-binh.md) | [Mục lục](0-muc-luc.md) | [Chương Sau: Phân tích tương quan & Hồi quy >](6-tuong-quan-va-hoi-quy.md)
