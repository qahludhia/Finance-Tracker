# Keuanganku – Finance Tracker

Aplikasi pencatat keuangan pribadi dalam **satu file HTML**. Bisa jalan offline dan tidak perlu install apa pun. Data tersimpan di perangkatmu sendiri, tidak dikirim ke server mana pun.

## Fitur

- **Transaksi**: catat pemasukan & pengeluaran per kategori dan per akun.
- **Akun & pocket**: BCA dan tiap pocket Jago dihitung sebagai akun terpisah, dengan saldo otomatis.
- **Fungsi pocket**:
  - **Jajan**: budget bulanan, sisa jajan, dan peringatan saat hampir habis atau over budget.
  - **Liburan**: target + tenggat, progress, dan berapa yang perlu disetor per bulan.
  - **Tabungan**: target, progress, dan peringatan kalau tabungan terpakai.
- **Transfer** antar rekening/pocket (tidak dihitung sebagai pengeluaran).
- **Alokasi gaji**: satu klik untuk mencatat transfer dari BCA ke semua pocket sesuai setoran rutin.
- **Dashboard**: total saldo, pemasukan vs pengeluaran 6 bulan, pengeluaran per kategori, dan budget kategori.
- **Ringkasan bulanan**, mode gelap otomatis, dan tampilan HP.

## Cara pakai

1. Download/clone repo ini, lalu buka `index.html` di **Chrome atau Edge**.
2. Buka tab **Akun & Pocket**: isi saldo awal, setoran rutin, budget jajan, dan target.
3. Catat transaksi dengan tombol **+ Transaksi**.

## Penyimpanan data

| Cara | Keterangan |
|---|---|
| Otomatis di browser | Selalu aktif. Data hilang kalau data browser dihapus. |
| **File data…** (disarankan) | Simpan otomatis ke file `.json` pilihanmu (Chrome/Edge desktop). Taruh di folder Google Drive/OneDrive supaya ter-backup. |
| **Sinkron GitHub** (untuk banyak perangkat) | Simpan otomatis ke repo GitHub **privat**, bisa dibuka dari laptop, komputer kantor, dan HP. Lihat panduan di bawah. |
| Ekspor / Impor | Backup manual atau pindah perangkat. |

## Sinkron GitHub (laptop, kantor, HP)

Data disimpan sebagai `data.json` di repo GitHub **privat** milikmu. Setiap perubahan langsung dikirim, dan data terbaru diambil saat aplikasi dibuka atau tab-nya aktif lagi. Setiap perubahan tercatat sebagai commit, jadi riwayat datanya ikut ter-backup.

**1. Buat repo privat (sekali saja)**
Buka https://github.com/new, isi nama `keuanganku-data`, pilih **Private**, lalu klik **Create repository**. Repo boleh kosong.

**2. Buat token (sekali per perangkat, disarankan)**
1. Buka https://github.com/settings/personal-access-tokens/new
2. Isi nama token, misalnya `keuanganku-laptop`, lalu pilih masa berlaku.
3. Di **Repository access**, pilih **Only select repositories**, lalu pilih `keuanganku-data`.
4. Di **Permissions → Repository permissions**, set **Contents** ke **Read and write**.
5. Klik **Generate token** dan salin tokennya (`github_pat_…`).

Token ini hanya bisa mengakses repo `keuanganku-data`, tidak bisa ke repo atau akun lain. Kalau satu perangkat tidak dipakai lagi, misalnya laptop kantor, cabut token perangkat itu di https://github.com/settings/personal-access-tokens

**3. Sambungkan di aplikasi**
Klik **Sinkron GitHub**, isi username GitHub, nama repo, dan token, lalu klik **Simpan**.
- Di perangkat pertama, data yang sudah ada di browser dikirim ke GitHub.
- Di perangkat berikutnya, data dari GitHub langsung diambil.

Status sinkron tampil di pojok atas. Klik status itu untuk sinkron manual.

**Catatan**
- Kalau dua perangkat sama-sama mencatat sebelum sempat sinkron, datanya **digabung**. Transaksi dari kedua perangkat tetap ada, dan yang dihapus tetap terhapus.
- Aplikasi menolak repo publik supaya data keuanganmu tidak terbuka.
- Token disimpan di browser perangkat itu dan tidak ikut file Ekspor.

> ⚠️ Repo ini **publik**. Jangan simpan file data `.json` di dalam folder repo. Kalaupun tersimpan di sana, `.gitignore` sudah mencegah file `.json` ikut ter-commit.
