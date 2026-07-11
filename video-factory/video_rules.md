# VIDEO RULES — VIDEO FACTORY

> Tải lên khu **Files** của Video Factory. File này chứa toàn bộ quy tắc làm video
> (đã tách khỏi `instructions` để dùng chung CORE_BRAIN cho mọi Factory).
> Danh tính, giọng, giá trị, tri thức → vẫn lấy từ CORE_BRAIN (`instructions`, các file knowledge).
> Cập nhật: 05/07/2026.

---

## 0. MÔ HÌNH SẢN XUẤT (đọc trước — quyết định mọi thứ)

Mỗi kịch bản gồm **2 lớp tách rời**:
- **LỚP LỜI (kịch bản voiceover tiếng Việt):** đây là lớp **mang độ dài và giá trị** của video.
- **LỚP HÌNH (shot list B-roll):** danh sách cảnh hình cho công cụ AI (Veo…), **dùng lại được**.

**Nguyên tắc cốt lõi — "cảnh" ≠ "clip lấp đầy thời lượng":**
- Một **cảnh = một Ý / một nhịp nội dung** (chỗ hình thay đổi), KHÔNG phải một clip cố định 8 giây.
- **Độ dài video do LỜI DẪN quyết định**, không phải do số cảnh × độ dài clip.
- Công cụ AI hiện tạo clip ngắn (Veo 3.1: 4/6/8 giây mỗi lần). Để phủ một ý dài hơn:
  **loop / nối (extend) / giữ hình / đổi góc B-roll** dưới cùng một mạch lời dẫn.
- ⚠️ Cảnh báo pipeline: nếu chỉ tạo N clip rồi ghép, video sẽ ngắn hơn nhiều so với mục tiêu.
  Phải khớp **thời lượng lời dẫn** với thời lượng đích, rồi rải B-roll (lặp lại được) lên trên.

**Tool-agnostic:** viết prompt hình theo Ý và bố cục, không khóa cứng "8 giây". Công cụ tự
cắt theo giới hạn của nó; khi Veo 4/5 cho clip dài hơn, cùng kịch bản vẫn dùng được.

**Thuận tự động hóa (n8n):** output luôn tách rõ 2 lớp (LỜI / HÌNH) + đánh số cảnh, để máy
bóc tách: gửi prompt HÌNH cho Veo, gửi LỜI cho TTS/giọng đọc, rồi ghép.

---

## 1. KHUÔN XUẤT KỊCH BẢN (mỗi lần)

- **A. TÊN VIDEO** + 1 câu ý chính (+ 1 câu hứa với video TRUNG/DÀI).
- **B. HOOK (3 giây đầu):** một câu/hình khơi tò mò điềm tĩnh — KHÔNG giật gân.
- **C. CÁC CẢNH** (đánh số). Mỗi cảnh gồm:
  - `[HÌNH]` — tiếng Anh: loại cảnh + chủ thể + chuyển động máy + ánh sáng + âm thanh nền.
    Tham chiếu nhân vật theo `core-brain/image_style_bible.md`. Đánh dấu cảnh nào **dùng lại / loop** được.
  - `[LỜI DẪN]` — tiếng Việt: voiceover cho ý đó. **Giọng đọc lồng riêng** (không để công cụ
    đọc tiếng Việt — giữ kiểm soát tông).
- **D. KẾT:** một câu lắng đọng, mở ra suy ngẫm. Không "like share" gắt.

**Ngân sách lời (giọng trầm-chậm):** ~110–130 từ/phút. Với video NGẮN, mỗi nhịp ý ngắn giữ
gọn (~14–16 từ/8 giây hình); với TRUNG/DÀI, lời dẫn viết liền mạch theo tổng thời lượng, B-roll
phủ bên dưới. Không nhồi chữ cho đủ, cũng không kéo dãn một ý cho đủ giờ.

---

## 2. KHUNG ĐỊNH DẠNG

### VIDEO NGẮN (SHORT)
- Nền tảng: TikTok · Facebook Reels · YouTube Shorts.
- Thời lượng: **60–120 giây**.
- Số cảnh (ý) tham khảo: **5–8** · khuyến nghị **6**.
- Mục tiêu: một ý chính duy nhất · một hook · một bài học · một kết lắng đọng.

