# **Latihan: Menambahkan List pada Halaman Profil**

### **Tujuan**

*   **Navigation list** berfungsi sebagai menu untuk berpindah ke bagian tertentu dari halaman.
*   Kita gunakan elemen `**<ul>**` **(unordered list)** untuk menampung daftar menu.
*   Di dalam `<ul>` terdapat beberapa `**<li>**` **(list item)**, masing-masing berisi tautan `<a>` ke bagian tertentu.
*   `<nav>` → wadah navigasi.
*   `<ul>` → daftar menu tanpa urutan.
*   `<li>` → item dalam daftar.
*   `<a href="#id">` → tautan menuju bagian dengan **id** yang sama di halaman.

Hasil akhirnya akan tampak seperti berikut.

![](https://file+.vscode-resource.vscode-cdn.net/c%3A/Users/asust/OneDrive/Dokumen/Materi%202025/X%20RPL/img_halaman_profil/image.jpg?version%3D1758353672139)

> Tips:
> 
> Pada langkah ini dan berikutnya, sebaiknya gunakanlah code editor yang disarankan pada pembahasan Requirement Tools agar proses penulisan dan pengelolaan berkas HTML dapat lebih cepat.

### **Alur Latihan**

Berikut adalah alur latihan kali ini.

1.  Membuka hasil latihan terakhir dengan VSCode.
2.  Menuliskan navigation list pada dokumen HTML.
3.  Menjalankan dokumen HTML pada browser.

### **Latihan Menambahkan List pada Halaman Profil**

Silakan ikuti dan simak beberapa langkah berikut untuk mengikuti latihan dengan baik.

1.  Silakan buka proyek Halaman Profil terakhir dengan VS Code. Jika belum memilikinya, silakan unduh proyek tersebut pada [GitHub repository ini](https://github.com/dicodingacademy/a123-webdasar-labs/tree/102-identifikasi-elemen-halaman-profil).
2.  Kita akan menambahkan daftar navigasi menggunakan elemen list. Silakan buka berkas index.html dan tambahkan elemen unordered list berikut di bawah dari elemen paragraf pertama pada berkas HTML. Elemen yang ditambahkan memiliki cetakan tebal

```html
<!-- Kode lainnya disembunyikan... -->

 <body>

      <h1>Bandung</h1>

 <p>
        Kota metropolitan terbesar di Provinsi Jawa Barat, sekaligus menjadi ibu kota provinsi tersebut.
</p>
    <ul>
       <li>Sejarah</li>
       <li>Geografis</li>  
       <li>Wisata</li>
    </ul>

<h2>Sejarah</h2>

<!-- Kode lainnya disembunyikan... -->

</body>
```

Hasilnya akan tampak seperti berikut.  
![](https://file+.vscode-resource.vscode-cdn.net/c%3A/Users/asust/OneDrive/Dokumen/Materi%202025/X%20RPL/img_halaman_profil/image.jpg?version%3D1758353672139)**Bedah Kode**

## 1\. Mengapa menggunakan `<ul>` daripada `<ol>`?

*   `<ul>` = _unordered list_ → daftar tanpa urutan/nomor.
*   `<ol>` = _ordered list_ → daftar dengan urutan/nomor.
*   Pada menu navigasi, **urutan biasanya tidak terlalu penting** (misalnya "Tentang Saya", "Pendidikan", "Kontak"). Tidak ada arti jika salah satunya ditampilkan sebagai nomor 1, 2, 3.  
    👉 Karena itu, lebih tepat menggunakan `<ul>`.

---

## 2\. Mengapa tetap menggunakan elemen list untuk navigasi?

*   **Aksesibilitas**: Screen reader (alat bantu untuk tunanetra) mengenali `<ul>` dan `<li>` sebagai daftar, sehingga pengguna tahu ada sekumpulan tautan navigasi.
*   **Standar HTML semantik**: `<ul>` dengan `<li>` menunjukkan bahwa isi `<nav>` memang berupa kumpulan item navigasi, bukan sekadar teks biasa.
*   **Mudah diatur dengan CSS**: Walaupun default tampilnya vertikal dengan bullet, kita bisa mengubah tampilannya menjadi horizontal, menghilangkan bullet, bahkan membuat gaya menu modern hanya dengan CSS.

---

## 3\. Mengapa tidak menggunakan `<div>` atau elemen generik lain?

*   `<div>` adalah **generic container**, tidak memberikan makna semantik khusus. Browser, mesin pencari, maupun alat bantu tidak akan tahu bahwa itu adalah daftar navigasi.
*   `<ul>` + `<li>` jauh lebih **tepat secara semantik** karena memang mendefinisikan kumpulan item.  
    👉 Dengan kata lain, `<div>` bisa dipakai, tetapi **kurang baik** karena kehilangan makna semantik dan aksesibilitas.

---

### ✨ Kesimpulan

*   Gunakan `**<ul>**` karena navigasi tidak perlu penomoran.
*   Gunakan `**<li>**` agar setiap tautan navigasi jelas sebagai satu item daftar.
*   Gunakan `**<div>**` **hanya jika terpaksa**, tapi sebaiknya hindari agar struktur HTML tetap semantik dan ramah aksesibilitas.

> Catatan:
> 
> Kita belum membahas elemen div. Sebagai informasi awal, ia merupakan generic element yang sebetulnya tidak memilki makna sedikit pun. Namun, ia dapat dimanfaatkan untuk mengelompokkan sejumlah elemen.

## 1\. Mengapa `<ul>` lebih tepat daripada `<ol>`?

*   `<ol>` → digunakan kalau urutan itu penting (misalnya resep masakan, langkah instalasi software).
*   `<ul>` → digunakan kalau urutan tidak penting (misalnya daftar menu navigasi, daftar fasilitas, daftar kontak).  
    Navigasi halaman bukanlah sesuatu yang harus diurutkan, jadi wajar memakai `<ul>`.

---

## 2\. Elemen List untuk Navigasi

*   Elemen **list (**`**<ul>**` **+** `**<li>**`**)** dipakai untuk menampilkan daftar item.
*   Dalam konteks **navigasi**, setiap item daftar biasanya berupa tautan menuju bagian halaman atau halaman lain.
*   Default-nya memang ada **bullet** pada tiap `<li>`. Tapi jangan khawatir, bullet ini bisa dihilangkan atau diganti gayanya dengan **CSS** (misalnya `list-style-type: none;`).  
    👉 Styling ini akan dibahas lebih detail di modul khusus CSS.

---

## 3\. Supaya Navigasi Berfungsi

*   Daftar navigasi bukan hanya teks biasa, tapi perlu bisa diklik.
*   Untuk itu digunakan **elemen** `**<a>**` **(anchor)**:

```
<ul>
  <li><a href="#tentang">Tentang Saya</a></li>
  <li><a href="#pendidikan">Pendidikan</a></li>
  <li><a href="#kontak">Kontak</a></li>
</ul>
```

*   Klik tautan di atas akan membawa pengguna ke bagian tertentu di halaman (jika ada elemen dengan `id` yang sesuai).

---

## 4\. Referensi Lanjutan

*   Kalau ingin memperdalam, dokumentasi **MDN** adalah sumber yang sangat bagus:
*   The Ordered List element (`<ol>`)
*   The Unordered List element (`<ul>`)

---

Jadi, intinya:

*   Gunakan `<ul>` untuk navigasi karena urutannya tidak penting.
*   Tambahkan `<a>` agar menu bisa diklik.
*   Hilangkan bullet dengan CSS nanti di modul styling.

[Kembali](index.md)