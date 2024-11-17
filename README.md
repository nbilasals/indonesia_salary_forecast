# Prediksi Gaji UMR di Indonesia:

## Domain Proyek

Di Indonesia, ketimpangan upah antar wilayah masih jadi salah satu isu besar yang sering terlupakan, meskipun dampaknya sangat terasa, baik bagi ekonomi daerah maupun individu yang bekerja di berbagai sektor. Misalnya, Jakarta yang dikenal sebagai pusat perekonomian punya standar gaji yang jauh lebih tinggi dibandingkan dengan kota-kota di luar Pulau Jawa atau Indonesia Timur. Hal ini menimbulkan gap yang cukup besar dalam kesempatan ekonomi, mobilitas tenaga kerja, dan kualitas hidup antar wilayah.

Masalah ketimpangan ini tidak hanya mempengaruhi gaji pekerja, tapi juga berimbas ke distribusi pendapatan yang tidak merata, dan tentu saja kualitas hidup masyarakat di daerah yang lebih terpencil. Oleh karena itu, sangat penting untuk bisa memprediksi dan memahami bagaimana gaji bisa berkembang seiring waktu, khususnya di kota-kota besar seperti Jakarta. Dengan pemahaman ini, kita bisa membantu merancang kebijakan yang lebih adil, tidak hanya untuk pekerja, tapi juga untuk perekonomian daerah secara keseluruhan.

**Kenapa masalah ketimpangan gaji ini perlu diatasi?**

Ada dua alasan utama yang cukup mendesak:

1. **Perencanaan Ekonomi yang Lebih Baik**  
   Mengetahui bagaimana tren gaji berkembang bisa membantu pemerintah dan perusahaan dalam merancang kebijakan yang lebih efektif dan berkelanjutan. Misalnya, kebijakan upah minimum yang lebih realistis atau program pengentasan kemiskinan yang bisa menargetkan daerah-daerah yang benar-benar membutuhkan. Kalau kita bisa memprediksi gaji di masa depan, pemerintah bisa lebih siap menghadapi fluktuasi ekonomi atau perubahan dalam sektor tenaga kerja.

2. **Pengelolaan SDM**  
   Di sisi perusahaan, forecasting gaji ini akan sangat membantu dalam hal pengelolaan sumber daya manusia. Pengusaha bisa merencanakan struktur gaji yang lebih adil dan sesuai dengan perkembangan ekonomi, serta meningkatkan kesejahteraan karyawan. Sementara bagi pekerja, peramalan gaji ini juga bisa jadi acuan dalam merencanakan karir mereka—mungkin untuk memilih lokasi kerja yang menawarkan peluang gaji yang lebih baik, atau sekadar untuk tahu apakah pekerjaan mereka masih relevan dengan standar gaji yang ada di pasaran.

**Bagaimana Masalah Ini Akan Diselesaikan**

Proyek ini bertujuan untuk membantu memahami dan memprediksi gaji UMP di provinsi-provinsi di Indonesia dengan menggunakan data historis gaji dari tahun 1997 hingga 2024. Menggunakan time series forecasting, sebuah metode statistik yang biasa dipakai untuk memprediksi nilai-nilai di masa depan berdasarkan data yang sudah ada.

Untuk modelnya, digunakan ARIMA (AutoRegressive Integrated Moving Average), karena model ini sudah terbukti efektif dalam menangani data yang bersifat waktu, seperti prediksi gaji yang bisa dipengaruhi oleh berbagai faktor musiman atau tren tahunan. Pertama-tama, data gaji yang ada akan dibersihkan dan dianalisis lebih dulu untuk melihat pola yang ada. Setelah itu, kita akan membangun model ARIMA untuk meramalkan gaji di masa depan, dan mencoba menganalisis apakah ada pola yang bisa digunakan untuk perbaikan kebijakan atau keputusan lainnya.

