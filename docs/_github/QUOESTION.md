# Questioning

---

## 🛠️ **DASAR GITHUB ACTIONS**

**1.** Apa itu GitHub Actions dan bagaimana cara kerjanya?  
**2.** Apa perbedaan antara `workflow`, `job`, dan `step` dalam GitHub Actions?  
**3.** Apa itu trigger event dalam GitHub Actions, dan bagaimana cara mengonfigurasi trigger untuk menjalankan workflow hanya pada event tertentu (seperti `push`, `pull_request`, atau `schedule`)?  
**4.** Bagaimana cara mendefinisikan environment dan secrets dalam GitHub Actions, dan untuk apa mereka digunakan?

---

## 🔀 **WORKFLOW AND JOB**

**5.** Bagaimana cara membuat workflow yang mengeksekusi beberapa jobs secara paralel dan mengonfigurasi dependensi antar jobs?  
**6.** Apa perbedaan antara `runs-on` dan `strategy.matrix` dalam GitHub Actions? Kapan sebaiknya menggunakan masing-masing?  
**7.** Bagaimana cara mengatur job untuk hanya berjalan pada branch tertentu (misalnya `main` atau `develop`)?  
**8.** Apa itu `continue-on-error` dalam GitHub Actions, dan kapan sebaiknya digunakan?

---

## 🐳 **DOCKER IN GITHUB ACTIONS**

**9.** Bagaimana cara menggunakan Docker dalam GitHub Actions untuk membangun dan menjalankan container?  
**10.** Apa itu `docker/setup-buildx-action`, dan bagaimana cara menggunakannya dalam GitHub Actions?  
**11.** Bagaimana cara memanfaatkan cache Docker di GitHub Actions untuk mempercepat build?  
**12.** Bagaimana cara login ke Docker Hub atau registry lainnya menggunakan GitHub Actions?

---

## ✅ **AUTOMATION BUILD AND TEST**

**13.** Bagaimana cara mengonfigurasi GitHub Actions untuk menjalankan unit tests (misalnya menggunakan Jest, Mocha, atau lainnya)?  
**14.** Apa itu `matrix` dalam GitHub Actions, dan bagaimana cara menggunakannya untuk menjalankan build dan test pada berbagai versi Node.js atau OS secara paralel?  
**15.** Bagaimana cara menggunakan caching dalam GitHub Actions untuk mempercepat instalasi dependencies, seperti `node_modules` di aplikasi Node.js?  
**16.** Bagaimana cara memastikan bahwa workflow berhenti jika ada kesalahan saat build atau test?

---

## 🔒 **SECURITY AND BEST PRACTICE**

**17.** Bagaimana cara mengelola `secrets` dan memastikan mereka tetap aman dalam workflow GitHub Actions?  
**18.** Apa itu `GITHUB_TOKEN`, dan bagaimana cara menggunakan token ini untuk autentikasi API di dalam workflow?  
**19.** Apa itu `permissions` dalam GitHub Actions dan bagaimana cara mengonfigurasi akses terbatas ke repository?  
**20.** Apa itu `workflow_run` dan bagaimana cara menggunakannya untuk menjalankan workflow lain setelah satu workflow selesai?

---

## ☁️ **MANAGEMENT AND DEPLOYMENT**

**21.** Bagaimana cara men-deploy aplikasi ke cloud (misalnya AWS, Azure, GCP) menggunakan GitHub Actions?  
**22.** Apa itu `actions/upload-artifact` dan `actions/download-artifact`, dan bagaimana cara menggunakannya untuk mentransfer file antar jobs?  
**23.** Bagaimana cara melakukan deployment otomatis ke Kubernetes menggunakan GitHub Actions?  
**24.** Bagaimana cara menggunakan GitHub Actions untuk mengelola multi-environment deployment (misalnya staging dan production)?

---

## 🔥 **ADVANCE GITHUB ACTIONS**

**25.** Bagaimana cara menggunakan self-hosted runners dalam GitHub Actions, dan kapan harus menggunakannya dibanding hosted runners?
**26.** Bagaimana cara membuat custom GitHub Actions menggunakan JavaScript atau Docker?
**27.** Apa itu composite actions, dan bagaimana cara menggunakannya untuk mengelompokkan beberapa langkah dalam satu action?
**28.** Bagaimana cara menangani concurrency dalam GitHub Actions untuk mencegah dua workflow berjalan secara bersamaan pada branch yang sama?
**29.** Apa itu dynamic matrix strategy, dan bagaimana cara membuat workflow yang secara dinamis menentukan jumlah job berdasarkan kebutuhan runtime?
**30.** Bagaimana cara menggunakan OIDC (OpenID Connect) untuk autentikasi ke cloud provider seperti AWS tanpa menggunakan credentials statis dalam secrets?
**31.** Bagaimana cara mengintegrasikan GitHub Actions dengan Terraform untuk mengelola infrastruktur sebagai kode (IaC)?
**32.** Bagaimana cara membuat GitHub Actions yang dapat dipanggil dari repo lain menggunakan reusable workflows?
**33.** Apa itu "Idempotent Workflows", dan bagaimana cara mendesain workflow yang dapat dijalankan berkali-kali tanpa efek samping yang tidak diinginkan?

---

## 🎯 **OPTIMIZATION AND TROUBLESHOOTING**

**34.** Bagaimana cara memantau dan mendiagnosis masalah dalam workflow GitHub Actions?
**35.** Apa itu workflow status dan bagaimana cara menambahkan status laporan ke workflow?
**36.** Apa saja fitur yang dapat membantu mempercepat waktu eksekusi workflow (seperti caching, matrix, dan reusable workflows)?
**37.** Bagaimana cara menangani error dan kegagalan dalam workflow, misalnya dengan retry atau menambahkan pengaturan kondisi untuk langkah-langkah tertentu?

---
