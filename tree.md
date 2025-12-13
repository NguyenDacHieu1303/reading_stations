lib/
├── config/                 # Cấu hình toàn bộ App (Routes, Theme)
│   ├── routes.dart         # Quản lý đường dẫn (Navigator)
│   └── theme.dart          # Cấu hình ThemeData chung
│
├── models/                 # Chứa các Class mô tả dữ liệu
│   ├── user_model.dart     # Thông tin người dùng (Avatar, tên, id...)
│   ├── book_model.dart     # Thông tin sách (Tựa, tác giả, ảnh, tiến độ...)
│   ├── post_model.dart     # Bài đăng trong phần Cộng đồng
│   └── review_stat.dart    # Dữ liệu thống kê cho màn hình Ôn tập
│
├── view_models/            # Logic xử lý (Provider/ChangeNotifier)
│   ├── auth_view_model.dart    # Xử lý Đăng nhập/Đăng ký
│   ├── home_view_model.dart    # Logic load sách trang chủ
│   ├── library_view_model.dart # Logic lọc sách (Đang đọc, Muốn đọc...)
│   ├── review_view_model.dart  # Logic tính toán biểu đồ ôn tập
│   └── profile_view_model.dart # Logic cập nhật hồ sơ
│
├── views/                  # Giao diện (UI)
│   ├── screens/            # Các màn hình chính (Phân theo tính năng)
│   │   ├── auth/           # Nhóm màn hình xác thực
│   │   │   ├── welcome_screen.dart  # Màn hình Chào mừng 
│   │   │   ├── login_screen.dart    # Màn hình Đăng nhập 
│   │   │   └── register_screen.dart # Màn hình Đăng ký 
│   │   │
│   │   ├── main_screen.dart         # Màn hình chứa Bottom Navigation Bar
│   │   │
│   │   ├── home/           # Nhóm Trang chủ
│   │   │   └── home_screen.dart
│   │   │
│   │   ├── library/        # Nhóm Thư viện 
│   │   │   ├── library_screen.dart
│   │   │   └── widgets/    # Widget riêng cho Library (Tab con)
│   │   │       ├── reading_tab.dart
│   │   │       └── wishlist_tab.dart
│   │   │
│   │   ├── review/         # Nhóm Ôn tập 
│   │   │   └── review_screen.dart
│   │   │
│   │   ├── community/      # Nhóm Cộng đồng 
│   │   │   └── community_screen.dart
│   │   │
│   │   └── profile/        # Nhóm Hồ sơ 
│   │       └── profile_screen.dart
│   │
│   └── widgets/            # Các Widget dùng chung cho toàn App (Reusable)
│       ├── buttons/
│       │   ├── primary_button.dart  # Nút xanh dương lớn (Đăng nhập/Đăng ký)
│       │   └── social_button.dart   # Nút Google/Facebook
│       │
│       ├── cards/
│       │   ├── book_card_vertical.dart   # Card sách đứng (Trong Thư viện)
│       │   ├── book_card_horizontal.dart # Card sách ngang (Gợi ý/List)
│       │   └── post_card.dart            # Card bài đăng cộng đồng
│       │
│       └── inputs/
│           └── custom_text_field.dart    # Ô nhập liệu (Email, Pass)
│
├── services/               # Xử lý dữ liệu (API, Local Storage) - Nâng cao
│   ├── api_service.dart    # Gọi API backend (nếu có)
│   └── local_storage.dart  # Lưu token đăng nhập, settings
│
├── utils/                  # Tiện ích bổ trợ
│   ├── app_colors.dart     # Bảng màu (Xanh, Xám, Trắng...)
│   ├── app_styles.dart     # TextStyles (H1, H2, Body...)
│   ├── app_assets.dart     # Đường dẫn ảnh (assets/images/logo.png...)
│   └── validators.dart     # Hàm kiểm tra email/pass hợp lệ
│
└── main.dart               # Điểm khởi chạy ứng dụng