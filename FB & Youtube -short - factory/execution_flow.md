# EXECUTION FLOW

Version: 4.0
Cập nhật: 17/10/2026

Purpose:
Điều phối toàn bộ Short Factory.

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

Input → Understand → Think → Plan → Write → Review → Output

---

# STEP 1
Understand Request

Mục tiêu: hiểu đúng yêu cầu. Không được viết ngay.

Xác định:

- Chủ đề
- Người nghe
- Mục đích
- Cảm xúc mong muốn

Nếu chủ đề chưa rõ:

Interactive Mode: hỏi lại để làm rõ trước.

Automation Mode: KHÔNG hỏi lại (theo `output_schema.md`). Tự thu hẹp đầu vào thành một ý duy nhất rồi đi tiếp.
Chọn ý gần đời sống nhất trong các cách hiểu có thể.

---

# STEP 2
Select Topic

Sử dụng `topic_map.md` để xác định Topic chính → Topic phụ → các chủ đề liên quan.

Chỉ chọn một Topic chính. Không trộn nhiều chủ đề.

Xoay vòng chủ đề: không viết liên tiếp hai Short cùng một nhóm (xem Topic Rotation ở `topic_map.md`).

**Chống lặp (bắt buộc):** đọc 5–8 dòng gần nhất của `short_log.md` (và liệt kê thư mục Drive đích, kể cả file mang tiền tố
`DONE_`/`SHORTDONE_`, nếu có công cụ). Ghi nhớ kiểu mở, ẩn dụ trung tâm, khung kể và kiểu kết của chúng — chọn ý và cách
kể KHÁC. Chống lặp không chỉ theo chủ đề mà theo cả bốn thứ đó, kẻo "bài nào cũng giống bài nào".

---

# STEP 3
Generate Ideas

Ba nguồn:

1. **Chủ đề do người vận hành đưa trực tiếp** — một chủ đề, một câu nói, một câu chuyện, một tình huống. Đây là
   nguồn ƯU TIÊN CAO NHẤT: khi có, bỏ qua nguồn 2, đi thẳng sang STEP 3.5. Nếu đầu vào quá rộng, tự thu hẹp thành
   một ý duy nhất trước khi đi tiếp.
2. `bai-dang-Facebook-Anh-Minh.md` (gốc repo `ai-assistants/`) — kho 210 hook/chủ đề, 7 series (Có những.../Đôi khi.../Hóa
   ra.../Đừng vội.../Nếu hôm nay.../Điều đáng nghĩ hôm nay/Một phút nhìn lại). Dùng khi người vận hành KHÔNG đưa
   chủ đề cụ thể. Nếu người dùng chỉ định số dòng → dùng đúng dòng đó. Nếu không, liệt kê thư mục Drive đích rồi
   ưu tiên dòng CHƯA có Short. Dòng trong kho chỉ là **điểm vào** — không đọc nguyên câu hook làm bài, vẫn phải qua
   Lọc an toàn (STEP 3.5), Hook (STEP 4), Framework (STEP 5) và Writing Craft (STEP 7) như ý tưởng tự sinh.
3. `idea_library.md` — tự sinh khi hai nguồn trên không đủ, hoặc khi cần thêm hướng tiếp cận cho cùng một chủ đề.

Không rút ngắn bài SEO hay kịch bản video dài để làm Short — viết lại từ đầu như một câu chuyện để nghe
(`instructions_short.md` mục 5A).

**Tạo ĐÚNG 3 góc tiếp cận** khác nhau cho cùng ý (ví dụ: Quan sát · Trải nghiệm · Nghịch lý · Ký ức chung · Câu hỏi · Một khoảnh
khắc) rồi chọn góc mạnh nhất. Không chọn góc nghĩ ra đầu tiên.

Với góc đã chọn, xác định ngay:

- **Một chi tiết cụ thể hình dung được** (mâm cơm nguội, chuông báo thức lần thứ ba, đôi dép trước cửa…) — thay cho một loạt câu
  triết lý.
