# VIDEO RULES — VIDEO FACTORY

> Tải lên khu **Files** của Video Factory. File này chứa toàn bộ quy tắc làm video
> (đã tách khỏi `instructions` để dùng chung CORE_BRAIN cho mọi Factory).
> Danh tính, giọng, giá trị, tri thức → vẫn lấy từ CORE_BRAIN (`instructions`, các file knowledge).
> Cập nhật: 05/07/2026.
> Cập nhật: 18/07/2026 — mục 1.C chuẩn hoá field Scene ID zero-padded/Duration/Voice/Visual/
> Camera/Character/Emotion/Loop, tách Master Script khỏi prompt platform-specific (xem mục 1, 4, 5).
> Cập nhật: 20/07/2026 — mục 2 làm rõ VIDEO NGẮN gồm 2 loại nội dung khác nhau (suy ngẫm vs
> Dưỡng Sinh Ngắn — xem `instructions_VIDEO.md` mục 1B).
> Cập nhật: 25/07/2026 — **chốt VIDEO DÀI = 8–10 cảnh · tối đa 3 Clip · tối đa 13–16 Ảnh giữ**
> (mục 2 + mục 6), thay "15–20 cảnh" cũ và gỡ mâu thuẫn với bảng "30–35 cảnh" ở
> `model_selection_rules.md`. Thêm **mục 6B Image Motion Engine** — Ken Burns đơn thuần chỉ giữ
> được ảnh ~20–25 giây, muốn giữ 30–45 giây phải xếp tầng hiệu ứng. Trần ảnh nâng từ 10–12 lên
> 13–16 (25/07/2026, quyết định của chủ kênh) — thời lượng giữ mỗi ảnh giảm tương ứng còn 30–45
> giây thay vì 45–75. Học từ mô hình kênh
> My Dog & My Love (`youtube-mydog_mylove`), điều chỉnh theo thể loại chiêm nghiệm và thực tế
> khán giả kênh này **nghe nhiều hơn nhìn**.

---

## 0. MÔ HÌNH SẢN XUẤT (đọc trước — quyết định mọi thứ)

Mỗi kịch bản gồm **2 lớp tách rời**:
- **LỚP LỜI (kịch bản voiceover tiếng Việt):** đây là lớp **mang độ dài và giá trị** của video.
- **LỚP HÌNH (shot list B-roll):** danh sách cảnh hình cho công cụ AI (Veo…), **dùng lại được**.

**Nguyên tắc cốt lõi — "cảnh" ≠ "clip lấp đầy thời lượng":**
- Một **cảnh = một Ý / một nhịp nội dung** (chỗ hình thay đổi), KHÔNG phải một clip cố định 8 giây.
- **Độ dài video do LỜI DẪN quyết định**, không phải do số cảnh × độ dài clip.
- Công cụ AI hiện tạo clip ngắn (Veo 3.1: 4/6/8 giây mỗi lần). Để phủ một ý dài hơn:
  **loop / nối (extend) / giữ hình / đổi góc B-roll** dưới cùng một mạch lời dẫn.
- ⚠️ Cảnh báo pipeline: nếu chỉ tạo N clip rồi ghép, video sẽ ngắn hơn nhiều so với mục tiêu.
  Phải khớp **thời lượng lời dẫn** với thời lượng đích, rồi rải B-roll (lặp lại được) lên trên.

**Tool-agnostic:** viết prompt hình theo Ý và bố cục, không khóa cứng "8 giây". Công cụ tự
cắt theo giới hạn của nó; khi Veo 4/5 cho clip dài hơn, cùng kịch bản vẫn dùng được.

**Thuận tự động hóa (n8n):** output luôn tách rõ 2 lớp (LỜI / HÌNH) + đánh số cảnh, để máy
bóc tách: gửi prompt HÌNH cho Veo, gửi LỜI cho TTS/giọng đọc, rồi ghép.
------
## 0B. NGUYÊN TẮC KHI LÀM VIDEO TỪ BÀI VIẾT NGUỒN NGOÀI (không phải bài SEO tự viết)

