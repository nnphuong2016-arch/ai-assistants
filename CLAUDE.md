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

**Nội dung thành phẩm KHÔNG lưu ở repo này** — xem Bước 5 bên dưới.
- Bài viết SEO → **CHỈ lưu Google Drive, KHÔNG dùng GitHub** (quyết định 06/08/2026 — quay lại
  "chỉ Drive", sau khi thử "GitHub + Drive" ngày 05/08/2026 rồi thấy không cần). Mỗi bài xuất
  **3 FILE, mỗi file 1 thư mục Drive riêng**, CÙNG TÊN (chỉ khác thư mục/đuôi file):
  **(1)** `.mdx` (có frontmatter 7 trường, dành cho web) → thư mục Drive "Bai-viet-seo-dang-web-MDX";
  **(2)** `.md` (thuần chữ, dành cho giọng đọc) → thư mục Drive "Bai-viet-SEO";
  **(3)** prompt Featured Image đi kèm → thư mục Drive "Prompt-Featured-Image" (xem Bước 5.5).
  Không còn manifest JSON nào cho bài SEO — mọi metadata cần thiết (title, subcategory, date,
  readTime, excerpt, tags, featured) đã nằm sẵn trong frontmatter của chính bản `.mdx`. Chi tiết
  đầy đủ ở `seo-factory/website_publishing_rules.md` — đọc file đó trước khi lưu bài.
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

> **Bắt buộc với SEO Factory:** luôn **đọc file `bai-seo-dang-website-Anh-Minh.md`** (gốc repo
> `ai-assistants/`) để lấy chủ đề bài viết tiếp theo — không tự nghĩ ra chủ đề ngoài file này khi
> người dùng không chỉ định. Viết **tuần tự từ trên xuống**, lấy dòng CHƯA dùng theo đúng thứ tự
> xuất hiện trong file, KHÔNG tự nhảy cóc chọn dòng theo chủ đề mình thấy hợp (đã bị người dùng
> sửa lỗi này 05/08/2026 — từng nhảy thẳng tới một chủ đề khác thay vì đi từ đầu file).

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
   Fail: title dài, slug thừa stopword, thiếu minh bạch AI, Disclaimer lẫn References, disclaimer
   y khoa lặp 2 lần, Body còn ký tự định dạng — sai 1 trong 6 điều này thì dừng và sửa ngay).
8. `seo-factory/internal_link_rules.md` — gắn 2–5 internal link (ghi ở field `Internal Links`,
   không nhúng markdown vào Body — mục 4 của file đó).
9. `core-brain/channel_roles.md` — vai trò Website so với Facebook/YouTube, tránh viết trùng vai
   trò kênh khi cùng một chủ đề gốc.
10. `seo-factory/output_schema.md` — đóng gói đúng khuôn field.
11. `seo-factory/website_publishing_rules.md` — **đọc trước khi lưu bài**: 7 trường frontmatter
    của bản `.mdx`, quy cách đặt tên chung cho cả 2 bản, và 3 nơi phải lưu (xem Bước 5.A).

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

> **Bắt buộc đọc lại từng bài sau khi viết xong** (xác nhận 06/08/2026, bổ sung 07/08/2026): viết
> xong một bài là chưa xong việc — phải đọc lại toàn bộ bài đó, đối chiếu từng điểm với checklist
> (mục 0 Quick Fail + mục 1–5 của `seo_checklist.md`, hoặc checklist tương ứng của Factory đang
> làm), và tự tìm xem có sai sót gì không: tên/tiêu đề có đúng nguyên văn backlog không (xem Bước
> 5.A), số thứ tự file có đúng không, độ dài có đúng khoảng quy định không, Body bản `.md` có còn
> sót ký tự định dạng không, có đoạn nào lặp ý/lan man/nghe rõ là AI viết không.
>
> **Không dừng lại ở việc bắt lỗi — phải chủ động sửa lại cho bài hay hơn, hấp dẫn hơn**: đọc
> tiếp theo đúng mục 6 "Chất lượng biên tập" của `seo_checklist.md` (nay là phần bắt buộc của
> bước đọc lại này, không còn là tự kiểm tùy chọn) — tìm đoạn nào đọc còn nhạt/chung chung/sáo
> rỗng, câu nào nghe rõ là AI viết, chỗ nào ý bị lặp giữa các H2, mở bài/kết bài có đủ cuốn
> người đọc chưa, ví dụ có đủ cụ thể/sống động chưa. Thấy chỗ nào nhạt hoặc sai thì **viết lại
> ngay tại chỗ đó**, không chỉ liệt kê ra rồi để nguyên. Không lưu bài "đúng checklist kỹ thuật
> là đủ" rồi để một bài nhạt, lặp ý, hoặc đọc chán lọt qua.

