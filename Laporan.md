# **Sistem Rekomendasi Produk Amazon Berbasis Colaborative Filtering**

## **1. Latar Belakang**

Dalam era digital yang terus berkembang, e-commerce telah menjadi pilar utama dalam transformasi ekonomi global. Kemudahan akses, beragamnya pilihan produk, dan fleksibilitas transaksi telah mendorong pertumbuhan pesat sektor ini. Namun, pertumbuhan tersebut juga membawa tantangan baru, terutama dalam hal membantu konsumen menemukan produk yang sesuai dengan preferensi mereka di tengah lautan pilihan yang tersedia. Namun, pertumbuhan ini juga membawa tantangan baru, seperti "information overload" atau kelebihan informasi, yang dapat membingungkan konsumen dalam memilih produk yang sesuai dengan kebutuhan mereka.

Untuk mengatasi tantangan tersebut, sistem rekomendasi menjadi solusi krusial dalam e-commerce. Sistem ini membantu menyaring informasi dan memberikan rekomendasi produk yang relevan berdasarkan preferensi dan perilaku pengguna. Menurut studi oleh [(Salunke & Nichite, 2022)](https://arxiv.org/abs/2212.13910). sistem rekomendasi dapat meningkatkan loyalitas pelanggan dan konversi penjualan dengan menyediakan rekomendasi yang dipersonalisasi dengan menganalisis data perilaku pengguna, sistem ini dapat memberikan rekomendasi produk yang relevan, meningkatkan pengalaman pengguna, dan mendorong penjualan serta sistem tidak hanya meningkatkan pengalaman pengguna tetapi juga berkontribusi signifikan terhadap peningkatan penjualan.

Salah satu pendekatan membangun sistem rekomendasi adalah Collaborative filtering. dimana pendekatan ini merupakan salah satu pendekatan populer dalam sistem rekomendasi, yang memanfaatkan data interaksi pengguna untuk menemukan pola dan memberikan rekomendasi. Pendekatan ini efektif dalam mengidentifikasi preferensi pengguna berdasarkan kesamaan dengan pengguna lain. [(Khodabandehlou, 2019)](https://www.inderscienceonline.com/doi/abs/10.1504/IJBIS.2019.101582)

Meskipun Begitu, Implementasi collaborative filtering juga menghadapi beberapa tantangan, seperti masalah cold start dan sparsity data. Untuk mengatasi hal ini, berbagai penelitian telah dilakukan. Misalnya, penelitian oleh [Hu et al. (2019)](https://journals.sagepub.com/doi/abs/10.1177/0040517518801200) mengeksplorasi algoritma collaborative filtering dalam konteks industri fashion e-commerce dan menunjukkan bahwa pendekatan ini efektif dalam meningkatkan akurasi rekomendasi . Selain itu, penerapan sistem rekomendasi berbasis collaborative filtering dapat membantu UMKM dalam meningkatkan penjualan melalui e-commerce [Khusnah et al. (2025)](https://ejournal.undip.ac.id/index.php/jsinbis/article/view/68333).

Implementasi sistem rekomendasi yang efektif menjadi hal yang krisial terutama bagi perusahaan e-commerce karena tidak hanya meningkatkan kepuasan pelanggan tetapi juga berdampak signifikan pada peningkatan pendapatan perusahaan. Menurut laporan dari [(KITRUM, 2023)](https://kitrum.com/blog/recommendation-systems-in-e-commerce-how-it-works), perusahaan e-commerce yang mengadopsi sistem rekomendasi mengalami peningkatan penjualan hingga 30% dan peningkatan nilai pesanan rata-rata sebesar 20% dari total penjualan yang ada dan menunjukan efektivitas dari penerapan sistem rekomendasi dalam aplikasi e-commerce.

Mengingat peran penting sistem rekomendasi dalam meningkatkan pengalaman pengguna dan kinerja bisnis di e-commerce, pembangunan sistem rekomendasi berbasis collaborative filtering menjadi sangat relevan. Dengan memanfaatkan data interaksi pengguna, sistem yang dikembangkan diharapkan  dapat memberikan rekomendasi yang lebih akurat dan relevan, meningkatkan kepuasan pelanggan, dan mendorong pertumbuhan bisnis serta memberikan kontribusi positif terhadap peningkatan kinerja platform e-commerce.

#### **Referensi:**

- [Recommender Systems in E-commerce](https://arxiv.org/abs/2212.13910)
- [Designing an e-commerce recommender system based on collaborative filtering using a data mining approach](https://www.inderscienceonline.com/doi/abs/10.1504/IJBIS.2019.101582)
- [Examining collaborative filtering algorithms for clothing recommendation in e-commerce](https://journals.sagepub.com/doi/abs/10.1177/0040517518801200)
- [Implementasi E-Commerce dengan Sistem Informasi Rekomendasi menggunakan Metode Collaborative Filtering untuk Pengembangan Penjualan pada UMKM](https://ejournal.undip.ac.id/index.php/jsinbis/article/view/68333)
- [Recommendation Systems in E-commerce: How It Works?](https://kitrum.com/blog/recommendation-systems-in-e-commerce-how-it-works/)

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

evaluasi dilakukan dengan pendekatan metrik berikut:

- Root Mean Squared Error (RMSE): Mengukur seberapa besar kesalahan prediksi sistem terhadap rating aktual.

- Mean Absolute Error (MAE): Mengukur kesalahan rata-rata prediksi rating tanpa memperbesar efek outlier.

- Coverage@N: Mengukur persentase produk unik yang berhasil direkomendasikan model dari seluruh produk yang tersedia, menunjukkan kemampuan model dalam memberikan rekomendasi yang beragam dan tidak monoton.

## **Data UnderStanding**

### 🔢 **Informasi Dataset**

Dataset ini terdiri dari:

- 1465 baris

- 16 kolom

Dataset ini merepresentasikan informasi mengenai ulasan dan interaksi pengguna terhadap produk-produk yang dijual di platform e-commerce Amazon. Data mencakup karakteristik produk, diskon, rating, serta informasi ulasan dari pengguna. Informasi ini sangat relevan untuk pembangunan sistem rekomendasi berbasis Collaborative Filtering karena memuat relasi antara pengguna dan produk

### **🧹 Kondisi Data**

Berdasarkan eksplorasi awal (EDA), kondisi dataset adalah sebagai berikut:

1. Tipe Data:
- Seluruh kolom saat ini bertipe object, termasuk kolom numerik seperti harga dan rating. Ini mengindikasikan perlunya preprocessing lanjutan seperti konversi tipe data sebelum digunakan dalam model (hanya pada data yang diperlukan konversinya).

```python
print(df.info())
```

| Kolom               | Non-Null Count | Dtype  |
| :------------------ | :------------- | :----- |
| product_id          | 1465           | object |
| product_name        | 1465           | object |
| category            | 1465           | object |
| discounted_price    | 1465           | object |
| actual_price        | 1465           | object |
| discount_percentage | 1465           | object |
| rating              | 1465           | object |
| rating_count        | 1463           | object |
| about_product       | 1465           | object |
| user_id             | 1465           | object |
| user_name           | 1465           | object |
| review_id           | 1465           | object |
| review_title        | 1465           | object |
| review_content      | 1465           | object |
| img_link            | 1465           | object |
| product_link        | 1465           | object |

2. Missing Value:
- Terdapat missing value pada kolom rating_count sebanyak 2 entri kosong. Kolom lain tidak memiliki nilai hilang.

```python
print(df.info())
```

| Kolom               | Jumlah Missing Values |
| :------------------ | :-------------------- |
| product_id          | 0                     |
| product_name        | 0                     |
| category            | 0                     |
| discounted_price    | 0                     |
| actual_price        | 0                     |
| discount_percentage | 0                     |
| rating              | 0                     |
| rating_count        | 2                     |
| about_product       | 0                     |
| user_id             | 0                     |
| user_name           | 0                     |
| review_id           | 0                     |
| review_title        | 0                     |
| review_content      | 0                     |
| img_link            | 0                     |
| product_link        | 0                     |

3. Data Duplikat:
- Tidak ditemukan baris duplikat. (0 duplikat).

```python
display(df.duplicated().sum())
```

```python
np.int64(0)
```

### **📚 Dataset yang digunakan:**
https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset

### **🧾 Variabel/Atribut pada Amazon Sales Dataset:**

**1. Users_id**

- ID unik untuk setiap siswa (identifikasi individual). ID pengguna terdiri dari range (1-1465).
- Catatan: Baris tersebut terdiri dari gabungan beberapa user (multiuser) dan akan bertambah ketika dilakukan pemisahan per baris sendiri.
- Karena sifatnya unik, ID tentu sangat digunakan digunakan sebagai fitur prediktor karena memuat informasi bermakna secara langsung terhadap user.

**2. product_id**

- ID unik (alphanumeric) untuk setiap produk di Amazon. Digunakan sebagai identifier utama untuk menghubungkan berbagai informasi tentang produk. Contoh: "B07XJ8C8F5", "B09W5XR9RT" dan id produk lainnya. ini juga sangat berpengaruh pada colaborative filtering

**3. product_name**
- Berisi Nama lengkap produk yang ditampilkan di halaman Amazon. Ini bisa mencakup nama merek, model, dan fitur utama. Contoh produk seperti: "Apple AirPods Pro (2nd Generation)"

**4. category**
- Kategori produk utama, biasanya satu dari: 'Computer', 'Electronics', 'Books', 'Clothing', 'Home & Kitchen', dll. Kategori ini penting untuk segmentasi dan analisis perilaku pengguna.

**5. discounted_price**
- Harga akhir produk setelah diskon. Aslinya berupa string (misal ₹500). Bisa digunakan untuk analisis pricing dan diskon. tetapi kurang dibutuhkan dalam colaborative filtering.

**6. actual_price**
- Harga asli produk sebelum potongan. tidak banyak yang bisa dimanfaatkan oleh fitur ini karena kita tidak menggunakannya dalam colaborative filtering

**7. discount_percentage**
- Persentase diskon yang diterapkan terhadap harga asli.yang membedakan dengan discounted price, diskon percentage adalah nilai diskon yang diberikan dan bukan harga akhir yang diberikan

**8. rating**
- Nilai rating yang diberikan (biasanya dalam skala 1–5). ini akan menjadi informasi penting pada pendekatan colaborative filtering dan juga perlu disesuaikan tipe dataya menjadi float.

**9. rating_count**
- Jumlah rating yang diberikan pengguna lain terhadap produk tersebut. menunjukkan berapa kali sebuah produk telah diberi rating secara keseluruhan, atau berapa banyak rating yang diterima oleh sebuah produk. Informasi ini adalah atribut dari produk itu sendiri, bukan interaksi spesifik antara user dan product.

**10. about_product**
- Deskripsi singkat produk yang biasanya ditulis oleh penjual atau sistem, bukan viewer. Ini bisa mencakup fitur, bahan, ukuran, dsb. Contoh: "Bluetooth-enabled wireless earphones with ANC"

**11. user_name**
- Nama pengguna yang memberikan ulasan. Nama tampilan pengguna (username) yang memberikan review. Ini bisa berupa nama asli atau pseudonim, tergantung preferensi pengguna Amazon.

**12. review_id**
- ID unik dari setiap review, digunakan sebagai primary key untuk ulasan. Format alfanumerik. Contoh: "R3U6J3XCKXQY8K". sama seperti user_id Baris tersebut terdiri dari gabungan beberapa user (multiuser) dan akan bertambah ketika dilakukan pemisahan per baris sendiri walaupun dalam kasus ini kita tidak menggunakannya.

**13. review_title**
- Judul singkat dari review yang ditulis oleh pengguna. Biasanya berupa kesan utama dalam satu kalimat. Contoh: "Worth every penny!"

**14. review_content**
- Isi lengkap ulasan pengguna terhadap produk. Bisa sangat bervariasi panjangnya — dari satu kalimat hingga beberapa paragraf. Data ini cocok untuk analisis sentimen dan NLP namun kurang memadai dalam kasus sistem rekomendasi kali ini.

**15. img_link**
- URL gambar utama produk di Amazon. Tipe data string. Digunakan dalam frontend display atau image-based analysis.

**16. product_link**
- URL halaman produk di situs Amazon. Bisa digunakan untuk scraping lanjutan atau redirect ke halaman aktual produk.

```python if recommendation_data['Place_Name'].duplicated().any():
```
