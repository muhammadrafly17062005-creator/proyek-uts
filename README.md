# Filter Wajah AR: Wisuda dan Kampus (`ar-filter-wisuda`)

Aplikasi Augmented Reality (AR) berbasis web (Prototipe v0.5) yang menempelkan aksesori 3D beranimasi bertema wisuda dan kehidupan kampus secara *real-time* pada wajah pengguna melalui browser smartphone.

Proyek ini disusun untuk memenuhi tugas Miniproject UTS mata kuliah **Praktikum Augmented dan Virtual Reality (ITIA730591)**, Program Studi Teknologi Informasi, Fakultas Ilmu Komputer dan Teknologi Informasi (FIKTI), Universitas Muhammadiyah Sumatera Utara (UMSU).

## Teknologi yang Digunakan
* **Three.js** (`v0.160.0`) — Rendering objek dan klip animasi 3D
* **MindAR** — *Face tracking* berbasis web
* **HTML5, CSS3, JavaScript** — Antarmuka pengguna (HUD) dan logika interaksi
* **Node.js (`serve-https.js`)** — Server HTTPS lokal untuk pengujian kamera saat *development*
* **GitHub Pages** — Hosting HTTPS untuk akses kamera pada perangkat smartphone

## Anggota Kelompok & Pembagian Tugas
| No | Nama | NPM | Peran | Tanggung Jawab Utama |
| :--- | :--- | :--- | :--- | :--- |
| 1 | Muhammad Rafly | 2409020044 | Project Manager & Integrator | Papan tugas, pengelolaan repository & *merge*, *deployment* HTTPS, kode QR |
| 2 | Gilang Indra Trisanu | 2409020076 | Engineer Tracking | MindAR *face tracking*, kalibrasi titik tempel wajah, uji kestabilan cahaya |
| 3 | Fanny Fadhillah | 2409020083 | Aset 3D & Animasi | Model 3D `.glb`, klip animasi *idle*/*loop*, optimasi ukuran file, tabel lisensi aset |
| 4 | M. Vicky Azhari | 2409020070 | Interaksi & UI/UX | HUD, tombol ganti filter, tombol ambil foto, penanganan izin kamera ditolak |
| 5 | R. Gilang Setyo Nugroho | 2409020019 | Data, Persistence, QA & Dokumentasi | Struktur `filters.json`, simpan foto ke perangkat, matriks perangkat, `README.md`, video demo, *issue log* |

## Struktur Folder
```text
ar-filter-wisuda/
├── assets/
│   └── .gitkeep        # Penyimpanan model 3D (.glb) dan ikon antarmuka
├── filters.json        # Konfigurasi daftar filter, path model, posisi, dan skala
├── index.html          # Halaman utama aplikasi AR (HUD, kamera, scene Three.js & MindAR)
├── README.md           # Dokumentasi proyek
├── serve-https.js      # Skrip server lokal Node.js dengan protokol HTTPS
└── start-https.bat     # Pintasan Windows untuk menjalankan server HTTPS lokal