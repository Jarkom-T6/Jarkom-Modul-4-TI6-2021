# Jarkom-Modul-4-TI6-2021

## Anggota Kelompok TI6:

- Syakhisk Al-Azmi 05311940000003
- Muhammad Rizqi Wijaya 05311940000014
- Shafira Firdausi 05311940000040

# CIDR pada CPT

## Perhitungan Subnetting

Berikut untuk hasil perhitungan lingkaran CIDR

![Subnetting CIDR untuk A](Jarkom-Modul-4-TI6-2021%20b4b0068305f1446e9f1988e0ab40b029/A.jpg)

Subnetting CIDR untuk A

![Subnetting CIDR untuk B](Jarkom-Modul-4-TI6-2021%20b4b0068305f1446e9f1988e0ab40b029/B.jpg)

Subnetting CIDR untuk B

![Subnetting CIDR untuk  C](Jarkom-Modul-4-TI6-2021%20b4b0068305f1446e9f1988e0ab40b029/C.jpg)

Subnetting CIDR untuk  C

![Subnetting CIDR untuk D dan E](Jarkom-Modul-4-TI6-2021%20b4b0068305f1446e9f1988e0ab40b029/D_E.jpg)

Subnetting CIDR untuk D dan E

## Pohon Pembagian

![Pembagian Tree CIDR](Jarkom-Modul-4-TI6-2021%20b4b0068305f1446e9f1988e0ab40b029/Tree_CIDR.jpg)

Pembagian Tree CIDR

## Pembagian NID dan Netmask

