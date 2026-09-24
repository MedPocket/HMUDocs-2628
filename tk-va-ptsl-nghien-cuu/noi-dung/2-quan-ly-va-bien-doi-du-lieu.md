# Chương 2: Quản Lý Và Biến Đổi Dữ Liệu Trong SPSS

Xử lý và chuẩn bị dữ liệu trước khi phân tích là bước chiếm $60\% - 70\%$ thời gian trong nghiên cứu khoa học.

---

## 1. Lọc Dữ Liệu (Select Cases)

Lệnh `Select Cases` được dùng để chọn ra một phân nhóm đối tượng thỏa mãn điều kiện nhất định để chạy phân tích (ví dụ: chỉ phân tích bệnh nhân Nam từ 60 tuổi trở lên).

Đường dẫn thực hiện lệnh:

```text
Data > Select Cases... > If condition is satisfied > If...
```

> **Ví dụ cú pháp điều kiện lọc:**
> ```text
> tuoi >= 60 AND hba1c > 7.0
> ```

---

## 2. Sắp Xếp Dữ Liệu (Sort Cases)

Lệnh `Sort Cases` giúp sắp xếp thứ tự các bản ghi theo chiều tăng dần (`Ascending`) hoặc giảm dần (`Descending`).

Đường dẫn thực hiện lệnh:

```text
Data > Sort Cases...
```

---

## 3. Tạo Biến Mới Dựa Trên Công Thức (Compute Variable)

Lệnh `Compute Variable` được dùng để tính toán và khởi tạo một biến số mới từ các biến số đã có.

Đường dẫn thực hiện lệnh:

```text
Transform > Compute Variable...
```

> **Ví dụ công thức tính Chỉ số khối cơ thể (BMI):**
> - Target Variable: `BMI`
> - Numeric Expression: `can_nang / ((chieu_cao / 100) ** 2)`

---

## 4. Mã Hóa Phân Nhóm Biến Số (Recode Variables)

Mã hóa biến số là thao tác chuyển đổi một biến định lượng liên tục thành một biến định tính phân nhóm (ví dụ: chuyển biến Tuổi thành các nhóm tuổi).

Đường dẫn thực hiện lệnh:

```text
Transform > Recode into Different Variables... > Old and New Values...
```

> **Lưu ý:** Luôn chọn `Recode into Different Variables` (Mã hóa thành biến mới) để giữ nguyên dữ liệu gốc ban đầu.

---

## 5. Tách Và Ghép File Dữ Liệu (Split File & Merge Files)

- **Tách tệp phân tích (Split File)**:
  ```text
  Data > Split File... > Compare groups / Organize output by groups
  ```
- **Ghép thêm bản ghi (Add Cases)**:
  ```text
  Data > Merge Files > Add Cases...
  ```
- **Ghép thêm biến số (Add Variables)**:
  ```text
  Data > Merge Files > Add Variables...
  ```

---

## Điều Hướng Bài Học

[< Chương Trước: Tổng quan và Nhập liệu](1-tong-quan-va-nhap-lieu-spss.md) | [Mục lục](0-muc-luc.md) | [Chương Sau: Thống kê mô tả >](3-thong-ke-mo-ta-va-trinh-bay-du-lieu.md)
