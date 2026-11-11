# Campus Canteen POS

Aplikasi kasir kantin kampus berbasis desktop menggunakan Java Swing dan Maven. Project ini dikembangkan sebagai Tugas Besar Mata Kuliah Pemrograman Berorientasi Objek (PBO) menggunakan konsep Object-Oriented Programming (OOP).

**Status:** Dalam Pengembangan

## Teknologi

| Teknologi | Versi / Keterangan |
|---|---|
| Java JDK | 21 atau lebih baru |
| Java Swing | GUI Desktop |
| Apache Maven | 3.9.10 |
| Maven Wrapper | 3.3.4 |
| JUnit Jupiter | 5.11.0 |
| IDE | Visual Studio Code / Apache NetBeans |
| Version Control | Git dan GitHub |

## Persyaratan Sistem

Sebelum menjalankan project, pastikan perangkat sudah memiliki:

1. Java JDK versi 21 atau lebih baru.
2. Git.
3. Visual Studio Code atau Apache NetBeans.
4. Koneksi internet untuk mengunduh Maven dan dependency pada penggunaan pertama.

**Catatan Maven:** Maven tidak perlu diinstal secara manual karena repository sudah menyediakan Maven Wrapper. Wrapper akan mengunduh dan menggunakan Apache Maven 3.9.10 secara otomatis apabila belum tersedia di komputer.

### Memeriksa Instalasi Java

Jalankan perintah berikut melalui terminal:

```bash
java -version
javac -version
```

Pastikan keduanya menggunakan JDK versi 21 atau lebih baru.

## Instalasi dan Menjalankan Project

### 1. Clone Repository

Clone repository dari GitHub:

```bash
git clone https://github.com/P0k1y/Tubes-pbo-jasJus.git
```

Masuk ke direktori project:

```bash
cd Tubes-pbo-jasJus
```

### 2. Berpindah ke Branch Develop

Setelah clone, secara default Git akan berada di branch `main`.

Ambil informasi branch terbaru dari GitHub:

```bash
git fetch origin
```

Buat branch lokal `develop` yang terhubung dengan branch remote:

```bash
git switch --track origin/develop
```

Pastikan posisi branch sudah benar:

```bash
git branch
```

Branch yang aktif ditandai dengan tanda `*`.

### 3. Buka Project

Buka folder project menggunakan Visual Studio Code atau Apache NetBeans.

Pastikan folder yang dibuka adalah folder utama `Tubes-pbo-jasJus`, yaitu folder yang berisi `pom.xml`.

### 4. Memeriksa Maven Wrapper

Untuk Windows PowerShell:

```powershell
.\mvnw.cmd -version
```

Untuk Linux/macOS:

```bash
./mvnw -version
```

Pastikan informasi yang muncul menunjukkan Apache Maven 3.9.10 dan Java 21 atau lebih baru.

### 5. Compile Project

Windows:

```powershell
.\mvnw.cmd compile
```

Linux/macOS:

```bash
./mvnw compile
```

Perintah ini digunakan untuk mengompilasi seluruh source code pada folder `src/main/java`.

### 6. Menjalankan Unit Testing

Windows:

```powershell
.\mvnw.cmd test
```

Linux/macOS:

```bash
./mvnw test
```

Perintah ini digunakan untuk menjalankan pengujian menggunakan JUnit.

### 7. Membersihkan dan Menguji Project

Windows:

```powershell
.\mvnw.cmd clean test
```

Linux/macOS:

```bash
./mvnw clean test
```

Perintah ini membersihkan hasil build sebelumnya, kemudian menjalankan proses pengujian kembali.

### 8. Menjalankan Main Class

Setelah project berhasil dikompilasi, jalankan melalui terminal:

```bash
java -cp target/classes id.pbo.canteenpos.Main
```

Saat ini `Main.java` masih merupakan entry point awal. Tampilan Java Swing akan diintegrasikan pada tahap pengembangan MainFrame.

## Struktur Project

