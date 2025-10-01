# **Modul Praktik: FORM HTML – Belajar Mandiri Berbasis Proyek**

> Target pembaca: Siswa pemula–menengah yang ingin menguasai pembuatan **form HTML** dari nol sampai siap membuat proyek sederhana.

## **Cara Pakai Modul**

1.  Ikuti **persesi** berurutan. Tiap sesi berisi: _Tujuan, Ringkasan Teori, Langkah Praktik, Eksperimen/Analisis, Tugas, dan Kriteria Penilaian_.
2.  Simpan semua karya dalam satu folder, misal `form-project/`, agar rapi.
3.  Kerjakan **Tugas** di akhir setiap sesi. Kumpulkan file sesuai nama yang diminta.
4.  Gunakan browser modern (Chrome/Firefox/Edge) dan editor teks (VS Code/Notepad++).

---

## **Prasyarat Minimal**

*   Mengerti struktur HTML dasar (`<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`)
*   Dapat membuat file `.html` dan membuka di browser

---

## **Peta Kompetensi**

*   Menyusun form dengan elemen-elemen HTML standar
*   Menggunakan atribut form penting (`action`, `method`, `enctype`)
*   Memanfaatkan **validasi HTML5** 
*   Menerapkan aksesibilitas dasar: `label`, `fieldset`, `legend`, `aria-describedby`
*   Menggunakan kontrol HTML khusus: `datalist`, `input type="file"`, `hidden`, dll.
*   Menyusun **proyek akhir** form murni HTML

---

# Form HTML

# **Sesi 1 — Dasar Form HTML**

**Tujuan:** Memahami struktur form, elemen input dasar, dan hubungan label–input.

### **Ringkasan Teori**

*   Form dibuat dengan `<form>…</form>`.
*   Input umum: `<input>`, `<textarea>`, `<select>`.
*   `label` terhubung ke input via `for` (sama dengan `id` pada input); meningkatkan aksesibilitas & area klik.

### **Langkah Praktik**

Buat `sesi1-dasar.html`:  

```html
<!DOCTYPE html>
<html lang="id">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Sesi 1 – Dasar Form</title>
    </head>
    <body>
        <h1>Form Kontak Sederhana</h1>
        <form>
        <div>
        <label for="nama">Nama</label>
        <input id="nama" name="nama" type="text" placeholder="Tulis nama lengkap" />
        </div>
        <div>
        <label for="email">Email</label>
        <input id="email" name="email" type="email" placeholder="nama@contoh.com" />
        </div>
        <button type="submit">Kirim</button>
        </form>
    </body>
</html>
```

Buka di browser, coba isi & tekan **Kirim**.

### **Eksperimen/Analisis**

*   Klik teks **Nama** atau **Email**. Apakah fokus pindah? Mengapa `label` penting?
*   Ubah `method` menjadi `post`. Apa perubahan saat submit?

### **Tugas**

1.  Tambahkan input **telepon** (`type="tel"`) dan **textarea** pesan.
2.  Pastikan setiap input punya `id` unik dan `label` yang sesuai. **Kumpulkan:** `sesi1-dasar.html`

### **Kriteria Penilaian**

*   Struktur HTML rapi, semua input memiliki `label`
*   Placeholder jelas; form dapat disubmit

# **Sesi 2 — Jenis Input Umum**

**Tujuan:** Mengenal berbagai `type` pada `<input>` dan atribut dasar.

## **Ringkasan Teori**

*   `type` umum: `text`, `email`, `password`, `number`, `date`, `url`, `tel`.
*   Atribut: `required`, `min`, `max`, `step`, `maxlength`, `placeholder`, `value`.

## **Langkah Praktik**

Buat `sesi2-input-umum.html`:

