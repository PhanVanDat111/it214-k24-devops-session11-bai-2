# Bài 2: Biên dịch đóng gói tệp ứng dụng .jar với Gradle và lưu trữ Artifacts

## Giới thiệu
Bài tập này cấu hình GitHub Actions để biên dịch, đóng gói ứng dụng Spring Boot thành tệp thực thi `.jar` sử dụng Gradle và lưu trữ tệp `.jar` đó làm GitHub Artifacts.

## Các bước đã thực hiện
1. Tạo thư mục cấu hình `.github/workflows/`.
2. Cấu hình tệp `ci.yml` bổ sung các bước:
   - Chạy lệnh `./gradlew bootJar` để đóng gói tệp JAR.
   - Sử dụng `actions/upload-artifact@v4` để lưu trữ tệp artifact với tên `app-jar` từ đường dẫn `build/libs/*.jar`.

## Hướng dẫn kiểm tra
- Đẩy commit lên nhánh `main`.
- Truy cập tab Actions trên GitHub để kiểm tra Workflow.
- Kiểm tra phần Summary để tải về tệp artifact `app-jar`.

## Ảnh chụp màn hình kết quả thực nghiệm
![Kết quả thực nghiệm](git_verification_result.png)
