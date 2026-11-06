# Warung Kita V2 — Offline (Android/iPhone)

## Instalasi / pembaruan GitHub Pages
1. Ekstrak ZIP. Upload **keenam file** (`index.html`, `app.js`, `sw.js`, `manifest.webmanifest`, `icon.svg`, `README.md`) ke root repository `warung-kita-offline` yang sama, **mengganti** file versi lama. Jangan buat repository baru.
2. GitHub Pages: Settings > Pages > Deploy from a branch > main > /(root). Tunggu deployment selesai.
3. Buka URL GitHub Pages, refresh; bila versi lama masih tampil, tutup aplikasi dan buka kembali. Jika perlu bersihkan cache situs **tanpa menghapus data situs / storage**.
4. Di Android, Chrome > menu > Add to Home screen / Install app.

## Fitur
Kasir, foto produk, kategori, stok menipis <=10, riwayat, harga modal, laba kotor, dashboard harian, restok, pembayaran & kembalian, laporan bulanan CSV, backup JSON, restore. Checkout dan restok memakai transaksi IndexedDB.

## Backup dan keamanan
Semua data tetap berada di browser HP, **bukan di GitHub**. Backup rutin ke Google Drive. Restore mengganti seluruh data. Format backup V2 dapat mengimpor backup V1; backup V2 menyimpan produk, penjualan, dan riwayat restok. Data V1 di browser tetap dipakai otomatis karena nama database sama dan skema dinaikkan dari versi 1 ke 2. Harga modal produk lama default Rp0 sampai diisi; laporan laba lama tidak akurat tanpa harga modal historis.

## Uji sebelum operasional
Tambah produk (harga modal, harga jual, stok), lakukan checkout, cek kembalian, cek stok dan dashboard, restok, ekspor CSV, backup JSON, coba offline. Jangan gunakan untuk transaksi nyata sebelum seluruh uji berhasil.
