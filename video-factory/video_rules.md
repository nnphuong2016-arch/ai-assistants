# VIDEO RULES — VIDEO FACTORY

> Tải lên khu **Files** của Video Factory. File này chứa toàn bộ quy tắc làm video
> (đã tách khỏi `instructions` để dùng chung CORE_BRAIN cho mọi Factory).
> Danh tính, giọng, giá trị, tri thức → vẫn lấy từ CORE_BRAIN (`instructions`, các file knowledge).
> Cập nhật: 05/07/2026.
> Cập nhật: 18/07/2026 — mục 1.C chuẩn hoá field Scene ID zero-padded/Duration/Voice/Visual/
> Camera/Character/Emotion/Loop, tách Master Script khỏi prompt platform-specific (xem mục 1, 4, 5).
> Cập nhật: 20/07/2026 — mục 2 làm rõ VIDEO NGẮN gồm 2 loại nội dung khác nhau (suy ngẫm vs
> Dưỡng Sinh Ngắn — xem `instructions_VIDEO.md` mục 1B).
> Cập nhật: 25/07/2026 — **chốt VIDEO DÀI = 8–12 cảnh · tối đa 3 Clip · tối đa 12–16 Ảnh giữ**
> (mục 2 + mục 6), thay "15–20 cảnh" cũ và gỡ mâu thuẫn với bảng "30–35 cảnh" ở
> `model_selection_rules.md`. Thêm **mục 6B** về chuyển động cho ảnh giữ (đã viết lại 26/07/2026
> — xem chính mục đó). Trần ảnh nâng từ 10–12 lên
> 12–16 (25/07/2026, quyết định của chủ kênh) — thời lượng giữ mỗi ảnh giảm tương ứng còn 30–45
> giây thay vì 45–75. Học từ mô hình kênh
> My Dog & My Love (`youtube-mydog_mylove`), điều chỉnh theo thể loại chiêm nghiệm và thực tế
> khán giả kênh này **nghe nhiều hơn nhìn**.
> Cập nhật: 25/07/2026 (2) — thêm **mục 1.E OUTRO CỐ ĐỊNH**: mọi video kết thúc bằng một đoạn
> nguyên văn cố định (93 từ ≈ 43–51 giây), là CTA duy nhất được phép trên toàn kênh. Nguyên văn
> chỉ nằm ở mục 1.E, các file khác trỏ về. Mục 2/4/7 cập nhật theo (trừ thời lượng outro khỏi
> ngân sách, thêm vào khung 5 phần, miễn trừ khỏi luật chống lặp).
> Cập nhật: 05/09/2026 — **chốt lại độ dài Nhánh A (Giải Đáp), quyết định của chủ kênh**: chỉ còn
> **2 định dạng DÀI (8–10 phút) và TRUNG (6–8 phút)** cho Nhánh A (thay 8–12 phút / 5–8 phút cũ);
> bỏ **NGẮN** khỏi hệ thống (không còn Nhánh/Factory nào dùng — trước đây NGẮN chỉ phục vụ Nhánh
> A). **CLIP (1–3 phút) giữ nguyên nhưng chỉ còn dùng cho Nhánh B — Dưỡng Sinh Ngắn**
> (`duong_sinh_bai_tap.md` mục 5), Nhánh A không dùng CLIP nữa. Trợ lý **tự chọn DÀI hay TRUNG
> theo độ sâu chủ đề, không hỏi lại** (thay quy tắc "mặc định luôn DÀI" 25/07/2026 — xem mục 3
> viết lại), nhưng **cả hai định dạng đều bắt buộc đủ 3 góc rõ ràng, tập trung, không dàn
> trải/lặp ý** — lý do đổi: ép mọi chủ đề (kể cả chủ đề mỏng, chỉ đủ 1 insight) thành DÀI 8–12
> phút cũ dễ dẫn tới nhồi/lặp ý để đủ giờ, vi phạm "Kỷ luật giữ chân" mục 4. Mục 2/3/4/6 cập nhật
> theo; trần Clip AI/Ảnh giữ của DÀI (tối đa 3 Clip · 12–16 Ảnh giữ) và TRUNG (tối đa 2 Clip ·
> 8–12 Ảnh giữ) giữ nguyên không đổi — chỉ đổi khung phút/số cảnh. Quyết định này cũng nêu trong
> `CLAUDE.md` (Bước 3, khối "KỊCH BẢN VIDEO") để không phải lật riêng file này mới biết.
> Cập nhật: 05/09/2026 (2) — thêm hướng **B-roll thiên nhiên miễn phí** (mục 6C): dùng clip/ảnh
> thiên nhiên có sẵn, miễn phí bản quyền, để giảm chi phí Clip AI/Ảnh giữ phải generate — học
> theo mô hình kênh tham chiếu chủ kênh gọi là "kênh Andre". Chi tiết tích hợp kỹ thuật (nguồn
> cụ thể, cách chèn vào Master Script/n8n) do workflow n8n riêng đang được dựng quyết định — mục
> 6C ở đây chỉ chốt **nguyên tắc chính sách**, cập nhật lại khi workflow đó hoàn tất.
> Cập nhật: 05/09/2026 (3) — mục 8: thêm khối **QUICK COPY + PROMPT THUMBNAIL** (Title/
> Description/SEO Keywords/Tags-Hashtag để dán khi đăng YouTube + prompt sinh ảnh thumbnail đầy
> đủ field) ở cuối file `..._prompts.md`, khuôn field đầy đủ ở `output_schema.md`. Vẫn giữ đúng
> **2 file/video**, không thêm file thứ 3. Tham khảo mô hình kênh "Dấu Vết Văn Minh" (chủ kênh
> dẫn), viết lại theo giọng và ranh giới riêng của kênh Anh Minh.
> Cập nhật: 07/09/2026 — **CHỐT LẠI tốc độ đọc & định dạng Nhánh A theo dữ liệu thật** (quyết
> định của chủ kênh, sau khi 3 tập đầu — 1.1/1.2/1.3 — dựng thật ra chỉ 2:44–3:43 dù viết theo
> mục tiêu ~9 phút). Tra trực tiếp log `Probe Scene Voice Durations`/`Call FFmpeg Service` của
> WFAnhMinhC201/C202 (27 cảnh thật) cho thấy giọng VieNeu đang dùng đọc **~250 từ/phút** —
> KHÔNG phải 110–130 từ/phút như giả định cũ (sai gần gấp đôi). Chủ kênh xác nhận giữ nguyên tốc
> độ đọc này (không đổi giọng/tốc độ TTS). Hệ quả: một câu hỏi "Tại sao...?" đơn lẻ của Nhánh A
> không đủ chất liệu để kéo dài 6–10 phút ở tốc độ đọc thật này mà không lặp ý/loãng (cần tới
> ~1500–2500 từ, gấp đôi–gấp ba số từ đã viết cho 3 tập đầu). **NGẮN (3–5 phút) khôi phục lại
> làm định dạng MẶC ĐỊNH của Nhánh A**, thay DÀI/TRUNG (05/09/2026) — xem mục 1.E/2/3/4 viết lại.
> TRUNG/DÀI vẫn giữ làm lựa chọn khi chủ đề thật sự đủ sâu, nhưng số từ mục tiêu đã tính lại theo
> đúng 250 từ/phút. Tập 1.1 (3:43) và 1.2 (3:02) đã nằm trong khoảng NGẮN, không cần viết lại;
> tập 1.3 (2:44) dưới mốc 3 phút — YouTube xếp video dưới 3 phút vào Shorts — nên đã viết lại
> cùng ngày (cụ thể hoá thêm chi tiết cho từng cảnh, không thêm góc/ý mới) để đạt ~3:38.
> Cập nhật: 07/09/2026 (2) — **CHỐT CỨNG: Nhánh A chỉ còn NGẮN (3–5 phút), bỏ hẳn TRUNG/DÀI**
> (quyết định của chủ kênh, cùng ngày, chỉ vài giờ sau bản trên). Không còn ngoại lệ "chủ đề đủ
> sâu thì lên TRUNG/DÀI" — cơ chế đó dễ bị lạm dụng, quay lại đúng vấn đề đã sửa. Trợ lý không
> còn phải chọn định dạng — mọi video Nhánh A đều NGẮN, không hỏi lại. Mục 2/3/4/6 cập nhật
> theo; CLAUDE.md Bước 3 khối "KỊCH BẢN VIDEO" cũng cập nhật để khớp.

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
------
## 0B. NGUYÊN TẮC KHI LÀM VIDEO TỪ BÀI VIẾT NGUỒN NGOÀI (không phải bài SEO tự viết)

