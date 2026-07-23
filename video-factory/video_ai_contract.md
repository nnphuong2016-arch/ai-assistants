# VIDEO PROMPT TEMPLATES
STATUS: LOCKED
VERSION: V1.4
DATE: 23/07/2026

> ⚠️ **Cập nhật 23/07/2026 (2):** làm rõ Stage 3 (Flux) còn dùng cho **nhân vật khách** (bất kỳ
> ai không phải Hiền triết Anh Minh) — chỉ Anh Minh có kho ảnh cố định, nhân vật khách phải
> generate mới nhưng CHỈ generate 1 lần/video rồi dùng lại cho mọi Scene cùng người đó trong
> video đó (xem Stage 2B/3/4 bên dưới + `video_ai_prompt_rules.md` mục 9).

> ⚠️ **Liên quan `video_ai_prompt_rules.md` + `model_selection_rules.md` (thêm 20/07/2026):**
> hai file đó định nghĩa quy tắc viết prompt đầy đủ + cách chọn công cụ (Veo 3/Kling/Hailuo/
> Runway) dùng chung mọi cảnh. File này (`video_ai_contract.md`) mô tả riêng pipeline n8n cho
> **cảnh có nhân vật Anh Minh** — img2video từ kho ảnh cố định (Stage 3/4, xem
> `image_style_bible.md` mục 0B) là cách khoá nhận diện cho các cảnh đó; cảnh B-roll/thiên
> nhiên/đồ vật không có nhân vật thì theo đúng `model_selection_rules.md` (thường Hailuo/Runway,
> text-to-video bình thường, không cần img2video).

> ⚠️ **Cập nhật 23/07/2026 — mô hình hybrid tiết kiệm chi phí (xem `model_selection_rules.md`
> mục 1B):** từ nay pipeline có **2 nhánh song song** sau Stage 2, không phải mọi Scene đều đi
> qua Stage 4 (generate Clip). Đa số Scene (~69–72% với video TRUNG/DÀI) chỉ dừng ở Ảnh tĩnh
> (Stage 3, hoặc lấy thẳng ảnh có sẵn trong kho `image_style_bible.md` mục 0B nếu là Anh Minh
> đứng/ngồi yên) rồi đi thẳng tới Stage 7 kèm tham số Ken Burns — **bỏ qua Stage 4 hoàn toàn**,
> tiết kiệm chi phí generate video. Chỉ Scene được đánh dấu Clip ở Stage 2B mới đi qua Stage 4.
> Xem Stage 2B (mới) bên dưới.

Mục đích:
Đây là nơi lưu các Prompt Template dùng riêng cho Video Factory.

Không chứa dữ liệu chủ đề.
Không chứa Hook.
Không chứa kiến thức.

Các Prompt này chỉ mô tả CÁCH AI phải làm việc.

