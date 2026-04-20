# Phát Hiện Rò Rỉ Khí Gas ESP32

## Mô tả dự án
Dự án này là hệ thống phát hiện rò rỉ khí gas và cảnh báo cháy sử dụng vi điều khiển ESP32. Hệ thống có khả năng kết nối WiFi, gửi cảnh báo qua ứng dụng Blynk, hiển thị thông tin trên LCD1602, điều khiển relay, còi báo động, và cửa sổ tự động (servo). Người dùng có thể cấu hình WiFi, ngưỡng cảnh báo, chế độ tự động/thủ công qua web hoặc app Blynk.

## Tính năng chính
- Phát hiện khí gas (cảm biến MQ2) và cảnh báo cháy (cảm biến lửa)
- Cảnh báo qua còi, điều khiển relay, mở cửa sổ tự động
- Gửi thông báo đến ứng dụng Blynk
- Hiển thị trạng thái trên LCD1602
- Cấu hình WiFi, token Blynk qua web
- Điều chỉnh ngưỡng cảnh báo, chế độ hoạt động qua nút nhấn hoặc app
- Hỗ trợ chế độ AP/STA, lưu cấu hình vào EEPROM

## Sơ đồ kết nối phần cứng
- ESP32
- Cảm biến khí gas MQ2 (chân 35)
- Cảm biến lửa (chân 34)
- LCD1602 (chân 15, 13, 12, 14, 27, 26)
- Relay (chân 22, 32)
- Servo (chân 33, 25)
- Còi (chân 23)
- Các nút nhấn (chân 5, 18, 19, 21)

## Thư viện sử dụng
- Blynk
- WiFi
- LiquidCrystal
- WebServer
- ESPmDNS
- EEPROM
- SimpleKalmanFilter
- ESP32Servo

Các thư viện này có thể cài qua Library Manager hoặc giải nén vào thư mục `libraries/`.

## Cấu trúc dự án
- Phat_Hien_Ro_Ri_Khi_Gas_ESP32.ino: File chính, chứa toàn bộ logic chương trình
- config.h: Cấu hình WiFi, biến toàn cục
- def.h: Định nghĩa chân kết nối phần cứng
- mybutton.h: Xử lý nút nhấn
- libraries/: Thư viện mở rộng (Blynk, ESP32Servo, SimpleKalmanFilter)

## Hướng dẫn sử dụng
1. Kết nối phần cứng theo sơ đồ
2. Nạp code vào ESP32
3. Khi khởi động, thiết bị phát WiFi AP tên "ESP32"
4. Kết nối WiFi, truy cập 192.168.4.1 để cấu hình WiFi và Blynk Token
5. Sau khi lưu, thiết bị sẽ tự động kết nối WiFi và Blynk
6. Theo dõi, điều khiển và nhận cảnh báo qua app Blynk

## Tùy chỉnh
- Ngưỡng cảnh báo khí gas có thể chỉnh qua nút nhấn MENU/UP/DOWN hoặc app Blynk
- Chuyển đổi chế độ tự động/thủ công qua nút nhấn hoặc app

## Nhóm thực hiện

**Nhóm 3**

| STT | Họ và tên         | Mã sinh viên   |
|-----|-------------------|---------------|
| 1   | Đinh Văn Bình     | B22DCCN079    |
| 2   | Vũ Văn Cường      | B22DCCN103    |
| 3   | Đỗ Xuân Bách      | B22DCCN053    |
| 4   | Trương Quang Vinh | B22DCCN906    |
| 5   | Nguyễn Đăng Trường| B22DCCN881    |

