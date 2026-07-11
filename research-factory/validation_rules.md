# VALIDATION RULES — XÁC NHẬN THÔNG TIN (RESEARCH FACTORY)

> Tải lên khu **Files** của Research Factory. Quy định khi nào một thông tin được coi là đủ tin
> cậy để đưa vào Knowledge Package, và cách đánh dấu khi chưa đủ.
> Cập nhật: 04/07/2026.

---

## 1. YÊU CẦU TỐI THIỂU

- Mỗi thông tin quan trọng (định nghĩa, khuyến nghị, số liệu) nên có **ít nhất 2 nguồn** đồng
  thuận trước khi ghi nhận với Confidence cao. Một nguồn duy nhất vẫn có thể dùng, nhưng
  Confidence tối đa chỉ ở mức **Medium**.
- Nguồn thuộc Mức 1 (`source_rules.md`) một mình vẫn có thể đạt Confidence **High** nếu nội
  dung rõ ràng, không mơ hồ.

## 2. ĐÁNH DẤU KHI CHƯA ĐỦ

| Tình huống | Đánh dấu |
|---|---|
| Chưa tìm được nguồn đủ tin cậy | `Need Verification` |
| Nguồn tìm được đã cũ (VD: hướng dẫn y tế >3–5 năm, giá sản phẩm đã lỗi thời) | `Update Needed` |
| Hai nguồn đáng tin mâu thuẫn nhau | Ghi cả hai, `Confidence: Medium/Low`, không tự kết luận |
| Chỉ có nguồn Mức 3 hoặc thấp hơn | Ghi rõ mức nguồn, `Confidence: Low` |

## 3. THANG CONFIDENCE (khớp cách dùng ở SEO Factory)

Dùng đúng 3 mức — không dùng điểm số:

- **High** — nguồn Mức 1/2 rõ ràng, nhất quán giữa các nguồn.
- **Medium** — có nguồn nhưng chỉ một nguồn, hoặc nguồn Mức 2/3, hoặc có mâu thuẫn nhẹ.
- **Low** — nguồn yếu, mâu thuẫn đáng kể, hoặc chưa xác minh được.

## 4. KHÔNG TỰ NÂNG CONFIDENCE ĐỂ "CHO GỌN"

Không tự nâng mức Confidence vì muốn Knowledge Package "nhìn hoàn chỉnh hơn". Factory nhận dữ
liệu (SEO Factory...) cần biết đúng mức độ chắc chắn thật để tự quyết định có dùng thông tin đó
hay không.
