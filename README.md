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
Sistem Scan-to-Order DYDY Coffee dirancang untuk memfacilitasi koordinasi antara staf kafe dan kenyamanan pelanggan melalui website pemesanan sederhana:
* **Pelanggan (Customer)**: Mengakses katalog digital via QR Code langsung dari meja masing-masing untuk memesan menu dan melakukan simulasi/konfirmasi pembayaran secara mandiri.
* **Kasir & Barista**: Memantau daftar pesanan masuk melalui monitor web, memvalidasi status pembayaran, dan memproses menu sesuai nomor meja.
* **Pelayan**: Mengantarkan pesanan fisik ke meja yang dituju berdasarkan informasi valid yang tertera di sistem monitor kasir.

### 📚 Analisis Masalah (Latar Belakang)
Pengelolaan pemesanan saat ini masih terpusat pada satu perangkat tablet di kasir, yang menyebabkan beberapa kendala utama:
1. **Queue Bottleneck**: Penumpukan antrean di pintu masuk saat jam sibuk (*rush hour*).
2. **Psychological Pressure**: Pelanggan merasa terburu-buru memilih menu karena merasa ditunggui antrean di belakangnya.
3. **Keterbatasan Fleksibilitas**: Staf kasir terpaku di meja untuk input manual pesanan satu per satu ke tablet.

## 📖 Referensi & Studi Literatur

Pengembangan sistem *Scan-to-Order* berbasis web untuk DYDY Coffee ini didasarkan pada landasan literatur ilmiah berikut yang memvalidasi penyelesaian masalah operasional di lapangan:

> 📄 **[Jurnal 1] Efisiensi Waktu Pemesanan dan Transaksi**
> * **Judul**: Implementasi QR Code untuk Efisiensi Waktu Pemesanan Menu Makanan dan Minuman di Restoran maupun Kafe
> * **Penulis**: Suharianto, dkk. (2020)
> * **Jurnal**: *BIOS: Jurnal Teknologi Informasi dan Rekayasa Komputer*
> * **Relevansi**: Pencatatan manual sering kali menimbulkan kendala antrean panjang. Penerapan teknologi QR Code sebagai media pemesanan menu terbukti dapat memotong durasi proses pemesanan secara signifikan dan meningkatkan akurasi data pesanan yang diterima oleh bagian dapur.
> * **🔗 Tautan Publikasi**: [Implementasi QR Code untuk Efisiensi Waktu Pemesanan Menu Makanan dan Minuman di Restoran maupun Kafe](https://bios.sinergis.org/bios/article/view/7)

---

> 📄 **[Jurnal 2] Pengurangan Kesalahan Pencatatan Manual & Antrean Kasir**
> * **Judul**: Perancangan Sistem Pemesanan Makanan Menggunakan QR Code Berbasis Website Mobile Pada RightCoffee
> * **Penulis**: Ratih Wahyuningrum, Daffa Btara Alif Putra Yuono (2025)
> * **Jurnal**: *Jurnal Esensi Infokom*
> * **Relevansi**: Kecenderungan konsumen batal memesan sering dipicu oleh rasa malas mengantre di kasir. Solusi *self-service* berbasis *website mobile* yang diakses via QR Code di meja terbukti mampu mereduksi penumpukan antrean fisik secara drastis serta menghilangkan risiko salah catat pesanan.
> * **🔗 Tautan Publikasi**: [Perancangan Sistem Pemesanan Makanan Menggunakan QR Code Berbasis Website Mobile Pada RightCoffee](https://esensijournal.com/index.php/infokom/article/view/350)

---

> 📄 **[Jurnal 3] Optimalisasi Kecepatan Pelayanan Kafe**
> * **Judul**: Pengembangan Aplikasi Pemesanan Makanan Berbasis Web Dengan QR Code Untuk Efisiensi Pelayanan Kafe
> * **Penulis**: Syahri, A., dkk. (2025)
> * **Jurnal**: *JATI (Jurnal Mahasiswa Teknik Informatika)*
> * **Relevansi**: Digitalisasi menu lewat integrasi QR Code terbukti dapat mempersingkat waktu rata-rata pemesanan dari semula 7,42 menit menjadi hanya 4 menit. Sistem berbasis web ini sangat efektif untuk meningkatkan efisiensi operasional kafe tanpa mengharuskan pelanggan mengunduh aplikasi tambahan.
> * **🔗 Tautan Publikasi**: [Pengembangan Aplikasi Pemesanan Makanan Berbasis Web Dengan QR Code Untuk Efisiensi Pelayanan Kafe](https://ejournal.itn.ac.id/jati/article/view/13955)

---

## 💬 Hasil Wawancara SOP DYDY Coffee
Klik pada masing-masing bagian di bawah ini untuk melihat detail transkrip wawancara dengan **Bapak Dani (Owner)**:

<details>
<summary><b>Bagian 1: Identifikasi Masalah (Fase 1)</b></summary>
<br>

**Q: Apakah sering terjadi antrean panjang di depan kasir saat jam sibuk?**
> "Pada hari hectic (weekend) tentu ada antrean yang panjang karena masih input order secara manual. Pemesanan juga bisa dilakukan lewat buku menu."

**Q: Seberapa sering terjadi miskomunikasi antara kasir and barista?**
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

<p align="center">
  <img src="image.png" alt="Dokumentasi wawancara" width="1000">
  <br>
  <i>Gambar 1: Dokumentasi wawancara DYDY Coffee</i>
</p>

---

## ⚖️ Analisis Perbandingan SOP
| Kategori | Sistem Lama (Konvensional) | Sistem Baru (Scan-to-Order Sederhana) |
| :--- | :--- | :--- |
| **Alur Antrean** | Menumpuk di depan kasir, mengganggu arus masuk. | Terurai karena pelanggan bisa langsung duduk dan scan QR meja. |
| **Proses Memilih** | Terburu-buru karena merasa ditunggui antrean. | Lebih santai menjelajahi e-katalog digital lewat HP masing-masing. |
| **Input Pesanan** | Kasir mengetik manual satu per satu di tablet. | Pelanggan memilih secara *self-service*, kasir tinggal menerima log. |
| **Instruksi Kerja** | Bergantung pada penyampaian verbal / ketikan kasir. | Pesanan tercatat otomatis pada monitor dasbor kasir dan barista. |

---

## ⚙️ Detail Use Case (Skenario Sistem)

### A. Melakukan Pemesanan Mandiri
* **Aktor**: Pelanggan
* **Deskripsi**: Pelanggan memilih menu yang diinginkan dari meja tanpa harus mengantre di meja kasir.

🎬 **Skenario Pelanggan & Sistem**:
1. Pelanggan memindai QR Code unik yang terempel di meja masing-masing.
2. Sistem otomatis membuka e-katalog menu tanpa perlu proses login/registrasi.
3. Pelanggan menjelajahi daftar menu dan memasukkan item pilihan ke keranjang digital.
4. Pelanggan menginput nomor meja dan menekan tombol **Checkout**.
* **Kondisi Akhir**: Pesanan terkirim ke server kasir dengan status *Pending*.

---

### B. Konfirmasi & Simulasi Pembayaran
* **Aktor**: Pelanggan
* **Precondition**: Pelanggan telah melakukan *Checkout* pesanan.

🎬 **Skenario Pelanggan & Sistem**:
1. Sistem menampilkan rincian nota digital (invoice) beserta total nominal yang harus dibayar.
2. Pelanggan melihat instruksi gambar QRIS statis yang muncul di layar gawai.
3. Pelanggan melakukan transfer dan menekan tombol konfirmasi **"Saya Sudah Bayar"**.
4. Sistem mengunci halaman pelanggan dengan tampilan "Menunggu Verifikasi Kasir".
* **Kondisi Akhir**: Riwayat konfirmasi transaksi masuk ke monitor dasbor kasir.

---

### C. Verifikasi & Kelola Antrean Pesanan
* **Aktor**: Kasir
* **Precondition**: Terdapat pesanan masuk dengan status *Pending* (🟡).

🎬 **Skenario Kasir & Sistem**:
1. Kasir membuka dasbor monitor khusus staf dan memilih data pesanan terbaru.
2. Kasir memverifikasi kecocokan dana masuk pada rekening bank dengan nominal di sistem.
3. Kasir mengonfirmasi ketersediaan bahan baku menu di dapur.
4. Kasir menekan tombol **"Verifikasi / Proses"** pada sistem.
5. Sistem otomatis mengubah status pesanan menjadi *Diproses* (🔵) dan memunculkannya di monitor dapur barista.
* **Kondisi Akhir**: Status pesanan diperbarui menjadi *Diproses* dan antrean masuk ke manifes kerja barista.

<p align="center">
  <img src="diagram_usecase.png" alt="DIagram usecase" width="1000">
    <i>Gambar 2: Diagram usecase & detailnya Coffee</i>
</p>

<p align="center">
  <img src="nama file nya" alt="diagram apa" width="1000">
    <i>Gambar 2: (sesuaiin gambar ke berapa sama itu gambar apa)</i>
</p>
---

## 👥 Analisis Aktor
Berdasarkan identifikasi sistem *Scan-to-Order* DYDY Coffee, berikut adalah karakteristik, hak akses, dan batasan tanggung jawab dari setiap aktor yang terlibat:

### 1. Pelanggan (Customer) - *Primary Actor (Eksternal)*
* **Deskripsi**: Pengguna akhir yang datang ke kafe dan ingin memesan menu secara mandiri lewat meja masing-masing.
* **Hak Akses Sistem**:
  * Melakukan *scanning* QR Code meja untuk masuk ke sistem tanpa registrasi akun.
  * Melihat e-katalog menu (nama, deskripsi, gambar, dan harga real-time).
  * Menambahkan menu ke dalam keranjang belanja digital.
  * Mengisi data nomor meja dan melakukan konfirmasi/simulasi transaksi pembayaran.

### 2. Kasir (Cashier) - *Primary Actor (Internal)*
* **Deskripsi**: Staf operasional kafe yang bertanggung jawab atas validasi finansial dan kendali utama status pesanan di dasbor web.
* **Hak Akses Sistem**:
  * Mengakses halaman dasbor monitor pesanan khusus staf (*back-office*).
  * Menerima notifikasi *real-time* pesanan masuk dengan status *Pending*.
  * Melakukan verifikasi pembayaran (mencocokkan dana masuk dengan data pesanan).
  * Mengubah status pesanan dari *Pending* -> *Diproses* -> *Selesai*.

### 3. Barista - *Secondary Actor (Internal)*
* **Deskripsi**: Staf produksi yang bertanggung jawab meracik minuman dan makanan sesuai manifes pesanan.
* **Hak Akses Sistem**:
  * Memantau antrean pesanan pada monitor dapur yang berstatus *Diproses*.
  * Melihat detail pesanan (jenis varian menu, catatan khusus dari pelanggan, dan nomor meja asal).
  * Memberikan sinyal ke sistem/pelayan jika pesanan telah selesai diracik dan siap diantar.

### 4. Pelayan (Waiter) - *Secondary Actor (Internal / Pendukung)*
* **Deskripsi**: Staf lapangan yang mengantarkan menu fisik ke pelanggan. Meskipun tidak berinteraksi langsung dengan input data ke sistem web, alur kerjanya digerakkan oleh output informasi valid dari monitor dasbor kasir/barista yang menunjukkan nomor meja tujuan secara akurat.

---

## 💡 Solusi yang Diberikan
Sistem berbasis web sederhana ini dibangun untuk mempermudah operasional melalui fitur utama:
* **E-Katalog Terbuka**: Pelanggan tidak perlu mengunduh aplikasi, cukup akses cepat lewat browser HP setelah memindai QR.
* **Simpel Gateway**: Menyediakan tampilan gambar QR pembayaran statis sehingga memangkas kerumitan integrasi API bank namun fungsi pembayaran tetap tersimulasikan dengan baik.
* **Dasbor Monitor Kasir (Real-Time)**: Kasir memegang kendali penuh atas alur pemrosesan pesanan yang masuk demi menjaga kualitas pelayanan (*Hybrid Control*).

---

## 💻 Git Workflow (Panduan Kontribusi)
1. `git clone` (Clone repo ke lokal)
2. `git checkout -b NAMA_ANDA` (Buat branch baru)
3. `git add .` && `git commit -m "Pesan commit"`
4. `git push -u origin NAMA_BRANCH` (**JANGAN PUSH KE MAIN**)
5. `git pull origin main` (Update data terbaru dari pusat)
