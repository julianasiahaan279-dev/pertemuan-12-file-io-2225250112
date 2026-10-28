# Pertemuan 12 - File I/O dan Error Handling

Nama: Angelita Juliana Siahaan
NIM: 2225250112
Kelas: 3B

## Tujuan
Membaca, memvalidasi, mengolah, dan menulis data file dengan Python.

## Format File Input
NIM,nilai (satu record per baris, contoh: A001,85)

## Cara Menjalankan
python tugas/rekap_nilai_file.py

## Error yang Ditangani
- FileNotFoundError
- ValueError

## Test Case
| Kondisi | Hasil diharapkan | Hasil aktual | Status |
|---|---|---|---|
| Normal (5 baris valid) | 5 data valid, rata-rata 83.40, lulus 5 | Sesuai | Lulus |
| File hilang | Pesan file tidak ditemukan, tidak crash | Sesuai | Lulus |
| Nilai invalid (A004,abc) | Baris 4 dilewati, 5 data lain diproses | Sesuai | Lulus |
| Baris kosong | Baris kosong dilewati, 3 data valid | Sesuai | Lulus |
| Batas lulus (nilai 60) | 60 dihitung lulus, 59 tidak, lulus = 2 | Sesuai | Lulus |

## Refleksi
Error yang ditemukan: nilai "abc" tidak bisa diubah ke float (ValueError). Program menangani dengan try-except per baris, jadi baris itu dilewati dan baris lain tetap diproses.