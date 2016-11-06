# Permissions

> Manajemen file system permission


## File System Permissions

Permissions merupakan authentication (otorisasi) suatu file & directory yang diberi batasan-batasan tertentu.


## Menampilkan Permissions

__Cara menampilkan permission__

``` bash
$ ls -al <path>
# atau
$ ls -l <path>
```

__Contoh Output__

``` bash
# > ...
drwxr-xr-x   3 guntur guntur 4,0K Sep 16 23:16 Desktop
drwxr-xr-x   6 guntur guntur 4,0K Okt 21 23:10 Documents
-rw-------   1 guntur guntur 4,3K Okt 22 00:03 .bash_history
-rw-r--r--   1 guntur guntur  220 Agu 25 18:42 .bash_logout
lrwxrwxrwx   1 guntur guntur   35 Okt  8 09:18 .bash_profile -> /home/guntur/.dotfiles/bash_profile
# > ...
```

## Scheme

![sample](http://i.imgur.com/OzXZ6.png)

__Pengelompokan__

| -/l/d | rwx | rwx | rwx |
|---|-----|-----|-----|
| Tipe File | Owner/User | Group | Other |

__Basic__

| Huruf | Angka | Keterangan |
|:-----:|:-----:|------------|
| __r__ |   4   | Read Only  |
| __w__ |   2   | Write      |
| __x__ |   1   | Execute    |

__Kombinasi Angka__

| --x | -w- | -wx | r-- | r-x | rw- | rwx |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1   | 2   | 3   | 4   | 5   | 6   | 7   |

__Contoh 1__

![fs-permissions.jpg](https://s15.postimg.org/4grarvxy3/fs_permissions.jpg)

| -rw-r--r-- | -rwxr-xr-x | -rwxrwxrwx |
| :--------: | :--------: | :--------: |
| 644        | 755        | 777        |
