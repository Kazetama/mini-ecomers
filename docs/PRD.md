# Product Requirements Document (PRD)

## Pratama Digital Services --- Mini E-Commerce Layanan Digital

**Versi:** 1.0\
**Status:** Draft\
**Tanggal:** 27 Oktober 2026\
**Platform:** Website responsif\
**Produk:** Pratama Digital Services

------------------------------------------------------------------------

## 1. Ringkasan Produk

Pratama Digital Services adalah website mini e-commerce untuk pemesanan
layanan digital, terutama pengecekan kemiripan dokumen, penyuntingan,
pemformatan, dan konsultasi akademik.

Website dirancang agar pelanggan dapat melihat layanan, memilih
kebutuhan, mengunggah dokumen secara privat, melakukan pemesanan dan
pembayaran, serta memantau status pesanan. Admin mengelola layanan,
pesanan, pembayaran, dan pengiriman hasil melalui dashboard.

Produk versi pertama berfokus pada alur transaksi yang sederhana dan
dapat digunakan, bukan pada fitur marketplace yang kompleks.

## 2. Latar Belakang dan Masalah

Pemesanan layanan digital melalui percakapan manual dapat membuat
informasi layanan, harga, dokumen, pembayaran, dan status pengerjaan
tersebar di beberapa tempat. Pelanggan juga dapat kesulitan mengetahui
progres pesanannya.

Pratama menyatukan proses tersebut dalam satu website dengan katalog
layanan, formulir pemesanan, pembayaran, pelacakan pesanan, dan
dashboard admin.

## 3. Tujuan Produk

1.  Menyediakan katalog layanan digital dengan informasi dan harga yang
    jelas.
2.  Memungkinkan pelanggan membuat pesanan tanpa harus menghubungi admin
    terlebih dahulu.
3.  Mengelola dokumen pelanggan secara privat dan terkontrol.
4.  Menyediakan status pesanan yang dapat dipantau pelanggan.
5.  Memudahkan admin mengelola layanan, pesanan, pembayaran, dan hasil
    pekerjaan.
6.  Menghasilkan proyek portofolio full-stack yang memiliki alur bisnis
    nyata dan arsitektur terpelihara.

## 4. Sasaran Pengguna

### 4.1 Pelanggan

Pengguna yang ingin membeli layanan pengecekan kemiripan dokumen,
penyuntingan, pemformatan, atau konsultasi akademik.

Kebutuhan utama: - Menemukan layanan dan harga. - Memahami persyaratan
layanan. - Mengirim dokumen dengan aman. - Melakukan pembayaran. -
Memantau status pesanan. - Mengakses hasil yang telah selesai.

### 4.2 Admin

Pengelola bisnis yang menangani layanan dan pesanan.

Kebutuhan utama: - Mengelola katalog dan harga. - Melihat detail
pesanan. - Memverifikasi pembayaran. - Memperbarui status pengerjaan. -
Mengunggah hasil. - Mengelola pelanggan dan operasional dasar.

## 5. Ruang Lingkup MVP

### 5.1 Termasuk dalam MVP

-   Landing page.
-   Katalog dan detail layanan.
-   Registrasi, login, dan logout.
-   Formulir checkout.
-   Upload dokumen privat.
-   Pembuatan nomor pesanan.
-   Ringkasan pesanan dan harga.
-   Integrasi pembayaran melalui penyedia pembayaran.
-   Verifikasi status pembayaran di sisi server.
-   Dashboard pelanggan.
-   Riwayat dan detail pesanan.
-   Pelacakan status pesanan.
-   Dashboard admin.
-   CRUD layanan.
-   Pengelolaan pesanan.
-   Pengunggahan hasil.
-   Validasi input dan kontrol akses.
-   Responsivitas desktop dan mobile.

### 5.2 Tidak termasuk dalam MVP

-   Marketplace multi-penjual.
-   Keranjang multi-layanan kompleks.
-   Chat real-time.
-   Program afiliasi.
-   Sistem poin dan loyalitas.
-   Aplikasi mobile native.
-   AI untuk mengerjakan tugas akademik.
-   Otomatisasi analisis dokumen berbasis AI.
-   Kupon dan promosi kompleks.
-   Integrasi banyak penyedia pembayaran sekaligus.

Fitur di luar MVP dapat dipertimbangkan setelah alur inti stabil dan
telah diuji.

## 6. Jenis Layanan

Admin dapat mengelola layanan melalui dashboard.

Kategori awal: 1. **Pengecekan kemiripan dokumen** --- layanan
pengecekan melalui akses yang sah dan sesuai kebijakan penyedia. 2.
**Penyuntingan dokumen** --- koreksi bahasa, tata tulis, dan
konsistensi. 3. **Pemformatan dokumen** --- penyesuaian format
berdasarkan pedoman yang diberikan pelanggan. 4. **Konsultasi akademik**
--- bantuan memahami materi dan menyusun pekerjaan secara mandiri.

