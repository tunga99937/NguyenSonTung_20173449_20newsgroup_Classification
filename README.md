# project1_ANN_NB_SVM
# Tập dữ liệu :
  Sử dụng tập dữ liệu 20newsgroup phiên bản 20news-18828 ( không gồm những văn bản trùng lặp và những văn bản thuộc nhiều chủ đề; dữ liệu chưa được phân loại thành tập train và test). Tập train và test được chia theo tỉ lệ 6/4 :
   - Dữ liệu được lưu trong 2 folder : 20newsgroup_train và 20newsgroup_test
   - Nhãn lớp của các văn bản được lưu vào 2 file : train_label.data và test_label.data
## Chú ý:
   Việc xử lý tập dữ liệu (phân thành 2 tập train và test, tạo các file label,...) được thực hiện khi làm việc với mạng ANN, 2 phương pháp còn lại sử dụng lại dữ liệu đã được xử lý đó
# So sánh 3 phương pháp : 
## 1. Naive Bayes:
  Sử dụng mô hình Multinomial Naive Bayes : chủ yếu được sử dụng trong phân loại văn bản mà feature vectors được tính bằng Bags of Words 
  Độ chính xác của tập dự đoán là 86%
## 2. SVM:
  Sử dụng mô hình LinearSVC (Linear Support Vector Classification) với chiến lược “one-vs-the-rest”
  Độ chính xác của tập dựu đoán là 87% (cao nhất trong 3 phương pháp)
## 3. Neural Network:
  - Mạng neural gồm 2 tầng:
   + Mỗi tầng có kích thước là 100 nút
   + Activation function : rectified linear unit (ReLu) : f(x) = max(0,x)
  - Quá trình học trải qua 15 lần liên tiếp
  - Độ chính xác của tập dự đoán là 77% ( thấp nhất trong 3 phương pháp), lý do:
   + Chưa tạo được một từ điển tốt : Vẫn tồn tại những từ vô nghĩa và những stopwords
   + Số lần học chưa đủ nhiều
   
     
  
