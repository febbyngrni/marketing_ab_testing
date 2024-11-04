# Marketing Analytics: A/B Testing Ads to Increase Conversions

**Report** : [Medium](https://medium.com/@febbyngrni/data-driven-marketing-ab-testing-ads-to-increase-conversions-18089917577c)<br>
**Dataset** : [Kaggle](https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing)

## Business Understanding
Mengukur dampak dari setiap kampanye pemasaran adalah langkah krusial untuk memastikan strategi yang tepat sasaran. Namun, banyak perusahaan yang menghadapi kesulitan dalam membuktikan efektivitas iklan yang diluncurkan dalam meningkatkan konversi pelanggan. Pengukuran hasil kampanye harus dilakukan secara jelas agar perusahaan tidak hanya dapat menarik perhatian pelanggan tetapi juga dapat mempengaruhi perilaku pelanggan secara signifikan.

Sebuah perusahaan pemasaran menghadapi tantangan dalam membuktikan efektivitas kampanye iklan yang telah diluncurkan, khususnya dalam hal peningkatan konversi pelanggan. Meski telah mengeluarkan biaya yang tidak sedikit, perusahaan belum memiliki data yang cukup untuk memastikan apakah iklan tersebut benar-benar mendorong perubahan yang signifikan dalam perilaku pelanggan. Untuk memperoleh gambaran yang lebih jelas tentang pengaruh iklan terhadap konversi, perusahaan memutuskan untuk menerapkan A/B Testing.

### Business Objectives
Tujuan dari analisis A/B Testing ini adalah sebagai berikut:
1. **Mengukur Efektivitas Iklan**: Menganalisis dampak dari berbagai versi iklan terhadap tingkat konversi untuk menentukan strategi yang paling efektif.
2. **Membandingkan Kinerja Iklan dengan Metode Pemasaran Lain**: Menganalisis kinerja iklan dibandingkan dengan pengumuman layanan publik, untuk menentukan pendekatan yang paling berhasil.

### Business Questions
Berikut adalah beberapa pertanyaan yang relevan untuk mengarahkan analisis ini:
1. Seberapa besar peningkatan tingkat konversi yang dihasilkan oleh iklan dibandingkan dengan pengumuman layanan publik?
2. Apa hari dan jam paling efektif untuk menampilkan iklan berdasarkan jumlah iklan yang dilihat dan konversi yang dicapai?
3. Apakah ada perbedaan signifikan dalam tingkat konversi antara pengguna yang melihat iklan dan pengguna yang melihat pengumuman layanan publik?

## Data
Dataset yang digunakan berasal dari Kaggle, terdiri dari 588.101 baris dan 7 fitur, yang mencakup:
- **User ID:** ID unik untuk setiap pengguna.
- **Test Group:** Menunjukkan apakah pengguna melihat iklan ("ad") atau PSA ("psa").
- **Converted:** Status konversi pengguna; "True" jika mereka melakukan pembelian, "False" jika tidak.
- **Total Ads:** Jumlah iklan yang dilihat oleh pengguna.
- **Most Ads Day:** Hari ketika pengguna melihat iklan terbanyak.
- **Most Ads Hour:** Jam ketika pengguna melihat iklan terbanyak.

### Preprocessing
1. **Data Balancing:** Menggunakan undersampling untuk menyeimbangkan data antara grup treatment dan kontrol guna menghindari bias akibat ketidakseimbangan sampel.
2. **Handling Outlier:** Memeriksa outlier pada variabel `total ads` untuk memastikan akurasi analisis.

## A/B Testing
**Uji Z untuk Proporsi:** Digunakan untuk membandingkan proporsi konversi antara dua kelompok, menentukan apakah perbedaan tersebut signifikan secara statistik.

### Results
![__results___61_0](https://github.com/user-attachments/assets/774e7175-d1eb-4599-8ae8-3ae79870a50f)
- Z-statistic: 6.1291
- P-value: 0.0000
- Nilai Kritis Z: 1.6449
- Interval Kepercayaan: (0.0056, 0.0110)
Hasil menunjukkan bukti statistik yang kuat yang mendukung hipotesis alternatif bahwa tingkat konversi pada grup treatment (yang melihat iklan) lebih tinggi dibandingkan dengan grup kontrol (yang melihat PSA).

## Kesimpulan dan Rekomendasi
- **Efektivitas Iklan:** Iklan memiliki efek positif terhadap tingkat konversi pengguna, dengan grup treatment menunjukkan tingkat konversi lebih tinggi dibandingkan dengan grup kontrol.
- **Interval Kepercayaan:** Dengan keyakinan 95%, selisih proporsi konversi antara grup treatment dan kontrol berada dalam rentang 0.0056 hingga 0.0110, yang menunjukkan bahwa iklan meningkatkan kemungkinan konversi pengguna sebesar 0.56% hingga 1.1%.
- **Distribusi Penayangan Iklan**: Analisis distribusi penayangan iklan berdasarkan waktu dan hari menunjukkan bahwa faktor-faktor seperti waktu tayang dan hari tidak berpengaruh signifikan terhadap konversi.
