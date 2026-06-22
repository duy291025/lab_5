# 🚀 Lab 5 V4: Dockerized Multi-Model AI Inference Service

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-009688.svg)
![Docker](https://img.shields.io/badge/Docker-Enabled-2496ED.svg)
![ONNX](https://img.shields.io/badge/ONNX-Runtime-blue.svg)

Dự án này là bước triển khai thực tế (Deployment) nối tiếp từ Lab 3 và Lab 4. Mục tiêu là đóng gói các mô hình AI (phát hiện bất thường, dự báo, phân loại ảnh) thành một **RESTful API Service** hoàn chỉnh, có khả năng chạy độc lập và ổn định trên mọi môi trường thông qua **Docker**.

---

## ✨ Điểm nhấn của dự án

- 🧠 **Multi-Model Support:** Xử lý đồng thời dữ liệu dạng số (Telemetry JSON) và dữ liệu hình ảnh (SqueezeNet ONNX ImageNet-1K).
- 📦 **Dockerized:** Đóng gói toàn bộ runtime, thư viện, port và model. Khởi chạy tất cả chỉ với một câu lệnh `docker compose up`.
- 📊 **Logging & Tracing:** Tự động lưu log kết quả inference dưới dạng CSV và xuất ảnh annotated thông qua hệ thống Docker Volume.
- 🌐 **Interactive Docs & UI:** Tích hợp sẵn tài liệu API Swagger UI và một mini web-interface (`/classify-image-demo`) để test upload ảnh trực tiếp trên trình duyệt.

## 🚦 Khởi chạy dự án (Quick Start)

Cách tối ưu nhất để chạy dự án mà không lo xung đột môi trường là sử dụng **Docker**.

```bash
# 1. Build image và khởi chạy container
docker compose up --build

# 2. Xem log để kiểm tra trạng thái hoạt động
docker compose logs -f
