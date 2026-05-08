# Optimasi Strategi Pemasaran (Data Analysis Project)

## Deskripsi Proyek

Proyek ini bertujuan untuk menganalisis data penjualan e-commerce menggunakan Python dan Google Colab. Analisis dilakukan untuk memahami pola penjualan, perilaku pelanggan, serta performa produk berdasarkan data transaksi.

Teknik analisis yang digunakan meliputi:

* Data Cleaning
* Data Visualization
* RFM Analysis
* Analisis Tren Penjualan
* Analisis Produk Underperformer
* Linear Regression

---

## Business Question

Analisis ini dilakukan untuk menjawab beberapa pertanyaan berikut:

* Produk apa yang memiliki harga tinggi tetapi jumlah penjualannya rendah?
* Bagaimana tren penjualan dari waktu ke waktu?
* Siapa pelanggan terbaik berdasarkan perilaku transaksi?
* Apakah jumlah pembelian berpengaruh terhadap total penjualan?

---

## Dataset

Dataset yang digunakan merupakan dataset transaksi retail/e-commerce dengan beberapa kolom utama berikut:

* `InvoiceNo`
* `StockCode`
* `Description`
* `Quantity`
* `InvoiceDate`
* `UnitPrice`
* `CustomerID`
* `Country`

Dataset kemudian diproses untuk menghasilkan kolom tambahan:

* `Total_Sales`
* `Month`

---

## Data Wrangling

Tahapan pembersihan data yang dilakukan:

### 1. Mengubah Format Tanggal

Kolom `InvoiceDate` diubah menjadi format datetime agar dapat digunakan untuk analisis waktu.

### 2. Menghapus Data Tidak Valid

Data dengan:

* `Quantity <= 0`
* `UnitPrice <= 0`

dihapus karena dianggap tidak valid atau merupakan data retur.

### 3. Menambahkan Kolom Total Penjualan

Dilakukan perhitungan:

```python
Total_Sales = Quantity × UnitPrice
```

### 4. Menambahkan Kolom Bulan

Kolom `Month` dibuat untuk analisis tren penjualan bulanan.

---

## Insights

### Tren Penjualan Bulanan

Hasil visualisasi menunjukkan bahwa penjualan mengalami perubahan pada beberapa periode tertentu. Terdapat bulan dengan peningkatan penjualan yang cukup signifikan dibanding bulan lainnya.

---

### Underperformer Product

Analisis menunjukkan bahwa beberapa produk dengan harga tinggi memiliki jumlah pembelian yang rendah. Hal ini mengindikasikan bahwa harga produk dapat memengaruhi minat pembelian pelanggan.

---

### RFM Analysis

Segmentasi pelanggan dilakukan berdasarkan:

* **Recency** → Seberapa lama pelanggan terakhir bertransaksi
* **Frequency** → Seberapa sering pelanggan melakukan transaksi
* **Monetary** → Total pengeluaran pelanggan

Hasil analisis menunjukkan bahwa:

* Pelanggan dengan skor RFM tinggi termasuk pelanggan loyal
* Pelanggan dengan skor rendah berpotensi tidak aktif

---

### Linear Regression

Dilakukan analisis regresi linear sederhana untuk melihat hubungan antara `Quantity` dan `Total_Sales`.

Hasil menunjukkan bahwa jumlah pembelian memiliki pengaruh terhadap total penjualan, sehingga peningkatan quantity dapat meningkatkan revenue perusahaan.

---

## Visualization

Visualisasi yang digunakan dalam proyek ini meliputi:

* Line Chart → Tren Penjualan Bulanan
* Scatter Plot → Underperformer Product
* Tabel RFM Analysis

---

## Recommendation

Berdasarkan hasil analisis, beberapa rekomendasi yang dapat diberikan adalah:

* Mengevaluasi produk dengan harga tinggi tetapi penjualan rendah
* Memberikan program loyalitas kepada pelanggan dengan skor RFM tinggi
* Mengoptimalkan strategi pemasaran pada periode dengan tren penjualan tinggi
* Menggunakan data penjualan sebagai dasar pengambilan keputusan bisnis

---

## Kesimpulan

Berdasarkan hasil analisis data yang dilakukan, dapat disimpulkan bahwa perilaku pelanggan, harga produk, dan jumlah pembelian memiliki pengaruh terhadap performa penjualan.

Penggunaan analisis data membantu perusahaan dalam memahami kondisi bisnis secara lebih mendalam sehingga strategi pemasaran dapat dilakukan secara lebih efektif dan efisien.
