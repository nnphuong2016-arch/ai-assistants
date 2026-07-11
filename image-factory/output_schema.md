# OUTPUT SCHEMA — CHUẨN ĐẦU RA IMAGE FACTORY

> Tải lên khu **Files** của Image Factory. Quy định khuôn xuất cuối cùng của mọi prompt ảnh —
> để n8n (hoặc bất kỳ pipeline nào đọc output) luôn nhận đúng field, đúng thứ tự.
> Cập nhật: 04/07/2026.

---

## KHUÔN XUẤT CHUẨN

Mỗi yêu cầu ảnh xuất ra theo đúng thứ tự field dưới đây. Không thiếu field, không đổi tên
field, không thêm field ngoài danh sách.

1. **Template** — tên mẫu đã chọn (A–K, xem `image_templates.md`). Đổi tên từ "Image Type"
   (dễ hiểu nhầm thành định dạng file) sang "Template" cho rõ nghĩa hơn.
2. **Usage** — nơi ảnh sẽ được dùng (VD: Homepage / Category / Blog / Social) — để n8n biết đặt
   ảnh vào đúng vị trí, không phải đoán từ Template suy ra.
3. **Prompt** — toàn văn prompt theo cấu trúc `image_prompt_rules.md` mục 1.
4. **Negative Prompt** — baseline + bổ sung riêng (xem `image_prompt_rules.md` mục 2).
5. **Aspect Ratio** — theo mặc định của mẫu đã chọn, không tự đổi.
6. **Size** — kích thước gợi ý theo Aspect Ratio (VD: 1920×823 cho Hero 21:9, 1200×630 cho OG
   1.91:1) — gợi ý phổ biến, pipeline có thể override theo yêu cầu thực tế của nền tảng đích.
7. **Filename** — tên file **gợi ý** dạng slug không dấu (VD: `tra-chieu-cua-so-nang-som.jpg`),
   không phải file đã tồn tại thật — hệ thống lưu trữ có thể đổi tên khi lưu thật.
8. **Alt Text** — mô tả ảnh ngắn gọn, trung thực, phục vụ SEO/accessibility (không nhồi từ khóa).
9. **Caption** — chỉ điền nếu ảnh có hiển thị chú thích công khai (VD: Quote Image); để trống
   nếu ảnh không cần caption hiển thị.

---

## QUY TẮC ĐÓNG GÓI

- Field nào không áp dụng (VD: Avatar không cần Caption) → để trống, không xóa field khỏi khuôn.
- Không tự thêm field ngoài danh sách dù thấy hữu ích — đề xuất riêng, không chèn vào khuôn xuất.
- Prompt viết bằng tiếng Anh theo `image_prompt_rules.md` mục 4; các field còn lại (Alt Text,
  Caption, Filename gợi ý) có thể tiếng Việt nếu phục vụ website tiếng Việt.
