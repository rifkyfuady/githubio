+++
title = "Tugas Arsitektur Dan Organsasi Komputer - Pengenalan Bahasa Assembly"
date = 2012-12-12T00:46:00Z
updated = 2012-12-12T00:54:03Z
tags = ["Bahasa Pemrograman", "Tugas"]
blogimport = true 
[author]
	name = "Rifky Fuady"
	uri = "https://plus.google.com/101982203483309256996"
+++

<div class="separator" style="clear: both; text-align: center;"><a href="http://1.bp.blogspot.com/-beftZiDfHNE/UMdwQaqPXjI/AAAAAAAAAZc/6HebV2GnTRg/s1600/logo_stmik_png.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="200" src="http://1.bp.blogspot.com/-beftZiDfHNE/UMdwQaqPXjI/AAAAAAAAAZc/6HebV2GnTRg/s200/logo_stmik_png.png" width="200" /></a></div><div class="separator" style="clear: both; text-align: center;"><br /></div><div class="separator" style="clear: both; text-align: center;">For &nbsp;<b><span lang="EN-US" style="font-family: 'Times New Roman', serif; font-size: 16pt; line-height: 24px;">Bpk.&nbsp;</span></b><b><span lang="EN-US" style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 16.0pt; line-height: 115%; mso-ansi-language: EN-US; mso-bidi-language: AR-SA; mso-bidi-theme-font: minor-bidi; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;">Sattriedi </span><span style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 16.0pt; line-height: 115%; mso-ansi-language: IN; mso-bidi-language: AR-SA; mso-bidi-theme-font: minor-bidi; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;">W</span><span lang="EN-US" style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 16.0pt; line-height: 115%; mso-ansi-language: EN-US; mso-bidi-language: AR-SA; mso-bidi-theme-font: minor-bidi; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;">.</span><span style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 16.0pt; line-height: 115%; mso-ansi-language: IN; mso-bidi-language: AR-SA; mso-bidi-theme-font: minor-bidi; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;">B</span><span lang="EN-US" style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 16.0pt; line-height: 115%; mso-ansi-language: EN-US; mso-bidi-language: AR-SA; mso-bidi-theme-font: minor-bidi; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;">,</span><span style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 16.0pt; line-height: 115%; mso-ansi-language: IN; mso-bidi-language: AR-SA; mso-bidi-theme-font: minor-bidi; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;">S</span><span lang="EN-US" style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 16.0pt; line-height: 115%; mso-ansi-language: EN-US; mso-bidi-language: AR-SA; mso-bidi-theme-font: minor-bidi; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;">.</span><span style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 16.0pt; line-height: 115%; mso-ansi-language: IN; mso-bidi-language: AR-SA; mso-bidi-theme-font: minor-bidi; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;">S</span><span lang="EN-US" style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 16.0pt; line-height: 115%; mso-ansi-language: EN-US; mso-bidi-language: AR-SA; mso-bidi-theme-font: minor-bidi; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;">i,</span><span style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 16.0pt; line-height: 115%; mso-ansi-language: IN; mso-bidi-language: AR-SA; mso-bidi-theme-font: minor-bidi; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;">M</span><span lang="EN-US" style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 16.0pt; line-height: 115%; mso-ansi-language: EN-US; mso-bidi-language: AR-SA; mso-bidi-theme-font: minor-bidi; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;">.</span><span style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 16.0pt; line-height: 115%; mso-ansi-language: IN; mso-bidi-language: AR-SA; mso-bidi-theme-font: minor-bidi; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;">K</span><span lang="EN-US" style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 16.0pt; line-height: 115%; mso-ansi-language: EN-US; mso-bidi-language: AR-SA; mso-bidi-theme-font: minor-bidi; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;">om</span></b></div><br /><div class="separator" style="clear: both; text-align: center;"><br /></div><h2 style="text-align: center;"><b>PENGENALAN BAHASA ASSEMBLY</b></h2><div class="separator" style="clear: both; text-align: center;"><br /></div><div class="separator" style="clear: both; text-align: center;"><br /></div><div class="separator" style="clear: both; text-align: center;"></div><div class="MsoNormal" style="text-align: justify;"><b><span lang="EN-US" style="font-size: 14.0pt; line-height: 115%;">BAB I . PENDAHULUAN</span></b></div><div class="MsoNormal" style="text-align: justify;"><b><span lang="EN-US" style="font-size: 14.0pt; line-height: 115%;"><br /></span></b></div><div class="MsoNormal" style="text-align: justify;"><span style="font-size: 19px; line-height: 21px;"><b>1.1 LATAR BELAKANG</b></span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Bahasa Assembly&nbsp; atau&nbsp; Rakitan&nbsp; diprakarsai oleh&nbsp; IBM&nbsp; pada&nbsp; tahun&nbsp; 1956&nbsp; – 1963.</span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%; mso-ansi-language: IN;"> </span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Bahasa&nbsp; assembly&nbsp; termasuk&nbsp; bahasa&nbsp; tingkat&nbsp; rendah.&nbsp; Pada&nbsp; tahun&nbsp; 1957,&nbsp; sebuah&nbsp; tim&nbsp; yang</span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%; mso-ansi-language: IN;"> </span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">dipimpin oleh&nbsp; John W. Backus berhasil mengembangkan sebuah bahasa baru yang lebih</span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%; mso-ansi-language: IN;"> </span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">mengarah pada keperluan untuk menganalisa persoalan numeric. Extensi yang dihasilkan</span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%; mso-ansi-language: IN;"> </span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">dari bahasa assembly adalah file dengan extensi Com dan Exe. Secara umum kedua jenis</span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%; mso-ansi-language: IN;"> </span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">file&nbsp; tersebut memiliki&nbsp; perbedaan&nbsp; antara&nbsp; program&nbsp; yang&nbsp; berekstensi&nbsp; Com dan&nbsp; Exe,&nbsp; yang</span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%; mso-ansi-language: IN;"> </span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">merupakan ukuran luas daerah yang menyebabkan kelainan program dalam assembler.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Untuk&nbsp; file&nbsp; yang&nbsp; diakhiri&nbsp; dengan&nbsp; extension&nbsp; Com,&nbsp; berarti&nbsp; file&nbsp; itu&nbsp; paling&nbsp; banyak</span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%; mso-ansi-language: IN;"> </span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">hanya&nbsp; akan&nbsp; memakan&nbsp; luas&nbsp; 64&nbsp; kilobyte&nbsp; yang&nbsp; disebut&nbsp; 1&nbsp; segment,&nbsp; sedangkan&nbsp; untuk&nbsp; file</span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%; mso-ansi-language: IN;"> </span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">berekstensi EXE&nbsp; tidak dibatasi berapa segment&nbsp; yang dapat dipakai. Dapat 1 segment, 2</span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%; mso-ansi-language: IN;"> </span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">segment,&nbsp; 3&nbsp; segment&nbsp; atau&nbsp; lebih&nbsp; dari&nbsp; 3&nbsp; segment.&nbsp; Oleh&nbsp; karena&nbsp; COM&nbsp; hanya&nbsp; memiliki&nbsp; 1</span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%; mso-ansi-language: IN;"> </span><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">segment, Maka file Com memiliki kelebihan dan kekurangan sebagai&nbsp; berikut :</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">a. Stack yang telah dibuat sendiri oleh program di akhir Segment</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">b. Hanya terdapat satu segment, sehingga tidak perlu mengatur DS, CS, SS, kecuali</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">bila diinginkan.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">c. Karena hanya satu segment, maka tidak mungkin membuat program lebih dari 64</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">kb.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">d. Butuh ruangan di awal program sebanyak 100 hexa byte untuk keperluan program</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">segment prefix (PSP).</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">e. Karena PSP&nbsp; diketahui&nbsp; dengan&nbsp; pasti,&nbsp; maka perlu dilakukan&nbsp; operasi&nbsp; ke&nbsp; PSP lebih</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">mudah karena masih berada dalam 1 segment.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">f. Dapat menggunakan utility DEBUG untuk membuat program.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Kelebihan dan kekurangan program EXE, sebagai berikut :</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">a. Hasil Program panjang</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">b. Tidak perlu menyediakan tempat untuk PSP.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">c. Pembagian segmen diatur sendiri</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">d. Membuat stack sendiri</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">e. Tidak dapat membuat progr am dengan Debug.</span></div><div class="MsoNormal" style="text-align: justify;"><br /></div><div class="MsoNormal" style="text-align: justify;"><span style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 12.0pt; line-height: 115%; mso-ansi-language: IN; mso-bidi-language: AR-SA; mso-fareast-font-family: Calibri; mso-fareast-language: EN-US; mso-fareast-theme-font: minor-latin;"><b>1.2. Rumusan Masalah</b>Permasalahan yang akan dibahas dalam penulisan makalah ini, adalah definisi dari bahasa assembly dan assembler; penjelasan mengenai system bilangan dan konversi bilangan; elemen dasar bahasa assembly.<br /><br /><b>1.3. Tujuan.</b><br />Tujuan dari penulisan makalah ini ialah untuk menyelesaikan tugas mata kuliah BAHASA ASSEMBLY,dan untuk mendapatkan pengetahuan mengenai bahasa assembly baik bagi penulis maupun pembaca.<br /><br /><b>1.4. Manfaat.</b><br />Manfaat Penulisan Makalah ini adalah sebagai sarana untuk menambah pengetahuan dan sebagai media pembelajaran.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">&nbsp;</span><span style="font-size: 12pt; line-height: 115%;">&nbsp;</span></div><div class="MsoNormal" style="text-align: justify;"><br /></div><div class="MsoNormal" style="text-align: justify;"><b><span lang="EN-US" style="font-size: 14.0pt; line-height: 115%;">BAB II PEMBAHASAN</span></b></div><div class="MsoNormal" style="text-align: center;"><br /></div><div class="MsoNormal" style="text-align: justify;"><b><span lang="EN-US" style="font-size: 14.0pt; line-height: 115%;">2.1. Elemen Bahasa Asembly</span></b></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Dalam&nbsp; pemrograman&nbsp; bahasa&nbsp; assembly&nbsp; lebih&nbsp; ditekankan&nbsp; pada&nbsp; system&nbsp; operasi&nbsp;</span><span style="font-size: 12pt; line-height: 115%;">Microsoft</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">Intel</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">yang</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">seiring</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">dengan</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">perkembangan</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">mikroprosesor</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">8088/8086.&nbsp;</span><span style="font-size: 12pt; line-height: 115%;">Perkembangan</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">bahasa</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">assembly</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">tergantung</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">pada</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">linker</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">yang</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">mengubah</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">file</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">*.obj&nbsp;</span><span style="font-size: 12pt; line-height: 115%;">menjadi</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">*.exe</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">atau</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">*.com.</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">Bahasa</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">assembly</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">dikategorikan</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">sebagai bahasa</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">tingkat&nbsp;</span><span style="font-size: 12pt; line-height: 115%;">rendah. Hal</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">ini</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">untuk menggambarkan spesifikasi sebagai</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">bahasa</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">yang berorientasi</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">pada machine dependent. Untuk membandingkan bahasa mesin dan bahasa assembly&nbsp;</span><span style="font-size: 12pt; line-height: 115%;">menurut karakteristik dibagi 2 bagian :</span></div><div class="MsoListParagraphCxSpFirst" style="text-align: justify; text-indent: -18pt;"><!--[if !supportLists]--><span lang="EN-US" style="font-family: Symbol; font-size: 12.0pt; line-height: 115%; mso-bidi-font-family: Symbol; mso-fareast-font-family: Symbol;">·<span style="font-family: 'Times New Roman'; font-size: 7pt; line-height: normal;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Mnemonic Operation Code</span></div><div class="MsoListParagraphCxSpLast" style="text-align: justify; text-indent: -18pt;"><!--[if !supportLists]--><span lang="EN-US" style="font-family: Symbol; font-size: 12.0pt; line-height: 115%; mso-bidi-font-family: Symbol; mso-fareast-font-family: Symbol;">·<span style="font-family: 'Times New Roman'; font-size: 7pt; line-height: normal;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Simbolic Operand Spesification</span></div><div class="MsoListParagraphCxSpLast" style="text-align: justify; text-indent: -18pt;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;"><br /></span></div><div class="MsoListParagraphCxSpLast" style="text-align: justify; text-indent: -18pt;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;"><br /></span></div><div class="MsoNormal" style="text-align: justify;"><b><span lang="EN-US" style="font-size: 14.0pt; line-height: 115%;">2.2. Proses Assembly</span></b></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Untuk&nbsp; membangun&nbsp; skema&nbsp; proses&nbsp; translasi&nbsp; dari&nbsp; satu&nbsp; bahasa&nbsp; ke&nbsp; bentuk&nbsp; lain,&nbsp; maka&nbsp;</span><span style="font-size: 12pt; line-height: 115%;">yang perlu diperhatikan adalah mengidentifikasi</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">tugas dasar</span><span style="font-size: 12pt; line-height: 115%;">&nbsp; </span><span style="font-size: 12pt; line-height: 115%;">yang dikerjakan dalam&nbsp;</span><span style="font-size: 12pt; line-height: 115%;">proses translasi .</span></div><div class="MsoNormal" style="text-align: justify;"><span style="font-size: 12pt; line-height: 115%;"><br /></span></div><div class="MsoNormal" style="text-align: justify;"><span style="font-size: 12pt; line-height: 115%;"><br /></span></div><div class="MsoNormal" style="text-align: justify;"><b><span lang="EN-US" style="font-size: 14.0pt; line-height: 115%;">2.3. Skema Assembly</span></b></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Proses penerjemahan secara sederhana dapat dikelompokkan dalam dua fase, yaitu:</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;"><br /></span></div><div class="MsoListParagraph" style="margin-left: 41pt; text-align: justify; text-indent: -18pt;"><!--[if !supportLists]--><span lang="EN-US" style="font-family: Symbol; font-size: 14.0pt; line-height: 115%; mso-bidi-font-family: Symbol; mso-fareast-font-family: Symbol;">·<span style="font-family: 'Times New Roman'; font-size: 7pt; line-height: normal;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><b><u><span lang="EN-US" style="font-size: 14.0pt; line-height: 115%;">Fase Analisa</span></u></b></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">a. Memisahkan label, mnemonic operation code dan operand field yang ada pada</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">statement.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">b. Memasukkan symbol yang ditemukan pada label field dan alamat yang dituju</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">machine word ke dalam symbol table.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">c. Melakukan validasi mnemonic operation code dengan melihat pada mnemonic</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">table</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">d. Menentukan&nbsp; alamat&nbsp; yang&nbsp; dibutuhkan&nbsp; oleh&nbsp; statement&nbsp; berdasarkan&nbsp; pada</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">mnem</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">onic operation code dan operand field pada statement.</span><span style="font-size: 12.0pt; line-height: 115%; mso-ansi-language: IN;"></span></div><div class="MsoNormal" style="text-align: justify;"><br /></div><div class="MsoNormal" style="text-align: justify;"><b><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">&nbsp; &nbsp; &nbsp; &nbsp;</span></b><span style="font-family: Symbol; font-size: 19px; line-height: 21px; text-indent: -24px;">·</span><span style="font-size: 7pt; text-indent: -24px;">&nbsp; &nbsp;</span><b><span lang="EN-US" style="font-size: 14.0pt; line-height: 115%;">&nbsp;Fase analisis dapat dikelompokkan menjadi beberapa tahap, yaitu :</span></b></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">&nbsp;a. Lexical Analisys</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Lexical&nbsp; Analisys&nbsp; adalah&nbsp; menjalankan&nbsp; mikro&nbsp; level&nbsp; examination&nbsp; dari&nbsp; teks</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">masukan&nbsp; untuk&nbsp; mengenal&nbsp; lexial&nbsp; unit&nbsp; yang&nbsp; ada&nbsp; didalamnya&nbsp; dan&nbsp; menentukan</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">kategori syntax.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">&nbsp;b. Syntax Analisys</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Proses&nbsp; Syntac&nbsp; Analisys&nbsp; dilakukan&nbsp; terhadap&nbsp; descriptor&nbsp; dari&nbsp; lexical&nbsp; analisys</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">untuk&nbsp; menentukan&nbsp; struktur&nbsp; syntax&nbsp; dari&nbsp; statement&nbsp; masukan.&nbsp; Proses&nbsp; tersebut</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">dikenal&nbsp; dengan&nbsp; PARSING.&nbsp; Output&nbsp; dari&nbsp; parsing&nbsp; adalah&nbsp; representasi&nbsp; dari</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">struktur syntac suatu statement.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">&nbsp; c. Semantic Analisys</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Proses&nbsp; semantic&nbsp; analisys&nbsp; dapat&nbsp; diklasifikasikan&nbsp; kedalam&nbsp; proses&nbsp; declarative</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">statement dan proses eksekusi.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;"><br /></span></div><div class="MsoListParagraph" style="margin-left: 41pt; text-align: justify; text-indent: -18pt;"><!--[if !supportLists]--><span lang="EN-US" style="font-family: Symbol; font-size: 14.0pt; line-height: 115%; mso-bidi-font-family: Symbol; mso-fareast-font-family: Symbol;">·<span style="font-family: 'Times New Roman'; font-size: 7pt; line-height: normal;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><b><u><span lang="EN-US" style="font-size: 14.0pt; line-height: 115%;">Fase Syntesis</span></u></b></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">a. Menghasilkan machine operation code yang berkorespodensi dengan</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">mnemonic operation code yang telah dicari pada mnemonic table.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">b. Menghasilkan alamat operand dari symbol table</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">c. Melakukan syntesis instruksi machine.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Pada fase sysntesis dilakukan pemilihan machine operation code yang sesuai</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">dengan mnemonic Load&nbsp; dan menempatkan pada&nbsp; machine&nbsp; instruction opcode</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">field.&nbsp; Evaluasi&nbsp; korespodensi&nbsp; pengalamatan&nbsp; dilakukan&nbsp; untuk&nbsp; operand</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">expression ‘ Result + 4.</span></div><div class="MsoNormal" style="text-align: justify;"><br /></div><div class="MsoNormal" style="text-align: justify;"><b><span style="font-size: 14.0pt; line-height: 115%; mso-ansi-language: IN;">&nbsp;</span></b><b><span style="font-size: 14.0pt; line-height: 115%; mso-ansi-language: IN;">&nbsp;</span></b></div><div class="MsoNormal" style="text-align: justify;"><b><span lang="EN-US" style="font-size: 14.0pt; line-height: 115%;">2.4. Proses Assembly</span></b></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Unit&nbsp; dalam sources program digunakan untuk&nbsp; menterjemah semua bagian program.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Ketika&nbsp; fase&nbsp; analisys&nbsp; statement&nbsp; program&nbsp; pertama&nbsp; kali&nbsp; dilakukan,&nbsp; maka&nbsp; proses&nbsp; LC</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">akan dikerjakan dan symbol yang didefinisikan dalam program dimasukkan ke dalam</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">symbol table. Untuk mengurangi pengulangan, maka hasil analisis sources statement</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">dari&nbsp; first&nbsp; pass&nbsp; direpresentasikan&nbsp; dalam&nbsp; internal&nbsp; form&nbsp; pada&nbsp; sources&nbsp; statement&nbsp; yang</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">disebut&nbsp; intermediate&nbsp; code. Selain&nbsp; membentuk&nbsp; intermediate&nbsp; code,&nbsp; suatu&nbsp; proses</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">assembler juga membangun struktur database yang digunakan oleh subsequent pass.</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;"><br /></span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;"><br /></span></div><div class="MsoNormal" style="text-align: justify;"><b><span lang="EN-US" style="font-size: 14.0pt; line-height: 115%;">2.5. Spesifikasi Komputer</span></b></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Dalam&nbsp; pemrograman&nbsp; bahasa&nbsp; assembly,&nbsp; ada&nbsp; beberapa&nbsp; aspek&nbsp; utama&nbsp; yang&nbsp; minimal</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">harus ada persyaratan yang menunjang, meliputi :</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">Langkah Pasti Menuju Sukses</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">A. Perangkat Keras (Hardware) yang diperlukan:</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">1. Prosesor Intel, minimal Intel Pentium I, Intel Pentium II dan Pentium III</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">2. Monitor CGA, EGA atau VGA</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">3. Keyboard dan Mouse</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">4. USB Port</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">5. Harddisk</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">B. Perangkat Lunak (Software) yang diperlukan :</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">1. Microsoft Windows XP</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">2. Turbo Assembler</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">3. Linker : Tlink ver 3 minimal</span></div><div class="MsoNormal" style="text-align: justify;"><span lang="EN-US" style="font-size: 12.0pt; line-height: 115%;">4. Text Editor : Edit atau bahasa pemrograman</span></div><br /><br /><br /><br /><br /><br /><div class="MsoNormal"><span style="font-family: &quot;Times New Roman&quot;,&quot;serif&quot;; font-size: 12.0pt; line-height: 115%;"><b>BAB III &nbsp;PENUTUP</b><br /><br /><br />3.1. Kesimpulan.<br />Bahasa Assembly adalah bahasa yang memudahkan pemahaman bagian computer yang paling rendah, mendekati mesin. Bahasa assembly sebaiknya dipelajari secara kontektual sehingga interaksi perangkat keras dan perangkat lunak computer mungkin lebih mudah dipahami.<br />Bahasa assembly adalah bahasa pemrograman dengan korespondensi satu-satu antara perintah-perintah/pertanyaannya dan bahasa mesin computer.<br />Assembler adalah program yang mengonversi kode program sumber ke dalam bahasa mesin<br />System bilangan (number system) adalah suatu cara untuk mewakili besaran dari suatu item fisik. System bilangan terdiri dari: bilangan biner, bilangan decimal, bilangan octal dan hexadesimal.<br />Kumpulan karakter dalam assembly<br />Letter : A-Z, a-z<br />Digit : 0-9<br />Karakter khusus:<br />? , (koma)<br />@ “<br />_ &amp;<br />$ %<br />: !<br />. ‘<br />[] ~<br />() |<br />{} =<br />+ #<br />- ^<br />/ ;<br />* `&nbsp;</span></div>