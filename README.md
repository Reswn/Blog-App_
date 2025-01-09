# DOKUMENTASI PROJECT UJIAN AKHIR SEMESTER PEMROGRAMAN BERBASIS WEB
# KELOMPOK  _IF-5A
### ANGGOTA : 1. DEDEN ADI MARDIAN LAESMANA
###           2. RENI KARTIKA SUWANDI
###           3. KIKIH ISMAN ISKANDAR

## LAPORAN PROJECT : APLIKASI BLOG FULL-STACK
## 1. Deskripsi Project
Aplikasi blog ini dirancang untuk memberikan pengguna pengalaman komprehensif dalam mengelola konten blog. Platform ini memungkinkan pengguna untuk membuat, membaca, memperbarui, dan menghapus (CRUD) postingan blog melalui antarmuka pengguna yang responsif dan modern. Proyek ini memanfaatkan pendekatan full-stack, di mana backend menangani logika bisnis dan pengelolaan data, sementara frontend menyediakan antarmuka pengguna yang dinamis.

Aplikasi ini juga dilengkapi dengan fitur autentikasi untuk memastikan keamanan akses dan otorisasi. Dengan menggunakan teknologi terkini, aplikasi blog ini dirancang untuk mudah dipelihara, dikembangkan, dan digunakan oleh pengguna.

## 2. Tujuan Project
Tujuan dari pengembangan aplikasi ini adalah:
1. Memberikan platform yang sederhana namun fungsional untuk manajemen blog.
2. Memanfaatkan teknologi web modern untuk menciptakan pengalaman pengguna yang mulus.
3. Menyediakan sistem keamanan berbasis autentikasi dan otorisasi.
4. Menyediakan antarmuka yang responsif untuk mendukung pengguna di berbagai perangkat.


## 3. Teknologi yang Digunakan
### a. Backend
1. Node.js:
Lingkungan runtime untuk menjalankan JavaScript di server.
Digunakan untuk membangun server aplikasi yang skalabel dan ringan.

2. Express.js:
Framework untuk membangun aplikasi web dengan Node.js.
Mendukung pembuatan rute API dan middleware dengan efisien.

3. MongoDB:
Database NoSQL untuk menyimpan data berbasis dokumen.
Data disimpan dalam format JSON untuk fleksibilitas.

5. JSON Web Tokens (JWT):
Standar untuk autentikasi pengguna dengan token.
Token ini memungkinkan komunikasi yang aman antara frontend dan backend.

6. Mongoose
Library untuk mempermudah interaksi dengan MongoDB melalui model skema.

### b Library dan Dependecies Backend
1. Body-parser
Middleware untuk mem-parsing data HTTP request, seperti JSON atau form-urlencoded.

2. Cors
Untuk mengelola Cross-Origin Resource Sharing pada API.

3. Dotenv
Untuk memuat variabel lingkungan (environment variables).

4. Express-validator
Library validasi input untuk API backend.

5. Nodemon
Tools untuk pengembangan backend yang memungkinkan server restart otomatis saat file diperbarui.


### c. FrontEnd
1. React (Versi: 19.0.0-rc-66855b96-20241106)
Library untuk membangun antarmuka pengguna berbasis komponen.

2. React DOM (Versi: 19.0.0-rc-66855b96-20241106)
Berfungsi untuk merender elemen React ke dalam DOM browser.

3. React Router DOM (Versi: 7.1.1)
Library untuk navigasi dan manajemen routing dalam aplikasi React.

4. React Quill New (Versi: 3.3.3)
Library untuk implementasi rich text editor.

5. ImageKitio React (Versi: 4.2.0)
Digunakan untuk pengelolaan dan transformasi gambar secara dinamis melalui layanan ImageKit.

6. @clerk/clerk-react (Versi: 5.21.0)
Library untuk autentikasi dan manajemen pengguna.

7. Axios
Library untuk melakukan permintaan HTTP.
Digunakan untuk berkomunikasi dengan backend.

### Tools Pendukung
1. Git
Sistem kontrol versi untuk kolaborasi dan manajemen proyek.

2. Visual Studio Code (VS Code)
Editor kode untuk pengembangan.

3. Postman
Digunakan untuk pengujian API backend.

4. ImageKit.io
Layanan CDN dan pengelolaan gambar.

5. Clerk
Layanan autentikasi dan manajemen pengguna berbasis cloud.

