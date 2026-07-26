# MODEL SELECTION RULES — CHỌN CÔNG CỤ TẠO VIDEO AI (VIDEO FACTORY)

> Tải lên khu **Files** của Video Factory. File này quyết định **cảnh nào dùng công cụ AI
> nào** để tối ưu chất lượng, chi phí và tốc độ sản xuất.
> Kịch bản (Master Script) KHÔNG BAO GIỜ tự chỉ định công cụ AI — việc chọn công cụ là của
> pipeline sản xuất, dựa theo file này, không phải việc của người viết kịch bản.
> Quy tắc viết prompt (chung mọi công cụ) → xem `video_ai_prompt_rules.md`. Ngoại hình nhân
> vật → luôn theo `core-brain/image_style_bible.md`, không định nghĩa lại ở đây.
> Cập nhật: 20/07/2026 — dịch + viết lại tiếng Việt từ bản gốc tiếng Anh (dự án tham khảo khác,
> nhân vật "Brian Chen"), thay bằng Hiền triết Anh Minh, gộp giữ nguyên khung quyết định gốc vì
> đã khá tốt — chỉ đổi ngôn ngữ và nhân vật, không đổi logic chọn công cụ.
> Cập nhật: 23/07/2026 — thêm **mục 1B "LỚP QUYẾT ĐỊNH 0"** (Clip AI video hay Ảnh tĩnh + Ken
> Burns) — quy định chính thức mô hình hybrid tiết kiệm chi phí: phần lớn cảnh dùng ảnh tĩnh +
> kỹ thuật zoom/pan (rẻ), chỉ cảnh thật sự quan trọng mới generate clip AI (đắt). Mục 4/5 cập
> nhật theo lớp quyết định mới này.
> Cập nhật: 25/07/2026 — thêm **cờ MỨC CHI HIỆN HÀNH** ngay dưới đây (đọc TRƯỚC mọi thứ khác);
> thay bảng "30–35 cảnh / 9–11 Clip" bằng trần cứng theo số tuyệt đối; đổi "Ken Burns" thành
> **Ảnh giữ + một cú Ken Burns** (xem `video_rules.md` mục 6B — viết lại 26/07/2026 sau khi
> kiểm tra thực tế `ffmpeg-service`).

---

## MỨC CHI HIỆN HÀNH: MỨC 1 (tối đa 3 Clip)

**Ngày đặt: 25/07/2026 · Người đặt: chủ kênh.**

**Mọi video DÀI sản xuất từ lúc này phải theo Mức 1 (tối đa 3 Clip: MỞ · khoảnh khắc chủ đạo ·
KẾT LẮNG) cho tới khi chính dòng này được sửa.**

Cờ này **chỉ chủ kênh mới được đổi**. KHÔNG AI nào trong pipeline (kể cả trợ lý viết kịch bản,
Scene Generator, hay chính lập luận của tài liệu này) được tự nâng lên mức cao hơn vì thấy một
video "có vẻ chạy tốt" — điều kiện nâng mức phụ thuộc số liệu thật trên YouTube Studio và doanh
thu, thứ mà không AI nào ở đây truy cập được. Chúng tồn tại để **con người** biết khi nào quay lại
sửa dòng này, không phải để AI tự đánh giá.

Nếu được yêu cầu lên kế hoạch hay viết một kịch bản video DÀI, phải đọc dòng này TRƯỚC và dùng
đúng mức đang ghi — không đoán, không suy diễn, không tự nâng.

| Mức | Trần Clip | Khi nào dùng |
|---|---|---|
| **Mức 1 — Khởi động** | **3 Clip** | Mặc định, từ video đầu tiên, cho tới khi đạt điều kiện nâng |
| **Mức 2 — Tăng trưởng** | 5 Clip | Khi kênh đã bật kiếm tiền, hoặc ≥8 video Mức 1 giữ chân trung bình ≥45% |
| **Mức 3 — Mở rộng** | 8 Clip | Khi doanh thu tháng vượt chi phí sản xuất 3–5 lần, 2 tháng liên tiếp |

Các mức **cộng dồn**, không phải bản dựng khác nhau: Mức 2 = 3 Clip của Mức 1 + 2 cảnh vốn là ảnh
được nâng lên Clip. Không phải làm lại video. **Ảnh giữ đứng yên ở mọi mức** — ảnh rẻ, không có lý
do gì phải scale theo.


