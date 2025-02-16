# Perintah Dasar di Docker

Dokumentasi ini menjelaskan perintah dasar yang digunakan untuk membangun, mengelola, dan memeriksa container serta image di Docker. Perintah-perintah ini akan membantu Anda dalam mengelola proyek dan lingkungan container dengan lebih mudah.

## 1. Membangun dan Menjalankan Docker

### Membangun Image Docker

Untuk membangun image Docker dari file `Dockerfile`, gunakan perintah berikut:

```sh
docker build -t <Nama-Proyek> .
```

Keterangan:

- `-t <Nama-Proyek>`: Menandai image yang dibangun dengan nama yang Anda tentukan (misalnya `my-app`).
- Titik (`.`) menunjukkan lokasi `Dockerfile`, yaitu direktori saat ini.

### Menjalankan Container

Setelah image selesai dibangun, Anda dapat menjalankan container menggunakan image tersebut dengan perintah:

```sh
docker run <Nama-Proyek>
```

Keterangan:

- `<Nama-Proyek>`: Nama image yang ingin dijalankan.

## 2. Menghapus Image dan Container

### Menghapus Image

Untuk menghapus image Docker, Anda dapat menggunakan beberapa perintah berikut:

- Menghapus image berdasarkan ID:

  ```sh
  docker rmi <IMAGE_ID>
  ```

- Menghapus semua image yang tidak digunakan (tag `<none>`):

  ```sh
  docker image prune -f
  ```

- Menghapus semua image yang ada:

  ```sh
  docker rmi $(docker image ls -q)
  ```

### Menghapus Container

Untuk menghapus container yang sudah ada, Anda dapat menggunakan beberapa perintah berikut:

- Menghapus container berdasarkan ID:

  ```sh
  docker rm <CONTAINER_ID>
  ```

- Menghapus semua container yang berhenti:

  ```sh
  docker container prune
  ```

- Menghapus semua container yang ada:

  ```sh
  docker rm $(docker container ls -aq)
  ```

## 3. Memeriksa Status dan ID Image dan Container

### Cek Container Berdasarkan Image

Untuk melihat container yang dijalankan berdasarkan image tertentu, gunakan perintah berikut:

```sh
docker ps -a --filter ancestor=<IMAGE_ID>
```

Keterangan:

- `<IMAGE_ID>`: ID image yang digunakan untuk memfilter container.

### Cek Seluruh ID Image

Untuk melihat seluruh ID image yang ada di sistem:

```sh
docker images -q
```

Atau:

```sh
docker image ls -q
```

### Cek Seluruh ID Container

Untuk melihat seluruh ID container yang ada di sistem:

```sh
docker container ls -aq
```

## 4. Menghentikan dan Menjalankan Container

### Menghentikan Semua Container

Untuk menghentikan semua container yang sedang berjalan, gunakan perintah berikut:

```sh
docker stop $(docker ps -aq)
```

### Menghentikan Semua Container Menggunakan Docker Compose

Jika Anda menggunakan Docker Compose, untuk menghentikan semua container yang dikelola oleh Compose:

```sh
docker-compose down
```

### Menjalankan Semua Container yang Dihentikan

Untuk menjalankan kembali semua container yang sebelumnya dihentikan, gunakan:

```sh
docker-compose start
```

## 5. Menggunakan Bash atau Shell di Dalam Container

### Akses Bash di Container (Untuk Image Umum)

Untuk masuk ke dalam container yang berjalan dan menggunakan shell Bash, gunakan perintah berikut:

```sh
docker exec -it <nama-container> bash
```

Keterangan:

- `<nama-container>`: Nama atau ID container yang ingin diakses.

### Akses MySQL di Dalam Container

Jika Anda ingin mengakses database MySQL yang berjalan di dalam container, gunakan perintah berikut:

```sh
docker exec -it <nama-container> mysql -u root -p<password> -e "SHOW DATABASES;"
```

Keterangan:

- `<nama-container>`: Nama atau ID container yang menjalankan MySQL.
- `<password>`: Kata sandi untuk pengguna `root` di MySQL.

## 6. Memeriksa Status dan Log Container

### Memeriksa Status Container

Untuk memeriksa apakah container sudah berjalan:

```sh
docker ps
```

Jika tidak ada container yang sedang berjalan, Anda bisa memeriksa status seluruh container (termasuk yang berhenti) dengan:

```sh
docker ps -a
```

- Jika container ada tetapi statusnya "Exited", itu berarti container pernah berjalan tetapi sekarang sudah berhenti. Anda bisa memulai ulang container dengan perintah berikut:

```sh
docker start <nama_container>
```

Jika tidak ada container yang berjalan sama sekali, jalankan container dengan perintah:

```sh
docker-compose up -d
```

Atau, jika Anda ingin membangun ulang container:

```sh
docker-compose up --build -d
```

---
