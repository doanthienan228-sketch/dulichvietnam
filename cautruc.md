# Trang web Du lịch Việt Nam

Trang web hiện đại, responsive, toàn bộ nội dung và giao diện bằng tiếng Việt, giới thiệu điểm du lịch nổi tiếng trên các tỉnh thành Việt Nam.

## Tính năng

- **Trang chủ** – Giới thiệu Vietnam’s tourism, banner hero, điểm đến nổi bật và thẻ vùng miền
- **Điều hướng** – Miền Bắc, Miền Trung, Miền Nam và Bản đồ tương tác
- **Trang điểm đến** – 12 điểm với nội dung tiếng Việt đầy đủ:
  - Ảnh hero, mô tả, địa danh nổi bật, nét văn hóa, mẹo du lịch (tự động từ `data/destinations.json`)
  - **Thư viện ảnh** – Carousel và lưới ảnh (phong cảnh, địa danh, văn hóa, ẩm thực, hoạt động), **lightbox toàn màn hình** (ảnh trước/sau, đóng, phím tắt)
  - **Sự kiện & Lễ hội** – Sự kiện/lễ hội chính theo từng điểm với mô tả, thời gian, ý nghĩa và ảnh
- **Bản đồ tương tác** – Bản đồ Việt Nam với marker (Leaflet) cho 12 điểm đến
- **Tìm kiếm** – Ô tìm kiếm trên header; gõ tỉnh hoặc điểm đến, kết quả dẫn tới trang điểm đến
- **Giao diện** – Bảng màu xanh lá, xanh dương, đất; bố cục gọn, responsive
- **SEO** – HTML ngữ nghĩa, meta description, từ khóa, cấu trúc heading rõ ràng

## Cách chạy (sẵn sàng chạy ngay)

1. **Mở trực tiếp**  
   Mở `index.html` bằng trình duyệt (double-click hoặc kéo vào browser). Điều hướng và tất cả trang HTML hoạt động bình thường.

2. **Tìm kiếm, bản đồ và nội dung động (khuyến nghị)**  
   Để tìm kiếm, bản đồ và nội dung trang điểm đến (từ JSON) hoạt động, cần mở qua HTTP (nhiều trình duyệt chặn `fetch()` với `file://`):
   - **VS Code / Cursor:** Cài “Live Server”, mở thư mục dự án và “Open with Live Server”.
   - **Node:** `npx serve vietnam-tourism` (hoặc `npx http-server vietnam-tourism`), rồi mở địa chỉ hiển thị (vd. http://localhost:3000).
   - **Python 3:** Trong thư mục `vietnam-tourism`, chạy `python -m http.server 8000`, mở http://localhost:8000.

## Project structure

```
vietnam-tourism/
├── index.html          # Trang chủ
├── map.html            # Interactive map page
├── css/
│   └── style.css       # Main styles
├── js/
│   ├── app.js          # Tìm kiếm, bản đồ, base path
│   └── destination.js  # Nội dung trang điểm đến, gallery, lightbox, sự kiện
├── data/
│   └── destinations.json  # All destination content (used by search)
├── regions/
│   ├── northern.html
│   ├── central.html
│   └── southern.html
├── destinations/
│   ├── hanoi.html
│   ├── halong-bay.html
│   ├── sapa.html
│   ├── ninh-binh.html
│   ├── hue.html
│   ├── danang.html
│   ├── hoi-an.html
│   ├── nha-trang.html
│   ├── ho-chi-minh-city.html
│   ├── mekong-delta.html
│   ├── da-lat.html
│   └── phu-quoc.html
└── README.md
```

## Images

Destination hero images use Unsplash URLs for demonstration. For production, replace with your own high-quality images (e.g. in an `images/` folder) and update the `src` in each destination page.

## Credits

- Map: [Leaflet](https://leafletjs.com/) with [OpenStreetMap](https://www.openstreetmap.org/copyright)
- Fonts: [Google Fonts](https://fonts.google.com/) (Playfair Display, Source Sans 3)
- Placeholder images: [Unsplash](https://unsplash.com/)
