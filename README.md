# Laporan Resmi Praktikum Jaringan Komputer Modul 4 D20  2023

## Author
| Nama | NRP |Github |
|---------------------------|------------|--------|
|Khairuddin Nasty | 5025201041 | https://github.com/khairuddin-n |
|Altriska Izzati Khairunnisa H | 5025211187 | https://github.com/altriskaa |

## Daftar Isi
- [Laporan Resmi](#laporan-resmi)
- [Daftar Isi](#daftar-isi)
  - [Topologi GNS VLSM](#topologi-gns-vlsm)
  - [Topologi PKT CIDR](#topologi-pkt-cidr)
  - [Prefix IP](#prefix-ip)
  - [Route](#route)
- [VLSM](#vlsm)
  - [Tree](#tree)
  - [Pembagian IP](#pembagian-ip)
  - [Konfigurasi Network](#konfigurasi-network)
  - [Routing](#routing)
  - [Testing](#testing)
- [CIDR](#cidr)
  - [Penggabungan IP](#penggabungan-ip)
  - [Tree](#tree-1)
  - [Pembagian IP](#pembagian-ip-1)
  - [Testing](#testing-1)

## Topologi GNS VLSM 
![image](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/114663340/e24a5a76-2746-44d0-882f-e6643f25ed80)

## Topologi PKT CIDR


## Prefix IP 
Kelompok kami memiliki prefix IP `192.201`

## Route
![image](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/114663340/50f54c31-3a53-4251-aa42-49ce3455e626)

# VLSM

## Tree
![image](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/114663340/b0a52f94-685d-4191-878f-2ef200b884d7)

### Pembagian IP
![image](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/114663340/b7eed327-1ac4-442e-b873-64c237b4f62c)


### Konfigurasi Network

- RoyalCapital (63 Host)


- WilleRegion (63 Host)

- Denken 


- Aura 


- Frieren 


- LakeKorridor (24 Host)


- Flamme 


- Fern 


- LaubHills (397 Host)


- AppetitRegion (625 Host)


- RohrRoad (1000 Host)


- Himmel 


- ShcwerMountains (5 Host)


- Eisen 


- Stark 


- Lugner 


- TurkRegion (1000 Host)

- GrobeForest (250 Host)


- Richter 


- Revolte


- Linie 


- GranzChannel (254 Host)


- Lawine 


- BredtRegion (29 Host)


- Heiter 


- Sein 


- RiegelCanyon (510 Host)


### Routing 

- Denken 


- Lugner 


- Linie 


- Lawine 


- Heiter


- Himmel 


- Flamme 


- Fern 


- Frieren


- Eisen 


- Aura 


### Testing


# CIDR


## Penggabungan IP
### A
![A](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/18bb157d-37c7-45a1-913c-851733e4e484)
### B
![B](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/f4a6e7a2-fa2c-46a2-b9e8-b0213f8b28ee)
### C
![C](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/ff5d448e-c371-42e5-814a-6da43172a886)
### D
![D](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/4ad0187c-2b3f-457f-b525-342d9ef48db3)
### E
![E](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/e76fe7f0-6599-4dba-a97d-b68473ae69ba)
### F
![F](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/ffde6060-c84b-4296-9608-7d84e7b29db8)
### G
![G](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/608ffd92-b805-4413-bbfc-05c764f9ac29)
### H
![H](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/094e1ad1-5d8e-4743-8f69-1fbf6ea2e3f6)
### I
![I](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/3746dcbc-2f76-4505-9d48-31dd25e77f95)
### J
![J](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/bcb1742b-58ab-4aec-8137-0a044c2b99e6)  
Dari proses penggabungan yang telah dilakukan, didapatkan sebuah subnet besar dengan netmask /13

## Tree
Setelah dilakukannya ``penggabungan IP``, sekarang kita melakukan pembagian IP dengan menggunakan ``tree`` pada masing-masing kelompok yang telah dibuat sebelumnya sebagai berikut
![tree](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/89869d06-19f5-481c-a00f-8eefe8e57c74)

## Pembagian IP
Berikut merupakan hasil dari pembagian IP berdasarkan Tree yang telah dibuat sebelumnya 
![IP](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/93fe2912-b593-442d-bed5-5554cf22a562)

## Setup Network Interface
![setup](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/63a97618-97e4-43e6-82c3-c79e4c123ce4)  
## Routing
### Aura
![aura1](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/9bf511d3-e8ac-4ef9-9fd4-1c6c8dbb43a6)  
![aura2](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/4b9d4e0a-7560-4a26-8cf5-90480631ad7d)  
### Frieren
![frieren](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/96d219cd-3940-4bb2-baa3-7bc05320d8a9)
### Flamme
![flamme](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/e4c1d713-bd0b-4dfd-b637-d61b380be5cd) 
### Fern
![fern](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/9c36e82b-ec03-4bc5-87a1-7f60ca008f4d) 
### Himmel
![himmel](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/df33f2a5-ad3f-4497-bf39-750aeaf622bd)
### Denken
![denken](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/e461571e-3383-4d96-84e6-a33921968c37)
### Eisen
![eisen](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/475ffcaa-7993-48ad-b147-1d905b0403c9)
### Lugner
![lugner](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/8914d84f-4aa0-4a64-b4f9-ff1b312cc4fc)
### Linie
![linie](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/8ee3e173-90d9-47d7-bfa4-d3b607ce5907)
### Lawine
![lawine](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/304a9c53-b26b-4e5f-b553-6ed384bda24a)
### Heiter
![heiter](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/abeaf1f6-e6c3-4fd5-9b8e-8ffdb4b44dbc)

## Testing 


