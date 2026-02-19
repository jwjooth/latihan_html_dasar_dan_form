# UJIAN AKHIR
## Mata Kuliah: HTML Dasar dan Form

| Keterangan | Detail |
|---|---|
| **Durasi** | 180 menit |
| **Sifat** | Open Book & Open Internet |
| **Format Jawaban** | File `.html` yang dapat dijalankan tanpa error di Web Browser |

---

## BAGIAN A — Dasar Markup & Hierarki Konten *(Easy to Medium)*

---

### Soal 1 — Struktur Dokumen HTML5

**Deskripsi Kasus:**
Konfigurasi kerangka dokumen utama merupakan hal esensial. Buat struktur dasar HTML5 yang mencakup tag root, meta charset, pengaturan viewport responsif, dan deklarasi favicon.

**Spesifikasi Input:**
- Teks judul tab: `"Ujian Akhir HTML"`
- URL favicon lokal: `assets/logo.png`

**Spesifikasi Output:**
File HTML yang merender halaman kosong secara valid di browser tanpa peringatan *missing charset* atau *viewport* di console.

**Constraint:**
- Harus menggunakan tag HTML5 yang valid.
- Favicon harus menggunakan atribut `rel` yang tepat.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Buka file di Chrome | Tab browser menampilkan teks `"Ujian Akhir HTML"` beserta logo ikon |

---

### Soal 2 — Hierarki Heading

**Deskripsi Kasus:**
Mesin pencari sangat memperhatikan hierarki Heading untuk memahami struktur dokumen. Implementasikan struktur heading berlapis untuk sebuah artikel blog.

**Spesifikasi Input:**
- Judul Utama: `"Belajar Pemrograman"`
- Sub-Judul: `"Bahasa Web"`
- Sub-Sub-Judul: `"HTML Dasar"`

**Spesifikasi Output:**
Rendering teks dengan ukuran menurun sesuai tingkatan prioritas semantik `H1`, `H2`, dan `H3`.

**Constraint:**
- Tidak boleh menggunakan tag kapitalisasi gaya lama seperti `<font>`.
- `H1` hanya boleh berjumlah **satu** buah.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Teks mentah artikel | Judul utama memiliki cetak tebal dan ukuran terbesar secara bawaan browser |

---

### Soal 3 — Pemformatan Teks Semantik

**Deskripsi Kasus:**
Pemformatan teks semantik (*Formatting*) digunakan untuk memberikan makna khusus pada kata tertentu di dalam paragraf, bukan sekadar gaya visual.

**Spesifikasi Input:**
```
"Harga normal adalah 10.000, kini menjadi 5.000. H2O adalah rumus air."
```

**Spesifikasi Output:**
- Angka `10.000` → tercoret
- Angka `5.000` → diberi garis bawah
- Angka `2` pada `H2O` → berada di bawah garis teks (*subscript*)

**Constraint:**
- Dilarang menggunakan CSS.
- Wajib menggunakan semantic formatting tags: `<del>`, `<ins>`, `<sub>`.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Teks plain string | Harga ~~10.000~~ <u>5.000</u>. H₂O |

---

### Soal 4 — HTML Entities

**Deskripsi Kasus:**
Browser akan menerjemahkan karakter khusus `<` dan `>` sebagai pembuka/penutup tag. Selesaikan masalah ini menggunakan HTML Entities.

**Spesifikasi Input:**
```
<h1>Selamat Datang</h1>
```

**Spesifikasi Output:**
Browser menampilkan teks persis seperti input, **bukan** mencetak teks `"Selamat Datang"` dengan gaya heading besar.

**Constraint:**
Gunakan Entity code yang tepat, bukan tag pembungkus biasa.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Pengembang mengetik sintaks HTML di dalam file HTML | Layar web menampilkan tulisan `<h1>Selamat Datang</h1>` |

---

### Soal 5 — Blok Kode Preformatted

**Deskripsi Kasus:**
Kode komputer harus ditampilkan apa adanya untuk mempertahankan spasi, indentasi, dan garis baru tanpa ternormalisasi oleh browser.

**Spesifikasi Input:**
```python
def salam():
    print("Halo")
```

**Spesifikasi Output:**
Blok teks yang mempertahankan jarak indentasi 4 spasi di depan kata `print`.

**Constraint:**
Wajib menggunakan *computer code tag* yang spesifik.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Tiga baris kode Python | Teks ter-render dengan font monospaced dan format indentasi terjaga |

---

### Soal 6 — Hyperlink Internal & Eksternal

