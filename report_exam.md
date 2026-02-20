# 📋 Penilaian Objektif Ujian Akhir HTML Dasar dan Form

| Keterangan | Detail |
|---|---|
| **Mata Kuliah** | HTML Dasar dan Form |
| **Total Soal** | 30 |
| **Metode Penilaian** | Objektif per-soal berdasarkan spesifikasi, constraint, dan validitas HTML |

---

## Rekap Nilai

| Bagian | Soal | Nilai Diperoleh | Nilai Maks |
|---|---|---|---|
| A — Dasar Markup & Hierarki Konten | 1–10 | 84 | 100 |
| B — Multimedia, Tabel & Semantik | 11–19 | 72 | 90 |
| C — Lanjutan HTML Form & Input | 20–30 | 88 | 110 |
| **TOTAL** | **30** | **244** | **300** |
| **NILAI AKHIR (skala 100)** | | **81.3** | **100** |

---

## Detail Penilaian Per Soal

### BAGIAN A — Dasar Markup & Hierarki Konten

---

#### ✅ Soal 1 — Struktur Dokumen HTML5 `(10/10)`

**Jawaban:**
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ujian Akhir HTML</title>
    <link rel="icon" href="assets/logo.png" />
  </head>
  <body></body>
</html>
```

**Analisis:**
- ✅ `<!DOCTYPE html>` deklarasi HTML5 hadir
- ✅ `<meta charset="UTF-8">` mencegah *missing charset* warning
- ✅ `<meta name="viewport" ...>` konfigurasi responsif benar
- ✅ `<title>` sesuai spesifikasi: `"Ujian Akhir HTML"`
- ✅ Favicon menggunakan `rel="icon"` dan path `assets/logo.png` tepat
- ✅ Struktur `<html>`, `<head>`, `<body>` lengkap dan valid

---

#### ✅ Soal 2 — Hierarki Heading `(10/10)`

**Jawaban:**
```html
<h1>Belajar Pemrograman</h1>
<h2>Bahasa Web</h2>
<h3>HTML Dasar</h3>
```

**Analisis:**
- ✅ Urutan hierarki H1 → H2 → H3 benar secara semantik
- ✅ Teks di setiap level sesuai spesifikasi
- ✅ H1 hanya berjumlah satu (constraint terpenuhi)
- ✅ Tidak menggunakan tag usang seperti `<font>`

---

#### ✅ Soal 3 — Pemformatan Teks Semantik `(10/10)`

**Jawaban:**
```html
<p>
  "Harga normal adalah <del>10.000</del>, kini menjadi <ins>5.000</ins>.
  H<sub>2</sub>O adalah rumus air."
</p>
```

**Analisis:**
- ✅ `<del>` untuk teks tercoret (`10.000`)
- ✅ `<ins>` untuk garis bawah (`5.000`)
- ✅ `<sub>` untuk subscript (`2` pada H₂O)
- ✅ Tidak menggunakan CSS (constraint terpenuhi)
- ✅ Teks konten sesuai spesifikasi

---

#### ✅ Soal 4 — HTML Entities `(10/10)`

**Jawaban:**
```html
<p>&lt;h1&gt;Selamat Datang&lt;/h1&gt;</p>
```

**Analisis:**
- ✅ `&lt;` dan `&gt;` digunakan dengan benar untuk karakter `<` dan `>`
- ✅ Browser akan menampilkan literal `<h1>Selamat Datang</h1>` tanpa merendernya sebagai heading
- ✅ Menggunakan entity code, bukan tag pembungkus biasa

---

#### ⚠️ Soal 5 — Blok Kode Preformatted `(8/10)`

**Jawaban:**
```html
<pre>
  <code style="font-family: monospace;">
    def salam():
        print("Halo")
  </code>
