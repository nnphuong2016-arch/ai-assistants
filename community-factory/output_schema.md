# OUTPUT SCHEMA — CHUẨN ĐẦU RA COMMUNITY FACTORY

> Tải lên khu **Files** của Community Factory. Quy định khuôn xuất cuối cùng của mọi post/reply
> — để n8n (hoặc bất kỳ pipeline nào đọc output) luôn nhận đúng field, đúng thứ tự. Theo đúng
> pattern đã dùng ở SEO/Image/Publish/Research Factory (mỗi Factory có output_schema.md riêng).
> Cập nhật: 04/07/2026.

---

## KHUÔN XUẤT CHUẨN

1. **Platform** — Facebook Page / Facebook Group / Zalo / Newsletter (theo `community_rules.md`
   mục 0).
2. **Content Type** — `Post` (kèm tên mẫu A–L đã dùng, xem `social_templates.md`) hoặc
   `Comment Reply` hoặc `SEO Topic Suggestion` (theo `engagement_rules.md` mục 5).
3. **Content Pillar** — `Relationship` / `Brand` / `Nhẹ` (khớp tỷ lệ ở `community_rules.md`
   mục 1 & 5) — để trống nếu là Comment Reply (không áp dụng).
4. **Main Text** — toàn văn post hoặc câu trả lời bình luận.
5. **CTA** — đúng một mục trong danh sách cho phép ở `community_rules.md` mục 6; để trống nếu
   post không có CTA (nhiều post không cần, không ép có).
6. **Suggested Image** — mô tả/ý tưởng ảnh cần dùng (không phải file thật, tương tự Featured
   Image của SEO Factory) — để `image-factory` biết cần tạo gì; để trống nếu post không cần ảnh.
7. **Emotion** — cảm xúc chủ đạo của post (VD: Hy vọng, Đồng cảm, Bình yên, Chiêm nghiệm) — chỉ
   để mô tả, không phải để tối ưu hóa tương tác.
8. **Audience** — đối tượng hướng tới (VD: người chăm sóc cha mẹ già, người mới nghỉ hưu).
9. **Season** — mùa/dịp liên quan nếu có (theo `seasonal_calendar.md`), để trống nếu không gắn mùa.
10. **Purpose** — mục đích chính: `Engagement` / `Awareness` / `Support` (đồng hành cảm xúc) /
    `Topic Signal` (khi Content Type là SEO Topic Suggestion).
11. **Memory Tags** — tag tự do để tra cứu lại về sau (VD: `#tuoigia #codon #chamsoc`) — chỉ để
    con người hoặc một Analytics Service (nếu có sau này) tra cứu/thống kê thủ công, KHÔNG phải
    cơ chế để Community Factory tự học hay tự đổi hành vi (Factory này không tự sửa rules của
    chính nó — xem `instructions_COMMUNITY.md` mục 2).

---

## QUY TẮC ĐÓNG GÓI

- Field không áp dụng (VD: Content Pillar khi là Comment Reply) → để trống, không xóa field
  khỏi khuôn.
- Không tự thêm field ngoài danh sách dù thấy hữu ích — đề xuất riêng, không chèn vào khuôn xuất.
- Mỗi post/reply phải qua `community_checklist.md` trước khi xuất theo khuôn này.