Setiap layanan memiliki: - Nama. - Slug. - Deskripsi. - Kategori. -
Harga dasar. - Estimasi waktu pengerjaan. - Persyaratan dokumen. -
Status aktif/nonaktif.

Harga final ditetapkan admin dan ditampilkan sebelum pelanggan melakukan
pembayaran. Website tidak menjanjikan persentase kemiripan tertentu atau
menyediakan manipulasi laporan.

## 7. Alur Pengguna

### 7.1 Alur pelanggan

1.  Pelanggan membuka website.
2.  Melihat katalog layanan.
3.  Membuka detail layanan.
4.  Memilih layanan.
5.  Login atau registrasi jika belum memiliki akun.
6.  Mengisi informasi pesanan.
7.  Mengunggah dokumen yang diperlukan.
8.  Memeriksa ringkasan dan total harga.
9.  Menyetujui ketentuan layanan dan privasi.
10. Membuat pesanan.
11. Melakukan pembayaran.
12. Sistem memverifikasi pembayaran melalui mekanisme server.
13. Admin memproses pesanan.
14. Pelanggan memantau status.
15. Admin mengunggah hasil.
16. Pelanggan mengunduh hasil secara aman.
17. Pesanan ditandai selesai.

### 7.2 Alur admin

1.  Admin login.
2.  Membuka dashboard.
3.  Melihat pesanan baru dan status pembayaran.
4.  Memeriksa detail pesanan dan dokumen sesuai kewenangan.
5.  Memverifikasi pembayaran melalui sistem.
6.  Memulai pengerjaan.
7.  Memperbarui status.
8.  Mengunggah hasil.
9.  Menandai pesanan selesai.

## 8. Status Pesanan dan Pembayaran

Status pesanan: - `pending_payment` - `paid` - `processing` -
`revision_requested` - `completed` - `cancelled`

Status pembayaran: - `pending` - `paid` - `failed` - `expired` -
`refunded`

Status pembayaran dan status pengerjaan harus dipisahkan. Pembayaran
berhasil tidak otomatis berarti pekerjaan selesai.

Transisi status harus divalidasi di sisi server. Admin tidak boleh
mengubah status secara sembarang tanpa aturan.

## 9. Persyaratan Fungsional

  -----------------------------------------------------------------------
  ID                      Fitur                   Persyaratan
  ----------------------- ----------------------- -----------------------
  FR-01                   Katalog layanan         Pengunjung dapat
                                                  melihat layanan aktif,
                                                  deskripsi, harga, dan
                                                  estimasi waktu.

  FR-02                   Detail layanan          Pengunjung dapat
                                                  melihat persyaratan dan
                                                  informasi lengkap
                                                  layanan.

  FR-03                   Autentikasi             Pengguna dapat
                                                  registrasi, login, dan
                                                  logout secara aman.

  FR-04                   Checkout                Pelanggan dapat mengisi
                                                  detail pesanan dan
                                                  melihat ringkasan
                                                  sebelum konfirmasi.

  FR-05                   Upload dokumen          Pelanggan dapat
                                                  mengunggah file yang
                                                  memenuhi tipe dan
                                                  ukuran yang diizinkan.

  FR-06                   Pembuatan pesanan       Sistem membuat nomor
                                                  pesanan unik dan
                                                  menyimpan snapshot
                                                  harga saat transaksi.

  FR-07                   Pembayaran              Sistem membuat
                                                  transaksi melalui
                                                  penyedia pembayaran dan
                                                  memverifikasi
                                                  notifikasi di server.

  FR-08                   Dashboard pelanggan     Pelanggan dapat melihat
                                                  pesanan miliknya dan
                                                  status terkini.

  FR-09                   Detail pesanan          Pelanggan dapat melihat
                                                  ringkasan, status,
                                                  pembayaran, dan dokumen
                                                  hasil yang tersedia.

  FR-10                   Dashboard admin         Admin dapat melihat
                                                  ringkasan operasional
                                                  dan daftar pesanan.

  FR-11                   Pengelolaan layanan     Admin dapat membuat,
                                                  mengubah, mengaktifkan,
                                                  dan menonaktifkan
                                                  layanan.

  FR-12                   Pengelolaan pesanan     Admin dapat melihat
                                                  pesanan, memprosesnya,
                                                  dan memperbarui status
                                                  sesuai aturan.

  FR-13                   Pengiriman hasil        Admin dapat mengunggah
                                                  hasil dan pelanggan
                                                  yang berwenang dapat
                                                  mengunduhnya.

  FR-14                   Riwayat                 Pelanggan dapat melihat
                                                  riwayat pesanan
                                                  miliknya.

  FR-15                   Notifikasi status       Sistem menampilkan
                                                  perubahan status pada
                                                  dashboard; notifikasi
                                                  eksternal dapat
                                                  ditambahkan setelah
                                                  MVP.
  -----------------------------------------------------------------------

