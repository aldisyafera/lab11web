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

Membuat Database

![image](https://user-images.githubusercontent.com/103243638/173825083-de514a2b-d74f-46ec-b835-f8126b14d009.png)

Membuat Tabel

![image](https://user-images.githubusercontent.com/103243638/173825157-4a0b159c-1289-4cbc-8a33-b879939e2fb7.png)

Konfigurasi koneksi 

database Selanjutnya membuat konfigurasi untuk menghubungkan dengan database server. Konfigurasi dapat dilakukan dengan du acara, yaitu pada file app/config/database.php atau menggunakan file .env. Pada praktikum ini kita gunakan konfigurasi pada file .env

![image](https://user-images.githubusercontent.com/103243638/173825248-60ef4762-6d04-4321-9d1c-ff217b8d2777.png)

Membuat Model 

Selanjutnya adalah membuat Model untuk memproses data Artikel. Buat file baru pada direktori app/Models dengan nama ArtikelModel.php

![image](https://user-images.githubusercontent.com/103243638/173825319-9ef58efb-f8ef-4ede-ac1d-2096a0d49e94.png)

Membuat Controller 

Buat Controller baru dengan nama Artikel.php pada direktori app/Controllers.

![image](https://user-images.githubusercontent.com/103243638/173825427-98564568-20b3-410c-9160-5147c58b6e5d.png)

Membuat View

 Buat direktori baru dengan nama artikel pada direktori app/views, kemudian buat file baru dengan nama index.php.

![image](https://user-images.githubusercontent.com/103243638/173825529-a55dad17-16a4-4c6e-b2b2-02c143627062.png)

•	Selanjutnya buka browser kembali, dengan mengakses url http://localhost:8080/artikel

![image](https://user-images.githubusercontent.com/103243638/173825584-7a79fca5-27d2-41b5-b44d-551845ab8a33.png)

![image](https://user-images.githubusercontent.com/103243638/173825690-2eaa7849-7f56-4d05-8fca-eae75470a6b3.png)

Membuat Menu Admin

Menu admin adalah untuk proses CRUD data artikel. Buat method baru pada Controller Artikel dengan nama admin_index().

![image](https://user-images.githubusercontent.com/103243638/173825789-2da71877-54b0-4ada-a4c2-ba55c8c9eb78.png)

Selanjutnya buat view untuk tampilan admin dengan nama admin_index.php

![image](https://user-images.githubusercontent.com/103243638/173825883-8264a3f5-ba49-41d9-81ea-930819d1274b.png)

![image](https://user-images.githubusercontent.com/103243638/173825931-fc7f0aa4-e98a-4e87-a104-510e051ea1fd.png)

Tambahkan routing untuk menu admin seperti berikut:

![image](https://user-images.githubusercontent.com/103243638/173826031-eff6c1ef-9271-461b-8a83-1a46d01f0950.png)

Akses menu admin dengan url http://localhost:8080/admin/artikel

![image](https://user-images.githubusercontent.com/103243638/173826156-48eb11e4-33bb-494a-9747-92cb11d88a69.png)

Menambah Data Artikel 

Tambahkan fungsi/method baru pada Controller Artikel dengan nama add().

![image](https://user-images.githubusercontent.com/103243638/173826328-04d7e555-a458-48a2-bbe8-974ec90edc15.png)

Mengubah Data 

Tambahkan fungsi/method baru pada Controller Artikel dengan nama edit().

![image](https://user-images.githubusercontent.com/103243638/173826465-9c40a4b5-0b67-481f-a03e-56130a259e38.png)

![image](https://user-images.githubusercontent.com/103243638/173826483-aa0d4d93-c60d-4f7b-aa5c-2a8c763c39d7.png)

Menghapus Data 

Tambahkan fungsi/method baru pada Controller Artikel dengan nama delete()

![image](https://user-images.githubusercontent.com/103243638/173826568-63d24b6a-99e4-4f40-b6d1-a1972ac29df7.png)

Pagination merupakan proses yang digunakan untuk membatasi tampilan yang panjang
dari data yang banyak pada sebuah website. Fungsi pagination adalah memecah
tampilan menjadi beberapa halaman tergantung banyaknya data yang akan ditampilkan
pada setiap halaman.

Pada Codeigniter 4, fungsi pagination sudah tersedia pada Library sehingga cukup
mudah menggunakannya.

Untuk membuat pagination, buka Kembali Controller Artikel, kemudian modifikasi
kode pada method admin_index seperti berikut.

![image](https://user-images.githubusercontent.com/103243638/176436507-46e15fa5-5674-4434-90c6-6ee98a199e00.png)


Kemudian buka file views/artikel/admin_index.php dan tambahkan kode berikut
dibawah deklarasi tabel data.

![image](https://user-images.githubusercontent.com/103243638/176436837-8ecd706c-e4c7-49f4-b28e-2482f372ca27.png)


Selanjutnya buka kembali menu daftar artikel, tambahkan data lagi untuk melihat
hasilnya.

![image](https://user-images.githubusercontent.com/103243638/176436936-8fd32317-2b50-438b-99ca-58cc78edce7d.png)


Membuat Pencarian
Pencarian data digunakan untuk memfilter data.

Untuk membuat pencarian data, buka kembali Controller Artikel, pada method
admin_index ubah kodenya seperti berikut

![image](https://user-images.githubusercontent.com/103243638/176437358-524fff30-bab5-47e2-bae1-f9bc4c6367b9.png)


Kemudian buka kembali file views/artikel/admin_index.php dan tambahkan form
pencarian sebelum deklarasi tabel seperti berikut:

![image](https://user-images.githubusercontent.com/103243638/176437971-bbf473d2-686a-4266-97e7-a0a9811f2b92.png)


Dan pada link pager ubah seperti berikut.

![image](https://user-images.githubusercontent.com/103243638/176438395-c3b74b4f-b9e3-4809-95ac-e20ce192e02b.png)


Selanjutnya ujicoba dengan membuka kembali halaman admin artikel, masukkan kata
kunci tertentu pada form pencarian.

![image](https://user-images.githubusercontent.com/103243638/176438563-4d6ef84c-a52e-4187-aec2-979f21c39558.png)

Upload Gambar
Menambahkan fungsi unggah gambar pada tambah artikel. Buka kembali Controller
Artikel, sesuaikan kode pada method add seperti berikut:

![image](https://user-images.githubusercontent.com/103243638/176439437-033d660c-3133-4204-955e-c534b81c89a0.png)


Upload Gambar
Menambahkan fungsi unggah gambar pada tambah artikel. Buka kembali Controller
Artikel, sesuaikan kode pada method add seperti berikut:

![image](https://user-images.githubusercontent.com/103243638/176439946-958530e0-1e0e-430a-b602-5bfb57923170.png)


Kemudian pada file views/artikel/form_add.php tambahkan field input file seperti
berikut.


![image](https://user-images.githubusercontent.com/103243638/176439946-958530e0-1e0e-430a-b602-5bfb57923170.png)

Dan sesuaikan tag form dengan menambahkan ecrypt type seperti berikut.

![image](https://user-images.githubusercontent.com/103243638/176440181-a5ec2a02-d383-446b-bc7c-aea295ccea36.png)

Ujicoba file upload dengan mengakses menu tambah artikel.

![image](https://user-images.githubusercontent.com/103243638/176441498-61f34f8e-100f-4d66-9045-a5c692b66dbd.png)



























