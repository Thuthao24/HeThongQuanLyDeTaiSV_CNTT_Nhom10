# Sườn toàn bộ đồ án — Hệ thống quản lý đề tài sinh viên

## Công nghệ
- Java 26
- Spring Boot 4.1.1
- Spring MVC
- Spring Data JPA
- Spring Security + BCrypt
- Thymeleaf
- MySQL 8+
- Tomcat nhúng của Spring Boot
- Maven

## Kiến trúc 3 tầng
`Controller -> Service -> Repository -> MySQL`

## Module đã dựng sườn
1. Tài khoản + phân quyền
2. Bộ môn
3. Giảng viên
4. Sinh viên
5. Đợt đăng ký
6. Đề tài
7. GV hướng dẫn
8. Nhóm sinh viên
9. Thành viên nhóm
10. Đăng ký đề tài
11. Nộp báo cáo
12. Hội đồng
13. Thành viên hội đồng
14. GV phản biện
15. Điểm
16. Kết quả
17. Thông báo

## Nghiệp vụ cốt lõi đã đặt sườn trong NghiepvuDetaiService
- Giai đoạn 1: GV đề xuất đề tài -> duyệt -> công bố.
- Giai đoạn 2: nhóm SV đăng ký đề tài đã công bố.
- Nhóm 3-5 SV.
- Mỗi nhóm chỉ đăng ký 1 đề tài.
- Đề tài phải có 1-2 GVHD trước khi công bố.
- Chỉ nhóm trưởng được nộp báo cáo.
- Điểm cuối = trung bình cộng các điểm thành phần.( Điểm phản biên * 30% + Điểm hội đồng * 70%)
- Công bố kết quả.

## Chạy project
1. Import `database/Quanlydetaisinhvien.sql` vào MySQL.
2. Sửa `src/main/resources/application.properties` nếu MySQL có mật khẩu:
   `spring.datasource.password=...`
3. Mở terminal tại thư mục project.
4. Chạy:
   `mvn spring-boot:run`
5. Mở:
   `http://localhost:8080`

