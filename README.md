🎮 BLOCK BLAST 3D
Game puzzle block-blast dengan animasi 3D, dibuat 100% dalam satu file HTML (tanpa dependensi eksternal apa pun — tidak ada CDN, tidak ada font online, tidak ada library luar). Dijamin tetap bisa jalan walau koneksi internet lambat atau bahkan offline, karena semua CSS dan JavaScript sudah menyatu di dalam block-blast-3d.html.

Developer: ikkyofc Brand: IKKY OFFICIAL

✨ Fitur
Grid 8x8 klasik ala Block Blast — susun balok, penuhi baris/kolom untuk membersihkannya.
±30 bentuk balok berbeda — dari 1x1 kotak kecil sampai bentuk L, T, S/Z, garis panjang, kotak 3x3, dan bentuk plus.
8 warna balok gradient yang dipilih acak setiap kali balok baru muncul.
Animasi 3D pada tiap balok — efek voxel/candy-block dengan bevel highlight & shadow, animasi jatuh (dropIn dengan rotateX), dan animasi pecah (clearPop) saat baris/kolom terhapus.
Ledakan partikel + layar bergetar (shake) setiap kali baris/kolom berhasil dibersihkan.
Sistem kombo — bersihkan baris berturut-turut tanpa jeda untuk mendapatkan skor berlipat ganda, lengkap dengan pop-up teks "COMBO x3!" dsb.
Preview & highlight penempatan — saat balok diseret, sel yang valid berwarna biru (bisa ditempatkan) dan sel yang tidak valid berwarna merah.
Drag & drop penuh menggunakan Pointer Events, jadi mendukung mouse, touchscreen, maupun stylus sekaligus.
Deteksi Game Over otomatis — game akan mengecek apakah ke-3 balok di tray masih punya tempat yang muat; kalau tidak ada, modal Game Over otomatis muncul.
Skor & skor terbaik tersimpan otomatis lewat localStorage, jadi rekor kamu tidak hilang walau browser ditutup.
Efek suara ringan memakai Web Audio API murni (tidak perlu file audio eksternal), bisa dimatikan lewat tombol speaker di pojok kanan atas.
Tampilan responsif — didesain mobile-first, nyaman dipakai di layar HP maupun desktop, lengkap dengan tema gelap bernuansa neon/ungu dan animasi latar belakang yang halus.
📂 Struktur File
block-blast-3d.html   -> Game utama (HTML + CSS + JS jadi satu file)
README.md             -> Dokumen ini
LICENSE               -> Lisensi MIT
▶️ Cara Menjalankan
Download file block-blast-3d.html.
Buka file tersebut langsung dua kali klik, atau buka lewat browser (Chrome/Firefox/Safari/Edge, juga aman dibuka di WebView seperti Acode/Spck Editor).
Tidak perlu server, tidak perlu instalasi apa pun — langsung main.
🎯 Cara Bermain
Di bagian bawah layar ada 3 slot balok yang bisa diseret (drag).
Seret salah satu balok ke papan 8x8 di tengah layar.
Sel yang berwarna biru terang menandakan posisi valid, merah menandakan posisi tidak valid (tertimpa balok lain atau keluar papan).
Lepaskan jari/klik di posisi yang valid untuk menempatkan balok.
Jika satu baris atau satu kolom terisi penuh, baris/kolom tersebut otomatis meledak dan memberi skor.
Bersihkan baris secara beruntun untuk mendapatkan bonus kombo.
Game berakhir ketika ketiga balok di tray sudah tidak ada lagi tempat yang cocok di papan.
Tekan tombol "MAIN LAGI" atau ikon restart di pojok kanan atas untuk mengulang dari awal.
🛠️ Detail Teknis
Tanpa framework — murni HTML, CSS, dan JavaScript vanilla (IIFE, strict mode), tanpa React/Vue/library pihak ketiga.
Tanpa font eksternal — memakai system font stack (-apple-system, Segoe UI, Roboto, dst) supaya tetap tampil rapi meski tanpa koneksi internet, dan menghindari masalah rendering di WebView (Acode/Spck) yang pernah dialami pada project sebelumnya.
Tanpa emoji di dalam kode — ikon suara & restart digambar pakai SVG inline, bukan emoji, untuk menghindari isu rendering di beberapa WebView Android.
Efek 3D murni CSS (box-shadow, linear-gradient, transform, perspective), tidak memakai WebGL/Three.js, sehingga ringan dan tetap cepat dimuat di perangkat dengan koneksi lambat.
Drag & drop dibangun dengan Pointer Events API (pointerdown, pointermove, pointerup) sehingga satu kode yang sama bekerja untuk mouse maupun sentuhan layar.
Penyimpanan skor memakai localStorage (key: ikky_blockblast3d_best), murni di perangkat pengguna, tidak mengirim data ke server mana pun.
🧩 Kustomisasi
Kalau ingin mengubah ukuran papan, cukup ubah nilai var SIZE = 8; di bagian <script> (perlu diingat: mengubah ukuran papan akan memengaruhi seberapa mudah bentuk balok besar bisa muat).

Untuk menambah warna baru, tambahkan objek baru ke array COLORS dengan format:

{ name:"nama-warna", c1:"#kode-terang", c2:"#kode-gelap" }
Untuk menambah bentuk balok baru, tambahkan array koordinat [baris, kolom] baru ke SHAPES, dimulai dari [0,0].

📄 Lisensi
Proyek ini dirilis di bawah lisensi MIT. Lihat file LICENSE untuk detail lengkap.

Dibuat dengan ❤️ oleh ikkyofc — IKKY OFFICIAL
