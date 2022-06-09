# Một số phương pháp học không giám sát cho bài toán dự đoán liên kết trên mạng xã hội

## 1. Người thực hiện và người hướng dẫn:
- Người thực hiện: Trần Hoàng Đức - K63A5 - HUS
- Người hướng dẫn: TS. Hoàng Tuấn Anh

## 2. Giới thiệu chung:
- Dự đoán liên kết trên mạng xã hội đã thu hút sự chú ý rộng rãi vì nó vừa có thể phát hiện ra các kết nối ẩn vừa có thể dự đoán các liên kết trong tương lai. Các dự đoán này có thể giúp tìm ra khách hàng tiềm năng, hay định hình thứ bậc, phân loại của một cá nhân, tổ chức dựa vào các mối quan hệ của họ trong mạng xã hội.

- Khóa luận này nghiên cứu, tìm hiểu các thuật toán dự đoán liên kết không được giám sát cho bài toán dự đoán liên kết trên mạng xã hội, Cụ thể, khóa luận khảo nghiệm hiệu năng của các thuật toán dựa trên Lân cận chung, hệ số Jaccard, Adamic / Adar, Simrank, đi bộ ngẫu nhiên có khởi động lại Pagerank.


## 3. Công cụ, ngôn ngữ sử dụng:
**Ngôn ngữ lập trình:** 
- Python

**IDE, Code Editor:** 
- Jupyter notebook

**Thư viện sử dụng:**
- networkX: 2.8.3
- matplotlib.pyplot: 3.5.2
- random


## 4. Thực nghiệm:
**Tập dữ liệu:**
- ego-Facebook
- wiki-Vote
- feather-lastfm-social
- soc-sign-bitcoin-otc
- feather-deezer-social

Nguồn dữ liệu: https://snap.stanford.edu/data/

**Thuật toán sử dụng:**
- Thuật toán Jaccard
- Thuật toán Common neighbors
- Thuật toán Adamic / Adar
- Thuật toán Pagerank
- Thuật toán Simrank

**Các bước triển khai thực nghiệm:**
- Bước 1 : Đọc dữ liệu từ tập dữ liệu, xây dựng các đồ thị bằng thư viện networkX.
- Bước 2 : Chọn ngẫu nhiên và xóa bỏ một lượng cạnh nhất định.
- Bước 3 : Dùng các thuật toán tính điểm để đánh giá khả năng xuất hiện liên kết giữa các đỉnh.
- Bước 4 : Chọn ra top 20 đỉnh có số điểm đánh giá cao nhất với mỗi thuật toán, so sánh các cạnh dự đoán và các cạnh đã xóa.
- Bước 5 : Từ kết quả thu được, lấy ra bảng đánh giá và vẽ biểu đồ kết quả thực nghiệm.

## 5. Kết luận và hướng phát triển:
**Kết luận:**
- Hai thuật toán Jaccard và Adamic / Adar có tỉ lệ đúng rất cao.
- Hai thuật toán Pagerank và Simrank cho kết quả thấp hơn.
- Hai thuật toán Simrank và lân cận chung có thời gian chạy tương đối lâu cho các dữ liệu lớn (trên 24h).
- Ba thuật toán Jaccard , Adamic / Adar, Pagerank phù hợp cho quá trình kiểm tra nhanh (dưới 1h).

**Hướng phát triển:**
- Tiến hành các khảo nghiệm với nhiều tập dữ liệu khác.
- Thay đổi số lượng dự đoán.
- Code lại các thuật toán theo lý thuyết mà không dùng thư viện.