### VIDEO TRUNG (MEDIUM)
- Nền tảng: Facebook Video · YouTube.
- Thời lượng: **3–6 phút**.
- Số cảnh (ý) tham khảo: **10–14** · khuyến nghị **12**.
- Mục tiêu: một chủ đề có chiều sâu hơn · có ví dụ hoặc một câu chuyện đời thực (xem `life_stories.md`).

### VIDEO DÀI (LONG)
- Nền tảng: YouTube · Podcast video.
- Thời lượng: **8–12 phút**.
- Số cảnh (ý) tham khảo: **15–22** · khuyến nghị **18**.
- Mục tiêu: đào sâu chủ đề · nhiều lớp góc nhìn · có phần áp dụng thực tế · KHÔNG kéo dài một ý cho đủ giờ.
- Theo **kiến trúc long-form ở mục 4**.

**Nguyên tắc chung về số cảnh:**
- Mỗi cảnh đại diện cho một ý.
- Không thêm cảnh chỉ để đạt đủ số lượng; không cắt ý quan trọng để giảm số cảnh.
- Chất lượng nội dung quan trọng hơn số cảnh. Trợ lý được phép tăng/giảm số cảnh theo yêu cầu của chủ đề.

---

## 3. QUY TẮC TỰ CHỌN ĐỊNH DẠNG

- Khi người dùng nói **NGẮN / TRUNG / DÀI** → trợ lý **tự chọn số cảnh** theo khung trên,
  KHÔNG hỏi lại. (VD: "Làm video trung về dưỡng sinh" → tự quyết: chủ đề đơn giản ~10 cảnh,
  trung bình ~12, sâu ~14.)
- Khi người dùng nêu **thời lượng cụ thể** (2 phút / 5 phút / 10 phút) → **thời lượng được ưu
  tiên hơn số cảnh**; trợ lý tự điều chỉnh số cảnh + độ dài lời dẫn cho khớp.
- Khi người dùng **không nói rõ định dạng** → hỏi lại: "Bạn muốn video NGẮN, TRUNG hay DÀI?".
- Mục tiêu cuối cùng: **đúng trải nghiệm xem**, không phải đúng con số cảnh.

---

## 4. KIẾN TRÚC VIDEO DÀI (8–12 phút)

Mục tiêu: chiều sâu thật, để người xem thấy "mình vừa nhận được điều gì đó".

**Khung 5 phần:**
1. **MỞ (10–20s):** hook điềm tĩnh + một câu hứa nhẹ về điều người xem sẽ hiểu. Không clickbait.
2. **VÌ SAO ĐÁNG QUAN TÂM (20–30s):** nối chủ đề vào đời sống người xem.
3. **THÂN — 2–3 LỚP (phần chính):** khai triển qua 2–3 góc KHÁC NHAU, không lặp một ý. Mỗi lớp
   có mở–khai triển–lắng riêng + B-roll riêng. Có thể chèn một câu chuyện đời thực (xem `life_stories.md`).
4. **ÁP DỤNG (30–45s):** vài gợi ý cụ thể, nhẹ nhàng, người xem làm được ngay.
5. **KẾT LẮNG (15–20s):** một câu để nhớ.

**Kỷ luật giữ chân:** mỗi lớp phải THÊM cái mới; chuyển lớp thì "re-hook" nhẹ; thà 8 phút đặc
còn hơn 12 phút loãng.

**Khuôn xuất video dài:** A. Tên + ý chính + 1 câu hứa · B. **LỜI DẪN liền mạch** theo 5 phần
(viết như một bài nói chậm — lớp mang độ dài) · C. **SHOT LIST B-ROLL** ~15–22 cảnh dùng lại
được, đánh dấu cảnh loop/kéo dài để phủ dưới lời dẫn.

---

## 5. QUY TẮC VIẾT PROMPT HÌNH (Veo / công cụ AI)

- Luôn nêu: loại cảnh (close-up, wide…), chuyển động máy (slow push-in, static, gentle pan…),
  ánh sáng (soft morning light…), tâm trạng, âm thanh nền (ambient). Mô tả cụ thể, điện ảnh,
  nhưng **tĩnh tại** — tránh chuyển động dồn dập, cắt nhanh.
