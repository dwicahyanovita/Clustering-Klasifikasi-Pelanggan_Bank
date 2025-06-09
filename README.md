# Clustering(KMeans) dan Klasifikasi(DecisionTree) Pelanggan Bank

## Deskripsi
Menerapkan metode unsupervised learning yaitu clustering, proyek ini bertujuan untuk membentuk segmentasi pelanggan bank yang merepresentasikan pola-pola pembelian yang serupa. Hasil segmentasi ini diharapkan dapat memberikan insight yang bernilai bagi pihak manajemen, khususnya dalam menyusun strategi promosi yang lebih tepat sasaran, mengembangkan program loyalitas, serta mengoptimalkan layanan pelanggan.
## Langkah-langkah Proyek

### 1. Persiapan Data

* Import library dan load dataset
* Eksplorasi data: `head()`, `info()`, `describe()`, korelasi fitur, dan visualisasi
* Pembersihan dan pra-pemrosesan:

  * Cek data kosong dan duplikat
  * Feature scaling (MinMaxScaler)
  * Encoding untuk data kategorikal
  * Drop kolom ID

### 2. Clustering (Segmentasi Pelanggan) menggunakan KMeans

Menggunakan metode clustering untuk membagi pelanggan ke dalam 3 kelompok:
Berikut adalah **rata-rata umur dan saldo** dari hasil clustering pelanggan bank:

### Rata-rata Umur dan Saldo per Cluster:

| Cluster | Rata-rata Umur (tahun) | Rata-rata Saldo (Account Balance) |
| ------- | ---------------------- | --------------------------------- |
| 0       | 45.08                  | 9,896.75                          |
| 1       | 26.11                  | 1,764.04                          |
| 2       | 62.20                  | 4,362.17                          |

* **Cluster 0:** Nasabah paruh baya, saldo tinggi, transaksi stabil
  💡 Cocok ditawari produk seperti deposito dan konsultasi keuangan.

* **Cluster 1:** Nasabah muda, saldo rendah, aktivitas rendah
  💡 Perlu edukasi keuangan dan penawaran produk dasar.

* **Cluster 2:** Nasabah lansia, saldo menengah, sering gunakan ATM
  💡 Dapat ditarget dengan program loyalitas usia lanjut dan layanan pensiun.

### 3. Klasifikasi menggunakan Decision Tree

Setelah segmentasi selesai, dilakukan klasifikasi untuk memprediksi cluster pelanggan baru menggunakan model supervised learning:

* **Algoritma yang digunakan:**

  * K-Nearest Neighbors (KNN)
  * Decision Tree (DT)
  * Random Forest (RF)
  * Support Vector Machine (SVM)
  * Naive Bayes (NB)

* **Hasil Evaluasi Model:**

| Model                     | Accuracy | Precision | Recall | F1-Score |
| ------------------------- | -------- | --------- | ------ | -------- |
| K-Nearest Neighbors (KNN) | 0.8079   | 0.8113    | 0.8075 | 0.8062   |
| Decision Tree (DT)        | 0.9883   | 0.9888    | 0.9873 | 0.9880   |
| Random Forest (RF)        | 0.9836   | 0.9828    | 0.9834 | 0.9831   |
| Support Vector Machine    | 0.7588   | 0.7603    | 0.7625 | 0.7592   |
| Naive Bayes (NB)          | 0.9485   | 0.9482    | 0.9489 | 0.9472   |

---

**Dibuat dengan ❤️ oleh Dwi Cahya Novita**
untuk memenuhi tugas course **Belajar Machine Learning untuk Pemula** di **Dicoding**

---

