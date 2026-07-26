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
`video-factory/`, `community-factory/` (Zalo/Newsletter/bình luận, KHÔNG còn viết Facebook),
`facebook-factory/` (chuyên riêng bài đăng Facebook — tách khỏi Community Factory từ
20/07/2026; **3 nguồn ý tưởng**, ưu tiên từ trên xuống: chủ đề người vận hành đưa trực tiếp →
`bai-dang-Facebook-Anh-Minh.md` → tự sinh qua `idea_library.md` — xem Bước 2), `image-factory/`, `featured-Image-factory/` (chuyên riêng ảnh
đại diện đầu bài viết — tách khỏi `image-factory/` từ 14/07/2026, độc lập, không gắn với Image
Factory hay bất kỳ Factory nào khác), `ai-anh-minh-chat-factory/`, `research-factory/`,
`review-factory/`, `publish-factory/`), cùng 3 file backlog chủ đề riêng cho từng kênh (thay
cho `hook_library_full.md` cũ — xem Bước 2): `bai-seo-dang-website-Anh-Minh.md`,
`bai-dang-Facebook-Anh-Minh.md`, `bai-video-dang-Youtube-Anh-Minh.md`.

**Nội dung thành phẩm KHÔNG lưu ở repo này** — xem Bước 5 bên dưới. **Từ 21/07/2026, KHÔNG còn
dùng GitHub cho bất kỳ loại thành phẩm nào — tất cả lưu thẳng Google Drive:**
- Bài viết SEO → **chỉ lưu Google Drive** (quyết định 21/07/2026 — ngừng dùng repo
  `nnphuong2016-arch/bai-viet-seo`) — thư mục "Anh Minh - N8N Trigger" → "Bai-viet-SEO".
  Không cần manifest JSON riêng (xem Bước 5.A + Bước 6).
- Kịch bản video → **chỉ lưu trực tiếp Google Drive, KHÔNG dùng GitHub nữa** (quyết định
  18/07/2026 — đã ngừng dùng repo `kich-ban-video`) — thư mục "Anh Minh - N8N Trigger" →
  "Kich-ban-video". Không cần thêm manifest JSON riêng cho video (xem Bước 5.B + Bước 6).
- Prompt Featured Image → Google Drive, "Anh Minh - N8N Trigger" → "Prompt-Featured-Image"
  (xem Bước 5.5).
- Bài đăng Facebook → Google Drive riêng (không GitHub) — xem Bước 5F.

---

## QUY TẮC BẮT BUỘC — ĐỌC TRƯỚC KHI TẠO BẤT KỲ NỘI DUNG NÀO

Trước khi viết **bài SEO**, **kịch bản video**, **post cộng đồng**, **prompt ảnh**, hay bất kỳ
nội dung nào cho kênh này, LUÔN thực hiện theo đúng thứ tự:

### Bước 1 — Luôn đọc CORE_BRAIN trước (bắt buộc, mọi loại nội dung)

> **Ngoại lệ đã xác nhận đúng, giữ nguyên:** Chat Factory (`ai-anh-minh-chat-factory/`) và
> Featured Image Factory (`featured-Image-factory/`) KHÔNG dán `core-brain/instructions.md` vào
> ô Instructions — mỗi factory có lý do riêng đã ghi trong `instructions_CHAT.md` và
> `instructions_FEATURED_IMAGE.md` của chính nó. Đây là ngoại lệ có chủ đích, không phải thiếu sót.

- `core-brain/instructions.md` — danh tính "Hiền triết Anh Minh", giọng nói, 6 trụ nội dung,
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

### Bước 2 — LUÔN lấy hook/chủ đề từ đúng file backlog riêng của kênh đang làm (KHÔNG dùng chung
một kho nữa)

> **Cập nhật 20/07/2026:** `hook_library_full.md` (kho hook dùng chung 5 trụ) **không còn dùng**.
> Lý do đổi: kho dùng chung khiến nhiều kênh dễ khai thác đúng một câu hook theo cùng cách diễn
> đạt, dẫn tới nội dung na ná nhau giữa Web/Facebook/YouTube. Thay vào đó, **mỗi kênh có một file
> backlog chủ đề riêng, KHÔNG dùng chéo sang factory khác**:

| Factory | File backlog nguồn hook/chủ đề | Vị trí |
|---|---|---|
| SEO Factory (Web) | `bai-seo-dang-website-Anh-Minh.md` | gốc repo `ai-assistants/` |
| Video Factory (nhánh Giải Đáp — YouTube) | `bai-video-dang-Youtube-Anh-Minh.md` **+ nguồn ngoài** (Google Drive/Google Sheet khi có) | gốc repo `ai-assistants/` + Drive/Sheet |
| Facebook Factory | **3 nguồn xếp hạng** (cập nhật 25/07/2026, nguồn gốc: `facebook-factory/execution_flow.md` STEP 3): (1) **chủ đề người vận hành đưa trực tiếp — ưu tiên cao nhất**, khi có thì bỏ qua (2) và đi thẳng sang STEP 3.5; (2) `bai-dang-Facebook-Anh-Minh.md` (kho 210 hook có sẵn, 7 series), ưu tiên hook chưa dùng gần đây; (3) tự sinh qua `facebook-factory/idea_library.md` (Pattern + Emotion + Observation + Contradiction) khi hai nguồn trên không đủ hoặc cần thêm hướng cho cùng một chủ đề. | người vận hành + gốc repo `ai-assistants/` + `facebook-factory/idea_library.md` |

