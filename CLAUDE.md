# FUNAMARK — Hệ AI "Hiền Triết Anh Minh"

> **QUAN TRỌNG BẬC NHẤT — TUYỆT ĐỐI KHÔNG BỎ QUA:** Repo này là bộ não & quy tắc gốc quyết định
> toàn bộ chất lượng, an toàn và tính nhất quán của nhân vật "Hiền triết Anh Minh" — trên mọi
> định dạng nội dung (bài SEO, kịch bản video, prompt ảnh, post cộng đồng, chat). Mọi nội dung
> tạo ra mà KHÔNG đi qua đúng quy trình trong file này đều coi là sai quy trình, phải dừng lại
> và làm lại đúng thứ tự — dù người dùng có nhắc lại hay không.

> File này tự động nạp vào đầu MỌI phiên làm việc trong repo `ai-assistants`. Đây chính là "file
> chức năng" nhắc Claude luôn đọc bộ não & quy tắc trước khi tạo nội dung — không cần người
> dùng nhắc lại mỗi lần.

Đây chính là repo `ai-assistants` — bộ não & quy tắc thật của hệ thống nội dung **AI Hiền triết
Anh Minh** (Funamark) nằm ngay trong các thư mục con của repo này: `core-brain/` (persona, ranh
giới an toàn, kiến thức nền dùng chung), và từng thư mục Factory riêng (`seo-factory/`,
`video-factory/`, `community-factory/`, `image-factory/`, `AI- Anh- Minh- chat-factory/`,
`research-factory/`, `review-factory/`, `publish-factory/`), cùng `hook_library_full.md` (kho
hook).

**Nội dung thành phẩm KHÔNG lưu ở repo này** — xem Bước 5 bên dưới:
- Bài viết SEO → `nnphuong2016-arch/bai-viet-seo`.
- Kịch bản video → `nnphuong2016-arch/kich-ban-video`.

---

## QUY TẮC BẮT BUỘC — ĐỌC TRƯỚC KHI TẠO BẤT KỲ NỘI DUNG NÀO

Trước khi viết **bài SEO**, **kịch bản video**, **post cộng đồng**, **prompt ảnh**, hay bất kỳ
nội dung nào cho kênh này, LUÔN thực hiện theo đúng thứ tự:

### Bước 1 — Luôn đọc CORE_BRAIN trước (bắt buộc, mọi loại nội dung)

- `core-brain/instructions.md` — danh tính "Hiền triết Anh Minh", giọng nói, 5 trụ nội dung,
  ranh giới TUYỆT ĐỐI KHÔNG (không dọa bệnh, không chẩn đoán/kê đơn, không thần bí, không sến,
  không toxic motivation, không CAPS/giật gân, không tranh cãi chính trị), và checkpoint "móc
  neo ký ức" ở mục 7 (mỗi bài cần ít nhất 1 trong 3: ẩn dụ thiên nhiên mạnh / câu hỏi tự vấn /
  insight không hiển nhiên — trước khi coi là xong).
- Tra cứu thêm khi cần dẫn chứng: `core-brain/health_knowledge.md` (sức khỏe — chỉ mức lối
  sống, có bảng semantic entity Preferred/Allowed/Forbidden ở mục 9), `core-brain/
  philosophy_reference.md` (Khổng–Lão–Trang, Kinh Dịch dùng NHẸ, không bói toán), `core-brain/
  dong_hanh_nguoi_benh.md` (ranh giới cứng khi nói về bệnh/người già — KHÔNG tư vấn bệnh, luôn
  đặt song song bác sĩ), `core-brain/life_stories.md`, `core-brain/anh_minh_quotes.md` (câu
  chốt), `core-brain/seasonal_calendar.md` (lịch mùa/dịp), `core-brain/image_style_bible.md`
  (ngoại hình nhân vật — nguồn DUY NHẤT, dùng cho mọi ảnh/video có nhân vật).

### Bước 2 — LUÔN lấy hook từ `hook_library_full.md`

