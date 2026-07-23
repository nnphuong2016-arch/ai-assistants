# VIDEO AI PROMPT RULES — QUY TẮC VIẾT PROMPT DÙNG CHUNG MỌI CÔNG CỤ (VIDEO FACTORY)

> Tải lên khu **Files** của Video Factory. File này gộp lại từ 4 file riêng lẻ trước đó
> (veo3/hailuo/runway/kling_prompt_rules.md — bản gốc tiếng Anh, tham khảo từ dự án khác) vì
> phần lớn nội dung 4 file đó **giống nhau ~80%** giữa các công cụ — chỉ khác nhau ở vài điểm
> kỹ thuật riêng (xem mục 12). Gộp lại để tránh 4 nơi định nghĩa gần như cùng một quy tắc rồi
> lệch nhau khi sửa.
> **Ngoại hình nhân vật Anh Minh KHÔNG định nghĩa lại ở đây** — luôn dùng
> `core-brain/image_style_bible.md` (nguồn DUY NHẤT). File này chỉ nói cách viết prompt, không
> nói nhân vật trông thế nào.
> Chọn công cụ nào cho cảnh nào → xem `model_selection_rules.md`. File đó và file này **luôn đi
> cùng nhau**, không dùng file này mà không tra `model_selection_rules.md` trước.
> Cập nhật: 20/07/2026 — dịch + gộp từ 4 file gốc tiếng Anh (veo3/hailuo/runway/kling_prompt_
> rules.md, dự án tham khảo khác, nhân vật "Brian Chen") thành 1 file tiếng Việt, thay bằng
> Hiền triết Anh Minh. Xoá 4 file gốc sau khi gộp.
> Cập nhật: 23/07/2026 — sửa mục 11 + bảng mục 12: chốt độ dài tối đa thực tế theo công cụ (Veo
> 3 = 8s, Kling = 10s/lần generate), khớp với con số "6–10 giây" đang dùng ở `video_rules.md` +
> `video_ai_contract.md` + `model_selection_rules.md` cho cảnh Anh Minh img2video.

---

## 0. TRIẾT LÝ GỐC

Prompt hiệu quả nhất khi mô tả cảnh **như thật**, không phải như lệnh kỹ thuật.

Đừng viết prompt kiểu liệt kê lệnh máy quay. Hãy mô tả điều một nhà quay phim sẽ quan sát thấy.

Mục tiêu không phải kiểm soát từng pixel — mục tiêu là truyền tải đúng **cảm giác** của cảnh.

---

## 1. BẢN SẮC HÌNH ẢNH (áp dụng mọi công cụ)

Mỗi khung hình nên mang cảm giác: **tĩnh lặng · chân thật · con người · tự nhiên · lắng đọng ·
phi thời gian**.

Tránh: phong cách quảng cáo · phong cách MV ca nhạc · thẩm mỹ mạng xã hội · quảng cáo hàng
xa xỉ · hoành tráng kiểu điện ảnh Hollywood.

---

## 2. PHONG CÁCH ĐIỆN ẢNH

Hướng tới: chân thực tuyệt đối · ánh sáng tự nhiên · kết cấu da chân thực · quang học đời
thực · chuyển động hữu cơ · màu phim dịu nhẹ · chân thực kiểu phim tài liệu.

Tránh: giả tưởng · render cách điệu · dáng vẻ CGI · da nhựa · xử lý hậu kỳ quá tay.

*(Bảng màu & ánh sáng cụ thể → tham chiếu `core-brain/image_style_bible.md` mục 5, không định
nghĩa lại riêng ở đây — tránh 2 nơi cùng nói về bảng màu rồi lệch nhau.)*

---

## 3. MÔ TẢ CẢNH

Mô tả cảnh như đang giải thích cho một nhà quay phim nghe. Ưu tiên nói rõ: ai đang ở đó → đang
làm gì → ở đâu → ánh sáng ra sao → khán giả nên cảm thấy gì.

Tránh liệt kê một chuỗi từ khóa rời rạc — ngôn ngữ tự nhiên, có mạch, hiệu quả hơn nhiều.

---

## 4. NGÔN NGỮ MÁY QUAY

Chuyển động máy quay luôn phải có mục đích.

Ưu tiên: tripod cố định · push-in nhẹ nhàng · dolly chậm · handheld nhẹ · bố cục tĩnh ·
chuyển động ngang chậm.

Tránh: whip pan · crash zoom · drone bay nhanh · góc quay kiểu action camera · chuyển động quá
kịch tính.