### Bước 5 — LƯU KẾT QUẢ VÀO ĐÚNG NƠI OUTPUT (bắt buộc, không nhầm lẫn)

Sau khi hoàn tất một bài SEO hoặc một kịch bản video (đã qua Bước 4), LUÔN lưu file kết quả vào
đúng nơi output — KHÔNG lưu trong repo `ai-assistants` này (repo này chỉ chứa bộ não/cấu hình,
không chứa nội dung thành phẩm). **Bài SEO và kịch bản video lưu ở HAI NƠI KHÁC NHAU** (5.A/5.B)
— quyết định 18/07/2026: kịch bản video chuyển hẳn sang Google Drive, ngừng dùng GitHub.

#### 5.A — Bài viết SEO: 3 FILE, 3 THƯ MỤC DRIVE (cập nhật 06/08/2026 — quay lại "chỉ Drive",
KHÔNG dùng GitHub)

> Quy tắc chi tiết (7 trường frontmatter, slug chuyên mục, quy tắc thân bài MDX) nằm ở
> `seo-factory/website_publishing_rules.md`. Mục này chỉ nêu quy trình lưu.

> **Luôn lấy chủ đề bài viết từ `bai-seo-dang-website-Anh-Minh.md`** (gốc repo `ai-assistants/`,
> xem Bước 2) trừ khi người dùng chỉ định chủ đề khác — viết TUẦN TỰ từ trên xuống, dòng CHƯA
> dùng, không tự nhảy cóc sang chủ đề khác trong file.

