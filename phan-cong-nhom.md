# Phân công nhóm AI Tutor — Day 18

## Nguyên tắc chung

- Cả nhóm chốt **một Hypothesis Problem**, cùng target user, situation, task, desired outcome và dữ liệu mẫu.
- Mỗi người chịu trách nhiệm chính một option; các option phải khác nhau ở cơ chế User–AI, không chỉ khác giao diện.
- Mỗi người tự điều phối một phiên test với **một tester ngoài nhóm**; trong phiên đó tester phải dùng đủ A/B/C.
- Không tuyên bố option đã được validated. Sau ba phiên, nhóm chỉ chốt **một Next Change** và ghi rõ phần còn chưa biết.

## Phân công chính

| Thành viên | Vai trò chính | Deliverable chịu trách nhiệm | Việc cụ thể |
|---|---|---|---|
| **Nguyễn Minh Quân** | Option A — User-led | Option A trong Design Sheet; prototype A; Feedback Note của Tester 1 | Thiết kế luồng user tự chủ động yêu cầu trợ giúp. Ghi rõ user chọn gì, AI chỉ làm gì khi được gọi, cách user bỏ qua/quay lại. Điều phối và ghi facts phiên test 1. |
| **Vũ Đình Huy** | Option B — Co-create | Option B trong Design Sheet; prototype B; Feedback Note của Tester 2 | Thiết kế luồng AI gợi ý nhưng user chọn/xác nhận hướng hỗ trợ. Ghi rõ điểm AI phải hỏi trước, evidence/uncertainty và quyền sửa. Điều phối và ghi facts phiên test 2. |
| **Đào Văn Đạt** | Option C — Proactive agent | Option C trong Design Sheet; prototype C; Feedback Note của Tester 3 | Thiết kế luồng AI chủ động đề xuất hỗ trợ khi nhận thấy người học có thể đang tắc. Ghi rõ trigger, cách tránh làm phiền, dismiss/undo/recovery. Điều phối và ghi facts phiên test 3. |

## Phần việc làm chung

| Thời điểm | Người làm | Kết quả cần có |
|---|---|---|
| 0–15 phút | Cả 3 | Đọc lại 3 Practice Notes Day 17; chốt một Hypothesis Problem; ghi evidence hỗ trợ và Still Unproven. |
| 15–35 phút | Cả 3, Quân ghi file | Hoàn thành constants và bảng A/B/C trong `three-option-design-sheet.md`; thực hiện Distance Check. |
| 35–65 phút | Cả 3 | Điền Human–AI decision table: expectation, agency, evidence/uncertainty, control/recovery. |
| 65–145 phút | Mỗi người theo option; cả 3 review chéo | Hoàn thành ba micro-prototype, dùng chung khoảng 70% context/style; kiểm link và reset path. |
| 145–160 phút | Huy soạn nháp; cả nhóm rà soát | Chốt test prompt, outcome task, 5 điểm quan sát và quy tắc facilitation. |
| Test | Quân / Huy / Đạt | Mỗi người test đủ A/B/C với một tester ngoài nhóm và hoàn thành Feedback Note của mình. |
| Sau test | Đạt tổng hợp, cả nhóm quyết định | Điền `group-feedback-synthesis.md`: pattern, một Group Next Change và Still Unproven. |
| Trước khi nộp | Quân kiểm repo; từng người tự kiểm phần mình | Cập nhật README, prototype links và AI Support Log trung thực. |

## Phân định A/B/C đề xuất cho case AI Tutor

| Option | Cơ chế cần giữ |
|---|---|
| **A — User-led** | Học viên tự bôi đen/chọn phần đang tắc rồi chủ động yêu cầu giải thích hoặc ôn nền. AI không tự chen vào. |
| **B — Co-create** | AI đưa ra một vài khả năng về kiến thức nền hoặc cách hỗ trợ; học viên chọn/xác nhận trước khi AI tạo phần ôn. |
| **C — Proactive** | AI chủ động nhận diện tín hiệu có thể mắc kẹt và đưa gợi ý hỗ trợ; học viên luôn có quyền bỏ qua hoặc tắt gợi ý. |

## Quy tắc bàn giao

- Người phụ trách option chỉ sở hữu **bản build đầu tiên**, không sở hữu kết luận: cả nhóm cùng review và test cả ba.
- Feedback Note chỉ ghi hành vi/lời nói quan sát được; không bịa quote hoặc làm đẹp feedback.
- Khi prototype của một người chưa test-ready, hai người còn lại hỗ trợ sửa common context và luồng recovery trước khi test.
