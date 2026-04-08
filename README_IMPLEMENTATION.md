# Hệ Thống Quản Lý và Kết Nối CLB - Sinh Viên NEU
## Club Management and Connection System

Một hệ thống web toàn diện được thiết kế để quản lý và kết nối các Câu Lạc Bộ (CLB) tại Đại Học Kinh Tế Quốc Dân (NEU).

### 📋 Tính Năng Chính

#### Cho Sinh Viên:
- ✅ Đăng ký tài khoản và quản lý hồ sơ cá nhân
- ✅ Tìm kiếm và xem thông tin CLB
- ✅ Đăng ký tham gia CLB
- ✅ Xem danh sách sự kiện
- ✅ Theo dõi đơn đăng ký và đơn hàng
- ✅ Mua sản phẩm từ CLB

#### Cho Ban Quản Trị CLB:
- ✅ Quản lý thông tin CLB
- ✅ Duyệt đơn đăng ký thành viên
- ✅ Tạo và quản lý sự kiện
- ✅ Quản lý sản phẩm bán
- ✅ Quản lý thành viên CLB

#### Cho Quản Trị Viên (Admin):
- ✅ Quản lý toàn bộ hệ thống
- ✅ Phê duyệt CLB mới
- ✅ Phê duyệt sự kiện và sản phẩm
- ✅ Xem báo cáo thống kê
- ✅ Quản lý người dùng

### 🛠️ Công Nghệ Sử Dụng

- **Backend**: Python 3.8+, Flask 2.3.0
- **Database**: SQLite3
- **Frontend**: HTML5, CSS3, Bootstrap 5
- **ORM**: SQLAlchemy
- **Authentication**: Flask-Login, Werkzeug

### 📦 Cài Đặt và Chạy

#### 1. Clone hoặc Download Dự Án
```bash
cd "d:\HỌC PHẦN\Lập trình Web\Hệ thống quản lý và kết nối CLB"
```

#### 2. Tạo Virtual Environment (Tùy Chọn Nhưng Khuyến Cáo)
```bash
python -m venv venv
# Windows
venv\Scripts\activate
# Linux/Mac
source venv/bin/activate
```

#### 3. Cài Đặt Dependencies
```bash
pip install -r requirements.txt
```

#### 4. Chạy Ứng Dụng
```bash
python app.py
```

Ứng dụng sẽ chạy tại: `http://localhost:5000`

### 🔐 Thông Tin Đăng Nhập Mặc Định

#### Admin Account
- **Username**: `admin`
- **Password**: `admin123`

### 📁 Cấu Trúc Dự Án

```
.
├── app.py                    # Main Flask application
├── models.py                 # Database models
├── requirements.txt          # Python dependencies
├── .env                      # Environment variables
├── readme.md                 # Project requirements (original)
├── README.md                 # This file
├── templates/                # HTML templates
│   ├── base.html            # Base template
│   ├── index.html           # Home page
│   ├── login.html           # Login page
│   ├── register.html        # Registration page
│   ├── error.html           # Error page
│   ├── student/             # Student templates
│   │   ├── dashboard.html
│   │   ├── profile.html
│   │   ├── profile_edit.html
│   │   ├── clubs.html
│   │   └── events.html
│   ├── club/                # Club templates
│   │   ├── dashboard.html
│   │   ├── profile.html
│   │   └── members.html
│   └── admin/               # Admin templates
│       ├── dashboard.html
│       └── clubs.html
└── db/                       # SQLite database folder
    └── club_management.db    # SQLite database file
```

### 📊 Cơ Sở Dữ Liệu

Hệ thống sử dụng SQLite và tạo tự động các bảng sau:

- **users**: Lưu trữ thông tin người dùng
- **students**: Thông tin sinh viên
- **clubs**: Thông tin CLB
- **club_members**: Thành viên của CLB
- **club_applications**: Đơn đăng ký tham gia CLB
- **events**: Sự kiện do CLB tổ chức
- **event_registrations**: Đăng ký tham gia sự kiện
- **products**: Sản phẩm bán của CLB
- **orders**: Đơn hàng
- **order_items**: Chi tiết sản phẩm trong đơn hàng
- **notifications**: Thông báo cho người dùng
- **reports**: Báo cáo thống kê

### 🔄 Quy Trình Hoạt Động

#### 1. Đăng Ký CLB
- Ban quản trị CLB đăng ký tài khoản
- Nộp đơn đăng ký thành lập CLB
- Admin phê duyệt/từ chối
- CLB hoạt động sau khi được phê duyệt

#### 2. Sinh Viên Tham Gia CLB
- Sinh viên tìm kiếm CLB
- Nộp đơn tham gia
- Ban quản trị CLB duyệt
- Sinh viên trở thành thành viên

#### 3. Trang Sự Kiện
- CLB tạo sự kiện
- Admin phê duyệt
- Sinh viên đăng ký tham gia
- Ban quản trị ghi nhận tham gia và cấp điểm Đoàn

### 🚀 Mở Rộng và Phát Triển

Các tính năng có thể được mở rộng:

1. **Payment Processing**: Tích hợp thanh toán trực tuyến
2. **Email Notification**: Gửi thông báo qua email
3. **File Upload**: Tải lên ảnh, tài liệu
4. **Analytics Dashboard**: Biểu đồ thống kê chi tiết
5. **Mobile App**: Ứng dụng di động
6. **API REST**: Phát triển API cho third-party integrations

### 📝 Hướng Dẫn Sử Dụng

#### Cho Sinh Viên:
1. Đăng ký tài khoản với loại "Sinh viên"
2. Vào dashboard và cập nhật hồ sơ
3. Tìm kiếm CLB và nộp đơn
4. Đợi duyệt từ ban CLB
5. Tham gia sự kiện và mua sản phẩm

#### Cho Ban Quản Trị CLB:
1. Đăng ký tài khoản với loại "Ban quản trị CLB"
2. Cập nhật thông tin CLB
3. Đợi Admin phê duyệt CLB
4. Tạo sự kiện và sản phẩm
5. Duyệt đơn đăng ký thành viên

#### Cho Admin:
1. Sử dụng tài khoản admin (username: admin)
2. Truy cập dashboard để xem thống kê
3. Duyệt CLB, sự kiện, sản phẩm
4. Quản lý người dùng
5. Xuất báo cáo

### 📞 Hỗ Trợ và Báo Cáo Lỗi

Nếu gặp vấn đề, vui lòng:
1. Kiểm tra đã cài đặt đúng dependencies
2. Đảm bảo sử dụng Python 3.8+
3. Xóa file `db/club_management.db` để reset database
4. Kiểm tra logs trong terminal

### 📄 Giấy Phép

Dự án này được phát triển cho mục đích giáo dục tại NEU.

### 👥 Tác Giả

Developed for NEU (Đại Học Kinh Tế Quốc Dân)

---

**Version**: 1.0.0  
**Last Updated**: 2024  
**Status**: In Development
chuyển database sang sqlite
