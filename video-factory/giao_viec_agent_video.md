# Hướng dẫn giao việc cho agent con — viết / sửa kịch bản video (Nhánh A, kênh Anh Minh)

> Tạo 25/11/2026 theo yêu cầu người vận hành. Phiên chính LUÔN dùng file này khi giao việc, để
> agent con có cùng một bộ quy tắc và người vận hành không phải nhắc lại. Tham chiếu từ
> `CLAUDE.md` Bước 3.5.

## 1. Quy tắc điều phối (phiên chính)

- **MỖI TẬP = ĐÚNG MỘT AGENT CON, chạy TUẦN TỰ từng tập** (foreground). Xong tập nào → phiên chính
  tự đọc lại và biên tập tập đó → rồi mới giao tập kế. KHÔNG chạy nhiều agent song song, KHÔNG nhờ
  một agent viết nhiều tập. Áp dụng cả khi **sửa lại** tập theo góp ý (mỗi tập sửa một agent).
- Khi người vận hành nói "viết tiếp N bài" mà không chỉ định: lấy **N dòng backlog kế tiếp**
  trong `bai-video-dang-Youtube-Anh-Minh.md`, ngay sau tập có số lớn nhất đang có trong repo
  `Youtube---Anh-Minh/kich-ban-video/`. Số tập = số dòng backlog (Series 01 → `1.<dòng>`, Series 02
  → `2.<dòng>`, ... đúng bảng số chủ đề ở `CLAUDE.md` Bước 5.A). Báo lại cho người vận hành danh
  sách tập sẽ viết trước khi bắt đầu.
- Prompt giao việc ngắn gọn, **trỏ tới file này** + nêu: số tập, dòng backlog, hook, "lưu ý riêng
  của tập" (xem mục 5). Không cần dán lại toàn bộ quy tắc.
- Giao tuần tự, mỗi lần nhắc agent: chỉ làm tập của mình, không đụng tập khác, không chạy git.
- Sau khi agent trả về, phiên chính: (a) đọc lại toàn bộ VOICE bằng mắt biên tập viên, đặc biệt
  đoạn giới hạn/cấp cứu; (b) chạy kiểm tự động mục 4; (c) sửa tại chỗ; (d) sang tập kế.
- Cuối đợt: `git add` đích danh từng file, commit, push `master` repo `Youtube---Anh-Minh`, xác
  nhận `git rev-list --count HEAD..origin/master` = 0 (Bước 5.B), rồi **báo giờ commit (giờ VN) +
  danh sách file đã đổi** để người vận hành biết cần copy sang Drive những file nào. Nhắc rõ: mỗi
  lần đẩy bản mới, bản trên Drive cũ hơn phải được thay lại.

## 2. Agent con phải đọc trước khi viết (không rút gọn)

Trong repo `ai-assistants`: `CLAUDE.md` (Bước 3.5, 4, 5.B), `core-brain/instructions.md`,
`core-brain/health_knowledge.md` (mục 9: bảng Preferred/Allowed/Forbidden — cấm cortisol,
melatonin, hormone, endorphin, dopamine, insulin, đường huyết, collagen, tế bào, miễn dịch, đề
kháng…), `core-brain/dong_hanh_nguoi_benh.md`, `core-brain/image_style_bible.md`,
`video-factory/instructions_VIDEO.md`, `video-factory/video_rules.md` (mục 0, 1.C, 2, 3, 6C, 7, 8),
`video-factory/output_schema.md`, `video-factory/examples_and_hooks.md`. Rồi đọc 3–4 tập mẫu gần
nhất trong `/home/user/youtube---anh-minh/kich-ban-video/` (cả `_master_script.md` lẫn `_prompts.md`).

## 3. Quy tắc cứng

1. Kênh chạy **Cách 2**: `_prompts.md` CHỈ gồm 2 khối "A. QUICK COPY" (Title 3 phương án,
   Description, SEO Keywords, Tags, Hashtag) và "B. PROMPT THUMBNAIL". KHÔNG có scene-prompt Clip AI/Ảnh giữ.
   Không để ghi chú nội bộ trong ô Title/Description (sẽ bị dán thẳng lúc đăng).
2. **NGẮN 3–5 phút DUY NHẤT**, tốc độ đọc thật ~250 từ/phút. Đếm từ bằng Python
   `len(text.split())` (KHÔNG `wc -w`). THÂN (không gồm outro) 750–1030 từ; tổng cả outro < 4:40,
   PHẢI > 3:00. 9 scene (hoặc 8–9).
