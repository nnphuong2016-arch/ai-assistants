# VIDEO PROMPT TEMPLATES
STATUS: LOCKED
VERSION: V1.1
DATE: 18/07/2026

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
3. FLUX IMAGE AI (chỉ cho cảnh KHÔNG có nhân vật)
========================================================

Mục tiêu

Sinh ảnh B-roll trung tính cho cảnh không có nhân vật (field Character trống ở Master Script).
KHÔNG dùng bước này để tạo ảnh nhân vật mới — cảnh có nhân vật bỏ qua Stage này, lấy thẳng ảnh
có sẵn trong kho ảnh nguồn (xem image_style_bible.md mục 0B) làm input cho Stage 4.

Input

Scene Prompt (field Visual + Camera)

Output

PNG

Yêu cầu

- giữ đúng bảng màu/ánh sáng theo image_style_bible.md
- không có nhân vật trong khung hình (cảnh này chỉ dùng khi Character trống)

========================================================
4. KLING / VEO3 IMG2VIDEO
========================================================

Mục tiêu

Animate một ảnh tĩnh có sẵn thành clip chuyển động — đây là cơ chế khoá nhận diện nhân vật
chính thức của pipeline (img2video, không train LoRA — xem image_style_bible.md mục 0B).

Input

Ảnh gốc — nếu Character có giá trị: chọn từ kho ảnh nhân vật cố định ở image_style_bible.md
mục 0B (KHÔNG tạo ảnh mới bằng text-to-image); nếu Character trống: dùng ảnh B-roll từ Stage 3
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
  hay đổi giọng giữa các video (voice ID xem image_style_bible.md mục 11)
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

Video Clips

Narration

Subtitle

Music

Logo

Output

Video.mp4

Yêu cầu

- ghép đúng thứ tự
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
- Voice ID (giọng đọc — xem image_style_bible.md mục 11)

Nếu phát hiện lỗi

→ trả lỗi

Không tự suy diễn.