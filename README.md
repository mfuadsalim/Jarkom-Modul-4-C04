# Jarkom-Modul-4-C04-2022

Laporan Resmi Praktikum Modul 4 Kelompok C04

## Kelompok C04

| **Nama**                  | **NRP**    |
| ------------------------- | ---------- |
| Muhammad Fuad Salim | 5025201057 |
| Handitanto Herprasetyo | 5025201077 |
| Sastiara Maulikh | 5025201257 |

IP Prefix Kelompok C04 : '192.181'

## Soal Praktikum Modul 4
# Topologi

- Soal shift dikerjakan pada Cisco Packet Tracer dan GNS3 menggunakan metode perhitungan CLASSLESS yang berbeda. Keterangan: Bila di CPT menggunakan VLSM, maka di GNS3 menggunakan CIDR atau Sebaliknya
- Jika tidak ada pemberitahuan revisi soal dari asisten, berarti semua soal BERSIFAT BENAR dan DAPAT DIKERJAKAN. Untuk di GNS3 CLOUD merupakan NAT1 jangan sampai salah agar bisa terkoneksi internet.
- Pembagian IP menggunakan Prefix IP yang telah ditentukan pada modul pengenalan.
- Pembagian IP dan routing harus SE-EFISIEN MUNGKIN.

Dalam mengerjakan soal ini, kami menggunakan teknik VLSM dengan menggunakan CPT, dan teknik CIDR dengan menggunakan GNS 3

# VLSM dan CPT
## Pembagian Subnet
Hal pertama yang akan dilakukan adalah dengan menentukan subnet yang ada pada topologi. Dikarenakan metode yang dipakai adalah VLSM. Kami melingkari tiap host yang terhubung pada interface router dan menghitung IP yang dibutuhkan. Berikut adalah gambaran pembagian subnetnya :
## Pembagian Subnet
gambarnya disini
## Jumlah IP
Setelah melakukan pembagian subnet kita melakukan penjumlahan pada IP, sehingga didapatkan hasil penjumlahan ip berikut :
gambar table
## VLSM Tree
Setelah mendapatkan penjumlahan IP kita membuat tree yang terdapat pada topologi. Pada subnet kami memiliki NID 192.181.0.0 dengan netmask /20 sehingga pembagian IP berdasarkan NID dan Netmask yang di dapat.
Pada VLSM ini diturunkan sesuai dengan netmask atasnya sehingga ketika /20 akan diturunkan menjadi /21, lakukan secara berulang-ulang sampai node semua terpenuhi.
## Pembagian IP 
Kemudian kita bagi dengan tetap menggunakan IP perfix `192.181` . hasil pembagian seperti berikut :