Khi input là một bài viết có sẵn từ nguồn ngoài (không phải bài SEO do Funamark tự tạo qua
SEO Factory), tuyệt đối KHÔNG chuyển thể theo kiểu "đổi định dạng" (giữ cấu trúc, ví dụ, câu
chữ gốc rồi đọc thành lời). Thay vào đó:

- Chỉ lấy **ý / chủ đề / thông tin chung** của bài làm điểm cảm hứng.
- Viết lại **hoàn toàn mới** bằng giọng Anh Minh (theo `examples_and_hooks.md` +
  `philosophy_reference.md`), diễn đạt, cấu trúc, ví dụ, câu mở-câu kết đều do trợ lý sáng
  tạo lại — không mô phỏng sát bài gốc.
- Không dùng chung hook / cách vào đề / thứ tự lập luận của bài gốc.
- Đây là khác biệt với chế độ "chuyển đổi từ bài SEO có sẵn" ở mục 1 `instructions_VIDEO.md`
  (áp dụng khi bài SEO ĐÃ do chính Funamark viết) — trường hợp đó được giữ nguyên hook vì là
  nội dung tự sở hữu.

Mục đích: tránh rủi ro vi phạm bản quyền khi dùng bài viết của người khác làm nguồn cảm hứng.
---

## 1. KHUÔN XUẤT KỊCH BẢN (mỗi lần)

> **Cập nhật 18/07/2026:** chuẩn hoá mỗi cảnh thành khối field cố định (Scene ID zero-padded +
> Duration/Voice/Visual/Camera/Character/Emotion/Loop tách riêng) — để Master Script là **nguồn
> dữ liệu** duy nhất, không lẫn prompt riêng cho một công cụ AI cụ thể (Kling/Veo3/Sora...).
> Việc build prompt cho từng công cụ là một bước RIÊNG, làm SAU khi Master Script này đã hoàn
> tất (thủ công: đưa lại Master Script cho Claude và yêu cầu "chuyển thành prompt Kling/Veo3";
> tự động: node Scene Generator trong n8n, xem `video_ai_contract.md`). Nhờ vậy khi công cụ AI
> đổi/ra bản mới, chỉ cần sửa bước build prompt, không phải viết lại kịch bản.

