# Membuat Database
1. Membuat database pada cmd
	code 
 ```sql
 CREATE DATABASE company_herani;
 ```

  ![](asset/foto_1.PNG) 
  analisis 
  - ``create database`` : digunakan untuk membuat database pada mysql yang dapat menempung data.
  -  ``company_herani`` : adalah nama database yang digunakan pada mysql.
2. Menggunakan database
	code 
  ```sql
  USE company_herani;
  ```
  ![](asset/foto_3.PNG) 
  analisis
  - ``USE ``: digunakan ketika ingin menggunakan database.
  - ``[company_herani]`` adalah alamat database yang ingin digunakan 
  
# Membuat table 
code:
```sql
CREATE TABLE pegawai (
NIP int(3) AUTO_INCREMENT PRIMARY KEY NOT NULL,
NDep varchar(50) NOT NULL,
NBlk varchar(50),
jenis_kelamin enum('Laki-laki','Perempuan') NOT NULL,
alamat text(50) NOT NULL,
Telp varchar(20) NOT NULL,
jabatan enum('Manajer','Staf','Sales'),
Gaji BIGINT NOT NULL,
NoCab varchar(50) NOT NULL
);
```

![](asset/foto_4.PNG)

analisis 
-  `create table` :  digunakan untuk membuat table pada database yang telah dibuat.
- Kolom `NIP` : kolom yang merupakan primary key yang akan diisi dan tidak boleh ada data yang sama, dengan tipe data `int(3)` dengan maksimal data 3 digit dan menggunakan fitur AUTO_INCREMENT.
- Kolom `NDep` : menyimpan data nama depan dengan tipe data `varchar(50)` dengan panjang data 50 karakter dan `NOT NULL ` yang bersifat wajib diisi.
-  Kolom `NBlk` : menyimpan data nama belakang dengan tipe data `varchar(50)` dengan panjang data 50 karakter dan  bersifat opsional / bisa tidak diisi.
- Kolom `jenis_kelamin` : menyimpan data jenis kelamin dengan tipe data `enum` digunakan untuk mendefinisikan sekumpulan nilai yang mewakili status atau kondisi tertentu dan bersifat `NOT NULL` yang bersifat wajib diisi.
- Kolom `alamat` : menyimpan data alamat dengan tipe data `text` 

# Menampilkan table 
code 
```sql
DESC pegawai;
```

![](asset/foto_12.PNG)
analisis 
- ``desc ``: di gunakan untuk menampilkan tabel yang telah dibuat.
- ``pegawai ``: adalah nama tabel yang ingin di tampilkan.
# Memasukkan data 
 code 
 ```sql
 INSERT INTO pegawai value
 (data yang ingin di masukkan);
```

![](asset/foto_5.PNG)

analisis 
- `INSERT INTO` :  di gunakan untuk memasukkan data pada tabel.
- `pegawai` : adalah nama tabel yang ingin di masukkan datanya.
-  `VALUE`:  di gunakan untuk data yang di masukkan. 

# Menampilkan data 
code
```sql
SELECT * FROM pegawai;
```

![](asset/foto_8.PNG)
analisis 
- `SELECT` : di gunakan untuk menampilkan data yang sudah di masukkan.
- ``* ``:  di gunakan untuk memilih semua kolom yang ada dalam tabel tertentu.
- `FROM`:  adalah alamat tabel yang ingin di tampilkan.
- `pegawai`:  adalah nama tabel yang ingin di tampilkan.
