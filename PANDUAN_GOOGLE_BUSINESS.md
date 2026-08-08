# Panduan: Daftarkan Bantuin ke Google Maps & Search Engine

Semua konten sudah disiapkan siap copy-paste. Ini yang perlu **Anda eksekusi
sendiri** (butuh login akun Google pribadi + verifikasi kepemilikan bisnis),
saya sudah siapkan semua isiannya supaya tinggal klik-klik.

---

## BAGIAN 1 — Google Business Profile (Muncul di Google Maps)

### Langkah 1: Buat Profil
1. Buka **[google.com/business](https://www.google.com/business/)**
2. Login pakai akun Google Anda (sebaiknya akun yang akan terus dipegang, bukan akun pribadi yang jarang dicek)
3. Klik **"Kelola sekarang"** / **"Manage now"**

### Langkah 2: Isi Data Bisnis (Copy-Paste Ini)

| Field | Isi |
|---|---|
| **Nama bisnis** | `Bantuin` |
| **Kategori utama** | `Handyman` atau `Home repair service` |
| **Kategori tambahan** | `Furniture assembly service`, `Air conditioning repair service` |
| **Alamat** | Alamat operasional Anda (kalau kerja dari rumah tanpa toko fisik, pilih opsi "Saya melayani pelanggan di lokasi mereka" / "I deliver goods and services to my customers") |
| **Area layanan** | BSD, Serpong, Tangerang Selatan (sesuaikan area asli Anda) |
| **Nomor telepon** | `0811-7255-11` |
| **Website** | URL situs Bantuin Anda (setelah live di Render) |
| **Jam operasional** | Sesuaikan jam kerja tim Anda |

### Langkah 3: Deskripsi Bisnis (Copy-Paste Langsung)

```
Satu tukang, semua beres. Bantuin bantu urus rakit furniture, servis AC, sampai perbaikan rumah tangga lainnya — tanpa perlu cari tukang beda-beda tiap masalah. Harga transparan dari awal, teknisi berpengalaman & terverifikasi identitasnya. 150+ proyek, rating 4.8★. Chat WhatsApp sekarang, langsung dibantu.
```

### Langkah 4: Verifikasi (Wajib, Ini yang Bikin Profil Tampil Publik)

Google akan tawarkan salah satu metode ini (tergantung kategori bisnis Anda):

| Metode | Kecepatan | Cara |
|---|---|---|
| **Video** (tercepat, umum di 2026) | Instan-1 hari | Rekam video singkat tanpa putus: tunjukkan lokasi kerja, alat/perlengkapan teknisi, bukti Anda pemilik (misal buka pintu tempat usaha) |
| **SMS/Telepon** | Instan | Kalau tersedia, kode OTP dikirim ke nomor terdaftar |
| **Kartu Pos** | 1-2 minggu | Kode dikirim fisik ke alamat, lalu input manual di dashboard |

### Langkah 5: Upload Foto

Pakai foto-foto teknisi yang sudah kita buat untuk situs (`images/services/*.jpg` dan `images/*.jpg`) — upload minimal 5-10 foto. Bisnis dengan foto berkualitas dapat **42% lebih banyak** permintaan arah menurut data terbaru.

### Langkah 6: Setelah Aktif — Rutin Dilakukan

- Posting **Google Posts** (fitur gratis di dashboard GBP) tiap ada promo/update — sinyal ke Google bahwa bisnis "aktif"
- Minta customer kasih **rating & ulasan** setelah selesai kerja
- Response cepat kalau ada yang tanya lewat fitur chat GBP

---

## BAGIAN 2 — Search Engine (Google Search Console)

Ini yang bikin situs Bantuin muncul di hasil pencarian Google biasa (bukan cuma Maps). Saya sudah siapkan file teknisnya (`sitemap.xml`, `robots.txt`, dan meta description di tiap halaman) — tinggal submit.

### Langkah 1: Ganti Placeholder Domain

Di file `sitemap.xml` dan `robots.txt` yang saya buatkan, ganti semua tulisan:
```
GANTI-DENGAN-DOMAIN-BANTUIN-ANDA
```
dengan domain situs Bantuin Anda yang sebenarnya (misal `bantuin-site.onrender.com` atau domain custom kalau sudah punya).

### Langkah 2: Upload ke Root Repo

Upload `sitemap.xml` dan `robots.txt` ke **root folder** repo GitHub Bantuin (sejajar dengan `index.html`, bukan di dalam folder `css/` atau `images/`).

### Langkah 3: Daftar ke Google Search Console

1. Buka **[search.google.com/search-console](https://search.google.com/search-console)**
2. Login pakai akun Google yang sama dengan GBP
3. Klik **"Add Property"** → pilih **"URL prefix"** → masukkan URL situs Bantuin
4. Verifikasi kepemilikan — paling gampang pilih metode **"HTML tag"**: copy meta tag yang diberikan, tempel di `<head>` semua file HTML (saya bisa bantu tempelkan kalau Anda kirim tag-nya)
5. Setelah terverifikasi, buka menu **"Sitemaps"** di sidebar kiri
6. Masukkan: `sitemap.xml`, klik **Submit**

### Langkah 4: Request Indexing (Biar Cepat Muncul)

1. Di Search Console, pakai fitur **"URL Inspection"**
2. Masukkan URL homepage Bantuin
3. Klik **"Request Indexing"**
4. Ulangi untuk 3 halaman lain (jasa-rakit, servis-ac, serba-bisa)

Biasanya butuh beberapa hari sampai 2 minggu untuk muncul di hasil pencarian, tergantung seberapa "baru" domain-nya di mata Google.

---

## Kalau Mau Dibantu Klik Langsung (Bukan Cuma Panduan Teks)

Kalau Anda pakai **Claude for Chrome** (browsing agent dari Anthropic), saya bisa bantu **navigasi klik-klik**-nya langsung di browser Anda selama Anda yang login & selesaikan bagian verifikasi (video/SMS) yang memang harus dilakukan pemilik bisnis. Kabari kalau mau pakai cara ini.
