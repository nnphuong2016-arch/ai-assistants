# REVIEW CHECKLISTS — ĐIỀU HƯỚNG THEO LOẠI NỘI DUNG (REVIEW FACTORY)

> Tải lên khu **Files** của Review Factory. File này CHỈ điều hướng: loại nội dung nào → dùng
> nguyên checklist gốc của Factory đó, cộng thêm (nếu có) **tiêu chí Review-riêng** — tức tiêu
> chí KHÔNG có trong checklist gốc, chỉ có ý nghĩa khi một bên độc lập kiểm tra lại. File này
> KHÔNG liệt kê lại toàn bộ tiêu chí gốc — làm vậy sẽ phình dài (300–400 dòng khi có thêm
> Podcast/Email/Chat Factory...) và tạo nguy cơ hai nơi định nghĩa cùng một chuẩn rồi trôi lệch
> nhau khi Factory gốc cập nhật checklist mà file này quên cập nhật theo.
> Cập nhật: 05/07/2026.

---

## SEO

**Dùng nguyên:** `seo-factory/seo_checklist.md` (đối chiếu chi tiết thêm với `output_schema.md`,
`web_content_rules.md`, `keyword_strategy.md`, `internal_link_rules.md` khi cần).

**Review-riêng (không có trong checklist gốc):**
- Claim y khoa vượt mức (chẩn đoán/kê đơn/cam kết điều trị) — **luôn kiểm độc lập lần 2** dù
  `seo_checklist.md` đã có mục này, vì đây là điểm compliance nhạy cảm nhất trong toàn hệ thống.
- **Content Quality (chỉ ghi vào Suggestions, KHÔNG ảnh hưởng Final Decision):** đối chiếu
  `seo-factory/writing_craft_examples.md` — nhịp đoạn có lặp khuôn 3 lần liên tiếp không, có câu
  nghe sáo AI không, có Information Gap không. Đây là chất lượng biên tập, không phải tiêu chí
  an toàn/schema — theo đúng `review_rules.md` mục 1 ("không đánh giá hay/dở theo cảm nhận"),
  tuyệt đối không dùng để hạ PASS xuống NEED FIX/FAIL. Chỉ ghi nhận ở khối **Suggestions** của
  `output_schema.md` để người phụ trách tham khảo.

## IMAGE

**Dùng nguyên:** `image-factory/image_checklist.md` (đối chiếu thêm `image_style_rules.md`,
`image_templates.md`, `core-brain/image_style_bible.md`, `output_schema.md` khi cần).

**Review-riêng:** không có — tin tưởng checklist gốc đã đủ.

## VIDEO

**Dùng nguyên:** `video-factory/video_rules.md` (đối chiếu thêm `core-brain/image_style_bible.md`; nếu có
thumbnail đi kèm, đối chiếu thêm `image-factory/image_checklist.md`).

**Review-riêng:** không có.

## COMMUNITY

**Dùng nguyên:** `community-factory/community_rules.md`, `engagement_rules.md` (đối chiếu thêm
`core-brain/dong_hanh_nguoi_benh.md` nếu chạm chủ đề nặng).

**Review-riêng:** không có.

## PUBLISH PACKAGE (MỚI — Pre-flight Check, KHÔNG review lại nội dung)

Lượt review cuối cùng, chạy SAU khi Publish Factory đã đóng gói xong, TRƯỚC khi Automation
(n8n) thực hiện đăng thật. Đây KHÔNG phải kiểm lại chất lượng nội dung (đã xong ở các lượt
review phía trên) — chỉ kiểm **cấu trúc gói có đúng không**, giống một "pre-flight check":

**Dùng nguyên:** `publish-factory/output_schema.md`.

**Chỉ kiểm:**
- Đủ field theo đúng thứ tự `output_schema.md`, không thiếu?
- Publish Package (JSON) hợp lệ — parse được, đúng kiểu dữ liệu từng field?
- Thumbnail/Featured Image có mặt (nếu loại nội dung cần ảnh)?
- Content ID + Version có mặt, và Version khớp `reviewed_version` (không bị Invalidation Rule
  ở `publish-factory/publish_rules.md` mục 5 — nếu lệch, đây tự nó đã là lỗi Critical: nghĩa là
  nội dung đổi sau review mà không ai bắt được)?

---

## FACTORY MỚI RA ĐỜI SAU NÀY

Chỉ cần thêm một mục mới (2–4 dòng): **Dùng nguyên:** file checklist/schema gốc của Factory đó.
**Review-riêng:** liệt kê đúng những tiêu chí KHÔNG có sẵn trong checklist gốc (nếu có) — không
liệt kê lại toàn bộ tiêu chí gốc. Không tạo Review Factory riêng cho loại nội dung mới.
