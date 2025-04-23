Saat ini menggunakan modul pembelajaran  
https://roadmap.sh/linux
- [x] Navigation Basics
![Latihan mv ](images/Ubuntu%20Server1.jpg)



- [x] Directory Hierarchy Overview

<details>
<summary> Struktur direktori di Linux </summary>

<br>
Dikenal sebagai Filesystem Hierarchy Standard (FHS). Memahami struktur ini penting agar kamu bisa lebih mudah mengelola file dan menjelajahi sistem Linux dengan efisien.  
  
📁 Struktur Direktori Utama di Linux:  
`/` (Root)  
Ini adalah akar dari seluruh sistem file. Semua direktori lainnya berada di bawah direktori ini.  
Anggap saja seperti “C:\” di Windows.

`/home`  
Berisi folder untuk setiap pengguna di sistem.  
Misalnya, pengguna bernama budi akan memiliki direktori `/home/budi`, yang berisi file pribadi dan konfigurasi pengguna tersebut.  

`/bin`  
Berisi perintah penting (binary executables) yang dibutuhkan sistem untuk bisa berjalan, terutama saat proses booting.  
Contoh: `ls`, `cp`, `mv`, `rm`.  

`/sbin`  
Berisi perintah penting untuk administrasi sistem, biasanya digunakan oleh superuser (root).  
Contoh: `reboot`, `shutdown`, `ifconfig`.  

`/etc`  
Berisi file konfigurasi sistem, seperti konfigurasi jaringan, pengguna, service, dan lainnya.  
Contoh: `/etc/passwd`, `/etc/hosts`, `/etc/fstab`.  

`/var`  
Berisi data yang berubah secara dinamis selama sistem berjalan.  
Termasuk log sistem, mail spool, print spool, cache, dsb.  
Contoh: `/var/log/syslog` untuk log sistem.  

`/usr`  
Berisi program dan file pengguna (user-level) seperti aplikasi, dokumentasi, library tambahan.  
`/usr/bin` berisi banyak program biasa, sedangkan `/usr/sbin` untuk utilitas sistem tambahan.  

`/lib`  
Berisi library (perpustakaan kode) yang dibutuhkan oleh program di `/bin dan /sbin`.  
Versi 64-bit biasanya ada di `/lib64`.

`/tmp`  
Digunakan untuk menyimpan file sementara.  
File di sini bisa dihapus otomatis saat sistem restart.  

</details>

