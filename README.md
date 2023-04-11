# latihan1

## A. Tugas Praktikum
## B. Evaluasi dan Pertanyaan 

### A. Tugas Praktikum

1. Buat sebuah database dengan nama latihan2

CREATE DATABASE nama_database;

Contoh
![gamabar](image/create%20latihan2.png)

2. Buat sebuah tabel dengan nama biodata (nama, alamat) di dalam database latihan2!
Note: "Sebelum membuat sebuah tabel, pastikan anda sudah menggunakan sebuah database dengan perintah

USE nama_database

contoh
![gambar](image/USE%20database.png)
di bawah ini adalah perintah untuk membuat sebuah tabel

CREATE TABLE nama_tabel (
    nama_field1 tipe_data(ukuran),
    nama_filed2 tipe_data(ukuran),
    ...nama_fieldn tip_data(ukuran)
    );

contoh
![gambar](image/CREATE%20TABLE%20biodata.png)

3. Tambahkan sebuah kolom keterangan (varchar 15), sebagai kolom terakhir!
Tidak ada tambahan query apapun karna jika memasukan query menambahkan kolom seperti biasa otomatis posisi kolom tersebut akan berada dipaling akhir. Berikut ini adalah query untuk menambahkan sebuah kolom pada kolom terakhir

ALTER TABLE nama_tabel ADD COLUMN nama_field tipe_data(ukuran);

contoh
![gambar](image/add%20keterangan.png)

4. Tambahkan kolom id (int 11) di awal (sebagai kolom pertama)! Ada sedikit tambahan query pada saat ingin meletakan kolom baru di awal yakni dengan menambahkan FIRST, berikut adalah querynya:

ALTER TABLE nama_tabel ADD COLUMN nama_field tipe_data FIRST;

contoh
![gambar](image/add%20id.png)

5. Sisipkan sebuah kolom dengan nama phone (varchar 15) setelah kolom alamat!
Jika ingin menambahkan sebuah kolom di antara kolom lain seperti sesudah dan sebelum kolom yang ingin diletakan, maka gunakan query tambahan yakni AFTER. Berikut adalah querynya,

ALTER TABLE nama_tabel ADD COLUMN nama_field tipe_data(ukuran) AFTER nama_field_tujuan;

contoh:
![gambar](image/add%20phone.png)

6. Ubah tipe data kolom id menjadi char(11)
Untuk mengubah tipe data pada kolom maka gunakan perintah sebagai berikut:

ALTER TABLE nama_tabel MODIFY COLUMN nama_field tipe_data_baru(ukuran);
bisa gunakan COLUMN atau tanpa menggunakan COLUMN
ALTER TABLE nama_tabel MODIFY id nama_field tipe_data_baru(ukuran);

contoh:
![gambar](image/MODIFY%20id.png)

7. Ubah nama kolom phone menjadi hp (varchar 20)!
Untuk mengubah kolom pada sebuah tabel gunakan query sebagai berikut:

ALTER TABLE nama_tabel CHANGE COLUMN nama_field_lama nama_field_baru tipe_data_lama(ukuran);
bisa gunakan COLUMN atau tanpa COLUMN
ALTER TABLE nama_tabel CHANGE nama_field_lama nama_field_baru tipe_data_lama(ukuran);

contoh:
![gambar](image/MODIFY%20phone%20to%20hp.png)

8. Tambahkan kolom email setelah kolom hp
Untuk Menambahkan kolom pada sebuah kolom setelah kolom yang ditentukan maka gunakan perintah AFTER berikut adalah querynya:

ALTER TABLE nama_tabel ADD COLUMN nama_field AFTER nama_field_tujuan;
bisa gunakan COLUMN atau tanpa menggunakan COLUMN
ALTER TABLE nama_tabel ADD nama_field AFTER nama_field_tujuan;

contoh:
![gambar](image/add%20email.png)

9. Hapus kolom keterangan dari tabel! Untuk menghapus kolom pada sebuah kolom yang ditentukan maka gunakan perintah berikut adalah querynya:

ALTER TABLE nama_tabel DROP COLUMN nama_field;
bisa gunakan COLUMN atau tanpa menggunakan COLUMN
ALTER TABLE nama_tabel DROP nama_field;

contoh:
![gambar](image/DROP%20keterangan.png)

10. Ganti nama tabel menjadi data_mahasiswa!
Untuk menganti nama pada subah tabel maka gunakan perintah berikut adalah querynya:

ALTER TABLE nama_tabel RENAME nama_tabel_baru;

contoh:
![gambar](image/RENAME%20TABLE%20biodata.png)

11. Ganti nama field id menjadi nim!
Untuk mengganti nama field/kolom maka gunakan perintah berikut adalah querynya:

ALTER TABLE nama_tabel CHANGE COLUMN nama_fiedl_lama
nama_field_baru tipe_data_lama(ukuran);
bisa gunakan COLUMN atau tanpa menggunakan COLUMN 
ALTER TABLE nama_tabel CHANGE nama_field_baru tipe_data_lama(ukuran);

contoh:
![gambar](image/CHANGE%20id%20.png)

12. Jadikan nim sebagai PRIMARY KEY!
Untuk Menjadikan PRIMARY KEY pada sebuah kolom maka gunakan perintah berikut adalah querynya:

ALTER TABLE nama_tabel ADD PRIMARY KEY(nama_field);

contoh:
![gambar](image/PRIMARY%20KEY.png)

13. Jadikan kolom email sebagai UNIQUE KEY
Untuk menjadikan UNIQUE KEY pada sebuah kolom maka gunakan perintah berikut adalah querynya:

ALTER TABLE nama_tabel ADD UNIQUE KEY(nama_field);

contoh:
![gambar](image/UNIQUE%20KEY.png)

### B.  Evaluasi dan Pertanyaan
>Maksud dari int (11) adalah int sebagai tipe data dan (11) sebagai index/ukuran tipe data tersebut, jadi jika int(11) maka artinya sebuah tipe data integer ber-index 11 (0<11) atau panjang dari tipe data integer tersebut tidak boleh lebih dari 10.
>Kolom Null,
    i. jika berisi Yes maka data dalam kolom tersebut boleh kosong/tidak ada data atau juga bisa diartikan jika user menginputkan sebuah data maka kolom tersebut boleh tidak diisi dan tidak akan terjadi eror jika data tersebut kosong. Contohnya kolom keterangan.
    ii. Sedangkan jika berisi No maka data dalam kolom tersebut tidak boleh kosong/tidak ada data, jika tidak ada data dalam kolom tersebut akan terjadi eror jika data dalam kolom tersebut kosong/tidak diisi. contohnya kolom nama dan nim.

SELESAI.

