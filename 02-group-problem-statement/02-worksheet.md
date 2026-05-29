# Day 02 Lab — Group Problem Statement



# Phase 3 — Group Convergence: từ 9-12 candidates về 1 (30')

## Bước 3.1 — Trình bày top 3



| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cảm nhận nhanh |
|---|---|---|---|---|---|
| 1 | Đào Duy Quyền | Tìm kiếm và trích xuất số liệu từ các file báo cáo PDF dài | Sinh viên | Tìm đúng chỗ có số liệu và xác nhận số liệu trong bảng/biểu mất nhiều thời gian, dễ bỏ sót. | Vấn đề cũng cần thiết đối với người cần tìm hiểu tài liệu. Tuy nhiên, các công cụ hỗ trợ như NotebookLM hiện nay đang làm rất tốt. Có thể giải quyết |
| 2 | Đào Duy Quyền | Sau khi chat nhóm kết thúc, trưởng nhóm mất thời gian biến các đoạn trao đổi rời rạc thành checklist việc làm rõ ràng, có owner và deadline. | Trưởng nhóm | Thông tin rải rác, nhiều đoạn chat không liên tục, task và owner dễ bị lẫn. | Nên có nút kích hoạt cho việc này với context được thống nhất chứ không thể để bot đọc hết cả tất cả đoạn chat, dễ gây hiểu nhầm hay tràn bộ nhớ cho bot tổng hợp |
| 3 | Đào Duy Quyền | Lớp trưởng hoặc trưởng ban phải trả lời lặp lại cùng một thông tin, quy định và lịch trình cũ trên Discord vì thành viên không tìm lại được thông báo gốc.| Lớp trưởng | Tìm lại thông tin cũ và trả lời lặp lại liên tục. | Có thể ghim các thông tin hoặc có 1 nơi như GG Sheet hay GG Calendar để liệt kê các việc cần làm  liên quan cho kế hoạch hiện tại hoặc sắp tới |
| 4 | Yến Phương | Debug Bug & Tìm Root Cause | Developer | Phân tích stack trace để tìm ra nguyên nhân gốc rễ (mapping error message -> root cause) giữa hàng chục file dependency và tài liệu rải rác. | Pain thật, technical mạnh nhưng scope dễ bị quá lớn |
| 5 | Yến Phương | Screening Paper AI | Sinh viên AI, Researcher | Đọc hiểu chi tiết kỹ thuật từ paper dài (thường 8-15 trang) để đối chiếu mức độ tương thích với bài toán thực tế của mình. | Có nhu cầu rõ, nhưng cần niche cụ thể để tránh quá rộng |
| 6 | Yến Phương| Đọc hiểu source code cũ khi onboarding | Developer | Tự lần theo luồng code phức tạp và suy đoán mục đích logic của tác giả cũ. | Workflow thực tế, dễ thấy giá trị nếu đúng target user |
| 7 | Khánh An| Học viên hỏi lại Lab Coach về những câu hỏi gần tương tự nhau | Lab Coach, học viên | Lab Coach phải đọc lại context và trả lời lặp lại nhiều câu hỏi tương tự mỗi tuần | Pain lặp rõ nhưng có thể xử lý bằng process trước |
| 8 | Khánh An|Debug bài làm mà chưa biết lỗi xuất phát từ chỗ nào | Học viên  | Học viên mất nhiều thời gian đọc error, search tài liệu và thử sai trước khi xác định được nguyên nhân thật sự | Pain mạnh, dễ validate với học viên |
| 9 | Khánh An | Ôn bài kiến thức từ nhiều buổi, trên nhiều nền tảng LMS, Github, bài tập thực hành | Học viên | Học viên tự chủ động ôn lại bài với lượng kiến thức khổng lồ trước mỗi buổi kiểm tra hoặc sau mỗi buổi học. | Có nhu cầu thật nhưng cần scope rõ hơn |


## Bước 3.2 — Gom trùng / cluster

Nhóm tiến hành phân loại các candidate thành các cụm chủ đề chung để dễ đánh giá:

