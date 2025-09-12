Sistem Informasi Penggajian Karyawan
Aplikasi web manajemen penggajian karyawan yang dibangun menggunakan Laravel 12. Didesain untuk mempermudah proses administrasi gaji, dari pengelolaan data karyawan, absensi, hingga pembuatan laporan gaji secara efisien dan akurat.

✨ Fitur Utama
Otentikasi Dua Peran: Sistem login terpisah untuk Admin dan Pegawai dengan hak akses yang berbeda.

Dashboard Interaktif:

Admin: Ringkasan data karyawan, jabatan, dan absensi terkini.

Pegawai: Informasi profil, rincian gaji bulan ini, dan rekap absensi pribadi.

Manajemen Master Data (Admin):

CRUD Data Karyawan (lengkap dengan foto profil dan penautan akun login).

CRUD Data Jabatan (termasuk gaji pokok dan tunjangan).

Manajemen Transaksi (Admin):

Input Absensi Harian untuk semua karyawan dalam satu halaman, terintegrasi dengan rekap bulanan.

Input Potongan Gaji insidental untuk karyawan tertentu atau semua karyawan.

Kalkulasi Gaji Otomatis: Gaji bersih dihitung secara otomatis berdasarkan Gaji Pokok, Tunjangan, Absensi (potongan alpha), dan potongan lainnya.

Laporan Profesional:

Laporan Gaji Bulanan.

Laporan Absensi Bulanan.

Cetak Slip Gaji individual yang modern dan informatif.

Fitur AJAX: Pencarian dan pemfilteran data secara real-time tanpa perlu me-refresh halaman untuk pengalaman pengguna yang lebih cepat.

Profil Pengguna: Setiap pengguna dapat melihat profil dan mengganti password dengan aman.

🚀 Teknologi yang Digunakan
Backend: Laravel 12, PHP 8.3

Frontend: Blade, Bootstrap (SB Admin 2 Template), jQuery, AJAX

Database: MySQL

Web Server: Apache (via Laragon) / Laravel Sail

🛠️ Cara Instalasi dan Penggunaan
Pastikan Anda sudah memiliki Composer dan NPM terinstal di sistem Anda.

Clone repositori ini:

git clone [https://github.com/adam-miftah/sistem-penggajian.git](https://github.com/adam-miftah/sistem-penggajian.git)
cd sistem-penggajian

Instal dependensi:

composer install
npm install && npm run build

Setup Environment:

Salin file .env.example menjadi .env.

Buat database baru (misal: sistem_penggajian).

Atur konfigurasi database di file .env Anda (DB_DATABASE, DB_USERNAME, DB_PASSWORD).

Jalankan Migrasi & Buat Key:

php artisan key:generate
php artisan migrate:fresh
php artisan storage:link

(Opsional) Buat Akun Admin Awal:
Buka terminal dan jalankan Tinker:

php artisan tinker

Lalu jalankan kode berikut di dalam shell Tinker:

\App\Models\User::create(['name' => 'Admin', 'email' => 'admin@gmail.com', 'password' => bcrypt('password'), 'role' => 'admin']);

Jalankan Aplikasi:

php artisan serve

Buka http://127.0.0.1:8000 di browser Anda.

📜 Lisensi
Proyek ini dilisensikan di bawah Lisensi MIT.
