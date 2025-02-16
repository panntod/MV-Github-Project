# Docker on Linux (WSL)

Berikut adalah langkah-langkah untuk mengaktifkan WSL dan menginstal Docker di Linux pada Windows.

---

## **1. Aktivasi WSL (Windows Subsystem for Linux)**

1️. **Cek apakah WSL sudah terinstall**

```sh
wsl -l
```

2️. **Buka Control Panel**  
📌 Tekan `Win + R` → ketik `control` → Enter

3️. **Aktifkan Windows Features**  
📌 Pergi ke `Control Panel > Programs > Turn Windows features on or off`  
**Centang fitur berikut:**

- [] **Virtual Machine Platform**
- [] **Windows Subsystem for Linux**

4️. **Update WSL**

```sh
wsl --update
```

---

## **2. Instalasi Distro Linux**

1️. **Install manual melalui Microsoft Docs**  
📌 [WSL Install Manual](https://learn.microsoft.com/en-us/windows/wsl/install-manual)

2️. **Pilih distro**  
💡 Rekomendasi: **Ubuntu (Latest)**

3️. **Ekstraksi file distro (.appx)**  
📌 Ubah `.appx` menjadi `.zip`, lalu ekstrak

4️. **Pilih file yang diperlukan**  
📌 Masuk ke folder hasil ekstraksi → **Gunakan file `install.tar.gz` & `ubuntu.exe`**  
📌 **Hapus file lainnya**

5️. **Login ke Ubuntu dan setup awal**  
📌 Setelah instalasi, bisa menghapus file `install.tar.gz`

---

## **3. Masuk ke dalam Linux & Install Docker**

1️. **Update repository**

```sh
sudo apt update
```

2️. **Install Docker Core**

```sh
sudo apt install docker.io -y
```

3️. **Tambahkan user saat ini ke grup `docker`**

```sh
sudo usermod -aG docker $USER
```

4️. **Install Docker Compose Daemon**

```sh
sudo curl -L "https://github.com/docker/compose/releases/download/2.33.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

5️. **Update permission untuk Docker Compose**

```sh
sudo chmod +x /usr/local/bin/docker-compose
```

---

## **4. Cek Instalasi Docker**

Jalankan perintah berikut untuk memastikan Docker berjalan:

```sh
sudo dockerd
```

Jika berhasil, maka Docker sudah siap digunakan di Linux melalui WSL! 🎉🚀
