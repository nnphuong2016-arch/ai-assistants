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

Hệ thống sản xuất nên tự động ưu tiên hiệu quả chi phí. Phân bổ khuyến nghị cho một tập video
chuẩn:

| Công cụ | Tỷ lệ | Dùng cho |
|---|---|---|
| **Veo 3** | ≈ 10% | Anh Minh nói trực diện · khoảnh khắc chủ đạo · cận cảnh cảm xúc |
| **Kling** | ≈ 45% | Nhân vật chính trong câu chuyện · cảnh kể chuyện · tương tác con người |
| **Hailuo** | ≈ 35% | Thiên nhiên · đồ vật · bối cảnh · hình ảnh biểu tượng · establishing shot |
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