3. Khuôn master_script y hệt tập mẫu: dòng đầu `**Video Title:** ...` đứng MỘT MÌNH một dòng sạch;
   Ý chính, Câu hứa, Content Track: Giải Đáp, Format, Duration mục tiêu, Hook nguồn, Structure
   Used, Character Reference: true, Music, Suggested Thumbnail, Metadata, Tags; `## VOICE` liền
   mạch; `### Scene 001..` với Scene ID, Duration, Voice, Shots, Visual, Camera, Character,
   Emotion, Loop. Scene 001 = HOOK, áp chót = KẾT, cuối = OUTRO CỐ ĐỊNH. **VOICE phải khớp từng chữ
   với phần Voice ghép từ các scene.**
4. **OUTRO CỐ ĐỊNH** (cuối VOICE + scene cuối), chép 100% nguyên văn:

   ```
   Cảm ơn bạn đã ngồi lại cùng Anh Minh đến những phút cuối của video.

   Nếu những chia sẻ hôm nay mang đến cho bạn một suy nghĩ mới, một chút bình yên hay chỉ là một lời nhắc nhẹ nhàng dành cho chính mình, hãy đăng ký kênh để chúng ta tiếp tục đồng hành trên hành trình này.

   Cuộc sống không phải lúc nào cũng dễ dàng. Nhưng chỉ cần mỗi ngày hiểu mình hơn một chút, lòng sẽ nhẹ hơn một chút.

   Hẹn gặp lại bạn trong video tiếp theo.
   ```
5. Tên file: `<số chủ đề>.<dòng backlog>. <Video Title bỏ \ / : * ? " < > |>_master_script.md` và
   `..._prompts.md`, lưu thẳng vào `/home/user/youtube---anh-minh/kich-ban-video/`. Video Title tự
   đặt, ngắn (≤ ~10 từ), khớp nội dung thật, KHÔNG copy nguyên dòng backlog. Agent con KHÔNG chạy git.
6. Không URL/tên tổ chức trong lời thoại. Không thần bí. Anh Minh là nhân vật AI, không kể như có
   trải nghiệm y khoa/cá nhân thật.

## 4. Khung an toàn bắt buộc + bài học từ các đợt góp ý (1.25–2.5)

**3 mức hành động — mỗi mức một câu riêng, rõ, trung tính, không dọa, KHÔNG mốc ngày/ngưỡng số cứng, không chẩn đoán:**
1. **Cấp cứu/khẩn:** triệu chứng đột ngột, nặng, tăng nhanh, dấu hiệu thần kinh, đau ngực/khó thở rõ,
   ngất, màn che thị lực, ý nghĩ tự làm hại… → nhờ người thân ở cạnh và liên hệ cấp cứu/cơ sở y tế
   khẩn/đường dây hỗ trợ khủng hoảng ở nơi mình sống NGAY. Không bao giờ "ngồi nghỉ xem có qua không".
2. **Khám sớm:** kéo dài, tái diễn, nặng dần, ảnh hưởng sinh hoạt → hẹn bác sĩ/chuyên gia.
3. **Tự chăm sóc nhẹ:** chỉ khi thoáng qua, không dấu hiệu nguy hiểm, người xem thấy ổn.
Không để một mẹo lối sống đứng sát cảnh báo theo kiểu "thử mẹo trước". Đoạn giới hạn là
scene/đoạn RIÊNG, đặt sau phần giải thích chính; nhắc không tự ý ngưng/đổi thuốc khi chạm bệnh nền.

**Bài học (đã bị góp ý — đừng lặp lại):**
- Kiến thức đúng nằm trong phần giải thích chính bằng lời thường, TRƯỚC khi khép bằng cảm xúc.
- **Tối đa MỘT ẩn dụ/tập** (≤ ~15% thân), nói rõ chỉ là minh họa; không thay cơ chế; chống lặp ẩn dụ
  đã dùng (grep thư mục kịch bản trước khi chọn).
- Không khẳng định tuyệt đối/trấn an gộp: tránh "ai cũng", "chắc chắn", "luôn luôn", "không đáng
  lo", "không cần thuốc", "vết thương nào rồi cũng lành". Dùng "thường", "có thể", "nhiều người".
