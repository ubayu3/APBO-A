# APBO-A KEL-5 
## LAPORAN TUGAS APBO: OPTIMALISASI ALUR PEMESANAN PADA DYDY COFFEE
**Dosen:** Adi Wahyu Pribadi, S.Si., M.Kom

---

### **Anggota Kelompok 5:**
* **4524210020** - Bryan Ananda Saputra Hulu
* **4524210056** - Muhammad Agis Irawan
* **4524210052** - M. AL GHIFARI
* **4524210019** - Bayu Sardo Situmorang
* **4524210029** - Dzikrullah Surachman


<br><br>

![alt text](image.png)

<br><br>

**Tema Tugas:**
OPTIMALISASI ALUR PEMESANAN PADA DYDY COFFEE


---
## 📖 Latar Belakang
DYDY Coffee saat ini menghadapi tantangan operasional dalam menangani lonjakan pelanggan di jam sibuk. Berdasarkan wawancara dengan Bapak Dani, sistem pemesanan konvensional di kasir menyebabkan penumpukan antrean (queue bottleneck). Hal ini memberikan tekanan psikologis bagi pelanggan saat memilih menu dan membuat staf kasir tidak fleksibel untuk membantu pelayanan di area meja.

Ketiadaan sistem pemesanan mandiri membuat alur kerja menjadi kurang efektif. Oleh karena itu, diperlukan sistem informasi Scan-to-Order berbasis web untuk mempercepat proses transaksi, meminimalisir kesalahan pesanan, namun tetap menjaga interaksi hangat (hospitality) yang menjadi ciri khas DYDY Coffee.

---
## 🎯 Sasaran Pengguna

👨‍💼 Kasir & Barista: Pengelola yang memvalidasi pesanan, memantau ketersediaan stok, dan menerima instruksi kerja otomatis di area produksi.

🧑‍💻 Customer (Pelanggan): Pengunjung yang menginginkan kemudahan memesan menu langsung dari meja tanpa harus mengantre lama di kasir.

---

## ⚖️ Bagian 1: Analisis Perbandingan Sistem

| Kategori | Sistem Lama (Konvensional) | Sistem Baru (Digital Scan-to-Order) |
| :--- | :--- | :--- |
| **Alur Antrean** | Menumpuk di depan kasir, mengganggu arus masuk. | Terurai karena pelanggan memesan langsung dari meja. |
| **Proses Memilih** | Terburu-buru karena merasa ditunggu antrean belakang. | Lebih santai, pelanggan bebas melihat detail menu di HP. |
| **Input Pesanan** | Kasir mengetik manual satu per satu di tablet. | Pelanggan input mandiri; Kasir tinggal verifikasi & bayar. |
| **Komunikasi Barista** | Bergantung pada penyampaian verbal atau input manual. | Struk otomatis tercetak di Bar sebagai instruksi kerja sah. |

---

## 📌 Bagian 2: Skenario Sistem (Use Case)
Diagram Use Case:
Rincian Alur Sistem (Proses Inti):
1. Pemesanan Mandiri: Pelanggan scan QR Code di meja, memilih menu, dan mengirim pesanan ke sistem.
2. Verifikasi Kasir: Kasir menerima notifikasi, mengecek stok, dan memvalidasi pembayaran pelanggan.
3. Integrasi Produksi: Setelah divalidasi, sistem mengirim perintah cetak struk ke area Barista untuk diproses.
4. Kontrol Layanan: Staf tetap bisa melakukan interaksi personal saat mengantar pesanan ke meja.

---
## 🛡️ Bagian 3: Langkah Antisipasi Kendala
Bagian 3: Langkah Antisipasi Kendala & Resiliensi Sistem
Untuk menjamin keberlangsungan operasional dan kenyamanan pelanggan di DYDY Coffee, kami telah menyusun strategi mitigasi terhadap potensi hambatan teknis maupun non-teknis:

