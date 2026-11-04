# MAMZZ PROJECT X MARKETPLACE

React + Vite marketplace prototype, mobile-friendly and deployable to Netlify.

## Jalankan dari komputer / terminal
1. Install Node.js versi LTS.
2. Buka folder project.
3. Jalankan `npm install`
4. Jalankan `npm run dev`
5. Untuk build: `npm run build`

## Pengaturan wajib sebelum dipublikasikan
Buka `src/App.jsx`, lalu ubah:
- `WA_NUMBER` menjadi nomor WhatsApp admin format internasional tanpa tanda `+`, contoh `628xxxxxxxxxx`.
- `BANK_DETAILS` menjadi rekening resmi milik toko.
- `QRIS_IMAGE` sudah disiapkan sebagai lokasi aset, tetapi UI demo saat ini mengarahkan admin memberikan QRIS setelah verifikasi. Jangan memakai QRIS palsu. Unggah QRIS resmi milik merchant melalui alur pembayaran yang aman.

## Deploy Netlify dari HP Android
Cara paling mudah:
1. Ekstrak ZIP ini menggunakan aplikasi pengelola file.
2. Buat akun / login Netlify melalui browser.
3. Buat repository GitHub dan unggah isi folder project (bukan file ZIP).
4. Di Netlify pilih **Add new site** > **Import an existing project** > GitHub.
5. Pilih repository.
6. Build command: `npm run build`
7. Publish directory: `dist`
8. Tekan **Deploy**. File `netlify.toml` juga sudah mengatur nilai tersebut.
9. Setelah deploy selesai, buka URL `.netlify.app` yang diberikan Netlify.

Alternatif tanpa Git:
1. Di HP, buka terminal online/cloud development yang mendukung Node.js, unggah dan ekstrak project.
2. Jalankan `npm install`, lalu `npm run build`.
3. Unggah folder `dist` ke Netlify melalui fitur deploy manual Netlify jika tersedia pada tampilan akun.

## Penting: batasan versi demo
- Produk, keranjang, dan pesanan disimpan di `localStorage` browser. Data tidak tersinkron antarperangkat dan bisa hilang jika data browser dihapus.
- Dashboard admin pada versi ini bukan sistem login aman. Jangan gunakan untuk mengelola transaksi nyata atau menyimpan data sensitif.
- Status pesanan yang diubah admin hanya berubah di browser/perangkat tersebut.
- Checkout membuka WhatsApp dengan rincian pesanan. Admin tetap harus memverifikasi pembayaran secara manual.
- Untuk operasional sungguhan, tambahkan backend/database, autentikasi admin di server, validasi stok dan harga di server, serta payment gateway/QRIS dinamis dari penyedia resmi. Jangan menyimpan secret key di React/frontend.
- Jual hanya produk dan layanan yang legal serta memiliki hak untuk ditawarkan. Jangan meminta atau menyimpan password, OTP, atau kredensial akun pelanggan.

## Struktur
- `src/App.jsx` — halaman toko, katalog, keranjang, checkout, dashboard demo
- `src/style.css` — tema responsif hitam-ungu
- `src/main.jsx` — entry React
- `netlify.toml` — konfigurasi deploy SPA