---

## 0. TRIẾT LÝ GỐC

Không phải cảnh nào cũng xứng đáng dùng công cụ đắt nhất.

Pipeline tốt nhất không phải pipeline tốn tiền nhất — mà là pipeline **dùng đúng công cụ cho
đúng cảnh**.

Dành công cụ cao cấp cho cảnh thật sự cần — nơi khán giả nhìn thấy rõ giá trị hình ảnh. Dùng
công cụ hiệu quả/rẻ hơn khi khán giả không nhận ra khác biệt.

**Chất lượng trước — hiệu quả sau — không lãng phí.**

---

## 1. VAI TRÒ TỪNG CÔNG CỤ

### VEO 3

**Vai trò chính:** Cảnh nhân vật cận cảnh, giá trị cảm xúc cao.

**Điểm mạnh:** Biểu cảm khuôn mặt chân thực nhất · diễn xuất cảm xúc tốt · hiểu ngôn ngữ máy
quay · chuyển động người tự nhiên · chất lượng điện ảnh cao cấp.

**Điểm yếu:** Chi phí cao hơn · tạo chậm hơn.

Chỉ dùng khi khán giả đang tập trung cảm xúc vào khuôn mặt một người.

### KLING

**Vai trò chính:** Cảnh kể chuyện có nhân vật lặp lại xuyên suốt.

**Điểm mạnh:** Giữ nhất quán nhân vật rất tốt · trang phục ổn định · bối cảnh ổn định · kể
chuyện đáng tin cậy · chân thực cao.

**Điểm yếu:** Ít biểu cảm hơn Veo ở những khoảnh khắc cảm xúc cận cảnh.

Công cụ mặc định cho phần lớn cảnh có nhân vật.

### HAILUO

**Vai trò chính:** Không khí và hình ảnh mang tính thơ.

**Điểm mạnh:** Nhanh · rẻ · ánh sáng đẹp · thiên nhiên xuất sắc · hình ảnh biểu tượng xuất sắc
· B-roll xuất sắc.

**Điểm yếu:** Khả năng giữ nhất quán nhân vật hạn chế.

Không bao giờ dựa vào Hailuo cho cảnh kể chuyện dài có cùng một nhân vật xuyên suốt.

### RUNWAY

**Vai trò chính:** Tăng giá trị hình ảnh (composition, chuyển động máy quay).

**Điểm mạnh:** Bố cục đẹp · chuyển động máy quay tinh tế · khung hình điện ảnh mạnh · cảnh
chèn (insert) xuất sắc.

**Điểm yếu:** Không phải lựa chọn ưu tiên cho diễn xuất nhân vật kéo dài.

Chỉ dùng Runway khi bố cục hoặc chuyển động máy quay là ưu tiên.

---

## 1B. LỚP QUYẾT ĐỊNH 0 — CLIP AI VIDEO HAY ẢNH GIỮ + KEN BURNS (quyết định TRƯỚC khi chọn công cụ)

> Thêm 23/07/2026 — chính thức hoá mô hình hybrid tiết kiệm chi phí. Đây là bước quyết định
> **đứng trước** mục 2–4 bên dưới: trước khi hỏi "cảnh này dùng Veo3 hay Kling hay Hailuo hay
> Runway", phải hỏi câu hỏi gốc hơn — **"cảnh này có cần generate clip AI (chuyển động thật)
> không, hay một ảnh giữ + một cú Ken Burns là đủ?"** Phần lớn cảnh KHÔNG cần
> clip — ảnh tĩnh rẻ hơn nhiều lần so với video generate (dù công cụ nào), vì chỉ tốn 1 lần
> generate ảnh (hoặc dùng ảnh có sẵn từ kho) thay vì generate video.

**Mặc định: Ảnh giữ + một cú Ken Burns** (`video_rules.md` mục 6B)**.** Chỉ chuyển sang Clip AI video khi cảnh thuộc một trong các
trường hợp sau:
- Anh Minh nói trực diện camera (môi/biểu cảm cần chuyển động thật).
- Cận cảnh cảm xúc — khoảnh khắc khán giả cần thấy vi biểu cảm (chớp mắt, thở, ngập ngừng).
- Khoảnh khắc chủ đạo (hero scene) của cả video — nơi giá trị hình ảnh quyết định cảm xúc chính.
- Hành động có chuyển động là chính nội dung cảnh (VD: bước đi, cầm/đặt vật, cử chỉ tay có ý
  nghĩa) — nếu đứng yên thì mất hết ý cảnh muốn truyền tải.

