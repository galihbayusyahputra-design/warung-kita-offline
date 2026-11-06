# Warung Kita — Kasir Offline 1 HP Android

Aplikasi kasir PWA tanpa akun, server database, atau langganan. Semua produk, foto, stok dan transaksi disimpan di IndexedDB pada perangkat/browser yang sama. Tidak sinkron ke HP lain.

## Isi paket
- `index.html` — tampilan
- `app.js` — fungsi produk, kasir, riwayat, backup/restore
- `sw.js` — cache offline
- `manifest.webmanifest` — instalasi PWA
- `icon.svg` — ikon aplikasi

## Cara paling mudah memasang (GitHub Pages)
1. Buat akun di https://github.com.
2. Buat repository baru bernama `warung-kita-offline`. Pilih **Public** agar GitHub Pages gratis dapat dipakai (file sumber aplikasi akan publik; jangan masukkan data pribadi atau backup).
3. Di repository, pilih **Add file > Upload files**. Upload kelima file aplikasi di atas dari folder hasil ekstrak (README opsional). Pastikan `index.html` ada di root repository. Klik **Commit changes**.
4. Buka **Settings > Pages**, pilih **Deploy from a branch**, branch **main**, folder **/(root)**, lalu **Save**.
5. Tunggu beberapa menit. Alamat akan berupa `https://USERNAME.github.io/warung-kita-offline/` (ganti USERNAME dengan username GitHub).
6. Di HP Android, buka URL tersebut di Chrome. Menu tiga titik > **Add to Home screen** / **Install app** > Install.
7. Buka ikon Warung Kita dari layar utama. Buka menu **Produk**, tambah barang dan foto, lalu gunakan menu **Kasir**.
8. Untuk menguji offline, buka aplikasi saat online setidaknya sekali hingga seluruh file termuat, lalu aktifkan mode pesawat dan buka lagi.

## Backup data (WAJIB)
- Menu **Backup > Download Backup**. File `.json` berisi semua produk, foto, stok dan riwayat transaksi.
- Simpan file di Google Drive atau penyimpanan eksternal. Backup setiap selesai jualan atau setidaknya tiap hari.
- Restore: pilih file backup pada menu Backup, lalu klik Restore Data. **Restore mengganti seluruh data yang ada**, tidak menggabungkan.
- Jangan hapus data situs Chrome / penyimpanan aplikasi, dan jangan uninstall sebelum backup. Data tidak otomatis pindah saat ganti HP.
- Hindari membuka aplikasi dari URL berbeda karena tiap origin memiliki data lokal sendiri.

## Penting
- Internet diperlukan saat pertama kali membuka dan memasang aplikasi; setelah aset tersimpan, aplikasi bisa dipakai offline.
- Aplikasi tidak mengirim transaksi ke server, tidak mempunyai login, dan tidak sinkron antarperangkat.
- Tidak ada cetak struk, pembayaran QRIS, laporan laba, maupun pengembalian barang di versi ini.
- Sebelum digunakan sungguhan, uji tambah/edit/hapus produk, checkout, peringatan stok <=10, backup, restore dan mode pesawat.
- Hosting file aplikasi di GitHub Pages tidak berarti data warung dipublikasikan; data produk/penjualan tersimpan lokal. Namun **jangan unggah file backup** ke repository publik.
