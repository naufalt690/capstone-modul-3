# capstone-modul-3

## **Business Understanding: Asuransi Perjalanan Syariah**

Asuransi Perjalanan Syariah adalah suatu bentuk layanan keuangan yang diberikan oleh perusahaan asuransi berdasarkan prinsip-prinsip syariah dalam rangka melindungi peserta asuransi dari risiko-risiko yang mungkin terjadi selama perjalanan. Layanan ini diperuntukkan bagi individu yang melakukan perjalanan baik dalam negeri maupun luar negeri dengan memberikan jaminan terhadap berbagai kemungkinan risiko seperti kecelakaan, sakit, atau kehilangan barang berharga.

#### **Nilai-nilai Asuransi Syariah:**

- **Prinsip Maqashid Syariah:** Asuransi Perjalanan Syariah beroperasi berdasarkan prinsip-prinsip syariah, yang melibatkan adanya keadilan, transparansi, dan Terukur. Produk-produk asuransi yang ditawarkan dirancang untuk memastikan kepatuhan terhadap hukum Islam.

- **Struktur Produk:** Produk asuransi travel syariah dirancang dengan struktur yang mematuhi hukum Islam. Ini termasuk ketentuan-ketentuan yang menghindari unsur-unsur riba (bunga), perjudian, dan ketidakpastian yang berlebihan.

- **Lingkup Jaminan:** Asuransi Perjalanan Syariah mencakup berbagai risiko yang mungkin dihadapi peserta asuransi selama perjalanan, seperti kecelakaan, penyakit, pembatalan perjalanan, atau kerugian materi.

- **Mitigasi Risiko:** Tujuan utama Asuransi Perjalanan Syariah adalah untuk memberikan perlindungan finansial dan kenyamanan bagi peserta asuransi. Proses klaim dan penanganan risiko dilakukan secara adil dan sesuai dengan prinsip-prinsip syariah.

- **Edukasi Peserta Asuransi:** Sebagai bagian dari prinsip syariah, perusahaan asuransi menyediakan edukasi kepada peserta asuransi mengenai produk asuransi yang mereka pilih, hak dan kewajiban, serta proses klaim.

- **Keterlibatan Masyarakat:** Asuransi Perjalanan Syariah berupaya untuk terlibat aktif dalam kegiatan sosial dan kegiatan amal sebagai bentuk kontribusi positif terhadap masyarakat, sesuai dengan nilai-nilai syariah.

Melalui penjelasan  tersebut asuransi travel syariah bertujuan untuk memberikan solusi pembiyayaan yang sesuai dengan prinsip-prinsip syariah bagi individu yang melakukan perjalanan bisnis dan wisata, sekaligus mempromosikan nilai-nilai islam secara etis dan sosial dalam konteks layanan keuangan.

#### **TUJUAN DARI PEMBUATAN MACHINE LEARNING**
Dari penjelasan mengenai perusahaan asuransi diatas penulis akan merumuskan sebuah permasalaan yang terjadi di perusahaan, intinya adalah perusahaan ingin mengukur kelayakan seseorang pemegang polis yang mendapatkan uang `Claim` dengan model machine learning (ML). Sehingga dari adanya pembuatan model ini perusahaan tetap bisa mendapatkan keuntungan yang wajar, perusahaan mendapatkan memiliki kredibilitas nama baik di masyarakat, serta perusahaan tetap berpegang teguh pada `prinsip maqashid syariah` yaitu keadilan. Selanjutnya,tujuan lain dari pembuatan model ML ini untuk memahami profil pemegang polis berdasarkan status klaim dan jenis produk asuransi yang cenderung memiliki tingkat klaim yang rendah. Intinya adalah informasi ini akan menjadi dasar penting dalam merancang apa saja syarat dan ketentuan `Claim` yang dapat diterima oleh calon pemegang polis selama proses pengajuan. Selain itu, pembuatan model ML ini akan berkontribusi pada penyusunan strategi penjualan yang lebih optimal. 

#### **MODEL DAN METRIK EVALUASI**
pada pembahasan model ini penulis menguji semua model untuk melihat model apa yang cocok untuk dipakai ML ini, serta mengambil 2 model yang terbaik, adapun model yang akan diuji adalah seperti berikut: `Logistic Regression, K Neighbors Classifier, Decision Tree Classifier,  XG Boost Classifier, Random Forest Classifier, Gradient Boosting Classifier, Ada Boost Classifier, Light Gradient Boosting Machine Classifier, Cat Boost Regressor`. selanjutnya, penulis juga membuat model dengan menggunakan `confussion matrix` yakni sebagai berikut:

| **Actual/Predict**         	| **Prediksi "Claim" "1"** 	| **Prediksi "Not Claim" "0"** 	|
|----------------------------	|--------------------------	|------------------------------	|
| **Actual "Claim" "1"**     	| True Positive (TP)       	| False Negative (FN)          	|
| **Actual "Not Claim" "0"** 	| False Positive (FP)      	| True Negative (TN)           	|

