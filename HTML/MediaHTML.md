# **Materi Media HTML: \<img>, \<audio>, dan \<video>**

Materi ini membahas atribut-atribut utama pada elemen media HTML dan cara menampilkan gambar, audio, serta video secara benar, aksesibel, dan ramah-performa.

---

# **\<img> - Gambar**

## **Fungsi:** Menyisipkan gambar statis.

### Atribut Utama

*   **src**: URL gambar.
*   **alt**: Teks alternatif (wajib untuk aksesibilitas).
*   **width / height**: Dimensi tampilan (disarankan untuk mencegah layout shift). Nilai tanpa satuan (piksel CSS).
*   **loading**: Strategi pemuatan (lazy/eager).
*   **decoding**: Strategi decoding (async/sync/auto).
*   **srcset**: Daftar sumber gambar beresolusi berbeda.
*   **sizes**: Aturan lebar tampilan untuk memilih kandidat di srcset.
*   **referrerpolicy**: Kebijakan referrer saat mengambil gambar.
*   **crossorigin**: anonymous atau use-credentials untuk CORS.
*   **fetchpriority**: Prioritas pengambilan (high/low/auto).
*   **title**: Tooltip opsional.

*   **Contoh Dasar \<img>**

```html
<img src="images/logo.png" alt="Logo Perusahaan UJIIMFTEAM" width="240" height="80">
```

*   **Contoh Responsif (srcset + sizes)**

```html
<img src="images/hero-800.jpg" srcset="images/hero-400.jpg 400w, images/hero-800.jpg 800w, images/hero-1200.jpg 1200w"

    sizes="(max-width: 600px) 100vw, 600px" alt="Pemandangan pegunungan saat matahari terbit" width="600" height="400"

    loading="lazy" decoding="async">
```

# **\<audio> - Audio**

## **Fungsi:** Memutar berkas audio dengan kontrol pemutar.

### **Atribut Utama**

*   **src**: URL audio (opsional jika pakai \<source>).
*   **controls**: Menampilkan kontrol pemutar (disarankan).
*   **autoplay**: Memulai otomatis (hormati kebijakan browser; sebaiknya bersama muted).
*   **muted**: Memulai dalam keadaan tanpa suara.
*   **loop**: Mengulang setelah selesai.
*   **preload**: none | metadata | auto (pilih hemat data sesuai kebutuhan).
*   **crossorigin**: Untuk CORS saat butuh.

*   **Struktur dengan \<source> (multi-format) & fallback**

```html
<audio controls preload="metadata">

    <source src="media/podcast-ep1.mp3" type="audio/mpeg">

    <source src="media/podcast-ep1.ogg" type="audio/ogg">

    Browser Anda tidak mendukung audio HTML5. Silakan unduh berkasnya.

</audio>
```

---

# \<video> **Video**

## **Fungsi:** Memutar berkas video, mendukung caption melalui \<track>.

### Atribut Utama

*   **src**: URL video (opsional jika pakai \<source>).
*   **controls**: Tampilkan kontrol.
*   **autoplay**: Mulai otomatis. **Catatan:** Di banyak browser hanya berfungsi jika **muted**.
*   **muted**: Mulai tanpa suara (sering dipakai untuk autoplay).
*   **loop**: Mengulang.
*   **poster**: Gambar placeholder sebelum diputar.
*   **preload**: none | metadata | auto.
*   **width / height**: Dimensi tampilan.
*   **playsinline**: Memutar inline di perangkat mobile (iOS/Android) tanpa fullscreen otomatis.
*   **crossorigin**: Untuk CORS.

*   **Teks/Captions dengan \<track>**
*   **kind**: captions, subtitles, descriptions, chapters, metadata.
*   **srclang**: Kode bahasa (mis. id, en).
*   **label**: Nama yang tampil pada pilihan caption.
*   **default**: Menjadikan track tersebut aktif awal.

*   **Contoh Video Lengkap**

```html
<video controls preload="metadata" poster="media/teaser-poster.jpg" width="640" height="360" playsinline>

    <source src="media/teaser-1080.mp4" type="video/mp4">

    <source src="media/teaser-720.webm" type="video/webm">

    <track kind="captions" src="media/teaser-id.vtt" srclang="id" label="Bahasa Indonesia" default>

    <track kind="subtitles" src="media/teaser-en.vtt" srclang="en" label="English">

    Browser Anda tidak mendukung video HTML5.

</video>
```

---