---

## 5. DIỄN XUẤT CON NGƯỜI

Nhân vật nên cử động rất tự nhiên, tiết chế: thở nhẹ · chớp mắt chậm · một khoảng ngập ngừng ·
cử chỉ nhỏ · tư thế tự nhiên · biểu cảm khuôn mặt vi tế.

Tránh diễn xuất cường điệu, phóng đại.

**Anh Minh không bao giờ trông như đang diễn.** Anh Minh đồng hành, không biểu diễn.

---

## 6. LỜI THOẠI TRONG CLIP

Hệ thống Funamark tách riêng lời dẫn (voiceover) khỏi hình ảnh (theo mô hình 2 lớp LỜI/HÌNH đã
có ở `video_rules.md` mục 0).

Clip do AI tạo ra thường **không nên có**: lời thoại phát ra trực tiếp trong clip, lip-sync.
Nhân vật có thể cử động tự nhiên nhưng lời dẫn được lồng riêng ở hậu kỳ.

---

## 7. MÔI TRƯỜNG/BỐI CẢNH

Mỗi bối cảnh nên có chi tiết đời sống thật, đáng tin: sách · cây xanh · tách trà/cà phê · chăn
gấp gọn · vân gỗ · giấy cũ · rèm mềm.

Tránh không gian vô trùng, quá sạch sẽ, thiếu sức sống.

---

## 8. TÍNH NHẤT QUÁN XUYÊN CẢNH

Giữ nguyên suốt cả tập video: trang phục · kiểu tóc · độ tuổi · đạo cụ · hướng ánh sáng · bối
cảnh · thời tiết.

Không "thiết kế lại" nhân vật giữa các cảnh.

---

## 9. NHÂN VẬT KHÁCH (không phải Anh Minh)

Mỗi tập/câu chuyện giới thiệu một nhân vật khách (người trong câu chuyện đang kể) riêng —
không dùng lại ngoại hình từ tập khác trừ khi cố ý nối tiếp câu chuyện.

Ngoại hình nhân vật khách nên khớp tự nhiên với: độ tuổi · nghề nghiệp · bối cảnh sống · nội
dung câu chuyện.

*(Khác với nhân vật khách: Anh Minh LUÔN theo đúng `core-brain/image_style_bible.md`, không
đổi giữa các tập.)*

---

## 10. B-ROLL MANG TÍNH BIỂU TƯỢNG

Thiên nhiên mang tính biểu tượng. Ví dụ: dòng sông chảy · sương sớm · ánh sáng ban mai · lá
lay động · ghế trống · hơi khói cà phê · sổ tay cũ · mưa trên cửa sổ.

Mỗi hình ảnh biểu tượng phải làm rõ thêm cho lời dẫn — không dùng biểu tượng chỉ vì đẹp, không
gắn với nội dung.

---

## 11. ĐỘ DÀI CẢNH & CẤU TRÚC PROMPT

**Độ dài generate khuyến nghị:** 4–10 giây/clip tuỳ công cụ (xem bảng chi tiết mục 12) — Veo 3
tối đa thực tế **8 giây**/lần generate, Kling tối đa thực tế **10 giây**/lần generate (đây là lý
do các cảnh Anh Minh dùng img2video Kling/Veo3 được tính "gốc 6–10 giây" ở `video_rules.md` mục
6 + `model_selection_rules.md` mục 1B). Cảnh dài hơn nên được ghép từ nhiều clip hoặc kéo dài
cảm giác bằng zoom/pan/crop ở bước dựng (xem `video_ai_contract.md` Stage 7), không yêu cầu
generate một clip cực dài.

**Thứ tự viết prompt khuyến nghị** (thứ tự có thể xê dịch nhẹ tuỳ công cụ):

Bối cảnh → Chủ thể → Hành động → Môi trường → Ánh sáng → Cảm xúc/tâm trạng → Máy quay →
Chuyển động → Phong cách hình ảnh → Chất lượng kỹ thuật → Negative Prompt.

---

## 11B. PROMPT ẢNH TĨNH + KEN BURNS (khác với prompt Clip)

> Thêm 23/07/2026 — theo mô hình hybrid ở `model_selection_rules.md` mục 1B, phần lớn cảnh
> (~69–72% với video TRUNG/DÀI) là **Ảnh tĩnh + hiệu ứng zoom/pan (Ken Burns)** ở bước dựng,
> không phải Clip AI video. Prompt cho ảnh tĩnh (Flux hoặc công cụ ảnh khác, xem
> `video_ai_contract.md` Stage 3) khác Clip ở vài điểm:

- **Chừa khoảng trống bố cục (headroom):** không đặt chủ thể chính sát mép khung hình — pan/zoom
  ở bước dựng sẽ cắt bớt viền ảnh, chủ thể sát mép dễ bị crop mất.
- **Một điểm nhìn rõ ràng, không nhồi nhiều chủ thể:** Ken Burns hiệu quả nhất khi ảnh có 1 tiêu
  điểm để mắt máy quay ảo "dịch chuyển tới/lui" — ảnh quá nhiều chi tiết ngang hàng làm hiệu ứng
  mất tự nhiên.
- **Độ phân giải/tỷ lệ ảnh cao hơn khung xuất** (nếu công cụ cho phép chọn) — để còn dư biên khi
  zoom in mà không vỡ nét.
- Các nguyên tắc còn lại (bản sắc hình ảnh, phong cách điện ảnh, môi trường, tính nhất quán) áp
  dụng y hệt mục 1–10 — chỉ khác ở bố cục chừa biên nói trên.

---

## 12. KHÁC BIỆT RIÊNG TỪNG CÔNG CỤ (thay cho 4 file riêng trước đây)

| | **Veo 3** | **Kling** | **Hailuo** | **Runway** |
|---|---|---|---|---|
| Mạnh nhất ở | Biểu cảm khuôn mặt, cận cảnh cảm xúc | Nhất quán nhân vật xuyên cảnh | Tốc độ, chi phí thấp, thiên nhiên/B-roll | Bố cục, chuyển động máy quay |
| Độ dài clip khuyến nghị | 5–8 giây (**tối đa thực tế 8s/lần generate**) | 5–10 giây (**tối đa thực tế 10s/lần generate**) | 4–6 giây (có thể 5–8s) | 5–8s (mặc định), 8–10s (suy ngẫm), 4–6s (macro), 6–8s (môi trường) |
| Tránh dùng cho | B-roll đơn giản, thiên nhiên (lãng phí chi phí) | Cận cảnh cảm xúc mạnh (dùng Veo 3 thay) | Hội thoại dài, nhiều nhân vật tương tác, cần nhất quán khuôn mặt chính xác | Diễn xuất nhân vật kéo dài |
| Đặc điểm prompt | Ngôn ngữ tự nhiên đầy đủ câu, tránh nhồi từ khóa | — | Prompt càng ngắn gọn càng hiệu quả, tránh chỉ dẫn quá kỹ thuật | Mỗi prompt chỉ mô tả **một** cảnh/một ý — không gộp nhiều ý trong 1 prompt |

---

## 13. NEGATIVE PROMPT (dùng chung mọi công cụ)

Luôn tránh: hoạt hình (cartoon) · anime · minh hoạ (illustration) · CGI · da nhựa · chữ · logo
· watermark · phụ đề chèn cứng · vật thể lơ lửng phi lý · giải phẫu biến dạng · chất lượng
thấp · màu bão hoà quá mức · biểu cảm khuôn mặt giả tạo.

---

## 14. VÍ DỤ

**Kịch bản (LỜI):** "Ánh sáng buổi sáng lọt qua căn bếp yên tĩnh, hơi khói bốc lên từ tách cà
phê bị bỏ quên."

**Prompt HÌNH (Hailuo, ví dụ):**
"Ánh nắng sớm ấm áp tràn vào căn bếp ngoại ô yên tĩnh, hơi khói nhẹ bốc lên từ tách cà phê gốm
đặt trên mặt bàn gỗ. Rèm cửa khẽ lay theo làn gió nhẹ, bóng đổ dịch chuyển tự nhiên trong
phòng. Không khí bình yên, lắng đọng, có cảm giác đã sống ở đó lâu. Bố cục tĩnh, push-in chậm.
Chân thực tuyệt đối. Màu phim dịu tự nhiên. Bảng màu tông đất nhẹ nhàng. Không chữ. Không
watermark. Không CGI."

---

## 15. NGUYÊN TẮC CUỐI CÙNG

Prompt hiệu quả nhất khi đọc như một người đang kể chuyện, không phải như lệnh phần mềm.

Mô tả khoảnh khắc. Mô tả cảm xúc. Mô tả ánh sáng. Mô tả chuyển động.

Đừng mô tả thuật toán.

Nếu người xem quên mất rằng đây là hình do AI tạo ra — prompt đã thành công.