**Deskripsi Kasus:**
Hyperlink dapat merujuk ke URL di luar maupun di dalam ekosistem domain saat ini.

**Spesifikasi Input:**
- Link 1: menuju `https://niagahoster.co.id/` → buka di **tab baru**
- Link 2: menuju file internal `kontak.html` → buka di **tab yang sama**

**Spesifikasi Output:**
Dua tautan biru bergaris bawah. Klik link pertama membuka tab baru, klik link kedua me-load di tab saat ini.

**Constraint:**
Gunakan format penulisan **Absolute URL** dan **Relative URL** yang tepat.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Tag `<a>` | Link 1 men-trigger pop-up tab baru |

---

### Soal 7 — Bookmark / Anchor Navigation

**Deskripsi Kasus:**
Untuk halaman yang sangat panjang, diperlukan sistem navigasi lompat cepat menggunakan Bookmark.

**Spesifikasi Input:**
- Menu tautan: `"Ke Bawah"`
- Sebuah elemen `div` di baris ke-500 dengan identifier `"footer"`

**Spesifikasi Output:**
Tautan di bagian atas web, ketika diklik, halaman otomatis menggulung ke elemen target di bawah.

**Constraint:**
Implementasikan atribut `id` dan `href` dengan prefix `#`.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Klik teks `"Ke Bawah"` | Layar browser bergeser langsung ke ID `"footer"` |

---

### Soal 8 — Ordered List dengan Tipe Huruf

**Deskripsi Kasus:**
Daftar yang diurutkan dapat memodifikasi gaya numbering-nya tanpa campur tangan CSS.

**Spesifikasi Input:**
Daftar pemenang lomba: Budi, Andi, Siti.

**Spesifikasi Output:**
Urutan menggunakan format huruf kapital (A, B, C) bukan angka numerik.

**Constraint:**
Manipulasi atribut `type` pada tag `<ol>`.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| 3 buah list item | `A. Budi`, `B. Andi`, `C. Siti` |

---

### Soal 9 — Nested List

**Deskripsi Kasus:**
Pengelompokan data logis dapat dilakukan melalui list bersarang.

**Spesifikasi Input:**
- Kategori: `"Kendaraan"`
- Sub-kategori (bullet): `"Mobil"` dan `"Motor"`

**Spesifikasi Output:**
Format list bullet utama berisi teks `"Kendaraan"`, dan di bawahnya terdapat indentasi untuk list bullet kedua.

**Constraint:**
Wajib menggunakan `<ol>` atau `<ul>` bersarang.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Induk list dan anak list | Render hierarki berjenjang bawaan dari browser |

---

### Soal 10 — Block vs Inline Element

**Deskripsi Kasus:**
Layout visual dan pengelompokan tingkat tinggi dalam HTML membedakan perilaku *Block* dan *Inline*.

**Spesifikasi Input:**
Kalimat `"Harga Diskon"` di mana kata `"Diskon"` harus dapat diseleksi/ditarget tanpa memaksa baris baru.

**Spesifikasi Output:**
Kata `"Harga"` dan `"Diskon"` tetap berada di baris horizontal yang sama.

**Constraint:**
- Kata `"Diskon"` wajib dibungkus dalam tag yang bersifat **inline**.
- Dilarang menggunakan tag *block*.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Dua kata dalam struktur DOM | Tidak terpotong ke bawah |

---

## BAGIAN B — Multimedia, Tabel & Semantik *(Medium)*

---

### Soal 11 — Gambar Responsif

**Deskripsi Kasus:**
Gambar harus responsif terhadap viewport induknya secara relatif, serta memiliki kriteria aksesibilitas.

**Spesifikasi Input:**
- File gambar: `pemandangan.jpg`
- Teks layar baca: `"Foto Pantai"`

**Spesifikasi Output:**
Gambar ditampilkan dengan lebar selalu memenuhi **setengah layar** browser.

**Constraint:**
- Gunakan properti persentase `%` pada lebar.
- Lengkapi tag pelengkap teks disabilitas (`alt`).

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Ukuran browser diperkecil/di-resize | Gambar otomatis mengecil mengikuti lebar 50% |

---

### Soal 12 — Responsive Image dengan `<picture>`

**Deskripsi Kasus:**
Optimalisasi load gambar berbasis ukuran layar (*Art Direction*) diselesaikan menggunakan tag `<picture>`.

**Spesifikasi Input:**
- Layar `< 500px` → memuat `kucing-kecil.png`
- Layar standar → memuat `kucing-besar.png`

**Spesifikasi Output:**
Peramban cerdas merender file yang relevan sesuai media query.