- **A. TÊN VIDEO** + 1 câu ý chính (+ 1 câu hứa với video TRUNG/DÀI).
- **B. HOOK (3 giây đầu):** một câu/hình khơi tò mò điềm tĩnh — KHÔNG giật gân.
- **C. CÁC CẢNH** — mỗi cảnh là một khối field cố định, theo đúng thứ tự sau.
  ⚠️ **Định dạng bắt buộc:** mỗi cảnh phải mở đầu bằng heading markdown `### Scene <ID>` (VD
  `### Scene 001`, có thể kèm chú thích trong ngoặc: `### Scene 001 (HOOK)`), rồi tới các field
  dạng gạch đầu dòng `- **Tên field:** giá trị` theo đúng thứ tự dưới đây. Đây không phải sở
  thích trình bày — Code node của n8n (WF-07B) parse file `_master_script.md` đúng theo khuôn
  này (`video_ai_contract.md` GHI CHÚ VẬN HÀNH). Viết "Cảnh 1:", "**Scene 001**" hay đổi thứ tự
  field đều làm parser gãy. Xem ví dụ đầy đủ ở `examples_and_hooks.md` mục 6.
  - **Scene ID:** số thứ tự cảnh, zero-padded 3 chữ số (`001`, `002`, `003`...) — để pipeline
    map 1:1 sang file media cùng ID (`Voice001.mp3`, `Clip001.mp4`, `Subtitle001.srt`...).
  - **Duration:** thời lượng cảnh (giây), ước theo ngân sách lời của đoạn Voice trong cảnh đó.
  - **Voice** — tiếng Việt: voiceover cho ý đó. **Giọng đọc lồng riêng** (không để công cụ đọc
    tiếng Việt — giữ kiểm soát tông).
  - **Visual** — tiếng Anh: bối cảnh + chủ thể + hành động (không lặp lại nội dung đã có ở
    Camera/Character bên dưới). ⚠️ **KHÔNG mô tả khuôn mặt/trang phục/đặc điểm ngoại hình nhân
    vật ở đây** — nhận diện nhân vật do field Character đảm nhiệm (xem bên dưới), khớp đúng quy
    tắc "Scene Generator AI" ở `video_ai_contract.md` ("không mô tả khuôn mặt, không mô tả quần
    áo, không mô tả nhân vật — Character sẽ được n8n ghép sau"). Nhờ vậy Master Script dùng
    được thẳng cho cả Cách 1 (thủ công) lẫn Cách 2 (n8n) mà không cần sửa lại.
  - **Camera** — tiếng Anh: loại cảnh (close-up, wide…) + chuyển động máy (slow push-in,
    static, gentle pan…) + ánh sáng + âm thanh nền (ambient). Cũng không mô tả nhân vật ở đây,
    cùng lý do như field Visual.
  - **Character** — tên nhân vật xuất hiện trong cảnh; để trống nếu cảnh chỉ có B-roll trung
    tính không có nhân vật. Hai loại nhân vật, xử lý khác nhau ở bước sau (Master Script chỉ cần
    ghi đúng tên, không cần biết chi tiết pipeline):
    - **"Hiền triết Anh Minh"** — nhân vật DUY NHẤT có kho ảnh cố định (tham chiếu
      `core-brain/image_style_bible.md` mục 0B). Phần lớn cảnh tĩnh của Anh Minh lấy thẳng ảnh
      có sẵn (không generate); cảnh cần chuyển động mới img2video từ đúng ảnh đó.
    - **Tên nhân vật khách** (người trong câu chuyện đang kể, không phải Anh Minh) — KHÔNG có
      kho ảnh sẵn, generate mới ở Flux nhưng chỉ 1 lần cho cả video rồi dùng lại xuyên suốt (xem
      `video_ai_prompt_rules.md` mục 9 + `video_ai_contract.md` Stage 3).
    Khi làm thủ công (Cách 1), thấy field này có tên Anh Minh thì tự nạp bộ ảnh reference tương
    ứng vào Veo3/Kling; nhân vật khách thì tự tạo ảnh nhất quán rồi dùng lại. Khi tự động (Cách
    2), n8n đọc field này ở Stage 2B/3/4 (`video_ai_contract.md`) để định tuyến đúng nguồn ảnh.
  - **Emotion** — tâm trạng/cảm xúc chủ đạo của cảnh (VD: "tĩnh lặng", "ấm áp", "trầm ngâm").
  - **Loop** — `true`/`false`: cảnh này có dùng lại/loop được cho video khác không.
- **D. KẾT:** một câu lắng đọng, mở ra suy ngẫm. Không "like share" gắt.

**Ngân sách lời (giọng trầm-chậm):** ~110–130 từ/phút. Với video NGẮN, mỗi cảnh giữ gọn
(~14–16 từ Voice / ~8 giây Duration); với TRUNG/DÀI, viết lời dẫn liền mạch theo tổng thời
lượng trước (giữ mạch cảm xúc), rồi chia thành các cảnh theo khuôn field ở trên — mỗi field
Voice là một đoạn của lời dẫn liền mạch đã viết, không viết lại. Không nhồi chữ cho đủ, cũng
không kéo dãn một ý cho đủ giờ.

---

## 2. KHUNG ĐỊNH DẠNG

### VIDEO NGẮN (SHORT)
- Nền tảng: TikTok · Facebook Reels · YouTube Shorts.
- Thời lượng: **60–120 giây**.
- Số cảnh (ý) tham khảo: **5–8** · khuyến nghị **6**.
- Mục tiêu: một ý chính duy nhất · một hook · một bài học · một kết lắng đọng.
- ⚠️ **Hai loại nội dung khác nhau dùng chung khung thời lượng này** (xem `instructions_VIDEO.md`
  mục 1B): (a) video suy ngẫm/insight ngắn theo khuôn Hook→Thân→Kết ở mục này, và (b) video
  **Dưỡng Sinh Ngắn** — thị phạm một động tác cụ thể, theo khuôn kịch bản riêng ở
  `duong_sinh_bai_tap.md` mục 5 (nhịp cảnh đi theo động tác/hơi thở, không theo nhịp kể chuyện).
  Xác định rõ đang làm loại nào trước khi chọn cấu trúc.

### VIDEO TRUNG (MEDIUM)
- Nền tảng: Facebook Video · YouTube.
- Thời lượng: **3–6 phút**.
- Số cảnh (ý) tham khảo: **10–14** · khuyến nghị **12**.
- Mục tiêu: một chủ đề có chiều sâu hơn · có ví dụ hoặc một câu chuyện đời thực (xem `life_stories.md`).

### VIDEO DÀI (LONG)
- Nền tảng: YouTube · Podcast video.
- Thời lượng: **8–10 phút**.
- Số cảnh: **8–10 cảnh** (chốt 25/07/2026 — thay "15–20" cũ). Mỗi cảnh **55–75 giây lời dẫn**.
- **Ngân sách hình (trần cứng): tối đa 3 Clip + tối đa 13–16 Ảnh giữ** — xem mục 6 và
  `model_selection_rules.md` mục 1B.
- Mục tiêu: đào sâu chủ đề · nhiều lớp góc nhìn · có phần áp dụng thực tế · KHÔNG kéo dài một ý cho đủ giờ.
- Theo **kiến trúc long-form ở mục 4**.

**Nguyên tắc chung về số cảnh:**
- Mỗi cảnh đại diện cho một ý.
- Không thêm cảnh chỉ để đạt đủ số lượng; không cắt ý quan trọng để giảm số cảnh.
- Chất lượng nội dung quan trọng hơn số cảnh. Trợ lý được phép tăng/giảm số cảnh theo yêu cầu của chủ đề.

---

## 3. QUY TẮC TỰ CHỌN ĐỊNH DẠNG

- Khi người dùng nói **NGẮN / TRUNG / DÀI** → trợ lý **tự chọn số cảnh** theo khung trên,
  KHÔNG hỏi lại. (VD: "Làm video trung về dưỡng sinh" → tự quyết: chủ đề đơn giản ~10 cảnh,
  trung bình ~12, sâu ~14.)
- Khi người dùng nêu **thời lượng cụ thể** (2 phút / 5 phút / 10 phút) → **thời lượng được ưu
  tiên hơn số cảnh**; trợ lý tự điều chỉnh số cảnh + độ dài lời dẫn cho khớp.
- Khi người dùng **không nói rõ định dạng** → hỏi lại: "Bạn muốn video NGẮN, TRUNG hay DÀI?".
- Mục tiêu cuối cùng: **đúng trải nghiệm xem**, không phải đúng con số cảnh.

---

## 4. KIẾN TRÚC VIDEO DÀI (8–10 phút)

Mục tiêu: chiều sâu thật, để người xem thấy "mình vừa nhận được điều gì đó".

**Khung 5 phần:**
1. **MỞ (10–20s):** hook điềm tĩnh + một câu hứa nhẹ về điều người xem sẽ hiểu. Không clickbait.
2. **VÌ SAO ĐÁNG QUAN TÂM (20–30s):** nối chủ đề vào đời sống người xem.
3. **THÂN — 2–3 LỚP (phần chính):** khai triển qua 2–3 góc KHÁC NHAU, không lặp một ý. Mỗi lớp
   có mở–khai triển–lắng riêng + B-roll riêng. Có thể chèn một câu chuyện đời thực (xem `life_stories.md`).
4. **ÁP DỤNG (30–45s):** vài gợi ý cụ thể, nhẹ nhàng, người xem làm được ngay.
5. **KẾT LẮNG (15–20s):** một câu để nhớ.

**Kỷ luật giữ chân:** mỗi lớp phải THÊM cái mới; chuyển lớp thì "re-hook" nhẹ; thà 8 phút đặc
còn hơn 10 phút loãng.

**Khuôn xuất video dài:** A. Tên + ý chính + 1 câu hứa · B. Viết **lời dẫn liền mạch theo 5
phần** trước (như một bài nói chậm, để giữ mạch cảm xúc — đây là bước nháp) · C. Sau đó **chia
lời dẫn đã viết thành 8–10 cảnh** (mỗi cảnh 55–75 giây lời dẫn — xem trần ngân sách hình ở mục
2 và mục 6), đóng gói mỗi cảnh theo đúng khuôn field ở mục 1.C (Scene ID
zero-padded, Duration, Voice, Visual, Camera, Character, Emotion, Loop) — mỗi field Voice là một
đoạn của lời dẫn liền mạch đã viết ở bước B, không viết lại. Đánh dấu `Loop: true` cho cảnh
B-roll dùng lại/kéo dài để phủ dưới nhiều đoạn lời dẫn khác nhau.

---

## 5. QUY TẮC VIẾT PROMPT HÌNH (tóm tắt — chi tiết đầy đủ ở file riêng)

> Mục này hướng dẫn nội dung cần có trong field **Visual** + **Camera** (mục 1.C) khi viết Master
> Script — KHÔNG phải nơi viết prompt platform-specific. Prompt đầy đủ cho từng công cụ AI (Veo
> 3, Kling, Hailuo, Runway) là một bước RIÊNG, làm SAU khi Master Script hoàn tất → xem
> `video_ai_prompt_rules.md` (cách viết prompt, dùng chung mọi công cụ) + `model_selection_rules.md`
> (chọn công cụ nào cho từng loại cảnh — Master Script KHÔNG tự chỉ định công cụ). Ngoại hình
> nhân vật Anh Minh → luôn `core-brain/image_style_bible.md`, không định nghĩa lại ở đây.

- Field **Camera**: luôn nêu loại cảnh (close-up, wide…), chuyển động máy (slow push-in, static,
  gentle pan…), ánh sáng (soft morning light…), âm thanh nền (ambient). Mô tả cụ thể, điện ảnh,
  nhưng **tĩnh tại** — tránh chuyển động dồn dập, cắt nhanh.
- Field **Character**: chỉ ghi tên nhân vật (VD "Hiền triết Anh Minh"), tham chiếu
  `core-brain/image_style_bible.md` để giữ nhất quán nhận diện — không mô tả lại ngoại hình bằng
  chữ trong Visual/Camera (nhận diện nhân vật do field Character + ảnh reference đảm nhiệm, xem
  `image_style_bible.md` mục 0B — không nhét mô tả ngoại hình vào Visual/Camera).
- **Chỉ chữ Việt** trong khung hình (hoặc không chữ) — không bao giờ chữ Hán (theo style bible).
- Ưu tiên B-roll **trung tính, dùng lại được** (trà, vườn, hơi thở, cửa sổ, bàn tay, bước chân,
  sách…) để một kho hình phục vụ nhiều video — tiết kiệm chi phí generate.

---

## 6. NGÂN SÁCH HÌNH & CHI PHÍ (tóm tắt — chi tiết đầy đủ ở `model_selection_rules.md` mục 1B/5)

> **Cập nhật 25/07/2026 — thay hẳn mô hình "% cảnh là Clip" cũ.** Tỷ lệ 28–31% Clip trước đây
> khiến một video 8–10 phút cần 9–11 Clip, tức **1,0–1,2 clip/phút** — đắt hơn cả mức cao nhất
> của kênh tham chiếu My Dog & My Love (Tier 3: 0,68 clip/phút, chỉ mở khi doanh thu đã gấp 3–5
> lần chi phí). Nay chuyển sang **trần cứng theo số tuyệt đối**, học từ mô hình đó.

**Trần cứng cho VIDEO DÀI (8–10 phút):**

| Thành phần | Trần |
|---|---|
| Cảnh | 8–10 (mỗi cảnh 55–75 giây lời dẫn) |
| Clip AI video | **tối đa 3** |
| Ảnh giữ | **tối đa 13–16** (mỗi ảnh giữ 30–45 giây) |

- **Vị trí 3 Clip:** MỞ (Anh Minh nói trực diện, neo sự hiện diện nhân vật) · một khoảnh khắc chủ
  đạo giữa bài · KẾT LẮNG. Không rải đều — đặt đúng 3 điểm cảm xúc.
- **Ảnh làm start-frame cho Clip KHÔNG tính vào trần 13–16.** Chỉ đếm ảnh **giữ độc lập** (tự nó
  hiện trên màn hình). Với kênh này, start-frame của cả 3 Clip lấy thẳng từ `characters/` nên
  **chi phí ảnh nhân vật bằng 0** — không generate lại (xem `core-brain/image_style_bible.md` mục 0B).
- **Khán giả kênh này NGHE nhiều hơn NHÌN** (nội dung sức khỏe/triết lý dạng kể chuyện, thường
  bật lên nghe khi đang làm việc khác). Vì vậy ưu tiên giữ ảnh ở **mức dài của khoảng (40–45
  giây)**, không cần đổi hình dồn dập. Giá trị video nằm ở lời dẫn — hình để nâng đỡ, không để
  tranh sự chú ý.
- **Cách tính ra 13–16 ảnh:** video 8–10 phút trừ đi ~27 giây của 3 Clip còn ~450–570 giây hình.
  Chia cho 13–16 ảnh ra ~30–45 giây mỗi ảnh. Muốn ảnh giữ lâu hơn thì giảm số ảnh, muốn đổi hình
  dày hơn thì tăng số ảnh — nhưng **không vượt trần 16**.
- Tạo MỘT kho B-roll tĩnh đẹp, dùng lại across nhiều video — đừng generate mới từng cảnh.
- Clip AI video generate gốc 6–10 giây → khi dựng, kéo dài cảm giác thành 8–12 giây bằng
  zoom/pan/crop nhẹ (không generate clip dài hơn — tốn thêm chi phí).
- Công cụ AI lo HÌNH + ambient; lời dẫn tiếng Việt lồng riêng (TTS chất lượng cao hoặc người đọc).

### 6B. IMAGE MOTION ENGINE (bắt buộc — không giữ ảnh lâu chỉ bằng Ken Burns)

> Thêm 25/07/2026. Đây là mảnh còn thiếu khiến các tính toán trước đó sai: **Ken Burns đơn thuần
> chỉ giữ được một ảnh ~20–25 giây trước khi màn hình thấy đứng chết.** Muốn giữ 30–45 giây thì
> phải xếp tầng hiệu ứng. Học từ `visual_bible_dog1.md` §15.4 của kênh My Dog & My Love.

Mỗi ảnh giữ đi qua một chồng lớp hiệu ứng ở bước dựng — **Ken Burns là lớp nền của mọi ảnh**,
cộng thêm **tối đa 2 lớp** trong số:

- **Parallax** — tách ảnh thành lớp gần/giữa/xa trôi khác tốc độ. Dùng cho cảnh không gian, hoặc
  ảnh có chủ thể tiền cảnh rõ (bàn tay, khung cửa, tách trà).
- **Depth of Field** — chuyển nét (rack focus) hoặc mờ hậu cảnh co/giãn nhẹ, để dẫn mắt người xem
  giữa một lần giữ dài. Hiệu quả nhất với ảnh giữ trên 35 giây.
- **Light Rays / Light Leak** — tia nắng mềm qua cửa sổ/tán cây. Để dành cho đoạn ấm áp, hy vọng,
  chữa lành — không dùng ở đoạn trầm buồn, sẽ mất trọng lượng cảm xúc.
- **Particles** — bụi nắng, lá rơi, hạt mưa. Dùng rất tiết chế, chỉ khi mùa/thời tiết trong nội
  dung gọi tới. Không thêm chỉ để cho đẹp.

⚠️ **Không chồng quá 2 lớp phụ** — nhiều hơn sẽ thành hình "làm quá", phạm đúng tinh thần tĩnh
tại/chân thật của kênh. **Không dùng Camera Shake** (kể cả nhẹ) cho kênh này: My Dog dùng nó cho
cảnh căng thẳng/hành động, còn nội dung Anh Minh là chiêm nghiệm — rung máy sẽ đọc thành lỗi kỹ
thuật chứ không thành chủ ý.

---

## 7. CHỐNG LẶP KHI LÀM HÀNG TRĂM VIDEO

**Nguyên tắc cốt lõi:** Cùng chủ đề ≠ cùng trải nghiệm. Người xem không bao giờ được cảm thấy "tôi đã xem video này rồi."

**Xoay vòng cấu trúc kịch bản (5 biến thể):**
- **Cấu trúc A:** Hook → Thói quen hằng ngày → Ảnh hưởng thân-tâm → Gợi ý nhẹ → Kết lắng.
- **Cấu trúc B:** Hook → Nhận diện cảm xúc → Lý giải nhịp sống hiện đại → Thay đổi nhỏ → Suy ngẫm.
- **Cấu trúc C:** Hook → Nguyên nhân ẩn → Tác động lặng lẽ → Trấn an → Khép nhẹ.
- **Cấu trúc D:** Hook → Tình huống quen thuộc → Cái mệt phía sau → Góc nhìn mới → Kết rất người.
- **Cấu trúc E:** Hook → Hiểu lầm thường gặp → Vì sao → Cách nhìn dịu hơn → An ủi.

**Xoay vòng góc vào (không lặp cùng góc 2 video liên tiếp):**
mệt mỏi cảm xúc · cảm giác cơ thể · thói quen hằng ngày · nhịp sống hiện đại · giấc ngủ ·
ăn uống · quá tải cảm xúc · phản ứng căng thẳng · hồi phục · cân bằng năng lượng.

**Xoay vòng bối cảnh hình:** góc trà · bàn viết cửa sổ · hiên nhà · vườn nhỏ · kệ sách · bước chân trong vườn.

**Xoay vòng câu kết:** tránh lặp "hãy chăm sóc cơ thể mình" — xoay giữa: an ủi cảm xúc / nhắc nhở thực tế / chiêm nghiệm lặng / khích lệ nhẹ / nhận ra bình thường.

## 8. THUMBNAIL ETHICS (ảnh đại diện video)

Thumbnail là ấn tượng đầu tiên — phải **mời người xem**, không tấn công cảm xúc.

**Ưu tiên:**
- Hình ảnh ấm, sạch, gợi tò mò điềm tĩnh
- Khuôn mặt nhân vật biểu cảm chân thực, nhẹ nhàng
- Tiêu đề ngắn, rõ, khơi curiosity — không bỏ lửng "…"
- Màu sắc theo bảng màu kênh (be, nâu, olive, gỗ)

**TUYỆT ĐỐI KHÔNG:**
- Hình đau đớn, bệnh tật, nội tạng, trước-sau gây sốc
- Biểu cảm phóng đại kiểu O_O, hoảng loạn
- Chữ CAPS LOCK, dấu chấm than dồn dập
- Fake urgency: "XEM NGAY KẺO MUỘN", "BÍ MẬT", "SỐC"
- Dọa bệnh, dọa chết, thống kê hù dọa
- Màu neon chói, hiệu ứng phô trương

**Nguyên tắc:** Thumbnail đúng tông kênh khiến người xem nghĩ "video này trông thú vị" — không phải "video này khiến tôi sợ".