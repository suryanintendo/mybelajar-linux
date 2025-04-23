# Command Line Interface (CLI)

> Perintah dasar pada terminal (CLI)


## 1. Perintah Dasar Terminal

### 1.1. Perintah Informasi
  

| Huruf | Keyword | Keterangan |
|:-----:|:-----:|------------|
| :o:|   __`pwd`__   | Melihat __Process Working Directory__ saat sekarang.  |
| :o: |   __`hostname`__   | Melihat hostname / computer name.     |
| :o: | __`whoami`__ | Menampilkan user ID dan nama user pengguna. |
| :o: | __`who`__ | Menampilkan informasi user yang telah login. |
| :o: | __`id`__ | Menampilkan informasi user dan group. |
| :o: | __`fg`__ | (*__Foreground__*), melihat daftar program yang sedang berjalan (__suspended__). |
| __:heavy_check_mark:__ | __`top`__ | Melihat informasi aplikasi yang sedang berjalan (__Task Manager CLI__).  |

### 1.2. Perintah Dasar

| Keyword | Keterangan |
|---------|------------|
| __[`ls`](#ls)__ | Melihat daftar isi suatu directory |
| __[`mkdir`](#mkdir)__ | Membuat directory |
| __[`touch`](#touch)__ | Membuat file |
| __[`cp`](#cp)__ | Menggandakan atau menyalin file dan directory |
| __[`mv`](#mv)__ | Melakukan perubahan nama file atau memindahkan file ke ke lokasi yang berbeda |
| __[`rm`](#rm-dan-rmdir)__ | Menghapus file atau directory (`-d`) |
| __[`rmdir`](#rm-dan-rmdir)__ | Menghapus directory |
| __[`cat`](#cat)__ | Menggabungkan data files dan menampilkannya pada standard output |
| __[`ping`](#ping)__ | Memanggil IP Address atau hostname server |
| __[`which`](#which)__ | Menampilkan lokasi file executable (bin) |
| __[`grep`](#grep)__ | Menemukan file atau standard input berdasarkan PATTERN. Default RegEx (BRE) |
| __[`sudo`](#sudo)__ | Mengeksekusi perintah sebagai user lain |
| __[`kill`](#kill)__ | Menghentikan program yang sedang bekerja (`background process`) |

#### 1.2.1. Bentuk Implementasi

- ##### ls

    Contoh 1 : Melihat daftar isi directory yang sedang aktif.
    ``` bash
    $ ls
    ```

    Contoh 2 : Melihat daftar isi directory lain.
    ``` bash
    $ ls Documents
    ```

- ##### mkdir

    Membuat directory atau folder.
    ``` bash
    $ mkdir games
    ```

    Membuat directory beserta sub-directory.
    ``` bash
    $ mkdir -p games/2016/need-4-speed
    ```

- ##### touch

    Membuat file.
    ``` bash
    $ touch index.py
    ```

- ##### cp

    Menggandakan atau menyalin file dan directory

    Contoh 1 : Mengcopy file
    ``` bash
    $ cp index.py index2.py
    ```

    Contoh 2 : Mengcopy directory
    ``` bash
    $ cp -r music Documents/music
    ```

- ##### mv

    Melakukan perubahan nama file atau memindahkan file ke ke lokasi yang berbeda

    Contoh 1 : Merubah nama file (rename file)
    ``` bash
    $ mv app.py index.py
    ```

    Contoh 2 : Memindahkan folder ke folder lainnya
    ``` bash
    $ mv need-4-speed games/2016
    ```

- ##### rm dan rmdir

    Menghapus file atau directory

    Contoh 1 : Menghapus file.
    ``` bash
    $ rm project-1/index.py
    ```

    Contoh 2 : Menghapus directory.
    ``` bash
    $ rm -d project-1

    # atau

    $ rmdir project-1
    ```

- ##### cat

    Menggabungkan data files dan menampilkannya pada standard output.
    ``` bash
    $ cat index.py
    ```

- ##### ping

    Memanggil IP Address atau hostname server.

    ``` bash
    $ ping www.google.com

    # atau

    $ ping 192.168.1.1
    # => PING 192.168.1.1 (192.168.1.1) 56(84) bytes of data.
    # => 64 bytes from 192.168.1.1: icmp_seq=1 ttl=64 time=1.49 ms
    # => 64 bytes from 192.168.1.1: icmp_seq=2 ttl=64 time=1.18 ms
    # => ...
    ```
    __Note :__ tekan `ctrl + c` pada keyboard (untuk menghentikan proses)

- ##### which

    Menampilkan lokasi file executable (bin).
    ``` bash
    $ which sudo
    # => /usr/bin/sudo

    $ which apt-get
    # => /usr/bin/apt-get
    ```

- ##### grep

    Menemukan file atau standard input berdasarkan PATTERN. Default RegEx (BRE).

    Contoh

    ``` bash
    $ ls | grep 'project-*'
    ```

- ##### sudo

    Mengeksekusi perintah sebagai (super user) atau user lain.

    ``` bash
    $ sudo apt-get update
    ```

- ##### kill

    Menghentikan program yang sedang bekerja (`background process`).

    `$ kill [PID]`

    Contoh, PID dari Gedit adalah 4112

    ``` bash
    $ kill 4112
    ```


## 2. Keyboard & Shortcut

| Key | Keterangan |
|:---:|------------|
| :arrow_up: | melihat history perintah yang di akses sebelumnya |
| :arrow_down: | `redo` melihat history perintah yang di akses sebelumnya |
| `|` (pipeline) | memisahkan perintah perintah untuk dikombinasikan dengan program lainnya |
| `~` (tilde) | alias dari /home/<username> |
| `ctrl + c` | membatalkan proses yang sedang berjalan |
| `ctrl + d` | Mengirim pesan EOF (End of File) kepada proses yang sedang berlangsung |
| `ctrl + z` | melakukan suspend proses yangg sedang berjalan |


## 3. Implementasi

Buka terminal dan ketikan `ls` atau `ls /home/<username>`

Contoh

``` bash
$ ls /home/guntur
```

__Bantuan (Help)__

Cara melihat bantuan atau informasi dari perintah adalah dengan menambahkan __`--help`__ setelah keyword perintah.

Contoh

``` bash
$ ls --help
```


## 4. PATH

### 4.1. Absolute PATH

__Absolut PATH__ atau dengan sebutan lain __fullpath__ merupakan metode penataan lokasi file atau directory yang akan implementasikan. Cara kerja __absolute path__ pada OS (__LINUX__) selalu di awali dengan symbol __root [ / ]__ kemudian disertai dengan subdirectory atau nama file.

Contoh implementasi pada absolute path

``` bash
$ pwd
# => /home/guntur

$ cd /etc/apt
$ pwd
# => /etc/apt
```

__Schema__

| Path | Deskripsi |
|------|-----------|
| __/__ | directory root |
| __/etc__ | directory _etc_ yang berada di dalam _root_ directory |
| __/etc/apt__ | directory _apt_ yang berada di dalam _etc_ directory |


### 4.2. Relative PATH

Berbeda dengan absolute path yang selalu diawali dengan __[ / ]__, __relative path__ tidak memerlukan tanda symbol root pada saat diimplementasikan. Cara kerja dari metode __relative path__ bergantung kepada lokasi directory yang sedang aktif.

Contoh implementasi pada relative path

- Contoh 1

    ``` bash
    $ pwd
    # => /home/guntur

    $ cd Documents
    $ pwd
    # => /home/guntur/Documents
    ```

- Contoh 2

    ``` bash
    $ pwd
    # => /home/guntur/Documents

    $ cd ../games/need-4-speed
    $ pwd
    # => /home/guntur/games/need-4-speed
    ```
