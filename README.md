#  Ứng dụng xử lý ngôn ngữ tự nhiên (NLP) trong phân loại tin nhắn rác

## Giới thiệu
Dự án áp dụng kỹ thuật **Xử lý ngôn ngữ tự nhiên (Natural Language Processing - NLP)** và các mô hình học máy (**Machine Learning**) để phân loại tin nhắn SMS/email thành **Spam** hoặc **Non-Spam**.  
Mục tiêu: Xây dựng hệ thống lọc tin nhắn rác hiệu quả, có thể triển khai thực tế trong ứng dụng email hoặc SMS.

---

##  Dữ liệu
- **Cấu trúc**:
  - `Message_body`: Nội dung tin nhắn/email.
  - `Label`: Nhãn (`Spam` hoặc `Non-Spam`).
- **Kích thước**:
  - `SMS_train.csv`: Dữ liệu huấn luyện.
  - `SMS_test.csv`: Dữ liệu kiểm thử.

---

##  Quy trình thực hiện
1. **Tiền xử lý văn bản**:
   - Chuyển toàn bộ văn bản về chữ thường.
   - Loại bỏ ký tự đặc biệt, số, dấu câu.
   - Loại bỏ stopwords.
   - Tokenization và stemming.
2. **Trích xuất đặc trưng**:
   - Sử dụng **Bag of Words** hoặc **TF-IDF Vectorizer**.
3. **Huấn luyện mô hình**:
   - Thử nghiệm các mô hình: Naive Bayes, Logistic Regression, SVM.
4. **Đánh giá mô hình**:
   - Accuracy, Precision, Recall, F1-score.
   - Ma trận nhầm lẫn (Confusion Matrix).

---

## Kết quả (ví dụ với Multinomial Naive Bayes + TF-IDF)
- **Accuracy**: 97.8% trên tập kiểm thử.
- **Precision**: 0.98
- **Recall**: 0.97
- **F1-score**: 0.975
- **Ma trận nhầm lẫn**:

|                | Predicted Spam | Predicted Non-Spam |
|----------------|----------------|--------------------|
| **Actual Spam**     | 56             | 2                  |
| **Actual Non-Spam** | 3              | 64                 |

---

