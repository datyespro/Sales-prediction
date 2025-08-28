
# 🛒 Sales Prediction – BigMart Dataset

## 📌 Giới thiệu

Dự án này xây dựng mô hình **Machine Learning** để dự đoán **doanh số bán hàng theo sản phẩm (Item\_Outlet\_Sales)** cho các sản phẩm tại hệ thống BigMart.

Mục tiêu chính:

* 🔎 Phân tích dữ liệu bán hàng
* 📈 Xây dựng mô hình dự đoán doanh số
* 🏪 Hỗ trợ doanh nghiệp quản lý tồn kho & tối ưu chiến lược

📂 Dataset: BigMart Sales Dataset – Kaggle

---

## 📊 Dataset

* 🗂 **Nguồn:** Kaggle – *BigMart Sales Dataset*
* 🛍 **Quy mô:** \~1.5k sản phẩm, 10 cửa hàng
* 🎯 **Biến mục tiêu:** `Item_Outlet_Sales` (Doanh thu theo sản phẩm)

---

## ⚙️ Quy trình xử lý

1️⃣ **Tải & chia dữ liệu**

* Import dữ liệu gốc, chia thành tập huấn luyện (70%) và tập kiểm tra (30%).

2️⃣ **Phân tích dữ liệu (EDA)**

* Kiểm tra dữ liệu, giá trị thiếu, thống kê mô tả.
* Trực quan hóa phân phối và mối quan hệ giữa các biến.

3️⃣ **Tiền xử lý & Feature Engineering**

* Chuẩn hóa và rút gọn nhóm sản phẩm (`Item_Type`).
* Điền giá trị thiếu cho `Item_Weight`, `Outlet_Size`.
* Chuẩn hóa `Item_Fat_Content` và xử lý đặc biệt cho sản phẩm **Non-Consumable**.

4️⃣ **Mã hóa dữ liệu phân loại**

* Sử dụng **OneHotEncoder** để chuyển dữ liệu categorical thành numerical.

5️⃣ **Huấn luyện mô hình**

* So sánh 3 mô hình:

  * 🌳 Decision Tree Regressor
  * 🌲 Random Forest Regressor
  * 🚀 XGBoost Regressor

6️⃣ **Đánh giá & Kết quả**

* Đo lường bằng **R²** và **RMSE** (sử dụng cross-validation).
* XGBoost cho kết quả tốt nhất trên tập test.
* Trực quan hóa: so sánh giá trị thực tế vs dự đoán, phân tích lỗi, top feature quan trọng.

---

## 📂 Cấu trúc dự án

```
/
├── README.md
├── environment.yml                # File môi trường Conda
├── Sales_Prediction_Starter.ipynb # Notebook chính
├── data/                          # Thư mục dữ liệu
```

---

## 🐍 Thiết lập môi trường (Anaconda)

### 🔧 Tạo file môi trường từ Conda (trên máy bạn)

```bash
conda activate ten_moi_truong
conda env export > environment.yml
```

### 📥 Cài đặt từ `environment.yml`

```bash
conda env create -f environment.yml
conda activate sales-prediction
```

### ▶️ Chạy Notebook

```bash
jupyter notebook Sales_Prediction_Starter.ipynb
```

---

## 🏆 Kết quả

* **Mô hình tốt nhất:** 🚀 XGBoost Regressor
* **Hiệu năng:** R² cao, RMSE thấp trên tập test
* **Insight:** Giá sản phẩm (MRP), loại sản phẩm và loại cửa hàng là những yếu tố quan trọng nhất ảnh hưởng đến doanh số

---

## 📜 License

📖 MIT License

---

## 👨‍💻 Tác giả

✍️ [Datyespro](https://github.com/datyespro)


