# Phạm vi Dự án

## 1. Phạm vi Frontend
Phần frontend của dự án gồm thiết kế và phát triển giao diện người dùng, đảm bảo tương thích và trải nghiệm người dùng tốt trên nhiều thiết bị khác nhau. Cụ thể bao gồm:

### 1.1. Trang chủ (Home Page)
Hiển thị các game nổi bật, chương trình khuyến mãi, các đề xuất game dựa trên sở thích của người dùng.
- **Chức năng:**
  - Hiển thị danh sách game đang được khuyến mãi hoặc đề xuất.
  - Cung cấp thanh tìm kiếm nhanh cho người dùng.
  - Hiển thị các banner quảng cáo về sự kiện hoặc game mới.

### 1.2. Trang danh sách game (Store Page)
Hiển thị tất cả các game có sẵn trên nền tảng, cho phép người dùng lọc và sắp xếp theo nhiều tiêu chí.
- **Chức năng:**
  - Bộ lọc game theo thể loại (action, RPG, indie...), giá tiền, xếp hạng, và độ phổ biến.
  - Hiển thị thông tin ngắn về mỗi game: tên game, giá, ngày phát hành, ảnh thumbnail.
  - Phân trang để tối ưu hiệu suất tải dữ liệu.

### 1.3. Trang chi tiết sản phẩm (Product Detail Page)
Hiển thị thông tin chi tiết về mỗi game, cho phép người dùng xem trước hoặc mua game.
- **Chức năng:**
  - Hiển thị tên game, mô tả chi tiết, trailer, yêu cầu hệ thống.
  - Cho phép người dùng thêm game vào giỏ hàng hoặc danh sách yêu thích.
  - Hiển thị đánh giá và bình luận từ người dùng khác.

### 1.4. Trang giỏ hàng (Cart Page)
Cho phép người dùng xem và quản lý các sản phẩm đã thêm vào giỏ hàng.
- **Chức năng:**
  - Hiển thị danh sách các game trong giỏ hàng, bao gồm tên game, giá tiền, và số lượng.
  - Cập nhật giỏ hàng (thêm, xóa game).
  - Tính tổng số tiền phải thanh toán, bao gồm giảm giá nếu có.

### 1.5. Trang thanh toán (Checkout Page)
Xử lý thanh toán cho các sản phẩm trong giỏ hàng.
- **Chức năng:**
  - Cho phép người dùng lựa chọn phương thức thanh toán (thẻ tín dụng, PayPal).
  - Hiển thị thông tin đơn hàng, tổng tiền và chi tiết giảm giá.
  - Xác nhận giao dịch và chuyển hướng người dùng đến trang xác nhận.

### 1.6. Trang quản lý người dùng (User Profile Page)
Người dùng có thể quản lý thông tin cá nhân và lịch sử giao dịch.
- **Chức năng:**
  - Cập nhật thông tin cá nhân (email, mật khẩu, avatar).
  - Xem lịch sử các giao dịch đã thực hiện, bao gồm các game đã mua và tải về.

### 1.7. Giao diện responsive
Tối ưu hóa giao diện để tương thích với nhiều loại thiết bị như desktop, tablet, và smartphone.
- **Chức năng:**
  - Thiết kế responsive cho tất cả các trang, đảm bảo trải nghiệm người dùng mượt mà trên mobile.
  - Tối ưu hiệu suất trên các trình duyệt và hệ điều hành khác nhau.

## 2. Phạm vi Backend
Phần backend phát triển và quản lý các API cần thiết, cũng như đảm bảo hiệu suất, bảo mật và khả năng mở rộng của hệ thống.

### 2.1. Quản lý người dùng (User Management)
Hệ thống quản lý người dùng cho phép đăng ký, đăng nhập và quản lý thông tin tài khoản.
- **Chức năng:**
  - API đăng ký tài khoản mới và xác thực email.
  - API đăng nhập và xác thực người dùng (sử dụng JWT hoặc OAuth).
  - API quản lý thông tin tài khoản (thay đổi mật khẩu, cập nhật thông tin cá nhân).
  - Bảo mật tài khoản bằng cách mã hóa mật khẩu và áp dụng các phương pháp bảo mật hai yếu tố (2FA).

### 2.2. Quản lý game (Game Management)
Hệ thống quản lý dữ liệu game và thông tin liên quan.
- **Chức năng:**
  - API thêm, sửa, xóa thông tin game từ cơ sở dữ liệu.
  - API để lấy danh sách game, chi tiết game cho trang frontend.
  - Hỗ trợ phân loại game theo thể loại, giá, đánh giá.

### 2.3. Giỏ hàng và thanh toán (Cart and Payment Management)
Quản lý quá trình thêm sản phẩm vào giỏ hàng và xử lý thanh toán.
- **Chức năng:**
  - API giỏ hàng: Thêm/xóa sản phẩm trong giỏ hàng, tính tổng tiền.
  - API thanh toán tích hợp với các cổng thanh toán như PayPal, Stripe để xử lý giao dịch.
  - Hỗ trợ lưu trữ thông tin đơn hàng và trạng thái thanh toán trong cơ sở dữ liệu.

### 2.4. Quản lý đơn hàng (Order Management)
Quản lý các đơn hàng của người dùng sau khi thanh toán.
- **Chức năng:**
  - API lưu trữ và hiển thị lịch sử giao dịch cho người dùng.
  - Hỗ trợ tính năng hoàn tiền hoặc hủy đơn hàng trong một số trường hợp đặc biệt.