- Không hướng dẫn điều trị/chăm sóc y khoa cụ thể (→ hỏi bác sĩ/dược sĩ); không hứa kết quả; gợi ý
  là linh hoạt, mỗi người khác nhau.
- Không phán đoán tâm lý người xem; không nhân hóa cơ thể ("cơ thể không thích/đang trách"); không
  dùng "cơ thể dồn hết năng lượng cho X" làm cơ chế chính; không nâng lời giải thích đơn giản thành "quy luật".
- Không mốc tuổi chung cho mọi người; không đảo ngược định kiến bằng công thức máy móc; không chê/so
  sánh người yếu, người bệnh, người lớn tuổi.
- Mở cửa/đi ra ngoài/vận động… phải kèm điều kiện ngoại lệ (không khí xấu, thời tiết, bệnh nền).
- Câu hứa không vượt quá nội dung; Ý chính/Câu hứa/Description/thumbnail khớp VOICE cuối.
- Phải có ≥1 "móc neo ký ức" (ẩn dụ thiên nhiên / câu hỏi tự vấn / insight không hiển nhiên) và một
  hành động nhỏ cụ thể ở cuối.
- Thumbnail: Anh Minh đúng ngoại hình `image_style_bible.md`, cinematic wellness, không CAPS/giật
  gân/bệnh viện/vết thương/chữ Hán/số đọc được; cảnh minh họa không mâu thuẫn lời thoại.

