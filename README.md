# Lab2web


## Tugas
<img width="1012" height="556" alt="Screenshot 2025-10-02 130905" src="https://github.com/user-attachments/assets/e25c0808-c363-4cdb-8f89-82e6be57ec2b" />


## Jawaban Pertanyaan dan Tugas

### 1.mengubah dan menambah properti CSS
Di percobaan pertama saya mencoba menambahkan beberapa properti CSS untuk mengatur tampilan elemen HTML. Pada elemen `<h1>` saya ubah warnanya menjadi biru, diperbesar ukurannya, dan saya posisikan di tengah. Pada elemen `<p>` saya beri warna abu-abu, ukuran teks sedang, dan jarak antar baris supaya lebih enak dibaca. Dari percobaan ini terlihat bahwa CSS sangat berperan dalam mempercantik tampilan halaman web.

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

### berikut screenshout codingannya dan output nya
<img width="1365" height="858" alt="Screenshot 2025-10-02 185559" src="https://github.com/user-attachments/assets/7ef3ff6f-8ca5-41e3-848b-74cc69adcf9a" />

---

### 2. Perbedaan `h1 {…}` dengan `#intro h1 {…}`

Perbedaan yang saya temukan adalah bahwa `h1 {…}` akan berlaku untuk semua elemen `<h1>` di halaman, sedangkan `#intro h1 {…}` hanya berlaku untuk elemen `<h1>` yang ada di dalam sebuah tag dengan id `intro`. Jadi aturan dengan `#intro h1` sifatnya lebih spesifik daripada aturan umum `h1 {…}`.

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

Di percobaan ini saya mencoba menerapkan CSS secara eksternal, internal, dan inline pada elemen yang sama. Hasilnya, aturan CSS yang ditampilkan browser mengikuti prioritas. Urutan prioritasnya adalah Inline > Internal > Eksternal. Jadi meskipun saya sudah mengatur warna teks di eksternal dan internal, ketika saya tambahkan style langsung di elemen dengan inline CSS, maka inline yang menang.

**Kode percobaan:**

```html
<link rel="stylesheet" href="style.css"> <!-- Eksternal -->
<style>
  p { color: blue; } /* Internal */
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

👉 Dari percobaan ini hasilnya teks tetap berwarna merah karena inline CSS memiliki prioritas tertinggi.

---

### 4. ID vs Class (spesifisitas CSS)

Pada percobaan terakhir saya menguji perbedaan antara penggunaan ID dan Class. Jika sebuah elemen HTML memiliki keduanya, maka aturan dengan ID akan lebih diutamakan dibandingkan Class. Jadi meskipun class memberi warna biru, tapi karena ID memberi warna merah, maka yang muncul di browser adalah merah.

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

👉 Hasilnya: teks muncul berwarna merah karena ID lebih kuat daripada Class.

---

## Screenshot

Berikut ini adalah tempat untuk menyimpan hasil screenshot dari setiap percobaan:

1. Hasil eksperimen properti CSS.
2. Perbedaan `h1` global dan `#intro h1`.
3. Prioritas eksternal, internal, dan inline CSS.
4. Spesifisitas ID vs Class.

---

## Cara Menjalankan

1. Simpan file `index.html` dan `style.css` dalam folder yang sama.
2. Buka file `index.html` menggunakan browser.
3. Lihat hasil percobaan dan bandingkan dengan penjelasan.
4. Upload hasil kerja ini ke repository GitHub dengan nama **Lab2Web**.

```

---

👉 Dengan gaya penulisan ini, README akan terlihat seolah-olah kamu sendiri yang membuat laporan.  

Mau saya bikin juga **versi index.html gabungan semua percobaan** biar kamu bisa langsung buka sekali jalan dan screenshot per nomor di bawahnya?
```