| Cluster | Candidates included | Pattern chung | Ghi chú |
|---|---|---|---|
| **A. Trích xuất & tổng hợp thông tin** | Candidate 1, 5, 9 | Gom thông tin/số liệu từ tài liệu dài (PDF, Paper, LMS) để phục vụ học tập, nghiên cứu. | Pain lớn về thời gian đọc hiểu và lọc thông tin. |
| **B. Tối ưu hóa giao tiếp & quản lý** | Candidate 2, 3, 7 | Biến đổi thông tin giao tiếp (chat nhóm, câu hỏi trùng lặp) thành checklist hoặc FAQ. | Lặp lại thường xuyên trong quản lý nhóm/lớp học. |
| **C. Debug & khắc phục lỗi kỹ thuật** | Candidate 4, 8 | Hỗ trợ developer và học viên tìm nguyên nhân lỗi code từ log/stack trace. | Pain rất lớn nhưng scope kỹ thuật rộng. |


## Bước 3.3 — Shortlist


| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
|---|---|---|
| Sau khi chat nhóm kết thúc, trưởng nhóm mất thời gian biến các đoạn trao đổi rời rạc thành checklist việc làm rõ ràng, có owner và deadline. | Actor khá rõ, workflow thật và rất quen thuộc, bottleneck nằm ở việc bóc action item từ thread rời rạc. Impact đo được bằng thời gian tổng hợp và số task bị quên/hỏi lại. Dễ vẽ before/after workflow và so sánh Rule / Workflow / Agent. | Cần kiểm tra xem team đã có format chốt việc sẵn chưa. Nếu đã có template tốt thì mức pain giảm, nhưng thường vẫn đủ rõ để pitch. |
| Debug Bug & Tìm Root Cause| Workflow debug là workflow thật, actor developer rõ, bottleneck cụ thể ở mapping error message -> root cause giữa nhiều file dependency và tài liệu rải rác. Impact có thể đo bằng thời gian tìm nguyên nhân gốc và số vòng thử sai. Dễ so sánh Rule / Workflow / Agent. | Scope dễ bị quá rộng nếu không chốt một stack, một loại bug, hoặc một bối cảnh cụ thể. Có nguy cơ trượt sang troubleshooting chung chung. |
| Ôn bài kiến thức từ nhiều buổi, trên nhiều nền tảng LMS, Github, bài tập thực hành | Actor là học viên khá rõ, workflow ôn tập sau buổi học và trước kiểm tra là workflow thật, pain lặp lại và có thể đo bằng thời gian chuẩn bị bài và mức độ nhớ lại. Có thể vẽ before/after workflow nếu chốt được output ôn tập. | Còn hơi rộng vì nguồn quá nhiều (LMS, GitHub, bài tập, note), chưa rõ output cuối là summary, flashcard hay question set. Cần thu hẹp scope trước khi deep-dive. |

## Bước 3.4 — Score để đồng thuận

Chấm 1-5. Điểm không cần tuyệt đối; mục tiêu là ép nhóm nói rõ lý do.

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Chat nhóm -> checklist công việc | 5 | 5 | 3 | 4 | 4 | 4 | 5 | 30 |
| Debug & Tìm Root Cause | 5 | 3 | 3 | 3 | 2 | 5 | 4 | 25 |
| Ôn kiến thức đa nguồn | 5 | 4 | 3 | 3 | 3 | 5 | 4 | 27 |

Candidate nhóm chọn: **Chat nhóm -> checklist công việc**


Vì sao chọn:
- Bài này có actor rất rõ, workflow thật và rất quen thuộc, bottleneck nằm đúng ở bước bóc action item từ thread rời rạc. 
- Impact đo được bằng thời gian tổng hợp và số task bị bỏ sót hoặc phải hỏi lại. 
- Scope đủ nhỏ để làm trong lab hôm nay và dễ so sánh Rule / Workflow / Agent.


Vì sao không chọn các candidate còn lại:
- Debug & Root Cause có pain thật nhưng scope dễ rộng quá, nếu không chốt rõ stack, kiểu bug và bối cảnh thì rất dễ trượt sang troubleshooting chung chung. 
- Ôn bài từ nhiều nguồn là nhu cầu thật nhưng hiện còn hơi rộng, chưa chốt rõ output ôn tập là summary, flashcard hay question set nên khó đi sâu ngay.

Nếu có disagreement, nhóm xử lý thế nào:

- Nhóm sẽ quay lại 3 tiêu chí chốt: bài nào scope nhỏ nhất, hiểu workflow thật nhất, và đo được nhanh nhất trong lab hôm nay. 
- Nếu vẫn ngang nhau, ưu tiên bài mà cả nhóm có thể validate ngay bằng một ví dụ workflow thật.


---

# Phase 4 — Quick Validation + Research giải pháp (30')



## Bước 4.1 — Quick validation

