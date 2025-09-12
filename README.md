# 💼 Sistem Informasi Penggajian Karyawan  

[![GitHub stars](https://img.shields.io/github/stars/adam-miftah/sistem-penggajian?style=for-the-badge)](https://github.com/adam-miftah/sistem-penggajian/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/adam-miftah/sistem-penggajian?style=for-the-badge)](https://github.com/adam-miftah/sistem-penggajian/network/members)
[![GitHub issues](https://img.shields.io/github/issues/adam-miftah/sistem-penggajian?style=for-the-badge)](https://github.com/adam-miftah/sistem-penggajian/issues)
[![GitHub license](https://img.shields.io/github/license/adam-miftah/sistem-penggajian?style=for-the-badge)](LICENSE)

Aplikasi web berbasis **Laravel 12** untuk mengelola proses penggajian karyawan dengan cepat, efisien, dan akurat.  
Dirancang untuk mempermudah administrasi mulai dari **data karyawan, absensi, hingga laporan gaji** dengan antarmuka yang ramah pengguna.  

---

## ✨ Fitur Utama  

### 🔑 Otentikasi Multi-Role  
- **Admin**: Mengelola data master, absensi, transaksi, dan laporan.  
- **Pegawai**: Melihat profil, rekap absensi, dan slip gaji pribadi.  

### 📊 Dashboard Interaktif  
- **Admin**: Ringkasan data karyawan, jabatan, dan absensi terkini.  
- **Pegawai**: Informasi gaji bulan berjalan & absensi pribadi.  

### 👥 Manajemen Master Data (Admin)  
- CRUD **Data Karyawan** (lengkap dengan foto profil + akun login).  
- CRUD **Data Jabatan** (gaji pokok & tunjangan).  

### 🕒 Manajemen Transaksi (Admin)  
- Input **Absensi Harian** (terintegrasi ke rekap bulanan).  
- Input **Potongan Gaji** (individu atau massal).  
- **Kalkulasi Gaji Otomatis**:  
  > Gaji Bersih = Gaji Pokok + Tunjangan – Potongan Absensi – Potongan Lainnya  

### 📑 Laporan Profesional  
- Laporan Gaji Bulanan.  
- Laporan Absensi Bulanan.  
- **Cetak Slip Gaji** modern & informatif.  

### ⚡ Fitur Tambahan  
- **AJAX Search & Filter** → Data real-time tanpa reload.  
- **Profil Pengguna** → Ganti password & edit profil dengan aman.  

---

## 🚀 Teknologi yang Digunakan  

- **Backend**: Laravel 12 (PHP 8.3)  
- **Frontend**: Blade + Bootstrap (SB Admin 2) + jQuery + AJAX  
- **Database**: MySQL  
- **Server**: Apache (Laragon) / Laravel Sail  

---

## 🛠️ Instalasi & Penggunaan  

### 1️⃣ Clone Repository  
```bash
git clone https://github.com/adam-miftah/sistem-penggajian.git
cd sistem-penggajian
```

### 2️⃣ Instal Dependensi
```bash
composer install
npm install && npm run build
```

### 3️⃣ Konfigurasi Environment
- Salin file .env.example menjadi .env
- Buat database baru, misalnya: sistem_penggajian
- Sesuaikan konfigurasi DB di file .env
- 
### 4️⃣ Migrasi & Setup
```bash
php artisan key:generate
php artisan migrate:fresh
php artisan storage:link
```

### 5️⃣ Buat Akun Admin Awal (Opsional)
```bash
php artisan tinker
\App\Models\User::create([
    'name' => 'Admin',
    'email' => 'admin@gmail.com',
    'password' => bcrypt('password'),
    'role' => 'admin'
]);
```

### 6️⃣ Jalankan Aplikasi
```bash
php artisan serve
```

Buka di browser → http://127.0.0.1:8000

## 📜 Lisensi
Proyek ini dilisensikan di bawah MIT License.
Silakan gunakan, modifikasi, dan kembangkan sesuai kebutuhan 🚀

---

Mau saya tambahkan juga **contoh badge GitHub (stars, forks, issues)** biar lebih estetik?
