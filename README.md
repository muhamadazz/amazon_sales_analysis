# 📊 Amazon Sales Data Analysis

Analisis eksploratif terhadap dataset penjualan dan ulasan produk di Amazon (kategori elektronik & aksesori). Proyek ini bertujuan untuk menggali pola harga, diskon, ulasan, dan tren kategori produk menggunakan Python.

---

## 🎯 Tujuan Proyek

- Membersihkan dan memahami struktur dataset penjualan Amazon
- Mengidentifikasi pola diskon, rating, dan distribusi harga
- Mengevaluasi korelasi antar variabel numerik
- Memberikan insight berbasis data untuk strategi penjualan e-commerce

---

## 🗃️ Deskripsi Dataset

Dataset berisi informasi produk dan ulasan seperti:

| Kolom                 | Deskripsi |
|-----------------------|----------|
| product_id            | ID unik produk |
| product_name          | Nama produk |
| category              | Kategori produk |
| discounted_price      | Harga setelah diskon |
| actual_price          | Harga asli sebelum diskon |
| discount_percentage   | Persentase diskon |
| rating                | Rating rata-rata produk |
| rating_count          | Jumlah orang yang memberi rating |
| about_product         | Deskripsi fitur produk |
| user_id, user_name    | Informasi pengguna pemberi ulasan |
| review_title, review_content | Judul dan isi ulasan |
| img_link, product_link| Link gambar dan produk |

---

## 🧼 Proses Data Cleaning

- Menghilangkan simbol mata uang dan koma dari kolom harga
- Mengubah tipe data menjadi numerik
- Menangani missing values
- Normalisasi kategori produk yang kompleks

---

## 📊 Exploratory Data Analysis (EDA)

### 1. 💬 **Hubungan Diskon vs Rating**
- Mayoritas produk memiliki rating tinggi (≥ 4.0)
- **Tidak ada korelasi signifikan** antara besar diskon dengan rating produk  
  → Artinya, **kualitas produk lebih memengaruhi rating daripada potongan harga**

---

### 2. 💰 **Distribusi Harga**
- Harga asli produk sangat **bervariasi**, tetapi mayoritas < ₹10,000
- Banyak outlier pada harga tinggi (hingga ₹140,000)

---

### 3. 📉 **Distribusi Diskon**
- Sebagian besar produk didiskon antara **40%–70%**
- Distribusi mirip normal, dengan sedikit outlier ekstrem di atas 90%

---

### 4. 🧠 **Korelasi Variabel Numerik**
| Variabel            | Korelasi |
|---------------------|----------|
| `discounted_price`  ↔ `actual_price` | Sangat tinggi (0.96) |
| `discount_percentage` vs lainnya     | Lemah atau negatif |
| `rating`, `rating_count`             | Hampir tidak berkorelasi kuat dengan variabel lain |

> Artinya: Harga diskon jelas tergantung pada harga asli, tapi **diskon tidak menjamin rating tinggi atau review banyak**

---

### 5. 📦 **10 Kategori Produk Terbanyak**
- Didominasi oleh produk seperti:
  - **USB Cables**
  - **Smart Watches**
  - **Smartphones**
- Menunjukkan kategori **elektronik dan aksesoris** sangat kompetitif

---

### 6. ⭐ **Distribusi Rating**
- Distribusi berbentuk normal, rata-rata rating di kisaran **4.1–4.3**
- Hampir tidak ada produk dengan rating < 3.0  
> Secara umum, pembeli cukup puas dengan produk-produk yang dijual

---

## 📌 Tools & Tech Stack

- **Python**: pandas, numpy, matplotlib, seaborn
- **Jupyter Notebook**
- Visualisasi: Histogram, Scatter plot, Bar chart, Heatmap korelasi

---

## 🧠 Insight Utama

- **Rating tinggi tidak bergantung pada besar diskon**
- Produk paling banyak dijual berada di kategori **aksesoris elektronik**
- Review yang banyak cenderung diberikan untuk produk populer, bukan yang termurah
- Diskon umum berkisar **50%**, mencerminkan strategi pemasaran Amazon di India

---
