# IMAGE STYLE BIBLE — NHÂN VẬT "HIỀN TRIẾT"

> Tải lên khu **Files** (CORE_BRAIN — dùng chung mọi Factory). Đây là nguồn ngoại hình nhân
> vật DUY NHẤT của toàn hệ thống — bất kỳ Factory nào có ảnh/video chứa nhân vật Hiền triết
> Anh Minh đều PHẢI dùng đúng file này, không tự định nghĩa lại. **Chuyển từ `video-factory/`
> sang `core-brain/`** vì thực tế đã được dùng chéo (Image Factory tham chiếu file này từ
> trước) — đặt ở CORE_BRAIN đúng vai trò "tài sản dùng chung mọi Factory" hơn là nằm trong một
> Factory cụ thể.
> Mục đích: giữ nhân vật & không khí hình ảnh NHẤT QUÁN qua mọi cảnh Veo/ảnh tĩnh.
> Nhân vật là HIỀN TRIẾT phương Đông (nam) — KHÔNG phải bác sĩ, KHÔNG phải đạo sĩ.
> Cập nhật: 18/07/2026 — thêm mục 0B (khoá nhận diện qua img2video, dùng thẳng kho ảnh có sẵn,
> không train LoRA) + Voice ID ở mục 11, để giữ nhân vật/giọng ổn định khi sản xuất hàng trăm
> video qua n8n.

---

## 0. CHARACTER REFERENCE

Reference Images

assets/characters:

anh_minh_front.png

anh_minh_left.png

anh_minh_right.png

anh_minh_back.png

anh_minh_fullbody.png

Khi Image Factory hoặc Video Factory tạo ảnh/video có nhân vật Anh Minh,
luôn nạp toàn bộ bộ ảnh Reference này cùng Master Character Prompt.

Không tạo lại nhân vật từ đầu.

## 0B. KHOÁ NHẬN DIỆN QUA QUY MÔ LỚN (img2video, không train LoRA) — quyết định 18/07/2026

> Bổ sung sau khi bàn về rủi ro "nhân vật trôi mặt" khi sản xuất hàng trăm video tự động qua
> n8n. Đã cân nhắc train LoRA riêng cho khuôn mặt Anh Minh, nhưng chọn phương án rẻ hơn: dùng
> thẳng tính năng **img2video có sẵn trong Kling/Veo3** (đã trả phí subscription, gần như không
> phát sinh thêm chi phí) — animate trực tiếp từ một ảnh nhân vật ĐÃ CÓ sẵn, thay vì generate
> ảnh mới mỗi cảnh bằng text-to-image (cách dễ trôi mặt nhất nếu không có LoRA khoá riêng).

- **Bộ ảnh reference ở mục 0** (`anh_minh_front/left/right/back/fullbody.png`) là **kho ảnh
  nguồn cố định** — đây chính là ảnh input trực tiếp cho bước img2video (xem `video-factory/
  video_ai_contract.md` Stage 4), KHÔNG chỉ để tham khảo.
- **Nguyên tắc chọn ảnh cho một cảnh có nhân vật:** chọn ảnh có sẵn trong kho khớp nhất với tư
  thế/bối cảnh cảnh đó, rồi img2video thẳng từ đúng ảnh này. KHÔNG text-to-image tạo ảnh nhân
  vật mới cho từng cảnh — mỗi lần tạo ảnh mới bằng text là một lần nhận diện có thể lệch.
- **Khi kho ảnh hiện có chưa đủ tư thế/bối cảnh cần dùng:** ưu tiên tạo ảnh mới bằng cách
  **chỉnh sửa/ghép ảnh (image editing/inpainting) từ chính ảnh gốc đã có** — giữ nguyên khuôn
  mặt, chỉ đổi tư thế/bối cảnh xung quanh — thay vì text-to-image từ đầu. Sau khi ảnh mới được
  review đạt (khớp nhận diện), thêm vào kho ảnh nguồn vĩnh viễn (đặt tên rõ, VD
  `anh_minh_sitting_tea.png`) để dùng lại về sau — kho ảnh nguồn sẽ nối dài theo thời gian,
  không cố định mãi ở 5 ảnh ban đầu.
- **KHÔNG bao giờ generate lại các ảnh đã có "cho đẹp hơn"** — ảnh trong kho là tài sản khoá
  cứng; thay ảnh cũ bằng ảnh mới (dù đẹp hơn) sẽ làm nhận diện lệch so với các video đã làm
  trước đó bằng ảnh cũ.