```html
<!DOCTYPE html>
<html lang="id">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Sesi 2 – Input Umum</title>
    </head>
    <body>
        <h1>Form Akun</h1>
        <form action="" method="post">
            <label for="user">Username</label>
            <input id="user" name="user" type="text" required maxlength="15">


            <label for="pass">Password</label>
            <input id="pass" name="pass" type="password" minlength="6" required>


            <label for="umur">Umur</label>
            <input id="umur" name="umur" type="number" min="1" max="120">


            <label for="tgl">Tanggal Lahir</label>
            <input id="tgl" name="tgl" type="date">


            <label for="web">Website</label>
            <input id="web" name="web" type="url" placeholder="https://">


            <button type="submit">Daftar</button>
        </form>
    </body>
</html>
```

## **Eksperimen/Analisis**

*   Coba isi password \< 6 karakter; apa pesan bawaan browser?
*   Coba `umur` di luar 1–120; apa yang terjadi?

## **Tugas**

1.  Tambahkan input `email` yang **wajib** diisi.
2.  Batasi `username` dengan `maxlength="15"` (sudah dicontohkan) dan tambahkan placeholder yang informatif. **Kumpulkan:** `sesi2-input-umum.html`

## **Kriteria Penilaian**

*   Penggunaan `required`, `min/max`, `minlength/maxlength` tepat
*   Validasi bawaan browser muncul ketika tidak sesuai

# **Sesi 3 — Radio, Checkbox, Select, Textarea**

**Tujuan:** Mengumpulkan pilihan tunggal/jamak serta teks panjang.

### **Ringkasan Teori**

*   **Radio**: satu pilihan dalam satu grup (`name` sama).
*   **Checkbox**: pilihan jamak (nilai yang dicentang saja yang terkirim).
*   **Select**: dropdown dengan `option` dan opsional `optgroup`.
*   **Textarea**: teks multi-baris, atribut utama: `rows`, `cols`, `maxlength`.

### **Langkah Praktik**

Buat `sesi3-pilihan.html`:

```html
<!DOCTYPE html>
<html lang="id">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Sesi 3 – Pilihan</title>
    </head>
    <body>
        <h1>Form Preferensi</h1>
        <form action="" method="post">
        <fieldset>
        <legend>Jenis Kelamin</legend>
        <label><input type="radio" name="gender" value="L"> Laki-laki</label>
        <label><input type="radio" name="gender" value="P"> Perempuan</label>
        </fieldset>


        <fieldset>
        <legend>Hobi</legend>
        <label><input type="checkbox" name="hobi" value="membaca"> Membaca</label>
        <label><input type="checkbox" name="hobi" value="olahraga"> Olahraga</label>
        <label><input type="checkbox" name="hobi" value="musik"> Musik</label>
        </fieldset>


        <label for="kota">Kota</label>
        <select id="kota" name="kota">
        <option value="">-- pilih kota --</option>
        <optgroup label="Jawa">
        <option>Bandung</option>
        <option>Yogyakarta</option>
        </optgroup>
        <optgroup label="Luar Jawa">
        <option>Makassar</option>
        <option>Medan</option>
        </optgroup>
        </select>


        <label for="bio">Bio Singkat</label>
        <textarea id="bio" name="bio" rows="4" cols="30" placeholder="Ceritakan tentang dirimu..."></textarea>


        <button type="submit">Simpan</button>
    </form>
    </body>
</html>
```

### **Eksperimen/Analisis**

*   Ubah `name` pada salah satu radio sehingga berbeda. Masih eksklusif?
*   Centang beberapa checkbox; cek data terkirim di developer tools (Network) jika memungkinkan.

### **Tugas**

1.  Jadikan `kota` **wajib** (`required`).
2.  Tambahkan opsi `Lainnya` pada hobi dengan sebuah `<input type="text">` bernama `hobi_lain` (tetap selalu terlihat; tanpa JS). **Kumpulkan:** `sesi3-pilihan.html`

### **Kriteria Penilaian**

*   Radio dalam satu grup `name` yang sama
*   `fieldset`/`legend` digunakan untuk kelompok terkait

