# **Latihan: Menambahkan List pada Halaman Profil**

### **Tujuan**

Pada latihan ini, kita akan mengembangkan lagi studi kasus Halaman Profil yang telah kita lakukan pada modul sebelumnya. Kali ini, kita akan menambahkan navigation list untuk menampilkan daftar konten yang tersedia dalam halaman tersebut. Kita akan memanfaatkan elemen list, lebih tepatnya adalah elemen ul.

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

Kerja bagus! Kamu berhasil menerapkan elemen list pada Halaman Profil. Elemen ini akan berfungsi sebagai navigation list yang menampilkan daftar konten dalam Halaman Profil. Mari kita pelajari hal yang telah kita lakukan pada latihan ini.

Sebagaimana dipelajari sebelumnya, elemen list digunakan untuk membuat daftar item. Namun, kita memanfaatkannya untuk membuat navigation list atau daftar navigasi. Jika boleh menerka-nerka, kami yakin bahwa Anda akan bertanya-tanya seperti berikut.

*   Mengapa menggunakan \<ul> daripada \<ol>?
*   Mengapa menggunakan elemen list untuk membuatnya? Padahal daftar navigasi umumnya ditampilkan secara horizontal dan tanpa penomoran.
*   Jika ditampilkan secara horizontal dan tanpa penomoran, bukankah bisa menggunakan elemen lain selain elemen list? Misalnya generic elemen seperti div.

> Catatan:
> 
> Kita belum membahas elemen div. Sebagai informasi awal, ia merupakan generic element yang sebetulnya tidak memilki makna sedikit pun. Namun, ia dapat dimanfaatkan untuk mengelompokkan sejumlah elemen.

Pada dasarnya, kita dibebaskan untuk menggunakan elemen apa pun untuk mencapai konten dan tampilan yang diinginkan. Alasan yang paling logis adalah elemen \<ol> umumnya untuk menampilkan item-item yang mementingkan urutan. Contohnya, membuat langkah-langkah memasak mie instan, membuat minuman kopi, dsb. Namun, ketika membaca sebuah artikel _feature_ yang informasinya tidak bergantung pada urutan (tidak seperti resep, novel, dsb.), tentu pembaca bebas memulai dari mana pun yang diinginkan, bukan? Oleh sebab itulah, kita menggunakan elemen \<ul>.

Elemen list merupakan salah satu elemen yang dapat dimanfaatkan menampilkan daftar navigasi halaman. Namun, tentu saja ada karakter _bullet_ pada setiap item dan ini tidak kita butuhkan. Bagaimana cara untuk mengubah tampilannya? Tentunya, kita akan mempelajari ini pada modul styling (modul terpisah).

Saat ini, kita baru bisa membuat daftar navigasi hanya dengan elemen list, tetapi belum dapat berfungsi sebagaimana mestinya.

Untuk melakukannya, kita memerlukan elemen anchor (\<a>). Apakah Anda bertanya-tanya untuk cara lain? Jawabannya, ada! Namun, kita memerlukan JavaScript dan ini tidak dicakup pada kelas ini. Anda akan belajar JavaScript pada kelas lanjutan.

Untuk menambahkan pengetahuan tentang elemen list, seperti biasa, kami mengarahkan Anda pada MDN sebagai dokumentasi terlengkap. Silakan kunjungi dan simak [The Ordered List element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol) dan [The Unordered List element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul).

[Kembali](index.md)