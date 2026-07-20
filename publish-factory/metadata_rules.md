# METADATA RULES — HOÀN THIỆN METADATA KỸ THUẬT (PUBLISH FACTORY)

> Tải lên khu **Files** của Publish Factory. File này chia rõ 2 nhóm metadata: nhóm ĐÃ có sẵn
> từ Factory khác (chỉ kiểm tra sự hiện diện, không tự sửa) và nhóm Publish Factory **tự hoàn
> thiện** (kỹ thuật xuất bản, không thuộc phạm vi Factory nào khác).
> Cập nhật: 04/07/2026.
> Cập nhật: 20/07/2026 — sửa nguồn Featured Image: từ 14/07/2026, Featured Image do
> `featured-image-factory/` (Factory riêng, độc lập) tạo ra, KHÔNG còn phải Image Factory.

---

## 1. NHÓM ĐÃ CÓ SẴN — CHỈ KIỂM TRA, KHÔNG TỰ SỬA

Những field này do SEO Factory / Featured Image Factory tạo ra. Publish Factory chỉ xác nhận có
mặt và không rỗng — nếu thiếu, áp dụng gate ở `publish_rules.md` mục 2, không tự viết thay:

- Title, Slug, Meta Description, Category, Tags (từ SEO Factory).
- Featured Image, Alt Text (từ **Featured Image Factory** — `featured-image-factory/`, KHÔNG
  phải Image Factory).

## 2. NHÓM PUBLISH FACTORY TỰ HOÀN THIỆN (kỹ thuật xuất bản)

Đây là các field **không thuộc phạm vi** SEO/Image Factory — vì chúng là chi tiết kỹ thuật của
việc xuất bản, không phải chiến lược nội dung/hình ảnh:

- **Canonical URL** — URL chuẩn của bài (tránh trùng lặp nội dung nếu có nhiều URL trỏ tới cùng bài).
- **Open Graph (OG title, OG description, OG image)** — mặc định lấy từ Title/Meta Description/
  Featured Image đã có, chỉ rút gọn độ dài nếu cần (OG description ngắn hơn Meta một chút là ổn).
- **Twitter Card** — tương tự OG, dùng lại dữ liệu đã có, không tự sáng tác nội dung mới.

## 3. NGUYÊN TẮC

- Không tự sáng tạo nội dung mới cho OG/Twitter Card — luôn tái sử dụng Title/Meta/Featured
  Image đã có, chỉ điều chỉnh độ dài/định dạng cho khớp chuẩn kỹ thuật từng nền tảng.
- Nếu Canonical URL chưa xác định được (chưa biết slug cuối cùng trên CMS thật) → để trống,
  ghi chú "n8n điền sau khi biết URL thật", không tự bịa URL giả.
