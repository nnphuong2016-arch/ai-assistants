# EXECUTION FLOW

Version: 2.0

Purpose:
Điều phối toàn bộ Facebook Factory.

File này không sinh nội dung.

Không chứa quy tắc viết.

Không chứa prompt.

Nó chỉ định nghĩa trình tự làm việc.

Nếu các file khác trả lời:

"Viết cái gì?"

"Viết như thế nào?"

Thì file này trả lời:

"Làm theo thứ tự nào?"

---

# Core Workflow

Input

↓

Understand

↓

Think

↓

Plan

↓

Write

↓

Review

↓

Output

---

# STEP 1
Understand Request

Mục tiêu:

Hiểu đúng yêu cầu.

Không được viết ngay.

Xác định:

- Chủ đề
- Đối tượng đọc
- Mục đích
- Cảm xúc mong muốn

Nếu chủ đề chưa rõ.

Phải làm rõ trước.

---

# STEP 2
Select Topic

Sử dụng

topic_map.md

Để xác định:

Topic chính

↓

Topic phụ

↓

Các chủ đề liên quan

Chỉ chọn một Topic chính.

Không trộn nhiều chủ đề.

---

# STEP 3
Generate Ideas

Hai nguồn song song (cập nhật 20/07/2026):

1. `bai-dang-Facebook-Anh-Minh.md` (gốc repo `ai-assistants/`) — kho 210 hook có sẵn, 7 series
   (Có những.../Đôi khi.../Hóa ra.../Đừng vội.../Nếu hôm nay.../Điều đáng nghĩ hôm nay/Một phút
   nhìn lại). Nếu người dùng chỉ định số dòng → dùng đúng dòng đó. Nếu không, ưu tiên dòng CHƯA
   dùng gần đây trong file này trước.
2. `idea_library.md` — tự sinh khi file ở trên không có hook hợp chủ đề đang cần, hoặc khi cần
   nhiều ý tưởng hơn 210 dòng có sẵn.

Sinh nhiều hướng tiếp cận.

Ví dụ:

- Quan sát
- Trải nghiệm
- Nghịch lý
- Ký ức
- Câu hỏi
- Một khoảnh khắc

Không chọn ý đầu tiên.

Tạo nhiều lựa chọn.

Sau đó chọn ý mạnh nhất.

Hook/dòng từ `bai-dang-Facebook-Anh-Minh.md` chỉ là **điểm vào** — không copy nguyên câu làm
bài hoàn chỉnh, vẫn phải qua Hook (STEP 4), Framework (STEP 5), Writing Craft (STEP 6) như ý
tưởng tự sinh.

---

# STEP 4
Choose Hook

Sử dụng

hook_library.md

Chọn kiểu Hook phù hợp.

Ví dụ

Observation

Question

Memory

Contradiction

Image

Tiny Story

Hook phải phù hợp chủ đề.

Không dùng Hook chỉ để gây tò mò.

---

# STEP 5
Choose Framework

Sử dụng

post_frameworks.md

Chọn cấu trúc phù hợp.

Ví dụ

Observation

↓

Realization

↓

Reflection

Hoặc

Story

↓

Lesson

↓

Open Ending

Framework quyết định nhịp bài.

---

# STEP 6
Write Draft

Sử dụng đồng thời:

writing_rules.md

writing_craft.md

Trong bước này.

Không kiểm tra.

Không sửa.

Chỉ tập trung viết.

---

# STEP 7
Inject Emotion

Sử dụng

emotion_palette.md

Kiểm tra:

Bài đang mang cảm xúc gì?

Ví dụ

- Bình yên
- Nhẹ nhàng
- Đồng cảm
- Hy vọng
- Biết ơn

Không cố tạo cảm xúc mạnh.

Chỉ cần đúng cảm xúc.

---

# STEP 8
Compare Examples

Sử dụng

post_examples.md

Không sao chép.

Chỉ so sánh.

Kiểm tra:

Có đang giống AI?

Có đang giống bài báo?

Có đang giống SEO?

Nếu có.

Viết lại.

---

# STEP 9
Quality Review

Sử dụng

quality_check.md

Kiểm tra toàn bộ.

Ví dụ

Một ý?

Một cảm xúc?

Một câu chuyện?

Có hình ảnh?

Có khoảng lặng?

Có dạy đời?

Có lặp?

Có quá dài?

Có quá nhiều giải thích?

Nếu chưa đạt.

Quay lại Step 6.

---

# STEP 10
Output Format

Sử dụng

output_schema.md

Xuất đúng định dạng.

Không thêm giải thích.

Không thêm ghi chú.

Không tự nhận xét.

Chỉ xuất bài.

---

# Complete Flow

Request

↓

Topic

↓

Ideas

↓

Hook

↓

Framework

↓

Draft

↓

Emotion

↓

Examples

↓

Quality

↓

Output

---

# Retry Logic

Nếu Hook yếu.

Quay lại Step 4.

Nếu ý tưởng yếu.

Quay lại Step 3.

Nếu cấu trúc chưa ổn.

Quay lại Step 5.

Nếu bài viết cứng.

Quay lại Step 6.

Nếu cảm xúc sai.

Quay lại Step 7.

Nếu chất lượng chưa đạt.

Quay lại Step 9.

Không sửa chắp vá.

Luôn sửa từ đúng bước.

---

# Priority Order

Khi có xung đột.

Ưu tiên theo thứ tự:

1.

instructions_facebook.md

↓

2.

execution_flow.md

↓

3.

writing_rules.md

↓

4.

writing_craft.md

↓

5.

quality_check.md

↓

6.

post_frameworks.md

↓

7.

emotion_palette.md

↓

8.

bai-dang-Facebook-Anh-Minh.md (nguồn hook có sẵn — gốc repo `ai-assistants/`)

↓

9.

idea_library.md

↓

10.

hook_library.md

↓

11.

topic_map.md

↓

12.

post_examples.md

↓

13.

output_schema.md

---

# Design Principles

Mỗi bước.

Chỉ làm một việc.

Không gộp.

Không bỏ qua.

Không đảo thứ tự.

Luôn hoàn thành bước trước.

Mới sang bước sau.

---

# Failure Recovery

Nếu bài viết:

- Lan man
- Thiếu cảm xúc
- Giống AI
- Quá học thuật
- Quá SEO
- Quá dài
- Quá nhiều lời khuyên

Không sửa từng câu.

Quay lại bước tạo ý tưởng hoặc chọn Framework.

Sửa từ gốc.

---

# Success Criteria

Một bài viết được xem là hoàn thành khi:

✓ Có đúng một ý chính.

✓ Có Hook tự nhiên.

✓ Có cấu trúc rõ ràng.

✓ Có ít nhất một hình ảnh đời thường.

✓ Có nhịp đọc tốt trên điện thoại.

✓ Có cảm xúc nhất quán.

✓ Không dạy đời.

✓ Không giống AI.

✓ Không giống bài SEO.

✓ Không giống bài báo.

✓ Kết mở tự nhiên.

✓ Đúng định dạng đầu ra.

Nếu thiếu một tiêu chí.

Bài viết chưa hoàn thành.

---

# Final Principle

Facebook Factory không được tối ưu để viết nhanh.

Facebook Factory được tối ưu để tạo ra bài viết mà người đọc cảm thấy:

"Đây giống như một người thật vừa chia sẻ điều mình đang nghĩ."

Đó là mục tiêu cuối cùng của toàn bộ quy trình.