**Giữ Ảnh giữ + Ken Burns cho các trường hợp còn lại** (đa số cảnh): thiên nhiên, đồ vật, bối
cảnh/không gian, ẩn dụ hình ảnh, establishing shot, nhân vật ngồi/đứng yên lặng không cần biểu
cảm vi tế, B-roll chuyển cảnh. Với cảnh có Anh Minh nhưng chỉ ngồi/đứng tĩnh (không nói, không
biểu cảm mạnh) → dùng thẳng ảnh từ kho ảnh nhân vật cố định (`core-brain/image_style_bible.md`
mục 0B) làm ảnh tĩnh, KHÔNG cần img2video — rẻ nhất, vẫn giữ đúng nhận diện nhân vật vì là ảnh
gốc, không generate lại.

**Ngân sách hình cho VIDEO DÀI (8–12 phút) — Mức 1, trần cứng:**

| Thành phần | Trần |
|---|---|
| Cảnh (đơn vị lời dẫn) | 8–12 (mỗi cảnh 55–70 giây) — nguồn chốt: `video_rules.md` mục 2 |
| Clip AI video | **tối đa 3** |
| Ảnh giữ độc lập | **tối đa 12–16** (mỗi ảnh giữ 30–45 giây, trần thực dụng 45 giây — mục 6B) |

> ⚠️ **Bảng này thay bảng cũ "30–35 cảnh / 9–11 Clip / 20–24 ảnh tĩnh"** (bản 23/07/2026). Bảng cũ
> vừa mâu thuẫn với `video_rules.md` mục 2, vừa đắt bất hợp lý: 9–11 Clip cho 8–12 phút là
> **1,0–1,2 clip/phút**, cao hơn cả mức chi cao nhất của kênh tham chiếu My Dog & My Love (Mức 3
> của họ: 0,68 clip/phút, chỉ mở khi đã có lãi vững). Nay `video_rules.md` mục 2 là nguồn chốt số
> cảnh, file này chốt trần hình.

**Hai quy tắc đếm bắt buộc nhớ:**

1. **Ảnh dùng làm start-frame cho Clip KHÔNG tính vào trần 12–16.** Chỉ đếm ảnh **giữ độc lập**
   (tự nó hiện trên màn hình). Mỗi Clip đều cần một khung mở đầu, nhưng khung đó không phải một
   "ảnh giữ".
2. **Start-frame của kênh này miễn phí.** Cả 3 Clip đều là img2video animate thẳng từ kho ảnh nhân
   vật cố định trong `characters/` (`core-brain/image_style_bible.md` mục 0B) — không generate lại.
   Đây là lợi thế so với kênh tham chiếu, vốn phải sinh mới ảnh nhân vật cho từng tập.

**Vì sao chỉ 3 Clip mà không phải 5 như kênh tham chiếu:** thể loại khác nhau. My Dog là kể chuyện
có chạy/cứu/đoàn tụ — chuyển động chính là nội dung, bỏ chuyển động là mất cảm xúc. Nội dung Anh
Minh là chiêm nghiệm về sức khỏe/triết lý, gần như không cảnh nào qua được bài kiểm "bỏ chuyển
động thì mất cảm xúc". Thêm nữa, **khán giả kênh này nghe nhiều hơn nhìn** — thường bật lên nghe
khi đang làm việc khác — nên hình chỉ cần nâng đỡ lời dẫn, không cần tranh sự chú ý.

**Ngân sách hình cho 3 định dạng còn lại** (chốt 25/07/2026 — giảm dần theo thời lượng, cùng
triết lý "đa số là Ảnh giữ"):

| Định dạng | Thời lượng | Cảnh | Clip AI | Ảnh giữ |
|---|---|---|---|---|
| CLIP | 1–3 phút | 3–6 | tối đa 1 | 3–6 |
| NGẮN | 3–5 phút | 5–7 | tối đa 2 | 5–8 |
| TRUNG | 5–8 phút | 6–9 | tối đa 2 | 8–12 |
| **DÀI** *(mặc định)* | 8–12 phút | 8–12 | **tối đa 3** | **12–16** |

