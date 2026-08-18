# Prototype Links — Nhóm AI Tutor

> **Trạng thái:** Ba prototype đang được build. Chưa có URL hoặc file prototype thật được cung cấp trong workspace, vì vậy cột link được giữ `PENDING` thay vì tạo link giả.

## A/B/C Prototype Index

| Option | Người phụ trách | Link prototype | Critical interaction cần test | Trạng thái |
|---|---|---|---|---|
| **A — User-led Inline Explain** | Nguyễn Minh Quân | `PENDING — bổ sung link thật sau khi build` | User bôi đen `RRF`/`top-k`, chọn kiểu giải thích và lấy lại control bằng đổi lựa chọn/đóng/quay lại | Đang build |
| **B — Collaborative Diagnosis** | Vũ Đình Huy | `PENDING — bổ sung link thật sau khi build` | User trả lời hai câu chẩn đoán, xem evidence và xác nhận hoặc bác bỏ kiến thức nền AI đề xuất | Đang build |
| **C — AI-led Recovery Path** | Đào Văn Đạt | `PENDING — bổ sung link thật sau khi build` | AI hiển thị suggestion card; user xem lý do rồi accept/change/dismiss/tắt gợi ý | Đang build |

## Common Test Contract

| Thành phần | Nội dung giữ nguyên cho A/B/C |
|---|---|
| Target user | Học viên trong khóa đang học một bài mới trên VLearn |
| Situation | Gặp đoạn RRF/top-k không hiểu trong khi bài học vẫn tiếp tục |
| Task | Hiểu RRF làm gì và vì sao hệ thống vẫn chọn top-k sau fusion |
| Desired outcome | Trả lời được câu hỏi kiểm tra và quay lại đúng vị trí đang học |
| Fixture | Cùng đoạn RRF, câu trả lời sai về cosine similarity và lịch sử học Ranking/Reranking |

## Hướng dẫn mở prototype

Sau khi có prototype thật, mỗi link phải mở trực tiếp đến Common Context hoặc kèm tối đa ba bước ngắn:

1. Mở link option.
2. Chọn `Start/Reset` để về Common Context.
3. Thực hiện task hiển thị trên màn hình; facilitator không giải thích UI.

Nếu dùng HTML/CSS/JavaScript, bổ sung thêm:

```text
Yêu cầu chạy:
- Trình duyệt:
- Lệnh khởi động:
- URL local:
```

Nếu dùng Figma/Framer, kiểm tra quyền xem ở chế độ không đăng nhập hoặc quyền mà giảng viên/TA có thể truy cập.

## Reset Path chung

- Mỗi option có nút `Bắt đầu lại/Reset`.
- Reset xóa lựa chọn, câu trả lời chẩn đoán và đề xuất của phiên.
- Sau reset, tester trở về cùng đoạn RRF và cùng câu trả lời gần đây.
- Không giữ lại feedback hoặc thay đổi tiến độ học giữa các lượt prototype.

## Kiểm tra trước khi test

- [ ] Link A mở được và không yêu cầu facilitator giải thích.
- [ ] Link B mở được và không yêu cầu facilitator giải thích.
- [ ] Link C mở được và không yêu cầu facilitator giải thích.
- [ ] Cả ba bắt đầu từ cùng context, task và dữ liệu mẫu.
- [ ] Mỗi option có 2–3 trạng thái quanh critical interaction.
- [ ] Mỗi option có cách để user sửa, bỏ qua hoặc quay lại context ban đầu.
- [ ] Reset path hoạt động ở cả A/B/C.
- [ ] Không option nào hoàn thiện hoặc có visual polish vượt trội rõ rệt.
- [ ] Annotation nằm ngoài frame và không hiện cho tester.

Chỉ đổi trạng thái sang `TEST-READY` sau khi toàn bộ checklist trên được kiểm tra bằng prototype thật.
