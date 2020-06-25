---
title: "Antrian Sms Gateway"
slug: antrian-sms-gateway
date: 2019-03-14T22:48:26+07:00
draft: true

type: post

tags:
    - tag

image: ""
description: ""
---


- `Ekstrak` file `antrian-sms-gateway.zip`. Isi file ada `3`, direktori `simpusbatang`, file `simpus-sms.zip` dan file `smsonline.sql`.
- `Import` file `smsonline.sql` ke database puskesmas.
- `Install` `gammu`, lihat [disini](/blog/gammu-sms-gateway/).
- `Ekstrak` file `simpus-sms.zip`, `copy` hasil ekstrak ke dalam `direktori` :
 - Jika `server baru` copy ke direktori `/var/www/html/`.
 - Jika `server lama` copy ke direktori `htdoc` dari `lampp`.
- Sesuaikan konfigurasi `koneksi` `database` aplikasi `simpus-sms` di file `config/koneksi.php`, *`(gunakan database puskesmas, bukan sayangbunda)`*, kemudian coba jalankan aplikasi `simpus-sms` dengan `mengakses` atau membuka `url` aplikasinya *`(http://localhost/simpus-sms/)`* di browser.
- Untuk aplikasi `simpusbatang`, `copy` file `sesuai tempat`. Sebagai `informasi`, ada `direktori baru` `sms-online` yang berisi `bot` dari sistem pendaftaran `sms-gateway` jangan lupa dicopy taruh di dalam direktori `simpusbatang`.
- Untuk file `reg1.php` `edit` baris `262` sesuaikan dengan data di `tabel klinik`, ambil kolom `id` yang merupakan `kunjungan sehat` tiap puskesmas. Contoh : `Limpung` kunjungan sehat ada di `klinik imunisasi`, maka ambil id `klinik imunisasi` di `tabel klinik`.
- Untuk file `bpjs/pendaftaran/index.php` `edit` : 
 - Baris `11` sesuaikan dengan `tabel klinik` data `kunjungan sakit` tiap puskesmas, isi `value` dengan kolom `pcare`, isi `data-id` dengan kolom `id`.
 - Baris `14` sesuaikan dengan `tabel klinik` data `kunjungan sehat` tiap puskesmas, isi `value` dengan kolom `pcare`, isi `data-id` dengan kolom `id`.
 - Sesuaikan data di `tabel klinik` kolom `sehat`, jika `0` berarti `kunjungan sehat`, jika `1` berarti `kunjungan sakit`.
- Tambahkan `cronjob` dengan mengedit file `/etc/crontab` dengan cara menjalankan perintah di `terminal` :

```bash
sudo gedit /etc/crontab
``` 
- Kemudian tambahkan dibawah ini dibaris terakhir : *`(ada keterangan untuk server baru / lama)`* 

```bash
# untuk server baru
* *	* * *	root    wget -q --spider http://localhost:88/sms-online/
``` 
```bash
# untuk server lama
* *	* * *	root    wget -q --spider http://localhost/simpusbatang/sms-online/
``` 
- Restart `cronjob` dengan perintah : 

```bash
# untuk server baru
sudo systemctl restart cron 
``` 

```bash
# untuk server lama
sudo service cron restart 
``` 