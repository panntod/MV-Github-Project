# Best Practices GitHub Actions

## Gunakan Caching untuk Mempercepat Build

Gunakan `actions/cache` untuk menyimpan dependencies agar tidak perlu mengunduh ulang setiap build.

```yaml
- name: Cache dependencies
  uses: actions/cache@v3
  with:
    path: ~/.npm
    key: npm-${{ runner.os }}-${{ hashFiles('**/package-lock.json') }}
    restore-keys: |
      npm-${{ runner.os }}-
```

## Minimalisasi Permissions

Jangan berikan lebih banyak izin dari yang diperlukan untuk mengurangi risiko keamanan.

```yaml
permissions:
  contents: read
  pull-requests: write
```

## Gunakan Matrices untuk Parallel Jobs

Gunakan `matrix` untuk menjalankan beberapa versi runtime sekaligus.

```yaml
strategy:
  matrix:
    node-version: [16, 18, 20]
```

## Selalu Validasi Konfigurasi YAML

Gunakan linter atau validator YAML untuk menghindari kesalahan sintaksis.

## Jangan Simpan Secrets dalam Kode

Gunakan `secrets.GITHUB_TOKEN` atau GitHub Secrets untuk menyimpan data sensitif.

---
