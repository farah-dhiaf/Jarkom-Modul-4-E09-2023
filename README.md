# Jarkom-Modul-4-E09-2023

|Nama Anggota |NRP |
|---|---|
|Thoriq Fatihassalam | 5025201254 |
|Farah Dhia Fadhila | 5025211030 |

## Soal
![image](https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/20a8b803-bcb1-4060-bb46-1a7a9970d4f0) </br>

**Keterangan:**
- Prefix 10.41 
- VLSM pada GNS3 
- CIDR pada Cisco Packet Tracer
- Tree dan subnetting dapat dilihat dengan jelas pada [Miro](https://miro.com/app/board/uXjVNGrjsTE=/?share_link_id=91337035905).

## Rute 
Sebelum memulai, kami membuat rute subnet terlebih dahulu dimulai dari A1 sampai A21, dan juga kami menghitung jumlah host untuk menentukan netmask masing-masing subnet. </br>
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/f16c8be3-eede-4771-97cd-8ded3c68f6f2">

## Topologi GNS3
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/3ff4d32d-2165-46a1-bdc5-299787d8c89d">

## VLSM
VLSM (Variable Length Subnet Masking) merupakan teknik yang digunakan dalam desain jaringan IP untuk mengalokasikan alamat IP dengan efisien dan menghemat ruang alamat. VLSM memungkinkan administrator jaringan untuk menggunakan panjang subnet yang berbeda untuk subnet yang berbeda, sehingga subnet dengan ukuran yang bervariasi dapat berdampingan dalam infrastruktur jaringan yang sama. Inti utama dari penggunaan teknik VLSM adalah untuk mengefisienkan pembagian IP di dalam jaringan. Besar netmask disesuaikan dengan banyaknya komputer/ host yang membutuhkan alamat IP. Jadi, pada teknik VLSM, subnet mask (netmask) akan diberikan sesuai dengan kebutuhan jumlah alamat IP dari subnet tersebut.

## Tree VLSM
Tree yang lebih jelas diakses pada [Miro](https://miro.com/app/board/uXjVNGrjsTE=/?share_link_id=91337035905).</br>
![image](https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/39a0a7f0-5a47-45bd-a8e5-eafe856ccdbd)

## Pembagian IP VLSM
Setelah membuat tree dengan metode VLSM, kita akan mendapatkan IP untuk masing-masing subnet, dan berikut adalah daftar IP yang sudah didapatkan. </br>
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/f9fbf95a-6907-459d-86b2-628a1de11054"></br>

## Subnetting
Kami membagikan IP tersebut ke masing-masing node untuk dilakukan subnetting.</br>
![image](https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/1c71cc5a-805e-4917-952e-beb825eaa1eb)

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

### Router-Router
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/00e68311-e734-4c0f-899b-8ba0e4ec5ac9">

### Server-Server
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/a47274dc-2b9a-43bf-afc7-cd00b97b8f75">

### Server-Router
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/e12473fc-457a-4bd2-ae20-c9ae67aba291">



## Topologi CISCO
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/02f774cd-c67c-4a9e-8873-8937a321d19a">

## CIDR 
CIDR (Classless Inter-Domain Routing) merupakan metode pengalamatan IP yang memungkinkan penggunaan lebih efisien dari ruang alamat IP dan pengelolaan alamat IP yang lebih fleksibel daripada metode tradisional berdasarkan kelas. Perhitungan pada teknik CIDR juga didasarkan pada jumlah komputer/ host yang ada di dalam subnet. Tetapi cara mendapatkan subnet besar tidak sama dengan VLSM.

## Penggabungan Subnet
Kami melakukan penggabungan subnet dimulai dari subnet paling jauh dari router default yaitu Aura. </br>
![image](https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/a6884545-41e4-488d-abca-82259835e0a7)
Berikut adalah hasil dari penggabungan subnet dan netmask akhir yang didapat. </br>
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/9ccf7ad8-0e88-4d61-a6d2-486cac3cc45d"> </br>

## Tree CIDR 
Setelah menggabungkan subnet-subnet tersebut, kami membuat tree dengan metode CIDR untuk mendapatkan IP untuk masing-masing subnet.
Tree yang lebih jelas diakses pada [Miro](https://miro.com/app/board/uXjVNGrjsTE=/?share_link_id=91337035905).
![image](https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/abd92005-0c43-40a2-85ab-f381a53e6af9)

## Pembagian IP
Setelah membuat tree, kami mendapatkan IP untuk subnet-subnet, berikut adalah listnya. </br>
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/56ca009d-63a3-4344-8e83-95ae34bb57e9">


## Subnetting
Kami melakukan konfigurasi untuk masing-masing node untuk dilakukan subnetting. Konfigurasi mengikuti pembagian IP untuk node berikut. </br>
![image](https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/e2ca0126-8000-41b3-ac74-45844dce8329)

## Routing 
### Aura
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/04d6aa20-f04e-4cfd-b4c0-dfccce18e594"> </br>
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/f335c192-9982-4703-9255-e82a7e5dad70"> </br>
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/cf611c84-d7c2-4c91-8934-9a32571bfbbd">

### Denken
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/e0358bd4-c517-43c2-82bb-f8ff1b77fc2e">

### Frieren
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/70489d0b-9353-48df-81d2-3bdd49bcc3e1">

### Flamme
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/4cc451ae-21f7-4af1-82e7-96ba0be7242d">

### Fern
<img width="253" alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/272d1ebb-1ce7-48eb-90ca-84c82393eb52">

### Himmel
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/0298b70b-6bd5-41e6-89ec-c7cd85981473">

### Eisen
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/9fb482fa-93ba-4d43-a074-c83cdc10fa5c">

### Lugner
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/0c67f1b7-d780-453a-aee6-77c767ff5d95">

### Linie
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/1c27bef5-8403-4cfe-94ff-acd1dc0cbb8f">

### Lawine
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/89190ca7-8bc3-48cf-9435-9d0cbb20434d">

### Heiter
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/44fbd055-e218-486b-9c2b-13bd01b8e7b7">

## Testing
### Client-Server
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/56a2e1e7-ccc6-4f86-bee3-bf1fd8b53df4">

### Client-Router
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/94ce41bd-a2e3-4afa-b140-3f59977b07c5">

### Server-Router
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/f3c448e4-4944-4273-8dd9-146bac257ee1">

### Client-Client
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/3b5c74a0-6407-43ab-83f8-b2f4149b0aad">

### Server-Server
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/a1c583be-a986-475d-b414-9d0a781227f0">

### Router-Router
<img alt="image" src="https://github.com/farah-dhiaf/Jarkom-Modul-4-E09-2023/assets/91003215/a1a98c79-8bf5-4be1-89e0-1b2a2cbd2894">

## Kendala
Node yang sangat banyak membuat routing menjadi sangat menguli.
