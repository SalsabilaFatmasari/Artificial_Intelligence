# Laporan Akhir Kecerdasan Buatan - Kelompok 9

**Anggota Kelompok :**

1. Nabila Norhaliza - NIM. 3.34.21.1.17

2. Salsabila Fatmasari - NIM. 3.34.21.1.21

 

## Domain Proyek

Menurut World Cancer Research Fund International, Kanker Paru - Paru berada pada tingkat ke-2 dengan penderita terbanyak. Kanker paru-paru merupakan kanker dengan kematian terbanyak. Banyaknya penderita kanker paru - paru dari tahun ke tahun selalu menunjukkan peningkatan. Pada tahun 2020, terdapat 2.206.771 kasus baru terdiagnosis terkena kanker paru-paru dengan kasus kematian sebanyak 1.796.144 kasus [1]. Dan tidak menutup kemungkinan anak muda terkena kanker paru-paru karena gaya hidup dan lingkungan. Guna meminimalisir terjadinya kanker paru - paru, maka perlu diketahui apa saja penyebab dan gejala yang dapat menimbulkan kanker paru -paru.

Terjadinya kanker paru – paru terdapat 2 faktor, yaitu internal dan eksternal. Untuk factor internal disebabkan adanya penyakit turunan dari orang tua atau orang terdahulu sebelumnya. Sedangkan factor external biasanya disebabkan oleh kegiatan merokok baik passive maupun aktif, sering meminum minuman keras dan masih banyak lainnya. Salah satu bidang pembelajaran mesin yang dapat digunakan untuk melakukan prediksi apakah seseorang terjangkit kanker paru paru atau tidak dan sudah seberapa prahanya yaitu menggunakan metode regresi. Dimana algoritma regresi dapat memprediksi hasil dengan menggunakan beberapa fitur. Salah satu penelitian yang dilakukan oleh [4] memprediksi tingkat kanke rmenggunakan algoritma Random Forest dengan hasil akurasi sebesar 90,32%. Pada penelitian ini akan dilakukan prediiksi kanker paru paru menggunakan algoritma machine learning yang dipilih dengan memanfaatkan Lazy Predict. Hasil pengujian menggunakan algoritma kneighbors, decision tree regressor dan extra tree regressor memiliki tingkat akurasi yang baik yaitu 100%.

 

## Business Understanding

Kanker paru-paru merupakan kanker dengan pengidap terbanyak di dunia dibandingkan kanker yang lain. Sejak dulu, rumah sakit banyak menerima pasien yang terserang penyakit paru-paru. Guna melakukan pencegahan dini kanker paru-paru maka kami sebagai data analis akan mengembangkan sebuah model sistem yang mampu memprediksi seseorang mengenai gejala awal dari kanker paru-paru dengan cara mengumpulkan informasi tentang riwayat penderita pasien kanker paru-paru. Informasi data yang dikumpulkan berdasarkan dari usia, jenis kelamin, paparan polusi udara, pengunaan alkohol, alergi terhadap debu, bahaya dari suatu pekerjaan, risiko genetik,diet seimbang, penyakit paru-paru kronis, obesitas, merokok, perokok pasif, nyeri pada dada, batuk berdarah, kelelahan, penurunan pada berat badan, sesak napas, mengi, kesulitan menelan, kuku jari tabuh, serta mendengkur.
 

#### **Problem Statements ** Berdasarkan persoalan yang telah dijabarkan sebelumnya,, problem statements dari proyek ini yaitu sebagai berikut.

1. Faktor-faktor apa saja yang berdampak besar terhadap level kanker ?

2. Bagaimana cara melakukan proses *Pre-Processing* supaya mendapatkan model *machine learning* yang akurat ?

3. Bagaimana cara memilih model *machine learning* yang memiliki tingkat akurasi terbaik dalam memprediksi level kanker ?

#### **Goals ** Tujuan yang hendak dicapai dari proyek ini adalah sebagai berikut

1. Mengetahui fitur yang paling berkorelasi dengan penentuan level kanker.

2. Membuat model *machine learning* yang dapat memprediksi level kanker.

