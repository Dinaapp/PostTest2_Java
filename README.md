Nama: Rizky Wahyu Dina Putri
NIM: 2409116111

Program Top Up Game adalah program CRUD yang mengelola daftar game beserta item Top Up. Pengguna dapat melihat daftar Game, mencari, menambahkan game baru, mengubah, dan menghapus data. Program juga dibuat menggunakan MVC dengan pemisahan packages agar lebih terstruktur dan sesuai dengan fungsi.

<img width="820" height="320" alt="image" src="https://github.com/user-attachments/assets/ae92dc26-5ef9-49cf-b722-7f6be87135ae" />

Pada MVC, program terbagi menjadi 3 packages.
1. Package model, menyimpan struktur data Game seperti atribut pada game dan constructor.
2. Package service, menyimpan logika proses CRUD dan fitur search.
3. Package main, sebagai entry poin atau menu interaksi untuk pengguna.



<img width="1914" height="1128" alt="image" src="https://github.com/user-attachments/assets/0779ae38-e42a-45e7-8f2b-6ed3e43fbbf9" />
<img width="1919" height="1122" alt="image" src="https://github.com/user-attachments/assets/74963294-21e2-49e6-b76a-72ea8bd883f9" />

Program Game pada packages model dibuat dengan menggunakan access modifier private untuk atribut/properti id, nama, dan top up, sehingga hanya bisa diakses melalui method getter dan setter. Constructor Game digunakan untuk menginialisasi objek Game dengan id dan nama, serta membuat ArrayList untuk list kosong item top up. Getter dan setter digunakan untuk memberikan akses terbatas terhadap atribut/properti. 

Method addTopUp digunakan untuk menambahkan item Top Up ke dalam game, namun apabila item yang diinputkan telah ada pada Arraylist maka akan ditolak (return false).

<img width="1919" height="1131" alt="image" src="https://github.com/user-attachments/assets/5417dafc-e7a8-4b49-84cb-004da8cc1be4" />

Pada bagian awal atribut daftarGame menyimpan seluruh data game dalam bentuk list. Atribut next id digunakan untuk memberikan nomor id otomatis (auto increment) saat pengguna menambahkan game baru, jadi tidak dibuat manual. Pada constructor, membuat data default yang disimpan di arraylist agar saat program pertama dijalankan, daftar game tidak kosong danmenampilkan game beserta item top up masing-masing.

<img width="1916" height="868" alt="image" src="https://github.com/user-attachments/assets/35d8b5e2-40cc-4daa-9502-541d9a7e3fef" />

Method tambahGame digunakan untuk menambahkan data game baru pada proses CRUD. Method ini mengecek terlbih dahulu apakah nama game yang diinputkan oleh pengguna sudah ada di dalam list atau belum, jika sudah maka gagal menambahkan game karena nama game sudah ada.

Method tambahTopUp digunakan untuk menambahkan item top up baru ke dalam game, termasuk ke game yang baru ditambahkan melalui input pengguna. Mmeiliki proses yang sama seperti tambahGame, jika item top up sudah tersedia maka gagal menambahkan karena item sudah tersedia.

<img width="1919" height="1044" alt="image" src="https://github.com/user-attachments/assets/2ebcf731-3dac-464f-b070-47cbe17aa1f0" />

Method updateGame digunakan untuk mengubah nama game yang ada di list, dengan menginput game sesuai id. Apabila id game seuai maka pengguna dapat memasukkan nama game baru. 

Method hapusGame digunakan untujk menghapus game berdasarkan id, jika data ditemukan, game akan dihapus dari list beserta item top upnya. 

Method cariGame mencari data berdasarkan kata kunci yaitu nama gamenya, pencarian game disetting dengan menggunakan toLowerCase()

<img width="1919" height="1122" alt="image" src="https://github.com/user-attachments/assets/c2c20041-4b15-4d45-9770-e641c0bdc103" />

Method ini digunakan untuk menampilkan seluruuh data game beserta item top up. Jika list game kosong, maka menampilkan belum ada game tersedia.

