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
Ketimpangan gaji antar wilayah di Indonesia masih menjadi masalah besar yang memengaruhi kehidupan masyarakat, terutama individu atau pekerja. Beberapa permasalahan yang sering muncul antara lain:  
- **Kurangnya Informasi Standar Gaji**: Pekerja sering kali tidak memiliki data yang cukup untuk mengetahui apakah gaji mereka sudah sesuai dengan standar di wilayah atau sektor tertentu.  
- **Sulitnya Negosiasi Gaji**: Minimnya transparansi tentang standar gaji membuat pekerja kesulitan dalam melakukan negosiasi yang adil dengan perusahaan.  
- **Kebingungan Memilih Lokasi Kerja**: Banyak pekerja tidak memiliki panduan yang jelas untuk menentukan lokasi kerja yang memberikan peluang ekonomi terbaik, terutama jika mempertimbangkan biaya hidup dan standar gaji antar wilayah.

---

### **Goals**
Proyek ini bertujuan untuk membangun model prediksi gaji berbasis data menggunakan teknik **time series forecasting**. Dengan model ini, diharapkan bisa memberikan insight yang mendukung pengambilan keputusan bagi individu/pekerja untuk:
   - Memberikan panduan untuk mengetahui standar gaji sesuai lokasi.
   - Membantu pekerja membandingkan standar gaji antar wilayah, sehingga mereka dapat mengambil keputusan karir yang lebih baik, seperti memilih lokasi kerja yang menawarkan peluang terbaik atau merencanakan negosiasi gaji yang lebih adil.


---

### Solution Statement

Untuk meraih tujuan-tujuan yang telah dijelaskan di atas, proyek ini akan menggunakan teknik **time series forecasting**, dengan model **ARIMA (AutoRegressive Integrated Moving Average)**.

Langkah-langkah solusi yang dilakukan:

1. **Pengumpulan dan Pembersihan Data**  
   Mengumpulkan data gaji UMP dari berbagai provinsi di Indonesia dari tahun 1997 hingga 2024. 
2. **Analisis dan Identifikasi Pola**  
   Setelah data dibersihkan, kita akan melakukan analisis untuk mengidentifikasi pola dan tren yang ada dalam data gaji.
3. **Modeling dengan ARIMA**  
   Membangun model ARIMA untuk meramalkan perkembangan gaji di masa depan.

4. **Evaluasi dan Validasi Model**  
   Setelah model dibangun, langkah berikutnya adalah mengevaluasi dan memvalidasi akurasi prediksi yang dihasilkan oleh model ARIMA dengan menggunakan data yang ada, serta membandingkannya dengan data aktual untuk mengukur tingkat keakuratan model dengan Mean Squared Error dan Mean Absolute Error.

## Data Understanding

Pada proyek ini, digunakan dataset mengenai Upah Minimum Provinsi (UMP) di Indonesia yang mencakup data dari tahun 1997 hingga 2024.

1. Dataset ini berisi informasi UMP yang terpisah berdasarkan provinsi dan tahun, mencakup periode 1997 hingga 2022. Dataset dapat diakses melalui Kaggle pada tautan berikut: [Dataset Upah di Indonesia](https://www.kaggle.com/datasets/linkgish/indonesian-salary-by-region-19972022).
2. Untuk melengkapi dataset hingga tahun 2024, data UMP tahun 2023 dan 2024 ditambahkan secara manual. Penambahan ini menggunakan sumber resmi dari **Badan Pusat Statistik (BPS)** untuk memastikan data yang digunakan tetap relevan dan akurat.


### Variabel-variabel pada dataset ini adalah sebagai berikut:

- **REGION**: Merupakan nama provinsi atau wilayah di Indonesia, yang mencakup daerah-daerah dari seluruh Indonesia, baik dari Jawa, Sumatera, Kalimantan, Sulawesi, hingga wilayah Indonesia Timur.
- **YEAR**: Menunjukkan tahun data gaji diambil, mulai dari 1997 hingga 2024.
- **SALARY**: Menyajikan angka upah minimum provinsi (UMP) yang diterapkan pada wilayah tersebut setiap tahunnya.

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

1. **Case Formatting untuk Kolom REGION**  
   Semua nilai dalam kolom `REGION` diformat ke huruf kapital untuk menjaga konsistensi data.
2.  **Menghapus Data REGION 'Indonesia' yang Tidak Relevan**  
   Data dengan region `Indonesia` dihapus karena tidak memberikan informasi spesifik terkait wilayah tertentu. Fokus hanya pada data level provinsi.  
3. **Penambahan Data untuk Tahun 2023 dan 2024**  
   Data untuk tahun 2023 dan 2024 ditambahkan secara manual berdasarkan data yang diambil dari BPS (Badan Pusat Statistik).   
4. **Penambahan Kolom ISLAND**  
   Kolom `ISLAND` ditambahkan untuk mengelompokkan wilayah berdasarkan pulau (misalnya Jawa, Sumatera, Kalimantan, dll.). Ini membantu dalam analisis lebih lanjut terkait distribusi gaji berdasarkan pulau.  


---

# Modeling
## Pendekatan Modeling  
1. **Membuat Model ARIMA untuk Jakarta dan Jogjakarta Secara Individual**  
   Model ARIMA pertama kali diuji pada dua region, yaitu Jakarta dan Jogjakarta. Setelah itu, model ARIMA di-*loop* untuk setiap wilayah di dataset.  

2. **Visualisasi Hasil Prediksi**  
   Dibuat visualisasi perbandingan antara data aktual dan prediksi untuk melihat seberapa baik model menangkap pola gaji historis. Selain itu, dilakukan prediksi gaji untuk 10 tahun ke depan menggunakan model ini.  

---

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

---

# Kesimpulan  
Model ARIMA cukup efektif dalam menangkap pola gaji berdasarkan data historis, dengan hasil prediksi untuk Jogjakarta yang lebih baik dibandingkan Jakarta. Metrik evaluasi menunjukkan bahwa meskipun terdapat kesalahan prediksi, model ini masih dapat digunakan untuk perencanaan gaji 10 tahun ke depan, terutama dengan data historis yang lebih lengkap dan relevan.