</pre>
```

**Analisis:**
- ✅ `<pre>` mempertahankan whitespace dan indentasi
- ✅ `<code>` sebagai *computer code tag* yang spesifik sesuai constraint
- ⚠️ Penambahan `style="font-family: monospace;"` redundan karena browser sudah menerapkan font monospaced secara default pada `<code>` yang berada di dalam `<pre>`. Meskipun soal tidak melarang CSS secara eksplisit, ini menunjukkan pemahaman yang kurang sempurna
- ✅ Indentasi 4 spasi sebelum `print` terjaga

**Pengurangan:** -2 (redundansi CSS yang tidak perlu)

---

#### ✅ Soal 6 — Hyperlink Internal & Eksternal `(10/10)`

**Jawaban:**
```html
<a href="https://niagahoster.co.id/" target="_blank">buka di tab baru</a>
<a href="kontak.html" target="_self">buka di tab yang sama</a>
```

**Analisis:**
- ✅ Absolute URL untuk link eksternal
- ✅ Relative URL untuk link internal (`kontak.html`)
- ✅ `target="_blank"` untuk tab baru
- ✅ `target="_self"` untuk tab yang sama

---

#### ✅ Soal 7 — Bookmark / Anchor Navigation `(10/10)`

**Jawaban:**
```html
<p><a href="#footer">Ke Bawah</a></p>
<div id="footer">INI ADALAH DIV FOOTER</div>
```

**Analisis:**
- ✅ `href="#footer"` menggunakan prefix `#` dengan benar
- ✅ Elemen target memiliki `id="footer"` yang bersesuaian
- ✅ Teks link sesuai spesifikasi: `"Ke Bawah"`

---

#### ✅ Soal 8 — Ordered List dengan Tipe Huruf `(10/10)`

**Jawaban:**
```html
<ol type="A">
  <li>Budi</li>
  <li>Andi</li>
  <li>Siti</li>
</ol>
```

**Analisis:**
- ✅ `type="A"` menghasilkan format huruf kapital (A, B, C)
- ✅ Tiga item sesuai spesifikasi: Budi, Andi, Siti
- ✅ Output akan menampilkan `A. Budi`, `B. Andi`, `C. Siti`

---

#### ⚠️ Soal 9 — Nested List `(6/10)`

**Jawaban:**
```html
<ul>
  Kendaraan        <!-- ❌ teks langsung di dalam <ul> tanpa <li> -->
  <ul>
    <li>Mobil
      <ul>
        <li>Avanza</li>
        ...
      </ul>
    </li>
    ...
  </ul>
</ul>
```

**Analisis:**
- ✅ Struktur nested list terbentuk secara fungsional
- ✅ Sub-sub list (Avanza, BYD, dll.) ter-wrap dengan `<li>` dan `<ul>` yang benar
- ❌ **Invalid HTML**: Teks `"Kendaraan"` diletakkan langsung sebagai *text node* di dalam `<ul>` tanpa dibungkus `<li>`. Menurut spesifikasi HTML, konten langsung di dalam `<ul>` hanya boleh berupa elemen `<li>`. Ini menyebabkan DOM yang tidak valid dan perilaku render yang tidak konsisten antar browser
- **Solusi benar:** `<li>Kendaraan</li>` sebagai parent item

**Pengurangan:** -4 (struktur HTML tidak valid pada elemen induk utama)

---

#### ❌ Soal 10 — Block vs Inline Element `(6/10)`

**Jawaban:**
```html
<p>Harga <diskon style="color: blue">Diskon</diskon></p>
```

**Analisis:**
- ✅ Secara visual kata "Harga" dan "Diskon" berada di baris yang sama
- ❌ **Tag `<diskon>` adalah custom/unknown tag yang tidak valid dalam standar HTML5.** Browser memang me-render unknown tag sebagai inline element secara default, namun ini bukan tag HTML yang sah. Constraint secara jelas mewajibkan penggunaan tag inline yang **valid**
- **Solusi benar:** Menggunakan `<span style="color: blue">Diskon</span>`, di mana `<span>` adalah representasi canonical tag inline di HTML
- ✅ Kata "Diskon" tidak menyebabkan line break (efek visual tercapai, meski caranya salah)

**Pengurangan:** -4 (tag tidak valid, tidak memenuhi standar HTML5)

---

### BAGIAN B — Multimedia, Tabel & Semantik

---

#### ⚠️ Soal 11 — Gambar Responsif `(7/10)`

**Jawaban:**
```html
<img src="./Indonesia Nature.jpg" alt="Foto Pantai" width="50%" />
```

