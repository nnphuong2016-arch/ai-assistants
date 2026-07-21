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
5. **Category** — một trong 5 trụ nội dung (Sức khỏe / Tâm lý & đời sống / Dưỡng sinh /
   Triết lý phương Đông / Đồng hành tuổi già & người bệnh) hoặc tầng Relationship/Brand nếu
   dùng Mẫu F/G.
6. **Tags** — 3–6 tag, gồm primary keyword + secondary keyword liên quan.
7. **Body** — toàn văn bài viết (H1 không lặp lại trong Body nếu Title đã đóng vai H1; heading
   dùng markdown `##`/`###`), đã qua `seo_checklist.md`.
8. **FAQ** — dạng danh sách câu hỏi/câu trả lời riêng biệt khỏi Body, để pipeline có thể tách
   ra dựng FAQ schema (Question/Answer từng cặp).
9. **References (optional)** — nguồn đã dẫn khi có thông tin sức khỏe/nghiên cứu (tên nguồn,
   không cần URL nếu không có URL thật — không bịa link). Nhiều bài (Mẫu C/F/G — triết lý,
   câu chuyện, nhật ký) không có nguồn khoa học nào — để trống, KHÔNG cố tìm nguồn cho có.
10. **Featured Image** — mô tả/từ khóa ảnh cần dùng cho bài (VD: "tách trà cạnh cửa sổ nắng
    sớm"), không phải tên file thật — AI không biết ảnh nào đã tồn tại. Image Factory chọn/tạo
    ảnh dựa trên mô tả này.

---

## QUY TẮC ĐÓNG GÓI

- Field nào không áp dụng cho loại bài (VD: Mẫu G Nhật ký thường không có FAQ) → để trống,
  không xóa field khỏi khuôn.
- Body là văn bản thuần 100% chữ liền mạch — KHÔNG markdown, KHÔNG HTML, KHÔNG bất kỳ ký tự
  định dạng/phân cách nào (`#`, `-`, `--`, `—`, `*`, `•`...), theo `web_content_rules.md`
  mục 3D — pipeline giọng đọc cần đọc được nguyên văn không vấp ký tự lạ.
- Không chèn disclaimer/ngày cập nhật như field riêng — chúng nằm trong Body, ở vị trí đã
  quy định tại `web_content_rules.md` và `article_templates.md`.
- **Reading Time không nằm trong khuôn xuất** — pipeline/CMS tự tính từ độ dài `Body`
  (khoảng 200–250 từ/phút). Không để AI tự ước lượng số phút đọc, vì AI đếm từ không đáng tin.
