# OUTPUT SCHEMA — CHUẨN ĐẦU RA PUBLISH FACTORY

> Tải lên khu **Files** của Publish Factory. Quy định khuôn xuất gói dữ liệu cuối cùng — để n8n
> đọc và đẩy thẳng lên CMS.
> Cập nhật: 04/07/2026.

---

## KHUÔN XUẤT CHUẨN

Mỗi bài xuất ra theo đúng thứ tự field dưới đây. Không thiếu field, không đổi tên field,
không thêm field ngoài danh sách.

1. **Content ID** — khóa nội bộ ổn định của bài, **lấy nguyên từ `content_queue.id` đã có sẵn**
   (được tạo từ lúc SEO Factory lưu draft ở WF-04) — Publish Factory KHÔNG tự sinh ID mới, chỉ
   mang theo. Dùng ID này để join dữ liệu, không dùng Slug làm khóa (Slug có thể đổi vì lý do SEO).
2. **Version** — số phiên bản nội dung hiện tại (VD: `v1.0`, `v1.1` sau khi sửa), lấy từ
   `content_queue.content_version`. Dùng để đối chiếu "phiên bản đã Review" — xem Invalidation
   Rule ở `publish_rules.md` mục 5.
3. **Publish Status** — `Ready to Publish` / `Scheduled` / `Blocked` (theo `publish_rules.md`).
4. **Publish Time** — thời điểm xuất bản cụ thể, hoặc `Immediately` (theo `scheduling_rules.md`).
5. **Target** — kênh xuất bản, hiện tại luôn là `Website` (theo `publishing_targets.md`).
6. **Category** — lấy nguyên từ SEO Factory, chỉ kiểm tra không rỗng.
7. **Slug** — lấy nguyên từ SEO Factory.
8. **Thumbnail** — lấy nguyên từ Image Factory (Featured Image).
9. **Meta** — Title + Meta Description, lấy nguyên từ SEO Factory.
10. **OG** — OG title/description/image (theo `metadata_rules.md` mục 2).
11. **Canonical** — URL chuẩn nếu đã biết, để trống nếu chưa (theo `metadata_rules.md` mục 3).
12. **Tags** — lấy nguyên từ SEO Factory.
13. **Review Status** — tổng hợp verdict của mọi kết quả Review liên quan (VD:
    `SEO: PASS · Image: PASS WITH NOTE`), kèm **phiên bản đã review** (VD: `reviewed at v1.0`)
    để đối chiếu Invalidation Rule — nếu Version hiện tại (field 2) khác phiên bản đã review,
    xem `publish_rules.md` mục 5 trước khi tin Review Status này.
14. **Publish Package** — toàn bộ gói trên đóng gói dạng JSON phẳng (mặc định định dạng
    **JSON** — đây là *định dạng đóng gói*, không phải kênh riêng; Target ở field 5 vẫn luôn
    là Website, xem `publishing_targets.md` mục 2), để pipeline đọc trực tiếp không cần parse thêm.

---

## QUY TẮC ĐÓNG GÓI

- Nếu **Publish Status = Blocked** → vẫn xuất đủ khuôn, nhưng ghi rõ lý do chặn ở field
  **Publish Status** (VD: `Blocked — thiếu Thumbnail`), để n8n dừng lại đúng chỗ thay vì lỗi ngầm.
- Không tự đoán field còn thiếu — để trống và để `Publish Status` phản ánh đúng tình trạng thật.
- **Publish Package** phải phản ánh chính xác 13 field còn lại phía trên, không thêm/bớt thông
  tin khi đóng gói.
