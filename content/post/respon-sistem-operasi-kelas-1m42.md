---
title: 'Respon Sistem Operasi'
date: 2012-10-21T22:57:00.000+07:00
draft: false
aliases: [ "/2012/10/respon-sistem-operasi-kelas-1m42.html" ]
tags : [Tugas]
---

for Pak M. Rifqi Maulana M.Kom  

  

**1\. Jelaskan mengenai Multiprogramming, Multiprocessing dan Distributed Processing!**

\-  Multiprogramming adalah kegiatan menjalankan beberapa program pada memori pada satu waktu.

\- Multiprocessing adalah istilah teknologi informasi dalam bahasa Inggris yang merujuk kepada kemampuan pemrosesan komputer yang dilakukan secara serentak

\-  Mengerjakan semua proses pengolahan data secara bersama antara komputer pusat dengan beberapa komputer yang lebih kecil dan saling dihubungkan melalui jalur komunikasi

  

**2\. Sebutkan 2 fungsi utama Sistem Operasi  dan 3 fungsi minor Sistem Operasi !**

a. Fungsi Utama Sistem Operasi :

\- melakukan pengelolaan proses mencakup penyiapan, penjadwalan, dan pemantauan proses program yang sedang dijalankan.

\- melakukan pengelolaan data pengendalian terhadap data masukan/keluaran.

b. Fungsi Minor Sistem Operasi :

\-Mengimplementasi antarmuka untuk pemakai

\-Memungkinkan pemakaian bersama perangkat keras

\-Memungkinkan pemakaian data scr bersama

\-Mencegah pengguna2 saling mengganggu

\-Menjadwalkan pemakaian sumber daya

\-Memberi fasilitas I/O

\-Memulihkan kesalahan2

\-Menghitung penggunaan sumber daya

\-Mengorganisasi data agar aman dan cepat diakses

\-Menangani komunikasi jaringan

  

3\. Sebutkan dan Jelaskan 3 sasaran Sistem Operasi!

Sistem operasi mempunyai 3 sasaran utama yaitu kenyamanan (membuat penggunaan komputer menjadi lebih nyaman), efisiensi (penggunaan sumberdaya sistem komputer secara efisien) dan mampu berevolusi (sistem operasi harus dibangun sehingga memungkinkan dan memudahkan pengembangan, pengujian serta pengajuan sistem-sistem yang baru).

  

**4\. Sebutkan 2 strategi penjadwalan dan jelaskan perbedaannya!**

a. Penjadwalan Nonpreemptive

Begitu proses diberi jatah waktu pemroses maka pemroses tidak dapat diambil alih oleh proses lain sampai proses itu selesai.

b. Penjadwalan Preemptive

Saat proses diberi jatah waktu pemroses maka pemroses dapat diambil alih proses lain sehingga proses disela sebelum selesai dan harus dilanjutkan menunggu jatah waktu pemroses tiba kembali pada proses itu.

  

**5\. Sebutkan 6 algoritma penjadwalan yang  Anda ketahui!**

 o First-Come First-Served (FCFS)

Algoritma ini merupakan algoritma penjadwalan yang paling sederhana yang digunakan CPU. Dengan menggunakan algoritma ini setiap proses yang berada pada status ready dimasukkan ke dalam antrian FIFO sesuai dengan waktu kedatangannya. Proses yang tiba terlebih dahulu yang akan dieksekusi

terlebih dahulu.

o Shortest-Job First (SJF)

Algoritma ini mempunyai cara penjadwalan yang berbeda dengan FCFS. Dengan algoritma ini maka setiap proses yang ada di antrian ready akan dieksekusi berdasarkan burst time terkecil. Hal ini mengakibatkan waiting time yang pendek untuk setiap proses dan karena hal tersebut maka waiting

o Penjadwalan dengan Prioritas

Priority Scheduling merupakan algoritma penjadwalan yang mendahulukan proses dengan nilai prioritas tertinggi.

o Round Robin

Algoritma ini didesin untuk sistem time-sharing. Proses akan mendapat jatah sebesar time quantum dengan nilai quantum umumnya sebesar 10-100 ms

o Antrian Multilevel (Multilevel Queue)

Ide dasar dari algoritma ini adalah berdasarkan pada sistem prioritas proses. Prinsipnya adalah, jika setiap proses dapat dikelompokkan berdasarkan prioritasnya.

o Multilevel Feedback Queue

Algoritma ini mirip sekali dengan algoritma Multilevel Queue. Perbedaannya ialah algoritma ini mengizinkan proses untuk pindah antrian. Jika suatu proses menyita CPU terlalu lama, maka proses itu akan dipindahkan ke antrian yang lebih rendah. Ini menguntungkan proses interaksi, karena proses

  

**6\. Jelaskan salah satu algoritma penjadwalan yang Anda ketahui!**

Penjadwalan Round Robin yaitu:

