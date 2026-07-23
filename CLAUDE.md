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
20/07/2026; **2 nguồn ý tưởng song song**: `bai-dang-Facebook-Anh-Minh.md` + tự sinh qua
`idea_library.md` — xem Bước 2), `image-factory/`, `featured-image-factory/` (chuyên riêng ảnh
đại diện đầu bài viết — tách khỏi `image-factory/` từ 14/07/2026, độc lập, không gắn với Image
Factory hay bất kỳ Factory nào khác), `ai-anh-minh-chat-factory/`, `research-factory/`,
`review-factory/`, `publish-factory/`), cùng 3 file backlog chủ đề riêng cho từng kênh (thay
cho `hook_library_full.md` cũ — xem Bước 2): `bai-seo-dang-website-Anh-Minh.md`,
`bai-dang-Facebook-Anh-Minh.md`, `bai-video-dang-Youtube-Anh-Minh.md`.

**Nội dung thành phẩm KHÔNG lưu ở repo này** — xem Bước 5 bên dưới:
- Bài viết SEO → GitHub `nnphuong2016-arch/bai-viet-seo`, sau đó luôn tạo thêm file manifest
  JSON trong Google Drive ("Anh Minh - N8N Trigger") để kích hoạt n8n — xem Bước 6.
- Kịch bản video → **chỉ lưu trực tiếp Google Drive, KHÔNG dùng GitHub nữa** (quyết định
  18/07/2026 — đã ngừng dùng repo `kich-ban-video`) — thư mục "Anh Minh - N8N Trigger" →
  "Kich-ban-video". Không cần thêm manifest JSON riêng cho video (xem Bước 5.B + Bước 6).
- Bài đăng Facebook → Google Drive riêng (không GitHub) — xem Bước 5F.

---

## QUY TẮC BẮT BUỘC — ĐỌC TRƯỚC KHI TẠO BẤT KỲ NỘI DUNG NÀO

Trước khi viết **bài SEO**, **kịch bản video**, **post cộng đồng**, **prompt ảnh**, hay bất kỳ
nội dung nào cho kênh này, LUÔN thực hiện theo đúng thứ tự:

### Bước 1 — Luôn đọc CORE_BRAIN trước (bắt buộc, mọi loại nội dung)

> **Ngoại lệ đã xác nhận đúng, giữ nguyên:** Chat Factory (`ai-anh-minh-chat-factory/`) và
> Featured Image Factory (`featured-image-factory/`) KHÔNG dán `core-brain/instructions.md` vào
> ô Instructions — mỗi factory có lý do riêng đã ghi trong `instructions_CHAT.md` và
> `instructions_FEATURED_IMAGE.md` của chính nó. Đây là ngoại lệ có chủ đích, không phải thiếu sót.

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
| Facebook Factory | **2 nguồn song song** (20/07/2026): `bai-dang-Facebook-Anh-Minh.md` (kho 210 hook có sẵn, 7 series) + tự sinh qua `facebook-factory/idea_library.md` (Pattern + Emotion + Observation + Contradiction). Ưu tiên hook chưa dùng trong file trước; nếu đã dùng hết/không hợp chủ đề đang cần → chuyển sang tự sinh. | gốc repo `ai-assistants/` + `facebook-factory/idea_library.md` |

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
- `hook_library_full.md` (2 bản cũ ở `assets/` và `project-memory/`) giữ lại để tham khảo lịch
  sử, KHÔNG xoá, nhưng KHÔNG Factory nào còn đọc file này nữa.

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

**Khi được yêu cầu viết KỊCH BẢN VIDEO:** đọc đúng theo thứ tự trong `video-factory/
instructions_VIDEO.md` mục 3 (nguồn danh sách file đầy đủ, cập nhật 23/07/2026 — không lặp lại
danh sách ở đây để tránh 2 nơi cùng liệt kê rồi lệch nhau khi thêm file mới): `instructions_VIDEO.md`
→ `video_rules.md` → `examples_and_hooks.md` → `core-brain/image_style_bible.md` →
`video_ai_prompt_rules.md` + `model_selection_rules.md` (luôn đọc cùng nhau) → `bep_an_nhien.md`
+ `food_library.md` (chỉ khi làm chuỗi "Bếp An Nhiên") → `duong_sinh_bai_tap.md` +
`bai_tap_library.md` (chỉ khi làm Nhánh B — Dưỡng Sinh Ngắn) → `core-brain/channel_roles.md` →
`output_schema.md`.