Khi input là một bài viết có sẵn từ nguồn ngoài (không phải bài SEO do Funamark tự tạo qua
SEO Factory), tuyệt đối KHÔNG chuyển thể theo kiểu "đổi định dạng" (giữ cấu trúc, ví dụ, câu
chữ gốc rồi đọc thành lời). Thay vào đó:

- Chỉ lấy **ý / chủ đề / thông tin chung** của bài làm điểm cảm hứng.
- Viết lại **hoàn toàn mới** bằng giọng Anh Minh (theo `examples_and_hooks.md` +
  `philosophy_reference.md`), diễn đạt, cấu trúc, ví dụ, câu mở-câu kết đều do trợ lý sáng
  tạo lại — không mô phỏng sát bài gốc.
- Không dùng chung hook / cách vào đề / thứ tự lập luận của bài gốc.
- Đây là khác biệt với chế độ "chuyển đổi từ bài SEO có sẵn" ở mục 1 `instructions_VIDEO.md`
  (áp dụng khi bài SEO ĐÃ do chính Funamark viết) — trường hợp đó được giữ nguyên hook vì là
  nội dung tự sở hữu.

Mục đích: tránh rủi ro vi phạm bản quyền khi dùng bài viết của người khác làm nguồn cảm hứng.
---

## 1. KHUÔN XUẤT KỊCH BẢN (mỗi lần)

> **Cập nhật 18/07/2026:** chuẩn hoá mỗi cảnh thành khối field cố định (Scene ID zero-padded +
> Duration/Voice/Visual/Camera/Character/Emotion/Loop tách riêng) — để Master Script là **nguồn
> dữ liệu** duy nhất, không lẫn prompt riêng cho một công cụ AI cụ thể (Kling/Veo3/Sora...).
> Việc build prompt cho từng công cụ là một bước RIÊNG, làm SAU khi Master Script này đã hoàn
> tất (thủ công: đưa lại Master Script cho Claude và yêu cầu "chuyển thành prompt Kling/Veo3";
> tự động: node Scene Generator trong n8n, xem `video_ai_contract.md`). Nhờ vậy khi công cụ AI
> đổi/ra bản mới, chỉ cần sửa bước build prompt, không phải viết lại kịch bản.

