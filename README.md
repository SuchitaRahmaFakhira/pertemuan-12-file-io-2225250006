# Pertemuan 12 - File I/O dan Error Handling

Nama: Suchita Rahma Fakhira  
NIM: 2225250006  
Kelas: 3B

## Tujuan
Membaca, memvalidasi, mengolah, dan menulis data file dengan Python.

## Format File Input
Format data pada file `data/nilai.txt` adalah:

NIM,nilai

Contoh:
```text
A001,85
A002,78
A003,92
```

## Cara Menjalankan
Jalankan perintah berikut pada terminal VS Code:

```bash
python tugas/rekap_nilai_file.py
```

## Error yang Ditangani
- `FileNotFoundError`: menangani kondisi ketika file tidak ditemukan.
- `ValueError`: menangani data nilai yang tidak valid atau bukan angka.

## Test Case

<table>
  <thead>
    <tr>
      <th>Kondisi</th>
      <th>Hasil yang Diharapkan</th>
      <th>Hasil Aktual</th>
      <th>Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Data normal</td>
      <td>Data valid berhasil direkap</td>
      <td>Data berhasil direkap</td>
      <td>Berhasil</td>
    </tr>
    <tr>
      <td>Data nilai tidak valid (A004,abc)</td>
      <td>Data tidak valid dilewati dan data lain tetap diproses</td>
      <td>Data tidak valid dilewati</td>
      <td>Berhasil</td>
    </tr>
    <tr>
      <td>Baris kosong</td>
      <td>Baris kosong dilewati</td>
      <td>Baris kosong dilewati</td>
      <td>Berhasil</td>
    </tr>
    <tr>
      <td>Nilai 60</td>
      <td>Dihitung sebagai lulus</td>
      <td>Nilai 60 dihitung sebagai lulus</td>
      <td>Berhasil</td>
    </tr>
    <tr>
      <td>File tidak ditemukan</td>
      <td>Pesan kesalahan ditampilkan tanpa program crash</td>
      <td>Pesan kesalahan ditampilkan</td>
      <td>Berhasil</td>
    </tr>
  </tbody>
</table>


## Refleksi
Pada praktikum ini, saya mempelajari cara membaca dan menulis file menggunakan Python serta mengolah data nilai secara terstruktur. Saya juga mempelajari penggunaan `try-except` untuk menangani error. Ketika terdapat nilai yang tidak valid, program melewati baris tersebut sehingga data lainnya tetap dapat diproses.