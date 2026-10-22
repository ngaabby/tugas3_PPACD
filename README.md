# Tugas 3 - Praktikum Analisis Citra Digital (PACD)

Repository ini berisi tugas praktikum PACD (Pertemuan 3) mengenai klasifikasi citra digit tulisan tangan (*handwritten digits*) menggunakan dataset **MNIST** dengan arsitektur **Convolutional Neural Network (CNN)** pada Keras / TensorFlow.

## Isi Tugas
1. **Modifikasi Hyperparameter:**
   - Memodifikasi satu bagian hyperparameter, yaitu **algoritma optimizer** pada `model.compile()` dari **Adam** menjadi **SGD** *(Stochastic Gradient Descent)*.
2. **Perbandingan Hasil & Evaluasi:**
   - Menguji performa model dengan metrik *loss* dan *accuracy* (pada data latih, validasi, dan data uji).
   - Menampilkan visualisasi kurva loss, accuracy, serta prediksi sampel citra.
3. **Kesimpulan dan Pembelajaran:**
   - Memberikan analisis komprehensif mengenai perbedaan kecepatan konvergensi, kualitas representasi bobot, dan karakteristik kedua optimizer.

## Ringkasan Hasil Eksperimen

| Metrik Evaluasi | Baseline (`Adam`) | Modifikasi (`SGD`) | Analisis |
| :--- | :---: | :---: | :--- |
| **Train Loss (Epoch 3)** | 0.0440 | 0.2709 | Adam meminimalkan loss jauh lebih tajam |
| **Train Accuracy (Epoch 3)** | 98.63% | 91.77% | SGD tertinggal -6.86% |
| **Val Accuracy (Epoch 3)** | 98.28% | 91.52% | Akurasi validasi Adam lebih stabil |
| **Test Accuracy** | **98.57%** | **92.55%** | **Adam unggul 6.02% pada data uji** |
| **Prediksi 10 Sampel Uji** | 10/10 Benar (100%) | 9/10 Benar (90%) | SGD mengalami 1 misklasifikasi (digit 5 tertebak 6) |

---
**File Notebook:** [`ppacd3.ipynb`](ppacd3.ipynb)