- Cách dùng: nếu người dùng chỉ định "hook/dòng số N" → dùng đúng câu đó trong đúng file backlog
  của Factory đang làm làm điểm vào. Nếu không chỉ định, tự chọn dòng phù hợp chủ đề trong đúng
  file đó, ưu tiên dòng CHƯA dùng gần đây (chống lặp — không có bộ nhớ dài hạn giữa các phiên,
  nên nếu người dùng nhắc "đã dùng dòng nào rồi" hãy tôn trọng thông tin đó).
- Hook/chủ đề gốc chỉ là **điểm vào**, không phải cả kịch bản/bài viết — giọng, cấu trúc, ví dụ
  vẫn theo file rules của Factory tương ứng (bước 3). Đặc biệt: **không copy nguyên một dòng
  trong file backlog để làm thẳng title/caption/lời thoại** — luôn viết lại theo đúng vai trò
  kênh (xem `core-brain/channel_roles.md`).
- Nếu SEO và Video cùng làm một chủ đề (chuyển đổi bài viết → video), Video Factory **không tự
  tra lại `bai-video-dang-Youtube-Anh-Minh.md`** cho chủ đề đó — dùng lại đúng góc/hook đã chọn
  ở bài SEO gốc, tránh lệch giữa bài viết và video.
- Video Factory là factory DUY NHẤT còn nhận hook từ **nguồn ngoài file backlog** (Google Drive/
  Google Sheet) khi vận hành tự động — vì nhánh Giải Đáp cần đồng bộ với hook đã chọn ở bài SEO
  (xem trên), và nhánh Dưỡng Sinh Ngắn dùng `video-factory/bai_tap_library.md` làm nguồn riêng,
  không phải file backlog nào ở trên.
- `hook_library_full.md`: **đã bị xoá hẳn khỏi repo** (rà soát 25/07/2026 — cả 2 thư mục
  `assets/` và `project-memory/` từng chứa file này đều không còn tồn tại). Ghi chú cũ ở đây nói
  "giữ lại để tham khảo lịch sử, KHÔNG xoá" nay không còn đúng thực tế. Không Factory nào đọc
  file này nữa, nên việc mất file không ảnh hưởng vận hành — chỉ cần biết để đừng đi tìm. Nếu
  cần xem lại nội dung cũ, lấy từ lịch sử git.

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
6. `seo-factory/article_examples_full.md` — 3 bài mẫu VIẾT TRỌN VẸN (Mẫu A/C/E), đối chiếu khi
   thấy bài đang viết còn mỏng hoặc lệch khuôn. Đọc TRƯỚC checklist — bài mẫu để viết, checklist
   để kiểm; thứ tự này khớp `seo-factory/instructions_SEO.md` mục 3.
7. `seo-factory/seo_checklist.md` — tự kiểm TRƯỚC khi xuất, bắt buộc không bỏ qua (mục 0 Quick
   Fail: title dài, slug thừa stopword, thiếu minh bạch AI, Disclaimer lẫn References, thiếu
   ngày cập nhật, Body còn ký tự định dạng — sai 1 trong 6 điều này thì dừng và sửa ngay).
8. `seo-factory/internal_link_rules.md` — gắn 2–5 internal link (ghi ở field `Internal Links`,
   không nhúng markdown vào Body — mục 4 của file đó).
9. `core-brain/channel_roles.md` — vai trò Website so với Facebook/YouTube, tránh viết trùng vai
   trò kênh khi cùng một chủ đề gốc.
10. `seo-factory/output_schema.md` — đóng gói đúng khuôn field.

Chủ đề Sức khỏe cần tăng chiều sâu (semantic entity) → tra bảng Preferred/Allowed/Forbidden ở
`core-brain/health_knowledge.md` mục 9 trước — KHÔNG tự thêm thuật ngữ hormone/y sinh (cortisol,
melatonin...) dù nghe "chuyên sâu hơn".

