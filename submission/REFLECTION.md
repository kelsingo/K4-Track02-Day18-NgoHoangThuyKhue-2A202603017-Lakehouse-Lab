# Reflection

Anti-pattern tôi chọn là small-file problem. Một hệ thống ingest log hoặc sự kiện liên tục dễ gặp vấn đề này khi mỗi micro-batch tạo một file riêng: metadata phình lên, query phải mở nhiều file và chi phí request tăng dù tổng dữ liệu chưa lớn. Trong lab, 200 lần ghi tạo 200 file; compaction giảm còn 11 file, khoảng 18 lần ít hơn. Tôi sẽ đặt kích thước/chu kỳ micro-batch theo lưu lượng, theo dõi file count và kích thước trung bình, rồi chạy compaction định kỳ. Cần phối hợp retention với reader/writer đang hoạt động để không xóa file còn được dùng. Kết quả thời gian query trên máy cá nhân biến động, nên nên theo dõi cả số file và pruning thay vì chỉ dựa vào thời gian.

**Sử dụng AI:** ChatGPT hỗ trợ đọc hướng dẫn/checkpoints, tổng hợp giải thích cơ chế và soạn thảo tài liệu nộp. Các số liệu trong notebook lấy từ output đã thực thi; tôi cần tự rà soát và hiểu các kết quả trước khi nộp.
