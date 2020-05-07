# NLP-IELTS

Giai đoạn 1 : Xác định phương hướng bài toán 
- Ban đầu nhóm định làm phần đọc hiểu trong bài thi IELTS. Tuy nhiên do, model BERT tối đa được 512 token so với hơn 1000 của bài thi IELTS.
- Sau đó, nhóm thống nhất làm bài toán điền từ vào chỗ trống với 4 đáp cho trước của bài thi Toeic

Giai đoạn 2 : Tự tạo dataset (có làm thì mới có ăn, không làm thì... à mà thôi)
- Các tài liệu Toeic có rất nhiều. Tuy nhiên đa số là sách scan, lúc convert sang file doc/txt thì thường bị mất chữ
- Nên phải chọn lựa các sách có dung lượng nhỏ (~5Mb) thì chất lượng convert lại tốt hơn. Do đây thường là sách convert từ word sang PDF. Ít thành phần nhiễu.

Giai đoạn 3 : Dùng BertforMaskLM để thử với các đáp án
- Kết quả rất tuyệt vời.
- Model có thể điền đúng hầu hết các câu ngữ pháp (trong <10s/câu)
- Với các câu phải phân tích nội dung và đáp án dài mặc dù tốn nhiều thời gian hơn (~3-5 phút / câu) nhưng vẫn trả lời đúng
(updating)
