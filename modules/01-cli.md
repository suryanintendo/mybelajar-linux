# Command Line Interface (CLI)

> Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod


## 1. Perintah Dasar Terminal

### 1.1. Perintah Informasi

| Keyword        | Keterangan                                                                       |
|----------------|----------------------------------------------------------------------------------|
| __`pwd`__      | Melihat __Process Working Directory__ saat sekarang.                             |
| __`hostname`__ | Melihat hostname / computer name.                                                |
| __`whoami`__   | Menampilkan user ID dan nama user pengguna.                                      |
| __`who`__      | Menampilkan informasi user yang telah login.                                     |
| __`id`__       | Menampilkan informasi user dan group.                                            |
| __`fg`__       | (*__Foreground__*), melihat daftar program yang sedang berjalan (__suspended__). |
| __`top`__      | Melihat informasi aplikasi yang sedang berjalan (__Task Manager CLI__).          |

<!-- - __`last`__ - Lorem ipsum dolor sit amet. -->
<!-- - __`ps`__ - Lorem ipsum dolor sit amet. -->
<!-- - __`df`__ - Lorem ipsum dolor sit amet. -->
<!-- - __`du`__ - Lorem ipsum dolor sit amet. -->

### 1.2. Perintah Dasar

| Keyword     | Keterangan                                                                    |
|-------------|-------------------------------------------------------------------------------|
| __`ls`__    | Melihat daftar isi suatu directory.                                           |
| __`mkdir`__ | Membuat directory atau folder.                                                |
| __`touch`__ | Membuat file.                                                                 |
| __`cp`__    | Menggandakan atau menyalin file dan directory                                 |
| __`mv`__    | Melakukan perubahan nama file atau memindahkan file ke ke lokasi yang berbeda |
| __`rm`__    | Menghapus file atau folder (`-d`).                                            |
| __`rmdir`__ | Menghapus directory atau folder.                                              |
| __`cat`__   | Menggabungkan data files dan menampilkannya pada standard output.             |
| __`ping`__  | Memanggil IP Address atau hostname server.                                    |
| __`which`__ | Menampilkan lokasi file executable (bin).                                     |
| __`grep`__  | Menemukan file atau standard input berdasarkan PATTERN. Default RegEx (BRE).  |
| __`sudo`__  | Mengeksekusi perintah sebagai user lain.                                      |
| __`kill`__  | Menghentikan program yang sedang bekerja (`background process`).              |


## 2. Keyboard & Shortcut

| Key            | Keterangan         |
|:--------------:|--------------------|
| :arrow_up:     | Lorem ipsum dolor. |
| :arrow_down:   | Lorem ipsum dolor. |
| `|` (pipeline) | Lorem ipsum dolor. |
| `~` (tilde)    | Lorem ipsum dolor. |
| `ctrl + c`     | Lorem ipsum dolor. |
| `ctrl + d`     | Lorem ipsum dolor. |
| `ctrl + z`     | Lorem ipsum dolor. |


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

| Path         | Deskripsi                                             |
|--------------|-------------------------------------------------------|
| __/__        | directory root                                        |
| __/etc__     | directory _etc_ yang berada di dalam _root_ directory |
| __/etc/apt__ | directory _apt_ yang berada di dalam _etc_ directory  |


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