**Constraint:**
- Gunakan sintaks `<source media="...">`.
- Sediakan tag default gambar (fallback).

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Inspect element di mobile view | File `kucing-kecil.png` yang terunduh di network tab |

---

### Soal 13 — Audio Multi-Format

**Deskripsi Kasus:**
Memutar media audio yang kompatibel dengan multi-browser secara fallback.

**Spesifikasi Input:**
File: `lagu.webm` dan `lagu.mp3`

**Spesifikasi Output:**
Pemutar audio yang dapat diputar-jeda oleh pengguna (memiliki UI tombol play).

**Constraint:**
- Tidak boleh auto-play.
- Wajib mencantumkan lebih dari satu format *source*.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Tag audio dirender | UI Control bar suara muncul di browser |

---

### Soal 14 — Video Autoplay Muted

**Deskripsi Kasus:**
Video yang di-embed membutuhkan serangkaian aturan UX spesifik.

**Spesifikasi Input:**
- URL: `trailer.mp4`
- Ukuran lebar: `800px`

**Spesifikasi Output:**
Frame video muncul, langsung berputar otomatis saat halaman dimuat, namun dalam kondisi *mute* (tanpa suara).

**Constraint:**
Eksplorasi atribut boolean spesifik pada tag `<video>`.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Buka halaman | Video bergerak tanpa suara |

---

### Soal 15 — Embed YouTube via Iframe

**Deskripsi Kasus:**
Iframe digunakan untuk menanamkan dokumen eksternal seperti YouTube.

**Spesifikasi Input:**
URL YouTube embed: `https://www.youtube.com/embed/xyz`

**Spesifikasi Output:**
Bingkai dimensi `500x500` menampilkan konten dari server YouTube di dalam halaman.

**Constraint:**
Wajib menggunakan atribut iframe yang valid.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Kode HTML disisipkan | Player YouTube fungsional di lokal layar |

---

### Soal 16 — Tabel dengan Rowspan

**Deskripsi Kasus:**
Tabel kompleks seringkali membutuhkan manipulasi baris untuk data repetitif. Gabungkan sel secara vertikal.

**Spesifikasi Input:**
- Header kolom: `"Divisi"`, `"Nama"`
- Baris 1: IT, Budi
- Baris 2: IT, Joko

**Spesifikasi Output:**
Sel kata `"IT"` menyatu membentang ke bawah untuk mengapit Budi dan Joko.

**Constraint:**
Gunakan properti `rowspan` yang terhitung benar.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Tabel statis | Border tabel menembus 2 tinggi baris di kolom Divisi |

---

### Soal 17 — Tabel dengan `<thead>`, `<tbody>`, `<tfoot>`

**Deskripsi Kasus:**
Struktur tabel enterprise wajib membedakan ruang lingkup data header, badan, dan catatan kaki.

**Spesifikasi Input:**
Kolom judul, baris rincian barang, dan baris `"Total Biaya"`.

**Spesifikasi Output:**
Struktur DOM yang bersih. Meskipun letak `<tfoot>` ditulis di tengah struktur DOM, browser tetap merendernya di posisi akhir bawah tabel.

**Constraint:**
Wajib membungkus *rows* menggunakan tag `<thead>`, `<tbody>`, dan `<tfoot>`.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Elemen `tfoot` didefinisikan | Posisi total stabil di paling bawah susunan data |

---

### Soal 18 — Gambar Semantik dengan `<figure>` dan `<figcaption>`

**Deskripsi Kasus:**
Konten ilustrasi harus dapat berdiri sendiri beserta keterangannya dan tidak terpisahkan secara semantik.

**Spesifikasi Input:**
- File gambar: `grafik.jpg`
- Teks keterangan: `"Grafik Penjualan 2025"`

**Spesifikasi Output:**
Browser mendeteksi kesatuan gambar dan teks secara semantis.

**Constraint:**
- Hindari penggunaan `<div class="gambar">`.
- Gunakan dua tag semantik HTML5 khusus gambar dan caption.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Tag pembungkus | Screen reader membaca relasi gambar dan caption-nya |

---

### Soal 19 — Accordion Tanpa JavaScript

**Deskripsi Kasus:**
Implementasikan tag interaktif bawaan browser untuk antarmuka *Accordion/Toggle* tanpa bantuan JavaScript.

**Spesifikasi Input:**
- Judul klik: `"Baca Syarat"`
- Teks isi: `"Anda harus patuh aturan."`

**Spesifikasi Output:**
Teks isi tersembunyi secara default. Muncul hanya saat tulisan `"Baca Syarat"` diklik.

