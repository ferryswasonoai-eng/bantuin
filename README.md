# Bantuin — Reliable Home Services

Situs statis (tanpa backend, tanpa database) untuk layanan jasa rumah
tangga: **Jasa Rakit Furniture**, **Servis AC & Elektronik**, dan
**Jasa Serba Bisa (Handyman)**.

## Struktur File

```
├── index.html          # Landing page
├── jasa-rakit.html      # Halaman Jasa Rakit Furniture
├── servis-ac.html       # Halaman Servis AC
├── serba-bisa.html      # Halaman Jasa Serba Bisa
├── css/
│   └── style.css
├── images/
│   ├── logo-bantuin.png
│   ├── handyman.jpg
│   ├── rakit-furniture.jpg
│   └── servis-ac.jpg
└── README.md
```

## Cara Deploy ke GitHub

1. Buat repo baru di GitHub, misal `bantuin-site`
2. Upload semua file & folder di sini (pertahankan struktur folder `css/` dan `images/` persis seperti di atas)
3. Commit & push

## Cara Deploy ke Render (Static Site)

1. Buka [dashboard.render.com](https://dashboard.render.com)
2. **New > Static Site**
3. Connect ke repo GitHub `bantuin-site`
4. Isi:
   - **Build Command**: kosongkan (tidak perlu)
   - **Publish Directory**: `.` (root)
5. Klik **Create Static Site**
6. Tunggu ~30-60 detik, situs langsung online

> ⚠️ Pastikan pilih tipe **Static Site**, bukan **Web Service** — karena
> situs ini murni HTML/CSS tanpa server/backend. Kalau salah pilih Web
> Service, deploy akan gagal karena Render akan coba jalankan `npm install`
> padahal tidak ada `package.json`.

## Cara Ganti Nomor WhatsApp

Nomor `62811725511` muncul di beberapa tempat di tiap file HTML (header,
tombol CTA per halaman, footer). Cara tercepat ganti semua sekaligus:

**Kalau pakai VS Code / editor kode:** gunakan fitur **Find & Replace in
Files** (Ctrl+Shift+H di VS Code), cari `62811725511`, ganti dengan nomor
baru (format: kode negara tanpa `+` atau `0` di depan).

## Cara Update Harga / Teks

Semua harga & deskripsi ditulis langsung di HTML (tidak ada database),
jadi edit langsung di file terkait:
- Harga rakit furniture → `jasa-rakit.html`, bagian `<table class="price-table">`
- Harga servis AC → `servis-ac.html`, bagian `<table class="price-table">`
- Harga & daftar sub-layanan handyman → `serba-bisa.html`, bagian `.subservice-grid`

## Menambah Halaman Layanan Baru

1. Duplikat salah satu file halaman layanan yang ada (misal `jasa-rakit.html`) sebagai starting point
2. Ganti konten (judul, harga, deskripsi) sesuai layanan baru
3. Tambahkan link ke halaman baru itu di dropdown menu "Services" — ada di
   **setiap file HTML** (index.html, jasa-rakit.html, servis-ac.html,
   serba-bisa.html) karena dropdown-nya di-duplikasi manual, bukan
   komponen shared. Cari blok ini di tiap file:
   ```html
   <div class="dropdown-menu">
     <a href="jasa-rakit.html">🪑 Jasa Rakit</a>
     <a href="servis-ac.html">❄️ Servis AC</a>
     <a href="serba-bisa.html">🔧 Serba Bisa</a>
   </div>
   ```
