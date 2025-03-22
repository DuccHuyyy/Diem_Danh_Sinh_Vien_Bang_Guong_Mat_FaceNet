<h1 align="center">ỨNG DỤNG CÔNG NGHỆ TRONG 
HỆ THỐNG QUẢN LÝ VÀ ĐIỂM DANH SINH VIÊN </h1>

<div align="center">

<p align="center">
  <img src="images/logoDaiNam.png" alt="DaiNam University Logo" width="200"/>
  <img src="images/LogoAIoTLab.png" alt="AIoTLab Logo" width="170"/>
</p>

[![Made by AIoTLab](https://img.shields.io/badge/Made%20by%20AIoTLab-blue?style=for-the-badge)](https://www.facebook.com/DNUAIoTLab)
[![Fit DNU](https://img.shields.io/badge/Fit%20DNU-green?style=for-the-badge)](https://fitdnu.net/)
[![DaiNam University](https://img.shields.io/badge/DaiNam%20University-red?style=for-the-badge)](https://dainam.edu.vn)

</div>

<h2 align="center">Ứng dụng công nghệ trong hệ thống quản lý và điểm danh sinh viên</h2>

<p align="left">
  Hệ thống quản lý và điểm danh sinh viên sử dụng công nghệ nhận diện khuôn mặt và database SQL Server. Ứng dụng này cho phép giảng viên dễ dàng quản lý thông tin sinh viên, thực hiện điểm danh tự động và theo dõi lịch sử điểm danh qua giao diện người dùng thân thiện.
</p>

---

## 🌟 Giới thiệu

- **📌 Điểm danh tự động:** Sinh viên quét mã QR để điểm danh. Hệ thống xác định điểm danh đúng hạn hay trễ qua khoảng thời gian quét.
- **💡 Thông báo trực quan:** Arduino sẽ điều khiển LED (xanh/đỏ) và còi để thông báo kết quả điểm danh. Nếu điểm danh trễ, hệ thống phát thông báo qua loa máy tính.
- **📊 Quản lý dữ liệu:** Dữ liệu điểm danh được lưu trong MongoDB, có thể xem lịch sử và xuất ra file CSV.
- **🖥️ Giao diện thân thiện:** Sử dụng Tkinter cho giao diện quản lý và Flask cho xử lý điểm danh qua web.

---
## 🏗️ HỆ THỐNG
<p align="center">
  <img src="images/sodohethong.png" alt="System Architecture" width="800"/>
</p>

---
## 📂 Cấu trúc dự án

📦 BTL_IOT

├── 📂 face-recognition-attendance       # Hệ thống điểm danh dựa trên nhận diện khuôn mặt  
│   ├── 📂 backend                        # Backend xử lý dữ liệu và logic  
│   │   ├── 📂 dataset                    # Dữ liệu khuôn mặt của sinh viên  

│   │   │   ├── CNTT_16-05/              # Dữ liệu sinh viên CNTT - lớp 16-05

│   │   │   ├── HAN_16-03/                # Dữ liệu sinh viên HAN - lớp 16-03

│   │   ├── 📂 sound                      # Âm thanh thông báo điểm danh

│   │   ├── app.py                       # API backend chính

│   │   ├── temp.jpg                     # Ảnh tạm lưu trong quá trình nhận diện

│   │

│   ├── 📂 frontend                       # Giao diện người dùng (React)

│   │   ├── 📂 node_modules               # Thư viện phụ thuộc cho frontend

│   │   ├── 📂 public                     # Tệp tĩnh của ứng dụng

│   │   ├── 📂 src                        # Mã nguồn frontend

│   │   │   ├── 📂 components             # Các component của React

│   │   │   │   ├── DsDiemDanh.js        # Component hiển thị danh sách điểm danh

│   │   │   │   ├── StudentList.js       # Component hiển thị danh sách sinh viên

│   │   │   │   ├── CameraComponent.js    # Component xử lý camera

│   │   │   │   ├── ManageStudents.js     # Component quản lý sinh viên

│   │   │   ├── App.js                    # Component chính của ứng dụng

│   │   │   ├── index.js                  # Điểm vào chính của ứng dụng React

│   │   │   ├── setupTests.js             # Cấu hình kiểm thử

│   │   ├── package.json                  # Thông tin về các dependencies của frontend

│   │   ├── package-lock.json             # Tệp khóa phiên bản cho các dependencies

├── 📂 venv                               # Môi trường ảo Python

├── 📄 package.json                       # Thông tin về các dependencies chung

---



## 🛠️ CÔNG NGHỆ SỬ DỤNG

<div align="center">

### 📡 Phần cứng
[![Webcam](https://img.shields.io/badge/Webcam-000000?style=for-the-badge)](https://www.logitech.com/en-us/products/webcams)
[![MTCNN](https://img.shields.io/badge/MTCNN-00979D?style=for-the-badge)](https://github.com/ipazc/mtcnn)
[![DeepFace](https://img.shields.io/badge/DeepFace-FF5722?style=for-the-badge)](https://github.com/serengil/deepface)

### 🖥️ Phần mềm
[![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)]()
[![Flask](https://img.shields.io/badge/Flask-Framework-black?style=for-the-badge&logo=flask)]()
[![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-blue?style=for-the-badge)]()
[![MongoDB](https://img.shields.io/badge/MongoDB-4.x-green?style=for-the-badge&logo=mongodb)]()
[![React](https://img.shields.io/badge/React-17.0.2-blue?style=for-the-badge&logo=react)]()
[![axios](https://img.shields.io/badge/axios-0.21.1-orange?style=for-the-badge)]()
[![CORS](https://img.shields.io/badge/CORS-4.x-black?style=for-the-badge)]()

</div>

## 🛠️ Yêu cầu hệ thống

### 🔌 Phần cứng
- **Arduino Uno** (hoặc board tương thích) với **LED (2 màu) và còi**.
- **Cáp USB** để kết nối Arduino với máy tính.
- ⚠️ **Lưu ý:** Mặc định mã nguồn Arduino trong `ThongBao.ino` sử dụng cổng `COM5`. Nếu Arduino của bạn sử dụng cổng khác, hãy thay đổi biến `SERIAL_PORT` trong `chuongTrinh.py`.

### 💻 Phần mềm
- **🐍 Python 3+**
- **🍃 MongoDB** (kết nối mặc định: `mongodb://localhost:27017/`)
- **⚡ Arduino IDE** để nạp file `ThongBao.ino` lên board Arduino.

### 📦 Các thư viện Python cần thiết
Cài đặt các thư viện bằng lệnh:

    pip install pillow qrcode pymongo tkcalendar flask pyserial gtts pygame
## 🧮 Bảng mạch

### 🔩 Kết nối phần cứng:
<img src="images/mohinhfacenet.png" alt="System Architecture" width="800"/>

### ⛓️‍💥 Hướng dẫn cắm dây
| Thiết bị        | Chân trên thiết bị | Kết nối Arduino UNO | Ghi chú                         |
|-----------------|-------------------|---------------------|---------------------------------|
| Breadboard      | -                 | -                   | Dùng để kết nối linh kiện       |
| Đèn LED xanh    | Anode (+), Cathode (-) | Anode → Digital Pin 9, Cathode → GND | Led thông báo khi sinh viên điểm danh đúng giờ|
| Đèn LED đỏ      | Anode (+), Cathode (-) | Anode → Digital Pin 10, Cathode → GND | Led thông báo khi sinh viên điểm danh muộn|
| Buzzer         | (+), (-)            | (+) → Digital Pin 11, (-) → GND |Còi thông báo khi sinh viên điểm danh muộn|
| 7 dây điện      | -                 | -                   | Dùng để nối các linh kiện       |

## 🚀 Hướng dẫn cài đặt và chạy
1️⃣ Chuẩn bị phần cứng
- **Nạp mã Arduino**:

    1. Mở file `ThongBao.ino` bằng Arduino IDE.
    2. Kết nối board Arduino với máy tính.
    3. Nạp (upload) mã nguồn lên board.
    4. Đảm bảo Arduino xuất hiện trên cổng COM5 (hoặc thay đổi trong `chuongTrinh.py` nếu cổng khác COM5).

2️⃣ Cài đặt thư viện Python. 

Cài đặt Python 3 nếu chưa có, sau đó cài đặt các thư viện cần thiết bằng pip.

3️⃣ Cấu hình MongoDB
- Cài đặt MongoDB nếu chưa có.
- Khởi động MongoDB và đảm bảo đang hoạt động tại `mongodb://localhost:27017/`.
- Khôi phục cơ sở dữ liệu từ bản sao lưu:

        mongorestore --db AttendanceDB "đường-dẫn-đến-thư-mục-AttendanceDB"
- Ví dụ:

        mongorestore --db AttendanceDB "C:\Users\LENOVO\Documents\Demo2QR\AttendanceDB"
📌 Lưu ý:
-	Tránh trùng lặp cơ sở dữ liệu: Trước khi thực hiện restore, hãy kiểm tra xem MongoDB đã có cơ sở dữ liệu tên AttendanceDB chưa. Nếu có, bạn có thể gặp lỗi hoặc dữ liệu cũ có thể bị ghi đè.
-	Đảm bảo MongoDB đang chạy: Nếu MongoDB chưa được khởi động, lệnh mongorestore sẽ không hoạt động.

4️⃣ Chạy các chương trình

Để đảm bảo hệ thống hoạt động đúng cách, bạn cần khởi chạy `chuongTrinh.py` trước, thay vì chạy từng file con riêng lẻ. File này cung cấp giao diện chính và bao gồm logic kết nối với Arduino board. Nếu chạy trực tiếp các file con, việc kết nối với Arduino sẽ không hoạt động.

✅ Chạy ứng dụng chính (`chuongTrinh.py`):

    python chuongTrinh.py
- Ứng dụng sẽ:

    - Khởi động **LED Service** tại `localhost:6000` để điều khiển LED và còi.
    - Hiển thị giao diện chính (Tkinter) với các nút: **Tạo mã QR** và **Xem điểm danh**

✅ Chạy ứng dụng quản lý điểm danh (`Diemdanh.py`):

    python Diemdanh.py

✅ Chạy ứng dụng tạo mã QR (`TaoQR.py`):

    python TaoQR.py

## 📖 Hướng dẫn sử dụng
1️⃣ Điểm danh qua QR code

- Sinh viên nhận email chứa mã QR.
- Khi quét mã, trình duyệt sẽ gửi yêu cầu điểm danh đến Flask server.
- Hệ thống kiểm tra tính hợp lệ và cập nhật vào MongoDB, đồng thời điều khiển Arduino:
    - ✅ Điểm danh đúng hạn → LED xanh.
    - ⏳ Điểm danh trễ → LED đỏ, còi, phát thông báo.
    
2️⃣ Quản lý sinh viên & mã QR
- Qua giao diện của TaoQR.py, bạn có thể:
    - Thêm, sửa, xóa thông tin sinh viên.
    - Nhập/xuất danh sách sinh viên từ/đến file CSV.
    - Tạo QR cho sinh viên theo lớp hoặc toàn bộ sinh viên.
    - Xóa mã QR cũ một cách thủ công.

3️⃣ Xem lịch sử điểm danh
- Qua giao diện của Diemdanh.py, bạn có thể:
    - Lọc danh sách điểm danh theo ngày, lớp, trạng thái.
    - Xuất dữ liệu điểm danh ra file CSV.
    - Hệ thống tự động cập nhật và chốt các phiên điểm danh.

## ⚙️ Cấu hình & Ghi chú

1. Cổng Arduino: 
- Mặc định sử dụng COM5, có thể cập nhật trong `chuongTrinh.py`.
2. Email gửi mã QR:
- Trong `TaoQR.py`, cập nhật thông tin *sender_email* và *sender_password*.(sender email là địa chỉ email gửi, sender password là mật khẩu ứng dụng của email đó.)
3. Thời gian hiệu lực mã QR: 
- Mã QR có hiệu lực 100 phút kể từ thời điểm tạo.
4. Môi trường mạng: 
- Thiết bị quét QR cần kết nối cùng mạng với máy chủ.

## 📰 Poster
<p align="center">
  <img src="images/Nhóm-7-Poster.png" alt="System Architecture" width="800"/>
</p>

## 🤝 Đóng góp
Dự án được phát triển bởi 4 thành viên:

| Họ và Tên            | Vai trò                  |
|----------------------|--------------------------|
| Chu Văn Huy          | Phát triển toàn bộ mã nguồn, thiết kế cơ sở dữ liệu, kiểm thử, triển khai dự án và thực hiện video giới thiệu.|
| Hồ Đức Mạnh          | Hỗ trợ bài tập lớn       |
| Nguyễn Đức Kiên      | Thiết kế slide PowerPoint, hỗ trợ bài tập lớn.  |
| Nguyễn Thị Mai Hương | Biên soạn tài liệu Overleaf, Poster, Powerpoint, thuyết trình, đề xuất cải tiến, và hỗ trợ bài tập lớn.|

© 2025 NHÓM 7, CNTT16-05, TRƯỜNG ĐẠI HỌC ĐẠI NAM