```text
Tubes-pbo-jasJus/
│
├── .github/
│
├── .mvn/
│   ├── wrapper/
│   │   └── maven-wrapper.properties
│   ├── jvm.config
│   └── maven.config
│
├── src/
│   │
│   ├── main/
│   │   └── java/
│   │       └── id/pbo/canteenpos/
│   │           ├── model/
│   │           ├── controller/
│   │           ├── gui/
│   │           └── Main.java
│   │
│   └── test/
│       └── java/
│           └── id/pbo/canteenpos/
│               └── AppTest.java
│
├── .gitignore
├── mvnw
├── mvnw.cmd
├── pom.xml
└── README.md
```

### Fungsi Struktur Folder

| Folder / File | Fungsi |
|---|---|
| `.github/` | Menyimpan konfigurasi GitHub. |
| `.mvn/` | Menyimpan konfigurasi Maven Wrapper. |
| `src/main/java/` | Menyimpan seluruh source code aplikasi. |
| `src/test/java/` | Menyimpan source code untuk unit testing. |
| `model/` | Menyimpan class model dan representasi objek aplikasi. |
| `controller/` | Mengatur proses bisnis dan komunikasi antara model dengan GUI. |
| `gui/` | Menyimpan seluruh tampilan aplikasi menggunakan Java Swing. |
| `Main.java` | Entry point atau titik awal eksekusi aplikasi. |
| `pom.xml` | Mengatur konfigurasi project, dependency, dan plugin Maven. |
| `mvnw` | Maven Wrapper untuk Linux/macOS. |
| `mvnw.cmd` | Maven Wrapper untuk Windows. |
| `target/` | Hasil kompilasi dan pengujian yang dibuat otomatis oleh Maven. |

**Catatan:**
- Folder `target/` tidak perlu dimasukkan ke GitHub karena dibuat otomatis ketika Maven dijalankan.
- Folder package yang belum memiliki class Java dapat menggunakan `.gitkeep` agar tetap tersimpan di Git.
- Seluruh class Java harus menggunakan package sesuai lokasi foldernya.

## Struktur Tim dan Pembagian Tugas

Project dikerjakan oleh tiga anggota dengan pembagian tanggung jawab sebagai berikut.

| NIM | Anggota | Tanggung Jawab |
|---|---|---|
| 607062530011 | Azka Putra Wirayudha | Produk, Kasir, Panel Produk, Riwayat, Struk |
| 607062500038 | Arsah Africh Maliki | Transaksi, Detail Transaksi, Keranjang |
| 607062500055 | Muhammad I'jaz Hasha | Pembayaran, Controller, MainFrame, Main |

### Pembagian Package Berdasarkan Tanggung Jawab

**Anggota 1**
- `model/Produk.java`
- `model/Kasir.java`
- `gui/PanelProduk.java`
- `gui/PanelRiwayat.java`
- `gui/StrukDialog.java`

**Anggota 2**
- `model/Transaksi.java`
- `model/DetailTransaksi.java`
- `model/Keranjang.java`

**Anggota 3**
- `model/Pembayaran.java`
- `controller/KasirController.java`
- `gui/MainFrame.java`
- `Main.java`

Penempatan class tersebut mengikuti pembagian tanggung jawab dan dapat disesuaikan apabila terdapat perubahan hasil diskusi kelompok.

## Alur Kerja Git dan Branch

Project menggunakan sistem branching untuk memisahkan pekerjaan setiap anggota dan menjaga kestabilan kode utama.

### Struktur Branch

```text
main
  |
  └── develop
        |
        ├── feature/anggota-1
        |
        ├── feature/anggota-2
        |
        └── feature/anggota-3
```

### Fungsi Branch

| Branch | Fungsi |
|---|---|
| `main` | Menyimpan versi final aplikasi yang sudah stabil. |
| `develop` | Menjadi branch integrasi seluruh pekerjaan kelompok. |
| `feature/anggota-1` | Menyimpan pekerjaan anggota pertama. |
| `feature/anggota-2` | Menyimpan pekerjaan anggota kedua. |
| `feature/anggota-3` | Menyimpan pekerjaan anggota ketiga. |

### Aturan Penggunaan Branch

