# OUTPUT SCHEMA — CHUẨN ĐẦU RA SEO FACTORY

> Tải lên khu **Files** của SEO Factory. Quy định khuôn xuất cuối cùng của mọi bài — để n8n
> (hoặc bất kỳ pipeline nào đọc output) luôn nhận đúng field, đúng thứ tự.
> Cập nhật: 04/07/2026.

---

## KHUÔN XUẤT CHUẨN

Mỗi bài xuất ra theo đúng thứ tự field dưới đây. Không thiếu field, không đổi tên field,
không thêm field ngoài danh sách.

1. **Title** — tiêu đề thẻ SEO (50–60 ký tự, theo `keyword_strategy.md` mục 5).
2. **Slug** — theo `keyword_strategy.md` mục 6.
3. **Meta Description** — 150–160 ký tự, theo `keyword_strategy.md` mục 7.
4. **Excerpt** — 1–2 câu tóm tắt để hiển thị ở trang danh sách/preview (khác Meta Description
   — Excerpt hướng người đọc trên site, Meta hướng người tìm trên Google).
5. **Category** — một trong **6 mục nội dung** của hệ thống (Sức khỏe / Tâm lý & đời sống /
   Dưỡng sinh / Triết lý phương Đông / Đồng hành tuổi già & người bệnh / Bếp An Nhiên — khớp
   đúng bảng số chủ đề ở `CLAUDE.md` Bước 5.A), hoặc tầng Relationship/Brand nếu dùng Mẫu F/G.
6. **Tags** — 3–6 tag, gồm primary keyword + secondary keyword liên quan.
7. **Body** — toàn văn bài viết (tiêu đề bài không lặp lại trong Body nếu Title đã đóng vai đó),
   viết **thuần chữ 100%** theo `web_content_rules.md` mục 3D, đã qua `seo_checklist.md`.
8. **FAQ** — dạng danh sách câu hỏi/câu trả lời riêng biệt khỏi Body, để pipeline có thể tách
   ra dựng FAQ schema (Question/Answer từng cặp). Nội dung từng cặp cũng viết thuần chữ như Body.
9. **Internal Links** — danh sách link của bài (2–5 link theo `internal_link_rules.md`), mỗi
   mục gồm `anchor` (cụm chữ có sẵn nguyên văn trong Body) cộng **một trong hai**:
   - `slug` — khi đích là bài khác trên chính website (ưu tiên 1–3 của `internal_link_rules.md`).
   - `url` — khi đích nằm ngoài website: video YouTube (ưu tiên 4) hoặc trang sản phẩm
     (ưu tiên 5). Hai loại này không có slug nội bộ nên bắt buộc ghi URL đầy đủ.

   Không ghi cả hai cho cùng một mục. Tách riêng khỏi Body để Body giữ được thuần chữ; n8n/CMS
   tự bọc thẻ `<a>` vào đúng cụm anchor khi đăng.
10. **References (optional)** — nguồn đã dẫn khi có thông tin sức khỏe/nghiên cứu (tên nguồn,
    không cần URL nếu không có URL thật — không bịa link). Nhiều bài (Mẫu C/F/G — triết lý,
    câu chuyện, nhật ký) không có nguồn khoa học nào — để trống, KHÔNG cố tìm nguồn cho có.
11. **Featured Image** — để trống. SEO Factory KHÔNG tự mô tả ảnh nữa: Featured Image Factory
    nhận đúng **tên file/slug bài viết** làm input rồi tự suy ra concept, prompt và filename
    (xem `CLAUDE.md` Bước 5.5 + `featured-Image-factory/input_schema.md`). Giữ field trong khuôn
    để pipeline điền ngược lại tên file ảnh sau khi ảnh đã được tạo.

---

## QUY TẮC ĐÓNG GÓI

- Field nào không áp dụng cho loại bài (VD: Mẫu G Nhật ký thường không có FAQ) → để trống,
  không xóa field khỏi khuôn.
- Body là văn bản thuần 100% chữ liền mạch — KHÔNG markdown, KHÔNG HTML, KHÔNG bất kỳ ký tự
  định dạng/phân cách nào (`#`, `-`, `--`, `—`, `*`, `•`...), theo `web_content_rules.md`
  mục 3D — pipeline giọng đọc cần đọc được nguyên văn không vấp ký tự lạ.
- Không chèn disclaimer như field riêng — nằm trong Body, ở vị trí đã quy định tại
  `web_content_rules.md` và `article_templates.md`. Không còn field/dòng "ngày cập nhật" (bỏ
  11/08/2026 — bài SEO không còn ghi "Cập nhật: ..." ở cuối nữa).
- **Reading Time không nằm trong khuôn xuất** — pipeline/CMS tự tính từ độ dài `Body`
  (khoảng 200–250 từ/phút). Không để AI tự ước lượng số phút đọc, vì AI đếm từ không đáng tin.
