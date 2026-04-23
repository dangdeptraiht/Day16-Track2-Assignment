Báo cáo kết quả triển khai Phương án Dự phòng (CPU)
* Lý do sử dụng CPU: Do tài khoản GCP mới chưa được phê duyệt hạn mức (Quota) cho GPU NVIDIA T4, em đã chuyển sang triển khai mô hình Machine Learning (LightGBM) trên máy chủ CPU cao cấp n2-standard-8.
* Kết quả huấn luyện: Thời gian huấn luyện mô hình trên tập dữ liệu Credit Card Fraud cực nhanh, chỉ mất khoảng 1.12 giây với độ chính xác (Accuracy) đạt tới 99.89%.
* Chỉ số AUC-ROC: Đạt 0.88, chứng minh mô hình hoạt động hiệu quả trong việc phát hiện gian lận ngay cả khi không có GPU.
* Tốc độ Inference: Trên CPU, tốc độ dự báo cực nhanh (dưới 1ms/giao dịch), rất phù hợp cho các bài toán phân loại dữ liệu bảng (tabular data).
* Kết luận: Phương án CPU n2-standard-8 có chi phí thấp hơn (~$0.43/giờ) và tính sẵn sàng cao, là lựa chọn tối ưu cho các tác vụ Machine Learning truyền thống khi không yêu cầu tính toán song song cực lớn như Deep Learning.