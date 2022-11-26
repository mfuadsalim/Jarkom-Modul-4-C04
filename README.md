# Jarkom-Modul-4-C04-2022

Laporan Resmi Praktikum Modul 4 Kelompok C04

## Kelompok C04

| **Nama**                  | **NRP**    |
| ------------------------- | ---------- |
| Muhammad Fuad Salim | 5025201057 |
| Handitanto Herprasetyo | 5025201077 |
| Sastiara Maulikh | 5025201257 |

IP Prefix Kelompok C04 : `192.181`

## Soal Praktikum Modul 4
# Topologi
 ![topologi](https://user-images.githubusercontent.com/80630201/204081750-9d342fa6-0085-45e6-b344-c3f6e84d3e89.png)
- Soal shift dikerjakan pada Cisco Packet Tracer dan GNS3 menggunakan metode perhitungan CLASSLESS yang berbeda. Keterangan: Bila di CPT menggunakan VLSM, maka di GNS3 menggunakan CIDR atau Sebaliknya
- Jika tidak ada pemberitahuan revisi soal dari asisten, berarti semua soal BERSIFAT BENAR dan DAPAT DIKERJAKAN. Untuk di GNS3 CLOUD merupakan NAT1 jangan sampai salah agar bisa terkoneksi internet.
- Pembagian IP menggunakan Prefix IP yang telah ditentukan pada modul pengenalan.
- Pembagian IP dan routing harus SE-EFISIEN MUNGKIN.

Dalam mengerjakan soal ini, kami menggunakan teknik VLSM dengan menggunakan CPT, dan teknik CIDR dengan menggunakan GNS 3

# VLSM dan CPT
## Pembagian Subnet
Hal pertama yang akan dilakukan adalah dengan menentukan subnet yang ada pada topologi. Dikarenakan metode yang dipakai adalah VLSM. Kami melingkari tiap host yang terhubung pada interface router dan menghitung IP yang dibutuhkan. Berikut adalah gambaran pembagian subnetnya :
## Pembagian Subnet
![pembagian subnetting](https://user-images.githubusercontent.com/80630201/204081755-c68fb7a5-1895-4870-a6f4-492d3c982b2e.png)
## Jumlah IP
Setelah melakukan pembagian subnet kita melakukan penjumlahan pada IP, sehingga didapatkan hasil penjumlahan ip berikut :
![table](https://user-images.githubusercontent.com/80630201/204081756-1f7471b7-ffaa-415d-bc95-0805fe965520.png)
## VLSM Tree
Setelah mendapatkan penjumlahan IP kita membuat tree yang terdapat pada topologi. Pada subnet kami memiliki `NID 192.181.0.0` dengan netmask /20 sehingga pembagian IP berdasarkan NID dan Netmask yang di dapat.
![tree](https://user-images.githubusercontent.com/80630201/204081752-57696e80-101e-4154-806d-7c398f5ebed9.jpg)
Pada VLSM ini diturunkan sesuai dengan netmask atasnya sehingga ketika /20 akan diturunkan menjadi /21, lakukan secara berulang-ulang sampai node semua terpenuhi.
## Pembagian IP 
Kemudian kita bagi dengan tetap menggunakan IP perfix `192.181` . hasil pembagian seperti berikut :
![ip](https://user-images.githubusercontent.com/80630201/204081753-7b77d442-d340-41bb-9d76-2cd94aaf6246.jpg)
