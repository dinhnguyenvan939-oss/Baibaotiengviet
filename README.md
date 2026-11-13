# Hệ thống tóm tắt tin tức tiếng Việt bằng AI

Đồ án thử nghiệm mô hình ViT5 đã huấn luyện sẵn để tạo bản tóm tắt tin tức tiếng Việt. Giai đoạn hiện tại tập trung vào notebook Google Colab: nhập văn bản, đếm token, chia bài dài thành đoạn, tóm tắt từng đoạn và tổng hợp kết quả.

## Trạng thái

- Đã thử nghiệm mô hình `NishiKyen/vit5-vietnamese-news` trên Google Colab.
- Đã thử quy trình với các bài ngắn và dài bằng văn bản nhập thủ công.
- Đầu ra có thể sai tên riêng, sai ý, bỏ sót hoặc thêm thông tin; cần đối chiếu với bài gốc.
- Chưa triển khai website, API, nhập URL tự động, đọc PDF hoặc cơ sở dữ liệu.

## Công nghệ thử nghiệm

Python, Google Colab, PyTorch, Hugging Face Transformers, ViT5 và SentencePiece.

## Cấu trúc

```text
Baibaotiengviet/
├── README.md
├── .gitignore
├── docs/
│   ├── ERD_tom_tat_tin_tuc.svg
│   └── so_do_er_chen_tom_tat_bai_bao.png
└── notebooks/
    └── Thu_nghiem_ViT5_Colab.ipynb
```

Notebook nhận văn bản được dán thủ công. Các URL trong notebook lưu thông tin nguồn, chưa được dùng để tự tải nội dung. Phần thân bài mẫu được để trống để tránh đưa nguyên văn bài báo có bản quyền vào repository.

## Chạy thử

Mở notebook trong Google Colab, bật GPU nếu có, dán văn bản vào các cell dữ liệu và chạy lần lượt từ trên xuống dưới. Đối chiếu kết quả với bài gốc trước khi sử dụng.
...