**Khi được yêu cầu viết KỊCH BẢN VIDEO:** đọc đúng theo thứ tự trong `video-factory/
instructions_VIDEO.md` mục 3 (nguồn danh sách file đầy đủ, cập nhật 23/07/2026 — không lặp lại
danh sách ở đây để tránh 2 nơi cùng liệt kê rồi lệch nhau khi thêm file mới): `instructions_VIDEO.md`
→ `video_rules.md` → `examples_and_hooks.md` → `core-brain/image_style_bible.md` →
`video_ai_prompt_rules.md` + `model_selection_rules.md` (luôn đọc cùng nhau) → `bep_an_nhien.md`
+ `food_library.md` (chỉ khi làm chuỗi "Bếp An Nhiên") → `duong_sinh_bai_tap.md` +
`bai_tap_library.md` (chỉ khi làm Nhánh B — Dưỡng Sinh Ngắn) → `core-brain/channel_roles.md` →
`output_schema.md` → `video_ai_contract.md` (chỉ khi đụng tới pipeline n8n/khuôn field, không
cần khi viết kịch bản thủ công).

**Khi được yêu cầu viết BÀI ĐĂNG FACEBOOK (Page/Group):** đọc đúng theo thứ tự ghi ở **khối
trích dẫn đầu** `facebook-factory/instructions_facebook.md` — 13 file, trong đó có
`bai-dang-Facebook-Anh-Minh.md` (kho 210 hook, nằm ở gốc repo chứ không trong thư mục Factory).
Đó là nguồn danh sách duy nhất; **không lặp lại danh sách ở đây** để tránh 2 nơi cùng liệt kê rồi
lệch nhau khi thêm file mới — cùng cách làm với khối KỊCH BẢN VIDEO ở trên. Khi làm việc bằng
Claude Code thì đọc thêm `facebook-factory/CLAUDE.md` (file này dành riêng cho Claude Code, không
thuộc khu Files của Custom GPT nên không nằm trong 13 file trên). Factory riêng, tách khỏi
Community Factory từ 20/07/2026.

**Khi được yêu cầu viết post Zalo/Newsletter hoặc trả lời bình luận:** đọc `community-factory/`
(instructions_COMMUNITY, community_rules, social_templates, storytelling_patterns,
engagement_rules, community_checklist, output_schema). Community Factory KHÔNG còn viết bài
Facebook nữa.

**Khi được yêu cầu tạo PROMPT ẢNH:**
- **Ảnh đại diện đầu bài viết (Featured Image)** → đọc `featured-Image-factory/`
  (`instructions_FEATURED_IMAGE.md` → `input_schema.md` → `featured_image_editorial_rules.md`
  → `featured_image_style_rules.md` → `featured_image_prompt_rules.md` →
  `featured_image_checklist.md` → `output_schema.md`). Đây là Factory riêng cho đúng việc này —
  xem Bước 5.5.
- **Mọi loại ảnh khác** (thumbnail YouTube, hero banner, quote image, avatar, ảnh chèn giữa
  bài, v.v. — KHÔNG bao gồm Featured Image) → đọc `image-factory/` (instructions_IMAGE,
  image_style_rules, image_prompt_rules, image_templates, image_checklist, output_schema); ảnh
  sản phẩm dùng thêm `product-image-factory/product_image_guide.md`.

**Khi được yêu cầu trò chuyện trực tiếp (chat/tư vấn nhanh):** đọc
`ai-anh-minh-chat-factory/` (đọc đúng thứ tự ghi trong `instructions_CHAT.md` mục 3 của
chính thư mục đó).

**Research / Review / Publish:** dùng khi pipeline cần — xem `research-factory/`,
`review-factory/`, `publish-factory/` tương ứng.

### Bước 4 — Tự kiểm trước khi đưa ra kết quả cuối

Luôn chạy qua đúng file `*_checklist.md` (hoặc `seo_checklist.md`/`community_checklist.md`/
`image_checklist.md`) của Factory tương ứng trước khi coi là xong — không xuất nội dung "tạm
được" rồi sửa sau.

### Bước 5 — LƯU KẾT QUẢ VÀO ĐÚNG NƠI OUTPUT (bắt buộc, không nhầm lẫn)

Sau khi hoàn tất một bài SEO hoặc một kịch bản video (đã qua Bước 4), LUÔN lưu file kết quả vào
đúng nơi output — KHÔNG lưu trong repo `ai-assistants` này (repo này chỉ chứa bộ não/cấu hình,
không chứa nội dung thành phẩm). **Bài SEO và kịch bản video lưu ở HAI NƠI KHÁC NHAU** (5.A/5.B)
— quyết định 18/07/2026: kịch bản video chuyển hẳn sang Google Drive, ngừng dùng GitHub.

#### 5.A — Bài viết SEO (Google Drive — KHÔNG dùng GitHub, đổi 21/07/2026)

**Nơi lưu:** Google Drive, thư mục "Anh Minh - N8N Trigger" → **"Bai-viet-SEO"** (parentId
`1ubrFWlDezfMX91zoV7hqjc1PqnGNZ3Gn`, dùng công cụ Drive `create_file`). Đây chính là thư mục
n8n theo dõi bằng Drive Trigger, nên file bài thật nằm sẵn ở đó là đủ để kích hoạt workflow —
KHÔNG cần tạo thêm manifest JSON (cùng lý do đã áp dụng cho video từ 18/07/2026, xem Bước 6).

