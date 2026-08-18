# MITRA ROSOK Banyuwangi — Website

Website statis (HTML/CSS/JS murni, tanpa framework berat) untuk **MITRA ROSOK Banyuwangi**, siap deploy gratis ke GitHub Pages.

## 🚀 Cara Deploy ke GitHub Pages (Gratis)

1. Buat repository baru di GitHub, misal: `mitra-rosok-banyuwangi`.
2. Upload **seluruh isi folder ini** (bukan foldernya, tapi isinya) ke root repository tersebut.
   - Bisa lewat GitHub Desktop, web upload, atau `git`:
     ```
     git init
     git add .
     git commit -m "Initial website MITRA ROSOK Banyuwangi"
     git branch -M main
     git remote add origin https://github.com/USERNAME/mitra-rosok-banyuwangi.git
     git push -u origin main
     ```
3. Di GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main / (root)** → Save.
4. Tunggu 1-2 menit. Website akan aktif di:
   `https://USERNAME.github.io/mitra-rosok-banyuwangi/`
5. (Opsional) Jika punya domain sendiri, tambahkan file `CNAME` berisi domain Anda, lalu atur DNS sesuai panduan GitHub Pages.

File `.nojekyll` sudah disertakan agar GitHub Pages tidak memproses situs lewat Jekyll (memastikan semua file ter-serve apa adanya).

## ⚠️ WAJIB dilakukan sebelum go-live

### 1. Ganti placeholder `[DOMAIN WEBSITE]`
Setelah tahu URL final (GitHub Pages atau domain sendiri), ganti semua `[DOMAIN WEBSITE]` di seluruh file dengan URL tersebut (tanpa trailing slash), lewat find-and-replace di editor, atau jalankan (Linux/Mac/Git Bash):

```bash
find . -type f \( -name "*.html" -o -name "*.xml" -o -name "*.txt" \) \
  -exec sed -i 's#\[DOMAIN WEBSITE\]#https://USERNAME.github.io/mitra-rosok-banyuwangi#g' {} +
```

Sesuaikan `https://USERNAME.github.io/mitra-rosok-banyuwangi` dengan URL Anda yang sebenarnya (tanpa `/` di akhir).

### 2. Placeholder data bisnis
Alamat lengkap, link Google Maps, jam operasional (buka 24 jam setiap hari), Instagram, dan Facebook **sudah diisi** di seluruh halaman termasuk footer dan structured data. Tidak ada lagi yang perlu dilengkapi di bagian ini.

### 3. Upload foto asli
Semua foto masih berupa **placeholder path** (belum ada file gambar), karena instruksi awal melarang penggunaan foto stok. Siapkan foto asli usaha dalam format **WebP** dan simpan di `assets/images/` dengan nama file berikut (persis, agar otomatis muncul di halaman terkait):

- `mitra-rosok-banyuwangi-lokasi.webp`
- `mitra-rosok-banyuwangi-lokasi-usaha.webp`
- `mitra-rosok-banyuwangi-gudang.webp`
- `mitra-rosok-banyuwangi-penimbangan.webp`
- `mitra-rosok-banyuwangi-rongsokan-elektronik.webp`
- `mitra-rosok-banyuwangi-aktivitas.webp`
- `mitra-rosok-banyuwangi-kendaraan-pickup.webp`
- `mitra-rosok-banyuwangi-og.webp` (untuk Open Graph / preview link, ukuran disarankan 1200×630px)

Kompres gambar sebelum upload (misal lewat squoosh.app) agar tetap ringan.

## 📁 Struktur Folder

```
/
├── index.html                  (Beranda)
├── tentang-kami/
├── layanan/
├── jenis-barang/
├── cara-menjual/
├── area-layanan/
├── faq/
├── galeri/
├── kontak/
├── blog/
│   ├── index.html
│   └── [6 artikel]/
├── privacy-policy/
├── terms/
├── 404.html
├── assets/
│   ├── images/   (taruh foto asli di sini)
│   ├── icons/    (favicon.svg)
│   └── logo/     (mitra-rosok-logo.svg)
├── css/style.css
├── js/script.js
├── sitemap.xml
├── robots.txt
└── .nojekyll
```

## ✅ Yang sudah diimplementasikan

- Mobile-first, ringan, tanpa dependency eksternal (HTML/CSS/JS vanilla)
- Semantic HTML5 + heading hierarchy yang benar
- Meta title & description unik per halaman
- Open Graph & Twitter Card
- Canonical URL di setiap halaman
- Structured data JSON-LD: `LocalBusiness`, `WebSite`, `BreadcrumbList`, `Article`, `FAQPage`
- Sitemap.xml & robots.txt
- Semua link internal memakai path **relatif** (aman untuk GitHub Pages project page maupun domain sendiri)
- Sticky bottom navigation mobile (Beranda | Layanan | Lokasi | WhatsApp)
- Tombol WhatsApp mengambang + CTA WhatsApp dengan pesan otomatis
- FAQ AEO-friendly (jawaban langsung di kalimat pertama)
- 6 artikel blog awal (people-first, tidak keyword stuffing)
- Tidak ada klaim palsu, review palsu, atau data bisnis yang dikarang — semua bagian yang datanya belum tersedia memakai placeholder eksplisit

## 🔜 Rekomendasi setelah live

1. Daftarkan website ke **Google Search Console**, submit `sitemap.xml`.
2. Buat/klaim **Google Business Profile** untuk MITRA ROSOK Banyuwangi agar muncul di Google Maps, lalu tempel link Maps-nya ke placeholder `https://maps.app.goo.gl/EtnyF4SS6KmL5KtK6`.
3. Tambahkan foto asli secara bertahap — semakin banyak foto asli, semakin kuat sinyal trust.
4. Setelah ada review pelanggan asli, section "Pengalaman Pelanggan" bisa diisi secara manual.
5. Tambahkan artikel blog baru secara bertahap (jangan sekaligus banyak) mengikuti pola 6 artikel yang sudah ada.
