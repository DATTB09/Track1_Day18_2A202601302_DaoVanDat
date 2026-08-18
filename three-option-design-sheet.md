# Three-option Design Sheet

## Hypothesis Problem

> Khi đang học một bài trên VLearn và gặp một khái niệm hoặc đoạn nội dung không hiểu, học viên gặp khó khăn trong việc khôi phục đủ kiến thức liên quan mà không làm mất mạch học. Họ phải tra cứu bên ngoài, bị chậm so với lớp hoặc bỏ qua nội dung khi chưa hiểu rõ. Ba option dưới đây cùng giải quyết task này (gỡ điểm vướng để tiếp tục bài học) nhưng phân chia vai trò user–AI khác nhau (user chủ động chọn điểm khó, AI và user cùng chẩn đoán, hoặc AI chủ động đề xuất lộ trình).

## Constants dùng chung cho A/B/C

| Thành phần | Nội dung |
|---|---|
| Target user | Học viên trong khóa đang học một bài mới trên VLearn |
| Situation | Học viên gặp một đoạn không hiểu trong khi bài học vẫn đang tiếp tục |
| Task | Gỡ điểm vướng, hiểu bài làm gì và giải thích được bài đó |
| Desired outcome | Học viên hiểu đủ để trả lời câu hỏi kiểm tra và quay lại đúng vị trí đang học mà không phải tra cứu bên ngoài |
| Content/data fixture | Cùng một đoạn bài đó, một câu trả lời gần đây chưa chính xác và cùng lịch sử học tập mẫu |

## Ba solution options

| Thành phần | Option A — User-led Inline Explain | Option B — Collaborative Diagnosis | Option C — AI-led Recovery Path |
|---|---|---|---|
| Solution mechanism | User chọn chính xác điểm khó và yêu cầu một kiểu giải thích; AI không tự suy luận nguyên nhân | User và AI cùng xác định kiến thức nền còn thiếu qua hai câu hỏi ngắn | AI sử dụng câu trả lời gần đây và lịch sử học để chủ động đề xuất lộ trình ôn |
| User làm gì? | Bôi đen "RRF" hoặc "top-k"; chọn định nghĩa, ví dụ hoặc giải thích từng bước | Báo chưa hiểu, trả lời hai câu chẩn đoán và xác nhận hoặc sửa kết luận của AI | Xem lý do AI đưa ra đề xuất; chấp nhận, đổi khái niệm, bỏ qua hoặc yêu cầu trợ giúp từ người thật |
| AI làm gì? | Chỉ giải thích nội dung user đã chọn, dựa trên đoạn bài hiện tại | Đặt câu hỏi, phân tích câu trả lời, đề xuất một kiến thức nền và tạo refresher ngắn | Phân tích câu trả lời sai và lịch sử bài học; đề xuất bản đồ kiến thức cùng mức chắc chắn |
| Trigger | User chủ động chọn nội dung và yêu cầu giải thích | User bấm "Tôi vẫn chưa hiểu" | Sau một câu trả lời sai ở checkpoint, AI chủ động đưa đề xuất nhưng chưa tự chuyển bài |
| Trade-off chính | Nhanh, ít suy luận và user kiểm soát cao; có thể chỉ xử lý triệu chứng bề mặt | Có khả năng tìm đúng nguyên nhân hơn; user phải trả lời thêm và mất thời gian trước khi được giải thích | Ít thao tác, hỗ trợ chủ động; có rủi ro AI suy luận sai, gây phiền hoặc làm user mất quyền chủ động |

## Distance check

- A khác B vì: A giả định user đã biết điểm mình cần hỏi và AI chỉ giải thích phần được chọn; B chưa giả định user biết nguyên nhân và cùng user thực hiện chẩn đoán trước.
- B khác C vì: B chỉ bắt đầu khi user yêu cầu và hai bên cùng xây dựng kết luận; C do AI chủ động suy luận từ dữ liệu học tập rồi đưa đề xuất để user xem xét.
- A khác C vì: A không sử dụng lịch sử học tập và không tự suy luận; C sử dụng context và câu trả lời gần đây để chủ động đề xuất một lộ trình kiến thức.

## Human-AI decision table

| Quyết định | Option A | Option B | Option C |
|---|---|---|---|
| Expectation & giới hạn | User chủ động chọn đúng đoạn khó và loại giải thích; AI chỉ giải thích nội dung được chọn, không tự suy luận nguyên nhân sâu hơn hoặc dùng lịch sử học | AI chỉ được đặt tối đa hai câu hỏi chẩn đoán ngắn trước khi đề xuất kiến thức nền, không tự kết luận nếu user chưa xác nhận | AI được chủ động đề xuất lộ trình dựa trên câu trả lời sai và lịch sử học, nhưng không được tự chuyển bài hoặc thay đổi tiến trình học nếu chưa có sự đồng ý của user |
| AI Act / Ask / Don't Act? | Act khi user đã chọn nội dung cụ thể; Don't Act (không tự suy luận hay đề xuất) nếu chưa có lựa chọn từ user | Ask trước (hai câu hỏi chẩn đoán) rồi mới Act (đề xuất refresher); chờ user xác nhận hoặc sửa kết luận trước khi hoàn tất | Act chủ động (đề xuất lộ trình kèm lý do) ngay sau câu trả lời sai ở checkpoint; Don't Act với việc tự chuyển bài — chỉ Ask và chờ user chấp nhận |
| Evidence & uncertainty | Chỉ dựa vào đoạn bài hiện tại được user bôi đen; không đánh giá mức độ chắc chắn vì không tự suy luận nguyên nhân | Dựa trên câu trả lời của user cho hai câu hỏi chẩn đoán; kết luận có thể sai nên cần user xác nhận hoặc sửa | Dựa trên câu trả lời gần đây sai và lịch sử học tập; AI phải nêu rõ mức độ chắc chắn của đề xuất vì suy luận có thể sai |
| User control & recovery | User toàn quyền chọn lại đoạn khác, đổi kiểu giải thích, hoặc bỏ qua nếu giải thích chưa đủ | User có thể sửa kết luận chẩn đoán của AI trước khi nhận refresher; có thể dừng ở bất kỳ bước nào | User có thể chấp nhận, đổi khái niệm khác, bỏ qua đề xuất, hoặc yêu cầu trợ giúp từ người thật |
