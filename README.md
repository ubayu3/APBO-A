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


# Laporan Pengembangan Sistem: Scan-to-Order DYDY Coffee

## Latar Belakang
Berdasarkan hasil observasi dan wawancara yang dilakukan dengan **Bapak Dani** selaku pemilik **DYDY Coffee**, ditemukan bahwa sistem operasional pemesanan saat ini masih menghadapi kendala, terutama pada saat jam sibuk (*rush hour*). Saat ini, proses pemesanan masih terpusat di satu meja kasir menggunakan satu perangkat tablet, sehingga menyebabkan penumpukan antrean (*queue bottleneck*) di area pintu masuk.

Selain masalah antrean, pelanggan sering kali merasa tertekan secara psikologis ketika harus memilih menu di depan kasir sementara antrean di belakangnya sudah memanjang, yang mengakibatkan pelanggan memilih menu secara terburu-buru. Di sisi lain, staf kasir menjadi kurang fleksibel karena harus terus berjaga di meja kasir untuk menginput pesanan secara manual.

Oleh karena itu, proyek ini bertujuan untuk mengembangkan **Sistem Informasi Scan-to-Order berbasis web**. Dengan sistem ini, pelanggan dapat memesan langsung dari meja masing-masing melalui QR Code. Implementasi ini diharapkan dapat mempercepat alur transaksi dan meminimalisir kesalahan komunikasi, namun tetap menjaga aspek pelayanan (*hospitality*) melalui interaksi saat verifikasi pesanan dan penyajian menu.

---

## Sasaran Pengguna
*   **Kasir & Barista**: Bertugas memvalidasi pesanan yang masuk, memantau ketersediaan stok secara *real-time*, dan menjalankan instruksi kerja berdasarkan struk pesanan otomatis.
*   **Pelanggan (Customer)**: Pengunjung cafe yang menginginkan kemudahan memesan menu secara mandiri dan santai langsung dari meja tanpa harus mengantre lama di kasir.

---

## Analisis Perbandingan Sistem

| Kategori | Sistem Lama (Konvensional) | Sistem Baru (Scan-to-Order) |
| :--- | :--- | :--- |
| **Alur Antrean** | Menumpuk di depan kasir, mengganggu arus masuk. | Terurai karena pelanggan memesan langsung dari meja. |
| **Proses Memilih** | Terburu-buru karena merasa ditunggui antrean belakang. | Lebih santai, pelanggan bebas melihat detail menu di HP. |
| **Input Pesanan** | Kasir mengetik manual satu per satu di tablet. | Pelanggan input mandiri; Kasir tinggal verifikasi & bayar. |
| **Komunikasi** | Bergantung pada penyampaian verbal atau input manual. | Struk otomatis tercetak di Bar sebagai instruksi kerja. |

---

## Struktur Use Case Diagram
Sistem ini membagi fungsionalitas berdasarkan peran aktor utama untuk menjamin alur kerja yang terstruktur:

### **Aktor & Peran Sistem**
*   **Pelanggan**: Melakukan pemindaian QR Code meja, memilih menu melalui katalog digital, melakukan pemesanan, dan melakukan pembayaran mandiri.
*   **Kasir**: Menerima notifikasi pesanan, melakukan verifikasi pembayaran, mengecek ketersediaan bahan, dan memberikan instruksi produksi melalui cetak struk.
*   **Barista/Dapur**: Menerima instruksi kerja berupa struk fisik dan memproses pesanan sesuai urutan.
*   **Pelayan**: Mengantarkan pesanan ke meja pelanggan sesuai dengan nomor meja yang tertera pada struk.

### **Fungsionalitas Utama (Use Case)**
1.  **Pemesanan Mandiri**: Pelanggan melakukan input pesanan langsung ke sistem tanpa melalui perantara kasir.
2.  **Verifikasi & Kontrol Stok**: Kasir memiliki kendali penuh untuk memperbarui status stok secara instan agar tidak terjadi salah pesan pada menu yang habis.
3.  **Integrasi Produksi**: Sistem secara otomatis mengirimkan perintah cetak struk ke bagian produksi setelah pesanan divalidasi oleh kasir.

---

## Langkah Antisipasi & Resiliensi Sistem
Untuk menjamin keberlangsungan operasional, telah disusun strategi mitigasi sebagai berikut:
*   **Infrastruktur Jaringan**: Menggunakan hosting dengan performa tinggi dan menyediakan WiFi khusus pelanggan yang terpisah dari jaringan operasional kasir untuk menjaga keamanan data.
*   **Offline Mode Standby**: Tetap menyediakan katalog fisik (*hardcopy*) sebagai cadangan darurat apabila terjadi gangguan pada penyedia layanan internet (ISP).
*   **Hybrid Service Support**: Staf tetap bersiaga di area meja untuk membantu pelanggan yang kesulitan dalam melakukan navigasi menu digital atau pemindaian QR Code.

---

## Kesimpulan
Permasalahan utama pada **DYDY Coffee** adalah efisiensi alur pemesanan yang menyebabkan penumpukan antrean dan tekanan pada pelanggan. Solusi **Scan-to-Order** berbasis web dengan konsep **Hybrid Control** memungkinkan proses transaksi menjadi lebih cepat dan terdata dengan baik, namun tetap mengedepankan aspek keramahan yang menjadi ciri khas layanan DYDY Coffee.

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
Diagram Use Case:
Rincian Alur Sistem (Proses Inti):
1. Pemesanan Mandiri: Pelanggan scan QR Code di meja, memilih menu, dan mengirim pesanan ke sistem.
2. Verifikasi Kasir: Kasir menerima notifikasi, mengecek stok, dan memvalidasi pembayaran pelanggan.
3. Integrasi Produksi: Setelah divalidasi, sistem mengirim perintah cetak struk ke area Barista untuk diproses.
4. Kontrol Layanan: Staf tetap bisa melakukan interaksi personal saat mengantar pesanan ke meja.

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

## Kesimpulan & Solusi yang Diberikan
Berdasarkan analisis, permasalahan utama pada DYDY Coffee adalah antrean panjang di kasir, tekanan pelanggan saat memilih menu, serta risiko kesalahan komunikasi dalam pesanan. Hal ini disebabkan oleh sistem pemesanan yang masih terpusat dan dilakukan secara manual, sehingga alur operasional menjadi kurang efisien.

Solusi yang diberikan adalah penerapan sistem Scan-to-Order berbasis web dengan konsep Hybrid Control, di mana pelanggan dapat memesan langsung dari meja melalui QR Code, sementara kasir tetap berperan sebagai pengendali untuk memverifikasi pesanan, ketersediaan stok, dan pembayaran. Sistem ini mampu meningkatkan kecepatan, ketepatan, dan keteraturan proses, sekaligus tetap mempertahankan interaksi pelayanan (hospitality) antara staf dan pelanggan.

--- 

## 📌 GIT WORKFLOW (Panduan Kontribusi)
1.  `git clone` (Clone repo ke local)
2.  `git checkout -b NAMAKALIAN` (Membuat branch dengan nama sendiri)
3.  `git checkout branch_tujuan` (Pindah branch kalian atau ke main)
4.  `git add .` (Menambah perubahan yang ingin dicommit)
5.  `git commit -m "pesan commit"` (Commit perubahan)
6.  `git push -u origin BRANCHKALIAN` (Push ke branch sendiri, **JANGAN KE MAIN!!**)
7.  `git pull origin main` (Pull dari main ketika sudah merge final)
8.  `git merge main` (Merge perubahan main yang terupdate ke branch sendiri)
