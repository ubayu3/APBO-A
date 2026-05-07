# ☕ Laporan Tugas APBO: Optimalisasi Alur Pemesanan DYDY Coffee
**Mata Kuliah:** Analisis dan Perancangan Berorientasi Objek (A)  
**Dosen Pengampu:** Adi Wahyu Pribadi, S.Si., M.Kom

---

## 👥 Anggota Kelompok 5
| Nama | NPM |
| :--- | :--- |
| **Bryan Ananda Saputra Hulu** | 4524210020 |
| **Muhammad Agis Irawan** | 4524210056 |
| **M. AL GHIFARI** | 4524210052 |
| **Bayu Sardo Situmorang** | 4524210019 |
| **Dzikrullah Surachman** | 4524210029 |

---

## 📌 Informasi & Ruang Lingkup Proyek

### 🎯 Sasaran Pengguna
Sistem Scan-to-Order DYDY Coffee dirancang untuk memfasilitasi koordinasi antara staf kafe dan kenyamanan pelanggan:
* **Kasir & Barista**: Bertugas memvalidasi pesanan masuk, memantau stok real-time, dan menjalankan instruksi kerja melalui struk otomatis.
* **Pelanggan (Customer)**: Pengunjung yang menginginkan kemudahan memesan menu secara mandiri dari meja tanpa harus mengantre lama.
* **Pelayan**: Mengantarkan pesanan sesuai nomor meja yang tertera pada sistem.

### 📚 Analisis Masalah (Latar Belakang)
Pengelolaan pemesanan saat ini masih terpusat pada satu perangkat tablet di kasir, yang menyebabkan:
1. **Queue Bottleneck**: Penumpukan antrean di pintu masuk saat jam sibuk (*rush hour*).
2. **Psychological Pressure**: Pelanggan merasa terburu-buru memilih menu karena merasa ditunggui antrean di belakangnya.
3. **Keterbatasan Fleksibilitas**: Staf kasir terpaku di meja untuk input manual satu per satu.

---

## 💬 Hasil Wawancara SOP DYDY Coffee
Klik pada masing-masing bagian di bawah ini untuk melihat detail transkrip wawancara dengan **Bapak Dani (Owner)**:

<details>
<summary><b>Bagian 1: Identifikasi Masalah (Fase 1)</b></summary>
<br>

**Q: Apakah sering terjadi antrean panjang di depan kasir saat jam sibuk?**
> "Pada hari hectic (weekend) tentu ada antrean yang panjang karena masih input order secara manual. Pemesanan juga bisa dilakukan lewat buku menu."

**Q: Seberapa sering terjadi miskomunikasi antara kasir dan barista?**
> "Untuk misskom dalam pemesanan sejauh ini masih aman dikarenakan staff selalu di-training dengan baik."

**Q: Bagaimana cara mengontrol stok yang habis di tablet kasir?**
> "Stok selalu dicek secara berkala oleh staff shift pagi. Sejauh ini tidak ada konsumen yang memesan menu yang sedang kosong."
</details>

<details>
<summary><b>Bagian 2: Analisa Solusi (Fase 3)</b></summary>
<br>

**Q: Lebih membantu mana: Kasir tetap input manual atau struk pesanan keluar otomatis?**
> "Lebih membantu yang keluar langsung dari printer, karena lebih efisien dan lebih membantu yang online."

**Q: Apakah Kakak setuju sistem ini membuat pelanggan lebih santai memilih menu?**
> "Jelas lebih membantu dalam pesanan, karena customer tidak terburu-buru untuk memesan menu."

**Q: Apa tantangan terbesar jika sistem ini diterapkan?**
> "Tantangan terbesar mungkin tidak ada karena ini sangat membantu. Mungkin hanya soal disiplin update stok atau masalah jaringan/hosting yang lambat."
</details>

<br>

![Dokumentasi Wawancara](image.png)

---

## ⚖️ Analisis Perbandingan SOP
| Kategori | Sistem Lama (Konvensional) | Sistem Baru (Scan-to-Order) |
| :--- | :--- | :--- |
| **Alur Antrean** | Menumpuk di depan kasir, mengganggu arus masuk. | Terurai karena pelanggan memesan langsung dari meja. |
| **Proses Memilih** | Terburu-buru karena merasa ditunggui antrean. | Lebih santai via katalog digital di HP pelanggan. |
| **Input Pesanan** | Kasir mengetik manual satu per satu di tablet. | Pelanggan input mandiri; Kasir tinggal verifikasi. |
| **Instruksi Kerja** | Bergantung pada penyampaian verbal/input manual. | Struk otomatis tercetak di Barista sebagai perintah kerja. |

---

---

## ⚙️ Use Case (Skenario Utama)

### **Ringkasan Peran**
* **Pelanggan**: Melakukan scan QR meja, memilih menu, dan melakukan pembayaran mandiri.
* **Kasir**: Menerima notifikasi, memverifikasi pembayaran, dan mencetak struk produksi.
* **Barista**: Menerima struk fisik dan memproses pesanan sesuai urutan.
* **Pelayan**: Mengantarkan pesanan ke nomor meja yang tertera pada struk.

### **Detail Alur (Skenario Utama)**
1. **Pemesanan Mandiri**: Pelanggan scan QR -> Pilih Menu -> Checkout & Bayar.
2. **Verifikasi Kasir**: Kasir menerima data -> Validasi Dana & Stok -> Klik tombol 'Cetak Struk'.
3. **Produksi & Serving**: Barista menyiapkan menu -> Pelayan mengantar pesanan -> Transaksi Selesai.

<br>

<p align="center">
  <img src="diagram_usecase.png" alt="Diagram Use Case Kelompok 5" width="600">
  <br>
  <i>Gambar 1: Diagram Use Case Sistem Scan-to-Order DYDY Coffee</i>
</p>

---

## 💡 Solusi yang Diberikan
Sistem ini dibangun untuk menyelesaikan masalah efisiensi dengan fitur unggulan:
* **Hybrid Control**: Teknologi mempercepat pesanan, namun kasir tetap memegang kendali penuh (filter) untuk menjaga kualitas layanan.
* **Digital Catalog & QR Unique**: Menghilangkan kebutuhan antre di kasir. Setiap meja memiliki QR unik sehingga nomor meja otomatis tercatat.
* **Otomatisasi Instruksi**: Mengurangi risiko miskomunikasi antara kasir dan dapur melalui printer struk otomatis.
* **Resiliensi Sistem**: Dilengkapi dengan strategi *Offline Mode Standby* (katalog fisik) jika terjadi gangguan ISP.

---

## 💻 Git Workflow (Panduan Kontribusi)
1. `git clone` (Clone repo ke lokal)
2. `git checkout -b NAMA_ANDA` (Buat branch baru)
3. `git add .` && `git commit -m "Pesan commit"`
4. `git push -u origin NAMA_BRANCH` (**JANGAN PUSH KE MAIN**)
5. `git pull origin main` (Update data terbaru dari pusat)