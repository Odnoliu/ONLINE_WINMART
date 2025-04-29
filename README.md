# ONLINE_WINMART

Dự án Laravel để xây dựng website thương mại điện tử WinMart. Dưới đây là mô tả chức năng của từng thư mục và tập tin trong dự án.

## Cấu trúc thư mục và tập tin

### Thư mục chính
- **`app/`**: Chứa logic nghiệp vụ của ứng dụng.
  - `Http/Controllers/`: Các controller xử lý yêu cầu HTTP (ví dụ: `HomeController.php`).
  - `Models/`: Các model Eloquent đại diện cho bảng trong database (ví dụ: `User.php`).
  - `Providers/`: Các service provider để đăng ký dịch vụ.

- **`bootstrap/`**: Chứa các file khởi động ứng dụng.
  - `app.php`: File khởi động chính của Laravel.

- **`config/`**: Chứa các file cấu hình.
  - `database.php`: Cấu hình kết nối database.
  - `app.php`: Cấu hình thông tin ứng dụng (tên, timezone,...).

- **`database/`**: Quản lý database.
  - `migrations/`: Các file migration để tạo và chỉnh sửa bảng.
  - `seeders/`: Các file tạo dữ liệu mẫu.
  - `factories/`: Tạo dữ liệu giả để test.

- **`lang/`**: Chứa các file ngôn ngữ để hỗ trợ đa ngôn ngữ.

- **`public/`**: Thư mục công khai, chứa tài nguyên tĩnh.
  - `css/`: Chứa file CSS (ví dụ: `style.css`).
  - `js/`: Chứa file JavaScript.
  - `index.php`: Điểm vào của ứng dụng.

- **`resources/`**: Chứa tài nguyên chưa biên dịch.
  - `css/`: File CSS nguồn (nếu dùng Vite).
  - `js/`: File JavaScript nguồn.
  - `views/`: Các file Blade template (giao diện, ví dụ: `welcome.blade.php`).

- **`routes/`**: Chứa các file định tuyến.
  - `web.php`: Định nghĩa routes cho giao diện web.
  - `api.php`: Định nghĩa routes cho API.

- **`storage/`**: Lưu trữ file tạm thời và log.
  - `app/public/`: Lưu file upload.
  - `logs/`: Lưu file log (ví dụ: `laravel.log`).
  - `framework/`: Lưu cache, session.

- **`tests/`**: Chứa các file kiểm thử.
  - `Feature/`: Test tính năng.
  - `Unit/`: Test đơn vị mã.

- **`vendor/`**: Chứa các thư viện bên thứ ba được cài qua Composer.

### File quan trọng ở thư mục gốc
- **`.editorconfig`**: Chuẩn định dạng code (khoảng cách, thụt lề).
- **`.env`**: File cấu hình môi trường (database, API keys,...). Không đẩy file này lên Git.
- **`.env.example`**: Bản mẫu của `.env` để chia sẻ cấu trúc.
- **`.gitattributes`**: Cấu hình cách Git xử lý file.
- **`.gitignore`**: Chỉ định các file/thư mục không đẩy lên Git.
- **`artisan`**: File dòng lệnh để chạy lệnh Artisan (ví dụ: `php artisan migrate`).
- **`composer.json`**: Định nghĩa các thư viện PHP cần thiết.
- **`composer.lock`**: Ghi lại phiên bản chính xác của các thư viện.
- **`package.json`**: Định nghĩa các thư viện JavaScript.
- **`phpunit.xml`**: Cấu hình cho PHPUnit để chạy kiểm thử.
- **`README.md`**: File hướng dẫn (bạn đang đọc file này).
- **`vite.config.js`**: Cấu hình Vite (công cụ biên dịch tài nguyên frontend). Không cần thiết nếu dùng HTML/CSS thuần.

## Cách cài đặt và chạy dự án
1. **Clone dự án**:
   ```bash
   git clone https://github.com/your-username/ONLINE_WINMART.git
   ```
2. **Cài đặt thư viện**:
   ```bash
   composer install
   ```
3. **Cấu hình môi trường**:
   - Sao chép `.env.example` thành `.env` và cập nhật thông tin database.
4. **Chạy migration**:
   ```bash
   php artisan migrate
   ```
5. **Khởi động server**:
   ```bash
   php artisan serve
   ```
   Truy cập `http://localhost:8000` để xem giao diện.

## Ghi chú
- Dự án sử dụng HTML/CSS thuần cho frontend.
- Tập trung làm việc trong `resources/views/` (Blade templates) và `public/` (CSS, hình ảnh).
- Không chỉnh sửa trực tiếp thư mục `vendor/`.