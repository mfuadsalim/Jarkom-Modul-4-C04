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

#### Mengatur _Network Configuration_ masing-masing interface pada setiap perangkat

##### Router
Atur IP pada interface setiap router dan set Port status menjadi **On**

- **The Resonance**
  - FastEthernet0/1
  ```
  IPv4 Address 192.181.11.201
  Subnet Mask 255.255.255.252
  ```
  - Ethernet1/0
  ```
  IPv4 Address 192.181.11.209
  Subnet Mask 255.255.255.252
  ```
  - Ethernet1/1
  ```
  IPv4 Address 192.181.11.213
  Subnet Mask 255.255.255.252
  ```
  - Ethernet1/2
  ```
  IPv4 Address 192.181.11.205
  Subnet Mask 255.255.255.252
  ```
- **The Magical**
  - FastEthernet0/0
  ```
  IPv4 Address 192.181.11.210
  Subnet Mask 255.255.255.252
  ```
  - FastEthernet0/1
  ```
  IPv4 Address 192.181.0.1
  Subnet Mask 255.255.254.0
  ```
- **The Order**
  - FastEthernet0/0
  ```
  IPv4 Address 192.181.11.202
  Subnet Mask 255.255.255.252
  ```
  - FastEthernet0/1
  ```
  IPv4 Address 192.181.11.197
  Subnet Mask 255.255.255.252
  ```
  - FastEthernet1/0
  ```
  IPv4 Address 192.181.11.129
  Subnet Mask 255.255.255.192
  ```
- **The Minister**
  - FastEthernet0/0
  ```
  IPv4 Address 192.181.11.198
  Subnet Mask 255.255.255.252
  ```
  - FastEthernet0/1
  ```
  IPv4 Address 192.181.4.1
  Subnet Mask 255.255.252.0
  ```
  - FastEthernet1/0
  ```
  IPv4 Address 192.181.11.193
  Subnet Mask 255.255.255.252
  ```
- **The Dauntless**
  - FastEthernet0/0
  ```
  IPv4 Address 192.181.11.194
  Subnet Mask 255.255.255.252
  ```
  - FastEthernet0/1
  ```
  IPv4 Address 192.181.8.1
  Subnet Mask 255.255.255.0
  ```
- **The Instrument**
  - FastEthernet0/0
  ```
  IPv4 Address 192.181.10.1
  Subnet Mask 255.255.255.128
  ```
  - FastEthernet0/1
  ```
  IPv4 Address 192.181.11.214
  Subnet Mask 255.255.255.252
  ```
  - FastEthernet1/0
  ```
  IPv4 Address 192.181.11.221
  Subnet Mask 255.255.255.252
  ```
  - FastEthernet1/1
  ```
  IPv4 Address 192.181.11.217
  Subnet Mask 255.255.255.252
  ```
- **The Profound**
  - FastEthernet0/0
  ```
  IPv4 Address 192.181.11.218
  Subnet Mask 255.255.255.252
  ```
  - FastEthernet0/1
  ```
  IPv4 Address 192.181.10.129
  Subnet Mask 255.255.255.128
  ```
  - FastEthernet1/0
  ```
  IPv4 Address 192.181.11.1
  Subnet Mask 255.255.255.128
  ```
- **The Firefist**
  - FastEthernet0/0
  ```
  IPv4 Address 192.181.11.222
  Subnet Mask 255.255.255.252
  ```
  - FastEthernet0/1
  ```
  IPv4 Address 192.181.9.1
  Subnet Mask 255.255.255.0
  ```
  - FastEthernet1/0
  ```
  IPv4 Address 192.181.2.1
  Subnet Mask 255.255.254.0
  ```
- **The Queen**
  - FastEthernet0/0
  ```
  IPv4 Address 192.181.11.225
  Subnet Mask 255.255.255.252
  ```
  - FastEthernet0/1
  ```
  IPv4 Address 192.181.9.2
  Subnet Mask 255.255.255.0
  ```

##### Client

- **Johan (100 Host)**

```
IPv4 Address 192.181.8.3
Subnet Mask 255.255.255.0
Default Gateway 192.181.8.1
```

- **Phanora (150 Host)**

```
IPv4 Address 192.181.8.2
Subnet Mask 255.255.255.0
Default Gateway 192.181.8.1
```

- **Guideau (1000 Host)**

```
IPv4 Address 192.181.4.2
Subnet Mask 255.255.252.0
Default Gateway 192.181.4.1
```

- **Ashaf (50 Host)**

```
IPv4 Address 192.181.11.130
Subnet Mask 255.255.252.192
Default Gateway 192.181.11.129
```

- **Haines (70 Host)**

```
IPv4 Address 192.181.0.2
Subnet Mask 255.255.254.0
Default Gateway 192.181.0.1
```

- **Corvekt (200 Host)**

```
IPv4 Address 192.181.0.3
Subnet Mask 255.255.254.0
Default Gateway 192.181.0.1
```

- **Matt Cugat (120 Host)**

```
IPv4 Address 192.181.10.2
Subnet Mask 255.255.255.128
Default Gateway 192.181.10.1
```

- **Spendrow (120 Host)**

```
IPv4 Address 192.181.10.130
Subnet Mask 255.255.255.128
Default Gateway 192.181.10.129
```

- **Helga (70 Host)**

```
IPv4 Address 192.181.11.2
Subnet Mask 255.255.255.128
Default Gateway 192.181.11.1
```

- **Oakleave (500 Host)**

```
IPv4 Address 192.181.2.2
Subnet Mask 255.255.254.0
Default Gateway 192.181.2.1
```

- **Keith (210 Host)**

```
IPv4 Address 192.181.9.3
Subnet Mask 255.255.255.0
Default Gateway 192.181.9.1
```

##### Server

- **The Beast**

```
IPv4 Address 192.181.11.206
Subnet Mask 255.255.255.252
Default Gateway 192.181.11.205
```

- **The Witch**

```
IPv4 Address 192.181.11.226
Subnet Mask 255.255.255.252
Default Gateway 192.181.11.225
```
