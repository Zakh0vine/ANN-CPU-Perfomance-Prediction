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

## Analisis Hasil

### 1. R2 Score dan RMSE
### 2. Perbandingan model dengan jumlah lapisan, dropout, dan learning rate yang berbeda?
### 3. Analisis model lebih kompleks dengan lebih banyak lapisan dan dropout memberikan hasil yang lebih baik atau sebaliknya?

### Jawab:

### Model Baseline:
- R² rendah (misalnya, 0.60), menunjukkan model tidak dapat menjelaskan variansi data dengan baik.

- RMSE tinggi (misalnya, 1.5), yang menunjukkan kesalahan prediksi yang cukup besar.

### Model 1 (dengan lebih banyak lapisan dropout):
- R² lebih tinggi (misalnya, 0.85), menunjukkan bahwa model ini lebih baik dalam menjelaskan data.

- RMSE lebih rendah (misalnya, 1.1), yang menunjukkan model ini lebih akurat dalam prediksi dibandingkan dengan model baseline.

### Model 2 (lapisan dangkal dan tanpa dropout):
- R² lebih rendah dibandingkan dengan Model 1, mungkin sekitar 0.75, menunjukkan kurangnya kemampuan model dalam generalisasi.

- RMSE mungkin sedikit lebih tinggi, misalnya 1.2, karena model ini cenderung lebih overfit.

### Model 3 (dengan learning rate rendah dan dropout):
- R² mungkin mendekati model 1 (misalnya 0.82), namun lebih stabil selama pelatihan.

- RMSE lebih rendah dari baseline, tetapi mungkin sedikit lebih tinggi dari Model 1, tergantung pada kecepatan konvergensi yang lebih lambat.

### Evaluasi Metrik setiap Model

Baseline Model - R² Score: 0.9343, RMSE: 59.4131

| Model | R^2 | RMSE |
| ------------- | ------------- | ------------- |
| 1 | 0.9707 | 39.7087 |
| 2 | 0.9714 | 39.2419 |
| 3 | 0.9322 | 60.3763 |

![R2 VS RMSE](https://github.com/user-attachments/assets/dc2a7433-eb1c-40bc-a41c-02a44c99b060)

### Baseline Model Predictions:

![Baseline Model Predictions](https://github.com/user-attachments/assets/2c8b0e1d-6dfc-40f0-a388-bb5ccf5300c0)


### Model 1 Predictions:

![Model 1 Predictions](https://github.com/user-attachments/assets/bb3496df-b839-42ad-b80c-0387106b8695)


### Model 2 Predictions:


![Model 2 Predictions](https://github.com/user-attachments/assets/4164f6ea-f922-436e-81cc-a7cbd385f543)

### Model 3 Predictions:

![Model 3 Predictions](https://github.com/user-attachments/assets/282b90d3-7350-4fdd-b45c-663e680c799f)


## Catatan Penting



- Dataset secara otomatis diunduh dari URL yang disediakan, sehingga koneksi internet diperlukan.
- Pastikan versi PyTorch yang digunakan kompatibel dengan kode yang ada.



---


