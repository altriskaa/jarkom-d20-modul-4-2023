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
  - [Subnet dan Prefix IP](#subnet-dan-prefix-ip)
  - [Route](#route)
- [VLSM](#vlsm)
  - [Tree](#tree)
  - [Pembagian IP](#pembagian-ip)
  - [Konfigurasi Network](#konfigurasi-network)
  - [Routing](#routing)
- [CIDR](#cidr)
  - [Penggabungan IP](#penggabungan-ip)
  - [Tree](#tree-1)
  - [Pembagian IP](#pembagian-ip-1)

## Topologi GNS VLSM 
![image](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/114663340/e24a5a76-2746-44d0-882f-e6643f25ed80)

## Subnet dan Prefix IP 
![image](https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/114663340/c54964d8-2778-4645-85fd-c2daa5cbb36a)

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
```
#A21
auto eth0
iface eth0 inet static
address 192.201.17.5
netmask 255.255.255.0
gateway 192.201.17.1
```

- WilleRegion (63 Host)
```
#A21
auto eth0
iface eth0 inet static
address 192.201.17.10
netmask 255.255.255.0
gateway 192.201.17.1
```

- Denken 
```
auto lo
iface lo inet loopback

#A20
auto eth0
iface eth0 inet static
address 192.201.7.246
netmask 255.255.255.252
gateway 192.201.18.245 

#A21
auto eth1
iface eth1 inet static
address 192.201.17.1
netmask 255.255.255.128
```

- Aura 
```
auto eth0
iface eth0 inet static

# A20
auto eth1
iface eth1 inet static
address 192.201.18.245 
netmask 255.255.255.252 

# A12
auto et2
iface eth2 inet static
address 192.201.18.229
netmask 255.255.255.252 

# A11
auto eth3
iface eth3 inet static
address 192.201.18.225 
netmask 255.255.255.252 
```

- Frieren 
```
auto lo
iface lo inet loopback

#A12
auto eth0
iface eth0 inet static
address 192.201.18.230
netmask 255.255.255.252
gateway 192.201.18.229

#A14
auto eth1
iface eth1 inet static
address 192.201.18.233
netmask 255.255.255.252

#A13
auto eth2
iface eth2 inet static
address 192.201.18.129
netmask 255.255.255.224
```

- LakeKorridor (24 Host)
```
#A13
auto eth0
iface eth0 inet static
address 192.201.18.130
netmask 255.255.252.0
gateway 192.201.18.129
```

- Flamme 
```
auto lo
iface lo inet loopback

#A14
auto eth0
iface eth0 inet static
address 192.201.18.234 # dipake route fern sm frieren
netmask 255.255.255.252
gateway 192.201.18.233

#A18
auto eth1
iface eth1 inet static
address 192.201.18.241
netmask 255.255.255.252

#A15
auto eth2
iface eth2 inet static
address 192.201.18.237
netmask 255.255.255.252

#A17
auto eth3
iface eth3 inet static
address 192.201.8.1
netmask 255.255.252.0
```

- Fern
```
auto lo
iface lo inet loopback

#A18
auto eth0
iface eth0 inet static
address 192.201.18.242
netmask 255.255.255.252
gateway 192.201.18.241

#A19
auto eth1
iface eth1 inet static
address 192.201.24.1
netmask 255.255.248.0
```

- LaubHills (397 Host)
```
# LaubHills a19
auto eth0
iface eth0 inet static
address 192.201.24.5
netmask 255.255.248.0
gateway 192.201.24.1
```

- AppetitRegion (625 Host)
```
# AppetitRegion a19
auto eth0
iface eth0 inet static
address 192.201.24.10
netmask 255.255.248.0
gateway 192.201.24.1
```

- RohrRoad (1000 Host)
```
#A17
auto eth0
iface eth0 inet static
address 192.201.9.0
netmask 255.255.252.0
gateway 192.201.8.1
```

- Himmel
``` 
auto lo
iface lo inet loopback

#A15
auto eth0
iface eth0 inet static
address 192.201.18.238
netmask 255.255.255.252
gateway 192.201.18.237

#A16
auto eth1
iface eth1 inet static
address 192.201.18.193
netmask 255.255.255.248
```

- ShcwerMountains (5 Host)
```
auto eth0
iface eth0 inet static
address 192.201.18.195
netmask 255.255.255.248
gateway 192.201.18.193
```

- Eisen 
```
auto lo
iface lo inet loopback

#A11
auto eth0
iface eth0 inet static
address 192.210.18.226
netmask 255.255.255.252
gateway 192.210.18.225

#A5
auto eth1
iface eth1 inet static
address 192.210.18.213
netmask 255.255.255.252

#A7
auto eth2
iface eth2 inet static
address 192.210.18.217
netmask 255.255.255.252

#A10
auto eth3
iface eth3 inet static
address 192.210.18.221
netmask 255.255.255.252

#A6
auto eth4
iface eth4 inet static
address 192.210.18.201
netmask 255.255.255.248
```

- Stark 
```
# stark a10
auto eth0
iface eth0 inet static
address 192.210.18.222
netmask 255.255.255.252
gateway 192.210.18.221
```

- Lugner 
```
auto lo
iface lo inet loopback

#A7
auto eth0
iface eth0 inet static
address 192.210.18.218
netmask 255.255.255.252
gateway 192.210.18.217

#A8
auto eth1
iface eth1 inet static
address 192.210.4.1
netmask 255.255.252.0

#A9
auto eth2
iface eth2 inet static
address 192.210.16.1
netmask 255.255.255.0
```

- TurkRegion (1000 Host)
```
# turk region a8
auto eth0
iface eth0 inet static
address 192.210.4.5
netmask 255.255.252.0
gateway 192.210.4.1
```

- GrobeForest (250 Host)
```
# grobeforest a9
auto eth0
iface eth0 inet static
address 192.210.16.5
netmask 255.255.255.0
gateway 192.210.16.1
```
- Richter 
```
# richter a6
auto eth0
iface eth0 inet static
address 192.210.18.203
netmask 255.255.255.248
gateway 192.210.18.201
```

- Revolte
```
#revolte a6
auto eth0
iface eth0 inet static
address 192.210.18.204
netmask 255.255.255.248
gateway 192.210.18.201
```

- Linie 
```
auto lo
iface lo inet loopback

#A5
auto eth0
iface eth0 inet static
address 192.210.18.214
gateway 192.210.18.213
netmask 255.255.255.252

#A3
auto eth1
iface eth1 inet static
address 192.210.18.209
netmask 255.255.255.252

#A4
auto eth2
iface eth2 inet static
address 192.210.12.1
netmask 255.255.254.0
```

- GranzChannel (254 Host)
```
# granz channel a4
auto eth0
iface eth0 inet static
address 192.210.12.5
netmask 255.255.254.0
gateway 192.210.12.1
```

- Lawine 
```
auto lo
iface lo inet loopback

#a3
auto eth0
iface eth0 inet static
address 192.201.18.210
netmask 255.255.255.252
gateway 192.201.18.209

#a2
auto eth1
iface eth1 inet static
address 192.201.18.1
netmask 255.255.255.192
```

- BredtRegion (29 Host)
```
# bredt region a2
auto eth0
iface eth0 inet static
address 192.201.18.5
netmask 255.255.252.0
gateway 192.201.18.1
```

- Heiter 
```
auto lo
iface lo inet loopback

#a2
auto eth0
iface eth0 inet static
address 192.201.18.2
netmask 255.255.255.192
gateway 192.201.18.1

#a1
auto eth1
iface eth1 inet static
address 192.201.0.1
netmask 255.255.255.0
```

- Sein 
```
# sein a1
auto eth0
iface eth0 inet static
address 192.201.0.3
netmask 255.255.255.0
gateway 192.201.0.1
```

- RiegelCanyon (510 Host)
```
# riegel canyon a1
auto eth0
iface eth0 inet static
address 192.201.0.4
netmask 255.255.255.0
gateway 192.201.0.1
```

### Routing 
<table dir="ltr" border="1" cellspacing="0" cellpadding="0" data-sheets-root="1"><colgroup><col width="100" /><col width="100" /><col width="100" /><col width="162" /><col width="138" /></colgroup>
<tbody>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Routing&quot;}">Routing</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Subnet&quot;}">Subnet</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Network ID&quot;}">Network ID</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Netmask&quot;}">Netmask</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Nexthop/gateway&quot;}">Nexthop/gateway</td>
</tr>
<tr>
<td colspan="1" rowspan="18" data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Aura&quot;}">
<div>Aura</div>
</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A1&quot;}">A1</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.0.0&quot;}">192.201.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.252.0&quot;}">255.255.252.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.226&quot;}">192.201.18.226</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A2&quot;}">A2</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.0&quot;}">192.201.18.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.224&quot;}">255.255.255.224</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.226&quot;}">192.201.18.226</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A3&quot;}">A3</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.208&quot;}">192.201.18.208</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.252&quot;}">255.255.255.252</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.226&quot;}">192.201.18.226</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A4&quot;}">A4</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.12.0&quot;}">192.201.12.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.0&quot;}">255.255.255.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.226&quot;}">192.201.18.226</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A5&quot;}">A5</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.212&quot;}">192.201.18.212</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.252&quot;}">255.255.255.252</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.226&quot;}">192.201.18.226</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A6&quot;}">A6</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.200&quot;}">192.201.18.200</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.252&quot;}">255.255.255.252</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.226&quot;}">192.201.18.226</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A7&quot;}">A7</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.216&quot;}">192.201.18.216</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.252&quot;}">255.255.255.252</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.226&quot;}">192.201.18.226</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A8&quot;}">A8</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.4.0&quot;}">192.201.4.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.252.0&quot;}">255.255.252.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.226&quot;}">192.201.18.226</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A9&quot;}">A9</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.16.0&quot;}">192.201.16.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.0&quot;}">255.255.255.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.226&quot;}">192.201.18.226</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A10&quot;}">A10</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.220&quot;}">192.201.18.220</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.252&quot;}">255.255.255.252</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.226&quot;}">192.201.18.226</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A13&quot;}">A13</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.128&quot;}">192.201.18.128</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.224&quot;}">255.255.255.224</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.230&quot;}">192.201.18.230</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A14&quot;}">A14</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.232&quot;}">192.201.18.232</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.252&quot;}">255.255.255.252</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.230&quot;}">192.201.18.230</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A15&quot;}">A15</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.236&quot;}">192.201.18.236</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.252&quot;}">255.255.255.252</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.230&quot;}">192.201.18.230</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A16&quot;}">A16</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.192&quot;}">192.201.18.192</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.248&quot;}">255.255.255.248</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.230&quot;}">192.201.18.230</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A17&quot;}">A17</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.8.0&quot;}">192.201.8.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.252.0&quot;}">255.255.252.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.230&quot;}">192.201.18.230</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A18&quot;}">A18</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.240&quot;}">192.201.18.240</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.252&quot;}">255.255.255.252</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.230&quot;}">192.201.18.230</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A19&quot;}">A19</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.24.0&quot;}">192.201.24.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.252.0&quot;}">255.255.252.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.230&quot;}">192.201.18.230</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A21&quot;}">A21</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.17.0&quot;}">192.201.17.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.128&quot;}">255.255.255.128</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.246&quot;}">192.201.18.246</td>
</tr>
<tr>
<td colspan="1" rowspan="6" data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Frieren&quot;}">
<div>Frieren</div>
</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;default&quot;}">default</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.229&quot;}">192.201.18.229</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A15&quot;}">A15</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.236&quot;}">192.201.18.236</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.252&quot;}">255.255.255.252</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.234&quot;}">192.201.18.234</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A16&quot;}">A16</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.192&quot;}">192.201.18.192</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.248&quot;}">255.255.255.248</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.234&quot;}">192.201.18.234</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A17&quot;}">A17</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.8.0&quot;}">192.201.8.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.252.0&quot;}">255.255.252.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.234&quot;}">192.201.18.234</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A18&quot;}">A18</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.240&quot;}">192.201.18.240</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.252&quot;}">255.255.255.252</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.234&quot;}">192.201.18.234</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A19&quot;}">A19</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.24.0&quot;}">192.201.24.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.252.0&quot;}">255.255.252.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.234&quot;}">192.201.18.234</td>
</tr>
<tr>
<td colspan="1" rowspan="3" data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Flamme&quot;}">
<div>Flamme</div>
</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;default&quot;}">default</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.233&quot;}">192.201.18.233</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A16&quot;}">A16</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.192&quot;}">192.201.18.192</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.248&quot;}">255.255.255.248</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.238&quot;}">192.201.18.238</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A19&quot;}">A19</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.24.0&quot;}">192.201.24.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.252.0&quot;}">255.255.252.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.242&quot;}">192.201.18.242</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Fern&quot;}">Fern</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;default&quot;}">default</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.241&quot;}">192.201.18.241</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Himmel&quot;}">Himmel</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;default&quot;}">default</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.237&quot;}">192.201.18.237</td>
</tr>
<tr>
<td colspan="1" rowspan="7" data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Eisen&quot;}">
<div>Eisen</div>
</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;default&quot;}">default</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.225&quot;}">192.201.18.225</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A1&quot;}">A1</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.0.0&quot;}">192.201.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.252.0&quot;}">255.255.252.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.214&quot;}">192.201.18.214</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A2&quot;}">A2</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.0&quot;}">192.201.18.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.224&quot;}">255.255.255.224</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.214&quot;}">192.201.18.214</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A3&quot;}">A3</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.208&quot;}">192.201.18.208</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.252&quot;}">255.255.255.252</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.214&quot;}">192.201.18.214</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A4&quot;}">A4</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.12.0&quot;}">192.201.12.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.0&quot;}">255.255.255.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.214&quot;}">192.201.18.214</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A8&quot;}">A8</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.4.0&quot;}">192.201.4.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.252.0&quot;}">255.255.252.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.218&quot;}">192.201.18.218</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A9&quot;}">A9</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.16.0&quot;}">192.201.16.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.0&quot;}">255.255.255.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.218&quot;}">192.201.18.218</td>
</tr>
<tr>
<td colspan="1" rowspan="3" data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Linie&quot;}">
<div>Linie</div>
</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;default&quot;}">default</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.213&quot;}">192.201.18.213</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A1&quot;}">A1</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.0.0&quot;}">192.201.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.252.0&quot;}">255.255.252.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.210&quot;}">192.201.18.210</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A2&quot;}">A2</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.0&quot;}">192.201.18.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.255.224&quot;}">255.255.255.224</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.210&quot;}">192.201.18.210</td>
</tr>
<tr>
<td colspan="1" rowspan="2" data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Lawine&quot;}">
<div>Lawine</div>
</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;default&quot;}">default</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.209&quot;}">192.201.18.209</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;A1&quot;}">A1</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.0.0&quot;}">192.201.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;255.255.252.0&quot;}">255.255.252.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.2&quot;}">192.201.18.2</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Heiter&quot;}">Heiter</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;default&quot;}">default</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.1&quot;}">192.201.18.1</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Lugner&quot;}">Lugner</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;default&quot;}">default</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.217&quot;}">192.201.18.217</td>
</tr>
<tr>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Denken&quot;}">Denken</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;default&quot;}">default</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;0.0.0.0&quot;}">0.0.0.0</td>
<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;192.201.18.245&quot;}">192.201.18.245</td>
</tr>
</tbody>
</table>

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
https://github.com/altriskaa/jarkom-d20-modul-44-2023/assets/56571284/ba57810a-f2fb-4db5-8bcf-c3f855438cb2

