# Modul Lengkap: Elemen Semantik HTML5

HTML5 memperkenalkan berbagai elemen semantik baru yang membantu membuat struktur halaman web menjadi lebih bermakna dan terorganisasi.

## 1\. Pengertian Elemen Semantik

Elemen semantik menjelaskan isi dari elemen tersebut. Misalnya, 

*   tag\<header> digunakan untuk bagian kepala halaman,
*   \<main> untuk konten utama, 
*   \<footer> untuk bagian bawah halaman.  
     

## 2\. Manfaat Elemen Semantik

*   Struktur halaman lebih teratur dan bermakna.
*   Memudahkan pembaca layar dalam membaca halaman.
*   Mempermudah pemeliharaan dan pengembangan kode.

## 3\. Daftar Elemen Semantik Utama HTML5

---

Elemen Fungsi

---

*   \<header> Bagian kepala halaman atau bagian yang berisi judul dan navigasi.
*   \<nav> Berisi tautan navigasi utama atau sekunder.
*   \<main> Konten utama dari halaman, hanya boleh satu kali per halaman.
*   \<section> Bagian bertema dari halaman, biasanya memiliki heading.
*   \<article> Konten mandiri seperti artikel, post, atau berita.
*   \<aside> Konten tambahan seperti sidebar atau catatan samping.
*   \<footer> Bagian bawah halaman, biasanya berisi informasi penulis atau hak cipta.
*   \<figure> Menampung konten media seperti gambar atau diagram.
*   \<figcaption> Memberikan keterangan untuk elemen \<figure>.
*   \<time> Menandai waktu atau tanggal dengan format yang dapat dibaca mesin.
*   \<address> Berisi informasi kontak penulis atau pemilik konten.
*   \<mark> Menyoroti teks penting dalam konteks tertentu.

---

## 4\. Contoh Struktur Halaman Semantik

![](https://www.w3schools.com/html/img_sem_elements.gif)

```html
<!doctype html>
<html lang="id">

<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Struktur Semantik HTML5</title>
</head>

<body>


    <header>
        <h1>Nama Situs</h1>
        <p>Deskripsi singkat situs.</p>
    </header>

    <nav aria-label="Menu utama">
        <ul>
            <li><a href="#">Beranda</a></li>
            <li><a href="#">Artikel</a></li>
            <li><a href="#">Tentang</a></li>
            <li><a href="#">Kontak</a></li>
        </ul>
    </nav>


    <main id="konten-utama">
        <section aria-labelledby="judul-section">
            <h2 id="judul-section">Section</h2>
            <p>Konten bertema (ringkasan/fitur/daftar).</p>
        </section>

        <article>
            <header>
                <h2>Judul Artikel</h2>
                <p>Oleh Penulis • <time datetime="2025-10-22">22 Oktober 2025</time></p>
            </header>
            <p>Konten artikel mandiri.</p>
            <footer>
                <address>Kontak penulis: <a href="mailto:penulis@example.com">email</a></address>
            </footer>
        </article>

        <aside aria-label="Sampingan">
            <h2>Aside</h2>
            <ul>
                <li><a href="#">Tautan terkait 1</a></li>
                <li><a href="#">Tautan terkait 2</a></li>
            </ul>
        </aside>
    </main>

    <footer>
        <p>&copy; 2025 Nama Situs</p>
    </footer>
</body>

</html>
```

## 5\. Latihan Kasus

Latihan 1: Ubah struktur non-semantik berikut menjadi struktur semantik  
yang benar.

**Kode Awal (Non-Semantik)**

```html
<div class="atas">
  <h1>Profil Pribadi</h1>

</div>

<ul class="menu">
    <li><a href="#tentang">Tentang Saya</a></li>
    <li><a href="#proyek">Proyek</a></li>
    <li><a href="#kontak">Kontak</a></li>
  </ul>

<div class="utama">
  <div class="bio">
    <h2>Tentang Saya</h2>
    <p>Saya seorang desainer web yang fokus pada antarmuka pengguna (UI/UX).</p>
  </div>

  <div class="projek">
    <h2>Proyek Terbaru</h2>
    <p>Website portofolio interaktif dengan animasi CSS.</p>
  </div>

  <div class="samping">
    <h3>Keahlian</h3>
    <ul>
      <li>HTML5</li>
      <li>CSS3</li>
      <li>Figma</li>
    </ul>
  </div>
</div>

<div class="bawah">
  <p>© 2025 Profil Pribadi</p>
</div>
```

1.  Ubah **judul situs**  `<div class="utama">` menjadi `<header>`.
2.  Ubah **judul situs** **menu navigasi** `<div class="menu">` dan `<nav>`.
3.  Ubah `<div class="utama">` menjadi `<main>`.
4.  Jadikan `<div class="bio">` sebagai `<section>` yang berisi profil diri.
5.  Jadikan `<div class="projek">` sebagai `<article>` untuk proyek yang bisa berdiri sendiri.
6.  Jadikan `<div class="samping">` sebagai `<aside>` untuk keahlian.
7.  Ganti `<div class="bawah">` dengan `<footer>`.
8.  Tambahkan atribut `aria-label` pada `<nav>` dan gunakan `<time>` untuk tanggal jika relevan.

**Latihan 2:** Buat halaman artikel dengan struktur lengkap seperti contoh di atas, tetapi dengan tema dan konten buatan sendiri.

## 6\. Tips Validasi & Optimasi

*   Gunakan validator W3C: https://validator.w3.org
*   Pastikan heading berurutan (h1 → h2 → h3).
*   Hanya gunakan satu \<main> per halaman.
*   Gunakan alt pada semua gambar penting.
*   Berikan aria-label untuk navigasi ganda.