1.  Praktik Terbaik (Best Practices)

*   **Aksesibilitas gambar:** alt harus menjelaskan fungsi gambar. Kosongkan alt="" untuk gambar dekoratif murni.
*   **Captioning:** Sertakan \<track kind="captions"> untuk video agar aksesibel.
*   **Kinerja:**
    *   Gambar: kompres & gunakan format modern (WebP/AVIF) + srcset/sizes.
    *   Video: sediakan beberapa format (MP4/H.264, WebM/VP9/AV1) sesuai dukungan.
    *   Gunakan preload="metadata" agar hemat data; loading="lazy" untuk \<img> di bawah lipatan.
*   **Ukuran tetap:** Tetapkan width/height di HTML untuk mencegah layout shift.
*   **Autoplay bertanggung jawab:** Jika perlu autoplay video, tambahkan muted dan pertimbangkan UX.
*   **CORS & Type:** Pastikan header MIME benar dan atur crossorigin bila mengambil dari domain lain.

---

## **Contoh Halaman Lengkap**

Salin tempel kode ini ke file media-demo.html, lalu buka di browser. Ganti jalur berkas (images/…, media/…) sesuai struktur proyek Anda.

```html
<!doctype html>
<html lang="id">



<head>

    <meta charset="utf-8">

    <meta name="viewport" content="width=device-width, initial-scale=1">

    <title>Demo Media HTML</title>

</head>



<body>

    <h1>Demo Media HTML: <code>&lt;img&gt;</code>, <code>&lt;audio&gt;</code>, <code>&lt;video&gt;</code></h1>



    <h2>Gambar (img)</h2>

    <figure>

        <img src="images/hero-800.jpg"

            srcset="images/hero-400.jpg 400w, images/hero-800.jpg 800w, images/hero-1200.jpg 1200w"

            sizes="(max-width: 600px) 100vw, 600px" alt="Pemandangan pegunungan dengan cahaya keemasan matahari terbit"

            width="600" height="400" loading="lazy" decoding="async">

        <figcaption>Gambar responsif dengan <code>srcset</code> dan <code>sizes</code>.</figcaption>

    </figure>



    <h2>Audio (audio)</h2>

    <audio controls preload="metadata">

        <source src="media/podcast-ep1.mp3" type="audio/mpeg">

        <source src="media/podcast-ep1.ogg" type="audio/ogg">

        Browser Anda tidak mendukung audio HTML5. <a href="media/podcast-ep1.mp3" download>Unduh audio</a>.

    </audio>

    <p>Gunakan beberapa format agar kompatibel lintas-browser.</p>



    <h2>Video (video)</h2>

    <video controls preload="metadata" poster="media/teaser-poster.jpg" width="640" height="360" playsinline>

        <source src="media/teaser-1080.mp4" type="video/mp4">

        <source src="media/teaser-720.webm" type="video/webm">

        <track kind="captions" src="media/teaser-id.vtt" srclang="id" label="Bahasa Indonesia" default>

        <track kind="subtitles" src="media/teaser-en.vtt" srclang="en" label="English">

        Browser Anda tidak mendukung video HTML5. <a href="media/teaser-1080.mp4">Unduh video</a>.

    </video>

    <ul>

        <li>Tambahkan <code>muted</code> jika ingin mengaktifkan <code>autoplay</code> secara konsisten.</li>

        <li>Gunakan <code>poster</code> untuk placeholder yang informatif.</li>

        <li>Sertakan <code>&lt;track&gt;</code> untuk caption/subtitle.</li>

    </ul>



    <p><strong>Tip:</strong> Tetapkan dimensi media di HTML untuk mencegah pergeseran tata letak dan meningkatkan

        stabilitas tampilan.</p>

</body>



</html>
```

---

## **Kesalahan Umum & Solusinya**

*   **Tidak ada alt pada gambar penting** → Tambahkan deskripsi singkat yang bermakna.
*   **autoplay tanpa muted** → Banyak browser akan memblokir; sertakan muted atau hindari autoplay.
*   **Format tunggal untuk audio/video** → Tambah \<source> dengan format alternatif.
*   **Dimensi tidak ditentukan** → Tetapkan width/height di HTML, lalu atur skala dengan CSS jika perlu.
*   **Ukuran berkas besar** → Kompres, batasi resolusi, gunakan CDN bila tersedia.

---

## **Aturan Penulisan Media HTML: \<img>, \<audio>, \<video>**

### Umum