Quy trình khi lưu:
1. Đặt tên file theo đúng quy cách ở dưới — không ghi đè file cũ trừ khi đang sửa đúng bài đó.
2. **File CHỈ chứa đúng nội dung bài viết (những gì hiển thị cho người đọc trên web) — KHÔNG
   thêm bất kỳ chữ/field/ghi chú nào khác**:
   - CÓ trong file: tiêu đề bài, toàn văn thân bài, FAQ hiển thị trên trang (Q&A thật),
     disclaimer + minh bạch AI + ngày cập nhật (đây là nội dung bắt buộc hiển thị ở chân bài
     theo `web_content_rules.md`, không phải ghi chú nội bộ).
   - **Viết thuần chữ 100%** theo `web_content_rules.md` mục 3D: KHÔNG `#`, `-`, `—`, `*`,
     bảng, link markdown — vì pipeline giọng đọc sẽ đọc thành lời mọi ký tự còn sót. Tiêu đề
     mục viết thành một dòng chữ riêng; n8n/CMS tự bọc thẻ `<h2>` khi đăng web.
   - **Hai thứ khác nhau, đừng gộp làm một:** *minh bạch AI* (người đọc phải biết đây là nhân
     vật AI) và *miễn trừ y khoa* (nội dung không thay tư vấn bác sĩ). Trước đây cả hai nằm chung
     một khối chỉ dùng cho Sức khỏe, khiến bài Tâm lý kẹt: `seo_checklist.md` mục 0 bắt buộc dòng
     minh bạch AI cho bài "chạm sức khỏe/tâm lý", mà khối chứa dòng đó lại không áp cho Tâm lý.
     Tách ra như sau:

     | Chủ đề | Minh bạch AI | Miễn trừ y khoa |
     |---|---|---|
     | Sức khỏe (1) | Có | Có — dùng khối đầy đủ dưới đây |
     | Tâm lý & đời sống (2) | **Có** — dùng khối rút gọn ở cuối mục này | Không |
     | Dưỡng sinh, Triết lý, Đồng hành, Bếp An Nhiên | Không bắt buộc | Không |

     (Mẫu D — Đồng hành — có khối kết riêng theo `dong_hanh_nguoi_benh.md`, giữ nguyên.)

   - **Khối đóng bài chuẩn (bắt buộc, CHỈ áp dụng cho bài thuộc chủ đề Sức khỏe — số 1):** đặt
     cuối file, sau FAQ, dùng đúng khuôn dưới đây — dòng tiêu đề "Lưu ý" (viết trơn, KHÔNG có
     `###` đứng trước, theo mục 3D) tạo ranh giới rõ giữa đoạn kết cảm xúc của bài và phần thông
     tin bắt buộc, tránh gãy mạch/gây hụt hẫng cho người
     đọc. Mở đầu bằng tên nhân vật "Hiền triết Anh Minh" (không mở đầu bằng chữ "AI") — vẫn giữ
     đủ minh bạch AI ngay trong cùng câu, chỉ đổi từ đầu tiên người đọc thấy. **Các chủ đề khác
     (Dưỡng sinh, Triết lý, Đồng hành, Bếp An Nhiên) KHÔNG dùng khối này; **Tâm lý dùng khối
     rút gọn** ghi ở cuối mục — khớp đúng
     `web_content_rules.md` mục 2 (disclaimer y khoa chỉ bắt buộc cho bài chạm sức khỏe) và
     `article_templates.md` (Mẫu C triết lý không cần disclaimer y khoa, Mẫu D đồng hành có
     khối kết riêng theo `dong_hanh_nguoi_benh.md`). Nếu một bài ở chủ đề khác có chạm nhẹ tới
     sức khỏe, cân nhắc theo đúng tinh thần "chỉ cần khi bài thật sự nói về sức khỏe", không áp
     máy móc.

     ```
     Lưu ý

     Hiền triết Anh Minh là nhân vật nội dung AI của Funamark, chia sẻ các góc nhìn về lối sống
     ở mức phổ thông. Nội dung không thay thế tư vấn, chẩn đoán hoặc điều trị y khoa. Nếu triệu
     chứng kéo dài hoặc ảnh hưởng đến sinh hoạt hằng ngày, hãy trao đổi với bác sĩ hoặc chuyên
     gia phù hợp.

     Cập nhật lần cuối: <ngày cập nhật thật của bài, không copy cố định>
     ```
   - KHÔNG cho vào file: Title thẻ SEO, Slug, Meta Description, Excerpt, Category, Tags,
     Featured Image, Internal Links, References, tên Hook đã dùng, Loại bài, ghi chú kiểu
     "References để trống vì...", "chưa có internal link vì...". Những thứ này là metadata cho
     pipeline, không phải nội dung đọc được — chúng đi vào **file manifest metadata** kèm theo
     (bước 3 dưới đây), KHÔNG nằm trong file bài và KHÔNG chỉ nằm trong cuộc trò chuyện.
   - Field nào không có nội dung thật (VD: chưa có nguồn để trích dẫn) → **không đưa vào file**,
     không viết placeholder giải thích.
