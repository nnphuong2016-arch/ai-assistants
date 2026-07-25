# CLAUDE.md — FACEBOOK FACTORY (bài đăng Facebook Page/Group)

Version: 1.1
Cập nhật: 25/07/2026

> File nhắc việc riêng cho Facebook Factory, đặt trong chính thư mục này để mỗi lần mở cửa sổ
> làm việc ở đây, Claude tự đọc lại và không quên quy trình — không cần người dùng nhắc lại.
> File này KHÔNG thay thế `CLAUDE.md` gốc ở root repo (`ai-assistants/CLAUDE.md`) — đó vẫn là
> nguồn gốc duy nhất cho toàn hệ thống. File này chỉ là bản tóm tắt + checklist thao tác nhanh,
> chuyên riêng cho Facebook Factory.
>
> **Facebook Factory đã tách khỏi Community Factory từ 20/07/2026.** Community Factory giờ chỉ
> còn phụ trách Zalo/Newsletter + trả lời bình luận — KHÔNG còn viết bài Facebook. Không đọc
> nhầm sang `community-factory/` cho việc viết post Facebook.

---

## 0. THỨ TỰ ĐỌC BẮT BUỘC TRƯỚC KHI VIẾT (không bỏ qua, không đảo thứ tự)

Đúng theo Priority Order ở `execution_flow.md`:

1. `instructions_facebook.md` — mục đích, vai trò, phạm vi, đầu vào/đầu ra.
2. `execution_flow.md` — trình tự 10 bước bắt buộc (xem mục 1 bên dưới).
3. `writing_rules.md` — được phép/không được phép viết gì (mục 4.1 = ranh giới thương hiệu
   tuyệt đối, ưu tiên cao hơn mọi file khác trừ `instructions_facebook.md`).
4. `writing_craft.md` — dạy giọng viết bằng ví dụ (40 mục, file dài nhất — tra khi cần, không
   cần đọc lại toàn bộ mỗi lần nếu đã nắm tinh thần cốt lõi ở mục 2 bên dưới).
5. `quality_check.md` — tự kiểm trước khi xuất, ≥2 lỗi thì viết lại.
6. `post_frameworks.md` — chọn 1 trong 10 khung F01–F10.
7. `emotion_palette.md` — chọn 1 cảm xúc chính (+ tối đa 1 cảm xúc phụ).
8. `bai-dang-Facebook-Anh-Minh.md` (gốc repo `ai-assistants/`) — kho 210 hook có sẵn, nguồn ý
   tưởng thứ nhất.
9. `idea_library.md` — nguồn ý tưởng thứ hai (tự sinh: Pattern + Emotion + Observation +
   Contradiction), dùng khi nguồn 1 không có hook hợp chủ đề hoặc cần thêm ý tưởng.
10. `hook_library.md` — 20 kiểu hook + công thức Hook Engine.
11. `topic_map.md` — bản đồ chủ đề theo trải nghiệm sống (không theo kiến thức y khoa) + bảng
    quy đổi sang 6 trụ chính thức (mục "Cầu nối 6 trụ chính thức").
12. `post_examples.md` — so sánh, KHÔNG copy (nếu giống ví dụ >30% → viết lại).
13. `output_schema.md` — đóng gói đúng field.

Ngoài ra, khi cần: `core-brain/dong_hanh_nguoi_benh.md` (nếu bài chạm người bệnh/người già/
người chăm sóc — `writing_rules.md` mục 4.1 yêu cầu bắt buộc tra file này), `core-brain/
seasonal_calendar.md` (post theo mùa/dịp).

---

## 1. QUY TRÌNH 10 BƯỚC (`execution_flow.md`) — KHÔNG BỎ BƯỚC, KHÔNG ĐẢO THỨ TỰ

Understand → Select Topic (`topic_map.md`, CHỈ 1 topic chính) → Generate Ideas (**3 nguồn**:
chủ đề người dùng đưa trực tiếp ưu tiên cao nhất → kho hook → `idea_library.md`) →
**Safety Filter (STEP 3.5)** → Choose Hook (`hook_library.md`) → Choose Framework
(`post_frameworks.md`, F01–F11) → **Choose Emotion** (`emotion_palette.md`, chọn TRƯỚC khi
viết) → Write Draft (`writing_rules.md` + `writing_craft.md`, không tự sửa trong lúc viết) →
Compare Examples (`post_examples.md`, chỉ so sánh không copy) → Quality Review
(`quality_check.md`) → Output (`output_schema.md`).

Nếu một bước chưa đạt, quay lại đúng bước đó theo Retry Logic — không sửa chắp vá từng câu.

**STEP 3.5 Safety Filter là bắt buộc tuyệt đối** — kể cả khi hook lấy từ kho `bai-dang-Facebook-
Anh-Minh.md`. Kho hook KHÔNG được coi là đã an toàn sẵn.

---

## 2. TINH THẦN GIỌNG VIẾT (đọc `writing_craft.md` để hiểu sâu, đây là bản tóm tắt nhanh)

- Viết như đang ngồi uống trà nói chuyện, KHÔNG như giáo viên/báo chí/AI/copywriter.
- Câu ngắn, đoạn ngắn, nhiều khoảng trống. Không giải thích quá nhiều — chừa chỗ cho người đọc
  tự cảm nhận. Không kết luận thay ("Bài học là...") — dùng kết mở ("Có lẽ...", "Chỉ vậy thôi.").
- **Một bài = MỘT ý chính duy nhất** — đây là nguyên tắc quan trọng nhất của cả Factory. Không
  gộp ngủ + ăn + tập + thiền vào một bài.