*   Gunakan **tag semantik yang tepat**: \<figure> + \<figcaption> untuk media yang butuh keterangan.
*   **Tentukan dimensi** (width/height) pada gambar & video untuk mencegah layout shift.
*   Letakkan **fallback text/link unduh** di dalam \<audio>/\<video> untuk browser lama.
*   Pastikan **tipe MIME** di server sesuai berkas (mis. image/avif, image/webp, image/jpeg, audio/mpeg, video/mp4, video/webm).
*   Bila mengambil lintas-domain, gunakan **crossorigin** yang sesuai dan aktifkan CORS di server asal bila diperlukan.

### \<img>

*   **Wajib** alt yang mendeskripsikan fungsi/isi gambar. Kosongkan alt="" untuk dekoratif murni.
*   Pakai **srcset + sizes** untuk responsif; sediakan format modern (AVIF/WebP) dan fallback JPEG/PNG bila perlu.
*   Tambahkan **loading="lazy"** untuk gambar di bawah lipatan; **decoding="async"** untuk mempercepat render.
*   **Jaga rasio aspek** dengan menetapkan width/height (nilai px) di HTML.
*   Hindari title sebagai pengganti alt—title opsional/tooltip saja.

**Contoh benar**

```html
<figure>
  <img
    src="/img/produk-800.jpg"
   srcset="/img/produk-400.jpg 400w, /img/produk-800.jpg 800w, /img/produk-1200.jpg 1200w"
    sizes="(max-width: 600px) 100vw, 600px"
    alt="Kamera mirrorless seri X warna hitam"
    width="600" height="400" loading="lazy" decoding="async">
  <figcaption>Kamera seri X dengan lensa 23mm.</figcaption>
</figure>
```

### **\<audio>**

*   **Selalu** gunakan controls untuk aksesibilitas; autoplay bersifat opsional dan sering dibatasi browser.
*   Jika memakai autoplay, tambahkan **muted** bila ingin memastikannya berjalan (kebijakan pemutaran otomatis).
*   Gunakan **preload="metadata"** secara default; hindari auto kecuali perlu.
*   Sediakan **multi-format** via \<source> (mis. MP3 + Ogg) dan fallback teks/link unduh.

**Contoh benar**

```html
<audio controls preload="metadata">
  <source src="/media/intro.mp3" type="audio/mpeg">
  <source src="/media/intro.ogg" type="audio/ogg">
 Peramban tidak mendukung audio. <a href="/media/intro.mp3">Unduh berkas</a>.
</audio>
```

### **\<video>**

*   **Selalu** controls; gunakan playsinline untuk pengalaman mobile.
*   Tentukan **poster** untuk pratinjau yang informatif.
*   Default **preload="metadata"**; gunakan autoplay hanya bila diperlukan dan **sertakan muted**.
*   Sediakan **beberapa format** (MP4/H.264 atau H.265/AV1, dan/atau WebM) via \<source>.
*   Tambahkan **caption/subtitle** dengan \<track kind="captions" ...>; set **srclang** dan **label** yang jelas, bisa default.

**Contoh benar**

```html
<video controls preload="metadata" poster="/media/cover.jpg" width="640" height="360" playsinline>
  <source src="/media/demo-1080.mp4" type="video/mp4">
  <source src="/media/demo-720.webm" type="video/webm">
  <track kind="captions" src="/media/demo-id.vtt" srclang="id" label="Bahasa Indonesia" default>
 Peramban tidak mendukung video. <a href="/media/demo-1080.mp4">Unduh video</a>.
</video>
```

### Jangan Lakukan

*   Jangan meninggalkan **alt** kosong pada gambar yang bermakna.
*   Jangan gunakan **format tunggal** saja untuk audio/video jika butuh dukungan luas.
*   Jangan mengandalkan **title** sebagai pengganti teks alternatif.
*   Jangan aktifkan **autoplay** dengan suara (tanpa muted)—kemungkinan diblokir dan mengganggu.
*   Jangan lupa **fallback** dan **dimensi** agar UX stabil.

---

## **Ringkasan**

*   \<img> untuk gambar statis (prioritaskan alt, srcset, sizes, dan dimensi).
*   \<audio> & \<video> mendukung multi-format via \<source>, kontrol bawaan, dan preload.
*   Tingkatkan aksesibilitas dengan caption \<track> dan teks alternatif.
*   Optimalkan performa dengan lazy load, kompresi, dan format modern.