| Nguồn | Số người | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Quick interview | 3 | 2/3 người nói sau khi chat xong đều phải đọc lại thread để bóc task, owner, deadline; bước đau nhất là tổng hợp lại thành checklist. | 1 người nói nếu team có template chốt việc sẵn thì pain giảm khá nhiều. | Thu hẹp problem thành biến thread chat sau thảo luận thành checklist có owner/deadline, không ôm toàn bộ chat. |
| Mini poll | 7 | 5/7 người gặp vấn đề ít nhất mỗi tuần; phần đau nhất là task trôi và không rõ ai phụ trách. | 2/7 người đã có pinned template hoặc summary sẵn nên ít đau hơn. | Giữ hướng Workflow, thêm non-AI alternative là template + rule chốt việc |
| Review thread| 2 thread | Trong thread thật có nhiều follow-up, task bị nhắc lại, và có đoạn không rõ owner.| Chưa đủ log để kết luận rộng, cần thêm mẫu thật nếu muốn chắc hơn.| Dùng thêm 2-3 thread thật làm evidence trước khi chốt Problem Statement.|

**Kết luận nhanh**

- Pain có thật và lặp lại.
- Bước đau nhất là chuyển hội thoại rời rạc thành checklist có owner/deadline.
- Non-AI alternative vẫn có giá trị, nên bài này hợp với Workflow hơn là Agent.
- Nếu làm sâu, scope nên giữ ở mức: chat nhóm -> checklist công việc, không mở rộng thành chatbot tổng quát.

## Bước 4.2 — Research giải pháp đã có


