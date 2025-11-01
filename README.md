# Final_Project
# Dự Báo Doanh Số Và Phân Tích Lợi Nhuận Cho Chuỗi Siêu Thị
## 1. Giới thiệu Dự án

Dự án này tập trung vào việc dự báo doanh số bán hàng và phân tích lợi nhuận của chuỗi cửa hàng bán lẻ (Superstore) bằng các mô hình chuỗi thời gian (time series) và phân tích dữ liệu kinh doanh.

* Mục tiêu chính:
    * Dự báo doanh số (Sales Forecasting) cho Superstore trong 6 tháng tới bằng mô hình Holt-Winter Forecast.
    * Phân tích lợi nhuận (Profit Analysis) để xác định yếu tố ảnh hưởng đến lợi nhuận, phân khúc khách hàng và danh mục hàng hóa hiệu quả.
    * Đề xuất chiến lược cải thiện doanh thu và lợi nhuận dựa trên kết quả mô hình và insight thực tế.

## 2. Phương pháp (Methodology)

* Phân tích mô tả (Descriptive Analysis): Sử dụng các chỉ số thống kê và biểu đồ trực quan (cột, đường, heatmap) để nhận diện xu hướng kinh doanh chính như doanh thu theo tháng, phân bố đơn hàng theo phương thức vận chuyển và tác động của chiết khấu đến lợi nhuận.

* Phân tích tương quan (Correlation Analysis): Đánh giá mối quan hệ giữa các biến kinh doanh chủ chốt — chiết khấu, doanh thu, lợi nhuận và biên lợi nhuận — nhằm xác định ảnh hưởng của chính sách chiết khấu đến hiệu quả hoạt động.

* Mô hình dự báo (Forecasting Model): Áp dụng mô hình Holt–Winters Exponential Smoothing để dự báo doanh thu 6–12 tháng tới, tận dụng đặc điểm xu hướng (trend) và mùa vụ (seasonality) của dữ liệu.

* Kiểm định: Xây dựng các kịch bản giảm chiết khấu để phân tích tác động tiềm năng đến doanh thu và lợi nhuận, hỗ trợ ra quyết định kinh doanh chiến lược.

***
**Enrollies'data**

* Tên dataset: Superstore Dataset (Kaggle – “Superstore Dataset Final”)
* Nguồn: `https://www.kaggle.com/datasets/vivek468/superstore-dataset-final/data`
* Cột dữ liệu
```
Row ID => Unique ID for each row.
Order ID => Unique Order ID for each Customer.
Order Date => Order Date of the product.
Ship Date => Shipping Date of the Product.
Ship Mode=> Shipping Mode specified by the Customer.
Customer ID => Unique ID to identify each Customer.
Customer Name => Name of the Customer.
Segment => The segment where the Customer belongs.
Country => Country of residence of the Customer.
City => City of residence of of the Customer.
State => State of residence of the Customer.
Postal Code => Postal Code of every Customer.
Region => Region where the Customer belong.
Product ID => Unique ID of the Product.
Category => Category of the product ordered.
Sub-Category => Sub-Category of the product ordered.
Product Name => Name of the Product
Sales => Sales of the Product.
Quantity => Quantity of the Product.
Discount => Discount provided.
Profit => Profit/Loss incurred.
```
link Google Colab: `https://colab.research.google.com/drive/1hSVeCvYeQvhUrJLBbMKy3CYuoSVVCguf?usp=sharing`

## 3. Phân tích (Analysis)
### 3.1. Chuẩn bị dữ liệu
* Kiểm tra tổng quan
* Data Cleaning

### 3.2. Phân tích khám phá dữ liệu (EDA)
* Tổng quan hiệu suất kinh doanh
* Xu hướng doanh số theo thời gian
* Phân tích theo vùng (Region)
* Phân tích theo danh mục sản phẩm (Category)
* Chiết khấu và hiệu quả đơn hàng
* Phân tích theo phân khúc khách hàng
* Phân tích theo logistic (Ship Mode / Shipping Time)
* Hệ số tương quan giữa các yếu tố
* Dự báo doanh thu
* Kiểm định giả thuyết

## 4. Kết quả (Result)
**Kết quả chính**

* Office Supplies: doanh số cao nhất nhưng lợi nhuận thấp – giúp duy trì dòng tiền.
* Furniture: doanh thu lớn nhưng biên lợi nhuận chỉ ~2.5% → rủi ro tài chính cao.
* Technology: dẫn đầu cả doanh thu và lợi nhuận → mảng cốt lõi nên tập trung đầu tư.
* Tables & Bookcases lỗ nặng, Copiers sinh lời tốt nhất.
* Chiết khấu cao làm giảm mạnh lợi nhuận, nhưng không giúp tăng doanh số đáng kể.

## 5. Kết luận (Conclusion)
* Phân tích mô tả cho thấy doanh thu có xu hướng biến động theo mùa, với các giai đoạn tăng mạnh vào giữa và cuối năm. Phương thức vận chuyển “Standard Class” chiếm tỷ trọng đơn hàng lớn nhất, trong khi “Same Day” có thời gian giao hàng ngắn nhất nhưng chi phí cao hơn.

* Kết quả phân tích tương quan chỉ ra rằng chiết khấu có mối quan hệ nghịch với lợi nhuận và biên lợi nhuận, cho thấy việc giảm chiết khấu có thể giúp cải thiện hiệu quả kinh doanh nếu không làm giảm đáng kể doanh thu.

* Mô hình Holt–Winters Exponential Smoothing cho thấy doanh thu dự kiến sẽ tiếp tục tăng nhẹ trong 6–12 tháng tới, phản ánh xu hướng tích cực nhưng có yếu tố dao động theo mùa.

* Các kịch bản giả định về việc giảm chiết khấu xuống ở mức dưới 20% có thể giúp tối ưu lợi nhuận tổng thể mà không ảnh hưởng lớn đến doanh thu. Điều này cung cấp căn cứ cho việc điều chỉnh chính sách chiết khấu nhằm cân bằng giữa tăng trưởng doanh thu và biên lợi nhuận.