- File: `hook_library_full.md` (gốc repo) — kho 300 hook, chia 6 mục: (1) Sức khỏe, (2) Tâm lý &
  đời sống, (3) Dưỡng sinh, (4) Triết lý phương Đông, (5) Đồng hành tuổi già & người bệnh,
  (6) Bếp An Nhiên (giọng kể chuyện món ăn — không dùng khuôn "Vì sao/Điều gì").
- Cách dùng: nếu người dùng chỉ định "hook số N trụ X" → dùng đúng câu đó làm điểm vào. Nếu
  không chỉ định, tự chọn hook phù hợp chủ đề, ưu tiên hook CHƯA dùng gần đây (chống lặp —
  không có bộ nhớ dài hạn giữa các phiên, nên nếu người dùng nhắc "đã dùng hook nào rồi" hãy
  tôn trọng thông tin đó).
- Hook chỉ là **điểm vào**, không phải cả kịch bản/bài viết — giọng, cấu trúc, ví dụ vẫn theo
  file rules của Factory tương ứng (bước 3).
- Nếu SEO và Video cùng làm một chủ đề (chuyển đổi bài viết → video), **dùng lại đúng hook** đã
  chọn ở bài SEO gốc — không tự chọn hook khác, tránh lệch giữa bài viết và video.

### Bước 3 — Đọc đúng file Factory theo loại nội dung được yêu cầu

**Khi được yêu cầu viết BÀI SEO / bài blog web:**
1. `seo-factory/instructions_SEO.md` — vai trò & quy trình.
2. `seo-factory/keyword_strategy.md` — chọn từ khóa, intent, title, slug, meta, heading.
3. `seo-factory/article_templates.md` — chọn khuôn A–I (Explainer, Thói quen, Suy ngẫm triết,
   Đồng hành, Câu chuyện, Nhật ký, Pillar, Checklist, So sánh).
4. `seo-factory/web_content_rules.md` — làn đường thắng (lối sống, KHÔNG truy vấn y tế cạnh
   tranh), tự chuyển góc khi chạm YMYL, độ dài theo loại bài, cấu trúc AEO.
5. `seo-factory/writing_craft_examples.md` — dạy giọng bằng ví dụ: nhịp đoạn xoay vòng, giọng
   trải nghiệm người đọc, cách mở/kết bài, Information Gap tự kiểm, ranh giới ngôn ngữ theo
   từng mục (áp dụng cả 6 mục nội dung, không riêng Sức khỏe).
6. `seo-factory/seo_checklist.md` — tự kiểm TRƯỚC khi xuất, bắt buộc không bỏ qua (mục 0 Quick
   Fail: title dài, slug thừa stopword, thiếu minh bạch AI, Disclaimer lẫn References, thiếu
   ngày cập nhật — sai 1 trong 5 điều này thì dừng và sửa ngay).
7. `seo-factory/internal_link_rules.md` — gắn 2–5 internal link.
8. `seo-factory/output_schema.md` — đóng gói đúng khuôn field.

Chủ đề Sức khỏe cần tăng chiều sâu (semantic entity) → tra bảng Preferred/Allowed/Forbidden ở
`core-brain/health_knowledge.md` mục 9 trước — KHÔNG tự thêm thuật ngữ hormone/y sinh (cortisol,
melatonin...) dù nghe "chuyên sâu hơn".

**Khi được yêu cầu viết KỊCH BẢN VIDEO:**
1. `video-factory/instructions_VIDEO.md` — vai trò & quy trình (2 chế độ: chuyển đổi từ bài SEO
   có sẵn, hoặc viết độc lập từ hook).
2. `video-factory/video_rules.md` — mô hình 2 lớp LỜI/HÌNH, khuôn xuất, khung NGẮN/TRUNG/DÀI,
   quy tắc viết prompt hình, chống lặp, thumbnail ethics.
3. `video-factory/examples_and_hooks.md` — dạy giọng bằng ví dụ, các cấu trúc kể (A–E), phản
   ví dụ (KHÔNG viết như thế nào).
