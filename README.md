# Dự đoán Tỷ giá hối đoái EUR/VND giai đoạn 2020–2025

Dự án sử dụng các mô hình học máy và chuỗi thời gian để phân tích, trực quan hóa và dự đoán tỷ giá EUR/VND dựa trên dữ liệu lịch sử từ năm 2020 đến 2025.  
Các mô hình được triển khai gồm:

- ARIMA – Mô hình thống kê truyền thống dùng để dự đoán dữ liệu chuỗi thời gian dựa trên các quan sát trong quá khứ.

- LSTM – Mạng nơ-ron sâu có khả năng ghi nhớ thông tin dài hạn, rất hiệu quả cho dữ liệu chuỗi phức tạp.

- XGBoost – Thuật toán boosting nhanh, mạnh, dùng nhiều cây quyết định để nâng cao độ chính xác.

- Random Forest – Tập hợp nhiều cây quyết định được xây dựng ngẫu nhiên, giúp cải thiện độ ổn định và tránh overfitting.
---

## Giới thiệu

Tỷ giá ngoại tệ luôn là một yếu tố quan trọng trong tài chính, đầu tư và thương mại quốc tế.  
Dự án này nhằm cung cấp một công cụ dự đoán tỷ giá EUR/VND trong ngắn hạn dựa trên các mô hình học máy hiện đại và mô hình chuỗi thời gian truyền thống.  
Kết quả giúp người dùng có cái nhìn rõ hơn về xu hướng tỷ giá và hỗ trợ ra quyết định tài chính.


## Quy trình thực hiện

1. Thu thập dữ liệu
   - Thu thập dữ liệu tỷ giá EUR/VND từ năm 2020 đến 2025 từ các nguồn công khai.
2. Tiền xử lý dữ liệu
   - Làm sạch dữ liệu, xử lý missing values, chuẩn hóa, tạo các đặc trưng độ trễ.
3. Phân tích dữ liệu khám phá (EDA)
   - Trực quan hóa xu hướng, độ biến động, tính mùa vụ.
4. Huấn luyện mô hình
   - Xây dựng và huấn luyện các mô hình: ARIMA, LSTM, XGBoost, Random Forest.
5. Đánh giá mô hình
   - So sánh kết quả dự đoán qua các chỉ số: MAE, MSE, RMSE, MAPE.
6. Dự đoán 7 ngày tiếp theo
   - Dự đoán và trực quan hóa tỷ giá trong tương lai ngắn hạn.

---

## Cấu trúc thư mục

```bash
.
├── data/                   # Dữ liệu thô và dữ liệu đã xử lý
│   ├── raw/                # Dữ liệu gốc thu thập được
│   └── processed/          # Dữ liệu đã làm sạch, tạo đặc trưng
│
├── model/                  # Các mô hình đã huấn luyện và lưu
│   ├── LSTM/
│   ├── RandomForest/
│   └── XGBoost/
│
├── notebook/               # Các notebook Jupyter cho từng bước xử lý
│   ├── crawl_data.ipynb          # Thu thập dữ liệu
│   ├── data_preprocessing.ipynb  # Tiền xử lý dữ liệu
│   ├── EDA.ipynb                 # Khám phá và trực quan hóa dữ liệu
│   ├── arima.ipynb              # Mô hình ARIMA
│   ├── lstm.ipynb               # Mô hình LSTM
│   ├── randomforest.ipynb       # Mô hình Random Forest
│   └── xgboost.ipynb            # Mô hình XGBoost
│
├── .gitignore
├── requirements.txt
└── README.md
