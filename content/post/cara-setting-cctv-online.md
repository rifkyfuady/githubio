---
title: 'Cara Setting CCTV Online'
date: 2012-03-12T23:49:00.000+07:00
draft: false
aliases: [ "/2012/03/cara-setting-cctv-online.html" ]
tags : [Tips dan Trik]
---

  

Di postingan ini saya akan berbagi ilmu cara setting **CCTV online**. Disini saya menggunakan Kamera dan DVR merk **Avtech**, serta modem Adsl Speedy (**TP-Link**). berikut ini cara setting agar CCTV bisa Online :

  

1\. Kita buka [www.dyndns.com](http://www.dyndns.com/)

[![](http://4.bp.blogspot.com/-6RifAuwzyq0/T14gpZCUUHI/AAAAAAAAAJM/OTWG7gSlmXo/s320/logindyn.jpg)](http://4.bp.blogspot.com/-6RifAuwzyq0/T14gpZCUUHI/AAAAAAAAAJM/OTWG7gSlmXo/s1600/logindyn.jpg)

  

   Login, bila belum punya akun, buat akun anda dulu. disini kita akan mendaftarkan DNS yg akan dipakai buat CCTV.

  

2\. Klik ke **My servise - Host Servise - Add Hostname**.

   Buat Hostname anda, lihat gambar :

[![](http://4.bp.blogspot.com/-z24HxTNYrgY/T14g6HxrEFI/AAAAAAAAAJU/oN7KDeEzqJc/s320/DNSadd.jpg)](http://4.bp.blogspot.com/-z24HxTNYrgY/T14g6HxrEFI/AAAAAAAAAJU/oN7KDeEzqJc/s1600/DNSadd.jpg)

  

3\. Untuk mengeceknya sudah aktif apa belum, kita lakukan ping test ke hostname tersebut.

[![](http://2.bp.blogspot.com/-6_rBKJJ5m18/T14hLzV8h6I/AAAAAAAAAJc/EBxfdh1az-w/s320/ping.jpg)](http://2.bp.blogspot.com/-6_rBKJJ5m18/T14hLzV8h6I/AAAAAAAAAJc/EBxfdh1az-w/s1600/ping.jpg)

  

   **Start - RUN.**

   ping home-rifky.dvrdns.org -t

   jika "**reply**from 144.79.61.122", berarti berhasil.

  

4\. Kalau sudah, kemudian kita Setting modem **Tp-Link** nya,

[![](http://4.bp.blogspot.com/-vNkCv5Wvi30/T14hdtGrdII/AAAAAAAAAJk/h28Ni45VM_Y/s320/loginmodem.jpg)](http://4.bp.blogspot.com/-vNkCv5Wvi30/T14hdtGrdII/AAAAAAAAAJk/h28Ni45VM_Y/s1600/loginmodem.jpg)

  

   Masuk ke settingan modem lewat browser dulu (defaultnya tulis di browser **192.168.1.1**, user sama passwordnya : admin).

  

5\. Masuk ke tab menu **Advanced Setup - NAT**

[![](http://2.bp.blogspot.com/-MgmFXQLWmPg/T14h-Xs3pGI/AAAAAAAAAJ0/HBE95vUlHsw/s320/Nat.jpg)](http://2.bp.blogspot.com/-MgmFXQLWmPg/T14h-Xs3pGI/AAAAAAAAAJ0/HBE95vUlHsw/s1600/Nat.jpg)

  

                Virtual Ciecuit : **PVC1**

  

6\. Setelah itu klik **DMZ**,

[![](http://2.bp.blogspot.com/-Azt3lnwgpVA/T14iNDkwaQI/AAAAAAAAAJ8/_JboRCmC25M/s320/DMZ.jpg)](http://2.bp.blogspot.com/-Azt3lnwgpVA/T14iNDkwaQI/AAAAAAAAAJ8/_JboRCmC25M/s1600/DMZ.jpg)

  

                DMZ : **Enable**

                DMZ Host IP Address : **192.168.1.10** (karena ini adalah IP default dari DVR Avtech)

  

7\. Kemudian masuk ke tab menu **Access Management - DDNS**,

[![](http://4.bp.blogspot.com/-7Yk57htsmRw/T14iamoHBaI/AAAAAAAAAKE/yVngCT1N3GY/s320/DDNS.jpg)](http://4.bp.blogspot.com/-7Yk57htsmRw/T14iamoHBaI/AAAAAAAAAKE/yVngCT1N3GY/s1600/DDNS.jpg)

  

                Dynamic DNS : **Actived**

                My Host name : home-rifky.dvrdns.org (nama DNS yang tadi didaftarkan di Dyndns)

                Wildcard support : **No**

  

8\. Jika sudah, kita hubungkan DVR ke Modem dengan **kabel LAN**(UTP).

[![](http://3.bp.blogspot.com/-P5aqzLPHGzM/T14k0tNNAlI/AAAAAAAAAKM/rdNo3sKmbf4/s320/cat512.jpg)](http://3.bp.blogspot.com/-P5aqzLPHGzM/T14k0tNNAlI/AAAAAAAAAKM/rdNo3sKmbf4/s1600/cat512.jpg)

  

  

9\. Untuk setting di DVRnya, Install Video Viewer.exe, biasanya ada di CD DVR nya. kalau belum punya, bisa donwload [disini](http://www.ziddu.com/download/18851966/Avtech.rar.html).

  

10\. Jalankan Video Viewer.exe, **Add **(tanda +). Settingan lihat digambar :

[![](http://3.bp.blogspot.com/-Z1LvBMNa6uc/T14lIRiUBfI/AAAAAAAAAKU/O_iTscg1c-s/s320/runAvexe.jpg)](http://3.bp.blogspot.com/-Z1LvBMNa6uc/T14lIRiUBfI/AAAAAAAAAKU/O_iTscg1c-s/s1600/runAvexe.jpg)

  

[![](http://4.bp.blogspot.com/-mu0sjfb4mNE/T14lXuCstBI/AAAAAAAAAKc/UzDNjQlg9RA/s320/addIPlocal.jpg)](http://4.bp.blogspot.com/-mu0sjfb4mNE/T14lXuCstBI/AAAAAAAAAKc/UzDNjQlg9RA/s1600/addIPlocal.jpg)

  

  

11\. Double klik IP settingan tadi untuk login.

[![](http://3.bp.blogspot.com/--NEvCN2auAI/T14lhHdVbpI/AAAAAAAAAKk/Ha-kfpnwIMg/s320/loginAvtect.jpg)](http://3.bp.blogspot.com/--NEvCN2auAI/T14lhHdVbpI/AAAAAAAAAKk/Ha-kfpnwIMg/s1600/loginAvtect.jpg)

  

  

12\. Kemudian masuk ke menu **Miscellaneous Control - Server seetting**.

[![](http://4.bp.blogspot.com/-0p8Ny3bvt48/T14lqlSEIkI/AAAAAAAAAKs/1kP3s1zwQa0/s320/milleciound.jpg)](http://4.bp.blogspot.com/-0p8Ny3bvt48/T14lqlSEIkI/AAAAAAAAAKs/1kP3s1zwQa0/s1600/milleciound.jpg)

  

  

13\. Klik **Network**. Setting sperti gambar dibawah.

[![](http://4.bp.blogspot.com/-G8Kz7m5enyE/T14lzaeJliI/AAAAAAAAAK0/2AVQjGUuDns/s320/network.jpg)](http://4.bp.blogspot.com/-G8Kz7m5enyE/T14lzaeJliI/AAAAAAAAAK0/2AVQjGUuDns/s1600/network.jpg)

  

                Web Port : 81, karena biar bisa diakses lewat Handphone.

  

14\. Masuk ke **DDNS**. Setting seperti gambar dibawah.

[![](http://4.bp.blogspot.com/-ECFTzf5YqUw/T14l-2Noi7I/AAAAAAAAAK8/_oXklPZmoTQ/s320/ddnsvv.jpg)](http://4.bp.blogspot.com/-ECFTzf5YqUw/T14l-2Noi7I/AAAAAAAAAK8/_oXklPZmoTQ/s1600/ddnsvv.jpg)

  

                DNS 1 dan DNS 2 adalah IP dari www.dyndns.com (lakukan ping test kalau tidak percaya)

  

15\. Klik **Apply - OK**.

  

16\. seperti langkah no. 10, coba IP Addres di ganti : “home-rifky.dvrdns.org” dan Login. berhasil berarti selesai.

[![](http://1.bp.blogspot.com/-vh6KeNwGBcg/T14oI7oEOSI/AAAAAAAAALM/Z1a37AWJgbw/s320/videoviewer_0130_full_screen_dashboard.jpg)](http://1.bp.blogspot.com/-vh6KeNwGBcg/T14oI7oEOSI/AAAAAAAAALM/Z1a37AWJgbw/s1600/videoviewer_0130_full_screen_dashboard.jpg)

  

  

  

Sekian dulu tutorial dari saya, semoga bermanfaat untuk anda.

  

Catatan : sekarang akun Dyndns sudah tidak free lagi, kalau ingin yang free bisa memakai akun [no-ip](http://www.no-ip.com/), tapi harus memakai modem yang support [no-ip](http://www.no-ip.com/), contoh : Modem **D-Link.**