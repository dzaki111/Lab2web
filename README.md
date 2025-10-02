# Lab2web

## Deskripsi
Praktikum ini bertujuan untuk memahami penerapan CSS pada HTML, meliputi penggunaan eksternal, internal, dan inline CSS, serta memahami prioritas aturan CSS berdasarkan spesifisitas (selector global, class, id). Pada laporan ini ditampilkan hasil percobaan dan jawaban pertanyaan.


## Jawaban Pertanyaan dan Tugas

### 1. Eksperimen mengubah dan menambah properti CSS
Pada percobaan pertama, dilakukan eksperimen dengan menambahkan properti CSS pada elemen HTML. Misalnya, elemen `<h1>` diberi warna teks biru, ukuran font diperbesar, dan diratakan ke tengah. Sementara itu, elemen `<p>` diberi warna abu-abu, ukuran teks sedang, serta jarak antar baris agar lebih mudah dibaca. Hal ini menunjukkan bahwa CSS berfungsi untuk mengendalikan tampilan elemen HTML sehingga tampilan lebih menarik dan rapi.

**Kode percobaan:**
```html
<style>
  body {
    background-color: #f2f2f2;
    font-family: Arial, sans-serif;
  }
  h1 {
    color: blue;
    text-align: center;
    font-size: 36px;
  }
  p {
    color: darkslategray;
    font-size: 18px;
    line-height: 1.5;
  }
</style>
````

---

### 2. Perbedaan `h1 {…}` dengan `#intro h1 {…}`

Perbedaan utama ada pada jangkauan selektornya. Selektor `h1 {…}` akan memengaruhi semua elemen `<h1>` di halaman. Sedangkan `#intro h1 {…}` hanya akan memengaruhi elemen `<h1>` yang berada di dalam tag dengan `id="intro"`. Dengan demikian, aturan `#intro h1` lebih spesifik daripada `h1 {…}`.

**Kode percobaan:**

```html
<style>
  h1 {
    color: red;
  }
  #intro h1 {
    color: green;
  }
</style>
<body>
  <h1>Judul Umum (kena CSS global h1)</h1>
  <div id="intro">
    <h1>Judul Intro (kena CSS #intro h1)</h1>
  </div>
</body>
```

---

### 3. Internal, Eksternal, dan Inline CSS

Apabila terdapat deklarasi CSS internal, eksternal, dan inline pada elemen yang sama, maka browser memilih berdasarkan prioritas. Urutannya adalah **Inline > Internal > Eksternal**. Dengan demikian, jika elemen diberi CSS di ketiga tempat tersebut, maka aturan inline selalu menang.

**Kode percobaan:**

```html
<link rel="stylesheet" href="style.css"> <!-- Eksternal -->
<style>
  p { color: blue; } <!-- Internal -->
</style>
<body>
  <p style="color: red;">Teks ini merah karena inline CSS lebih kuat.</p>
</body>
```

**File style.css (eksternal):**

```css
p {
  color: green;
}
```

👉 Hasilnya: teks berwarna **merah** karena inline CSS memiliki prioritas tertinggi.

---

### 4. ID vs Class (spesifisitas CSS)

Jika sebuah elemen HTML memiliki ID dan Class sekaligus, maka aturan CSS akan dipilih berdasarkan tingkat spesifisitas. ID memiliki tingkat spesifisitas lebih tinggi daripada Class. Artinya, jika keduanya memiliki aturan berbeda, maka aturan dari ID yang akan ditampilkan browser.

**Kode percobaan:**

```html
<style>
  .text-paragraph {
    color: blue;
  }
  #paragraph-1 {
    color: red;
  }
</style>
<body>
  <p id="paragraph-1" class="text-paragraph">
    Paragraf ini merah karena ID lebih kuat daripada Class.
  </p>
</body>
```

Hasilnya: teks ditampilkan **merah** karena ID `#paragraph-1` lebih kuat dibandingkan Class `.text-paragraph`.

---

## Screenshot

Tambahkan screenshot hasil percobaan masing-masing nomor di sini:

1. Hasil eksperimen properti CSS.
2. Perbedaan `h1` global dan `#intro h1`.
3. Prioritas eksternal, internal, dan inline CSS.
4. Spesifisitas ID vs Class.

---

## Cara Menjalankan

1. Simpan file `index.html` dan `style.css` pada folder yang sama.
2. Buka `index.html` menggunakan browser.
3. Amati hasil percobaan sesuai penjelasan di atas.
4. Commit hasil kerja ke repository GitHub dengan nama **Lab2Web**.

```

---

👉 README ini sudah siap dipakai, kamu tinggal tambahkan **screenshot hasil browser** setelah menjalankan kodingan tadi.  

Mau sekalian saya gabungkan semua percobaan tadi jadi **satu file index.html** dengan komentar pembatas (Percobaan 1, 2, 3, 4) biar gampang jalannya?
```
