# **Latihan: Identifikasi Elemen pada Halaman Profil**

Setelah mengetahui struktur dasar HTML, mari kita terapkan ilmu ini pada halaman web yang sudah kita buat dalam latihan awal. Yuk, berlatih!

### **Tujuan**

## Mengapa Perlu Elemen?

*   **Heading (**`**<h1>–<h6>**`**)** → untuk judul dan subjudul.
*   **Paragraf (**`**<p>**`**)** → untuk isi teks atau penjelasan.
*   **Daftar (**`**<ul>**`**,** `**<ol>**`**,** `**<li>**`**)** → untuk informasi berbentuk list.
*   **Tautan (**`**<a>**`**)** → untuk membuat teks bisa diklik.
*   **Alur Latihan**

Berikut adalah alur latihan kali ini.

1.  Menuliskan struktur dasar dokumen HTML pada berkas index.html.
2.  Menempatkan seluruh konten pada elemen body.
3.  Membungkus setiap bagian dari artikel dengan elemen yang tepat.
4.  Menjalankan dokumen HTML pada browser.

### **Latihan Identifikasi Elemen pada Halaman Website**

### 1\. Buat Folder dan File

Buat folder bernama **KotaBanjarmasin**.

Di dalamnya, buat file bernama **index.html**.

---

### 2\. Tambahkan Struktur Dasar HTML

Pada `index.html`, masukkan struktur dasar berikut (kode tebal menandakan bagian yang penting ditambahkan):

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Kota Banjarmasin</title>
</head>
<body>

  <!-- Konten artikel akan ditulis di sini -->

</body>
</html>
```

### 3\. Identifikasi Konten Artikel

**Judul utama/topik** → gunakan `<h1>`.

**Penjelasan utama/topik** → gunakan `<p>`.

**Subjudul/topik turunan** → gunakan `<h2>` atau `<h3>`.

**Paragraf pendukung** → gunakan `<p>` di bawah heading terkait.

### 4\. Masukkan artikel ke dalam body

Misalnya artikel tentang Banjarmasin berisi: judul, deskripsi kota, dan keunikan sungai. Maka kodenya bisa seperti ini:  

# Bandung

Kota metropolitan terbesar di Provinsi Jawa Barat, sekaligus menjadi ibu kota provinsi tersebut.

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>Halaman Profil Bandung</title>
  </head>

  <body>
    <h1>Bandung</h1>
    <p>
      Kota metropolitan terbesar di Provinsi Jawa Barat, sekaligus menjadi ibu kota provinsi
      tersebut.
    </p>

    <ul>
      <li>Sejarah</li>
      <li>Geografis</li>
      <li>Wisata</li>
    </ul>

    <h2>Sejarah</h2>
    <p>
      Kata Bandung berasal dari kata bendung atau bendungan karena terbendungnya sungai Citarum oleh
      lava Gunung Tangkuban Parahu yang lalu membentuk telaga. Legenda yang diceritakan oleh
      orang-orang tua di Bandung mengatakan bahwa nama Bandung diambil dari sebuah kendaraan air
      yang terdiri dari dua perahu yang diikat berdampingan yang disebut perahu bandung yang
      digunakan oleh Bupati Bandung, R.A. Wiranatakusumah II, untuk melayari Ci Tarum dalam mencari
      tempat kedudukan kabupaten yang baru untuk menggantikan ibu kota yang lama di Dayeuhkolot.
    </p>

    <p>
      Berdasarkan filosofi Sunda, kata Bandung juga berasal dari kalimat Nga-Bandung-an Banda
      Indung, yang merupakan kalimat sakral dan luhur karena mengandung nilai ajaran Sunda.
      Nga-Bandung-an artinya menyaksikan atau bersaksi. Banda adalah segala sesuatu yang berada di
      alam hidup yaitu di bumi dan atmosfer, baik makhluk hidup maupun benda mati. Sinonim dari
      banda adalah harta. Indung berarti Ibu atau Bumi, disebut juga sebagai Ibu Pertiwi tempat
      Banda berada.
    </p>

    <h2>Geografis</h2>
    <p>
      Kota Bandung dikelilingi oleh pegunungan, sehingga bentuk morfologi wilayahnya bagaikan sebuah
      mangkok raksasa, secara geografis kota ini terletak di tengah-tengah provinsi Jawa Barat,
      serta berada pada ketinggian ±768 m di atas permukaan laut, dengan titik tertinggi di berada
      di sebelah utara dengan ketinggian 1.050 meter di atas permukaan laut dan sebelah selatan
      merupakan kawasan rendah dengan ketinggian 675 meter di atas permukaan laut.
    </p>

    <p>
      Kota Bandung dialiri dua sungai utama, yaitu Sungai Cikapundung dan Sungai Citarum beserta
      anak-anak sungainya yang pada umumnya mengalir ke arah selatan dan bertemu di Sungai Citarum.
      Dengan kondisi yang demikian, Bandung selatan sangat rentan terhadap masalah banjir terutama
      pada musim hujan.
    </p>

    <h2>Wisata</h2>
    <p>
      Sejak dibukanya Jalan Tol Cipularang, kota Bandung telah menjadi tujuan utama dalam menikmati
      liburan akhir pekan terutama dari masyarakat yang berasal dari Jakarta sekitarnya. Selain
      menjadi kota wisata belanja, kota Bandung juga dikenal dengan sejumlah besar bangunan lama
      berarsitektur peninggalan Belanda.
    </p>

    <h3>Farm House Lembang</h3>
    <p>
      Berada di jalur utama Bandung-Lembang, Farm House menjadi objek wisata yang tidak pernah sepi
      pengunjung. Selain karena letaknya strategis, kawasan ini juga menghadirkan nuansa wisata khas
      Eropa. Semua itu diterapkan dalam bentuk spot swafoto Instagramable.
    </p>

    <h3>Observatorium Bosscha</h3>
    <p>
      Memiliki beberapa teleskop, antara lain, Refraktor Ganda Zeiss, Schmidt Bimasakti, Refraktor
      Bamberg, Cassegrain GOTO, dan Teleskop Surya. Refraktor Ganda Zeiss adalah jenis teleskop
      terbesar untuk meneropong bintang. Benda ini diletakkan pada atap kubah sehingga saat teropong
      digunakan, atap tersebut harus dibuka. Observatorium Bosscha boleh dikunjungi oleh siapapun,
      tanpa tiket. Namun, bagi yang ingin menggunakan teleskop Zeiss, wajib mendaftarkan diri. Untuk
      instansi atau lembaga pendidikan, diberikan jadwal hari Selasa sampai Jumat. Sementara itu,
      kunjungan individu dibuka setiap hari Sabtu.
    </p>
  </body>
</html>
```

[Kembali](index.md)