
# Laporan Proyek Machine Learning - M. Taufiq Hidayat Pohan

## Domain Proyek

<p  style='text-align: justify;'>

Dalam beberapa tahun terakhir ini, pencemaran udara menjadi isu yang vital bagi pemerintah daerah dan pusat ​(Plaia et al., 2013)​. Pencemaran udara di perkotaan sudah tidak dapat dihindarkan, sebagai akibat dari berbagai aktivitas masyarakat, seperti transportasi, industri, dan aktivitas konstruksi ​(Turyanti et al., 2022)​. Pencemaran udara adalah terkontaminasinya atmosfer dengan unsur-unsur berbahaya yang mengakibatkan kerusakan lingkungan sehingga menurunkan kualitas lingkungan dan dapat menyebabkan gangguan pada kesehatan manusia ​(Gindo Simanjuntak, 2007)​. Beberapa unsur-unsur berbahaya yang berdampak buruk bagi manusia ialah Karbon Monoksida (CO), Sulfur Dioksida (SO<sub>2</sub>), Nitrogen Dioksida (NO<sub>2</sub>), Ozon (O<sub>3</sub>) dan sebagainya ​(Kumar & Goyal, 2011)​. Selain itu terdapat unsur-unsur mikro yang disebut *Particulate Matter* (PM). Partikel ini tidak hanya berbentuk padatan, namun juga berbentuk cairan yang mengendap dalam partikel debu ​(Gindo Simanjuntak, 2007)​. Ukuran partikulat yang umumnya diukur adalah PM<sub>10</sub> dan PM<sub>2.5</sub> diaman PM<sub>10</sub> adalah partikulat dengan diameter 10 mikrometer atau kurang ​(IRCEL - CELINE, n.d.)​. Sedangkan PM<sub>2.5</sub> merupakan partikulat yang berukuran kurang dari 2.5 mikrometer. Partikel ini dapat menembus bagian paling dalam paru-paru dan sistem jantung, sehingga menyebabkan infeksi saluran pernafasan akut, kanker paru-paru, penyakit kardiovaskular dan bahkan kematian ​(Santoso et al., 2016)​.

</p>

<p  style='text-align: justify;'>

Daerah Khusus Ibukota Jakarta merupakah salah satu kota yang sedang menghadapi permasalahan pencemaran udara yang disebabkan oleh peningkatan jumlah kendaraan bermotor dan juga pembangunan infrastruktur ​(Hermawan, 2019)​. Jakarta menempati urutan ke 4 sebagai kota paling berpolutan di Asia Tenggara dengan nilai PM<sub>2.5</sub> rata-rata sebesar 36.2. Meskipun termasuk tinggi, namun telah terjadi penurunan kadar PM<sub>2.5</sub> selama 3 tahun berturut dimana penurunan sebesar 11% dibandingkan tahun 2021, 7,7% dibandingkan tahun 2020 dan 27% dibandingkan tahun 2019 ​(IQAir, 2023)​. Berbagai kebijakan sudah dilaksanakan oleh Pemerintah DKI Jakarta untuk meningkatkan kualitas udara, seperti program Ganjil Genap untuk kendaraan yang masuk ke Kota Jakarta, program *Car Free Day (CDF)* atau Hari Bebas Kendaraan Bermotor (HBKB), program *Low Emission Zone*, serta program Uji Emisi kendaraan bermotor. Provinsi DKI Jakarta melalui Dinas Lingkungan Hidup Provinsi DKI Jakarta juga telah melakukan pemantauan kualitas udara secara kontinu pada 5 titik Stasiun Pemantauan Kualitas Udara Ambien (SPKUA), yang berada di lokasi Bundaran HI (DKI1), Kelapa Gading (DKI2), Jagakarsa (DKI3), Lubang Buaya (DKI4), dan Kebon Jeruk (DKI5). Selain itu terdapat juga beberapa lembaga yang mengukur kualitas udara secara resmi pada beberapa lokasi, seperti Kementerian Lingkungan Hidup dan Kehutanan (KLHK), BMKG dan juga Kedutaan Besar Amerika Serikat di Jakarta ​(Turyanti et al., 2022)​. Hasil pengukuran dari SPKUA ini menggunakan Indeks Standar Pencemaran Udara (ISPU). Berdasarkan Pasal 1 Peraturan Menteri Lingkungan Hidup dan Kehutanan Nomor P.14/MENLHK/SETJEN/KUM.1/7/2020 berbunyi Indeks Standar Pencemaran Udara adalah angka yang tidak mempunyai satuan yang menggambarkan kondisi mutu udara ambien di lokasi tertentu, yang didasarkan kepada dampak terhadap kesehatan manusia, nilai estetika dan makhluk hidup lainnya. Nilai Indeks Standar Pencemaran Udara ini sangat bermanfaat untuk mengategorikan seberapa baik atau buruknya kualitas udara bagi kesehatan masyarakat dan membantu pemerintah untuk proses pengambilan keputusan terkait tindakan mitigasi polusi dan manajemen kualitas udara suatu wilayah ​(Kumar & Goyal, 2011)​. Penerapan model prediksi kualitas udara merupakan salah satu langkah untuk memberikan data kualitas lingkungan yang efektif untuk masyarakat dan pemerintahan serta dapat menggambarkan tren pencemaran udara ​(Liu et al., 2021)​.

</p>

<p  style='text-align: justify;'>

​​Hermawan (2019)​ membuat model prediksi dengan algoritma *Support Vector Machine (SVM)* dengan *Kernel Gaussian Radial Basis Function (RBF)* untuk memprediksi kualitas udara di DKI Jakarta dengan hasil akurasi seluruh data SPKU Jakarta sebesar 96.03%, akurasi prediksi pada data Jakarta Pusat (DKI1) sebesar 93.97%, akurasi prediksi pada data Jakarta Utara (DKI2) sebesar 91.35, akurasi prediksi pada data Jakarta Selatan (DKI3) sebesar 89.47%, akurasi prediksi pada data Jakarta Timur (DKI4) sebesar 89.27%, dan akurasi prediksi pada data Jakarta Barat (DKI5) sebesar 87.29%. Studi serupa dilakukan oleh (X. Yan & Enhua, 2020) yang perbandingan model _Autoregresif Integrated Moving Average_ (_ARIMA), ARIMA + Linear Regression, dan ARIMA + Interactive Regression_ dimana penelitian tersebut menggunakan _mean_ dan _linear interpolation_ untuk mengatasi data PM2.5 yang hilang dengan pengukuran metrik menggunakan _Average Relative Errors_ dengan hasil _ARIMA + Linear Regression_ menjadi model terbaik dengan _error rate_ sebesar 0.1616. Studi lain dilakukan oleh ​Yan et al. (2021)​ telah melakukan perbandingan algoritma *Convolution Neural Network (CNN), Long Short-Term Memory (LSTM), CNN-LSTM*, dan *Back Propagation Neural Network (BPNN)* untuk memprediksi kualitas udara di Beijing dimana model yang menggunakan *CNN-LSTM* dan *LSTM* secara umum memiliki kinerja lebih baik dibandingkan *CNN* dan *BPNN*.

</p>

  

## Business Understanding

### Problem Statement

Berdasarkan uraian diatas, dapat disimpulkan bahwa permasalahan utama dari proyek ini ialah pencemaran udara telah memberikan dampak buruk bagi kesehatan masyarakat, sehingga diperlukan langkah mitigasi dan perencanaan yang matang untuk mengurangi polusi udara di Jakarta.

  

### Goal

Tujuan dari proyek ini adalah untuk mengimplementasikan model *machine learning* dengan jenis _Time Series Forecasting_ untuk memprediksi salah satu komponen pencemar udara di Jakarta, yaitu NO<sub>2</sub> sebagai bagian dari langkah mitigasi untuk mengurangi polusi udara di Jakarta.

  

### Solution Statement

Tahapan untuk menyelesaikan tujuan dari proyek ini adalah sebagai berikut.

1. Melakukan *Exploratory Data Analysis (EDA)* untuk melakukan pembersihan data, visualisasi diagram dan analisis tren dan normalitas Indeks Standar Pencemaran Udara

2. Membangun model *machine learning* dimana akan menggunakan beberapa algoritma yaitu *ARIMA* dan *LSTM*

3. Melakukan perbandingkan ketiga model tersebut menggunakan *_Mean Average Error (MAE)_*, *Mean Square Error (MSE)* dan *Root Mean Square Error (RMSE)*

## Data Understanding

