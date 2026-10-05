# Reflection — Lab 19

**Tên:** Nguyễn Quang Huy - 2A202602820
**Cohort:** 4
**Path đã chạy:** Lite

## Câu hỏi (≤ 200 từ)

Trên 50 queries, Precision@10 trung bình: BM25 77,8%, vector 73,2%, hybrid 78,6%.

Nhóm exact: BM25 và hybrid cùng đạt 96,7%, vượt vector 88,7%; từ khóa kỹ thuật khớp trực tiếp giúp BM25 xếp hạng chính xác. Nhóm mixed: hybrid đạt 100%, vượt vector 98,5% và BM25 97%; RRF kết hợp bằng chứng từ hai danh sách với rank bắt đầu từ 1, k=60.

Nhóm paraphrase: BM25 đạt 33,3%, hybrid 32%, vector 24%. Vector không dẫn đầu như kỳ vọng. Đây là hạn chế của mô hình bge-small-en-v1.5 chủ yếu dành cho tiếng Anh trên dữ liệu tiếng Việt. Hybrid không bảo đảm thắng mọi loại truy vấn.

Tôi chọn pure BM25 khi cần khớp mã định danh, thuật ngữ chính xác hoặc hạn chế chi phí embedding. Tôi chọn pure vector khi truy vấn thiên về ngữ nghĩa và mô hình đã được kiểm chứng phù hợp ngôn ngữ, đặc biệt khi từ vựng ít trùng nhau. Tôi dùng hybrid khi lợi ích chất lượng đo được bù cho độ trễ và chi phí bổ sung.
