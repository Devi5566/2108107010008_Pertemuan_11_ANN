# 2108107010008_Pertemuan_11_ANN

Nama : Devi Anggraini
NPM : 2108107010008

## Dataset Klasifikasi

Dataset yang digunakan di ambil dari situs kaggel (https://www.kaggle.com/datasets/jillanisofttech/diabetes-disease-updated-dataset).
Data ini terdiri dari beberapa atribut sebagai berikut:
- Kehamilan (Pregnancies): Jumlah kehamilan yang pernah dialami oleh pasien.
- Glukosa (Glucose): Konsentrasi glukosa plasma 2 jam setelah tes toleransi glukosa oral.
- Tekanan darah (BloodPressure): Tekanan darah diastolik (mm Hg).
- Ketebalan Kulit (	SkinThickness): Ketebalan lipatan kulit trisep (mm).
- Insulin (Insulin): Kadar insulin serum 2 jam setelah pemberian glukosa (mu U/ml).
- IMT (Indeks Massa Tubuh)/ (BMI): IMT (berat dalam kg/(tinggi dalam m)^2).
- Fungsi Pedigree Diabetes (DiabetesPedigreeFunction): Nilai fungsi pedigri diabetes.
- Usia (Age): Usia pasien (tahun).
- Hasil (Outcome): Variabel kelas yang menunjukkan apakah pasien dinyatakan positif (1) atau negatif (0) terhadap diabetes.
Dataset ini berisi 768 instansi dengan 8 atribut numerik dan satu atribut kelas. Semua pasien dalam dataset ini adalah wanita setidaknya berusia 21 tahun dengan warisan Indian Pima.

Tujuannya adalah untuk memprediksi apakah seorang pasien memiliki diabetes berdasarkan pengukuran diagnostik.


## Dataset Regresi

Dataset yang digunakan pada tugas kali ini adalah dataset Medical Cost Personal Datasets yang di ambil dari situs kaggle (https://www.kaggle.com/datasets/mirichoi0218/insurance). Dataset ini berisi informasi tentang biaya medis individu, termasuk atribut seperti usia, jenis kelamin, indeks massa tubuh (BMI), jumlah anak yang ditanggung oleh asuransi kesehatan, apakah perokok atau tidak, dan wilayah tempat tinggal di Amerika Serikat.

Informasi Atribut:
Atribut input dan output adalah sebagai berikut:

- Usia (age): Usia penerima utama asuransi.
- Jenis Kelamin (sex): Jenis kelamin kontraktor asuransi, perempuan atau laki-laki.
- Indeks Massa Tubuh (BMI): Indeks massa tubuh, memberikan pemahaman tentang berat badan yang relatif tinggi atau rendah terhadap tinggi badan, merupakan indeks objektif berat badan (kg / m ^ 2) menggunakan rasio tinggi terhadap berat badan, idealnya 18.5 hingga 24.9.
- Jumlah Anak (children): Jumlah anak yang ditanggung oleh asuransi kesehatan atau jumlah tanggungan.
- Perokok (smoker): Status merokok, apakah perokok atau tidak.
- Wilayah (region): Wilayah tempat tinggal penerima asuransi di Amerika Serikat, termasuk northeast, southeast, southwest, northwest.
- Biaya Medis (charges): Biaya medis individu yang ditagih oleh asuransi kesehatan.

Menggunakan data ini untuk mengetahui pengaruh riwayat seseorang dengan Biaya Medis


# Perbandingan antara hasil SVM dan ANN

## Klasifikasi

```
HASIL KLASIFIKASI UNTUK MODEL SUPPORT VECTOR MACHINE:

              precision    recall  f1-score   support

           0       0.81      0.84      0.83        99
           1       0.69      0.65      0.67        55

    accuracy                           0.77       154
   macro avg       0.75      0.75      0.75       154
weighted avg       0.77      0.77      0.77       154


HASIL KLASIFIKASI UNTUK MODEL ARTIFICIAL NEURAL NETWORK:

              precision    recall  f1-score   support

           0       0.78      0.78      0.78        99
           1       0.60      0.60      0.60        55

    accuracy                           0.71       154
   macro avg       0.69      0.69      0.69       154
weighted avg       0.71      0.71      0.71       154
```

Dari hasil klasifikasi, model Support Vector Machine (SVM) menunjukkan akurasi yang sedikit lebih tinggi dengan nilai 0.77 dibandingkan dengan model Artificial Neural Network (ANN) yang memiliki akurasi sebesar 0.71. Meskipun demikian, baik SVM maupun ANN menunjukkan performa yang relatif seimbang dalam memprediksi kelas positif dan negatif, seperti yang tercermin dari nilai precision, recall, dan f1-score yang serupa di antara keduanya.

## Regresi

```
Melatih Support Vector Machine (Regresi)...
Hasil evaluasi untuk Support Vector Machine (Regresi):
MAE: 8039.034086862273
MSE: 152487822.87840414
RMSE: 12348.595988143921
R2 Square 0.017783775666570634


Melatih Artificial Neural Network...
34/34 ━━━━━━━━━━━━━━━━━━━━ 2s 3ms/step - accuracy: 0.0000e+00 - loss: -31292.6699
9/9 ━━━━━━━━━━━━━━━━━━━━ 0s 9ms/step
Hasil evaluasi untuk Artificial Neural Network:
MAE: 12967.330701392048
MSE: 323400159.8541406
RMSE: 17983.33005464062
R2 Square -1.0831098376560795
```

Dari hasil evaluasi, terlihat bahwa model Support Vector Machine (Regresi) memiliki kinerja yang lebih baik daripada Artificial Neural Network dalam memprediksi target variabel. Hal ini diperkuat oleh nilai R-squared yang lebih tinggi pada model Support Vector Machine, menunjukkan bahwa model tersebut lebih baik dalam menjelaskan variasi dalam data. Namun, perlu diperhatikan bahwa baik model SVM maupun ANN memiliki Mean Absolute Error (MAE) dan Root Mean Squared Error (RMSE) yang cukup tinggi, menunjukkan bahwa keduanya memiliki tingkat kesalahan prediksi yang signifikan.