# **Sesi 4 — Atribut Form Penting: action, method, enctype**

**Tujuan:** Memahami cara data dikirim serta perbedaan GET vs POST, dan unggah berkas.

*   Ringkasan Teori
*   `action`: alamat tujuan pengiriman data.
*   `method`: `GET` (data di URL) vs `POST` (data di body).
*   `enctype`: tipe encoding; untuk upload file gunakan `multipart/form-data`.

### **Langkah Praktik**

Buat `sesi4-kirim.html` untuk mengamati **query string**:

```html
<!DOCTYPE html>
<html lang="id">

    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Sesi 4 – GET</title>
    </head>
    
    <body>
        <h1>Uji GET</h1>
        <form action="" method="get">
        <label>Keyword <input name="q" type="text"></label>
        <button type="submit">Cari</button>
        </form>
    </body>
</html>
```

Ubah `method` menjadi `post` lalu bandingkan perubahan URL saat submit.

Tambahkan contoh upload file (`POST` + `enctype`):

```html
<form action="" method="post" enctype="multipart/form-data">
    <label for="foto">Upload Foto</label>
    <input id="foto" name="foto" type="file" accept="image/*">
    <button type="submit">Kirim</button>
</form>
```

### **Eksperimen/Analisis**

*   Kapan gunakan GET (pencarian, dapat di-bookmark) vs POST (data sensitif/perubahan data)?

### **Tugas**

1.  Buat dua form identik: satu `GET`, satu `POST`. Dokumentasikan perbedaan di komentar `<!-- ... -->`.
2.  Tambahkan input file pada form `POST` dengan `accept="image/*"`. **Kumpulkan:** `sesi4-kirim.html`

### **Kriteria Penilaian**

*   Contoh GET & POST berjalan
*   Penjelasan beda GET/POST tertulis di komentar

# **Sesi 5 — Validasi HTML5**

**Tujuan:** Memakai validasi bawaan browser tanpa.

### **Ringkasan Teori**

*   Atribut: `required`, `pattern`, `min`, `max`, `step`, `minlength`, `maxlength`.
*   `novalidate` pada `<form>` menonaktifkan validasi bawaan (jangan digunakan jika ingin validasi menyala).
*   `title` pada input dapat menambah pesan bantuan untuk pola (`pattern`).

### **Langkah Praktik**

Buat `sesi5-validasi.html`:

```html
<!DOCTYPE html>
<html lang="id">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Sesi 5 – Validasi</title>
    </head>
    
    <body>
        <h1>Form Validasi</h1>
        <form action="" method="post">
            <label>Email
            <input name="email" type="email" required>
            </label>
            <label>Kode Pos (5 digit)
            <input name="kodepos" type="text" pattern="^\d{5}$" title="Masukkan 5 digit angka" placeholder="40123" required>
            </label>
            <label>Skor (0–100)
            <input name="skor" type="number" min="0" max="100" step="1" required>
            </label>
            <button type="submit">Kirim</button>
        </form>
    </body>
</html>
```

### **Eksperimen/Analisis**

*   Isi `kodepos` dengan 4 digit → amati pesan kesalahan.
*   Ubah `pattern` menjadi `^\d{5,6}$` agar menerima 5–6 digit.

### **Tugas**

1.  Tambahkan input `username` dengan `pattern` hanya huruf/angka (`^[A-Za-z0-9]+$`) dan `minlength="4"`.
2.  Tambahkan `title` yang menjelaskan aturan `username`. **Kumpulkan:** `sesi5-validasi.html`

### **Kriteria Penilaian**

*   Validasi berjalan sesuai aturan atribut HTML
*   Pesan bantuan melalui `title` relevan

# **Sesi 6 — Aksesibilitas Dasar (a11y)**

**Tujuan:** Membuat form mudah dipahami pembaca layar & logis urutannya.

### **Ringkasan Teori**