GHI CHÚ VẬN HÀNH (cập nhật 18/07/2026, xem funamark-master-blueprint-v2.md WF-07B):
Khi input là file `..._master_script.md` do Video Factory (WF-07) xuất ra và đã PASS Review
(WF-05), Stage 1 + Stage 2 dưới đây KHÔNG cần gọi AI — file đã có sẵn đúng Storyboard (mỗi
`### Scene <ID>` = 1 scene, ID zero-padded 3 chữ số theo `video_rules.md` mục 1.C) và đúng nội
dung Scene Prompt (field **Visual** + **Camera** từng cảnh, đã tuân luật "không mô tả mặt/quần
áo/nhân vật" bên dưới — nhận diện nhân vật nằm riêng ở field **Character**). WF-07B chỉ cần
PARSE file bằng Code node theo thứ tự field: Scene ID → Duration → Voice → Visual → Camera →
Character → Emotion → Loop. Chỉ gọi AI cho Stage 1-2 khi input là script rời rạc KHÔNG qua Video
Factory (trường hợp hiếm, chưa build).

========================================================
1. VIDEO PLANNER AI
========================================================

Mục tiêu

Biến một Video Script hoàn chỉnh thành Storyboard.

Input

- Video Script
- Thời lượng mục tiêu
- Video Rules

Output

JSON

[
  {
    "scene_id":"001",
    "duration":12,
    "purpose":"Hook",
    "summary":"..."
  }
]

Yêu cầu

- Chia theo Ý, không chia theo số câu.
- Mỗi Scene chỉ có 1 ý chính.
- Video phải đủ thời lượng.
- Không kéo dài nội dung vô nghĩa.
- Không bỏ sót CTA.
- Tuân thủ video_rules.md.

========================================================
2. SCENE GENERATOR AI
========================================================

Mục tiêu

Sinh Prompt cho từng Scene.

Input

Storyboard JSON

Output

JSON

{
   "scene_id":"001",
   "prompt":"..."
}

Yêu cầu

Không mô tả khuôn mặt.

Không mô tả quần áo.

Không mô tả nhân vật.

Character sẽ được n8n ghép sau.

Chỉ mô tả

- hành động
- bối cảnh
- góc máy
- ánh sáng
- cảm xúc
- composition

========================================================
2B. MEDIA TYPE & TOOL SELECTION AI (MỚI — 23/07/2026)
========================================================

Mục tiêu

Với mỗi Scene, quyết định: Clip AI video hay Ảnh tĩnh + Ken Burns — và nếu là Clip, chọn công
cụ nào (Veo3/Kling/Hailuo/Runway). Theo đúng logic ở `model_selection_rules.md` mục 1B (Lớp
quyết định 0) + mục 2-4 (chọn công cụ).

Input

Storyboard JSON (Stage 1) + Scene Prompt (Stage 2) + field Character (từ Master Script gốc)

Output

JSON

{
   "scene_id":"001",
   "media_type":"static",
   "tool": null
}

hoặc

{
   "scene_id":"002",
   "media_type":"clip",
   "tool":"kling"
}

Yêu cầu

- Mặc định `media_type: "static"` trừ khi Scene khớp 1 trong 4 tiêu chí "Clip" ở
  `model_selection_rules.md` mục 1B (Anh Minh nói trực diện / cận cảnh cảm xúc / khoảnh khắc
  chủ đạo / hành động là chính nội dung cảnh).
- Tỷ lệ tham khảo toàn video: ~28–31% Scene là `"clip"`, phần còn lại `"static"` (video TRUNG/DÀI
  — xem bảng số liệu ở `model_selection_rules.md` mục 1B). Không ép cứng %, chỉ dùng để tự kiểm
  nếu lệch quá xa (VD 80% Scene ra "clip" thì phải xét lại).
- **Phân loại field Character trước khi quyết định nguồn ảnh** (3 trường hợp, xem thêm Stage 3):
  1. **Character trống** → B-roll, không có nhân vật.
  2. **Character = "Hiền triết Anh Minh"** → CHỈ nhân vật này có kho ảnh cố định. `media_type =
     "static"` → lấy thẳng ảnh từ kho (`image_style_bible.md` mục 0B), KHÔNG generate. `media_type
     = "clip"` → img2video từ đúng ảnh đó (Stage 4).
  3. **Character = tên khác** (nhân vật khách trong câu chuyện, xem `video_ai_prompt_rules.md`
     mục 9) → KHÔNG có kho ảnh sẵn, phải generate ở Flux (Stage 3) — xem quy tắc nhất quán trong
     Stage 3.
- Nếu `media_type = "clip"` → đi Stage 4, `tool` xác định theo bảng quyết định
  `model_selection_rules.md` mục 4.
- Không tự suy diễn ngoài 2 file rules trên.

========================================================
3. FLUX IMAGE AI
========================================================

Mục tiêu

Sinh ảnh cho 2 trường hợp: (a) B-roll không có nhân vật (Character trống), và (b) nhân vật khách
— bất kỳ ai KHÔNG PHẢI Hiền triết Anh Minh (Character có tên khác Anh Minh). Anh Minh là nhân
vật DUY NHẤT có kho ảnh cố định — Stage này KHÔNG BAO GIỜ generate ảnh Anh Minh, luôn lấy thẳng
từ kho (`image_style_bible.md` mục 0B) cho Stage 4.

Quy tắc nhất quán nhân vật khách: nếu nhiều Scene trong CÙNG một video dùng cùng một tên nhân vật
khách, chỉ generate ảnh gốc CHO người đó MỘT LẦN (ở Scene đầu tiên xuất hiện), rồi dùng lại đúng
ảnh đó cho mọi Scene khác cùng nhân vật trong video đó — kể cả khi Scene là `"clip"` (img2video
từ chính ảnh Flux vừa tạo, giống cơ chế Anh Minh nhưng không lưu vĩnh viễn qua nhiều video, chỉ
nhất quán trong nội bộ MỘT video/tập — xem `video_ai_prompt_rules.md` mục 9: không dùng lại
ngoại hình nhân vật khách giữa các tập trừ khi cố ý nối tiếp câu chuyện).

Input

Scene Prompt (field Visual + Camera) — nếu là nhân vật khách, thêm mô tả ngoại hình nhân vật đó
(tuổi/nghề nghiệp/bối cảnh sống khớp nội dung câu chuyện, xem video_ai_prompt_rules.md mục 9)

Output

PNG

Yêu cầu

- giữ đúng bảng màu/ánh sáng theo image_style_bible.md
- Nếu Character trống: không có nhân vật trong khung hình.
- Nếu Character là nhân vật khách: generate MỘT LẦN cho cả video, các Scene sau dùng lại đúng
  ảnh đó (không generate lại mỗi Scene).
- TUYỆT ĐỐI KHÔNG generate ảnh Hiền triết Anh Minh ở Stage này dưới bất kỳ hình thức nào.

========================================================
4. KLING / VEO3 IMG2VIDEO (chỉ chạy khi Stage 2B đánh dấu media_type = "clip")
========================================================

Mục tiêu

Animate một ảnh tĩnh có sẵn thành clip chuyển động — đây là cơ chế khoá nhận diện nhân vật
chính thức của pipeline (img2video, không train LoRA — xem image_style_bible.md mục 0B).

Chỉ chạy Stage này cho Scene có `media_type: "clip"` (theo Stage 2B). Scene `"static"` bỏ qua
hoàn toàn Stage này, đi thẳng từ Stage 3 (hoặc kho ảnh nhân vật) sang Stage 7.

Input

Ảnh gốc, chọn theo đúng 3 trường hợp Character ở Stage 2B:
- Character = "Hiền triết Anh Minh" → chọn từ kho ảnh nhân vật cố định ở image_style_bible.md
  mục 0B (KHÔNG tạo ảnh mới bằng text-to-image).
- Character = tên nhân vật khách → dùng đúng ảnh Flux đã generate cho người đó ở Stage 3 (không
  generate ảnh mới riêng cho Stage 4).
- Character trống → dùng ảnh B-roll từ Stage 3.
+
Motion Prompt (field Camera + Visual)

Output

MP4

Yêu cầu

- chuyển động tự nhiên, camera CHẬM (chuyển động mạnh dễ khiến model tự vẽ thêm chi tiết mặt
  không có trong ảnh gốc — xem image_style_bible.md mục 0B)
- không méo mặt
- không đổi nhân vật
- cinematic
- giữ ánh sáng

========================================================
5. ELEVENLABS AI
========================================================

Input

Voice Script

Output

Narration.mp3

Yêu cầu

- dùng ĐÚNG 1 voice ID đã clone/khoá riêng cho Anh Minh — KHÔNG dùng giọng preset ngẫu nhiên
  hay đổi giọng giữa các video (voice ID xem image_style_bible.md mục 10)
- giọng ấm
- tốc độ chậm
- ngắt nghỉ tự nhiên
- không đọc như MC
- đúng tone Anh Minh

========================================================
6. WHISPER AI
========================================================

Input

Narration.mp3

Output

subtitle.srt

Yêu cầu

- timestamp từng câu
- đồng bộ lời đọc
- UTF-8
- không tự sửa nội dung

========================================================
7. FFMPEG COMPOSER
========================================================

Input

Video Clips (Scene "clip", từ Stage 4)

Ảnh tĩnh + tham số Ken Burns (Scene "static", từ Stage 3 hoặc kho ảnh nhân vật — xem Stage 2B)

Narration

Subtitle

Music

Logo

Output

Video.mp4

Yêu cầu

- ghép đúng thứ tự theo Scene ID
- Scene "static": áp Ken Burns (zoom in/out chậm, pan ngang/dọc nhẹ) trong đúng **Duration** của
  Scene đó (lấy từ Master Script, ~110–130 từ/phút theo Voice — xem `video_rules.md` mục 1.C)
- Scene "clip": clip gốc 6–10 giây → kéo dài cảm giác thành 8–12 giây bằng zoom/pan/crop nhẹ
  ngay trên clip đó (không generate lại clip dài hơn)
- subtitle đồng bộ
- nhạc nhỏ hơn voice
- giữ 1080p
- xuất H264 mp4

========================================================
QUY TẮC CHUNG
========================================================

Không AI nào được tự ý thay đổi:

- Hook
- Nội dung lời
- CTA
- Giọng Anh Minh
- Nhân vật
- Thời lượng
- Ảnh nhân vật dùng cho img2video (chỉ lấy từ kho ảnh cố định — xem image_style_bible.md mục 0B)
- Voice ID (giọng đọc — xem image_style_bible.md mục 10)

Nếu phát hiện lỗi

→ trả lỗi

Không tự suy diễn.