**Referensi**:  
- [The effect of minimum wages on employment in emerging economies: a survey and meta-analysis](https://www.tandfonline.com/doi/abs/10.1080/13600818.2017.1279134)  
- [Time Series Salaries Prediction](https://ieeexplore.ieee.org/abstract/document/10721542)


## Business Understanding

**Ketimpangan Gaji Antar Wilayah di Indonesia**  
Ketimpangan gaji antara wilayah di Indonesia merupakan masalah yang penting, yang berdampak langsung pada perekonomian dan kualitas hidup masyarakat. Gaji yang lebih tinggi di kota-kota besar, seperti Jakarta, dibandingkan dengan daerah lain, menciptakan ketidakseimbangan kesempatan ekonomi bagi pekerja yang tinggal di daerah terpencil atau di luar Pulau Jawa. Hal ini menyebabkan kesenjangan sosial dan ekonomis yang berlarut-larut. Oleh karena itu, sangat penting untuk memiliki model yang dapat memprediksi tren perkembangan gaji di berbagai wilayah, untuk membantu merancang kebijakan yang lebih adil dan memadai.

**Pengelolaan Sumber Daya Manusia yang Tidak Optimal**  
Perusahaan-perusahaan di Indonesia sering kali kesulitan dalam merencanakan struktur gaji yang sesuai dengan perkembangan ekonomi yang ada, terutama dalam pengelolaan sumber daya manusia (SDM). Tanpa pemahaman yang jelas tentang bagaimana gaji akan berkembang di masa depan, perusahaan mungkin tidak dapat menetapkan upah yang adil dan kompetitif, yang pada akhirnya dapat memengaruhi retensi karyawan dan kesejahteraan mereka. Forecasting gaji yang akurat akan sangat membantu dalam merencanakan kebijakan SDM yang lebih efektif dan adil, baik untuk perusahaan maupun karyawan.

**Perencanaan Ekonomi dan Kebijakan yang Kurang Tepat Sasaran**  
Bagi pemerintah, ketimpangan gaji antar wilayah bisa menjadi penghalang dalam merancang kebijakan ekonomi yang berkelanjutan. Tanpa adanya prediksi yang akurat mengenai perkembangan gaji di masa depan, pemerintah akan kesulitan dalam menentukan kebijakan upah minimum yang realistis atau dalam merancang program pengentasan kemiskinan yang sesuai dengan kebutuhan tiap daerah. Oleh karena itu, sangat penting untuk memiliki alat yang dapat memprediksi gaji di berbagai provinsi agar kebijakan yang dibuat bisa lebih tepat sasaran dan efektif dalam mengurangi kesenjangan sosial-ekonomi antar wilayah.

**Keterbatasan Data Gaji yang Tersedia untuk Analisis**  
Walaupun data historis mengenai gaji telah tersedia, namun data tersebut tidak selalu lengkap atau mudah diakses untuk tujuan analisis yang mendalam. Beberapa daerah mungkin tidak memiliki data yang cukup untuk analisis tren gaji secara tepat. Oleh karena itu, penting untuk menggunakan teknik analisis data dan time series forecasting yang efektif, untuk memanfaatkan data yang terbatas menjadi informasi yang bermanfaat dalam merencanakan kebijakan yang lebih baik.


### Goals

1. Setiap pernyataan masalah yang telah diidentifikasi di atas memiliki tujuan yang jelas untuk memecahkan masalah ketimpangan gaji antar wilayah di Indonesia dan memberikan solusi yang lebih efektif dalam perencanaan kebijakan dan pengelolaan sumber daya manusia. Berikut adalah tujuan untuk masing-masing pernyataan masalah:

2. Mengurangi ketimpangan gaji antar wilayah di Indonesia dengan menyediakan pemahaman yang lebih baik mengenai prediksi perkembangan gaji di tiap provinsi. Tujuan ini dapat dicapai dengan menggunakan analisis time series untuk meramalkan tren gaji di masa depan, memberikan data yang akurat bagi pemerintah dan pengambil kebijakan dalam merancang kebijakan yang lebih adil dan efektif. Dengan memprediksi gaji yang realistis, kita dapat membantu menciptakan kesempatan ekonomi yang lebih merata antara wilayah, serta mengurangi kesenjangan sosial yang ada.

3. Membantu perusahaan dalam merencanakan kebijakan upah dan pengelolaan sumber daya manusia yang lebih efisien dan adil. Tujuannya adalah untuk memberikan alat yang memungkinkan perusahaan untuk memperkirakan perkembangan gaji di masa depan, sehingga mereka dapat merancang struktur gaji yang kompetitif dan adil sesuai dengan perkembangan ekonomi. Dengan mengetahui tren gaji yang ada, perusahaan bisa lebih siap untuk mempertahankan karyawan dengan memberikan kesejahteraan yang lebih baik, serta mengurangi tingkat turnover karyawan.
 
4. Mendukung perencanaan ekonomi yang lebih baik dengan memberikan data yang akurat mengenai prediksi perkembangan gaji antar wilayah. Dengan memanfaatkan hasil prediksi gaji, pemerintah dapat merancang kebijakan ekonomi dan program sosial yang lebih efektif, seperti penetapan upah minimum yang tepat dan program pengentasan kemiskinan yang lebih menyeluruh. Tujuan akhirnya adalah untuk menciptakan pemerataan ekonomi di seluruh Indonesia, serta meningkatkan kualitas hidup masyarakat di daerah-daerah dengan gaji yang lebih rendah.

5. Memperbaiki akses terhadap data gaji yang lebih terstruktur dan lengkap. Dengan menggunakan teknik analisis data dan time series forecasting yang canggih, kita dapat mengoptimalkan data historis yang terbatas untuk membuat peramalan gaji yang lebih akurat. Hal ini memungkinkan pembuatan kebijakan yang lebih baik, berdasarkan data yang lebih representatif dan lengkap, sehingga kebijakan yang dihasilkan lebih tepat sasaran dan dapat diterapkan di berbagai daerah di Indonesia.

---

### Solution Statement

Untuk meraih tujuan-tujuan yang telah dijelaskan di atas, proyek ini akan menggunakan teknik **time series forecasting**, dengan model **ARIMA (AutoRegressive Integrated Moving Average)**.

Langkah-langkah solusi yang dilakukan:

1. **Pengumpulan dan Pembersihan Data**  
   Mengumpulkan data gaji UMP dari berbagai provinsi di Indonesia dari tahun 1997 hingga 2024, kemudian membersihkan data tersebut agar siap digunakan untuk analisis. Proses pembersihan ini termasuk menghilangkan data yang tidak lengkap atau tidak valid.

2. **Analisis dan Identifikasi Pola**  
   Setelah data dibersihkan, kita akan melakukan analisis untuk mengidentifikasi pola dan tren yang ada dalam data gaji, termasuk fluktuasi tahunan atau musiman yang bisa mempengaruhi prediksi.

3. **Modeling dengan ARIMA**  
   Membangun model ARIMA untuk meramalkan perkembangan gaji di masa depan. Model ini akan disesuaikan dengan data yang ada untuk menghasilkan prediksi yang akurat dan dapat diandalkan.

4. **Evaluasi dan Validasi Model**  
   Setelah model dibangun, langkah berikutnya adalah mengevaluasi dan memvalidasi akurasi prediksi yang dihasilkan oleh model ARIMA dengan menggunakan data yang ada, serta membandingkannya dengan data nyata untuk mengukur tingkat keakuratan model dengan Mean Squared Error dan Mean Absolute Error.

## Data Understanding

Pada proyek ini, kami menggunakan dataset mengenai upah minimum provinsi (UMP) di Indonesia dari tahun 1997 hingga 2024. Dataset ini dapat diunduh melalui Kaggle pada tautan berikut [Dataset Upah di Indonesia](https://www.kaggle.com/datasets/linkgish/indonesian-salary-by-region-19972022).

Dataset ini mencakup data upah minimum provinsi (UMP) yang terpisah berdasarkan wilayah dan tahun. Data yang digunakan pada tahun 2023 dan 2024 ditambahkan secara manual dengan menggunakan data dari Badan Pusat Statistik (BPS), untuk memastikan kelengkapan informasi hingga tahun terbaru.

### Variabel-variabel pada dataset ini adalah sebagai berikut:

- **REGION**: Merupakan nama provinsi atau wilayah di Indonesia, yang mencakup daerah-daerah dari seluruh Indonesia, baik dari Jawa, Sumatera, Kalimantan, Sulawesi, hingga wilayah Indonesia Timur.
- **YEAR**: Menunjukkan tahun data gaji diambil, mulai dari 1997 hingga 2024.
- **SALARY**: Menyajikan angka upah minimum provinsi (UMP) yang diterapkan pada wilayah tersebut setiap tahunnya.

Data ini mengandung informasi yang sangat penting dalam memahami tren gaji dari waktu ke waktu di berbagai wilayah di Indonesia, serta ketimpangan gaji yang mungkin terjadi antar daerah.

### Teknik yang Digunakan untuk Memahami Data

Untuk memahami lebih dalam tentang data ini, kami melakukan beberapa tahapan analisis eksplorasi data (EDA), yang meliputi:
1. **Visualisasi Tren Upah**: Melihat bagaimana perkembangan upah minimum antar provinsi dari tahun ke tahun.
2. **Analisis Distribusi Gaji**: Memeriksa sebaran gaji antar provinsi untuk mengetahui daerah mana yang memiliki upah tertinggi atau terendah.
3. **Perbandingan Antar Wilayah**: Menganalisis ketimpangan upah antar wilayah, baik berdasarkan rata-rata maupun distribusi gaji untuk melihat kesenjangan yang ada.


# Data Preparation
Pada tahap ini, beberapa langkah dilakukan untuk memastikan data siap digunakan dalam pemodelan. Langkah-langkah yang dilakukan adalah:  

1. **Case Formatting untuk Kolom REGION**  
   Semua nilai dalam kolom `REGION` diformat ke huruf kapital untuk menjaga konsistensi data.  

2. **Penambahan Data untuk Tahun 2023 dan 2024**  
   Data untuk tahun 2023 dan 2024 ditambahkan secara manual berdasarkan data yang diambil dari BPS (Badan Pusat Statistik).  

3. **Menghapus Data REGION 'Indonesia' yang Tidak Relevan**  
   Data dengan region `Indonesia` dihapus karena tidak memberikan informasi spesifik terkait wilayah tertentu. Fokus hanya pada data level provinsi.  

4. **Penambahan Kolom ISLAND**  
   Kolom `ISLAND` ditambahkan untuk mengelompokkan wilayah berdasarkan pulau (misalnya Jawa, Sumatera, Kalimantan, dll.). Ini membantu dalam analisis lebih lanjut terkait distribusi gaji berdasarkan pulau.  

5. **Konversi Tanggal**  
   Kolom `YEAR` dikonversi menjadi format datetime untuk mempermudah analisis time series.  

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

