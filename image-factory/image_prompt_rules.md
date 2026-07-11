# IMAGE PROMPT RULES — CÁCH VIẾT PROMPT (IMAGE FACTORY)

> Tải lên khu **Files** của Image Factory. File này CHỈ nói cấu trúc viết prompt — không bàn
> style (xem `image_style_rules.md`) hay chọn mẫu (xem `image_templates.md`).
> Cập nhật: 05/07/2026.

---

## 1. CẤU TRÚC PROMPT CHUẨN

Mọi prompt viết theo đúng thứ tự 8 phần sau:

**Scene → Subject → Composition → Lighting → Color → Mood → Camera → Negative Prompt**

1. **Scene** — bối cảnh tổng thể (không gian, thời điểm trong ngày).
2. **Subject** — chủ thể chính (người/vật/props), theo `image_style_rules.md` hoặc
   `core-brain/image_style_bible.md` nếu là nhân vật chính.
3. **Composition** — bố cục (wide shot, close-up, rule of thirds, khoảng trống để chèn chữ nếu cần).
4. **Lighting** — theo mục 2 của `image_style_rules.md` (golden hour, soft morning...).
5. **Color** — theo tone màu mục 1 của `image_style_rules.md`.
6. **Mood** — cảm giác tổng thể (điềm tĩnh, ấm áp, tĩnh lặng — khớp giọng CORE_BRAIN).
7. **Camera** — thông số gợi ý (VD: 50mm, f/1.8, độ sâu trường ảnh nông để làm mờ hậu cảnh).
8. **Negative Prompt** — xem mục 2 (baseline bắt buộc).

## 2. BASELINE NEGATIVE PROMPT (luôn có trong mọi prompt)

Luôn bao gồm — không bỏ sót dù mẫu nào:

`no text, no watermark, no logo, no AI artifact, no extra fingers, no distorted hands,
natural skin texture, no oversaturated colors, no neon`

Thêm negative riêng theo tình huống nếu cần (VD: ảnh sức khỏe → thêm `no medical equipment,
no hospital setting, no distressed expression`).

## 3. VÍ DỤ PROMPT HOÀN CHỈNH

**Yêu cầu:** Blog Cover cho bài "Vì sao người xưa sống chậm mà khỏe" (Mẫu E).

```
Scene: a quiet home garden corner in early morning
Subject: a warm cup of tea on a wooden table, soft steam rising, no people
Composition: wide shot, rule of thirds, negative space top-left for text overlay
Lighting: soft morning natural light, warm golden tone
Color: beige, cream, walnut brown, muted warm green
Mood: calm, unhurried, contemplative
Camera: 50mm, f/1.8, shallow depth of field
Negative prompt: no text, no watermark, no logo, no AI artifact, no extra fingers,
no distorted hands, natural skin texture, no oversaturated colors, no neon
```

## 4. QUY TẮC VIẾT

- Viết prompt bằng tiếng Anh (tương thích tốt hơn với hầu hết công cụ tạo ảnh), trừ khi công cụ
  đích yêu cầu khác.
- Không nhồi quá nhiều chi tiết mâu thuẫn nhau (VD: vừa "wide shot" vừa "close-up") — chọn một.
- Nếu ảnh có nhân vật chính, phần Subject phải khớp chính xác mô tả ở `core-brain/image_style_bible.md`,
  không tự thêm chi tiết ngoại hình mới.
- **Không nhồi prompt dài:** AI có xu hướng viết prompt rất dài (nhiều tính từ hoa mỹ), nhưng
  các công cụ tạo ảnh (Flux...) thường cho kết quả tốt hơn với prompt gọn. Nếu prompt bắt đầu
  dài quá mức cần thiết, ưu tiên giữ lại đúng 3 phần cốt lõi **Scene → Subject → Lighting**,
  cắt bớt tính từ/mô tả phụ thay vì giữ nguyên cả 8 phần chi tiết dài dòng.