**Bài học đợt góp ý 1.46–2.5 (26/11/2026 — Gemini + một bản góp ý độc lập; đừng lặp lại):**
- **Chống "khuôn lắp ráp" giữa các tập.** 10 tập viết liền nhau từng dùng chung một công thức: câu dẫn
  ẩn dụ ("Có một hình ảnh giúp dễ nhớ, nhưng chỉ là minh họa thôi" + chốt "hình ảnh ấy chỉ để... phức
  tạp hơn nhiều") và đoạn kết Scene 008 ("Nếu muốn thử một điều thật nhỏ... Không cần hoàn hảo... Có
  một điều ít khi ta để ý... Anh Minh xin để lại một câu hỏi"). Mỗi tập phải dẫn ẩn dụ và kết bài bằng
  cách RIÊNG; trước khi viết, agent grep/đọc Scene 007–008 của các tập đã có trong thư mục để chọn cách
  mở/kết khác tất cả. Vẫn nói rõ ẩn dụ chỉ là minh họa. Cụm "mỗi người một khác" tối đa 2 lần/tập.
- **Scene 008 phải `Loop: false`** (chỉ Scene 009 outro `Loop: true`). Tổng Duration các scene phải
  BẰNG "Duration mục tiêu" ghi ở đầu file; đổi số từ thì sửa lại cả hai. Phiên chính kiểm bằng Python.
- **Sửa theo góp ý không được sinh lỗi mới:** đã xảy ra (2.2) agent viết lại Scene 008 bằng một ẩn dụ
  THỨ HAI có nhân cách hóa ("câu tự trách gõ cửa, như khách quen ghé muộn"). Khi dặn agent viết lại cảnh
  kết, nói rõ: không thêm ẩn dụ, không nhân cách hóa, dùng một việc nhỏ cụ thể hoặc một câu hỏi.
- **Tiêu đề không được đặt cảm nhận chủ quan đối lập/cao hơn tư vấn chuyên môn** (VD "lắng nghe cơ thể
  quan trọng hơn chạy theo lời khuyên" → đổi thành "Giữa nhiều lời khuyên, lắng nghe cơ thể thế nào cho
  đúng"); không đặt một hiệu ứng tâm lý thành quy luật trong tiêu đề ("càng cố quên càng nhớ" → "Vì sao
  có lúc chuyện cũ quay lại khi ta cố gạt đi"). Đổi tiêu đề = đổi cả Video Title, tên 2 file, Quick Copy,
  Filename thumbnail. Ý nghĩ bám theo backlog vẫn giữ ở "Hook nguồn".
- **Dấu hiệu cấp cứu không đặt điều kiện thừa:** sốc nhiệt có thể da khô HOẶC ẩm/đổ mồ hôi — chỉ nêu lú
  lẫn, nói năng lạ, ngất/co giật, cơ thể rất nóng. Không dùng "da nóng mà khô" như điều kiện.
- **Mẹo chăm sóc phải kèm điều kiện:** súc miệng nước sạch KHÔNG thay chải răng + làm sạch kẽ răng; không
  lấy "bớt khẩu phần/bỏ bữa" làm ví dụ cho người nghe nói chung; ghi chép triệu chứng để hỏi bác sĩ, không
  để tự chẩn đoán/tự loại thực phẩm hay thuốc; "khi không có cảm giác gì" nói là "một số vấn đề chỉ được
  phát hiện qua thăm khám phù hợp", không gợi lo bệnh âm thầm.
- **Tâm lý — giảm quy luật, mở lối an toàn:** dùng "đôi khi / một số người / có lúc"; một lời giải thích
  chỉ là MỘT khả năng (tự trách không phải lúc nào cũng chứng tỏ quan tâm; nước mắt không có một ý nghĩa
  chung; trống trải sau thành công còn có thể đi cùng mệt mỏi, mất mát, cô đơn, sức khỏe, tâm trạng);
  các cách tự làm nhẹ phải kèm "chỉ chọn cách bạn thấy an toàn, có thể dừng, tìm người hỗ trợ"; lời
  khuyên chia sẻ phải kèm "chỉ khi thấy an toàn"; chuyên gia là người cùng hiểu và hỗ trợ, không chỉ "người
  nghe". Tránh "tự đánh mình" (dễ hiểu là đánh thể xác) — dùng "tự dằn vặt/tự hạ thấp mình".
- Visual/Camera của scene phải bám lời thoại của chính scene đó (Scene 001 minh họa đúng hook, không
  chỉ đổi bối cảnh chung chung).

**Kiểm tự động phiên chính phải chạy sau mỗi tập (Python):** outro xuất hiện đúng 2 lần nguyên văn;
VOICE (bỏ dòng tiêu đề `## VOICE`) khớp từng chữ với Voice ghép từ các scene; thân/tổng từ trong khoảng; tổng Duration
các scene BẰNG "Duration mục tiêu"; `Loop` Scene 008 = false; không từ cấm mục 9; `_prompts.md` chỉ có Quick Copy + Thumbnail, không rò ghi chú nội bộ.

## 5. "Lưu ý riêng của tập" — phiên chính viết vào prompt từng agent

Nêu: góc hẹp khuyến nghị; tập lân cận cần tránh trùng; dấu hiệu giới hạn riêng của chủ đề (3 mức
ở mục 4). Theo nhóm chủ đề:

- **Sức khỏe (Series 01):** chỉ mức lối sống phổ thông; không số liệu thống kê/chỉ số; không chẩn đoán;
  người có bệnh nền/đang dùng thuốc → hỏi bác sĩ.
- **Tâm lý & cảm xúc (Series 02):** KHÔNG toxic positivity ("hãy luôn tích cực"), không ép phải vui/
  mạnh mẽ, không tuyên bố "chữa trầm cảm/lo âu", không gọi tên rối loạn để chẩn đoán, không sến/giả
  đạo lý. Cho phép nói "có những ngày không ổn vẫn bình thường". Giới hạn riêng (tách đoạn riêng):
  buồn/mất hứng thú/mệt/mất ngủ kéo dài ảnh hưởng sinh hoạt → gặp bác sĩ/chuyên gia sức khỏe tinh
  thần sớm; có ý nghĩ/ý định làm hại bản thân hoặc không thấy an toàn → đừng ở một mình, gọi người
  tin cậy đến ở cạnh, liên hệ NGAY số cấp cứu hoặc đường dây hỗ trợ khủng hoảng ở nơi mình sống
  (không nêu số điện thoại cụ thể). Giọng ấm, không phán xét.
- **Dưỡng sinh / Tuổi già / Đồng hành:** theo `dong_hanh_nguoi_benh.md` (không tư vấn bệnh, không hứa
  hẹn, luôn song song bác sĩ; tôn trọng phẩm giá; có lời nhắn cho người chăm sóc khi hợp).

## 6. Báo cáo của agent con (dưới ~150 từ, KHÔNG dán toàn văn)

Tên file đã tạo, Video Title, số từ THÂN/tổng, duration, số scene, ẩn dụ đã dùng (1 câu), điểm còn
băn khoăn. Khi **sửa** theo góp ý: 1 dòng cho mỗi điểm đã xử lý, điểm nào không làm kèm lý do.
Nếu agent trước bị ngắt giữa chừng, agent mới phải chạy `git diff` chỉ-đọc để xem hiện trạng rồi hoàn
thiện, không làm lại từ đầu.
