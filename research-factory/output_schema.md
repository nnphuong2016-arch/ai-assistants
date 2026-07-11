# OUTPUT SCHEMA — KNOWLEDGE PACKAGE (RESEARCH FACTORY)

> Tải lên khu **Files** của Research Factory. Quy định khuôn xuất Knowledge Package — để SEO
> Factory (và Factory khác khi cần) đọc trực tiếp, không phải research lại từ đầu.
> Cập nhật: 04/07/2026.

---

## KHUÔN XUẤT CHUẨN

1. **Package ID** — khóa nội bộ ổn định của Knowledge Package, **lấy nguyên từ
   `research_results.id`** đã có sẵn (Research Factory KHÔNG tự sinh ID mới), có thể trình bày
   dạng thân thiện (VD: `KP-20260705-001`) để Video/Community/SEO cùng tham chiếu một package
   mà không cần tra lại theo keyword mỗi lần.
2. **Research Date** — ngày thực hiện research (VD: `2026-07-05`) — để Factory nhận package
   biết package cũ hay mới, không cần đoán.
3. **Freshness** — hạn dùng của package trước khi cần research lại: `Evergreen` / `180 ngày` /
   `90 ngày` / `30 ngày` / `7 ngày`. Không phải để SEO Factory dùng khi viết — mà để pipeline
   (n8n/Scheduler) biết khi nào cần gọi lại WF-03 thay vì dùng cache. Cách chọn mức theo loại
   nghiên cứu (xem `research_templates.md` để biết mức gợi ý mỗi khuôn):
   - Chủ đề triết lý/lối sống/nhân sinh (ít đổi theo thời gian) → **Evergreen** hoặc **180 ngày**.
   - Chủ đề sức khỏe/dưỡng chất (khuyến nghị có thể cập nhật nhưng không nhanh) → **90 ngày**.
   - Giá sản phẩm, thông số thị trường (đổi nhanh) → **30 ngày**.
   - Xu hướng/trend đang thảo luận (đổi rất nhanh) → **7 ngày**.
4. **Scope** — phạm vi địa lý/thị trường của thông tin: `Việt Nam` / `Quốc tế` / `Toàn cầu`.
   Mặc định **Việt Nam** nếu không có lý do khác (kênh phục vụ người Việt) — chỉ đổi khi chủ đề
   thực sự cần góc quốc tế (VD: nghiên cứu khoa học gốc, sản phẩm chưa bán tại VN). Quan trọng
   nhất với Product Research (giá/thương hiệu khác nhau theo thị trường) và Health Topic
   Research (khuyến nghị Bộ Y tế VN có thể khác WHO/NIH).
5. **Topic** — chủ đề/sản phẩm được research.
6. **Intent** — search intent chính (Trả lời nhanh / Tìm hiểu sâu / Tổng quan chủ đề — khớp
   thang ở `seo-factory/keyword_strategy.md` mục 3).
7. **Entities** — 5–8 thực thể/khái niệm liên quan.
8. **Keywords** — Primary Keyword ứng viên + 2–3 Secondary Keyword ứng viên (SEO Factory sẽ tự
   quyết định chọn/điều chỉnh theo `keyword_strategy.md`, đây chỉ là đề xuất).
9. **FAQs** — 3–5 câu hỏi thường gặp thật, kèm nguồn nếu câu trả lời có thông tin cụ thể.
10. **Audience** — đối tượng liên quan (VD: người trung niên, người chăm sóc cha mẹ già...).
11. **Sources** — danh sách nguồn đã dùng, kèm mức (1/2/3, theo `source_rules.md`).
12. **Confidence** — High / Medium / Low (theo `validation_rules.md` mục 3), áp dụng cho toàn
    package hoặc theo từng trường nếu mức độ tin cậy khác nhau rõ rệt.
13. **YMYL** — `true`/`false` (theo `research_rules.md` mục 4).
14. **Category** — trụ nội dung liên quan (Sức khỏe/Tâm lý/Dưỡng sinh/Triết lý/Đồng hành...).
15. **Season** — mùa/dịp liên quan nếu có (theo `seasonal_calendar.md`), để trống nếu không gắn mùa.
16. **Notes** — ghi chú tự do: mâu thuẫn giữa nguồn, thông tin cần xác minh thêm, giới hạn tìm
    kiếm gặp phải trong lượt research này.

---

## QUY TẮC ĐÓNG GÓI

- Field nào không tìm được dữ liệu đủ tin cậy → để trống + ghi lý do ở **Notes**, không tự bịa
  cho đủ khuôn.
- Có thể lưu package dưới dạng file JSON độc lập (quy ước tên: `<topic-slug>.json`) để tái sử
  dụng cho nhiều lượt viết sau, tránh research lại cùng chủ đề nhiều lần.
- Factory nhận package (chủ yếu SEO Factory) tự quyết định dùng gì — Research Factory không áp
  đặt package phải được dùng nguyên văn.