- **A. TÊN VIDEO** + 1 câu ý chính (+ 1 câu hứa).
- **B. HOOK (3 giây đầu):** một câu/hình khơi tò mò điềm tĩnh — KHÔNG giật gân.
- **C. CÁC CẢNH** — mỗi cảnh là một khối field cố định, theo đúng thứ tự sau.
  ⚠️ **Định dạng bắt buộc:** mỗi cảnh phải mở đầu bằng heading markdown `### Scene <ID>` (VD
  `### Scene 001`, có thể kèm chú thích trong ngoặc: `### Scene 001 (HOOK)`), rồi tới các field
  dạng gạch đầu dòng `- **Tên field:** giá trị` theo đúng thứ tự dưới đây. Đây không phải sở
  thích trình bày — Code node của n8n (WF-07B) parse file `_master_script.md` đúng theo khuôn
  này (`video_ai_contract.md` GHI CHÚ VẬN HÀNH). Viết "Cảnh 1:", "**Scene 001**" hay đổi thứ tự
  field đều làm parser gãy. Xem ví dụ đầy đủ ở `examples_and_hooks.md` mục 6.
  - **Scene ID:** số thứ tự cảnh, zero-padded 3 chữ số (`001`, `002`, `003`...) — để pipeline
    map 1:1 sang file media cùng ID (`Voice001.mp3`, `Clip001.mp4`, `Subtitle001.srt`...).
  - **Duration:** thời lượng cảnh (giây), ước theo ngân sách lời của đoạn Voice trong cảnh đó.
  - **Voice** — tiếng Việt: voiceover cho ý đó. **Giọng đọc lồng riêng** (không để công cụ đọc
    tiếng Việt — giữ kiểm soát tông).
  - **Shots** — số hình phủ cảnh này: `1`, `2` hoặc `3` (mặc định `1`).
    ⚠️ Ở tốc độ đọc thật ~250 từ/phút (mục 1.E), một cảnh NGẮN (~20–35 giây) thường chỉ cần
    `Shots: 1` — chỉ đặt `Shots: 2` khi một cảnh cụ thể vượt quá ~40–45 giây (trần thực dụng giữ
    một ảnh, mục 6B). Cộng tổng Shots của cả video trước khi xuất để tự kiểm trần Ảnh giữ
    (mục 2).
    Khi `Shots > 1`, viết Visual/Camera thành đúng ngần ấy khối đánh số (`Visual 1:`/`Camera 1:`,
    `Visual 2:`/`Camera 2:`...), mỗi khối là một hình riêng. File media map theo
    `<Scene ID>-<số shot>` (VD cảnh 003 có 2 hình → `Shot003-1`, `Shot003-2`); riêng
    `Voice003.mp3` và `Subtitle003.srt` vẫn 1 file/cảnh vì lời dẫn không tách theo hình.
  - **Visual** — tiếng Anh: bối cảnh + chủ thể + hành động (không lặp lại nội dung đã có ở
    Camera/Character bên dưới). ⚠️ **KHÔNG mô tả khuôn mặt/trang phục/đặc điểm ngoại hình nhân
    vật ở đây** — nhận diện nhân vật do field Character đảm nhiệm (xem bên dưới), khớp đúng quy
    tắc "Scene Generator AI" ở `video_ai_contract.md` ("không mô tả khuôn mặt, không mô tả quần
    áo, không mô tả nhân vật — Character sẽ được n8n ghép sau"). Nhờ vậy Master Script dùng
    được thẳng cho cả Cách 1 (thủ công) lẫn Cách 2 (n8n) mà không cần sửa lại.
  - **Camera** — tiếng Anh: loại cảnh (close-up, wide…) + chuyển động máy (slow push-in,
    static, gentle pan…) + ánh sáng + âm thanh nền (ambient). Cũng không mô tả nhân vật ở đây,
    cùng lý do như field Visual.
  - **Character** — tên nhân vật xuất hiện trong cảnh; để trống nếu cảnh chỉ có B-roll trung
    tính không có nhân vật. Hai loại nhân vật, xử lý khác nhau ở bước sau (Master Script chỉ cần
    ghi đúng tên, không cần biết chi tiết pipeline):
    - **"Hiền triết Anh Minh"** — nhân vật DUY NHẤT có kho ảnh cố định (tham chiếu
      `core-brain/image_style_bible.md` mục 0B). Phần lớn cảnh tĩnh của Anh Minh lấy thẳng ảnh
      có sẵn (không generate); cảnh cần chuyển động mới img2video từ đúng ảnh đó.
    - **Tên nhân vật khách** (người trong câu chuyện đang kể, không phải Anh Minh) — KHÔNG có
      kho ảnh sẵn, generate mới ở Flux nhưng chỉ 1 lần cho cả video rồi dùng lại xuyên suốt (xem
      `video_ai_prompt_rules.md` mục 9 + `video_ai_contract.md` Stage 3).
    Khi làm thủ công (Cách 1), thấy field này có tên Anh Minh thì tự nạp bộ ảnh reference tương
    ứng vào Veo3/Kling; nhân vật khách thì tự tạo ảnh nhất quán rồi dùng lại. Khi tự động (Cách
    2), n8n đọc field này ở Stage 2B/3/4 (`video_ai_contract.md`) để định tuyến đúng nguồn ảnh.
  - **Emotion** — tâm trạng/cảm xúc chủ đạo của cảnh (VD: "tĩnh lặng", "ấm áp", "trầm ngâm").
  - **Loop** — `true`/`false`: cảnh này có dùng lại/loop được cho video khác không.
- **D. KẾT:** một câu lắng đọng, mở ra suy ngẫm. Không "like share" gắt.
- **E. OUTRO CỐ ĐỊNH (bắt buộc, đọc nguyên văn — xem mục 1.E bên dưới).**

### 1.E. OUTRO CỐ ĐỊNH — NGUỒN GỐC DUY NHẤT (chốt 25/07/2026)

> ⚠️ **Đây là nơi DUY NHẤT chứa nguyên văn đoạn outro.** Mọi file khác chỉ được **trỏ về mục
> này**, không chép lại — chép lại là mở đường cho hai bản lệch nhau khi sửa.

**Mọi video đều kết thúc bằng đúng đoạn này, đọc nguyên văn, KHÔNG viết lại, KHÔNG rút gọn,
KHÔNG diễn đạt khác:**

```
Cảm ơn bạn đã ngồi lại cùng Anh Minh đến những phút cuối của video.

Nếu những chia sẻ hôm nay mang đến cho bạn một suy nghĩ mới, một chút bình yên hay chỉ là một
lời nhắc nhẹ nhàng dành cho chính mình, hãy đăng ký kênh để chúng ta tiếp tục đồng hành trên
hành trình này.

Cuộc sống không phải lúc nào cũng dễ dàng. Nhưng chỉ cần mỗi ngày hiểu mình hơn một chút, lòng
sẽ nhẹ hơn một chút.

Hẹn gặp lại bạn trong video tiếp theo.
```

**Ngân sách thời lượng:** 93 từ ≈ **22–23 giây** (ở tốc độ đọc THẬT ~250 từ/phút, đo trực tiếp từ
3 tập đầu — chốt lại 07/09/2026, xem changelog đầu file. Con số 43–51 giây trước đây tính theo
giả định 110–130 từ/phút chưa kiểm chứng, sai gần gấp đôi). Phải **trừ trước** khỏi tổng thời
lượng khi chia cảnh.

**Quan hệ với phần D:** outro đứng **SAU** câu kết lắng đọng, không thay thế nó. Phần D vẫn là
câu để nhớ của riêng video đó; outro là phần đóng khung chung của kênh.

**Đóng gói trong Master Script:** outro là **một cảnh riêng, luôn là cảnh cuối cùng**, với
`Loop: true` (dùng lại được ở mọi video). Không tính vào phần THÂN khi phân bổ nội dung.

**Ngoại lệ về CTA:** câu "hãy đăng ký kênh" trong outro là **CTA duy nhất được phép** trên toàn
kênh, và chỉ ở đúng chỗ này, đúng cách diễn đạt này. Quy tắc *không "like share" gắt* (phần D,
`bep_an_nhien.md` mục 5, `duong_sinh_bai_tap.md` mục 5) vẫn giữ nguyên cho mọi vị trí khác — cấm
chèn thêm lời kêu gọi like/share/bình luận/bấm chuông ở đầu hay giữa video, cấm tự chế biến thể
khác của lời mời đăng ký.

**Miễn trừ chống lặp:** outro cố ý giống hệt nhau ở mọi video — **không** áp quy tắc chống lặp ở
mục 7 lên đoạn này, và không tính nó khi kiểm tra "video này có trùng câu kết với video trước
không".

**Tiết kiệm chi phí:** vì lời và hình của outro không đổi giữa các video, chỉ cần render **một
lần** rồi tái sử dụng — không tốn TTS và không tốn generate hình cho mỗi tập (xem
`video_ai_contract.md` Stage 5 và Stage 7).

**Ngân sách lời — tốc độ đọc THẬT ~250 từ/phút** (đo trực tiếp từ giọng VieNeu đang dùng cho
kênh, chốt lại 07/09/2026 — xem changelog đầu file. Con số 110–130 từ/phút trước đây chỉ là giả
định "giọng trầm-chậm" chưa từng kiểm chứng bằng TTS thật — sai gần gấp đôi so với thực tế, đây
là nguyên nhân khiến 3 tập đầu viết cho ~9 phút lại dựng ra chỉ 2:44–3:43). Với video CLIP (chỉ
Nhánh B), mỗi cảnh giữ gọn (~35–45 từ Voice / ~8–10 giây Duration ở tốc độ thật); **với video
NGẮN (định dạng DUY NHẤT của Nhánh A — chốt cứng 07/09/2026 (2), mục 2/3), mỗi cảnh ~80–145 từ
Voice / ~20–35 giây Duration**. Luôn **tính số từ theo đúng
250 từ/phút trước khi viết** (đừng ước theo cảm giác), rồi viết lời dẫn liền mạch theo tổng thời
lượng đã tính (giữ mạch cảm xúc), sau đó chia thành các cảnh theo khuôn field ở trên — mỗi field
Voice là một đoạn của lời dẫn liền mạch đã viết, không viết lại. Không nhồi chữ cho đủ, cũng
không kéo dãn một ý cho đủ giờ.

---

## 2. KHUNG ĐỊNH DẠNG (chốt lại 25/07/2026 theo tiêu chí kênh My Dog & My Love)

> ⚠️ **Lưu ý tránh nhầm hai nghĩa của chữ "clip":**
> - **CLIP** viết hoa, đứng một mình = **một định dạng video** 1–3 phút (bảng dưới).
> - **Clip AI** = **một loại hình** trong kịch bản, đối lập với **Ảnh giữ** (mục 6/6B).
>
> Một video định dạng CLIP vẫn có thể chứa 1 Clip AI + vài Ảnh giữ. Trong toàn bộ hệ thống, loại
> hình luôn viết đầy đủ là **"Clip AI"**, không bao giờ viết tắt thành "Clip" khi đang nói về
> ngân sách hình.

| Định dạng | Thời lượng | Số cảnh | Giây/cảnh (ở tốc độ đọc thật ~250 từ/phút) | Clip AI | Ảnh giữ |
|---|---|---|---|---|---|
| **CLIP** *(chỉ Nhánh B)* | 1–3 phút | **3–6** | ~20–30 | tối đa **1** | **3–6** |
| **NGẮN** *(DUY NHẤT cho Nhánh A)* | 3–5 phút | **8–9** | ~20–35 | tối đa **2** | **4–8** |

> **Cập nhật 07/09/2026 (2) — CHỐT CỨNG: Nhánh A chỉ còn NGẮN (3–5 phút), bỏ hẳn TRUNG/DÀI**
> (quyết định của chủ kênh, thay bản "NGẮN mặc định, TRUNG/DÀI khi đủ sâu" cùng ngày — chỉ vài
> giờ trước). Không còn ngoại lệ "chủ đề đủ sâu thì lên TRUNG/DÀI" — **mọi video Nhánh A đều
> 3–5 phút**, không hỏi lại, không tự xét "đủ sâu" để kéo dài. Lý do siết thêm: dữ liệu thật (3
> tập đầu, tốc độ đọc ~250 từ/phút) cho thấy ngay cả NGẮN 3–5 phút cũng đã cần viết cụ thể/khéo
> mới không loãng; cho phép TRUNG/DÀI làm ngoại lệ dễ bị lạm dụng thành "chủ đề nào cũng đủ sâu"
> rồi quay lại đúng vấn đề đã sửa hôm 05/09 và 07/09 (1). TRUNG/DÀI **vẫn còn định nghĩa** ở
> `model_selection_rules.md` cho các Nhánh/kịch bản khác nếu cần trong tương lai, nhưng **Nhánh A
> không còn được chọn hai định dạng này nữa dưới bất kỳ lý do gì** — kể cả khi người dùng không
> chỉ định gì (mặc định luôn là NGẮN) hoặc khi tự thấy chủ đề "có vẻ sâu" (không tự xét nữa, xem
> mục 3 viết lại). **CLIP giữ nguyên, chỉ dành cho Nhánh B** (Dưỡng Sinh Ngắn, `duong_sinh_bai_tap.md`
> mục 5).
>
> ⚠️ Số cảnh/Ảnh giữ trong bảng áp dụng khi Nhánh A dùng pipeline sinh ảnh AI từng cảnh ("Cách 1"
> trong `video_ai_contract.md`). Khi dùng pipeline nền thiên nhiên có sẵn (không sinh ảnh AI —
> xem mục 6C), số Ảnh giữ/Clip AI ở đây không áp dụng; thời lượng video vẫn do đúng tổng số từ
> Voice ở tốc độ đọc thật quyết định, không phải số hình.

**Cách nhớ nhanh cho NGẮN (mặc định):** ~750–1250 từ cả outro (outro cố định 93 từ ≈ 22–23 giây
ở tốc độ thật), chia 8–9 cảnh.

> ⚠️ **Số cảnh trong bảng ĐÃ BAO GỒM cảnh outro cố định** (mục 1.E, ~22–23 giây ở tốc độ thật).
> Nghĩa là phần nội dung thật chỉ còn N−1 cảnh. **Luôn trừ outro trước khi chia cảnh.**
>
> ⚠️ **Định dạng CLIP: outro chiếm tỷ trọng quá lớn — cần chủ kênh quyết.** Outro ~22–23 giây
> trên một CLIP 60 giây vẫn là **~37% thời lượng**. Hiện quy định "mọi video đều có outro" áp cho
> **NGẮN/TRUNG/DÀI** là an toàn; với **CLIP**, tạm thời vẫn gắn outro theo đúng yêu cầu nhưng đây
> là điểm **chờ quyết định** — hai hướng khả dĩ: (a) dùng bản rút gọn chỉ 2 câu cuối cho CLIP,
> hoặc (b) miễn outro cho CLIP. Không tự chọn thay chủ kênh.

**Ngân sách hình là TRẦN CỨNG, không phải chỉ tiêu** — dùng ít hơn luôn tốt hơn. Ảnh làm
start-frame cho Clip AI **không tính vào trần Ảnh giữ** (xem mục 6). Chi tiết cách chia và cách
chọn công cụ → `model_selection_rules.md` mục 1B.

### Ghi chú riêng từng định dạng

- **CLIP (1–3 phút) — chỉ Nhánh B (Dưỡng Sinh Ngắn)** — nền tảng: TikTok · Facebook Reels ·
  YouTube Shorts. Thị phạm một động tác, theo khuôn riêng ở `duong_sinh_bai_tap.md` mục 5 (nhịp
  cảnh đi theo động tác/hơi thở, không theo nhịp kể chuyện). Nhánh A không dùng CLIP.
- **NGẮN (3–5 phút) — ĐỊNH DẠNG DUY NHẤT của Nhánh A, chốt cứng 07/09/2026** — nền tảng: YouTube.
  Trả lời trọn vẹn một câu hỏi "Tại sao...?" bằng **3 góc rõ ràng** ở mức súc tích, đúng với chất
  liệu thật sự có của một câu hỏi đơn lẻ trong backlog — không dàn trải, không nhồi chữ cho đủ
  phút. Không còn TRUNG/DÀI cho Nhánh A (xem changelog đầu file + mục 3) — mọi video Nhánh A đều
  nằm trong khoảng này, không có ngoại lệ theo độ sâu chủ đề.

⚠️ **Cách chọn định dạng cho Nhánh A: xem mục 3.** Không còn gì để "chọn" nữa — NGẮN là định
dạng duy nhất, luôn luôn dùng, mọi chủ đề.

**Nguyên tắc chung về số cảnh:**
- Mỗi cảnh đại diện cho một ý.
- Không thêm cảnh chỉ để đạt đủ số lượng; không cắt ý quan trọng để giảm số cảnh.
- Chất lượng nội dung quan trọng hơn số cảnh. Trợ lý được phép xê dịch số cảnh trong khoảng của
  định dạng — nhưng **trần ngân sách hình là con số cứng, không tự nới**. Nếu chủ đề thấy chật,
  gộp ý lại hoặc chuyển lên định dạng dài hơn, không thêm hình.

---

## 3. QUY TẮC TỰ CHỌN ĐỊNH DẠNG

### ⭐ NHÁNH A: CHỐT CỨNG NGẮN (3–5 PHÚT) — KHÔNG CÒN NGOẠI LỆ (chốt lại 07/09/2026 (2) — quyết
định của chủ kênh, thay quy tắc "NGẮN mặc định, lên TRUNG/DÀI khi đủ sâu" cùng ngày)

