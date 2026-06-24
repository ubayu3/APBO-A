# ☕ DYDY Coffee Scan-to-Order System

## 📖 Deskripsi Proyek

DYDY Coffee Scan-to-Order System merupakan sistem pemesanan berbasis web yang dirancang untuk membantu proses pemesanan menu secara mandiri melalui QR Code yang tersedia pada setiap meja pelanggan.

Sistem ini dibuat sebagai solusi atas beberapa kendala pada proses pemesanan konvensional, seperti antrean panjang di kasir, proses pemilihan menu yang terburu-buru, serta tingginya beban kerja kasir saat jam operasional sibuk.

---

## 👥 Tim Pengembang

| Nama | NPM |
|--------|--------|
| Bryan Ananda Saputra Hulu | 4524210020 |
| Muhammad Agis Irawan | 4524210056 |
| M. Al Ghifari | 4524210052 |
| Bayu Sardo Situmorang | 4524210019 |
| Dzikrullah Surachman | 4524210029 |

---

## 🎯 Sasaran Pengguna

### Pelanggan
- Mengakses katalog menu melalui QR Code.
- Melakukan pemesanan secara mandiri.
- Melakukan konfirmasi pembayaran.

### Kasir
- Memverifikasi pembayaran.
- Mengelola status pesanan.
- Memantau daftar pesanan masuk.

### Barista
- Melihat daftar pesanan yang telah diverifikasi.
- Menyiapkan pesanan sesuai data sistem.

### Pelayan
- Mengantarkan pesanan ke meja pelanggan.

---

## 📚 Latar Belakang

Pengelolaan pemesanan di DYDY Coffee saat ini masih terpusat pada perangkat tablet di area kasir. Pada jam sibuk, kondisi ini sering menyebabkan antrean pelanggan yang cukup panjang.

Selain itu, pelanggan sering merasa terburu-buru saat memilih menu karena adanya antrean di belakang mereka. Di sisi lain, kasir harus melakukan input pesanan secara manual sehingga meningkatkan beban kerja operasional.

Untuk mengatasi permasalahan tersebut, dikembangkan sistem Scan-to-Order berbasis web yang memungkinkan pelanggan melakukan pemesanan langsung dari meja melalui QR Code.

---

## 📑 Studi Literatur

### Jurnal 1
**Implementasi QR Code untuk Efisiensi Waktu Pemesanan Menu Makanan dan Minuman di Restoran maupun Kafe**

Hasil penelitian menunjukkan bahwa penggunaan QR Code dapat mempercepat proses pemesanan dan meningkatkan akurasi pencatatan pesanan.

### Jurnal 2
**Perancangan Sistem Pemesanan Makanan Menggunakan QR Code Berbasis Website Mobile Pada RightCoffee**

Penelitian menunjukkan bahwa sistem pemesanan berbasis QR Code mampu mengurangi antrean pelanggan serta meminimalkan kesalahan pencatatan pesanan.

### Jurnal 3
**Pengembangan Aplikasi Pemesanan Makanan Berbasis Web Dengan QR Code Untuk Efisiensi Pelayanan Kafe**

Hasil penelitian menunjukkan bahwa penggunaan QR Code dan website dapat meningkatkan efisiensi pelayanan tanpa memerlukan aplikasi tambahan.

---

## 🎤 Hasil Wawancara

Narasumber:
**Bapak Dani (Owner DYDY Coffee)**

### Permasalahan yang Ditemukan

- Antrean panjang masih terjadi saat akhir pekan atau jam sibuk.
- Pemesanan masih dilakukan secara manual.
- Stok menu harus diperiksa secara berkala oleh staf.
- Sistem digital dinilai dapat meningkatkan efisiensi pelayanan.

### Dokumentasi Wawancara

<p align="center">
  <img src="image.png" width="800">
</p>

**Gambar 1. Dokumentasi Wawancara dengan Owner DYDY Coffee**

---

## ⚖️ Analisis SOP

| Aspek | Sistem Lama | Sistem Usulan |
|---------|---------|---------|
| Pemesanan | Melalui kasir | Melalui QR Code |
| Antrean | Tinggi saat jam sibuk | Berkurang |
| Input Pesanan | Manual | Otomatis |
| Informasi Pesanan | Komunikasi antar staf | Tersimpan dalam sistem |

---

## 🎭 Analisis Aktor

### Pelanggan
Melakukan pemesanan menu secara mandiri melalui QR Code.

### Kasir
Memverifikasi pembayaran dan mengelola status pesanan.

### Barista
Menyiapkan pesanan yang telah diverifikasi.

### Pelayan
Mengantarkan pesanan ke meja pelanggan.

---

## 📌 Use Case

### Melakukan Pemesanan

1. Pelanggan memindai QR Code.
2. Sistem menampilkan menu.
3. Pelanggan memilih menu.
4. Pelanggan melakukan checkout.

**Hasil:** Pesanan tersimpan dengan status Pending.

### Konfirmasi Pembayaran

1. Sistem menampilkan invoice.
2. Pelanggan melakukan pembayaran.
3. Pelanggan melakukan konfirmasi pembayaran.

**Hasil:** Data pembayaran masuk ke sistem.

### Verifikasi Pesanan

1. Kasir membuka dashboard.
2. Kasir memeriksa pembayaran.
3. Kasir memverifikasi pesanan.
4. Sistem meneruskan pesanan ke barista.

**Hasil:** Pesanan siap diproses.

---

## 📊 Use Case Diagram

<p align="center">
  <img src="diagram_usecase.png" width="900">
</p>

**Gambar 2. Use Case Diagram Sistem**

---

## 💡 Solusi yang Diusulkan

Fitur utama sistem:

- QR Code Scan-to-Order
- E-Katalog Menu
- Keranjang Belanja Digital
- Dashboard Kasir
- Monitoring Pesanan Real-Time
- Konfirmasi Pembayaran
- Informasi Nomor Meja

---

## 🔀 Git Workflow

```bash
git clone <repository>

git checkout -b nama_branch

git add .
git commit -m "pesan commit"

git push -u origin nama_branch

git pull origin main
