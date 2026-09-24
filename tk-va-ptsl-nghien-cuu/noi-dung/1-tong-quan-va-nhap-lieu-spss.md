# Chương 1: Tổng Quan Về SPSS Và Quản Lý Nhập Dữ Liệu Nghiên Cứu

## 1. Tổng Quan Về SPSS Statistics Trong Nghiên Cứu Khoa Học

SPSS (Statistical Package for the Social Sciences) là một trong những hệ thống phần mềm phân tích thống kê phổ biến nhất thế giới. SPSS được ứng dụng rộng rãi trong nghiên cứu Y - Dược học, Y tế công cộng, Dịch tễ học, Quản lý bệnh viện và Khoa học xã hội. Phiên bản hiện nay được tập đoàn IBM quản lý và phát triển với tên gọi chính thức là IBM SPSS Statistics.

Giao diện SPSS được thiết kế theo dạng hệ thống menu thả xuống (pull-down menu) trực quan, cho phép nghiên cứu viên thực hiện hầu hết các thao tác từ quản lý dữ liệu, kiểm định thống kê đến vẽ biểu đồ mà không bắt buộc phải viết mã lệnh phức tạp.

![Giao diện chính SPSS Statistics](_images/img-1-tong-quan-1.png)

---

## 2. Giao Diện Làm Việc Của SPSS

Giao diện làm việc chính của SPSS bao gồm 2 chế độ hiển thị (tabs ở góc dưới bên trái màn hình):

### 2.1. Màn hình Data View (Hiển thị dữ liệu thực tế)
- Mỗi hàng (Row) tương ứng với một bản ghi hay một đối tượng nghiên cứu (Case / Observation), ví dụ: Bệnh nhân 1, Bệnh nhân 2,...
- Mỗi cột (Column) tương ứng với một biến số nghiên cứu (Variable), ví dụ: Mã bệnh nhân, Tuổi, Giới tính, Huyết áp tâm thu.

### 2.2. Màn hình Variable View (Khai báo thuộc tính biến)
Nơi nghiên cứu viên tiến hành định nghĩa cấu trúc dữ liệu, các thuộc tính của biến số trước khi nhập liệu thực tế.

---

## 3. Khai Báo 11 Thuộc Tính Biến Trong Variable View

![Khai báo 11 thuộc tính biến trong Variable View](_images/img-1-tong-quan-2.png)

Mỗi biến số trong SPSS được quản lý bởi 11 thuộc tính cơ bản sau:

1. **Name (Tên biến)**: Tên viết tắt của biến số.
   - Quy tắc: Viết liền không khoảng trắng, không chứa ký tự đặc biệt, không bắt đầu bằng chữ số, không dùng tiếng Việt có dấu.
   - Ví dụ: `tuoi`, `gioi_tinh`, `BMI`, `sBP`.
2. **Type (Kiểu dữ liệu)**:
   - `Numeric`: Dữ liệu dạng số (tuổi, chiều cao, huyết áp).
   - `String`: Dữ liệu dạng chuỗi văn bản (ghi chú, mã định danh).
   - `Date`: Dữ liệu dạng ngày tháng (ngày vào viện, ngày ra viện).
3. **Width (Độ rộng)**: Số ký tự tối đa được phép nhập. Mặc định là 8.
4. **Decimals (Số chữ số thập phân)**: Số chữ số sau dấu phẩy. Đối với biến số nguyên hoặc biến định tính mã hóa, đặ `Decimals = 0`.
5. **Label (Nhãn biến)**: Mô tả chi tiết ý nghĩa của biến số, cho phép viết tiếng Việt có dấu và khoảng trắng.
   - Ví dụ: `"Giới tính bệnh nhân"`, `"Huyết áp tâm thu lúc vào viện (mmHg)"`.
6. **Values (Nhãn giá trị mã hóa)**: Gán nhãn chữ cho các mã số định tính.
   - Ví dụ: `1 = Nam`, `2 = Nữ`; `1 = Nhẹ`, `2 = Vừa`, `3 = Nặng`.
7. **Missing (Giá trị khuyết thiếu)**: Khai báo các mã số được quy ước là thiếu dữ liệu (User-defined missing values), ví dụ gán `99` hoặc `999`.
8. **Columns (Độ rộng hiển thị cột)**: Độ rộng hiển thị của cột trên giao diện Data View.
9. **Align (Căn lề)**: Căn lề dữ liệu (`Left`, `Right`, `Center`). Mặc định biến số căn phải, biến chuỗi căn trái.
10. **Measure (Thang đo thống kê)**:
    - `Nominal` (Danh nghĩa): Các giá trị phân loại không có thứ tự hơn kém (Giới tính, Nhóm máu, Tỉnh thành).
    - `Ordinal` (Thứ tự): Các giá trị phân loại có mối quan hệ thứ tự rõ ràng (Mức độ đau: Nhẹ < Vừa < Nặng; Giai đoạn ung thư: I < II < III < IV).
    - `Scale` (Định lượng): Biến đo lường liên tục hoặc đếm được (Tuổi, Cân nặng, Huyết áp, Chiều cao).
11. **Role (Vai trò của biến)**: Vai trò trong mô hình phân tích (`Input`, `Target`, `Both`, `None`). Mặc định để `Input`.

---

## 4. Quy Trình Khai Báo Bộ Biến Số Và Nhập Dữ Liệu

> **Các bước chuẩn bị bộ số liệu nghiên cứu chuẩn:**
> 1. Xây dựng phiếu thu thập số liệu / Bệnh án nghiên cứu.
> 2. Khai báo danh sách biến số trong màn hình `Variable View`.
> 3. Thiết lập chính xác `Values` mã hóa và thang đo `Measure`.
> 4. Chuyển sang màn hình `Data View` và tiến hành nhập liệu theo từng hàng (đối tượng).
> 5. Kiểm tra tính hợp lý của dữ liệu (làm sạch dữ liệu).
> 6. Lưu file dữ liệu với định dạng `.sav`.

---

## 5. Nhập Dữ Liệu Từ Các Nguồn Bên Ngoài (Excel, CSV, Stata)

Thực tế nghiên cứu thường thu thập số liệu thông qua Google Forms hoặc file Excel (.xlsx). Các bước nhập file Excel vào SPSS:

```text
File > Import Data > Excel...
```

> **Các thiết lập trong hộp thoại Read Excel File:**
> - Tích chọn `Read variable names from the first row of data` để lấy dòng đầu tiên làm tên biến.
> - Chọn đúng `Worksheet` chứa dữ liệu.
> - Bấm `OK` để hoàn tất nhập liệu, sau đó chuyển sang `Variable View` để kiểm tra lại `Measure` và gán `Values`.

---

## Điều Hướng Bài Học

[Mục lục](0-muc-luc.md) | [Chương Sau: Quản lý và Biến đổi Dữ liệu >](2-quan-ly-va-bien-doi-du-lieu.md)