3. Memilih model *machine learning* yang menghasilkan prediksi paling akurat. Untuk menentukannya dibantu dengan library LazyPredict

#### **Solution Statements ** Solusi yang diajukan untuk menyelesaikan masalah yang telah diuraikan adalah sebagai berikut.

1. Melakukan analisis deskriptif untuk mengetahui pola dan informasi yang tersimpan di data mengenai fitur atau spesifikasi yang mempengaruhi level kanker.

2. Melakukan Proses *Preprocessing* seperti :

​		–      Mengecek *missing value* dan duplikasi data.

​		–      Menghapus kolom yang tidak berpengaruh terhadap prediksi level kanker

​		–      Melakukan visualisasi data untuk melihat persebaran dan korelasi antar kolom

​		–      Membagi data menjadi *training* dan *test set*, dengan prosentase 80% banding 20%. 	Alasan menggunakan 20% karena jumlah dataset yang dimiliki cukup banyak, sehingga bisa mendapatkan banyak data uji hanya dengan 20%. 

​		–      Melakukan *Encoding* terhadap kolom yang bertipe kategorikal menggunakan fungsi Map.

3. Melakukan pemilihan model terbaik menggunakan LazyPredict

​		–      Memilih 4 algoritma yang menghasilkan model dengan performa terbaik

​		–      Perfoma model terbaik dilihat dari skor *Mean Square Error* (MSE), *Root Mean Square Error* (RMSE), dan *R Square* (R2).

## Data Understanding  Dataset yang digunakan pada proyek ini diperoleh dari Kaggle. Silahkan kunjungi tautan berikut [Long Cancer](https://www.kaggle.com/datasets/thedevastator/cancer-patients-and-air-pollution-a-new-link) untuk mengakses dataset yang dipakai. Adapun variabel-variabel yang terdapat pada dataset adalah sebagai berikut :

1. **index :** index data

2. **Patient Id :** Id Pasien

3. **Age :** Usia pasien.

4. **Gender :** Jenis kelamin pasien.

5. **Air Polution :** Tingkat paparan polusi udara terhadap pasien. 

6. **Alcohol Use :** Tingkat penggunaan alkohol pasien.

7.     **Dust Allergy :** Tingkat alergi debu pasien.

8. **OccuPational Hazard :** Tingkat bahaya kerja pasien.

9. **Generic Risk :** Tingkat risiko genetik pasien.

10.   **chronic Lung Diases :** Tingkat penyakit paru kronis pasien.

11. **Balanced Diet :** Tingkat diet seimbang pasien.

12. **Obesity :** Tingkat obesitas pasien. 

13.   **Smooking :** Tingkat merokok pasien. 

14. **Passive Smooking :** Tingkat perokok pasif pasien. 

15. **Chest Paint :** Tingkat nyeri dada pasien.

16.   **Coughing of Blood :** Tingkat batuk darah pasien.

17. **Fatigue :** Tingkat kelelahan pasien. 

18. **Weight Loss** : Tingkat penurunan berat badan

19.   **Shoert of Breath :** Tingkat sesak nafas pasien. 

20. **Wheezing :** Tingkat wheezing pasien. 

21. **Swallowing Difficulty :** Tingkat kesulitan menelan pasien. 

22. **Clubbing of Finger Nails :** Tingkat kuku jari tabuh pasien. 

23. **Frequent Cold :** Tingkat kedinginan. 

24. **Batuk Kering :** Tingkat Batuk Kering.

25.   **Snoring :** Tingkat kekeruhan Cairan .

26. **Level :** Tingkat Kanker Paru Paru.

 

