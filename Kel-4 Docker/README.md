# Tugas Docker Praktik Sistem Operasi - Kelompok 4
**Topik:** Implementasi Database Service dengan Docker (PostgreSQL & Adminer)

## 👥 Anggota Kelompok
1. **M.Fazril Hidayat** - 062430701478
2. **Mawar Cantika** - 062430701473

---

## 📖 Deskripsi Proyek
Proyek ini bertujuan untuk membangun lingkungan database server yang terisolasi menggunakan teknologi **Docker Container**.

Fitur Utama:
* **Database:** PostgreSQL Versi 16.
* **Management Tool:** Adminer (Web Interface).
* **Persistent Storage:** Menggunakan Docker Volume (`pg_data_k4`) sehingga data **TIDAK HILANG** saat container di-restart.

---

## 📂 File Konfigurasi (Source Code)
Silakan klik link di bawah ini untuk melihat source code konfigurasi:

* **File Konfigurasi Utama:** 👉 [docker-compose.yml](./docker-compose.yml)
* **File Definisi Image:** 👉 [Dockerfile](./Dockerfile)

---

## 🚀 Cara Instalasi & Menjalankan

### 1. Clone Repository
Download atau clone repository ini ke komputer Anda.

### 2. Jalankan Container
Buka terminal di folder project dan ketik:

```bash
sudo docker compose up -d
```
### 3. Cek Status
Pastikan status container Up.

```bash
sudo docker ps
```
---
## 💻 Cara Akses & Login
**1. Buka browser dan akses: http://localhost:8080**
**2. Login dengan data berikut:**
* SystemPostgreSQL (Pilih di dropdown)
* Server   : db_kelompok4
* Username : admin
* Password : password123
* Database : tugas_db

### Pembuktian Persistent Data (Docker Volume)
Untuk membuktikan bahwa data aman tersimpan di Volume:

1. Input data di Adminer (buat tabel/row baru).

2. Matikan container: sudo docker compose down.

3. Nyalakan kembali: sudo docker compose up -d.

4. Login ulang ke Adminer.

Hasil: Data yang diinput sebelumnya MASIH ADA (Tidak hilang).




