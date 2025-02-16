# 🐳 Docker Tutorial

**Docker Version:** `27.4.0`

---

## 📌 Apa Itu Docker?

Docker adalah platform untuk **membangun, menjalankan, dan mengirimkan aplikasi** dalam lingkungan yang terisolasi. Dengan Docker, kita dapat:

✅ Menghindari **ketidaksesuaian versi software**  
✅ Menjalankan berbagai **konfigurasi aplikasi** tanpa konflik  
✅ **Mengemas aplikasi** agar berjalan di mana saja  
✅ Menggunakan berbagai **versi library** pada satu mesin  
✅ **Mengotomatisasi** konfigurasi dan deployment

## 🔍 Perbedaan Docker vs VM

| **Docker (Container)**                           | **Virtual Machine (VM)**          |
| ------------------------------------------------ | --------------------------------- |
| Lingkungan terisolasi untuk menjalankan aplikasi | Abstraksi dari mesin fisik        |
| Berbagi kernel dengan host                       | Memiliki kernel sendiri           |
| Ringan dan cepat                                 | Lebih berat karena butuh OS penuh |
| Startup dalam hitungan detik                     | Startup lebih lama                |

---

## ⚙️ Docker Architecture

Docker memiliki arsitektur yang terdiri dari tiga komponen utama:

```text
Client → REST API → Docker Engine (Server)
```

1. **Client**: Tempat kita menjalankan perintah Docker (CLI atau UI).
2. **REST API**: Jembatan komunikasi antara client dan Docker Engine.
3. **Docker Engine (Server)**: Menjalankan dan mengelola container.

### Konsep Penting

- **Container** adalah sebuah **proses yang berjalan secara terisolasi** di dalam sistem.
- **Docker Daemon** bertanggung jawab untuk membuat, menjalankan, dan mengelola container.
- **Kernel** tetap berbagi sumber daya dengan container, tetapi setiap container memiliki lingkungan eksekusi sendiri.

Dengan arsitektur ini, Docker dapat berjalan ringan dan cepat dibandingkan dengan virtual machine tradisional.

---

## 📦 Docker Image

Docker Image adalah **cetak biru (blueprint) dari container**, yang berisi semua yang dibutuhkan untuk menjalankan aplikasi.

### Apa yang Ada di Dalam Docker Image?

1. **OS Minimal** → Sistem operasi yang diperkecil agar lebih ringan.
2. **Runtime Environment** → Lingkungan untuk menjalankan aplikasi (misalnya Node.js, Python, dll.).
3. **Source Code Aplikasi** → File dan folder proyek yang diperlukan.
4. **Library & Dependencies** → Semua pustaka pihak ketiga yang dibutuhkan aplikasi.
5. **Environment Variables** → Konfigurasi yang dapat disesuaikan saat runtime.

### Workflow

1. **Dockerfile** → Menentukan cara membangun image.
2. **Docker Image** → Dibuat berdasarkan Dockerfile.
3. **Container** → Instance dari image yang sedang berjalan.

Didalam Dockerfile kita menggunakan format `.yml`, format yang hampir mirp dengan json

json format:

```json
{
  "name": "The Ultimate Docker Course",
  "price": 19,
  "is_published": true,
  "tags": ["sofware", "devops"],
  "author": {
    "first_name": "Pandhu",
    "midle_name": "Arya",
    "last_name": "Munjalindra"
  }
}
```

yaml format:

```yaml
---
name: The Ultimate Docker Course
price: 19
is_published: true
tags:
  - sofware
  - devops
author:
  first_name: Pandhu
  midle_name: Arya
  last_name: Munjalindra
```

mengapa tidak selalu menggunakan yaml, karena parse yaml lebih lama dan rumit dibandingkan memparse json. Untuk mengetahui lebih dalam tentang Dockerfile baca di [Dockerfile Reference](https://docs.docker.com/reference/dockerfile/)

---

### 📌 **Kesimpulan**

Docker adalah teknologi yang sangat berguna untuk mengemas, mengelola, dan mendistribusikan aplikasi dengan efisien. Dengan memahami konsep dasar seperti **Dockerfile, Image, Container, Networking, dan Scaling**, kita dapat membangun aplikasi yang lebih stabil, portabel, dan mudah dikelola.

#### Poin Penting yang Harus Diingat

1. **Optimasi Dockerfile sangat penting** untuk membuat image lebih ringan dan efisien.
2. **Networking dalam Docker** memungkinkan komunikasi antar-container menggunakan network yang sama.
3. **Scaling dengan Docker Compose** dapat digunakan untuk menjalankan beberapa instance dari service yang sama.
4. **ENTRYPOINT vs CMD** memiliki perbedaan penting dalam bagaimana command dieksekusi dalam container.
5. **Multi-Stage Build** membantu mengurangi ukuran image dan meningkatkan performa deployment.
