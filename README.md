# UTANG VOUCHER — Catatan Utang Voucher

Versi baru menghapus nama teman dan preview per teman. Setiap transaksi memperoleh ID otomatis seperti `TRX-0001`.

## Firebase
Konfigurasi Firebase bawaan dari project sebelumnya tetap digunakan di `index.html`.
Pastikan Authentication Email/Password aktif dan akun admin sudah dibuat.

## Firestore Rules
Ganti UID admin pada `firestore.rules` dengan UID akun admin dari Firebase Authentication, lalu Publish.

## Fitur
- Dashboard ringkasan utang, pembayaran, sisa, dan transaksi lunas.
- ID transaksi otomatis.
- Catat transaksi voucher dan pembayaran berdasarkan ID transaksi.
- Status lunas/berjalan, pencarian, filter, dan riwayat.
- Kelola harga voucher.
- Ekspor CSV dan backup/impor JSON.
- Tampilan responsif untuk Android.

## Migrasi data lama
Saat pertama kali login, aplikasi akan mencoba menambahkan ID transaksi ke data lama yang masih memiliki kolom `friend`, lalu pembayaran lama dihubungkan ke transaksi pertama yang cocok. Data lama tidak dihapus. Jika satu nama lama memiliki beberapa transaksi terpisah, pembayaran lama tidak dapat dipastikan pembagiannya secara otomatis; periksa hasil migrasi sebelum mengandalkannya.

## Hosting
Unggah `index.html` ke folder publik hosting (misalnya root repository GitHub Pages atau folder `public` Vercel). Jalankan melalui HTTPS.