**Analisis:**
- ✅ `width="50%"` menggunakan persentase sesuai constraint
- ✅ `alt="Foto Pantai"` sesuai spesifikasi aksesibilitas
- ❌ **Nama file tidak sesuai spesifikasi.** Soal mewajibkan `pemandangan.jpg`, jawaban menggunakan `Indonesia Nature.jpg`. Gambar tidak akan tampil karena path salah
- ✅ Logika dan atribut HTML sudah benar secara teknis

**Pengurangan:** -3 (nama file tidak sesuai spesifikasi input)

---

#### ⚠️ Soal 12 — Responsive Image dengan `<picture>` `(8/10)`

**Jawaban:**
```html
<picture>
  <source media="(max-width: 500px)" srcset="kucing_kecil.jpg" />
  <img src="./kucing_besar.jpg" alt="default images" />
</picture>
```

**Analisis:**
- ✅ Struktur `<picture>` + `<source>` + `<img>` fallback benar
- ✅ Media query `(max-width: 500px)` sesuai spesifikasi
- ⚠️ Nama file berbeda dengan spesifikasi: soal minta `kucing-kecil.png` (hyphen, .png), jawaban `kucing_kecil.jpg` (underscore, .jpg). Logika HTML sudah benar
- ✅ Tag fallback `<img>` hadir

**Pengurangan:** -2 (inkonsistensi nama file)

---

#### ⚠️ Soal 13 — Audio Multi-Format `(7/10)`

**Jawaban:**
```html
<audio controls>
  <source src="./dj_html.mp3" type="audio/mp3" />
  <source src="./dj_html_weba.weba" type="audio/weba" />
  YOUR BROWSER DOESNT SUPPORT THE AUDIO
</audio>
```

**Analisis:**
- ✅ `controls` hadir, UI play/pause tersedia
- ✅ Tidak ada `autoplay` (constraint terpenuhi)
- ✅ Dua format source dicantumkan
- ✅ Fallback text untuk browser yang tidak support
- ❌ MIME type `type="audio/weba"` tidak valid. Format yang benar adalah `type="audio/webm"`
- ❌ Nama file `dj_html.mp3` dan `dj_html_weba.weba` tidak sesuai spesifikasi (`lagu.mp3` dan `lagu.webm`)

**Pengurangan:** -3 (nama file salah, MIME type tidak valid)

---

#### ✅ Soal 14 — Video Autoplay Muted `(10/10)`

**Jawaban:**
```html
<video muted width="800px" autoplay>
  <source src="trailer.mp4" />
</video>
```

**Analisis:**
- ✅ Atribut `autoplay` hadir
- ✅ Atribut `muted` hadir (wajib oleh browser modern agar autoplay bekerja)
- ✅ `width="800px"` sesuai spesifikasi
- ✅ File `trailer.mp4` sesuai spesifikasi

---

#### ✅ Soal 15 — Embed YouTube via Iframe `(10/10)`

**Jawaban:**
```html
<iframe
  src="https://www.youtube.com/embed/xyz"
  frameborder="0"
  width="500px"
  height="500px"
></iframe>
```

**Analisis:**
- ✅ URL embed YouTube sesuai spesifikasi
- ✅ Dimensi `500x500` sesuai spesifikasi
- ✅ `frameborder="0"` untuk tampilan bersih
- ✅ Semua atribut iframe valid

---

#### ✅ Soal 16 — Tabel dengan Rowspan `(10/10)`

**Jawaban:**
```html
<table border="1px solid black">
  <tr>
    <th>DIVISI</th>
    <th>NAMA</th>
  </tr>
  <tr>
    <td rowspan="2">IT</td>
    <td>Budi</td>
  </tr>
  <tr>
    <td>Joko</td>
  </tr>
</table>
```

**Analisis:**
- ✅ `rowspan="2"` pada sel IT dengan nilai yang tepat (mencakup 2 baris: Budi dan Joko)
- ✅ Header `DIVISI` dan `NAMA` sesuai spesifikasi
- ✅ Struktur tabel valid dan ter-render dengan benar

---

#### ⚠️ Soal 17 — Tabel dengan `<thead>`, `<tbody>`, `<tfoot>` `(7/10)`