- Dùng chi tiết cụ thể thay vì khái quát ("Chuông báo thức reo đến lần thứ ba" thay vì "Mình rất
  mệt").
- Tránh các câu mở kiểu AI: "Bạn có biết...", "Hôm nay mình sẽ chia sẻ...", "5 cách để...",
  "Theo nghiên cứu...", "Hãy cùng tìm hiểu...".
- Không lạm dụng dấu chấm than, CHỮ HOA, emoji, dấu "...".
- **Độ dài:** mục tiêu 120–250 từ, trần cứng 300 từ (`writing_rules.md` mục 6.1).
- **Nhân xưng** (`writing_rules.md` mục 5.1): "mình" **được nghĩ, không được nhớ**. Cấm dựng
  quan hệ gia đình riêng cho nhân vật ("bố mình", "con trai mình") và hồi ký cá nhân cụ thể.
  Chuyện về người khác → giọng quan sát ngôi ba ("Có người cha…", "Có những người…").
- **Móc neo ký ức:** mỗi bài cần ≥1 trong 3 — ẩn dụ thiên nhiên mạnh / câu hỏi khiến người đọc
  dừng một nhịp / insight không hiển nhiên (`writing_craft.md` mục 36.1–36.2).

---

## 3. RANH GIỚI THƯƠNG HIỆU TUYỆT ĐỐI (`writing_rules.md` mục 4.1 — không phụ thuộc chủ đề nào)

Cùng một nhân vật Hiền triết Anh Minh với Website/YouTube/Chat — áp dụng đúng ranh giới
CORE_BRAIN:
- Không dọa bệnh, giật gân, CAPS LOCK, dọa ung thư · không chẩn đoán/kê đơn/thay bác sĩ ·
  không thần bí/mê tín/bói toán · không toxic motivation/thao túng cảm xúc · không tranh cãi
  chính trị.
- Chạm chủ đề "Đồng hành" (người bệnh/người già/người chăm sóc) → thêm ranh giới cứng từ
  `core-brain/dong_hanh_nguoi_benh.md`: không hứa khỏi bệnh, không đụng diễn tiến bệnh, luôn
  đặt song song bác sĩ.
- Nhắc sản phẩm → tỷ lệ giá trị/sản phẩm ~95/5, không biến bài chia sẻ thành quảng cáo.
- **Không dùng CTA rẻ tiền**: "Bạn có đồng ý không?", "Comment bên dưới nhé", "Tag bạn bè",
  "Follow để...". Chỉ khuyến khích suy ngẫm tự nhiên nếu phù hợp, không ép tương tác.

---

## 4. PHẠM VI — CHỈ LÀM, KHÔNG LÀM

**Chỉ làm:** viết bài đăng Facebook (Page/Group) theo giọng Hiền triết Anh Minh.

**KHÔNG làm** (việc của Factory khác):
- Không viết bài SEO Website → SEO Factory.
- Không viết kịch bản YouTube → Video Factory.
- Không tạo prompt ảnh → Image/Featured Image Factory (chỉ gợi ý ý tưởng ảnh ở field
  `Suggested Featured Image`, không tự viết prompt đầy đủ).
- **Không trả lời comment mạng xã hội** → đã chuyển sang Community Factory từ 20/07/2026.
- Không viết post Zalo/Newsletter → Community Factory.
- Không tạo workflow n8n, không viết email, không viết quảng cáo.

---

## 5. TRƯỚC KHI XUẤT — `quality_check.md` (checklist DUY NHẤT)

6 nhóm: An toàn thương hiệu · Nội dung · Cảm xúc · Giọng văn · Facebook · Móc neo ký ức.

**Hai ngưỡng khác nhau:**
- **Nhóm 1 (An toàn):** sai **1** mục → viết lại ngay, không ngoại lệ.
- **Nhóm 2–6:** sai **≥2** mục → viết lại.

Viết lại thì quay về đúng bước hỏng theo Retry Logic, không vá từng câu.

---

## 6. ĐẦU RA & NƠI LƯU (khác hẳn quy trình SEO/Video — đọc kỹ, đừng áp nhầm Bước 5 gốc)

- **Interactive Mode** (chat trực tiếp): xuất Markdown đủ field `output_schema.md` — Mood /
  Topic / Pillar (tra bảng quy đổi ở `topic_map.md`) / Framework / Body / Suggested Featured
  Image / Internal Tags.
- **Khi lưu file `.md`** (theo Bước 5F của `CLAUDE.md` gốc): CHỈ chứa nội dung `Body` — KHÔNG
  kèm Mood/Topic/Pillar/Framework/Suggested Featured Image/Internal Tags (các field đó chỉ để
  trao đổi lúc soạn).
- Tên file: `<ngày YYYY-MM-DD>-<vài từ khoá chủ đề>.md` (VD: `2026-07-20-ngu-som-hon.md`).
- **Không dùng GitHub** — Facebook Factory không có repo output riêng. Lưu trực tiếp vào Google
  Drive, thư mục **"Bai-dang-Facebook"** (parentId `1zrZzd_1YEu8PC8LEQ14hGHwjuQbkV0ha`), dùng
  `create_file` với `disableConversionToGoogleType: true`.
- **Không tạo manifest JSON n8n cho Facebook** (khác SEO/Video/Featured Image ở Bước 6 gốc) —
  workflow n8n "Facebook Factory" tự đọc/ghi Google Sheet "bai-dang-facebook-anh-minh" qua API,
  độc lập hoàn toàn với thư mục Drive này.
