#  Student AI Usage Analysis

### Kelompok 5 — Kelas F

**Praktikum Algoritma dan Pemrograman**
**Teknik Elektro — Universitas Diponegoro**

---

##  Deskripsi Proyek

Repositori ini dibuat sebagai dokumentasi dan penyimpanan seluruh tugas **Post-Test Praktikum Algoritma dan Pemrograman Semester 2**.

Proyek ini berfokus pada **Analisis Data Eksploratif (Exploratory Data Analysis / EDA)** terhadap pola penggunaan Artificial Intelligence (AI) di kalangan siswa menggunakan dataset **`Kelas_F_Student_AI_Usage.csv`**.

Analisis yang dilakukan mencakup:

* Analisis agregasi data
* Filter dan tren penggunaan AI
* Analisis korelasi nilai akademik
* Analisis distribusi jam belajar
* Visualisasi data menggunakan berbagai jenis grafik

> Repositori ini bersifat **Public** agar dapat diakses oleh asisten praktikum untuk keperluan penilaian dan verifikasi hasil pekerjaan.

---

#  Akuntabilitas & Distribusi Peran

Sebagai bentuk transparansi dan tanggung jawab kerja kelompok, berikut pembagian tugas masing-masing anggota:

| Nama                           | NIM            | Jobdesk                                                                                                                                                                                                                                  |
| ------------------------------ | -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Alvina Rafeyfa Asyla**       | 21060125120051 | • Mendesain infografis hasil analisis data dalam format PDF Slider<br>• Mempublikasikan infografis ke LinkedIn beserta tautan GitHub<br>• Melakukan connect dan tag akun LinkedIn BKTI serta seluruh Asprak                              |
| **Muhammad Zaky Khasani**      | 21060125120028 | • Mendesain infografis hasil analisis data dalam format Instagram Story (9:16)<br>• Mempublikasikan infografis ke Instagram Story<br>• Follow dan tag akun Instagram BKTI serta seluruh Asprak                                           |
| **Nur Fadzly Maulana Pratama** | 21060125120046 | • Membuat visualisasi **Kategori A** (Bar Chart rata-rata nilai setelah AI berdasarkan umur)<br>• Membuat visualisasi **Kategori B** (Bar Chart perbandingan jam belajar pengguna ChatGPT dan Copilot)                                   |
| **Pauli Nasib Simatupang**     | 21060125120042 | • Membuat visualisasi **Kategori C** (Scatter Plot korelasi nilai sebelum dan sesudah AI)<br>• Membuat visualisasi **Kategori D** (Boxplot distribusi jam belajar)<br>• Menggabungkan seluruh grafik ke dalam layout grid 2×2 (Grafik 5) |

---

#  Deskripsi Dataset

Dataset yang digunakan adalah:

```text
Kelas_F_Student_AI_Usage.csv
```

Dataset berisi informasi mengenai kebiasaan belajar, penggunaan tools AI, serta perubahan performa akademik dari **100 siswa**.

## Struktur Dataset

| Kolom                   | Tipe Data | Deskripsi                              |
| ----------------------- | --------- | -------------------------------------- |
| age                     | Integer   | Umur siswa (14–19 tahun)               |
| education_level         | String    | Jenjang pendidikan siswa               |
| study_hours_per_day     | Float     | Lama belajar mandiri per hari (jam)    |
| uses_ai                 | String    | Status penggunaan AI (Yes/No)          |
| ai_tools_used           | String    | Tools AI yang digunakan                |
| purpose_of_ai           | String    | Tujuan penggunaan AI                   |
| grades_before_ai        | Float     | Nilai sebelum menggunakan AI           |
| grades_after_ai         | Float     | Nilai setelah menggunakan AI           |
| daily_screen_time_hours | Float     | Durasi penggunaan layar per hari (jam) |

---

#  Arsitektur dan Alur Analisis

Program dibangun melalui lima tahapan visualisasi data.

## 1 Pemuatan & Eksplorasi Data

* Membaca dataset menggunakan **Pandas**
* Memeriksa struktur data
* Memvalidasi tipe data
* Mendeteksi missing values

## 2 Analisis Agregasi (Kategori A)

* Mengelompokkan data berdasarkan umur menggunakan `groupby()`
* Menghitung rata-rata `grades_after_ai`
* Menampilkan hasil dalam bentuk **Bar Chart**