- **`TP`** = merupakan suatu kondisi `ML` ini menebak dengan tepat orang yang `layak mendapatkan` `Claim`.
- **`TN`** = merupakan suatu kondisi `ML` ini menebak dengan tepat orang yang `tidak layak mendapatkan` `Claim`.
- **`FP`** = merupakan suatu kondisi `ML` ini `tidak bisa memprediksi dengan benar` orang yang melakukan `Claim`, padahal `realitanya pemegang polis tidak` melakukan `Claim`. untuk masalah konsekuensi yang ditimbulkan dari kelsalahan prediksi ini adalah cuma uang dari perusahaan menganggur. Juga tidak berdampak merugikan terhadap perusahaan.
- **`FN`** = merupakan suatu kondisi `ML` ini `tidak bisa memprediksi dengan benar` orang yang `tidak melakukan Claim`, padahal `realitanya pemegang polis` melakukan `Claim`. dampak dari adanya masalah ini besar sebab dari sisi penerapan `maqashid syariah` tidak bisa menerapkan konsep `al-adlu` (keadilan), dimana perusahaan melakukan praktik kecurangan. selain itu dampak lain yang ditimbulkan adalah kredibilitas nama perusahaan rusak.<br>

Setelah menilai dampak yang ditimbulkan dari ke 4 nilai confussion matrix diatas bahwa `false negative` memiliki dampak yang paling besar, sehingga konsern penulis pada penentuan matrix ini adalah dengan menggunakan matrix `Recall` dimana penulis ingin fokus untuk mengurangi nilai `FN`, dan memaksa nilai `FN` tersebut menuju `true positive`. Rumusnya adalah rasio antara jumlah prediksi positif yang benar (TP) dengan total kasus positif yang sebenarnya (TP + FN). Recall ditujukan mengukur seberapa baik model dapat menemukan semua kasus positif yang sebenarnya.

selepas menentukan model diatas maka langkah untuk menaikan kinerja model tersebut dengan menggunakan hyperparameter tunning.



# **KESIMPULAN DAN REKOMENDASI**
untuk kesimpulannya adalah sebagai berikut:


- Metrik yang dipilih pada model ini adalah `recall` karena perusahaan asuransi syariah ini berpegang teguh pada nilai keadilan yang sesuai dengan prinsip maqashid syariah. Dengan memilih `recall`, perusahaan fokus untuk memberikan hak yang seharusnya kepada nasabah, khususnya dalam hal klaim asuransi.

- Untuk encoding data, dilakukan pada kolom 'Agency', 'Agency Type', 'Distribution Channel', 'Product Name', dan 'Claim'. Sementara itu, scaling hanya diterapkan pada kolom 'Duration', 'Net Sales', 'Commision (in value)', dan 'Age'.

- Model yang digunakan adalah Random Forest dan LGBMClassifier, dengan random state=42. Tingkat keberhasilan model Random Forest meningkat dari 86.95% sebelum tuning menjadi 87.82% setelah tuning. Faktor penting yang memengaruhi prediksi model ini adalah fitur 'Commision (in value)' dan 'Duration', dengan tingkat importance tertinggi. Fitur 'Age', 'Net Sales', hingga 'Agency_C2B' memiliki importance yang lebih rendah. Pada interpretasi plot tree, fitur 'Commission (in value)' menjadi head root, diikuti oleh 'Product Name_Cancellation Plan' dan 'Age' sebagai cabang-cabang dari plot tree tersebut.

- Model LGBMClassifier memiliki tingkat akurasi sebesar 85.21%, tanpa peningkatan setelah dilakukan hyperparameter tuning. Fitur yang paling berpengaruh pada model ini adalah "Net Sales" dan "Duration". Sedangkan fitur "Product Name_Basic Plan", "Agency Type_Airlines", dan "Distribution Channel_Offline" memiliki pengaruh yang lebih rendah.

- Pada interpretasi LIME, dapat disimpulkan bahwa fitur 'Agency_C2B' memiliki nilai interpretasi paling tinggi dan cenderung ke arah negatif. Sementara itu, fitur 'Net Sales' memiliki kecenderungan positif namun dengan peluang yang relatif kecil. Fitur 'Agency Type_Airlines' dan 'Product Name_Basic Plan' juga memiliki pengaruh yang tidak begitu signifikan pada model.


#### **KETERBATASAN MODEL**

Model yang telah dikembangkan memiliki beberapa keterbatasan yang perlu diperhatikan:

1. **Keterbatasan pada Variabel 'Agency':**
   - Model hanya mampu menghandle unique values pada variabel yaitu: `C2B, EPX, JZI, CWT, LWC, ART, CSR, SSI, RAB, KML, TST, TTW, JWT, ADM, CCR, CBH`.
   - Jika terdapat nilai unik lain di luar kategori tersebut, model tidak bisa memberikan hasil prediksi yang akurat.

2. **Keterbatasan pada Variabel 'Agency Type':**
   - Model hanya dapat memproses dua unique values pada variabel `'Agency Type'`, yaitu: `Airlines` dan `Travel Agency`.
   - Jikalau ada jenis agensi lainnya maka model dapat diolah dengan baik.