⚠️ **Chữ "Clip" ở đây là loại hình (Clip AI video), KHÔNG phải định dạng CLIP 1–3 phút.** Một
video định dạng CLIP vẫn chứa tối đa 1 Clip AI + 3–6 Ảnh giữ. Xem lưu ý đầu `video_rules.md`
mục 2.

**Định dạng mặc định của kênh là DÀI.** Khi người dùng chỉ đưa một tiêu đề mà không nói gì thêm
→ làm VIDEO DÀI, không hỏi lại (`video_rules.md` mục 3).

**Độ dài Clip AI video (khi đã chọn generate clip):** gốc 6–10 giây (tuỳ công cụ, xem mục 12
`video_ai_prompt_rules.md`) — khi dựng (edit), có thể **kéo dài cảm giác thành 8–12 giây** bằng
kỹ thuật zoom/pan/crop nhẹ trên chính clip đó (không phải generate clip dài hơn — tốn thêm chi
phí). Kỹ thuật này áp dụng ở bước FFMPEG Composer, xem `video_ai_contract.md` Stage 7.

**Độ dài hiển thị Ảnh tĩnh:** bám sát **Duration** của scene đó (đã có sẵn ở khuôn field
`video_rules.md` mục 1.C — Duration ước theo ngân sách lời của đoạn Voice, ~110–130 từ/phút),
không phải một con số cố định riêng cho ảnh tĩnh. Ảnh tĩnh giữ nguyên khung hình, chỉ áp Ken
Burns (zoom in/out chậm, pan ngang/dọc nhẹ) trong suốt Duration đó.

**Quan trọng:** quyết định Clip hay Ảnh tĩnh là việc của **pipeline sản xuất** (bước Scene
Generator/chọn công cụ, sau khi Master Script đã viết xong), giống hệt nguyên tắc ở mục 0 —
**Master Script KHÔNG tự đánh dấu cảnh nào là Clip/Ảnh tĩnh**, để giữ kịch bản tool-agnostic
(không phải sửa lại Master Script mỗi khi đổi kỹ thuật sản xuất).

---

## 2. THỨ TỰ ƯU TIÊN MẶC ĐỊNH

| Loại cảnh | Công cụ mặc định |
|---|---|
| Nhân vật kể chuyện | Kling |
| Nhân vật cận cảnh | Veo 3 |
| Thiên nhiên | Hailuo |
| Đồ vật | Hailuo |
| Bối cảnh/không gian | Hailuo |
| Ẩn dụ hình ảnh | Hailuo |
| Montage (dựng nhanh nhiều cảnh) | Runway |
| Chuyển cảnh | Runway |
| Cảnh chủ đạo (hero scene) | Veo 3 |

---

## 3. PHÂN LOẠI CẢNH TRƯỚC KHI CHỌN CÔNG CỤ

Luôn phân loại cảnh trước khi chọn công cụ. Các loại cảnh:

Nhân vật · Hội thoại · Anh Minh nói trực diện · Thiên nhiên · Đồ vật · Bối cảnh · Ẩn dụ hình
ảnh · Chuyển cảnh · Montage · Ký ức · Giấc mơ/hồi tưởng · Suy ngẫm · Biểu tượng.

---

## 4. BẢNG QUYẾT ĐỊNH CHI TIẾT

