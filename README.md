# Track1_Day18_2A202601302_DaoVanDat

Track 1 · Three Human–AI Solution Options & Micro-prototypes  
Team: **ABC** · Case tiếp tục từ Day 17: **AI Tutor — Diagnostic Refresher**

> **Trạng thái hiện tại:** Nhóm đã tổng hợp evidence Day 17, chốt một Hypothesis Problem, ba Solution Options và Human–AI decisions. Nhóm đang build ba micro-prototype; chưa test A/B/C với user thật. Feedback Notes, Group Next Change và kết luận sau test vẫn để `PENDING`.

## 1. Thông tin cá nhân và nhóm

| Mục | Nội dung |
|---|---|
| Họ và tên | Đào Văn Đạt |
| MHV | 2A202601302 |
| Track / Ngày | Track 1 · Day 18 |
| Team | **ABC** |
| Case | **AI Tutor — Diagnostic Refresher** |

### Thành viên và vai trò

| Thành viên | MHV | Vai trò Day 18 |
|---|---|---|
| Nguyễn Minh Quân | 2A202601478 | Phụ trách Option A — User-led Inline Explain; sau đó facilitate Tester 1 |
| Vũ Đình Huy | 2A202601288 | Phụ trách Option B — Collaborative Diagnosis; sau đó facilitate Tester 2 |
| Đào Văn Đạt | 2A202601302 | Phụ trách Option C — AI-led Recovery Path; sau đó facilitate Tester 3 và tổng hợp bản nháp Group Feedback Synthesis |

Chi tiết phân công: [Phân công nhóm](phan-cong-nhom.md)

## 2. Hypothesis Problem

> Khi **đang học một bài mới trên VLearn và gặp một đoạn hoặc khái niệm không hiểu**, **học viên** gặp khó khăn trong việc **gỡ điểm vướng để tiếp tục bài học** vì **họ không thể nhanh chóng xác định và bổ sung phần kiến thức liên quan ngay trong mạch học**, dẫn đến **phải rời bài đi tra cứu, mất mạch, bị chậm so với lớp hoặc tiếp tục khi chưa hiểu chắc nội dung**.

### Evidence nối tiếp từ Day 17

| Practice Note | Evidence đã ghi nhận | Diễn giải tạm thời |
|---|---|---|
| P01 | User nói mình “không biết hổng chỗ nào để đi vá”; đã tra “RRF reranking là gì” nhưng sau đó vẫn không giải thích được lý do chọn top-k. | Có tín hiệu user xác định được đoạn tắc nhưng chưa xác định được phần nền cần bổ sung. |
| P02 | User nói việc cố gắng tìm hiểu có thể khiến mình bỏ lỡ phần bài sau. | Có tín hiệu chi phí gián đoạn là một barrier riêng. |
| P03 | User đưa nội dung slide vào ChatGPT để hỏi Harness; mất khoảng 5 phút và lớp đi trước 5 slide. | Có workaround và consequence quan sát được; nghiêng nhẹ về chi phí gián đoạn. |

Ba Practice Notes là evidence ban đầu từ buổi luyện tập, không phải validation. Nhóm vẫn chưa biết barrier chính là thiếu chẩn đoán, chi phí gián đoạn hay cách AI Tutor hiện tại phản hồi.

## 3. Three Solution Options

Ba option giữ nguyên target user, situation, task, desired outcome và fixture. Chúng khác nhau ở solution mechanism và quyền chủ động giữa user–AI.

| Option | Mechanism | User làm gì? | AI làm gì? | Trade-off chính |
|---|---|---|---|---|
| **A — User-led Inline Explain** | User chủ động chọn điểm khó; AI không tự suy luận nguyên nhân. | Bôi đen `RRF` hoặc `top-k`, chọn định nghĩa, ví dụ hoặc giải thích từng bước. | Chỉ giải thích nội dung được chọn dựa trên bài hiện tại. | Nhanh và user kiểm soát cao; có thể chỉ xử lý điểm khó bề mặt. |
| **B — Collaborative Diagnosis** | User và AI cùng chẩn đoán trước khi ôn. | Báo chưa hiểu, trả lời hai câu ngắn và xác nhận hoặc sửa đề xuất. | Phân tích câu trả lời, đề xuất một kiến thức nền và tạo refresher sau khi user xác nhận. | Có thể xử lý nguyên nhân sâu hơn nhưng thêm thao tác và thời gian. |
| **C — AI-led Recovery Path** | AI chủ động đề xuất dựa trên tín hiệu học tập; user review. | Xem evidence, chấp nhận, đổi khái niệm, dismiss hoặc yêu cầu trợ giúp từ người thật. | Dùng câu trả lời gần đây và tiến độ học để đề xuất bản đồ kiến thức cùng mức chắc chắn. | Ít thao tác nhưng có nguy cơ suy luận sai, gây phiền hoặc giảm agency. |

```text
Option A: USER INITIATES — AI RESPONDS
→ Option B: USER + AI CO-DIAGNOSE
→ Option C: AI INITIATES — USER REVIEWS
```

Chi tiết: [Three-option Design Sheet](three-option-design-sheet.md)  
Trạng thái build: [Prototype links](prototype-link.md)

