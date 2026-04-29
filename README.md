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

**Tema Tugas:**
OPTIMALISASI ALUR PEMESANAN PADA DYDY COFFEE

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
