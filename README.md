# Prediksi Gaji UMR di Indonesia

## Domain Proyek

Di Indonesia, ketimpangan upah antar wilayah jadi isu besar yang sering terlupakan, meski dampaknya nyata bagi ekonomi daerah dan pekerja. Misalnya, Jakarta yang dikenal sebagai pusat perekonomian punya standar gaji yang jauh lebih tinggi dibandingkan dengan kota-kota di luar Pulau Jawa atau Indonesia Timur. Hal ini menciptakan kesenjangan dalam mobilitas tenaga kerja dan kualitas hidup.

Ketimpangan ini juga memperburuk distribusi pendapatan yang tidak merata, sehingga penting untuk memahami bagaimana gaji berkembang. Pemahaman ini dapat membantu merancang kebijakan yang lebih adil, baik untuk pekerja maupun ekonomi daerah.

**Kenapa masalah ketimpangan gaji ini perlu diatasi?**

Ada dua alasan utama yang cukup mendesak:

1. **Perencanaan Ekonomi yang Lebih Baik**  
  Prediksi gaji membantu pemerintah dan perusahaan merancang kebijakan, seperti upah minimum realistis atau program penanggulangan kemiskinan yang terfokus pada daerah membutuhkan. Dengan data tren gaji, pemerintah bisa lebih siap menghadapi fluktuasi ekonomi dan perubahan sektor tenaga kerja.

2. **Pengelolaan SDM**  
  Perusahaan dapat menggunakan prediksi gaji untuk merancang struktur upah yang adil dan mengikuti perkembangan ekonomi. Sementara itu, pekerja bisa memanfaatkan informasi ini untuk memilih lokasi kerja atau merencanakan karir yang lebih menguntungkan.

**Bagaimana Masalah Ini Akan Diselesaikan**

Proyek ini bertujuan memprediksi gaji UMP provinsi di Indonesia menggunakan data historis 1997–2024 dengan pendekatan time series forecasting.

Model ARIMA dipilih karena efektif menangani data berbasis waktu dengan tren musiman. Proses pengerjaannya:
1. Data gaji historis akan dibersihkan dan dianalisis untuk menemukan pola.
2. Dibangun model ARIMA untuk memprediksi gaji di masa depan.