|           | **index**   | **Age**     | **Gender**  | **Air Pollution** | **Alcohol use** | **Dust Allergy** | **OccuPational Hazards** | **Genetic Risk** | **chronic Lung Disease** | **Balanced Diet** | **...** | **Coughing of Blood** | **Fatigue** | **Weight Loss** | **Shortness of Breath** | **Wheezing** | **Swallowing Difficulty** | **Clubbing of Finger  Nails** | **Frequent Cold** | **Dry Cough** | **Snoring** |
| --------- | ----------- | ----------- | ----------- | ----------------- | --------------- | ---------------- | ------------------------ | ---------------- | ------------------------ | ----------------- | ------- | --------------------- | ----------- | --------------- | ----------------------- | ------------ | ------------------------- | ----------------------------- | ----------------- | ------------- | ----------- |
| **count** | 1000.000000 | 1000.000000 | 1000.000000 | 1000.0000         | 1000.000000     | 1000.000000      | 1000.000000              | 1000.000000      | 1000.000000              | 1000.000000       | ...     | 1000.000000           | 1000.000000 | 1000.000000     | 1000.000000             | 1000.000000  | 1000.000000               | 1000.000000                   | 1000.000000       | 1000.000000   | 1000.000000 |
| **mean**  | 499.500000  | 37.174000   | 1.402000    | 3.8400            | 4.563000        | 5.165000         | 4.840000                 | 4.580000         | 4.380000                 | 4.491000          | ...     | 4.859000              | 3.856000    | 3.855000        | 4.240000                | 3.777000     | 3.746000                  | 3.923000                      | 3.536000          | 3.853000      | 2.926000    |
| **std**   | 288.819436  | 12.005493   | 0.490547    | 2.0304            | 2.620477        | 1.980833         | 2.107805                 | 2.126999         | 1.848518                 | 2.135528          | ...     | 2.427965              | 2.244616    | 2.206546        | 2.285087                | 2.041921     | 2.270383                  | 2.388048                      | 1.832502          | 2.039007      | 1.474686    |
| **min**   | 0.000000    | 14.000000   | 1.000000    | 1.0000            | 1.000000        | 1.000000         | 1.000000                 | 1.000000         | 1.000000                 | 1.000000          | ...     | 1.000000              | 1.000000    | 1.000000        | 1.000000                | 1.000000     | 1.000000                  | 1.000000                      | 1.000000          | 1.000000      | 1.000000    |
| **25%**   | 249.750000  | 27.750000   | 1.000000    | 2.0000            | 2.000000        | 4.000000         | 3.000000                 | 2.000000         | 3.000000                 | 2.000000          | ...     | 3.000000              | 2.000000    | 2.000000        | 2.000000                | 2.000000     | 2.000000                  | 2.000000                      | 2.000000          | 2.000000      | 2.000000    |
| **50%**   | 499.500000  | 36.000000   | 1.000000    | 3.0000            | 5.000000        | 6.000000         | 5.000000                 | 5.000000         | 4.000000                 | 4.000000          | ...     | 4.000000              | 3.000000    | 3.000000        | 4.000000                | 4.           |                           |                               |                   |               |             |

 

Pada tahap Data, dilakukan analisis data eksploratif untuk memperoleh pemahaman tentang sifat data, memahami struktur data, dan mengidentifikasi kemungkinan masalah atau kesalahan yang dapat terjadi. Kegiatan Pemahaman Data yang dilakukan dalam proyek ini meliputi :

·    Memberikan keterangan terkait banyaknya data, nilai yang salah, data yang duplikat, korelasi antar kolom serta sebaran data.

·    Melakukan tahapan manipulasi data dengan mengubah kolom kategorical pada kolom level menjadi tipe numeric agar bisa dicari korelasinya dengan kolom lainnya. Level Low : 1, Medium : 2, High : 3.

·    Melakukan visualiasasi data untuk memperoleh gambaran korelasi dan sebaran data. Korelasi antar kolom divisualisasikan menggunakan heatmap yang ditunjukkan pada Gambar 1 dan Gambar 2 Berdasarkan diagram heatmap dan point b serial. Semakin tinggi hasil korelasi (mendekati 1) maka korelasi semakin tinggi. Berdasarkan korelasi point b serial dapat dilihat yang sangat mendekati 1 yaitu kolom obesity dan Coughing of blood sedangkan yang sangar rendah korelasinya yaitu kolom Age, Gender, Wheezing, Swallowing Difficulty

 

 

 

 

 

 

Gambar 1. Korelasi Heatmap

