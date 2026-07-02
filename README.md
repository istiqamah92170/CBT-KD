# CBT Kabut Digital — PWA Package
Dibuat oleh **PWA Converter Engine v2.0** pada 3 Juli 2026

## Struktur File
```
/
├── index.html       ← Halaman utama (sudah dimodifikasi untuk PWA)
├── manifest.json    ← Web App Manifest
├── sw.js            ← Service Worker
├── offline.html     ← Halaman fallback offline
├── README.md        ← Panduan ini
└── icons/
    ├── icon-72.png
    ├── icon-96.png
    ├── icon-128.png
    ├── icon-144.png
    ├── icon-152.png
    ├── icon-192.png  ← Maskable
    ├── icon-384.png
    └── icon-512.png  ← Maskable
```

## Cara Deploy

### Netlify (Paling Mudah)
1. Buka https://app.netlify.com/drop
2. Drag & drop folder ini → Selesai! HTTPS otomatis aktif.

### Vercel
1. Buat akun di vercel.com
2. Drag & drop folder ke dashboard Vercel

### GitHub Pages
1. Upload semua file ke repository GitHub
2. Settings → Pages → Aktifkan

### Hosting Biasa
1. Upload ke public_html via FTP/cPanel
2. Pastikan SSL/HTTPS aktif

## Persyaratan PWA
- ✅ HTTPS wajib (untuk Service Worker)
- ✅ manifest.json harus dapat diakses
- ✅ Ikon 192×192 dan 512×512 → sudah ada
- ✅ Service Worker → sudah ada di sw.js

## Strategi Cache: stale-while-revalidate
Tampilkan cache instan, perbarui di background. Keseimbangan kecepatan & kebaruan.

## Tes PWA
- Chrome DevTools → Application → Manifest
- Chrome DevTools → Lighthouse → Generate report → PWA