**Referensi**:  
- [The effect of minimum wages on employment in emerging economies: a survey and meta-analysis](https://www.tandfonline.com/doi/abs/10.1080/13600818.2017.1279134)  
- [Time Series Salaries Prediction](https://ieeexplore.ieee.org/abstract/document/10721542)


## Business Understanding
Ketimpangan gaji antar wilayah di Indonesia masih menjadi masalah besar yang memengaruhi kehidupan masyarakat, terutama individu atau pekerja. Beberapa permasalahan utama yang sering muncul meliputi kurangnya informasi standar gaji, sulitnya negosiasi gaji, dan kebingungan dalam memilih lokasi kerja dengan peluang terbaik. 

Dengan menyelesaikan masalah ini, diharapkan pekerja dapat membuat keputusan yang lebih baik terkait karir mereka, termasuk pemilihan lokasi kerja atau perencanaan negosiasi gaji.

### Problem Statement

1. **Kurangnya Informasi Standar Gaji**  
   Pekerja sering kali tidak memiliki data yang cukup untuk mengetahui apakah gaji mereka sudah sesuai dengan standar di wilayah atau sektor tertentu.

2. **Sulitnya Negosiasi Gaji**  
   Minimnya transparansi tentang standar gaji membuat pekerja kesulitan dalam melakukan negosiasi yang adil dengan perusahaan.

3. **Kebingungan Memilih Lokasi Kerja**  
   Banyak pekerja tidak memiliki panduan yang jelas untuk menentukan lokasi kerja yang memberikan peluang ekonomi terbaik, terutama jika mempertimbangkan biaya hidup dan standar gaji antar wilayah.

### Goals

Proyek ini bertujuan untuk membangun model prediksi gaji berbasis data menggunakan teknik time series forecasting. Dengan model ini, diharapkan dapat memberikan panduan kepada individu atau pekerja dalam:

- Mengetahui standar gaji sesuai lokasi.
- Memudahkan perencanaan negosiasi gaji yang lebih adil.
- Membandingkan standar gaji antar wilayah untuk membantu dalam pengambilan keputusan karir yang lebih baik.


### Solution Statement

Untuk mencapai tujuan di atas, proyek ini akan menggunakan pendekatan berbasis data dan model prediktif dengan langkah-langkah berikut:

1. **Pengumpulan dan Pembersihan Data**  
   - Mengumpulkan data gaji UMP dari berbagai provinsi di Indonesia dari tahun 1997 hingga 2024.
   - Melakukan pembersihan data untuk memastikan kelengkapan dan keakuratan.

2. **Analisis dan Identifikasi Pola**  
   - Menganalisis data untuk mengidentifikasi pola dan tren gaji dari waktu ke waktu, serta perbedaan antar wilayah.

3. **Modeling dengan ARIMA**  
   - Menggunakan model ARIMA (AutoRegressive Integrated Moving Average) untuk meramalkan perkembangan gaji di masa depan berdasarkan data historis.

4. **Evaluasi dan Validasi Model**  
   - Mengevaluasi akurasi prediksi model menggunakan metrik seperti Mean Squared Error (MSE) dan Mean Absolute Error (MAE).
   - Membandingkan hasil prediksi dengan data aktual untuk memastikan keandalan model.


## Data Understanding

Pada proyek ini, digunakan dataset mengenai Upah Minimum Provinsi (UMP) di Indonesia yang mencakup data dari tahun 1997 hingga 2024.

1. Dataset ini berisi informasi UMP yang terpisah berdasarkan provinsi dan tahun, mencakup periode 1997 hingga 2022. Dataset dapat diakses melalui Kaggle pada tautan berikut: [Dataset Upah di Indonesia](https://www.kaggle.com/datasets/linkgish/indonesian-salary-by-region-19972022).
2. Untuk melengkapi dataset hingga tahun 2024, data UMP tahun 2023 dan 2024 ditambahkan secara manual. Penambahan ini menggunakan sumber resmi dari **Badan Pusat Statistik (BPS)** untuk memastikan data yang digunakan tetap relevan dan akurat. [Sumber Data Resmi BPS](https://www.bps.go.id/).

### Variabel-variabel pada dataset ini adalah sebagai berikut:

- **REGION**: Merupakan nama provinsi atau wilayah di Indonesia, yang mencakup daerah-daerah dari seluruh Indonesia, baik dari Jawa, Sumatera, Kalimantan, Sulawesi, hingga wilayah Indonesia Timur.
- **YEAR**: Menunjukkan tahun data gaji diambil, mulai dari 1997 hingga 2024.
- **SALARY**: Menyajikan angka upah minimum provinsi (UMP) yang diterapkan pada wilayah tersebut setiap tahunnya.

### Kondisi Data

- **Jumlah data (baris dan kolom):**  
  `(870, 3)`  
  Dataset terdiri dari 870 baris dan 3 kolom.

- **Jumlah nilai yang hilang (missing values) per kolom:**
Tidak terdapat *missing values* pada dataset.

- **Jumlah baris duplikat:**  
Tidak terdapat baris duplikat pada dataset.

### Uraian Fitur

Berikut adalah deskripsi dari setiap fitur pada dataset:

1. **Feature: REGION**  
 - **Tipe Data:** object  
 - **Contoh Nilai:**  
   `'Aceh'`, `'Bali'`, `'Banten'`, `'Bengkulu'`, `'Di Yogyakarta'`

2. **Feature: SALARY**  
 - **Tipe Data:** int64  
 - **Statistik Deskriptif:**  
   ```
   count      870.0  
   mean   1,179,872.0  
   std    9,175,435.0  
   min      106,000.0  
   25%      421,500.5  
   50%      890,387.0  
   75%    1,867,583.0  
   max    4,452,724.0  
   ```

3. **Feature: YEAR**  
 - **Tipe Data:** object  
 - **Contoh Nilai:**  
   `1997`, `1998`, `1999`, `2000`, `2001`

### Exploratory Data Analysis (EDA)

Tahapan eksplorasi data dilakukan untuk memahami karakteristik dataset dan menemukan pola yang relevan. Beberapa analisis dan visualisasi yang akan dilakukan meliputi:

1. **Rata-rata Gaji Per Wilayah**
   - Menghitung rata-rata gaji di setiap provinsi untuk mendapatkan gambaran tentang ketimpangan gaji antar wilayah.
![image](https://github.com/user-attachments/assets/c4eaaff2-70ba-446c-b7e7-896871b5ee22)

2. **Tren Tahunan**
   - Menganalisis bagaimana gaji minimum provinsi (UMP) berubah dari tahun ke tahun di tingkat nasional.
   - Menghitung tingkat pertumbuhan gaji rata-rata per tahun untuk mengidentifikasi pola kenaikan gaji.
![image](https://github.com/user-attachments/assets/8c4bf288-41aa-458d-9f7f-c7c30258d850)

3. **Top 5 Provinsi dengan Gaji Tertinggi dan Terendah**
   - Mengidentifikasi provinsi dengan UMP tertinggi dan terendah setiap tahun untuk melihat disparitas gaji yang signifikan.
![image](https://github.com/user-attachments/assets/bb860b8f-6e04-4775-9336-88639c11b4f5)
![image](https://github.com/user-attachments/assets/5265aaf1-9448-4a15-918b-ba1e2f9e2c85)

4. **Distribusi Gaji Per Wilayah dari Tahun ke Tahun**
   - Melihat bagaimana distribusi gaji berubah antar tahun untuk mempelajari pergeseran disparitas.
   ![image](https://github.com/user-attachments/assets/e471eae2-f0a1-4921-af9a-26c066006d52)
*yang ditampilkan tahun 2024

5. **Perbandingan Rata-rata Gaji Antar Pulau (2017-2024)**
   - Mengelompokkan provinsi berdasarkan pulau (misalnya, Jawa, Sumatera, Kalimantan, dll.) dan menghitung rata-rata UMP per pulau.
   ![image](https://github.com/user-attachments/assets/01843102-2f06-4ab4-b860-05a5a3df5387)

# Data Preparation
Pada tahap ini, beberapa langkah dilakukan untuk memastikan data siap digunakan dalam pemodelan. Langkah-langkah yang dilakukan adalah:  
### 1. Penanganan Missing Values
Dataset tidak memiliki **missing values** pada kolom `REGION`, `SALARY`, `YEAR` maupun `ISLAND`.  

### 2. Case Formatting pada Kolom `REGION`
Semua nilai pada kolom `REGION` diformat ke **huruf kapital** untuk menjaga konsistensi dan menghindari duplikasi data akibat perbedaan penulisan (contoh: `Aceh` dan `ACEH` dianggap berbeda tanpa formatting).

### 3. Penghapusan Data `REGION` yang Tidak Relevan
Baris dengan nilai `REGION` berupa `'Indonesia'` dihapus karena data ini tidak memberikan informasi spesifik terkait wilayah tertentu. Fokus analisis hanya pada level provinsi.

### 4. Penambahan Data untuk Tahun 2023 dan 2024
Dataset awal hanya mencakup data hingga tahun 2022. Untuk melengkapi dataset hingga tahun 2024, data UMP tahun 2023 dan 2024 ditambahkan secara manual.  
Sumber data berasal dari **Badan Pusat Statistik (BPS)** untuk memastikan akurasi dan relevansi.

### 5. Penambahan Kolom `ISLAND`
Kolom `ISLAND` ditambahkan untuk mengelompokkan provinsi berdasarkan pulau. Kelompok ini membantu dalam analisis distribusi UMP berdasarkan wilayah geografis.  
Contoh pengelompokannya adalah sebagai berikut:
- **Sumatera:** Aceh, Sumatera Utara, Riau, dan lain-lain.
- **Jawa:** DKI Jakarta, Jawa Barat, Jawa Timur, dan lainnya.
- **Kalimantan:** Kalimantan Barat, Kalimantan Timur, dll.

### 6. Perubahan Tipe Data Kolom `YEAR`
Kolom `YEAR` awalnya memiliki tipe data string (object). Tipe data ini diubah menjadi **datetime** agar dapat digunakan untuk analisis berbasis waktu dan pemodelan time series.


### Output Data Setelah Proses
Dataset setelah proses ini memiliki struktur berikut:
- **Baris dan Kolom:** `(920, 4)`  
- **Nama Kolom:** `REGION`, `SALARY`, `YEAR`, `ISLAND`  
- **Jumlah Missing Values:**  0
---

# Modeling

Pada tahap modeling, proyek ini menggunakan algoritma **ARIMA (AutoRegressive Integrated Moving Average)** untuk memprediksi tren gaji historis dan memberikan estimasi gaji di masa depan. Berikut adalah penjelasan detail proses yang dilakukan:

### Proses Modeling

1. **Membuat Model ARIMA untuk Jakarta dan Jogjakarta**
   - Untuk memvalidasi performa awal, model ARIMA pertama kali diterapkan pada data dari dua wilayah: Jakarta dan Jogjakarta.
   - Tahapan meliputi:
     - **Preprocessing Data**: Kolom tahun (`YEAR`) diubah menjadi format waktu (`datetime`) agar sesuai dengan kebutuhan ARIMA.
     - **Parameter Model**: ARIMA menggunakan parameter `(p, d, q)` di mana:
       - `p`: jumlah lag dalam model autoregresif.
       - `d`: jumlah differencing untuk membuat data stasioner.
       - `q`: jumlah lag error dalam moving average.
       - Parameter awal dipilih `(2, 1, 2)` berdasarkan eksperimen awal.
     - **Fitting Model**: Model di-fit pada data historis gaji masing-masing wilayah.
     - **Evaluasi Awal**: Model diuji dengan menghitung *Mean Absolute Error (MAE)* dan *Mean Squared Error (MSE)* untuk menilai seberapa baik model memprediksi data historis.

2. **Looping Model ARIMA ke Seluruh Wilayah**
   - Setelah validasi awal berhasil, model ARIMA diimplementasikan secara iteratif untuk setiap wilayah di dataset. Proses ini memastikan model dapat menangkap pola spesifik di setiap wilayah.

3. **Prediksi Gaji 10 Tahun ke Depan**
   - Model digunakan untuk memprediksi tren gaji hingga 10 tahun ke depan di setiap wilayah. Prediksi ini bertujuan untuk memberikan insight tentang kemungkinan ketimpangan gaji yang akan datang.

### Visualisasi Hasil Prediksi
- **Prediksi vs Data Aktual**
  - Dibuat visualisasi perbandingan antara data aktual dan prediksi untuk melihat seberapa baik model ARIMA menangkap pola historis.
  - Grafik menunjukkan tren gaji dari tahun ke tahun, dengan garis prediksi ditampilkan sebagai garis putus-putus.

- **Prediksi 10 Tahun ke Depan**
  - Prediksi untuk tahun mendatang divisualisasikan sebagai ekstensi tren data historis. Hal ini memberikan gambaran bagaimana gaji di setiap wilayah akan berkembang di masa depan.

### Evaluasi Model
- **Metode Evaluasi**: 
  - *Mean Absolute Error (MAE)*: Mengukur rata-rata kesalahan prediksi secara absolut.
  - *Mean Squared Error (MSE)*: Mengukur rata-rata kuadrat kesalahan prediksi untuk menilai model.
- Hasil evaluasi menunjukkan bahwa model dapat menangkap pola data historis dengan tingkat kesalahan yang dapat diterima.

### Contoh Implementasi ARIMA pada Jakarta
```python
from statsmodels.tsa.arima.model import ARIMA
from sklearn.metrics import mean_absolute_error, mean_squared_error
import matplotlib.pyplot as plt
import pandas as pd

# Preprocessing: Rename columns and ensure datetime format
df_jakarta = df_jakarta.rename(columns={'YEAR': 'ds', 'SALARY': 'y'})
df_jakarta['ds'] = pd.to_datetime(df_jakarta['ds'], format='%Y')

# Fit the ARIMA model
model = ARIMA(df_jakarta['y'], order=(2,1,2))  # Adjust parameters as needed
model_fit = model.fit()

# Predictions and evaluation
predictions = model_fit.predict(start=0, end=len(df_jakarta)-1)
mae = mean_absolute_error(df_jakarta['y'], predictions)
mse = mean_squared_error(df_jakarta['y'], predictions)

# Print metrics
print(f"Mean Absolute Error (MAE): {mae}")
print(f"Mean Squared Error (MSE): {mse}")

# Visualization
plt.figure(figsize=(12, 6))
plt.plot(df_jakarta['ds'], df_jakarta['y'], label='Actual')
plt.plot(df_jakarta['ds'], predictions, label='Predicted', linestyle='--')
plt.title('ARIMA Predictions vs Actual Salary in Jakarta')
plt.xlabel('Year')
plt.ylabel('Salary')
plt.legend()
plt.grid(True)
plt.show()


---
```
# Evaluation
## Metrik yang Digunakan  
1. **Mean Absolute Error (MAE)**  
   Mengukur rata-rata kesalahan absolut antara nilai aktual dan prediksi. MAE memberikan gambaran rata-rata kesalahan dalam satuan yang sama dengan data (*salary*).  

2. **Mean Squared Error (MSE)**  
   Mengukur rata-rata kesalahan kuadrat antara nilai aktual dan prediksi. MSE lebih sensitif terhadap kesalahan besar karena menekankan kuadrat dari selisih.  

## Hasil Evaluasi untuk Jakarta  
- **MAE:** 86,525.06  
- **MSE:** 18,992,191,220.62  

Nilai MAE menunjukkan rata-rata kesalahan prediksi sebesar Rp 86,525, sedangkan MSE menyoroti bahwa ada beberapa prediksi dengan kesalahan besar, yang meningkatkan nilai kesalahan kuadrat.  

## Hasil Evaluasi untuk Jogjakarta  
- **MAE:** 40,306.83  
- **MSE:** 4,736,783,035.49  
Hasil evaluasi ini memberikan gambaran yang cukup jelas bahwa meskipun model ini memberikan insight awal tentang standar gaji di Jakarta dan Jogjakarta, masih ada ruang yang luas untuk perbaikan. Model ini memang memberikan gambaran mengenai standar gaji di dua wilayah tersebut, yang tentu bisa menjadi dasar yang baik bagi pekerja untuk mengetahui apakah gaji mereka sudah sesuai dengan standar. Selain itu, model ini juga memberikan perbandingan antara semua wilayah di Indonesia, sehingga pekerja bisa lebih mudah memilih lokasi kerja berdasarkan potensi gaji yang lebih menguntungkan.

Namun, meskipun model ini memberikan manfaat, kesalahan dalam prediksi  menunjukkan bahwa model ini belum sepenuhnyaakurat. Akurasi prediksi yang lebih tinggi akan sangat membantu pekerja untuk membuat keputusan lebih cerdas dalam memilih lokasi kerja atau merencanakan negosiasi gaji. Saat ini, meskipun bermanfaat, model ini hanya bisa menjadi panduan awal yang membantu pekerja untuk memahami standar gaji antar wilayah, namun tidak bisa dijadikan satu-satunya acuan.

---

# Kesimpulan  
Model ARIMA cukup efektif dalam menangkap pola gaji berdasarkan data historis, dengan hasil prediksi untuk Jogjakarta yang lebih baik dibandingkan Jakarta. Metrik evaluasi menunjukkan bahwa meskipun terdapat kesalahan prediksi, model ini masih dapat digunakan untuk perencanaan gaji 10 tahun ke depan, terutama dengan data historis yang lebih lengkap dan relevan.

