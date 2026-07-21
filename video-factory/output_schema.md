# OUTPUT SCHEMA — CHUẨN ĐẦU RA VIDEO FACTORY

> Tải lên khu **Files** của Video Factory. Quy định khuôn xuất cuối cùng của mọi kịch bản — để
> n8n (hoặc bất kỳ pipeline nào đọc output) luôn nhận đúng field, đúng thứ tự. Theo đúng pattern
> đã dùng ở SEO/Image/Community/Publish/Research Factory (mỗi Factory có output_schema.md riêng).
> Cập nhật: 18/07/2026 — field Scenes chuẩn hoá theo Scene ID zero-padded (khớp `video_rules.md`
> mục 1.C), rõ Master Script không chứa prompt platform-specific.

---

## KHUÔN XUẤT CHUẨN

1. **Video Title** — tên video + 1 câu ý chính (theo `video_rules.md` mục 1.A).
2. **Format** — NGẮN / TRUNG / DÀI (theo khung định dạng `video_rules.md` mục 2).
3. **Duration** — thời lượng mục tiêu (VD: 90 giây, 4 phút, 10 phút).
4. **Hook** — câu/hình mở đầu 3 giây. Nếu video chuyển đổi từ bài SEO có sẵn, **dùng nguyên
   hook bài đó đã dùng** (không tự chọn hook khác); nếu viết độc lập, ghi rõ nguồn hook (VD:
   "Hook #12, trụ Dưỡng sinh — từ Sheet dùng chung", xem `project-memory/hook_library_full.md`
   để biết bối cảnh chuyển đổi từ file này sang Sheet).
5. **Voice** — toàn văn lời dẫn (LỜI), viết liền mạch theo khuôn xuất kịch bản (`video_rules.md`
   mục 1/4 tùy độ dài) — đây là lớp mang độ dài và giá trị của video. Bằng đúng nội dung ghép nối
   các field Voice trong Scenes theo thứ tự Scene ID; dùng để đọc liền mạch/kiểm tra tổng thể,
   không thay thế Scenes.
6. **Scenes** — danh sách cảnh theo đúng khuôn field ở `video_rules.md` mục 1.C. Mỗi cảnh gồm:
   **Scene ID** (zero-padded 3 chữ số, VD `001`), **Duration** (giây), **Voice** (đoạn lời dẫn
   tiếng Việt của cảnh đó), **Visual** (bối cảnh + chủ thể + hành động, tiếng Anh), **Camera**
   (loại cảnh + chuyển động máy + ánh sáng + âm thanh nền, tiếng Anh), **Character** (tên nhân
   vật nếu có, tham chiếu `core-brain/image_style_bible.md` — để trống nếu B-roll trung tính),
   **Emotion** (tâm trạng chủ đạo của cảnh), **Loop** (`true`/`false`).

   ⚠️ Đây là **Master Script** — nguồn dữ liệu gốc, KHÔNG chứa prompt platform-specific
   (Kling/Veo3/Sora/Hailuo...) và KHÔNG mô tả khuôn mặt/trang phục nhân vật trong Visual/Camera
   (nhận diện nhân vật do field Character đảm nhiệm). Prompt cho từng công cụ AI cụ thể được
   build ở bước RIÊNG, SAU khi Master Script này hoàn tất — thủ công (đưa lại Master Script cho
   Claude, yêu cầu "chuyển thành prompt Kling/Veo3") hoặc tự động (node Scene Generator trong
   n8n, xem `video_ai_contract.md`). Nhờ vậy khi đổi/thêm công cụ AI, chỉ cần sửa bước build
   prompt, không phải viết lại Master Script.
7. **Character Reference** — `true`/`false`: cảnh nào có nhân vật chính xuất hiện, tham chiếu
   `core-brain/image_style_bible.md` — để trống nếu toàn bộ video chỉ có B-roll trung tính.
8. **Suggested Thumbnail** — mô tả ý tưởng thumbnail (không phải ảnh thật) theo mục 8
   `video_rules.md` — để Image Factory hoặc bước sau tạo ảnh thật.
9. **Music** — gợi ý nhạc nền theo `core-brain/image_style_bible.md` mục 11 (piano tối giản,
   ambient) — để trống nếu dùng nhạc mặc định của kênh.
10. **Structure Used** — cấu trúc kịch bản đã dùng (A–E theo `video_rules.md` mục 7), để hỗ trợ
    chống lặp khi tra Production Memory (xem ghi chú cuối file).
11. **Metadata** — Category (trụ nội dung), Season (nếu gắn mùa, theo `seasonal_calendar.md`),
    Audience (đối tượng hướng tới).
12. **Tags** — 3–6 tag liên quan chủ đề, dùng cho tìm kiếm nội bộ trên nền tảng đăng.

---

## QUY TẮC ĐÓNG GÓI

- Field không áp dụng (VD: Music khi dùng nhạc mặc định) → để trống, không xóa field khỏi khuôn.
- Không tự thêm field ngoài danh sách dù thấy hữu ích — đề xuất riêng, không chèn vào khuôn xuất.
- Mỗi kịch bản phải theo đúng `video_rules.md` trước khi xuất theo khuôn này.

**Production Memory (khi vận hành qua n8n):** Hook, Structure Used, Scenes lặp lại (VD: cùng
Hook #27, cùng Cấu trúc D, cùng cảnh "Garden") nên được đối chiếu với lịch sử sản xuất gần đây
(bảng `video_production_log` — xem `funamark-master-blueprint-v2.md` Phần D, WF-07) trước khi
chọn, để tránh lặp quá gần nhau khi sản xuất hàng trăm video. Ở chế độ chat thủ công (không qua
n8n), Video Factory chỉ dựa vào ngữ cảnh cuộc trò chuyện hiện tại để chống lặp (không có bộ nhớ
dài hạn) — đây là giới hạn đã biết, không phải lỗi.