### 2.5. Bảo mật và quyền hạn (Security and Authorization)
Đảm bảo an toàn cho hệ thống thông qua quản lý bảo mật.
- **Chức năng:**
  - Mã hóa tất cả các giao dịch thanh toán qua HTTPS.
  - Hỗ trợ OAuth cho đăng nhập an toàn và phân quyền người dùng (admin, user).
  - Bảo vệ chống lại các cuộc tấn công phổ biến như SQL Injection, Cross-Site Scripting (XSS), và Cross-Site Request Forgery (CSRF).

## 3. Phạm vi Testing
Phạm vi kiểm thử sẽ đảm bảo hệ thống vận hành chính xác và bảo mật trước khi phát hành.

### 3.1. Kiểm thử đơn vị (Unit Testing)
Kiểm tra tính chính xác của từng chức năng nhỏ, chẳng hạn như API đăng ký tài khoản, giỏ hàng.
- **Chức năng:**
  - Tạo các trường hợp kiểm thử cho các API và tính năng.
  - Đảm bảo các chức năng độc lập như thêm sản phẩm vào giỏ hàng, tính tổng tiền hoạt động đúng.

### 3.2. Kiểm thử tích hợp (Integration Testing)
Đảm bảo các thành phần trong hệ thống hoạt động mượt mà với nhau.
- **Chức năng:**
  - Kiểm thử sự tương tác giữa frontend và backend.
  - Kiểm thử quá trình từ giỏ hàng đến thanh toán và lưu trữ đơn hàng.
  - Test case, thuc hien test case, log bugs
  - San pham du moi du tieu chi test tiep

### 3.3. Kiểm thử hiệu năng (Performance Testing)
Đánh giá hiệu suất của hệ thống trong điều kiện tải nặng.
- **Chức năng:**
  - Đo lường tốc độ phản hồi của hệ thống với số lượng người dùng tăng dần.
  - Tối ưu hóa thời gian tải trang và hiệu suất API.

### 3.4. Kiểm thử bảo mật (Security Testing)
Đảm bảo hệ thống an toàn trước các cuộc tấn công và lỗ hổng bảo mật.
- **Chức năng:**
  - Kiểm thử khả năng chống lại các tấn công SQL Injection, XSS, CSRF.
  - Xác thực tính bảo mật của hệ thống đăng nhập và thanh toán.

## 4. Phạm vi Deployment
Phạm vi triển khai sẽ bao gồm quá trình cài đặt, vận hành và giám sát hệ thống sau khi phát hành.

### 4.1. Cấu hình máy chủ (Server Setup)
Cấu hình máy chủ để chạy ứng dụng và đảm bảo hiệu suất.
- **Chức năng:**
  - Thiết lập môi trường máy chủ, bao gồm cài đặt web server (Nginx/Apache) và cơ sở dữ liệu (MySQL/PostgreSQL).
  - Cấu hình hệ thống CI/CD để tự động triển khai ứng dụng.

### 4.2. Quản lý bản phát hành (Release Management)
Đảm bảo quá trình phát hành diễn ra mượt mà và có kiểm soát.
- **Chức năng:**
  - Xây dựng pipeline CI/CD cho quá trình phát hành tự động và liên tục (Continuous Integration and Continuous Deployment).
  - Tạo phiên bản phát hành (versioning) và ghi chú thay đổi (release notes).
  - Thực hiện kiểm thử cuối cùng (final testing) trước khi phát hành chính thức.

### 4.3. Giám sát sau triển khai (Post-Deployment Monitoring)
Giám sát hệ thống sau khi triển khai để đảm bảo hiệu suất và phát hiện sớm các lỗi tiềm ẩn.
- **Chức năng:**
  - Thiết lập hệ thống giám sát (monitoring) để theo dõi hiệu suất của ứng dụng (sử dụng các công cụ như Grafana, Prometheus).
  - Cấu hình cảnh báo (alert) khi xảy ra các lỗi về hiệu suất, bảo mật hoặc tài nguyên hệ thống.
  - Theo dõi log để phát hiện các vấn đề liên quan đến bảo mật và hiệu suất.

### 4.4. Khả năng mở rộng (Scalability)
Đảm bảo hệ thống có khả năng mở rộng khi số lượng người dùng tăng đột ngột.
- **Chức năng:**
  - Cấu hình hệ thống load balancing để phân phối tải đều trên nhiều máy chủ.
  - Thiết lập auto-scaling để hệ thống tự động tăng/giảm tài nguyên dựa trên lượng người dùng.
  - Lên kế hoạch mở rộng hạ tầng máy chủ khi cần thiết.

### 4.5. Hỗ trợ sau phát hành (Post-Release Support)
Đảm bảo hỗ trợ kỹ thuật sau khi phát hành để xử lý các vấn đề hoặc cập nhật hệ thống.
- **Chức năng:**
  - Hỗ trợ kỹ thuật và khắc phục các sự cố trong giai đoạn vận hành sau phát hành.
  - Cập nhật và vá lỗi (bug fixes) thường xuyên dựa trên phản hồi của người dùng và kết quả giám sát.
  - Cập nhật tính năng và cải thiện hiệu suất hệ thống dựa trên yêu cầu mới từ người dùng.