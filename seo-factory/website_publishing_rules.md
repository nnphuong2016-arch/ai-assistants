# WEBSITE PUBLISHING RULES — BÀN GIAO BÀI SEO CHO WEBSITE

> Tải lên khu **Files** của SEO Factory. File này quy định **định dạng bàn giao** bài SEO cho
> website (Next.js/MDX) — khác với `output_schema.md` (khuôn field nội bộ của Factory) và
> `web_content_rules.md` (quy tắc viết nội dung).
> Nguồn: Claude website bàn giao ngày 26/07/2026, file gốc `huong-dan-dang-bai-seo.md`.
> Cập nhật: 26/07/2026.

> ⚠️ **FILE NÀY CHƯA ĐẦY ĐỦ.** Mới nhận được bản tóm tắt, chưa nhận toàn văn
> `huong-dan-dang-bai-seo.md`. Hai phần còn thiếu được đánh dấu **[CHƯA CÓ]** bên dưới — chưa
> lấp đủ hai phần đó thì **KHÔNG xuất file `.mdx` thật**, vì đoán sai tên trường frontmatter sẽ
> làm hỏng build của website.

---

## 1. ĐỊNH DẠNG BÀN GIAO

- **Đuôi file:** `.mdx` (không phải `.md`).
- **Quy trình:** SEO Factory xuất file `.mdx` → người vận hành đặt tên file → copy vào đúng thư
  mục chuyên mục → xong, không phải sửa code. Server đang chạy `npm run dev` thì refresh là thấy;
  bản build production thì cần build/deploy lại.
- **Chuyên mục KHÔNG nằm trong frontmatter** — chuyên mục do **thư mục chứa file** quyết định.
  Vì vậy không điền field `category` vào frontmatter, tránh hai nguồn sự thật đá nhau.

---

## 2. FRONTMATTER (7 trường, nhận 26/07/2026)

```
---
title: "Tiêu đề bài viết"
subcategory: "cam-xuc-noi-tam"
date: "2026-08-05"
readTime: "6 phút đọc"
excerpt: "Tóm tắt 1-2 câu"
tags: ["Cảm xúc", "Tâm lý"]
featured: false
---
```

| Trường | Quy tắc |
|---|---|
| `title` | Tiêu đề hiển thị. Website tự render thành H1 → **không viết H1 trong thân bài** (mục 5) |
| `subcategory` | **Đúng 1 slug** mục con, lấy từ danh sách mục 4 |
| `date` | Định dạng `YYYY-MM-DD` |
| `readTime` | Chuỗi có chữ, VD `"6 phút đọc"` |
| `excerpt` | 1–2 câu, dùng lại field `Excerpt` ở `output_schema.md` |
| `tags` | Mảng chuỗi, **có dấu tiếng Việt và viết hoa** (khác slug) |
| `featured` | `true`/`false`, mặc định `false` |

**KHÔNG có trường `category`** — chuyên mục do thư mục quyết định (mục 1).

> ⚠️ **Xung đột cần biết:** `output_schema.md` ghi *"Reading Time không nằm trong khuôn xuất,
> không để AI tự ước lượng số phút đọc vì AI đếm từ không đáng tin"*. Nhưng frontmatter website
> **bắt buộc** có `readTime`. Cách xử lý đang dùng: đếm từ bằng công cụ (không ước lượng bằng
> mắt) rồi chia 220 từ/phút, làm tròn lên. Nếu website tự tính được readTime thì nên bỏ trường
> này khỏi frontmatter để tránh hai nguồn số liệu.

**Ánh xạ frontmatter với `output_schema.md`:** `title` ← Title · `excerpt` ← Excerpt ·
`tags` ← Tags · `subcategory` là field MỚI, chưa có trong output_schema. Các field Slug, Meta
Description, Category, Internal Links, References **không có chỗ trong frontmatter** — vẫn giữ
ở `.meta.json` cho n8n.

---

## 3. THƯ MỤC CHUYÊN MỤC (6 slug)

Ánh xạ giữa ba cách gọi đang tồn tại song song trong hệ thống:

| Số chủ đề (CLAUDE.md Bước 5.A) | Tên trong CORE_BRAIN | Tên trong backlog | **Slug thư mục website** |
|---|---|---|---|
| 1 | Sức khỏe | SỨC KHỎE - Hiểu cơ thể | `suc-khoe` |
| 2 | Tâm lý & đời sống | TÂM LÝ VÀ ĐỜI SỐNG - Hiểu tâm trí | `tam-ly-doi-song` |
| 3 | Dưỡng sinh | DƯỠNG SINH - Hiểu cách sống | `duong-sinh` |
| 4 | Triết lý phương Đông | TRIẾT LÝ SỐNG - Hiểu cuộc đời | `triet-ly-song` |
| 5 | Đồng hành tuổi già & người bệnh | ĐỒNG HÀNH TUỔI GIÀ VÀ NGƯỜI BỆNH | `dong-hanh` |
| 6 | Bếp An Nhiên | BẾP AN NHIÊN - Văn hóa bữa cơm Việt | `bep-an-nhien` |

