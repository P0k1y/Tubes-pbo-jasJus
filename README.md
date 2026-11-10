# Campus Canteen POS

Aplikasi kasir kantin kampus berbasis desktop menggunakan Java Swing.

## Teknologi

- Java JDK 17
- Apache NetBeans
- Java Swing
- Apache Maven

## Struktur Tim

| NIM | Anggota | Tanggung Jawab |
|---|---|---|
| 607062530011 | Azka Putra Wirayudha | Produk, Kasir, Panel Produk, Riwayat, Struk |
| 607062500038 | Arsah Africh Maliki | Transaksi, Detail Transaksi, Keranjang |
| 607062500055 | Muhammad I'jaz Hasha | Pembayaran, Controller, MainFrame, Main |

## Struktur Branch

| Branch | Fungsi |
|---|---|
| `main` | Menyimpan versi final aplikasi yang stabil. |
| `develop` | Menjadi tempat integrasi pekerjaan seluruh anggota. |
| `feature/anggota-1` | Branch pengembangan fitur Anggota 1. |
| `feature/anggota-2` | Branch pengembangan fitur Anggota 2. |
| `feature/anggota-3` | Branch pengembangan fitur Anggota 3. |

## Alur Kerja Kelompok

Alur pembentukan branch:

```text
main
  └── develop
        ├── feature/anggota-1
        ├── feature/anggota-2
        └── feature/anggota-3
```

Alur penggabungan kode:

```text
feature/anggota-1 ──┐
feature/anggota-2 ──┼──> develop ───> main
feature/anggota-3 ──┘
```

### Ketentuan Penggunaan Git

1. Setiap anggota membuat branch fitur masing-masing dari `develop`.
2. Setiap anggota mengerjakan dan melakukan commit pada branch masing-masing.
3. Hasil pekerjaan dikirim melalui Pull Request menuju `develop`.
4. Seluruh pekerjaan diuji dan diintegrasikan pada branch `develop`.
5. Setelah aplikasi selesai dan dinyatakan stabil, `develop` digabungkan ke `main`.

### Aturan Pengembangan

- Hindari melakukan perubahan langsung pada branch `main`.
- Hindari mengerjakan fitur anggota lain tanpa koordinasi.
- Gunakan commit message yang jelas dan deskriptif.
- Pastikan aplikasi dapat dijalankan sebelum mengajukan Pull Request.
- Setiap perubahan struktur class harus disepakati bersama anggota kelompok.