*   `label` harus terkait dengan input (`for`–`id`).
*   Gunakan `fieldset` dan `legend` untuk mengelompokkan bagian form.
*   Bantuan/penjelasan dapat dihubungkan ke input lewat `aria-describedby`.

### **Langkah Praktik**

Buat `sesi6-a11y.html`:

```html
<!DOCTYPE html>
<html lang="id">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Sesi 6 – Aksesibilitas</title>
    </head>
    <body>
        <h1>Form Aksesibel</h1>
        <form action="" method="post">
            <fieldset>
            <legend>Informasi Kontak</legend>
            <label for="email">Email</label>
            <input id="email" name="email" type="email" aria-describedby="emailHelp" required>
            <small id="emailHelp">Kami tidak akan membagikan email Anda.</small>
            </fieldset>
            <button type="submit">Kirim</button>
        </form>
    </body>
</html>
```

### Eksperimen/Analisis

*   Gunakan tombol **Tab** untuk berpindah fokus. Apakah urutannya logis?
*   Hilangkan `for` pada salah satu label; bandingkan pengalaman fokus.

### Tugas

1.  Tambahkan grup alamat (jalan, kota, kode pos) dalam `fieldset` terpisah.
2.  Tautkan teks error (mis. `<small>`) ke masing-masing input via `aria-describedby`. **Kumpulkan:** `sesi6-a11y.html`

### Kriteria Penilaian

*   Semua input ber-`label`
*   Kelompok `fieldset/legend` bermakna; ada `aria-describedby` bila relevan

# **Sesi 7 — Struktur & Organisasi**

**Tujuan:** Menyusun form yang tetap terstruktur rapi hanya dengan HTML.

### **Ringkasan Teori**

*   Susun urutan input secara logis (dari identitas → kontak → opsi → konfirmasi).
*   Gunakan judul/heading (`<h1>`, `<h2>`) untuk memecah bagian.
*   Manfaatkan `placeholder`, `value` awal, `selected` pada `option`, dan `checked` pada radio/checkbox untuk memberi konteks.
*   Gunakan `autofocus` pada satu input yang paling awal dibutuhkan (opsional; jangan lebih dari satu per halaman).

### **Langkah Praktik**

Buat `sesi7-struktur.html`:

```html
<!DOCTYPE html>
<html lang="id">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Sesi 7 – Struktur</title>
    </head>
    <body>
        <h1>Form Pendaftaran</h1>
        <h2>Data Diri</h2>
        <form action="" method="post">
            <label for="fn">Nama Depan</label>
            <input id="fn" name="fn" type="text" autofocus>


            <label for="ln">Nama Belakang</label>
            <input id="ln" name="ln" type="text">


            <h2>Kontak</h2>
            <label for="em">Email</label>
            <input id="em" name="em" type="email" placeholder="nama@contoh.com">


            <h2>Pesan</h2>
            <label for="msg">Pesan</label>
            <textarea id="msg" name="msg" rows="5" cols="30"></textarea>


            <button type="submit">Kirim</button>
        </form>
    </body>
</html>
```

## **Eksperimen/Analisis**

*   Tambahkan `value` awal pada beberapa field. Bagaimana pengaruhnya ke pengalaman pengguna?

## **Tugas**

1.  Tambahkan heading untuk bagian **Alamat** dan letakkan input jalan/kota/kode pos di bawahnya.
2.  Tetapkan opsi default `selected` pada sebuah `<select>`. **Kumpulkan:** `sesi7-struktur.html`

## **Kriteria Penilaian**

*   Hirarki heading jelas; urutan input logis
*   Atribut `autofocus`, `selected`, `checked` digunakan secara wajar

# **Sesi 8 — Kontrol & Atribut Khusus HTML**

**Tujuan:** Mengenal kontrol/form fitur khusus tanpa bantuan CSS/JS.

### **Ringkasan Teori**