3. **Keterbatasan pada Variabel 'Distribution Channel':**
   - Variabel 'Distribution Channel' hanya dapat menghandle dua kategori, yaitu: `Online` dan `Offline`.
   - Jika terdapat kategori distribusi lainnya, model tidak dapat memberikan hasil optimal.

4. **Keterbatasan pada Variabel 'Product Name':**
   - Model mempertimbangkan sejumlah kategori produk asuransi tertentu seperti `Annual Silver Plan, Cancellation Plan, Basic Plan, 2 way Comprehensive Plan`, dan lain-lain.
   - Jika ada produk selain yang diatas maka prediksi model kurang akurat.

5. **Keterbatasan pada Variabel 'Duration':**
   - Variabel 'Duration' hanya dapat memproses rentang nilai antara `0` hingga `365` atau setara dengan 1 tahun.

6. **Keterbatasan pada Variabel 'Net Sales':**
   - Variabel 'Net Sales' hanya mampu mengakomodasi rentang nilai antara `-$357` hingga `$682`.
   - Jika terdapat nilai `net sales` lebih dari rentang tersebut, model pasti memberikan hasil yang kurang optimal.

7. **Keterbatasan pada Variabel 'Commision (in value)':**
   - Variabel `'Commision (in value)'` hanya dapat memproses komisi dalam rentang sekitar `$0` hingga `$210`.
   - Komisi di luar rentang ini mungkin tidak dapat diinterpretasikan dengan baik oleh model.

8. **Keterbatasan pada Variabel 'Age':**
   - Pada variabel `'Age'` hanya dapat memproses umur dalam rentang dari beberapa bulan (`0`) hingga `80` tahun.
   - Umur di luar rentang ini mungkin tidak sesuai dengan kapabilitas model.

Dengan memahami keterbatasan-keterbatasan tersebut, user dapat memastikan bahwa data yang akan dimasukkan ke dalam model sesuai dengan karakteristik yang telah dijelaskan di atas untuk mendapatkan hasil prediksi yang lebih akurat.





### **REKOMENDASI**

Penulis memberikan rekomendasi yang dapat diterapkan oleh perusahaan asuransi syariah, baik dari aspek bisnis maupun aspek model:

1. **Rekomendasi Dari Aspek Bisnis:**
   - **Paket Layanan Khusus Asia Tenggara:** Perusahaan disarankan untuk menyusun paket layanan asuransi yang khusus ditujukan untuk beberapa negara di Asia, seperti Singapura, Malaysia, Thailand, Indonesia, dan Filipina. paket ini dapat menarik minat pemegang polis asuransi yang berencana melakukan perjalanan ke wilayah tersebut.
   - **Penekanan pada Penjualan Online:** Mengingat tren pembelian asuransi secara online yang semakin meningkat, perusahaan sebaiknya memperkuat strategi pemasaran online dan memberikan insentif kepada nasabah yang membeli asuransi melalui platform online.
   - **Paket Asuransi Jangka Waktu Panjang:** Menyusun paket asuransi dengan fokus pada jangka waktu panjang, seperti paket bulanan atau mingguan, dapat menjadi alternatif menarik bagi pemegang polis.
   - **Insentif Komisi untuk Agen Berkualitas:** Memberikan bonus komisi kepada agen yang berhasil mempertahankan rating tinggi dapat meningkatkan motivasi agen dan kualitas layanan yang diberikan kepada nasabah.
   - **Optimasi Produk Asuransi:** Menghapus produk asuransi dengan tingkat penjualan premi yang rendah, atau menggabungkan beberapa jenis premi, dapat membantu mengoptimalkan portofolio produk asuransi.

2. **Rekomendasi Dari Aspek Model:**
   - **Pengelolaan Fitur Sensitive:** Sebelum membangun model ML, disarankan untuk melakukan penghapusan fitur yang berpotensi mendatangkan bias, seperti jenis kelamin dan kebangsaan, guna menghindari prediksi yang tidak adil.
   - **Peningkatan Data Minoritas:** Untuk meningkatkan kinerja model, disarankan untuk menambahkan data pada kelas minoritas, khususnya pada kategori nasabah yang tidak melakukan klaim. Hal ini dapat meningkatkan kemampuan model dalam memprediksi dengan tepat.
   - **Eksplorasi Model Lain:** Melakukan eksplorasi terhadap model supervised learning lainnya sesuai dengan tujuan bisnis dan matriks evaluasi yang sesuai. Model alternatif dapat memberikan sudut pandang yang berbeda.
   - **Penambahan Fitur Tambahan:** Menambahkan kolom baru seperti premi yang dibayarkan oleh nasabah dan fitur keperluan perjalanan, seperti tujuan perjalanan (bisnis atau wisata), dapat memperkaya informasi yang dimiliki oleh model.
   - **Analisis Premi yang Dibayarkan oleh Perusahaan:** Menambahkan kolom baru yang mencatat premi yang dibayarkan oleh perusahaan kepada nasabah dapat memberikan wawasan tambahan mengenai pola pembayaran premi.

Rekomendasi ini diharapkan dapat membantu perusahaan dalam meningkatkan kinerja bisnis dan model prediktif, serta memberikan nilai tambah bagi nasabah yang lebih baik.
