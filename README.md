# Dashboard Tugas Praktikum — Contoh Proyek Vercel

Proyek web statis berbahasa Indonesia, dibuat dengan HTML, CSS, dan JavaScript murni. Cocok untuk praktikum deploy melalui GitHub dan Vercel.

## Struktur proyek

```text
contoh-dashboard-tugas/
├── index.html
├── style.css
├── script.js
└── README.md
```

## Menjalankan lokal

1. Buka folder ini di VS Code.
2. Buka `index.html` dengan browser, atau gunakan ekstensi Live Server.
3. Tambahkan tugas, tandai selesai, hapus, dan coba filter status.
4. Tutup lalu buka kembali halaman pada browser yang sama untuk memeriksa `localStorage`.

## Deployment melalui GitHub + Vercel

1. Buat repository GitHub baru (contoh: `praktikum-vercel-tugas`).
2. Unggah `index.html`, `style.css`, `script.js`, dan `README.md` pada **root** repository.
3. Kunjungi https://vercel.com, masuk lalu pilih **Add New > Project** atau **New Project**.
4. Hubungkan GitHub, pilih repository ini, kemudian klik **Import**.
5. Pilih **Framework Preset: Other**. Pastikan **Root Directory** mengarah ke folder yang berisi `index.html` (umumnya `./`). Untuk proyek statis, **Build Command** harus kosong/tidak menjalankan build. Bila perlu aktifkan override Build Command lalu kosongkan. Jika mengisi **Output Directory** secara manual, gunakan `.` untuk struktur di root; jangan arahkan ke `dist` yang tidak ada.
6. Klik **Deploy**, periksa status dan buka URL produksi yang dihasilkan.
7. Lakukan perubahan teks atau tampilan, commit ke branch produksi GitHub, lalu periksa apakah Vercel memperbarui situs.

## Batasan penting

- `localStorage` tersimpan pada browser/perangkat yang digunakan; bukan database bersama.
- Data mungkin hilang ketika data situs dibersihkan atau browser dibuka dalam lingkungan yang berbeda.
- Jangan memasukkan kata sandi, API key rahasia, atau informasi pribadi ke repository publik atau kode JavaScript klien.
- Nama menu dan UI Vercel dapat berubah. Rujuk dokumentasi resmi: https://vercel.com/docs/git dan https://vercel.com/docs/builds/configure-a-build.

## Uji fungsi

1. Halaman memuat tanpa error JavaScript di Console.
2. Tiga tugas contoh tampil saat akses pertama.
3. Tugas baru muncul setelah dikirim.
4. Kolom nama tugas tidak menerima input kosong.
5. Tugas dapat ditandai selesai dan dibatalkan.
6. Tugas dapat dihapus.
7. Filter Semua, Aktif, Selesai bekerja.
8. Statistik dan progres berubah sesuai kondisi.
9. Data bertahan setelah refresh pada browser yang sama.
10. Tampilan dapat digunakan pada layar ponsel.
