# SCORING RULES — MỨC ĐỘ NGHIÊM TRỌNG & QUYẾT ĐỊNH CUỐI (REVIEW FACTORY)

> Tải lên khu **Files** của Review Factory. Quy định cách gắn mức độ nghiêm trọng cho lỗi và
> suy ra quyết định cuối. KHÔNG dùng điểm số (0–100) — AI tự chấm điểm số là cảm tính, không
> đáng tin. Dùng đúng 4 mức quyết định: **PASS / PASS WITH NOTE / NEED FIX / FAIL**.
> Cập nhật: 04/07/2026.

---

## 1. BA MỨC ĐỘ NGHIÊM TRỌNG

| Mức | Định nghĩa | Ví dụ |
|---|---|---|
| **Critical** | Vi phạm ranh giới an toàn/CORE_BRAIN, hoặc sai sự thật nghiêm trọng | Claim y khoa quá mức (chẩn đoán/kê đơn/cam kết điều trị), thông tin sức khỏe bịa đặt, nội dung dọa bệnh/giật gân |
| **Major** | Thiếu yêu cầu bắt buộc trong checklist gốc, ảnh hưởng chất lượng/chuẩn xuất bản | Thiếu Meta Description, thiếu FAQ, sai Output Schema, thiếu disclaimer, lệch Search Intent |
| **Minor** | Lỗi nhỏ không ảnh hưởng an toàn hay chuẩn xuất bản, chỉ ảnh hưởng độ mượt | Một câu hơi dài, một H2 hơi lặp ý nhẹ, anchor text hơi cứng |

## 2. QUY TẮC SUY RA QUYẾT ĐỊNH CUỐI

```
Có ít nhất 1 lỗi Critical       → FAIL
Không Critical, có ít nhất 1 Major → NEED FIX
Không Critical/Major, có Minor  → PASS WITH NOTE
Không lỗi nào                  → PASS
```

- **FAIL:** không được xuất bản/sử dụng cho tới khi Factory gốc sửa lại và review lại từ đầu.
- **NEED FIX:** cần sửa các mục Major trước khi xuất; có thể xuất tạm nếu người dùng chấp nhận rủi ro đã ghi rõ.
- **PASS WITH NOTE:** có thể xuất bản ngay; các Minor chỉ mang tính ghi nhận, không bắt buộc sửa.
- **PASS:** đạt chuẩn hoàn toàn theo checklist.

## 3. NGUYÊN TẮC GẮN MỨC ĐỘ

- Một lỗi chỉ thuộc **đúng một mức** — không gắn cả Critical và Major cho cùng một lỗi.
- Khi không chắc một lỗi là Major hay Minor, chọn mức **cao hơn** (thận trọng hơn là bỏ sót).
- Không tự hạ mức Critical xuống Major để "cho qua" — nếu nghi ngờ có claim y khoa vượt mức,
  luôn giữ Critical và để người phụ trách xác nhận lại.
- **KHÔNG cộng dồn Minor để tự nâng mức quyết định.** VD: 20 lỗi Minor vẫn là **PASS WITH
  NOTE**, KHÔNG tự suy diễn thành NEED FIX vì "nhiều Minor quá nên chắc là nghiêm trọng". Công
  thức ở mục 2 là cố định theo MỨC ĐỘ NGHIÊM TRỌNG cao nhất tìm thấy, không theo SỐ LƯỢNG lỗi.
  Nếu một Factory thực sự lặp lại quá nhiều Minor tới mức đáng lo, đó là tín hiệu để ghi vào
  **Suggestions** (`output_schema.md`) cho người phụ trách biết — không phải lý do tự đổi
  Final Decision.
