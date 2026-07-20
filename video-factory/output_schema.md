# OUTPUT SCHEMA — CHUẨN ĐẦU RA VIDEO FACTORY

> Tải lên khu **Files** của Video Factory. Quy định khuôn xuất cuối cùng của mọi kịch bản — để
> n8n (hoặc bất kỳ pipeline nào đọc output) luôn nhận đúng field, đúng thứ tự. Theo đúng pattern
> đã dùng ở SEO/Image/Community/Publish/Research Factory (mỗi Factory có output_schema.md riêng).
> Cập nhật: 05/07/2026.
> Cập nhật: 20/07/2026 — thêm field 2 "Content Track" (Giải Đáp / Dưỡng Sinh Ngắn / Bếp An
> Nhiên / Suy Ngẫm), field còn lại đánh số lại theo đó.

---

## KHUÔN XUẤT CHUẨN

1. **Video Title** — tên video + 1 câu ý chính (theo `video_rules.md` mục 1.A).
2. **Content Track** — `Giải Đáp` (Nhánh A, câu hỏi "Tại sao" cho YouTube) / `Dưỡng Sinh Ngắn`
   (Nhánh B, thị phạm động tác cho TikTok/Reels/Shorts, theo `duong_sinh_bai_tap.md`) /
   `Bếp An Nhiên` (theo `bep_an_nhien.md`) / `Suy Ngẫm` (video ngắn insight thường, không thuộc
   3 track trên) — xem `instructions_VIDEO.md` mục 1B. Quyết định track TRƯỚC khi chọn Format.
3. **Format** — NGẮN / TRUNG / DÀI (theo khung định dạng `video_rules.md` mục 2).
4. **Duration** — thời lượng mục tiêu (VD: 90 giây, 4 phút, 10 phút).
5. **Hook** — câu/hình mở đầu 3 giây. Nếu video chuyển đổi từ bài SEO có sẵn, **dùng nguyên
   hook bài đó đã dùng** (không tự chọn hook khác); nếu viết độc lập (Nhánh A), ghi rõ nguồn
   (VD: "Dòng #12, `bai-video-dang-Youtube-Anh-Minh.md`" hoặc "Google Drive/Sheet, mục X" nếu
   lấy từ nguồn ngoài — KHÔNG còn dùng `hook_library_full.md`, xem `CLAUDE.md` Bước 2). Với
   Content Track `Dưỡng Sinh Ngắn`, Hook ghi tên động tác nguồn từ `bai_tap_library.md` thay vì
   dòng backlog.
6. **Voice** — toàn văn lời dẫn (LỜI), viết liền mạch theo khuôn xuất kịch bản (`video_rules.md`
   mục 1/4 tùy độ dài) — đây là lớp mang độ dài và giá trị của video.
7. **Scenes** — shot list B-roll (HÌNH), đánh số cảnh, mỗi cảnh gồm mô tả cảnh + đánh dấu
   cảnh nào dùng lại/loop được (theo `video_rules.md` mục 0/1).
8. **Character Reference** — `true`/`false`: cảnh nào có nhân vật chính xuất hiện, tham chiếu
   `core-brain/image_style_bible.md` — để trống nếu toàn bộ video chỉ có B-roll trung tính.
9. **Suggested Thumbnail** — mô tả ý tưởng thumbnail (không phải ảnh thật) theo mục 8
   `video_rules.md` — để Image Factory hoặc bước sau tạo ảnh thật.
10. **Music** — gợi ý nhạc nền theo `core-brain/image_style_bible.md` mục 11 (piano tối giản,
    ambient) — để trống nếu dùng nhạc mặc định của kênh.
11. **Structure Used** — cấu trúc kịch bản đã dùng (A–E theo `video_rules.md` mục 7); để trống
    nếu Content Track là `Dưỡng Sinh Ngắn` (dùng khung riêng ở `duong_sinh_bai_tap.md` mục 5,
    không phải cấu trúc kể chuyện A–E) — để hỗ trợ chống lặp khi tra Production Memory (xem ghi
    chú cuối file).
12. **Metadata** — Category (trụ nội dung), Season (nếu gắn mùa, theo `seasonal_calendar.md`),
    Audience (đối tượng hướng tới).
13. **Tags** — 3–6 tag liên quan chủ đề, dùng cho tìm kiếm nội bộ trên nền tảng đăng.

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
