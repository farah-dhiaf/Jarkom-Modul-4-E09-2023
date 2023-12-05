# Jarkom-Modul-4-E09-2023

|Nama Anggota |NRP |
|---|---|
|Thoriq Fatihassalam | 5025201254 |
|Farah Dhia Fadhila | 5025211030 |

Pada praktikum kali ini, kami mengimplementasikan VLSM untuk GNS3 dan CIDR untuk CPT dengan prefix kelompok kami yaitu 10.41

## Rute 
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/f16c8be3-eede-4771-97cd-8ded3c68f6f2">

## Topologi VLSM - GNS3
![image](https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/4b8d68e0-815b-4ddb-bc2f-50d3d672ef41)

## VLSM
VLSM (Variable Length Subnet Masking) merupakan teknik yang digunakan dalam desain jaringan IP untuk mengalokasikan alamat IP dengan efisien dan menghemat ruang alamat. VLSM memungkinkan administrator jaringan untuk menggunakan panjang subnet yang berbeda untuk subnet yang berbeda, sehingga subnet dengan ukuran yang bervariasi dapat berdampingan dalam infrastruktur jaringan yang sama. Inti utama dari penggunaan teknik VLSM adalah untuk mengefisienkan pembagian IP di dalam jaringan. Besar netmask disesuaikan dengan banyaknya komputer/ host yang membutuhkan alamat IP. Jadi, pada teknik VLSM, subnet mask (netmask) akan diberikan sesuai dengan kebutuhan jumlah alamat IP dari subnet tersebut.

