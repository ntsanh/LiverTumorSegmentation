# Liver Tumor Segmentation using Deep Learning

## Giới thiệu
Dự án thực hiện bài toán **phân đoạn gan và khối u gan trên ảnh CT** bằng phương pháp học sâu. Hai mô hình được xây dựng và so sánh gồm:
- **UNet_Baseline**
- **UNet_TxBottleneck (U-Net + Transformer tại bottleneck)**

## Dữ liệu
- Bộ dữ liệu: **LiTS – Liver Tumor Segmentation**
- Dữ liệu CT 3D được tiền xử lý và chuyển sang **2D slices (.npy)**
- Nhãn gồm 3 lớp: background (0), gan (1), khối u (2)

## Phương pháp
- Kiến trúc nền tảng: **U-Net**
- Mô hình cải tiến: thêm **Transformer block** tại bottleneck để học ngữ cảnh toàn cục
- Hàm loss: **Cross-Entropy + Dice Loss**
- Đánh giá bằng: **Dice coefficient, IoU**

## Thực nghiệm
- Huấn luyện và đánh giá trên Google Colab (GPU)
- So sánh định lượng và trực quan kết quả trên tập test
- Lưu checkpoint, history, metrics và hình ảnh trực quan

## Cấu trúc thư mục
...

## Kết quả
- UNet_TxBottleneck cho kết quả **tốt hơn UNet_Baseline** ở Dice/IoU trên tập test
- Cải thiện rõ rệt ở các slice có khối u nhỏ

## Công nghệ sử dụng
TensorFlow/Keras, NumPy, OpenCV, scikit-image, Google Colab

---
