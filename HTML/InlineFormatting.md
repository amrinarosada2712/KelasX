## **Inline Formatting Text: Anchor, Emphasized Text, Important Text, dan Short Quotation**

Kita sudah belajar mengidentifikasi penggunaan elemen pada konten yang mayor (besar) dengan menerapkan _semantic HTML_ untuk mengorganisasi kontennya. Sekarang, kita akan mengenal beberapa _formatting text_ yang digunakan dalam sebuah baris teks (inline teks). 

Sebelum menjelaskan elemen _inline_ untuk _formatting text_ yang dapat digunakan, sepertinya kita perlu membahas sekilas mengenai block dan inline.

Pada standarnya, elemen HTML memiliki dua sifat, yaitu **block** dan **inline**. Elemen yang bersifat block selalu membuat baris baru ketika di-render. Contohnya seperti elemen paragraf, list, heading, dan lainnya. Lawan dari elemen tersebut, yaitu elemen inline. Elemen ini tidak menambahkan baris baru ketika di-render. Apa saja elemen tersebut? Mari kita bahas satu persatu.

*   **Tambahkan Folder InlineFormatting**

## **Anchor**

Apa itu _anchor_? Anchor (jangkar) merupakan elemen yang digunakan untuk membuat sebuah hyperlink ke halaman atau website lain, file, alamat email, atau URL lainnya. Untuk menggunakan elemen ini kita gunakan \<a> sebagai tag pembuka dan \</a> sebagai tag penutup. Selain itu, ada atribut wajib agar elemen ini berfungsi dengan baik, yaitu href untuk menetapkan sebuah target yang dituju. 

*   **Tambahkan File Anchor.php pada Folder InlineFormatting**

```html
<p>Hubungi kami di</p>
<ul>
  <li><a href="https://example.com">Website</a></li>
  <li><a href="mailto:info@example.com">Email</a></li>
  <li><a href="tel:+62123456">Telepon</a></li>
  <li><a href="#address">Alamat</a></li>
</ul>
```

Berikut adalah daftar atribut khusus yang dapat digunakan pada elemen ini.

<table><tbody><tr><td><strong>Atribut</strong></td><td><strong>Nilai</strong></td><td><strong>Deskripsi</strong></td></tr><tr><td>download</td><td>filename</td><td>Menginstruksikan browser untuk mengunduh pada URL yang ditetapkan daripada mengarahkannya.</td></tr><tr><td>href</td><td>URL</td><td>Menetapkan target yang akan diarahkan/unduh ketika pengguna menekan hyperlink.</td></tr><tr><td>hreflang</td><td>language_code</td><td>Menetapkan bahasa dari dokumen target.</td></tr><tr><td>ping</td><td>list_of_URLs</td><td>Menetapkan URL yang akan diberitahu dengan mengirimkan post request ping pada body oleh browser (berjalan di belakang layar) ketika target URL pada hyperlink ditekan. Biasanya atribut ini digunakan untuk pelacakan.</td></tr><tr><td>referrerpolicy</td><td><p>no-referrer,</p><p>no-referrer-when-downgrade,</p><p>origin,</p><p>origin-when-cross-origin,</p><p>unsafe-url</p></td><td>Menetapkan referensi untuk dikirim pada target.</td></tr><tr><td>rel</td><td><p>alternate,</p><p>author,</p><p>bookmark,</p><p>external,</p><p>help,</p><p>license,</p><p>next,</p><p>nofollow,</p><p>noreferrer,</p><p>noopener,</p><p>prev,</p><p>search,</p><p>tag</p><p><br>&nbsp;</p></td><td>Menetapkan hubungan antara halaman yang ditampilkan dengan target.</td></tr><tr><td>target</td><td><p>_blank,</p><p>_parent,</p><p>_self,</p><p>_top</p></td><td>Menetapkan lokasi ketika membuka target contohnya pada sebuah tab, window, atau tab itu sendiri.</td></tr><tr><td>media</td><td>media_type</td><td>Menetapkan tipe media yang digunakan pada target.</td></tr></tbody></table>

## **Emphasized Text**

Gunakan elemen \<em> untuk menunjukkan bagian kata yang perlu kita tekankan. Elemen ini menunjukkan _stress emphasis_ atau konten/kata yang perlu mendapatkan penekanan atau perhatian khusus. Berikut contoh penggunaannya.

*   **Tambahkan File em.php pada Folder InlineFormatting**

```html
<p><em>Oding</em> adalah seorang pelajar</p>
<p>Dia adalah seorang <em>pelajar</em></p>
```

Pada kalimat pertama, penekanan terdapat pada “siapa” seorang pelajar. Pada kalimat kedua, penekanan terdapat pada “apa” yang sedang ditekuni oleh Oding.

Standarnya, pada browser sebuah kata yang ditekankan akan ditampilkan dalam gaya _miring_ pada teksnya

*   **Important Text**

Gunakan elemen \<strong> untuk menunjukkan sebuah teks yang begitu penting (strong importance), serius ataupun mendesak. Artinya, teks tersebut harus dapat perhatian lebih dari teks biasa lainnya.

*   **Tambahkan File ImportantText.php pada Folder InlineFormatting**

```html
<p>Kesehatan merupakan hal yang penting, jaga pola makan yang teratur dan <strong>jangan sampai makan tengah malam!</strong></p>
```

Standarnya, pada browser sebuah teks yang diberi _markup_ \<strong> akan ditampilkan tebal. Lalu, ketika pengguna menggunakan pembaca layar (_screen reader_), suara yang terdengar akan berbeda. Ini mengartikan bahwa teks tersebut penting, tidak hanya sekadar tebal.

