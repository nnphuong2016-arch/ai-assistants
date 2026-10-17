# CLAUDE.md — SHORT FACTORY (kịch bản Short cho Reel & YouTube Shorts)

Version: 1.3
Cập nhật: 17/10/2026

> File nhắc việc riêng cho Short Factory, đặt trong chính thư mục này để mỗi lần mở cửa sổ làm việc ở đây,
> Claude tự đọc lại và không quên quy trình. File này KHÔNG thay thế `CLAUDE.md` gốc ở root repo
> (`ai-assistants/CLAUDE.md`) — đó vẫn là nguồn gốc duy nhất cho toàn hệ thống. File này là bản tóm tắt +
> checklist thao tác nhanh, chuyên riêng cho Short Factory.

---

## 0. FACTORY NÀY LÀM RA CÁI GÌ

Mỗi lần chạy ra **một file kịch bản `.md`** — một đoạn lời đọc ngắn (thường 30–90 giây, tối đa 2 phút) của **Hiền triết Anh Minh**.
Phần còn lại do n8n lo (workflow `WFAnhMinhC204`): đọc nguyên file làm lời đọc bằng giọng VieNeu, dựng phụ đề,
ghép clip thiên nhiên + nhạc nền + logo, rồi workflow `WFAnhMinhC205` đăng YouTube Shorts. Cùng một video đó
dùng cho Reel.

**File được đọc thành tiếng NGUYÊN VĂN — trừ đúng một dòng: dòng đầu `# Tiêu đề`** (tiêu đề YouTube của video, lấy từ
tiêu đề bài viết tương ứng, KHÔNG được đọc). Mọi chữ còn lại trong file đều là lời đọc: không ghi chú, không tiêu đề
mục khác, không hướng dẫn quay, không hashtag. Chi tiết khuôn file: `output_schema.md`.

---

## 1. THỨ TỰ ĐỌC BẮT BUỘC TRƯỚC KHI VIẾT (không bỏ qua, không đảo thứ tự)

Đúng theo Priority Order ở `execution_flow.md`:

1. `instructions_short.md` — mục đích, vai trò, phạm vi, đầu vào/đầu ra.
2. `execution_flow.md` — trình tự 10 bước bắt buộc (mục 2 bên dưới).
3. `writing_rules.md` — được phép/không được phép viết gì (mục 4.1 = ranh giới thương hiệu tuyệt đối).
4. `writing_craft.md` — dạy giọng viết cho lời đọc (tra khi cần).
5. `quality_check.md` — tự kiểm trước khi xuất, ≥2 lỗi thì viết lại.
6. `short_frameworks.md` — chọn 1 trong 15 khung F01–F15 (kèm khi nào KHÔNG nên dùng).
7. `emotion_palette.md` — chọn 1 cảm xúc chính (+ tối đa 1 cảm xúc phụ).
8. `bai-dang-Facebook-Anh-Minh.md` (gốc repo `ai-assistants/`) — kho 210 hook/chủ đề của Anh Minh, 7 series × 30 dòng, nguồn ý tưởng thứ hai.
9. `idea_library.md` — nguồn ý tưởng thứ ba (tự sinh) khi hai nguồn trên không đủ.
10. `hook_library.md` — 20 kiểu câu mở + công thức Hook Engine.
11. `topic_map.md` — bản đồ chủ đề theo trải nghiệm sống + bảng quy đổi sang 6 trụ chính thức.
12. `short_examples.md` — hai kịch bản mẫu hoàn chỉnh + kỹ thuật nhỏ; so sánh, KHÔNG copy.
13. `short_log.md` — nhật ký từng Short: đọc 5–8 dòng gần nhất để CHỐNG LẶP, ghi thêm sau mỗi bài, điền số liệu sau khi đăng.
14. `output_schema.md` — đóng gói đúng khuôn: khối A (file kịch bản) + khối B (gói đăng, nhật ký).
15. `custom_gpt_instructions.md` — bản gọn (dưới 8000 ký tự) để DÁN vào ô Instructions của Custom GPT; không dùng để viết bài ở đây.

Ngoài ra, khi cần: `core-brain/dong_hanh_nguoi_benh.md` (nếu bài chạm người bệnh/người già/người chăm sóc —
`writing_rules.md` mục 4.1 yêu cầu bắt buộc tra file này), `core-brain/seasonal_calendar.md` (bài theo mùa/dịp).

---

## 2. QUY TRÌNH 10 BƯỚC (`execution_flow.md`) — KHÔNG BỎ BƯỚC, KHÔNG ĐẢO THỨ TỰ

