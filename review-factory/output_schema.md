# OUTPUT SCHEMA — CHUẨN ĐẦU RA REVIEW FACTORY

> Tải lên khu **Files** của Review Factory. Quy định khuôn xuất kết quả review — để n8n (hoặc
> bất kỳ pipeline nào đọc output) luôn nhận đúng field, đúng thứ tự.
> Cập nhật: 04/07/2026.

---

## KHUÔN XUẤT CHUẨN

```
Review Result
[Loại nội dung] — [Tên/ID nội dung được review]

Reviewed Factory
[SEO Factory / Image Factory / Video Factory / Community Factory / Publish Package]

Review Timestamp
[YYYY-MM-DD HH:MM]

---

Critical Issues
- [lỗi] — vi phạm [tiêu chí nào, trỏ tới review_checklists.md/file gốc] — đề xuất: [1 câu]
(hoặc "Không có")

---

Major Issues
- [lỗi] — vi phạm [tiêu chí nào] — đề xuất: [1 câu]
(hoặc "Không có")

---

Minor Issues
- [lỗi] — [ghi chú ngắn]
(hoặc "Không có")

---

Suggestions
- [đề xuất KHÔNG nằm trong checklist, chỉ mang tính tham khảo — không tính vào quyết định cuối]
(hoặc "Không có")

---

Final Decision
[PASS / PASS WITH NOTE / NEED FIX / FAIL]
```

---

## QUY TẮC ĐÓNG GÓI

- Luôn xuất đủ 5 khối theo đúng thứ tự trên, kể cả khi một khối trống (ghi "Không có").
- **Reviewed Factory** + **Review Timestamp** ở đầu là bắt buộc, không được để trống — dùng để
  log/audit về sau (biết ai/loại nào được review, lúc nào), không phải phần tự do.
- **Final Decision** phải khớp đúng công thức ở `scoring_rules.md` mục 2 — không tự quyết định
  khác đi dù cảm thấy nội dung "gần đạt".
- Mỗi Issue phải trỏ được về đúng tiêu chí trong `review_checklists.md` hoặc file gốc của
  Factory liên quan — không ghi chung chung.
- Không viết lại nội dung đang review trong phần output — chỉ mô tả lỗi và đề xuất, không dán
  đoạn văn đã sửa.