6. npm
Pengelola paket untuk menginstal dan mengelola dependensi.

## 4.  Ringkasan Alur Teknologi
1. Frontend dibangun menggunakan React dengan dukungan dari library seperti React Router DOM untuk routing, React Quill New untuk rich text editor, dan ImageKitio React untuk pengelolaan gambar.
2. Backend menggunakan Node.js dengan Express.js untuk membangun API, MongoDB sebagai database, dan berbagai library untuk keamanan (JWT, bcrypt) dan validasi input (Express-validator).
3. Tools pendukung seperti Git, Postman, dan VS Code membantu pengembangan dan pengujian aplikasi.

## 5. Cara Instalasi
## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```

2. Navigate to the project directory:
   ```bash
   cd full-stack-blog
   ```

3. Install dependencies for both backend and frontend:
   ```bash
   # Install backend dependencies
   cd backend
   npm install

   # Install frontend dependencies
   cd ../client
   npm install
   ```



## 6. Fitur Aplikasi
1. CRUD Postingan Blog:
Pengguna dapat membuat, membaca, memperbarui, dan menghapus postingan.
2. Autentikasi dan Otorisasi:
Sistem login dengan validasi berbasis token JWT.
3. Desain Responsif:
Antarmuka yang mendukung berbagai ukuran layar.
4. Manajemen Akun Pengguna:
Setiap pengguna memiliki akun untuk mengelola postingannya.
5. Navigasi yang Mudah:
Pengguna dapat dengan mudah berpindah antar halaman melalui sistem routing.


## Cara Kerja Aplikasi
### a. Backend:
1. Autentikasi:
Pengguna mendaftar dengan memasukkan nama pengguna, email, dan kata sandi.
Kata sandi dienkripsi menggunakan bcrypt.js sebelum disimpan.
Setelah login, token JWT dibuat untuk mengelola sesi pengguna.

2. CRUD Data:
API REST menyediakan endpoint untuk setiap operasi CRUD.
Data disimpan dalam MongoDB dengan skema berbasis dokumen.

3. Middleware:
Middleware digunakan untuk memvalidasi token JWT pada permintaan yang memerlukan autentikasi.

### b. Frontend:
4. UI Interaktif:
Dibangun dengan React.js menggunakan pendekatan berbasis komponen.
Komponen seperti form, daftar postingan, dan halaman detail terintegrasi dengan backend.
5. Manajemen State:
Redux digunakan untuk mengelola state, memastikan sinkronisasi antara UI dan data.
6. Permintaan API:
Axios digunakan untuk mengirimkan permintaan ke API backend.
Token JWT dilampirkan pada header untuk endpoint yang dilindungi.

## 7. Alur Penggunaan
1. Halaman Utama:

Pengguna melihat daftar semua postingan yang tersedia.
2. Login/Signup:

Pengguna baru mendaftar, dan pengguna yang ada login dengan kredensial mereka.
3. Dashboard Pengguna:

Pengguna dapat membuat postingan baru, serta mengedit atau menghapus postingan yang sudah ada.
4. Halaman Detail Postingan:

Pengguna dapat melihat detail postingan dengan membaca kontennya secara lengkap.
5. Logout:

Pengguna dapat keluar dari akun mereka, dan token JWT dihapus.

## 8. Struktur Folder
full-stack-blog/
├── backend/         # Kode backend
│   ├── models/      # Skema database
│   ├── routes/      # Endpoint API
│   ├── controllers/ # Logika bisnis
│   ├── middleware/  # Middleware autentikasi
│   └── server.js    # Server utama
├── client/          # Kode frontend
│   ├── src/         # Kode sumber React.js
│   │   ├── components/ # Komponen antarmuka pengguna
│   │   ├── routes/       # route Halaman 
│   │   └── layout/       # Manajemen layout
│   └── public/      # File statis
├── .git/            # Metadata Git
├── package.json     # Konfigurasi proyek
└── README.md        # Dokumentasi

## 9. Kesimpulan
Aplikasi blog full-stack ini dirancang untuk memberikan pengguna pengalaman pengelolaan blog yang efisien dan aman. Dengan memanfaatkan teknologi modern seperti Node.js, React.js, dan MongoDB, aplikasi ini mampu memberikan performa yang tinggi sekaligus kemudahan dalam penggunaan. Proyek ini juga fleksibel untuk dikembangkan lebih lanjut, baik dalam hal fitur maupun skalabilitas.