*   `datalist` memberi saran nilai pada input teks.
*   `input type="file"` untuk unggah berkas (`accept`, `multiple`).
*   `hidden` menyimpan nilai yang tidak terlihat namun terkirim.
*   `readonly` (bisa disalin, tidak bisa diubah) vs `disabled` (tidak bisa difokus/terkirim).

### **Langkah Praktik**

Buat `sesi8-khusus.html`:

```html
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sesi 8 – Kontrol Khusus</title>
</head>
<body>
<h1>Kontrol & Atribut Khusus</h1>
<form action="" method="post" enctype="multipart/form-data">
<label for="warna">Warna Favorit</label>
<input id="warna" name="warna" list="opsi-warna" placeholder="Ketik atau pilih">
<datalist id="opsi-warna">
<option value="Merah">
<option value="Hijau">
<option value="Biru">
</datalist>


<label for="foto">Foto Profil (jpg/png)</label>
<input id="foto" name="foto" type="file" accept="image/jpeg,image/png">


<input type="hidden" name="sumber" value="form-html-only">


<label for="kode">Kode Referensi (readonly)</label>
<input id="kode" name="kode" type="text" value="REF-001" readonly>


<button type="submit">Kirim</button>
</form>
</body>
</html>
```

### Eksperimen/Analisis

*   Bandingkan `readonly` vs `disabled` pada input `kode`.
*   Coba `multiple` pada `type="file"`; bagaimana perilaku unggahnya?

### Tugas

1.  Tambahkan input file yang menerima **lebih dari satu** berkas (`multiple`).
2.  Tambahkan `datalist` untuk saran **kota**. **Kumpulkan:** `sesi8-khusus.html`

### Kriteria Penilaian

*   `datalist`, `file`, `hidden`, `readonly/disabled` dipahami dan digunakan benar

# **Sesi 9 — Atribut Form Terkait Pengisian & Pengiriman**

**Tujuan:** Mengoptimalkan pengisian dengan `autocomplete` dan memahami tombol submit/reset.

### **Ringkasan Teori**

*   `autocomplete` membantu pengisian otomatis (mis: `name`, `email`, `tel`, `postal-code`, `given-name`, `family-name`).
*   Tombol: `<button type="submit">`, `<button type="reset">`, dan `<input type="submit">`.
*   `form` attribute pada kontrol: mengaitkan input/tombol dengan form **meski berada di luar** elemen `<form>`.

### **Langkah Praktik**

Buat `sesi9-autocomplete.html`:

```html
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sesi 9 – Autocomplete & Tombol</title>
</head>
<body>
<h1>Pengisian & Pengiriman</h1>
<form id="f" action="" method="post">
<label for="nama">Nama Lengkap</label>
<input id="nama" name="nama" autocomplete="name" required>


<label for="em">Email</label>
<input id="em" name="email" type="email" autocomplete="email" required>


<label for="telp">Nomor HP</label>
<input id="telp" name="telp" type="tel" autocomplete="tel">


<label for="kode">Kode Pos</label>
<input id="kode" name="kodepos" autocomplete="postal-code" pattern="^\d{5}$" required>
</form>


<!-- Tombol di luar form tetapi tetap mengirim form melalui atribut form -->
<button type="submit" form="f">Kirim</button>
<button type="reset" form="f">Reset</button>
</body>
</html>
```

### **Eksperimen/Analisis**

*   Coba pengisian otomatis browser setelah beberapa kali mengetik data yang sama.
*   Pindahkan tombol ke dalam form; apakah perilaku berubah?

### **Tugas**

1.  Tambahkan `autocomplete` untuk nama depan (`given-name`) dan belakang (`family-name`).
2.  Jadikan `telp` wajib diisi dengan pola sederhana angka 10–13 digit. **Kumpulkan:** `sesi9-autocomplete.html`

### **Kriteria Penilaian**

*   `autocomplete` digunakan secara tepat
*   Atribut `form` pada tombol dipahami

---

# **Sesi 10 — Proyek Akhir (HTML Saja): Form Pendaftaran Lomba Sains**

