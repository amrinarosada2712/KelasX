# MODUL CSS SMK

## BOX MODEL • DISPLAY • POSITION

### (Materi + Latihan + Project 1 Halaman)

---

## PENDAHULUAN (WAJIB DIBACA SISWA)

Di dalam CSS, **tampilan website tidak dibuat asal-asalan**.  
Ada **aturan dasar** yang harus dipahami dulu, yaitu:

**Box Model** → mengatur ukuran & jarak elemen

**Display** → mengatur cara elemen tampil

**Position** → mengatur letak elemen

👉 **Kalau 3 ini paham, bikin website jadi jauh lebih mudah.**

---

# **BAGIAN 1 — CSS BOX MODEL**

## (Dasar Semua Layout)

### A. Materi Inti (Bahasa Sederhana)

Setiap elemen HTML itu **kotak (box)**.

Isi kotak terdiri dari:

**Content** → isi (teks, gambar, tombol)

**Padding** → jarak isi dengan garis

**Border** → garis tepi

**Margin** → jarak antar kotak

📦 Ibarat kardus:

Barang = content

Ruang kardus = padding

Dinding kardus = border

Jarak antar kardus = margin

---

### B. Contoh Dasar Box Model

```css
.card {
  width: 300px;
  padding: 16px;
  border: 2px solid black;
  margin: 20px;
}
```

Artinya:

Kotak lebarnya 300px

Isi tidak menempel ke tepi

Ada jarak dengan elemen lain

---

### C. Penting! `box-sizing`

```css
* {
  box-sizing: border-box;
}
```

👉 Ini bikin ukuran elemen **tidak membesar walaupun ada padding & border**.  
📌 **WAJIB dipakai di awal CSS.**

---

### D. Latihan 1 — Kartu Produk

#### HTML

```html
<div class="card">
  <h2>Es Kopi Susu</h2>
  <p>Minuman segar favorit siswa.</p>
  <p class="harga">Rp 10.000</p>
  <button>Beli</button>
</div>
```

#### CSS

```css
.card {
  width: 300px;
  padding: 16px;
  border: 2px solid #000;
  margin: auto;
}
```

📌 **Siswa WAJIB melihat hasilnya di browser.**

---

### E. Tugas Box Model

Tambahkan `border-radius`

Ubah `padding` jadi `24px`

Tambahkan `margin-top: 30px`

---

# **BAGIAN 2 — DISPLAY CSS**

## (Supaya Elemen Bisa Sejajar)

### **A. Materi Inti**

`display` mengatur **cara elemen tampil di halaman**.

Jenis penting:

`block` → satu baris penuh

`inline` → sejajar tapi kecil

`inline-block` → sejajar + bisa diatur ukuran

`none` → disembunyikan

---

### **B. Kenapa** `**inline-block**` **Penting?**

Menu, tombol, dan card **BUTUH padding**, tapi **tetap sejajar**.  
👉 Maka dipakai `inline-block`.

---

### **C. Latihan 2 — Menu Website**

#### HTML

```html
<div class="menu">
  <a href="#">Home</a>
  <a href="#">Produk</a>
  <a href="#">Kontak</a>
</div>
```

#### CSS

```css
.menu a {
  display: inline-block;
  padding: 10px 14px;
  background: black;
  color: white;
  margin-right: 6px;
  text-decoration: none;
}
```

📌 Menu sekarang **sejajar dan rapi**.

---

### **D. Tugas Display**

Ubah `display` jadi `block`

Sembunyikan menu “Kontak” pakai `display: none`

---

# **BAGIAN 3 — POSITION CSS**

## (Menempel, Melayang, dan Nempel Layar)

### **A. Materi Inti**

`position` mengatur **letak elemen secara khusus**.

Jenis utama:

`relative` → posisi normal (PATOKAN)

`absolute` → nempel ke parent

`fixed` → nempel ke layar

---

### **B. Aturan Penting (WAJIB INGAT)**

> **absolute BUTUH parent yang relative**

---

### **C. Latihan 3 - Label Promo**

#### HTML

```html
<div class="produk">
  <span class="promo">PROMO</span>
  <h3>Sepatu Sekolah</h3>
</div>
```

#### CSS

```css
.produk {
  width: 300px;
  padding: 16px;
  border: 2px solid black;
  position: relative;
}

.promo {
  position: absolute;
  top: 10px;
  right: 10px;
  background: red;
  color: white;
  padding: 6px;
}
```

📌 Label PROMO menempel di pojok card.

---

### D. Tugas Position

Pindahkan promo ke kiri atas

Ganti warna promo

Tambahkan tombol `position: fixed`

---

# **BAGIAN 4 — PROJECT BESAR (1 HALAMAN)**

## STUDI KASUS

Kamu diminta membuat **Landing Page Toko Online Sederhana**.

### Fitur WAJIB:

✅ Menu di atas  
✅ Banner / Hero  
✅ Produk minimal 3  
✅ Badge promo di setiap produk  
✅ Tombol chat nempel layar

---

# **Struktur HTML Project**

```html
<div class="navbar">
  <a href="#">Home</a>
  <a href="#">Produk</a>
  <a href="#">Kontak</a>
</div>

<div class="hero">
  <h1>MyShop</h1>
  <p>Toko Online Sederhana</p>
</div>

<div class="card">
  <span class="badge">DISKON</span>
  <h3>Jaket</h3>
  <p>Nyaman dipakai</p>
  <button>Beli</button>
</div>

<div class="chat">Chat Admin</div>
```

---

## Aturan CSS Project

Gunakan `box-sizing: border-box`

Card pakai `inline-block`

Badge pakai `absolute`

Chat pakai `fixed`