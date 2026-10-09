# Bài thực hành: Truy vấn nâng cao CSDL Quản Lý Sinh Viên

## 📋 Thông tin
- **Database:** QuanLySinhVien
- **Công cụ:** MySQL Workbench
- **Số lượng truy vấn:** 5

## 📝 Danh sách các truy vấn

### Truy vấn 1: Sinh viên tên bắt đầu 'h'
```sql
SELECT * FROM Student WHERE StudentName LIKE 'h%';
Truy vấn 2: Lớp bắt đầu tháng 12
sql
SELECT * FROM Class WHERE MONTH(StartDate) = 12;
Truy vấn 3: Môn học Credit 3-5
sql
SELECT * FROM Subject WHERE Credit BETWEEN 3 AND 5;
Truy vấn 4: Đổi ClassID của Hung thành 2
sql
UPDATE Student SET ClassId = 2 WHERE StudentName = 'Hung';
Truy vấn 5: Điểm thi sắp xếp
sql
SELECT S.StudentName, Sub.SubName, M.Mark
FROM Student S 
JOIN Mark M ON S.StudentId = M.StudentId 
JOIN Subject Sub ON M.SubId = Sub.SubId
ORDER BY M.Mark DESC, S.StudentName ASC;