**Nhánh A (Giải Đáp) CHỈ VIẾT NGẮN (3–5 phút). Không còn TRUNG, không còn DÀI, không có ngoại
lệ theo độ sâu chủ đề.** Bản chốt trước đó (07/09/2026, sáng) vẫn cho phép lên TRUNG/DÀI "khi
chủ đề đủ sâu" — chủ kênh siết lại ngay trong ngày vì cơ chế "tự xét đủ sâu" dễ bị áp dụng rộng
rãi hơn dự tính, quay lại đúng vấn đề mà lần chốt 05/09/2026 và 07/09/2026 (1) đã sửa (ép chủ đề
mỏng thành video dài, lặp ý/loãng). CLIP vẫn chỉ dành cho Nhánh B (Dưỡng Sinh Ngắn).

**Trợ lý KHÔNG còn phải chọn định dạng nào nữa — luôn luôn viết NGẮN, mọi chủ đề, không hỏi lại
người dùng.** Việc còn lại chỉ là viết đủ **3 góc rõ ràng, không lặp ý** trong khoảng 3–5 phút đó
(đúng khung THÂN mục 4) — không phải cân nhắc "chủ đề này có xứng đáng dài hơn không".

**Bắt buộc: luôn đủ 3 góc rõ ràng, tập trung — không dàn trải, không lặp ý, không kéo dài một ý
cho đủ giờ.** Nếu một chủ đề viết xong vẫn thấy mỏng ở mức tối thiểu 3 phút dù đã cụ thể hoá hết
mức có thể (thêm chi tiết/ví dụ thật cho từng góc, KHÔNG lặp ý — xem cách làm ở tập 1.3, phần
"viết lại 07/09/2026" trong ghi chú vận hành nội bộ), đó là dấu hiệu nên đổi chủ đề/góc vào khác
từ backlog, không phải dấu hiệu để phá lệ lên TRUNG/DÀI.

