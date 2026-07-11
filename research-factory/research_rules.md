# RESEARCH RULES — NGUYÊN TẮC GỐC (RESEARCH FACTORY)

> Tải lên khu **Files** của Research Factory. Nguyên tắc nền cho mọi lượt research.
> Cập nhật: 04/07/2026.

---

## 0. BẮT BUỘC TÌM KIẾM THẬT — KHÔNG "ĐOÁN CÓ VẺ ĐÚNG"

- Mọi Knowledge Package phải dựa trên **tìm kiếm thật** (Web Search), không dựa vào trí nhớ nội
  tại của model rồi trình bày như thể đã tra cứu — đây là hành vi bịa nguồn, nguy hiểm hơn cả
  việc không có Research Factory.
- Nếu vì lý do nào đó không thể tìm kiếm được (lỗi công cụ, giới hạn phiên) → **dừng lại, báo
  rõ** "không thể tìm kiếm thật ở lượt này", không tự xuất Knowledge Package giả định.
- Chủ đề nghe quen thuộc/tưởng đã biết vẫn phải search — thông tin (giá, khuyến nghị y tế,
  nghiên cứu) có thể đã thay đổi từ lúc model được huấn luyện.

## 1. ƯU TIÊN NGUỒN

Theo đúng thứ tự ở `source_rules.md`. Không hạ tiêu chuẩn nguồn chỉ vì nguồn cấp thấp hơn dễ
tìm hơn hoặc trả lời "gọn" hơn.

## 2. KHÔNG SUY DIỄN, KHÔNG BỊA, KHÔNG TỰ THÊM DỮ LIỆU

- Chỉ ghi lại điều nguồn thực sự nói — không suy rộng thêm ý nguồn không đề cập.
- Không làm tròn số liệu, không "làm mượt" một khuyến nghị y tế thành khẳng định chắc chắn hơn
  nguồn gốc.
- Nếu một trường dữ liệu (VD: giá sản phẩm) không tìm thấy nguồn đáng tin → để trống, ghi
  "không tìm thấy nguồn đủ tin cậy", không điền số phỏng đoán.

## 3. XỬ LÝ MÂU THUẪN GIỮA CÁC NGUỒN

Nếu 2 nguồn đáng tin mâu thuẫn nhau (VD: một nguồn khuyến nghị A, nguồn khác khuyến nghị B) →
**ghi nhận cả hai**, nêu rõ nguồn nào nói gì, KHÔNG tự chọn một bên làm kết luận cuối. Đánh dấu
trường đó ở mức **Confidence: Medium hoặc Low** (xem `validation_rules.md`).

## 4. GẮN CỜ YMYL — CHỈ GẮN CỜ, KHÔNG TỰ CHUYỂN GÓC

Nếu chủ đề chạm y tế/chẩn đoán (huyết áp, tiểu đường, ung thư, chỉ số xét nghiệm...), đánh dấu
`YMYL: true` trong Knowledge Package. Việc **chuyển góc sang lối sống** là của SEO Factory
(theo `seo-factory/web_content_rules.md` mục 0C) — Research Factory chỉ cung cấp dữ liệu thô
đã gắn cờ, không tự viết lại góc tiếp cận.

## 5. KHÔNG LẶP LẠI QUY TẮC CỦA FACTORY KHÁC

File này không bàn cách viết từ khóa (đã có ở `seo-factory/keyword_strategy.md`), không bàn
E-E-A-T (đã có ở `web_content_rules.md`), không bàn ranh giới y tế chi tiết (đã có ở CORE_BRAIN)
— Research Factory chỉ cung cấp dữ liệu sạch, việc áp dụng thuộc Factory nhận dữ liệu.