> **Tiêu đề (title/H1) phải giữ sát đúng nguyên văn dòng backlog tương ứng** (xác nhận
> 06/08/2026, sau khi bị sửa lỗi tự đổi câu backlog thành một câu hỏi khác). VD dòng backlog
> `1.1. Huyết áp thay đổi theo từng thời điểm trong ngày.` → title phải là "Huyết Áp Thay Đổi
> Theo Từng Thời Điểm Trong Ngày" (chỉ viết hoa đầu từ, bỏ dấu chấm cuối câu) — KHÔNG tự đổi
> thành "Vì sao huyết áp thay đổi..." hay một góc/câu hỏi khác. Slug cũng bám sát cụm từ chính
> của dòng backlog đó (không tự rút gọn mất nghĩa). Đây là ngoại lệ riêng cho **title/slug của
> SEO Factory** — không áp dụng cho quy tắc chung ở Bước 2 ("không copy nguyên dòng backlog làm
> thẳng title/caption") vốn dành cho hook mạng xã hội/video; dòng backlog SEO đã được viết sẵn
> như một tiêu đề hoàn chỉnh nên giữ nguyên là đúng.

**Thứ tự làm — viết BẢN MDX TRƯỚC, rồi sinh bản MD từ chính nó** (để hai bản không thể lệch chữ,
không viết tay hai lần):

1. **Viết bản `.mdx`** — có frontmatter 7 trường, có `##`/`###`, blockquote khi trích lời Anh
   Minh, link markdown. Lưu vào Google Drive, thư mục "Anh Minh - N8N Trigger" →
   **"Bai-viet-seo-dang-web-MDX"** (dùng Drive `create_file`, `disableConversionToGoogleType: true`
   để giữ nguyên chữ markdown, không bị Google Docs diễn giải).
2. **Sinh bản `.md` bằng cách gỡ lớp định dạng khỏi chính file `.mdx` đó**: bỏ frontmatter, bỏ
   `#`, `>`, `**`, đổi `[chữ neo](/url)` thành chữ neo trần. Kết quả phải **thuần chữ 100%** theo
   `web_content_rules.md` mục 3D. Lưu vào Google Drive, thư mục "Anh Minh - N8N Trigger" →
   **"Bai-viet-SEO"** (parentId `1ubrFWlDezfMX91zoV7hqjc1PqnGNZ3Gn`, dùng Drive `create_file`,
   `contentMimeType: "text/plain"`, `disableConversionToGoogleType: true`). Đây là thư mục n8n
   theo dõi bằng Drive Trigger để kích hoạt pipeline giọng đọc.
3. Gửi người dùng link cả 3 file (mdx, md, và prompt Featured Image ở Bước 5.5) — **không dùng
   GitHub, không commit/push** cho bài SEO.

**3 file TRÙNG TÊN, chỉ khác thư mục/đuôi file** — để đối chiếu được bằng mắt. VD:
`1.1.vi-sao-ngu-du-tam-tieng-van-met.mdx` (thư mục MDX), `1.1.vi-sao-ngu-du-tam-tieng-van-met.md`
(thư mục Bai-viet-SEO), và `1.1.vi-sao-ngu-du-tam-tieng-van-met` (thư mục Prompt-Featured-Image,
không đuôi — xem Bước 5.5).

Nội dung file (áp dụng cho phần thân bài của CẢ HAI bản):
1. Đặt tên file theo đúng quy cách ở dưới — không ghi đè file cũ trừ khi đang sửa đúng bài đó.
2. **File CHỈ chứa đúng nội dung bài viết (những gì hiển thị cho người đọc trên web) — KHÔNG
   thêm bất kỳ chữ/field/ghi chú nào khác** (riêng bản `.mdx` có thêm frontmatter ở đầu):
   - CÓ trong file: tiêu đề bài, toàn văn thân bài, FAQ hiển thị trên trang (Q&A thật),
     disclaimer + minh bạch AI (đây là nội dung bắt buộc hiển thị ở chân bài theo
     `web_content_rules.md`, không phải ghi chú nội bộ). **Không còn ghi "Cập nhật: ngày"** — bỏ
     hẳn 11/08/2026 theo yêu cầu người vận hành (lý do: field này không phục vụ người đọc, và khi
     ép mỗi bài phải có dòng ngày tháng cuối bài, AI dễ sinh thêm câu đệm để "đủ format" quanh nó).
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
     | Sức khỏe (1) | Không — bỏ 06/08/2026, xem khối đóng bài mới dưới đây | Có — dùng khối đầy đủ dưới đây |
     | Tâm lý & đời sống (2) | **Có** — dùng khối rút gọn ở cuối mục này | Không |
     | Dưỡng sinh, Triết lý, Đồng hành, Bếp An Nhiên | Không bắt buộc | Không |

     (Mẫu D — Đồng hành — có khối kết riêng theo `dong_hanh_nguoi_benh.md`, giữ nguyên.)

   - **Khối đóng bài chuẩn (bắt buộc, CHỈ áp dụng cho bài thuộc chủ đề Sức khỏe — số 1, chốt lại
     06/08/2026 theo yêu cầu người vận hành, bỏ dòng "Cập nhật: ngày" ngày 11/08/2026 — áp dụng
     cho MỌI bài Sức khỏe, kể cả các bài đã lưu trước đó, cần sửa lại theo đúng khối mới này):** đặt cuối file, sau FAQ, dùng đúng khuôn
     dưới đây — dòng tiêu đề "Lưu ý" (viết trơn, KHÔNG có `###` đứng trước, theo mục 3D) tạo
     ranh giới rõ giữa đoạn kết cảm xúc của bài và phần thông tin bắt buộc, tránh gãy mạch/gây
     hụt hẫng cho người đọc. **Không còn nhắc tên nhân vật hay chữ "AI" trong khối này** — dòng
     minh bạch AI đã bị bỏ khỏi khối đóng bài Sức khỏe theo quyết định 06/08/2026 (xem bảng ở
     trên). **Các chủ đề khác (Dưỡng sinh, Triết lý, Đồng hành, Bếp An Nhiên) KHÔNG dùng khối
     này; Tâm lý dùng khối rút gọn** ghi ở cuối mục — chưa đổi, vẫn giữ nguyên như cũ, khớp đúng
     `web_content_rules.md` mục 2 (disclaimer y khoa chỉ bắt buộc cho bài chạm sức khỏe) và
     `article_templates.md` (Mẫu C triết lý không cần disclaimer y khoa, Mẫu D đồng hành có
     khối kết riêng theo `dong_hanh_nguoi_benh.md`). Nếu một bài ở chủ đề khác có chạm nhẹ tới
     sức khỏe, cân nhắc theo đúng tinh thần "chỉ cần khi bài thật sự nói về sức khỏe", không áp
     máy móc. Các chủ đề khác (Tâm lý, Dưỡng sinh, Triết lý, Đồng hành, Bếp An Nhiên) người vận
     hành sẽ chốt khối đóng bài riêng sau — chưa áp dụng thay đổi này cho các chủ đề đó.

     ```
     Lưu ý

     Đây là chia sẻ các góc nhìn về lối sống ở mức phổ thông, không thay thế tư vấn, chẩn đoán
     hoặc điều trị y khoa. Nếu triệu chứng kéo dài hoặc ảnh hưởng đến sinh hoạt hằng ngày, hãy
     trao đổi với bác sĩ chuyên môn.
     ```

     > **Không lặp disclaimer** (chốt 11/08/2026, sau khi bị người vận hành bắt lỗi 50 bài SEO đầu
     > tiên đều mắc): khối "Lưu ý" trên là nơi DUY NHẤT nhắc "không thay thế tư vấn y khoa". Nếu
     > bài có mục "Khi nào nên tìm đến bác sĩ" ở giữa thân bài, mục đó chỉ nêu dấu hiệu cụ thể nên
     > đi khám — KHÔNG lặp lại câu kiểu "những chia sẻ trên chỉ ở mức thói quen sống chung, không
     > thay thế tư vấn y khoa" ngay sau đó, vì khối Lưu ý cuối bài đã nói đúng ý này rồi. Đọc lại
     > bài (Bước 4) phải tự rà xem có bị lặp ý này không trước khi coi là xong.
   - KHÔNG cho vào file: Title thẻ SEO (khác H1), Meta Description, Loại bài, tên Hook đã dùng,
     ghi chú kiểu "References để trống vì...", "chưa có internal link vì...". Đây là nội dung
     chỉ dùng nội bộ lúc soạn — nếu cần lưu lại, ghi trong phần trả lời cho người dùng, KHÔNG
     nhét vào 3 file lưu. (Slug/Category suy ra từ tên file; Tags/Excerpt/Internal Links đã nằm
     sẵn trong frontmatter + body của bản `.mdx` — không cần file manifest riêng.)
   - Field nào không có nội dung thật (VD: chưa có nguồn để trích dẫn) → **không đưa vào file**,
     không viết placeholder giải thích.
3. Lưu đủ 3 thư mục Drive theo thứ tự ở đầu mục 5.A (MDX → md → prompt Featured Image ở Bước
   5.5), rồi gửi người dùng link cả 3. Hỏi người dùng trước nếu ngữ cảnh chưa rõ có nên tự lưu
   luôn không, trừ khi đã xác nhận sẵn "luôn tự lưu, không cần hỏi lại" trong phiên.

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
**"Bai-viet-SEO"** (parentId `1ubrFWlDezfMX91zoV7hqjc1PqnGNZ3Gn`, dùng `search_files` với
`parentId`) bắt đầu bằng đúng `<số chủ đề>.` (VD: liệt kê file bắt đầu `1.` để biết đã có bài
Sức khỏe nào), lấy số thứ tự lớn nhất + 1. Nếu chưa có file nào của chủ đề đó → bắt đầu từ `1`.
Cả 3 thư mục Drive đằng nào cũng mang cùng một tên file, nên đếm ở thư mục nào cũng ra cùng
kết quả — chọn "Bai-viet-SEO" làm chuẩn để nhất quán.

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
3. **LẤY Ý CHÍNH BÀI VIẾT LÀM SUBJECT TRỰC TIẾP + TỰ KIỂM "2 GIÂY" — BẮT BUỘC, làm TRƯỚC khi
   viết Prompt hoàn chỉnh** (chốt 06/08/2026, sau sự cố thật: nhiều Featured Image chọn Subject
   là cảnh đời sống chung chung — VD "người cầm ly nước" cho bài so sánh huyết áp cao/thấp,
   "người tưới cây" cho bài huyết áp tăng âm thầm — đúng Concept Lifestyle nhưng Subject không
   ai đoán được bài nói về điều gì). Quy tắc gốc và ví dụ áp dụng theo từng loại chủ đề (bộ
   phận cơ thể, giấc ngủ, cảm xúc, thói quen...) nằm ở `featured_image_editorial_rules.md`
   mục 7B — đọc kỹ mục đó trước khi chọn Subject, không tự suy diễn xa khỏi nội dung bài thật.
   Sau khi chọn Subject theo đúng mục 7B, tự hỏi đúng nguyên văn: *"Nếu người đọc chỉ nhìn
   Featured Image này trong khoảng 2 giây, họ có đoán đúng bài viết đang nói về điều gì
   không?"*
   - Nếu **CÓ** → được viết Prompt hoàn chỉnh, sang bước 4.
   - Nếu **KHÔNG** → STOP, quay lại mục 7B chọn Subject khác, không viết Prompt cho Subject
     vừa loại.
   - Nếu chủ đề CHÍNH của bài là cấu trúc/bộ phận bên trong cơ thể (mạch máu, nội tạng, cơ
     chế sinh lý) chứ không phải một hành vi/thói quen sống → đổi hẳn Concept sang **Medical
     Illustration** (đúng `featured_image_editorial_rules.md` mục 6), vẫn giữ bảng màu thương
     hiệu, phong cách nhẹ nhàng/giáo dục, không máu/rùng rợn.
4. Featured Image **không bao giờ có nhân vật Hiền triết Anh Minh** — đây là ảnh minh họa nội
   dung chung (người vô danh/phong cảnh/đồ vật), không phải ảnh nhân vật thương hiệu. Không tra
   `core-brain/image_style_bible.md` cho việc này.
5. **KHÔNG** cho prompt ảnh vào file bài viết (giữ đúng quy tắc pure-content ở Bước 5).
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
6. **KHÔNG còn dùng file Excel `prompt-anh.xlsx`** và **KHÔNG dùng repo GitHub nào** cho việc
   này (bỏ hẳn 06/08/2026). Mỗi prompt là một file Drive riêng như trên, n8n đọc trực tiếp;
   không cần bảng tổng hợp trung gian.
7. Sau khi tạo xong, gửi link cả 3 file (mdx, md, prompt ảnh) cho người dùng.

> ⚠️ **Công cụ Drive hiện có KHÔNG hỗ trợ xóa hay ghi đè file** — chỉ có `create_file`. Nếu phát
> hiện một prompt ảnh đã lưu bị sai (như sự cố 06/08/2026 ở trên) và cần sửa, tạo file mới đúng
> nội dung rồi **báo rõ cho người dùng ID/link file CŨ cần tự xóa thủ công**, không im lặng để
> hai file trùng tên (một đúng, một sai) cùng tồn tại trong thư mục mà không cảnh báo.

### Bước 6 — CÁC THƯ MỤC GOOGLE DRIVE N8N THEO DÕI (KHÔNG manifest JSON nào — cập nhật 06/08/2026)

**Lịch sử quyết định:** 14/07/2026 chuyển từ Google Sheet sang Google Drive. 18/07/2026 bỏ
manifest cho video, vì file `_master_script.md` thật đã nằm sẵn trong chính thư mục n8n theo dõi.
21/07/2026 bỏ manifest lặp Body cho SEO/prompt ảnh. 26/07/2026 từng thêm lại 1 manifest CHỈ
METADATA riêng cho bài SEO (khi đó dùng 2 repo GitHub + Drive). 05/08/2026 thử "GitHub quay lại
dùng". **06/08/2026 — quay lại "chỉ Drive" hẳn, bỏ luôn manifest JSON của bài SEO**: từ nay bản
`.mdx` (thư mục "Bai-viet-seo-dang-web-MDX") tự mang đủ 7 trường frontmatter cần cho web
(title, subcategory, date, readTime, excerpt, tags, featured); slug/category suy ra từ tên file;
internal link nằm ngay trong markdown link của body. Không còn field nào bị thiếu chỗ chứa, nên
không cần manifest nữa. Cả 3 loại sản phẩm giờ đều **không có manifest**:

| Loại | Manifest |
|---|---|
| Bài SEO | KHÔNG — bản `.mdx` (frontmatter + body) và bản `.md` là toàn bộ sản phẩm |
| Kịch bản video | KHÔNG — file `_master_script.md` là toàn bộ sản phẩm |
| Prompt Featured Image | KHÔNG — file prompt là toàn bộ sản phẩm |

**Thư mục gốc:** "Anh Minh - N8N Trigger" trên Google Drive, gồm các thư mục con sau (ID xác
nhận qua ảnh chụp thư mục thật của người dùng ngày 06/08/2026, dùng công cụ Drive `create_file`
với đúng `parentId`):

| Thư mục | parentId | Chứa gì (file thật, KHÔNG phải manifest) |
|---|---|---|
| `Bai-viet-SEO` | `1ubrFWlDezfMX91zoV7hqjc1PqnGNZ3Gn` | Bản `.md` thuần chữ của bài viết SEO (Bước 5.A) |
| `Bai-viet-seo-dang-web-MDX` | `1FBUMRZSLWmfe1d3WkdLfp9l0IXm_ihIA` | Bản `.mdx` có frontmatter của bài viết SEO (Bước 5.A) |
| `Prompt-Featured-Image` | `17ni-02iYzjljg0IM1E9aQcPShtxhiE0I` | Prompt Featured Image từng bài (Bước 5.5) |
| `Kich-ban-video` | `1aqbgUNiaPJ5KKQEC3QZqAn23j7oTrr4F` | Master Script + file prompt kịch bản video (Bước 5.B) |

> Thư mục "Anh Minh - N8N Trigger" còn có `voice-doc-bai-seo` (chứa file `.mp3` giọng đọc) và
> `Featured-Image` (chứa file `.jpg` ảnh đã render) — đây là **thư mục OUTPUT của n8n** (kết quả
> sau khi n8n xử lý xong file mình lưu), KHÔNG phải nơi Claude ghi vào.

Tên file trong 3 thư mục bài SEO đều theo quy cách `<số chủ đề>.<STT>.<slug>` ở Bước 5.A, để đối
chiếu 1–1 giữa bản mdx, bản md, và prompt ảnh của chính bài đó.

**Không áp dụng cho Facebook** — thư mục Drive `Bai-dang-Facebook`
(`1zrZzd_1YEu8PC8LEQ14hGHwjuQbkV0ha`) lưu file `.md` nội dung thuần theo Bước 5F, và workflow
Facebook Factory trong n8n đọc trực tiếp Google Sheet "bai-dang-facebook-anh-minh" qua API,
không dùng Drive Trigger.

**Quy trình gọn lại còn 2 việc:** lưu bài SEO — 2 file mdx+md (Bước 5.A) → lưu prompt Featured Image của đúng bài
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

> ⚠️ **PUSH LÊN NHÁNH CHƯA PHẢI LÀ XONG — PHẢI ĐI TỚI `main`** (siết lại 05/08/2026, sau sự cố
> thật ngay trong ngày). Người vận hành kéo về máy từ **`main`**, không từ nhánh làm việc. Một
> thay đổi mới push lên nhánh mà chưa merge thì với họ **coi như chưa tồn tại** — kể cả khi đã
> commit sạch sẽ và báo "đã push xong".
>
> Sự cố: quy trình lưu bài SEO 2 bản/3 nơi đã sửa vào `CLAUDE.md` và push lên nhánh, nhưng
> `main` vẫn giữ câu cũ *"chỉ lưu Google Drive, ngừng dùng repo `bai-viet-seo`"* — ngược hẳn.
> Vì `CLAUDE.md` tự nạp đầu mỗi phiên, một phiên mới đọc `main` sẽ làm sai hoàn toàn. Người vận
> hành phải tự hỏi "đồng bộ chưa" mới lộ ra.
>
> **Chưa merge vào `main` thì KHÔNG được báo là "đã đồng bộ".** Nếu không tự merge được (thiếu
> quyền, PR còn chờ duyệt), phải nói thẳng: *"đã push lên nhánh, còn chờ merge vào `main`, bạn
> kéo về máy chưa thấy đâu"* — không được để người dùng tưởng là xong.
