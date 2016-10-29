# User & Group

> Manajemen User & Group pada DISTRO LINUX (Ubuntu 14.04)


## User

__User__ atau __owner__ adalah pengguna yang terdaftar pada sistem operasi yang kita gunakan.

- ### Menambahkan user

    __Syntax__
    ``` bash
    $ sudo adduser [nama]
    ```

    __Contoh__
    ``` bash
    $ sudo adduser excel
    ```

    Jika ada permintaan password, selanjutnya ketikkan __(`input`)__ password anda yang sesuai.

- ### Memberikan atau mengubah password user

    __Syntax__
    ``` bash
    $ sudo passwd [options] [namauser]
    ```

    __Contoh__
    ``` bash
    $ sudo passwd excel
    ```

    Masukkanlah __(`input`)__ password baru untuk user yang anda tujukan.

- ### Menghapus user

    __Syntax__
    ``` bash
    $ sudo userdel [options] [nama]
    ```

    __Contoh__
    ``` bash
    $ sudo userdel excel
    ```

## Group

Group adalah kelompok dari kumpulan dari beberapa user yang terdaftar didalamnya.

- ### Menambahkan group

    __Syntax__
    ``` bash
    $ sudo groupadd [options] [namagroup]
    ```

    __Contoh__
    ``` bash
    $ sudo groupadd marketing
    ```

- ### Mendaftarkan user ke dalam group

    __Syntax__
    ``` bash
    $ sudo gpasswd [namauser] [namagroup]
    ```

    __Contoh__
    ``` bash
    $ sudo gpasswd -a excel marketing
    ```

- ### Menghapus group

    __Syntax__
    ``` bash
    $ sudo groupdel [options] [namagroup]
    ```

    __Contoh__
    ``` bash
    $ sudo groupdel marketing
    ```


## Options

__Syntax__
``` bash
$ sudo [nama-perintah] --help
```

__Contoh__
``` bash
$ sudo gpasswd --help
```
