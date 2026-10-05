# Modul Praktikum: CSS Dasar dan CSS Eksternal

Dokumen ini berisi panduan dan langkah-langkah praktikum pembuatan halaman web sederhana menggunakan **CSS Internal**, **Inline CSS**, dan **CSS Eksternal** serta penerapan berbagai **Selector CSS**.

---

## 📂 Struktur Berkas Proyek
Buatlah folder praktikum dan pastikan memiliki struktur berkas sebagai berikut:
```text
praktikum-css/
│
├── dasar.html            # File HTML utama
└── style_eksternal.css   # File stylesheet eksternal
```

---

## 🛠️ Langkah-Langkah Praktikum

### **Langkah 1: Membuat File CSS Eksternal**
1. Buat berkas baru dengan nama `style_eksternal.css`.
2. Ketikkan kode CSS berikut untuk mengatur elemen **navigasi**, **ID Selector**, dan **Class Selector**:

```css
/* Styling Menu Navigasi */
nav {
    background: #20A759;
    color: #fff;
    padding: 10px;
}

nav a {
    color: #fff;
    text-decoration: none;
    padding: 10px 20px;
}

nav .active,
nav a:hover {
    background-color: #178043;
}

/* ID Selector (#intro) */
#intro {
    background: #418fb1;
    border: 1px solid #099249;
    padding: 10px;
    min-height: 100px;
}

#intro h1 {
    text-align: left;
    border: 0;
    color: #fff;
}

/* Class Selector (.button) */
.button {
    padding: 15px 20px;
    background: #ff1c1c;
    color: #fff;
    display: inline-block;
    margin: 10px;
    text-decoration: none;
}
```
3. Simpan berkas `style_eksternal.css`.

---

### **Langkah 2: Membuat File HTML dan Mengintegrasikan CSS**
1. Buat berkas baru dengan nama `dasar.html` di dalam folder yang sama.
2. Tuliskan kode HTML dasar beserta pemanggilan CSS eksternal, internal, dan inline sebagai berikut:

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Dasar</title>
    
    <!-- 1. Menghubungkan CSS Eksternal -->
    <link rel="stylesheet" type="text/css" href="style_eksternal.css">

    <!-- 2. Menambahkan CSS Internal -->
    <style>
        body {
            font-family: 'Open Sans', sans-serif;
        }
        header {
            min-height: 80px;
            border-bottom: 1px solid #77CCEF;
        }
        h1 {
            font-size: 24px;
            color: #0F189F;
            text-align: center;
            padding: 20px 10px;
        }
        h1 i {
            color: #7b7a7a;
        }
    </style>
</head>
<body>
    <header>
        <h1>CSS Internal dan <i>Inline CSS</i></h1>
    </header>

    <!-- Menu Navigasi menggunakan style dari CSS Eksternal -->
    <nav>
        <a href="lab2_css_dasar.html">CSS Dasar</a>
        <a href="lab2_css_eksternal.html">CSS Eksternal</a>
        <a href="lab1_tag_dasar.html">HTML Dasar</a>
    </nav>

    <!-- Konten Utama dengan ID Selector -->
    <div id="intro">
        <h1>HELLO World</h1>
        <p>
            Kami sedang belajar HTML dan CSS dasar pada mata kuliah <b>Pemrograman Web</b> 
            di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat adalah 
            membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML dan CSS.
        </p>
        
        <!-- Tombol menggunakan Class Selector -->
        <a class="button btn-primary" href="#intro">Informasi Selengkapnya</a>
    </div>

    <!-- 3. Penerapan Inline CSS -->
    <p style="text-align: center; color: #ccd8e4;">&copy; 2026 Praktikum Web</p>
</body>
</html>
```
3. Simpan berkas `dasar.html`.

---

### **Langkah 3: Pengujian di Browser**
1. Buka folder proyek Anda.
2. Klik dua kali pada file `dasar.html` atau buka menggunakan browser (Chrome/Firefox).
3. Amati perubahan tampilan:
   - Header atas menggunakan style dari **CSS Internal**.
   - Navigasi hijau dan kotak biru (`#intro`) menggunakan **CSS Eksternal**.
   - Tombol merah menggunakan **Class Selector (`.button`)**.

---