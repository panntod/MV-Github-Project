# Learning Docker - Kubernetes - GitHub Actions

Copy-Paste roadmap ini ke dalam notepad atau notian untuk digunakan sebagai tolak ukur kemampuan, Berikan [x] untuk setiap materi yang dirasa sudah paham

---

## DOCKER

### Dasar-Dasar Docker

[] Apa itu Docker?
[] Perbedaan Docker vs Virtual Machine
[] Arsitektur Docker (Client, Engine, Daemon, CLI, API)
[] Konsep Container, Image, Volume, dan Network

### Memulai dengan Docker

[] Instalasi Docker di berbagai OS (Windows, Mac, Linux)
[] Perintah dasar Docker (docker run, docker ps, docker stop, dll.)
[] Membuat dan menjalankan container dari Docker Hub
[] Menghapus container dan image yang tidak digunakan

### Dockerfile dan Image

[] Apa itu Dockerfile?
[] Menulis Dockerfile pertama
[] Docker Build: Cara membangun image kustom
[] Layering dalam Docker (cache & optimasi build)
[] Best practice dalam menulis Dockerfile
[] Tagging dan versioning image

### Container Lifecycle & Management

[] Start, Stop, Restart, dan Remove Container
[] Inspect & Logs Container (docker inspect, docker logs)
[] Masuk ke dalam Container (docker exec, docker attach)
[] Export dan Import Container

### Docker Volume & Persistent Data

[] Apa itu Volume dan Bind Mount?
[] Membuat dan mengelola volume (docker volume create, docker volume ls)
[] Menggunakan volume untuk menyimpan data aplikasi
[] Backup dan restore volume

### Networking dalam Docker

[] Docker Network Types (Bridge, Host, Overlay, None, Macvlan)
[] Membuat custom network (docker network create)
[] Menghubungkan beberapa container dalam satu jaringan
[] Menggunakan docker-compose untuk mengatur jaringan

### Docker Compose (Multi-Container Apps)

[] Apa itu Docker Compose?
[] Menulis docker-compose.yml pertama
[] Membangun dan menjalankan banyak container sekaligus
[] Scaling dengan Docker Compose (docker-compose up --scale)

## GITHUB ACTIONS

### Dasar-Dasar GitHub Actions

[] Apa itu GitHub Actions?  
[] Memahami Workflow, Job, dan Step  
[] Konsep Triggering Event di GitHub Actions  
[] Menyusun file YAML untuk GitHub Actions

### Membuat dan Mengelola Workflow

[] Menulis workflow pertama dengan GitHub Actions  
[] Menambahkan berbagai jenis Jobs dan Steps ke dalam Workflow  
[] Menggunakan Secrets dan Environments di GitHub Actions  
[] Memahami berbagai jenis Trigger (push, pull_request, schedule, dll.)

### Menjalankan Build dan Test di GitHub Actions

[] Menyiapkan Action untuk build project (contoh: Node.js, Python, Java, dll.)  
[] Menjalankan unit test otomatis dengan GitHub Actions  
[] Menggunakan caching untuk mengoptimalkan waktu build  
[] Mengatur matrix builds untuk berbagai environment

### Advanced GitHub Actions

[] Menggunakan Docker dalam GitHub Actions (Docker container jobs)  
[] Menyusun dan menggunakan reusable workflows  
[] Mengintegrasikan GitHub Actions dengan layanan CI/CD eksternal  
[] Menangani error dan kondisi kegagalan di workflow (failures, retries, etc.)

### Keamanan dan Best Practices

[] Mengelola Secrets dengan GitHub Actions secara aman  
[] Membatasi akses ke repository dan actions dengan environment dan approval workflow  
[] Memahami dan mengatur permissions pada workflows, jobs, dan secrets

---

## KUBERNETES

### Dasar-Dasar Kubernetes

[] Apa itu Kubernetes?  
[] Komponen utama Kubernetes (Master Node, Worker Node, Pod, Deployment, Service, etc.)  
[] Arsitektur Kubernetes (Kubernetes API Server, Scheduler, Controller Manager, Kubelet, Kube Proxy)  
[] Konsep Pod, ReplicaSet, Deployment, Namespace, dan Label  
[] Cara Kerja Kubernetes dalam Orkestrasi Container

### Instalasi dan Konfigurasi Kubernetes

[] Instalasi Kubernetes di local (Minikube, kubeadm, atau Docker Desktop)  
[] Menyambungkan ke Kubernetes Cluster dengan kubectl  
[] Konfigurasi Kubeconfig untuk akses ke cluster  
[] Menyiapkan cluster multi-node (opsional)

### Pod, Deployment, dan ReplicaSet

[] Membuat dan menjalankan Pod dengan kubectl  
[] Memahami Deployment dan ReplicaSet  
[] Scaling Deployment di Kubernetes (kubectl scale)  
[] Update dan Rollback Deployment  
[] Mengelola Pods dengan Labels dan Selectors

### Service dan Networking

[] Membuat dan mengonfigurasi Kubernetes Service (ClusterIP, NodePort, LoadBalancer, ExternalName)  
[] DNS dan Internal Networking di Kubernetes  
[] Menghubungkan aplikasi menggunakan Service Discovery  
[] Network Policies di Kubernetes

### Volume dan Persistent Storage

[] Apa itu Persistent Volumes (PV) dan Persistent Volume Claims (PVC)?  
[] Mengonfigurasi Storage Class dan Volume di Kubernetes  
[] Menggunakan NFS, HostPath, atau cloud storage dengan Kubernetes  
[] Backup dan Restore data dengan Kubernetes Volumes

### Manajemen Konfigurasi dan Secrets

[] Menggunakan ConfigMaps untuk menyimpan konfigurasi  
[] Menggunakan Secrets untuk menyimpan informasi sensitif  
[] Mounting ConfigMaps dan Secrets ke dalam Pod

### Monitoring dan Logging

[] Integrasi dengan monitoring tools (Prometheus, Grafana)  
[] Logging dengan EFK Stack (Elasticsearch, Fluentd, Kibana)  
[] Menggunakan kubectl untuk melihat log dan status Pod

### Helm (Package Manager di Kubernetes)

[] Apa itu Helm?  
[] Instalasi dan setup Helm  
[] Membuat dan mengelola Helm Chart  
[] Menggunakan Helm untuk menginstall aplikasi di Kubernetes

---

## Tugas Akkhir

### Docker

[] Membuat Container dan Images berisi Aplikasi Fullstack
[] Mengupload nya ke dalam registry (Aws, Google Cloud, Docker Hub)
[] Mencoba Pull Images dari Registry Tsb.

### GitHub Actions

[] Membuat Action untuk otomatisasi deployment (contoh: ke AWS, GCP, atau Heroku)  
[] Menyebarkan aplikasi menggunakan SSH atau GitHub Actions Deploy Keys  
[] Deploy ke Kubernetes dari GitHub Actions

### Kubernetes

[] Mengimplementasikan CI/CD ke server (Aws, Azure, Vercel)

---