- Khi người dùng nêu **thời lượng cụ thể trong khoảng 3–5 phút** → làm theo đúng thời lượng đó,
  tính số từ theo 250 từ/phút (mục 1.E).
- Khi người dùng yêu cầu thời lượng **ngoài khoảng 3–5 phút** cho Nhánh A → nói rõ Nhánh A hiện
  chỉ làm NGẮN (3–5 phút), hỏi lại xem có muốn giữ nguyên khoảng này hay đây là yêu cầu đổi
  chính sách (nếu là đổi chính sách, đó là quyết định của chủ kênh, không tự ý làm khác đi).
- Khi người dùng KHÔNG nói rõ thời lượng (kể cả khi chỉ đưa một tiêu đề/câu hỏi "Tại sao...") →
  mặc định viết NGẮN, KHÔNG hỏi lại.
- Mục tiêu cuối cùng: **đúng trải nghiệm xem, nội dung tập trung, vượt qua mốc 3 phút để không
  bị YouTube xếp nhầm vào Shorts** — không phải đúng con số cảnh hay cố kéo dài cho có vẻ đầy đặn.

---

## 4. KIẾN TRÚC 5 PHẦN CHO NHÁNH A (dùng chung NGẮN/TRUNG/DÀI — chỉ khác độ dài mỗi phần)