3. `create_file` lên đúng thư mục Drive ở trên rồi gửi link file cho người dùng. Không có bước
   commit/push (không còn GitHub cho bài SEO). Hỏi người dùng trước nếu ngữ cảnh chưa rõ có nên
   tự lưu luôn không, trừ khi đã xác nhận sẵn "luôn tự lưu, không cần hỏi lại" trong phiên.
4. **Tạo thêm 1 file manifest metadata** cùng thư mục, tên `<tên file bài>.meta.json`. Đây là
   nơi duy nhất 8 field metadata tồn tại — file bài chỉ chứa chữ đọc được, còn cuộc trò chuyện
   thì mất khi đóng phiên. Manifest **KHÔNG lặp lại Body** (đó là lý do manifest cũ bị bỏ):

   ```json
   {
     "file": "1.5.co-the-can-nhung-khoang-yen-tinh",
     "title_seo": "Tiêu đề thẻ SEO ≤ 60 ký tự",
     "slug": "co-the-can-nhung-khoang-yen-tinh",
     "meta_description": "…",
     "excerpt": "…",
     "category": "Sức khỏe",
     "tags": ["…", "…"],
     "internal_links": [
       { "anchor": "cụm chữ có sẵn trong bài", "slug": "bai-dich-noi-bo" },
       { "anchor": "cụm chữ khác", "url": "https://youtube.com/watch?v=…" }
     ],
     "references": [],
     "hook_used": "…",
     "article_template": "Mẫu A"
   }
   ```

   Field nào thật sự không có nội dung → để mảng rỗng hoặc chuỗi rỗng, KHÔNG bịa.

**Quy cách đặt tên file bài SEO:** `<số chủ đề>.<số thứ tự bài trong chủ đề đó>.<slug>`

Số chủ đề đánh theo đúng thứ tự 6 trụ/mục nội dung chuẩn của hệ thống (theo `core-brain/
instructions.md` mục 6 + mục Bếp An Nhiên — không tự đổi số, không còn phụ thuộc
`hook_library_full.md` đã ngưng dùng):

| Số | Chủ đề |
|---|---|
| 1 | Sức khỏe |
| 2 | Tâm lý & đời sống |
| 3 | Dưỡng sinh |
| 4 | Triết lý phương Đông |
| 5 | Đồng hành tuổi già & người bệnh |
| 6 | Bếp An Nhiên |

Ví dụ: bài SEO đầu tiên thuộc chủ đề Sức khỏe → `1.1.<slug>`. Bài Sức khỏe tiếp theo →
`1.2.<slug>`. Bài đầu tiên thuộc Tâm lý & đời sống → `2.1.<slug>`.

**Cách xác định số thứ tự:** trước khi tạo file mới, liệt kê các file đã có trong thư mục Drive
"Bai-viet-SEO" bắt đầu bằng đúng `<số chủ đề>.` (VD: liệt kê file bắt đầu `1.` để biết đã có bài
Sức khỏe nào), lấy số thứ tự lớn nhất + 1. Nếu chưa có file nào của chủ đề đó → bắt đầu từ `1`.

> ⚠️ **KHÔNG nhầm với số dòng trong file backlog** (làm rõ 21/07/2026). Backlog
> `bai-seo-dang-website-Anh-Minh.md` cũng đánh số dạng `<số chủ đề>.<số>` (VD `1.26. Có một loại
> mệt mà ngủ đủ tám tiếng vẫn không tan.`) — đó là **vị trí của chủ đề trong backlog**, KHÁC hẳn
> số thứ tự bài đã viết. Hai hệ số trùng dạng nhưng khác nghĩa:
> - **Tên file** dùng số thứ tự bài đã viết trong chủ đề đó (đếm trong thư mục Drive).
> - Khi cần ghi lại chủ đề gốc đã dùng, ghi **nguyên câu hook** kèm số dòng backlog trong phần
>   trả lời cho người dùng — không đưa vào tên file, không đưa vào nội dung bài.
>
> VD thực tế: bài `1.1.vi-sao-ngu-du-tam-tieng-van-met` là bài Sức khỏe **thứ nhất đã viết**,
> lấy chủ đề từ **dòng 1.26** của backlog. Hai số này không cần khớp nhau.

#### 5.B — Kịch bản video (Google Drive — KHÔNG dùng GitHub)

