## **Sistem Rekomendasi Produk Amazon Berbasis Colaborative Filtering**

## **1. Latar Belakang**

Dalam era digital yang terus berkembang, e-commerce telah menjadi pilar utama dalam transformasi ekonomi global. Kemudahan akses, beragamnya pilihan produk, dan fleksibilitas transaksi telah mendorong pertumbuhan pesat sektor ini. Namun, pertumbuhan tersebut juga membawa tantangan baru, terutama dalam hal membantu konsumen menemukan produk yang sesuai dengan preferensi mereka di tengah lautan pilihan yang tersedia. Namun, pertumbuhan ini juga membawa tantangan baru, seperti "information overload" atau kelebihan informasi, yang dapat membingungkan konsumen dalam memilih produk yang sesuai dengan kebutuhan mereka.

Untuk mengatasi tantangan tersebut, sistem rekomendasi menjadi solusi krusial dalam e-commerce. Sistem ini membantu menyaring informasi dan memberikan rekomendasi produk yang relevan berdasarkan preferensi dan perilaku pengguna. Menurut studi oleh [(Salunke & Nichite, 2022)](https://arxiv.org/abs/2212.13910). sistem rekomendasi dapat meningkatkan loyalitas pelanggan dan konversi penjualan dengan menyediakan rekomendasi yang dipersonalisasi dengan menganalisis data perilaku pengguna, sistem ini dapat memberikan rekomendasi produk yang relevan, meningkatkan pengalaman pengguna, dan mendorong penjualan serta sistem tidak hanya meningkatkan pengalaman pengguna tetapi juga berkontribusi signifikan terhadap peningkatan penjualan.

Salah satu pendekatan membangun sistem rekomendasi adalah Collaborative filtering. dimana pendekatan ini merupakan salah satu pendekatan populer dalam sistem rekomendasi, yang memanfaatkan data interaksi pengguna untuk menemukan pola dan memberikan rekomendasi. Pendekatan ini efektif dalam mengidentifikasi preferensi pengguna berdasarkan kesamaan dengan pengguna lain. [(Khodabandehlou, 2019)](https://www.inderscienceonline.com/doi/abs/10.1504/IJBIS.2019.101582)

Meskipun Begitu, Implementasi collaborative filtering juga menghadapi beberapa tantangan, seperti masalah cold start dan sparsity data. Untuk mengatasi hal ini, berbagai penelitian telah dilakukan. Misalnya, penelitian oleh [Hu et al. (2019)](https://journals.sagepub.com/doi/abs/10.1177/0040517518801200) mengeksplorasi algoritma collaborative filtering dalam konteks industri fashion e-commerce dan menunjukkan bahwa pendekatan ini efektif dalam meningkatkan akurasi rekomendasi . Selain itu, penerapan sistem rekomendasi berbasis collaborative filtering dapat membantu UMKM dalam meningkatkan penjualan melalui e-commerce [Khusnah et al. (2025)](https://ejournal.undip.ac.id/index.php/jsinbis/article/view/68333).

Implementasi sistem rekomendasi yang efektif menjadi hal yang krisial terutama bagi perusahaan e-commerce karena tidak hanya meningkatkan kepuasan pelanggan tetapi juga berdampak signifikan pada peningkatan pendapatan perusahaan. Menurut laporan dari [(KITRUM, 2023)](https://kitrum.com/blog/recommendation-systems-in-e-commerce-how-it-works), perusahaan e-commerce yang mengadopsi sistem rekomendasi mengalami peningkatan penjualan hingga 30% dan peningkatan nilai pesanan rata-rata sebesar 20% dari total penjualan yang ada dan menunjukan efektivitas dari penerapan sistem rekomendasi dalam aplikasi e-commerce.

Mengingat peran penting sistem rekomendasi dalam meningkatkan pengalaman pengguna dan kinerja bisnis di e-commerce, pembangunan sistem rekomendasi berbasis collaborative filtering menjadi sangat relevan. Dengan memanfaatkan data interaksi pengguna, sistem yang dikembangkan diharapkan  dapat memberikan rekomendasi yang lebih akurat dan relevan, meningkatkan kepuasan pelanggan, dan mendorong pertumbuhan bisnis serta memberikan kontribusi positif terhadap peningkatan kinerja platform e-commerce.

#### **Referensi:**

- [Recommender Systems in E-commerce]([https://kitrum.com/blog/recommendation-systems-in-e-commerce-how-it-works](https://arxiv.org/abs/2212.13910))

## **Problem Statement**

Berdasarkan latar belakang yang dibahas, berikut ini adalah pernyataan masalah yang dihadapi tentang perfoma belajar siswa:

1. Sistem e-commerce kurang mampu memberikan rekomendasi produk yang relevan secara personal kepada masing-masing pengguna.

2. Jumlah interaksi pengguna dengan produk cenderung sparsity (jarang), sehingga menyulitkan model dalam memahami preferensi pengguna secara menyeluruh.

3. kurangnya pengunaan metrik terukur yang digunakan untuk mengevaluasi seberapa baik sistem rekomendasi bekerja dalam menyajikan produk yang tepat dan mencakup berbagai jenis produk.

## **Goals**

Berdasarkan latar belakang yang dibahas, Mengembangkan dan menerapkan model sistem rekomendasi berbasis colaborative filtering bertujuan untuk:

1. Mengembangkan sistem rekomendasi berbasis Collaborative Filtering untuk menyarankan produk yang relevan sesuai preferensi masing-masing pengguna.

2. Mengatasi tantangan data sparsity dengan pendekatan embedding dan pemetaan interaksi user–item menggunakan neural network untuk mempelajari representasi pengguna dan produk.

3. Mengevaluasi sistem rekomendasi menggunakan metrik terukur seperti RMSE, MAE, dan Coverage untuk menilai akurasi prediksi dan keragaman produk yang direkomendasikan.

## **Solution Statements**

- Mengembangkan model Collaborative Filtering menggunakan pendekatan Neural Collaborative Filtering (NCF) dengan embedding layer untuk mempelajari representasi pengguna dan produk secara otomatis dari interaksi historis.

- Menerapkan dan mengukur performa model dengan metrik RMSE dan MAE untuk mengukur prediksi rating, serta metrik Coverage@N untuk menilai seberapa luas model menjangkau variasi produk dalam rekomendasi.

### **Evaluasi:**

Sevaluasi dengan metrik berikut:

- Root Mean Squared Error (RMSE): Mengukur seberapa besar kesalahan prediksi sistem terhadap rating aktual.

- Mean Absolute Error (MAE): Mengukur kesalahan rata-rata prediksi rating tanpa memperbesar efek outlier.

- Coverage@N: Mengukur persentase produk unik yang berhasil direkomendasikan model dari seluruh produk yang tersedia, menunjukkan kemampuan model dalam memberikan rekomendasi yang beragam dan tidak monoton.
