# Day 02 Lab — Individual Problem Scan


# Phase 1 — Individual Scan: tìm 5+ problems (25')

## Bảng scan
| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Ôn bài kiến thức từ nhiều buổi, trên nhiều nền tảng LMS, Github, bài tập thực hành | Học viên | Lặp lại gần như mỗi ngày |
| 2 | Pain từ người khác | Học viên hỏi lại Lab Coach về những câu hỏi gần tương tự nhau | Lab Coach | Nhiều lần / tuần |
| 3 | Tốn thời gian | Thời gian làm báo cáo với mỗi dự án thường kéo dài và thao tác thủ công | Thành viên dự án | 90-210phút |
| 4 | AI có thể làm tốt hơn | Hệ thống hoá kiến thức | Học viên | Lặp lại sau mỗi ngày học |
| 5 | AI có thể tốt hơn | Gợi ý roadmap ôn tập cá nhân dựa trên bài yếu | Học viên | AI có thể cá nhân hoá |
| 6 | Pain từ người khác | Lab Coach khó phân loại, nhận biết học viên đang kẹt phần nào | Lab Coach, Học viên | Số lượng học viên quá đông, tỉ lệ nghịch với số lượng Lab Coach |
| 7 | Tốn thời gian | Debug bài làm mà chưa biết lỗi xuất phát từ chỗ nào | Học viên | Nhiều giờ |


---

# Phase 2 — Top 3 Problem Cards + draft workflow (35')

### Chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|------|---------|-------------|-------------------|
| 1 | Debug bài làm mà chưa biết lỗi xuất phát từ chỗ nào | Tốn nhiều thời gian, ảnh hưởng tiến độ học tập và project. | AI có thể chưa hỗ trợ tốt cho nhiều stack khác nhau. |
| 2 | Học viên hỏi lại Lab Coach về những câu hỏi gần tương tự nhau | Lab Coach phải trả lời lặp lại nhiều lần. | Học viên có thể chưa tin tưởng AI. |
| 3 | Ôn bài kiến thức từ nhiều buổi, trên nhiều nền tảng LMS, Github, bài tập thực hành | Kiến thức phân tán, khó tổng hợp và theo dõi. | Khó đồng bộ dữ liệu, cá nhân hoá và chưa xác định rõ output. |

## Problem Card #1 - Debug bài làm mà chưa biết lỗi xuất phát từ chỗ nào.

```text
Problem 1 câu: Học viên mất nhiều thời gian debug vì không xác định được nguyên nhân lỗi nằm ở code, logic hay môi trường chạy.

Actor: Học viên làm bài tập

Thời điểm / bối cảnh: Trong lúc làm lab, assignment hoặc project cá nhân.

Current workflow 3-7 bước:
1. Code feature hoặc làm bài tập
2. Chạy chương trình và gặp lỗi
3. Tự đọc error log
4. Search Google / StackOverflow
5. Sửa thử nhiều cách khác nhau
6. Hỏi bạn bè hoặc Lab Coach
7. Debug lại từ đầu

Bottleneck:
Không xác định được root cause nên thử sai rất nhiều lần.

Impact:
Mất nhiều giờ, giảm động lực học tập và chậm tiến độ project.

Success metric:
- Giảm thời gian debug trung bình
- Tăng số lỗi tự xử lý được
- Giảm số lần hỏi Lab Coach cho lỗi cơ bản

Non-AI alternative:
- Viết checklist debug chuẩn
- FAQ lỗi phổ biến
- Pair programming

AI hypothesis:
AI có thể đọc error log, phân tích code và gợi ý nguyên nhân lỗi cùng hướng sửa nhanh hơn.

Quick gut:
Agent

```

### Draft workflow cho Problem Card #1


```text
CURRENT STATE — 2-4 giờ

[Code bài]
→ [Run lỗi]
→ [Đọc log]
→ [Google lỗi]
→ [Sửa thử nhiều cách] <-- bottleneck
→ [Hỏi Lab Coach]
→ [Fix được hoặc vẫn lỗi]

FUTURE STATE — 15-30 phút

[Paste code + error]
→ [AI phân tích root cause]
→ [AI gợi ý hướng fix]
→ [Học viên thử fix]
→ [Run lại]
→ [Lab Coach hỗ trợ nếu vẫn fail] <-- human boundary

Fallback: AI phân tích sai → học viên hỏi Lab Coach
```

### Problem Card #2 - Học viên hỏi lại Lab Coach về những câu hỏi gần tương tự nhau

```text
Problem 1 câu:
Lab Coach phải trả lời lặp đi lặp lại nhiều câu hỏi tương tự nhau từ học viên.

Actor:
Lab Coach

Thời điểm / bối cảnh:
Trong giờ lab hoặc khi support online qua chat nhóm.

Current workflow 3-7 bước:
1. Học viên gặp vấn đề
2. Gửi câu hỏi vào nhóm chat
3. Lab Coach đọc câu hỏi
4. Trả lời thủ công
5. Học viên khác hỏi câu tương tự
6. Lab Coach trả lời lại

Bottleneck:
Thông tin bị lặp nhiều lần và không có hệ thống tra cứu tập trung.

Impact:
Lab Coach mất thời gian, phản hồi chậm và khó tập trung cho vấn đề khó hơn.

Success metric:
- Giảm số câu hỏi lặp
- Giảm thời gian phản hồi trung bình
- Tăng số câu được tự giải quyết

Non-AI alternative:
- Tạo FAQ thủ công
- Tài liệu onboarding
- Discord pinned messages

AI hypothesis:
AI có thể tự động gợi ý câu trả lời từ lịch sử chat và tài liệu trước đó.

Quick gut:
[x] Workflow
[x] Agent
```