**Khi được yêu cầu viết BÀI ĐĂNG FACEBOOK (Page/Group):** đọc `facebook-factory/` theo đúng thứ
tự trong `instructions_facebook.md` (đã ghi rõ trong file: instructions_facebook → execution_flow
→ writing_rules → writing_craft → quality_check → post_frameworks → emotion_palette →
idea_library → hook_library → topic_map → post_examples → output_schema). Factory riêng, tách
khỏi Community Factory từ 20/07/2026.

**Khi được yêu cầu viết post Zalo/Newsletter hoặc trả lời bình luận:** đọc `community-factory/`
(instructions_COMMUNITY, community_rules, social_templates, storytelling_patterns,
engagement_rules, community_checklist, output_schema). Community Factory KHÔNG còn viết bài
Facebook nữa.

**Khi được yêu cầu tạo PROMPT ẢNH:**
- **Ảnh đại diện đầu bài viết (Featured Image)** → đọc `featured-image-factory/`
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

#### 5.A — Bài viết SEO (GitHub `nnphuong2016-arch/bai-viet-seo`)

Quy trình khi lưu:
1. Nếu repo chưa có trong session → gọi `add_repo` (owner: `nnphuong2016-arch`, repo:
   `bai-viet-seo`), clone, rồi `register_repo_root`.
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
     đọc được — chuyển sang lưu ở Google Drive manifest (xem Bước 6) hoặc trong commit message
     (lý do quyết định), không nằm trong file.
   - Field nào không có nội dung thật (VD: chưa có nguồn để trích dẫn) → **không đưa vào file**,
     không viết placeholder giải thích.
4. Commit + push (hỏi người dùng trước nếu ngữ cảnh chưa rõ có nên tự push luôn không, trừ khi
   người dùng đã xác nhận sẵn "luôn tự lưu, không cần hỏi lại" trong phiên).

**Quy cách đặt tên file bài SEO:** `<số chủ đề>.<số thứ tự bài trong chủ đề đó>.<slug>.md`

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

Ví dụ: bài SEO đầu tiên thuộc chủ đề Sức khỏe → `1.1.<slug>.md`. Bài Sức khỏe tiếp theo →
`1.2.<slug>.md`. Bài đầu tiên thuộc Tâm lý & đời sống → `2.1.<slug>.md`.

**Cách xác định số thứ tự:** trước khi tạo file mới, liệt kê các file đã có trong repo
`bai-viet-seo` bắt đầu bằng đúng `<số chủ đề>.` (VD: liệt kê file bắt đầu `1.` để biết đã có bài
Sức khỏe nào), lấy số thứ tự lớn nhất + 1. Nếu chưa có file nào của chủ đề đó → bắt đầu từ `1`.

Repo `bai-viet-seo` KHÔNG chứa bộ não/quy tắc — chỉ chứa thành phẩm cuối cùng. Không tự thêm
CLAUDE.md hay file cấu hình vào repo đó.

#### 5.B — Kịch bản video (Google Drive — KHÔNG dùng GitHub)

- **Nơi lưu:** Google Drive, thư mục "Anh Minh - N8N Trigger" → "Kich-ban-video" (parentId
  `1aqbgUNiaPJ5KKQEC3QZqAn23j7oTrr4F`, dùng công cụ Drive `create_file`). File chứa **toàn văn
  Master Script** — n8n đọc/parse trực tiếp file này (xem `video-factory/video_ai_contract.md`),
  KHÔNG cần repo GitHub `kich-ban-video` (đã ngừng dùng) và KHÔNG cần thêm manifest JSON riêng
  (nội dung thật đã nằm sẵn trong chính file `.md` này — xem thêm ghi chú ở Bước 6).
- **Tên file:** `<số chủ đề>.<STT>. <Tên video>_master_script.md` — số chủ đề theo đúng bảng ở
  mục 5.A; STT xác định bằng cách liệt kê file đã có cùng `<số chủ đề>.` trong thư mục Drive
  "Kich-ban-video" (đếm ĐỘC LẬP với `bai-viet-seo`, kể cả khi video chuyển thể từ đúng bài SEO
  đó). `<Tên video>` giữ nguyên tên tiếng Việt, có dấu cách/viết hoa như bình thường — KHÔNG rút
  gọn thành slug; bỏ các ký tự không an toàn cho tên file khi tải về máy (Windows):
  `\ / : * ? " < > |` (VD dấu `?` cuối câu hỏi thì bỏ hẳn).
  VD: `1.1. Vì sao ngủ đủ tám tiếng mà vẫn thấy mệt_master_script.md`.
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