**Jawaban:**
```html
<table border="1px solid black">
  <thead>
    <tr><th rowspan="3">Kolom Judul</th></tr>
  </thead>
  <tbody>
    <tr><td rowspan="3" colspan="3">Baris Rincian Barang</td></tr>
  </tbody>
  <tfoot>
    <tr><td rowspan="3">Total Biaya</td></tr>
  </tfoot>
</table>
```

**Analisis:**
- ✅ Tiga tag semantik `<thead>`, `<tbody>`, `<tfoot>` digunakan
- ✅ Konten di setiap bagian sesuai konteks: judul, rincian, total
- ⚠️ Penggunaan `rowspan="3"` pada `<thead>` dan `<tfoot>` tidak diperlukan dan **tidak logis** karena hanya ada satu baris di masing-masing section — tidak ada baris tambahan untuk di-span. Ini menunjukkan misunderstanding pada rowspan
- ⚠️ `colspan="3"` pada tbody tidak didukung struktur kolom yang ada (hanya 1 kolom di thead)

**Pengurangan:** -3 (rowspan dan colspan tidak tepat secara konteks)

---

#### ✅ Soal 18 — Gambar Semantik dengan `<figure>` `(10/10)`

**Jawaban:**
```html
<figure>
  <img src="grafik.jpg" alt="Grafik" />
  <figcaption>Grafik Penjualan 2025</figcaption>
</figure>
```

**Analisis:**
- ✅ `<figure>` sebagai pembungkus semantik
- ✅ `<figcaption>` dengan teks `"Grafik Penjualan 2025"` sesuai spesifikasi
- ✅ Nama file dan alt sesuai
- ✅ Tidak menggunakan `<div class="gambar">`

---

#### ✅ Soal 19 — Accordion Tanpa JavaScript `(10/10)`

**Jawaban:**
```html
<details>
  <summary>Baca Syarat</summary>
  <p>Anda harus patuh aturan</p>
</details>
```

**Analisis:**
- ✅ `<details>` sebagai tag accordion native HTML
- ✅ `<summary>` sebagai trigger klik dengan teks `"Baca Syarat"`
- ✅ Konten tersembunyi secara default dan muncul saat diklik
- ✅ Tanpa JavaScript sama sekali

> **Catatan:** Teks isi sedikit berbeda: spesifikasi `"Anda harus patuh aturan."` vs jawaban `"Anda harus patuh aturan"` (tanpa titik). Ini sangat minor.

---

### BAGIAN C — Lanjutan HTML Form & Input

---

#### ✅ Soal 20 — Konfigurasi Form Action & Method `(10/10)`

**Jawaban:**
```html
<form action="/submit-profile" method="post">
  <button type="submit">pencet aku</button>
</form>
```

**Analisis:**
- ✅ `action="/submit-profile"` sesuai spesifikasi
- ✅ `method="post"` untuk transfer via Payload Body (tidak terekspos di URL)
- ✅ Tombol submit hadir

---

#### ✅ Soal 21 — Label & Input Aksesibel `(10/10)`

**Jawaban:**
```html
<label for="soal_21">Klik Saya</label>
<input type="text" name="soal_21" id="soal_21" />
```

**Analisis:**
- ✅ `for="soal_21"` pada label identik dengan `id="soal_21"` pada input
- ✅ Klik pada label akan mem-fokus input (constraint terpenuhi)
- ✅ Input tidak dibungkus di dalam label (constraint terpenuhi)
- ✅ Teks label `"Klik Saya"` sesuai spesifikasi

---

#### ✅ Soal 22 — Radio Button Mutual Exclusive `(10/10)`

**Jawaban:**
```html
<input type="radio" name="soal_22" id="kartu_kredit" />
<label for="kartu_kredit">Kartu Kredit</label>
<input type="radio" name="soal_22" id="transfer_bank" />
<label for="transfer_bank">Transfer Bank</label>
<input type="radio" name="soal_22" id="e-wallet" />
<label for="e-wallet">E-Wallet</label>
```

**Analisis:**
- ✅ Semua radio button memiliki `name="soal_22"` yang sama → mutual exclusive terpenuhi
- ✅ Tiga opsi sesuai spesifikasi
- ✅ Setiap radio berelasi dengan label melalui `for`/`id`

---

