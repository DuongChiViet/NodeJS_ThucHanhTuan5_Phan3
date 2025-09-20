# Hệ Thống Quản Lý Sản Phẩm & Nhà Cung Cấp Duong Chi Viet

Ứng dụng web quản lý sản phẩm và nhà cung cấp với đầy đủ tính năng CRUD, xác thực người dùng và bảo mật phiên làm việc.

## Tính Năng

- **Quản lý sản phẩm**: Thêm, sửa, xóa, xem danh sách sản phẩm
- **Quản lý nhà cung cấp**: Thêm, sửa, xóa, xem danh sách nhà cung cấp  
- **Tìm kiếm & lọc**: Tìm kiếm sản phẩm theo tên, lọc theo nhà cung cấp
- **Xác thực người dùng**: Đăng ký, đăng nhập, đăng xuất
- **Bảo mật**: Tất cả chức năng CRUD yêu cầu đăng nhập
- **Quên mật khẩu**: Đặt lại mật khẩu qua email

## Công Nghệ

- **Backend**: Node.js, Express.js
- **Database**: MongoDB với Mongoose ODM
- **Template Engine**: EJS
- **UI Framework**: Bootstrap 5
- **Authentication**: bcryptjs, express-session
- **Email**: nodemailer

## Cài Đặt

1. **Clone repository**
```bash
git clone <repository-url>
cd node-mvc-crud-product-supplier
```

2. **Cài đặt dependencies**
```bash
npm install
```

3. **Tạo file .env**
```env
MONGO_URI=mongodb://localhost:27017/product_supplier_db
SESSION_SECRET=your-secret-key
```

4. **Seed dữ liệu mẫu**
```bash
npm run seed
```

5. **Khởi động ứng dụng**
```bash
npm start
```

Truy cập: http://localhost:3000

## Tài Khoản Demo

- **Username**: admin
- **Password**: 123456
- **Email**: admin@example.com

## Cấu Trúc Thư Mục

```
├── app.js              # File chính
├── package.json        # Dependencies
├── seed.js            # Dữ liệu mẫu
├── config/            # Cấu hình
├── controllers/       # Controllers
├── middleware/        # Middleware
├── models/           # Models
├── routes/           # Routes
├── views/            # Templates EJS
└── public/           # Static files
```

## API Routes

### Authentication
- `GET /auth/login` - Trang đăng nhập
- `POST /auth/login` - Xử lý đăng nhập
- `GET /auth/register` - Trang đăng ký
- `POST /auth/register` - Xử lý đăng ký
- `GET /auth/logout` - Đăng xuất

### Products (Yêu cầu đăng nhập)
- `GET /products` - Danh sách sản phẩm
- `GET /products/new` - Form tạo sản phẩm
- `POST /products` - Tạo sản phẩm mới
- `GET /products/:id/edit` - Form sửa sản phẩm
- `PUT /products/:id` - Cập nhật sản phẩm
- `DELETE /products/:id` - Xóa sản phẩm

### Suppliers (Yêu cầu đăng nhập)
- `GET /suppliers` - Danh sách nhà cung cấp
- `GET /suppliers/new` - Form tạo nhà cung cấp
- `POST /suppliers` - Tạo nhà cung cấp mới
- `GET /suppliers/:id/edit` - Form sửa nhà cung cấp
- `PUT /suppliers/:id` - Cập nhật nhà cung cấp
- `DELETE /suppliers/:id` - Xóa nhà cung cấp

---

*Ứng dụng được phát triển với mục đích học tập và thực hành.*
