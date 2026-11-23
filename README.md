## NLP Asssignment.

# 1. Mô tả Kiến trúc hệ thống
Hệ thống được thiết kế theo pipeline xử lý tuần tự: Natural Language Input -> Parser -> Semantic Interpretation -> Intent/Entity Extraction -> Knowledge Base Retrieval -> Answer Generation.

# 2. Chi tiết các thành phần cốt lõi
Grammar & Parser: Sử dụng CFG kết hợp thuật toán Earley Parser để trích xuất cây cú pháp. (Xem file data/grammar.cfg).

Semantic Representation: Ánh xạ cây cú pháp thành các hành động đại diện (ví dụ: GET_COURSE_INFO(course=NLP)).

Intent/Entity: Sử dụng rule-based/keyword matching để gán nhãn câu hỏi.

Knowledge Base: Dữ liệu tĩnh lưu dưới dạng file .txt trong data/course_data/.

Dialogue Context (Phần III): Lưu lại entity của lượt hội thoại trước (ví dụ: Chủ đề bài học) để giải quyết các đại từ chỉ định như "phần này", "nó".