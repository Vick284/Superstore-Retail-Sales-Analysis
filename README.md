# 📊 Superstore Giant: Profit Optimization & Strategic Analysis
> **Dự án tốt nghiệp khóa DA95 - Phân tích yếu tố ảnh hưởng đến lợi nhuận và xây dựng mô hình Machine Learning dự báo đơn hàng.**

---

## 📖 1. Tổng quan dự án (Context)
Dự án tập trung vào việc giải quyết bài toán kinh doanh thực tế tại chuỗi siêu thị bán lẻ **Superstore Giant**. Mục tiêu cốt lõi là trả lời câu hỏi: *"Tại sao doanh thu (Sales) tăng trưởng nhưng lợi nhuận (Profit) vẫn không đạt kỳ vọng?"*. 

Thông qua dữ liệu, dự án xác định các "điểm đen" gây thua lỗ và đề xuất chiến lược tối ưu hóa lợi nhuận thay vì chạy theo doanh thu ảo.

## 🛠 2. Công nghệ & Thư viện (Tech Stack)
* **Ngôn ngữ:** Python 3.x
* **Phân tích & Xử lý:** `Pandas`, `NumPy`
* **Trực quan hóa:** `Matplotlib`, `Seaborn` (Biểu đồ nhiệt, biểu đồ phân tán, histogram)
* **Machine Learning:** `Scikit-learn`
    * Mô hình: `Logistic Regression`, `Random Forest`, `Gradient Boosting`
* **Xử lý dữ liệu mất cân bằng:** `SMOTE` (Synthetic Minority Over-sampling Technique)

## 📁 3. Cấu trúc dự án
* `DA95_FinalProject_TRAN NGUYEN SI DAN.ipynb`: Mã nguồn thực thi chi tiết (EDA, Pre-processing, Modeling).
* `DA95_FinalProject_TRAN NGUYEN SI DAN.pdf`: Báo cáo chiến lược và thuyết trình kết quả.
* `Superstore_Dataset.csv`: Dữ liệu đầu vào (Thông tin đơn hàng, khách hàng, doanh thu, lợi nhuận).

## 🚀 4. Quy trình thực hiện (Methodology)

### Bước 1: Khám phá dữ liệu (EDA)
- Phân tích sự phân bổ Doanh thu & Lợi nhuận theo khu vực (Region), Nhóm hàng (Category).
- Nhận diện các đơn hàng có lợi nhuận âm (Loss-making orders).

### Bước 2: Phân tích chuyên sâu (Business Analysis)
- Đánh giá tác động của chính sách **Discount** (Chiết khấu) đến biên lợi nhuận.
- Tìm kiếm ngưỡng chiết khấu tối ưu.

### Bước 3: Tiền xử lý dữ liệu
- Xử lý các giá trị ngoại lai (Outliers).
- Mã hóa biến phân loại (Label Encoding).
- Cân bằng dữ liệu bằng **SMOTE** để cải thiện khả năng dự báo đơn hàng High Profit.

### Bước 4: Huấn luyện mô hình (Machine Learning)
- Xây dựng mô hình phân loại để dự đoán khả năng sinh lời của đơn hàng trước khi thực hiện giao dịch.
- So sánh hiệu suất giữa các thuật toán dựa trên F1-Score và AUC-ROC.

## 💡 5. Kết quả & Insights quan trọng (Key Findings)

* **⚠️ Ngưỡng chiết khấu "Tử thần":** Khi **Discount > 25%**, xác suất đơn hàng có lợi nhuận gần như bằng **0**. 
* **Yếu tố quyết định:** `Discount` là biến có sức mạnh dự báo Profit lớn nhất, quan trọng hơn cả `Sales` hay `Quantity`.
* **Mô hình tối ưu:** `Gradient Boosting` đạt hiệu quả cao nhất trong việc nhận diện các đơn hàng tiềm năng mang lại lợi nhuận cao.

## 📈 6. Đề xuất chiến lược (Recommendations)

1.  **Thiết lập chính sách Discount dựa trên dữ liệu:**
    * Chặn ngưỡng chiết khấu trần theo từng danh mục. Đặc biệt kiểm soát chặt nhóm **Furniture** (Nội thất).
2.  **Ứng dụng AI vào vận hành:**
    * Tích hợp mô hình dự báo vào phần mềm bán hàng để cảnh báo nhân viên Sale ngay khi mức chiết khấu đề xuất đe dọa đến lợi nhuận đơn hàng.
3.  **Thay đổi tư duy tăng trưởng:**
    * Tập trung vào các nhóm hàng **High-margin** thay vì giảm giá sâu để lấy doanh thu.

---

## 👤 Thông tin tác giả
* **Học viên:** Trần Nguyễn Sĩ Đan
* **Khóa học:** DA95 - Data Analysis
* **Mentor:** Nguyễn Việt Nin
