## **Block Formatting Text: Long Quotations, Preformatted Text, dan Figure**

Sejauh ini, kita sudah mengenal paragraf, heading, dan juga list pada HTML. Tapi masih ada beberapa lagi yang merupakan spesial teks format yang dapat kita gunakan yaitu \<blockquote>, \<pre>, dan \<figure>.

*   **Tambahkan Folder BlockFormatting**

### **Long Quotations**

Gunakan tag `<blockquote>` untuk menampilkan kutipan atau testimonial; isinya bisa paragraf, heading, atau daftar.

*   **Buat File LongQuotations.html**

```html
<blockquote>
  <p>
    Situs web (bahasa Inggris: website) adalah sekumpulan halaman web yang saling berhubungan yang
    umumnya berada pada peladen yang sama berisikan kumpulan informasi yang disediakan secara
    perorangan, kelompok, atau organisasi.
  </p>
</blockquote>
```

Gunakan atribut `cite` pada `<blockquote>` untuk menautkan sumber URL kutipan; ini bersifat metadata dan tidak mengubah tampilan di browser.

```html
<blockquote cite="https://id.wikipedia.org/wiki/Situs_web">
  <p>
    Situs web (bahasa Inggris: website) adalah sekumpulan halaman web yang saling berhubungan yang
    umumnya berada pada peladen yang sama berisikan kumpulan informasi yang disediakan secara
    perorangan, kelompok, atau organisasi.
  </p>
</blockquote>
```

### **Preformatted Text**

HTML biasanya mengabaikan spasi ganda dan baris baru. Untuk konten yang butuh format persis seperti di editor (mis. kode atau puisi), bungkus dengan `<pre>` agar spasi dan line break dipertahankan.

*   **Buat File PreformattedText.html**

```html
<pre>
  SAJAK PUTIH

Bersandar pada tari warna pelangi
Kau depanku bertudung sutra senja
Di hitam matamu kembang mawar dan melati
Harum rambutmu mengalun bergelut senda

Sepi menyanyi, malam dalam mendoa tiba
Meriak muka air kolam jiwa
Dan dalam dadaku memerdu lagu
Menarik menari seluruh aku

Hidup dari hidupku, pintu terbuka
Selama matamu bagiku menengadah
Selama kau darah mengalir dari luka
Antara kita Mati datang tidak membelah...

                  Karya: Chairil Anwar
</pre>
```

### **Figure**

Gunakan `<figure>` untuk konten berdiri sendiri (ilustrasi, foto, diagram, cuplikan kode) yang bisa dipindah tanpa mengubah makna dokumen. Tambahkan `<figcaption>` sebagai judul/penjelasan konten.

*   **Buat File Figure.html**

```html
<p>
  Dicoding adalah sebuah perusahaan startup yang bertujuan mengembangkan ekosistem developer di
  Indonesia. Berdiri sejak 5 Januari 2015, Dicoding memiliki platform pembelajaran elektronik di
  laman Dicoding.com.
</p>

<figure>
  <img
    src="https://raw.githubusercontent.com/dicodingacademy/a123-webdasar-labs/099-shared-files/shared-media/g-dicoding-logo.png"
    alt="g Dicoding Logo"
    width="200px"
  />
  <figcaption>Dicoding</figcaption>
</figure>

<p>
  Materi perdana yang menjadi magnet dari awal berdirinya Dicoding hingga kini adalah kelas Menjadi
  Android Developer Expert. Kelas ini dikembangkan oleh Google Developer Expert in Android, Sidiq
  Permana dan Head of Dicoding Academy, Ahmad Imaduddin. Seperti halnya kelas Picodiploma lain,
  modul online-nya juga hadir dalam bentuk buku berjudul sama yang telah mendapatkan ijin dan ISBN.
</p>
```

Contoh lainnya, elemen figure dapat kita gunakan untuk me-_markup_ sebuah konten puisi.

*   **Buat File Figure1.html**

```html
<figure>
  <pre>
          SAJAK PUTIH

      Bersandar pada tari warna pelangi
      Kau depanku bertudung sutra senja
      Di hitam matamu kembang mawar dan melati
      Harum rambutmu mengalun bergelut senda

      Sepi menyanyi, malam dalam mendoa tiba
      Meriak muka air kolam jiwa
      Dan dalam dadaku memerdu lagu
      Menarik menari seluruh aku

      Hidup dari hidupku, pintu terbuka
      Selama matamu bagiku menengadah
      Selama kau darah mengalir dari luka
      Antara kita Mati datang tidak membelah...
  </pre>
  <figcaption>Sajak Putih oleh Charil Anwar</figcaption>
</figure>
```

[Kembali](index.md)