# Sistem Penilaian Mahasiswa Sederhana (Java)

Tugas Pemrograman Berorientasi Objek, Kelompok 6
Fakultas MIPA, Universitas Syiah Kuala

**Anggota**
- Al Aul Tsaqif (250810701100034)
- M Farras Munawwir (250810701100004)
- Imam Assadiq (250810701100079)
- Syella Zikra Arifa (250810701100014)

## Deskripsi

Program berbasis konsol untuk mengelola data mahasiswa, menghitung nilai akhir berbobot, dan mengonversinya menjadi huruf mutu. Data disimpan sementara di memori selama program berjalan.

Konsep OOP yang diterapkan: kelas dan objek, encapsulation, constructor, dan method.

## Fitur

- Tambah data mahasiswa (nama, NIM, nilai tugas, UTS, UAS)
- Validasi nilai 0 sampai 100 dan pengecekan NIM ganda
- Perhitungan nilai akhir otomatis dan konversi ke huruf mutu A sampai E
- Tampilan daftar semua mahasiswa dalam bentuk tabel
- Rekap kelas: jumlah mahasiswa, rata-rata, nilai tertinggi, dan nilai terendah

## Struktur Proyek

```
.
├── Mahasiswa.java   # Kelas entitas: data dan logika penilaian
├── Main.java        # Kelas eksekusi: menu dan interaksi pengguna
└── README.md
```

## Aturan Penilaian

Nilai akhir = (30% x Tugas) + (35% x UTS) + (35% x UAS)

| Nilai Akhir | Huruf Mutu | Keterangan    |
|-------------|------------|---------------|
| 80 - 100    | A          | Sangat baik   |
| 70 - < 80   | B          | Baik          |
| 60 - < 70   | C          | Cukup         |
| 50 - < 60   | D          | Kurang        |
| < 50        | E          | Sangat kurang |

Contoh: Tugas 85, UTS 78, UAS 80 menghasilkan 25,5 + 27,3 + 28,0 = 80,80, yaitu huruf mutu A.

## Kebutuhan

- JDK 8 atau lebih baru (fitur `String.repeat` memerlukan JDK 11 atau lebih baru)

## Cara Menjalankan

```
javac Mahasiswa.java Main.java
java Main
```

Contoh tampilan:

```
===== SISTEM PENILAIAN MAHASISWA =====
1. Tambah mahasiswa
2. Tampilkan semua mahasiswa
3. Rekap kelas
0. Keluar
Pilih menu:
```

## Desain Kelas

**Mahasiswa**

| Atribut (private) | Tipe   |
|-------------------|--------|
| nama              | String |
| nim               | String |
| nilaiTugas        | double |
| nilaiUTS          | double |
| nilaiUAS          | double |

Method publik: konstruktor `Mahasiswa(nama, nim, nilaiTugas, nilaiUTS, nilaiUAS)`, `hitungNilaiAkhir()`, `hitungGrade()`, getter untuk semua atribut, dan setter nilai dengan validasi 0 sampai 100.

**Main** hanya berisi menu dan input/output. Logika penilaian seluruhnya ada di `Mahasiswa`.

## Catatan

- Jangan letakkan file Java lain yang punya `class Mahasiswa` di folder yang sama, karena akan bentrok dengan kelas di proyek ini.
- Data tidak disimpan permanen dan hilang saat program ditutup.

## Pengembangan Selanjutnya

- Penyimpanan data ke berkas atau basis data
- Antarmuka grafis (Swing atau JavaFX)
