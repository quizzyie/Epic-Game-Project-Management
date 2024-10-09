# QLDA Epic Game Web

### 1. **Planning** (Lập kế hoạch)

- **Define Project Scope**
    - Xác định tính năng chính (mua game, tải game, hệ thống điểm thưởng).
    - Xác định các trang (home, store, cart, profile, thanh toán).
- **Set Project Milestones**
    - Đặt mốc hoàn thành: Wireframe, UI/UX, API, Testing.
- **Identify Stakeholders**
    - Xác định các bên liên quan: Team Dev, Team UX/UI, Quản lý dự án, Khách hàng.

### 2. **Requirement Gathering** (Thu thập yêu cầu)

- **Client Meeting & Interviews**
    - Thu thập thông tin từ khách hàng về loại game, mô hình thanh toán.
- **Business Requirement Documentation**
    - Tạo tài liệu yêu cầu nghiệp vụ (game listing, user profile, hệ thống giao dịch).
- **Technical Requirement Documentation**
    - Yêu cầu kỹ thuật cụ thể: bảo mật, số lượng người dùng đồng thời, tích hợp thanh toán.
- **Approval of Requirements**
    - Nhận sự chấp thuận cuối cùng từ khách hàng và các bên liên quan.

### 3. **Design** (Thiết kế)

- **Wireframing**
    - Wireframe cho trang chủ (home page), trang cửa hàng (store), trang sản phẩm, trang thanh toán.
- **UI/UX Design**
    - Thiết kế giao diện người dùng (UI) cho từng thành phần.
    - Chế độ tối/sáng cho giao diện (dark/light mode).
- **Prototype Development**
    - Tạo nguyên mẫu tương tác cho phép người dùng thử nghiệm điều hướng.
- **Design Review & Approval**
    - Nhận xét và chỉnh sửa thiết kế từ các bên liên quan.

### 4. **Development** (Phát triển)

### 4.1 **Front-end Development**

- **Home Page Development**
    - Xây dựng phần hiển thị danh mục game nổi bật.
    - Chức năng tìm kiếm game theo tên, thể loại.
- **Game Store Interface**
    - Chức năng lọc game theo danh mục, giá, đánh giá.
    - Thanh tìm kiếm động (real-time search).
- **User Profile Page**
    - Cập nhật thông tin cá nhân, ảnh đại diện.
    - Quản lý lịch sử mua hàng và tải game.
- **Shopping Cart**
    - Thêm/xóa game vào giỏ hàng.
    - Hiển thị tổng giá tiền với các loại thuế, phí áp dụng.

### 4.2 **Back-end Development**

- **Database Schema Design**
    - Thiết kế bảng cơ sở dữ liệu: games (tên, giá, chi tiết), users (profile, quyền truy cập).
- **API Development**
    - API lấy danh sách game (GET /games).
    - API thanh toán (POST /checkout).
- **User Authentication & Authorization**
    - Đăng ký, đăng nhập người dùng bằng email, Google/Facebook.
    - Quản lý quyền truy cập của admin (thêm game mới, sửa/xóa game).
- **Integration of Payment Gateway**
    - Tích hợp Stripe/PayPal cho hệ thống thanh toán.
    - Chức năng lưu thẻ tín dụng của người dùng một cách an toàn.
- **Game Download System**
    - Xây dựng hệ thống tải game an toàn qua token download (mỗi lần mua chỉ tải 1 lần duy nhất).

### 5. **Testing** (Kiểm thử)

- **Unit Testing**
    - Kiểm thử từng component front-end (home, store, profile).
    - Kiểm thử chức năng API (tìm kiếm game, thanh toán).
- **Integration Testing**
    - Kiểm tra tích hợp giữa front-end và back-end (lấy danh sách game, thêm vào giỏ hàng).
- **Performance Testing**
    - Kiểm thử tốc độ tải trang với 100.000 người dùng cùng truy cập.
    - Kiểm tra tốc độ tải game khi kết nối yếu.
- **Security Testing**
    - Kiểm thử bảo mật đăng nhập (chống brute force, SQL injection).
    - Kiểm thử bảo mật cổng thanh toán (PCI DSS).
- **User Acceptance Testing (UAT)**
    - Người dùng thực hiện các chức năng (mua, tải game, cập nhật profile) để xác nhận hệ thống hoạt động đúng yêu cầu.

### 6. **Deployment** (Triển khai)

- **Setup Production Environment**
    - Thiết lập môi trường production trên AWS/GCP.
- **Data Migration**
    - Di chuyển dữ liệu (games, user profiles, lịch sử giao dịch) từ môi trường phát triển lên production.
- **Launch Website**
    - Đưa trang web vào hoạt động chính thức.
- **Post-launch Monitoring**
    - Theo dõi log hệ thống để phát hiện lỗi và cải thiện hiệu suất.

### 7. **Maintenance & Support** (Bảo trì và hỗ trợ)

- **Bug Fixes**
    - Sửa các lỗi phát sinh sau khi ra mắt (giao diện, chức năng).
- **Feature Updates**
    - Cập nhật các tính năng mới (hệ thống đánh giá game, leaderboard).
- **User Support**
    - Cung cấp hỗ trợ qua hệ thống ticket cho người dùng gặp vấn đề.