- Tham chiếu nhân vật & bối cảnh theo `core-brain/image_style_bible.md` để giữ nhất quán; nạp tối đa 3 ảnh
  tham chiếu khi generate.
- **Chỉ chữ Việt** trong khung hình (hoặc không chữ) — không bao giờ chữ Hán (theo style bible).
- Ưu tiên B-roll **trung tính, dùng lại được** (trà, vườn, hơi thở, cửa sổ, bàn tay, bước chân,
  sách…) để một kho hình phục vụ nhiều video — tiết kiệm chi phí generate.

---

## 6. MẸO HYBRID & CHI PHÍ

- Tạo MỘT kho B-roll tĩnh đẹp, dùng lại across nhiều video — đừng generate mới từng cảnh.
- Chỉ generate vài cảnh "mặt nhân vật" làm điểm nhấn; phần còn lại là B-roll loop + lời dẫn phủ lên.
- Veo lo HÌNH + ambient; lời dẫn tiếng Việt lồng riêng (TTS chất lượng cao hoặc người đọc).
- Video dài: chi phí generate tăng nhanh — hybrid (kho B-roll dùng lại + lời dẫn dài) là cách bền nhất.

---

## 7. CHỐNG LẶP KHI LÀM HÀNG TRĂM VIDEO

**Nguyên tắc cốt lõi:** Cùng chủ đề ≠ cùng trải nghiệm. Người xem không bao giờ được cảm thấy "tôi đã xem video này rồi."

**Xoay vòng cấu trúc kịch bản (5 biến thể):**
- **Cấu trúc A:** Hook → Thói quen hằng ngày → Ảnh hưởng thân-tâm → Gợi ý nhẹ → Kết lắng.
- **Cấu trúc B:** Hook → Nhận diện cảm xúc → Lý giải nhịp sống hiện đại → Thay đổi nhỏ → Suy ngẫm.
- **Cấu trúc C:** Hook → Nguyên nhân ẩn → Tác động lặng lẽ → Trấn an → Khép nhẹ.
- **Cấu trúc D:** Hook → Tình huống quen thuộc → Cái mệt phía sau → Góc nhìn mới → Kết rất người.
- **Cấu trúc E:** Hook → Hiểu lầm thường gặp → Vì sao → Cách nhìn dịu hơn → An ủi.

**Xoay vòng góc vào (không lặp cùng góc 2 video liên tiếp):**
mệt mỏi cảm xúc · cảm giác cơ thể · thói quen hằng ngày · nhịp sống hiện đại · giấc ngủ ·
ăn uống · quá tải cảm xúc · phản ứng căng thẳng · hồi phục · cân bằng năng lượng.

**Xoay vòng bối cảnh hình:** góc trà · bàn viết cửa sổ · hiên nhà · vườn nhỏ · kệ sách · bước chân trong vườn.

**Xoay vòng câu kết:** tránh lặp "hãy chăm sóc cơ thể mình" — xoay giữa: an ủi cảm xúc / nhắc nhở thực tế / chiêm nghiệm lặng / khích lệ nhẹ / nhận ra bình thường.

## 8. THUMBNAIL ETHICS (ảnh đại diện video)

Thumbnail là ấn tượng đầu tiên — phải **mời người xem**, không tấn công cảm xúc.

**Ưu tiên:**
- Hình ảnh ấm, sạch, gợi tò mò điềm tĩnh
- Khuôn mặt nhân vật biểu cảm chân thực, nhẹ nhàng
- Tiêu đề ngắn, rõ, khơi curiosity — không bỏ lửng "…"
- Màu sắc theo bảng màu kênh (be, nâu, olive, gỗ)

**TUYỆT ĐỐI KHÔNG:**
- Hình đau đớn, bệnh tật, nội tạng, trước-sau gây sốc
- Biểu cảm phóng đại kiểu O_O, hoảng loạn
- Chữ CAPS LOCK, dấu chấm than dồn dập
- Fake urgency: "XEM NGAY KẺO MUỘN", "BÍ MẬT", "SỐC"
- Dọa bệnh, dọa chết, thống kê hù dọa
- Màu neon chói, hiệu ứng phô trương

**Nguyên tắc:** Thumbnail đúng tông kênh khiến người xem nghĩ "video này trông thú vị" — không phải "video này khiến tôi sợ".