1. Đọc `featured-image-factory/` theo đúng thứ tự trong `instructions_FEATURED_IMAGE.md` mục
   "Đọc theo thứ tự" (editorial → style → prompt → checklist → output schema). **Không dùng**
   `image-factory/` cho việc này nữa (đã tách riêng).
2. Input = đúng tên file bài viết vừa lưu (VD `1.5.co-the-can-nhung-khoang-yen-tinh.md`) —
   Featured Image Factory tự suy luận chủ đề từ slug và tự đặt `filename` output khớp nguyên
   tên bài (chỉ đổi đuôi `.md`→`.jpg`), không cần tự viết prompt tay.
3. Featured Image **không bao giờ có nhân vật Hiền triết Anh Minh** — đây là ảnh minh họa nội
   dung chung (người vô danh/phong cảnh/đồ vật), không phải ảnh nhân vật thương hiệu. Không tra
   `core-brain/image_style_bible.md` cho việc này.
4. **KHÔNG** cho prompt ảnh vào file `.md` của bài viết (giữ đúng quy tắc pure-content ở Bước 5).
   Thay vào đó, ghi vào **1 file Excel chạy dọc duy nhất** (không tạo file rời cho từng bài):
   - Vị trí: `bai-viet-seo/_prompt-anh/prompt-anh.xlsx` (cho ảnh bài SEO). Nếu sau này cần prompt
     ảnh riêng cho video/kịch bản, lưu tương tự nhưng dưới dạng file Excel riêng trong Google
     Drive (không dùng đường dẫn GitHub `kich-ban-video/_prompt-anh/` nữa — repo đó đã ngừng
     dùng từ 18/07/2026, xem Bước 5.B).
   - **Thứ tự cột đầy đủ** (cập nhật 14/07/2026, khớp cấu trúc Google Sheet "Anh Minh hook
     list" ở Bước 6 để đồng bộ; cột Link kịch bản video sửa 18/07/2026 vì video không còn ở
     GitHub): STT, Bài viết (tên file), Link bài SEO (raw GitHub link), **Link kịch bản video**
     (link Google Drive file `_master_script.md` trong thư mục "Kich-ban-video" — để trống nếu
     bài chưa có video), rồi tới các cột theo `featured-image-factory/output_schema.md` (Image
     Type, Category, Concept,
     Subject, Prompt, Negative Prompt, Aspect Ratio, Suggested Size, Filename, Alt Text,
     Caption), và **Trạng thái** ở cột cuối cùng (để trống khi mới tạo, cập nhật thủ công khi
     đã đăng/publish).
   - Không ghi đè các dòng cũ — chỉ thêm dòng mới ở cuối.
5. Commit + push file Excel đã cập nhật vào đúng repo output (cùng lúc hoặc ngay sau khi push bài
   viết), rồi gửi file đã cập nhật cho người dùng (không chỉ báo đã làm xong mà không đưa file).
6. File Excel này nằm trong repo chỉ để lưu bền qua các phiên làm việc (môi trường chạy có thể bị
   dọn sạch giữa các phiên) — không phải nội dung xuất bản, không vi phạm quy tắc "repo output chỉ
   chứa thành phẩm cuối cùng" vì đây là file phụ trợ pipeline riêng, đặt trong thư mục con
   `_prompt-anh/` tách biệt rõ khỏi các file `.md` bài viết.

### Bước 6 — TẠO FILE MANIFEST TRONG GOOGLE DRIVE CHO N8N (bắt buộc — chỉ còn áp dụng cho SEO
và Featured Image, KHÔNG áp dụng cho video/Facebook, xem lý do bên dưới)

**Đã đổi từ Google Sheet sang Google Drive (quyết định 14/07/2026)** — Google Sheet "Anh Minh
hook list" KHÔNG còn dùng làm đầu vào n8n nữa (không có connector ghi Sheet, kỹ thuật không cho
phép). Thay bằng: tạo 1 file JSON "manifest" trong Google Drive cho mỗi bài/ảnh đã hoàn tất —
n8n dùng Drive Trigger theo dõi các thư mục dưới đây để tự kích hoạt workflow (đăng bài, tạo
ảnh...).