Dataset yang digunakan berasal dari [Open Data Jakarta](https://data.jakarta.go.id/dataset?q=ispu). 

### Deskripsi dan Variabel Dataset

Dataset tersebut berisi data Indeks Standar Pencemaran Udara (ISPU) yang dipantau harian dari tahun 2010 hingga 2021 dari 5 Stasiun Pemantauan Kualitas Udara (SPKU) DKI Jakarta, yaitu
* DKI 1 (Bundaran HI)
* DKI 2 (Kelapa Gading)
*  DKI3 (Jagakarsa)
* DKI4 (Lubang Buaya)
* DKI5 (Kebon Jeruk)

Variabel yang terdapat dalam dataset tersebut sebagai berikut
1.  tanggal : Tanggal pengukuran kualitas udara
2.  stasiun : Lokasi pengukuran di stasiun
3.  pm10 : Partikulat salah satu parameter yang diukur
4.  pm25 : Partikulat salah satu parameter yang diukur
5.  so2 : Sulfida (dalam bentuk SO2) salah satu parameter yang diukur
6.  co : Carbon Monoksida salah satu parameter yand diukur
7.  o3 : Ozon salah satu parameter yang diukur
8.  no2 : NItrogen dioksida salah satu parameter yang diukur
9.  max : Nilai ukur paling tinggi dari seluruh parameter yang diukur dalam waktu yang sama
10.  critical : Parameter yang hasil pengukurannya paling tinggi
11.  categori : Kategori hasil perhitungan indeks standar pencemaran udara

Selain itu, setiap dataset terdapat 2 jenis, yaitu dataset akumulatif dari setiap stasiun yang setiap disusun setiap bulannya dan dataset aggregat dari setiap stasiun yang berarti data ISPU dari dataset tersebut diambil dari nilai ISPU maksimal dari setiap stasiun (dataset akumulatif).

Misalkan ada dataset akumulatif setiap stasiun untuk tanggal 21 Juni 2023 sepert tabel berikut.

| tanggal    | stasiun              | pm10 | pm25 | so2 | co | o3 | no2 | max | critical | category |
|------------|----------------------|------|------|-----|----|----|-----|-----|----------|----------|
| 2023-06-21 | DKI1 (Bundaran HI)   |  83  | 90   |  85 | 22 | 18 |  25 | 90  | pm25     | SEDANG   |
| 2023-06-21 | DKI2 (Kelapa Gading) |  84  | 85   |  82 | 21 | 20 |  18 | 85  | pm25     | SEDANG   |
| 2023-06-21 | DKI3 (Jagakarsa)     |  75  | 88   |  89 | 22 | 20 |  22 | 88  | pm25     | SEDANG   |
| 2023-06-21 | DKI4 (Lubang Buaya)  |  90  | 93   |  87 | 20 | 15 |  23 | 93  | pm25     | SEDANG   |
| 2023-06-21 | DKI5 (Kebon Jeruk)   |  88  | 82   |  83 | 23 | 22 |  24 | 88  | pm10     | SEDANG   |

Jika memperhatikan kolom **max** dari semua stasiun yang dicatat pada tanggal tersebut, stasiun DKI4 memiliki nilai ISPU paling besar, yaitu 93. Sehingga data ISPU untuk tanggal tersebut di dalam dataset aggregat adalah sebagai berikut.

| tanggal    | stasiun              | pm10 | pm25 | so2 | co | o3 | no2 | max | critical | category |
|------------|----------------------|------|------|-----|----|----|-----|-----|----------|----------|
| 2023-06-21 | DKI4 (Lubang Buaya)  |  90  | 93   |  87 | 20 | 15 |  23 | 93  | pm25     | SEDANG   |

Untuk penetuan kategori pada kolom **categori** telah tercantum berdasarkan Lampiran II Peraturan Menteri Lingkungan Hidup dan Kehutanan Nomor P.14/MENLHK/SETJEN/KUM.1/7/2020  sebagai berikut
| Kategori           | Status Warna | Angka Rentang |
|--------------------|--------------|---------------|
| Baik               |     Hijau    |     1 - 50    |
| Sedang             |     Biru     |    51 - 100   |
| Tidak Sehat        |    Kuning    |   101 - 200   |
| Sangat Tidak Sehat |     Merah    |   201 - 300   |
| Berbahaya          |     Hitam    |     >= 300    |

Dalam proyek ini, penulis menggunakan data aggregat setiap stasiun dimana terdapat **114 file CSV** untuk setiap bulan dari tahun 2010 hingga 2021.

### Exploratory Data Analysis (EDA)

Di tahap EDA ini, penulis akan melakukan beberapa tahapan berikut
* Pembersihan Data
* Visualisasi dan analisa setiap komponen pencemar udara
* Visualisasi dan analisa setiap komponen pencemar udara setiap stasiun
* _Missing Value_
* Analisis dan transformasi Skewness dan Kurtosis
* Uji dan transformasi stasioneritas *Time Series*

#### 1. Pembersihan Data

Setelah melakukan *Import Dataset* dan melakukan *concat*, dataset memiliki kondisi sebagai berikut.

|        | tanggal    | stasiun            | pm10   | so2   | co    | o3    | no2   |   max | critical   | categori   |       s02 | keterangan   | kategori   |   Unnamed: 10 |   Unnamed: 11 |   Unnamed: 12 |   Unnamed: 13 |   Unnamed: 14 |   Unnamed: 15 |   Unnamed: 16 |   Unnamed: 17 |   Unnamed: 18 |   Unnamed: 19 |   Unnamed: 20 |   Unnamed: 21 |   pm25 | location   |
|:-------|:-----------|:-------------------|:-------|:------|:------|:------|:------|------:|:-----------|:-----------|----------:|:-------------|:-----------|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|-------:|:-----------|
| count  | 21915      | 21610              | 21864  | 21705 | 21854 | 21805 | 21816 | 21883 | 19537      | 21755      | 143       | 150          | 155        |             0 |             0 |             0 |             0 |             0 |             0 |             0 |             0 |             0 |             0 |             0 |             0 |   1763 | 305        |
| unique | 4410       | 55                 | 246    | 251   | 201   | 463   | 225   |   355 | 102        | 11         | nan       | 5            | 5          |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |    191 | 4          |
| top    | 2020-06-06 | DKI1 (Bunderan HI) | ---    | ---   | ---   | ---   | ---   |     0 | O3         | SEDANG     | nan       | SEDANG       | SEDANG     |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |     77 | SEDANG     |
| freq   | 121        | 4291               | 3098   | 2884  | 2696  | 2918  | 2805  |  2343 | 10638      | 12684      | nan       | 96           | 80         |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |     43 | 182        |
| mean   | nan        | nan                | nan    | nan   | nan   | nan   | nan   |   nan | nan        | nan        |  20.6853  | nan          | nan        |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |    nan | nan        |
| std    | nan        | nan                | nan    | nan   | nan   | nan   | nan   |   nan | nan        | nan        |   7.25532 | nan          | nan        |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |    nan | nan        |
| min    | nan        | nan                | nan    | nan   | nan   | nan   | nan   |   nan | nan        | nan        |   7       | nan          | nan        |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |    nan | nan        |
| 25%    | nan        | nan                | nan    | nan   | nan   | nan   | nan   |   nan | nan        | nan        |  16       | nan          | nan        |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |    nan | nan        |
| 50%    | nan        | nan                | nan    | nan   | nan   | nan   | nan   |   nan | nan        | nan        |  22       | nan          | nan        |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |    nan | nan        |
| 75%    | nan        | nan                | nan    | nan   | nan   | nan   | nan   |   nan | nan        | nan        |  23.5     | nan          | nan        |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |    nan | nan        |
| max    | nan        | nan                | nan    | nan   | nan   | nan   | nan   |   nan | nan        | nan        |  58       | nan          | nan        |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |    nan | nan        |

Berdasarkan kondisi berikut, sangat diperlukan untuk melakukan pembersihan data dan normalisasi susunan data yang tidak konsisten.

##### 1.1. Hapus Kolom "Unnamed[n]"
Langkah pertama ialah dengan menghapus kolom "Unnamed". Hal tersebut dikarenakan kolom tersebut tidak mempunyai nilai sama sekali atau disebut dengan NaN seperti terlihat pada tabel berikut.
|       |   Unnamed: 10 |   Unnamed: 11 |   Unnamed: 12 |   Unnamed: 13 |   Unnamed: 14 |   Unnamed: 15 |   Unnamed: 16 |   Unnamed: 17 |   Unnamed: 18 |   Unnamed: 19 |   Unnamed: 20 |   Unnamed: 21 |
|:------|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|--------------:|
| count |             0 |             0 |             0 |             0 |             0 |             0 |             0 |             0 |             0 |             0 |             0 |             0 |
| mean  |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |
| std   |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |
| min   |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |
| 25%   |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |
| 50%   |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |
| 75%   |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |
| max   |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |           nan |

##### 1.2. Hapus baris yang NaN
Setelah menghapus kolom yang bernilai NaN, langkah berikutnya adalah menghapus baris dimana seluruh data nya adalah NaN.

##### 1.3. Periksa dan Normalisasi Format Tanggal
Format tanggal yang digunakan dalam dataset adalah "YYYY-MM-DD" (contohnya: 2023-06-21). Sebelum memasuki tahapan berikutnya, perlu melakukan pemeriksaan tanggal yang tidak sesuai format agak data konsistan dan seragam. Setelah dilakukan pemeriksaan, ditemukan terdapat 274 data yang data tanggalnya tidak sesuai format dimana salah satu data tanggal yang bermasalah seperti berikut.

|       | tanggal    | stasiun                          | pm10   |   so2 |   co |   o3 |   no2 |   max | critical   | categori   |   s02 |   keterangan |   kategori |   pm25 |   location |
|------:|:-----------|:---------------------------------|:-------|------:|-----:|-----:|------:|------:|:-----------|:-----------|------:|-------------:|-----------:|-------:|-----------:|
| 12856 | 26/12/2016 | DKI2 (Kelapa Gading)             | 38     |    17 |   10 |   62 |    21 |    62 | O3         | SEDANG     |   nan |          nan |        nan |    nan |        nan |
| 12887 | 26/12/2016 | DKI3 (Jagakarsa)                 | 52     |    31 |   10 |   43 |     3 |    52 | PM10       | SEDANG     |   nan |          nan |        nan |    nan |        nan |
| 12918 | 26/12/2016 | DKI4 (Lubang Buaya)              | 52     |    26 |   14 |   47 |     5 |    52 | PM10       | SEDANG     |   nan |          nan |        nan |    nan |        nan |
| 12949 | 26/12/2016 | DKI5 (Kebon Jeruk) Jakarta Barat | ---    |    18 |   39 |   66 |     5 |    66 | O3         | SEDANG     |   nan |          nan |        nan |    nan |        nan |

Berdasarkan hasil berikut, format yang digunakan adalah "DD/MM/YYYY", sehingga perlu dilakukan normalisasi format tanggal sehingga hasilnya menjadi seperti berikut.

|       | tanggal             | stasiun                          | pm10   |   so2 |   co |   o3 |   no2 |   max | critical   | categori   |   s02 |   keterangan |   kategori |   pm25 |   location |
|------:|:--------------------|:---------------------------------|:-------|------:|-----:|-----:|------:|------:|:-----------|:-----------|------:|-------------:|-----------:|-------:|-----------:|
| 12825 | 2016-12-26 | DKI1 (Bunderan HI)               | 49     |    32 |   23 |   23 |     2 |    49 | PM10       | BAIK       |   nan |          nan |        nan |    nan |        nan |
| 12856 | 2016-12-26 | DKI2 (Kelapa Gading)             | 38     |    17 |   10 |   62 |    21 |    62 | O3         | SEDANG     |   nan |          nan |        nan |    nan |        nan |
| 12887 | 2016-12-26 | DKI3 (Jagakarsa)                 | 52     |    31 |   10 |   43 |     3 |    52 | PM10       | SEDANG     |   nan |          nan |        nan |    nan |        nan |
| 12918 | 2016-12-26 | DKI4 (Lubang Buaya)              | 52     |    26 |   14 |   47 |     5 |    52 | PM10       | SEDANG     |   nan |          nan |        nan |    nan |        nan |
| 12949 | 2016-12-26 | DKI5 (Kebon Jeruk) Jakarta Barat | ---    |    18 |   39 |   66 |     5 |    66 | O3         | SEDANG     |   nan |          nan |        nan |    nan |        nan |

##### 1.4. Normalisasi struktur data Bulan Juni hingga Juli 2021

Langkah berikutnya adalah melakukan pemeriksaan nilai NaN pada kolom stasiun, dan ditemukan terdapat 305 baris data yang bernilai NaN. Setelah dilakukan analisa, ternyata ditemukan inkonsistensian pengisian data Bulan Juni hinggal Juli 2021 di seluruh stasiun, dimana 5 baris pertamanya adalah sebagai berikut.

|       | tanggal             |   stasiun | pm10               |   so2 |   co |   o3 |   no2 |   max |   critical | categori   |   s02 |   keterangan |   kategori |   pm25 | location   |
|------:|:--------------------|----------:|:-------------------|------:|-----:|-----:|------:|------:|-----------:|:-----------|------:|-------------:|-----------:|-------:|:-----------|
| 21050 | 2021-06-01 |       nan | DKI1 (Bunderan HI) |    83 |   22 |   18 |    19 |    35 |         83 | PM25       |   nan |          nan |        nan |     59 | SEDANG     |
| 21051 | 2021-06-02 |       nan | DKI1 (Bunderan HI) |    84 |   21 |   20 |    24 |    38 |         84 | PM25       |   nan |          nan |        nan |     59 | SEDANG     |
| 21052 | 2021-06-03 |       nan | DKI1 (Bunderan HI) |    76 |   22 |   20 |    17 |    41 |         76 | PM25       |   nan |          nan |        nan |     54 | SEDANG     |
| 21053 | 2021-06-04 |       nan | DKI1 (Bunderan HI) |    87 |   20 |   13 |    14 |    30 |         87 | PM25       |   nan |          nan |        nan |     63 | SEDANG     |
| 21054 | 2021-06-05 |       nan | DKI1 (Bunderan HI) |    79 |   23 |   20 |    19 |    38 |         79 | PM25       |   nan |          nan |        nan |     59 | SEDANG     |

Berdasarkan tabel berikut dapat disimpulkan bahwa terjadi kesalahan pengisian data dimana data yang harusnya lokasi stasiun berada di kolom pm10, data pm10 berada di kolom pm25 dan seterusnya.

Untuk mengatasi masalah tersebut, perlu dilakukan penyusunan ulang data ke kolom yang asli berdasarkan data di bulan sebelumnya, sehingga hasilnya menjadi sebagai berikut.

|       | tanggal             | stasiun            |   pm10 |   so2 |   co |   o3 |   no2 |   max | critical   | categori   |   s02 |   keterangan |   kategori |   pm25 | location   |
|------:|:--------------------|:-------------------|-------:|------:|-----:|-----:|------:|------:|:-----------|:-----------|------:|-------------:|-----------:|-------:|:-----------|
| 21050 | 2021-06-01 | DKI1 (Bunderan HI) |     59 |    22 |   18 |   19 |    35 |    83 | PM25       | SEDANG     |   nan |          nan |        nan |     83 | SEDANG     |
| 21051 | 2021-06-02 | DKI1 (Bunderan HI) |     59 |    21 |   20 |   24 |    38 |    84 | PM25       | SEDANG     |   nan |          nan |        nan |     84 | SEDANG     |
| 21052 | 2021-06-03 | DKI1 (Bunderan HI) |     54 |    22 |   20 |   17 |    41 |    76 | PM25       | SEDANG     |   nan |          nan |        nan |     76 | SEDANG     |
| 21053 | 2021-06-04 | DKI1 (Bunderan HI) |     63 |    20 |   13 |   14 |    30 |    87 | PM25       | SEDANG     |   nan |          nan |        nan |     87 | SEDANG     |
| 21054 | 2021-06-05 | DKI1 (Bunderan HI) |     59 |    23 |   20 |   19 |    38 |    79 | PM25       | SEDANG     |   nan |          nan |        nan |     79 | SEDANG     |

##### 1.5. Pemeriksaan data unik dan Perbaikan Data Stasiun

Langkah berikutnya adalah memeriksa data unik stasiun. Seperti di penjelasan deskripsi dan variabel dataset, ada terdapat 5 stasiun pemantauan. Setelah di periksa, ditemukan ada 55 data yang unik sebagai berikut.

    array(['DKI1 (Bunderan HI)', 'DKI2 (Kelapa Gading)', 
    'DKI3 (Jagakarsa)', 'DKI4 (Lubang Buaya)', 
    'DKI5 (Kebon Jeruk)', 'DKI5 (Kebon Jeruk) Jakarta Barat', 
    '45', '34', '59', '56', '35', '36', '37', '39', '30', '40', 
    '48', '64', '50', '41', '44', '62', '43', '58', '33', '49', 
    '61', '47', '51', '42', '55', '54', '65', '53', '27', '71', 
    '52', '63', '60', '66', '38', '---', '32', '74', '76', '70', 
    '89', '69', '101', '57', '73', '78', '22', '24', '25'], 
    dtype=object)

Dimana jika diperhatikan terdapat 2 stasiun DKI5, yaitu **"DKI5 (Kebon Jeruk)"** dan **"DKI5 (Kebon Jeruk) Jakarta Barat"**. Selain itu, terdapat beberapa angka dan data kosong **"---"**.

Untuk melakukan perbaikan data stasiun, ada 2 tahapan yang harus dilakukan, yaitu menganalisis data stasiun yang berisi selain 5 stasiun diatas (termasuk duplikatnya) dan melakukan perbaikan posisi data.

Setelah dilakukan analisis, terdapat 155 baris data yang kolom stasiun tidak sesuai format dari dataset dimana 5 diantaranya sebagai berikut.

|       | tanggal             |   stasiun |   pm10 |   so2 |   co |   o3 |   no2 |   max | critical   | categori   |   s02 |   keterangan |   kategori |   pm25 |   location |
|------:|:--------------------|----------:|-------:|------:|-----:|-----:|------:|------:|:-----------|:-----------|------:|-------------:|-----------:|-------:|-----------:|
| 18765 | 2020-03-01 |        45 |      5 |    13 |   28 |    8 |    45 |     1 | PM10       | BAIK       |   nan |          nan |        nan |    nan |        nan |
| 18766 | 2020-03-02 |        34 |      5 |    15 |   32 |   10 |    34 |     1 | PM10       | BAIK       |   nan |          nan |        nan |    nan |        nan |
| 18767 | 2020-03-03 |        59 |      5 |    23 |   29 |   14 |    59 |     1 | PM10       | SEDANG     |   nan |          nan |        nan |    nan |        nan |
| 18768 | 2020-03-04 |        56 |      7 |    19 |   55 |   16 |    56 |     1 | PM10       | SEDANG     |   nan |          nan |        nan |    nan |        nan |
| 18769 | 2020-03-05 |        35 |      6 |    16 |   30 |   13 |    35 |     1 | PM10       | BAIK       |   nan |          nan |        nan |    nan |        nan |

Dimana data stasiun hilang dan terjadi perubahan posisi dimana posisi kolom stasiun diisi oleh data PM10, kolom PM10 adalah data SO2 dan seterusnya. Sedangkan data pada kolom max adalah indeks dari kolom yang memiliki nilai ISPU paling tinggi, dimana data di kolom NO2 harusnya berada di kolom max.

Untuk memperbaiki masalah tersebut dengan cara mengubah posisi setiap data tiap komponen pencemar udara ISPU ke kolom yang seharusnya. Kemudian dilakukan _generate_ data stasiun untuk setiap bulannya sehingga hasilnya sebagai berikut.

|       | tanggal             | stasiun            |   pm10 |   so2 |   co |   o3 |   no2 |   max | critical   | categori   |   s02 |   keterangan |   kategori |   pm25 |   location |
|------:|:--------------------|:-------------------|-------:|------:|-----:|-----:|------:|------:|:-----------|:-----------|------:|-------------:|-----------:|-------:|-----------:|
| 18765 | 2020-03-01 | DKI1 (Bunderan HI) |     45 |     5 |   13 |   28 |     8 |    45 | PM10       | BAIK       |   nan |          nan |        nan |    nan |        nan |
| 18766 | 2020-03-02 | DKI1 (Bunderan HI) |     34 |     5 |   15 |   32 |    10 |    34 | PM10       | BAIK       |   nan |          nan |        nan |    nan |        nan |
| 18767 | 2020-03-03 | DKI1 (Bunderan HI) |     59 |     5 |   23 |   29 |    14 |    59 | PM10       | SEDANG     |   nan |          nan |        nan |    nan |        nan |
| 18768 | 2020-03-04 | DKI1 (Bunderan HI) |     56 |     7 |   19 |   55 |    16 |    56 | PM10       | SEDANG     |   nan |          nan |        nan |    nan |        nan |
| 18769 | 2020-03-05 | DKI1 (Bunderan HI) |     35 |     6 |   16 |   30 |    13 |    35 | PM10       | BAIK       |   nan |          nan |        nan |    nan |        nan |

Setelah melakukan perbaikan posisi data, tahapan berikutnya adalah melakukan _rename_ untuk nama stasiun **"DKI5 (Kebon Jeruk) Jakarta Barat"** menjadi **"DKI5 (Kebon Jeruk)"**.

##### 1.6. Gabungkan data kolom yang sejenis dan hapus kolom yang tidak digunakan

Setelah melakukan perbaikan format data, langkah berikut nya adalah melakukan penyatuan kolom yang sama secara konteks. Ada 2 kolom yang akan disatukan, yaitu kolom "categori" dengan "kategori" dan kolom "so2" dengan "s02".

Setelah melakukan penggabungkan, maka langkah berikutnya adalah menghapus kolom yang tidak digunakan. Selain kolom "kategori" dan "s02" yang sudah tidak digunakan karena sudah digabungkan, kolom "location" juga dihapus karena kolom tersebut tidak memiliki data apapun setelah dipindahkan ke kolom "stasiun".

##### 1.7. Perbaiki format kolom "categori"

Setelah menghapus 3 kolom sebelumnya, ada satu kolom yang memiliki fungsi yang serupa, yaitu kolom "categori" dan "keterangan". Kolom ini berisi keterangan mengenai kategori ISPU dari stasiun pemantauan.

Setelah dilakukan pemeriksaan, ditemukan 150 baris yang memiliki data di kolom keterangan, dimana 5 baris pertama adalah sebagai berikut.

|       | tanggal             | stasiun            |   pm10 |   so2 |   co |   o3 |   no2 |   max |   critical | categori   | keterangan   |   pm25 |
|------:|:--------------------|:-------------------|-------:|------:|-----:|-----:|------:|------:|-----------:|:-----------|:-------------|-------:|
| 15265 | 2018-04-01 | DKI1 (Bunderan HI) |     25 |    22 |   17 |   22 |     1 |    25 |          1 | PM10       | BAIK         |    nan |
| 15266 | 2018-04-02 | DKI1 (Bunderan HI) |     39 |    22 |   18 |   24 |     2 |    39 |          1 | PM10       | BAIK         |    nan |
| 15267 | 2018-04-03 | DKI1 (Bunderan HI) |     45 |    22 |   27 |   23 |     2 |    45 |          1 | PM10       | BAIK         |    nan |
| 15268 | 2018-04-04 | DKI1 (Bunderan HI) |     18 |    22 |   20 |   29 |     3 |    29 |          4 | O3         | BAIK         |    nan |
| 15269 | 2018-04-05 | DKI1 (Bunderan HI) |      8 |    24 |   25 |   16 |     4 |    25 |          3 | CO         | BAIK         |    nan | 

Seperti yang terlihat pada tabel berikut, terjadi permasalahan dimana kolom "critical" berisi nomor indeks partikel pencemar udara seperti yang terjadi pada data sebelumnya. Untuk mengatasi masalah tersebut, perlu dilakukan perubahan posisi data dimana data "critical" diambil dari kolom "categori" dan seterusnya sehingga menjadi sebagai berikut.

|       | tanggal             | stasiun            |   pm10 |   so2 |   co |   o3 |   no2 |   max | critical   | categori   | keterangan   |   pm25 |
|------:|:--------------------|:-------------------|-------:|------:|-----:|-----:|------:|------:|:-----------|:-----------|:-------------|-------:|
| 15265 | 2018-04-01 | DKI1 (Bunderan HI) |     25 |    22 |   17 |   22 |     1 |    25 | PM10       | BAIK       | BAIK         |    nan |
| 15266 | 2018-04-02 | DKI1 (Bunderan HI) |     39 |    22 |   18 |   24 |     2 |    39 | PM10       | BAIK       | BAIK         |    nan |
| 15267 | 2018-04-03 | DKI1 (Bunderan HI) |     45 |    22 |   27 |   23 |     2 |    45 | PM10       | BAIK       | BAIK         |    nan |
| 15268 | 2018-04-04 | DKI1 (Bunderan HI) |     18 |    22 |   20 |   29 |     3 |    29 | O3         | BAIK       | BAIK         |    nan |
| 15269 | 2018-04-05 | DKI1 (Bunderan HI) |      8 |    24 |   25 |   16 |     4 |    25 | CO         | BAIK       | BAIK         |    nan |

Setelah itu, kolom keterangan sudah dapat dihapus dengan aman.

##### 1.8. Hapus data yang memiliki kategori "TIDAK ADA DATA"

Setelah sebelumnya telah melakukan perbaikan pada data kolom "categori", langkah berikutnya adalah menghapus baris data yang memiliki kategori "TIDAK ADA DATA". Data yang memiliki kategori tersebut memiliki arti bahwa tidak ada catatan pengukuran ISPU pada hari tersebut. Setelah dilakukan pemeriksaan, ditemukan bahwa ada sebanyak 2379 data yang memiliki kategori tersebut dimana beberapa sampelnya seperti berikut.

|    | tanggal             | stasiun              | pm10   | so2   | co   | o3   | no2   |   max |   critical | categori       |   pm25 |
|---:|:--------------------|:---------------------|:-------|:------|:-----|:-----|:------|------:|-----------:|:---------------|-------:|
| 31 | 2010-01-01 | DKI2 (Kelapa Gading) | ---    | ---   | ---  | ---  | ---   |     0 |        nan | TIDAK ADA DATA |    nan |
| 32 | 2010-01-02 | DKI2 (Kelapa Gading) | ---    | ---   | ---  | ---  | ---   |     0 |        nan | TIDAK ADA DATA |    nan |
| 33 | 2010-01-03 | DKI2 (Kelapa Gading) | ---    | ---   | ---  | ---  | ---   |     0 |        nan | TIDAK ADA DATA |    nan |
| 34 | 2010-01-04 | DKI2 (Kelapa Gading) | ---    | ---   | ---  | ---  | ---   |     0 |        nan | TIDAK ADA DATA |    nan |
| 35 | 2010-01-05 | DKI2 (Kelapa Gading) | ---    | ---   | ---  | ---  | ---   |     0 |        nan | TIDAK ADA DATA |    nan |

Ada 2 cara yang dapat dilakukan untuk mengatasi kasus data hilang seperti ini, yaitu dengan menghapus data yang hilang dan yang terakhir adalah menggantikan dengan berpatok dengan urutan data sebelumnya atau urutan data setelahnya. Untuk kasus ini, penulis memutuskan untuk menghapus seluruh data yang memiliki kategori tersebut.

##### 1.9. Pemeriksaan data unik untuk kolom "categori" dan "critical"

Langkah selanjutnya adalah memeriksa keunikan data di kolom "categori" dan "critical". Berdasarkan dari peraturan menteri, terdapat 5 kategori ISPU dan ada 6 komponen kritikal yang terdapat di Deskripsi dan Variabel dataset.

Setelah diperiksa, ditemukan hasil sebagai berikut.

    ['CO' 'O3' 'PM10' 'NO2' 'SO2' 'PM25' 'BAIK'] 
    ['SEDANG' 'BAIK' 'TIDAK SEHAT' 'SANGAT TIDAK SEHAT' 'BERBAHAYA' nan]

Dari hasil tersebut, baris pertama merupakan data unik dari kolom "critical" dan baris berikutnya merupakan data unik dari kolom "categori". Disini dapat disimpulkan pada kolom "critical" terdapat sebuah data **BAIK** dimana data tersebut harusnya ada di kolom "categori". Selain itu di kolom "categori" terdapat data yang berupa nan.

Untuk itu perlu dilakukan analisa data yang bermasalah tersebut, dan hasilnya ditemukan sebuah masalah di baris dengan indeks **21967**.

|       | tanggal             | stasiun            |   pm10 |   so2 |   co |   o3 |   no2 | max   | critical   |   categori |   pm25 |
|------:|:--------------------|:-------------------|-------:|------:|-----:|-----:|------:|:------|:-----------|-----------:|-------:|
| 21967 | 2021-12-03 00:00:00 | DKI1 (Bunderan HI) |     49 |     9 |   19 |    7 |    49 | PM25  | BAIK       |        nan |     31 |

Disini dapat disimpulkan terdapat anomali data dimana data di kolom max yang harusnya adalah nilai ISPU maksimal dari seluruh komponen pencemar, namun diisi dengan data dari kolom critical, begitu juga data di kolom critical yang harusnya berada di kolom categori. Untuk itu dilakukan pemindahan data ke kolom yang sebenarnya sehingga hasilnya sebagai berikut.

|       | tanggal             | stasiun            |   pm10 |   so2 |   co |   o3 |   no2 |   max | critical   | categori   |   pm25 |
|------:|:--------------------|:-------------------|-------:|------:|-----:|-----:|------:|------:|:-----------|:-----------|-------:|
| 21967 | 2021-12-03 00:00:00 | DKI1 (Bunderan HI) |     49 |     9 |   19 |    7 |    49 |     0 | PM25       | BAIK       |     31 |

##### 1.10. Konversi tipe data ISPU ke Float64 dan data "---" ke NaN

Jika melihat tabel terakhir, alasan nilai kolom max diberi dengan 0 disebabkan seluruh data angka masih menggunakan tipe data **string** sehingga sangat sulit untuk menjalankan perintah `max()`. Untuk itu perlu dilakukan konversi data numerik ke Float64.

Sebelum melakukan konversi, langkah pertama adalah melakukan konversi data _null_ **"---"** ke data NaN. Alasan untuk melakukan konversi adalah untuk mencegah program melakukan konversi pada data _null_.  Sehingga deskripsi dataset sebelumnya sebagai berikut.

|        | tanggal             | stasiun            | pm10   |   so2 |    co | o3    |   no2 |   max | critical   | categori   |   pm25 |
|:-------|:--------------------|:-------------------|:-------|------:|------:|:------|------:|------:|:-----------|:-----------|-------:|
| count  | 19536               | 19536              | 19522  | 19506 | 19512 | 19463 | 19474 | 19536 | 19536      | 19536      |   1749 |
| unique | 4377                | 5                  | 241    |   179 |   183 | 461   |   177 |   327 | 6          | 5          |    192 |
| top    | 2020-06-06 00:00:00 | DKI1 (Bunderan HI) | ---    |     5 |    11 | ---   |     9 |    65 | O3         | SEDANG     |     77 |
| freq   | 120                 | 4273               | 744    |   607 |   636 | 573   |  1124 |   343 | 10715      | 13042      |     45 |
| first  | 2010-01-01 00:00:00 | nan                | nan    |   nan |   nan | nan   |   nan |   nan | nan        | nan        |    nan |
| last   | 2021-12-31 00:00:00 | nan                | nan    |   nan |   nan | nan   |   nan |   nan | nan        | nan        |    nan |

Menjadi sebagai berikut

|        | tanggal             | stasiun            |   pm10 |   so2 |    co |    o3 |   no2 |   max | critical   | categori   |   pm25 |
|:-------|:--------------------|:-------------------|-------:|------:|------:|------:|------:|------:|:-----------|:-----------|-------:|
| count  | 19536               | 19536              |  18778 | 18968 | 19144 | 18890 | 19008 | 19536 | 19536      | 19536      |   1725 |
| unique | 4377                | 5                  |    240 |   178 |   182 |   460 |   176 |   327 | 6          | 5          |    191 |
| top    | 2020-06-06 00:00:00 | DKI1 (Bunderan HI) |     55 |     5 |    11 |    65 |     9 |    65 | O3         | SEDANG     |     77 |
| freq   | 120                 | 4273               |    468 |   607 |   636 |   230 |  1124 |   343 | 10715      | 13042      |     45 |
| first  | 2010-01-01 00:00:00 | nan                |    nan |   nan |   nan |   nan |   nan |   nan | nan        | nan        |    nan |
| last   | 2021-12-31 00:00:00 | nan                |    nan |   nan |   nan |   nan |   nan |   nan | nan        | nan        |    nan |

Setelah melakukan konversi data _null_, langkah berikutnya adalah melakukan konversi data numerik ISPU ke _float64_ dimana hasil akhirnya sebagai berikut.

|       |       pm10 |        so2 |         co |         o3 |         no2 |      pm25 |
|:------|-----------:|-----------:|-----------:|-----------:|------------:|----------:|
| count | 18778      | 18968      | 19144      | 18890      | 19008       | 1725      |
| mean  |    53.114  |    18.1176 |    20.938  |    64.9766 |    12.3655  |   78.0557 |
| std   |    18.9246 |    12.681  |    12.4737 |    36.9294 |     8.67499 |   23.003  |
| min   |     2      |     0      |     0      |     3      |     1       |   13      |
| 25%   |    41      |     9      |    12      |    39      |     7       |   63      |
| 50%   |    55      |    16      |    18      |    60      |    11       |   78      |
| 75%   |    65      |    25      |    27      |    83      |    15       |   92      |
| max   |   179      |   112      |   135      |   314      |   148       |  174      |

Dengan begini, penulis dapat menganalisa komponen numerik ISPU seperti rata-rata, standar deviasi, nilai minimum, maksimum, dan kuartal.

##### 1.11. Perbaiki nilai kolom max di baris indeks 21967

Setelah melakukan konversi tipe data, maka fungsi `max()` juga dapat digunakan, sehingga nilai max dari data tersebut adalah **49** .

|       | tanggal             | stasiun            |   pm10 |   so2 |   co |   o3 |   no2 |   max | critical   | categori   |   pm25 |
|------:|:--------------------|:-------------------|-------:|------:|-----:|-----:|------:|------:|:-----------|:-----------|-------:|
| 21967 | 2021-12-03 00:00:00 | DKI1 (Bunderan HI) |     49 |     9 |   19 |    7 |    49 |    49 | PM25       | BAIK       |     31 |

##### 1.12. Split Setiap Stasiun Pemantauan

Langkah selanjutnya adalah melakukan pemecahan antar stasiun ke dalam 5 _dataframe_. Pemisahan ini digunakan untuk melakukan analisis antar stasiun secara lebih detail dan juga digunakan dalam pembuatan model dimana setiap model akan bekerja sesuai data setiap stasiun. Selain itu, pembagian ini juga digunakan untuk memasuki tahapan berikutnya, yaitu pemeriksaan dan perbaikan data tanggal yang duplikat setiap stasiun.

##### 1.13. Perbaiki Data Tanggal yang Duplikat

Data tanggal merupakan kolom yang sangat penting, karena kolom ini digunakan sebagai sumbu x dari sebuah data deret waktu / _time series_. Karena itu kolom tanggal harusnya memiliki format yang seragam dan juga tidak boleh ada yang duplikat. Setelah sebelumnya sudah dilakukan penyamaan format, langkah yang belum dilakukan adalah pengecekan duplikasi data tanggal. Pada tahap ini akan dilakukan pemeriksaan data tanggal untuk setiap stasiun sehingga mengurangi tingkat kesalahan sewaktu melakukan perbaikan data tanggal.

Setelah dilakukan analisis, ditemukan data tanggal yang duplikat dengan hasil sebagai berikut.

| Stasiun | Total Data Duplikat |
|---------|:-------------------:|
| DKI1    |          27         |
| DKI2    |          63         |
| DKI3    |          63         |
| DKI4    |          62         |
| DKI5    |          39         |

Mayoritas permasalahan terjadi pada data di tanggal 8 Oktober 2016, 8-9 November 2016, 8 Desember 2016, data bulan Juni 2020 dan data bulan September 2016 dimana data tersebut seharusnya berada di bulan 9, namun di dataset tercatat kembali ke bulan 8.

#### 2. Visualisasi dan Analisa Setiap Komponen Pencemar Udara Secara Umum

##### 2.1. Analisa data yang bernilai NaN dan _Zero_

Sebelum memasuki tahap berikutnya, langkah yang harus dilakukan adalah memeriksa jumlah data komponen pencemar udara yang bernilai **NaN** dan **0**. Data ini akan menjadi masalah dalam melakukan analisa kedepannya sehingga perlu dianalisa. Sehingga didapatkan hasilnya sebagai berikut.

| Tipe | pm10 | so2 |  co |  o3 | no2 |
|------|:----:|:---:|:---:|:---:|:---:|
| NaN  |  758 | 568 | 392 | 646 | 528 |
| Zero |   0  |  59 |  12 |  0  |  0  |

##### 2.2. Analisis Deskripsi Variabel

![Total Kategori ISPU Seluruh Stasiun](https://media.discordapp.net/attachments/1121095008926302358/1121098789185404958/Total_Kategori_ISPU.png)

Berdasarkan grafik ini dapat disimpulkan bahwa kategori ISPU maksimum di 5 stasiun SPKU di DKI Jakarta mayoritas kategori Sedang dengan persentase 66.76%, diikuti dengan kategori Baik dengan persentase 18.86%, Tidak Sehat dengan persentase 13.34%, Sangat Tidak Sehat dengan persentase 1.04% dan Berbahaya dengan persentase 0.005% dengan detail sebagai berikut.

| Kategori           | Total |
| ------------------ | ----- |
| BAIK               | 13042 |
| SEDANG             | 3683  |
| TIDAK SEHAT        | 2606  |
| SANGAT TIDAK SEHAT | 203   |
| BERBAHAYA          | 1     |

![Total Data setiap stasiun](https://media.discordapp.net/attachments/1121095008926302358/1121098789466427475/Total_Kategori_Stasiun.png)

Berdasarkan grafik ini, total data ISPU yang dicatat oleh Stasiun DKI 1 sebesar 4273 data, DKI 2 sebesar 4032 data, DKI 3 sebesar 3980, DKI 4 sebesar 3974, dan DKI 5 sebesar 3277. Ini menunjukkan bahwa tidak semua stasiun melakukan pencatatan ISPU dalam satu hari yang sama.


#### 3.  Visualisasi dan Analisa Setiap Komponen Pencemar Udara Setiap Stasiun

##### 3.1. Analisa ISPU DKI 1 (Bundaran HI)

a. Analisis nilai ISPU

|       |      pm10 |       so2 |        co |        o3 |        no2 |     pm25 |
|:------|----------:|----------:|----------:|----------:|-----------:|---------:|
| count | 4171      | 4208      | 4233      | 4180      | 4190       | 365      |
| mean  |   52.2263 |   18.091  |   24.8524 |   49.5146 |   14.1076  |  69.074  |
| std   |   14.5788 |   10.7554 |   11.1532 |   25.7847 |    8.94871 |  18.1171 |
| min   |    4      |    1      |    3      |    3      |    1       |  20      |
| 25%   |   43      |   10      |   17      |   29      |    7       |  57      |
| 50%   |   54      |   17      |   24      |   46      |   14       |  70      |
| 75%   |   62      |   25      |   31      |   66      |   19       |  81      |
| max   |  104      |  106      |   95      |  198      |   79       | 112      |

Berdasarkan tabel diatas

* Kandungan PM10 mendominasi dengan nilai ISPU rata-rata sebesar 52.29 dengan nilai maksimum 104

* Kandungan O3 menempati urutan kedua dengan nilai ISPU rata-rata 49.41 dengan nilai maksimum 198

* Kandungan CO menempati urutan ketiga dengan nilai ISPU rata-rata 24.81 dengan nilai maksmimum 95

* Kandungan SO2 menempati urutan keempat dengan nilai ISPU rata-rata sebesar 18.03 dengan nilai maksimum 106

* Kandungan NO2 menempati urutan terakhir dengan nilai ISPU rata-rata 14.01 dan nilai maksimum 79

* Kandungan PM25 memiliki nilai ISPU rata-rata sebesar 69.07 dengan nilai maksimum 112

* Secara angka, komponen PM25 menempati urutan tertinggi walaupun pengukurannya dimulai di tahun 2021 (Penjelasan lengkap akan dibahas di segmen Pengukuran PM2.5)

b. Analisis _Missing Value_ dan _Zero Value_ serta _range_ tanggal

| Tipe | pm10 | so2 |  co |  o3 | no2 |
|------|:----:|:---:|:---:|:---:|:---:|
| NaN  |  102 | 65 | 40 | 93 | 83 |
| Zero |   0  |  0 |  0 |  0  |  0  |

    Range tanggal pada data stasiun 
    2010-01-01 00:00:00 2021-12-31 00:00:00

**Berdasarkan hasil analisis _Missing Value_, _Zero Value_ serta tanggal _Range_ berikut**

* Data dari DKI1 dicatat mulai dari tanggal 01 Januari 2010 hingga 31 Desember 2021

* Secara total, terdapat 383 Data NaN dimana PM10, O3, dan NO3 merupakan komponen udara yang paling banyak data NaN

* Selain itu, seluruh nilai data > 0

c. Analisis Komponen PM<sub>10</sub>

![Nilai ISPU PM10](https://media.discordapp.net/attachments/1121095008926302358/1121109254254891158/pm10.png)

**Berdasarkan diagram PM10 berikut**

* Berdasarkan diagram tahun 2010 hingga 2015, terdapat sebuah tren dimana setiap akhir tahun, pergerakan indeks akan turun

* Berdasarkan diagram tahun 2016 hingga 2021

	* Pergerakan indeks sangat bervariatif dan berfluktuatif

	* Pada awal tahun 2016, terjadi peningkatan indeks PM10 hingga mendekati 150, kemudian indeks perlahan menurun hingga berada di bawah level indeks 50 hingga menurun di akhir tahun

	* Pada tahun 2017, terjadi tren peningkatan hingga berada di puncak di pertengahan hingga mendekati akhir tahun, kemudian indeks menurun secara tajam di akhir tahun dan stagnan di bawah level 50 hingga awal tahun 2018

	* Pada tahun 2018, terjadi peningkatan indeks hingga melewati 120, setelah itu terjadi penurunan. Peningkatan secara besar kembali terjadi di bulan November hingga turun di bulan Desember akhir

	* Pada tahun 2019, pergerakan sangat fluktuatif, dimana nilai indeks terjadi peningkatan sangat tajam di awal tahun dan di akhir tahun indeks akan menurun dibandingkan dengan rata-rata indeks selama tahun tersebut hingga awal tahun 2020

	* Pada tahun 2020, setelah penurunan terjadi tren peningkatan sejak bulan Maret hingga mengalami penurunan secara tajam sejak memasuki bulan November 2020. Peningkatan terjadi di akhir November dan mulai turun dan stagnan di bulan Desember hingga akhir tahun 2020

	* Pada tahun 2021, tren indeks sempat tinggi di Januari kemudian selama Febuari mengalami stagnasi hingga perlahan mengalami peningkatan dari Maret hingga Agustus dan September. Setelah itu mengalami tren penurunan hingga akhir November dan kembali mengalami peningkatan di Desember

d. Analisis Komponen O<sub>3</sub>

![Nilai ISPU O3](https://cdn.discordapp.com/attachments/1121095008926302358/1121109255991349340/o3.png)

**Berdasarkan diagram O3 berikut**

* Selama tahun 2010 hingga 2012 terjadi tren peningkatan indeks O3, kemudian terjadi penurunan hingga awal tahun 2016

* Pada tahun 2016, setelah terjadi peningkatan yang tajam di awal bulan, tren penurunan kembali terjadi hingga pertengahan tahun, kemudian perlahan naik hingga kembali turun di akhir tahun

* Pada tahun 2017, indeks mengalami tren peningkatan yang cukup besar hingga mendekati akhir tahun dan mengalami penurunan hingga awal tahun 2018

* Pada tahun 2018 terjadi peningkatan mendekati pertengahan tahun dan mendekati akhir tahun

* Pada tahun 2019 diawali dengan peningkatan indeks yang sangat tajam hingga mendekati level 200, selain itu terjadi tren peningkatan hingga mendekati akhir tahun dan mengalami tren penurunan hingga mendekati pertengahan tahun 2020

* Pada tahun 2020 terjadi peningkatan hingga mengalami penurunan secara dalam mendekati akhir tahun kemudian mulai meningkat di akhir tahun

* Pada tahun 2021 terdapat tren peningkatan hingga pertengahan tahun kemudian mengalami penurunan dan peningkatan di akhir tahun. Meskipun begitu, tingkat indeks dan fluktuasi di tahun 2021 lebih rendah dibandingkan dengan tahun-tahun sebelumnya

e. Analisis Komponen SO<sub>2</sub>

![Nilai ISPU SO2](https://cdn.discordapp.com/attachments/1121095008926302358/1121109254913413150/so2.png)

**Berdasarkan diagram SO2 berikut**

* Dari 2010 hingga 2012 terjadi tren peningkatan indeks SO2.

* Pada akhir tahun 2012, terjadi penurunan hingga awal tahun 2013

* Meskipun awal tahun 2013 pergerakan indeks bersifat stagnan, namun perlahan terjadi peningkatan nilai indeks hingga mendekati akhir tahun, setelah itu terjadi penurunan hingga awal tahun 2014

* Pada tahun 2014 kembali terjadi tren peningkatan. Peningkatan paling pesat terjadi pada bulan April dan mulai mengalami penurunan di akhir tahun

* Pada tahun 2015 terjadi peningkatan yang cukup pesat, terutama di bulan April dan pali besar terjadi di bulan Juni hingga Oktober, setelah itu terjadi penurunan dan sempat meningkat di awal Desember yang setelah itu kembali stagnan hingga akhir tahun

* Pada awal tahun 2016 terjadi peningkatan yang sangat tajam dan mulai menurun di pertengahan bulan Febuari. Pada bulan Maret hingga April, indeks mengalami stagnasi dan mulai April pertengahan mengalami tren kenaikan secara perlahan hingga tahun 2017 awal

* Pada awal tahun 2017, grafik terputus yang disebabkan indeks SO2 di tanggal tersebut tidak tercatat, namun bisa terlihat dari data-data berikutnya, posisi indeks berada lebih rendah dibandingkan indeks di awal tahun. Kemungkinan di antara tanggal dimana indeks SO2 tidak tercatat, telah terjadi tren penurunan indeks.

* Di bulan Febuari 2017 kembali terjadi tren peningkatan indeks SO2 dan mengalami perlambatan sejak di pertengahan November, namun tetap terjadi peningkatan indeks hingga akhir tahun

* Pada tahun 2018, peningkatan indeks tetap terus terjadi hingga mengalami penurunan di pertengahan tahun, kemudian kembali terjadi peningkatan hingga pada akhir tahun terjadi penurunan

* Pada tahun 2019, indeks tetap bergerak naik dan pada bulan Maret akhir terjadi penurunan yang cukup besar. Setelah penurunan, indeks tetap stagnan di dibawah level 20 ISPU hingga mengalami peningkatan kembali di awal Juli. Tren ini terus berlangsung meskipun bergerak lambat hingga awal tahun 2020

* Pada tahun 2020 terjadi lonjakan kenaikan indeks SO2 hingga melampaui level 60 ISPU. Setelah itu terjadi tren penurunan hingga pertengahan bulan dan mulai meningkat hingga terjadi peningkatan yang sangat tajam di bulan November dan menurun hingga awal Desember. Setelah itu indeks kembali mulai stagnasi hingga akhir tahun

* Pada tahun 2021 indeks bergerak menurun kemudian kembali naik dengan cukup cepat hingga pada akhir tahun, indeks sudah menyentuk di level antara level 40 dan 60 ISPU

f. Analisis Komponen NO<sub>2</sub>

![Nilai ISPU NO2](https://cdn.discordapp.com/attachments/1121095008926302358/1121109255643209828/no2.png)

**Berdasarkan diagram NO2 berikut**

* Pada tahun 2010 hingga 2015, pergerakan indeks NO2 mengalami satu tren yang sama dimana indeks akan meningkat hingga pertengahan tahun dan mengalami penurunan di akhir dan awal tahun berikutnya

* Pada tahun 2015 akhir terjadi penurunan yang signifikan sehingga pada akhir tahun 2015 hingga pertengahan Januari 2017, indeks bergerak stagnan mendekati level 5 ISPU

* Kemudian terjadi peningkatan secara perlahan hingga di Oktober-November 2017 terjadi penurunan dan kembali stagnan hingga akhir 2019

* Setelah itu terjadi peningkatan yang cukup drastis hingga pertengahan tahun 2019. Setelah itu terjadi stagnasi dan kembali menurun mendekati akhir tahun

* Pada tahun 2020, terjadi peningkatan di awal tahun dan terjadi stagnasi hingga secara perlahan menurun di akhir Maret

* Setelah memasuki bulan Maret 2020, terjadi peningkatan secara lambat hingga terjadi puncaknya dimana pergerakan indeks meningkat drastis di akhir Oktober dan November 2020. Indeks kembali menurun dengan tajam di akhir November dan penurunan melambat hingga mendekati akhir tahun.

* Di akhir tahun 2020, indeks bergerak naik hingga mencapai puncaknya di Juni 2021, kemduian menurun di bulan Juli dan perlahan naik hingga akhir Oktober.

* Setelah itu terjadi penurunan yang tajam, dan tidak lama berselang terjadi fluktuasi yang tajam hingga kembali turun dan perlahan memulai tren kenaikan indeks di akhir tahun

g. Analisis Komponen CO

![Nilai ISPU CO](https://cdn.discordapp.com/attachments/1121095008926302358/1121109255253135500/co.png)

**Berdasarkan diagram CO berikut**

* Berdasarkan data di tahun 2010 hingga 2015, indeks CO mengalami tren kenaikan dan penurunan secara rutin dengan detail sebagai berikut

	* Sejak 2010, indeks CO mengalami tren peningkatan dan beberapa bulan kemudian, indeks perlahan mengalami penurunan hingga di pertengahan tahun 2011

	* Setelah pertengahan tahun 2011, indeks mengalami peningkatan yang lambat hingga awal tahun 2012

	* Di tahun 2012, indeks mengalami fluktuatif dimana di separuh pertama tahun menglami penurunan sebanyak dua kali, kemudian di bulan Agustus mengalami penurunan paling rendah, setelah itu kembali meningkat hingga pengalami penurunan kembali di Desember

	* Di tahun 2013 diawali dengan peningkatan indeks yang cukup besar, kemudian dilanjutkan dengan fluktuatifnya indeks dimana terjadi kenaikan yang paling besar di pertengahan bulan diikuti dengan penurunan yang tajam setelahnya. Setelah itu indeks berangsur-angsur menaik walaupun pergerakannya sangat fluktuatif hingga akhir tahun

	* Indeks mengalami penurunan paling besar di akhir tahun 2014 dan awal tahun 2015, akhir April dan awal Bulan Mei 2015 dan bulan Agustus 2015

	* Indeks mulai menurun di akhir tahun 2015

* Bedasarkan data di tahun 2016 hingga 2021, pergerakan indeks CO tidak sebesar di _range_ waktu sebelumnya dengan detail sebagai berikut

	* Di awal tahun 2016, indeks mengalami peningkatan yang konsisten dan sempat melewati level 50 ISPU. Namun setelah itu, indeks tidak pernah melewati level 50 ISPU dan sejak mendekati akhir tahun, indeks bergerak menurun hingga akhir tahun

	* Di tahun 2017, indeks kembali menaik, meskipun tidak sebesar tahun sebelumnya namun setelahnya indeks justru semakin menurun. Peningkatan sempat kembali terjadi di pertengahan September, meskipun peningkatannya sangat fluktuatif. Di bulan November, indeks perlahan menurun dan mulai berada di rata-rata level di bawah 25 ISPU hingga akhir tahun

	* Di tahun 2018, tren serupa kembali terjadi, namun di tahun tersebut, tingkat penurunan indeksnya lebih besar dan lebih lama dibandingkan dengan tahun lalu

	* Di tahun 2019, indeks kembali mengalami apa yang terjadi di dua tahun sebelumnya dimana di awal tahun mengalami peningkatan yang peningkatan kemudian di pertengahan tahun mengalami penurunan. Namun di tahun ini, terjadi peningkatan cukup konsisten di akhir tahun hingga puncaknya terjadi di awal tahun 2020

	* Di awal tahun 2020, indeks pengalami puncak kenaikannya sejak akhir tahun lalu, dan kemudian melandai dengan cukup dalam di pertengahan tahun, meskipun sempat mengalami peningkatan yang drastis menjelang akhir tahun, namun indeks kembali menurun di bawah level 10 ISPU hingga akhir tahun.

	* Di tahun 2021, indeks mengalmi kenaikan, meskipun begitu indeks bergerak sangat fluktuatif rata-rata berada di _range_ 10 hingga 25 ISPU, dan setelah itu mengalami penurunan rata-rata nya di pertengahan tahun hingga akhir tahun mengalami tren kenaikan

h. Analisis _Skewness_

![skew pm10](https://media.discordapp.net/attachments/1121095008926302358/1121111116513284216/skew1.png?width=1440&height=627)

![skew so2](https://media.discordapp.net/attachments/1121095008926302358/1121111116945309716/skew2.png?width=1440&height=627)

![skew co](https://media.discordapp.net/attachments/1121095008926302358/1121111117389901945/skew3.png?width=1440&height=627)

![skew o3](https://media.discordapp.net/attachments/1121095008926302358/1121111117998067742/skew4.png?width=1440&height=627)

![skew no2](https://media.discordapp.net/attachments/1121095008926302358/1121111118367178782/skew5.png?width=1440&height=627)

Berdasarkan histogram berikut, seluruh histogram selain Histogram PM10 dan PM2.5 memiliki distribusi positif dimana _tail_ kanan lebih panjang dibandingkan _tail_ kiri dimanai skor skew rata-rata berada diluar range -0.5 sampai 0.5.

##### 3.2. Analisa ISPU DKI 2 (Kelapa Gading)

a. Analisis nilai ISPU

|       |      pm10 |       so2 |        co |        o3 |        no2 |     pm25 |
|:------|----------:|----------:|----------:|----------:|-----------:|---------:|
| count | 3904      | 3971      | 3992      | 3983      | 3998       | 349      |
| mean  |   55.3463 |   20.3986 |   18.5521 |   76.4346 |   15.1368  |  76.6476 |
| std   |   16.8321 |   14.1851 |    9.6382 |   45.9389 |    7.67406 |  20.0017 |
| min   |   10      |    1      |    1      |    3      |    2       |  29      |
| 25%   |   45      |   11      |   12      |   47      |   11       |  61      |
| 50%   |   58      |   17      |   16      |   64      |   14       |  79      |
| 75%   |   67      |   25      |   23      |   90      |   18       |  90      |
| max   |  116      |  103      |   75      |  314      |  148       | 129      |


Berdasarkan tabel diatas

* Kandungan O3 mendominasi dengan nilai ISPU rata-rata sebesar 76.47 dengan nilai maksimum 314

* Kandungan PM10 menempati urutan kedua dengan nilai ISPU rata-rata 55.20 dengan nilai maksimum 116

* Kandungan SO2 menempati urutan ketiga dengan nilai ISPU rata-rata 20.44 dengan nilai maksmimum 103

* Kandungan CO menempati urutan keempat dengan nilai ISPU rata-rata sebesar 18.50 dengan nilai maksimum 75

* Kandungan NO2 menempati urutan terakhir dengan nilai ISPU rata-rata 15.09 dan nilai maksimum 148

* Kandungan PM25 memiliki nilai ISPU rata-rata sebesar 76.65 dengan nilai maksimum 129

* Secara angka, komponen PM25 menempati urutan tertinggi walaupun pengukurannya dimulai di tahun 2021 (Penjelasan lengkap akan dibahas di segmen Pengukuran PM2.5)

b. Analisis _Missing Value_ dan _Zero Value_ serta _range_ tanggal

| Tipe | pm10 | so2 |  co |  o3 | no2 |
|------|:----:|:---:|:---:|:---:|:---:|
| NaN  |  121 | 61 | 40 | 49 | 34 |
| Zero |   0  |  0 |  0 |  0  |  0  |

    Range tanggal pada data stasiun 
    2010-11-04 00:00:00 2021-12-31 00:00:00
    

**Berdasarkan hasil analisis _Missing Value_, _Zero Value_ serta tanggal _Range_ berikut**

* Data dari DKI2 dicatat mulai dari tanggal 04 November 2010 hingga 31 Desember 2021

* Secara total, terdapat 312 Data NaN dimana PM10, SO2, dan O3 merupakan komponen udara yang paling banyak data NaN

* Selain itu, seluruh nilai data > 0

c. Analisis Komponen PM<sub>10</sub>

![Nilai ISPU PM10](https://cdn.discordapp.com/attachments/1121095008926302358/1121249724356366477/pm10.png)

**Berdasarkan diagram PM10 berikut**

* Dari tahun 2010 akhir hingga 2012, terdapat _tren_ dimana dari awal tahun terjadi kenaikan indeks hingga pertengahan tahun, kemudian disusul dengan penurunan hingga akhir tahun

* Namun, mulai dari tahun 2013 hingga 2015, dimana terjadi penurunan di pertengahan tahun dimana penurunan tersebut cukup dalam, namun akan kembali naik dan akan menurun di akhir tahun.

* Sejak tahun 2016, pergerakan sangat _seasonial_ dan mirip dengan situasi sebelum tahun 2013

d. Analisis Komponen O<sub>3</sub>

![Nilai ISPU O3](https://cdn.discordapp.com/attachments/1121095008926302358/1121249725933436968/o3.png)


**Berdasarkan diagram O3 berikut**

* Dari akhir tahun 2010 hingga mendekati akhir tahun 2012, terjadi tren peningkatan indeks O3, meskipun sempat menurun di awal tahun 2012 dan pertengahan tahun 2012, namun secara garis besar, tren bergerak menaik

* Setelah itu tren bergerak turun hingga memasuki tahun 2013 dimana hingga tahun 2015 terdapat tren dimana akan terjadi kenaikan sebanyak 2 kali di mendekati dan setelah pertengahan tahun, dan akan menurun di pertengahan tahun dan akhir tahun

* Di tahun 2016, pergerakan terlihat sangat berfluktuatif, meskipun di awal dan akhir tahun terjadi penurunan

* Di tahun 2017 hingga 2019, terdapat tren pergerakan dimana indeks akan bergerak naik hingga pertengahan tahun dan akan turun hingga akhir tahun

* Pada tahun 2018, tren terlihat berbeda dimana kenaikannya paling tinggi hingga beberapa kali melewati batas 200 ISPU

* Di tahun 2020, indeks bergerak mirip dengan di tahun 2016, namun terjadi penurunan paling dalam mendekati akhir tahun 2020

* Di tahun 2021, indeks bergerak stagnan setelah awal tahun mengalami penurunan

e. Analisis Komponen SO<sub>2</sub>

![Nilai ISPU SO2](https://cdn.discordapp.com/attachments/1121095008926302358/1121249724800974878/so2.png)


**Berdasarkan diagram SO2 berikut**

* Sejak akhir tahun 2010 hingga 2017, pergerakan bergerak secara _seasional_ dimana indeks akan bergerak naik dan akan turun mendekati akhir tahun

* Di tahun 2018, indeks justru menurun dan stagnan mendekati pertengahan tahun hingga akhir tahun

* Di tahun 2019, indeks kembali menurun setelah awal tahun dan bergerak stagnan dan tidak sefluktuatif di tahun sebelumnya

* Di tahun 2020, indeks mulai bergerak mirip seperti sebelum tahun 2018, namun pergerakan mendekati akhir tahun mengalami peningkatan sangat tinggi, setelah itu kembali jatuh dan bergerak menurun di awal tahun berikutnya

* Di tahun 2021, meskipun masih sangat fluktuatif seperti tahun lalu dan pergerakan naiknya cukup tajam, namun pola yang dibentuk mulai mendekati seperti pola sebelum tahun 2018, meskipun sempat mengalami penurunan yang sangat tajam mendekati akhir tahun

f. Analisis Komponen NO<sub>2</sub>

![Nilai ISPU NO2](https://cdn.discordapp.com/attachments/1121095008926302358/1121249725576904754/no2.png)


**Berdasarkan diagram NO2 berikut**

* Pergerakan indeks sejak 2010 akhir hingga 2019 pertengahan mengalami stagnasi dimana tidak terlihat terjadinya tren kenaikan atau penurunan secara garis besar

* Pada tahun 2019 hingga pertengahan 2020, indeks mulai bergerak menurun meskipun lambat dan tidak terlalu besar

* Mendekati pertengahan tahun 2020, indeks mulai bergerak naik dan setelahnya mengalami kenaikan yang signifikan hingga menembus level 140 ISPU, setelah itu indeks turun dengan tajam

* Di akhir tahun 2020 hingga 2021, indeks mulai menunjukan pergerakan menaik secara perlahan, hingga indeks telah melewati level 40 ISPU

g. Analisis Komponen CO

![Nilai ISPU CO](https://cdn.discordapp.com/attachments/1121095008926302358/1121249725161672735/co.png)


**Berdasarkan diagram CO berikut**

* Berdasarkan data tahun 2011 hingga 2015 terdapat pola dimana di akhir dan awal tahun berikutnya terjadi peningkatan indeks, selain itu indeks juga meningkat mendekati pertengahan bulan atau awal bulan

* Peningkatan terbesar terjadi di awal tahun 2015

* Pada tahun 2016, indeks bergerak sedikit berbeda dimana terjadi fluktuasi, dan mengalami penurunan di akhir tahun

* Pada awal tahun 2017, indeks menurun dan mulai mengalami pola yang terjadi sebelum tahun 2015

* Sejak tahun 2018 hingga 2021, pola bergerak dimana sempat mengalami peningkatan di awal tahun dan menurun di pertengahan tahun, kemudian meningkat di akhir tahun, namun di tahun 2021, pergerakan tidak sefluktuatif di tahun-tahun sebelumnya

h. Analisis _Skewness_

![skew pm10](https://cdn.discordapp.com/attachments/1121095008926302358/1121249830942031892/skew_pm10.png)

![skew so2](https://cdn.discordapp.com/attachments/1121095008926302358/1121249831248207882/skew_so2.png)

![skew co](https://cdn.discordapp.com/attachments/1121095008926302358/1121249831483084930/skew_co.png)

![skew o3](https://cdn.discordapp.com/attachments/1121095008926302358/1121249832011571260/skew_o3.png)

![skew no2](https://cdn.discordapp.com/attachments/1121095008926302358/1121249831768309850/skew_no2.png)

Berdasarkan histogram berikut, seluruh histogram selain Histogram PM10 dan PM2.5 memiliki distribusi positif dimana _tail_ kanan lebih panjang dibandingkan _tail_ kiri dimanai skor skew rata-rata berada diluar range -0.5 sampai 0.5.

##### 3.3. Analisa ISPU DKI 3 (Jagaraksa)

a. Analisis nilai ISPU

|       |      pm10 |       so2 |        co |        o3 |        no2 |     pm25 |
|:------|----------:|----------:|----------:|----------:|-----------:|---------:|
| count | 3772      | 3833      | 3927      | 3902      | 3762       | 358      |
| mean  |   43.1927 |   15.9371 |   19.974  |   69.0495 |    8.96624 |  74.2402 |
| std   |   18.3598 |   12.9009 |   11.2547 |   33.1326 |    6.46116 |  23.1405 |
| min   |    2      |    0      |    1      |    4      |    1       |  13      |
| 25%   |   27      |    7      |   12      |   43      |    6       |  62      |
| 50%   |   46      |   13      |   18      |   69      |    8       |  76.5    |
| 75%   |   57      |   19      |   25      |   90      |   11       |  89      |
| max   |  118      |  112      |   98      |  274      |  107       | 132      |



Berdasarkan tabel diatas

* Kandungan O3 mendominasi dengan nilai ISPU rata-rata sebesar 69.01 dengan nilai maksimum 118

* Kandungan PM10 menempati urutan kedua dengan nilai ISPU rata-rata 43.55 dengan nilai maksimum 274

* Kandungan CO menempati urutan ketiga dengan nilai ISPU rata-rata 19.94 dengan nilai maksmimum 98

* Kandungan SO2 menempati urutan keempat dengan nilai ISPU rata-rata sebesar 15.74 dengan nilai maksimum 112

* Kandungan NO2 menempati urutan terakhir dengan nilai ISPU rata-rata 8.79 dan nilai maksimum 107

* Kandungan PM25 memiliki nilai ISPU rata-rata sebesar 74.24 dengan nilai maksimum 132

* Secara angka, komponen PM25 menempati urutan tertinggi walaupun pengukurannya dimulai di tahun 2021 (Penjelasan lengkap akan dibahas di segmen Pengukuran PM2.5)

b. Analisis _Missing Value_ dan _Zero Value_ serta _range_ tanggal

| Tipe | pm10 | so2 |  co |  o3 | no2 |
|------|:----:|:---:|:---:|:---:|:---:|
| NaN  |  208 | 147 | 53 | 78 | 218 |
| Zero |   0  |  30 |  0 |  0  |  0  |

    Range tanggal pada data stasiun 
    2010-11-07 00:00:00 2021-12-31 00:00:00
   

**Berdasarkan hasil analisis _Missing Value_, _Zero Value_ serta tanggal _Range_ berikut**

* Data dari DKI3 dicatat mulai dari tanggal 07 November 2010 hingga 31 Desember 2021

* Secara total, terdapat 704 Data NaN dimana PM10, SO2, dan O3 merupakan komponen udara yang paling banyak data NaN

* Selain itu, seluruh nilai data > 0 kecuali SO2 dimana terdapat 30 data yang bernilai 0

c. Analisis Komponen PM<sub>10</sub>

![Nilai ISPU PM10](https://cdn.discordapp.com/attachments/1121095008926302358/1121251757851410472/pm10.png)

**Berdasarkan diagram PM10 berikut**

* Nilai PM10 mengalami tren penurunan dimulai di akhir 2012 hingga akhir 2015

* Terjadi peningkatan mulai tahun 2016 dan berada di puncaknya di tahun 2017

* Setelah itu terjadi penurunan di akhir tahun 2017 hingga merangkak naik di awal tahun 2018

* Sejak 2018, nilai ISPU PM10 mengalami tren _seasonial_ hingga akhir 2021

* Sejak tahun 2016, pergerakan sangat _seasonial_ dan mirip dengan situasi sebelum tahun 2013

d. Analisis Komponen O<sub>3</sub>

![Nilai ISPU O3](https://cdn.discordapp.com/attachments/1121095008926302358/1121251758224707584/o3.png)

**Berdasarkan diagram O3 berikut**

* Nilai O3 umumnya mengalami tren penurunan menjelang akhir tahun hingga awal tahun berikutnya.

* Berdasarkan data tahun 2010 hingga 2015

	* Nilai O3 mencapat puncaknya di bulan November 2010 dan Oktober - November 2012

	* Penurunan nilai O3 cukup drastis terjadi akhir tahun 2014, awal dan akhir tahun 2015

* Berdasarkan data tahun 2016 hingga 2021

	* Pola musiman dimana setiap akhir dan awal tahun, kadar O3 menurun terap terjadi

	* Meskipun begitu, penurunan di akhir tahun 2018 hingga awal tahun 2019 tidak sebesar tahun-tahun sebelumnya

	* Terjadi penurunan kadar O3 secara drastis sejak akhir tahun 2020 hingga akhir tahun 2021

	* Meskipun sempat terjadi lonjakan yang cukup tajam di sekitar pertengahan tahun 2021

	* Terjadinya penurunan kadar O3 secara drastis sejak akhir tahun 2020 bertepatan kebijakan PSBB total dan PPKM yang berlaku di Jakarta waktu itu.

e. Analisis Komponen SO<sub>2</sub>

![Nilai ISPU SO2](https://media.discordapp.net/attachments/1121095008926302358/1121251758564454480/so2.png)

**Berdasarkan diagram SO2 berikut**

* Adanya pola _seasional_ yang terjadi dari Desember 2010 hingga pertengahan 2017

* Selain itu sejak tahun 2010 hingga 2014, nilai ISPU SO2 mengalami tren penurunan hingga awal tahun berikutnya.

* Berdasarkan data dari tahun 2010 hingga 2015

	* Secara perlahan dan pasti, nilai ISPU SO2 mengalami peningkatan.

	* Puncak nilai SO2 berada di tahun 2014 dan 2015, terutama menjelang akhir tahun.

	* Pada tahun 2015, nilai SO2 tetap tinggi hingga akhir tahun

* Berdasarkan data dari tahun 2016 hingga 2021

	* Tren peningkatan SO2 sempat menurun di sekitar Febuari dan Maret 2016, dan secara perlahan merangkak naik hingga tahun 2017 pertengahan

	* Setelah itu, nilai SO2 menurun drastis dan berikutnya secara berangsur menurun hingga mengalami peningkatan secara perlahan di tahun 2020 awal hingga pertengahan

	* Setelah sempat mengalami penurunan di pertengahan tahun 2020, nilai SO2 mengalami peningkatan secara tajam, terutama mendekati akhir tahun 2020.

	* Meski sempat menurun di akhir tahun 2020 dan awal tahun 2021, nilai SO2 mengalami peningkatan hingga mendekati pertengahan tahun, dan kembali meningkat setelah sempat mengalami penurunan yang cukup besar hingga akhir tahun.

f. Analisis Komponen NO<sub>2</sub>

![Nilai ISPU NO2](https://media.discordapp.net/attachments/1121095008926302358/1121251759235534928/no2.png)


**Berdasarkan diagram NO2 berikut**

* Terdapat pola _seasional_ dimana nilai NO2 akan mengalami penurunan di setiap akhir hingga awal tahun berikutnya.

* Meskipun begitu, ada beberapa hari yang tidak tercatat oleh stasiun pemantauan, terutama di akhir tahun 2013 hingga awal tahun 2014

* Berdasarkan data dari tahun 2010 hingga 2015

	* Kadar NO2 umumnya mengalami peningkatan di pertengahan tahun, kecuali di tahun 2014 dan 2015

	* Pada tahun 2014 dan 2015, kadar NO2 mengalami peningkatan menjelang dan akhir pertengahan tahun

* Berdasarkan data dari tahun 2016 hingga 2021

	* Meskipun membentuk pola yang mirip dengan _range_ tahun 2010 hingga 2015, namun pola di _range_ ini sedikit berfluaktif

	* Pada akhir pertengahan 2016, nilai NO2 sempat mengalami peningkatan hingga nilai ISPU melewati 20.

	* Sedangkan pada tahun 2020, terjadi peningkatan indeks NO2 yang sangat drastis hingga melewati ISPU 100

g. Analisis Komponen CO

![Nilai ISPU CO](https://media.discordapp.net/attachments/1121095008926302358/1121251759650779136/co.png)


**Berdasarkan diagram CO berikut**

* Indeks CO mengalami peningkatan yang cukup tajam di awal tahun 2011 dan kembali menurun menjelang pertengahan tahun 2011

* Kemudian sejak pertengahan tahun 2012, nilai indeks mengalami tren penurunan hingga pertengahan tahun 2013

* Namun Indeks CO mengalami peningkatan yang cukup besar sejak pertengahan tahun 2013

* Indeks CO kembali mengalami penurunan sejak awal tahun 2016 hingga pertengahan tahun 2017

* Setelah itu indeks CO perlahan naik hingga berada di puncaknya di awal tahun 2020

* Setelah itu tren penurunan kembali terjadi dan mengalami stagnansi sejak akhir tahun 2020 hingga akhir tahun 2021

h. Analisis _Skewness_

![skew pm10](https://media.discordapp.net/attachments/1121095008926302358/1121251916710678639/skew_pm10.png)

![skew so2](https://media.discordapp.net/attachments/1121095008926302358/1121251917461454968/skew_so2.png)

![skew co](https://media.discordapp.net/attachments/1121095008926302358/1121251918161903727/skew_co.png)

![skew o3](https://media.discordapp.net/attachments/1121095008926302358/1121251917092376576/skew_o3.png)

![skew no2](https://media.discordapp.net/attachments/1121095008926302358/1121251917864128592/skew_no2.png)

Berdasarkan histogram berikut, seluruh histogram selain Histogram PM10 dan PM2.5 memiliki distribusi positif dimana _tail_ kanan lebih panjang dibandingkan _tail_ kiri dimanai skor skew rata-rata berada diluar range -0.5 sampai 0.5.

##### 3.4. Analisa ISPU DKI 4 (Lubang Buaya)

a. Analisis nilai ISPU

|       |      pm10 |       so2 |        co |        o3 |        no2 |     pm25 |
|:------|----------:|----------:|----------:|----------:|-----------:|---------:|
| count | 3819      | 3840      | 3808      | 3686      | 3871       | 323      |
| mean  |   63.2113 |   20.9719 |   17.8443 |   61.1932 |   11.6143  |  93.1734 |
| std   |   20.896  |   14.2984 |   12.4081 |   29.1168 |    7.89589 |  25.3209 |
| min   |    7      |    0      |    0      |    5      |    1       |  33      |
| 25%   |   52      |    7      |   10      |   39      |    8       |  77      |
| 50%   |   62      |   22      |   15      |   60      |   10       |  93      |
| 75%   |   74      |   31      |   22      |   79      |   14       | 108      |
| max   |  179      |   72      |  134      |  236      |  107       | 174      |

Berdasarkan tabel diatas

* Kandungan PM10 mendominasi dengan nilai ISPU rata-rata sebesar 63.13 dengan nilai maksimum 179

* Kandungan O3 menempati urutan kedua dengan nilai ISPU rata-rata 60.97 dengan nilai maksimum 236

* Kandungan SO2 menempati urutan ketiga dengan nilai ISPU rata-rata sebesar 20.76 dengan nilai maksimum 72

* Kandungan CO menempati urutan keempat dengan nilai ISPU rata-rata 17.61 dengan nilai maksmimum 134

* Kandungan NO2 menempati urutan terakhir dengan nilai ISPU rata-rata 12.30 dan nilai maksimum 107

* Kandungan PM25 memiliki nilai ISPU rata-rata sebesar 93.17 dengan nilai maksimum 174

* Secara angka, komponen PM25 menempati urutan tertinggi walaupun pengukurannya dimulai di tahun 2021 (Penjelasan lengkap akan dibahas di segmen Pengukuran PM2.5)

b. Analisis _Missing Value_ dan _Zero Value_ serta _range_ tanggal

| Tipe | pm10 | so2 |  co |  o3 | no2 |
|------|:----:|:---:|:---:|:---:|:---:|
| NaN  |  155 | 134 | 166 | 288 | 103 |
| Zero |   0  |  0 |  25 |  12  |  0  |

    Range tanggal pada data stasiun 
    2010-11-04 00:00:00 2021-12-31 00:00:00
    
**Berdasarkan hasil analisis _Missing Value_, _Zero Value_ serta tanggal _Range_ berikut**

* Data dari DKI4 dicatat mulai dari tanggal 04 November 2010 hingga 31 Desember 2021

* Secara total, terdapat 846 Data NaN dimana O3, CO, dan PM10 merupakan komponen udara yang paling banyak data NaN

* Selain itu, seluruh nilai data > 0 kecuali SO2 dimana terdapat 25 data dan CO sebanyak 12 data yang bernilai 0

c. Analisis Komponen PM<sub>10</sub>

![Nilai ISPU PM10](https://media.discordapp.net/attachments/1121095008926302358/1121252108411355166/pm10.png)

**Berdasarkan diagram PM10 berikut**

* Indeks PM10 mengalami tren penurunan setiap akhir tahun dan awal tahun. Tren tersebut terjadi hampir di setiap tahunnya

* Indeks PM10 mengalami tren peningkatan setiap menjelang dan pertengahan tahun

* Peningkatan yang besar terjadi di tahun 2011, 2012, 2019 dan 2020

* Peningkatan PM10 di tahun 2020 terjadi justru di awal tahun

* Indeks PM10 mengalami penurunan yang sangat drastis di tahun 2021

d. Analisis Komponen O<sub>3</sub>

![Nilai ISPU O3](https://media.discordapp.net/attachments/1121095008926302358/1121252108751077386/o33.png)

**Berdasarkan diagram O3 berikut**

* Secara umum, kadar O3 mengalami penurunan di akhir dan awal tahun

* Pada akhir tahun 2013 hingga awal tahun 2014 indeks O3 mengalami peningkatan

* Pada akhir tahun 2014, indeks sempat meningkat tajam hingga melewati 200 sebelum kembali turun dengan tajam dibawah 50

* Pada tahun 2019, indeks mengalami tren peningkatan yang cukup panjang sejak mendekati pertengahan tahun hingga akhir tahun.

* Pada awal tahun 2020, indeks meningkat dengan tajam sebelum mengalami penurunan yang cukup besar sejak pertengahan hingga akhir tahun

* Pada tahun 2021, indeks stagnan dan rata-rata berada dibawah 50, walaupun mendekati akhir tahun sempat meningkat hingga hampir melewati 75

e. Analisis Komponen SO<sub>2</sub>

![Nilai ISPU SO2](https://media.discordapp.net/attachments/1121095008926302358/1121252109837418599/so2.png)

**Berdasarkan diagram SO2 berikut**

* Terjadi tren peningkatan indeks SO2 sejak tahun 2013 hingga awal tahun 2016 sebelum terjadi penurunan

* Setelah penurunan, tren kembali meningkat hingga mendekati akhir tahun 2017 sebelum terjadi penurunan ke level dibawah 30

* Pada awal tahun 2018, indeks mengalami peningkatan sangat tajam hingga melewati level 70, kemudian mengalami penurunan secara tajam hingga dibawah level 10.

* Namun indeks SO2 mengalami peningkatan hingga mendekati akhir tahun 2018.

* Sejak tahun 2019, indeks SO2 mengalami peningkatan dan akan turun di akhir tahun atau awal tahun berikutnya. hal tersebut terjadi terus menerus hingga akhir tahun 2021

f. Analisis Komponen NO<sub>2</sub>

![Nilai ISPU NO2](https://media.discordapp.net/attachments/1121095008926302358/1121252110734983210/no2.png)

**Berdasarkan diagram NO2 berikut**

* Melihat dari data indeks NO2 di tahun 2010 hingga 2019 akhir, indeks NO2 berada di posisi stagnan dimana tidak terlalu banyak peningkatan indeks secara signifikan dan rata-rata kenaikan tertinggi berada di level 30

* Pada akhir tahun 2019, indeks NO2 mengalami penurunan dibandingkan tahun sebelumnya

* Namun, pada tahun 2020, terjadi 2 kali peningkatan indeks NO2 secara drastis, dimana pada bulan Maret terjadi peningkatan di level indeks 70, kemudian pada bulan Oktober, terjadi peningkatan yang sangat signifikan yaitu melewati level index 100 dan setelah memasuki bulan November, indeks menurun ke level mendekati seperti di bulan Januari

* Memasuki tahun 2021, indeks NO2 perlahan mengalami kenaikan dan di akhir tahun 2021 indeks perlahan menurun walaupun mendekati akhir tahun kembali meningkat

g. Analisis Komponen CO

![Nilai ISPU CO](https://media.discordapp.net/attachments/1121095008926302358/1121252111116669008/co.png)

**Berdasarkan diagram CO berikut**

* Indeks CO mengalami peningkatan besar di awal dan menjelang akhir tahun 2012, pertengahan akhir tahun 2016, awal tahun 2020 dan akhir tahun 2020

* Penurunan indeks CO yang besar terjadi di pertengahan tahun 2012, menjelang akhir tahun 2014 dan pertengahan hingga akhir tahun 2016

* Pada tahun 2021, pergerakan indeks CO tidak terlalu fluaktif seperti di tahun-tahun sebelumnya dimana rata-rata indeks CO di tahun 2021 adalah 12.15

h. Analisis _Skewness_

![skew pm10](https://media.discordapp.net/attachments/1121095008926302358/1121252236564115577/skew_pm10.png)

![skew so2](https://media.discordapp.net/attachments/1121095008926302358/1121252237126139914/skew_so2.png)

![skew co](https://media.discordapp.net/attachments/1121095008926302358/1121252238170542090/skew_co.png)

![skew o3](https://media.discordapp.net/attachments/1121095008926302358/1121252236811587654/skew_o3.png)

![skew no2](https://media.discordapp.net/attachments/1121095008926302358/1121252237394587678/skew_no2.png)

Berdasarkan histogram berikut, seluruh histogram selain Histogram SO2 dan PM2.5 memiliki distribusi positif dimana _tail_ kanan lebih panjang dibandingkan _tail_ kiri dimanai skor skew rata-rata berada diluar range -0.5 sampai 0.5.

Meskipun begitu, pada Histogram SO2 ada 2 titik puncak dimana titik puncak tertinggi berada pada range 0-10.

##### 3.5. Analisa ISPU DKI 5 (Kebon Jeruk)

a. Analisis nilai ISPU

|       |      pm10 |        so2 |        co |        o3 |       no2 |     pm25 |
|:------|----------:|-----------:|----------:|----------:|----------:|---------:|
| count | 3112      | 3116       | 3184      | 3139      | 3187      | 330      |
| mean  |   51.1372 |   14.4111  |   23.6146 |   70.4075 |   11.5237 |  78.8212 |
| std   |   17.9188 |    8.57302 |   16.3169 |   41.6352 |   10.7754 |  21.1058 |
| min   |    2      |    0       |    1      |    3      |    1      |  26      |
| 25%   |   41      |    8       |   12      |   38      |    7      |  65      |
| 50%   |   54      |   13       |   19      |   65      |   10      |  78.5    |
| 75%   |   62      |   20       |   32      |   90      |   13      |  91      |
| max   |  114      |   51       |  135      |  243      |  135      | 140      |



Berdasarkan tabel diatas

* Kandungan O3 mendominasi dengan nilai ISPU rata-rata sebesar 67.44 dengan nilai maksimum 243

* Kandungan PM10 menempati urutan kedua dengan nilai ISPU rata-rata 48.56 dengan nilai maksimum 114

* Kandungan CO menempati urutan ketiga dengan nilai ISPU rata-rata sebesar 22.94 dengan nilai maksimum 243

* Kandungan SO2 menempati urutan keempat dengan nilai ISPU rata-rata 13.70 dengan nilai maksmimum 51

* Kandungan NO2 menempati urutan terakhir dengan nilai ISPU rata-rata 11.21 dan nilai maksimum 135

* Kandungan PM25 memiliki nilai ISPU rata-rata sebesar 78.82 dengan nilai maksimum 140

* Secara angka, komponen PM25 menempati urutan tertinggi walaupun pengukurannya dimulai di tahun 2021 (Penjelasan lengkap akan dibahas di segmen Pengukuran PM2.5)

b. Analisis _Missing Value_ dan _Zero Value_ serta _range_ tanggal

| Tipe | pm10 | so2 |  co |  o3 | no2 |
|------|:----:|:---:|:---:|:---:|:---:|
| NaN  |  165 | 161 | 93 | 138 | 90 |
| Zero |   0  |  4 |  0 |  0  |  0  |

    Range tanggal pada data stasiun 
    2012-11-27 00:00:00 2021-12-31 00:00:00
    


**Berdasarkan hasil analisis _Missing Value_, _Zero Value_ serta tanggal _Range_ berikut**

* Data dari DKI5 dicatat mulai dari tanggal 27 November 2012 hingga 31 Desember 2021

* Secara total, terdapat 647 Data NaN dimana PM10, SO2, dan O3 merupakan komponen udara yang paling banyak data NaN

* Selain itu, seluruh nilai data > 0 kecuali SO2 dimana terdapat 4 data yang bernilai 0

* Selain itu, seluruh nilai data > 0

c. Analisis Komponen PM<sub>10</sub>

![Nilai ISPU PM10](https://media.discordapp.net/attachments/1121095008926302358/1121252343590166628/pm10.png)

**Berdasarkan dari diagram PM10 berikut**

* Terjadinya pola _seasional_ dimana ada pola indeks PM10 mengalami kenaikan secara umum di pertengahan tahun dan akan menurun di akhir tahun.

* Meskipun begitu, berdasarkan data di tahun 2012 - 2016, sempat terjadi kenaikan indeks secara besar di sekitaran bulan Febuari dan Maret 2014 dan sekitaran Juni dan Juli 2015.

* Kenaikan tertinggi terjadi di pertengahan tahun 2018 dan sekitaran awal tahun 2019 dimana indeks di awal tahun 2019 sangat dekat dengan level 250

* Indeks PM10 di tahun 2021 berada di posisi paling rendah yaitu dibawah level 50.

* Penurunan indeks PM10 paling dalam terjadi mendekati akhir tahun 2014 hingga awal tahun 2015 dimana indeks turun dari 70-an menjadi dibawah level 20 di awal tahun 2015

d. Analisis Komponen O<sub>3</sub>

![Nilai ISPU O3](https://media.discordapp.net/attachments/1121095008926302358/1121252344626172014/o3.png)

**Berdasarkan dari diagram O3 berikut**

* Pola pada data tahun 2013-2015 cukup berfluaktif

* Sejak dari tahun 2015 hingga 2017, peningkatan O3 terjadi menjelang akhir tahun, walaupun di tahun 2015 terjadi peningkatan O3 di sekitar bulan Maret dan April kemudian perlahan menurun

* Berdasarkan data tahun 2018, terjadi peningkatan indeks O3 di pertengahan tahun

* Berdasarkan data tahun 2019, peningkatan terjadi 2 kali, yaitu di awal tahun dan akhir tahun

* Berdasarkan data tahun 2020

* Peningkatan tertinggi terjadi di akhir bulan Febuari dan berpuncak di tanggal 1 Maret dan mulai menurun sejak pertengahan Maret hingga April

* Sejak akhir September hingga akhir Oktober, terjadi penurunan yang sangat tajam dimana sebelumnya Indeks berada diatas level 100 kemudian menurun di bawah level 50 dan mendekati level 0 ISPU

* Peningkatan kembali terjadi di 1 November dan bergerak melewati level 50 ISPU di beberapa hari kedepannya

* Pergerakan mulai menurun di pertengahan November hingga akhir tahun, namun nilai Indeks tidak serendah seperti di akhir September hingga akhir Oktober

e. Analisis Komponen SO<sub>2</sub>

![Nilai ISPU SO2](https://media.discordapp.net/attachments/1121095008926302358/1121252344949121054/so2.png)


**Berdasarkan dari diagram SO2 berikut**

* Pada tahun 2013 hingga 2014, terjadi sebuah pola dimana sepanjang tahun akan terjadi peningkatan kadar SO2 dan akan menurun secara dalam di bulan November-Desember

* Pola tersebut berubah ketika tahun 2015 dimana indeks SO2 mengalami peningkatan yang pesat sejak April hingga Juni 2015 hingga seterusnya nilai indeks terlihat stagnan hingga akhir tahun

* Pola yang terjadi di tahun 2013 dan 2014 kembali terjadi di tahun 2018 hingga 2020

* Peningkatan indeks SO2 secara tajam terjadi 3 kali, yaitu awal tahun 2018, pertengahan akhir tahun 2018, dan awal pertengahan tahun 2021

* Jika melihat data di antara bulan Mei dan September 2015, terdapat beberapa hari dimana tidak tercatat indeks SO2. Kejadian serupa terjadi di awal pertengahan tahun 2020, sebelum akhirnya nilai indeks sempat naik dan turun, kemudian naik secara perlahan

f. Analisis Komponen NO<sub>2</sub>

![Nilai ISPU NO2](https://media.discordapp.net/attachments/1121095008926302358/1121252345297240074/no2.png)

**Berdasarkan dari diagram NO2 berikut**

* Pergerakan indeks NO2 sejak akhir tahun 2012 hingga 2020, indeks NO2 rata-rata berada di antara 0 hingga 20 ISPU

* Peningkatan indeks yang tajam terjadi di akhir September hingga akhir Oktober 2020 dimana puncak kenaikan berada di pertengahan bulan Oktober

* Berdasarkan data tahun 2021, pergerakan indeks NO2 mengalami fluktuatif dimana peningkatan terbesar terjadi di akhir bulan Juni dan akhir Desember

g. Analisis Komponen CO

![Nilai ISPU CO](https://media.discordapp.net/attachments/1121095008926302358/1121252345687330848/co.png)

**Berdasarkan dari diagram CO berikut**

* Sejak akhir 2012 hingga Juli 2013, indeks CO mengalami fluktuatif kemudian bergerak menurun secara besar di bulan Agustus hingga Desember 2013, kemudian meningkat secara tajam di pertengahan Desember hingga turun mendekati awal tahun 2014

* Dari bulan Juli 2014 hingga awal tahun 2016, indeks rata-rata berada di bawah 40 ISPU, kemudian di bulan berikutnya terjadi peningkatan hingga mengalami tren penurunan di pertengahan tahun 2017 hingga awal tahun 2018

* Setelah itu terjadi peningkatan selama beberapa pulan kemudian menurun dan mulai stagnan hingga mulai pertengahan 2019

* Sejak pertengahan 2019 indeks menurun hingga mendekati akhir 2019 dan mulai meningkat hingga awal tahun 2020

* Di tahun 2020, terdapat peningkatan secara tinggi di bulan Oktober dimana indeks melewati zona 120 ISPU

h. Analisis _Skewness_

![skew pm10](https://media.discordapp.net/attachments/1121095008926302358/1121252445721481226/skew_pm10.png)

![skew so2](https://media.discordapp.net/attachments/1121095008926302358/1121252446665183262/skew_so2.png)

![skew co](https://media.discordapp.net/attachments/1121095008926302358/1121252447273365576/skew_co.png)

![skew o3](https://media.discordapp.net/attachments/1121095008926302358/1121252446359007372/skew_o3.png)

![skew no2](https://media.discordapp.net/attachments/1121095008926302358/1121252446967189564/skew_no2.png)

Berdasarkan histogram berikut, seluruh histogram selain Histogram PM10 dan PM2.5 memiliki distribusi positif dimana _tail_ kanan lebih panjang dibandingkan _tail_ kiri dimanai skor skew rata-rata berada diluar range -0.5 sampai 0.5.

##### 3.6. Analisa PM<sub>2.5</sub> di Seluruh Stasiun

![PM25 DKI 1](https://media.discordapp.net/attachments/1121095008926302358/1121385307254837308/pm25.png)

![PM25 DKI 2](https://media.discordapp.net/attachments/1121095008926302358/1121385307561013348/pm25.png)

![PM25 DKI 3](https://media.discordapp.net/attachments/1121095008926302358/1121385307875594271/pm25.png)

![PM25 DKI 4](https://media.discordapp.net/attachments/1121095008926302358/1121385308177576068/pm25.png)

![PM25 DKI 5](https://media.discordapp.net/attachments/1121095008926302358/1121385308492136458/pm25.png)

Berdasarkan diagram berikut

* Seluruh stasiun memiliki pola pergerakan yang sama dimana indeks akan bergerak naik hingga mencapai puncaknya di bulan Juli awal.

* Setelah itu indeks akan bergerak turun hingga puncaknya di awal Desember

* Setelah itu indeks akan bergerak naik hingga akhir tahun

* Jika kembali melihat hasil rata-rata dan nilai maksimum PM<sub>2.5</sub> di setiap stasiun, bisa dilihat meskipun data PM<sub>2.5</sub> tidak sebanyak data komponen pencemar lainnya, tapi nilai rata-ratanya paling tinggi dibandingkan dengan komponen pencemar lainnya

Salah satu hal yang menjadi catatan adalah pengukuran PM<sub>2.5</sub> baru mulai tersedia **sejak tahun 2021**. Hal ini disebabkan dikarenakan aturan mengenai pengukuran PM<sub>2.5</sub> baru dikeluarkan di bulan Juli 2020 melalui **Peraturan Menteri Lingkungan Hidup dan Kehutanan Nomor P.14/MENLHK/SETJEN/KUM.1/7/2020**. Sebelumnya aturan mengenai Index Standar Pencemaran Udara merujuk kepada **Keputusan Menteri Negara Lingkungan Hidup Nomor KEP-45/MENLH/10/1997** dimana belum ada aturan pengukuran PM<sub>2.5</sub>.

Ditambah berdasarkan Pasal 11 peraturan menteri terbaru tertulis bahwa penyesuaian penentuan ISPU sesuai dengan ketentuan Peraturan Menteri tersebut paling lambat 2 (dua) tahun sejak berlaku, sehingga sangat wajar jika pengukuran PM<sub>2.5</sub> dilakukan di tahun 2021.

#### 4. _Missing Value_

Dalam artikel di **_Towards Data Science_** yang berjudul [**4 Techniques to Handle Missing values in Time Series Data**](https://towardsdatascience.com/4-techniques-to-handle-missing-values-in-time-series-data-c3568589b5a8") terdapat 4 teknik yang dapat digunakan untuk mengatasi _Missing Value_ pada data Time Series, yaitu 

1. _Last Observation Carried Forward (LOCF)_

2. _Next Observation Carried Backward (NOCB)_

3. _Rolling Statistics_

4. _Interpolation_

Dimana teknik _LOCF_ bekerja dengan mengganti nilai yang hilang dengan nilai sebelumnya, sebaliknya _NOCB_ bekerja dengan menggantikannya dengan nilai berikutnya.

Teknik ini sangat simpel, namun memiliki kelemahan dimana akan kehilangan gambaran pergerakan tren, terutama jika nilai yang hilang cukup banyak.

Selain itu, kelemahan _NOCB_ adalah jika setelah nilai yang hilang tersebut adalah NaN juga, maka nilai yang hilang tersebut akan digantikan dengan NaN.

Selain kedua teknik tersebut, terdapat teknik _Rolling Statistics_ yang bekerja dengan menggantikan nilai yang hilang dengan aggregat nilai sebelumnya sebesar _n_ dimana _n_ ini merupakan jarak atau banyak data yang ingin di aggregatkan.

Ada 3 metode untuk menggunakan metode ini, yaitu

a. _Simple Moving Average_

![Simple Moving Average Formula](https://miro.medium.com/v2/resize:fit:640/format:webp/1*GqcyY6_vA-cvcj90Tg6KdA.png)

_Simple Moving Average (SMA)_ merupakan salah satu metode yang paling simpel dimana nilai data sebelumnya yang sebanyak _n_ akan di jumlahkan dan akan di bagikan dengan _n_. Sederhananya, metode ini bekerja dengan mengganti data yang hilang dengan nilai rata-rata data sebelumnya sebesar _n_-data.

b. _Weighted Moving Average_

![Weighted Moving Average Formula](https://miro.medium.com/v2/resize:fit:720/format:webp/1*6PlxApRuwnKzomxEaN1zjw.png)

_Weighted Moving Average (WMA)_ adalah metode lainnya dimana nilai yang akan di jumlahkan akan diberikan sebuah _weigth_ atau bobot dimana bobot ini di distribusikan secara merata sehingga jumlah keseluruhan bobotnya adalah 1 (100%). Contohnya, jika rata-rata yang ingin diambil adalah rata-rata 5 hari sebelumnya, maka bobotnya adalah: **5/15; 4/15; 3/15; 2/15; 1/15** dimana jika dijumlahkan akan menghasilkan 1.

c. _Exponential Moving Average_

![_Exponential Moving Average Formula](https://miro.medium.com/v2/resize:fit:720/format:webp/1*1tmY0vW2LmgAY4ASIWD-5A.png)

_Exponential Moving Average (EMA)_ adalah metode memiliki kerja yang mirip dengan _WMA_, namun jika di _WMA_ penurunan bobotnya konsisten, penurunan pada _EMA_ bersifat eksponensial dimana nilai _alpha_ merupakan nilai _smoothing factor_ mirip seperti penentuan bobot pada _WMA_.

Teknik _Rolling Statistics_ selain dipakai untuk menggantikan data yang hilang, juga digunakan oleh pelaku _trader_ untuk memprediksi harga aset mereka di pasar.

Selain teknik _Rolling Statistics_ ada juga satu teknik lainnya yaitu _Interpolation_. Teknik ini bekerja dengan dengan menggantikan nilai yang hilang dengan mengasumsikan hubungan dalam rentang titik data. Perbedaan dengan teknik sebelumnya adalah pada teknik _Rolling Statistics_ data yang digunakan hanyalah data masa lalu, sedangkan pada teknik interpolasi, data yang digunakan adalah data masa lalu dan masa depan yang sudah diketahui.

Ada 3 variasi dalam teknik interpolasi, yaitu

a. _linear_

Teknik ini bekerja dengan melakukan asumsi hubungan secara linear lurus antar rentang titik data

![Linear Function Graph](https://upload.wikimedia.org/wikipedia/commons/thumb/d/dd/LinearInterpolation.svg/256px-LinearInterpolation.svg.png)

b. _spline_

Teknik ini bekerja dengan memperkirakan nilai yang meminimalisir kelengkungan sehingga memperoleh lengkungan fungsi yang lebih halus.

![Spline Function Graph](https://upload.wikimedia.org/wikipedia/commons/thumb/5/55/Parametic_Cubic_Spline.svg/350px-Parametic_Cubic_Spline.svg.png)

c. _time_

Teknik ini bekerja dengan memperkirakan nilai yang berfokus pada titik terdekatnya.

Pada proyek ini, akan dilakukan penerapan _Spline Interpolation_ dan _time Interpolation_ untuk mengetahui metode mana yang lebih efektif dan dapat meningkatkan akurasi prediksi. Hasil dari penerapan metode tersebut dapat dilihat pada grafik berikut ini untuk setiap stasiun

**Perbandingan (Stasiun DKI 1)**
![Data Original](https://media.discordapp.net/attachments/1121095008926302358/1121428019488243762/ori.png)

![Data Hasil Spline Interpolation](https://media.discordapp.net/attachments/1121095008926302358/1121428019823783977/spline.png)

![Data Hasil Time Interpolation](https://media.discordapp.net/attachments/1121095008926302358/1121428020176093214/time.png)

**Perbandingan (Stasiun DKI 2)**

![Data Original](https://media.discordapp.net/attachments/1121095008926302358/1121428044347871342/ori.png)

![Data Hasil Spline Interpolation](https://media.discordapp.net/attachments/1121095008926302358/1121428044645679154/spline.png)

![Data Hasil Time Interpolation](https://media.discordapp.net/attachments/1121095008926302358/1121428044964433980/time.png)

**Perbandingan (Stasiun DKI 3)**

![Data Original](https://cdn.discordapp.com/attachments/1121095008926302358/1121428071090753576/ori.png)

![Data Hasil Spline Interpolation](https://media.discordapp.net/attachments/1121095008926302358/1121428071434682428/spline.png)

![Data Hasil Time Interpolation](https://media.discordapp.net/attachments/1121095008926302358/1121428071724101662/time.png)

**Perbandingan (Stasiun DKI 4)**

![Data Original](https://media.discordapp.net/attachments/1121095008926302358/1121428097225470072/ori.png)

![Data Hasil Spline Interpolation](https://media.discordapp.net/attachments/1121095008926302358/1121428097493893201/spline.png)

![Data Hasil Time Interpolation](https://media.discordapp.net/attachments/1121095008926302358/1121428097787510784/time.png)

**Perbandingan (Stasiun DKI 5)**

![Data Original](https://media.discordapp.net/attachments/1121095008926302358/1121428121950883880/ori.png)

![Data Hasil Spline Interpolation](https://media.discordapp.net/attachments/1121095008926302358/1121428122231898183/spline.png)

![Data Hasil Time Interpolation](https://media.discordapp.net/attachments/1121095008926302358/1121428122470989954/time.png)

**Kesimpulan**

Setelah dilakukan perbandingan dan pengecekan, disimpulkan bahwa hasil _time interpolation_ memiliki hasil yang lebih baik dibandingkan _spline interpolation_ dimana hasil interpolasi dari _time interpolation_ tidak melewati batas bawah dari nilai ISPU, yaitu 0 dan pergerakannya tidak setajam dari _spline interpolation_. Sehingga hasil dari _time interpolation_ akan dipakai ke tahap berikutnya.

#### 5. Analisis dan Normalisasi Skewness dan Kurtosis

Dalam dunia nyata, data yang akan diterima umumnya tidak memiliki distribusi normal. Hal ini karena sampel tersebut memang tidak berasal dari populasi yang berdistribusi normal. Oleh karena itu, perlu dilakukan pengujian normalitas untuk memastikan apakah data yang sudah dikumpulkan telah memenuhi normalitas data.

Data dikatakan memiliki distribusi normal jika memenuhi ciri-ciri berikut:

1. Bentuk simetris: Distribusi normal memiliki bentuk yang simetris di sekitar nilai tengahnya. Artinya, nilai rata-rata, median, dan modus berada pada posisi yang sama di tengah distribusi.

2. Tidak ada skewness (kemencengan): Distribusi normal tidak memiliki kemencengan yang signifikan. Kemencengan mengindikasikan adanya kecondongan ekor distribusi ke satu sisi. Dalam distribusi normal, ekor distribusi di kedua sisi memiliki kecondongan yang sama.

3. Tidak ada kurtosis ekstrem: Distribusi normal memiliki kurtosis yang moderat. Kurtosis mengukur tingkat keekstreman ekor distribusi. Dalam distribusi normal, kurtosis tidak terlalu tinggi atau rendah, menunjukkan ekor yang tidak terlalu berat atau ringan.

4. Persentil sesuai dengan nilai z: Persentil data dalam distribusi normal sesuai dengan nilai z dalam standar deviasi. Misalnya, 68% data berada dalam satu standar deviasi dari rata-rata, 95% data berada dalam dua standar deviasi, dan 99.7% data berada dalam tiga standar deviasi.

5. Diagram Q-Q: Plot kuantil-kuantil (Q-Q plot) data terhadap kuantil-kuantil dari distribusi normal menghasilkan garis lurus. Ini menunjukkan kesesuaian data dengan distribusi normal.

Dalam proyek ini, akan dilakukan pengujian normalitas data menggunakan pendekatan skewness dan kurtosis.

Skewness dan kurtosis adalah ukuran statistik yang digunakan untuk menggambarkan bentuk distribusi data. Skewness mengukur asimetri dari distribusi data, sedangkan kurtosis mengukur keekstreman (atau bentuk ekor) dari distribusi data.

Skewness mengindikasikan sejauh mana distribusi data condong ke satu sisi. Nilai skewness positif menunjukkan bahwa ekor distribusi data condong ke kanan, sedangkan nilai skewness negatif menunjukkan bahwa ekor distribusi data condong ke kiri. Nilai skewness nol menunjukkan bahwa distribusi data simetris.

Rumus skewness yang umum digunakan adalah:

![skewness formula](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQgI0VXs9SvS2SMXUXbfVR0Bj_43i4OL9n39pHaHTeB2hhjEkh2jMqTbbHXzICt7eeVHic&usqp=CAU)

Dimana dalam rumus ini:

* X mewakili setiap titik data dalma sampel

* X̄ mewakili rata-rata sampel

* n mewakili jumlah data dalam sampel

* S mewakili simpangan baku (standar deviasi) sampel

Sedangkan Kkrtosis mengukur keekstreman (atau bentuk ekor) dari distribusi data. Nilai kurtosis tinggi menunjukkan bahwa distribusi data memiliki ekor yang lebih berat dan puncak yang lebih tajam, sedangkan nilai kurtosis rendah menunjukkan distribusi data dengan ekor yang lebih ringan dan puncak yang lebih datar.

Rumus kurtosis yang umum digunakan adalah:

![kurtosis formula](https://media.discordapp.net/attachments/1121095008926302358/1121430127188910200/kurtosis_formula.png)

Dimana dalam rumus ini memiliki arti yang sama dengan rumus skewness.

Sebuah distribusi data dinyatakan normal jika memenuhi aspek berikut:

1. Jika skewness berkisar antara -0,5 hingga 0,5, data dapat dianggap mendekati distribusi normal.

2. Jika kurtosis berkisar antara -2 hingga 2 (atau antara 2 hingga 3 jika menggunakan definisi kurtosis ekscess), data dapat dianggap mendekati distribusi normal.

	![skewness categorical](https://upload.wikimedia.org/wikipedia/commons/thumb/c/cc/Relationship_between_mean_and_median_under_different_skewness.png/600px-Relationship_between_mean_and_median_under_different_skewness.png)

Jika suatu distribusi data tidak memenuhi kriteria berikut, dapat dilakukan langkah normalisasi. Ada 2 teknik yang umum digunakan dalam melakukan normalisasi skewness dan kurtosis:

1. Logaritmik

* Normalisasi menggunakan logaritma dapat digunakan untuk mengubah distribusi data yang umumnya condong ke kanan menjadi lebih simetris. Pendekatan ini berguna ketika terdapat perbedaan variabilitas yang besar di antara nilai-nilai data.

* Rumus normalisasi logaritmik:

	X' =log(X)

2. Box-Cox

* Metode normalisasi Box-Cox adalah transformasi yang memperhitungkan skewness dan kurtosis data asli. Transformasi ini menggunakan parameter lambda (λ) yang ditentukan secara otomatis untuk menghasilkan distribusi yang lebih simetris.

	Rumus normalisasi Box-Cox:
  
	![box-cox formula](https://www.leansigmacorporation.com/wp/wp-content/uploads/2016/01/Box-Cox-EQ1.png)

* Dimana dalam rumus ini

* Y adalah data asli.

* λ adalah parameter Box-Cox yang ditentukan secara otomatis untuk mencapai distribusi yang lebih simetris.

* Selain itu x akan di logaritmik jika lambda adalah 0

**Perbandingan (Stasiun DKI 1)**

![Perbandingan Skewness di DKI 1](https://media.discordapp.net/attachments/1121095008926302358/1121433725511667742/join.jpeg)

**Perbandingan (Stasiun DKI 2)**

![Perbandingan Skewness di DKI 2](https://media.discordapp.net/attachments/1121095008926302358/1121433725830447104/join.jpeg)

**Perbandingan (Stasiun DKI 3)**

![Perbandingan Skewness di DKI 3](https://media.discordapp.net/attachments/1121095008926302358/1121433726161784902/join.jpeg)

**Perbandingan (Stasiun DKI 4)**

![Perbandingan Skewness di DKI 4](https://media.discordapp.net/attachments/1121095008926302358/1121433726161784902/join.jpeg)

**Perbandingan (Stasiun DKI 5)**

![Perbandingan Skewness di DKI 5](https://media.discordapp.net/attachments/1121095008926302358/1121433726447009833/join.jpeg)

**Kesimpulan**

Berdasarkan hasil berikut, hasil normalisasi dari Box-Cox memberikan hasil rata-rata **11.43%** lebih baik dibandingkan metode Logaritma. Untuk itu hasil dari normalisasi Box-Cox akan dipakai di tahap berikutnya.

#### 6. Stasioneritas

Data stasioner adalah data yang menunjukan mean, varian, dan autovarians tetap sama pada waktu kapan saja data itu dibentuk atau dipakai, artinya dengan data yang stasioner model time series dapat dikatakan lebih stabil. Apabila data yang digunakan dalam model ada yang tidak stasioner.

Beberapa metode pengujian data stasioner yang umum digunakan adalah _Augmented Dickey-Fuller (ADF)_ dan _Kwiatkowski-Phillips-Schmidt-Shin_ (KPSS).

Pengujian ADF adalah metode statistik yang digunakan untuk menguji apakah suatu deret waktu stasioner atau tidak. Deret waktu stasioner tidak memiliki tren atau pola sistematis yang berubah seiring waktu.

Rumus pengujian ADF (Augmented Dickey-Fuller) dapat dinyatakan sebagai berikut:

![enter image description here](https://static.packt-cdn.com/products/9781789346466/graphics/assets/2177ca63-55d4-40b3-93ae-80a298b53df9.png)

Di dalam rumus tersebut:

* Δy<sub>t</sub> adalah selisih atau differencing pertama dari deret waktu yang diuji.

* α adalah konstanta.

* βt adalah komponen linear yang mewakili tren waktu.

* yt-1 adalah nilai lag satu dari deret waktu.

* Δy<sub>t−1</sub> adalah differencing pertama dari lag-lag sebelumnya.

* δ<sub>j</sub> adalah koefisien yang diestimasi dalam model.

* ε<sub>t</sub> adalah residual atau kesalahan pada waktu t.

Dalam ADF ada 2 Hipotesis yang berlaku

_H0_ : _p-value_ >= **α** (Tidak Stasioner)

_H1_ : _p-value_ < **α** (Stasioner)

Pengujian KPSS (Kwiatkowski-Phillips-Schmidt-Shin) adalah metode statistik yang digunakan untuk menguji sifat stasioneritas dari suatu deret waktu. Stasioneritas adalah sifat deret waktu di mana statistik dasarnya, seperti rata-rata dan varians, tidak berubah secara signifikan seiring waktu.

Perbedaan antara ADF dan KPSS ada pada penentuan hipotesisnya. Jika pada ADF _H0_ ditolak jika _p-value_ lebih kecil dari nilai _alpha_ yang menunjukkan data tersebut stasioner, pada KPSS terjadi kebalikannya.

_H0_ : _p-value_ >= **α** (Stasioner)

_H1_ : _p-value_ < **α** (Tidak Stasioner)

Selain itu ADF juga berfungsi untuk mengukur _unit root_ pada data dimana jika _unit root_ tinggi, maka data tidak stasioner.

Dalam pengujian Stasioner, sangat disarankan untuk menerapkan kedua pengujian tersebut, sehingga dapat dipastikan bahwa deret tersebut benar-benar stasioner. Hasil yang mungkin didapatkan dari penerapan tes stasioner ini adalah sebagai berikut:

Kasus 1: Kedua pengujian menyimpulkan bahwa deret tidak stasioner - Deret tidak stasioner
Kasus 2: Kedua pengujian menyimpulkan bahwa deret tersebut stasioner - Deret tersebut stasioner
Kasus 3: KPSS menunjukkan stasioneritas dan ADF menunjukkan tidak stasioner - Deret ini _trend stationary_. Tren perlu dihilangkan untuk membuat seri stasioner yang ketat. Seri detrended diperiksa untuk stasioneritas.
Kasus 4: KPSS menunjukkan tidak stasioner dan ADF menunjukkan stasioneritas - Deretnya _difference stationary_. Diferensiasi dapat digunakan untuk membuat data jadi stasioner. 

Untuk pengujian ini, nilai _alpha_ yang di tetapkan adalah **0.05**. Hasil dari pengujiannya adalah sebagai berikut.

| Stasiun | _p-value (ADF)_        | _p-value_ (KPSS) |
|---------|------------------------|------------------|
| DKI1    |  0.007447112672842345  |     0.010000     |
| DKI2    |  4.220321542506222e-09 |     0.026535     |
| DKI3    |  4.508933490274137e-13 |     0.010000     |
| DKI4    | 3.0919198638968907e-10 |     0.010000     |
| DKI5    |  9.310078495263056e-11 |     0.019092     |

Berdasarkan hasil pengujian, nilai _p-value_ ADF dan KPSS seluruh stasiun berada dibawah 0.05, dimana berdasarkan pengujian ADF seluruhnya stasioner. Namun berdasarkan pengujian KPSS, seluruhnya tidak stasioner, sehingga seluruh data stasiun merupakan _difference stationary_. Untuk mengubah data tersebut menjadi stasioner, maka seluruh data stasiun harus dilakukan differensiasi agar data menjadi stasioner. 

_Difference_ merupakan operasi dengan mengambil selisih dari beberapa data di satu waktu.

![how difference works](https://sp-ao.shortpixel.ai/client/to_auto,q_lossless,ret_img,w_1024,h_840/https://dataindependent.com/wp-content/uploads/2021/12/Screen-Shot-2020-09-22-at-7.37.51-AM-1024x840-1.png)

Pada contoh diatas, dimana nilai _lag_ atau jarak waktu yang dilakukan _difference_ adalah 1, maka data di index 1 akan bernilai selisih dari data sekarang dengan data sebelumnya, pada kasus ini data indeks 1 nya adalah data **Tues**, maka selisih dari data **Mon** dan **Tues** yang akan dipakai di indeks **Tues**, sedangkan indeks **Mon** yang dipakai sebagai patokan awal akan diberi nilai **NaN**.  Dalam melakukan _Difference Transform_ ada 2 metode yang umumnya dilakukan

1. _Difference Order_
	
	_Difference Order_ adalah teknik differensiasi paling simpel. Cara kerjanya dengan melakukan operasi _different_ secara berulang yang disebut dengan _order_. Contohnya pada _First Order Difference_, maka rumusnya adalah

	y'<sub>t</sub> = y<sub>t</sub> - y<sub>t-1</sub>

	Kemudian jika hasil _difference_ belum memberikan hasil yang memuaskan, bisa melakukan _difference_ kembali terhadap data yang sudah di-_difference_ sebelumnya. Operasi ini yang disebut _Second Order Difference_ dengan rumus

	y''<sub>t</sub> = y'<sub>t</sub> - y'<sub>t-1</sub>

	Sehingga rumus untuk operasi _Difference Order_ adalah sebagai berikut

	y<sup>n</sup><sub>t</sub> = y<sup>n-1</sup><sub>t</sub> - y<sup>n-1</sup><sub>t-1</sub>

	Dimana nilai _n_ merupakan jumlah _order_ yang dilakukan.

2.  _Lag Difference / Seasional Difference_

	_Lag Difference_ adalah metode _difference_ dimana nilai _lag_ ini merupakan jarak data yang akan dicari selisihnya. Jika mengambil contoh dari gambar sebelumnya, jika _lag_ nya adalah 2, maka data indeks **Wed** merupakan selisih dari data **Mon** dengan data **Wed**. Kemudian data di indeks **Mon** dan **Tues** akan bernilai NaN karena tidak ditemukan selisih data 2 indeks sebelumnya. Secara rumus dapat dijelaskan sebagai berikut.

	y'<sub>t</sub> = y<sub>t</sub> - y<sub>t-n</sub>

	Dimana nilai _n_ merupakan nilai _lag_.

_Pandas_ menyediakan fitur _diff()_ yang dapat melakukan _difference_ dengan mudah, penerapannya bisa dilihat di bawah ini.

```py
	## First-order Difference
	df = df.diff()

	## Second-order Difference
	df = df.diff().diff()

	## Lag Difference
	df = df.diff(7)
```

Pada proyek ini, penulis menerapkan _Lag Difference_ dimana nilai _lag_ adalah 7 yang merujuk kepada data yang dicatat selama 1 minggu. Sehingga hasil pengujian stasioneritasnya sebagai berikut.

| Stasiun | _p-value (ADF)_        | _p-value_ (KPSS) |
|---------|------------------------|------------------|
| DKI1    |  2.7285470185710886e-29  |     0.100000     |
| DKI2    |  7.784563056237512e-26 |     0.100000     |
| DKI3    |  5.220703057245167e-27 |     0.100000     |
| DKI4    | 7.763233808925082e-26 |     0.100000     |
| DKI5    |  1.418021032753268e-23 |     0.100000     |

#### 7. Korelasi (ACF dan P-ACF)

Korelasi ACF (Autocorrelation Function) dan PACF (Partial Autocorrelation Function) adalah alat statistik yang digunakan dalam analisis deret waktu untuk memahami ketergantungan atau hubungan antara nilai-nilai dalam deret waktu.

Fungsi dari ACF dan PACF selain untuk melihat korelasi, juga dapat digunakan untuk mengetahui stasioneritas suatu data. Plot ACF dan PACF juga digunakan untuk mengetahui urutan model AR, MA, dan ARMA termasuk juga ARIMA. Dibagian ini, akan dijelaskan secara singkat mengenai AR dan MA.

**_Auto-Regressive Model (AR)_** 

Model _Auto-Regressive_ mengasumsikan bahwa nilai saat ini (y<sub>t</sub>) bergantung pada nilai sebelumnya (y<sub>t-1</sub>, y<sub>t-2</sub>, y<sub>t-n</sub>).  Berdasarkan asumsi ini, maka model regresi linear dapat dibangun.

![AR Formula](https://miro.medium.com/v2/resize:fit:720/format:webp/1*O6l94lPN-3dl4y-ilEirbw.png)

Jika merujuk pada plot ACF dan P-ACF, plot P-ACF dapat digunakan untuk mengetahui urutan dari model AR.

**_Moving Average (MA)_**

Model Moving Average (MA) mengasumsikan bahwa nilai saat ini (y<sub>t</sub>) bergantung pada _error terms_ termasuk _error_ saat ini (𝜖<sub>t</sub>, 𝜖<sub>t-1</sub>, 𝜖<sub>t-n</sub>). Karena  _error terms_ ini bersifat acak, tidak ada hubungan linier antara nilai saat ini dan  _error terms_.

![AR Formula](https://miro.medium.com/v2/resize:fit:720/format:webp/1*ye-hv0jI0nYGdJiBOCkTKQ.png)

Jika merujuk pada plot ACF dan P-ACF, plot ACF dapat digunakan untuk mengetahui urutan dari model MA.

Dari penjelasan ini dapat disimpulkan bahwa untuk menentukan nilai AR dapat melihat dari plot P-ACF. Begitu dengan MA dengan melihat plot ACF. Untuk memperjelas, dapat dilihat dari plot ACF dan P-ACF **Stasiun DKI 1** berikut.

![ACF PACF DKI 1](https://media.discordapp.net/attachments/1121095008926302358/1121467631921275010/dki1.png)

Plot ini disebut dengan "lolipop plot" dikarena setiap garis korelasi memiliki ujung bulat seperti lolipop. Jika melihat plot diatas, terlihat _lag_ pada ACF dan PACF dimulai dari 0 dan selalu bernilai **korelasi 1**. Selain itu terdapat sebuah area yang berwarna biru. Area biru ini menggambarkan interval kepercayaan 95% dan merupakan indikator ambang signifikansi. Artinya, apa pun di dalam area biru secara statistik mendekati nol dan apa pun di luar area biru secara statistik bukan nol.

Untuk mengetahui urutan dari model ini dengan cara menghitung berapa jumlah "lolipop" atau _lag_ yang berada di bawah atau di atas "area biru" sebelum _lag_ berikutnya memasuki "area biru".

Pada contoh ACF dan PACF DKI 1 ini, di plot ACF terdapat 5 _lag_ yang berada di luar area biru sebelum _lag _ ke-6 memasuki area biru, maka urutan model MA adalah **MA(5)**. Sedangkan pada plot PACF terdapat 4 _lag_ yang berada di luar area biru sebelum _lag_ ke-5 memasuki area biru, sehingga urutan model AR adalah **AR(4)**.

**ACF dan PACF DKI 2**

![ACF PACF DKI 2](https://media.discordapp.net/attachments/1121095008926302358/1121467632189718539/dki2.png)

**ACF dan PACF DKI 3**

![ACF PACF DKI 3](https://media.discordapp.net/attachments/1121095008926302358/1121467632634298501/dki3.png)

**ACF dan PACF DKI 4**

![ACF PACF DKI 4](https://media.discordapp.net/attachments/1121095008926302358/1121467632906944552/dki4.png)

**ACF dan PACF DKI 5**

![ACF PACF DKI 5](https://media.discordapp.net/attachments/1121095008926302358/1121467633208918036/dki5.png)



## Data Preparation

### Train-Test Split

Langkah awal untuk membangun model adalah dengan melakukan pembagian antara data latih dengan data pengujian. Untuk proyek ini, pembagian akan menggunakan rasio **80:20** untuk ARIMA dan **60:20:20** untuk LSTM dimana 20% tambahan digunakan untuk data validasi.

Sehingga total data untuk model ARIMA dan LSTM adalah sebagai berikut

<table>
<thead>
  <tr>
    <th>Model</th>
    <th>Stasiun</th>
    <th>Train</th>
    <th>Val</th>
    <th>Test</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="5">ARIMA</td>
    <td>DKI 1</td>
    <td>3413</td>
    <td>0</td>
    <td>853</td>
  </tr>
  <tr>
    <td>DKI 2</td>
    <td>3221</td>
    <td>0</td>
    <td>805</td>
  </tr>
  <tr>
    <td>DKI 3</td>
    <td>3179</td>
    <td>0</td>
    <td>795</td>
  </tr>
  <tr>
    <td>DKI 4</td>
    <td>3174</td>
    <td>0</td>
    <td>794</td>
  </tr>
  <tr>
    <td>DKI 5</td>
    <td>2617</td>
    <td>0</td>
    <td>654</td>
  </tr>
  <tr>
    <td rowspan="5">LSTM</td>
    <td>DKI 1</td>
    <td>2560</td>
    <td>853</td>
    <td>853</td>
  </tr>
  <tr>
    <td>DKI 2</td>
    <td>2416</td>
    <td>805</td>
    <td>805</td>
  </tr>
  <tr>
    <td>DKI 3</td>
    <td>2385</td>
    <td>794</td>
    <td>795</td>
  </tr>
  <tr>
    <td>DKI 4</td>
    <td>2381</td>
    <td>793</td>
    <td>794</td>
  </tr>
  <tr>
    <td>DKI 5</td>
    <td>1963</td>
    <td>654</td>
    <td>654</td>
  </tr>
</tbody>
</table>

### Windowed Dataset

_Windowing_ adalah suatu teknik _preprocessing data_ untuk _time series_ dengan cara melakukan pembagian suatu dataset dan menggunakan data berikutnya sebagai validasi untuk prediksinya. Contohnya seperti berikut, diasumsikan terdapat suatu kolom dari _time series_ dengan deretan sebagai berikut

    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

Dan akan dilakukan _preprocessing_ dengan ukuran _window_ sebesar **7**, maka hasilnya menjadi sebagai berikut

```
[0, 1,  2, 3, 4, 5, 6] -> [7]
[1,  2, 3, 4, 5, 6, 7] -> [8]
[2,  3, 4, 5, 6, 7, 8] -> [9]
```

Dari hasil berikut, dapat disimpulkan bahwa konsep dari _windowing_ ini mirip dengan konsep _train-test split_ dimana akan ada data yang dipotong dengan ukuran _window_ yang akan jadi data latih kemudian nilai berikutnya yang menjadi nilai _test_ atau harapan yang ingin dicapai.

Namun jika diperhatikan, nilai awal dari setiap _array_ akan bergerak maju setiap ada _array_ baru. Teknik ini yang disebut dengan _Sliding Window_ . Sedangkan metode lainnya yaitu _Expanding Window_ dimana ukuran _window_ untuk data latih akan semakin membersar seperti contoh berikut.

```
[0, 1,  2, 3, 4, 5, 6] -> [7]
[0, 1,  2, 3, 4, 5, 6, 7] -> [8]
[0, 1, 2,  3, 4, 5, 6, 7, 8] -> [9]
```

![Sliding vs Expanding Window](https://www.mlq.ai/content/images/size/w1000/2022/10/image6-e1536165830511.png)

 _Windowed Dataset_ digunakan ketika menerapkan model yang berbasis RNN ataupun CNN / _Deep Learning_.  Pada proyek ini akan digunakan pendekatan _sliding window_ menggunakan fitur _datasets_ dari _Tensorflow_.

## Modelling

Untuk model yang akan digunakan dalam proyek ini yaitu ARIMA dan LSTM. Model akan dibangun di setiap stasiun dan akan dilakukan perbandingan akurasi terhadap data uji. Sehingga terdapat **10 model** yang akan dibangun.

### ARIMA (Autoregressive Integrated Moving Average)

ARIMA (Autoregressive Integrated Moving Average) adalah suatu model yang digunakan untuk menganalisis dan meramalkan deret waktu, seperti data penjualan bulanan, harga saham, atau suhu harian. Model ARIMA memperhitungkan pola dan tren dalam data untuk membuat perkiraan tentang nilai-nilai di masa depan.  

ARIMA terdiri dari tiga komponen utama:  

1. Autoregresi (AR): Komponen ini memperhitungkan bagaimana nilai-nilai sebelumnya dalam deret waktu mempengaruhi nilai saat ini. Misalnya, jika penjualan bulan lalu tinggi, kemungkinan penjualan bulan ini juga akan tinggi.

2. Integrasi (I): Komponen ini digunakan untuk membuat deret waktu menjadi lebih stabil dengan menghilangkan tren atau fluktuasi sistematis. Dengan cara ini, kita dapat melihat pola yang lebih jelas dalam data.

3. Moving Average (MA): Komponen ini memperhitungkan pola kesalahan atau perbedaan antara nilai sebenarnya dan nilai yang diprediksi. Dalam model MA, kesalahan masa lalu digunakan untuk memprediksi kesalahan di masa depan.

Dalam model ARIMA, kita menentukan tiga angka dalam format ARIMA(p, d, q), di mana:

* p adalah jumlah lag yang diperhitungkan dalam komponen autoregresi. Semakin besar nilai p, semakin jauh ke belakang kita melihat untuk memprediksi nilai saat ini.

* d adalah jumlah differencing yang dilakukan pada data. Ini membantu menghilangkan tren dan membuat deret waktu menjadi lebih stasioner.

* q adalah jumlah lag yang diperhitungkan dalam komponen moving average. Semakin besar nilai q, semakin banyak kesalahan masa lalu yang diperhitungkan untuk memprediksi kesalahan di masa depan.

Dikarena hal tersebut, penerapan plot ACF dan PACF digunakan untuk menentukan parameter _p_ dan _q_.

**Kelebihan dari ARIMA**
* Arsitektur dan penerapan yang sangat sederhana
* ARIMA menggunakan jumlah observasi terakhir dalam peramalan, yang membuatnya lebih cocok untuk data deret waktu yang memiliki ketergantungan jangka pendek
* Dikarenakan arsitektur nya sederhana, proses pelatihan dan prediksi model ARIMA menjadi cepat walaupun di jalankan di mode _CPU_

**Kekurangan dari ARIMA**
* ARIMA kurang efektif dalam menangani data deret waktu yang memiliki pola jangka panjang atau pola yang rumit
* Sangat sensitif terhadap stasioneritas data
* ARIMA didasarkan pada model linier, sehingga tidak mampu menangkap pola non-linier dalam data deret waktu

Pada proyek ini, penulis mencoba membangun model ARIMA(4, 0, 5) dengan ARIMA(5, 0, 5).

### LSTM (Long Short-Term Memory)

_LSTM (Long Short-Term Memory)_ adalah jenis arsitektur jaringan saraf yang digunakan untuk memodelkan dan memprediksi data deret waktu. LSTM sangat efektif dalam menangani data deret waktu dengan ketergantungan jangka panjang, seperti pola yang terjadi dalam rentang waktu yang lebih luas.

LSTM merupakan pengembangan dari _Recrusive Neural Network (RNN)_. LSTM memiliki arsitektur sebagai berikut.

![LSTM Arcitecture](https://miro.medium.com/v2/resize:fit:720/format:webp/1*jikKbzFXCq-IYnFZankIMg.png)

**Kelebihan dari LSTM**

* LSTM sangat baik dalam menangkap ketergantungan jangka panjang dalam data _time series_, sehingga lebih cocok untuk data dengan pola kompleks dan tidak linier
* LSTM dapat mengadaptasi dan belajar dari data dengan cepat, serta menyesuaikan diri dengan perubahan pola dalam deret waktu
* LSTM memiliki mekanisme memori internal yang memungkinkannya mengingat informasi penting dari masa lalu, yang membantu dalam pemodelan dan prediksi _time series_ yang memiliki ketergantungan jangka panjang

**Kekurangan dari LSTM**

* LSTM merupakan salah satu model _Deep Learing_ sehingga memiliki kompleksitas yang lebih berat dibandingkan dengan ARIMA. Sehingga dalam melakukan pelatihan dan prediksi sangat disarankan menggunakan _GPU_ untuk mempercepat proses komputasi
* LSTM melibatkan banyak _hyperparameter_ seperti jumlah _layer_, unit, dan _epoch_, yang memerlukan berbagai percobaan agar mendapatkan _hyperparameter_ yang optimal

Pada proyek ini, penulis membangun model LSTM dengan arsitektur sebagai berikut ini.

![LSTM Model](https://media.discordapp.net/attachments/1121095008926302358/1121482722100125696/image.png)

Sedangkan untuk _loss function_ menggunakan _Hubber_ dengan metrik MAE dan _optimizer RMSProp(0.0001)_ dengan nilai _epoch_ sebesar 300. Selain itu dilakukan implementasi _callback_ berupa _Early Stopping_ dengan nilai _patience_ sebesar 50 _epochs_ dengan _weights_ yang diambil adalah model dengan _eror rate_ paling rendah / terbaik. _Early stopping_ digunakan untuk menghentikan proses pelatihan sehingga menghemat waktu dan juga mencegah terjadinya _overfitting_ pada model _deep learning_.

## Evaluation

Untuk pengujian akan menggunkan 3 metrik evaluasi, yaitu _Mean Average Error (MAE)_, _Mean Square Error (MSE)_ dan _Root Mean Square Error (RMSE)_.

###  _Mean Absolute Error (MAE)_

MAE adalah metrik evaluasi yang mengukur rata-rata kesalahan absolut antara nilai-nilai aktual dan nilai-nilai yang diprediksi. MAE memberikan gambaran tentang sejauh mana nilai prediksi secara keseluruhan berbeda dari nilai aktual.

Rumus yang digunakan adalah

MAE = (1/n) * Σ|i=1 to n| |yi - ŷi|

Dimana dalam rumus berikut

* yi adalah nilai aktual

* ŷi adalah nilai prediksi

* n adalah jumlah sampel

### _Mean Square Error (MSE)_

MSE adalah metrik evaluasi yang mengukur rata-rata dari kuadrat kesalahan antara nilai-nilai aktual dan nilai-nilai yang diprediksi. MSE memberikan informasi tentang variabilitas atau dispersi kesalahan prediksi.

Rumus yang digunakan adalah

MSE = (1/n) * Σ|i=1 to n| (yi - ŷi)^2

Dimana dalam rumus berikut

* yi adalah nilai aktual

* ŷi adalah nilai prediksi

* n adalah jumlah sampel

### _Root Mean Square Error (RMSE)_

RMSE adalah akar kuadrat dari MSE dan merupakan metrik evaluasi yang umum digunakan dalam analisis prediksi. RMSE memberikan indikasi rata-rata kesalahan prediksi dalam satuan yang sama dengan variabel yang diukur.

Rumus yang digunakan adalah

RMSE = √((1/n) * Σ|i=1 to n| (yi - ŷi)^2)

Dimana dalam rumus berikut

* yi adalah nilai aktual

* ŷi adalah nilai prediksi

* n adalah jumlah sampel

Berdasarkan hasil dari perhitungan metrik untuk model ARIMA dan LSTM dapat dilihat dari tabel berikut

<table>
<thead>
  <tr>
    <th>Model</th>
    <th>Metrik<sup>*</sup></th>
    <th>DKI1</th>
    <th>DKI2</th>
    <th>DKI3</th>
    <th>DKI4</th>
    <th>DKI5</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="3">ARIMA (4, 0 ,5)</td>
    <td>MAE</td>
    <td>1.139</td>
    <td>0.484</td>
    <td>0.478</td>
    <td>0.342</td>
    <td>0.409</td>
  </tr>
  <tr>
    <td>MSE</td>
    <td>2.674</td>
    <td>0.437</td>
    <td>0.492</td>
    <td>0.279</td>
    <td>0.336</td>
  </tr>
  <tr>
    <td>RMSE</td>
    <td>1.635</td>
    <td>0.661</td>
    <td>0.701</td>
    <td>0.528</td>
    <td>0.58</td>
  </tr>
  <tr>
    <td rowspan="3">ARIMA (5, 0 ,5)</td>
    <td>MAE</td>
    <td>1.136</td>
    <td>0.484</td>
    <td>0.478</td>
    <td>0.342</td>
    <td>0.409</td>
  </tr>
  <tr>
    <td>MSE</td>
    <td>2.672</td>
    <td>0.437</td>
    <td>0.492</td>
    <td>0.279</td>
    <td>0.336</td>
  </tr>
  <tr>
    <td>RMSE</td>
    <td>1.635</td>
    <td>0.661</td>
    <td>0.701</td>
    <td>0.528</td>
    <td>0.58</td>
  </tr>
  <tr>
    <td rowspan="3">LSTM</td>
    <td>MAE</td>
    <td>1.046</td>
    <td>0.418</td>
    <td>0.421</td>
    <td>0.296</td>
    <td>0.374</td>
  </tr>
  <tr>
    <td>MSE</td>
    <td>2.132</td>
    <td>0.335</td>
    <td>0.358</td>
    <td>0.186</td>
    <td>0.275</td>
  </tr>
  <tr>
    <td>RMSE</td>
    <td>1.46</td>
    <td>0.579</td>
    <td>0.599</td>
    <td>0.432</td>
    <td>0.524</td>
  </tr>
</tbody>
</table>

<sup>*) Semakin kecil semakin baik</sup>

Berdasarkan tabel berikut dapat disimpulkan bahwa model LSTM memberikan hasil yang lebih baik dibandingkan menggunakan model ARIMA dimana hasil **MAE 10.32%, MSE 22.05% dan RMSE 12.45%** lebih baik di model LSTM dibandingkan dengan ARIMA.

## Referensi

Gindo Simanjuntak, A. (2007). PENCEMARAN UDARA. _Buletin LIMBAH_, _11_(1), 34–40.

Hermawan, A. (2019). _SPKU: SISTEM PREDIKSI KUALITAS UDARA (STUDI KASUS: DKI JAKARTA)_. UNIVERSITAS TEKNOLOGI YOGYAKARTA.

IQAir. (2023). _World Air Quality Report 2022_.

IRCEL - CELINE. (n.d.). _What is PM10 and PM2.5?_ Belgian Interregional Environment Agency.

Kumar, A., & Goyal, P. (2011). Forecasting of daily air quality index in Delhi. _Science of the Total Environment_, _409_(24), 5517–5523. https://doi.org/10.1016/j.scitotenv.2011.08.069

Liu, H., Yan, G., Duan, Z., & Chen, C. (2021). Intelligent modeling strategies for forecasting air quality time series: A review. In _Applied Soft Computing_ (Vol. 102). Elsevier Ltd. https://doi.org/10.1016/j.asoc.2020.106957

Plaia, A., Di Salvo, F., Ruggieri, M., & Agró, G. (2013). A Multisite-Multipollutant Air Quality Index. _Atmospheric Environment_, _70_, 387–391. https://doi.org/10.1016/j.atmosenv.2013.01.028

Santoso, Prof. Dr. M., Lestiani, D. D., Marselina, M., & Mukhtar, R. (2016). KARAKTERISTIK PARTIKULAT UDARA AMBIEN DAN TERESPIRASI DI SEKITAR KAWASAN INDUSTRI NON FORMAL. _Jurnal Sains Dan Teknologi Nuklir Indonesia_, _17_(1), 49. https://doi.org/10.17146/jstni.2016.17.1.2342

Turyanti, A., Salmayenti, R., Rohmawati, F. Y., Fauziyah, Y., & Yulian, N. I. (2022). _LAPORAN AKHIR KEGIATAN PEMANTAUAN KUALITAS UDARA PROVINSI DKI JAKARTA TAHUN 2022_.

Yan, R., Liao, J., Yang, J., Sun, W., Nong, M., & Li, F. (2021). Multi-hour and multi-site air quality index forecasting in Beijing using CNN, LSTM, CNN-LSTM, and spatiotemporal clustering. _Expert Systems with Applications_, _169_. https://doi.org/10.1016/j.eswa.2020.114513

Yan, X., & Enhua, X. (2020). ARIMA and Multiple Regression Additive Models for PM2.5 Based on Linear Interpolation. _Proceedings - 2020 International Conference on Big Data and Artificial Intelligence and Software Engineering, ICBASE 2020_, 266–269. https://doi.org/10.1109/ICBASE51474.2020.00062

_Stationarity and detrending (ADF/KPSS) — statsmodels_. (n.d.). Www.statsmodels.org. https://www.statsmodels.org/stable/examples/notebooks/generated/stationarity_detrending_adf_kpss.html

‌Kumar, V. (2021, June 16).  _Statistical tests to check stationarity in Time Series_. Analytics Vidhya. https://www.analyticsvidhya.com/blog/2021/06/statistical-tests-to-check-stationarity-in-time-series-part-1/

‌Ph.D, K. R. C. (2022, June 24).  _How to test normality, skewness and kurtosis using Python_. Omics Diary. https://medium.com/omics-diary/how-to-test-normality-skewness-and-kurtosis-using-python-18fb2d8e35b9

‌Turney, S. (2022, May 10).  _Skewness | Definition, Examples & Formula_. Scribbr. https://www.scribbr.com/statistics/skewness/#:~:text=Revised%20on%20July%2012%2C%202022

‌Brownlee, J. (2017, July 9).  _How to Remove Trends and Seasonality with a Difference Transform in Python_. Machine Learning Mastery. https://machinelearningmastery.com/remove-trends-seasonality-difference-transform-python/

Kwiatkowski, D., Phillips, P. C. B., Schmidt, P., & Shin, Y. (1992). Testing the null hypothesis of stationarity against the alternative of a unit root: How sure are we that economic time series have a unit root? _Journal of Econometrics_, _54_(1-3), 159–178.

‌Selva Prabhakaran. (2019, February 18).  _ARIMA Model - Complete Guide to Time Series Forecasting in Python | ML+_. Machine Learning Plus. https://www.machinelearningplus.com/time-series/arima-model-time-series-forecasting-python/

‌Walkenhorst, J. (2019, June 22).  _How to Interpolate Time Series Data in Apache Spark and Python Pandas — Part 1: Pandas_. Medium. https://towardsdatascience.com/how-to-interpolate-time-series-data-in-apache-spark-and-python-pandas-part-1-pandas-cff54d76a2ea

‌Kumar, S. (2022, April 29).  _4 Techniques to Handle Missing values in Time Series Data_. Medium. https://towardsdatascience.com/4-techniques-to-handle-missing-values-in-time-series-data-c3568589b5a8

‌Keith, M. (2022, October 7).  _Exploring the LSTM Neural Network Model for Time Series_. Medium. https://towardsdatascience.com/exploring-the-lstm-neural-network-model-for-time-series-8b7685aa8cf

‌Kutzkov, K. (2022, September 13).  _ARIMA vs Prophet vs LSTM for Time Series Prediction_. Neptune.ai. https://neptune.ai/blog/arima-vs-prophet-vs-lstm#:~:text=We%20see%20that%20ARIMA%20yields

‌Dolphin, R. (2021, March 26).  _LSTM Networks | A Detailed Explanation_. Medium. https://towardsdatascience.com/lstm-networks-a-detailed-explanation-8fae6aefc7f9

‌
