# README.md

## 🚀 Website Rumah Sakit

Website yang menggunakan WordPress dan beberapa plugin untuk membangunnya. Website ini diperuntukkan untuk tes kompetensi PT. Inova Medika Solusindo.

## 📥 Instalasi WordPress dari GitHub

Berikut langkah untuk menginstal file WordPress dari GitHub ke server atau localhost:

### **1. Clone Repository WordPress**

Pastikan Git sudah terinstal, lalu jalankan:

```
git clone https://github.com/tatangbukhori/Website_Rumah_Sakit.git
```

Ini akan mengunduh file project wordpress.

### **2. Pindahkan Folder ke Direktori Server**

Jika menggunakan XAMPP/WAMP/Laragon:

- Pindahkan folder **WordPress/** ke
  - `htdocs/` untuk xampp atau
  - &#x20;`www/` untuk laragon
- Ubah nama folder menjadi nama proyek, misalnya: `rs-sehat-utama`

### **3. Buat Database Baru**

Masuk ke phpMyAdmin/HeidiSQL → buat database:

```
db_rssu
```

Tanpa tabel.

### **4. Konfigurasi wp-config.php**

Masuk ke folder WordPress hasil clone:

- Duplikat `wp-config-sample.php`
- Rename menjadi `wp-config.php`
- Edit bagian berikut:

```
define( 'DB_NAME', 'db_rssu' );
define( 'DB_USER', 'root' );
define( 'DB_PASSWORD', '' );
define( 'DB_HOST', 'localhost' );
```

penggunaan akun database "root" hanya untuk penggunaan secara lokal, karena root merupakan otoritas akun tertinggi yang dapat mengancam keamanan database apabila disalahgunakan.

### **5. Jalankan Instalasi WordPress**

Akses:

```
http://localhost/rs-sehat-utama
```

Isi:

- Nama situs, contoh Rumah Sakit Sehat Utama
- Username = admin
- Password = admin
- Email

### **6. Upload Theme & Plugins Proyek**

Masukkan theme dan plugin ke:

```
wp-content/themes/
wp-content/plugins/
```

Aktifkan semuanya melalui Dashboard.

---

## 📦 **Plugins yang Digunakan**

Berikut plugin yang digunakan dalam pengembangan website ini:

### **1. Greenshift**

- Digunakan untuk membangun layout modern, animasi, dan style visual.
- Mendukung block builder modular.
- Beberapa fitur dynamic data membutuhkan addon premium.

### **2. Meta Box (Metabox)**

- Framework utama untuk membuat custom fields.
- Digunakan untuk menyimpan data dokter seperti: spesialis, jadwal, kontak, deskripsi.

### **3. MB Custom Post Types**

- Untuk membuat Custom Post Type (CPT), seperti:
  - **Dokter**

### **4. Meta Field Block**

- Memungkinkan menampilkan custom field Meta Box ke halaman.
- Cara gratis untuk menampilkan field secara dinamis.

### **5. Advanced Custom Types**

- Plugin tambahan untuk pembuatan field type.

### **6. Advanced Query Loop**

- Memungkinkan membuat daftar dinamis dari CPT (misalnya daftar dokter).
- Digunakan sebagai alternatif Query Loop bawaan.

### **7. Breadcrumb NavXT**

- Menampilkan breadcrumb navigasi untuk memudahkan pengguna.

### **8. Contact Form 7**

- Formulir kontak utama.

### **9. Info Cards**

- Menampilkan kartu informasi memakai layout card modern.

---

## 🏥 **Struktur Custom Post Types**

### **CPT: Dokter**

Digunakan untuk menampilkan daftar dokter beserta jadwalnya.

**Title (Meta Box):**

- Berisi nama dokter

**Field (ACF):**

- `spesialis` — Spesialisasi dokter
- `jadwal_praktik` — Informasi jadwal praktik dokter di RS
- `kontak` — Berisi informasi kontak dokter
- `deskripsi` — Menjelaskan posisi dokter

---

## 📁 **Struktur Halaman Utama**

- **Home** → hero, CTA (Layanan & Lokasi RS), Layanan Kami
- **Layanan** → halaman list layanan yang tersedia
- **Dokter** → halaman daftar dan jadwal dokter
- **Kontak** → form kontak rumah sakit & janji temu
- **Lokasi** -> halaman lokasi dan kontak darurat rumah sakit

---

## 🧩 **Dynamic Data Setup**

Karena Greenshift dynamic data beberapa harus premium, maka alternatif gratis:

### **Menampilkan Data Dokter Menggunakan Advanced Query Loop**

- Gunakan **Advanced Query Loop** untuk looping menampilkan data dokter yang tersedia
- Pilih **Template**
- Hapus untuk block yang tidak terpakai
- Gunakan **Meta Field Block** untuk menampilkan field tambahan

## 🎨 **Info Cards Setup**

Info Cards digunakan untuk daftar layanan:

- Gunakan block Info Card dari plugin **Info Cards**
- Isi semua element yang ada

## 📎 **Breadcrumbs**

Breadcrumb NavXT otomatis menampilkan struktur navigasi untuk CPT.

- Tambahkan block Breadcrumb ke halaman.

---

Dokumentasi ini dapat diperbarui sesuai kebutuhan proyek.