[Untitled](https://www.notion.so/e095557b3b6c494696a42dad9efc5091)

## Pembagian IP

dari NID yang sudah didapatkan, berikut pembagian IP masing-masing node:

### Router

![IP Router CIDR](Jarkom-Modul-4-TI6-2021%20b4b0068305f1446e9f1988e0ab40b029/Untitled.png)

IP Router CIDR

### Client

![IP Client CIDR](Jarkom-Modul-4-TI6-2021%20b4b0068305f1446e9f1988e0ab40b029/Untitled%201.png)

IP Client CIDR

## Routing

- Foosha
    
    ```bash
    192.214.16.0/22 via 192.214.20.2
    192.214.24.0/23 via 192.214.20.2
    192.214.26.0/28 via 192.214.20.2
    192.214.8.4/30 via 192.214.20.2
    192.214.4.0/24 via 192.214.20.2
    192.214.0.0/22 via 192.214.20.2
    192.214.48.0/22 via 192.214.68.2
    192.214.32.0/21 via 192.214.68.2
    192.214.40.0/25 via 192.214.68.2
    192.214.8.0/30 via 192.214.20.2
    192.214.52.0/30 via 192.214.68.2
    ```
    
- Guanhao
    
    ```bash
    0.0.0.0/0 via 192.214.20.1
    192.214.26.0/28 via 192.214.24.2
    192.214.8.4/30 via 192.214.8.2
    192.214.4.0/24 via 192.214.8.2
    192.214.0.0/22 via 192.214.8.2
    ```
    
- Alabasta
    
    ```bash
    0.0.0.0/0 via 192.214.24.1
    ```
    
- Oimo
    
    ```bash
    0.0.0.0/0 via 192.214.8.1
    192.214.0.0/22 via 192.214.4.2
    ```
    
- Seastone
    
    ```bash
    0.0.0.0/0 via 192.214.4.1
    ```
    
- Water7
    
    ```bash
    0.0.0.0/0 via 192.214.68.1
    192.214.32.0/21 via 192.214.52.2
    192.214.40.0/25 via 192.214.52.2
    ```
    
- Pucci
    
    ```bash
    0.0.0.0/0 via 192.214.52.1
    ```

# VLSM pada GNS3

## Perhitungan Subnetting

![Subnetting VLSM](Jarkom-Modul-4-TI6-2021%20b4b0068305f1446e9f1988e0ab40b029/A%201.jpg)

Subnetting VLSM

## Pohon Pembagian

![Pembagian Tree untuk VLSM](Jarkom-Modul-4-TI6-2021%20b4b0068305f1446e9f1988e0ab40b029/Tree_VLSM.jpg)

Pembagian Tree untuk VLSM

## Labelling Netmask

[Untitled](https://www.notion.so/28ccd7231b4e4800b885670a1e51562b)

## Pembagian NID dan Netmask

[Untitled](https://www.notion.so/80dceae85377417c91ccece7d2666ef0)

## Pembagian IP

Dari pembagian NID dan Netmask diatas, ditentukanlah IP masing-masing node sebagai berikut

### Router

![IP Router VLSM](Jarkom-Modul-4-TI6-2021%20b4b0068305f1446e9f1988e0ab40b029/Untitled%202.png)

IP Router VLSM

### Client

![IP Client VLSM](Jarkom-Modul-4-TI6-2021%20b4b0068305f1446e9f1988e0ab40b029/Untitled%203.png)

IP Client VLSM

## Routing

Berikut routing yang diperlukan dari tiap node yang ada

```bash
##Foosha
route add -net 192.214.16.0 netmask 255.255.252.0 gw 192.214.27.150 # A14 - A12 (Cipher)
route add -net 192.214.27.0 netmask 255.255.255.128 gw 192.214.27.150
route add -net 192.214.0.0 netmask 255.255.248.0 gw 192.214.27.150
route add -net 192.214.20.0 netmask 255.255.252.0 gw 192.214.27.166 #guanho eth0
route add -net 192.214.24.0 netmask 255.255.254.0 gw 192.214.27.166 #guanho eth0
route add -net 192.214.27.128 netmask 255.255.255.240 gw 192.214.27.166 #guanho eth0
route add -net 192.214.26.0 netmask 255.255.255.0 gw 192.214.27.166 #guanho eth0
route add -net 192.214.12.0 netmask 255.255.252.0 gw 192.214.27.166 #guanho eth0
route add -net 192.214.27.160 netmask 255.255.255.252 gw 192.214.27.166 #guanho eth0
route add -net 192.214.27.144 netmask 255.255.255.252 gw 192.214.27.150
route add -net 192.214.27.156 netmask 255.255.255.252 gw 192.214.27.166 #guanho eth0
route add -net 192.214.26.0 netmask 255.255.255.0 gw 192.214.27.166 #guanho eth0

##Water7
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.214.27.149
route add -net 192.214.27.0 netmask 255.255.255.128 gw 192.214.27.146
route add -net 192.214.0.0 netmask 255.255.248.0 gw 192.214.27.146
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.214.27.149

##Guanhao
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.214.27.165 #foosha eth3
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.214.27.165 #foosha eth3 (sama)
route add -net 192.214.27.128 netmask 255.255.255.240 gw 192.214.24.3 # alabasta eth0
route add -net 192.214.26.0 netmask 255.255.255.0 gw 192.214.27.158 #oimo eth0
route add -net 192.214.12.0 netmask 255.255.252.0 gw 192.214.27.158 #oimo eth0
route add -net 192.214.27.160 netmask 255.255.255.252 gw 192.214.27.158 #oimo eth0
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.214.27.165 #foosha eth3
route add -net 192.214.26.0 netmask 255.255.255.0 gw 192.214.27.158 #oimo eth0

##Oimo
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.214.27.157 #guanho eth3
route add -net 192.214.12.0 netmask 255.255.252.0 gw 192.214.26.3 #seastone eth0
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.214.27.157 #guanho eth3
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.214.27.157 #guanho eth3

##Pucci
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.214.27.145

##Alabasta
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.214.24.1 #guanho eth2

##Seastone
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.214.26.1 #oimo eth2
```

## Config

### Router

- Foosha
    
    ```bash
    auto eth0
    iface eth0 inet dhcp
    
    auto eth1
    iface eth1 inet static
    	address 192.214.8.1
    	netmask 255.255.252.0
            up iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.214.0.0/19
    
    auto eth2
    iface eth2 inet static
    	address 192.214.27.153
    	netmask 255.255.255.252
           # up iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.214.0.0/19
    
    auto eth3
    iface eth3 inet static
    	address 192.214.27.165
    	netmask 255.255.255.252
           # up iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.214.0.0/19
    
    auto eth4
    iface eth4 inet static
    	address 192.214.27.149
    	netmask 255.255.255.252
           up iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.214.0.0/19
    ```
    
- Guanhao
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.27.166
    	netmask 255.255.255.252
            gateway 192.214.27.165
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    
    auto eth1
    iface eth1 inet static
    	address 192.214.20.1
    	netmask 255.255.252.0
        
    auto eth2
    iface eth2 inet static
    	address 192.214.24.1
    	netmask 255.255.254.0
        
    auto eth3
    iface eth3 inet static
    	address 192.214.27.157
    	netmask 255.255.255.252
    ```
    
- Alabasta
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.24.3
    	netmask 255.255.254.0
    	gateway 192.214.24.1
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    
    auto eth1
    iface eth1 inet static
    	address 192.214.27.129
    	netmask 255.255.255.240
    ```
    
- Oimo
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.27.158
    	netmask 255.255.255.252
    	gateway 192.214.27.157
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    
    auto eth1
    iface eth1 inet static
    	address 192.214.27.161
    	netmask 255.255.255.252
    
    auto eth2
    iface eth2 inet static
    	address 192.214.26.1
    	netmask 255.255.255.0
    ```
    
- Seastone
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.26.3
    	netmask 255.255.255.0
    	gateway 192.214.26.1
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    
    auto eth1
    iface eth1 inet static
    	address 192.214.12.1
    	netmask 255.255.252.0
    ```
    
- Water7
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.27.150
    	netmask 255.255.255.252
            gateway 192.214.27.149
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
      
    auto eth1
    iface eth1 inet static
    	address 192.214.16.1
    	netmask 255.255.252.0
    
    auto eth2
    iface eth2 inet static
    	address 192.214.27.145
    	netmask 255.255.255.252
    ```
    
- Pucci
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.27.146
    	netmask 255.255.255.252
            gateway 192.214.27.145
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    
    auto eth1
    iface eth1 inet static
    	address 192.214.27.1
    	netmask 255.255.255.128
    
    auto eth2
    iface eth2 inet static
    	address 192.214.0.1
    	netmask 255.255.248.0
    ```
    

### Client

- Doriki (Server)
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.27.154
    	netmask 255.255.255.252
            gateway 192.214.27.153
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    ```
    
- Jabra
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.20.2
    	netmask 255.255.252.0
    	gateway 192.214.20.1
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    ```
    
- Maingate
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.24.2
    	netmask 255.255.254.0
    	gateway 192.214.24.1
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    ```
    
- Jorge
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.27.130
    	netmask 255.255.255.240
    	gateway 192.214.27.129
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    ```
    
- EniesLobby
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.26.2
    	netmask 255.255.255.0
    	gateway 192.214.26.1
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    ```
    
- Fukurou (Server)
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.27.162
    	netmask 255.255.255.252
    	gateway 192.214.27.161
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    ```
    
- Elena
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.12.2
    	netmask 255.255.252.0
    	gateway 192.214.12.1
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    ```
    
- Blueno
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.8.2
    	netmask 255.255.252.0
            gateway 192.214.8.1
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    ```
    
- Cipher
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.16.2
    	netmask 255.255.252.0
    	gateway 192.214.16.1
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    ```
    
- Calmbelt
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.0.2
    	netmask 255.255.248.0
            gateway 192.214.0.1
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    ```
    
- Courtyard
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.4.237
    	netmask 255.255.248.0
            gateway 192.214.0.1
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    ```
    
- Jipangu
    
    ```bash
    auto eth0
    iface eth0 inet static
    	address 192.214.27.2
    	netmask 255.255.255.128
            gateway 192.214.27.1
            up echo "nameserver 192.168.122.1" > /etc/resolv.conf
    ```
    

# Kendala

1. Pada GNS3 (VLSM), Elena sempat kesulitan untuk terkoneksi. Namun setelah dilaukan traceroute dari Foosha ke Elena, ternyata masalahnya terdapat pada Oimo yang mengembalikan koneksi dari Foosha ke Guanhao.
2. Pada CPT (CIDR), Oimo - Courtyard dan Oimo - Pucci tidak bisa melakukan ping. Dapat diselesaikan dengan menambahkan konfigurasi routing dari Foosha ke subnet-subnet tersebut
