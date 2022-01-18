+++
date = 2022-01-01T14:00:00Z
title = "Pertemuan Tgl 16 Januari 2022"

+++
### Mendapatkan input di PHP

PHP CLI merupakan PHP yang berjalan di atas _Command Line_. Biasanya, program yang berbasis teks memiliki fungsi tersendiri untuk mengambil input. Contohnya Python menggunakan fungsi **`input()`** dan **`raw_input()`**, java menggunakan **`Scanner`** dan **`BufferReader`**, C++ menggunakan **`cin`**, Pascal menggunakan **`readln()`**, dsb. Lalu, Bagaiaman dengan PHP?

**Menggunakan STDIN**

cara sederhana untuk mendapatkan input dari user ialah melalui CLI (Command Line), yaitu menggunakan **`STDIN,`** gunakan fungsi **`trim()`** untuk membersihkannya dari “**`\n`**”. Contoh:


```
<?php

echo "Siapa nama kamu: ";
$nama = trim(fgets(STDIN));
echo "Hello $nama, apa kabar?\\n";
?>
```

Buka Terminal atau shell

lalu ketikan

    > php nama_file.php

dan hasilnya akan seperti ini :

>     PS C:\xampp\htdocs> php .\input.php
>     
>     Siapa nama kamu: Herman
>     
>     Hello Herman, apa kabar?

**Study Kasus**

_membuat aplikasi pembayaran menggunakan STDIN dan Control Flow IF ELSE_

![](/uploads/aplikasi-pembayaran-drawio.png)

Code :

    <?php
    echo "========== Aplikasi Pembayaran =========== \n";
    echo "Masukan total belanja anda : ";
    $total_belanja = trim(fgets(STDIN));
    if ($total_belanja > 100000) {
    echo "Selamat anda mendapatkan hadiah..!";
    } else {
    echo "Terimakasi anda telah berbelanja di toko kami!";
    }
    ?>

Hasilnya akan seperti ini :

>     PS C:\xampp\htdocs> php .\aplikasi_pembayaran.php
>     ========== Aplikasi Pembayaran ===========
>     Masukan total belanja anda : 300000
>     Selamat anda mendapatkan hadiah..!
>     PS C:\xampp\htdocs>