> Viết lại 07/09/2026 để áp dụng cho cả NGẮN (mặc định) — trước đó mục này chỉ mô tả riêng DÀI.
> Khung 5 phần và nguyên tắc "3 góc rõ ràng, không lặp ý" giữ nguyên ở mọi định dạng; khác nhau
> ở SỐ TỪ mỗi phần. Từ 07/09/2026 (2), Nhánh A chỉ còn một định dạng (NGẮN) nên mục này áp dụng
> trực tiếp cho NGẮN — không còn nhánh rẽ TRUNG/DÀI nào phải cân nhắc.

Mục tiêu: chiều sâu thật, để người xem thấy "mình vừa nhận được điều gì đó" — dù NGẮN cũng không
hời hợt.

> ⚠️ **Các mốc dưới đây là TỶ TRỌNG NỘI DUNG, không phải ranh giới cảnh cứng.** Tổng ~750–1250 từ
> cả outro ở tốc độ đọc thật ~250 từ/phút (mục 1.E): outro cố định chiếm 93 từ (~22–23 giây);
> phần THÂN gánh phần lớn còn lại, khai triển qua 8–9 cảnh.

**Khung 5 phần:**
1. **MỞ:** hook điềm tĩnh + một câu hứa nhẹ về điều người xem sẽ hiểu. Không clickbait.
2. **VÌ SAO ĐÁNG QUAN TÂM:** nối chủ đề vào đời sống người xem.
3. **THÂN — 2–3 LỚP (phần chính):** khai triển qua 2–3 góc KHÁC NHAU, không lặp một ý. Mỗi lớp
   có mở–khai triển–lắng riêng + B-roll riêng. Có thể chèn một câu chuyện đời thực (xem `life_stories.md`).
4. **ÁP DỤNG:** vài gợi ý cụ thể, nhẹ nhàng, người xem làm được ngay.
5. **KẾT LẮNG:** một câu để nhớ.
6. **OUTRO CỐ ĐỊNH (93 từ ≈ 22–23 giây ở tốc độ thật):** đọc nguyên văn đoạn ở mục 1.E — không
   viết lại, không rút gọn. Đây là cảnh cuối cùng, `Loop: true`, dùng lại y hệt ở mọi video.

**Kỷ luật giữ chân:** mỗi lớp phải THÊM cái mới; chuyển lớp thì "re-hook" nhẹ; thà NGẮN đặc còn
hơn kéo dài mà loãng — đây chính là lý do Nhánh A chỉ còn NGẮN (mục 3).

**Khuôn xuất:** A. Tên + ý chính + 1 câu hứa · B. **Tính số từ mục tiêu theo đúng 250 từ/phút**
(mục 1.E, ~750–1250 từ cả outro), rồi viết **lời dẫn liền mạch theo 5 phần đầu** trước (outro ở
phần 6 là văn bản cố định, không cần viết — chỉ dán nguyên văn từ mục 1.E vào cảnh cuối), như
một bài nói chậm, để giữ mạch cảm xúc — đây là bước nháp · C. Sau đó **chia lời dẫn đã viết
thành 8–9 cảnh**, đóng gói mỗi cảnh theo đúng khuôn field ở mục 1.C (Scene ID zero-padded,
Duration, Voice, Visual, Camera, Character, Emotion, Loop) — mỗi field Voice là một đoạn của lời
dẫn liền mạch đã viết ở bước B, không viết lại. Đánh dấu `Loop: true` cho cảnh B-roll dùng lại/
kéo dài để phủ dưới nhiều đoạn lời dẫn khác nhau.

---

## 5. QUY TẮC VIẾT PROMPT HÌNH (tóm tắt — chi tiết đầy đủ ở file riêng)

> Mục này hướng dẫn nội dung cần có trong field **Visual** + **Camera** (mục 1.C) khi viết Master
> Script — KHÔNG phải nơi viết prompt platform-specific. Prompt đầy đủ cho từng công cụ AI (Veo
> 3, Kling, Hailuo, Runway) là một bước RIÊNG, làm SAU khi Master Script hoàn tất → xem
> `video_ai_prompt_rules.md` (cách viết prompt, dùng chung mọi công cụ) + `model_selection_rules.md`
> (chọn công cụ nào cho từng loại cảnh — Master Script KHÔNG tự chỉ định công cụ). Ngoại hình
> nhân vật Anh Minh → luôn `core-brain/image_style_bible.md`, không định nghĩa lại ở đây.

- Field **Camera**: luôn nêu loại cảnh (close-up, wide…), chuyển động máy (slow push-in, static,
  gentle pan…), ánh sáng (soft morning light…), âm thanh nền (ambient). Mô tả cụ thể, điện ảnh,
  nhưng **tĩnh tại** — tránh chuyển động dồn dập, cắt nhanh.
- Field **Character**: chỉ ghi tên nhân vật (VD "Hiền triết Anh Minh"), tham chiếu
  `core-brain/image_style_bible.md` để giữ nhất quán nhận diện — không mô tả lại ngoại hình bằng
  chữ trong Visual/Camera (nhận diện nhân vật do field Character + ảnh reference đảm nhiệm, xem
  `image_style_bible.md` mục 0B — không nhét mô tả ngoại hình vào Visual/Camera).
