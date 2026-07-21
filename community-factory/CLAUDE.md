# CLAUDE.md — COMMUNITY FACTORY (Facebook/X/Zalo — kênh "Chia sẻ điều đáng nhớ mỗi ngày")

> File nhắc việc riêng cho Community Factory, đặt trong chính thư mục này để mỗi lần mở cửa sổ
> làm việc ở đây, Claude tự đọc lại và không quên quy trình — không cần người dùng nhắc lại.
> File này KHÔNG thay thế `CLAUDE.md` gốc ở root repo (`ai-assistants/CLAUDE.md`) — đó vẫn là
> nguồn gốc duy nhất cho toàn hệ thống. File này chỉ là bản tóm tắt + checklist thao tác nhanh,
> chuyên riêng cho việc viết post/reply Facebook.

---

## 0. THỨ TỰ ĐỌC BẮT BUỘC TRƯỚC KHI VIẾT (không bỏ qua, không đảo thứ tự)

1. `core-brain/instructions.md` — danh tính Hiền triết Anh Minh, giọng nói, 5 trụ nội dung,
   ranh giới TUYỆT ĐỐI KHÔNG, checkpoint "móc neo ký ức" (mục 7: mỗi bài cần ít nhất 1 trong 3—
   ẩn dụ thiên nhiên mạnh / câu hỏi tự vấn / insight không hiển nhiên).
2. `bai-dang-Facebook-Anh-Minh.md` (gốc repo) — backlog RIÊNG của Community Factory (210 chủ đề,
   7 series × 30 bài: Có những.../Đôi khi.../Hóa ra.../Đừng vội.../Nếu hôm nay.../Điều đáng nghĩ
   hôm nay/Một phút nhìn lại). **KHÔNG dùng `hook_library_full.md`** (đã ngưng). **KHÔNG đọc
   chéo** backlog của SEO (`bai-seo-dang-website-Anh-Minh.md`) hay Video
   (`bai-video-dang-Youtube-Anh-Minh.md`) trừ khi người dùng chủ động đưa sang tham khảo.
3. Trong thư mục này, đọc theo đúng thứ tự:
   - `instructions_COMMUNITY.md` — vai trò & phạm vi (chỉ làm/không làm).
   - `community_rules.md` — tỷ lệ nội dung, giọng, ranh giới, CTA cho phép/cấm.
   - `social_templates.md` — chọn khuôn A–L phù hợp loại post.
   - `storytelling_patterns.md` — khuôn kể + 24 archetype (nếu post dạng câu chuyện).
   - `engagement_rules.md` — khi trả lời bình luận/tương tác thành viên.
   - `community_checklist.md` — tự kiểm bắt buộc trước khi xuất.
   - `output_schema.md` — đóng gói đúng field cho n8n.
4. `core-brain/channel_roles.md` — **bắt buộc**, để không lấn vai trò Website/YouTube khi cùng
   một chủ đề gốc (xem mục 2 bên dưới).
5. Khi cần: `core-brain/anh_minh_quotes.md` (câu chốt, dùng tiết chế), `core-brain/
   seasonal_calendar.md` (post theo mùa/dịp), `core-brain/dong_hanh_nguoi_benh.md` (bệnh/người
   già/mất mát), `core-brain/health_knowledge.md` (mục 9 — bảng Preferred/Allowed/Forbidden, nếu
   post chạm sức khỏe).

---

## 1. GHI NHỚ VAI TRÒ KÊNH — ĐỪNG QUÊN MỖI LẦN VIẾT

**Facebook/X/Zalo = kênh NÔNG NHẤT có chủ đích.** Một cảm xúc, một hình ảnh, một câu chốt —
KHÔNG giải thích nguyên nhân/cơ chế như bài SEO. Nếu post đang dài ra và bắt đầu giải thích
"vì sao"/"cơ chế" → đang lấn vai Website, phải cắt lại.

- Độ dài lý tưởng: **100–300 từ**. Cấu trúc: câu mở chạm ngay → thân ngắn 2–5 câu → 1 câu hỏi mở.
- Nếu chủ đề đã có bài SEO/video gần đây: **KHÔNG mở post bằng đúng câu hook đã dùng ở kênh
  kia** — kể lại theo khuôn khác (`storytelling_patterns.md`: quan sát/ký ức/câu hỏi mở...).
- Không copy nguyên một dòng trong backlog Facebook làm thẳng caption — luôn viết lại theo giọng.

---

## 2. RANH GIỚI TUYỆT ĐỐI (không có ngoại lệ, kể cả khi trả lời bình luận)

- Không dọa bệnh/giật gân/CAPS LOCK · không chẩn đoán/kê đơn/thay bác sĩ, **kể cả khi thành viên
  hỏi thẳng trong comment**.
- Không thần bí/mê tín/bói toán · không thao túng cảm xúc (tag người, bait nước mắt, FOMO) ·
  không toxic motivation · không sến/giả đạo lý · không tranh cãi chính trị.
- Mảng bệnh/mất mát/người già → theo đúng `core-brain/dong_hanh_nguoi_benh.md` — chỉ đồng hành
  cảm xúc, luôn đặt song song bác sĩ, không hứa hẹn khỏi bệnh.
- CTA chỉ dùng nhóm cho phép (Lưu lại/Chia sẻ/Theo dõi/Tham gia/Xem thêm) — **cấm tuyệt đối**:
  "Mua ngay", "Tag 3 người bạn", "Comment số 1", "Like nếu đồng ý", mọi kiểu tạo FOMO.
- Sản phẩm chỉ ~5% nội dung, giá trị ~95%.

---

## 3. TRƯỚC KHI XUẤT — CHẠY QUA `community_checklist.md`

Không xuất post/reply "tạm được rồi sửa sau" — post thường đăng gần như ngay lập tức, không có
bước soát lại thủ công sau. Đặc biệt kiểm:
- Một post = một ý chính, không gộp nhiều thông điệp.
- Không mở bài bằng cùng một mẫu câu như 2–3 post gần đây; không lặp archetype đã dùng gần đây.
- Có ít nhất 1 trong 3 "móc neo ký ức" (ẩn dụ mạnh / câu hỏi tự vấn / insight không hiển nhiên).
- Đúng field `output_schema.md`, đúng thứ tự, không thiếu.

---

## 4. PHẠM VI — KHÔNG TỰ LÀM VIỆC CỦA FACTORY KHÁC

- Không viết bài SEO/blog dài → việc của SEO Factory.
- Không viết kịch bản video, không tạo prompt ảnh/thumbnail → việc của Video/Image Factory.
- Nhận thấy nhiều thành viên hỏi cùng một vấn đề → **chỉ đề xuất** chủ đề cho SEO Factory
  (`engagement_rules.md` mục 5), không tự viết bài thay.

---

## 5. NƠI LƯU KẾT QUẢ

Post Facebook không phải bài SEO/kịch bản video nên **không áp dụng Bước 5 của `CLAUDE.md` gốc**
(không cần lưu vào repo `bai-viet-seo`/`kich-ban-video`, không cần đặt tên theo quy cách
`<số chủ đề>.<số thứ tự>.<slug>.md`). Trả kết quả trực tiếp cho người dùng theo khuôn
`output_schema.md`, trừ khi người dùng yêu cầu lưu file cụ thể.
