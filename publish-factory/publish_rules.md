# PUBLISH RULES — ĐIỀU KIỆN BẮT BUỘC ĐỂ XUẤT BẢN (PUBLISH FACTORY)

> Tải lên khu **Files** của Publish Factory. Đây là **gate rules** — điều kiện chặn cứng, không
> có ngoại lệ trừ khi người phụ trách xác nhận rõ ràng chấp nhận rủi ro.
> Cập nhật: 04/07/2026.

---

## 1. GATE THEO REVIEW FACTORY (quan trọng nhất)

- **Chỉ publish khi TẤT CẢ kết quả Review liên quan tới bài này** (SEO, Image, Video nếu có
  thumbnail/video riêng) đều ở mức **PASS hoặc PASS WITH NOTE**.
- Nếu bất kỳ kết quả nào là **NEED FIX hoặc FAIL** → **KHÔNG PUBLISH**, trả bài lại cho Factory
  gốc, không tự sửa thay.
- Nếu một phần nội dung (VD: thumbnail) **chưa có kết quả Review nào** → coi như chưa đạt điều
  kiện, không tự suy đoán là PASS.

## 2. GATE THEO METADATA BẮT BUỘC

Thiếu bất kỳ mục nào dưới đây → **KHÔNG PUBLISH**:

- ☐ Title
- ☐ Slug
- ☐ Meta Description
- ☐ Category (không được rỗng)
- ☐ Body (không rỗng, không phải nội dung placeholder)
- ☐ Thumbnail / Featured Image (trừ loại nội dung không cần ảnh, phải xác nhận rõ trường hợp này)

## 3. KHÔNG TỰ BỔ SUNG NỘI DUNG THIẾU

- Nếu thiếu Title/Meta/Slug — Publish Factory **không tự viết thay**. Báo lại cho SEO Factory
  (hoặc Factory tương ứng) để bổ sung, sau đó review lại nếu cần.
- Publish Factory chỉ tự bổ sung **metadata kỹ thuật** không thuộc phạm vi Factory nào khác
  (Canonical URL, Open Graph, Twitter Card — xem `metadata_rules.md`), không tự bổ sung nội
  dung sáng tạo.

## 4. KHÔNG TỰ ĐÁNH GIÁ CHẤT LƯỢNG NỘI DUNG

Publish Factory không đọc lại Body để tự chấm "bài này hay/dở/đúng chuẩn không" — việc đó đã
xong ở Review Factory. Publish Factory chỉ kiểm **sự hiện diện & tính hợp lệ hình thức** của
field, không đánh giá lại nội dung bên trong.

## 5. INVALIDATION RULE — NỘI DUNG ĐỔI SAU REVIEW THÌ VERDICT CŨ MẤT HIỆU LỰC

Một verdict Review chỉ đúng cho **đúng phiên bản nội dung** tại thời điểm review, không đúng
mãi mãi. Tình huống cần chặn: bài đã Review PASS, nhưng sau đó (vài phút hay vài tuần sau)
SEO Factory hoặc người dùng sửa lại Body/Title/Meta — verdict PASS cũ giờ mô tả một nội dung
không còn tồn tại.

- Mỗi kết quả Review phải kèm **phiên bản nội dung tại thời điểm review** (`reviewed_version`,
  xem `output_schema.md` mục 13).
- Trước khi cho phép publish, đối chiếu `content_queue.content_version` **hiện tại** với
  `reviewed_version` của mọi kết quả Review liên quan.
- Nếu **khác nhau** (nội dung đã đổi sau khi review) → verdict cũ **mất hiệu lực ngay lập tức**,
  coi như **chưa có Review nào** (áp dụng mục 1) — **KHÔNG PUBLISH**, bắt buộc gửi lại Review
  Factory để review lại phiên bản mới trước khi có thể publish.
- Áp dụng dù thay đổi nhỏ (sửa một lỗi chính tả tiêu đề) — không tự đánh giá "thay đổi nhỏ chắc
  không sao", vì đó lại chính là việc tự đánh giá chất lượng nội dung mà Publish Factory không
  được làm (mục 4).

---

## TÓM TẮT

```
Thiếu field bắt buộc                → KHÔNG PUBLISH
Có Review NEED FIX/FAIL             → KHÔNG PUBLISH
Chưa có Review nào                  → KHÔNG PUBLISH
Nội dung đổi sau khi Review (mục 5) → verdict cũ mất hiệu lực, coi như CHƯA CÓ REVIEW → KHÔNG PUBLISH
Đủ field + mọi Review PASS/PASS WITH NOTE + verdict còn khớp phiên bản hiện tại
                                     → ĐỦ ĐIỀU KIỆN, chuyển sang scheduling_rules.md
```