1. `main` hanya digunakan untuk menyimpan versi aplikasi yang sudah stabil.
2. `develop` digunakan sebagai branch integrasi seluruh pekerjaan anggota.
3. Setiap anggota wajib mengerjakan fitur pada branch masing-masing.
4. Branch fitur dibuat berdasarkan branch `develop` terbaru.
5. Anggota tidak diperbolehkan melakukan commit langsung ke `main` atau `develop`.
6. Setiap pekerjaan yang sudah selesai diajukan melalui Pull Request menuju `develop`.
7. Penggabungan `develop` ke `main` dilakukan setelah seluruh fitur terintegrasi dan diuji.

### Panduan Kerja Anggota

**1. Mengambil perkembangan terbaru develop**

```bash
git switch develop
git pull origin develop
```

**2. Membuat branch pekerjaan masing-masing**

Anggota pertama:

```bash
git switch -c feature/anggota-1
```

Anggota kedua:

```bash
git switch -c feature/anggota-2
```

Anggota ketiga:

```bash
git switch -c feature/anggota-3
```

Perintah pembuatan branch dilakukan satu kali untuk setiap branch kerja.

**3. Memeriksa perubahan**

```bash
git status
```

**4. Menambahkan perubahan ke staging**

```bash
git add .
```

**5. Membuat commit**

Contoh:

```bash
git commit -m "feat: implement product management"
```

**6. Mengirim branch ke GitHub**

Anggota pertama:

```bash
git push -u origin feature/anggota-1
```

Anggota kedua:

```bash
git push -u origin feature/anggota-2
```

Anggota ketiga:

```bash
git push -u origin feature/anggota-3
```

**7. Membuat Pull Request**

Setelah branch berhasil dikirim ke GitHub:

- Buka repository GitHub.
- Pilih menu Pull Requests.
- Buat Pull Request dari branch fitur masing-masing.
- Pastikan base branch adalah `develop`.
- Periksa perubahan sebelum mengajukan Pull Request.
- Tunggu pemeriksaan dan persetujuan sebelum penggabungan.

**8. Sinkronisasi setelah pekerjaan terintegrasi**

Setelah Pull Request berhasil digabungkan ke `develop`, anggota mengambil pembaruan terbaru:

```bash
git switch develop
git pull origin develop
```

Jika masih melanjutkan branch fitur yang sama, ambil pembaruan `develop` ke branch fitur:

```bash
git switch feature/anggota-1
git merge develop
```

Sesuaikan nama branch dengan branch masing-masing anggota.

**9. Rilis aplikasi**

Setelah seluruh pekerjaan selesai, terintegrasi, dan berhasil diuji, pengelola repository mengajukan Pull Request dari `develop` menuju `main`.

## Standar Penulisan Kode

Untuk menjaga konsistensi kode antaranggota, gunakan aturan berikut:

1. Gunakan penamaan class dengan PascalCase, contohnya `Produk`, `PanelProduk`, dan `KasirController`.
2. Gunakan penamaan variabel dan method dengan camelCase, contohnya `kodeProduk`, `getHarga()`, dan `tambahStok()`.
3. Setiap class ditempatkan pada package sesuai tanggung jawabnya.
4. Gunakan access modifier sesuai kebutuhan enkapsulasi.
5. Hindari mengubah class milik anggota lain tanpa koordinasi.
6. Pastikan project dapat dikompilasi dan pengujian berhasil sebelum mengajukan Pull Request.

### Konvensi Commit

Gunakan awalan commit berikut agar perubahan mudah dikenali:

| Prefix | Keterangan |
|---|---|
| `feat:` | Menambahkan fitur baru. |
| `fix:` | Memperbaiki kesalahan kode. |
| `refactor:` | Merapikan atau memperbaiki struktur kode tanpa mengubah fungsi. |
| `test:` | Menambahkan atau memperbaiki pengujian. |
| `docs:` | Mengubah dokumentasi. |
| `chore:` | Perubahan konfigurasi atau pemeliharaan project. |

Contoh:

```bash
git commit -m "feat: add product management"
git commit -m "fix: correct stock calculation"
git commit -m "docs: update project README"
```

---

**Campus Canteen POS**

Tugas Besar Pemrograman Berorientasi Objek (PBO)