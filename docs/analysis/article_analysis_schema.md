# Mẫu phân tích bài báo khoa học

## Mục đích
Chuẩn hóa kết quả phân tích để hỗ trợ nhà nghiên cứu tìm và hiểu tài liệu. Mỗi nhận định cần truy lại được nguồn; hệ thống không tự kết luận tính mới của đề tài.

## Nguyên tắc
- Chỉ sử dụng thông tin có trong tài liệu đã nạp.
- Gắn nhận định quan trọng với trang và trích đoạn ngắn khi xác định được.
- Nếu bài không nêu thông tin, ghi “Không tìm thấy trong bài”.
- Tách nội dung trích từ bài khỏi diễn giải hoặc gợi ý của hệ thống.
- Người dùng cần đối chiếu kết quả với bài gốc trước khi sử dụng.

## Các trường phân tích

| Trường | Nội dung cần ghi |
|---|---|
| Thông tin bài báo | Tiêu đề, tác giả, năm, tạp chí/hội nghị, DOI hoặc URL nếu có |
| Vấn đề nghiên cứu | Vấn đề hoặc khoảng trống mà bài báo nêu |
| Mục tiêu/câu hỏi | Mục tiêu và câu hỏi nghiên cứu được nêu |
| Phương pháp | Thiết kế, phương pháp, công cụ và quy trình nghiên cứu |
| Dữ liệu/mẫu | Đối tượng, cỡ mẫu, dữ liệu, phạm vi và thời gian |
| Kết quả chính | Kết quả và số liệu; giữ nguyên đơn vị và ngữ cảnh |
| Hạn chế | Hạn chế do tác giả nêu; nếu không có, ghi rõ |
| Liên quan đến ý tưởng | Bài báo có thể hỗ trợ khía cạnh nào trong ý tưởng người dùng, kèm căn cứ |
| Câu hỏi tiếp theo | Câu hỏi cần người dùng tự kiểm tra hoặc đọc thêm |

## Dẫn chứng
Mỗi dẫn chứng gồm số trang PDF (đếm từ 1), trích đoạn ngắn, loại nội dung (`trích từ bài` hoặc `diễn giải`) và mức chắc chắn (`cao`, `vừa`, `thấp`). Dùng mức thấp khi PDF trích xuất lỗi hoặc thiếu ngữ cảnh. Không tạo dẫn chứng nếu không tìm thấy câu chữ hỗ trợ.

## Mẫu JSON đề xuất

```json
{
  "article": {"title": "", "authors": [], "year": null, "venue": "", "doi_or_url": ""},
  "research_problem": {"text": "", "evidence": []},
  "objectives_or_questions": {"text": "", "evidence": []},
  "methodology": {"text": "", "evidence": []},
  "data_or_sample": {"text": "", "evidence": []},
  "key_findings": [{"text": "", "evidence": []}],
  "limitations": {"text": "Không tìm thấy trong bài", "evidence": []},
  "relevance_to_user_idea": [{"text": "", "evidence": [], "interpretation": true}],
  "follow_up_questions": [],
  "review_note": "Cần đối chiếu với PDF gốc trước khi sử dụng."
}
```

Mỗi phần tử trong `evidence` nên có `page`, `quote`, `type` và `confidence`.

## Cách kiểm tra trên PDF
1. Trích xuất PDF và giữ số trang gắn với từng đoạn.
2. Điền các trường bằng mô hình; yêu cầu mô hình bỏ trống hoặc ghi “Không tìm thấy trong bài” khi thiếu căn cứ.
3. Đối chiếu tên riêng, số liệu, kết quả và diễn giải với trang nguồn.
4. Sửa nội dung sai hoặc thiếu dẫn chứng trước khi dùng.
5. Lưu kết quả thử riêng; không đưa toàn văn bài có bản quyền vào kho mã nguồn.

## Tiêu chí hoàn thành
- Có mẫu đầu ra tiếng Việt có thể chuyển thành JSON/API.
- Nhận định quan trọng có dẫn chứng theo trang.
- Phân biệt nội dung bài báo với diễn giải của hệ thống.
- Có ít nhất một kết quả thử được đối chiếu với PDF gốc.

## Trạng thái
Bản nháp schema; cần kiểm chứng với PDF trước khi xem là hoàn tất.
