# Tugas Pendahuluan Modul 6 Pemrograman Web: JavaScript dan jQuery

- **Nama:** Angga Farhat Diziky
- **NIM:** 103092400060
- **Program Studi:** Teknologi Informasi, Telkom University
- **Mata Kuliah:** Pemrograman Web, Ganjil 2026/2027

## Isi Repository

| File | Keterangan |
|------|------------|
| `soal1.html`, `style1.css` | Soal 4: prompt nama dan NIM dengan JavaScript |
| `soal2.html`, `style2.css` | Soal 5: Bermain dengan Warna dengan jQuery |
| `screenshots/` | Screenshot hasil program |

Cara menjalankan: buka folder di VS Code, klik kanan file HTML, lalu pilih **Open with Live Server**. Soal 5 membutuhkan koneksi internet karena jQuery dimuat dari CDN.

---

## 1. Apa itu JavaScript dan kegunaannya?

JavaScript adalah bahasa pemrograman tingkat tinggi yang bersifat interpreted dan dijalankan langsung oleh browser. Bersama HTML (struktur) dan CSS (tampilan), JavaScript berperan sebagai pembuat perilaku atau interaksi pada halaman web, sehingga halaman tidak hanya statis tetapi dapat merespons aksi pengguna.

Kegunaan JavaScript antara lain:
- memanipulasi elemen HTML dan CSS melalui DOM (mengubah teks, warna, menambah atau menghapus elemen)
- menangani event seperti klik, input, dan submit
- validasi form di sisi klien sebelum data dikirim ke server
- mengambil data dari server tanpa memuat ulang halaman (AJAX/Fetch API)
- membuat animasi, slider, dan efek interaktif
- membangun aplikasi web yang lengkap, baik di sisi klien (React, Vue) maupun sisi server (Node.js)

## 2. Apa itu jQuery dan kegunaannya?

jQuery adalah library JavaScript yang ringan dan open source dengan semboyan "write less, do more". jQuery menyediakan fungsi-fungsi siap pakai dengan sintaks yang lebih singkat untuk pekerjaan umum JavaScript, serta menyembunyikan perbedaan perilaku antar browser.

Kegunaan jQuery antara lain:
- memilih dan memanipulasi elemen DOM dengan selector bergaya CSS, misalnya `$("#kotak")`
- menangani event dengan mudah, misalnya `.click()`
- mengubah gaya elemen dengan `.css()`
- membuat efek dan animasi sederhana seperti `.hide()`, `.show()`, `.fadeIn()`, dan `.slideUp()`
- mempermudah permintaan AJAX melalui `$.ajax()`

## 3. Perbedaan JavaScript dan jQuery

JavaScript adalah bahasa pemrogramannya, sedangkan jQuery hanyalah library yang ditulis menggunakan JavaScript untuk mempermudah penulisan kode.

| Aspek | JavaScript | jQuery |
|-------|------------|--------|
| Jenis | Bahasa pemrograman yang berjalan native di browser. | Library (kumpulan fungsi) yang dibangun di atas JavaScript. |
| Instalasi | Tidak perlu, sudah tersedia di browser. | Harus di-import (file lokal atau CDN) sebelum dipakai. |
| Sintaks | Lebih panjang, misalnya `document.getElementById("id").style.color = "red"`. | Lebih ringkas, misalnya `$("#id").css("color", "red")`. |
| Seleksi elemen | `getElementById`, `querySelector`, dan sejenisnya. | Selector bergaya CSS lewat fungsi `$()`. |
| Efek/animasi | Dibuat manual dengan CSS atau JS. | Tersedia siap pakai: `hide`, `show`, `fadeIn`, `slideUp`, `animate`. |
| Kompatibilitas browser | Perlu ditangani sendiri bila ada perbedaan antar browser. | Menangani perbedaan antar browser secara otomatis. |
| Ukuran dan performa | Tanpa beban tambahan sehingga lebih cepat dan ringan. | Perlu memuat file library sehingga ada tambahan ukuran. |
| Fleksibilitas | Dapat dipakai untuk semua kebutuhan, termasuk di sisi server (Node.js). | Terbatas pada manipulasi DOM, event, efek, dan AJAX di sisi klien. |

Kesimpulannya, jQuery tidak menggantikan JavaScript. Semua kode jQuery pada akhirnya dijalankan sebagai JavaScript, dan jQuery hanya menyediakan cara penulisan yang lebih singkat dan seragam.

---

## 4. Edit `soal1.html` (JavaScript: prompt nama dan NIM)

Saat halaman dibuka (event `onload` pada body), fungsi `mintaData()` menampilkan dua prompt untuk meminta nama dan NIM. Hasil inputan kemudian dimasukkan ke field Nama dan NIM pada form oleh fungsi `tampilkanData()` menggunakan `document.getElementById(...).value`. Kode ini juga memperbaiki typo pada template, yaitu tag penutup `</title>` yang kurang tanda `<`.

![Hasil form soal1.html setelah nama dan NIM diinput melalui prompt](screenshots/soal4-hasil-form.png)

## 5. Edit `soal2.html` (jQuery: Bermain dengan Warna)

Pada bagian head ditambahkan jQuery melalui CDN (`jquery-3.7.1.min.js`). Seluruh event dipasang di dalam `$(document).ready()` agar dijalankan setelah DOM siap. Tombol Ungu, Biru, dan Hijau mengubah `background-color` elemen `#kotakWarna` memakai `.css()` (efek transisi 0.5 detik berasal dari `style2.css`). Tombol Sembunyikan memakai `.hide()` dan tombol Tampilkan memakai `.show()`.

**Tombol Ungu**

![Tombol Ungu](screenshots/soal5-ungu.png)

**Tombol Biru**

![Tombol Biru](screenshots/soal5-biru.png)

**Tombol Hijau**

![Tombol Hijau](screenshots/soal5-hijau.png)

**Tombol Sembunyikan Kotak**

![Tombol Sembunyikan Kotak](screenshots/soal5-sembunyi.png)
