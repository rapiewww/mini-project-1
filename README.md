# Mini Project 1: Product Information System

Proyek ini adalah implementasi sistem manajemen data informasi produk sederhana berbasis PHP murni. Proyek ini dibangun berdasarkan konsep arsitektur desain konseptual dari materi "Pemrograman Web - Pertemuan 2: PHP Fundamental & Data Structure".

## 🏗️ Arsitektur Proyek (Separation of Concerns)

Aplikasi ini menerapkan konsep pemrograman modular dengan membagi kode ke dalam tiga layer utama:

1. **Data Layer (`products.php`)**
   Berfungsi sebagai basis data *dummy* menggunakan *multidimensional associative array*. File ini menyimpan detail informasi komoditas produk seperti ID, Nama, Kategori, Harga, Stok, dan Deskripsi.

2. **Processing Layer (`functions.php`)**
   Berisi kumpulan fungsi khusus untuk menangani logika bisnis dan kalkulasi:
   * `hitungTotalNilaiStok()`: Menghitung nilai aset gudang (Harga × Stok).
   * `cekStatusStok()`: Mengembalikan *style* CSS khusus (warna latar merah muda) jika jumlah stok berada pada level kritis (kurang dari 3).

3. **Presentation Layer (`index.php`)**
   Bertindak sebagai antarmuka pengguna (UI) yang merajut seluruh komponen menggunakan `require_once`. File ini merender data dari *Data Layer* ke dalam bentuk tabel HTML menggunakan perulangan `foreach`.

## ✨ Fitur Utama

* **Modularisasi Kode:** Memisahkan data, logika, dan tampilan antarmuka.
* **Kalkulasi Otomatis:** Menghitung total nilai aset untuk setiap baris produk secara otomatis.
* **Peringatan Stok Kritis (Visual):** Baris tabel akan berubah warna secara otomatis jika stok suatu produk berada di bawah batas aman (< 3).

## 🚀 Cara Menjalankan Aplikasi

1. **Persiapan Lingkungan:** Pastikan Anda memiliki *local web server* yang mendukung PHP (seperti XAMPP, MAMP, Laragon, atau menggunakan PHP Built-in Server).
2. **Ekstraksi File:** Buat folder baru di dalam direktori root server Anda (misal: `htdocs/produk-katalog/`) dan letakkan ketiga file (`products.php`, `functions.php`, dan `index.php`) ke dalam folder tersebut.
3. **Akses via Browser:** Buka web browser Anda dan akses URL folder tersebut (contoh: `http://localhost/produk-katalog/`).
4. **Alternatif (PHP Built-in Server):** 
   * Buka terminal/command prompt.
   * Arahkan ke direktori tempat file disimpan.
   * Jalankan perintah: `php -S localhost:8000`
   * Buka browser dan akses: `http://localhost:8000`

## 📚 Konsep Pembelajaran Terkait
* *Multidimensional Associative Array*
* *Custom Functions* (Parameter & Return Value)
* *Conditional Logic* (If/Else)
* *Control Flow* (`foreach` loop)
* *File Inclusion* (`require_once`)