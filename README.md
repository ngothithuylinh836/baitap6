# baitap6
Bài tập 6: Hệ quản trị CSDL
Chủ đề: Câu lệnh Select
Yêu cầu bài tập: 
Cho file sv_tnut.sql (1.6MB)
1. Hãy nêu các bước để import được dữ liệu trong sv_tnut.sql vào sql server của em
2. dữ liệu đầu vào là tên của sv; sđt; ngày, tháng, năm sinh của sinh viên (của sv đang làm bài tập này)
3. nhập sql để tìm xem có những sv nào trùng hoàn toàn ngày/tháng/năm với em?
4. nhập sql để tìm xem có những sv nào trùng ngày và tháng sinh với em?
5. nhập sql để tìm xem có những sv nào trùng tháng và năm sinh với em?
6. nhập sql để tìm xem có những sv nào trùng tên với em?
7. nhập sql để tìm xem có những sv nào trùng họ và tên đệm với em.
8. nhập sql để tìm xem có những sv nào có sđt sai khác chỉ 1 số so với sđt của em.
9. BẢNG SV CÓ HƠN 9000 ROWS, HÃY LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG  VIỆT, GIẢI THÍCH.
10. HÃY NHẬP SQL ĐỂ LIỆT KÊ CÁC SV NỮ NGÀNH KMT CÓ TRONG BẢNG SV (TRÌNH BÀY QUÁ TRÌNH SUY NGHĨ VÀ GIẢI NHỮNG VỨNG MẮC)
# bai lam
1. Các bước để import được dữ liệu trong sv_tnut.sql vào sql server :
  - B1: Mở SQL Server Management Studio (SSMS)
  - B2:  Chọn Database ( đặt tên sv_tnut )
  - B3: Mở và kiểm tra tệp sv_tnut.sql
  - B4 : Import tệp .sql vào SQL Server
  - B5 : Kiểm tra kết quả
2. dữ liệu đầu vào là tên của sv; sđt; ngày, tháng, năm sinh của sinh viên 
- Họ tên : Ngô Thị Thùy Linh
- Sdt : 0337036640
- Ngày,tháng, năm sinh : 11/05/2004

3. nhập sql để tìm xem có những sv nào trùng hoàn toàn 2004-05-11 với em
 - Kiểm tra sinh viên nào có cùng ngày sinh cưa mình .Tìm người có ngày sinh cụ thể để cập nhật thông tin. Kiểm tra sinh viên trùng ngày sinh (có thể cần cho thống kê).


   ![image](https://github.com/user-attachments/assets/12e4915b-8b28-4ff0-be38-2cc4f5f4189c)

4. nhập sql để tìm xem có những sv nào trùng ngày 11 và tháng 5 với em?
- em đang lấy danh sách tất cả sinh viên (dòng SELECT *) từ bảng sv có ngày sinh là 11/05 (ngày 11 tháng 5), bất kể năm sinh.


   ![image](https://github.com/user-attachments/assets/3d260e7a-be3e-4f45-9e03-a6205c5d5dbb)

5. nhập sql để tìm xem có những sv nào trùng tháng 05 và năm sinh 2004 với em?

   - SELECT *: Lấy toàn bộ thông tin (masv, hodem, ten, ns, lop, sdt...) từ bảng SV.

   - FROM SV: Truy vấn từ bảng SV (có thể là bảng Sinh Viên).

   - WHERE MONTH(ns) = 5: Lọc các dòng mà tháng của ngày sinh (ns) là tháng 

   - AND YEAR(ns) = 2004: Đồng thời năm sinh là 2004.

![image](https://github.com/user-attachments/assets/d6ac2da1-d501-4f66-b8e3-d51e450c775d)

6. nhập sql để tìm xem có những sv nào trùng tên với em

![image](https://github.com/user-attachments/assets/1a3b1ecf-3f94-4d98-bcaa-4b8eff43a4de)

7. nhập sql để tìm xem có những sv nào trùng họ và tên đệm với em.

   ![image](https://github.com/user-attachments/assets/6237bf4a-73cd-4b39-a617-f25e7b09cd31)

8. nhập sql để tìm xem có những sv nào có sđt sai khác chỉ 1 số so với sđt của em.

   ![image](https://github.com/user-attachments/assets/4e9d5441-fe89-44f5-bed0-64c4affdf950)

9. BẢNG SV CÓ HƠN 9000 ROWS, HÃY LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG  VIỆT, GIẢI THÍCH.

    ![image](https://github.com/user-attachments/assets/94d16e15-0e80-4640-aa81-325dd2e96ff4)

10. HÃY NHẬP SQL ĐỂ LIỆT KÊ CÁC SV NỮ NGÀNH KMT CÓ TRONG BẢNG SV (TRÌNH BÀY QUÁ TRÌNH SUY NGHĨ VÀ GIẢI NHỮNG VỨNG MẮC)
    - Nếu bảng SV không có cột giới tính nhưng em muốn lọc các sinh viên nữ, thì cách em đang làm là dựa vào họ đệm (hodem) và tên (ten)
      
    ![image](https://github.com/user-attachments/assets/37a23bb3-2a90-4244-b641-81cd26fdb565)

