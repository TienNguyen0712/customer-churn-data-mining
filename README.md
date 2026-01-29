![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Academic%20Project-orange)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-ML-yellow)

# 👤 Customer Churn - Data Mining Project

## 📌 Giới thiệu
Trong bối cảnh các ngành thương mại điện tử đang ngày càng phát triển việc nắm bắt được tâm lý khách hàng lại càng được quan tâm nhiều hơn. Do đó việc quan tâm, cải thiện để mang lại trải nghiệm tốt nhất cho khách hàng lại càng được đề cao.
Các câu hỏi thường thấy đối với một doanh nghiệp muốn tìm hiểu nhu cầu khách hàng như:
- Yếu tố nào ảnh hưởng đến khả năng rời bỏ của khách hàng ?
- Dự đoán khách hàng nào có khả năng rời bỏ ?
- Đề xuất các hành động giữ chân khách hàng ?  
- Phân cụm các nhóm khách hàng ?

Đề tài này áp dụng **quy trình Khai phá dữ liệu (Data Mining)** để khám phá tri thức tiềm ẩn từ **Telco Customer Churn dataset**

---

## 🎯 Mục tiêu & Câu hỏi nghiên cứu

### Mục tiêu
- Áp dụng toàn bộ pipeline Khai phá dữ liệu:  
  **Tiền xử lý → Phân tích mô tả → Mô hình hóa → Đánh giá → Insight**
- Thực nghiệm và so sánh nhiều thuật toán học máy (Phân loại - Phân cụm)
- Rút ra insight có ý nghĩa cho bài toán khách hàng rời bỏ

### Câu hỏi nghiên cứu
1. Các **yếu tố** nào ảnh hưởng đến khả năng rời bỏ của khách hàng?
2. Điểm nào phân biệt khách hàng rời bỏ và không rời bỏ ?
3. Hành vi sử dụng dịch vụ thay đổi như thế nào trước khi rời bỏ?
4. Phương thức thanh toán có ảnh hưởng đến rời bở hay không ?
5. Có tồn tại **interaction effects** giữa các đặc trưng hay không ?

---

## 📂 Dataset

- **Tên:** Telco Customer Churn 
- **Nguồn:** Public dataset ([Kaggle – dữ liệu nghiên cứu học thuật](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Số dòng:** gồm **~7043 khách hàng**
- **Số cột:** 21
- **Đối tượng:** **Khả năng rời bỏ** của khách hàng
### Một số thuộc tính quan trọng
- **Thông tin cá nhân:** `customerID`, `gender`, `SeniorCitizen`
- **Thông tin gia đình:** `tenure`, `Partner`, `Dependents`
- **Thông tin xã hội:** `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`
- **Thông tin liên lạc:** `PhoneService`, `MultipleLines`
- **Thông tin hợp đồng:** `Contract`, `PaperlessBilling`, `PaymentMethod`, `MonthlyCharges`, `TotalCharges`, `Churn`

---

## 🧪 Quy trình Khai phá dữ liệu

### 1️⃣ Tiền xử lý dữ liệu ✔️


### 2️⃣ Phân tích mô tả (EDA) ✖️

  
### 3️⃣ Huấn luyện mô hình ✖️


### 4️⃣ Đánh giá mô hình ✖️


### 5️⃣ Rút ra insight - ý nghĩa ✖️

---

## 🤖 Các kỹ thuật Khai phá dữ liệu được sử dụng

### 🔹 Phân loại (Classification)
**Mục tiêu:** Dự đoán khả năng rời bỏ của khách hàng 

**Thuật toán:**


**Đánh giá:**

---

### 🔹 Phân cụm (Clustering)
**Mục tiêu:** Phân khúc khách hàng rời bỏ

**Thuật toán:**


**Đánh giá:**


---

## 📊 Kết quả & Insight chính


---

## 🗂️ Cấu trúc thư mục
```text
customer-churn-data-mining/
│
├── README.md
│
├── configs/
│   ├── base.yaml
│   ├── classification.yaml      # Định nghĩa các cáu trúc tuyến tính
│   └── clustering.yaml          # Định nghĩa các cấu trúc phân cụm  
|
├── data/
│   ├── raw/
│   │   └── telco_customer.csv                   # Dữ liệu khách hàng
│   └── processed/
|       ├── telco_customer_classification.csv    # Dữ liệu phân loại khách hàng
│       └── telco_customer_clustering.csv        # Dữ liệu phân cụm
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_eda.ipynb
│   ├── 04_classification.ipynb
│   └── 05_clustering.ipynb
│
├── reports/
│   ├── Report.pdf
│   └── Poster.pdf
|
├── requirements.txt
└── .gitignore
```

---

## 🚀 Công nghệ & Thư viện
- Python 3.12
- pandas, numpy
- matplotlib, seaborn
- scikit-learn

---

## ⚠️ Hạn chế & Hướng mở rộng


---

## 👨‍🎓 Thông tin học thuật
- Sản phẩm là **bài làm gốc**
- Các tài liệu, thư viện được trích dẫn rõ ràng
- Tác giả: **Nguyễn Đăng Tiến**

---

## 📎 Tài liệu tham khảo
- Kaggle: Telco Customer Churn Dataset