## 4. Đóng góp của tôi và phân công nhóm

### Đóng góp của tôi — Đào Văn Đạt

Tôi phụ trách chính **Option C — AI-led Recovery Path**. Phần việc của tôi gồm:

- Thiết kế trigger xuất hiện sau câu trả lời sai ở checkpoint nhưng không tự chuyển bài.
- Thể hiện rõ evidence AI sử dụng: câu trả lời gần đây và trạng thái hoàn thành Ranking/Reranking.
- Thiết kế mức uncertainty và thông báo giới hạn để user biết AI có thể suy luận sai.
- Bổ sung quyền kiểm soát: accept, chọn đường khác, dismiss, chỉ dùng câu trả lời hiện tại và tắt gợi ý chủ động.
- Thiết kế recovery/human escalation: quay lại đúng đoạn RRF hoặc yêu cầu giảng viên/trợ giảng hỗ trợ.
- Xây dựng bản đầu của prototype C bằng shared context và components chung.
- Sau prototype checkpoint, facilitate Tester 3 dùng đủ A/B/C, ghi Feedback Note 3 và tổng hợp bản nháp Group Feedback Synthesis.

Ở checkpoint hiện tại, phần test với user, Feedback Note 3 và Group Feedback Synthesis chưa được thực hiện.

### Phân công theo option

- **Quân — Option A:** thiết kế interaction user-led, phạm vi AI, lựa chọn kiểu giải thích, dismiss và quay lại bài.
- **Huy — Option B:** thiết kế hai câu chẩn đoán, evidence/uncertainty, quyền xác nhận hoặc sửa của user.
- **Đạt — Option C:** thiết kế trigger chủ động, lý do đề xuất, data control, dismiss/undo/recovery và human escalation.

### Phần việc chung của ba thành viên

- Chốt Evidence Snapshot, Hypothesis Problem và Still Unproven.
- Chuẩn hóa Comparison Contract và content/data fixture RRF/top-k.
- Hoàn thành Distance Check và Human–AI Decision Table.
- Dùng chung context screen, content, task, components và visual style.
- Review chéo để cả ba option có chất lượng tương đương và đều có reset path.
- Sau prototype checkpoint, mỗi thành viên test đủ A/B/C với một tester ngoài nhóm.

## 5. Prototype Feedback

**Trạng thái:** `PENDING — CHƯA TEST VỚI USER THẬT`

- Feedback Note Tester 1: chưa thực hiện.
- Feedback Note Tester 2: chưa thực hiện.
- Feedback Note Tester 3: chưa thực hiện.
- Group Feedback Synthesis: chưa có đủ dữ liệu.
- Group Next Change: chưa được quyết định.

### Still Unproven

- Tester có tự thao tác được A/B/C mà không cần facilitator giải thích hay không.
- Option nào giúp user hiểu RRF/top-k và quay lại task với công sức chấp nhận được.
- User có hiểu evidence, uncertainty và quyền kiểm soát của từng option hay không.
- Đề xuất chủ động của Option C hữu ích hay gây gián đoạn.
- Product value, learning outcome, pain prevalence và market demand chưa được chứng minh.

Nhóm không tạo trước quote, observation, lựa chọn của tester hoặc kết luận option thắng.

## 6. AI Support Log

Nhóm sử dụng ChatGPT/Codex để gợi ý cơ chế A/B/C, rà soát Human–AI decisions, tạo fixture/canned output mẫu và kiểm tra tính nhất quán giữa các artifact. AI không được sử dụng để tạo interview evidence, tester feedback, observation, quote hoặc Group Next Change.

Chi tiết: [AI Support Log](ai-support-log.md)

## Artifact Index

- [Three-option Design Sheet](three-option-design-sheet.md)
- [Prototype links](prototype-link.md)
- [Phân công nhóm](phan-cong-nhom.md)
- [AI Support Log](ai-support-log.md)
- `prototype-feedback-note.md` — tạo/điền sau phiên test của từng facilitator
- `group-feedback-synthesis.md` — điền sau khi có đủ ba Feedback Notes

## Kiểm tra tại checkpoint Prototype

- [x] Giữ nguyên case AI Tutor từ Day 17.
- [x] Có một Hypothesis Problem chung và ghi rõ điều chưa biết.
- [x] A/B/C cùng problem/task nhưng khác mechanism và vai trò user–AI.
- [x] Có Expectation, Agency, Evidence/Uncertainty và Control/Recovery.
- [x] Có content/data fixture chung cho A/B/C.
- [x] Có scope 2–3 trạng thái và prototype annotation cho từng option.
- [ ] Ba prototype đã hoàn thành và mở được.
- [ ] `prototype-link.md` đã có đủ link thật của A/B/C.
- [ ] Reset path đã được kiểm tra trên cả ba prototype.
- [ ] Đã thực hiện ba phiên test với user ngoài nhóm.
- [ ] Đã có ba Feedback Notes và một Group Next Change.

> Đây là README cá nhân của Đào Văn Đạt, sử dụng các artifact chung của Team ABC. Sau phiên test, Đạt phải cập nhật observation, đóng góp thực tế và AI reflection cá nhân trước khi nộp cuối.