- **Một chuyển biến** trong cách nhìn: từ cách nghĩ nào sang điều nhận ra nào.

Kiểm tra ý đó (xem thêm `idea_library.md` mục 11): nói được trong hai câu; có góc nhìn riêng; kể được bằng một tình huống cụ
thể; và **đủ cho một trong ba cỡ** ở `writing_rules.md` mục 6.1 (không quá lớn để phải nhồi, không quá mỏng để phải kéo dài).

Chọn luôn cỡ (Nhanh / Tiêu chuẩn / Kể chuyện) ở bước này.

---

# STEP 3.5
Safety Filter

Bắt buộc. Không bỏ qua.

Kho hook và ý tưởng tự sinh đều KHÔNG được coi là đã an toàn — kể cả dòng lấy từ kho.

Đối chiếu ý tưởng vừa chọn với `writing_rules.md` mục 4.1.

Loại ngay nếu ý tưởng chứa:

- Dọa bệnh.
- Hàm ý cơ thể đang suy yếu mà ta không biết.
- Hàm ý sẽ phải trả giá về sau.
- Nói về diễn tiến bệnh.
- Chỉ số xét nghiệm.
- Tên cơ quan nội tạng làm chủ đề chính.

Ví dụ

Không dùng

Sức khỏe mất đi rất chậm, đến mức ta tưởng nó vẫn còn nguyên vẹn.

Cơ thể tha thứ rất nhiều, nhưng không tha thứ mãi mãi.

Dùng

Sức khỏe thay đổi rất chậm, chậm đến mức ta quên để ý tới nó.

Cơ thể chịu đựng rất giỏi, nên càng cần được nghỉ đúng lúc.

Cùng một quan sát. Bỏ phần dọa. Giữ phần thấu hiểu.

Nếu ý tưởng không qua được bước này: quay lại STEP 3.

---

# STEP 4
Choose Hook

Sử dụng `hook_library.md`. Chọn kiểu câu mở phù hợp (Observation, Question, Memory, Contradiction, Image, Tiny
Story...).

Câu mở phải phù hợp chủ đề, đọc thành tiếng trong dưới năm giây, và có thể nghe hiểu ngay — người xem không có
cơ hội đọc lại. Không dùng câu mở chỉ để gây tò mò.

---

# STEP 5
Choose Framework

Sử dụng `short_frameworks.md`. Chọn một cấu trúc phù hợp (F01–F16) và đọc phần "Khi nào chọn / khi nào không" của nó.

Framework quyết định nhịp bài — đường đi từ câu mở đến câu kết. Lập **đường dây** trước khi viết: mở → phát triển → nhận ra
→ kết, mỗi nhịp một dòng ghi chú ngắn (chỉ để mình dùng, không xuất).

Chọn khung KHÁC khung của hai Short liền trước (`short_log.md`).

---

# STEP 6
Choose Emotion

Sử dụng `emotion_palette.md`. Chọn TRƯỚC khi viết, không phải sau.

Cảm xúc quyết định cách chọn chi tiết và nhịp câu — chọn sau thì chỉ còn cách tô thêm, và bài sẽ lộ ra là đang
cố tạo cảm xúc.

Chọn một cảm xúc chính, tối đa một cảm xúc phụ. Không chọn cảm xúc mạnh. Chỉ cần đúng cảm xúc.

---

# STEP 7
Write Draft

Sử dụng đồng thời `writing_rules.md` và `writing_craft.md`.

Giữ đúng cảm xúc đã chọn ở STEP 6. Viết theo khuôn file Short (`output_schema.md`): mỗi ý một đoạn ngắn, câu kết có
dư âm (mặc định là một câu hỏi tự vấn in đậm; đổi kiểu theo `writing_rules.md` mục 8 để khỏi lặp).

Trong bước này: không kiểm tra, không sửa. Chỉ tập trung viết.

---

# STEP 8
Compare Examples

Sử dụng `short_examples.md`. Không sao chép. Chỉ so sánh.

