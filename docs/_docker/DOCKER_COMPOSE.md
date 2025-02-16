# Langkah-Langkah Set Up Project menggunakan Docker Compose

Dokumentasi ini menjelaskan langkah-langkah yang diperlukan untuk menyiapkan, menjalankan, dan melakukan debugging container Docker menggunakan `docker-compose`. Langkah-langkah ini mencakup pembuatan submodule Git, build image Docker, dan cara-cara lainnya untuk memastikan aplikasi berjalan dengan lancar.

## Langkah-langkah Persiapan

### 1. Membuat Git Submodule

- Buat git submodule untuk menghubungkan repositori yang diperlukan dalam proyek Anda.

### 2. Clone Backend (BE) dan Frontend (FE)

- Clone repositori untuk bagian backend (BE) dan frontend (FE) proyek Anda.

### 3. Jalankan Build untuk Memastikan Tidak Ada Error

- Coba jalankan build untuk memastikan bahwa tidak ada error atau masalah yang muncul dalam proses build aplikasi.

### 4. Tambahkan `.dockerignore`

- Pastikan Anda menambahkan file `.dockerignore` untuk mengecualikan file atau folder yang tidak diperlukan saat membangun image Docker, seperti folder build atau node_modules.

### 5. Buat Dockerfile di Masing-masing Folder

- Buat file `Dockerfile` di masing-masing folder (misalnya, folder backend dan frontend). Untuk proyek dengan struktur lebih kompleks, file `Dockerfile` bisa ditempatkan di direktori root jika diperlukan.

### 6. Buat `docker-compose.yml`

- Buat file `docker-compose.yml` untuk mengonfigurasi layanan dan container yang dibutuhkan dalam aplikasi Anda.

Jika anda tertarik membaca lanjut docker-compose.yml tersedia di [Docker Compose Documentation](https://docs.docker.com/compose/)

## Deployment

Setelah semua persiapan selesai, Anda dapat memulai container dan layanan menggunakan `docker-compose`.

### Menjalankan Layanan di Background

```sh
docker-compose up -d
```

Keterangan:

- `-d` (detached mode) memastikan container berjalan di latar belakang, sehingga terminal tetap bisa digunakan untuk perintah lain.

### Membangun Ulang Image Docker

```sh
docker-compose up --build
```

Keterangan:

- Perintah ini memaksa Docker untuk membangun ulang image dari `Dockerfile`, bahkan jika image yang sama sudah ada sebelumnya.

### Membangun Tanpa Cache

```sh
docker-compose up --no-cache
```

Keterangan:

- `--no-cache` memastikan bahwa Docker tidak menggunakan cache build sebelumnya dan menjalankan setiap langkah dalam `Dockerfile` dari awal.

## Debugging

Jika container tidak berjalan sebagaimana mestinya atau Anda perlu memeriksa log untuk masalah tertentu, gunakan beberapa perintah berikut:

### Melihat Log dari Layanan yang Dijalankan oleh `docker-compose`

```sh
docker-compose logs
```

Perintah ini akan menampilkan log dari seluruh layanan yang dijalankan oleh `docker-compose`.

Menambahkan log dalam aplikasi sangat penting untuk melakukan debug dan memantau aplikasi yang berjalan. Berikut adalah beberapa cara untuk menambahkan log:

1. **Log dari Container**:
   Gunakan perintah `docker logs` untuk melihat log output dari container yang sedang berjalan.

2. **Menggunakan Volumes untuk Log**:
   Anda dapat mengonfigurasi Docker untuk menyimpan log aplikasi dalam volume atau direktori lokal agar lebih mudah diakses.

3. **Menggunakan Alat Pemantauan**:
   Pertimbangkan untuk menggunakan alat pemantauan dan logging seperti ELK Stack (Elasticsearch, Logstash, Kibana) atau Grafana untuk memantau log dari seluruh container dan aplikasi.

---
