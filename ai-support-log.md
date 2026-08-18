# AI Support Log — Đào Văn Đạt

| Mục | Nội dung |
|---|---|
| Họ và tên | Đào Văn Đạt |
| MHV | 2A202601302 |
| Team | ABC |
| Case | AI Tutor — Diagnostic Refresher |
| Vai trò | Option C — AI-led Recovery Path; facilitate Tester 3; tổng hợp bản nháp Group Feedback Synthesis sau test |
| Công cụ | ChatGPT/Codex |
| Ngày sử dụng | 17–18/08/2026 |

> **Phạm vi bài làm hiện tại:** Tôi chỉ hoàn thiện nội dung và flow của micro-prototype Option C; chưa xây dựng production product, model, API hoặc bản tương tác.

## AI đã hỗ trợ và tôi đã tự quyết định lại như thế nào

| AI đã giúp gì? | AI sai, hời hợt hoặc thiếu ở đâu? | Tôi đã tự sửa hoặc quyết định lại gì? |
|---|---|---|
| Hỗ trợ bóc tách transcript P03 thành facts, workaround, consequence và phần diễn giải A/B/C. | Bản diễn giải đầu từng gắn Pain B với tốc độ/cách giảng, không khớp định nghĩa B trong README nhóm. | Tôi xác nhận lại dữ liệu thật: thuật ngữ Harness, thời gian 13h15, mất khoảng 5 phút, lớp đi trước 5 slide và đã có consent ghi âm. Phần kết luận được sửa thành tín hiệu ban đầu nghiêng B do chi phí gián đoạn; chưa đủ bác A và C chưa được kiểm tra. |
| Gợi ý cách tổng hợp P01/P02/P03 thành Hypothesis Problem Day 18. | AI có thể biến diễn giải thành fact hoặc làm ba Practice Notes nghe như validation. | Tôi giữ riêng evidence và diễn giải, đồng thời ghi rõ problem/pain chưa được validated. |
| Gợi ý ba solution mechanisms và spectrum User-led → Co-create → Proactive. | Cơ chế ban đầu có nguy cơ chỉ khác giao diện hoặc Option C làm quá nhiều thay user. | Tôi giữ Option C là **AI-led Recovery Path** nhưng AI chỉ được hiển thị đề xuất; user quyết định accept, change, dismiss hoặc tắt gợi ý. |
| Hỗ trợ thiết kế critical interaction của Option C. | AI có thể tự động chuyển bài sau khi phát hiện câu trả lời sai, gây mất mạch và giảm agency. | Tôi quyết định trigger chỉ tạo suggestion card, không tự điều hướng hoặc thay đổi tiến độ học. |
| Gợi ý evidence, uncertainty và data control cho Option C. | AI có thể giả định được dùng toàn bộ lịch sử học và ghi nhớ feedback cho lần sau. | Tôi giới hạn dữ liệu ở câu trả lời gần đây và trạng thái hoàn thành bài; prototype không mặc định lưu, huấn luyện hoặc cá nhân hóa. User có thể chọn “Chỉ dùng câu trả lời hiện tại” hoặc “Tắt đề xuất chủ động”. |
| Gợi ý control/recovery và human escalation. | Danh sách control ban đầu có thể quá nhiều hoặc biến prototype thành full product. | Tôi giữ các control cần test: accept, chọn đường khác, dismiss, quay lại đúng đoạn RRF và hỏi giảng viên/trợ giảng. |
| Tạo fixture/canned output mẫu về RRF/top-k để ba option dùng chung. | Nội dung do AI tạo không phải evidence và có thể chưa khớp hoàn toàn bài thật trên VLearn. | Tôi đánh dấu fixture là dữ liệu giả lập và cần đối chiếu nội dung kỹ thuật với tài liệu thật trước khi chuyển sang test. |
| Hỗ trợ soạn README cá nhân, Design Sheet và `prototype-link.md`. | AI không có bản tương tác hoặc URL nên không thể kiểm chứng link, reset path hay khả năng tự thao tác. | Tôi ghi rõ phạm vi hiện tại chỉ là nội dung/flow micro-prototype và giữ link/test status là `PENDING`. |

## AI không được sử dụng cho

- Tạo quote, observation hoặc feedback giả của Tester 3.
- Điền trước Prototype Feedback Note khi chưa facilitate phiên test.
- Quyết định tester thích option nào hoặc option nào thắng.
- Viết Group Next Change trước khi nhóm có đủ ba Feedback Notes.
- Biến canned output hoặc fixture thành evidence về user.
- Tuyên bố problem hoặc solution đã được validated.

## Phần tôi phải tự thực hiện

- Đối chiếu nội dung RRF/top-k với bài thật trên VLearn.
- Rà soát và hoàn thiện nội dung/flow của Option C, sau đó review chéo nội dung A/B.
- Nếu bài chuyển sang giai đoạn test, dựng bản tương tác vừa đủ và kiểm tra trigger, evidence, dismiss, data control, recovery cùng reset path; không cần production product.
- Facilitate Tester 3 dùng đủ C → A → B mà không giải thích giao diện hộ tester.
- Ghi hành vi/lời nói trước, diễn giải sau trong Feedback Note 3.
- Tổng hợp bản nháp pattern, khác biệt, một Next Change và Still Unproven sau khi nhận đủ ba Feedback Notes.

## Cam kết dữ liệu

Mọi feedback sau test phải xuất phát từ hành vi và lời nói thực tế. Tôi không dùng AI để tạo hoặc làm sạch evidence đến mức không còn phân biệt được lời tester với diễn giải của mình. Ba phiên test chỉ tạo input cho iteration tiếp theo, không chứng minh product value hoặc market demand.