## 10. Persyaratan Nonfungsional

### 10.1 Keamanan

-   Dokumen disimpan di private storage, bukan direktori publik.
-   Akses dokumen harus memeriksa autentikasi, kepemilikan, dan izin.
-   File divalidasi berdasarkan ukuran, ekstensi, dan MIME type.
-   Nama file penyimpanan menggunakan identifier acak.
-   Rahasia dan kredensial pembayaran hanya berada di server.
-   Pembayaran tidak boleh dianggap berhasil hanya berdasarkan redirect
    browser.
-   Notifikasi pembayaran harus diverifikasi sesuai dokumentasi
    provider.
-   Operasi pembayaran harus idempotent untuk mencegah pemrosesan
    berulang.
-   Admin memiliki kontrol akses berbasis peran.
-   Data sensitif tidak boleh dicatat dalam log.

### 10.2 Usability

-   Navigasi mudah dipahami.
-   Informasi harga dan persyaratan terlihat sebelum checkout.
-   Formulir memberikan pesan validasi yang jelas.
-   Status loading, kosong, berhasil, dan gagal tersedia.
-   Alur utama dapat digunakan pada perangkat mobile.

### 10.3 Maintainability

-   UI, business logic, data access, dan integrasi eksternal dipisahkan.
-   TypeScript digunakan untuk kode aplikasi.
-   Validasi server menjadi sumber validasi utama.
-   Dokumentasi diperbarui ketika arsitektur berubah.
-   Perubahan database menggunakan migration yang terkontrol.

### 10.4 Performance

-   Hindari JavaScript client yang tidak diperlukan.
-   Gunakan server-side rendering atau strategi rendering sesuai
    kebutuhan.
-   Optimalkan gambar dan query database.
-   Hindari pengambilan data berulang yang tidak diperlukan.

## 11. Halaman dan Routing

  ---------------------------------------------------------------------------
  Route                       Akses                   Fungsi
  --------------------------- ----------------------- -----------------------
  `/`                         Publik                  Beranda

  `/layanan`                  Publik                  Katalog layanan

  `/layanan/[slug]`           Publik                  Detail layanan

  `/login`                    Publik                  Login

  `/register`                 Publik                  Registrasi

  `/checkout`                 Pelanggan               Checkout

  `/dashboard`                Pelanggan               Ringkasan akun dan
                                                      pesanan

  `/dashboard/pesanan`        Pelanggan               Riwayat pesanan

  `/dashboard/pesanan/[id]`   Pemilik pesanan         Detail dan status
                                                      pesanan

  `/admin/dashboard`          Admin                   Ringkasan operasional

  `/admin/pesanan`            Admin                   Pengelolaan pesanan

  `/admin/layanan`            Admin                   Pengelolaan katalog

  `/admin/pelanggan`          Admin                   Pengelolaan pelanggan
                                                      dasar
  ---------------------------------------------------------------------------

Route dapat disesuaikan dengan konvensi Next.js versi yang terpasang.

## 12. Data Utama

Entitas inti: - User - Service - Order - OrderDocument - Payment -
OrderStatusHistory

### User

Menyimpan identitas akun, email, kredensial yang aman, dan role.

### Service

Menyimpan informasi layanan, kategori, harga, estimasi, dan status
aktif.

### Order

Menyimpan pelanggan, nomor pesanan, layanan, snapshot harga, status, dan
waktu.

### OrderDocument

Menyimpan metadata file, lokasi private storage, jenis dokumen, dan
relasi pesanan.

### Payment

Menyimpan provider, identifier transaksi, status, nominal, dan waktu
pembayaran.

### OrderStatusHistory

Menyimpan perubahan status, aktor, waktu, dan catatan yang relevan.

Data pembayaran dan dokumen harus memiliki kontrol akses dan retensi
yang sesuai.

## 13. Design System

Arah visual: - Gaya: Clean Premium. - Warna utama: electric blue. -
Warna pendukung: navy. - Latar: putih dan neutral gray. - Tipografi:
modern dan mudah dibaca. - Ikon: Lucide React. - Komponen dasar:
shadcn/ui. - Styling: Tailwind CSS.

Prinsip: - Hindari desain generik yang berulang. - Hindari penggunaan
gradient, glassmorphism, dan animasi berlebihan. - Gunakan komposisi
berbeda sesuai fungsi halaman. - Pertahankan konsistensi spacing,
typography, warna, dan komponen. - Prioritaskan aksesibilitas dan
responsivitas.

## 14. Teknologi

