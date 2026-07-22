# OUTPUT SCHEMA — FEATURED IMAGE FACTORY

> Tải lên khu **Files** của Featured Image Factory.
> File này định nghĩa dữ liệu đầu ra chuẩn của Factory.
> Mọi Output phải tuân thủ đúng Schema này.
> Không tự thêm Field.
> Không tự bỏ Field.
> Không đổi tên Field.
> Cập nhật: 20/07/2026 — thêm dòng ngày cập nhật; đổi heading cuối file "OUTPUT RULES" thành
> "QUY TẮC ĐÓNG GÓI" cho khớp quy ước heading đóng gói dùng ở mọi Factory khác (SEO/Video/
> Community/Research/Publish), nội dung không đổi.

---

# OUTPUT OBJECT

Factory luôn xuất một Object gồm các Field sau.

---

## image_type

Luôn là:

Featured Image

---

## category

Một trong các giá trị:

- Sức khỏe
- Tâm lý & Đời sống
- Dưỡng sinh
- Triết lý phương Đông
- Đồng hành tuổi già
- Bếp An Nhiên

---

## concept

Concept đã chọn.

Ví dụ:

Lifestyle

Food

Human Emotion

Medical Illustration

Nature

Object

---

## subject

Chủ thể chính của ảnh.

Ví dụ:

Asian elderly woman drinking warm tea

---

## prompt

Prompt hoàn chỉnh.

Viết bằng tiếng Anh.

Theo đúng Prompt Rules.

---

## negative_prompt

Negative Prompt hoàn chỉnh.

Không được để trống.

---

## aspect_ratio

Mặc định:

16:9

---

## suggested_size

Mặc định:

1600x900

Có thể thay đổi nếu Workflow yêu cầu.

---

## filename

**Nếu input có slug (tên file bài viết, VD: `1.5.co-the-can-nhung-khoang-yen-tinh.md`) → dùng
NGUYÊN slug đó, chỉ đổi đuôi `.md` thành `.jpg`.** Ví dụ:
`1.5.co-the-can-nhung-khoang-yen-tinh.jpg`.

Nếu không có slug, tự sinh từ title/hook. Ví dụ: `gan-nhiem-mo-nen-an-gi.jpg`.

Không có dấu.

Không có khoảng trắng.

---

## alt_text

Viết bằng tiếng Việt.

Ngắn gọn.

Trung thực.

Mô tả đúng hình ảnh.

Không nhồi từ khóa.

---

## caption

Nếu không cần.

Để trống.

---

# OUTPUT FORMAT

Trong Interactive Mode.

Xuất dạng Markdown.

Ví dụ:

Image Type:

Category:

Concept:

Subject:

Prompt:

Negative Prompt:

Aspect Ratio:

Suggested Size:

Filename:

Alt Text:

Caption:

---

Trong Automation Mode.

Xuất đúng Object.

Ví dụ:

{
  "image_type": "...",
  "category": "...",
  "concept": "...",
  "subject": "...",
  "prompt": "...",
  "negative_prompt": "...",
  "aspect_ratio": "...",
  "suggested_size": "...",
  "filename": "...",
  "alt_text": "...",
  "caption": ""
}

---

# QUY TẮC ĐÓNG GÓI (OUTPUT RULES)

Không đổi tên Field.

Không đổi thứ tự Field.

Không thêm giải thích.

Không thêm nhận xét.

Không thêm Markdown ngoài Interactive Mode.

Automation Mode chỉ trả về Object.

Factory phải đảm bảo Output luôn hợp lệ để có thể sử dụng trực tiếp trong:

- Custom GPT
- OpenAI API
- n8n
- Google Sheet
- WordPress
- Workflow Automation