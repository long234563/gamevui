# THIÊN CHIẾN — Android APK

Game MOBA 2D ba đường, chuyển từ HTML/JavaScript thành ứng dụng Android offline bằng WebView.

## Tạo APK bằng GitHub Actions

1. Mở tab **Actions** của repository `long234563/gamevui`.
2. Chọn workflow **Thiên Chiến - Build APK**.
3. Nhấn **Run workflow** (chọn main). Hoặc chờ job tự chạy khi thay đổi thư mục này.
4. Sau khi job hoàn thành (màu xanh), mở job và kéo xuống mục **Artifacts**.
5. Tải **Thien-Chien-APK**; giải nén file zip để lấy `app-debug.apk`.
6. Chép `app-debug.apk` vào điện thoại Android và cài đặt. Android có thể yêu cầu cho phép cài ứng dụng từ nguồn này.

Điều khiển: chạm vào bản đồ để tướng di chuyển; chạm nút Q/W/E/R trên màn hình để tung chiêu. Xoay điện thoại nằm ngang. Game hiện chơi với bot, không phải multiplayer trực tuyến.

## Dự án

- `app/src/main/assets/index.html`: mã nguồn game
- `app/src/main/java/com/long234563/thienchien/MainActivity.java`: Android WebView offline
- `app/src/main/AndroidManifest.xml`: cấu hình ứng dụng
- `app/build.gradle`: thông số Android

## Thử build trên máy

Yêu cầu Java 17, Android SDK 35, Gradle 8.9:

```sh
gradle :app:assembleDebug
```

APK tại `app/build/outputs/apk/debug/app-debug.apk`.

> Đây là bản debug APK để thử nghiệm, chưa ký bản release/đăng Google Play.
