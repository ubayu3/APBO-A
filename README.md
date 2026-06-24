# DYDY Coffee Scan-to-Order System

Sistem pemesanan berbasis QR Code untuk membantu proses pemesanan pelanggan di DYDY Coffee secara lebih praktis dan efisien.

---

## Tentang Proyek

DYDY Coffee saat ini masih menggunakan proses pemesanan yang berpusat pada area kasir. Saat kondisi ramai, pelanggan harus mengantre untuk melakukan pemesanan sehingga proses pelayanan menjadi lebih lambat.

Berdasarkan hasil wawancara dengan owner DYDY Coffee, salah satu kendala yang sering terjadi adalah antrean pada akhir pekan atau jam sibuk. Oleh karena itu, dikembangkan sistem **Scan-to-Order berbasis web** yang memungkinkan pelanggan melakukan pemesanan langsung dari meja menggunakan QR Code.

---

## Dokumentasi Wawancara

<p align="center">
    <img src="image.png" width="800">
</p>

<p align="center">
    <i>Gambar 1. Dokumentasi wawancara dengan owner DYDY Coffee</i>
</p>

---

## Permasalahan yang Ditemukan

* Pemesanan masih dilakukan secara manual melalui kasir.
* Antrean pelanggan meningkat saat jam sibuk.
* Kasir harus menangani pencatatan pesanan sekaligus pembayaran.
* Pelanggan memiliki waktu terbatas saat memilih menu.

---

## Solusi yang Diusulkan

Sistem Scan-to-Order dirancang untuk membantu proses pemesanan dengan fitur berikut:

* Pemesanan melalui QR Code.
* Katalog menu digital.
* Keranjang belanja (cart).
* Konfirmasi pembayaran.
* Dashboard monitoring pesanan.
* Manajemen status pesanan.

---

## Analisis Sistem

| Sistem Lama                          | Sistem Usulan                     |
| ------------------------------------ | --------------------------------- |
| Pemesanan melalui kasir              | Pemesanan melalui QR Code         |
| Input pesanan dilakukan kasir        | Input pesanan dilakukan pelanggan |
| Antrean sering terjadi saat ramai    | Antrean dapat dikurangi           |
| Informasi pesanan disampaikan manual | Informasi tersimpan pada sistem   |

---

## Aktor Sistem

### Pelanggan

* Memindai QR Code.
* Melihat daftar menu.
* Melakukan pemesanan.
* Melakukan konfirmasi pembayaran.

### Kasir

* Memverifikasi pembayaran.
* Mengelola status pesanan.
* Memantau pesanan yang masuk.

### Barista

* Melihat daftar pesanan.
* Menyiapkan pesanan sesuai data sistem.

### Pelayan

* Mengantarkan pesanan ke meja pelanggan.

---

## Use Case Diagram

<p align="center">
    <img src="diagram_usecase.png" width="900">
</p>

<p align="center">
    <i>Gambar 2. Use Case Diagram Sistem Scan-to-Order</i>
</p>

---

## Alur Pemesanan

1. Pelanggan memindai QR Code pada meja.
2. Sistem menampilkan daftar menu.
3. Pelanggan memilih menu yang diinginkan.
4. Pelanggan melakukan checkout.
5. Sistem menampilkan rincian pembayaran.
6. Pelanggan melakukan konfirmasi pembayaran.
7. Kasir melakukan verifikasi.
8. Barista memproses pesanan.
9. Pelayan mengantarkan pesanan ke meja pelanggan.

---

## Teknologi yang Digunakan

* Laravel
* PHP
* MySQL
* HTML
* CSS
* JavaScript

---

## Struktur Tim

| Nama                      | NPM        |
| ------------------------- | ---------- |
| Bryan Ananda Saputra Hulu | 4524210020 |
| Muhammad Agis Irawan      | 4524210056 |
| M. Al Ghifari             | 4524210052 |
| Bayu Sardo Situmorang     | 4524210019 |
| Dzikrullah Surachman      | 4524210029 |

---

## Git Workflow

```bash
git clone <repository>

git checkout -b nama_branch

git add .
git commit -m "pesan commit"

git push -u origin nama_branch

git pull origin main
```

---

## Kesimpulan

Berdasarkan hasil analisis dan wawancara yang telah dilakukan, sistem Scan-to-Order dapat membantu mengurangi antrean pelanggan serta mempermudah proses pemesanan di DYDY Coffee. Sistem ini memungkinkan pelanggan melakukan pemesanan secara mandiri melalui QR Code sehingga proses pelayanan menjadi lebih terorganisir.