- **MỖI VIDEO SINH RA 2 FILE `.md`, KHÔNG PHẢI 1** (chuẩn hoá 25/07/2026 theo mô hình kênh
  My Dog & My Love — xem `video-factory/output_schema.md` mục "File prompt đi kèm"):
  1. `..._master_script.md` — kịch bản: cảnh, lời dẫn, Visual/Camera trung tính. **Không** chứa
     prompt của bất kỳ công cụ AI nào.
  2. `..._prompts.md` — prompt thật để generate, viết **SAU** khi Master Script xong. Đánh dấu rõ
     cảnh nào là Clip (`🎬 CLIP 1/3`), cảnh nào là Ảnh giữ; cuối file có dòng tự kiểm ngân sách
     (đếm Clip và Ảnh giữ, đối chiếu trần ở `model_selection_rules.md` mục 1B).

  Chưa tạo đủ 2 file thì **chưa coi là xong**. Tách 2 file để khi đổi/thêm công cụ AI chỉ phải
  viết lại file prompt, giữ nguyên kịch bản.
- **Nơi lưu:** Google Drive, thư mục "Anh Minh - N8N Trigger" → "Kich-ban-video" (parentId
  `1aqbgUNiaPJ5KKQEC3QZqAn23j7oTrr4F`, dùng công cụ Drive `create_file`) — lưu **cả hai file** vào
  đây. File Master Script chứa **toàn văn** kịch bản — n8n đọc/parse trực tiếp file này (xem
  `video-factory/video_ai_contract.md`),
  KHÔNG cần repo GitHub `kich-ban-video` (đã ngừng dùng) và KHÔNG cần thêm manifest JSON riêng
  (nội dung thật đã nằm sẵn trong chính file `.md` này — xem thêm ghi chú ở Bước 6).
- **Tên file:** `<số chủ đề>.<STT>. <Tên video>_master_script.md` — số chủ đề theo đúng bảng ở
  mục 5.A; STT xác định bằng cách liệt kê file đã có cùng `<số chủ đề>.` trong thư mục Drive
  "Kich-ban-video" (đếm ĐỘC LẬP với thư mục "Bai-viet-SEO", kể cả khi video chuyển thể từ đúng bài SEO
  đó). `<Tên video>` giữ nguyên tên tiếng Việt, có dấu cách/viết hoa như bình thường — KHÔNG rút
  gọn thành slug; bỏ các ký tự không an toàn cho tên file khi tải về máy (Windows):
  `\ / : * ? " < > |` (VD dấu `?` cuối câu hỏi thì bỏ hẳn).
  VD: `1.1. Vì sao ngủ đủ tám tiếng mà vẫn thấy mệt_master_script.md`.
  File prompt dùng **đúng tên đó**, chỉ đổi đuôi `_master_script.md` → `_prompts.md`
  (VD: `1.1. Vì sao ngủ đủ tám tiếng mà vẫn thấy mệt_prompts.md`).
- **Nội dung & khuôn field:** viết đúng theo `video-factory/video_rules.md` mục 1.C (Scene ID
  zero-padded, Duration, Voice, Visual, Camera, Character, Emotion, Loop) và đóng gói theo
  `video-factory/output_schema.md`.
- **Hook/chủ đề gốc:** lấy theo đúng Bước 2 — `bai-video-dang-Youtube-Anh-Minh.md` (hoặc nguồn
  ngoài Drive/Sheet khi vận hành tự động) nếu viết độc lập, hoặc hook đã chọn sẵn ở bài SEO gốc
  nếu đang convert. **KHÔNG còn dùng `hook_library_full.md`.**
- Không có bước commit/push (không còn GitHub cho video) — chỉ `create_file` lên đúng thư mục
  Drive trên rồi gửi link file cho người dùng. Hỏi người dùng trước nếu ngữ cảnh chưa rõ có nên
  tự lưu luôn không, trừ khi đã xác nhận sẵn "luôn tự lưu, không cần hỏi lại" trong phiên.

### Bước 5F — LƯU BÀI ĐĂNG FACEBOOK (song song với Bước 5, khác quy trình — thêm 20/07/2026)

Khi được yêu cầu viết **bài đăng Facebook** (đọc `facebook-factory/` — xem Bước 3), quy trình
lưu KHÁC hẳn bài SEO/kịch bản video:

- **Không dùng GitHub** — Facebook Factory không có repo output riêng.
- Sau khi bài đạt `facebook-factory/quality_check.md`, lưu thành file `.md` chứa ĐÚNG nội dung
  bài viết (không kèm field Mood/Topic/Framework/Internal Tags — những field đó chỉ dùng nội bộ
  lúc soạn, không đưa vào file lưu, giữ đúng tinh thần "pure content" như Bước 5).
- Đặt tên file: `<ngày YYYY-MM-DD>-<vài từ khoá chủ đề>.md` (VD: `2026-07-20-ngu-som-hon.md`) —
  Facebook Factory không có quy cách số thứ tự theo trụ như SEO/Video.
- Lưu trực tiếp vào thư mục Google Drive **"Bai-dang-Facebook"**
  (parentId `1zrZzd_1YEu8PC8LEQ14hGHwjuQbkV0ha`, dùng công cụ Drive `create_file`,
  `disableConversionToGoogleType: true`).
- **Đây KHÔNG phải file trigger cho n8n** — n8n có workflow "Facebook Factory" riêng, tự đọc/ghi
  Google Sheet "bai-dang-facebook-anh-minh" qua API, hoàn toàn độc lập với thư mục Drive này.
  Không tạo thêm manifest JSON cho Facebook ở Bước 6 bên dưới.

