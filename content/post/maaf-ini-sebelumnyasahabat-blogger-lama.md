---
title: 'Tutorial Dasar Pemrograman Batch File'
date: 2013-01-02T21:00:00.000+07:00
draft: false
aliases: [ "/2013/01/maaf-ini-sebelumnyasahabat-blogger-lama.html" ]
tags : [Bahasa Pemrograman, Tips dan Trick]
---

[![](http://3.bp.blogspot.com/-U_g5qOIx2rE/UOQtt7mH9NI/AAAAAAAAAas/KDiSL2C2IFY/s200/G_127.png)](http://3.bp.blogspot.com/-U_g5qOIx2rE/UOQtt7mH9NI/AAAAAAAAAas/KDiSL2C2IFY/s1600/G_127.png)

  

  

Maaf ini sebelumnya sahabat blogger, lama gak pernah posting...

Soalnya My D. Inspiron yang biasa saya jinjing tak bawa kemana-mana, membantu menyelesaikan pekerjaan-pekerjaan saya serta menjadi media pembelajaran saya, 3 bulan terakhir harus terpaksa di sharing sama temen, biasa lah masalah finansial yang kurang balance dan mungkin akibat terkena imbas krisis Moneter Global (hiyah alasan, Krisis Moneter Global kan awal 2012) hehhehe...:p

Oke. Sekarang kita langsung saja masuk ke Judul posting di atas, kemaren makul Sistem Operasi Praktek yang di ajarkan Oleh _Bpk. **M. Rifqi Maulana M.Kom**_ adalah Pemrograman Batch File di Windows, setelah mengajarkan cara mengoprek-oprek registry tools di Windows. Dan sekarang saya ingin men-sharing apa yang diajarkan **_Beliau._**

Udah pada tau Perintah-perintah dasar di DOS belum? Kalo belum bisa lihat [disini.](http://rifky-fuady.blogspot.com/2013/01/perintah-dasar-dos.html)

Biar nggak kebingunan, lebih baik baca dasar-dasarnya dulu. Oke...????

Lanjut deh,  yang ingin saya sharing disini adalah source code dan tutorial pemrograman batch file yang masih sederhana, masih dalam tingkatan pemula, jadi kalo ada master-master yang membaca  postingan saya, dan mungkin saya ada kesalahan, bisa membagikan kritik dan saran nya dibawah komentar, supaya kita semua disini bisa sama belajar dan berbagi ilmu. Setuju gak??? Hehehhe...:-)

· **Apa itu Pemrograman Batch File?**

\- Batch file programming adalah pemrograman dasar yang dikenalkan oleh sistem operasi  Microsoft Windows (Premkumar, 2009).

\- Batch file biasanya dibuat untuk memberikan perintah kepada SO Windows secara beruntun. Misalnya:

1. Copykan file bernama myfile.txt dari drive d:\\ ke c:\\

2. Setelah itu rename c:\\myfile.txt menjadi c:\\fileku.txt

3. Kemudian hapus file d:\\myfile.txt

\- Dasar sintak program didalam batch file adalah perintah-perintah DOS.

\- Ketika Batch Program di eksekusi, program didalamnya di interpreter baris demi baris oleh CLI (Commad Line Interpreter) yaitu: command.com atau cmd.exe

\- Interpreter: Proses pembacaan, pengecekan dan pegeksekusian sintak program secara perbaris.

\- Misal, jika ada 5 baris program, dan dibaris ke-3 ada kesalahan penulisan, maka yang akan dieksekusi baris 1 dan 2 saja sedangkan baris 3,4 dan 5 tidak dieksekusi.

  

· **Bagaimana cara membuat File Batch?**

\- Batch file dapat dibuat dengan editor apapun semacam Notepad, Notepad++, WordPad dan lain sebagainya.

\- Penulisan script / sintak pada batch file tidak case sensitive artinya huruf besar dan huruf kecil dianggap sama

\- Ekstensi batch file adalah .bat

\- Contohnya seperti gambar berikut (buka spoiler):

**Membuat File Batch**: 

[![](http://1.bp.blogspot.com/-_EFHV38NsSE/UOQuvACuziI/AAAAAAAAAa8/ceEHlltEFh0/s320/gmbr1.jpg)](http://1.bp.blogspot.com/-_EFHV38NsSE/UOQuvACuziI/AAAAAAAAAa8/ceEHlltEFh0/s1600/gmbr1.jpg)

[![](http://1.bp.blogspot.com/-uvuFoB665z0/UOQuvtgE8HI/AAAAAAAAAbI/_P7v9DIEDQo/s320/gmbr2.jpg)](http://1.bp.blogspot.com/-uvuFoB665z0/UOQuvtgE8HI/AAAAAAAAAbI/_P7v9DIEDQo/s1600/gmbr2.jpg)

[![](http://1.bp.blogspot.com/-82cybRpRzh4/UOQuwZbp94I/AAAAAAAAAbU/v4F9BAD95xE/s320/gmbr3.jpg)](http://1.bp.blogspot.com/-82cybRpRzh4/UOQuwZbp94I/AAAAAAAAAbU/v4F9BAD95xE/s1600/gmbr3.jpg)

[![](http://2.bp.blogspot.com/-bfAKZXSS0Zs/UOQuw3rwixI/AAAAAAAAAbk/va8mZHsLVZY/s320/gmbr4.jpg)](http://2.bp.blogspot.com/-bfAKZXSS0Zs/UOQuw3rwixI/AAAAAAAAAbk/va8mZHsLVZY/s1600/gmbr4.jpg)

[![](http://4.bp.blogspot.com/-PF5kfUYMjwg/UOQux1C6AmI/AAAAAAAAAbw/JNYhOXPkumM/s320/gmbr5.jpg)](http://4.bp.blogspot.com/-PF5kfUYMjwg/UOQux1C6AmI/AAAAAAAAAbw/JNYhOXPkumM/s1600/gmbr5.jpg)

[![](http://3.bp.blogspot.com/-MHXWWKwW2U4/UOQvzTWXONI/AAAAAAAAAcA/bYuzcsLsuZ4/s320/gmbr6.jpg)](http://3.bp.blogspot.com/-MHXWWKwW2U4/UOQvzTWXONI/AAAAAAAAAcA/bYuzcsLsuZ4/s1600/gmbr6.jpg)

  

  

· **Bagaimana cara Memberi Title Window?**

\- Kita dapat mengubah window title dengan menambah title nama\_window sebelum sintak pause. Disarankan: letakkan sintak title setelah sintak: @echo off.

\- Contoh :

**Memberi Title Window**: 

[![](http://4.bp.blogspot.com/-56QNC2lFqw0/UOQweeAojwI/AAAAAAAAAcQ/jDSfGDlyDwc/s320/gmbrtw1%2Bfix.jpg)](http://4.bp.blogspot.com/-56QNC2lFqw0/UOQweeAojwI/AAAAAAAAAcQ/jDSfGDlyDwc/s1600/gmbrtw1%2Bfix.jpg)

  
@echo off  
title Program Pertamaku  
echo NIM : 12.240.0001  
echo Nama : A. Fuady Rifky  
echo HP : 0878 3081 4574  
pause  
  

[![](http://4.bp.blogspot.com/-srXgNP5L7ww/UOQw5LslfXI/AAAAAAAAAcc/fucD9ZEeyl4/s320/gmbrtw3%2Bfix.jpg)](http://4.bp.blogspot.com/-srXgNP5L7ww/UOQw5LslfXI/AAAAAAAAAcc/fucD9ZEeyl4/s1600/gmbrtw3%2Bfix.jpg)

  

  

  

· **Bagaimana cara Mendefinisikan Variabel?**

\- Seperti bahasa pemrograman, batch file programming juga dapat mendefinisikan variabel.

\- Variabel: adalah salah satu cara yang dilakukan oleh program untuk menyimpan sebuah nilai di dalam memory. Secara default pendefinisian variabel pada batch file bertipe string.

\- Contoh: a=2, b=4, nama=budi, jenjang=S1 dan lain sebagainya.

\- Cara mendefinisikan variabel pada batch programming adalah dengan menggunakan sintak _set_

\- Contoh:

**Mendefinisikan Variabel**: 

@echo off  
set a=2  
set b=4  
set nama=budi  
set jenjang=S1  
pause

  

  

· **Bagaimana cara Menampilkan Isi Variabel?**

\- Variabel yang telah kita definisikan sebelumnya belum ditampilkan ke layar. Nah, cara menampilkan isi variabel tersebut ke layar secara sederhana adalah dengan: **echo** _%nama\_variabel%_

\- Contoh:

**Menampilkan Variabel**: 

@echo off  
set a=2  
set b=4  
set nama=fuady  
set jenjang=S1  
echo %a%  
echo %b%  
echo %nama%  
echo %jenjang%  
pause