#### ⚠️ Soal 23 — Validasi Form HTML5 Native `(7/10)`

**Jawaban:**
```html
<form action="#">
  <label for="email">Email: </label>
  <input type="email" name="email" id="email"
    required="Please fill out this field" /><br />
  <button type="submit" id="email" name="email">Submit Email</button>
</form>
```

**Analisis:**
- ✅ `type="email"` memvalidasi format email secara native
- ✅ `required` hadir untuk mencegah submit saat kosong
- ❌ **`required` adalah boolean attribute** — nilai `"Please fill out this field"` tidak berpengaruh. Browser mengabaikan nilai tersebut dan menampilkan pesan default browser. Untuk custom message diperlukan JavaScript (yang di luar scope HTML murni)
- ❌ **Duplikasi `id="email"`** antara `<input>` dan `<button>`. `id` harus unik dalam satu dokumen. Ini invalid HTML dan bisa menyebabkan bug pada screen reader dan JavaScript DOM selection

**Pengurangan:** -3 (misunderstanding boolean attribute required + duplikasi id)

---

#### ✅ Soal 24 — Date Picker dengan Batasan Rentang `(10/10)`

**Jawaban:**
```html
<label for="tiket">Pemesanan Tiket: </label>
<input type="date" name="tiket" id="tiket" max="2026-05-31" min="2026-05-01" />
```

**Analisis:**
- ✅ `type="date"` menampilkan date picker native
- ✅ `min="2026-05-01"` dan `max="2026-05-31"` sesuai spesifikasi
- ✅ Tanggal di luar rentang akan greyed-out
- ✅ Label terhubung dengan `for`/`id`

---

#### ⚠️ Soal 25 — File Upload dengan Enctype `(8/10)`

**Jawaban:**
```html
<form action="" enctype="multipart/form-data" method="post">
  <input type="file" id="soal_25" name="soal_25" /><br />
  <button type="submit" id="soal_25" name="soal_25">Submit</button>
</form>
```

**Analisis:**
- ✅ `enctype="multipart/form-data"` benar untuk file upload
- ✅ `method="post"` tepat
- ✅ `type="file"` menampilkan file chooser
- ❌ **Duplikasi `id="soal_25"`** pada `<input>` dan `<button>`. Sama seperti soal 23, ini invalid HTML

**Pengurangan:** -2 (duplikasi id)

---

#### ⚠️ Soal 26 — Autocomplete dengan `<datalist>` `(8/10)`

**Jawaban:**
```html
<label for="soal_26">Asal Sekolah: </label>
<input list="sekolah" id="soal_26" name="soal_26" />
<datalist id="sekolah">
  <option value="SDN 1" id="soal_26">SDN 001</option>
  <option value="SMP 2">SMP 002</option>
  <option value="SMA 3">SMA 003</option>
</datalist>
```

**Analisis:**
- ✅ Koneksi `list="sekolah"` ↔ `id="sekolah"` pada datalist benar
- ✅ Tiga opsi rekomendasi sesuai spesifikasi
- ❌ `id="soal_26"` pada elemen `<option>` tidak diperlukan dan menyebabkan **duplikasi id** dengan input di atas
- ✅ Fungsionalitas autocomplete akan berjalan dengan baik

**Pengurangan:** -2 (id tidak valid pada option + duplikasi id)

---

#### ❌ Soal 27 — Hidden Input Field `(4/10)`

**Jawaban:**
```html
<form action="" method="post">
  <label for="hidden_input">Token ID: </label>
  <input type="text" value="ABX123" id="hidden_input" name="hidden_input" required />
  <button type="submit">Submit</button>
</form>
```

**Analisis:**
- ❌ **Kesalahan fundamental:** Menggunakan `type="text"` bukan `type="hidden"`. Field dengan `type="text"` **terlihat** oleh pengguna, bertentangan langsung dengan constraint: *"Tidak terlihat kotak apapun pada antarmuka web"*
- ❌ Penambahan `<label>` dan `required` pada hidden field tidak masuk akal secara konsep — hidden input tidak memerlukan label atau validasi wajib
- ✅ Nilai `value="ABX123"` sudah benar
- **Solusi benar:** `<input type="hidden" name="token_id" value="ABX123" />`

