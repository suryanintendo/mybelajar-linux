# Command Line Interface (CLI)

> Perintah dasar pada terminal (CLI)


## 1. Perintah Dasar Terminal

### 1.1. Perintah Informasi

| Keyword | Keterangan |
|---------|------------|
| __`pwd`__ | Melihat __Process Working Directory__ saat sekarang. |
| __`hostname`__ | Melihat hostname / computer name. |
| __`whoami`__ | Menampilkan user ID dan nama user pengguna. |
| __`who`__ | Menampilkan informasi user yang telah login. |
| __`id`__ | Menampilkan informasi user dan group. |
| __`fg`__ | (*__Foreground__*), melihat daftar program yang sedang berjalan (__suspended__). |
| __`top`__ | Melihat informasi aplikasi yang sedang berjalan (__Task Manager CLI__). |


### 1.2. Perintah Dasar

| Keyword | Keterangan |
|---------|------------|
| __`ls`__ | Melihat daftar isi suatu directory. |
| __`mkdir`__ | Membuat directory atau folder. |
| __`touch`__ | Membuat file. |
| __`cp`__ | Menggandakan atau menyalin file dan directory |
| __`mv`__ | Melakukan perubahan nama file atau memindahkan file ke ke lokasi yang berbeda |
| __`rm`__ | Menghapus file atau folder (`-d`). |
| __`rmdir`__ | Menghapus directory atau folder. |
| __`cat`__ | Menggabungkan data files dan menampilkannya pada standard output. |
| __`ping`__ | Memanggil IP Address atau hostname server. |
| __`which`__ | Menampilkan lokasi file executable (bin). |
| __`grep`__ | Menemukan file atau standard input berdasarkan PATTERN. Default RegEx (BRE). |
| __`sudo`__ | Mengeksekusi perintah sebagai user lain. |
| __`kill`__ | Menghentikan program yang sedang bekerja (`background process`). |


## 2. Keyboard & Shortcut

| Key            | Keterangan         |
|:--------------:|--------------------|
| :arrow_up:     | melihat history perintah yang di akses sebelumnya |
| :arrow_down:   | `redo` melihat history perintah yang di akses sebelumnya |
| `|` (pipeline) | memisahkan perintah perintah untuk dikombinasikan dengan program lainnya |
| `~` (tilde)    | alias dari /home/<username> |
| `ctrl + c`     | membatalkan proses yang sedang berjalan |
| `ctrl + d`     | Mengirim pesan EOF (End of File) kepada proses yang sedang berlangsung |
| `ctrl + z`     | melakukan suspend proses yangg sedang berjalan |


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
