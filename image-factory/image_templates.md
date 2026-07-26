# IMAGE TEMPLATES — MẪU ẢNH (IMAGE FACTORY)

> Tải lên khu **Files** của Image Factory. Khung mẫu để chọn nhanh loại ảnh cần tạo.
> Mọi mẫu theo `image_style_rules.md` + `core-brain/image_style_bible.md` (nếu có nhân vật).
> **Aspect Ratio ghi ở mỗi mẫu là mặc định** — không tự đổi tỷ lệ trừ khi được yêu cầu rõ, để
> ảnh cùng loại luôn đồng nhất kích thước giữa các lần sinh.
> Cập nhật: 05/07/2026.
> Cập nhật: 14/07/2026 — Mẫu B (Thumbnail bài viết = Featured Image) chuyển hẳn sang
> `featured-Image-factory/`; Mẫu E (Blog Cover/OG) chỉ còn dùng cho trường hợp ngoại lệ cần
> ảnh OG khác Featured Image.

---

## MẪU A — HERO BANNER

- **Dùng cho:** đầu trang chủ / đầu trang chuyên mục.
- **Aspect Ratio mặc định:** 21:9 (hoặc 16:9 nếu nền tảng không hỗ trợ 21:9).
- Bối cảnh rộng, nhiều khoảng trống, có thể có nhân vật ở góc khung (không che nội dung/text overlay).

## MẪU B — THUMBNAIL BÀI VIẾT (⚠️ CHUYỂN SANG `featured-Image-factory/` TỪ 14/07/2026)

- Đây chính là "Featured Image" — không còn tạo ở Image Factory nữa, xem
  `featured-Image-factory/instructions_FEATURED_IMAGE.md`.
- Giữ lại mục này chỉ để tránh nhầm khi có người tìm "Mẫu B" theo thói quen cũ.

## MẪU C — CATEGORY THUMBNAIL

- **Dùng cho:** ảnh đại diện chuyên mục (Sức khỏe, Tâm lý, Dưỡng sinh...).
- **Aspect Ratio mặc định:** 1:1.
- Đơn giản, mang tính biểu tượng (icon-like), một prop đại diện chủ đề (VD: tách trà cho Dưỡng sinh).

## MẪU D — PRODUCT (⚠️ chỉ dùng khi phạm vi affiliate/sản phẩm đã được xác nhận rõ)

- **Dùng cho:** ảnh sản phẩm (nếu Image Factory được giao việc này).
- **Aspect Ratio mặc định:** 1:1 hoặc 4:5.
- Nền sạch, ánh sáng đều, không dàn cảnh quảng cáo giật gân — vẫn giữ tinh thần 95/5 CORE_BRAIN.

## MẪU E — BLOG COVER (Open Graph) — CHỈ DÙNG KHI CẦN ẢNH OG RIÊNG, KHÁC FEATURED IMAGE

- **Dùng cho:** ảnh chia sẻ mạng xã hội, CHỈ khi bài cần một ảnh OG khác hẳn Featured Image
  (trường hợp ngoại lệ). Mặc định, Featured Image (từ `featured-Image-factory/`) đã tự động
  dùng luôn làm ảnh chia sẻ mạng xã hội — không cần tạo thêm Mẫu E trừ khi có lý do cụ thể.
- **Aspect Ratio mặc định:** 1.91:1 (chuẩn OG).
- Giống Hero Banner nhưng theo đúng chủ đề riêng của từng bài, không dùng ảnh chung chung.

## MẪU F — AVATAR

- **Dùng cho:** ảnh đại diện thương hiệu trên các nền tảng (Facebook Page, YouTube...).
- **Aspect Ratio mặc định:** 1:1.
- Cận mặt/vai nhân vật chính — **bắt buộc theo `core-brain/image_style_bible.md`**, dùng cố định lâu dài,
  không tạo biến thể mới liên tục (mất nhận diện thương hiệu).

## MẪU G — QUOTE IMAGE

- **Dùng cho:** ảnh có câu chốt trích từ `anh_minh_quotes.md`, đăng community/social.
- **Aspect Ratio mặc định:** 1:1 hoặc 4:5.
- Nền tối giản, có khoảng trống rõ để chèn chữ (chữ do bước sau overlay, ảnh nền không tự vẽ chữ).

## MẪU H — COMPARISON

- **Dùng cho:** minh họa bài dạng so sánh (khớp Mẫu I của `seo-factory/article_templates.md`).
- **Aspect Ratio mặc định:** 16:9.
- Bố cục chia đôi cân xứng, hai chủ thể đối xứng, không thiên vị hình ảnh cho bên nào.

## MẪU I — INFOGRAPHIC

- **Dùng cho:** minh họa bài dạng checklist (khớp Mẫu H của `seo-factory/article_templates.md`).
- **Aspect Ratio mặc định:** 4:5 hoặc 1:1.
- Dạng liệt kê trực quan, tối giản, dễ đọc khi thu nhỏ trên feed.

## MẪU J — BEFORE / AFTER (dùng khi cần — thận trọng)

- **Aspect Ratio mặc định:** 1:1 (chia đôi trái/phải).
- ⚠️ KHÔNG dùng cho nội dung sức khỏe/giảm cân/điều trị — dễ tạo hiểu lầm cam kết y khoa,
  phạm ranh giới CORE_BRAIN. Chỉ dùng cho ngữ cảnh trung tính (VD: trước/sau dọn vườn, trước/sau sắp xếp góc trà).

## MẪU K — INLINE IMAGE (ảnh chèn giữa bài)

- **Dùng cho:** ảnh nhỏ chèn giữa thân bài để ngắt đoạn văn dài — KHÁC Thumbnail (đại diện
  ngoài trang danh sách) và KHÁC Hero/Blog Cover (đầu trang). Dùng khi bài dài, cần một điểm
  dừng mắt giữa hai đoạn.
- **Aspect Ratio mặc định:** 4:3 hoặc 16:9 (nhỏ hơn Hero, không chiếm hết chiều rộng bài).
- Một chi tiết đơn giản liên quan trực tiếp đoạn văn ngay trên/dưới nó — không lặp lại y hệt
  Hero/Thumbnail của cùng bài (tránh cảm giác dùng đi dùng lại một ảnh).

---

## LƯU Ý DÙNG MẪU

- Chọn mẫu theo mục đích sử dụng thực tế, không đoán.
- Aspect Ratio ở trên là mặc định cho `output_schema.md` — chỉ đổi khi có yêu cầu tường minh.
- Mỗi bài chốt bằng `image_checklist.md` trước khi xuất.
