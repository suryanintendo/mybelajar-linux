# Repository

> Repository dan Aplikasi


## Daftar Konten

- [Ilustrasi](#ilustrasi)
- [Menambahkan Repository](#menambahkan-repository)
- [Instalasi Aplikasi Melalui Repository](#instalasi-aplikasi-melalui-repository)
- [Memperbaharui Repository](#memperbaharui-repository)
- [Menghapus Repository](#menghapus-repository)
- [Menghapus Aplikasi](#menghapus-aplikasi)

### Ilustrasi


### Menambahkan Repository

- #### Syntax CLI

    ``` bash
    $ sudo add-apt-repository ppa:[vendor/repo-name]
    ```

- #### Implementasi

    Contoh menambahkan repository Java 8.

    ``` bash
    $ sudo add-apt-repository ppa:webup8team/java
    ```

    Setelah menambahkan repository, selanjutnya melakukan update cache repository __DISTRO__ kita.

    ``` bash
    $ sudo apt-get update
    ```


### Instalasi Aplikasi Melalui Repository

- #### Syntax CLI

    ``` bash
    $ sudo apt-get install [app-name]
    ```

- #### Implementasi

    Contoh menginstall aplikasi Java 8 setelah mendaftarkan / menambahkan repository dari vendor __`webup8team`__

    ``` bash
    $ sudo apt-get install java
    ```

### Memperbaharui Repository dan Aplikasi

- #### Update Caches Repository

    ``` bash
    $ sudo apt-get update
    ```

- #### Upgrade Dependencies & Aplikasi

    ``` bash
    $ sudo apt-get upgrade
    ```

### Menghapus Repository

- #### Syntax CLI

    ``` bash
    $ sudo add-apt-repository rm ppa:[vendor/repo-name]
    ```

- #### Implementasi

    ``` bash
    $ sudo add-apt-repository rm ppa:webup8team/java
    ```

### Menghapus Aplikasi

- #### Syntax CLI

    ``` bash
    $ sudo apt-get remove [app-name]
    ```

- #### Implementasi

    ``` bash
    $ sudo apt-get remove java
    ```

    __Optimasi__

    ``` bash
    $ sudo apt-get purge
    ```