Kiểm tra: Có đang giống AI? Có đang giống bài báo? Có đang giống SEO? Có đang giống một kịch bản mẫu?

Nếu có: viết lại.

---

# STEP 9
Quality Review

Sử dụng `quality_check.md` — **hai tầng**: Tầng 1 là cổng (an toàn, đúng khuôn, trong giới hạn hệ thống); Tầng 2 là chấm chất
lượng (câu mở, chuyển biến, kết có dư âm, không giống bài gần đây, phép thử "bỏ tên Anh Minh đi").

Đếm độ dài thật (số từ, số ký tự) và **đọc nhẩm thành tiếng một lượt** — chỗ nào vấp, chỗ nào dài hơi thở, sửa từ gốc.
Rớt Tầng 1 hoặc rớt Tầng 2 theo ngưỡng: quay lại đúng bước hỏng.

---

# STEP 10
Output Format

Sử dụng `output_schema.md`. Xuất hai khối: **A. File kịch bản** (tên file + dòng tiêu đề `# …` + lời đọc) và **B. Gói đăng và
nhật ký** (thông tin nội bộ, Reel Caption, Log Row).

Không thêm giải thích. Không thêm ghi chú. Không tự nhận xét. Chỉ xuất bài.

**Sau khi đăng:** thêm dòng `Log Row` vào `short_log.md`; khoảng 7 ngày sau điền số liệu và bài học. Dùng chúng ở STEP 2–5
cho các Short tiếp theo.

---

# Complete Flow

Request → Topic → Ideas → Safety Filter → Hook → Framework → Emotion → Draft → Examples → Quality → Output

---

# Retry Logic

Nếu hook yếu → quay lại Step 4.

Nếu ý tưởng yếu → quay lại Step 3.

Nếu ý tưởng chạm ranh giới an toàn → quay lại Step 3. Không sửa nhẹ để lách.

Nếu cấu trúc chưa ổn → quay lại Step 5.

Nếu cảm xúc sai → quay lại Step 6.

Nếu bài viết cứng → quay lại Step 7.

Nếu chất lượng chưa đạt → quay lại Step 9.

Không sửa chắp vá. Luôn sửa từ đúng bước.

---

# Priority Order

Khi có xung đột, ưu tiên theo thứ tự:

1. instructions_short.md
2. execution_flow.md
3. writing_rules.md
4. writing_craft.md
5. quality_check.md
6. short_frameworks.md
7. emotion_palette.md
8. bai-dang-Facebook-Anh-Minh.md (kho 210 hook — gốc repo `ai-assistants/`)
9. idea_library.md
10. hook_library.md
11. topic_map.md
12. short_examples.md
13. output_schema.md

---

# Design Principles

Mỗi bước chỉ làm một việc. Không gộp. Không bỏ qua. Không đảo thứ tự. Luôn hoàn thành bước trước mới sang bước
sau.

---

# Failure Recovery

Nếu bài viết:

- Lan man
- Thiếu cảm xúc
- Giống AI
- Quá học thuật
- Quá dài (vượt trần ký tự)
- Quá nhiều lời khuyên
- Có chỗ đọc thành tiếng bị vấp

Không sửa từng câu. Quay lại bước tạo ý tưởng hoặc chọn Framework. Sửa từ gốc.

---

# Success Criteria

Tiêu chí hoàn thành nằm ở **một nơi duy nhất**: `quality_check.md`.

Bài được coi là hoàn thành khi qua trọn `quality_check.md`.

Nhắc lại một điều duy nhất, vì nó có ngưỡng riêng: Nhóm 1 An toàn — sai một mục là viết lại. Không có ngoại lệ.

---

# Final Principle

Short Factory không được tối ưu để viết nhanh.

Short Factory được tối ưu để tạo ra đoạn lời đọc mà người nghe cảm thấy:

"Đây giống như một người thật vừa nói ra điều mình đang nghĩ."

Đó là mục tiêu cuối cùng của toàn bộ quy trình.
