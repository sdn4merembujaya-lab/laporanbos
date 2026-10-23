# Aplikasi Laporan BOS

Aplikasi web satu file untuk membuat dokumen pertanggungjawaban Dana BOS: BKU, kwitansi, invois, SPK, BAST, SPPD, surat tugas, dan daftar penerima honor.

## Cara pakai
1. Buka aplikasi (GitHub Pages) di browser.
2. Isi identitas sekolah dan penandatangan, lalu isi daftar pegawai.
3. Impor file RPD sekolah (.xlsx) di tab RPD.
4. Catat realisasi, lalu cetak dokumen yang diperlukan.

## Login Admin dan Bendahara
- Saat pertama dibuka, aplikasi meminta Anda membuat username dan password untuk Admin dan Bendahara. Tidak ada password bawaan.
- Admin: semua menu, termasuk Data Sekolah, Daftar Pegawai, impor RPD, pemulihan data, dan pengaturan akun.
- Bendahara: RPD dan Realisasi (tanpa impor), Transaksi dan Dokumen, Daftar Penerima, BKU, Laporan BOS, serta ubah password sendiri.
- Akun tersimpan di browser perangkat itu (password disimpan dalam bentuk hash, bukan teks asli). Setiap perangkat membuat akunnya sendiri.
- Ini pengunci tingkat aplikasi untuk mencegah akses iseng di komputer bersama. Ini bukan keamanan server: orang yang menguasai browser tersebut dan paham developer tools masih bisa membaca data tersimpan.
- Lupa password Admin: akun hanya bisa diatur ulang dengan menghapus kunci `bos_auth` di penyimpanan situs (developer tools) atau menghapus data situs. Cadangkan data lebih dulu.

## Data dan privasi
- Semua data tersimpan di browser masing-masing pengguna (localStorage). Tidak ada data yang dikirim ke server.
- Data tidak pindah antar perangkat. Gunakan fitur cadangan di aplikasi sebelum membersihkan cache browser.
- Satu browser menyediakan 10 slot sekolah yang datanya terpisah.

## Penyesuaian daerah
- Dasar hukum, format nomor surat, dan jam kerja pada pengaturan SPK bisa diedit sesuai daerah.

## Catatan
- Butuh internet saat dibuka (library SheetJS dimuat dari cdnjs).
- Periksa semua dokumen hasil cetak sebelum dipakai secara resmi. Aplikasi ini disediakan apa adanya, tanpa jaminan.
