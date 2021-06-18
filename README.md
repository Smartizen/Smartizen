# Hướng dẫn chạy Hệ thống IoT quản lý nhà thông minh
## Server
Cần cài đăt các thư viện:
- docker : https://docs.docker.com/engine/install/ubuntu/
- docker-compose : https://docs.docker.com/compose/install/
- nodejs & npm : https://nodejs.org/en/download/
- nestjs : https://docs.nestjs.com/

Sau khi cài đặt xong tiến hành cài đặt source code
### cài đặt môi trường chạy: 
```
git clone https://github.com/Smartizen/DeployConfig.git
```
sau đó cd vào folder DeployConfig và clone các user service và iot service 
```
cd DeployConfig
# cài đặt user service
git clone https://github.com/Smartizen/backend.git
# cài đặt iot service
git clone https://github.com/Smartizen/sensor_backend
```
Sau đó chúng ta cần cài đặt các biến môi trường trong bằng cách copy file .env.example rồi rename thành .env. Tiếp theo là cài đặt các thư viện cho user service và iot service
```
cd backend
yarn install
# OR
npm install
```
Cài đặt thư viện cho iot service
```
cd sensor_backend
yarn install
# OR
npm install
```
Sau khi cài đặt xong chạy khởi chạy docker tại folder DeployConfig
```
docker-compose up
```
### Start Admin page
```
git clone https://github.com/Smartizen/Web_Admin.git
cd Web_Admin
yarn install
yarn start
```
### Start mobile app
Cài đặt Dart và Flutter 
- Dart : https://dart.dev/get-dart
- Flutter : https://flutter.dev/docs/get-started/install
Cài đặt các ide hỗ trợ như android studio và các máy giả lập.
```
git clone https://github.com/Smartizen/mobile.git
cd mobile
flutter get pub
flutter run
```
### Cài đặt các device
Cài đặt ide hỗ trợ :
- arduino ide : https://www.arduino.cc/en/guide/windows
Download source code:
```
git clone https://github.com/Smartizen/Device_ESP8266_v1.git
```
### Cài đặt camera motion detection
```
git clone https://github.com/Smartizen/Device_RaspberryPi_v1.git
```