4. `core-brain/image_style_bible.md` — ngoại hình & hành vi nhân vật khi prompt hình có nhân vật.
5. Nếu là chuỗi món ăn "Bếp An Nhiên": thêm `video-factory/bep_an_nhien.md` +
   `video-factory/food_library.md`.
6. `video-factory/output_schema.md` — đóng gói đúng khuôn field.

**Khi được yêu cầu viết POST CỘNG ĐỒNG / social:** đọc `community-factory/` (instructions_COMMUNITY,
community_rules, social_templates, storytelling_patterns, engagement_rules, community_checklist,
output_schema).

**Khi được yêu cầu tạo PROMPT ẢNH:** đọc `image-factory/` (instructions_IMAGE, image_style_rules,
image_prompt_rules, image_templates, image_checklist, output_schema); ảnh sản phẩm dùng thêm
`product-image-factory/product_image_guide.md`.

**Khi được yêu cầu trò chuyện trực tiếp (chat/tư vấn nhanh):** đọc
`AI- Anh- Minh- chat-factory/` (đọc đúng thứ tự ghi trong `instructions_CHAT.md` mục 3 của
chính thư mục đó).

**Research / Review / Publish:** dùng khi pipeline cần — xem `research-factory/`,
`review-factory/`, `publish-factory/` tương ứng.

### Bước 4 — Tự kiểm trước khi đưa ra kết quả cuối

Luôn chạy qua đúng file `*_checklist.md` (hoặc `seo_checklist.md`/`community_checklist.md`/
`image_checklist.md`) của Factory tương ứng trước khi coi là xong — không xuất nội dung "tạm
được" rồi sửa sau.

### Bước 5 — LƯU KẾT QUẢ VÀO ĐÚNG REPO ĐẦU RA (bắt buộc, không nhầm lẫn)

Sau khi hoàn tất một bài SEO hoặc một kịch bản video (đã qua Bước 4), LUÔN lưu file kết quả vào
đúng repo output riêng — KHÔNG lưu trong repo `ai-assistants` này (repo này chỉ chứa bộ não/cấu
hình, không chứa nội dung thành phẩm):

- **Bài viết SEO** → repo `nnphuong2016-arch/bai-viet-seo`.
- **Kịch bản video** → repo `nnphuong2016-arch/kich-ban-video`.

Quy trình khi lưu:
1. Nếu repo output chưa có trong session → gọi `add_repo` (owner: `nnphuong2016-arch`, repo:
   `bai-viet-seo` hoặc `kich-ban-video`), clone, rồi `register_repo_root`.
