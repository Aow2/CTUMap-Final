# CTUMap-Final
Ứng dụng bản đồ dành cho sinh viên và cán bộ tại Đại học Cần Thơ (CTU), giúp tìm kiếm các tòa nhà, khoa, và chỉ dẫn đường đi một cách nhanh chóng và chính xác (Outdoor). Bên cạnh đó, ứng dụng được phát triển tính năng định vị bên trong tòa nhà kết hợp trải nghiệm UI 360 Virtual Tour thay vì chỉ là navigate đơn thuần (Indoor).

## Tính năng nổi bật
### Oudoor: 
* ***Bản đồ trực quan***: Hiển thị chi tiết khuôn viên khu II - Đại học Cần Thơ.
* ***Tìm kiếm thông minh***: Tìm nhanh các địa điểm như Hội trường rùa, Nhà học B1, Khoa CNTT&TT...
* ***Chỉ đường nội khu***: Tính toán và hiển thị đường đi ngắn nhất giữa các vị trí.
* ***Thông tin địa điểm***: Xem hình ảnh và mô tả chi tiết của từng tòa nhà khi chọn trên bản đồ.
* ***Định vị GPS***: Xác định vị trí hiện tại của người dùng trong khuôn viên trường.
### Indoor:
* **Virtual Tour 360°**: Trải nghiệm không gian bên trong tòa nhà bằng ảnh panorama 360°.
* **Tìm đường thông minh**: Tính toán tuyến đường ngắn nhất giữa các phòng bằng thuật toán BFS.
* **Hotspot Navigation**: Điều hướng giữa các panorama thông qua hệ thống hotspot liên kết.
* **Sơ đồ tầng tương tác**: Hiển thị vị trí, điểm đến và lộ trình ngay trên sơ đồ tầng.
* **Hướng dẫn trực quan**: Kết hợp Virtual Tour và sơ đồ tầng để hỗ trợ người dùng di chuyển dễ dàng.
* **Tích hợp với bản đồ ngoài trời**: Chuyển tiếp từ điều hướng ngoài trời đến trong nhà một cách liền mạch

## Công nghệ sử dụng
### Android
- **Ngôn ngữ**: Kotlin
- **UI Framework**: Jetpack Compose
- **Kiến trúc**: MVVM (Model–View–ViewModel)
- **Bất đồng bộ**: Kotlin Coroutines & StateFlow
- **Định vị**: Fused Location Provider (GPS)

### Outdoor Navigation
- **Map SDK**: Mapbox Maps SDK for Android
- **Routing**: Mapbox Directions API
- **Nguồn dữ liệu bản đồ**: OpenStreetMap (OSM)

### Indoor Navigation
- **Web Integration**: Android WebView
- **Web Technologies**: HTML5, CSS3, JavaScript
- **Panorama Viewer**: Pannellum
- **Indoor Map**: Leaflet.js
- **Pathfinding Algorithm**: Breadth-First Search (BFS)

### Backend & Cloud
- **Database**: Firebase Realtime Database
- **Image Hosting**: Cloudinary

## Hướng dẫn cài đặt

### 1. Yêu cầu hệ thống
* Android Studio Ladybug (hoặc mới hơn)
* JDK 17
* Android SDK 24+ (Android 7.0 trở lên)

### 2. Thiết lập Access Token
Dự án sử dụng Mapbox cần cấu hình Token để bản đồ hiển thị:

1.  Mở file `local.properties` trong thư mục gốc của dự án.
2.  Thêm dòng sau vào cuối file:
    ```properties
    MAP_ACCESS_TOKEN=your_mapbox_access_token_here
    ```

### 3. Build & Run
* Nhấn **Sync Project with Gradle Files** trong Android Studio.
* Chọn thiết bị (máy ảo hoặc máy thật) và nhấn **Run (Shift + F10)**.

---
💻 **Tác giả:** Trần Thảo My - Sinh viên Trường CNTT&TT - Đại học Cần Thơ
