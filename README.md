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
| Ekspor / Impor | Backup manual atau pindah perangkat. |

> ⚠️ Repo ini **publik**. Jangan simpan file data `.json` di dalam folder repo. Kalaupun tersimpan di sana, `.gitignore` sudah mencegah file `.json` ikut ter-commit.