1. Stabilitas Konektivitas & Infrastruktur Jaringan
Ketergantungan pada sistem berbasis web menuntut infrastruktur jaringan yang kokoh. Langkah yang diambil meliputi:

Implementasi High-Performance Hosting: Menggunakan layanan hosting dengan uptime tinggi dan latency rendah untuk memastikan akses menu digital tetap cepat meskipun diakses banyak pengguna secara bersamaan.

Dedicated Customer WiFi: Menyediakan jaringan WiFi khusus pelanggan yang terpisah dari jaringan operasional kasir. Hal ini dilakukan untuk menghindari interferensi sinyal dan menjaga keamanan data internal cafe.

Offline Mode Standby: Menyiapkan katalog fisik (hardcopy) sebagai cadangan (backup) darurat apabila terjadi gangguan total pada penyedia layanan internet (ISP).

2. Edukasi Pelanggan & Inklusivitas Layanan
Kami menyadari adanya variasi tingkat literasi digital di kalangan pelanggan. Strategi antisipasinya adalah:

Hybrid Service Support: Staf tetap bersiaga (standby) di area meja untuk memberikan panduan langsung bagi pelanggan yang kesulitan melakukan pemindaian QR Code atau navigasi menu.

Visual Guide Stand: Menempatkan instruksi visual yang ringkas dan menarik di setiap meja tentang cara memesan melalui sistem Scan-to-Order.

Human-Centered Technology: Sistem dirancang hanya sebagai alat bantu efisiensi, sementara aspek keramahan (hospitality) tetap diutamakan melalui interaksi manual saat penyajian menu dan proses verifikasi akhir di kasir.

3. Sinkronisasi Data & Stok Real-Time
Untuk menghindari pelanggan memesan menu yang ternyata sudah habis:

Admin Control Panel: Menyediakan fitur bagi kasir untuk memperbarui status ketersediaan stok secara instan, sehingga menu yang habis akan langsung tertandai secara otomatis di sisi pelanggan.


## 📌 GIT WORKFLOW (Panduan Kontribusi)
1.  `git clone` (Clone repo ke local)
2.  `git checkout -b NAMAKALIAN` (Membuat branch dengan nama sendiri)
3.  `git checkout branch_tujuan` (Pindah branch kalian atau ke main)
4.  `git add .` (Menambah perubahan yang ingin dicommit)
5.  `git commit -m "pesan commit"` (Commit perubahan)
6.  `git push -u origin BRANCHKALIAN` (Push ke branch sendiri, **JANGAN KE MAIN!!**)
7.  `git pull origin main` (Pull dari main ketika sudah merge final)
8.  `git merge main` (Merge perubahan main yang terupdate ke branch sendiri)

---

## 1. Topik Proyek
"Optimalisasi Alur Pemesanan melalui Sistem Scan-to-Order Berbasis Web dengan Kasir sebagai Pusat Kendali Operasional (Studi Kasus: Coffee Shop DYDY)."

## 2. Identifikasi Masalah (Problem)
Berdasarkan observasi pada sistem pemesanan yang saat ini terpusat di satu tablet kasir:

### Antrean Fisik (Queue Bottleneck)
* Pelanggan tetap harus berdiri mengantre di kasir meskipun sudah menggunakan tablet. Ini menghambat pelanggan lain yang ingin segera duduk atau masuk.
* Owner mengonfirmasi bahwa pada hari sibuk (weekend), terjadi antrean panjang akibat input order yang masih manual.

### Tekanan Saat Memesan
* Pelanggan sering merasa terburu-buru memilih menu karena ada antrean di belakangnya, sehingga jarang melakukan pesanan tambahan (add-ons).

### Risiko Operasional
* **Risiko Salah Komunikasi:** Tanpa dokumentasi yang teratur, risiko kesalahan pembuatan menu oleh barista tetap tinggi.
* **Keterbatasan Jangkauan:** Staf kasir tidak bisa meninggalkan meja kasir karena harus menjaga satu-satunya akses pemesanan (tablet).