> ⚠️ **Trụ 4 có ba tên khác nhau:** CORE_BRAIN gọi "Triết lý phương Đông", backlog gọi "Triết lý
> sống", website dùng slug `triet-ly-song`. Không phải lỗi chặn vận hành, nhưng nên chốt một tên
> hiển thị để field `Category` ở `output_schema.md` không lệch với chuyên mục thật trên web.

---

## 4. MỤC CON (subcategory)

**Quy tắc sinh slug** (suy từ ví dụ `Cảm xúc & Nội tâm` → `cam-xuc-noi-tam`): bỏ dấu tiếng Việt,
bỏ ký tự `&`, chuyển về chữ thường, nối các chữ bằng dấu gạch nối. Bỏ luôn emoji đứng đầu.

> ⚠️ Slug bên dưới do **suy ra theo quy tắc trên**, chưa đối chiếu với danh sách gốc trong
> `huong-dan-dang-bai-seo.md`. Trước khi đăng loạt bài đầu tiên, đối chiếu lại một lượt — sai slug
> thì bài rơi sai mục con.

Hướng dẫn của Claude website nói có **78 slug (13 × 6)**. Danh sách dưới đây trích từ backlog:

> ⚠️ **Lệch số cần làm rõ:** đếm thực tế trong `bai-seo-dang-website-Anh-Minh.md` ra **76** mục
> con, không phải 78 — vì chuyên mục **Tâm lý & Đời sống chỉ có 11 mục con**, các chuyên mục còn
> lại 13. Cần biết website thật sự có 76 hay 78 mục, và nếu 78 thì 2 mục thừa ở Tâm lý tên là gì.

**1. Sức khỏe (13):** Tim mạch & Huyết áp · Giấc ngủ & Phục hồi · Dinh dưỡng & Chuyển hóa ·
Tiêu hóa & Đường ruột · Gan & Thanh lọc · Thận & Tiết niệu · Đường huyết & Tiểu đường ·
Xương khớp & Cơ bắp · Miễn dịch & Phòng bệnh · Mắt Tai Mũi Họng · Sức khỏe Nam nữ ·
Vận động & Phục hồi · Theo dõi sức khỏe tại nhà

**2. Tâm lý & Đời sống (11 — thiếu 2 so với hướng dẫn):** Cảm xúc & Nội tâm ·
Giao tiếp & Các mối quan hệ · Gia đình & Hôn nhân · Nuôi dạy con & Thế hệ · Phát triển bản thân ·
Stress Lo âu Bình an · Hạnh phúc & Biết ơn · Tuổi trung niên & Tuổi già · Công việc & Cuộc sống ·
Yêu bản thân & Chữa lành · Sống tối giản & Cân bằng

**3. Dưỡng sinh (13):** Nhịp sinh học & Đồng hồ cơ thể · Đi Đứng Ngồi Nằm · Hơi thở & Thư giãn ·
Dưỡng sinh mỗi ngày · Ăn uống theo dưỡng sinh · Theo mùa & Theo thời tiết · Âm dương & Cân bằng ·
Không gian sống & Phong cách sống · Thiên nhiên & Chữa lành · Dưỡng sinh theo từng độ tuổi ·
Thói quen nuôi dưỡng cơ thể · Tinh thần & Dưỡng tâm · Sống thuận tự nhiên

**4. Triết lý sống (13):** Thuận theo tự nhiên · Cân bằng trong cuộc sống · Thời gian & Vô thường ·
Buông bỏ & Chấp nhận · Đủ & Không tham cầu · Nghịch cảnh & Trưởng thành · Đối nhân xử thế ·
Trí tuệ sống · Tuổi già & Chiêm nghiệm · Sống chậm & Hiện tại · Quy luật của cuộc đời ·
Đức hạnh & Nhân cách · Một đời sống an nhiên

**5. Đồng hành (13):** Đồng hành tuổi già · Đồng hành với người bệnh · Người chăm sóc ·
Điều trị & Phục hồi · Hy vọng & Nghị lực · Chăm sóc giảm nhẹ · Cuộc sống sau điều trị ·
Những điều khó nói · Câu chuyện đồng hành · Sống trọn từng ngày · Đối diện mất mát ·
Gia đình & Yêu thương · Một hành trình không cô đơn

**6. Bếp An Nhiên (13):** Bữa cơm Việt mỗi ngày · Canh theo mùa · Món quê & Ký ức ·
Trà & Thức uống · Ăn theo mùa · Bữa cơm tuổi trung niên · Không gian bếp ·
Câu chuyện quanh mâm cơm · Thực phẩm tự nhiên · Bếp An Nhiên mỗi ngày ·
Gia vị Việt & Bí quyết bếp nhà · Quà từ căn bếp · Nơi bình yên bắt đầu

---

## 5. QUY TẮC THÂN BÀI (bổ sung cho `web_content_rules.md`)

- **KHÔNG viết H1 trong thân bài** — tiêu đề bài lấy từ frontmatter, website tự render H1. Viết
  thêm H1 sẽ thành hai tiêu đề chồng nhau.
