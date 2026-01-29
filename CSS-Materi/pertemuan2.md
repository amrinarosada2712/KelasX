# Media Pembelajaran Praktek CSS

Materi ini dirancang **langsung bisa dipraktikkan** oleh siswa. Setiap bagian berisi:

*   Tujuan
*   Contoh kasus
*   Contoh kode HTML & CSS
*   Tugas praktekp

---

## **CSS Box Model**

### Tujuan

Memahami bahwa setiap elemen HTML adalah sebuah **kotak** yang terdiri dari:  
**Content → Padding → Border → Margin**

### Contoh Kasus

Membuat sebuah kotak dengan jarak isi, garis tepi, dan jarak antar elemen.

### Contoh Praktekpp

**HTML**

```html
<div class="box">Ini adalah content</div>
```

**CSS**

```css
.box {
  width: 200px;
  padding: 10px;
  border: 2px solid black;
  margin: 20px;
  background-color: lightblue;
}
```

### Penjelasan Praktek

*   **Content** → teks "Ini adalah content"
*   **Padding** → jarak teks ke border
*   **Border** → garis hitam
*   **Margin** → jarak antar elemen

### Tugas Praktek

1.  Ubah padding menjadi 20px
2.  Ganti warna border menjadi merah
3.  Tambahkan 2 kotak dan lihat jaraknya

---

## **Display CSS**

### Tujuan

Memahami cara elemen ditampilkan di halaman.

### Contoh Kasus

Membandingkan `block`, `inline`, dan `inline-block`.

### Contoh Praktek

**HTML**

```html
<div class="block">Block</div>
<span class="inline">Inline</span>
<span class="inline-block">Inline Block</span>
```

**CSS**

```css
.block {
  display: block;
  background: lightcoral;
  margin-bottom: 10px;
}

.inline {
  display: inline;
  background: lightgreen;
}

.inline-block {
  display: inline-block;
  width: 150px;
  height: 50px;
  background: lightblue;
}
```

### Penjelasan Praktek

*   **block** → satu baris penuh
*   **inline** → sejajar, tidak bisa atur ukuran
*   **inline-block** → sejajar dan bisa atur ukuran

### Tugas Praktek

1.  Ubah inline menjadi inline-block
2.  Tambahkan width & height
3.  Amati perbedaannya

---

## **Position CSS**

### Tujuan

Mengatur posisi elemen secara bebas.

### Contoh Kasus

Menempatkan kotak di posisi tertentu.

### Contoh Praktek

**HTML**

```html
<div class="container">
  <div class="box">Kotak</div>
</div>
```

**CSS**

```css
.container {
  position: relative;
  height: 200px;
  border: 2px dashed gray;
}

.box {
  position: absolute;
  top: 10px;
  left: 20px;
  background: orange;
  padding: 10px;
}
```

### Penjelasan Praktek

*   **relative** → posisi acuan
*   **absolute** → mengikuti parent
*   **top & left** → jarak dari atas & kiri

### Tugas Praktek

1.  Ubah posisi ke kanan bawah
2.  Ganti menjadi `fixed`
3.  Scroll halaman dan lihat efeknya