### Draft workflow cho Problem #2


```text
CURRENT STATE — 20-40 phút / buổi

[Học viên hỏi]
→ [Lab Coach đọc]
→ [Tìm context cũ]
→ [Trả lời thủ công]
→ [Câu hỏi lặp lại] <-- bottleneck
→ [Tiếp tục support]

FUTURE STATE — 3-10 phút

[Học viên hỏi]
→ [AI detect câu hỏi tương tự]
→ [AI suggest FAQ / answer]
→ [Học viên tự đọc]
→ [Lab Coach review nếu cần] <-- human boundary

Fallback: AI trả lời chưa đúng → Lab Coach trả lời trực tiếp
```
### Problem Card #3 - Ôn bài kiến thức từ nhiều buổi, nhiều nền tảng

```text
Problem Card #3: Học viên khó tổng hợp và ôn tập kiến thức vì tài liệu nằm rải rác trên nhiều nền tảng khác nhau (LMS, Github, bài tập thực hành).

Actor:
Học viên tại Chương trình AI Thực chiến.

Thời điểm / bối cảnh: Học viên tự chủ động ôn lại bài với lượng kiến thức khổng lồ trước mỗi buổi kiểm tra hoặc sau mỗi buổi học.

Current workflow:
1. Mở LMS để xem slide/tài liệu bài học.
2. Mở repo GitHub để xem code mẫu hoặc bài thực hành.
3. Mở bài tập cũ để đối chiếu cách làm.
4. Tự tổng hợp lại kiến thức vào note cá nhân hoặc tự ôn lại.

Bottleneck:
Kiến thức bị phân tán trên nhiều nguồn, học viên phải tự tìm kiếm và nối thông tin thủ công trước khi thật sự bắt đầu ôn tập.

Impact:
- Tốn nhiều thời gian chỉ để tìm và tổng hợp tài liệu.
- Dễ bỏ sót context hoặc kiến thức quan trọng.
- Giảm hiệu quả ôn tập trước lab/quiz/deadline.
- Học viên dễ bị quá tải khi phải chuyển đổi liên tục giữa nhiều nền tảng.

Success metric:
- Giảm thời gian chuẩn bị ôn tập từ khoảng 60-90 phút xuống còn dưới 20-30 phút mỗi ngày.
- Giảm số lần phải chuyển đổi nền tảng khi review kiến thức.
- Học viên tìm được tài liệu liên quan trên dưới 2 phút.
- Tăng mức độ hoàn thành bài tập đúng hạn.

Non-AI alternative:
- Chuẩn hoá cấu trúc tài liệu học tập.
- Gom toàn bộ tài nguyên vào một Notion/Drive/NotebookLM chung.
- Tạo checklist tóm tắt theo từng buổi học.
AI hypothesis:
- Tổng hợp tài liệu từ nhiều nguồn
- Tạo summary theo từng topic/buổi học
- Gợi ý resource liên quan
- Sinh checklist ôn tập hoặc flashcard dựa trên nội dung đã học
Quick gut:
Workflow 

```

### Draft workflow cho problem #3


```text
CURRENT WORKFLOW — ~60-90 phút
[Bắt đầu ôn tập]
↓
[Mở LMS để xem slide/tài liệu: 10-15']
↓
[Tìm lại discussion/Q&A trên Discord: 10-20']
↓
[Mở GitHub/repo để xem code mẫu hoặc lab cũ: 10-15']
↓
[Đọc lại bài tập thực hành và note cá nhân: 10-20']
↓
[Tự nối context và tổng hợp kiến thức: 20-30']
↑
BOTTLENECK
(context phân tán, nhiều nguồn)
↓
[Bắt đầu thật sự ôn tập hoặc làm bài]
FUTURE WORKFLOW — ~15-30 phút
[Chọn topic/buổi học cần review]
↓
[Workflow tự pull dữ liệu từ:
LMS + GitHub + Lab notes]
↓
[AI tổng hợp:
•	key concepts
•	code examples
•	Q&A liên quan
•	checklist ôn tập]
↓
[AI tạo structured review page / summary]
↓
[Học viên review + chỉnh sửa note cá nhân]
↑
HUMAN BOUNDARY
(người học tự kiểm tra và hiểu)
↓
[Bắt đầu ôn tập hoặc làm bài]
Fallback nếu AI sai hoặc thiếu context:
[Học viên mở lại source gốc]
↓
[Đọc trực tiếp slide/repo/discussion]
↓
[Tự xác minh kiến thức]

```
## Chọn card muốn pitch nhất

Card tôi muốn pitch nhất:

```text
#3 - Ôn bài kiến thức từ nhiều buổi, trên nhiều nền tảng LMS, GitHub, bài tập thực hành
```

Vì sao:

```text
• Problem xảy ra gần như mỗi ngày với học viên.
• Workflow và bottleneck khá rõ.
• Có thể đo impact bằng thời gian ôn tập và thời gian tìm tài liệu.
• Có dữ liệu thật từ LMS, GitHub, Discord, lab cũ.
```

Câu hỏi tôi muốn nhóm challenge:

```text
• Pain lớn nhất là tìm tài liệu hay nối context giữa các nguồn?
• Nếu tự tổ chức tài liệu tốt hơn thì còn cần AI không?
• AI nên hỗ trợ bước nào là hiệu quả nhất?
```