2. Đặt tên file theo đúng quy cách ở dưới — không ghi đè file cũ trừ khi đang sửa đúng bài đó.
3. **File .md CHỈ chứa đúng nội dung bài viết (những gì hiển thị cho người đọc trên web) — KHÔNG
   thêm bất kỳ chữ/field/ghi chú nào khác**:
   - CÓ trong file: tiêu đề (H1), toàn văn thân bài (H2/H3, đoạn văn, list), FAQ hiển thị trên
     trang (Q&A thật), disclaimer + minh bạch AI + ngày cập nhật (đây là nội dung bắt buộc hiển
     thị ở chân bài theo `web_content_rules.md`, không phải ghi chú nội bộ).
   - **Khối đóng bài chuẩn (bắt buộc, CHỈ áp dụng cho bài thuộc chủ đề Sức khỏe — số 1):** đặt
     cuối file, sau FAQ, dùng đúng khuôn dưới đây — heading `### Lưu ý` tạo ranh giới rõ giữa
     đoạn kết cảm xúc của bài và phần thông tin bắt buộc, tránh gãy mạch/gây hụt hẫng cho người
     đọc. Mở đầu bằng tên nhân vật "Hiền triết Anh Minh" (không mở đầu bằng chữ "AI") — vẫn giữ
     đủ minh bạch AI ngay trong cùng câu, chỉ đổi từ đầu tiên người đọc thấy. **Các chủ đề khác
     (Tâm lý, Dưỡng sinh, Triết lý, Đồng hành, Bếp An Nhiên) KHÔNG dùng khối này** — khớp đúng
     `web_content_rules.md` mục 2 (disclaimer y khoa chỉ bắt buộc cho bài chạm sức khỏe) và
     `article_templates.md` (Mẫu C triết lý không cần disclaimer y khoa, Mẫu D đồng hành có
     khối kết riêng theo `dong_hanh_nguoi_benh.md`). Nếu một bài ở chủ đề khác có chạm nhẹ tới
     sức khỏe, cân nhắc theo đúng tinh thần "chỉ cần khi bài thật sự nói về sức khỏe", không áp
     máy móc.

     ```
     ### Lưu ý

     Hiền triết Anh Minh là nhân vật nội dung AI của Funamark, chia sẻ các góc nhìn về lối sống
     ở mức phổ thông. Nội dung không thay thế tư vấn, chẩn đoán hoặc điều trị y khoa. Nếu triệu
     chứng kéo dài hoặc ảnh hưởng đến sinh hoạt hằng ngày, hãy trao đổi với bác sĩ hoặc chuyên
     gia phù hợp.

     **Cập nhật lần cuối:** <ngày cập nhật thật của bài, không copy cố định>
     ```
   - KHÔNG cho vào file: Slug, Meta Description, Excerpt, Category, Tags, Featured Image
     (mô tả prompt ảnh), tên Hook đã dùng, Loại bài, ghi chú kiểu "References để trống vì...",
     "chưa có internal link vì...". Những thứ này là metadata cho pipeline, không phải nội dung
     đọc được — chuyển sang lưu ở Google Sheet (xem Bước 6) hoặc trong commit message (lý do
     quyết định), không nằm trong file.
   - Field nào không có nội dung thật (VD: chưa có nguồn để trích dẫn) → **không đưa vào file**,
     không viết placeholder giải thích.
4. Commit + push (hỏi người dùng trước nếu ngữ cảnh chưa rõ có nên tự push luôn không, trừ khi
   người dùng đã xác nhận sẵn "luôn tự lưu, không cần hỏi lại" trong phiên).

**Quy cách đặt tên file (bắt buộc, áp dụng cả `bai-viet-seo` và `kich-ban-video`):**

`<số chủ đề>.<số thứ tự bài trong chủ đề đó>.<slug>.md`

Số chủ đề đánh theo đúng thứ tự 6 mục của `hook_library_full.md` (không tự đổi số):

| Số | Chủ đề |
|---|---|
| 1 | Sức khỏe |
| 2 | Tâm lý & đời sống |
| 3 | Dưỡng sinh |
| 4 | Triết lý phương Đông |
| 5 | Đồng hành tuổi già & người bệnh |
| 6 | Bếp An Nhiên |

Ví dụ: bài SEO đầu tiên thuộc chủ đề Sức khỏe → `1.1.<slug>.md`. Bài Sức khỏe tiếp theo →
`1.2.<slug>.md`. Bài đầu tiên thuộc Tâm lý & đời sống → `2.1.<slug>.md`.

**Cách xác định số thứ tự:** trước khi tạo file mới, liệt kê các file đã có trong repo output
đó bắt đầu bằng đúng `<số chủ đề>.` (VD: liệt kê file bắt đầu `1.` để biết đã có bài Sức khỏe
nào), lấy số thứ tự lớn nhất + 1. Nếu chưa có file nào của chủ đề đó → bắt đầu từ `1`. `bai-viet-seo`
và `kich-ban-video` đếm **độc lập nhau** (số thứ tự trong hai repo không cần khớp nhau, kể cả khi
video được chuyển thể từ đúng bài SEO đó).

Hai repo output này KHÔNG chứa bộ não/quy tắc — chỉ chứa thành phẩm cuối cùng. Không tự thêm
CLAUDE.md hay file cấu hình vào hai repo đó.

### Bước 5.5 — TẠO PROMPT ẢNH MINH HỌA ĐI KÈM (bắt buộc, ngay sau khi lưu bài SEO — quyết định
18/07/2026)

Ngay sau khi một bài SEO đã lưu xong (Bước 5), luôn tạo kèm **1 prompt ảnh minh họa** cho đúng
bài đó — không phải việc riêng phải đợi người dùng nhắc:

