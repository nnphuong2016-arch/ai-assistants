# OUTPUT SCHEMA

Version: 4.0
Cập nhật: 17/10/2026

Đầu ra gồm **hai khối tách bạch**. Đừng nhét khối B vào khối A: n8n đọc nguyên văn mọi chữ trong file A (trừ dòng tiêu đề)
bằng giọng đọc máy.

------------------------------------------------------------------------

# KHỐI A — FILE KỊCH BẢN (đưa cho n8n)

**File Name** — `<chuỗi>.<thứ tự>.<slug-không-dấu>.md`:
- `<chuỗi>.<thứ tự>`: Short viết từ kho 210 hook → số hiệu = `<series>.<dòng>` của dòng đó (hai Short đầu: `1.1` =
  `S1-1`, `1.2` = `S1-2`). Short có chủ đề không lấy từ kho → chuỗi `0` (`0.1`, `0.2`…, số kế tiếp chưa dùng; n8n sẽ làm
  chúng trước hàng đợi của kho). Luôn tra thư mục Drive và `short_log.md` để không trùng số nào đang có; không gắn với số tập
  của video dài.
- `<slug>`: nói đúng ý chính của bài, chữ thường không dấu, chỉ gồm `a–z`, `0–9` và dấu gạch nối, không có dấu chấm, dài
  vừa phải (khoảng 40–70 ký tự). Phải khớp mẫu `^\d+\.\d+\..+\.md$` mà n8n dùng để nhận file.
- Ví dụ: `1.2.thay-doi-cua-co-the-dien-ra-rat-lau-truoc-khi-ta-nhan-ra.md`

**Body** — toàn văn file = dòng tiêu đề + lời đọc. Khuôn bắt buộc:
- **Dòng 1:** `# <Title>` — KHÔNG được đọc thành tiếng (n8n lấy làm tiêu đề YouTube và bỏ khỏi lời đọc). Dòng 2 để trống.
  Short từ kho: Title = đúng câu của dòng đó trong kho, bỏ dấu chấm cuối. Chủ đề khác: một câu tiêu đề cùng kiểu, dưới 90 ký tự
  (`writing_rules.md` mục 8A).
- Từ dòng 3: lời đọc, mỗi đoạn 1–3 câu ngắn, hai đoạn cách nhau **một dòng trống**.
- Ngoài dòng tiêu đề: không tiêu đề mục khác, không gạch đầu dòng, không chữ nghiêng, không ghi chú, không hashtag, không emoji.
- **Câu kết** (dòng cuối): mặc định là câu hỏi tự vấn in đậm `**…**`; có thể là kiểu kết khác (`writing_rules.md` mục 8) — khi đó
  viết thường, không in đậm. Được đọc thành tiếng. n8n bỏ các dấu `**`, `#`, `>`, `__` trước khi đọc nên dấu Markdown không bị
  đọc lên.
- Độ dài: một trong ba cỡ — Nhanh 30–45 giây, Tiêu chuẩn 45–90 giây, Kể chuyện 90–120 giây; **trần cứng 2100 ký tự (tối đa
  2 phút), không phải bài nào cũng dài** (`writing_rules.md` mục 6.1).

Khi lưu file `.md` vào Drive (CLAUDE.md mục 7): file CHỈ chứa `Body` (dòng tiêu đề + lời đọc).

------------------------------------------------------------------------

# KHỐI B — GÓI ĐĂNG VÀ NHẬT KÝ (cho người vận hành, KHÔNG vào file)

**Title** — nhắc lại tiêu đề YouTube (đã nằm ở dòng 1 của file). YouTube Shorts: tiêu đề = Title + `#Shorts`; mô tả = nguyên lời
đọc; thẻ cố định — n8n tự làm.

**Reel Caption** — chữ đăng kèm Reel: 1–2 câu ngắn gợi ý chính của video và một câu hỏi mở dễ trả lời, khác với câu kết của
video. Không hashtag dài, không lời kêu gọi rẻ tiền. (Dùng chung một video cho Reel và YouTube Shorts; chỉ tối ưu tiêu đề, caption
và mô tả theo từng nơi.)

**Mood** — cảm xúc chính, đúng một tên trong `emotion_palette.md` (phụ: sau dấu `/`).

**Topic** — theo `topic_map.md`, đúng một Topic chính.

**Pillar** — 1 trong 6 trụ chính thức, tra bảng "Cầu nối 6 trụ" ở `topic_map.md`.

**Framework** — mã F01–F16 theo `short_frameworks.md`.

**Hook Source** — `S<series>-<dòng>` (từ kho), `Trực tiếp` (người vận hành đưa) hoặc `Tự sinh` (idea_library).

**Hook Type** — tên TYPE câu mở đã dùng trong `hook_library.md` (VD: "Có những…", Ký ức chung, Hình ảnh).

**Ending Type** — Câu hỏi / Nhận ra / Hình ảnh / Lời nhắn / Khoảng lặng.

**Size** — Nhanh / Tiêu chuẩn / Kể chuyện, kèm số từ và số ký tự đã đếm.

**Log Row** — một dòng sẵn để dán vào bảng của `short_log.md`:
`| Mã | Topic / Góc | Khán giả · Mùa | Mood · Khung | Kiểu mở | Hình/ẩn dụ | Kiểu kết | Cỡ (giây) | Đăng | | |` (hai cột cuối — số
liệu và bài học — để trống, điền sau khi đăng). Kèm: nếu bài lấy từ kho thì nhắc người vận hành thêm mã `S<series>-<dòng>` vào
danh sách "Dòng kho đã làm" ở đầu `short_log.md`.

------------------------------------------------------------------------

## Interactive Mode (Custom GPT / Claude Project / Claude Code — người vận hành trực tiếp)

Trong cuộc trò chuyện, xuất theo thứ tự: **A** (File Name + Body trong MỘT khối code để copy nguyên), rồi **B** (mỗi field một
dòng; Log Row cuối cùng). Có thể kèm giải thích ngắn nếu người dùng chủ động hỏi lý do chọn khung/cảm xúc — không tự thêm giải
thích khi không được hỏi.

------------------------------------------------------------------------

## Automation Mode (n8n / API)

Không hỏi lại. Không hội thoại. Không giải thích. Không thêm nhận xét. Nếu đầu vào chưa rõ, tự thu hẹp thành một ý theo
`execution_flow.md` STEP 1 — không trả về câu hỏi.

Chỉ trả đúng Object:

```json
{
  "file_name": "...",
  "body": "...",
  "title": "...",
  "reel_caption": "...",
  "mood": "...",
  "topic": "...",
  "pillar": "...",
  "framework": "...",
  "hook_source": "...",
  "hook_type": "...",
  "ending_type": "...",
  "size": "...",
  "log_row": "..."
}
```

------------------------------------------------------------------------

## Quy định

-   Chỉ xuất đúng cấu trúc. Không tự thêm trường mới, không đổi tên trường, không đổi thứ tự trường.
-   Mọi bài phải qua `quality_check.md` (cả hai tầng) trước khi xuất theo khuôn này.
-   Phù hợp để n8n, ChatGPT và Claude xử lý thống nhất.
