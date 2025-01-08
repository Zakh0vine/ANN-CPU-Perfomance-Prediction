# CPU Performance Prediction


## Kontributor
- Achmad Ata Irsyaduduin (21102013)
- Aditya Setiawan (21102034)

## Deskripsi Proyek

Program ini dirancang untuk memprediksi kinerja CPU menggunakan dataset dari UCI Machine Learning Repository. Model yang digunakan adalah Neural Network yang dilatih menggunakan PyTorch. Proyek ini mencakup proses preprocessing data, pelatihan model, evaluasi kinerja, dan visualisasi hasil prediksi.

## Fitur

- Mengunduh dan memproses dataset kinerja CPU.
- Melakukan standarisasi data menggunakan `StandardScaler` dari scikit-learn.
- Melatih model Neural Network menggunakan PyTorch.
- Mengevaluasi kinerja model dengan metrik seperti R² dan Mean Squared Error (MSE).
- Menyediakan visualisasi hasil prediksi dan perbandingan dengan data aktual.

## Dataset

Dataset yang digunakan berasal dari UCI Machine Learning Repository dan dapat diakses melalui tautan berikut: [CPU Performance Dataset](https://archive.ics.uci.edu/ml/machine-learning-databases/cpu-performance/machine.data)

Kolom-kolom dalam dataset:

- `MYCT`: Time in microseconds to execute one machine cycle.
- `MMIN`: Minimum main memory in kilobytes.
- `MMAX`: Maximum main memory in kilobytes.
- `CACH`: Cache memory in kilobytes.
- `CHMIN`: Minimum channels.
- `CHMAX`: Maximum channels.
- `PRP`: Published relative performance.
- `ERP`: Estimated relative performance (target output).

## Prasyarat

Pastikan lingkungan Python Anda memiliki pustaka berikut:

```
pip install torch pandas numpy scikit-learn matplotlib seaborn
```

## Struktur Kode

1. **Import Library**: Mengimpor pustaka yang dibutuhkan seperti PyTorch, pandas, numpy, dll.
2. **Memuat Dataset**: Mengunduh data dari UCI dan membagi menjadi fitur (X) dan target (y).
3. **Preprocessing Data**: Menghapus kolom yang tidak relevan dan melakukan standarisasi fitur.
4. **Konversi ke Tensor**: Mengonversi data ke tensor PyTorch untuk digunakan dalam model.
5. **Membangun Model Neural Network**: Membangun arsitektur model menggunakan PyTorch.
6. **Training Model**: Melatih model dengan DataLoader.
7. **Evaluasi Kinerja**: Menghitung MSE dan R² untuk mengevaluasi performa model.
8. **Visualisasi Hasil**: Membuat grafik perbandingan hasil prediksi dengan nilai aktual.

## Penggunaan

1. Jalankan skrip Jupyter Notebook dengan perintah berikut:

```
jupyter notebook try_2.ipynb
```

2. Ikuti langkah-langkah dalam notebook untuk memuat data, melatih model, dan melihat hasil evaluasi.

## Hasil Evaluasi

Model akan menampilkan metrik berikut setelah pelatihan:

- **Mean Squared Error (MSE)**: Mengukur kesalahan kuadrat rata-rata.
- **R² (R-squared)**: Mengukur seberapa baik model menjelaskan variasi dalam data.

Visualisasi prediksi dibandingkan dengan data aktual juga akan ditampilkan untuk analisis lebih lanjut.

## Catatan Penting

- Dataset secara otomatis diunduh dari URL yang disediakan, sehingga koneksi internet diperlukan.
- Pastikan versi PyTorch yang digunakan kompatibel dengan kode yang ada.



---

Jika Anda memiliki pertanyaan atau saran perbaikan, jangan ragu untuk menghubungi saya!