- **Chỉ chữ Việt** trong khung hình (hoặc không chữ) — không bao giờ chữ Hán (theo style bible).
- Ưu tiên B-roll **trung tính, dùng lại được** (trà, vườn, hơi thở, cửa sổ, bàn tay, bước chân,
  sách…) để một kho hình phục vụ nhiều video — tiết kiệm chi phí generate.

---

## 6. NGÂN SÁCH HÌNH & CHI PHÍ (tóm tắt — chi tiết đầy đủ ở `model_selection_rules.md` mục 1B/5)

> **Cập nhật 25/07/2026 — thay hẳn mô hình "% cảnh là Clip" cũ.** Tỷ lệ 28–31% Clip trước đây
> khiến một video 8–12 phút cần 9–11 Clip, tức **1,0–1,2 clip/phút** — đắt hơn cả mức cao nhất
> của kênh tham chiếu My Dog & My Love (Tier 3: 0,68 clip/phút, chỉ mở khi doanh thu đã gấp 3–5
> lần chi phí). Nay chuyển sang **trần cứng theo số tuyệt đối**, học từ mô hình đó.

> ⚠️ Mục 6/6B mô tả trần hình cho **DÀI** — từ 07/09/2026 (2), Nhánh A **không còn được dùng DÀI
> dưới bất kỳ lý do gì** (chốt cứng, xem mục 2/3). Bảng dưới đây giữ lại làm tài liệu tham khảo
> (VD nếu sau này có Nhánh/kịch bản khác cần định dạng dài hơn), KHÔNG áp dụng cho Nhánh A hiện
> tại. Trần thật đang dùng cho Nhánh A là **NGẮN** — bảng mục 2 (Ảnh giữ 4–8, tối đa 2 Clip AI).
> Mục 6/6B cũng chỉ áp dụng khi dùng pipeline sinh ảnh AI từng cảnh — không áp dụng khi dùng
> pipeline nền thiên nhiên có sẵn (mục 6C), vốn là pipeline Nhánh A đang chạy thật.

**Trần cứng cho VIDEO DÀI (8–10 phút):**

| Thành phần | Trần |
|---|---|
| Cảnh | 8–10 (mỗi cảnh 55–70 giây lời dẫn) |
| Clip AI video | **tối đa 3** |
| Ảnh giữ | **tối đa 12–16** (mỗi ảnh giữ 30–45 giây) |

- **Vị trí 3 Clip:** MỞ (Anh Minh nói trực diện, neo sự hiện diện nhân vật) · một khoảnh khắc chủ
  đạo giữa bài · KẾT LẮNG. Không rải đều — đặt đúng 3 điểm cảm xúc.
- **Ảnh làm start-frame cho Clip KHÔNG tính vào trần 12–16.** Chỉ đếm ảnh **giữ độc lập** (tự nó
  hiện trên màn hình). Với kênh này, start-frame của cả 3 Clip lấy thẳng từ `characters/` nên
  **chi phí ảnh nhân vật bằng 0** — không generate lại (xem `core-brain/image_style_bible.md` mục 0B).
- **Khán giả kênh này NGHE nhiều hơn NHÌN** (nội dung sức khỏe/triết lý dạng kể chuyện, thường
  bật lên nghe khi đang làm việc khác). Vì vậy ưu tiên giữ ảnh ở **mức dài của khoảng (40–45
  giây)**, không cần đổi hình dồn dập. Giá trị video nằm ở lời dẫn — hình để nâng đỡ, không để
  tranh sự chú ý.
- **Cách tính ra 12–16 ảnh:** video 8–10 phút (480–600 giây) trừ ~27 giây của 3 Clip AI còn
  ~453–573 giây hình. Chia cho 12–16 ảnh ra ~28–48 giây mỗi ảnh, vẫn nằm sát khoảng giữ tự
  nhiên 30–45 giây (hai đầu cực của khung phút có thể lệch nhẹ ra ngoài khoảng này, chấp nhận
  được vì đây là khoảng linh hoạt, không phải ranh giới cứng). Muốn ảnh giữ lâu hơn thì giảm số
  ảnh, muốn đổi hình dày hơn thì tăng số ảnh — nhưng **không vượt trần 16**.
- Tạo MỘT kho B-roll tĩnh đẹp, dùng lại across nhiều video — đừng generate mới từng cảnh.
- Clip AI video generate gốc 6–10 giây → khi dựng, kéo dài cảm giác thành 8–12 giây bằng
  zoom/pan/crop nhẹ (không generate clip dài hơn — tốn thêm chi phí).
- Công cụ AI lo HÌNH + ambient; lời dẫn tiếng Việt lồng riêng (TTS chất lượng cao hoặc người đọc).

### 6B. CHUYỂN ĐỘNG CHO ẢNH GIỮ — trình dựng làm được gì, và phần còn lại phải yêu cầu ở khâu sinh ảnh

> Viết lại 26/07/2026. Bản trước ghi rằng mỗi ảnh giữ "đi qua một chồng lớp hiệu ứng ở bước
> dựng", gồm Parallax, Depth of Field, Light Rays và Particles. **Điều đó không đúng với hệ
> thống đang chạy.** `ffmpeg-service` — dịch vụ mà WF-07.2 gọi để ghép video — chỉ áp **một
> cú Ken Burns** cho mỗi ảnh tĩnh. Không có tách lớp chiều sâu, không có chuyển nét, không có
> tia sáng, không có hạt. Bốn thứ đó cần bản đồ chiều sâu và một chuỗi ghép lớp mà dịch vụ
> không có, nên lên kế hoạch giữ ảnh dựa vào chúng là lên kế hoạch dựa vào thứ không tồn tại.

**Trình dựng làm gì với mỗi ảnh giữ.** Một cú Ken Burns duy nhất, nhưng tốc độ zoom được tính
theo **độ dài giữ của chính ảnh đó**, nên chuyển động trải đều từ giây đầu đến giây cuối thay
vì chạy hết sớm rồi đứng im. Chiều zoom đổi xen kẽ giữa các ảnh liên tiếp và có trôi ngang nhẹ
đổi hướng theo chu kỳ, để một loạt ảnh không cùng bò vào một kiểu.

