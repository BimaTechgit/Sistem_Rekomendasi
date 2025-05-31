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

Berdasarkan latar belakang yang dibahas, berikut ini adalah pernyataan masalah yang dihadapi:

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

**1. Tipe Data:**
- Seluruh kolom saat ini bertipe object, termasuk kolom numerik seperti harga dan rating. Ini mengindikasikan perlunya preprocessing lanjutan seperti konversi tipe data sebelum digunakan dalam model (konversi hanya dilakukan pada data yang diperlukan).

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

**2. Missing Value:**
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

**3. Data Duplikat:**
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

## Exploratory Data Analysis (EDA)

![download (25)](https://github.com/user-attachments/assets/ce6c43cb-7879-4d06-96dc-7fe33e5fb693)

Berdasarkan visualisasi grafik yang menampilkan 10 kategori produk terpopuler , kita dapat melihat bahwa kategori produk sangat beragam namun tetap mencerminkan tren konsumsi modern yang didominasi oleh teknologi dan kebutuhan sehari-hari. Kategori dengan jumlah produk tertinggi adalah "Computers&Accessories|Accessories&Peripherals|Cables&Accessories|Cables|USBCables" , yang menunjukkan bahwa aksesori elektronik seperti kabel USB memiliki permintaan yang sangat tinggi. Hal ini tidak mengherankan, mengingat perangkat elektronik saat ini hampir selalu membutuhkan koneksi data yang cepat dan andal, serta kabel USB menjadi salah satu komponen penting dalam ekosistem teknologi modern. Dominasi kategori ini juga mencerminkan bagaimana pengguna cenderung membeli produk-produk pendukung untuk perangkat utama mereka, seperti laptop, smartphone, atau tablet.

Selain kabel USB, kategori elektronik lainnya seperti SmartWatches , Smartphones , dan SmartTelevisions juga mendominasi daftar terpopuler. Fenomena ini menunjukkan bahwa masyarakat semakin bergantung pada teknologi pintar dalam kehidupan sehari-hari. Misalnya, jam tangan pintar (smartwatches) menjadi populer karena fungsinya yang tidak hanya sebagai alat penunjuk waktu, tetapi juga sebagai perangkat kesehatan dan produktivitas. Sementara itu, televisi pintar (smart TVs) dan ponsel pintar (smartphones) mencerminkan kebutuhan akan hiburan dan konektivitas yang semakin meningkat. Kategori-kategori ini juga sering kali menjadi prioritas bagi pengguna yang mencari produk dengan fitur inovatif dan desain modern.

Di sisi lain, ada beberapa kategori rumah tangga seperti Mixer Grinders dan Dry Irons yang meskipun jumlah produknya lebih rendah dibandingkan kategori elektronik, tetap relevan dalam dataset ini. Kehadiran kategori ini menunjukkan bahwa produk-produk rumah tangga tradisional masih memiliki pasar yang stabil, meskipun mungkin tidak sepopuler produk elektronik. Produk-produk ini sering kali dibutuhkan untuk menunjang aktivitas sehari-hari di rumah, sehingga tetap menjadi pilihan bagi konsumen yang mencari barang-barang praktis dan fungsional.

Secara keseluruhan, grafik ini memberikan gambaran yang jelas tentang preferensi konsumen di era digital saat ini. Kategori elektronik mendominasi daftar terpopuler, mencerminkan tren global menuju gaya hidup yang lebih cerdas dan terhubung. Namun, produk rumah tangga tradisional tetap memiliki tempat tersendiri dalam kehidupan konsumen. Informasi ini sangat berguna untuk membangun sistem rekomendasi yang lebih relevan, karena kita dapat memprioritaskan rekomendasi berdasarkan kategori yang paling banyak diminati, seperti kabel USB, smartwatches, atau smart TVs, sambil tetap mempertimbangkan produk rumah tangga sebagai opsi tambahan bagi pengguna dengan minat yang lebih spesifik. Dengan pemahaman ini, bisnis dapat lebih efektif dalam menargetkan kebutuhan konsumen dan meningkatkan pengalaman belanja mereka.

## **Data Preparation**

# **Data Preparation & Preprocessing**

Tahap data preparation & preprocessing merupakan salah satu langkah krusial dalam pengembangan sistem rekomendasi berbasis collaborative filtering. Pada tahap ini, data mentah yang telah dikumpulkan dari dataset amazon.csv akan dibersihkan, diorganisasi, diseleksi dan dipersiapkan agar siap digunakan untuk analisis lebih lanjut serta pembuatan model rekomendasi. Tujuan utama dari tahap ini adalah memastikan bahwa data yang digunakan memiliki kualitas tinggi, konsisten, dan sesuai dengan kebutuhan algoritma collaborative filtering.

---

### **Tahapan yang dilakukan diantaranya:**

**1. Pemilihan Kolom Penting**
```python
# Tahap 1: Pemilihan Kolom Penting
# Kolom penting yang akan digunakan
important_columns = [
    'product_id', 'user_id', 'product_name', 'category', 'about_product', 'rating', 'review_content'
]

df = df[important_columns]
df.head()
```
- Proses: Hanya memilih kolom-kolom yang relevan untuk analisis lebih lanjut. Kolom yang dipilih adalah ('product_id', 'user_id', 'product_name', 'category', 'about_product', 'rating', 'review_content')
- Alasan: Mengurangi dimensi dataset agar fokus hanya pada informasi yang relevan, serta mempercepat proses analisis selanjutnya.

**2. Konversi Tipe Data**
```python
# Tahap 2: Konversi Tipe Data
# Konversi 'rating' dan rating_count ke tipe numerik
df['rating'] = pd.to_numeric(df['rating'], errors='coerce')
df.info()
```
- Proses: Mengubah kolom rating dari string menjadi numerik menggunakan pd.to_numeric()
- Alasan: Agar bisa dilakukan analisis numerik (misalnya rata-rata) dan juga Rating tidak memberikan informasi berguna ketika masih menjadi string.

**3. Menghapus Nilai Kosong dan duplikat di Kolom Penting**
```python
# Tahap 3: Menghapus Nilai Kosong dan duplikat di Kolom Penting
# Untuk tahap awal, kita drop baris yang missing di kolom penting
important_cols = ['user_id', 'product_id', 'rating']
df_clean = df.dropna(subset=important_cols)

print(f"\nJumlah baris setelah drop missing: {df_clean.shape[0]}")

# Periksa duplikasi
print("\n=== CEK DUPLIKASI ===")
print(f"Jumlah sebelum cleaning: {df_clean.duplicated().sum()}")

# Hapus duplikasi jika ada
df_clean = df_clean.drop_duplicates()
print(f"Jumlah setelah cleaning: {df_clean.duplicated().sum()}")
print(f"Jumlah baris setelah drop duplikasi: {df_clean.shape[0]}")
```
- Proses: Menghapus baris yang tidak memiliki user_id, product_id, atau rating jik ada.
- Alasan: untuk memastikan ulang tidak ada nilai yang hilang dan jika ada yang hilang maka data yang memiliki salah satu dari ketiga kolom ini tidak bisa digunakan dalam rekomendasi berbasis colaborative filtering

**4. Menangani Format List pada Kolom user_id (Exploding List)**
```python
# Tahap 4: Menangani Format List pada Kolom user_id (Exploding List)
# Pecah user_id & review_id jika masih dalam bentuk list string
# Contoh: '["user1", "user2"]' → pisah jadi dua baris

import ast

def explode_column_list(df, col_name):
    df[col_name] = df[col_name].apply(lambda x: ast.literal_eval(x) if isinstance(x, str) and x.startswith('[') else [x])
    return df.explode(col_name)

# Terapkan jika perlu
if isinstance(df_clean['user_id'].iloc[0], str) and df_clean['user_id'].iloc[0].startswith('['):
    df_clean = explode_column_list(df_clean, 'user_id')

# Pastikan hasil akhirnya adalah satu baris per user–produk–rating
print("\n=== DATA HASIL AKHIR ===")
df_clean[['user_id', 'product_id', 'rating']].head(10)
```
- Proses: Mendeteksi jika user_id disimpan dalam bentuk list string (misalnya '["u1", "u2"]'), lalu dipecah menjadi baris-baris terpisah per user.
- Alasan:Agar satu baris hanya merepresentasikan satu user dan satu review, seperti yang disyaratkan oleh kebanyakan algoritma rekomendasi.

**5. Normalisasi Dataframe menjadi Format User–Product–Rating**
```python
# Tahap 5: Normalisasi Dataframe menjadi Format User–Product–Rating

# Hanya ambil kolom yang kita perlukan
df_small = df_clean[['user_id', 'product_id', 'rating']]

# Buat list untuk tampung hasil pecahan
rows = []

# Iterasi tiap baris
for index, row in df_small.iterrows():
    user_list = str(row['user_id']).split(',')  # Pecah user_id berdasar koma
    product_id = row['product_id']
    rating = row['rating']

    # Untuk setiap user, buat satu baris baru
    for user in user_list:
        user = user.strip()  # Hapus spasi jika ada
        rows.append({
            'user_id': user,
            'product_id': product_id,
            'rating': rating
        })

# Buat dataframe baru dari hasil pecahan
df_expanded = pd.DataFrame(rows)

# Tampilkan hasil
print("Data setelah diekstrak:")
df_expanded.head(20)
```

| | user_id | product_id | rating |
|---|---|---|---|
| 0 | AG3D6O4STAQKY2UVGEUV46KN35Q | B07JW9H4J1 | 4.2 |
| 1 | AHMY5CWJMMK5BJRBSNLYT3ONILA | B07JW9H4J1 | 4.2 |
| 2 | AHCTC6ULH4XB6YHDY6PCH2R772LQ | B07JW9H4J1 | 4.2 |
| 3 | AGYHHJERNXKA6P5T7CZLXKVPT7IQ | B07JW9H4J1 | 4.2 |
| 4 | AG4OGOFWXJZTQ2HKYIOCOY3KXF2Q | B07JW9H4J1 | 4.2 |
| 5 | AENGU523SXMOS7JPDTW52PNNWVGQ | B07JW9H4J1 | 4.2 |
| 6 | AEQJHCVTNINBS4FKTBGRQRTGTE5Q | B07JW9H4J1 | 4.2 |
| 7 | AFC3FFC5PKFF5PMA52S3VCHOZ5FQ | B07JW9H4J1 | 4.2 |
| 8 | AECPFYFQVRUWC3KGNLJIQREFP5LQ | B098NS6PVG | 4.0 |
| 9 | AGYVPPDO7YG7FYNBXNGXZJT525AQ | B098NS6PVG | 4.0 |
| 10 | AHONIZU3ICIEHQIGQ6R2VFRSBXOQ | B098NS6PVG | 4.0 |
| 11 | AFPHD2CRPDZMWMBL7WXRSVYWVS5JA | B098NS6PVG | 4.0 |
| 12 | AEZ346GX3HJ4O4XNRPHCNHXQURMQ | B098NS6PVG | 4.0 |
| 13 | AEPSWFPNECKO34PUC7I56ITGXR6Q | B098NS6PVG | 4.0 |
| 14 | AHWVVEHR5DYLVFTO2KF3IZATFQSWRQ | B098NS6PVG | 4.0 |
| 15 | AH4QT33M55677I7ISQOAKEQWACYQ | B098NS6PVG | 4.0 |
| 16 | AGU3BBQ2V2DDAMOAKGFAWDDQ6QHA | B096MSW6CT | 3.9 |
| 17 | AESFLDV2PT363T2AQLWQOWZ4N3OA | B096MSW6CT | 3.9 |
| 18 | AHTPQRIMGUD4BYR5YIHBHC3CCGEFQ | B096MSW6CT | 3.9 |
| 19 | AEUWVXYP5LT7PZLLZENEO2NODPBQ | B096MSW6CT | 3.9 |

- Proses: Melakukan loop untuk memastikan bahwa satu baris = satu user_id, satu product_id, dan satu rating.
- Alasan: Format ini adalah bentuk yang standar dan umum digunakan untuk collaborative filtering dan matrix factorization.

**6. Mengabungkan Semua Kolom (Versi Diperluas)**
```python
# Tahap 6: Mengabungkan Semua Kolom (Versi Diperluas)
all_columns = df_clean.columns.tolist()

# Buat list untuk tampung hasil pecahan
rows = []

# Iterasi tiap baris
for index, row in df.iterrows():
    user_list = str(row['user_id']).split(',')  # Pecah user_id berdasar koma

    # Untuk setiap user, buat satu baris baru dengan semua kolom lain ikut
    for user in user_list:
        user = user.strip()
        new_row = row.copy()
        new_row['user_id'] = user  # Replace jadi satu user saja
        rows.append(new_row)

# Buat dataframe baru dari hasil pecahan
df_expanded = pd.DataFrame(rows)

# Tampilkan hasil
print("Data setelah diekstrak:")
df_expanded.head(10)
```

| | product_id | user_id | product_name | category | about_product | rating | review_content |
|---|---|---|---|---|---|---|---|
| 0 | B07JW9H4J1 | AG3D6O4STAQ... | Wayona Nylon Braided USB to Lightning Fast Cha... | Computers&Accessories Acces... | High Compatibility : Compati... | 4.2 | Looks durable Charging is fi... |
| 0 | B07JW9H4J1 | AHMY5CWJM... | Wayona Nylon Braided USB to Lightning Fast Cha... | Computers&Accessories Acces... | High Compatibility : Compati... | 4.2 | Looks durable Charging is fi... |
| 0 | B07JW9H4J1 | AHCTC6ULH... | Wayona Nylon Braided USB to Lightning Fast Cha... | Computers&Accessories Acces... | High Compatibility : Compati... | 4.2 | Looks durable Charging is fi... |
| 0 | B07JW9H4J1 | AGYHHJERN... | Wayona Nylon Braided USB to Lightning Fast Cha... | Computers&Accessories Acces... | High Compatibility : Compati... | 4.2 | Looks durable Charging is fi... |
| 0 | B07JW9H4J1 | AG4OGOFWX... | Wayona Nylon Braided USB to Lightning Fast Cha... | Computers&Accessories Acces... | High Compatibility : Compati... | 4.2 | Looks durable Charging is fi... |
| 0 | B07JW9H4J1 | AENGU523S... | Wayona Nylon Braided USB to Lightning Fast Cha... | Computers&Accessories Acces... | High Compatibility : Compati... | 4.2 | Looks durable Charging is fi... |
| 0 | B07JW9H4J1 | AEQJHCVTN... | Wayona Nylon Braided USB to Lightning Fast Cha... | Computers&Accessories Acces... | High Compatibility : Compati... | 4.2 | Looks durable Charging is fi... |
| 0 | B07JW9H4J1 | AFC3FFC5P... | Wayona Nylon Braided USB to Lightning Fast Cha... | Computers&Accessories Acces... | High Compatibility : Compati... | 4.2 | Looks durable Charging is fi... |
| 1 | B098NS6PVG | AECPFYFQR... | Ambrane Unbreakable 60W / 3A Fast Charging 1.5... | Computers&Accessories Acces... | Compatible with all Type C e... | 4.0 | I ordered this cable to conn... |
| 1 | B098NS6PVG | AGYVPPDO7... | Ambrane Unbreakable 60W / 3A Fast Charging 1.5... | Computers&Accessories Acces... | Compatible with all Type C e... | 4.0 | I ordered this cable to conn... |


- Proses: pengabungan kolom dataframe dengan mempertahankan semua kolom (tidak hanya user_id, product_id, rating).
- Alasan: Menyiapkan data yang tetap lengkap untuk keperluan modeling sistem rekomendasi berbasis colaborative filtering

**7. Check dan Inputasi/drop nilai yang hilang**

```python
# Tahap 7: Check dan Inputasi/drop nilai yang hilang.
df_expanded.isnull().sum()
```
| Kolom             | Jumlah |
| :---------------- | :----- |
| product_id        | 0      |
| user_id           | 0      |
| product_name      | 0      |
| category          | 0      |
| about_product     | 0      |
| **rating** | **8** |
| review_content    | 0      |

```python
# isi nilai hilang dengan mean
mean_rating = df_expanded['rating'].mean()
df_expanded['rating'].fillna(mean_rating, inplace=True)
df_expanded.reset_index(drop=True, inplace=True)

# tampilkan data pasca pengabungan dataframe
df_expanded.isnull().sum()
```
| Kolom             | Jumlah |
| :---------------- | :----- |
| product_id        | 0      |
| user_id           | 0      |
| product_name      | 0      |
| category          | 0      |
| about_product     | 0      |
| rating            | 0      |
| review_content    | 0      |


- Proses: Mengecek ulang nilai yang hilang pasca pengabungan tahap 6. lalu Menghapus baris yang banyak nilai kosong atau inputasi jika data hilang tidak terlalu banyak.
Alasan: Memastikan Data harus bersih dan lengkap untuk proses analisis lanjutan, termasuk membangun model

**8. Membersihkan Teks**
```python
# Tahap 8: Membersihkan Teks dan melakukan preprocessing text
import re
def clean_text(text):
    text = str(text).lower()
    text = re.sub(r'<.*?>', ' ', text)
    text = re.sub(r'[^a-zA-Z0-9\s]', ' ', text)
    text = re.sub(r'\s+', ' ', text).strip()
    return text

df_expanded['product_name'] = df_expanded['product_name'].apply(clean_text)
df_expanded['about_product'] = df_expanded['about_product'].apply(clean_text)
df_expanded['category'] = df_expanded['category'].apply(clean_text)
```
- Proses: Membersihkan kolom teks dari HTML tag, karakter khusus, dan mengubah ke huruf kecil. agar semakin bersih.
- Alasan: Menghilangkan noise dari data teks

**9. menukar variable data**
```python
# Tahap 9: Menukar variable data
# Misalnya hasil preparation disimpan ke df
df = df_expanded.copy()  # df adalah hasil transformnya
```
- Proses: variable yang telah dilakukan preparation dan preprocessing akan dikembalikan lagi kedalam bentuk variable df
- Alasan: untuk mengembalikan variable seperti format sebelumnya dan lebih mudah dipahami.

**10. Encoding Kolom Kategorikal (user_id dan product_id)**
```python
# Tahap 10: Encoding Kolom Kategorikal (user_id dan product_id)
from sklearn.preprocessing import LabelEncoder

user_encoder = LabelEncoder()
product_encoder = LabelEncoder()

# Transform ke bentuk numerik
df['user_idx'] = user_encoder.fit_transform(df['user_id'])
df['product_idx'] = product_encoder.fit_transform(df['product_id'])
```
- Proses: Mengubah nilai kategorikal dari kolom user_id dan product_id menjadi nilai numerik menggunakan LabelEncoder dari Scikit-learn.
- Alasan: Model machine learning tidak bisa memproses string atau ID non-numerik. Oleh karena itu, perlu dilakukan encoding ke format integer (label encoding). Langkah ini penting untuk algoritma neural collaborative filtering, atau embedding layer pada neural network.

**11. Normalisasi Rating dan Split Dataset**
```python
# Tahap 11: Normalisasi dan Split Data
from sklearn.model_selection import train_test_split

# Normalisasi rating (0–1)
min_rating = df['rating'].min()
max_rating = df['rating'].max()
df['rating_norm'] = (df['rating'] - min_rating) / (max_rating - min_rating)

# Siapkan input X dan target y
X = df[['user_idx', 'product_idx']].values
y = df['rating_norm'].values

# Split data
X_train, x_val_cf, y_train, y_val_cf = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Cek kembali
print("Sample of X (user_idx, product_idx):")
print(X[:5])
print("\nSample of y (rating_norm):")
print(y[:5])
print(f"\nShape of X_train: {X_train.shape}")
print(f"Shape of x_val_cf: {x_val_cf.shape}")
print(f"Shape of y_train: {y_train.shape}")
print(f"Shape of y_val_cf: {y_val_cf.shape}")

# Pastikan kolom asli tidak dihapus
print("\nKolom-kolom dalam dataframe setelah preprocessing:")
print(df.columns)
```
- Proses: Normalisasi rating ke skala 0–1 menggunakan formula min–max normalization kemudian Membagi dataset menjadi data pelatihan dan validasi (80:20) menggunakan train_test_split.
- Alasan: Normalisasi membantu mempercepat konvergensi model dan mencegah dominasi nilai besar saat training sementara Split data dilakukan agar performa model dapat diuji pada data yang belum pernah dilihat, mencegah overfitting.

## **Modeling**

### **Neutral Collaborative Filtering**

Model yang digunakan adalah Neural Collaborative Filtering, yaitu model pembelajaran mendalam yang memetakan user dan produk ke dalam embedding vector berdimensi tetap, kemudian mengalkulasi dot product antar keduanya untuk memperkirakan rating:

- User Embedding Layer: Mengubah user_idx menjadi representasi dense.

- Product Embedding Layer: Mengubah product_idx menjadi representasi dense.

- Dot Product: Interaksi antara user dan produk dihitung sebagai hasil perkalian dot (inner product) dari dua vektor embedding.

- Bias Layer: Penyesuaian bias individu untuk user dan produk.

- Sigmoid Activation: Karena rating sudah dinormalisasi ke 0–1, maka output model menggunakan fungsi aktivasi sigmoid.

#### **Parameter Penting**

| Parameter                                            | Nilai           | Penjelasan                                                                                                                                                            |
| ---------------------------------------------------- | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `embedding_size`                                     | 50              | Dimensi latent space untuk merepresentasikan user dan produk. Nilai 50 dipilih setelah tuning dari nilai lebih kecil (20) untuk menangkap relasi yang lebih kompleks. |
| `embeddings_initializer='he_normal'`                 | Default         | Inisialisasi bobot awal dari distribusi He, cocok untuk model non-linear.                                                                                             |
| `embeddings_regularizer=keras.regularizers.l2(1e-6)` | 1e-6            | Regularisasi L2 untuk menghindari overfitting dengan membatasi besar bobot.                                                                                           |
| `loss='MeanSquaredError'`                            | MSE             | Digunakan karena target (rating) adalah data kontinyu.                                                                                                                |
| `optimizer='Adam'`                                   | Adam (lr=0.001) | Optimizer adaptif yang cocok untuk data sparse. Learning rate 0.001 stabil saat training.                                                                             |
| `metrics=['RootMeanSquaredError']`                   | RMSE            | Dipilih karena lebih interpretable dibanding MSE dan sesuai dengan konteks rating.                                                                                    |
| `activation=tf.nn.sigmoid`                           | Sigmoid         | Digunakan untuk memastikan output berada di rentang \[0, 1] karena target telah dinormalisasi.                                                                        |

#### **📈 Proses Training**

- Data telah melalui proses label encoding untuk mengubah user_id dan product_id ke dalam format integer.

- Rating dinormalisasi ke skala 0–1 untuk konsistensi dengan fungsi aktivasi output.

- Data dibagi menjadi training dan validation set (80:20).

- import seluruh library untuk model Recommendernet

- Model dirancang dengan dua buah embedding layer: satu untuk user dan satu untuk produk. Setiap pasangan user–produk dihitung dot product dari embedding-nya, ditambahkan bias user dan produk, kemudian dilalui fungsi aktivasi sigmoid.

- Optimizer: Adam umumnya terbaik untuk kecepatan dan akurasi.

- Model dilatih dengan fit(), dan performa divalidasi setiap epoch menggunakan RMSE.

- membuat function untuk mendapatkan top recommendation sesuai dengan jumlah top_n yang diinisiasi

- Menyajikan top-N recommendation sebagai output.

#### **Kelebihan Model**

- Scalable: Mampu menangani jumlah user dan produk yang sangat besar.

- Fleksibel: Bisa dikembangkan menjadi hybrid model dengan menambahkan fitur konten.

- Non-Linear: Berbasis neural network sehingga mampu menangkap pola kompleks dalam interaksi user–produk.

#### **Kekurangan Model**

- Cold Start Problem: Tidak dapat merekomendasikan untuk user/produk baru tanpa histori.

- Butuh Banyak Data: Performa sangat tergantung pada jumlah interaksi (rating) yang tersedia.

- Latihannya Lambat: Dibanding model klasik seperti matrix factorization, training membutuhkan waktu lebih lama.


### **Output Collaborative Filtering:**

```python
Final Validation Loss (MSE): 0.0241
Final Validation RMSE): 0.1441
```

![download (26)](https://github.com/user-attachments/assets/7742a3ce-4934-45a7-992d-9f324e596c26)

Showing recommendations for user: AGE6O2NLNA3NUGORPU4SDK2S23QQ

============================================================================================

**Top products high_rated_by_user:**

| | product_id | product_name | category | rating |
|---|---|---|---|---|
| 568 | B0B5ZF3NRK | cedo 65w oneplus dash warp charge cable usb a... | computers accessories accessories peripherals ... | 4.1 |

============================================================================================

**Top 10 product recommendations:**

| | product_id | product_name | category | predicted_rating |
|---|---|---|---|---|
| 0 | B07WMS7TWB | pigeon by stovekraft amaze plus electric kettl... | home kitchen kitchen homeappliances smallkitch... | 0.570694 |
| 1 | B0B12KBPM | zebronics zeb astra 20 wireless bt v5 0 portab... | electronics homeaudio speakers bluetoothspeakers | 0.570185 |
| 2 | B071VMP1Z4 | inripli compatible sony bravia lcd led remote wo... | electronics hometheater tv video accessories r... | 0.569737 |
| 3 | B083M7WPZD | agaro 33398 rapid 1000 watt 10 litre wet dry v... | home kitchen kitchen homeappliances vacuum cle... | 0.569318 |
| 4 | B07RX42D3D | tosaa t2stsr sandwich gas toaster regular black | home kitchen kitchen homeappliances smallkitch... | 0.569260 |
| 5 | B07DJLFMPS | hp 32gb class 10 microsd memory card u1 tf car... | electronics accessories memorycards microsd | 0.568389 |
| 6 | B085LPT5F4 | solidaire 550 watt mixer grinder with 3 jars b... | home kitchen kitchen homeappliances smallkitch... | 0.568382 |
| 7 | B08VGDBF3B | kuber industries round non woven fabric foldab... | home kitchen homestorage organization laundryo... | 0.568241 |
| 8 | B082DJDCPX | swapkart fast charging cable and data sync usb... | computers accessories accessories peripherals ... | 0.568208 |
| 9 | B096MSW6CT | sounce fast phone charging cable data sync usb... | computers accessories accessories peripherals ... | 0.567745 |

berdasarkan hasil tabel rekomendasi yang telah dibuat, diketahui bahwa produk dengan rating tinggi yang pernah diberi oleh user (misalnya rating 4.1 pada kabel OnePlus) digunakan sebagai referensi pola preferensi pengguna.

melalui prediksi tersebut, Sistem berhasil merekomendasikan beragam kategori produk yang sebelumnya belum pernah diberi rating oleh user, dan semuanya memiliki prediksi rating > 0.55 dalam skala 0–1. Ini menunjukkan bahwa sistem memprioritaskan produk dengan estimasi ketertarikan pengguna yang tinggi. Ini menunjukkan bahwa model yang dibangun telah belajar representasi user-product yang bermakna, dan dapat digunakan untuk membantu pengguna menemukan produk baru yang sesuai preferensi mereka.


## 📈 **Evaluasi Model**

Laporan ini menyajikan hasil evaluasi dari model rekomendasi berbasis _Collaborative Filtering_, yang mengukur performa model dalam memprediksi rating pengguna terhadap produk. Dua metrik yang digunakan untuk evaluasi adalah **Root Mean Squared Error (RMSE)** dan **Mean Absolute Error (MAE)**.

## 🔢 1. Metrik Evaluasi

### **A. Root Mean Squared Error (RMSE)**

RMSE digunakan untuk mengukur rata-rata dari kuadrat selisih antara nilai prediksi dan nilai aktual. Metrik ini memberikan penalti lebih besar terhadap prediksi yang meleset jauh dari nilai sebenarnya, sehingga cocok untuk mengidentifikasi outlier dalam prediksi.

**Formula:**

$$
RMSE = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2}
$$

**Keterangan:**
- $y_i$: nilai rating aktual pada sampel ke-\(i\)
- $\hat{y}_i$: nilai rating hasil prediksi model pada sampel ke-\(i\)
- $n$: jumlah total data (sampel)

**Interpretasi:**
- Nilai RMSE yang **kecil** menunjukkan model memiliki performa yang baik dalam memprediksi nilai yang mendekati rating aktual.
- Nilai RMSE yang **besar** mengindikasikan model melakukan kesalahan prediksi yang signifikan pada beberapa sampel.

---

### **B. Mean Absolute Error (MAE)**

MAE menghitung rata-rata dari selisih absolut antara prediksi dan nilai aktual. Tidak seperti RMSE, MAE tidak memberi penalti lebih besar untuk kesalahan besar, sehingga lebih tahan terhadap outlier.

**Formula:**

$$
MAE = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|
$$

**Keterangan:**
- $y_i$: nilai rating aktual pada sampel ke-\(i\)
- $\hat{y}_i$: nilai rating hasil prediksi model pada sampel ke-\(i\)
- $n$: jumlah total data (sampel)

**Interpretasi:**
- Semakin kecil nilai MAE, semakin akurat model dalam memberikan prediksi.
- MAE memberikan rata-rata kesalahan model tanpa memperhitungkan arah kesalahan (positif atau negatif).

---

### **C. Coverage@K**

**Coverage** adalah metrik yang digunakan untuk mengukur sejauh mana sistem rekomendasi mengeksplorasi keseluruhan item yang tersedia dalam dataset. Metrik ini menggambarkan **diversitas** dari hasil rekomendasi: apakah model hanya merekomendasikan item yang itu-itu saja, atau justru mampu memberikan hasil yang beragam.

Coverage biasanya diukur dalam skenario **Top-N Recommendation**, dan dikenal dengan istilah **Coverage@K**.

**Formula**

$$
Coverage@K = \frac{\text{Jumlah item unik yang direkomendasikan}}{\text{Jumlah total item tersedia}}
$$

Ketarangan:

- **Numerator**: jumlah item unik yang muncul dalam semua daftar Top-K hasil rekomendasi
- **Denominator**: total jumlah item unik yang tersedia di dataset

## 📊 Hasil Evaluasi Model

Evaluasi dilakukan pada data validasi, menggunakan hasil prediksi model Collaborative Filtering. Nilai-nilai metrik dihitung sebagai berikut:

#### **RSME dan MAE**

```python
Collaborative Filtering - RMSE: 0.1441
Collaborative Filtering - MAE: 0.1098
```

![download (28)](https://github.com/user-attachments/assets/0e95a3db-f9c4-4ae9-8fe6-356e0cd71c1e)

Interpretasi:

- Karena data rating telah dinormalisasi ke skala 0–1, maka nilai RMSE dan MAE dalam konteks ini juga berada dalam rentang tersebut.

- Nilai error ini relatif kecil, sehingga model dinilai mampu menangkap hubungan antara user dan item secara efektif.

- Nilai **RMSE = 0.1441** mengindikasikan bahwa akar rata-rata kuadrat kesalahan cukup rendah, yang berarti model cukup baik dalam menangani error besar.
- Nilai **MAE = 0.1098** juga menunjukkan bahwa rata-rata selisih absolut antara prediksi dan nilai aktual tergolong rendah, menandakan stabilitas prediksi model.

RMSE = 0.1441 dan MAE = 0.1098 menunjukkan bahwa model memberikan prediksi yang cukup akurat terhadap preferensi user. Secara keseluruhan, hasil ini menunjukkan bahwa model Collaborative Filtering yang dikembangkan mampu memberikan performa prediksi yang baik, meskipun masih dapat ditingkatkan lebih lanjut melalui teknik seperti hyperparameter tuning, penambahan data, atau modifikasi arsitektur model.

#### **C. Coverage@K**

```python
Coverage @ 10: 0.5574
Total recommended items: 753
Total available items: 1351

Top 10 Categories in Recommendations:
computers accessories accessories peripherals cables accessories cables usbcables                        81
electronics hometheater tv video televisions smarttelevisions                                            29
electronics wearabletechnology smartwatches                                                              22
computers accessories accessories peripherals keyboards mice inputdevices mice                           21
electronics hometheater tv video accessories cables hdmicables                                           19
home kitchen kitchen homeappliances vacuum cleaning ironing irons steamers accessories irons dryirons    18
electronics mobiles accessories smartphones basicmobiles smartphones                                     15
electronics hometheater tv video accessories remotecontrols                                              15
home kitchen kitchen homeappliances vacuum cleaning ironing irons steamers accessories lintshavers       15
home kitchen kitchen homeappliances smallkitchenappliances handblenders                                  12
```

**Interpretasi:**
- Nilai coverage sebesar **0.5574** berarti bahwa sistem rekomendasi mencakup sekitar **55.74%** dari seluruh produk yang tersedia.
- Ini menandakan bahwa model tidak hanya merekomendasikan produk populer secara sempit, tetapi sudah cukup **beragam** dalam menyarankan produk dari berbagai jenis.

---

### **B. Distribusi Kategori Produk dalam Top-10 Rekomendasi berdasarkan evaluasi Coverage@K:**

Visualisasi berikut menunjukkan kategori produk yang paling sering muncul dalam hasil rekomendasi:

![download (24)](https://github.com/user-attachments/assets/ac1263ae-9039-49e7-82a5-a173d0738074)

**Observasi:**
- Kategori terbanyak berasal dari sub-kategori **computer & accessories** seperti kabel USB dan mouse.
- Produk elektronik seperti **smartwatch**, **televisi pintar**, dan **smartphone** juga banyak direkomendasikan.
- Beberapa kategori rumah tangga seperti **penghisap debu**, **pemanas air**, dan **alat setrika** muncul dalam Top-10, menandakan keberagaman sektor yang dicakup.

---

### **C. Kesimpulan dari Coverage Evaluation**

- Nilai coverage **> 50%** merupakan indikator positif bahwa model berhasil menjelajahi lebih dari separuh item yang tersedia.
- Ini memperkuat asumsi bahwa model tidak sekadar menyarankan item-item paling populer saja.
- Tingkat coverage yang tinggi juga berkontribusi terhadap **pengalaman pengguna yang lebih personal dan bervariasi**, karena produk yang ditampilkan tidak terbatas pada subset kecil dari katalog.

Jika coverage rendah, maka pengguna cenderung melihat produk yang sama terus-menerus. Sebaliknya, coverage yang baik dapat meningkatkan peluang pengguna menemukan produk yang relevan namun belum dikenal.

---

# Kesimpulan Akhir Proyek Sistem Rekomendasi Berbasis Collaborative Filtering

## 1. Apakah Sudah Menjawab Setiap Problem Statement?

| Problem Statement | Pemenuhan Solusi | Penjelasan |
|-------------------|------------------|------------|
| **1. Sistem belum memberikan rekomendasi yang personal.** | ✅ Ya | MModel berbasis Collaborative Filtering berhasil mempelajari preferensi pengguna berdasarkan interaksi historis, menghasilkan rekomendasi yang spesifik dan personal terhadap perilaku masing-masing user. |
| **2. Interaksi user-item bersifat sparse.** | ✅ Ya | Dengan menggunakan pendekatan Neural Collaborative Filtering (NCF) dan teknik embedding, model dapat mengatasi sparsity dengan menyandikan relasi user-item secara lebih efisien. |
| **3. Tidak ada evaluasi metrik yang komprehensif.** | ✅ Ya | Proyek ini mengevaluasi hasil rekomendasi menggunakan tiga metrik utama: RMSE, MAE, dan Coverage@10—yang memberikan pengukuran menyeluruh terhadap akurasi dan keragaman rekomendasi. |

---

## 2. Apakah Berhasil Mencapai Setiap Goals yang diharapkan?

| Goals | Status | Penjelasan |
|-------|--------|------------|
| **1. Membangun sistem rekomendasi berbasis Collaborative Filtering.** | ✅ Tercapai | Sistem telah berhasil dibangun menggunakan pendekatan neural collaborative filtering, memanfaatkan data interaksi pengguna dan produk. |
| **2. Mengatasi sparsity dengan embedding & neural network.** | ✅ Tercapai | Embedding layer secara efektif mempelajari representasi user-item.  |
| **3. Evaluasi dengan metrik RMSE, MAE, dan Coverage.** | ✅ Tercapai | Evaluasi menunjukkan hasil yang baik: <br>• `RMSE = 0.1441` <br>• `MAE = 0.1098` <br>• `Coverage@10 = 0.5574` Ini menunjukkan akurasi tinggi dan keragaman rekomendasi yang baik. |

---

## 3. Apakah Setiap Solution Statement Berdampak?

| Solusi | Dampak & Bukti |
|--------|----------------|
| **1. Penggunaan NCF dan embedding.** | Memberikan dampak signifikan terhadap kualitas representasi pengguna dan item, serta memperbaiki masalah sparsity. Hal ini dibuktikan dari nilai MAE & RMSE yang rendah, menunjukkan prediksi model sangat dekat dengan nilai aktual. |
| **2. Evaluasi menggunakan RMSE, MAE, Coverage.** | ✅ Evaluasi komprehensif ini tidak hanya menilai akurasi prediksi, tetapi juga menilai seberapa beragam dan luas model menjangkau produk, dibuktikan dengan coverage di atas 50%, yang berarti lebih dari separuh produk berhasil dijangkau oleh sistem rekomendasi. |

---

## Keselarasan dengan Business Understanding

Proyek ini **selaras secara menyeluruh** dengan tujuan bisnis:

- ✅ Problem statement yang diajukan telah dijawab secara sistematis.
- ✅ Goals tercapai baik dari sisi teknis maupun fungsional.
- ✅ Solusi yang ditetapkan memberikan dampak nyata terhadap kualitas hasil sistem rekomendasi.
- ✅ Evaluasi dengan visualisasi dan angka menunjukkan performa model yang baik secara kuantitatif dan praktis.

---

## 🧾 Kesimpulan Akhir

Model sistem rekomendasi berbasis **Neural Collaborative Filtering (NCF)** yang telah dibangun berhasil menjawab kebutuhan bisnis dalam menyediakan sistem rekomendasi yang akurat, personal, dan beragam. Evaluasi dengan RMSE, MAE, dan Coverage membuktikan bahwa:

- **Tingkat akurasi prediksi yang tinggi**, ditunjukkan oleh nilai RMSE dan MAE yang sangat rendah menunujukan mampu memprediksi rating dengan kesalahan minimal.
- **Ragam rekomendasi yang luas**, Rekomendasi tidak terbatas pada item populer, melainkan tersebar ke berbagai kategori produk.
- **Personalisasi rekomendasi yang efektif**, Sistem mendekatkan pengguna dengan produk yang sesuai dengan preferensinya dan berhasil menciptakan pengalaman pengguna yang lebih relevan dan variatif, yang pada akhirnya dapat meningkatkan engagement dan konversi di platform e-commerce.

Dengan pencapaian ini, sistem rekomendasi siap untuk diimplementasikan lebih lanjut, baik dalam skala terbatas (A/B testing) maupun integrasi penuh ke dalam sistem e-commerce yang ada.

## Saran

Model yang dibuat masih dapat ditingkatkan lebih lanjut melalui teknik seperti hyperparameter tuning, penambahan data, atau modifikasi arsitektur model untuk dapat dilakukan untuk meningkatkan akurasinya. sehingga personalisasi dari model colaborative filtering bisa memberikan personalisasi lebih dalam berdasarkan preferensi pengguna.

**---Ini adalah bagian akhir laporan---**
---

