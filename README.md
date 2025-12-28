# 🥗 Health & Recipe Management System (PHP Native Version)

[![PHP](https://img.shields.io/badge/Language-PHP-777BB4.svg)](https://www.php.net/)
[![MySQL](https://img.shields.io/badge/Database-MySQL-4479A1.svg)](https://www.mysql.com/)
[![Docker](https://img.shields.io/badge/Deployment-Docker-2496ED.svg)](https://www.docker.com/)

Aplikasi berbasis web untuk manajemen profil, perhitungan kalkulator kesehatan, dan pengelolaan resep. Proyek ini dibangun menggunakan **PHP Native** untuk mendemonstrasikan pemahaman dasar pemrograman web, manajemen session, dan interaksi database relasional tanpa framework.

> **📌 Informasi Penting:**
> Repository ini adalah versi **PHP Native**. Jika Anda ingin melihat versi yang lebih modern dan terstruktur menggunakan framework, silakan kunjungi: **[BloodWellness (Laravel Version)](https://github.com/WAHYUDLP/BloodWellness)**

---

## 🚀 Fitur Utama

* **Autentikasi User:** Sistem login, register, lupa password, dan verifikasi OTP.
* **Kalkulator Kesehatan:** Fitur kalkulasi BMR dan kebutuhan kalori harian yang akurat.
* **Manajemen Resep:** Fitur pencatatan dan pengelolaan resep makanan (`recipe.php`).
* **Perencana Menu:** Fitur untuk merencanakan menu harian user (`pagePlanner.php`).
* **Manajemen Akun:** Edit profil dan penghapusan akun secara aman.
* **Docker Ready:** Sudah dilengkapi dengan `Dockerfile` dan `docker-compose.yml`.

---

## 🧠 Metodologi Perhitungan (Kalkulator Kesehatan)

Aplikasi ini menggunakan algoritma perhitungan standar medis untuk menentukan *Basal Metabolic Rate* (BMR) user:

### 1. Katch-McArdle Formula
Digunakan apabila data **persentase lemak tubuh** diketahui. Rumus ini lebih akurat karena didasarkan pada massa tubuh tanpa lemak (*Lean Body Mass*).
$$LBM = Berat \times (1 - \% Lemak\ Tubuh)$$
$$BMR = 370 + (21.6 \times LBM)$$

### 2. Mifflin-St Jeor Formula
Digunakan apabila **lemak tubuh tidak diketahui**. Rumus ini merupakan standar industri saat ini untuk estimasi BMR berdasarkan parameter fisik umum:
* **Pria:** $BMR = 10 \times berat\ (kg) + 6.25 \times tinggi\ (cm) - 5 \times usia\ (tahun) + 5$
* **Wanita:** $BMR = 10 \times berat\ (kg) + 6.25 \times tinggi\ (cm) - 5 \times usia\ (tahun) - 161$

---

## 🛠️ Stack Teknologi

* **Backend:** PHP (Native)
* **Frontend:** HTML, CSS (Tailwind CSS style), Vanilla JavaScript
* **Database:** MySQL (`db.php` untuk koneksi)
* **Tools:** Composer, Docker (Containerization)

---

## 📂 Struktur Folder Penting

* `/dataset`: Penyimpanan data pendukung aplikasi.
* `/images` & `/uploads`: Penyimpanan aset statis dan file user.
* `/vendor`: Library pihak ketiga via Composer.
* `process...php`: Backend logic untuk handling form.

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
    * Impor file database ke MySQL.
    * Sesuaikan kredensial di file `db.php`.
4.  **Menjalankan via Docker:**
    ```bash
    docker-compose up -d
    ```

---

## 💡 Konsep Pengembangan

Aplikasi ini menerapkan pola **Procedural-Functional PHP** dengan fokus pada:
1.  **Security:** Implementasi hashing password dan verifikasi OTP.
2.  **Session Management:** Pengamanan akses halaman berbasis role/status login.
3.  **Data Integrity:** Validasi input pada sisi server untuk perhitungan kalkulator yang akurat.

---

**Dibuat oleh [WAHYUDLP](https://github.com/WAHYUDLP)**
