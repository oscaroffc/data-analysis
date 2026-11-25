Tool ini digunakan untuk **menganalisis repository GitHub secara aman (read-only)**.  
Fokus utama:
- Menampilkan daftar file di repo
- Menjelaskan bahasa & fungsi tiap script
- Menandai potensi risiko (misalnya ransomware, DDoS, malware, dsb)
- (Opsional) Menjalankan demo enkripsi/dekripsi aman dengan `cryptography` (tanpa merusak file)

---

## 📦 Instalasi

### 1. Clone atau Download
```bash
git clone https://github.com/username/data-analysis.git
cd data-analysis
```
### 2. Install Python & pip (jika belum)

Untuk Termux:

```bash
pkg update && pkg upgrade
pkg install python git -y
```
### 3. Install dependensi

```bash
pip install requests cryptography
```
### ⚙️ Setup

Script utama bernama analisis.py
Argumen yang wajib diberikan adalah alamat repo GitHub (format owner/repo atau URL lengkap).
```
🔑 Opsi Tambahan:

--no-save → hasil analisis tidak disimpan ke file, hanya ditampilkan di terminal.
--max-file-bytes N → batasi ukuran maksimal file yang dianalisis (default 50 KB).
--demo-encrypt → jalankan demo aman enkripsi & dekripsi dengan library cryptography.
```
### 🚀 Cara Menjalankan

1. Analisis repo dengan URL
```bash
python3 cek.py https://github.com/****/***
```
2. Analisis repo dengan format owner/repo
```bash
python3 cek.py ***/***
```
3. Analisis tanpa menyimpan hasil
```bash
python3 cek.py username/repo --no-save
```