Understand → Select Topic (CHỈ 1 topic chính) → Generate Ideas (3 nguồn: chủ đề người dùng đưa trực tiếp ưu tiên cao
nhất → kho 210 hook → `idea_library.md`) → **Safety Filter (STEP 3.5)** → Choose Hook → Choose Framework (F01–F15) →
**Choose Emotion** (chọn TRƯỚC khi viết) → Write Draft → Compare Examples → Quality Review → Output.

Nếu một bước chưa đạt, quay lại đúng bước đó theo Retry Logic — không sửa chắp vá từng câu.

**STEP 3.5 Safety Filter là bắt buộc tuyệt đối.** Ý tưởng tự sinh KHÔNG được coi là đã an toàn sẵn.

---

## 3. TINH THẦN GIỌNG VIẾT (đọc `writing_craft.md` để hiểu sâu)

- Viết để **nghe**, không để đọc: như đang ngồi uống trà nói chuyện, KHÔNG như giáo viên/báo chí/AI.
- Câu ngắn, mỗi dòng một ý nhỏ, có chỗ nghỉ. Không giải thích quá nhiều, không kết luận thay người nghe
  ("Bài học là...") — dùng câu hỏi mở hoặc khoảng lặng.
- **Một bài = MỘT ý chính duy nhất.** Không gộp ngủ + ăn + tập + thiền vào một bài.
- Dùng chi tiết cụ thể thay vì khái quát ("Chuông báo thức reo đến lần thứ ba" thay vì "Mình rất mệt").
- Tránh câu mở kiểu AI: "Bạn có biết...", "Hôm nay mình sẽ chia sẻ...", "5 cách để...", "Theo nghiên cứu...".
- Không CHỮ HOA, không emoji, không dấu chấm than, không hashtag, không chữ số (viết số bằng chữ).
- **Độ dài:** ba cỡ — Nhanh 30–45 giây · Tiêu chuẩn 45–90 giây · Kể chuyện 90–120 giây (`writing_rules.md` mục 6.1). **Tối đa 2
  phút — là mức trần, không phải mục tiêu:** không phải bài nào cũng dài, không có sàn cứng, ngắn hơn được nếu ý đã trọn. Trần cứng
  2100 ký tự (n8n chặn đúng mốc này và chặn thêm nếu giọng đọc vượt 120 giây).
- **Chống lặp:** trước khi chọn ý, đọc 5–8 dòng gần nhất của `short_log.md`; không dùng lại cùng kiểu mở, ẩn dụ, khung kể, kiểu
  kết như hai Short liền trước. Sau mỗi bài, thêm một dòng vào log.
- **Chấm hai tầng** (`quality_check.md`): Tầng 1 là cổng (an toàn, đúng khuôn, trong giới hạn); Tầng 2 là chất lượng (câu mở cụ thể,
  chuyển biến, kết có dư âm, phép thử "bỏ tên Anh Minh đi"). An toàn thì cứng; nghệ thuật thì linh hoạt (`writing_rules.md` mục 6.2).
- **Short không phải bài SEO hay video dài rút ngắn:** cùng chủ đề nhưng viết lại từ đầu như một câu chuyện để nghe
  (`instructions_short.md` mục 5A).
- **Nhân xưng** (`writing_rules.md` mục 5.1): "ta/chúng ta" và "bạn" là chính; "mình" **được nghĩ, không được nhớ**.
  Cấm dựng quan hệ gia đình riêng cho nhân vật và hồi ký cá nhân cụ thể.
- **Móc neo ký ức:** mỗi bài cần ≥1 trong 3 — ẩn dụ thiên nhiên mạnh / câu hỏi khiến người nghe dừng một nhịp /
  điều nhận ra không hiển nhiên (`writing_craft.md` mục 36).
- **Tiêu đề** = dòng `# …` đầu file: với Short viết từ kho 210 hook thì dùng ĐÚNG câu của dòng đó trong kho (bỏ dấu chấm
  cuối); chủ đề khác thì viết một câu tiêu đề cùng kiểu. Không được đọc thành tiếng.
- **Câu kết** (dòng cuối) để người nghe mang theo: mặc định là MỘT câu hỏi tự vấn in đậm `**…**`; có thể đổi kiểu (nhận ra / hình
  ảnh / lời nhắn / khoảng lặng) nhưng không dùng cùng một kiểu quá hai Short liên tiếp. Không còn là tiêu đề.

---