1. Đọc `image-factory/image_prompt_rules.md` (cấu trúc 8 phần Scene→Subject→Composition→
   Lighting→Color→Mood→Camera→Negative Prompt), `image-factory/image_style_rules.md` (tone màu
   Beige/Cream/Warm Green/Walnut/Gold, ánh sáng tự nhiên, không nhân vật trừ khi bài cần),
   `image-factory/image_templates.md` (mặc định dùng **Mẫu E — Blog Cover/OG**, 1.91:1, trừ khi
   người dùng chỉ định mẫu khác), và `core-brain/image_style_bible.md` nếu ảnh có nhân vật chính.
2. Ưu tiên ảnh tĩnh vật/khung cảnh đời thường (không có nhân vật) khi bài không cần nhân vật
   chính xuất hiện — tránh phải khớp ngoại hình mỗi lần, vẫn đủ ẩn dụ khớp nội dung bài.
3. **KHÔNG** cho prompt ảnh vào file `.md` của bài viết (giữ đúng quy tắc pure-content ở Bước 5).
   Thay vào đó, ghi vào **1 file Excel chạy dọc duy nhất** (không tạo file rời cho từng bài, không
   kiểm soát được khi số bài tăng — quyết định 18/07/2026):
   - Vị trí: `bai-viet-seo/_prompt-anh/prompt-anh.xlsx` (cho ảnh bài SEO). Nếu sau này cần prompt
     ảnh riêng cho video/kịch bản, tạo tương tự ở `kich-ban-video/_prompt-anh/prompt-anh.xlsx`
     (không gộp chung 2 file, vì 2 repo đếm số thứ tự độc lập nhau).
   - Mỗi bài = 1 dòng mới, cột theo đúng thứ tự `image-factory/output_schema.md` (Template, Usage,
     Prompt, Negative Prompt, Aspect Ratio, Size, Filename, Alt Text, Caption), cộng thêm cột định
     danh ở đầu: STT, Bài viết (tên file), Link bài SEO (raw GitHub link).
   - Không ghi đè các dòng cũ — chỉ thêm dòng mới ở cuối.
4. Commit + push file Excel đã cập nhật vào đúng repo output (cùng lúc hoặc ngay sau khi push bài
   viết), rồi gửi file đã cập nhật cho người dùng (không chỉ báo đã làm xong mà không đưa file).
5. File Excel này nằm trong repo chỉ để lưu bền qua các phiên làm việc (môi trường chạy có thể bị
   dọn sạch giữa các phiên) — không phải nội dung xuất bản, không vi phạm quy tắc "repo output chỉ
   chứa thành phẩm cuối cùng" vì đây là file phụ trợ pipeline riêng, đặt trong thư mục con
   `_prompt-anh/` tách biệt rõ khỏi các file `.md` bài viết.

### Bước 6 — DÁN LINK VÀO GOOGLE SHEET ĐẦU VÀO CHO N8N (bắt buộc, sau khi đã push file)

Sheet: `https://docs.google.com/spreadsheets/d/145dk7FIIzMphDeaZJa9KCyp_Hq4c2YkmNO0h37SIFUk/edit?gid=0#gid=0`
(tên "Anh Minh hook list") — đây là bảng n8n đọc để tự động đăng bài lên web.

**Cấu trúc Sheet thật (xác nhận 12/07/2026, không đoán nữa):**

| Cột | Nội dung |
|---|---|
| A | `stt` |
| B | `Tên chủ đề` — mỗi dòng là **đúng một hook**, số + câu y hệt `hook_library_full.md` (có
  dòng tiêu đề mục lớn xen giữa, kiểu `## 1. SỨC KHỎE — HIỂU CƠ THỂ`, không phải hook, bỏ qua) |
| C | `link bài viết seo` |
| D | `link ảnh cho bài viết seo` |
| E | `link video tạo ra từ bài viết seo` |
| F | `Trạng thái` |

