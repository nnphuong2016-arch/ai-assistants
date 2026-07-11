# PUBLISHING TARGETS — KÊNH XUẤT BẢN (PUBLISH FACTORY)

> Tải lên khu **Files** của Publish Factory. Quy định kênh xuất bản khả dụng.
> Cập nhật: 04/07/2026.

---

## 1. HIỆN TẠI — CHỈ WEBSITE

Funamark hiện chỉ xuất bản lên **Website CMS**. Publish Factory không tự mở rộng sang kênh
khác (Facebook/Telegram/Email/Pinterest...) dù có vẻ hợp lý — đa kênh là việc của lớp
**Automation (n8n)**, chạy SAU khi bài đã có mặt trên Website, không phải việc của Factory này.

Định dạng CMS khả dụng (AI chỉ cần biết TÊN, không cần biết cấu hình kỹ thuật — đó là việc của
Node n8n tương ứng):

- WordPress
- Next.js CMS (headless)
- Ghost
- Markdown (file tĩnh, dùng cho staging/preview)
- JSON (dùng khi pipeline cần dữ liệu thô để tự xử lý)

## 2. CÁCH CHỌN TARGET

- **Target luôn là Website** (mục 1) — "JSON" KHÔNG phải một Target/kênh riêng, chỉ là **định
  dạng đóng gói** của Publish Package. Nói cách khác: câu đúng là *"Publish Package mặc định
  đóng gói dạng JSON"*, không phải *"Target mặc định là JSON"* — tránh nhầm định dạng với kênh.
- Nếu không được chỉ định rõ định dạng CMS cụ thể, mặc định đóng gói **JSON** — trung lập, n8n
  tự map sang CMS thật đang dùng.
- Nếu được chỉ định rõ một CMS (VD: "xuất cho WordPress") → ghi tên CMS đó, không cần biết cách
  gọi API của CMS đó — Target trong `output_schema.md` vẫn ghi `Website`.

## 3. KHÔNG LÀM

- Không tự tạo file riêng cho từng CMS (`wordpress_rules.md`, `nextjs_rules.md`...) — cấu hình
  kỹ thuật (API, auth, endpoint) là việc của Node n8n, không phải kiến thức AI cần giữ.
- Không tự quyết định đăng đa kênh (Facebook/Telegram...) dù nội dung có vẻ hợp cả hai. Nếu
  người dùng yêu cầu đăng đa kênh, báo rằng việc đó thuộc lớp Automation, không phải Publish Factory.
