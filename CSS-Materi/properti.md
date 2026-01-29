# BAGIAN A

# DAFTAR PROPERTI CSS PER MODUL (LENGKAP + FUNGSI)

## **TEXT MODULE (CSS Text & Fonts)**

### **Font**

| Properti | Fungsi |
| --- | --- |
| `font-family` | Jenis huruf |
| `font-size` | Ukuran font |
| `font-weight` | Ketebalan |
| `font-style` | Italic / normal |
| `font-stretch` | Lebar font |
| `font-variant` | Small-caps, dll |
| `font-optical-sizing` | Auto penyesuaian font variable |
| `font-kerning` | Kerning huruf |
| `font-feature-settings` | Fitur OpenType |
| `font-variation-settings` | Variable font |
| `font` | Shorthand semua font |

---

### **Text Layout & Decoration**

| Properti | Fungsi |
| --- | --- |
| `line-height` | Tinggi baris |
| `letter-spacing` | Jarak huruf |
| `word-spacing` | Jarak kata |
| `text-align` | Perataan teks |
| `text-indent` | Indent baris pertama |
| `text-transform` | Uppercase, dll |
| `text-decoration` | Underline, line-through |
| `text-decoration-color/style/thickness` | Detail dekorasi |
| `text-shadow` | Bayangan teks |
| `text-overflow` | Ellipsis |
| `white-space` | Aturan spasi |
| `word-break` | Pemotongan kata |
| `overflow-wrap` | Paksa wrap |
| `hyphens` | Pemenggalan kata |
| `writing-mode` | Horizontal / vertikal |
| `direction` | LTR / RTL |
| `unicode-bidi` | Kontrol teks bidirectional |

---

## **BACKGROUNDS & COLORS MODULE**

### **Colors**

| Properti | Fungsi |
| --- | --- |
| `color` | Warna teks |
| `opacity` | Transparansi |
| `accent-color` | Warna kontrol form |

### **Background**

| Properti | Fungsi |
| --- | --- |
| `background-color` | Warna latar |
| `background-image` | Gambar / gradient |
| `background-repeat` | Pengulangan |
| `background-position` | Posisi |
| `background-size` | Cover / contain |
| `background-attachment` | Scroll / fixed |
| `background-origin` | Area referensi |
| `background-clip` | Area gambar |
| `background-blend-mode` | Mode blending |
| `background` | Shorthand |

---

## 3️⃣ BORDERS & OUTLINES MODULE

| Properti | Fungsi |
| --- | --- |
| `border` | Border lengkap |
| `border-width/style/color` | Detail border |
| `border-top/right/bottom/left` | Sisi tertentu |
| `border-radius` | Sudut |
| `border-collapse` | Tabel |
| `border-spacing` | Jarak sel |
| `outline` | Garis fokus |
| `outline-offset` | Jarak outline |

---

## **BOX MODEL & SIZING MODULE**

| Properti | Fungsi |
| --- | --- |
| `width / height` | Ukuran |
| `min/max-width` | Batas |
| `min/max-height` | Batas |
| `margin` | Jarak luar |
| `padding` | Jarak dalam |
| `box-sizing` | Perhitungan box |
| `aspect-ratio` | Rasio elemen |
| `overflow` | Konten meluber |
| `overflow-x/y` | Arah tertentu |

---

## **LAYOUT MODULE (Display, Position)**

### **Display**

`display: block | inline | inline-block | none`

`display: flex | grid | flow-root | contents`

### **Position**

| Properti | Fungsi |
| --- | --- |
| `position` | Static, relative, absolute |
| `top/right/bottom/left` | Offset |
| `inset` | Shorthand |
| `z-index` | Layer |
| `float` | Layout lama |
| `clear` | Clear float |
| `isolation` | Stacking context |

---

## **FLEXBOX MODULE**

| Properti | Fungsi |
| --- | --- |
| `flex-direction` | Arah |
| `flex-wrap` | Bungkus |
| `justify-content` | Main axis |
| `align-items` | Cross axis |
| `align-content` | Multi-line |
| `gap` | Jarak |
| `flex-grow/shrink/basis` | Ukuran |
| `flex` | Shorthand |
| `order` | Urutan |
| `align-self` | Override |

---

## **GRID MODULE**

