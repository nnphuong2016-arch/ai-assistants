# OUTPUT SCHEMA

Version: 3.1
Cập nhật: 17/10/2026

## Đối tượng đầu ra

**Mood** — cảm xúc chính đã chọn ở STEP 6. Bắt buộc lấy đúng một tên trong danh sách của `emotion_palette.md`,
không tự đặt tên cảm xúc mới. Nếu có cảm xúc phụ, ghi sau dấu gạch chéo (VD: `Đồng cảm / Bình yên`).

**Topic** — theo `topic_map.md`, đúng một Topic chính.

**Pillar** — 1 trong 6 trụ chính thức, tra bảng quy đổi ở `topic_map.md` mục "Cầu nối 6 trụ".

**Framework** — mã framework đã dùng (F01–F10) theo `short_frameworks.md`.

**Hook Source** — ghi lại điểm vào đã dùng, để về sau tra cứu chống trùng:
- Dòng từ kho 210 hook: ghi mã `S<series>-<dòng>` (VD: `S1-1` = Series 1 dòng 1).
- Chủ đề do người vận hành đưa: ghi `Trực tiếp`.
- Tự sinh qua `idea_library.md`: ghi `Tự sinh`.

**Reel Caption** — chữ đăng kèm Reel (chỉ để người vận hành copy, KHÔNG vào file): 1–2 câu ngắn gợi ý chính của video và
một câu hỏi mở dễ trả lời, khác với câu hỏi cuối video. Không hashtag dài, không lời kêu gọi rẻ tiền. YouTube Shorts đã có
tiêu đề/mô tả tự động từ file nên không cần field riêng.

**File Name** — `<chuỗi>.<thứ tự>.<slug-không-dấu>.md`:
- `<chuỗi>.<thứ tự>`: Short viết từ kho 210 hook → số hiệu = `<series>.<dòng>` của dòng đó (hai Short đầu: `1.1` =
  `S1-1`, `1.2` = `S1-2`). Short có chủ đề không lấy từ kho → chuỗi `0` (`0.1`, `0.2`…, số kế tiếp chưa dùng; n8n sẽ làm
  chúng trước hàng đợi của kho). Luôn liệt kê thư mục (kể cả file mang tiền tố `DONE_`/`SHORTDONE_`/`LOI_`) để không
  trùng số nào đang có; không gắn với số tập của video dài.
- `<slug>`: nói đúng ý chính của bài, chữ thường không dấu, chỉ gồm `a–z`, `0–9` và dấu gạch nối, không có dấu
  chấm, dài vừa phải (khoảng 40–70 ký tự). Phải khớp mẫu `^\d+\.\d+\..+\.md$` mà n8n dùng để nhận file.
- Ví dụ: `1.2.thay-doi-cua-co-the-dien-ra-rat-lau-truoc-khi-ta-nhan-ra.md`

**Body** — toàn văn kịch bản = toàn bộ lời đọc. Khuôn bắt buộc:
- Mỗi đoạn 1–2 câu ngắn, hai đoạn cách nhau **một dòng trống**.
- Không tiêu đề mục, không gạch đầu dòng, không chữ nghiêng, không ghi chú, không hashtag, không emoji.
- **Dòng cuối cùng** là câu hỏi tự vấn in đậm `**…**` (dưới 80 ký tự) — n8n dùng nó làm tiêu đề YouTube.
- Độ dài: mục tiêu 150–200 từ, trần 1400 ký tự (`writing_rules.md` mục 6.1).

------------------------------------------------------------------------

## Interactive Mode (Custom GPT / Claude Project / Claude Code — người vận hành trực tiếp)

Trong cuộc trò chuyện: xuất theo thứ tự — `File Name`, `Body`, rồi các field nội bộ (Mood, Topic, Pillar,
Framework, Hook Source, Reel Caption) ghi gọn một dòng mỗi field (Reel Caption đặt cuối cùng). Có thể kèm giải thích ngắn nếu người dùng chủ động hỏi lý do
chọn Framework/Mood — không tự thêm giải thích khi không được hỏi.

**Khi lưu file `.md` vào Drive (xem CLAUDE.md mục 7): CHỈ chứa nội dung `Body`** — không kèm
Mood/Topic/Pillar/Framework/Hook Source/Reel Caption/File Name vào file. Các field đó chỉ để trao đổi trong lúc soạn, không phải
lời đọc (nếu lọt vào file, giọng đọc sẽ đọc luôn).

------------------------------------------------------------------------

## Automation Mode (n8n / API)

Không hỏi lại. Không hội thoại. Không giải thích. Không thêm nhận xét.

Nếu đầu vào chưa rõ, tự thu hẹp thành một ý theo `execution_flow.md` STEP 1 — không trả về câu hỏi.

Chỉ trả đúng Object:

```json
{
  "mood": "...",
  "topic": "...",
  "pillar": "...",
  "framework": "...",
  "hook_source": "...",
  "reel_caption": "...",
  "file_name": "...",
  "body": "..."
}
```

------------------------------------------------------------------------

## Quy định

-   Chỉ xuất đúng cấu trúc.
-   Không tự thêm trường mới.
-   Không đổi tên trường, không đổi thứ tự trường.
-   Mọi bài phải qua `quality_check.md` trước khi xuất theo khuôn này.
-   Phù hợp để n8n, ChatGPT và Claude xử lý thống nhất.
