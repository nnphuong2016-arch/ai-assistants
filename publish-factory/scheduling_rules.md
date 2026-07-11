# SCHEDULING RULES — THỜI ĐIỂM XUẤT BẢN (PUBLISH FACTORY)

> Tải lên khu **Files** của Publish Factory. Quy định thời điểm/lịch xuất bản.
> Cập nhật: 04/07/2026.

---

## 1. CHẾ ĐỘ XUẤT BẢN

- **Mặc định — không chỉ định gì → Immediately.** Đây là hành vi mặc định khi người dùng không
  nêu giờ/lịch cụ thể — xuất ngay khi đủ điều kiện (`publish_rules.md`), không cần hỏi lại.
- **Immediately** — xuất ngay khi đủ điều kiện (`publish_rules.md`) và không có ràng buộc mùa/giờ.
- **Giờ cố định** — nếu được chỉ định, publish vào một trong các khung giờ chuẩn:
  **07:30 / 12:00 / 19:30** (giờ Việt Nam) — khớp giờ người trung niên/lớn tuổi hay lên mạng.
- **Hẹn giờ theo yêu cầu cụ thể** — nếu người dùng chỉ định ngày giờ khác, dùng đúng theo yêu cầu.

## 2. GATE THEO MÙA (Seasonal)

Nếu nội dung gắn với một mùa/dịp cụ thể (theo `core-brain/seasonal_calendar.md`), **không
publish trái mùa** dù đã đủ điều kiện kỹ thuật:

- VD: bài "thanh nhiệt mùa hè" **không publish vào tháng 12**.
- VD: bài liên quan Tết **không publish vào giữa năm**.

Nếu nội dung không gắn mùa cụ thể (lối sống chung, triết lý, câu chuyện đời thường) → không áp
gate này, có thể publish bất kỳ lúc nào.

## 3. KHI PHÁT HIỆN TRÁI MÙA

- Không tự publish rồi thôi — báo lại thời điểm phù hợp gần nhất theo `seasonal_calendar.md`,
  đề xuất hẹn lịch (schedule) thay vì publish ngay.
- Không tự đổi nội dung bài để "chữa cháy" cho hợp mùa hiện tại — đó là việc của Factory gốc
  (SEO/Community), không phải Publish Factory.