Teknologi awal yang direncanakan: - Next.js dengan versi yang telah
terpasang. - TypeScript. - Tailwind CSS. - shadcn/ui. - PostgreSQL. -
Prisma atau ORM yang dipilih setelah memeriksa proyek. - Sistem
autentikasi yang kompatibel. - Penyimpanan dokumen privat. - Midtrans
atau provider pembayaran yang dipilih.

Semua API dan konvensi harus diverifikasi melalui dokumentasi versi yang
terpasang. Daftar ini merupakan rancangan, bukan bukti bahwa semua
dependensi telah terinstal.

## 15. Acceptance Criteria

MVP dapat dianggap siap untuk demo ketika:

1.  Pengunjung dapat melihat katalog layanan aktif.
2.  Pelanggan dapat membuat akun dan login.
3.  Pelanggan dapat memilih layanan dan membuat pesanan.
4.  Sistem memvalidasi input dan dokumen.
5.  Pesanan memiliki nomor unik dan ringkasan harga.
6.  Pelanggan dapat memulai pembayaran.
7.  Status pembayaran diverifikasi di server.
8.  Pelanggan hanya dapat melihat pesanan miliknya.
9.  Admin dapat mengelola layanan dan pesanan.
10. Admin dapat memperbarui status sesuai aturan.
11. Admin dapat mengunggah hasil secara privat.
12. Pelanggan yang berwenang dapat mengunduh hasil.
13. UI responsif pada desktop dan mobile.
14. Validasi, error state, dan loading state tersedia.
15. Pemeriksaan lint, type checking, dan pengujian relevan telah
    dijalankan.
16. Dokumentasi utama sesuai dengan implementasi aktual.

## 16. Rencana Implementasi

### Fase 1 --- Fondasi

-   Audit proyek dan versi Next.js.
-   Menetapkan struktur folder.
-   Menyiapkan design system.
-   Menyiapkan database dan migration.
-   Menulis dokumentasi arsitektur awal.

### Fase 2 --- UI Publik

-   Beranda.
-   Katalog layanan.
-   Detail layanan.
-   Layout responsif.
-   FAQ dan informasi layanan.

### Fase 3 --- Autentikasi dan Pesanan

-   Registrasi dan login.
-   Form checkout.
-   Validasi.
-   Pembuatan pesanan.
-   Dashboard pelanggan.
-   Riwayat dan detail pesanan.

### Fase 4 --- Dokumen dan Pembayaran

-   Private document storage.
-   Upload dan download terkontrol.
-   Integrasi provider pembayaran.
-   Verifikasi notifikasi.
-   Penanganan pembayaran gagal dan kedaluwarsa.

### Fase 5 --- Admin

-   Dashboard admin.
-   CRUD layanan.
-   Pengelolaan pesanan.
-   Pengelolaan status.
-   Upload hasil.

### Fase 6 --- Quality Assurance

-   Pengujian business logic.
-   Pengujian authorization.
-   Pengujian alur pembayaran.
-   Pengujian upload dokumen.
-   Responsivitas.
-   Lint, type checking, dan build.

## 17. Risiko dan Mitigasi

  -----------------------------------------------------------------------
  Risiko                              Mitigasi
  ----------------------------------- -----------------------------------
  Dokumen pelanggan bocor             Private storage, authorization,
                                      signed URL, dan kebijakan retensi.

  Pembayaran palsu                    Verifikasi server-side dan validasi
                                      notifikasi provider.

  Pesanan diproses dua kali           Idempotency dan transaksi database.

  Scope proyek membesar               Batasi MVP dan tunda fitur
                                      non-esensial.

  API framework berubah               Periksa dokumentasi versi yang
                                      terpasang.

  UI tidak konsisten                  Design system dan review setiap
                                      halaman.

  Status pesanan tidak valid          Validasi transisi status di server.
  -----------------------------------------------------------------------

## 18. Pengembangan Berikutnya

Setelah MVP stabil, fitur berikut dapat dipertimbangkan berdasarkan
kebutuhan pengguna: - Notifikasi email atau Telegram. - Voucher
sederhana. - Rating layanan. - Chat atau dukungan pelanggan. -
Otomatisasi alur administrasi. - Analisis operasional. - Integrasi
layanan tambahan.

Fitur lanjutan tidak boleh mengganggu stabilitas alur inti.

## 19. Keputusan Produk

Pratama versi pertama adalah website e-commerce layanan digital dengan
satu pengelola bisnis.

Prioritas produk: 1. Pemesanan yang mudah. 2. Harga yang transparan. 3.
Pembayaran yang dapat diverifikasi. 4. Dokumen yang aman. 5. Status
pesanan yang jelas. 6. Admin yang dapat mengelola operasional. 7.
Arsitektur yang mudah dikembangkan.

**Prinsip akhir:** bangun sedikit fitur, tetapi setiap fitur harus
berfungsi, aman, terdokumentasi, dan memiliki kualitas UI/UX yang baik.