> Con số "Ken Burns chỉ giữ nổi 20–25 giây" ở bản cũ đo trên hành vi trước đây: tốc độ zoom cố
> định, chạm trần sau khoảng 11 giây rồi bất động. Sau khi sửa (26/07/2026) thì không còn mốc
> chết đó nữa. Vẫn nên coi **45 giây** là trần thực dụng cho một ảnh — quá đó thì một cú
> chuyển động đơn không còn giữ nổi khung hình, hãy cắt ngắn hoặc tách beat làm hai ảnh.

**Bốn thứ dưới đây là từ vựng cho PROMPT SINH ẢNH, không phải hiệu ứng hậu kỳ.** Muốn khung
hình có chúng thì phải yêu cầu model vẽ sẵn vào ảnh; không thể thêm sau ở khâu dựng. Mỗi prompt
chỉ nên gọi **tối đa 2** trong số này:

- **Chiều sâu lớp (thay cho Parallax)** — yêu cầu chủ thể tiền cảnh tách rõ khỏi hậu cảnh: bàn
  tay, khung cửa, tách trà ở gần; không gian lùi xa phía sau. Ảnh có phân tầng rõ thì một cú
  zoom chậm tự đọc ra chiều sâu.
- **Độ sâu trường ảnh (thay cho Depth of Field)** — yêu cầu sẵn hậu cảnh mờ dịu, tiền cảnh nét.
  Không có rack focus động, nhưng một khung đã sẵn phân biệt nét/mờ vẫn dẫn được mắt người xem
  qua một lần giữ dài.
- **Ánh sáng có hướng (thay cho Light Rays)** — tia nắng mềm qua cửa sổ hoặc tán cây, vẽ thẳng
  vào ảnh. Để dành cho đoạn ấm áp, hy vọng, chữa lành — không dùng ở đoạn trầm buồn, sẽ mất
  trọng lượng cảm xúc.
- **Hạt trong không khí (thay cho Particles)** — bụi nắng, lá rơi, hạt mưa, cũng vẽ sẵn. Dùng
  rất tiết chế, chỉ khi mùa/thời tiết trong nội dung gọi tới. Không thêm chỉ để cho đẹp.

⚠️ **Không chồng quá 2 lớp phụ** — nhiều hơn sẽ thành hình "làm quá", phạm đúng tinh thần tĩnh
tại/chân thật của kênh. **Không dùng Camera Shake** (kể cả nhẹ) cho kênh này: nội dung Anh Minh là
chiêm nghiệm — rung máy sẽ đọc thành lỗi kỹ thuật chứ không thành chủ ý.

### 6C. B-ROLL THIÊN NHIÊN MIỄN PHÍ — CHÍNH SÁCH (thêm 05/09/2026, quyết định của chủ kênh)

> ⚠️ **Mục này chỉ chốt nguyên tắc chính sách, KHÔNG phải khuôn kỹ thuật đầy đủ.** Chủ kênh muốn
> giảm chi phí Clip AI/Ảnh giữ bằng cách lồng thêm B-roll thiên nhiên có sẵn, miễn phí bản
> quyền, theo hướng một kênh tham chiếu (chủ kênh gọi là "kênh Andre"). Cách tích hợp kỹ thuật cụ
> thể (nguồn thư viện stock nào, node n8n nào chèn vào, cách khớp với field Visual/Camera ở mục
> 1.C) đang được dựng riêng trong một workflow n8n khác — mục này sẽ cập nhật lại phần "Đóng gói
> trong Master Script" bên dưới khi workflow đó chốt xong, không tự đoán trước chi tiết.

**Nguyên tắc chính sách đã chốt:**
- **Thêm một loại B-roll thứ 3** bên cạnh Clip AI (generate, tốn phí) và Ảnh giữ (generate, tốn
  phí): **B-roll thiên nhiên stock miễn phí** (mây, lá, nước, nắng, gió, rừng, biển… cảnh thiên
  nhiên trung tính, không có nhân vật/thương hiệu) — lấy từ thư viện video miễn phí bản quyền
  thương mại, KHÔNG generate bằng AI.
- **Mục đích duy nhất: cắt chi phí**, không phải thay thế giá trị nội dung — B-roll stock chỉ
  dùng cho những đoạn hình nền trung tính mà Ảnh giữ/Clip AI trước đây phải generate tốn tiền
  (VD: cảnh vườn, cảnh trà, cảnh mây trôi) chứ không dùng cho cảnh cần đúng phong cách nhân vật
  Anh Minh (`core-brain/image_style_bible.md` vẫn là nguồn duy nhất cho mọi cảnh có nhân vật).
- **Không tính vào trần Clip AI/Ảnh giữ ở mục 6** — vì không tốn chi phí generate AI, đúng tinh
  thần "trần là chi phí sinh ảnh AI", không phải trần tổng số cảnh hình. Số lượng B-roll stock
  dùng trong một video hiện chưa có trần riêng — chờ workflow n8n xác định giới hạn thực tế
  (băng thông, thời gian dựng) rồi bổ sung vào đây.
- **Vẫn phải đúng tông kênh**: chọn cảnh thiên nhiên tĩnh tại, ấm áp, không chọn cảnh giật gân/
  timelapse dồn dập — giữ đúng tinh thần chiêm nghiệm (mục 8 Thumbnail Ethics áp dụng tinh thần
  tương tự cho B-roll).

**Đóng gói trong Master Script:** *(để trống, chờ workflow n8n chốt xong — không tự bịa khuôn
field mới khi chưa có quyết định kỹ thuật cụ thể)*.

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

⚠️ **Miễn trừ: outro cố định (mục 1.E) KHÔNG thuộc phạm vi chống lặp.** Nó cố ý giống hệt nhau ở
mọi video. Quy tắc xoay vòng câu kết ở trên chỉ áp cho **phần D — câu kết lắng đọng riêng của
từng video**, đứng trước outro.

## 8. THUMBNAIL ETHICS (ảnh đại diện video)

> **Prompt sinh ảnh thumbnail thật (đầy đủ field) + khối Quick Copy đăng YouTube** → viết ở cuối
> file `..._prompts.md`, theo đúng khuôn `output_schema.md` mục "QUICK COPY + PROMPT THUMBNAIL"
> (thêm 05/09/2026). Mục này chỉ nêu NGUYÊN TẮC/ranh giới nội dung — không lặp khuôn field ở đây.

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