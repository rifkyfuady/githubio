---
title: "Panduan Lengkap Membangun Sms Gateway dengan Gammu"
slug: gammu-sms-gateway
date: 2019-03-14T22:47:52+07:00
draft: false

type: post

tags:
    - tag

image: ""
description: ""
---


**Apa itu SMS-Gateway?**

Secara sederhana `SMS-Gateway` adalah suatu layanan `SMS` *(Short Message Service)* yang memungkinkan untuk melakukan pengiriman `SMS`, maupun penerimaan `SMS` melalui komputer. Kita bisa dengan mudah melakukan menejemen `SMS` dengan komputer kita. 

Pada kesempatan kali ini saya akan berbagi cara membangun `SMS-Gateway` dengan [Gammu](https://wammu.eu/gammu/). Spesifikasi sistem operasi komputer saya menggunakan [Ubuntu 18.04 LTS](http://releases.ubuntu.com/18.04/) dan modem `Wavecom Fastrack M1306B`.

Berikut langkah-langkah instalasinya :

- Install `gammu` dan juga `gammu-smsd` menggunakan terminal, pastikan terhubung dengan internet. Masukkan perintah di `terminal` :

```bash
sudo apt-get update
sudo apt-get install gammu gammu-smsd
```
<img data-src="/img/gammu-sms-gateway/1.png" class="lazyload" />


- Kemudian setting `gammu`-nya. Masukkan perintah :

```bash
gammu-config
```
<img data-src="/img/gammu-sms-gateway/2.png" class="lazyload" />

Akan tampil menu untuk konfigurasi `gammu`. Kita akan mengubah ini dengan kongurasi yang `benar` sesuai `modem` yang digunakan.


- Buka tab baru di terminal, lalu masukkan perintah :

```bash
dmesg | grep tty
```
<img data-src="/img/gammu-sms-gateway/3.png" class="lazyload" />

Nanti akan muncul `port` yang terhubung dengan modem. Jika tidak muncul, mungkin modem `belum ditancapkan` atau anda perlu `menginstall driver` modem tersebut. Langkah ini bertujuan untuk melihat apakah modem `sudah` `terdeteksi` pada komputer atau `belum`.

- Jika kita sudah mengetahui `port` yang terhubung dengan `modem`, isikan pada konfigurasi `gammu`. Yaitu pada bagian :

```bash
port = /dev/ttyUSB0
```
<img data-src="/img/gammu-sms-gateway/4.png" class="lazyload" />

`ttyUSB0` disesuaikan dengan hasil `dmesg | grep tty`. 

- Untuk `connection` saya pilih `at115200` karena saya menggunakan `modem` `Wavecom Fastrack M1306B`, jika anda menggunakan `modem` yang `berbeda`, sesuaikan konfigurasi `connection` dengan `jenis modem` anda.

```bash
connection = at115200
```
<img data-src="/img/gammu-sms-gateway/5.png" class="lazyload" />

- `Logfile` kita isi dengan `path` di mana kita ingin menyimpan `log` *(informasi)* dari `gammu`. Saya taruh di `/var/log/gammulog`

```bash
logfile = /var/log/gammulog
```
<img data-src="/img/gammu-sms-gateway/6.png" class="lazyload" />


- Untuk `logformat` saya pilih `textdate`. Nantinya, `log` `gammu` akan menyimpan informasi `teks` beserta `tanggal` dan `jam` kejadianya.

```bash
logformat = textdate
```
<img data-src="/img/gammu-sms-gateway/7.png" class="lazyload" />


- Setelah itu `save`, dan konfigurasi `gammu` tersebut akan tersimpan di file `.gammurc` pada direktori home user yang kita gunakan.

<img data-src="/img/gammu-sms-gateway/8.png" class="lazyload" />

<img data-src="/img/gammu-sms-gateway/9.png" class="lazyload" />


- Kita matikan dulu `service` `gammu-smsd`. Kenapa? Karena jika `service` tersebut berjalan, kita tidak bisa menggunakan perintah `gammu` di `terminal`. Masukkan perintah :

```bash
sudo /etc/init.d/gammu-smsd stop
```

- Kita cek apakah settingan `gammu` dengan `modem` tersebut sudah `benar` atau belum. Masukkan perintah :

```bash
sudo gammu --identify
```

- Jika sudah muncul `informasi` dari `modem` yang menancap pada komputer kita, berarti settingan `benar`. Kita periksa dengan cara mencoba mengirim `SMS` menggunakan perintah `sudo gammu sendsms TEXT no_tujuan -text "isi sms"`. Contohnya:

```bash
sudo gammu sendsms TEXT +6285326967372 -text "ini pesan gammu"
```
<img data-src="/img/gammu-sms-gateway/10.png" class="lazyload" />

Jika `berhasil` mengirim `SMS`, berarti semua settingan `berhasil`. Tapi bila kita `gagal` mengirim `SMS`, coba `periksa` settingan `port` pada konfigurasi `gammu`. Atau ulangi cara di atas dari `dmesg | grep tty` dan jangan lupa ganti `port`-nya. Jika semua `port` yang ada sudah kita coba tetapi masih `gagal`, coba ganti `connection`-nya.


- Kemudian kita setting `gammu-smsd`-nya agar `service` `gammu` bisa terhubung dengan `database`. Edit file `/etc/gammu-smsdrc` dengan perintah :

```bash
sudo gedit /etc/gammu-smsdrc
```
<img data-src="/img/gammu-sms-gateway/11.png" class="lazyload" />

- Sesuaikan `konfigurasi` seperti ini :

```bash
# Configuration file for Gammu SMS Daemon

# Gammu library configuration, see gammurc(5)
[gammu]
port = /dev/ttyUSB0
connection = at115200
logformat = textdate
logfile = /var/log/gammulog

# SMSD configuration, see gammu-smsdrc(5)
[smsd]
service = SQL
driver = native_mysql
logfile = /var/log/smsdlog
commtimeout = 30
sendtimeout = 30
checksecurity = 0
checksignal = 1

#Database sesuaikan sendiri
pc = localhost
user = root
password = rahasia
database = terserah
```

<img data-src="/img/gammu-sms-gateway/12.png" class="lazyload" />


- `Simpan` dan jangan lupa untuk `menjalankan` kembali `service` `gammu` dengan perintah :

```bash
sudo /etc/init.d/gammu-smsd start
```