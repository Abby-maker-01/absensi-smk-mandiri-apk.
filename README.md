# Absensi SMK Mandiri Haurgeulis — perbaikan

Perubahan:
- Pilihan dan alur absensi murid dihilangkan; hanya Guru dan Admin.
- Admin melihat riwayat absensi guru dari semua tanggal secara default. Isi tanggal untuk memfilter satu hari; kosongkan untuk semua riwayat.
- Riwayat diurutkan tanggal terbaru terlebih dahulu. Data lama yang sudah ada di Firestore tidak dihapus.
- Pendaftaran hanya untuk guru dan tetap menunggu persetujuan admin.

## Build APK lewat GitHub
1. Ekstrak ZIP ini, lalu unggah semua isi folder ke repo GitHub baru atau repo aplikasi yang dipakai.
2. Pastikan `www/firebase-config.js` menunjuk ke proyek Firebase yang benar (saat ini memakai project ID absensi-smk-mandiri-haurgeulis).
3. Pastikan Firestore Rules mengizinkan admin membaca koleksi `attendance` dan guru membuat/membaca dokumen absensinya sendiri. Riwayat tidak bisa muncul jika aturan Firestore menolak admin membaca data lama.
4. Buka tab Actions, pilih **Build Absensi APK**, lalu tekan **Run workflow**. Unduh artifact setelah proses selesai.

Catatan: file yang dikirim sebelumnya adalah APK jadi, bukan source project. ZIP ini berisi source web yang diekstrak dan workflow build baru; APK lama tidak dapat diperbarui dengan aman hanya dengan mengedit file di dalam APK.