| Properti | Fungsi |
| --- | --- |
| `grid-template-columns/rows` | Struktur |
| `grid-template-areas` | Area |
| `grid-auto-flow` | Alur |
| `grid-auto-rows/columns` | Ukuran |
| `grid-column/row` | Posisi |
| `grid-area` | Area item |
| `justify-items/content` | Alignment |
| `align-items/content` | Alignment |
| `place-items/content/self` | Shorthand |

---

## **TRANSFORMS MODULE**

| Properti | Fungsi |
| --- | --- |
| `transform` | Translate, rotate |
| `transform-origin` | Titik pusat |
| `perspective` | 3D |
| `backface-visibility` | Tampilan belakang |
| `transform-style` | Preserve-3d |

---

## **TRANSITIONS MODULE**

| Properti | Fungsi |
| --- | --- |
| `transition-property` | Properti |
| `transition-duration` | Durasi |
| `transition-timing-function` | Easing |
| `transition-delay` | Delay |
| `transition` | Shorthand |

---

## **ANIMATIONS MODULE**

| Properti | Fungsi |
| --- | --- |
| `animation-name` | Nama keyframes |
| `animation-duration` | Durasi |
| `animation-timing-function` | Easing |
| `animation-delay` | Delay |
| `animation-iteration-count` | Pengulangan |
| `animation-direction` | Arah |
| `animation-fill-mode` | State akhir |
| `animation-play-state` | Pause |
| `animation` | Shorthand |
| `@keyframes` | Frame |

---

## **SCROLL SNAP MODULE**

| Properti | Fungsi |
| --- | --- |
| `scroll-snap-type` | Mode snap |
| `scroll-snap-align` | Posisi snap |
| `scroll-snap-stop` | Paksa berhenti |
| `scroll-margin` | Offset snap |
| `scroll-padding` | Padding snap |
| `overscroll-behavior` | Bounce scroll |

---

## **MULTI-COLUMN MODULE**

| Properti | Fungsi |
| --- | --- |
| `column-count` | Jumlah kolom |
| `column-width` | Lebar |
| `column-gap` | Jarak |
| `column-rule` | Garis kolom |
| `column-span` | Span kolom |
| `columns` | Shorthand |

---

## **INTERACTION & UI MODULE**

| Properti | Fungsi |
| --- | --- |
| `cursor` | Bentuk kursor |
| `pointer-events` | Interaksi |
| `user-select` | Seleksi teks |
| `caret-color` | Cursor teks |
| `resize` | Resize |
| `appearance` | Native look |
| `touch-action` | Gesture |
| `scroll-behavior` | Smooth scroll |

---

# **BAGIAN B**

# **CONTOH KOMPONEN UI (REAL-WORLD)**

---

## **CARD**

```css
.card{
  padding: 20px;
  border-radius: 16px;
  background: #fff;
  box-shadow: 0 10px 30px rgba(0,0,0,.08);
  transition: transform .2s ease;
}
.card:hover{ transform: translateY(-4px); }
```

---

## **NAVBAR**

```css
.navbar{
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 14px 24px;
  position: sticky;
  top: 0;
  background: #fff;
  z-index: 10;
}
.navbar ul{
  display: flex;
  gap: 16px;
  list-style: none;
}
```

---

## **SIDEBAR**

```css
.sidebar{
  width: 240px;
  height: 100vh;
  position: fixed;
  left: 0;
  top: 0;
  background: #111;
  color: #fff;
  padding: 20px;
}
```

---

## **MODAL**

```css
.modal{
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,.5);
  display: grid;
  place-items: center;
}
.modal-box{
  background: #fff;
  padding: 24px;
  border-radius: 14px;
  animation: pop .25s ease;
}
```

---

## **DROPDOWN**

```css
.dropdown{ position: relative; }
.dropdown-menu{
  position: absolute;
  top: 100%;
  right: 0;
  background: #fff;
  border-radius: 10px;
  box-shadow: 0 10px 30px rgba(0,0,0,.1);
  display: none;
}
.dropdown:hover .dropdown-menu{ display: block; }
```

---

## **FORM**

```css
input, textarea{
  width: 100%;
  padding: 12px;
  border-radius: 10px;
  border: 1px solid #ddd;
}
input:focus{
  outline: 3px solid #7aa7ff;
}
```

---

## **TABLE RESPONSI**

```css
.table{
  width: 100%;
  border-collapse: collapse;
}
th, td{
  padding: 12px;
  border-bottom: 1px solid #eee;
}

@media(max-width:600px){
  table, thead, tbody, tr, td, th{
    display: block;
  }
}
```

---