**Tujuan:** Mengintegrasikan seluruh kemampuan menjadi satu halaman form murni HTML.

### **Spesifikasi Wajib**

*   Satu berkas: `index.html` (tanpa CSS/JS).
*   Field minimal: Nama lengkap, Email, Sekolah, Kelas (select), Tanggal Lahir, Nomor HP, Pilihan Cabang (radio), Persetujuan (checkbox), Alamat, Kota, Kode Pos.
*   Aksesibilitas: semua input ber-`label`; kelompokkan dengan `fieldset/legend`; gunakan `aria-describedby` untuk bantuan/error bila perlu.
*   Validasi HTML5: `required`, `pattern`, `min/max`, `minlength/maxlength` sesuai kebutuhan.
*   Pengisian: `autocomplete` relevan di beberapa field.
*   Pengiriman: `method="post"`; `action` boleh dikosongkan saat latihan.

### Kerangka Contoh `index.html` (silakan modifikasi & lengkapi)

```html
<!DOCTYPE html>
<form action="" method="post">
<fieldset>
<legend>Data Diri</legend>
<label for="nama">Nama Lengkap</label>
<input id="nama" name="nama" required autocomplete="name">


<label for="email">Email</label>
<input id="email" name="email" type="email" required autocomplete="email">


<label for="sekolah">Sekolah</label>
<input id="sekolah" name="sekolah" required>


<label for="kelas">Kelas</label>
<select id="kelas" name="kelas" required>
<option value="">-- pilih --</option>
<option>VII</option>
<option>VIII</option>
<option>IX</option>
</select>


<label for="lahir">Tanggal Lahir</label>
<input id="lahir" name="lahir" type="date" required>


<label for="hp">Nomor HP</label>
<input id="hp" name="hp" type="tel" pattern="^[0-9+\-\s]{9,}$" placeholder="08xxxxxxxx" required>
</fieldset>


<fieldset>
<legend>Pilihan Lomba</legend>
<label><input type="radio" name="cabang" value="Fisika" required> Fisika</label>
<label><input type="radio" name="cabang" value="Kimia"> Kimia</label>
<label><input type="radio" name="cabang" value="Biologi"> Biologi</label>
</fieldset>


<fieldset>
<legend>Alamat</legend>
<label for="alamat">Alamat</label>
<textarea id="alamat" name="alamat" rows="3" required></textarea>


<label for="kota">Kota</label>
<input id="kota" name="kota" required autocomplete="address-level2">


<label for="kodepos">Kode Pos</label>
<input id="kodepos" name="kodepos" pattern="^\d{5}$" required autocomplete="postal-code">
<small id="kodeBantuan">Masukkan 5 digit angka.</small>
</fieldset>


<label>
<input type="checkbox" name="setuju" required>
Saya menyetujui syarat & ketentuan.
</label>


<button type="submit">Daftar</button>
</form>
</body>
</html>
```

### **Rubrik Penilaian Proyek (100 poin)**

*   **Struktur & Aksesibilitas (35):** label terhubung, `fieldset/legend` bermakna, urutan fokus logis.
*   **Validasi HTML5 (30):** aturan tepat; form tidak bisa disubmit jika data tidak valid.
*   **Pengisian & Semantik (20):** `autocomplete`, placeholder, nilai default yang membantu.
*   **Kerapian Kode (15):** indentasi, penamaan, komentar seperlunya.

### **Laporan Singkat (maks. 1 halaman)**

*   Tujuan form & pengguna target
*   Keputusan desain (validasi, struktur, bantuan teks)
*   Tantangan & solusi

### **Opsi Pengayaan (Tetap HTML Murni)**

*   Gunakan `datalist` untuk saran nilai di beberapa field.
*   Tambahkan `readonly`/`disabled` pada skenario tertentu dan jelaskan alasannya.
*   Demonstrasikan `form` attribute untuk tombol di luar form utama.

---