| Tình huống | Công cụ ưu tiên | Lý do / Công cụ thay thế |
|---|---|---|
| Anh Minh nói trực diện camera | **Veo 3** | Biểu cảm chân thực nhất |
| Anh Minh cận cảnh | **Veo 3** | Khuôn mặt là trọng tâm cảm xúc |
| Anh Minh trung cảnh | **Kling** | Thay thế: Veo 3 |
| Nhân vật chính trong câu chuyện (khách mời/nhân vật kể) | **Kling** | Giữ nhất quán khuôn mặt, trang phục, bối cảnh xuyên suốt tập |
| Cận cảnh cảm xúc của nhân vật chính | **Veo 3** | Biểu cảm vi mô thuyết phục hơn |
| Nhân vật đang đi | **Kling** | — |
| Nhân vật ngồi yên lặng | **Kling** | — |
| Nhân vật cầm đồ vật | **Kling** | — |
| Nhân vật tương tác bối cảnh | **Kling** | — |
| Rừng / Sông / Mưa / Gió / Mây / Bình minh / Hoàng hôn | **Hailuo** | — |
| Hơi khói cà phê / Sổ tay / Ảnh cũ / Ghế trống / Ánh sáng cửa sổ / Rèm bay | **Hailuo** | — |
| Hình ảnh biểu tượng | **Hailuo** | — |
| Cảnh thiết lập bối cảnh (establishing shot) | **Hailuo** | Thay thế: Runway |
| Không gian nội thất/ngoại thất | **Hailuo** | — |
| Cảnh chuyển tiếp | **Runway** | — |
| Camera reveal (mở dần khung hình) | **Runway** | — |
| Push chậm điện ảnh / Orbit chậm | **Runway** | — |
| Montage | **Runway** | — |
| Ẩn dụ hình ảnh trừu tượng | **Runway** | Thay thế: Hailuo |

---

## 5. TỐI ƯU CHI PHÍ

Hệ thống sản xuất nên tự động ưu tiên hiệu quả chi phí. **Trước hết, áp dụng Lớp quyết định 0
(mục 1B)** — loại phần lớn cảnh sang Ảnh giữ + Ken Burns, không tốn chi phí generate
video. Bảng % dưới đây chỉ áp dụng cho phần CÒN LẠI đã được xác định là cần Clip AI video (video
DÀI Mức 1: tối đa 3 Clip, xem mục 1B) — tức là % trong nội bộ "rổ Clip", không phải % trên tổng
số cảnh của cả video:

| Công cụ | Tỷ lệ (trong số cảnh đã chọn là Clip) | Dùng cho |
|---|---|---|
| **Veo 3** | ≈ 10% | Anh Minh nói trực diện · khoảnh khắc chủ đạo · cận cảnh cảm xúc |
| **Kling** | ≈ 45% | Nhân vật chính trong câu chuyện · cảnh kể chuyện · tương tác con người |
| **Hailuo** | ≈ 35% | Thiên nhiên/B-roll hiếm khi cần chuyển động thật — phần lớn trường hợp này nên là Ảnh tĩnh (mục 1B) thay vì Clip Hailuo; chỉ dùng Clip Hailuo khi B-roll đó thật sự cần chuyển động (nước chảy, khói bay, mưa rơi) |
| **Runway** | ≈ 10% | Chuyển cảnh · chuyển động máy quay · montage · tăng giá trị hình ảnh |

---

## 6. QUY TẮC LEO THANG (chỉ nâng cấp công cụ khi thật sự cần)

Luôn bắt đầu bằng công cụ rẻ nhất vẫn đạt đủ chất lượng cần thiết. Chỉ leo thang khi cần thiết.

Ví dụ:

Thiên nhiên → Hailuo · Cảnh kể chuyện nhân vật → Kling · Cận cảnh cảm xúc → Veo 3.

Không bao giờ dùng Veo 3 cho B-roll đơn giản. Không bao giờ dùng Veo 3 cho hơi khói cà phê.
Không bao giờ dùng Veo 3 cho cảnh phong cảnh thông thường.

Chất lượng cao cấp chỉ dành cho khoảnh khắc thật sự quan trọng về cảm xúc.

---

## 7. CẬP NHẬT CÔNG CỤ TRONG TƯƠNG LAI

File này định nghĩa **loại cảnh**, không phải ràng buộc cứng theo tên công cụ cụ thể.

Nếu sau này có công cụ mới vượt trội hơn cho một loại cảnh nào đó, chỉ cần sửa bảng ánh xạ
trong file này. Kịch bản (Master Script), quy tắc viết prompt (`video_ai_prompt_rules.md`) và
ngoại hình nhân vật (`core-brain/image_style_bible.md`) không cần đổi.

---

## 8. NGUYÊN TẮC CUỐI CÙNG

Khán giả không bao giờ biết cảnh nào được tạo bởi công cụ nào.

Họ chỉ biết câu chuyện có cảm thấy thật hay không.

Chọn công cụ phục vụ câu chuyện — không phải công cụ có tên nghe hoành tráng nhất.