## Tree VLSM
[Miro](https://miro.com/app/board/uXjVNGrjsTE=/?share_link_id=91337035905)
![image](https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/39a0a7f0-5a47-45bd-a8e5-eafe856ccdbd)

## Pembagian IP VLSM
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/44cf5735-7f46-458b-af8e-993ea7d1f73c">

## Subnetting
### Aura
```
auto eth0	
iface eth0 inet dhcp	

auto eth1	
iface eth1 inet static	
         address 10.41.7.125
         netmask 255.255.255.252

auto eth2
iface eth2 inet static	
         address 10.41.7.117
         netmask 255.255.255.252

auto eth3
iface eth3 inet static	
         address 10.41.7.121
         netmask 255.255.255.252
```
### Frieren
```
auto eth0
iface eth0 inet static
	address 10.41.7.126
	netmask 255.255.255.252
	gateway 10.41.7.125

auto eth1
iface eth1 inet static
	address 10.41.7.161
	netmask 255.255.255.224

auto eth2
iface eth2 inet static
	address 10.41.7.129
	netmask 255.255.255.252
```
### Denken
```
auto eth0
iface eth0 inet static
	address 10.41.7.118
	netmask 255.255.255.252
	gateway 10.41.7.117

auto eth1
iface eth1 inet static
	address 10.41.9.1
	netmask 255.255.255.0

```
### Eisen
```
auto eth0
iface eth0 inet static
	address 10.41.7.122
	netmask 255.255.255.252
	gateway 10.41.7.121

auto eth1
iface eth1 inet static
	address 10.41.7.113
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.41.7.145
	netmask 255.255.255.248

auto eth3
iface eth3 inet static
	address 10.41.7.141
	netmask 255.255.255.252

auto eth4
iface eth4 inet static
	address 10.41.7.109
	netmask 255.255.255.252
```
### Flamme
```
auto eth0
iface eth0 inet static
	address 10.41.7.130
	netmask 255.255.255.252
	gateway 10.41.7.129

auto eth1
iface eth1 inet static
	address 10.41.20.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 10.41.7.133
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 10.41.7.137
	netmask 255.255.255.252

```
### Fern
```
auto eth0
iface eth0 inet static
	address 10.41.7.134
	netmask 255.255.255.252
	gateway 10.41.7.133

auto eth1
iface eth1 inet static
	address 10.41.24.1
	netmask 255.255.248.0
```
### Himmel
```
auto eth0
iface eth0 inet static
	address 10.41.7.138
	netmask 255.255.255.252
	gateway 10.41.7.137

auto eth1
iface eth1 inet static
	address 10.41.7.153
	netmask 255.255.255.248
```
### Linie
```
auto eth0
iface eth0 inet static
	address 10.41.7.142
	netmask 255.255.255.252
	gateway 10.41.7.141

auto eth1
iface eth1 inet static
	address 10.41.10.1
	netmask 255.255.254.0

auto eth2
iface eth2 inet static
	address 10.41.7.105
	netmask 255.255.255.252
```
### Lawine
```
auto eth0
iface eth0 inet static
	address 10.41.7.106
	netmask 255.255.255.252
	gateway 10.41.7.105

auto eth1
iface eth1 inet static
	address 10.41.7.193
	netmask 255.255.255.192
```
### Lugner
```
auto eth0
iface eth0 inet static
	address 10.41.7.110
	netmask 255.255.255.252
	gateway 10.41.7.109

auto eth1
iface eth1 inet static
	address 10.41.8.1
	netmask 255.255.255.0

auto eth2
iface eth2 inet static
	address 10.41.16.1
	netmask 255.255.252.0
```
### Heiter
```
auto eth0
iface eth0 inet static
	address 10.41.7.194
	netmask 255.255.255.192
	gateway 10.41.7.193

auto eth1
iface eth1 inet static
	address 10.41.12.1
	netmask 255.255.252.0
```
### RoyalCapital
```
auto eth0
iface eth0 inet static
	address 10.41.9.2
	netmask 255.255.255.0
	gateway 10.41.9.1
```
### WilleRegion
```
auto eth0
iface eth0 inet static
	address 10.41.9.3
	netmask 255.255.255.0
	gateway 10.41.9.1
```
### TurkRegion
```
auto eth0
iface eth0 inet static
	address 10.41.16.2
	netmask 255.255.252.0
	gateway 10.41.16.1
```
### GrobeForest
```
auto eth0
iface eth0 inet static
	address 10.41.8.2
	netmask 255.255.255.0
	gateway 10.41.8.1
```
### GranzChannel
```
auto eth0
iface eth0 inet static
	address 10.41.10.2
	netmask 255.255.254.0
	gateway 10.41.10.1
```
### BredtRegion
```
auto eth0
iface eth0 inet static
	address 10.41.7.195
	netmask 255.255.255.192
	gateway 10.41.7.193
```
### RiegelCanyon
```
auto eth0
iface eth0 inet static
	address 10.41.12.2
	netmask 255.255.252.0
	gateway 10.41.12.1
```
### SchwerMountains
```
auto eth0
iface eth0 inet static
	address 10.41.7.154
	netmask 255.255.255.248
	gateway 10.41.7.153
```
### RohrRoad
```
auto eth0
iface eth0 inet static
	address 10.41.20.2
	netmask 255.255.252.0
	gateway 10.41.20.1
```
### AppetitRegion
```
auto eth0
iface eth0 inet static
	address 10.41.24.2
	netmask 255.255.248.0
	gateway 10.41.24.1
```
### LaubHills
```
auto eth0
iface eth0 inet static
	address 10.41.24.3
	netmask 255.255.248.0
	gateway 10.41.24.1
```
### LakeKorridor
```
auto eth0
iface eth0 inet static
	address 10.41.7.162
	netmask 255.255.255.224
	gateway 10.41.7.161
```
### Stark
```
auto eth0
iface eth0 inet static
	address 10.41.7.114
	netmask 255.255.255.252
	gateway 10.41.7.113
```
### Richter
```
auto eth0
iface eth0 inet static
	address 10.41.7.146
	netmask 255.255.255.248
	gateway 10.41.7.145
```
### Revolte
```
auto eth0
iface eth0 inet static
	address 10.41.7.147
	netmask 255.255.255.248
	gateway 10.41.7.145
```
### Sein
```
auto eth0
iface eth0 inet static
	address 10.41.12.2
	netmask 255.255.252.0
	gateway 10.41.12.1
```

## Routing
### Aura
```
route add -net 10.41.7.160 netmask 255.255.255.252 gw 10.41.7.126 
route add -net 10.41.7.128 netmask 255.255.255.252 gw 10.41.7.126 
route add -net 10.41.9.0 netmask 255.255.255.0 gw 10.41.7.118
route add -net 10.41.7.112 netmask 255.255.255.252 gw 10.41.7.122
route add -net 10.41.7.144 netmask 255.255.255.248 gw 10.41.7.122
route add -net 10.41.7.108 netmask 255.255.255.252 gw 10.41.7.122
route add -net 10.41.16.0 netmask 255.255.252.0 gw 10.41.7.122
route add -net 10.41.8.0 netmask 255.255.255.0 gw 10.41.7.122
route add -net 10.41.7.140 netmask 255.255.255.252 gw 10.41.7.122
route add -net 10.41.10.0 netmask 255.255.254.0 gw 10.41.7.122
route add -net 10.41.7.104 netmask 255.255.255.252 gw 10.41.7.122
route add -net 10.41.7.132 netmask 255.255.255.252 gw 10.41.7.126
route add -net 10.41.24.0 netmask 255.255.248.0 gw 10.41.7.126
route add -net 10.41.20.0 netmask 255.255.252.0 gw 10.41.7.126
route add -net 10.41.7.136 netmask 255.255.255.252 gw 10.41.7.126
route add -net 10.41.7.152 netmask 255.255.255.248 gw 10.41.7.126
route add -net 10.41.7.192 netmask 255.255.255.192 gw 10.41.7.122
route add -net 10.41.12.0 netmask 255.255.252.0 gw 10.41.7.122
```

### Flamme
```
route add -net 10.41.24.0 netmask 255.255.248.0 gw 10.41.7.134
route add -net 10.41.7.152 netmask 255.255.255.248 gw 10.41.7.138
```

### Frieren
```
route add -net 10.41.7.132 netmask 255.255.255.252 gw 10.41.7.130
route add -net 10.41.24.0 netmask 255.255.248.0 gw 10.41.7.130
route add -net 10.41.20.0 netmask 255.255.252.0 gw 10.41.7.130
route add -net 10.41.7.136 netmask 255.255.255.252 gw 10.41.7.130
route add -net 10.41.7.152 netmask 255.255.255.248 gw 10.41.7.130
```

### Linie
```
route add -net 10.41.7.192 netmask 255.255.255.192 gw 10.41.7.106
route add -net 10.41.12.0 netmask 255.255.252.0 gw 10.41.7.106
```
### Lawine
```
route add -net 10.41.12.0 netmask 255.255.252.0 gw 10.41.7.194
```
### Eisen
```
route add -net 10.41.16.0 netmask 255.255.252.0 gw 10.41.7.110
route add -net 10.41.8.0 netmask 255.255.255.0 gw 10.41.7.110
route add -net 10.41.10.0 netmask 255.255.254.0 gw 10.41.7.142
route add -net 10.41.7.104 netmask 255.255.255.252 gw 10.41.7.142
route add -net 10.41.7.192 netmask 255.255.255.192 gw 10.41.7.142
route add -net 10.41.12.0 netmask 255.255.252.0 gw 10.41.7.142
```

## Testing
### Client-Client
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/80076c59-2381-494a-a3c9-4b3b61ffc83d">

### Client-Router
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/42e246ba-9da9-4d96-8498-f2f1ead07ac3">

### Client-Server
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/6ce459bf-b0bc-48d1-b1ff-1e2780a93043">

## Topologi CIDR - CISCO
![image](https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/a6884545-41e4-488d-abca-82259835e0a7)

## CIDR 
CIDR (Classless Inter-Domain Routing) merupakan metode pengalamatan IP yang memungkinkan penggunaan lebih efisien dari ruang alamat IP dan pengelolaan alamat IP yang lebih fleksibel daripada metode tradisional berdasarkan kelas. Perhitungan pada teknik CIDR juga didasarkan pada jumlah komputer/ host yang ada di dalam subnet. Tetapi cara mendapatkan subnet besar tidak sama dengan VLSM.

## Tree CIDR 
[Miro](https://miro.com/app/board/uXjVNGrjsTE=/?share_link_id=91337035905)
![image](https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/d58e4f93-0887-461f-879c-ba29874b2fdc)

## Penggabungan Subnet
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/9ccf7ad8-0e88-4d61-a6d2-486cac3cc45d">

## Pembagian IP
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/b35db36c-fa61-4377-8cca-bcb84e54d891">