## **Short Quotations**

Gunakan elemen \<q> untuk menandai sebuah kutipan dalam sebuah teks. Elemen ini berbeda dengan \<blockquote>. Elemen ini digunakan untuk kutipan pendek yang terletak di dalam baris (_inline_).

*   **Tambahkan File ShortQuotations.php pada Folder InlineFormatting**

```html
<p>Sebelum pulang kerja, ia berkata kepadaku: <q>Maaf saya tidak bisa hadir dalam pertemuan nanti</q></p>
```

Standarnya, sebuah teks yang diberi markup \<q> akan ditampilkan di dalam tanda kutip (_quotation marks_) pada browser.

Elemen quotation marks memiliki atribut cite untuk menentukan sumber URL dari sebuah kutipan (jika kutipan tersebut bersumber dari sebuah situs website). Namun, tidak ada perbedaan yang terlihat secara kasat mata jika dijalankan di browser.

*   **Tambahkan File ShortQuotations1.html pada Folder InlineFormatting**

```html
<p>Dilansir dari website Mozilla, <q cite="https://www.mozilla.org/en-US/about/history/details/">Firefox 1.0 diluncurkan
   pada 2004 dan menjadi produk yang sukses.</q>
</p>
```

# **Inline Formatting Text: Citation, Defining Terms, Subscript, Superscript, Highlighted Text, dan Line Break**

Kita sudah belajar banyak formatting text. Namun, ada beberapa sisanya yang belum kita bahas. Tentunya, mereka tidak kalah penting dalam membangun konten halaman web yang lebih baik. Mari kita lengkapi pembahasan ini. _Jom!_

## **Citation**

Selain sebuah atribut, \<cite> juga merupakan sebuah elemen yang digunakan untuk sebuah rujukan pada sebuah dokumen, contohnya sebuah buku, majalah, artikel, dan lainnya.

**Buat File Citation.html pada Folder InlineFormatting**

```
<p>Informasi selengkapnya bisa Anda dapatkan di <cite><a href="https://dicoding.com">dicoding.com</a></cite>.</p>
```

Standarnya, pada browser sebuah teks yang diberi markup \<cite> akan ditampilkan dengan huruf miring (_italic_).

## **Defining Terms**

Elemen \<dfn> digunakan ketika mendefinisikan sebuah istilah (_term_). Elemen ini harus terletak pada elemen lain yang menaunginya. Contohnya pada sebuah elemen \<p> atau elemen \<section>. Berikut contoh penggunaannya.

**Buat File DefiningTerms.html pada Folder InlineFormatting**

```
<p><dfn>Website</dfn> merupakan halaman yang menampilkan informasi melalui teks atau gambar. Website dapat diakses melalui internet dengan menggunakan browser.</p>
```

Standar pada browser yakni sebuah teks yang diberi markup \<dfn> akan ditampilkan dengan huruf miring (_italic_).

## **Subscript dan Superscript**

Subscript \<sub> dan superscript \<sup> adalah elemen yang dapat membuat teks yang ditampilkan tampak kecil, dengan posisi di bawah (sub) atau di atas (sup) dari teks biasanya. Elemen ini digunakan untuk menunjukkan sebuah rumus kimia ataupun matematika.

**Buat File SubSup.html pada Folder InlineFormatting**

```
<p>
  Sukrosa merupakan suatu disakarida yang dibentuk dari monomer-monomernya yang berupa unit glukosa dan fruktosa, dengan rumus molekul C<sub>12</sub>H<sub>22</sub>O<sub>11</sub>.
</p>

<p>Salah satu persamaan paling umum dalam semua fisika adalah E=MC<sup>2</sup></p>
```

## **Highlighted Text**

Untuk menandai atau menyorot sebuah teks kita bisa menggunakan elemen \<mark>. Elemen ini digunakan ketika terdapat sebuah teks yang memiliki peran penting, biasanya teks tersebut merupakan bagian yang paling relevan atau penting dalam sebuah konteks kalimat.

**Buat File HighlightedText.html pada Folder InlineFormatting**

```
<p>
  Ini adalah periode perang saudara. Pesawat ruang angkasa pemberontak, menyerang dari pangkalan
  tersembunyi, telah memenangkan kemenangan pertama mereka melawan Kekaisaran Galactic yang jahat.
  Selama pertempuran,
  <mark>mata-mata Pemberontak berhasil mencuri rencana rahasia </mark>
  ke senjata pamungkas Kekaisaran, STAR DEATH, stasiun ruang angkasa berlapis baja dengan kekuatan
  yang cukup untuk menghancurkan seluruh planet.
</p>
```

Standarnya, pada browser teks yang diberi markup \<mark> akan ditampilkan dengan background kuning dan teks hitam.

## **Line Break**

Terkadang, kita mungkin perlu menambahkan sebuah baris baru pada sebuah baris teks (termasuk dalam paragraf), tetapi kita mengetahui bahwa browser akan mengabaikan sebuah penulisan spasi ganda ataupun garis baru. Jadi, kita memerlukan sebuah tanda yang dapat digunakan untuk memberitahu browser untuk “Tambahkan baris baru di sini!”.

_Inline line break element_ (\<br>) dapat digunakan untuk memberitahu browser untuk memberikan sebuah garis baru pada baris teks. Sama seperti gambar, elemen ini merupakan elemen kosong sehingga kita tidak membutuhkan sebuah tag penutup.

**Buat File LineBreak.html pada Folder InlineFormatting**

```
<p>
   Dicoding Space,<br>
   Jln. Batik Kumeli No. 50.<br>
   Bandung.<br>
   40123
</p>
```

[Kembali](index.md)