- **Kiểm tra định kỳ:** vì img2video giữ gần như nguyên khuôn mặt của ảnh gốc, rủi ro "trôi
  mặt" chủ yếu đến từ chuyển động quá mạnh khiến Kling/Veo3 tự vẽ thêm chi tiết khuôn mặt không
  có trong ảnh gốc — ưu tiên chuyển động máy chậm, camera tĩnh (đã quy định ở `video_rules.md`
  mục 5), và rà soát nhanh bằng mắt các cảnh có chuyển động mạnh trước khi publish.

---

## 1. MASTER CHARACTER PROMPT (chính diện — dùng làm ảnh tham chiếu gốc)

```
A semi-realistic cinematic portrait of a calm Vietnamese man in his early 50s — an
Eastern sage and reflective scholar (NOT a doctor, NOT a daoist priest). Short slightly
wavy salt-and-pepper black hair, neatly trimmed grey-flecked goatee and mustache, thin
round metal-framed glasses, warm intelligent brown eyes, gentle faint half-smile, soft
naturally aged skin with subtle smile lines, medium-light Vietnamese skin tone. He wears
an oatmeal-beige linen shirt with a mandarin stand-collar (modern oriental style, not a
costume), sleeves slightly rolled. He sits at a dark wooden desk, holding a dark charcoal
ceramic tea cup in one hand. Setting: a quiet wooden study opening onto a lush green
forest / garden seen through large windows — a dark clay teapot and tea set, an open old
book, a small bowl of dried tea leaves, a small stack of old books, potted green plants,
and a wooden bookshelf. Soft green daylight filtering through the foliage; warm gentle
indoor light. NO Chinese characters, NO Han calligraphy scroll, NO Chinese text anywhere
in frame — Vietnamese text only (or no text). Lighting: soft natural morning light, warm, low-contrast, gentle
shadows, cinematic healing-wellness mood. Color palette: warm beige, soft brown, muted
olive green, natural wood tones, cream. Shot on 35mm, shallow depth of field, eye-level
intimate medium close-up. Mood: serene, wise, warm, trustworthy, scholarly. Subtle human
imperfections, realistic skin texture.
```

**Negative prompt (luôn kèm):**
```
Chinese characters, Han calligraphy, hanzi, Chinese scroll, Chinese couplet, any Chinese
text, daoist robe, priest costume, lab coat, stethoscope, clinic, hospital, cartoon,
anime, Pixar look, plastic CGI skin, glossy beauty filter, neon lighting, harsh contrast,
horror shadows, exaggerated expression, influencer aesthetic, watermark, fast cuts,
aggressive camera movement, motivational-speaker energy, fake CGI shots, robotic movement,
overly smooth skin, uncanny valley, toy-like humans, emotionless eyes, epic soundtrack.
```

---

## 2. BIẾN THỂ ẢNH THAM CHIẾU (tạo 2–3 ảnh để khóa nhận diện)

Tạo cùng nhân vật, cùng trang phục & ánh sáng, chỉ đổi góc — rồi nạp tối đa 3 ảnh này
làm reference khi generate clip:
- **3/4 góc:** `...three-quarter angle, looking slightly off-camera, same wardrobe and lighting...`
- **Không kính (dự phòng):** `...without glasses, same face identity, same beard and hair...`
- **Toàn thân ngồi:** `...wider seated shot at the wooden desk, hands resting near the teapot...`

---

## 3. BIẾN THỂ 9:16 (TikTok / Reels / Shorts)

Thêm vào cuối Master Prompt:
```
Vertical 9:16 composition, subject centered with comfortable head-room, props arranged
vertically (teapot and books framing the lower edge), subtitle-safe lower third, mobile-
optimized framing, face clearly readable on a phone screen.
```

---

## 4. KHÓA TRANG PHỤC & NGOẠI HÌNH

> **NGÔN NGỮ HIỂN THỊ — chỉ chữ Việt.** Mọi chữ xuất hiện trong khung hình (tranh, sách,
> bảng, hoành phi, câu đối, decor) chỉ được là tiếng Việt — hoặc không có chữ. TUYỆT ĐỐI
> không dùng chữ Hán / chữ Trung Quốc dưới bất kỳ dạng nào. Trang trí tường nên dùng:
> tranh phong cảnh, cành lá, hoặc thư pháp tiếng Việt — không thư pháp Hán tự.

- Áo: **linen cổ trụ (mandarin collar)**, tông oatmeal/be/nâu nhạt/olive trầm. Có thể đổi
  giữa các màu đất này, nhưng luôn là linen tối giản — KHÔNG họa tiết sặc sỡ, KHÔNG áo
  choàng đạo sĩ, KHÔNG đồ hiệu, KHÔNG streetwear.
- Phụ kiện hợp lệ (dùng tiết chế): vòng gỗ, đồng hồ cũ, sổ tay, chén trà gốm.
- Giữ cố định: cấu trúc khuôn mặt, hình mắt, kiểu tóc muối tiêu, độ tuổi ~50, tông da,
  cặp kính tròn mảnh.