Algoritma round robin dirancang untuk sistem time sharing. Algoritma ini mirip dengan penjadwalan FCFS (First Come First Served), namun preemption ditambahkan untuk switch (peralihan proses) antara proses. Antrian ready diperlakukan atau dianggap sebagai antrian sirkular. CPU menglilingi antrian ready dan mengalokasikan masing-masing proses untuk interval waktu tertentu sampai satu time slice /quantum.

 Algoritma ini berjalan dengan menggilir proses yang ada pada antrian. Setiap Proses akan mendapat jatah sebesar time quantum.  Jika time quantum-nya habis atau proses sudah selesai, CPU akan dialihkan ke proses yang selanjutnya. Tentu proses ini cukup adil karena tak ada proses yang diprioritaskan, semua proses mendapat jatah waktu yang sama dari CPU yaitu (1/n), dan tak akan menunggu lebih lama dari (n-1)q dengan q adalah lama 1 quantum.

Ketentuan algoritma round robin adalah sebagai berikut:

1\. Jika quantum dan proses belum selesai maka proses menjadi runnable dan pemroses dialihkan ke proses lain.

2\. Jika quantum belum habis dan proses menunggu suatu kejadian (selesainya operasi I/O), maka proses menjadi blocked dan pemroses dialihkan ke proses lain.

3\. Jika quantum belum habis tapi proses telah selesai, maka proses diakhiri dan pemroses dialihkan ke proses lain.

  

**7\. Sebutkan kriteria untuk mengukur dan optimasi kinerja penjadwalan!**

1.  Adil (fairness)

¡ Proses-proses yg dilakukan sama, yaitu mendapat jatah waktu layanan pemroses yg sama dan tidak ada proses yg tidak kebagian layanan pemroses sehingga mengalami starvation. Starvation adalah kondisi bahwa proses tidak pernah berjalan karena tidak dijadwalkan untuk berjalan.

2. Efisiensi

¡ Efisiensi atau utilitas pemroses yg dihitung dengan perbandingan (rasio) waktu sibuk pemroses dengan total waktu operasi sistem komputer scr keseluruhan.

3. Waktu tanggap (response time)

¡ Waktu tanggap pd sistem interaktif didefinisikan sbg waktu yg dihabiskan dari saat karakter terakhir dari perintah dimasukkan oleh program sampai hasil pertama muncul di I/O device seperti monitor.

4. Turn arround time

¡ Adalah waktu yg dihabiskan dari saat proses mulai masuk ke sistem sampai proses itu diselesaikan sistem. Waktu yg dimaksud adl waktu yg dihabiskan proses berada di sistem, diekspresikan sbg penjumlahan waktu eksekusi dan waktu menunggu proses itu selesai.

5. Throughput

¡ Adalah jumlah proses yg diselesaikan selama satu selang/unit waktu. Diekspresikan dengan menjumlahkan proses pemakai yg dapat dieksekusi dalam satu unit/interval waktu tertentu.

  

**8\. Jelaskan dan berikan contoh gambar tentang algoritma penjadwalan FIFO!**

Penjadwalan FIFO merupakan penjadwalan tidak berprioritas. FIFO adalah penjadwalan paling sederhana, yaitu proses-proses diberi jatah waktu pemroses berdasarkan waktu kedatangan. Pada saat proses mendapat jatah waktu pemroses, proses dijalankan sampai selesai.

Contoh :

Ada 4 proses, yaitu P1, P2, P3, dan P4 sedang menunggu dijadwal dengan prediksi Burst Time (waktu eksekusi) 10ms, 3ms, 5ms, 4ms. Diasumsikan keempat proses masuk pada saat yang hampir bersamaan, yaitu detik ke-0. Misalkan urutan masuknya proses: P1, P2, P3 dan P4, maka Gantt Chart untuk penjadwalannya adalah:

[![](http://2.bp.blogspot.com/-ZU2X2eseTMM/UIQaVLGNvLI/AAAAAAAAAV0/T7VF3SWhRmA/s320/7.jpg)](http://2.bp.blogspot.com/-ZU2X2eseTMM/UIQaVLGNvLI/AAAAAAAAAV0/T7VF3SWhRmA/s1600/7.jpg)

  

Maka: Waiting Time untuk P1 = 0, P2 = 10, P3 = 13, P4 = 18 dan Rata-rata Waiting Time = (0 + 10 + 13 + 18)/4 = 10,25 ms.  Sementara jika urutan masuknya proses P2, P4, P3, P1 maka Gantt Chart untuk penjadwalnya adalah:

[![](http://3.bp.blogspot.com/-424eYXjyYgY/UIQablk4dpI/AAAAAAAAAV8/cuDnDergo84/s320/6.png)](http://3.bp.blogspot.com/-424eYXjyYgY/UIQablk4dpI/AAAAAAAAAV8/cuDnDergo84/s1600/6.png)

  

  
  

Maka Waiting timenya adalah: P1 = 12, P2 = 0, P3 = 7, P4 = 3 dan Rata-rata Waiting Timenya adalah: (12 + 0 + 7 + 3) / 4 = 5,5 ms