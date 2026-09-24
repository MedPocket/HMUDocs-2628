# Chương 1: Tổng Quan Về SPSS Và Quản Lý Nhập Dữ Liệu Nghiên Cứu

## 1. Tổng Quan Về SPSS Statistics Trong Nghiên Cứu Khoa Học

SPSS (Statistical Package for the Social Sciences) là một trong những gói phần mềm phân tích thống kê hàng đầu, được ứng dụng rộng rãi trong các nghiên cứu Y - Dược học, Y tế công cộng, Dịch tễ học và Quản lý. Phiên bản hiện nay do tập đoàn IBM phát triển với tên gọi chính thức là IBM SPSS Statistics.

Giao diện SPSS được thiết kế theo dạng menu thả xuống (pull-down menu) trực quan, giúp nghiên cứu viên xử lý số liệu nhanh chóng, chính xác và hiệu quả.

---

## 2. Giao Diện Làm Việc Của SPSS

Giao diện chính của SPSS gồm 2 chế độ hiển thị chính:

### 2.1. Màn hình Data View (Dữ liệu)
- Mỗi hàng (Row): Đại diện cho 1 bản ghi / quan sát / đối tượng nghiên cứu (Case).
- Mỗi cột (Column): Đại diện cho 1 biến số nghiên cứu (Variable).

### 2.2. Màn hình Variable View (Biến số)
Nơi tiến hành khai báo danh sách biến và định nghĩa 11 thuộc tính cấu trúc cho từng biến trước khi nhập số liệu.

---

## 3. Khai Báo 11 Thuộc Tính Biến Trong Variable View

Mỗi biến số trong SPSS được quản lý bởi 11 thuộc tính cơ bản sau:

1. **Name (Tên biến)**: Tên viết tắt của biến số.
   - Quy tắc: Viết liền không khoảng trắng, không dùng tiếng Việt có dấu, không chứa ký tự đặc biệt.
   - Ví dụ: `tuoi`, `gioi_tinh`, `BMI`, `sBP`.
2. **Type (Kiểu dữ liệu)**:
   - `Numeric`: Dữ liệu dạng số (tuổi, chiều cao, huyết áp).
   - `String`: Dữ liệu dạng chuỗi văn bản (ghi chú, mã bệnh nhân).
   - `Date`: Dữ liệu dạng ngày tháng.
3. **Width (Độ rộng)**: Số ký tự tối đa được phép nhập (mặc định = 8).
4. **Decimals (Số chữ số thập phân)**: Số chữ số hiển thị sau dấu phẩy.
5. **Label (Nhãn biến)**: Mô tả chi tiết ý nghĩa biến số, hỗ trợ viết tiếng Việt có dấu.
   - Ví dụ: `"Giới tính của bệnh nhân"`, `"Huyết áp tâm thu lúc vào viện (mmHg)"`.
6. **Values (Nhãn giá trị mã hóa)**: Mã hóa danh mục giá trị chữ thành số.
   - Ví dụ: `1 = Nam`, `2 = Nữ`; `1 = Nhẹ`, `2 = Vừa`, `3 = Nặng`.
7. **Missing (Giá trị khuyết thiếu)**: Quy ước các mã số thiếu dữ liệu (ví dụ: `99` hoặc `999`).
8. **Columns (Độ rộng cột)**: Độ rộng hiển thị của cột trên giao diện Data View.
9. **Align (Căn lề)**: Căn lề hiển thị dữ liệu (`Left`, `Right`, `Center`).
10. **Measure (Thang đo thống kê)**:
    - `Nominal` (Danh nghĩa): Các giá trị phân loại không có thứ tự (Giới tính, Nhóm máu, Tỉnh thành).
    - `Ordinal` (Thứ tự): Các giá trị phân loại có mối quan hệ thứ tự (Mức độ đau: Nhẹ < Vừa < Nặng).
    - `Scale` (Định lượng): Biến đo lường liên tục hoặc đếm được (Tuổi, Cân nặng, Huyết áp).
11. **Role (Vai trò)**: Vai trò trong mô hình phân tích (Mặc định để `Input`).

---

## 4. Quy Trình Thao Tác Nhập Dữ Liệu

Thao tác đường dẫn lệnh nhập dữ liệu từ Excel vào SPSS:

```text
File > Import Data > Excel...
```

> **Các thiết lập quan trọng trong hộp thoại Read Excel File:**
> - Tích chọn `Read variable names from the first row of data` để lấy dòng đầu tiên làm tên biến.
> - Chọn đúng `Worksheet` chứa dữ liệu.
> - Bấm `OK` để hoàn tất.

---

## Điều Hướng Bài Học

[Mục lục](0-muc-luc.md) | [Chương Sau: Quản lý và Biến đổi Dữ liệu >](2-quan-ly-va-bien-doi-du-lieu.md)