**Quan trọng:** dòng khớp theo **đúng số hook + câu hook đã dùng** (cột B), KHÔNG phải theo tên
bài SEO/tiêu đề bài viết — vì cột B là hook gốc, còn tiêu đề bài do Factory viết ra có thể diễn
đạt khác câu hook. Luôn đối chiếu lại đúng hook đã dùng ở Bước 2 để tìm đúng dòng.

**Cách truy cập Sheet:** cần connector Google có quyền ghi (Sheets) đã bật trong phiên. Tính đến
12/07/2026: chỉ có connector Google Drive (đọc, không ghi được ô) hoạt động; connector Custom
"google sheet - Anh Minh hook list" bị lỗi cấu hình OAuth (Authorization URL sai, trả 404) —
CHƯA dùng được để tự ghi. Cho tới khi có connector ghi được:
1. Xác định đúng dòng theo hook (cột B) đã dùng cho bài/kịch bản vừa xong.
2. Đưa cho người dùng: **số dòng/hook** + **link raw GitHub** tương ứng đúng cột (C = bài SEO,
   D = ảnh, E = video) — để người dùng tự dán, không tự đoán rồi báo "đã dán" khi chưa thật sự
   ghi được.
3. Nếu sau này có connector ghi Sheet hoạt động, chuyển sang tự làm bước dán, không cần hỏi lại.

Metadata còn lại mà pipeline cần (Slug, Meta Description, Category, Tags, Featured Image mô tả...)
— vì không còn nằm trong file .md (xem Bước 5) — Sheet này hiện CHƯA có cột riêng cho các
metadata đó (chỉ có 3 cột link + Trạng thái). Nếu cần lưu, hỏi lại người dùng nên thêm cột nào,
không tự ý thêm cột mới vào Sheet.

---

## RANH GIỚI TUYỆT ĐỐI (nhắc lại — không bao giờ được vi phạm dù ở Factory nào)

Không dọa bệnh/giật gân/CAPS LOCK · không chẩn đoán/kê đơn/thay bác sĩ · không thần bí/mê tín/
bói toán (tử vi, phong thủy, Kinh Dịch chỉ dùng NHẸ làm ẩn dụ) · không thao túng cảm xúc/toxic
motivation · không sến/giả đạo lý · không tranh cãi chính trị · sản phẩm chỉ ~5% nội dung, giá
trị luôn ~95%.

Mảng **đồng hành tuổi già & người bệnh**: theo đúng `core-brain/dong_hanh_nguoi_benh.md` —
TUYỆT ĐỐI không tư vấn bệnh, không hứa hẹn khỏi bệnh, không đụng diễn tiến bệnh, luôn đặt song
song với bác sĩ.

---

## GHI CHÚ VẬN HÀNH

- Mỗi Factory chỉ làm đúng phạm vi của nó (xem mục 2 "CHỈ LÀM / KHÔNG LÀM" trong từng
  `instructions_<TÊN>.md`). Nếu người dùng yêu cầu việc thuộc Factory khác trong lúc đang làm
  một Factory, nói rõ việc đó thuộc Factory khác thay vì tự làm lệch phạm vi — trừ khi người
  dùng rõ ràng muốn một trợ lý tổng hợp làm hết (trường hợp phiên làm việc này, vì đang thao
  tác qua Claude Code chứ không phải nhiều Custom GPT tách biệt, có thể linh hoạt làm nối tiếp
  nhiều Factory trong một yêu cầu, miễn giữ đúng thứ tự & file rules của từng Factory).
- Không tự bịa kiến thức sức khỏe/triết học — luôn tra file knowledge base của CORE_BRAIN trước.
- Anh Minh là **nhân vật AI**, không phải người thật — không viết như thể nhân vật có trải
  nghiệm y khoa/cá nhân thật.
- File này (`CLAUDE.md`) nằm ngay trong `ai-assistants` — khi repo này được cập nhật (thêm/sửa
  file bộ não), lần sau chỉ cần đọc lại từ đầu (không cần hỏi lại người dùng), vì đây là nguồn
  gốc duy nhất (single source of truth) cho toàn bộ persona & quy tắc.
