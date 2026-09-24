# Chương 2: Quản Lý Và Biến Đổi Dữ Liệu Trong SPSS

Xử lý và chuẩn bị dữ liệu trước khi phân tích là bước chiếm $60\% - 70\%$ thời gian trong nghiên cứu. Chương này trình bày chi tiết các công cụ xử lý, lọc, mã hóa và ghép file dữ liệu trong SPSS.

---

## 1. Lọc Và Chọn Lọc Bản Ghi Nghiên Cứu (Select Cases)

Lệnh `Select Cases` được dùng để lọc ra một phân nhóm đối tượng thỏa mãn điều kiện nhất định để chạy phân tích (ví dụ: chỉ phân tích bệnh nhân Nam từ 60 tuổi trở lên).

![Hộp thoại Select Cases](_images/img-2-quan-ly-1.png)

Đường dẫn thực hiện lệnh:

```text
Data > Select Cases...
```

> **Các tùy chọn lọc bản ghi trong SPSS:**
> - `All cases`: Chọn tất cả các bản ghi (hủy bỏ mọi bộ lọc trước đó).
> - `If condition is satisfied`: Lọc theo điều kiện logic (Bấm nút `If...` để nhập công thức).
> - `Random sample of cases`: Chọn ngẫu nhiên một tỷ lệ % hoặc số lượng bản ghi.
> - `Based on time or case range`: Chọn theo khoảng hàng (ví dụ: từ hàng 1 đến 100).

```text
Data > Select Cases > If condition is satisfied > If... > [tuoi >= 60 AND hba1c > 7.0]
```

---

## 2. Sắp Xếp Dữ Liệu (Sort Cases)

Lệnh `Sort Cases` giúp sắp xếp các bản ghi theo thứ tự tăng dần (`Ascending`) hoặc giảm dần (`Descending`) dựa trên một hoặc nhiều biến số.

Đường dẫn thực hiện lệnh:

```text
Data > Sort Cases...
```

> **Thao tác:** Đưa biến cần sắp xếp vào khung `Sort by` -> Chọn `Ascending` hoặc `Descending` -> Bấm `OK`.

---

## 3. Tạo Biến Mới Dựa Trên Công Thức Toán Học (Compute Variable)

Lệnh `Compute Variable` được dùng để tính toán và khởi tạo một biến số mới từ các biến số đã có.

![Hộp thoại Compute Variable](_images/img-2-quan-ly-2.png)

Đường dẫn thực hiện lệnh:

```text
Transform > Compute Variable...
```

> **Ví dụ tính Chỉ số khối cơ thể (BMI):**
> - Target Variable: `BMI`
> - Numeric Expression: `can_nang / ((chieu_cao / 100) ** 2)`

---

## 4. Mã Hóa Và Phân Nhóm Biến Số (Recode Variables)

Mã hóa biến số là thao tác chuyển đổi một biến định lượng liên tục thành một biến định tính phân nhóm (ví dụ: chuyển biến Tuổi thành các nhóm tuổi).

![Hộp thoại Recode into Different Variables](_images/img-2-quan-ly-3.png)

Đường dẫn thực hiện lệnh:

```text
Transform > Recode into Different Variables...
```

> **Quy tắc quan trọng:** Luôn dùng `Recode into Different Variables` (Mã hóa thành biến mới) để giữ nguyên giá trị gốc của biến ban đầu.

---

## 5. Tách Và Ghép File Dữ Liệu (Split File & Merge Files)

### 5.1. Tách tệp dữ liệu phân tích (Split File)
Lệnh `Split File` chia bộ dữ liệu thành các nhóm theo một biến định tính. Mọi phân tích sau đó sẽ tự động xuất kết quả riêng biệt cho từng nhóm.

```text
Data > Split File... > Compare groups / Organize output by groups
```

### 5.2. Ghép tệp dữ liệu (Merge Files)
- **Ghép thêm bản ghi (Add Cases)**: Gộp thêm các đối tượng mới có cùng bộ biến số.
  ```text
  Data > Merge Files > Add Cases...
  ```
- **Ghép thêm biến số (Add Variables)**: Gộp thêm các biến mới cho cùng tập đối tượng dựa trên mã định danh chung (Key Variable như `MaBN`).
  ```text
  Data > Merge Files > Add Variables...
  ```

---

## Điều Hướng Bài Học

[< Chương Trước: Tổng quan và Nhập liệu](1-tong-quan-va-nhap-lieu-spss.md) | [Mục lục](0-muc-luc.md) | [Chương Sau: Thống kê mô tả >](3-thong-ke-mo-ta-va-trinh-bay-du-lieu.md)
