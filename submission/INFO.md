# Thông tin bài nộp

- **Họ tên:** Ngô Hoàng Thùy Khuê (tên không dấu dùng trong repo: `NgoHoangThuyKhue`)
- **MSSV:** `2A202603017`
- **Mã bài:** `K4-Track02-Day18`
- **Đường chạy:** Lightweight, không dùng Spark. Cả NB1–NB8 chạy bằng Python; NB1–NB4 dùng `deltalake`/Polars/DuckDB, NB5 dùng PyIceberg với SQLite catalog, NB6–NB8 dùng các thư viện lightweight tương ứng.
- **Python:** 3.14.6 (venv `.venv`)
- **Hệ điều hành:** macOS 26.5.2, Apple Silicon (arm64)
- **Thư viện chính:** `deltalake` 1.6.6, Polars 1.44.2, DuckDB 1.5.6, PyIceberg 0.12.0, PyArrow 25.0.1, NumPy 2.5.3.
- **Lưu trữ scratch:** `_lakehouse/` ở thư mục gốc repo; các bảng Delta/Iceberg và dữ liệu sinh cho lab nằm tại đây.

Các phiên bản và đường chạy trên được đọc từ môi trường `.venv` hiện tại; notebook đã lưu output thực thi trong `notebooks/`.
