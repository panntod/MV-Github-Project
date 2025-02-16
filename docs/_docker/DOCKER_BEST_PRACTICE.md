# Best Practices for Writing Dockerfiles

Berikut adalah beberapa praktik terbaik saat menulis Dockerfile agar lebih aman, efisien, dan optimal.

---

## 1️. **Gunakan Base Image Resmi**

Selalu gunakan **official images** dari Docker Hub untuk memastikan keamanan dan dukungan yang baik.

- **Contoh:**

```dockerfile
FROM node:18-alpine
```

---

## 2️. **Gunakan Versi Spesifik, Hindari `latest`**

Hindari penggunaan tag `latest` karena dapat menyebabkan ketidakcocokan versi.

- **Contoh (Benar ✅)**

```dockerfile
FROM python:3.10
```

- **Contoh (Salah ❌)**

```dockerfile
FROM python:latest
```

---

## 3️. **Gunakan Base Image yang Ringan**

Gunakan versi **Alpine** atau **Slim** untuk mengurangi ukuran image.

- **Contoh:**

```dockerfile
FROM node:18-alpine
```

**Alpine** lebih ringan dibandingkan `node:18` yang menggunakan Debian.

---

## 4️. **Optimalkan Caching Layer**

Docker membangun image berdasarkan layer, jadi urutkan perintah agar memanfaatkan cache sebaik mungkin.

- **Contoh:**

```dockerfile
# COPY package.json lebih awal agar cache layer npm install tetap digunakan
COPY package.json package-lock.json ./
RUN npm install
COPY . .
```

---

## 5️. **Gunakan `.dockerignore`**

Agar build lebih cepat, tambahkan file yang tidak perlu ke `.dockerignore`.

- **Contoh `.dockerignore`**

```env
node_modules
.git
.env
```

---

## 6️. **Gunakan Multi-Stage Build**

Multi-Stage Build membantu mengurangi ukuran image akhir dengan hanya menyertakan file yang diperlukan.

- **Contoh:**

```dockerfile
# Stage 1: Build
FROM node:18-alpine AS builder
WORKDIR /app
COPY . .
RUN npm install && npm run build

# Stage 2: Production
FROM nginx:alpine
COPY --from=builder /app/dist /usr/share/nginx/html
```

---

## 7️. **Gunakan User dengan Hak Terbatas**

Hindari menjalankan container sebagai `root` untuk keamanan.

- **Contoh:**

```dockerfile
RUN addgroup -S appgroup && adduser -S appuser -G appgroup
USER appuser
```

---

## 8️. **Lakukan Scanning Keamanan pada Image**

Gunakan alat seperti **Trivy** atau **Docker Scout** untuk memeriksa kerentanan dalam image.

- **Contoh scanning dengan Trivy:**

```bash
trivy image my-docker-image
```

---
