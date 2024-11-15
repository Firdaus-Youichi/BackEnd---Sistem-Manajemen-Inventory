# Anggota Kelompok

Firdaus Youichi Yamamoto (A11.2022.14607)

# Manajemen Inventaris

Proyek ini adalah web app manajemen penyimpanan dengan menggunakan web framework Django, relational database PostgreSQL, dan dikontainerisasi menggunakan Docker.

# Fitur

1. Dashboard Ringkasan Sistem (Kategori, Item, Suppliers, Laporan stok minimal)
2. Manajemen Kategori (Create, Read) 
3. Manajemen Item (Create, Read)
4. Manajemen Suppliers (Create, Read)

# Teknologi

1. Django
2. PostgreSQL
3. HTML dan Bootstrap CSS
4. Docker

# Cara Menjalankan Proyek

1. Pastikan memiliki software Docker Desktop dan menggunakan VSCode Extension PostgreSQL(Weijan Chen)

2. Git clone repositori ini

3. Jika ada folder "postgres_data" hapus foldernya.

4. Set terminal dengan folder yang ada file docker-compose.yml dan run syntax-nya
    <pre>docker-compose up -d --build</pr> 

5. Jika sudah ada images dan container di Docker Desktop dan semua container jalan, maka sudah berhasil.

6. Buka extension PostgreSQL, lalu koneksikan sesuai yang ada di file docker-compose.yml

5. Mulai ulang kontainer docker
   <pre>docker-compose down</pre>
   <pre>docker-compose restart</pre>

6. Buka Docker Desktop, lalu buka container web_uts_test dan ketik syntax di bagian Exec
    <pre>python manage.py makemigrations</pre>
    <pre>python manage.py migrate</pre>
    <pre>python importer.py</pre>

6. Akses Aplikasi
   - Untuk mengakses web, Anda dapat mengunjungi http://localhost:8000 (Tergantung port yang diatur) dengan cara klik kanan containers web_uts_test dan klik open in browser. Note: Jika web tidak bisa dibuka, coba matikan semua container lalu hidupkan kembali secara manual di Docker Desktop
   - Untuk dapat menambahkan kategori, item, dan suppliers Anda harus masuk ke halaman Admin dan melakukan login.

7. Masuk ke halaman Admin

   - Login menggunakan akun Admin yang tersedia di table auth_user ataupun di Admins.csv
   - Setelah login Anda bisa klik pada view site untuk beralih ke halaman dashboard.
   - Sekarang Anda dapat menambahkan item, kategori, dan juga supplier.
