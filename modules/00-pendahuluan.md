# Welcome Linux

> __SELAMAT DATANG BELAJAR LINUX__


## Pengantar

Sebelum kita memulai belajar __LINUX__, ada baiknya kita mengenali beberapa istilah-istilah yang sering muncul dalam lingkungan __*NIX__.

:open_mouth: Lho, apa maksudnya __*NIX__? Ok. Lets get started.


<hr>

## Istilah Umum

- ### *NIX

    Istilah ini akan sering kita jumpai ketika berbicara sistem operasi yang memiliki arsitektur __UNIX__. __Linux__ (__GNU/Linux__) adalah salah satu sistem operasi yang berada pada lingkungan __UNIX__.

    Beberapa contoh yang lain dan cukup populer diantaranya adalah __MAC OS X__ keluaran __Apple__, yang juga merupakan OS yang dibangun pada arsitektur __UNIX__.

    Lihat beberapa jenis [__UNIX__](https://id.wikipedia.org/wiki/Unix#Jenis-jenis_UNIX) yang lainnya.
    <br>


- ### Open Source

    *__Sumber Terbuka__*. Ini memungkinkan pengguna sebuah program / aplikasi dapat melihat sumber kode dari aplikasi yang sedang digunakannya.

    :confused: Apa tujuan dan manfaat dari program __open source__?

    - Memungkinkan penggunanya memahami cara kerja program tersebut.
    - Memungkinkan penggunanya dapat mengembangkan program tersebut menjadi lebih baik.

    __GNU/Linux__ merupakan sebuah project program (__open source__), artinya seorang pengguna __LINUX__ diberi hak kebebasan untuk mengembangkan, memodifikasi *__source code__* dari program yang digunakannya.

    Tidak hanya sampai batasan itu, seseorang yang telah mengembangkan program __open source__ dapat mendistribusikan kembali program tersebut. Yang perlu dipahami ketika kita mendistribusikan kembali sebuah program yang __open source__, kita diperbolehkan mendistribusikannya kembali sebagai sebuah project __open source__ atau komersil.


- ### GNU/GPL

    [__GNU__](https://id.wikipedia.org/wiki/GNU) __General Public License__ (GNU/GPL) merupakan lisensi dari sebuah perangkat lunak yang paling banyak digunakan. Perangkat lunak dengan lisensi __GNU/GPL__ menjamin pengguna akhir, baik individu, organisasi, ataupun perusahaan, memiliki kebebasan untuk menggunakan, mempelajari, berbagi (menyalin), dan mengembangkan perangkat lunak tersebut.


- ### Distributions

    Distribusi atau biasanya juga disebut [__Distro Linux__](https://id.wikipedia.org/wiki/Distribusi_Linux) adalah istilah untuk sistem operasi komputer dan aplikasinya yang masih merupakan keluarga __UNIX__ dan menggunakan kernel Linux.

    Ada banyak distribusi atau distro Linux yang telah muncul. Beberapa bertahan dan menjadi distro besar, bahkan sampai menghasilkan distro turunan, contohnya distro Debian GNU/Linux. Distro ini telah menghasilkan puluhan distro turunan, antara lain Ubuntu, Knoppix, Xandros, DSL, dan sebagainya.

    | Distribusi Debian |
    |:-----------------:|
    |![Debian Tree](https://upload.wikimedia.org/wikipedia/commons/d/d8/Debian_family_tree_11-06.png)|
    |*sumber: `wikipedia`*|


<hr>


## Istilah Teknis

- ### Repository

    Sebuah repository perangkat lunak merupakan lokasi penyimpanan dari paket perangkat lunak yang dapat diambil dan digunakan. Contohnya adalah seperti software teks editor.

    Ada banyak sekali software yang bisa kita dapatkan baik secara offline ataupun online (internet), tetap dalam hal ini repository memudahkan kita untuk melakukan instalasi program yang kita inginkan.

    :open_mouth: Mengapa harus ada repository?

    - Update (Pembaharuan)
    - Keamanan (Security)

    Pengguna __GNU/LINUX__, sangat dianjurkan agar terhubung dengan internet agar dapat melakukan update repository, perangkat lunak, meningkatkan sistem keamanan dan sebagainya.


- ### CLI

    Command Line Interface (__CLI__), adalah program berbasis teks untuk mengeksekusi program-program yang tersedia pada unit komputer.

    Pada lingkungan __UNIX__, software ini dikenal dengan nama __terminal__ yang secara default telah terintegrasi (*terinstall*). Masih ada lagi program-program lainnya yang semacam ini, sebut saja __UXTerm__ dan __XTerm__.

    Tidak sama seperti program yang berada pada keluarga __Windows__ keluaran __Microsoft__, program seperti ini dikenal dengan nama __command prompt__ dan __PowerShell__.

    Setiap (__CLI__) memiliki cara kerja yang berbeda dan interpretasi yang berbeda pula. Tetapi, secara umum tidak mengubah fungsi-fungsi dasar.


- ### Root

    Root (__[ / ]__, *__Akar__*), adalah istilah directory utama sistem operasi berbasis __UNIX__.


- ### Super User

    Merupakan __User__ yang memiliki otorisasi tertinggi untuk setiap directory dan file yang berada pada __file system, kernel, dll__.

    Maksudnya adalah ketika user akan menginstall sebuah perangkat lunak baru atau melakukan perubahan __Repository__, secara default user yang bukan __Super User__ tidak akan bisa mengeksekusi perintah tersebut.

    Agar dapat mengeksekusi perintah tersebut, pengguna harus mengeksekusi perintah tersebut pada mode (sebagai) __Super User__.


- ### Sudo

    __`sudo`__ merupakan keyword (kata kunci) perintah untuk mengubah mode level otorisasi (sebagai) __super user__ atau __user lainnya__.

    Setiap penggunaan kata kunci (__`sudo`__), pengguna akan diminta untuk mengetikan kata sandi (*password*) sebelum mengeksekusi sebuah program atau melakukan perubahan data.


- ### Permissions

    Permissions (*__Hak Akses__*), merupakan otorisasi pada file dan directory.

    | Huruf | Angka | Keterangan |
    |:-----:|:-----:|------------|
    | __r__ |   4   | Read Only  |
    | __w__ |   2   | Write      |
    | __x__ |   1   | Execute    |
