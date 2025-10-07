# **TUGAS MANDIR FORM**

> ### **Ketentuan Umum :** HTML murni — hanya elemen dan atribut HTML; Sintaks HTML wajib ditulis **lengkap** dan **benar**. Gunakan validasi bawaan HTML5 (mis. `required`, `pattern`, `min`, `max`). Setiap input wajib memiliki **label** yang terhubung melalui atribut `for`–`id`.

**Petunjuk Pengerjaan :**

1.  Kerjakan **secara mandiri**.
2.  Tulis kode pada berkas `.html` lalu uji di browser
    *   **Komputer:** gunakan editor teks seperti _Visual Studio Code_.
    *   **Ponsel:** gunakan editor daring seperti _W3Schools Tryit Editor_.
3.  **Catat** hasil pekerjaan di **buku** masing‑masing.
4.  Tambahkan komentar singkat di bagian atas file yang menjelaskan keputusan penting (mis. pola `pattern`, alasan `required`).

> ## Soal 1 — Form Kontak Dasar0
> 
> **Berkas:** `tugas1-form-kontak.html`
> 
> **Spesifikasi**
> 
> Field: Nama (text, required), Email (email, required), Subjek (text, opsional), Pesan (textarea, required).
> 
> `method="post"`, `action` boleh kosong.
> 
> Gunakan placeholder yang informatif.
> 
> **Kriteria Penilaian**: label–id benar; validasi email & wajib; struktur rapi.

> ## Soal 2 — Form Pendaftaran Akun
> 
> **Berkas:** `tugas2-daftar-akun.html`
> 
> **Spesifikasi**
> 
> Username (text, required, `maxlength=15`, `pattern=^[A-Za-z0-9]+$`, `autocomplete="username"`).
> 
> Email (email, required, `autocomplete="email"`).
> 
> Password (password, required, `minlength=6`, `autocomplete="new-password"`).
> 
> Konfirmasi Password (password, required, `minlength=6`).
> 
> Tambahkan teks bantuan menggunakan elemen HTML (mis. `<small>`).
> 
> **Kriteria Penilaian**: aturan validasi tepat; `autocomplete` sesuai; aksesibilitas baik.

> ## Soal 3 — Form Survei Preferensi
> 
> **Berkas:** `tugas3-survei.html`
> 
> **Spesifikasi**
> 
> Radio (satu grup `name` sama) untuk memilih A/B/C (wajib pilih satu).
> 
> Checkbox untuk Hobi (≥4 opsi; kirim hanya yang dicentang).
> 
> Select Kota dengan `optgroup` (Jawa/Luar Jawa), `required`.
> 
> Textarea Komentar (opsional, `maxlength` disarankan).
> 
> Gunakan `fieldset` & `legend` untuk mengelompokkan bagian.
> 
> **Kriteria Penilaian**: radio eksklusif; checkbox multi; `select` ber-`optgroup`; pengelompokan jelas.

> ## Soal 4 — Form Upload Portofolio
> 
> **Berkas:** `tugas4-upload-portofolio.html`
> 
> **Spesifikasi**
> 
> Nama (text, required), Email (email, required), URL Portofolio (url, opsional).
> 
> Input berkas: `type="file"`, `accept="image/*"`, `multiple`.
> 
> Tambah `input type="hidden"` bernama `sumber` dengan nilai `html-only`.
> 
> `method="post"`, `enctype="multipart/form-data"`.
> 
> **Kriteria Penilaian**: method/enctype benar; file constraints tepat; field wajib tervalidasi.

> ## Soal 5 — Form Pemesanan Tiket
> 
> **Berkas:** `tugas5-pemesanan-tiket.html`
> 
> **Spesifikasi**
> 
> Nama (text, required), Email (email, required), Nomor HP (tel, `pattern` 10–13 digit, required).
> 
> Tanggal Kunjungan (date, required); Jumlah Tiket (number, `min=1`, `max=10`, `step=1`, required).
> 
> Kategori (select, required): Dewasa/Anak/Lansia.
> 
> Checkbox persetujuan syarat & ketentuan (`required`).
> 
> `autocomplete` relevan pada `name`, `email`, `tel`.
> 
> **Kriteria Penilaian**: validasi angka/tanggal berjalan; semua field penting `required`; struktur semantik & label benar.