**Constraint:**
Gunakan tag `<details>` beserta elemen pendukungnya.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Klik pada panah kecil | Kotak membesar, teks rahasia terekspos |

---

### Soal 20 — Konfigurasi Form Action & Method

**Deskripsi Kasus:**
Form membutuhkan definisi spesifik ke mana data disalurkan dan bagaimana metodologinya.

**Spesifikasi Input:**
- Form profil pengguna
- Target URL pengiriman: `/submit-profile`
- Mode transfer: via Payload Body (tidak terekspos di URL bar)

**Spesifikasi Output:**
Objek form yang terhubung.

**Constraint:**
Sesuaikan nilai atribut `action` dan `method` dengan tepat.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Tombol Submit form ditekan | Browser memposting request body (POST) ke path `/submit-profile` |

---

## BAGIAN C — Lanjutan HTML Form & Input *(Medium to Hard)*

---

### Soal 21 — Label & Input Aksesibel

**Deskripsi Kasus:**
Aksesibilitas interaktif form sangat bergantung pada teks penanda (Label) yang terkait secara persis ke inputnya.

**Spesifikasi Input:**
Teks `"Klik Saya"`, diikuti oleh elemen input teks.

**Spesifikasi Output:**
Ketika kursor mengklik persis di atas teks `"Klik Saya"`, elemen input teks di sebelahnya langsung terfokus dan kursor berkedip di dalamnya.

**Constraint:**
- Wajib menggunakan atribut `for` pada Label yang **sama identik** dengan atribut `id` pada Input.
- Dilarang hanya sekadar membungkus input di dalam label.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| User klik pada Label teks | Input box menjadi *active/focused* |

---

### Soal 22 — Radio Button Mutual Exclusive

**Deskripsi Kasus:**
Sistem formulir pilihan ganda di mana pengguna secara mutlak hanya boleh memilih **satu** opsi tunggal (*Mutual Exclusive*).

**Spesifikasi Input:**
Opsi pembayaran: `"Kartu Kredit"`, `"Transfer Bank"`, `"E-Wallet"`

**Spesifikasi Output:**
Tiga bulatan opsi. Memilih opsi satu akan me-reset ceklis pada opsi yang sudah dipilih sebelumnya.

**Constraint:**
- Wajib menggunakan input radio.
- Kunci utamanya adalah atribut `name` harus di-set sama pada semua opsi.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Klik Radio 1, lalu klik Radio 2 | Status *checked* pindah ke Radio 2, Radio 1 kosong |

---

### Soal 23 — Validasi Form HTML5 Native

**Deskripsi Kasus:**
Pembuatan formulir registrasi membutuhkan validasi pengisian di sisi front-end sebelum dikirimkan ke server.

**Spesifikasi Input:**
Kotak input alamat Email.

**Spesifikasi Output:**
Jika kosong dan tombol daftar ditekan, peramban menampilkan alert balon pop-up: *"Please fill out this field"*. Format juga harus berjenis email yang valid.

**Constraint:**
Terapkan atribut validasi bawaan HTML5 dan tipe spesifik input.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Input di-kosongkan dan di-submit | Event pengiriman form digagalkan browser dan error ter-trigger |

---

### Soal 24 — Date Picker dengan Batasan Rentang

**Deskripsi Kasus:**
Batasi kebebasan memilih pengguna pada kalender agar jadwal yang tidak masuk akal tidak direkam sistem.

**Spesifikasi Input:**
- Input untuk jadwal `"Pemesanan Tiket"`
- Rentang yang diizinkan: `2026-05-01` s.d. `2026-05-31`

**Spesifikasi Output:**
Elemen *Date-Picker* muncul. Tanggal di luar batasan akan tampak redup (*greyed-out*) dan tidak bisa diseleksi.

**Constraint:**
Manfaatkan kombinasi atribut `min` dan `max` spesifik pada tipe `date`.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| User klik ikon kalender, bulan Juni terbuka | Tidak ada opsi tanggal bulan Juni yang dapat ditekan |

---

### Soal 25 — File Upload dengan Enctype

**Deskripsi Kasus:**
Mengunggah berkas multimedia memerlukan perubahan krusial pada deklarasi parameter Form.

**Spesifikasi Input:**
Form dengan satu tombol unggah dokumen (file chooser).

**Spesifikasi Output:**
Jendela eksplorer lokal komputer terbuka jika di klik. Data biner dikemas dan dikirim tuntas secara mutlak utuh.

