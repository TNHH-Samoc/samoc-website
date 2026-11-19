# Website Công ty TNHH Công nghệ - Dịch vụ số SAMOC
*(SAMOC DIGITAL SERVICES - TECHNOLOGY COMPANY LIMITED — Giám đốc: Nguyễn Thành Trung)*

Website giới thiệu công ty công nghệ, tổ chức theo **5 khối ngành**:

1. **Phát triển phần mềm và giải pháp trí tuệ nhân tạo**
2. **Nền tảng phần mềm dịch vụ (SaaS) và hạ tầng điện toán đám mây**
3. **Thiết bị thông minh và tích hợp hệ thống**
4. **Tư vấn chuyển đổi số và tối ưu hóa vận hành**
5. **Đào tạo và nền tảng học tập số**

Có kinh nghiệm tư vấn quốc tế tại **Nam Phi**, **Liberia** và **Namibia** (xem trang Dự án).

## 📁 Cấu trúc dự án

```
New folder/
├── index.html          # Trang chủ (hero, dịch vụ, thống kê, quy trình, đánh giá, CTA)
├── about.html          # Giới thiệu (sứ mệnh, tầm nhìn, giá trị, GĐ Nguyễn Thành Trung)
├── services.html       # 5 khối ngành chi tiết + khóa đào tạo + FAQ
├── projects.html       # Dự án tiêu biểu (có bộ lọc theo lĩnh vực)
├── contact.html        # Liên hệ (form tư vấn + thông tin)
├── assets/
│   ├── css/style.css   # Toàn bộ giao diện (design system, responsive)
│   └── js/main.js      # Tương tác: menu mobile, animation, đếm số, FAQ, form
└── README.md
```

## 🚀 Cách chạy

Đây là website tĩnh (HTML/CSS/JS thuần) — **không cần cài đặt gì**.

- **Cách 1:** Nhấp đúp vào `index.html` để mở bằng trình duyệt.
- **Cách 2 (khuyến nghị):** Chạy máy chủ tĩnh để điều hướng mượt hơn:
  ```powershell
  # Nếu có Python
  python -m http.server 8000
  # rồi mở http://localhost:8000
  ```

## ✨ Tính năng & thiết kế (bản nâng cấp chuyên nghiệp v2)

- **Typography cao cấp:** Plus Jakarta Sans (tiêu đề) · Inter (nội dung) · JetBrains Mono (code) — tải từ Google Fonts.
- **Line icons SVG** đồng bộ (thay toàn bộ emoji), logo SVG monogram có gradient.
- **Bento grid** cho phần dịch vụ, **glassmorphism** + nền lưới + hiệu ứng glow theo phong cách Linear/Apple.
- Micro-animation: reveal khi cuộn, đếm số liệu động, spotlight theo con trỏ trên thẻ bento, header đổ bóng khi cuộn.
- Hoàn toàn **responsive** (máy tính, tablet, điện thoại) + tôn trọng `prefers-reduced-motion`.
- Bộ lọc dự án theo lĩnh vực, accordion FAQ, menu mobile.
- **Form liên hệ gửi mail thật qua Formspree** (AJAX, chống spam honeypot, trạng thái loading, thông báo thành công/lỗi). Khi chưa cấu hình, form chạy ở chế độ demo.

> ⚠️ Font chữ tải từ Google Fonts nên cần internet để hiển thị đẹp nhất. Khi offline, trình duyệt tự fallback sang font hệ thống (vẫn đọc tốt).

## 📨 Kết nối form gửi mail thật (Formspree — miễn phí)

Form ở `contact.html` đã tích hợp sẵn Formspree, chỉ cần dán mã form:

1. Vào **https://formspree.io** → đăng ký (có thể dùng chính `tnhhsamoc@gmail.com`).
2. Bấm **New Form** → đặt tên (vd "SAMOC Website") → email nhận là **tnhhsamoc@gmail.com**.
3. Formspree cho một endpoint dạng `https://formspree.io/f/abcdwxyz` → copy phần mã `abcdwxyz`.
4. Mở `contact.html`, tìm dòng `action="https://formspree.io/f/YOUR_FORM_ID"` và **thay `YOUR_FORM_ID` bằng mã** vừa copy.
5. Mở trang Liên hệ, gửi thử 1 lần → Formspree gửi mail xác nhận về hộp thư; bấm xác nhận là form hoạt động.

> Gói miễn phí Formspree: 50 lượt gửi/tháng. Cần nhiều hơn có thể nâng cấp hoặc chuyển sang EmailJS / backend riêng.

## 🔧 Cần tùy chỉnh trước khi đưa lên mạng

- **Form liên hệ:** dán mã form Formspree (xem mục "Kết nối form gửi mail thật" ở trên).
- **Header bảo mật trên Cloudflare:** khai báo trong tệp `_headers` (Cloudflare áp dụng khi triển khai; `netlify.toml` chỉ có tác dụng nếu dùng Netlify).
- **Mạng xã hội:** phần `.socials` có Facebook, LinkedIn và Zalo. Liên kết LinkedIn đang để `href="#"`; khi có địa chỉ trang, thay `#` trong các thẻ `aria-label="LinkedIn SAMOC"` (8 vị trí trên 7 trang) và thêm `target="_blank" rel="noopener noreferrer"`.
- **Tên miền:** các thẻ canonical/Open Graph, `sitemap.xml`, `robots.txt` đã dùng `https://samocdigital.com/`; nếu đổi tên miền cần thay đồng loạt.
- **Ảnh chia sẻ:** `assets/og-image.png` (1200×630) được xuất từ `assets/og-image.svg`; khi sửa SVG cần xuất lại PNG.
- **Số liệu thật:** số liệu hiện để ở mức trung tính (5 khối ngành, 3 dự án quốc tế…); cập nhật khi có số thực tế.

> ✅ Đã cấu hình sẵn: thông tin liên hệ thật (địa chỉ, `0922 216 123`, `tnhhsamoc@gmail.com` — bấm gọi/gửi mail được), Google Maps nhúng thật, favicon, SEO/Open Graph.

## 🎨 Đổi màu thương hiệu

Mở `assets/css/style.css`, sửa các biến trong `:root` (ví dụ `--c-primary`, `--grad-brand`).
