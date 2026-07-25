# OUTPUT SCHEMA

Version: 2.1
Cập nhật: 25/07/2026

## Đối tượng đầu ra

**Mood** — cảm xúc chính đã chọn ở STEP 6. Bắt buộc lấy đúng một tên trong danh sách
của `emotion_palette.md`, không tự đặt tên cảm xúc mới. Nếu có cảm xúc phụ, ghi sau dấu
gạch chéo (VD: `Đồng cảm / Bình yên`).

**Topic** — theo `topic_map.md`, đúng một Topic chính.

**Pillar** — 1 trong 6 trụ chính thức, tra bảng quy đổi ở `topic_map.md` mục
"Cầu nối 6 trụ".

**Framework** — mã framework đã dùng (F01–F11) theo `post_frameworks.md`.

**Hook Source** — ghi lại điểm vào đã dùng, để về sau tra cứu chống trùng:
- Hook từ kho: ghi mã `S<series>-<dòng>` (VD: `S1-16` = Series 1 dòng 16).
- Chủ đề do người vận hành đưa: ghi `Trực tiếp`.
- Tự sinh qua `idea_library.md`: ghi `Tự sinh`.

**Body** — toàn văn bài viết.

**Suggested Featured Image** — mô tả ngắn Ý TƯỞNG ảnh, KHÔNG phải prompt đầy đủ. Nếu cần
ảnh thật, đưa nguyên câu này làm `hook` input cho Featured Image Factory; không tự viết
prompt ở đây, tránh trùng vai trò hai Factory.

**Internal Tags** — 3 đến 5 tag để tra cứu nội bộ. Quy ước: chữ thường, không dấu, nối
bằng gạch nối, mỗi tag bắt đầu bằng `#`. VD: `#tuoi-gia #co-don #cham-soc`.
Đây là nhãn tra cứu thủ công cho người vận hành, KHÔNG phải hashtag đăng kèm bài, và
KHÔNG phải cơ chế để Factory tự học hay tự đổi hành vi.

------------------------------------------------------------------------

## Interactive Mode (Custom GPT / Claude Project / Claude Code — người vận hành trực tiếp)

Trong cuộc trò chuyện: xuất dạng Markdown theo đúng thứ tự field ở trên. Có thể kèm giải
thích ngắn nếu người dùng chủ động hỏi lý do chọn Framework/Mood — không tự thêm giải thích
khi không được hỏi.

**Khi lưu file `.md` vào Drive (xem CLAUDE.md Bước 5F): CHỈ chứa nội dung `Body`** — không
kèm Mood/Topic/Pillar/Framework/Hook Source/Suggested Featured Image/Internal Tags vào file.
Các field đó chỉ để trao đổi trong lúc soạn, không phải nội dung xuất bản (giống quy tắc
"pure content" của SEO Factory ở Bước 5 CLAUDE.md).

------------------------------------------------------------------------

## Automation Mode (n8n / API)

Không hỏi lại. Không hội thoại. Không giải thích. Không thêm nhận xét.

Nếu đầu vào chưa rõ, tự thu hẹp thành một ý theo `execution_flow.md` STEP 1 — không
trả về câu hỏi.

Chỉ trả đúng Object:

```json
{
  "mood": "...",
  "topic": "...",
  "pillar": "...",
  "framework": "...",
  "hook_source": "...",
  "body": "...",
  "suggested_featured_image": "...",
  "internal_tags": "..."
}
```

------------------------------------------------------------------------

## Quy định

-   Chỉ xuất đúng cấu trúc.
-   Không tự thêm trường mới.
-   Không đổi tên trường, không đổi thứ tự trường.
-   Mọi bài phải qua `quality_check.md` trước khi xuất theo khuôn này.
-   Phù hợp để n8n, ChatGPT và Claude xử lý thống nhất.