- **Trích lời Anh Minh dùng blockquote.** Đây là **ngoại lệ có chủ đích** của quy tắc thuần chữ
  ở `web_content_rules.md` mục 3D: ký tự `>` là cú pháp MDX cho website, không phải ký tự trang
  trí. Xử lý ở bước bàn giao `.mdx`, KHÔNG đưa vào bản Body dành cho pipeline giọng đọc.
- Các quy tắc còn lại giữ nguyên theo `web_content_rules.md` và `seo_checklist.md`.

---

## 6. MỖI BÀI SEO LƯU 3 NƠI (cập nhật 05/08/2026 — người vận hành chốt)

Từ 05/08/2026, mỗi bài SEO viết xong phải xuất **hai bản**, lưu vào **ba nơi**:

| Bản | Nơi lưu | Định dạng | Dùng cho |
|---|---|---|---|
| **Bản giọng đọc** | Repo GitHub `nnphuong2016-arch/bai-viet-seo` (file `.md`) | Thuần chữ 100%, không ký tự định dạng nào (`web_content_rules.md` mục 3D) | Pipeline n8n đọc thành tiếng |
| **Bản giọng đọc** | Google Drive `Bai-viet-SEO` + `<tên bài>.meta.json` | Như trên | Drive Trigger kích hoạt n8n + chứa 8 field metadata |
| **Bản website** | Repo GitHub `nnphuong2016-arch/Bai-seo-web-MDX-anhminh` (file `.mdx`) | Có frontmatter 7 trường, có `##`/`###`, blockquote, link markdown | Đăng lên web |

**Cách làm để hai bản không bao giờ lệch chữ:** viết bản `.mdx` trước (bản đầy đủ định dạng),
rồi sinh bản `.md` bằng cách **gỡ lớp định dạng** khỏi chính file đó — bỏ frontmatter, bỏ `#`,
`>`, `**`, và đổi `[chữ neo](/url)` thành chữ neo trần. Không viết tay hai lần.

> ⚠️ **Câu hỏi chưa chốt (05/08/2026):** khi đã có `.md` trên GitHub thì Google Drive còn cần
> nữa không? Hiện **vẫn giữ Drive** vì n8n dùng Drive Trigger để kích hoạt pipeline giọng đọc, và
> `.meta.json` là nơi duy nhất chứa 8 field metadata (Title thẻ SEO, Slug, Meta Description,
> Excerpt, Category, Tags, Internal Links, References). Bỏ Drive thì phải đổi n8n sang đọc GitHub
> và tìm chỗ khác cho metadata trước. Cần chốt với Claude n8n.

### 6B. QUY CÁCH ĐẶT TÊN — HAI BẢN LUÔN TRÙNG TÊN (chốt 05/08/2026)

**Hai bản của cùng một bài phải mang ĐÚNG MỘT TÊN, chỉ khác thư mục và đuôi file** — để người
vận hành đối chiếu được bằng mắt, không phải dò.

```
<số chủ đề>.<STT trong chủ đề>.<slug có gạch nối>
```

| Bản | Repo | Ví dụ |
|---|---|---|
| Giọng đọc | `bai-viet-seo` | `1.1.vi-sao-ngu-du-tam-tieng-van-met.md` |
| Website | `Bai-seo-web-MDX-anhminh` | `1.1.vi-sao-ngu-du-tam-tieng-van-met.mdx` |

Số chủ đề theo bảng 6 trụ ở `CLAUDE.md` Bước 5.A. STT đếm trong phạm vi từng chủ đề (bài Tâm lý
đầu tiên là `2.1`, không phải `6`).

> **Lịch sử:** repo MDX ban đầu dùng `<STT>.<slugliềnkhônggạch>.mdx` (VD
> `1.visaongudutamtiengvanmet.mdx`). Đã đổi hết sang quy cách trên ngày 05/08/2026, vì kiểu cũ
> không có số chủ đề nên sẽ đụng số ngay khi sang chủ đề thứ hai.

> ⚠️ **Rủi ro còn lại — phải kiểm trước khi đăng loạt tiếp theo:** internal link trong bài đang
> trỏ dạng `/[category-slug]/[slug-có-gạch-nối]`, VD `/suc-khoe/vi-sao-ngu-du-tam-tieng-van-met`
> — tức **không có phần số** `1.1.` ở đầu. Nếu website sinh URL từ tên file thì URL thật sẽ là
> `/suc-khoe/1.1.vi-sao-ngu-du-tam-tieng-van-met` và mọi internal link sẽ 404. Bấm thử một link
> trên web để biết website lấy slug từ **tên file** hay từ một trường riêng; nếu lấy từ tên file
> thì phải thêm phần số vào link, hoặc bỏ phần số khỏi tên file.

---

## 7. CÒN THIẾU — CHECKLIST TRƯỚC KHI DÙNG FILE NÀY

- [ ] Danh sách trường frontmatter đầy đủ (mục 2).
- [ ] Danh sách slug mục con thật (mục 4) + làm rõ 76 hay 78.
- [ ] Link bài mẫu đã lên web để đối chiếu văn phong (hướng dẫn có nhắc, chưa nhận được link).
- [ ] Chốt tên hiển thị của trụ 4 (mục 3).
