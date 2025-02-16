# Implementasi Docker di Aplikasi Microservices

"Implementasi Docker di Aplikasi Microservices" adalah repositori demonstrasi yang lengkap untuk menunjukkan kemampuan Docker dan Docker Compose. Dengan fokus pada kesederhanaan dan efisiensi, proyek ini menggambarkan integrasi kontainer Docker untuk menyebarkan aplikasi full-stack.

Repositori ini menampilkan aplikasi frontend React.js di mana pengguna dapat memasukkan data mereka dan mengirimkannya. Data yang dikirimkan kemudian diproses dan disimpan dengan aman di server backend Node.js, yang menyimpannya di dalam database MySQL. Dengan memanfaatkan Docker Compose, seluruh stack aplikasi, termasuk frontend, backend, dan database, dapat dikelola dan dijalankan dengan mudah sebagai kontainer yang terisolasi.

## Persiapan

Untuk memulai proyek ini, ikuti langkah-langkah berikut:

### Prasyarat

Sebelum menjalankan proyek, pastikan Anda sudah menginstal hal-hal berikut:

- Docker: [Unduh dan Install Docker](https://docs.docker.com/get-docker/)
- Git: [Unduh dan Install Git](https://git-scm.com/downloads)
- Node: [Unduh dan Install Node](https://nodejs.org/en/download)

### Instalasi

1. **Clone Repositori**

   Clone repositori dengan perintah berikut:

   ```shell
   git clone --recurse-submodules https://github.com/panntod/MV-Github-Project.git
   ```

   Jika ada satu atau lebih submodule yang gagal saat proses cloning, jalankan perintah berikut untuk clone manual sesuai submodule yang gagal:

   ```shell
   # clone submodule frontend
   rm -rf ./frontend && git submodule update --recursive --remote ./frontend

   # clone submodule solution core
   rm -rf ./backend && git submodule update --recursive --remote ./backend
   ```

2. **Install Dependencies**

   Install semua dependency yang dibutuhkan dengan menjalankan:

   ```shell
   npm install
   ```

3. **Setup Variabel Lingkungan**

   Ganti nama file `.env.example` menjadi `.env`:

   ```shell
   cp .env.example .env
   ```

## Penggunaan

Contoh ini merupakan sumber daya yang ramah pemula untuk mempelajari tentang kontainerisasi full-stack menggunakan Docker dalam aplikasi praktis. Ini menyediakan implementasi sederhana di aplikasi full-stack menggunakan React.js, Node.js, dan MySQL, yang dikelola menggunakan Docker Compose. Untuk setup lebih lanjut bisa membaca dokumentasi [Langkah-Langkah Set Up Project menggunakan Docker Compose](/docs/_docker/DOCKER_COMPOSE.md)
