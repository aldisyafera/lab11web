# lab11web

Nama : Aldi Syafera

Kelas : TI.20.D.1

NIM : 312010008

Langkah-langkah Praktikum:

1. Membuat folder lab11_php_ci

![image](https://user-images.githubusercontent.com/103243638/172711621-d0ae3882-3248-43b4-9e33-8f7fb0c63cd2.png)

2.Sebelum memulai menggunakan Framework Codeigniter, perlu dilakukan konfigurasi pada webserver. Beberapa ekstensi PHP perlu diaktifkan untuk kebutuhan pengembangan Codeigniter 4. Berikut beberapa ekstensi yang perlu diaktifkan: • php-json ekstension untuk bekerja dengan JSON; • php-mysqlnd native driver untuk MySQL; • php-xml ekstension untuk bekerja dengan XML; • php-intl ekstensi untuk membuat aplikasi multibahasa; • libcurl (opsional), jika ingin pakai Curl. Untuk mengaktifkan ekstentsi tersebut, melalu XAMPP Control Panel, pada bagian Apache klik Config -> PHP.ini

![image](https://user-images.githubusercontent.com/103243638/172711726-67626376-bdd0-4e1b-9c21-399ce8b04cc1.png)

Pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan diaktifkan. Kemudian simpan kembali filenya dan restart Apache web server.

![image](https://user-images.githubusercontent.com/103243638/172711787-695b0e21-1e70-4e80-b01f-796c512e32e4.png)

3.Instalasi Codeigniter 4 Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara manual. • Unduh Codeigniter dari website https://codeigniter.com/download • Extrak file zip Codeigniter ke direktori htdocs/lab11_ci. • Ubah nama direktory framework-4.x.xx menjadi ci4. • Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/

![image](https://user-images.githubusercontent.com/103243638/172711909-486af7ca-5b16-4a80-a192-1d7aaa6055f1.png)

4.Menjalankan CLI (Command Line Interface) Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk mengakses CLI buka terminal/command prompt. Kemudian arahkan lokasi direktori sesuai dengan direktori kerja project dibuat (xampp/htdocs/lab11_ci/ci4/)

![image](https://user-images.githubusercontent.com/103243638/172712011-2053e1f4-b262-49d5-8666-555c1221cc51.png)

Perintah yang dapat dijalankan untuk memanggil CLI Codeigniter adalah:

![image](https://user-images.githubusercontent.com/103243638/172712066-82bcda35-6988-4908-9904-8c08e0e3159a.png)

5.Mengaktifkan Mode Debugging Codeigniter 4 menyediakan fitur debugging untuk memudahkan developer untuk mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program. Secara default fitur ini belum aktif. Ketika terjadi error pada aplikasi akan ditampilkan pesan kesalahan seperti berikut.

![image](https://user-images.githubusercontent.com/103243638/172712179-7b817869-7420-4afd-947a-385933fa3deb.png)

Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis errornya, maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi pada environment variable CI_ENVIRINMENT menjadi development. Ubah nama file env menjadi .env kemudian buka file tersebut dan ubah nilai variable CI_ENVIRINMENT menjadi development.

![image](https://user-images.githubusercontent.com/103243638/172712255-3d25e57c-a231-440b-9046-a7fc01921bd9.png)

Contoh eror Untuk mencoba error tersebut, ubah kode pada file app/Controller/Home.php hilangkan titik koma pada akhir kode.

![image](https://user-images.githubusercontent.com/103243638/172712341-cb36eb89-eb30-4f10-8426-e43ffa585bca.png)

![image](https://user-images.githubusercontent.com/103243638/172712360-f34e55e1-f271-4943-bdb8-b75ef88ff954.png)

7.Membuat route baru dalam Routes.php Tambahkan kode berikut ini pada Routes.php

![image](https://user-images.githubusercontent.com/103243638/172712424-e5c6e5c4-22b1-4f11-931b-d183fc5ba102.png)

![image](https://user-images.githubusercontent.com/103243638/172712475-52a07edd-bb7d-46d6-9de4-8537653c70b9.png)

Selanjutnya coba akses route yang telah dibuat dengan mengakses alamat url http://localhost:8080/about seperti berikut. Maka hasilnya akan terjadi error, yang artinya file/page tersebut tidak ada. Untuk dapat mengakses halaman tersebut, harus dibuat terlebih dahulu Contoller yang sesuai dengan routing yang dibuat yaitu Contoller Page.

![image](https://user-images.githubusercontent.com/103243638/172712616-73d19316-e7dd-47e1-ab9e-bd3091162b5b.png)

8.Membuat Controller Kemudian membuat Controller Page. Buat file baru dengan nama page.php pada direktori Controller kemudian isi kodenya seperti berikut.

![image](https://user-images.githubusercontent.com/103243638/172712717-f75b9de8-5ca7-4269-ad54-144359c432cd.png)

Selanjutnya refresh Kembali browser, maka akan ditampilkan hasilnya yaotu halaman sudah dapat diakses.

![image](https://user-images.githubusercontent.com/103243638/172712774-146f5222-e16a-48d5-a357-3dc1de39c82f.png)

9.Auto Routing Secara default fitur autoroute pada Codeiginiter sudah aktif. Untuk mengubah status autoroute dapat mengubah nilai variabelnya. Untuk menonaktifkan ubah nilai true menjadi false.

![image](https://user-images.githubusercontent.com/103243638/172712842-56b4fced-5a0b-4c88-ad99-8fed206365ab.png)

Method ini belum ada pada routing, sehingga cara mengaksesnya dengan menggunakan alamat: http://localhost:8080/page/tos

![image](https://user-images.githubusercontent.com/103243638/172712970-57bd18a5-0b84-4e48-a7ff-6265c7bd03f9.png)

10.Membuat View Selanjutnya adalam membuat view untuk tampilan web agar lebih menarik. Buat file baru dengan nama about.php pada direktori view (app/view/about.php) kemudian isi kodenya seperti berikut.

![image](https://user-images.githubusercontent.com/103243638/172713038-a7083a95-3cf9-406e-b17d-acebcc4ffdd8.png)

Ubah method about pada class Controller Page menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/103243638/172713085-c267829b-3ee2-4e91-b126-d264fc67293e.png)

Kemudian lakukan refresh pada halaman tersebut.

![image](https://user-images.githubusercontent.com/103243638/172713163-c5d55dbb-87e1-4127-912e-732e1038fd84.png)

11.Membuat Layout Web dengan CSS Pada dasarnya layout web dengan css dapat diimplamentasikan dengan mudah pada codeigniter. Yang perlu diketahui adalah, pada Codeigniter 4 file yang menyimpan asset css dan javascript terletak pada direktori public. Buat file css pada direktori public dengan nama style.css (copy file dari praktikum lab4_layout. Kita akan gunakan layout yang pernah dibuat pada praktikum 4.

![image](https://user-images.githubusercontent.com/103243638/172713266-3efca2de-b8e8-43dc-b6b6-e9a2b4dc47fa.png)

Kemudian buat folder template pada direktori view kemudian buat file header.php dan footer.php

File app/view/template/header.php

![image](https://user-images.githubusercontent.com/103243638/172713351-6bca4d95-b2f0-4892-a762-4952a5b36144.png)

File app/view/template/footer.php

![image](https://user-images.githubusercontent.com/103243638/172713702-a5d6ca2c-25b2-43ea-8160-520117e9b6ff.png)

File app/view/template/about.php

![image](https://user-images.githubusercontent.com/103243638/172713744-3b109605-8444-4c52-b2b3-e22fae4c72fd.png)

Selanjutnya refresh tampilan pada alamat http://localhost:8080/about











































