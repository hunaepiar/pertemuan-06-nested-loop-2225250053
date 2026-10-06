# Pertemuan 06 Nested Loop Python

**Nama:** Khunaepi
**NIM:** 2225250053
**Kelas:** 3B

## Tujuan

Pada Pertemuan 06, saya mempelajari penggunaan nested loop dalam Python untuk membentuk pola, mengolah pasangan data, melakukan akumulasi, dan melakukan pencacahan. Selain itu, saya belajar menelusuri perubahan dua variabel kontrol, menjalankan dan menguji program di VS Code, serta mengunggah hasil kerja melalui GitHub.

## Struktur Folder

```text
pertemuan-06-nested-loop-2225250053/
├── README.md
├── .gitignore
├── latihan/
│   ├── 01_pasangan_indeks.py
│   ├── 02_pola_segitiga.py
│   ├── 03_jumlah_per_baris.py
│   └── 04_hitung_pasangan.py
├── tugas/
│   └── tabel_perkalian_dan_statistik.py
└── kuis/
    └── kuis_formatiif.py
```

## Cara Menjalankan

Program dijalankan melalui terminal VS Code menggunakan Python 3.12 melalui `uv`.

### Latihan 1

```powershell
uv run --python 3.12 latihan/01_pasangan_indeks.py
```

### Latihan 2

```powershell
uv run --python 3.12 latihan/02_pola_segitiga.py
```

### Latihan 3

```powershell
uv run --python 3.12 latihan/03_jumlah_per_baris.py
```

### Latihan 4

```powershell
uv run --python 3.12 latihan/04_hitung_pasangan.py
```

### Tugas 3

```powershell
uv run --python 3.12 tugas/tabel_perkalian_dan_statistik.py
```

### Kuis Formatif

```powershell
uv run --python 3.12 kuis/kuis_formatiif.py
```

## Algoritma Tugas 3

Program Tugas 3 membuat tabel perkalian dari 1 sampai `n` dan menghitung statistik dari seluruh hasil perkalian.

Langkah algoritmanya:

1. Membaca nilai `n` sebagai bilangan bulat.
2. Memvalidasi `n` menggunakan `while` agar nilainya positif.
3. Menginisialisasi `total_semua = 0` dan `count_genap = 0`.
4. Menjalankan loop luar untuk nilai `i` dari 1 sampai `n`.
5. Menginisialisasi `total_baris = 0` pada setiap baris.
6. Menjalankan loop dalam untuk nilai `j` dari 1 sampai `n`.
7. Menghitung `hasil = i * j`.
8. Menambahkan hasil ke `total_baris` dan `total_semua`.
9. Jika hasil perkalian genap, `count_genap` ditambah 1.
10. Setelah loop dalam selesai, menampilkan jumlah pada baris tersebut.
11. Setelah seluruh loop selesai, menampilkan total keseluruhan dan banyak hasil genap.

## Hasil Pengujian

| Input n | Jumlah Pasangan | Total Semua | Banyak Hasil Genap | Status   |
| ------- | --------------: | ----------: | -----------------: | -------- |
| 1       |               1 |           1 |                  0 | Berhasil |
| 2       |               4 |           9 |                  3 | Berhasil |
| 3       |               9 |          36 |                  5 | Berhasil |

Hasil pengujian sesuai dengan test case yang ditentukan pada Tugas 3.

### Contoh Pengujian n = 2

```text
Tabel Perkalian dan Statistik
   1   2 | jumlah baris = 3
   2   4 | jumlah baris = 6
Total seluruh hasil = 9
Banyak hasil genap = 3
```

## Analisis Efisiensi

Pada Tugas 3 terdapat nested loop. Loop luar berjalan sebanyak `n` kali dan loop dalam juga berjalan sebanyak `n` kali untuk setiap iterasi loop luar.

Jadi, badan loop dalam dijalankan sebanyak:

```text
n × n = n²
```

Contohnya:

* `n = 1` → 1 iterasi
* `n = 2` → 4 iterasi
* `n = 3` → 9 iterasi

Semakin besar nilai `n`, semakin banyak operasi yang dilakukan. Oleh karena itu, batas loop harus dibuat sesuai kebutuhan agar tidak melakukan perulangan yang tidak diperlukan.

## Kuis Formatif

Kuis formatif terdiri dari 10 pertanyaan mengenai nested loop, akumulasi, pencacahan, dan Git.

1. Jika loop luar berjalan 4 kali dan loop dalam 6 kali, total iterasi badan loop dalam adalah **24 iterasi**.
2. Loop dalam kembali ke nilai awal setiap kali loop luar berpindah ke iterasi berikutnya.
3. `print()` setelah loop dalam berfungsi untuk berpindah ke baris berikutnya pada pola.
4. `total_baris` diinisialisasi di dalam loop luar sebelum loop dalam agar nilainya direset untuk setiap baris.
5. `total_semua` diinisialisasi sebelum loop luar agar mencakup seluruh pasangan.
6. Counter digunakan untuk menghitung banyak kejadian, sedangkan accumulator digunakan untuk menjumlahkan nilai.
7. Jika `i` dan `j` dari 1 sampai 3, terdapat **9 pasangan** yang diperiksa.
8. `if` dapat ditempatkan di dalam nested loop untuk memeriksa kondisi dan menambah counter ketika kondisi terpenuhi.
9. `working tree clean` berarti tidak ada perubahan file yang belum di-commit.
10. Perintah untuk mengirim commit lokal ke GitHub adalah `git push`.

## Exit Ticket

### 1. Hal yang paling menentukan jumlah iterasi nested loop adalah ...

Batas iterasi pada loop luar dan loop dalam. Jika keduanya masing-masing berjalan `n` kali, jumlah iterasinya menjadi `n²`.

### 2. Perbedaan akumulasi per baris dan akumulasi keseluruhan adalah ...

Akumulasi per baris menggunakan `total_baris` yang direset pada setiap baris, sedangkan akumulasi keseluruhan menggunakan `total_semua` yang terus menyimpan jumlah dari seluruh baris.

### 3. Bagian program Pertemuan 6 yang paling tepat dijadikan fungsi pada Pertemuan 7 adalah ...

Bagian pembuatan tabel perkalian dan perhitungan statistik, karena bagian tersebut memiliki proses yang jelas dan dapat dipisahkan menjadi fungsi agar dapat dipanggil dan digunakan kembali.

## Refleksi

Pada Pertemuan 06 saya memahami bahwa nested loop digunakan ketika suatu proses perlu dilakukan berulang untuk setiap nilai dari loop luar. Saya juga memahami pentingnya menentukan posisi inisialisasi accumulator dan counter. `total_baris` harus direset pada setiap baris, sedangkan `total_semua` tidak boleh direset karena digunakan untuk menghitung seluruh hasil.

Selain itu, saya belajar melakukan pengujian dengan beberapa nilai `n` untuk memastikan program menghasilkan nilai yang benar. Saya juga belajar bahwa semakin besar nilai `n`, jumlah iterasi nested loop dapat bertambah dengan cepat karena jumlah operasi mengikuti `n²`.

Pada bagian Git dan GitHub, saya belajar menyimpan perkembangan program melalui commit dan mengirim hasil kerja ke repository menggunakan `git push`.