**Cập nhật 18/07/2026 — bỏ manifest JSON cho video:** từ khi kịch bản video chuyển sang lưu trực
tiếp Google Drive dưới dạng file `..._master_script.md` thật (Bước 5.B) ngay trong chính thư mục
`Kich-ban-video` mà n8n theo dõi, việc tạo thêm 1 file `.json` chứa lại y nguyên nội dung đó là
**dư thừa/trùng lặp** — n8n parse thẳng file `.md` (xem `video-factory/video_ai_contract.md`
ghi chú WF-07B). Vì vậy **KHÔNG còn tạo manifest JSON cho video nữa** — chỉ còn áp dụng cho bài
viết SEO và Featured Image.

**Thư mục gốc:** "Anh Minh - N8N Trigger" trên Google Drive, gồm 3 thư mục con (ID xác nhận
14/07/2026, dùng công cụ Drive `create_file` với đúng `parentId`):

| Thư mục | parentId | Dùng cho |
|---|---|---|
| `Bai-viet-SEO` | `1ubrFWlDezfMX91zoV7hqjc1PqnGNZ3Gn` | Manifest bài viết SEO (JSON) |
| `Kich-ban-video` | `1aqbgUNiaPJ5KKQEC3QZqAn23j7oTrr4F` | File Master Script kịch bản video thật (`.md`, xem Bước 5.B) — KHÔNG tạo thêm manifest JSON ở đây nữa |
| `Prompt-Featured-Image` | `17ni-02iYzjljg0IM1E9aQcPShtxhiE0I` | Manifest Featured Image (JSON) |

**Không áp dụng cho Facebook** — thư mục Drive `Bai-dang-Facebook`
(`1zrZzd_1YEu8PC8LEQ14hGHwjuQbkV0ha`) lưu file `.md` nội dung thuần theo Bước 5F, KHÔNG phải
manifest JSON kích hoạt n8n — workflow Facebook Factory trong n8n đọc trực tiếp Google Sheet
"bai-dang-facebook-anh-minh" qua API, không dùng Drive Trigger.

**Tên file manifest:** khớp đúng slug bài viết + `.json` (VD:
`1.5.co-the-can-nhung-khoang-yen-tinh.json`) — dùng `disableConversionToGoogleType: true` khi
tạo, để giữ đúng JSON thuần, không bị convert sang Google Docs.

**Nội dung file:**

`Bai-viet-SEO/<slug>.json`:
```json
{
  "slug": "1.5.co-the-can-nhung-khoang-yen-tinh",
  "hook_number": "1.5",
  "hook_text": "...(đúng câu/dòng đã dùng, khớp đúng file backlog của Factory tương ứng — xem Bước 2)...",
  "category": "Sức khỏe",
  "title": "...",
  "content_markdown": "...(toàn văn bài viết, đúng nội dung đã push GitHub — Bước 5.A)...",
  "link_github": "https://raw.githubusercontent.com/nnphuong2016-arch/bai-viet-seo/main/1.5.co-the-can-nhung-khoang-yen-tinh.md"
}
```

`Prompt-Featured-Image/<slug>.json`: đúng nguyên object `output_schema.md` của Featured Image
Factory (`image_type`, `category`, `concept`, `subject`, `prompt`, `negative_prompt`,
`aspect_ratio`, `suggested_size`, `filename`, `alt_text`, `caption`) — thêm `slug` ở đầu để dễ
đối chiếu.

**Quy trình:** ngay sau khi push GitHub bài SEO (Bước 5.A) và cập nhật Excel (Bước 5.5), tạo
LUÔN manifest JSON tương ứng (SEO luôn có, Featured Image tuỳ đã làm xong phần nào) — không đợi
người dùng nhắc, không hỏi lại. Với kịch bản video, chỉ cần lưu đúng file `_master_script.md`
theo Bước 5.B, KHÔNG tạo thêm file `.json`. Facebook cũng không tham gia bước này (xem Bước 5F).
Không tự xoá/ghi đè manifest cũ trừ khi đang sửa đúng bài đó.

Excel (`prompt-anh.xlsx`, Bước 5.5) vẫn giữ nguyên song song — dùng để người dùng rà soát thủ
công, độc lập với luồng Drive/n8n tự động.

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