<img width="1919" height="695" alt="image" src="https://github.com/user-attachments/assets/74f82bc9-2768-4eb7-b7d4-e70a980a16e2" />

Pada bagian awal class main pada package main menggunakan impor gameservice dari package service untuk memanggil logika CRUD. import canner untuk membaca input dari pengguna dan variabel pilihan yang menyimpan input menu yang dipilih pengguna.

<img width="1918" height="628" alt="image" src="https://github.com/user-attachments/assets/375ffced-d21c-469b-96ad-0629ed0065b3" />

Program menampilkan menu utama pada proghram, validasi input menggunakan scanner.hasNextInt() agar input hanya berupa angka saja. 

<img width="1919" height="943" alt="image" src="https://github.com/user-attachments/assets/eba79699-dec8-4f3c-85a9-bf7e2789c768" />

<img width="1919" height="559" alt="image" src="https://github.com/user-attachments/assets/9ad12e56-7121-4c2f-bf45-b2380fd457ad" />

<img width="1917" height="927" alt="image" src="https://github.com/user-attachments/assets/a4a0925d-4df1-46a4-a33a-8192d458e93d" />

<img width="1919" height="923" alt="image" src="https://github.com/user-attachments/assets/cacf782e-daf6-415f-82cd-494b0295290a" />

<img width="1915" height="1118" alt="image" src="https://github.com/user-attachments/assets/796a4ab3-5520-4446-a8ef-ea7c023fa2e7" />

Menu dibuat menggunakan switch case, setiap case mewakili operasi CRUD.
1. read, menampilkan daftar game
2. search, mencari game berdasrkan kata kunci nama game
3. create, menambahkan game baru
4. create, menambahkan item top up baru
5. update, mengubah nama game
6. delete, menghapus nama game berdasarkan id
7. exit dan keluar dari program.

Program berjalan menggunakan loop do-while yang artinya akan terus menampilkan menu sampai pengguna memilih untuk keluar dari program.


RUN PROGRAM

<img width="1919" height="1128" alt="image" src="https://github.com/user-attachments/assets/13aa4df2-8aee-44f9-9e01-54a415db956a" />

<img width="1919" height="690" alt="image" src="https://github.com/user-attachments/assets/49612565-c12a-4657-9dce-ca87ce39e4c5" />

<img width="1919" height="564" alt="image" src="https://github.com/user-attachments/assets/901f8da7-3d15-4300-8876-21f6d754c6ce" />

<img width="1912" height="1018" alt="image" src="https://github.com/user-attachments/assets/b53b850c-daf9-4ccb-abf1-00ff2c5b955e" />

<img width="1919" height="731" alt="image" src="https://github.com/user-attachments/assets/7f938459-3d2c-46d0-b2e1-1f019ae1b078" />

<img width="1919" height="975" alt="image" src="https://github.com/user-attachments/assets/56f4ac39-5778-4f56-b6c5-968ff3259be7" />

Validasi Input

Digunakan agar saat pengguna memasukkan input yang tidak sesuai dengan program, maka akan menampilkan pesan seperti "input tidak diperbolehkan", "input harus angka". Apabila pengguna melakukan input seperti spasi, enter dengan input kosong, simbol yang tidak sesuai dengan program, dan huruf apabila memilih menu.

<img width="1919" height="692" alt="image" src="https://github.com/user-attachments/assets/d6566dc6-aa8a-40f4-bf65-8ef2c3537005" />

<img width="1919" height="838" alt="image" src="https://github.com/user-attachments/assets/04739132-72f0-44fc-8d24-a9ac7440fe79" />

<img width="1919" height="973" alt="image" src="https://github.com/user-attachments/assets/253b2b03-f18e-48d8-8bf4-c1d17a18e39f" />

<img width="1919" height="801" alt="image" src="https://github.com/user-attachments/assets/40494873-bd90-46c0-bf45-0e992a40382b" />