**Constraint:**
- Form pengunggah wajib mengatur konfigurasi `enctype` secara presisi.
- Tipe form method harus tepat.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Pilih foto `"KTP.png"`, Submit | Payload HTTP yang ter-request via `multipart/form-data` |

---

### Soal 26 — Autocomplete dengan `<datalist>`

**Deskripsi Kasus:**
Tampilan dropdown opsi pilihan konvensional kurang fungsional jika opsinya sangat panjang. Fitur rekomendasi (*Autocomplete*) memecahkan masalah ini.

**Spesifikasi Input:**
- Kotak teks: `"Asal Sekolah"`
- Data rekomendasi: `"SDN 1"`, `"SMP 2"`, `"SMA 3"`

**Spesifikasi Output:**
Saat user mulai mengetik huruf `"S"`, kotak teks memunculkan ketiga saran *dropdown* list yang bisa diseleksi.

**Constraint:**
Gunakan tag relasional `<datalist>` dengan koneksi ID.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Ketik `"SMA"` pada kolom | Rekomendasi `"SMA 3"` mem-filter dan dapat langsung diklik masuk |

---

### Soal 27 — Hidden Input Field

**Deskripsi Kasus:**
Terkadang server mewajibkan pencantuman *tracking identifier* yang disisipkan di Form secara tersembunyi, agar tidak merusak antarmuka pengguna.

**Spesifikasi Input:**
- Parameter: `token_id`
- Nilai default: `ABX123`

**Spesifikasi Output:**
Tidak terlihat kotak apapun pada antarmuka web. Namun parameter dikirim secara pasif saat *form submission*.

**Constraint:**
Implementasikan atribut input `type` dan nilai default yang tepat.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| User klik form submit | URL/Body Payload menyertakan `&token_id=ABX123` tanpa user input secara manual |

---

### Soal 28 — Validasi Pattern Regex pada Input Tel

**Deskripsi Kasus:**
Format nomor telepon secara internasional bervariasi luas. Klien ini mengharuskan format statis angka telepon sepanjang **11 hingga 13 digit**. Validasi menggunakan Regex murni HTML.

**Spesifikasi Input:**
Box isian nomor kontak darurat.

**Spesifikasi Output:**
Jika input memuat selain rentang angka (misal `"ab123"` atau 9 angka saja), HTML mencegah submission.

**Constraint:**
- Tambahkan pola Regular Expression di dalam atribut `pattern` pada input type `tel`.
- *Hint: Pattern Regex numerik berantai.*

**Contoh Input/Output:**

| Input | Output |
|---|---|
| `"08123456789"` | Valid sukses |
| `"ab123"` atau 9 digit | Submission dicegah browser |

---

### Soal 29 — Grouping Form dengan `<fieldset>` dan `<legend>`

**Deskripsi Kasus:**
Pengelompokan visual dan fungsional bagian form wajib menggunakan kotak penegas batas border.

**Spesifikasi Input:**
- Satu blok grup berjudul `"Informasi Detail"`
- Di dalamnya memuat 1 input textbox

**Spesifikasi Output:**
Kotak garis tepi melingkari inputan teks, dan di garis tepi bagian atas menyempil teks menyatu `"Informasi Detail"`.

**Constraint:**
- Tag `div` / CSS dilarang digunakan.
- Wajib menggunakan tag Semantic HTML5 Form untuk mengikat elemen.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Struktur Tag Grouping dan Tag Judul Grouping | UI form terkotak-kotak secara rapi |

---

### Soal 30 — Slider Range dengan Step Diskrit

**Deskripsi Kasus:**
Elemen kontrol input angka Slider dapat diinstruksikan untuk tidak bergerak bebas secara inkremental, melainkan melompat nilai mutlak yang ditetapkan (misal slider volume melompat per 25%).

**Spesifikasi Input:**
- Slider indikator
- Range: `0` sampai maksimum `100`

**Spesifikasi Output:**
Saat slider digeser, nilainya hanya dapat berhenti di titik loncatan diskrit: **0, 25, 50, 75, 100**. Slider tidak akan pernah bernilai `"13"` atau `"30"`.

**Constraint:**
Pemanfaatan ketat atribut `step` pada konfigurasi tag `range`.

**Contoh Input/Output:**

| Input | Output |
|---|---|
| Klik slider lalu drag 1mm ke kanan | Poin slider langsung "meloncat" menempel di 25 |

---

> **Selamat Mengerjakan.**
> Pastikan seluruh logika Form Validation HTML terapan mampu berjalan sempurna **tanpa intervensi JavaScript sedikitpun**.
