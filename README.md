# ☕ DYDY Coffee Scan-to-Order System

[![Laravel Framework](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)](https://laravel.com)
[![MySQL Database](https://img.shields.io/badge/MySQL-00758F?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com)
[![Figma Design](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)](https://www.figma.com)

---

## 🔗 Tautan Proyek Penting

Untuk meninjau aset desain, demonstrasi sistem, dan kode sumber proyek ini, silakan akses tautan resmi di bawah ini:

* **📺 Video Presentasi & Demo Aplikasi (YouTube):** [Video Persentasi](https://youtu.be/xuw1A8ZIf2k)
* **🎨 Rancangan Antarmuka Pengguna (UI Figma):** [Desain Figma](https://www.figma.com/design/zga9oOmBJZ8eoYTyhUCSju/apbo?node-id=0-1&p=f&t=1OFRazVjugHFkz2q-0)
* **💻 Kode Sumber Aplikasi (GitHub Repository):** [Lihat Repositori GitHub (Code pembuatan web)](https://github.com/bryanhulu/DYDY-COFFE_APBO-A.git)

---

## 📝 Tentang Proyek

Proyek ini dibuat berdasarkan hasil observasi dan wawancara langsung yang dilakukan di **DYDY Coffee**. Saat ini, proses pemesanan menu masih dilakukan secara konvensional melalui kasir menggunakan perangkat tablet yang tersedia di area meja kasir.

Pada kondisi tertentu—terutama saat akhir pekan (*weekend*) atau jam-jam ramai (*rush hour*)—pelanggan kerap menghadapi antrean panjang sebelum dapat melakukan pemesanan. Keterbatasan waktu juga membuat pelanggan merasa terburu-buru saat melihat menu karena ada pelanggan lain yang sedang mengantre di belakang mereka.

Sebagai solusi dari permasalahan tersebut, kami merancang sistem **Scan-to-Order berbasis Web**. Sistem ini memungkinkan pelanggan untuk memesan makanan atau minuman secara mandiri langsung dari meja mereka masing-masing menggunakan pemindaian **QR Code**.

---

## 📸 Dokumentasi Wawancara

<p align="center">
    <img src="image.png" width="750" alt="Wawancara Owner DYDY Coffee" style="border-radius: 12px; shadow: 0 4px 6px rgba(0,0,0,0.1);">
    <br>
    <i>Gambar 1. Sesi wawancara dengan Bapak Dani selaku Owner DYDY Coffee</i>
</p>

---

## 💬 Transkrip Wawancara (QnA)

Berikut adalah detail tanya-jawab hasil wawancara bersama **Bapak Dani** selaku pemilik DYDY Coffee:

* **Q: Apakah sering terjadi antrean panjang di depan kasir saat jam sibuk?**
  > *"Pada hari hectic (weekend) tentu ada antrean yang panjang karena masih input order secara manual. Pemesanan juga bisa dilakukan lewat buku menu."*
* **Q: Seberapa sering terjadi miskomunikasi antara kasir dan barista?**
  > *"Untuk misskom dalam pemesanan sejauh ini masih aman dikarenakan staff selalu di-training dengan baik."*
* **Q: Bagaimana cara mengontrol stok yang habis di tablet kasir?**
  > *"Stok selalu dicek secara berkala oleh staff shift pagi. Sejauh ini tidak ada konsumen yang memesan menu yang sedang kosong."*
* **Q: Lebih membantu mana: Kasir tetap input manual atau struk pesanan keluar otomatis?**
  > *"Lebih membantu yang keluar langsung dari printer, karena lebih efisien dan lebih membantu yang online."*
* **Q: Apakah Kakak setuju sistem ini membuat pelanggan lebih santai memilih menu?**
  > *"Jelas lebih membantu dalam pesanan, karena customer tidak terburu-buru untuk memesan menu."*
* **Q: Apa tantangan terbesar jika sistem ini diterapkan?**
  > *"Tantangan terbesar mungkin tidak ada karena ini sangat membantu. Mungkin hanya soal disiplin update stok atau masalah jaringan/hosting yang lambat."*

---

## 📊 Hasil Analisis Wawancara

### Permasalahan yang Ditemukan
* 🚨 Proses pemesanan masih terpusat di satu titik area kasir.
* 🚨 Antrean padat rawan terjadi saat jumlah pelanggan meningkat (akhir pekan).
* 🚨 Beban kerja kasir ganda karena harus menangani pencatatan pesanan sekaligus proses pembayaran secara bersamaan.
* 🚨 Pelanggan kehilangan kenyamanan (merasa terburu-buru) saat memilih menu akibat adanya antrean di belakang mereka.

### Solusi yang Diusulkan
Menghadirkan sistem pemesanan berbasis aplikasi web (*Scan-to-Order*) menggunakan integrasi QR Code unik di setiap meja. Pelanggan dapat menjelajahi menu (*e-katalog*), memilih variasi hidangan, memasukkannya ke keranjang digital, dan melakukan *checkout* mandiri. Informasi data pesanan yang masuk akan dialirkan secara *real-time* ke dashboard kasir dan barista untuk efisiensi produksi di dapur.

### Perbandingan Sistem
| Aspek Evaluasi | Sistem Saat Ini (Manual) | Sistem Usulan (Scan-to-Order) |
| :--- | :--- | :--- |
| **Lokasi Pemesanan** | Harus berjalan dan mengantre di meja kasir | Cukup duduk diam di meja masing-masing |
| **Pencatatan Menu** | Kasir mengetik/mencatat pesanan secara manual | Sistem mencatat otomatis dari gawai pelanggan |
| **Manajemen Antrean** | Sering terjadi penumpukan pelanggan saat ramai | Antrean fisik berkurang karena proses terdesentralisasi |
| **Aliran Informasi** | Disampaikan manual (lisan/kertas kertas) ke dapur | Tersimpan permanen di database dan dashboard monitor |

---

## 👥 Aktor Sistem
1. **Pelanggan:** Memindai QR Code meja, memilih menu makanan/minuman, melakukan *checkout*, dan mengirim konfirmasi tanda bukti pembayaran.
2. **Kasir:** Memantau antrean pesanan masuk melalui dashboard, memverifikasi kesesuaian dana pembayaran, mengubah status produksi, dan mencetak struk belanja.
3. **Barista:** Menerima detail pesanan yang valid dari sistem untuk segera diproduksi di bar/dapur.
4. **Pelayan:** Mengambil pesanan yang telah selesai disiapkan oleh barista lalu mengantarkannya ke nomor meja pelanggan yang tertera pada sistem.

---

## 🔄 Alur Kerja Sistem (System Workflow)
1. Pelanggan melakukan pemindaian (**Scan**) QR Code di meja cafe.
2. Sistem mendeteksi nomor meja dan menyajikan visual **Daftar Menu** interaktif.
3. Pelanggan memilih kombinasi menu dan memasukkannya ke dalam **Keranjang Digital**.
4. Pelanggan mengisi data pelengkap lalu menekan tombol **Checkout**.
5. Sistem menyajikan **Rincian Invoice** beserta metode pembayaran (QRIS Statis).
6. Pelanggan menyelesaikan transaksi keuangan lalu menekan tombol **"Saya Sudah Bayar"**.
7. Dashboard **Kasir melakukan verifikasi** dana masuk di mutasi bank/e-wallet.
8. Dashboard **Barista menerima notifikasi** otomatis untuk meracik pesanan.
9. **Pelayan mengantarkan** sajian ke meja kustomer berdasarkan data pelacakan sistem.

---

## 📐 Pemodelan Berorientasi Objek (UML Diagrams)

### Use Case Diagram
<p align="center">
    <img width="425" alt="Use Case Diagram" src="https://github.com/user-attachments/assets/228d165e-d0c9-4646-b62d-fbdadf74104d">
    <br>
    <i>Gambar 2. Use Case Diagram Sistem Scan-to-Order DYDY Coffee</i>
</p>

#### Skenario Use Case Utama
* **A. Melakukan Pemesanan Mandiri:** Pelanggan memindai QR Code → pelanggan menginput nomor meja → sistem menampilkan e-katalog tanpa login → pelanggan memilih menu → melakukan checkout.
* **B. Konfirmasi & Pembayaran:** Sistem menampilkan rincian tagihan → pelanggan mentransfer dana/bayar di kasir → jika memilih qris maka, setelah bayar pelanggan menekan tombol "Saya Sudah Bayar" ... jika pelanggan memilih bayar cash, maka harus datang ke kasir dan membayar tagihannya → sistem mengunci halaman kustomer ke mode pending untuk tunggu verifikasi pembayaran dari kasir.
* **C. Verifikasi & Kelola Antrean:** Kasir mengecek pesanan di dashboard → memvalidasi kecocokan dana → kasir menekan tombol verifikasi → status order otomatis berubah menjadi diproses dan diteruskan ke bar.

### Class Diagram
<p align="center">
    <img width="900" alt="Class Diagram" src="https://github.com/user-attachments/assets/d6af1bc8-ca7b-46d1-b2cd-6e792966913e">
    <br>
    <i>Gambar 3. Class Diagram Struktur Data Sistem Scan-to-Order DYDY Coffee</i>
</p>

### State Diagram
<p align="center">
    <img width="850" alt="State Diagram" src="https://github.com/user-attachments/assets/da93d018-fb1c-482e-bb12-d604e4f0a8c5">
    <br>
    <i>Gambar 4. State Diagram Perubahan Status Pesanan DYDY Coffee</i>
</p>

### Sequence Diagram
<p align="center">
    <img width="900" alt="Sequence Diagram" src="https://github.com/user-attachments/assets/d81296df-922f-4b07-b60a-29ed7383ab49">
    <br>
    <i>Gambar 5. Sequence Diagram Interaksi Komponen Sistem Scan-to-Order DYDY Coffee</i>
</p>

### Activity Diagram
<p align="center">
    <img width="850" alt="Activity Diagram" src="https://github.com/user-attachments/assets/acc5eb08-1f97-43f4-8c50-c0b3a10db729">
    <br>
    <i>Gambar 6. Activity Diagram Alur Kerja Sistem Scan-to-Order DYDY Coffee</i>
</p>

---

## 🛠️ Spesifikasi Teknologi (Tech Stack)

Aplikasi dikembangkan menggunakan standar arsitektur modern berbasis monolitik yang efisien:
* **Backend Framework:** Laravel (PHP 8.x)
* **Frontend Languages:** HTML5, JavaScript (ES6+), CSS3
* **CSS Framework:** Tailwind CSS
* **Database Management:** MySQL

---

## 👥 Tim Pengembang (Kelompok Tugas Besar)

Proyek Analisis & Perancangan Berorientasi Objek (APBO) Kelas A ini disusun oleh:

| Nama Pengembang | NPM (Nomor Pokok Mahasiswa) | Peran Fokus |
| :--- | :--- | :--- |
| **Bryan Ananda Saputra Hulu** | 4524210020 | Lead Backend & Database Architect |
| **Muhammad Agis Irawan** | 4524210056 | System Analyst & UML Modeling |
| **M. Al Ghifari** | 4524210052 | Software Tester & QA |
| **Bayu Sardo Situmorang** | 4524210019 | UI/UX Designer & Frontend Developer |
| **Dzikrullah Surachman** | 4524210029 | Technical Writer & Documentation |

---

## 🚀 Panduan Alur Kerja Git (Git Workflow)

Gunakan standardisasi perintah di bawah ini untuk berkolaborasi di dalam repositori ini:

```bash
# 1. Salin repositori ke komputer lokal
git clone [https://github.com/bryanhulu/DYDY-COFFE_APBO-A.git](https://github.com/bryanhulu/DYDY-COFFE_APBO-A.git)

# 2. Pindah ke folder proyek dan buat branch baru untuk fiturmu
git checkout -b nama_branch_fitur

# 3. Rekam perubahan kode setelah selesai pengerjaan
git add .

# 4. Buat catatan komit yang deskriptif
git commit -m "feat: menambah animasi pembayaran sukses gopay style"

# 5. Unggah perubahan branch kamu ke GitHub remote
git push -u origin nama_branch_fitur

# 6. Selalu sinkronkan branch lokal dengan update terbaru dari main branch
git pull origin main