## 3 Filter & Tren (Kategori B)

* Menghitung median `study_hours_per_day` pengguna Copilot
* Memfilter pengguna ChatGPT yang belajar di atas median tersebut
* Membandingkan hasil menggunakan **Bar Chart**

## 4 Analisis Korelasi (Kategori C)

* Menghitung korelasi Pearson antara:

  * `grades_before_ai`
  * `grades_after_ai`
* Menampilkan hubungan menggunakan **Scatter Plot** dan garis regresi

## 5 Analisis Distribusi (Kategori D)

* Menghitung:

  * Q1
  * Median
  * Q3
  * IQR
* Mengidentifikasi outlier
* Menampilkan distribusi data menggunakan **Boxplot**

## 6 Visualisasi Gabungan

Empat grafik utama digabungkan ke dalam satu figure menggunakan:

```python
plt.subplots(2, 2)
```

Pendekatan ini memungkinkan seluruh visualisasi ditampilkan dalam satu dashboard tanpa menuliskan ulang logika analisis.

---

#  Teknologi dan Library

| Teknologi    | Fungsi                                      |
| ------------ | ------------------------------------------- |
| Python 3     | Bahasa pemrograman utama                    |
| Google Colab | Lingkungan pengembangan berbasis notebook   |
| Pandas       | Manipulasi dan analisis data                |
| Matplotlib   | Pembuatan visualisasi dasar                 |
| Seaborn      | Visualisasi statistik yang lebih informatif |
| Canva        | Desain infografis akhir                     |

---

#  Cara Menjalankan Program

## Menggunakan Google Colab (Direkomendasikan)

1. Buka Google Colab
2. Upload file:

```text
PostTest_KelasF_Kelompok5.ipynb
```

3. Upload dataset:

```text
Kelas_F_Student_AI_Usage.csv
```

4. Jalankan seluruh cell menggunakan:

```text
Shift + Enter
```

---

## Menggunakan Jupyter Notebook (Lokal)

### Instalasi Library

```bash
pip install pandas matplotlib seaborn jupyter
```

### Jalankan Notebook

Pastikan file berikut berada dalam folder yang sama:

```text
PostTest_KelasF_Kelompok5.ipynb
Kelas_F_Student_AI_Usage.csv
```

Kemudian jalankan:

```bash
jupyter notebook
```

Buka notebook dan jalankan seluruh cell secara berurutan.

---

#  Struktur Repositori

```text
posttest-kelas-f-kelompok-5/
│
├── 📓 PostTest_KelasF_Kelompok5.ipynb
├── 📄 Kelas_F_Student_AI_Usage.csv
├── 🖼️ grafik1_kategori_A.png
├── 🖼️ grafik2_kategori_B.png
├── 🖼️ grafik3_kategori_C.png
├── 🖼️ grafik4_kategori_D.png
├── 🖼️ grafik5_gabungan.png
├── 📑 Student_AI_Usage_Analysis.pdf
└── 📄 README.md
```

---

#  Temuan Utama

| Kategori      | Temuan                                                                                                                                                                  |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Agregasi      | Siswa usia 17 tahun memiliki rata-rata nilai tertinggi (71.9) setelah menggunakan AI, sedangkan usia 19 tahun memiliki rata-rata terendah (65.3).                       |
| Filter & Tren | Pengguna ChatGPT yang aktif belajar memiliki rata-rata waktu belajar 3.26 jam/hari, hampir dua kali lebih tinggi dibanding pengguna Copilot (2.43 jam/hari).            |
| Korelasi      | Terdapat korelasi positif antara nilai sebelum dan sesudah penggunaan AI, menunjukkan bahwa AI tidak sepenuhnya menghilangkan perbedaan kemampuan akademik antar siswa. |
| Distribusi    | Median jam belajar siswa berada pada 2.8 jam/hari dengan variasi yang cukup besar antar individu.                                                                       |

---


##  Lisensi

Repositori ini dibuat untuk keperluan akademik dalam rangka memenuhi tugas **Post-Test Praktikum Algoritma dan Pemrograman Semester 2**.

---

<div align="center">

**Post-Test Praktikum Algoritma dan Pemrograman**
Kelas F • Kelompok 5
Teknik Elektro • Universitas Diponegoro • 2026

</div>