## 3. Analisa Solusi
Sistem dirancang agar kasir berfungsi sebagai penyaring (filter) utama dengan keunggulan:
* **Kontrol Kualitas & Stok:** Kasir dapat memvalidasi stok secara manual sebelum barista mulai bekerja.
* **Sentuhan Manusia (Hospitality):** Menjaga interaksi antara staf dan pelanggan agar kasir tetap menjadi pengelola alur pesanan, bukan sekadar penerima uang.
* **Validasi Pembayaran:** Kasir memastikan status "Paid" sesuai dengan dana yang masuk sebelum memerintahkan produksi.

## 4. Struktur Aktor dan Use Case

### Aktor Sistem
1.  **Pelanggan:** Melakukan scan QR, memilih menu, dan membayar mandiri melalui web.
2.  **Kasir:** Memverifikasi pesanan, mengecek ketersediaan bahan, dan memberikan instruksi produksi (struk fisik).
3.  **Barista/Dapur:** Membuat pesanan berdasarkan urutan struk fisik yang diterima dari kasir.
4.  **Pelayan:** Mengantarkan pesanan ke meja sesuai nomor yang tertera di struk.

### Use Case Utama
* **Scan-to-Order:** Pelanggan memindai QR Code unik di setiap meja.
* **Pemesanan Mandiri:** Pelanggan memilih menu dan membayar via e-wallet di halaman web.
* **Verifikasi Pusat:** Kasir menerima notifikasi pesanan dan mencetak struk otomatis untuk divalidasi.

## 5. Diagram Workflow (Alur Kerja/SOP)
1.  **Pemisahan Meja:** Setiap meja diberikan QR Code unik yang tertanam nomor mejanya.
2.  **Pemesanan Mandiri:** Pelanggan duduk, scan, memilih menu, dan membayar langsung di web.
3.  **Verifikasi Pusat (Kasir):** Pesanan masuk ke tablet kasir; printer mencetak struk secara otomatis.
4.  **Instruksi Produksi:** Kasir mengecek stok, lalu menyerahkan struk fisik ke Barista sebagai tanda "Sah".
5.  **Proses Pembuatan:** Barista membuat pesanan berdasarkan urutan struk fisik.
6.  **Pengantaran (Serving):** Pelayan mengantarkan pesanan ke meja sesuai nomor di struk.
7.  **Penyelesaian:** Pelanggan bisa langsung pulang tanpa harus kembali ke kasir (mengurangi kerumunan).

<img width="708" height="400" alt="WF2" src="https://github.com/user-attachments/assets/00c43213-015e-499c-8f70-00384ff603b7" />


## 6. Hasil Validasi (Interview Owner)
Hasil wawancara dengan Dani (Owner DYDY):
* Sistem keluar struk otomatis dinilai jauh lebih efisien dan membantu dibandingkan input manual.
* Owner setuju bahwa sistem ini memberikan kenyamanan bagi pelanggan agar tidak terburu-buru memesan.
* Tantangan utama adalah pengelolaan update stok secara berkala serta stabilitas jaringan/hosting web.

## 💡 Rangkuman & Usulan yang Diberikan
Setelah menilai, masalah utama yang dihadapi DYDY Coffee adalah antrian yang lama di kasir, tekanan dari pelanggan saat memilih menu, dan kemungkinan kesalahan komunikasi dalam pesanan. Situasi ini terjadi karena sistem pemesanan masih terpusat dan dilakukan secara manual, sehingga proses operasional menjadi tidak efisien.

Usulan yang diberikan adalah penerapan sistem Scan-to-Order berbasis web dengan kontrol Hybrid, di mana pelanggan bisa memesan langsung dari meja melalui QR Code, sementara kasir berfungsi sebagai pengendali untuk memverifikasi pesanan, persediaan, dan pembayaran. Sistem ini mempercepat, mempermudah, dan menstrukturkan proses, namun tetap mempertahankan interaksi yang ramah antara staf dan pelanggan.