![img](file:///C:/Users/LENOVO/AppData/Local/Packages/oice_16_974fa576_32c1d314_39f5/AC/Temp/msohtmlclip1/01/clip_image002.gif)

 

Gambar 2. Korelasi Point B Serial

![img](file:///C:/Users/LENOVO/AppData/Local/Packages/oice_16_974fa576_32c1d314_39f5/AC/Temp/msohtmlclip1/01/clip_image004.gif)

 

​       

 

 

Gambar 3. Sebaran Data

 ![img](file:///C:/Users/LENOVO/AppData/Local/Packages/oice_16_974fa576_32c1d314_39f5/AC/Temp/msohtmlclip1/01/clip_image006.gif)

 

**Data Preparation**

Tahapan data preparation dalam proyek ini yaitu sebagai berikut :

1. Penyeleksian Fitur : Melakukan penyeleksian fitur yang digunakan untuk melakukan seleksi kolom yang berfungsi untuk data fitur dan kolam yang berfungsi sebagai data label.

2. Split Data : Melakukan pembagian dataset menjadi dua bagian yaitu data uji dan data latih. Dalam proyek ini kedua bagian tersebut memiliki perbandingan 20 : 80. Dimana 20% sebagai data uji dan 80% sebagai data latih.

3. Menampilkan banyaknya data uji dan data latih. Data uji yang digunakan berjumlah 800 sedangkan data latih berjumlah 200 dan untuk fitur yang digunakan sebanyak 19

 

**Modelling**

Ditahapan ini berlangsung proses pelatihan yang berfungsi untuk mendapatkan sebuah model yang memiliki performa yang baik. Tahapan pada proses ini yaitu sebagai berikut.

1. Memperkirakan algoritma yang memiliki performa terbagus dengan memanfaatkan library Lazy Predict. Hasil dari tahap pelatihan menggunakan Lazy Predict ditampilkan pada Tabel 2.

 

Tabel 2. Hasil perbedaan akurasi model menggunakan Lazy Predict

 



| Model                         | Adjusted R-Squared | R-Squared | RMSE | Time  Taken |
| ----------------------------- | ------------------ | --------- | ---- | ----------- |
| KNeighborsRegressor           | 1                  | 1         | 0    | 0.01        |
| DecisionTreeRegressor         | 1                  | 1         | 0    | 0.01        |
| ExtraTreeRegressor            | 1                  | 1         | 0    | 0           |
| ExtraTreesRegressor           | 1                  | 1         | 0    | 0.09        |
| GaussianProcessRegressor      | 1                  | 1         | 0    | 0.06        |
| XGBRegressor                  | 1                  | 1         | 0    | 0.03        |
| NuSVR                         | 1                  | 1         | 0    | 0.03        |
| GradientBoostingRegressor     | 1                  | 1         | 0    | 0.06        |
| LGBMRegressor                 | 1                  | 1         | 0    | 0.03        |
| HistGradientBoostingRegressor | 1                  | 1         | 0    | 0.34        |
| RandomForestRegressor         | 1                  | 1         | 0    | 0.13        |
| BaggingRegressor              | 1                  | 1         | 0.01 | 0.01        |
| AdaBoostRegressor             | 1                  | 1         | 0.01 | 0.08        |
| MLPRegressor                  | 0.99               | 1         | 0.03 | 0.07        |
| SVR                           | 0.96               | 0.96      | 0.09 | 0.01        |
| TransformedTargetRegressor    | 0.86               | 0.87      | 0.16 | 0.01        |
| LinearRegression              | 0.86               | 0.87      | 0.16 | 0.01        |
| Ridge                         | 0.86               | 0.87      | 0.16 | 0.02        |
| RidgeCV                       | 0.86               | 0.87      | 0.16 | 0.02        |
| LassoLarsCV                   | 0.86               | 0.87      | 0.16 | 0.02        |
| LassoCV                       | 0.86               | 0.87      | 0.16 | 0.04        |
| ElasticNetCV                  | 0.86               | 0.87      | 0.16 | 0.05        |
| BayesianRidge                 | 0.86               | 0.87      | 0.16 | 0.02        |
| LassoLarsIC                   | 0.86               | 0.87      | 0.16 | 0.01        |
| Lars                          | 0.85               | 0.86      | 0.17 | 0.02        |
| SGDRegressor                  | 0.84               | 0.85      | 0.17 | 0.01        |
| LarsCV                        | 0.84               | 0.85      | 0.17 | 0.02        |
| HuberRegressor                | 0.82               | 0.83      | 0.18 | 0.05        |
| TweedieRegressor              | 0.8                | 0.81      | 0.19 | 0.01        |
| PassiveAggressiveRegressor    | 0.79               | 0.8       | 0.2  | 0.01        |
| OrthogonalMatchingPursuitCV   | 0.77               | 0.79      | 0.2  | 0.01        |
| RANSACRegressor               | 0.75               | 0.77      | 0.21 | 0.06        |
| LinearSVR                     | 0.74               | 0.76      | 0.22 | 0.02        |
| PoissonRegressor              | 0.71               | 0.73      | 0.23 | 0.01        |
| OrthogonalMatchingPursuit     | 0.62               | 0.65      | 0.26 | 0.01        |
| QuantileRegressor             | -0.07              | -0.01     | 0.45 | 4.74        |
| DummyRegressor                | -0.08              | -0.01     | 0.45 | 0.01        |
| ElasticNet                    | -0.08              | -0.01     | 0.45 | 0           |
| LassoLars                     | -0.08              | -0.01     | 0.45 | 0.01        |
| Lasso                         | -0.08              | -0.01     | 0.45 | 0.02        |
| KernelRidge                   | -1.25              | -1.11     | 0.65 | 0           |

 

Model algoritma yang memiliki performa yang bagus dapat dilihat melalui nilai RMSE dan R-Square. Nilai R RMSE dan R-Square semakin besar atau mendekati 1 maka model tersebut memiliki tingkat akurasi atau keakuratan yang baik. Begitupun sebaliknya, nilai RMSE dan R-Square yang kecil atau mendekati angka 0 maka tingkat akurasinya rendah. Jika dilihat dari table tersebut, maka model algoritma yang paling bagus yaitu KNeighborsRegressor, DecisionTreeRegressor, ExtraTreeRegressor.

​       

2. Mencari nilai K untuk menentukan banyaknya tetangga yang terdekat yang digunakan untuk memprediksi suatu node data yang belum diketahui.

 

Tabel 3. Nilai K terbaik

| K                  | R-Squared                      |
| ------------------ | ------------------------------ |
| K = 1              | R-Squared = 1.0                |
| K = 2              | R-Squared = 1.0                |
| K = 3              | R-Squared = 0.9995593550108559 |
| K = 4              | R-Squared = 0.9990085487744258 |
| K = 5              | R-Squared = 0.9981972704760524 |
| K = 6              | R-Squared = 0.9962830423185318 |
| K = 7              | R-Squared = 0.9926471351287468 |
| K = 8              | R-Squared = 0.9874851222008438 |
| K = 9              | R-Squared = 0.9811406678538648 |
| K = 10             | R-Squared = 0.9741903583427135 |
| K = 11             | R-Squared = 0.9672642399601562 |
| K = 12             | R-Squared = 0.9609533864392326 |
| K = 13             | R-Squared = 0.9548456236156344 |
| K = 14             | R-Squared = 0.9489564720167566 |
| K = 15             | R-Squared = 0.9437796719300492 |
| K = 16             | R-Squared = 0.9387406912951974 |
| K = 17             | R-Squared = 0.9329824772193863 |
| K = 18             | R-Squared = 0.927666367525943  |
| K = 19             | R-Squared = 0.9225021088721046 |
| K = 20             | R-Squared = 0.9179018794946261 |
| K = 21             | R-Squared = 0.9141054223798999 |
| K = 22             | R-Squared = 0.9115059004522543 |
| K = 23             | R-Squared = 0.9087390908880341 |
| K = 24             | R-Squared = 0.9059594632009164 |
| K = 25             | R-Squared = 0.9035597243252415 |
| K = 26             | R-Squared = 0.9021295325295613 |
| K = 27             | R-Squared = 0.9002360214364071 |
| K = 28             | R-Squared = 0.8979663747128075 |
| K = 29             | R-Squared = 0.895956967018984  |
| K = 30             | R-Squared = 0.8936775644710495 |
| Nilai k terbaik: 1 |                                |

Dari table tersebut dapat dilihat nilai K yang menghasilkan R-Squared 1 terdapat pada K1 dan K2. Namun jika nilai K yang terlalu kecil akan membuat model membentuk suato pola yang umun dan sulit untuk menyelesaikan permasalahan pola yang kompleks. Setelah dicoba hasil akurasi dari K1 - K9 yang tetap menghasilkan RMSE pada nilai 0 adalah K1-K6. Oleh karena itu diputuskan untuk menggunakan nilai k = 6 untuk tetap menjaga akurasi dan membuat model yang bisa membaca pola yang lebih kompleks

 

3. Memilih tiga model algoritma yang memiliki performa paling baik untuk nantinya dapat dievaluasi.

Beradarkan tahapan pelatihan dengan memanfaatkan Lazy Predict, maka didapatkan 3 algoritma dengan performa paling baik yaitu sebagai berikut :

 

\-     KNeighborsRegressor

KNeighborsRegressor yaitu sebuah kelas pada scikit-learn pada libraray pthon untuk kebutuhan machine learning yang dipakai untuk menerapkan algoritma K-Nearest Neighbors (K-Neighbors) dalam regresi dimana berfungsi dalam meramalkan nilai suatu variabel berkelanjutan berdasarkan nilai pada variabel prediksi yang ada.

 

Nilai target untuk label yang belum diketahui diperkirakan berdasarkan range nilai target dari k neighboars terdekat. Nilai k yang telah ditetapkan awalnya dipakai untuk menetapkan jumlah neighboars terdekat yang akan dipakai untuk perkiraan.

 

Gambar 4. Proses Kaneighboars

![Yuk Kenali Apa itu Algoritma K-Nearest Neighbors (KNN) - Trivusi](file:///C:/Users/LENOVO/AppData/Local/Packages/oice_16_974fa576_32c1d314_39f5/AC/Temp/msohtmlclip1/01/clip_image008.gif)

 

 

\-     DecisionTreeRegressor

Decision Tree Regressor adalah salah satu algoritma machine learning yang digunakan untuk mengatasi . Ini dapat digunakan untuk menyelesaikan kasus regresi . Memiliki 3 node yaitu Node Root, Node Interior, dan Node Leaf. Node Root merupakan node awal yang mempunyai seluruh sampel. Selain itu dapat dipecah menjadi node-node yang lain. Node Interior mempunyai fitur kumpulan data dan cabang-cabang mewakili aturan keputusan. Akhirnya, Node Leaf mewakili hasilnya. Algoritma ini sangat berguna untuk memecahkan masalah yang berhubungan dengan keputusan. Ilustrai dari struktur Decision tree Regressor terdapat pada Gambar 5

 

Gambar 5. Ilustrasi struktur decision tree regressor

![img](file:///C:/Users/LENOVO/AppData/Local/Packages/oice_16_974fa576_32c1d314_39f5/AC/Temp/msohtmlclip1/01/clip_image010.gif)

 

\-     ExtraTreeRegressor.

Algortima ini masih memiliki fungsi yang sama dengan decision tree regressor, yaitu untuk menyelesaikan tugas regresi untuk melakukan prediksi terhadap suatu variable. Pada Regresi Pohon Ekstra, pemisahan simpul dilakukan secara random serta tidak berdasarkan penelusuran threshold yang maksimal tidak seperti decision tree regressor sehingga dapat meminimalisir tingkat variasi dan mengoptimalkan kekuatan akan gangguan pada data. Selain itu, Extra tree regression juga menerapkan teknik bagging, yang mana sejumlah pohon regresi dibuat secara sejajar pada label-label data acak yang dipungut dengan pengalihan dari dataset latih sehingga meningkatkan tingkat akurasi dan mengurangi adanya overfitting. Tidak hanya itu, algoritma ini juga menerapkan pengacakan dalam proses pemilihan variabel prediktor yang dipakai untuk membagi node yang nantinya akan diambil untuk pertimbangan dalam pemecahan yang akan memperkuat variasi pohon-pohon.

 

Gambar 6. Struktur Extra Tree Regressor

![Structure of Extra Trees (Kapoor 2020). Extra Trees constructs the set... |  Download Scientific Diagram](file:///C:/Users/LENOVO/AppData/Local/Packages/oice_16_974fa576_32c1d314_39f5/AC/Temp/msohtmlclip1/01/clip_image012.gif)

## Evaluation

Dilakukan evaluasi dengan final report menggunakan model regresion dengan metrik Mean Squared Error (MSE), Root Mean Squared Error (RMSE), dan R-Squared (R2).

\* Mean Squared Error (MSE) 
 MSE dibutuhkan untuk mengetahui berapa nilai kesalahan pada prediksi. Nilai MSE yang rendah atau hampil nol menunjukkan bahwa hasil prediksi sesuai dengan data sebenarnya sehingga keaktualnnya dapat diperhitungkan untuk memprediksi di masa mendatang. 

MSE = ![img](file:///C:/Users/LENOVO/AppData/Local/Packages/oice_16_974fa576_32c1d314_39f5/AC/Temp/msohtmlclip1/01/clip_image014.gif)2

Diketahui:
 \- n = Jumlah Data
 \- yi = Actual Value / Nilai Sebenarnya
 \- ŷi = Predicted Value / Nilai Prediksi
 
 dari hasil final report, didapatkan MSE sebesar 0,00000 yang sesuai teori maka data prediksi yang didapatkan sesuai dengan data sebenernya untuk memprediksi kanker paru-paru berdasarkan 23 faktor tersebut.

*Root Mean Squared Error (RMSE)
 RMSE digunakan untuk mengukur tingkat akurasi hasil perkiraan model. Nilai RMSE yang rendah menunjukkan bahwa variasi nilai model perkiraan / prediksi (ŷ) hampir sama dengan variasi nilai sebenarnya (y) dan juga menunjukkan bahwa nilai yang diprediksi dan diamati lebih dekat satu sama lain. 

RMSE = ![img](file:///C:/Users/LENOVO/AppData/Local/Packages/oice_16_974fa576_32c1d314_39f5/AC/Temp/msohtmlclip1/01/clip_image016.gif)2

Diketahui:
 \- n = Jumlah Data
 \- yi = Actual Value / Nilai Sebenarnya
 \- ŷi = Predicted Value / Nilai Prediksi

dari hasil final report, didapatkan RMSE sebesar 0,00000 yang sesuai teori maka data prediksi yang didapatkan sesuai dengan data sebenernya untuk memprediksi kanker paru-paru berdasarkan 23 faktor tersebut.

*R-Squared (R2)
 R-Squared menunjukkan seberapa seberapa besar kombinasi variabel independen (variabel yang nilainya dapat dimanipulasi dan diatur) berdampak pada nilai variabel dependen (variabel yang nilainya ditentukan oleh variabel independen). Angkanya berkisar antara 0 dan 1 yang dimana angka 1 menunjukkan bahwa model regresi yang dihasilkan lebih baik.

R2 = ![img](file:///C:/Users/LENOVO/AppData/Local/Packages/oice_16_974fa576_32c1d314_39f5/AC/Temp/msohtmlclip1/01/clip_image018.gif)

Diketahui:
 \- SSRes : Kuadrat dari selisih nilai Y prediksi dengan nilai rata-rata 
                Y = ∑ (Ypred – Yrata-rata)²
 
 \- SSTotal : Kuadrat dari selisih nilai Y aktual dengan nilai rata-rata 
               Y = ∑ (Yaktual – Yrata-rata)²
 
 dari hasil final report, didapatkan R2 sebesar 1,00000 yang sesuai teori maka model regresi ini menghasilkan data yang baik untuk memprediksi kanker paru-paru. 

Tabel 3. Hasil Pengujian

|       | **Model_Name**          | **mse**   | **r2**    | **rmse**  |
| ----- | ----------------------- | --------- | --------- | --------- |
| **0** | Kneighbors              | 0.0000000 | 1.0000000 | 0.0000000 |
| **1** | Decision Tree Regressor | 0.0000000 | 1.0000000 | 0.0000000 |
| **2** | Extra Tree Regressor    | 0.0000000 | 1.0000000 | 0.0000000 |

 

Setelah itu Membandingkan data sebenarnya dengan hasil prediksi dapat dilihat pada table 4. 

Tabel 4. Hasil Perbandingan Data Sebenarya dengan hasil Prediksi

|         | **y_true** | **prediksi_K** | **prediksi_D** | **prediksi_E** |
| ------- | ---------- | -------------- | -------------- | -------------- |
| **204** | 1.0986123  | 1.1            | 1.1            | 1.1            |
| **71**  | 0.6931472  | 0.7            | 0.7            | 0.7            |
| **594** | 0          | 0              | 0              | 0              |
| **672** | 0          | 0              | 0              | 0              |
| **14**  | 0          | 0              | 0              | 0              |
| **...** | ...        | ...            | ...            | ...            |
| **647** | 1.0986123  | 1.1            | 1.1            | 1.1            |
| **797** | 1.0986123  | 1.1            | 1.1            | 1.1            |
| **605** | 0          | 0              | 0              | 0              |
| **611** | 0          | 0              | 0              | 0              |
| **988** | 1.0986123  | 1.1            | 1.1            | 1.1            |

##  

## Conclussion

\1.     Berdasarkan hasil pengolahan data yang dilakukan, didapatkan 23 kolom yang memengaruhi Kanker Paru-paru yaitu *age* (usia), *gender* (jenis kelamin), *air pollution* (polusi udara), *alcohol use* (konsumsi alkohol), *dust allergy* (alergi debu), *occupational hazards* (bahaya profesi), *genetic risk* (risiko genetik), *chronic lung disease* (penyakit paru-paru kronis), *balanced diet* (diet seimbang), *obesity* (kegemukan), *smoking* (merokok), *passive smoker* (perokok pasif), *chest pain* (nyeri dada), *coughing of blood* (batuk berdarah), *fatigue* (kelelahan), *weight loss* (penurunan berat badan), *shortness of breath* (sesak nafas), *wheezing* (mengi), *swallowing difficulty* (susah menelan), *clubbing of finger nails* (kuku jari tabuh), *frequent cold* (sering pilek), *dry cough* (batuk kering), *snoring* (mendengkur)

\2.     Dilakukan *cleaning data* untuk mengubah data yang asli (numerik) menjadi data kategorik level agar nanti dapat dicari korelasinya

\3.     Untuk mengukur seberapa jauh model regresi memprediksi kanker paru-paru yang akurat digunakan metrik Mean Squared Error (MSE), Root Mean Squared Error (RMSE), dan R-squared (R2). Dengan hasil 0.00000, 1.00000, 0.00000 dimana ketiga hasil tersebut menunjukkan bahwa data prediksi memiliki keakuratan yang tinggi berdasarkan data sebenarnya. Sehingga dapat digunakan untuk memprediksi di masa mendatang.
 

## Referensi

[1] *Lung cancer statistics | World Cancer Research Fund International*. (n.d.). WCRF International. https://www.wcrf.org/cancer-trends/lung-cancer-statistics/

[2] Bunjaku, J., Lama, A., Pesanayi, T., Shatri, J., Chamberlin, M., & Hoxha, I. (2023, June). Lung Cancer and Lifestyle Factors. *Hematology/Oncology Clinics of North America*. https://doi.org/10.1016/j.hoc.2023.05.018

[3] Deboever, N., Eisenberg, M. A., Antonoff, M. B., Hofstetter, W. L., Mehran, R. J., Rice, D. C., Roth, J. A., Sepesi, B., Swisher, S. G., Vaporciyan, A. A., Walsh, G. L., & Rajaram, R. (2023, June). Perspectives, Risk Factors, and Coping Mechanisms in Patients with Self-Reported Financial Burden following Lung Cancer Surgery. *The Journal of Thoracic and Cardiovascular Surgery*. https://doi.org/10.1016/j.jtcvs.2023.05.044

[4] Setyotini, Maria. (2020). Analisis Perbandingan Metode Machine Learning: RandomForest dan Support Vector Machine untuk Deteksi Kanker Paru-Paru. https://repository.unej.ac.id/