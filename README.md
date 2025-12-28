# 🥗 Health & Recipe Management System (PHP Native Version)

[![PHP](https://img.shields.io/badge/Language-PHP-777BB4.svg)](https://www.php.net/)
[![MySQL](https://img.shields.io/badge/Database-MySQL-4479A1.svg)](https://www.mysql.com/)
[![Docker](https://img.shields.io/badge/Deployment-Docker-2496ED.svg)](https://www.docker.com/)

Aplikasi berbasis web untuk manajemen profil, perhitungan kalkulator kesehatan, dan pengelolaan resep. Proyek ini dibangun menggunakan **PHP Native** untuk mendemonstrasikan pemahaman dasar pemrograman web, manajemen session, dan interaksi database relasional tanpa framework.

> **📌 Informasi Penting:** > Repository ini adalah versi **PHP Native**. Jika Anda ingin melihat versi yang lebih modern dan terstruktur menggunakan framework, silakan kunjungi: https://github.com/WAHYUDLP/BloodWellness

---

## 🚀 Fitur Utama

* **Autentikasi User:** Sistem login, register, lupa password, dan verifikasi OTP (melalui `processVerifikasiOTP.php`).
* **Kalkulator Kesehatan:** Fitur khusus untuk melakukan kalkulasi data kesehatan (melalui `kalkulator.php`).
* **Manajemen Resep:** Fitur pencatatan dan pengelolaan resep makanan (`recipe.php`).
* **Perencana Menu:** Fitur untuk merencanakan menu harian user (`pagePlanner.php`).
* **Manajemen Akun:** Edit profil dan penghapusan akun secara aman.
* **Docker Ready:** Sudah dilengkapi dengan `Dockerfile` dan `docker-compose.yml` untuk deployment yang mudah.

---

## 🛠️ Stack Teknologi

* **Backend:** PHP (Native)
* **Frontend:** HTML, CSS (terdapat folder `/css`), Vanilla JavaScript
* **Database:** MySQL (`db.php` untuk koneksi)
* **Tools:** Composer (Dependency Manager), Docker (Containerization)

---

## 📂 Struktur Folder Penting

* `/dataset`: Penyimpanan data pendukung aplikasi.
* `/images` & `/uploads`: Penyimpanan aset statis dan file yang diunggah user.
* `/vendor`: Library pihak ketiga yang dikelola via Composer.
* `process...php`: File logic untuk menangani pengiriman form (Backend logic).

---

## ⚙️ Cara Instalasi (Lokal)

1.  **Clone Repository:**
    ```bash
    git clone [https://github.com/WAHYUDLP/nama-repo-anda.git](https://github.com/WAHYUDLP/nama-repo-anda.git)
    ```
2.  **Install Dependencies:**
    ```bash
    composer install
    ```
3.  **Konfigurasi Database:**
    * Impor file database (jika ada) ke MySQL.
    * Sesuaikan kredensial database di file `db.php`.
4.  **Menjalankan via Docker (Opsional):**
    ```bash
    docker-compose up -d
    ```

---

## 💡 Metodologi Pengembangan

Aplikasi ini mengikuti pola pengembangan **Procedural-Functional PHP**. Fokus utama dari proyek ini adalah:
1.  **Security:** Implementasi hashing password dan verifikasi OTP.
2.  **Session Management:** Memastikan keamanan data user antar halaman.
3.  **CRUD Operations:** Interaksi langsung dengan MySQL menggunakan ekstensi `mysqli` atau `PDO`.

---

**Dibuat oleh [WAHYUDLP](https://github.com/WAHYUDLP)**
