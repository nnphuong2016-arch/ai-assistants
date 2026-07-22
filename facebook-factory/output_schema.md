# OUTPUT SCHEMA

Version: 2.0

## Đối tượng đầu ra

Mood: ...

Topic: ... (theo `topic_map.md`)

Pillar: ... (1 trong 6 trụ chính thức — xem `topic_map.md` mục "Cầu nối 6 trụ")

Framework: ...

Body: ...

Suggested Featured Image: ... (mô tả ngắn Ý TƯỞNG ảnh, KHÔNG phải prompt đầy đủ — nếu cần ảnh
thật, đưa nguyên câu này làm `hook` input cho Featured Image Factory, không tự viết prompt ở
đây, tránh trùng vai trò 2 Factory)

Internal Tags: ...

------------------------------------------------------------------------

## Interactive Mode (Custom GPT / Claude Project / Claude Code — người vận hành trực tiếp)

Trong cuộc trò chuyện: xuất dạng Markdown theo đúng field ở trên (đủ Mood/Topic/Pillar/
Framework/Body/Suggested Featured Image/Internal Tags), có thể kèm giải thích ngắn nếu người
dùng chủ động hỏi lý do chọn Framework/Mood — không tự thêm giải thích khi không được hỏi.

**Khi lưu file `.md` vào Drive (xem CLAUDE.md Bước 5F): CHỈ chứa nội dung `Body`** — không kèm
Mood/Topic/Pillar/Framework/Suggested Featured Image/Internal Tags vào file. Các field đó chỉ
để trao đổi trong lúc soạn, không phải nội dung xuất bản (giống quy tắc "pure content" của
SEO Factory ở Bước 5 CLAUDE.md).

------------------------------------------------------------------------

## Automation Mode (n8n / API)

Không hỏi lại. Không hội thoại. Không giải thích. Không thêm nhận xét.

Chỉ trả đúng Object:

```json
{
  "mood": "...",
  "topic": "...",
  "pillar": "...",
  "framework": "...",
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
-   Phù hợp để n8n, ChatGPT và Claude xử lý thống nhất.
