## Customer Segmentation — Dự án cá nhân

- **Chính**: `Clustering-Project.ipynb` (tự triển khai)
- **Tham khảo/học**: thư mục `study/` (các notebook học từ YouTube, không phải kết quả dự án chính)

### 🎯 Mục tiêu
Phân khúc khách hàng để hỗ trợ quyết định marketing: ưu đãi phù hợp, giữ chân khách hàng, tối ưu chi phí. Dự án sử dụng phân cụm không giám sát (KMeans) trên dữ liệu khách hàng.

### 📊 Dữ liệu
- Bộ dữ liệu: Mall Customers (Kaggle) — tải qua `kagglehub` trong notebook
- Các cột chính: `CustomerID`, `Gender`, `Age`, `Annual Income (k$)`, `Spending Score (1-100)`

### 🔎 Cách tiếp cận (trong `Clustering-Project.ipynb`)
1. EDA nhanh: `head/info/describe`, biểu đồ phân phối, kiểm tra outliers
2. Chọn không gian đặc trưng và tìm số cụm k bằng:
   - **Elbow (Inertia)**
   - **Silhouette Score**
3. Huấn luyện **KMeans** và trực quan hóa kết quả (scatter 2D, scatter 3D)
4. Đặt tên/diễn giải cụm và đề xuất hành động marketing

### 🧪 Kết quả chính (tóm tắt)
- Age vs Spending Score → k ≈ **4**
  - Ví dụ: "Spending cao – Tuổi trẻ"; "Spending trung bình – Tuổi trẻ"; "Spending trung bình – Tuổi trung niên"; "Spending thấp – Tuổi 30+"
- Annual Income vs Spending Score → k ≈ **5**
- Annual Income + Spending Score + Age (3D) → k ≈ **4** (trực quan bằng `plotly`)

Gợi ý hành động mẫu theo cụm:
- **VIP bạo chi**: sản phẩm cao cấp, VIP tier, ưu đãi độc quyền, personalization
- **Trẻ ham deal**: flash sale, combo giá tốt, kênh social/TikTok Shop, referral
- **Trung lưu cân bằng**: combo tiết kiệm, loyalty, email remarketing theo mùa
- **Tiết kiệm thận trọng**: nhấn mạnh giá trị/ROI, bảo hành, mua nhiều giảm sâu

### 🚀 Cách chạy
1. Cài thư viện
```bash
pip install pandas numpy matplotlib seaborn scikit-learn plotly kagglehub
```
2. Mở và chạy notebook chính: `Clustering-Project.ipynb`
   - Cần internet cho lần đầu `kagglehub` tải dữ liệu
   - Nếu không dùng `kagglehub`, có thể tải CSV thủ công và sửa đường dẫn đọc file trong notebook

### 🧰 Thư viện sử dụng
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn` (KMeans, silhouette)
- `plotly` (trực quan 3D)
- `kagglehub` (tải dataset Kaggle)

### 🗂️ Ghi chú về thư mục `study/`
- `study/customer-segmentation-ytb.ipynb` dùng dữ liệu bán lẻ (`data/online_retail_II.xlsx`) để học quy trình RFM (Monetary, Frequency, Recency) và KMeans.
- Đây là tài liệu học tham khảo, **không phải** kết quả dự án chính.