### Bước 5.5 — TẠO PROMPT ẢNH MINH HỌA ĐI KÈM (bắt buộc, ngay sau khi lưu bài SEO — quyết định
18/07/2026, cập nhật 14/07/2026 dùng Featured Image Factory riêng)

Ngay sau khi một bài SEO đã lưu xong (Bước 5), luôn tạo kèm **1 Featured Image** cho đúng bài
đó — không phải việc riêng phải đợi người dùng nhắc:

1. Đọc `featured-Image-factory/` theo đúng thứ tự trong `instructions_FEATURED_IMAGE.md` mục
   "Đọc theo thứ tự" (editorial → style → prompt → checklist → output schema). **Không dùng**
   `image-factory/` cho việc này nữa (đã tách riêng).
2. Input = đúng tên file bài viết vừa lưu (VD `1.5.co-the-can-nhung-khoang-yen-tinh`) —
   Featured Image Factory tự suy luận chủ đề từ slug và tự đặt `filename` output khớp nguyên
   tên bài (thêm đuôi `.jpg`), không cần tự viết prompt tay.
3. Featured Image **không bao giờ có nhân vật Hiền triết Anh Minh** — đây là ảnh minh họa nội
   dung chung (người vô danh/phong cảnh/đồ vật), không phải ảnh nhân vật thương hiệu. Không tra
   `core-brain/image_style_bible.md` cho việc này.
4. **KHÔNG** cho prompt ảnh vào file bài viết (giữ đúng quy tắc pure-content ở Bước 5).
   Thay vào đó, lưu thành **1 file riêng cho mỗi bài** trong Google Drive, thư mục
   "Anh Minh - N8N Trigger" → **"Prompt-Featured-Image"** (parentId
   `17ni-02iYzjljg0IM1E9aQcPShtxhiE0I`, dùng `create_file`):
   - **Tên file:** khớp nguyên tên bài viết tương ứng (VD bài `1.5.co-the-can-nhung-khoang-yen-tinh`
     → file prompt cùng tên `1.5.co-the-can-nhung-khoang-yen-tinh`), để đối chiếu 1–1 giữa hai
     thư mục.
   - **Nội dung:** đúng các field theo `featured-Image-factory/output_schema.md`, mỗi field một
     dòng: Image Type, Category, Concept, Subject, Prompt, Negative Prompt, Aspect Ratio,
     Suggested Size, Filename, Alt Text, Caption.
   - Không ghi đè file cũ trừ khi đang sửa đúng bài đó.
5. **KHÔNG còn dùng file Excel `prompt-anh.xlsx`** (bỏ 21/07/2026 cùng lúc ngừng dùng GitHub cho
   bài SEO — Excel vốn nằm ở `bai-viet-seo/_prompt-anh/`, repo đó đã ngừng dùng). Mỗi prompt giờ
   là một file Drive riêng như trên, n8n đọc trực tiếp; không cần bảng tổng hợp trung gian.
6. Sau khi tạo xong, gửi link cả hai file (bài viết + prompt ảnh) cho người dùng.

### Bước 6 — CÁC THƯ MỤC GOOGLE DRIVE N8N THEO DÕI (không còn manifest JSON — đơn giản hoá
21/07/2026)

**Lịch sử quyết định:** 14/07/2026 chuyển từ Google Sheet sang Google Drive (không có connector
ghi Sheet). Khi đó mỗi bài/ảnh cần thêm 1 file JSON "manifest" để n8n đọc. 18/07/2026 bỏ manifest
cho video, vì file `_master_script.md` thật đã nằm sẵn trong chính thư mục n8n theo dõi nên tạo
thêm JSON chứa lại y nguyên nội dung là dư thừa.

**Cập nhật 21/07/2026 — bỏ manifest JSON *lặp lại nội dung*.** Từ khi bài SEO (Bước 5.A) và
prompt ảnh (Bước 5.5) đều được lưu thẳng dưới dạng file thật vào đúng thư mục n8n theo dõi, việc
tạo thêm file `.json` **chép lại y nguyên Body** là dư thừa và dễ lệch bản (sửa file thật mà
quên sửa JSON). n8n parse trực tiếp file nội dung.

**Đính chính 26/07/2026 — riêng bài SEO vẫn cần 1 manifest CHỈ CHỨA METADATA.** Video và prompt
ảnh thì file thật *là toàn bộ sản phẩm*, nên bỏ manifest là đúng. Bài SEO thì khác: nó có 8 thứ
không tồn tại trong thân bài — Title thẻ SEO (khác H1), Slug, Meta Description, Excerpt,
Category, Tags, Internal Links, References. Bỏ manifest mà không thay bằng gì thì 8 field đó
không còn ở đâu cả, n8n chỉ nhận được thân bài. Vì vậy:

| Loại | Manifest |
|---|---|
| Kịch bản video | KHÔNG — file `_master_script.md` là toàn bộ sản phẩm |
| Prompt Featured Image | KHÔNG — file prompt là toàn bộ sản phẩm |
| **Bài SEO** | **CÓ — `<tên file>.meta.json`, chỉ metadata, KHÔNG lặp Body** |

**Thư mục gốc:** "Anh Minh - N8N Trigger" trên Google Drive, gồm 3 thư mục con (ID xác nhận
14/07/2026, dùng công cụ Drive `create_file` với đúng `parentId`):

| Thư mục | parentId | Chứa gì (file thật, KHÔNG phải manifest) |
|---|---|---|
| `Bai-viet-SEO` | `1ubrFWlDezfMX91zoV7hqjc1PqnGNZ3Gn` | Toàn văn bài viết SEO (Bước 5.A) |
| `Kich-ban-video` | `1aqbgUNiaPJ5KKQEC3QZqAn23j7oTrr4F` | Master Script kịch bản video (Bước 5.B) |
| `Prompt-Featured-Image` | `17ni-02iYzjljg0IM1E9aQcPShtxhiE0I` | Prompt Featured Image từng bài (Bước 5.5) |

Tên file trong cả 3 thư mục đều theo quy cách `<số chủ đề>.<STT>.<slug>` ở Bước 5.A, để đối
chiếu 1–1 giữa bài viết và prompt ảnh của chính bài đó.

**Không áp dụng cho Facebook** — thư mục Drive `Bai-dang-Facebook`
(`1zrZzd_1YEu8PC8LEQ14hGHwjuQbkV0ha`) lưu file `.md` nội dung thuần theo Bước 5F, và workflow
Facebook Factory trong n8n đọc trực tiếp Google Sheet "bai-dang-facebook-anh-minh" qua API,
không dùng Drive Trigger.

**Quy trình gọn lại còn 2 việc:** lưu bài SEO (Bước 5.A) → lưu prompt Featured Image của đúng bài
đó (Bước 5.5). Làm luôn, không đợi người dùng nhắc, không hỏi lại. Không tự xoá/ghi đè file cũ
trừ khi đang sửa đúng bài đó.

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

### ĐỒNG BỘ REPO — TRƯỚC KHI ĐỌC VÀ SAU KHI SỬA (bắt buộc — quy tắc thường trực,
xác nhận 25/07/2026, bổ sung vế "trước khi đọc" ngày 25/07/2026)

**Vế 1 — TRƯỚC khi đọc / rà soát / sửa bất kỳ file nào trong repo này:** luôn chạy
`git fetch origin main` rồi đối chiếu bản đang có với `origin/main`
(`git rev-list --count HEAD..origin/main` phải bằng 0). Môi trường chạy giữa các phiên có thể
giữ lại một clone cũ — đọc bản cũ sẽ cho kết luận sai. Nếu lệch → đồng bộ trước
(`git rebase origin/main`), rồi mới bắt đầu làm việc. **Không bao giờ kết luận "file X có vấn
đề" khi chưa kiểm bản đang đọc có phải bản mới nhất không.**

> Sự cố thật (21/07/2026) khiến quy tắc này ra đời: đã rà soát và báo cáo trên một bản lạc hậu
> 27 commit — nhận xét về `hook_library_full.md` vốn đã bị xoá khỏi `main`, đồng thời bỏ sót các
> file mới như `seo-factory/article_examples_full.md`, `facebook-factory/`,
> `core-brain/channel_roles.md`. Toàn bộ báo cáo phải làm lại từ đầu.

**Vế 2 — SAU khi sửa xong:**

Mỗi lần sửa BẤT KỲ file nào trong repo `ai-assistants` (kể cả sửa nhỏ, sửa 1 dòng, sửa file
bộ não của bất kỳ Factory nào — `seo-factory/`, `video-factory/`, `core-brain/`, các file
backlog ở gốc repo, hay chính `CLAUDE.md`), phải **commit + push lên GitHub ngay trong cùng
lượt làm việc đó** — KHÔNG để dồn sang lượt sau, KHÔNG đợi người dùng nhắc.

- Lý do: môi trường chạy là container tạm, có thể bị dọn sạch giữa các phiên — sửa mà chưa
  push là mất trắng. Người dùng cũng làm việc song song trên máy khác, nên bản GitHub phải
  luôn là bản mới nhất.
- Mức "đồng bộ" đạt yêu cầu = cả 3 nơi cùng trỏ về một commit: worktree local sạch
  (`git status` không còn file modified/untracked), nhánh làm việc trên remote, và `main`.
- Quy trình chuẩn đang dùng: commit → push nhánh làm việc → tạo PR → merge vào `main` →
  `git checkout -B <nhánh> origin/main` rồi push lại nhánh để mọi thứ cùng một commit.
- Sau khi xong, báo lại cho người dùng commit/PR tương ứng, không chỉ nói "đã sửa xong".