---

## 5. BẢNG MÀU & ÁNH SÁNG

- **Màu:** be ấm, nâu mềm, olive trầm, tông gỗ tự nhiên, kem, vàng nắng nhẹ, xanh lá thảo mộc.
- **Ánh sáng:** sáng cửa sổ mềm, ánh ngày dịu, đèn vonfram ấm trong nhà, bóng đổ tự nhiên,
  tương phản thấp. TRÁNH: ánh neon, ánh phòng khám lạnh, đèn beauty cháy sáng, bóng kiểu phim kinh dị.

---

## 6. PHONG CÁCH DỰNG HÌNH (chắt lọc từ Visual Style)

- Semi-realistic cinematic, mặt người chân thực, da có kết cấu thật, bất đối xứng tự nhiên nhẹ.
- Giữ "khuyết điểm người thật" tinh tế: tránh hoàn hảo nhựa, tránh uncanny valley.
- TRÁNH: hoạt hình, anime, CGI bóng nhựa, biểu cảm cường điệu, mắt vô hồn, chuyển động robot.

---

## 8. KHÓA NHẤT QUÁN (đọc trước mỗi lần generate)

Luôn giữ: cùng nhận diện khuôn mặt, hình mắt, kiểu tóc, độ tuổi, tông da, cặp kính, trang phục
linen, năng lượng ấm-tĩnh, không khí điện ảnh ấm áp.
KHÔNG: thiết kế lại nhân vật, làm trẻ ra, làm cơ bắp, làm hoạt hình, đổi cấu trúc mặt,
biến thành phong cách influencer.

---

## 9. HÀNH VI & NĂNG LƯỢNG NHÂN VẬT (dùng khi viết prompt cảnh có nhân vật)

Nhân vật hành xử như:
- **không bao giờ vội** — mọi cử chỉ đều chậm và có chủ đích
- **ánh mắt mềm** — nhìn vào camera hoặc nhìn ra vườn, không nhìn thẳng cứng
- **khoảng dừng trước khi nói** — suy nghĩ trước, không phát ngôn ngay
- **cử chỉ tay nhẹ** — nâng chén trà, lật trang sách, không gesture cường điệu
- **tư thế bình tĩnh** — ngồi thẳng nhưng thoải mái, không căng cứng
- **phản ứng cảm xúc tinh tế** — nụ cười nửa miệng, gật đầu nhẹ, không biểu cảm phô

Nhân vật KHÔNG bao giờ trông như:
- diễn giả truyền động lực
- người bán hàng
- influencer mạng xã hội
- bác sĩ TV kịch tính

**Cảm giác:** như đang ngồi nói chuyện riêng với một người, không phải biểu diễn cho đám đông.

---

## 10. EMOTIONAL TONE (kiểm soát cảm xúc hình ảnh)

Cường độ cảm xúc: **LOW → MEDIUM** — ấm áp nhưng không kịch tính, an ủi nhưng không giả tạo.

Hình ảnh nên gợi cảm giác:
- "bạn không cô đơn"
- "được phép chậm lại"
- "cơ thể xứng đáng được đối xử nhẹ nhàng"

TRÁNH: cảm xúc áp đảo, hình ảnh bi kịch, ánh sáng u ám gây nặng nề, nhạc hoành tráng kiểu trailer.

---

## 11. SOUND DESIGN (nhắc nhở khi render / ghép video)

Âm thanh nền ưu tiên:
- tiếng trà rót chậm
- mưa nhẹ ngoài cửa sổ
- gió thoảng
- chim xa
- lật trang sách
- hơi thở nhẹ
- không khí căn phòng yên tĩnh

Nhạc nền: piano tối giản, cello nhẹ, ambient Việt Nam tinh tế — **cảm xúc nhưng kiềm chế**.

TUYỆT ĐỐI KHÔNG: nhạc epic, nhạc motivational beats, nhạc thao túng cảm xúc kiểu phim quảng cáo.

**Giọng đọc (Voice ID — ElevenLabs, quyết định 18/07/2026):** dùng đúng **1 voice đã clone/khoá
riêng cho Anh Minh**, giữ nguyên qua mọi video — không dùng giọng preset có sẵn hoặc đổi giọng
giữa các video (giống nguyên tắc khoá LoRA ở mục 0B, áp dụng cho giọng thay vì mặt).
Voice ID: `<điền khi đã tạo voice clone chính thức>`. Cho tới khi có voice ID chính thức, ưu
tiên một giọng đọc người thật thu âm nhất quán thay vì TTS ngẫu nhiên đổi giọng mỗi video.
