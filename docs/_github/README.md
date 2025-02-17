# 🚀 GITHUB ACTIONS

## 🔰 Dasar-Dasar GitHub Actions

✅ **Apa itu GitHub Actions?**  
GitHub Actions adalah layanan otomatisasi CI/CD yang memungkinkan kamu menjalankan skrip dan tugas secara otomatis di repository GitHub. Dengan ini, kamu bisa membangun, menguji, dan menerapkan kode dengan lebih efisien! 🎯

✅ **Memahami Workflow, Job, dan Step**

- **Workflow** 🛠️: Proses otomatisasi yang dieksekusi berdasarkan event tertentu.
- **Job** 💼: Sekumpulan langkah (steps) yang dijalankan dalam satu runner.
- **Step** 🔄: Perintah atau tindakan yang dijalankan dalam satu job.

✅ **Konsep Triggering Event di GitHub Actions**  
GitHub Actions berjalan berdasarkan event yang terjadi di repository, seperti:

- 📌 `push` → Ketika kode di-push ke repository.
- 🔄 `pull_request` → Saat ada PR yang dibuat atau diperbarui.
- ⏰ `schedule` → Menjalankan workflow berdasarkan jadwal tertentu.
- 🏗️ `workflow_dispatch` → Workflow dijalankan secara manual oleh pengguna.

✅ **Menyusun File YAML untuk GitHub Actions**  
GitHub Actions dikonfigurasi menggunakan file `.yml` yang diletakkan di `.github/workflows/`. Contoh sederhana:

```yaml
ame: CI Pipeline
on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v5

      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: 18

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test
```

Dengan konfigurasi ini, setiap kali ada push atau PR, GitHub Actions akan menjalankan workflow untuk:

1. 🔍 Mengecek repository
2. ⚙️ Menyiapkan Node.js
3. 📦 Menginstal dependencies
4. ✅ Menjalankan unit test

---
