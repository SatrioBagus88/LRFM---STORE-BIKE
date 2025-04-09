##### *Disclaimer*:
1. *Analisis ini dibuat sebagai bagian dari portofolio pribadi di bidang Data Science.*
2. *Notebook ini ditulis dalam bahasa pemrograman Python dan menggunakan Bahasa Indonesia.*
3. *Dataset bersifat fiktif/sintetik dan digunakan untuk tujuan edukasi dan analisis segmentasi pelanggan.*

---

# Analisis Segmentasi Pelanggan dengan Metode LRFM – Toko Sepeda

## Deskripsi Proyek

Proyek ini bertujuan untuk menganalisis data transaksi dari sebuah toko sepeda menggunakan metode LRFM. Metode ini mengelompokkan pelanggan berdasarkan kebiasaan pembelian mereka dalam empat dimensi utama:  
- **Length**: Sejak kapan pelanggan mulai aktif  
- **Recency**: Kapan terakhir kali pelanggan bertransaksi  
- **Frequency**: Seberapa sering pelanggan melakukan transaksi  
- **Monetary**: Total nilai transaksi yang dilakukan  

Melalui analisis ini, dihasilkan segmentasi pelanggan yang dapat dijadikan dasar strategi pemasaran yang lebih terarah dan personal.

---

## Tujuan

- Mengelompokkan pelanggan ke dalam segmen berdasarkan perilaku pembelian mereka.
- Memberikan rekomendasi strategi pemasaran berdasarkan segmentasi.
- Memahami karakteristik pelanggan yang bernilai tinggi bagi bisnis.

---

## Deskripsi Kolom Dataset

1. `transaction_id`: ID unik untuk setiap transaksi  
2. `product_id`: ID produk  
3. `customer_id`: ID pelanggan  
4. `transaction_date`: Tanggal transaksi  
5. `online_order`: Status apakah transaksi dilakukan online (TRUE) atau tidak  
6. `order_status`: Status pemesanan (contoh: Approved)  
7. `brand`: Merek produk  
8. `product_line`: Kategori produk  
9. `product_class`: Kelas produk (low, medium, high)  
10. `product_size`: Ukuran produk (small, medium, large)  
11. `list_price`: Harga produk  
12. `standard_cost`: Biaya standar produk  
13. `product_first_sold_date`: Tanggal pertama kali produk dijual  

---

## Metodologi Analisis

1. **Pembersihan Data**  
   - Menghapus nilai kosong dan data duplikat  
   - Menstandardisasi format tanggal dan tipe data  

2. **Perhitungan Nilai LRFM**  
   - **Length**: Jarak waktu antara tanggal analisis dan tanggal pertama transaksi pelanggan  
   - **Recency**: Jarak waktu antara tanggal analisis dan transaksi terakhir pelanggan  
   - **Frequency**: Jumlah transaksi yang dilakukan pelanggan  
   - **Monetary**: Total nilai transaksi oleh pelanggan  

3. **Segmentasi**  
   Pelanggan dikelompokkan menjadi beberapa tier:
   - **Elite Rider**
   - **Priority Rider**
   - **Sport Rider**
   - **Fun Rider**

---

## Library yang Digunakan

- `pandas` – manipulasi data  
- `numpy` – perhitungan numerik  
- `matplotlib` & `seaborn` – visualisasi data  
- `datetime` – manipulasi tanggal  
- `sklearn.preprocessing` – normalisasi data  
- `sklearn.cluster` – KMeans untuk segmentasi

---

## Output

Analisis ini menghasilkan segmentasi pelanggan berbasis LRFM yang dapat membantu toko sepeda dalam:
- Mengidentifikasi pelanggan potensial bernilai tinggi
- Merancang promosi dan pendekatan berbeda untuk setiap segmen
- Meningkatkan loyalitas dan retensi pelanggan secara strategis

---

