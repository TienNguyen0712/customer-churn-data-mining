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
1. Các **yếu tố** nào ảnh hưởng tiêu cực đến điểm số học sinh ?
2. Liệu cồn hay gia đình có ảnh hưởng đến học sinh hay không ?
3. Có thể **phân cụm** thành các nhóm học sinh dựa theo đặc điểm hay không ?
4. Các nhóm học sinh có những yếu tố nào thì có thể phân chúng về một nhóm  ?
5. Ta có thể **dự đoán** điểm số của những học sinh dược không ?

---

## 📂 Dataset

- **Tên:** Student Alcohol Consumption 
- **Nguồn:** Public dataset ([Kaggle – dữ liệu nghiên cứu học thuật](https://www.kaggle.com/datasets/uciml/student-alcohol-consumption))
- **Số dòng:** gồm hai bộ dữ liệu **Toán ~395 dòng** và **Tiếng Bồ Đào Nha ~649 dòng**
- **Số cột:** 33 
- **Đối tượng:** Điểm só của những học sinh cấp hai của lớp **Toán** và **Tiếng Bồ Đào Nha**
### Một số thuộc tính quan trọng
- **Thông tin cá nhân:** `sex`, `age`, `address`, `famsize`, `Pstatus`, `Medu`, `Fedu`, `Mjob`, `Fjob`
- **Thông tin học tập:** `school`, `reason`, `guardian`
- **Thông tin thời gian:** `traveltime`, `studytime`, `failures`
- **Thông tin tài chính:** `schoolsup`, `famsup`, `paid`
- **Thông tin sinh hoạt:** `activities`, `nursery`, `higher`, `internet`, `romantic` 
- **Thông tin sức khỏe tinh thần:** `famrel`, `freetime`, `goout`, `Dalc`, `Walc`, `health`, `absences`
- **Thông tin điểm số:** `G1`, `G2`, `G3`

---

## 🧪 Quy trình Khai phá dữ liệu

### 1️⃣ Tiền xử lý dữ liệu ✔️
- Bộ dữ liệu gồm 2 bảng **Toán** và **Tiếng Bồ Đào Nha**
- Bộ dữ liệu không có dữ liệu thiếu hay trùng
- Thực hiện gộp 2 bảng lại tạo bảng mới phục vụ quá trình huán luyện mô hình
- Loại bỏ các cột mới sinh ra sau khi gộp (`Dalc`, `Walc`, `freetime`, `goout`)
  - Với dữ liệu phân loại ưu tiên lấy theo bảng **Toán** nếu không có thì lấy theo **Bồ**
  - Với dữ liệu số học sinh nào có 2 môn thì lấy **trung bình** không thì bỏ qua
- Với các cột điểm `G1`, `G2`, `G3` lấy **trung bình** với học sinh có cả hai môn, nếu chỉ có 1 môn thì lấy **điểm của môn đó**

### 2️⃣ Phân tích mô tả (EDA) ✔️
- Phân tích phân bố của biến mục tiêu (**G3**)
- Quan sát mối quan hệ giữa các nhóm dến biến mục tiêu
  - Học thuật (`G1`, `G2`, `failures`, ... )
  - Sử dụng đồ cồn (`Dalc`, `Walc`)
  - Gia đình / Xã hội (`famel`, `schoolsup`, ...)
- Sử dụng các biểu đồ Histogram để quan sát phân bố
- Scatter Plot để kiểm tra mối quan hệ
- Boxplot để check ngoại lai
- Heatmap để quan sát corrleration
  
### 3️⃣ Huấn luyện mô hình ✔️

### 4️⃣ Đánh giá mô hình ✔️

### 5️⃣ Rút ra insight - ý nghĩa ✖️

---

## 🤖 Các kỹ thuật Khai phá dữ liệu được sử dụng

### 🔹 Tuyến tính (Regression)
**Mục tiêu:** Dự đoán điểm số cuối kỳ (G3) của học sinh  

**Thuật toán:**
- Linear Regression
- Ridge / Lasso
- Random Forest Regressor
- Gradient Boosting

**Đánh giá:**
- MAE
- RMSE
- R^2

---

### 🔹 Phân cụm (Clustering)
**Mục tiêu:** Phân khúc học sinh theo điểm

**Thuật toán:**
- K-Means
- Hierarchical Clustering
- DBSCAN 

**Đánh giá:**
- Elbow Method
- Silhouette Score

---

## 📊 Kết quả & Insight chính


---

## 🗂️ Cấu trúc thư mục
```text
student-alcohol-consumption-data-mining/
│
├── README.md
│
├── configs/
│   ├── base.yaml
│   ├── regression.yaml      # Định nghĩa các cáu trúc tuyến tính
│   └── clustering.yaml      # Định nghĩa các cấu trúc phân cụm  
|
├── data/
│   ├── raw/
│   │   ├── student_mat.csv  # Học sinh lớp Toán 
│   │   └── student_por.csv  # Học ính lớp Tiếng Bồ
│   └── processed/
|       ├── student_merge.csv               # Bộ dữ liệu gộp từ 2 bảng Toán và Bồ
|       ├── student_merge_regression.csv    # Bộ dữ liệu sử dụng cho tuyến tính
│       └── student_merge_clustering.csv    # Bộ dữ liệu sử dụng cho phân cụm
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_eda.ipynb
│   ├── 04_regression.ipynb
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
- *P. Cortez and A. Silva. Using Data Mining to Predict Secondary School Student Performance*
- Kaggle: Student Alcohol Consumption Dataset
