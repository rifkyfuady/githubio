---
title: "Portofolio"
slug: portofolio
date: 2019-03-12T17:34:44+07:00
draft: false
meta:
    image: ""
    description: ""
---


Halaman ini berisi project yang pernah saya kerjakan dan yang sedang dikerjakan.
Ada yang bersifat _side project_ dan ada juga yang serius. Untuk project *private*,
saya tidak cantumkan di sini. Untuk project yang lainnya bisa ditemukan di [Github](https://github.com/rifkyfu32).


## Aplikasi mobile Dinkes Batang

- URL: [Google Play](https://play.google.com/store/apps/details?id=io.github.rifkyfu32.dinkes)
- Status: <span class="badge badge-success">production</span>

Portal aplikasi mobile resmi `Dinas Kesehatan Kabupaten Batang` yang memberikan informasi kepada masyarakat yang ingin mendapat berita, kegiatan maupun artikel di lingkungan instansi `Dinas Kesehatan Kabupaten Batang`.

![gambar](/images/porto/dinkes-apk-1.png)

Dibangun menggunakan framework mobile [Flutter](https://flutter.dev/) dan sumber data yang digunakan dalam aplikasi ini berasal dari Web Service API `Dinas Kesehatan Kabupaten Batang`.

Pada tanggal 24 Maret 2019 sudah masuk di [Showcase Flutter](https://itsallwidgets.com/flutter-app/dinkes-batang)

![gambar](/images/porto/dinkes-apk-2.png)


## Dinkes Batang

- URL: [dinkes.batangkab.go.id](https://dinkes.batangkab.go.id/)
- Status: <span class="badge badge-success">production</span>

Web resmi `Dinas Kesehatan Kabupaten Batang` menyediakan informasi 
untuk masyarakat yang ingin mengetahui berita maupun informasi di lingkungan 
instansi `Dinas Kesehatan Kabupaten Batang`.

![gambar](/images/porto/dinkes.png)

Dibangun mengunakan CMS [Wordpress](https://wordpress.org) dengan menggunakan tema dan visual page builder [Divi](https://www.elegantthemes.com).



## PPID Dinkes Batang

- URL: [dinkes.batangkab.go.id/e-ppid](https://dinkes.batangkab.go.id/e-ppid)
- Status: <span class="badge badge-success">production</span>

PPID Dinkes Batang adalah sistem informasi yang bertujuan untuk merencanakan,
mengorganisasikan dan melaksanakan kegiatan pengelolaan dan pelayanan informasi menuju pelayanan informasi yang cepat, 
mudah dan wajar di lingkungan `Dinas Kesehatan Kabupaten Batang`.

![gambar](/images/porto/ppid-web.png)

Halaman depan PPID Dinkes, pemohon(masyarakat) bisa melakukan pendaftaran sebelum mengajukan permohonan informasi yang diinginkan.

![gambar](/images/porto/ppid-backend.png)

Halaman administator PPID Dinkes, untuk pejabat pengelola informasi dan dokumentasi Dinas Kesehatan Batang yang menyediakan data informasi.

Dibangun mengunakan framework PHP [CodeIgniter](https://codeigniter.com), sedangkan untuk mempercantik tampilan menggunakan framework CSS yang sudah sangat mainstream, yaitu [Bootstrap](https://getbootstrap.com).



## Aplikasi KTP, BPJS & DPT

- URL: [dinkes.batangkab.go.id/ktp](https://dinkes.batangkab.go.id/ktp)
- Status: <span class="badge badge-success">production</span>

![gambar](/images/porto/ktp-1.png)

![gambar](/images/porto/ktp-2.png)

![gambar](/images/porto/ktp-3.png)

1.`Cek KTP` Adalah aplikasi untuk memeriksa KTP elektronik online, dengan memasukan nomor induk kependudukan (NIK) masyarakat bisa melihat data kependudukan mereka sesuai dengan KTP masing-masing. Jika NIK tidak terdaftar cek kembali NIK pada KTP elektronik dan Kartu Keluarga dipastikan harus sama. Atau dapat langsung datang ke `Dinas Kependudukan dan Pencatatan Sipil Kabupaten Batang` untuk konfirmasi. 
Sumber Data yang digunakan dalam Aplikasi ini berasal dari API dari server resmi `Dinas Kependudukan dan Pencatatan Sipil Kabupaten Batang`.

![gambar](/images/porto/ktp-4.png)

2.`Cek BPJS` Adalah aplikasi untuk memeriksa data peserta `BPJS`, dengan memasukan nomor induk kependudukan (NIK) atau nomor kartu `BPJS` masyarakat bisa melihat data kepesertaan `BPJS`. 
Sumber Data yang digunakan dalam Aplikasi ini berasal dari `Web Service Pcare BPJS Resmi.`

![gambar](/images/porto/ktp-5.png)

3.`Cek DPS` Adalah aplikasi untuk memeriksa daftar pemilih sementara pilkada serentak tahun 2018. Apabila anda belum terdaftar, segera mengunjungi kantor KPU kabupaten/kota atau sekretariat PPS di kantor kelurahan/desa sesuai alamat di KTP-el/Suket. 
Sumber Data yang digunakan dalam Aplikasi ini berasal dari `Redirect API dari website resmi KPU`.

Dibangun mengunakan [PHP native](http://www.php.net/) memanfaatkan fungsi curl untuk mengambil data dari server [Dispendukcapil](http://dispendukcapil.batangkab.go.id) maupun [KPU](https://infopemilu.kpu.go.id), sedangkan untuk mempercantik tampilan menggunakan framework CSS  [MUI](https://www.muicss.com).



## Mirror PCARE BPJS

- URL: [dinkes.batangkab.go.id/pcare](https://dinkes.batangkab.go.id/pcare)
- Status: <span class="badge badge-info">Development</span>

Sudah menjadi rahasia umum kalau dokumentasi Bridging System BPJS sering lambat diakses maupun sering berganti link URL,
sehingga mempersulit pengembang sistem informasi puskesmas untuk melakukan integrasi dengan sistem brigging BPJS. 
Dengan ada halaman dokumentasi ini semoga bisa menjadi alternatif rekan sejawat guna percepatan integrasi dengan sistem brigging BPJS.

![gambar](/images/porto/pcare.png)

Dibangun mengunakan [PHP native](http://www.php.net/) dan untuk mempercantik tampilan menggunakan framework CSS [MUI](https://www.muicss.com), sedangkan untuk mempercantik snippets kode sumber menggunakan bantuan library [JavaScript code prettifier](https://github.com/google/code-prettify).



## SI-Pentol

- URL: [rsudbatang.com/sipentol](https://rsudbatang.com/sipentol)
- Status: <span class="badge badge-success">production</span>

`Sistem Pendaftaran Online Rawat Jalan` atau `SI-Pentol` adalah aplikasi pendaftaran online via SMS gateway, Android dan Website persembahan dari RSUD Batang untuk memberikan kemudahan pelayanan kepada masyarakat pengguna jasa RSUD Batang dalam mendaftar klinik rawat jalan.

![gambar](/images/porto/sipentol-backend.png)

- Tampilan backend page SI-Pentol yang digunakan oleh pegawai RSUD Batang sesuai jabatan yang dimiliki, dibangun mengunakan framework PHP [Laravel](https://laravel.com), sedangkan untuk mempercantik tampilan menggunakan framework CSS yang sudah sangat mainstream, yaitu [Bootstrap](https://getbootstrap.com).


![gambar](/images/porto/sipentol-web.png)

- Tampilan halaman pendaftaran online yang bisa digunakan masyarakat pengguna jasa RSUD Batang untuk mendaftar klinik rawat jalan, dibangun mengunakan [PHP native](http://www.php.net/), sedangkan untuk mempercantik tampilan menggunakan framework CSS [MUI](https://www.muicss.com).


![gambar](/images/porto/sipentol-android.png)

- Aplikasi SI-Pentol platform android bisa di download google play store di link berikut : [SI-Pentol Android](https://play.google.com/store/apps/details?id=com.rifky.fuady.pendaftaranrawatjalan), dibangun mengunakan [Android native](https://developer.android.com/docs) dengan menggunakan bantuan build tools [Android Studio](https://developer.android.com/studio), sedangkan untuk membangun `REST API` menggunakan mikro framework PHP [Lumen](https://lumen.laravel.com).


![gambar](/images/porto/sms.png)

- SMS Gateway SI-Pentol dengan cara mengetik SMS dengan format :

```bash
Nomor_RM * Klinik_tujuan kirim SMS ke 08112625552
```

Untuk membangun Bot auto reply SMS mengunakan [PHP native](http://www.php.net/), sedangkan untuk menghubungkan perangkat modem dengan komputer server menggunakan library opensource [Gammu](https://wammu.eu/gammu). 



## Fintech BitAlley

- URL: [bitalley.io](https://bitalley.io)
- Status: <span class="badge badge-secondary">EOL</span>

BitAlley adalah platform untuk transaksi peer to peer dalam menciptakan pasar cryptocurrency yang membuat mudah user untuk membeli dan menjual aset dan layanan menggunakan cryptocurrency.

![gambar](/images/porto/bitalley.png)

Dibangun mengunakan CMS [Wordpress](https://wordpress.org) dan menggunakan open source boilerplate tema [HTML5 Blank](http://html5blank.com).



## Bunda Berencana

- URL: [Google Play Store](https://play.google.com/store/apps/details?id=com.rifky.bundaberencana)
- Status: <span class="badge badge-secondary">EOL</span>

Aplikasi Bunda Berencana adalah aplikasi yang dapat membantu bunda dalam merencanakan kehamilan dengan mengkalkulasi masa subur dan menemani bunda dalam setiap momen kehamilan dengan informasi yang bunda butuhkan saat hamil.

Aplikasi ini telah memenangkan Challenge dengan tema [Bantu Ibu dengan Teknologi](https://www.dicoding.com/challenges/125) yang dilaksanakan pada tanggal 22 Desember 2016 yang diadakan oleh [IBM Bluemix Platform](https://console.ng.bluemix.net/) bekerjasama dengan [Dicoding](https://blog.dicoding.com).

Pengumuman pemenang challenge dimuat dalam [Blog Dicoding](https://blog.dicoding.com/5-aplikasi-memenangkan-challenge-bantu-ibu-dengan-teknologi/) dan [Blog Codepolitan](https://www.codepolitan.com/5-aplikasi-memenangkan-challenge-bantu-ibu-dengan-teknologi).

![gambar](/images/porto/bunda-berencana.png)

Dibangun mengunakan [Android native](https://developer.android.com/docs) dengan menggunakan bantuan build tools [Android Studio](https://developer.android.com/studio). 