| Nguồn / tool / case  | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|
|[SlackAI](https://slack.com/help/articles/25076892548883-Guide-to-AI-features-in-Slack) | Tóm tắt channel, DM, thread; search theo nội dung trong Slack | Native ngay trong nơi chat diễn ra, rất hợp để “catch up” nhanh | Dừng chủ yếu ở tóm tắt và tìm kiếm, chưa tự biến hội thoại thành checklist có owner/deadline |Nếu nguồn là Slack, bước đầu tiên nên là summarize thread rồi mới chuyển sang checklist | 
|[Discord In-Channel Conversation Summaries](https://support.discord.com/hc/en-us/articles/12926016807575-In-Channel-Conversation-Summaries) | Tóm tắt các cuộc hội thoại trong channel thành topic và snippet | Hữu ích để đọc lại cuộc trò chuyện dài | Tính năng còn là experiment, giới hạn server, và không nhắm vào task extraction | Nếu nhóm dùng Discord, native AI hiện nghiêng về catch-up chứ chưa phải tasking | 
|[Notion AI Meeting Notes](https://www.notion.com/help/ai-meeting-notes) | Transcribe cuộc họp, rút key points và action items | Có sẵn luồng từ hội thoại sang action items, có citation | Thiên về meeting transcript hơn là chat thread rời rạc; cần quyền audio/screen | Đây là pattern tốt: AI đọc nội dung hội thoại rồi bóc ra action items, nhưng vẫn trong bối cảnh có cấu trúc | 
|[CLickUp AI](https://clickup.com/ai) | Lấy action items từ docs, chats, meetings và biến thành task / plan| Có chats trong input | Hợp nhất khi team đã làm việc trong ClickUp; vẫn cần kiểm tra lại output trước khi giao việc | Có bằng chứng mạnh rằng bài toán này hợp với Workflow hơn là Agent|


---

# Phase 5 — Workflow + Problem Statement (45')

## Bước 5.1 — Current workflow bản nhóm

```text
CURRENT STATE — chat nhóm -> checklist công việc

+------------------------------------------------------------------+
| 1. Paste thread log                                              |
| Actor      : Trưởng nhóm / người tổng hợp                        |
| Input      : Thread chat sau khi trao đổi xong                   |
| Output     : Thread log đã gom lại                               |
| Time/freq  : 5-10 phút / mỗi lần                                 |
| Handoff    : Group chat -> người tổng hợp                        |
| Bottleneck : Thread dài, nhiều đoạn rời rạc, khó đọc lại theo    |
|              thứ tự                                              |
+------------------------------------------------------------------+
                                  |
                                  v
+------------------------------------------------------------------+
| 2. AI tạo checklist có owner và deadline                         |
| Actor      : AI hỗ trợ                                           |
| Input      : Thread log đã paste                                 |
| Output     : Draft checklist (task / owner / deadline)           |
| Time/freq  : 1-3 phút / mỗi lần                                  |
| Handoff    : Người tổng hợp -> AI                                 |
| Bottleneck : Bóc task thiếu ngữ cảnh hoặc gán owner/deadline sai |
+------------------------------------------------------------------+
                                  |
                                  v
+------------------------------------------------------------------+
| 3. Trưởng nhóm sửa nhanh                                          |
| Actor      : Trưởng nhóm                                         |
| Input      : Draft checklist từ AI                               |
| Output     : Checklist đã chỉnh đúng                              |
| Time/freq  : 5-15 phút / mỗi lần                                 |
| Handoff    : AI -> người phụ trách                                |
| Bottleneck : Phải kiểm lại task trùng, thiếu, hoặc owner lệch    |
+------------------------------------------------------------------+
                                  |
                                  v
+------------------------------------------------------------------+
| 4. Gửi bản cuối                                                  |
| Actor      : Trưởng nhóm                                         |
| Input      : Checklist cuối                                       |
| Output     : Bản chốt gửi cho cả nhóm                            |
| Time/freq  : 1-2 phút / mỗi lần                                  |
| Handoff    : Người phụ trách -> cả nhóm                           |
| Bottleneck : Nếu format chưa rõ, người nhận vẫn phải hỏi lại    |
+------------------------------------------------------------------+

Fallback: nếu chat quá rối / thiếu ngữ cảnh

+------------------------------------------------------------------+
| Dùng template thủ công                                           |
| Actor      : Trưởng nhóm                                         |
| Input      : Chat + template checklist chuẩn                     |
| Output     : Checklist thủ công                                  |
| Time/freq  : 10-20 phút / mỗi lần                                |
| Handoff    : Chat -> template -> người phụ trách -> cả nhóm      |
| Bottleneck : Tốn công điền lại nhưng ổn định hơn                 |
+------------------------------------------------------------------+

```

| Bước | Actor | Input | Output | Thời gian/tần suất | Handoff | Bottleneck |
|---|---|---|---|---|---|---|
| 1. Paste thread log | Trưởng nhóm / người tổng hợp | Thread chat sau khi trao đổi xong | Toàn bộ nội dung trao đổi được đưa vào một chỗ | 5-10 phút / mỗi cuộc trao đổi | Từ group chat sang người tổng hợp | Thread dài, nhiều đoạn rời rạc, khó đọc lại theo thứ tự |
| 2. AI tạo checklist có owner và deadline | AI hỗ trợ | Thread log đã paste | Draft checklist gồm task, owner, deadline, notes | 1-3 phút / mỗi lần tổng hợp | Từ người tổng hợp sang AI | AI có thể bóc task chưa chính xác hoặc thiếu ngữ cảnh |
| 3. Trưởng nhóm sửa nhanh | Trưởng nhóm | Draft checklist từ AI | Checklist đã chỉnh đúng ý nhóm | 5-15 phút / mỗi lần | Từ AI sang người phụ trách | Phải kiểm tra lại owner, deadline, task bị sót hoặc trùng |
| 4. Gửi bản cuối | Trưởng nhóm / người tổng hợp | Checklist đã sửa | Bản checklist cuối gửi cho cả nhóm | 1-2 phút / mỗi lần | Từ người phụ trách sang cả nhóm | Nếu format chưa rõ thì người nhận vẫn phải hỏi lại |



Bottleneck chính:

```text
biến thread chat rối thành checklist có owner/deadline đúng.
```

## Bước 5.2 — Future workflow bản nhóm

Dán workflow hoặc link file:

```text
FUTURE STATE — chat nhóm -> checklist công việc

+------------------------------------------------------------------+
| 1. Chuẩn hóa thread theo template                                |
| Actor      : Trưởng nhóm / người tổng hợp                        |
| Type       : Rule                                                |
| Input      : Thread chat raw                                     |
| Output     : Thread đã được gắn mốc, lọc bớt noise                |
| Time/freq  : 3-5 phút / mỗi lần                                  |
| Handoff    : Group chat -> template chuẩn                        |
| Bottleneck : Thread dài, thiếu cấu trúc, nhiều đoạn lạc chủ đề   |
+------------------------------------------------------------------+
                                  |
                                  v
+------------------------------------------------------------------+
| 2. AI draft checklist                                            |
| Actor      : AI hỗ trợ                                           |
| Type       : AI / Workflow                                       |
| Input      : Thread đã chuẩn hóa                                 |
| Output     : Draft checklist (task / owner / deadline / note)    |
| Time/freq  : 1-3 phút / mỗi lần                                 |
| Handoff    : Người tổng hợp -> AI                                |
| Bottleneck : AI có thể bóc thiếu task hoặc gán owner/deadline sai|
+------------------------------------------------------------------+
                                  |
                                  v
+------------------------------------------------------------------+
| 3. Trưởng nhóm review & chốt                                     |
| Actor      : Trưởng nhóm                                         |
| Type       : Human                                               |
| Input      : Draft checklist                                     |
| Output     : Checklist cuối                                      |
| Time/freq  : 5-10 phút / mỗi lần                                |
| Handoff    : AI -> người phụ trách                               |
| Boundary   : AI không tự chốt owner/deadline cuối                |
| Bottleneck : Phải kiểm lại task trùng, thiếu, hoặc lệch ngữ cảnh |
+------------------------------------------------------------------+
                                  |
                                  v
+------------------------------------------------------------------+
| 4. Gửi checklist theo format cố định                             |
| Actor      : Trưởng nhóm                                         |
| Type       : Rule                                                |
| Input      : Checklist cuối                                      |
| Output     : Bản chốt gửi cho cả nhóm                           |
| Time/freq  : 1-2 phút / mỗi lần                                 |
| Handoff    : Người phụ trách -> cả nhóm                          |
| Bottleneck : Nếu format chưa rõ, người nhận vẫn hỏi lại         |
+------------------------------------------------------------------+

Fallback: nếu chat quá rối / thiếu ngữ cảnh
        |
        v
+------------------------------------------------------------------+
| Dùng template thủ công trước                                     |
| Actor      : Trưởng nhóm                                         |
| Type       : Rule / manual                                       |
| Input      : Chat + template checklist                           |
| Output     : Checklist thủ công                                  |
| Time/freq  : 10-20 phút / mỗi lần                               |
| Handoff    : Chat -> template -> người phụ trách                 |
| Bottleneck : Tốn công nhưng ổn định hơn                          |
+------------------------------------------------------------------+
```

**Before/after impact:**

| Metric | Trước | Sau kỳ vọng | Ghi chú |
|---|---:|---:|---|
| Số bước | 5 | 4 | Giảm một bước xử lý trung gian |
| Tổng thời gian | 20-30 phút | 8-12 phút | Giảm mạnh ở đoạn đọc lại và bóc task |
| Số bước thủ công | 5 | 3 | Rule/template giúp giảm thao tác nặng |
| Bottleneck chính | Đọc thread rời rạc và bóc action item | Review và chốt owner/deadline | Bottleneck chuyển sang kiểm tra chất lượng |
| Risk mới | Chậm, dễ quên task, dễ phải hỏi lại | AI bóc sai task/owner/deadline, cần người review | Nếu chat quá rối thì phải fallback sang template thủ công |

## Bước 5.3 — Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Trưởng nhóm hoặc người tổng hợp sau khi cuộc thảo luận kết thúc. |
| **Workflow** | Thread chat kết thúc -> đọc lại nội dung rời rạc -> bóc action item -> gán owner/deadline -> gửi checklist cho cả nhóm. |
| **Bottleneck** | Đọc lại thread dài và rời rạc để chốt đúng task, owner và deadline. |
| **Impact** | Mỗi lần tổng hợp mất khoảng 20-30 phút, dễ bỏ sót task hoặc phải hỏi lại nhiều lần, làm chậm việc chốt đầu việc của cả nhóm. |
| **Success Metric** | Giảm thời gian tổng hợp checklist xuống dưới 10-15 phút và giảm số task bị bỏ sót / phải nhắc lại. |
| **Boundary** | AI chỉ hỗ trợ draft checklist; người thật vẫn phải review và chốt owner/deadline cuối cùng. Không để AI tự gửi bản cuối khi chưa được kiểm tra. |


# Phase 6 — Rule / Workflow / Agent + Decision (25')

## Bước 6.1 — So sánh Rule / Workflow / Agent

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **Rule** | Dùng template meeting notes + format chat cố định | Team nhỏ, ít discussion | Người dùng không follow format, vẫn phải đọc thủ công | |
| **Workflow** | AI đọc thread chat $\rightarrow$ extract Task/owner/deadline $\rightarrow$ tạo draft checklist | Discussion dài, nhiều task và nhiều người tham gia | AI hiểu sai context hoặc assign sai owner | ✓ |
| **Agent** | AI tự follow-up, nhắc deadline, tự phân công việc | Team lớn, workflow phức tạp nhiều giai đoạn | Over-engineering, khó kiểm soát | |


**Mức chọn:** Workflow

**Vì sao chọn:**
- Workflow xử lý khá tuần tự và rõ ràng.
- AI chủ yếu hỗ trợ:
    - summarize
    - extract action items
    - format checklist
- Có human boundary rõ:
    - trưởng nhóm review trước khi gửi.
- Không cần AI tự ra quyết định hoặc tự điều phối nhóm.

**Vì sao không chọn mức đơn giản hơn:**
- Rule có thể giảm một phần pain nhưng không giải quyết được:
    - chat rời rạc
    - context phân tán
    - discussion không theo format
- Người dùng thường không duy trì format chat cố định trong thời gian dài.

## Bước 6.2 — Problem Statement v1

| Field | Nội dung |
|---|---|
| **Actor** | Trưởng nhóm hoặc người tổng hợp sau khi cuộc thảo luận kết thúc. |
| **Workflow** | Chat nhóm kết thúc -> chuẩn hóa nội dung theo template -> AI draft checklist -> trưởng nhóm review/chốt -> gửi checklist cuối cho cả nhóm. |
| **Bottleneck** | Bóc action item từ thread rời rạc và chốt đúng owner/deadline. |
| **Impact** | Mỗi lần tổng hợp checklist mất khoảng 20-30 phút; nếu làm chậm hoặc sai sẽ khiến task bị trôi, phải hỏi lại, và chậm tiến độ cả nhóm. |
| **Success Metric** | Giảm thời gian tổng hợp xuống dưới 10-15 phút, giảm số task bị bỏ sót hoặc phải nhắc lại, và không tăng số lỗi owner/deadline. |
| **Boundary** | AI chỉ được draft checklist; người thật vẫn phải kiểm tra owner, deadline, và nội dung cuối cùng trước khi gửi. Không cho AI tự chốt hoặc tự gửi bản cuối nếu chưa review. |
| **AI intervention point** | Sau khi thread đã được chuẩn hóa theo template, trước bước trưởng nhóm review và chốt checklist cuối. |
| **Mức chọn** | Workflow |
| **Rủi ro & người thật kiểm tra** | Rủi ro: AI bóc thiếu task, gán sai owner/deadline, hoặc hiểu sai ngữ cảnh. Người thật kiểm tra: trưởng nhóm phải rà lại task, owner, deadline và quyết định cuối trước khi gửi. |

## Bước 6.3 — Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú |
|---|---|---|
| Actor và workflow đã rõ chưa? | Yes | Actor là trưởng nhóm/người tổng hợp; workflow chat -> bóc task -> chốt owner/deadline -> gửi checklist khá rõ. |
| Baseline và success metric đã đo được chưa? | Not Yet | Mới có ước lượng từ quick validation, chưa có log đo thật trên nhiều thread. |
| Có data/input đủ dùng chưa? | Yes | Có thread chat thật hoặc sample thread đủ để pilot nhỏ. |
| Nếu AI sai, hậu quả có chấp nhận được không? | Yes | Vì người thật vẫn review trước khi gửi bản cuối. |
| Có người review/owner vận hành không? | Yes | Trưởng nhóm là người chốt cuối và chịu trách nhiệm. |
| Có cách non-AI đơn giản hơn không? | Yes | Template + pinned format + checklist thủ công có thể xử lý phần lớn. |

**Decision:**

```text
Go với scope nhỏ.
```

**Pilot nhỏ nhất:**

```text
Dùng 2-3 thread chat thật của một nhóm nhỏ trong 2 tuần gần nhất.
Chạy workflow bán thủ công: người tổng hợp paste thread đã chuẩn hóa vào prompt chuẩn.
AI draft checklist.
Trưởng nhóm edit và đo thời gian sửa + số lỗi phải sửa.
```

**Exit / rollback:**

```text
Nếu trưởng nhóm vẫn phải viết lại hơn 70% draft trong 2 tuần liên tiếp, hạ xuống template + checklist thủ công.
Nếu AI bóc sai task hoặc gán sai owner/deadline, không cho dùng trực tiếp bản draft trong checklist cuối.
```

**Decision rationale:**

```text
Problem rõ, workflow rõ, metric rõ.
Có non-AI components.
AI nằm ở một bước cụ thể, không ôm toàn bộ workflow.
Human review rõ.
```


---
