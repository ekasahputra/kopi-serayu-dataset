# Dataset Kopi Serayu

Dataset latihan untuk buku **Literasi TIK untuk Mahasiswa: Dari Mencari Referensi sampai Membaca Data**.

Kopi Serayu adalah kedai kopi **rekaan** dengan dua gerai, Kampus dan Kota, di Purwokerto. Semua data di sini **sintetis**, yaitu dibuat dengan program komputer khusus untuk latihan, sehingga tidak menggambarkan usaha mana pun dan tidak memuat data pribadi.

## Cara mengunduh

- **Semua berkas sekaligus:** klik tombol hijau **Code** di atas, lalu pilih **Download ZIP**.
- **Satu berkas saja:** klik nama berkasnya, lalu klik ikon unduh (**Download raw file**) di kanan atas.
- **Langsung dari Google Colab** (Bab 12), tanpa mengunggah berkas:

```python
import pandas as pd
url = "https://raw.githubusercontent.com/ekasahputra/kopi-serayu-dataset/main/kopi_serayu_2026.csv"
data = pd.read_csv(url, parse_dates=["tanggal"])
```

## Daftar berkas

| No | Berkas | Isi | Dipakai pada |
|---|---|---|---|
| 1 | `kopi_serayu_2026.xlsx` | 20.259 baris penjualan 1 Januari sampai 31 Desember 2026; lembar Transaksi, Menu, dan Keterangan | Bab 8, 9, 11 |
| 2 | `kopi_serayu_2026.csv` | isi lembar Transaksi dalam format CSV (UTF-8, pemisah koma) | Bab 12 |
| 3 | `kopi_serayu_maret_kotor.xlsx` | 1.757 baris penjualan Maret 2026 yang sengaja dibuat tidak rapi | Bab 10 |

## Kolom pada lembar Transaksi

| No | Kolom | Tipe | Keterangan |
|---|---|---|---|
| 1 | `id_transaksi` | teks | nomor nota; satu nota dapat terdiri atas beberapa baris |
| 2 | `tanggal` | tanggal | tanggal transaksi |
| 3 | `jam` | waktu | jam transaksi |
| 4 | `gerai` | teks | Kampus atau Kota |
| 5 | `saluran` | teks | Makan di Tempat, Bawa Pulang, atau Antar Daring (mulai April 2026) |
| 6 | `kode_menu` | teks | kode yang menghubungkan ke lembar Menu |
| 7 | `nama_menu` | teks | nama menu |
| 8 | `kategori` | teks | Kopi, Nonkopi, atau Makanan |
| 9 | `jumlah` | angka | banyaknya porsi |
| 10 | `harga_satuan` | angka | harga satu porsi (rupiah) |
| 11 | `total` | angka | jumlah dikali harga satuan (rupiah) |
| 12 | `metode_bayar` | teks | Tunai, QRIS, Kartu Debit, atau Dompet Digital |
| 13 | `jenis_pelanggan` | teks | Member atau Umum |

## Lembar Menu

| Kode | Nama menu | Kategori | Harga (Rp) | HPP (Rp) |
|---|---|---|---|---|
| K01 | Es Kopi Susu Serayu | Kopi | 18.000 | 7.000 |
| K02 | Americano | Kopi | 15.000 | 4.500 |
| K03 | Cappuccino | Kopi | 22.000 | 8.000 |
| K04 | Kopi Tubruk | Kopi | 10.000 | 3.000 |
| K05 | Es Kopi Gula Aren | Kopi | 20.000 | 7.500 |
| N01 | Es Teh Manis | Nonkopi | 7.000 | 1.500 |
| N02 | Cokelat Panas | Nonkopi | 18.000 | 7.000 |
| N03 | Matcha Latte | Nonkopi | 23.000 | 9.000 |
| M01 | Mendoan (3 pcs) | Makanan | 10.000 | 4.000 |
| M02 | Roti Bakar Cokelat | Makanan | 15.000 | 6.000 |
| M03 | Nasi Goreng | Makanan | 22.000 | 10.000 |
| M04 | Kentang Goreng | Makanan | 15.000 | 6.000 |

## Berkas Maret yang tidak rapi

Berkas `kopi_serayu_maret_kotor.xlsx` memakai kolom `waktu` yang berisi tanggal dan jam dalam satu teks, serta kolom `harga_satuan` berupa teks seperti "Rp18.000". Masalah lainnya sengaja tidak dirinci karena menemukannya merupakan bagian dari latihan Bab 10.

## Lisensi

Dataset ini dapat dipakai, disalin, dan diubah untuk keperluan belajar maupun mengajar dengan lisensi [Creative Commons Attribution 4.0 (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/deed.id), dengan menyebutkan sumbernya:

> Sahputra, E. (2027). *Dataset Kopi Serayu* [Data set]. Pendamping buku Literasi TIK untuk Mahasiswa. https://github.com/ekasahputra/kopi-serayu-dataset
