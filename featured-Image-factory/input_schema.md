# INPUT SCHEMA — FEATURED IMAGE FACTORY

> Tải lên khu **Files** của Featured Image Factory.
> File này định nghĩa toàn bộ dữ liệu đầu vào mà Factory có thể nhận.
> Không bắt buộc phải có đầy đủ tất cả Field.
> Factory phải tự suy luận khi thiếu dữ liệu theo quy định trong `instructions_FEATURED_IMAGE.md`.
> Cập nhật: 20/07/2026 — thêm dòng ngày cập nhật cho đồng bộ quy ước với các Factory khác.

---

# 1. INPUT OBJECT

Factory có thể nhận một hoặc nhiều trường sau.

---

## Required

Ít nhất phải có một trong các trường sau:

- slug (VD: `1.5.co-the-can-nhung-khoang-yen-tinh` hoặc `1.5.co-the-can-nhung-khoang-yen-tinh.md`)
- hook
- title
- article

**Trường hợp phổ biến nhất: người dùng chỉ dán đúng 1 dòng là tên file/slug bài viết** (không
kèm gì khác). Factory tự động:
1. Bỏ đuôi `.md` nếu có.
2. Dùng nguyên slug đó làm `filename` output (chỉ đổi đuôi sang `.jpg`) — KHÔNG tự sinh tên
   khác.
3. Bỏ dấu chấm/gạch ngang, đọc phần chữ sau số thứ tự (VD: `co-the-can-nhung-khoang-yen-tinh`
   → hiểu là "cơ thể cần những khoảng yên tĩnh") để suy luận chủ đề, dùng như `hook`.
4. Chạy thẳng toàn bộ quy trình (Editorial → Style → Prompt → Checklist → Output) và trả Output
   ngay — không hỏi lại, không giải thích từng bước, kể cả ở Interactive Mode.

Nếu cả bốn trường trên đều thiếu.

Factory không thể tạo Featured Image.

---

## Optional

category

keyword

summary

language

target_audience

image_style

aspect_ratio

filename

notes

---

# 2. FIELD DESCRIPTION

## hook

Hook hoặc tiêu đề ngắn.

Ví dụ:

"Gan nhiễm mỡ nên ăn gì?"

---

## title

Tiêu đề bài viết.

Nếu có title.

Ưu tiên title hơn hook.

---

## article

Toàn bộ bài viết.

Nếu có article.

Factory luôn ưu tiên article.

Không chỉ dựa vào title.

---

## summary

Tóm tắt bài.

Dùng khi không có bài viết đầy đủ.

---

## category

Một trong các giá trị:

- Sức khỏe
- Tâm lý & Đời sống
- Dưỡng sinh
- Triết lý phương Đông
- Đồng hành tuổi già
- Bếp An Nhiên

Nếu thiếu.

Factory tự suy luận.

---

## keyword

Từ khóa SEO chính.

Chỉ dùng để hỗ trợ.

Không quyết định Concept.

---

## language

Ngôn ngữ đầu vào.

Ví dụ:

vi

en

ja

Nếu không có.

Factory tự nhận biết.

---

## target_audience

Đối tượng độc giả.

Ví dụ:

Người cao tuổi

Người trung niên

Người bệnh

Gia đình

Phụ nữ

Nam giới

Nếu thiếu.

Factory tự suy luận.

---

## image_style

Cho phép ghi đè Style Rules.

Chỉ dùng khi người dùng yêu cầu.

Nếu không có.

Factory luôn dùng:

featured_image_style_rules.md

---

## aspect_ratio

Ví dụ:

16:9

4:3

1:1

Nếu thiếu.

Factory dùng mặc định.

---

## filename

Tên file mong muốn.

**Nếu input có `slug` (tên file bài viết) → filename LUÔN lấy nguyên slug đó (đổi đuôi
`.md`→.jpg), không tự sinh tên khác, không tự rút gọn/diễn giải lại.**

Nếu không có slug và cũng không có filename.

Factory tự sinh từ title/hook.

---

## notes

Ghi chú thêm.

Không bắt buộc.

---

# 3. INPUT PRIORITY

Nếu nhận nhiều nguồn dữ liệu.

Factory ưu tiên theo thứ tự (riêng `filename` output luôn lấy từ `slug` nếu có, bất kể thứ tự
dưới đây — xem field `filename`):

article

↓

summary

↓

title

↓

hook

↓

slug (diễn giải thành hook nếu không có gì khác)

↓

keyword

Không sử dụng dữ liệu ưu tiên thấp để ghi đè dữ liệu ưu tiên cao.

---

# 4. THIẾU DỮ LIỆU

Nếu thiếu:

category

↓

Factory tự suy luận.

Nếu thiếu:

title

↓

Dùng hook.

Nếu thiếu:

article

↓

Sử dụng title hoặc hook.

Nếu thiếu:

target_audience

↓

Factory tự suy luận.

Nếu thiếu:

filename

↓

Factory tự sinh.

Không được từ chối tạo Featured Image chỉ vì thiếu dữ liệu.

---

# 5. AUTOMATION MODE

Trong Automation Mode.

Factory không hỏi lại.

Không hội thoại.

Không giải thích.

Tự suy luận các Field còn thiếu.

---

# 6. INTERACTIVE MODE

Trong Interactive Mode.

Nếu dữ liệu quá mơ hồ.

Factory có thể hỏi thêm.

Ví dụ:

- Chủ đề thuộc chuyên mục nào?
- Muốn hướng đến đối tượng nào?

Nếu không hỏi.

Factory tự suy luận.

---

# 7. INPUT EXAMPLE

## Ví dụ 1

{
  "hook": "Gan nhiễm mỡ nên ăn gì?"
}

---

## Ví dụ 2

{
  "title": "7 loại thực phẩm tốt cho tim mạch",
  "category": "Sức khỏe"
}

---

## Ví dụ 3

{
  "article": "...toàn bộ bài viết...",
  "category": "Sức khỏe",
  "target_audience": "Người trung niên"
}

---

## Ví dụ 4 (Google Sheet)

{
  "hook": "Đừng uống nước ngay sau khi ăn",
  "category": "Sức khỏe",
  "keyword": "uống nước sau ăn"
}

---

# 8. QUY TẮC

Factory không yêu cầu tất cả Field.

Factory chỉ cần đủ dữ liệu để hiểu đúng nội dung bài viết.

Mọi Field còn thiếu phải được tự suy luận theo các quy tắc của Factory.

Không tạo lỗi chỉ vì thiếu dữ liệu không bắt buộc.