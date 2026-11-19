<div align="center">

# 🎓 Sistem Penilaian Mahasiswa

### Aplikasi penilaian sederhana berbasis Java dengan konsep OOP

![Java](https://img.shields.io/badge/Java-11%2B-orange?style=for-the-badge&logo=openjdk&logoColor=white)
![OOP](https://img.shields.io/badge/Paradigma-OOP-2563eb?style=for-the-badge)
![UI](https://img.shields.io/badge/UI-Swing%20%7C%20Console-16a34a?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Selesai-success?style=for-the-badge)

📚 Tugas Mata Kuliah **Pemrograman Berorientasi Objek** · Kelompok 6
🏛️ Fakultas MIPA, Universitas Syiah Kuala

</div>

---

## 📖 Deskripsi

Program untuk mengelola data mahasiswa, **menghitung nilai akhir berbobot** secara otomatis, dan **mengonversinya menjadi huruf mutu**. Data disimpan sementara di memori selama program berjalan.

Tersedia dalam **dua tampilan**: 🖥️ GUI (Swing) dan ⌨️ konsol.

## ✨ Fitur

| Ikon | Fitur | Keterangan |
|:---:|---|---|
| ➕ | Tambah mahasiswa | Nama, NIM, nilai tugas, UTS, dan UAS |
| ✅ | Validasi input | Nilai harus 0 sampai 100, NIM tidak boleh ganda |
| 🧮 | Hitung otomatis | Nilai akhir berbobot dan huruf mutu A sampai E |
| 📋 | Tabel daftar | Huruf mutu diberi warna agar mudah dibaca |
| 📊 | Rekap kelas | Jumlah, rata-rata, nilai tertinggi, dan terendah |
| 🗑️ | Hapus data | Hapus baris terpilih (versi GUI) |

## 🧠 Konsep OOP yang Diterapkan

- 🧱 **Class & Object**: `Mahasiswa` sebagai cetak biru data
- 🔒 **Encapsulation**: atribut `private`, akses lewat getter dan setter
- 🏗️ **Constructor**: atribut langsung terisi saat objek dibuat
- ⚙️ **Method**: `hitungNilaiAkhir()` dan `hitungGrade()`

## 📁 Struktur Proyek

```
📦 sistem-penilaian
 ┣ 📜 Mahasiswa.java   → kelas entitas: data dan logika penilaian
 ┣ 🖥️ MainGUI.java     → tampilan GUI (Swing)
 ┣ ⌨️ Main.java        → tampilan konsol (menu teks)
 ┗ 📝 README.md
```

## 🧾 Aturan Penilaian

> **Nilai Akhir = (30% × Tugas) + (35% × UTS) + (35% × UAS)**

| Nilai Akhir | Mutu | Keterangan |
|:---:|:---:|---|
| 80 – 100 | 🟢 **A** | Sangat baik |
| 70 – < 80 | 🔵 **B** | Baik |
| 60 – < 70 | 🟡 **C** | Cukup |
| 50 – < 60 | 🟠 **D** | Kurang |
| < 50 | 🔴 **E** | Sangat kurang |

💡 **Contoh:** Tugas 85, UTS 78, UAS 80 → 25,5 + 27,3 + 28,0 = **80,80** → Mutu **A**

## 🚀 Cara Menjalankan

**1️⃣ Pastikan JDK 11 atau lebih baru terpasang**

```bash
java -version
```

**2️⃣ Kompilasi**

```bash
javac Mahasiswa.java Main.java MainGUI.java
```

**3️⃣ Jalankan salah satu**

```bash
java MainGUI   # 🖥️ versi GUI
java Main      # ⌨️ versi konsol
```

## 🏛️ Desain Kelas

**`Mahasiswa`**

| Atribut | Tipe | Akses |
|---|---|:---:|
| `nama` | String | 🔒 private |
| `nim` | String | 🔒 private |
| `nilaiTugas` | double | 🔒 private |
| `nilaiUTS` | double | 🔒 private |
| `nilaiUAS` | double | 🔒 private |

Method publik: konstruktor `Mahasiswa(nama, nim, nilaiTugas, nilaiUTS, nilaiUAS)`, `hitungNilaiAkhir()`, `hitungGrade()`, getter semua atribut, dan setter nilai dengan validasi 0 sampai 100.

Kelas `Main` dan `MainGUI` hanya mengurus tampilan. Semua logika penilaian ada di `Mahasiswa` (*separation of concerns*).

## ⚠️ Catatan

- 🚫 Jangan taruh file Java lain yang punya `class Mahasiswa` di folder yang sama, karena akan bentrok.
- 💾 Data tidak tersimpan permanen dan hilang saat program ditutup.

## 🔮 Rencana Pengembangan

- [ ] 💾 Simpan data ke berkas atau basis data (MySQL)
- [ ] 📤 Ekspor rekap ke CSV
- [ ] 🔍 Cari dan urutkan data

## 👥 Anggota Kelompok 6

| | Nama | NIM |
|:---:|---|---|
| 👤 | Al Aul Tsaqif | 250810701100034 |
| 👤 | M Farras Munawwir | 250810701100004 |
| 👤 | Imam Assadiq | 250810701100079 |
| 👤 | Syella Zikra Arifa | 250810701100014 |

---

<div align="center">

⭐ Dibuat dengan ☕ dan Java oleh Kelompok 6 ⭐

</div>