## 4. RANH GIỚI THƯƠNG HIỆU TUYỆT ĐỐI (`writing_rules.md` mục 4.1)

Cùng một nhân vật Hiền triết Anh Minh với Website/YouTube/Chat:
- Không dọa bệnh, giật gân, CAPS LOCK, dọa ung thư · không chẩn đoán/kê đơn/thay bác sĩ · không thần bí/mê
  tín/bói toán · không toxic motivation/thao túng cảm xúc · không tranh cãi chính trị.
- Chạm chủ đề "Đồng hành" (người bệnh/người già/người chăm sóc) → thêm ranh giới cứng từ
  `core-brain/dong_hanh_nguoi_benh.md`: không hứa khỏi bệnh, không đụng diễn tiến bệnh, luôn đặt song song bác sĩ.
- Nhắc sản phẩm → tỷ lệ giá trị/sản phẩm ~95/5; với Short thì **không nhắc sản phẩm**.
- **Không dùng lời kêu gọi rẻ tiền**: "Bình luận bên dưới nhé", "Chia sẻ cho bạn bè", "Theo dõi kênh để...". Câu hỏi
  cuối chỉ là câu tự vấn.

---

## 5. PHẠM VI — CHỈ LÀM, KHÔNG LÀM

**Chỉ làm:** viết kịch bản Short (lời đọc) theo giọng Hiền triết Anh Minh.

**KHÔNG làm** (việc của Factory khác hoặc của n8n):
- Không viết bài SEO Website → SEO Factory.
- Không viết kịch bản video dài → Video Factory.
- Không viết prompt ảnh/clip — Short ghép từ clip thiên nhiên có sẵn, không sinh ảnh.
- Không trả lời comment → Community Factory.
- Không tạo workflow n8n, không viết email, không viết quảng cáo.
- Không tự đặt mô tả, thẻ — workflow tự lấy: tiêu đề = dòng `# …` đầu file + `#Shorts`, mô tả = nguyên lời đọc,
  thẻ cố định. (Tiêu đề thì Factory viết ở dòng đầu file; file không có dòng `# …` thì n8n dùng tạm câu in đậm cuối bài.)

---

## 6. TRƯỚC KHI XUẤT — `quality_check.md` (checklist DUY NHẤT)

6 nhóm: An toàn thương hiệu · Nội dung · Cảm xúc · Giọng văn · Khuôn Short · Móc neo ký ức.

**Hai ngưỡng khác nhau:**
- **Nhóm 1 (An toàn):** sai **1** mục → viết lại ngay, không ngoại lệ.
- **Nhóm 2–6:** sai **≥2** mục → viết lại.

---

## 7. ĐẦU RA & NƠI LƯU

- **Interactive Mode** (chat trực tiếp): xuất **khối A** (tên file + toàn văn file) rồi **khối B** (Title, Reel Caption, Mood,
  Topic, Pillar, Framework, Hook Source, Hook Type, Ending Type, Size, Log Row) theo `output_schema.md`.
- **Khi lưu file `.md`:** CHỈ chứa nội dung kịch bản (lời đọc) — KHÔNG kèm các field nội bộ.
- **Tên file:** `<chuỗi>.<thứ tự>.<slug-không-dấu>.md` — ví dụ `1.2.thay-doi-cua-co-the-dien-ra-rat-lau-truoc-khi-ta-nhan-ra.md`.
  Số hiệu theo kho 210 hook: Short viết từ Series N dòng M của kho → file `N.M.…` (1.1 = Series 1 dòng 1, 1.2 = dòng 2).
  Chủ đề không lấy từ kho → chuỗi `0` (`0.1`, `0.2`…, n8n sẽ làm trước hàng đợi của kho). Không trùng số nào đang có trong thư mục,
  không gắn với số tập video dài.
- **Nơi lưu:** Google Drive tài khoản funamark, thư mục **"Kich-ban-short for Reel FB & Youtube"**
  (`Anh Minh - N8N Trigger/Kich-ban-short for Reel FB & Youtube`, parentId `1SoKkr2dzkuc0sNWzYkHFv_Z_R03FRw38`).
  Lưu `.md` thuần (nếu dùng `create_file` thì `disableConversionToGoogleType: true`).
- **Không tự đổi tên file đã nằm trong thư mục** — tiền tố `SHORTDONE_`/`DONE_` do n8n tự thêm để đánh dấu
  tiến độ. File chưa có tiền tố là file đang chờ làm.
- Không tạo manifest JSON, không thêm CLAUDE.md hay file cấu hình vào thư mục Drive đó.
