# MAMZZ PROJECT X Marketplace

Website katalog layanan digital berbasis React + Vite.

## Jalankan di komputer / lingkungan Node.js
```bash
npm install
npm run dev
```

## Build untuk Netlify
- Build command: `npm run build`
- Publish directory: `dist`
- Base directory: kosong

## Pengaturan wajib sebelum publikasi
1. Buka `src/App.jsx`.
2. Ganti `WHATSAPP_NUMBER` dengan nomor WhatsApp bisnis yang benar, format internasional tanpa `+`. Contoh Indonesia: `628xxxxxxxxxx`.
3. Periksa ulang semua nama layanan, harga, deskripsi, kontak, kebijakan, dan ketentuan toko. Pastikan hanya memuat produk/jasa yang benar-benar tersedia dan legal.
4. Jangan menambahkan klaim pembayaran otomatis sebelum integrasi resmi selesai.

## Status pembayaran
Website ini saat ini adalah katalog dan sistem pengiriman ringkasan pesanan ke admin. Website BELUM memproses pembayaran, belum membuat QRIS dinamis, dan belum memverifikasi transaksi. Untuk pembayaran otomatis diperlukan akun merchant yang disetujui penyedia pembayaran, backend aman, webhook, dan database.

Jangan pernah meletakkan API secret/private key di React, `App.jsx`, atau repository GitHub. Simpan rahasia hanya di environment variables backend.

## Halaman dan kebijakan
Katalog, cara pemesanan, kontak, kebijakan layanan/pengembalian dana, dan privasi dasar sudah disediakan. Sesuaikan semuanya dengan praktik bisnis sebenarnya sebelum mengirim URL untuk verifikasi merchant.