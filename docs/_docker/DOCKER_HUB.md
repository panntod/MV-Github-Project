# Mengunggah Docker Image ke Docker Hub

Dokumen ini menjelaskan langkah-langkah untuk membangun dan mengunggah Docker image ke Docker Hub.

---

## 1. Membuat Akun

Daftar atau masuk ke [Docker Hub](https://hub.docker.com) untuk mendapatkan akses ke repositori image.

---

## 2. Membuat Repositori

Buat repositori baru di Docker Hub untuk setiap image yang akan diunggah.

---

## 3. Login ke Docker Hub

Gunakan perintah berikut untuk masuk ke akun Docker Hub:

```bash
docker login
```

Masukkan kredensial akun saat diminta.

---

## 4. Membangun Image dengan Tag

Gunakan perintah berikut untuk membangun image dengan tag yang sesuai dengan repositori di Docker Hub.

```bash
# Membangun image untuk backend
docker build -t panntod/mv-docker-backend:latest ./backend

# Membangun image untuk frontend
docker build -t panntod/mv-docker-frontend:latest ./frontend
```

---

## 5. Mengunggah Image ke Docker Hub

Setelah berhasil membangun image, gunakan perintah berikut untuk mengunggahnya ke Docker Hub.

```bash
docker push panntod/mv-docker-backend:latest
docker push panntod/mv-docker-frontend:latest
```

Pastikan setiap image telah berhasil diunggah dengan memeriksa di Docker Hub.