**Pengurangan:** -6 (kesalahan tipe input yang bersifat fundamental)

---

#### ✅ Soal 28 — Validasi Pattern Regex pada Input Tel `(10/10)`

**Jawaban:**
```html
<input type="tel" pattern="^\d{11,13}$" required id="phone" name="phone" />
<input type="submit" value="Submit" />
```

**Analisis:**
- ✅ `type="tel"` sesuai constraint
- ✅ `pattern="^\d{11,13}$"` — regex benar untuk validasi 11–13 digit angka
- ✅ `required` mencegah field kosong disubmit
- ✅ Submission akan diblokir browser untuk input tidak valid

---

#### ⚠️ Soal 29 — Grouping Form dengan `<fieldset>` `(8/10)`

**Jawaban:**
```html
<fieldset>
  <legend>Informasi Detail</legend>
  <label for="username">Username: </label>
  <input type="text" id="username" name="username" /><br />
  <label for="password">Password: </label>
  <input type="password" id="password" name="password" /><br />
  <input type="submit" value="Submit" />
</fieldset>
```

**Analisis:**
- ✅ `<fieldset>` + `<legend>` digunakan dengan benar
- ✅ Teks legend `"Informasi Detail"` sesuai spesifikasi
- ✅ Tidak menggunakan `<div>` atau CSS
- ⚠️ Soal hanya mewajibkan **1 input textbox**, namun jawaban menambahkan input password dan submit button. Meskipun ini tidak salah secara teknis, ini melebihi scope dan dapat mengurangi nilai pada ujian yang ketat

**Pengurangan:** -2 (melebihi spesifikasi dengan input tambahan yang tidak diminta)

---

#### ✅ Soal 30 — Slider Range dengan Step Diskrit `(10/10)`

**Jawaban:**
```html
<label for="slider">Indikator: </label>
<input type="range" value="50" step="25" id="slider" name="slider" min="0" max="100" />
```

**Analisis:**
- ✅ `type="range"` benar
- ✅ `min="0"` dan `max="100"` sesuai spesifikasi
- ✅ `step="25"` membuat titik diskrit: 0, 25, 50, 75, 100
- ✅ `value="50"` sebagai nilai awal
- ✅ Label berelasi dengan `for`/`id`

---

## Ringkasan Temuan & Rekomendasi

### 🔴 Kesalahan Kritis (perlu diperbaiki)

| No | Soal | Masalah |
|---|---|---|
| 10 | Block vs Inline | Menggunakan `<diskon>` (unknown tag) alih-alih `<span>` |
| 27 | Hidden Input | Menggunakan `type="text"` bukan `type="hidden"`, field terlihat oleh pengguna |

### 🟡 Peringatan Sedang (perlu diperhatikan)

| No | Soal | Masalah |
|---|---|---|
| 9 | Nested List | Teks `"Kendaraan"` sebagai text node langsung di `<ul>` (invalid HTML, harus dalam `<li>`) |
| 11 | Gambar Responsif | Nama file `Indonesia Nature.jpg` tidak sesuai spesifikasi `pemandangan.jpg` |
| 13 | Audio | MIME type `audio/weba` salah (seharusnya `audio/webm`), nama file tidak sesuai |
| 17 | Tabel Semantik | Nilai `rowspan` tidak logis pada thead dan tfoot |
| 23 | Validasi Form | `required` adalah boolean attribute, tidak menerima custom string |
| 23 & 25 | Form | Duplikasi `id` antara input dan button (invalid HTML) |

### 🟢 Yang Dikerjakan dengan Baik

- Penguasaan dasar HTML5 boilerplate (soal 1)
- Penggunaan semantic formatting tags (soal 3)
- HTML Entities (soal 4)
- Anchor navigation / bookmark (soal 7)
- Radio button mutual exclusive (soal 22)
- Date picker dengan min/max (soal 24)
- Regex pattern validation pada input tel (soal 28)
- Accordion native HTML tanpa JavaScript (soal 19)
- Video autoplay muted (soal 14)

---

> *Penilaian ini bersifat objektif berdasarkan kesesuaian terhadap spesifikasi soal, validitas HTML5, dan kelengkapan constraint yang diberikan.*