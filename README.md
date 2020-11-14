# Jarkom_A10_Modul2

Anggota :

Kana Rekha 05111840000001

Abdul Rozak Baharudin 05111840000148	

- [Lapres_modul2_A10](#lapres_modul2_A10)
	- [Soal 9](#soal-9)
	- [Soal 10](#soal-10)
 	- [Soal 11](#soal-11)
	- [Soal 12](#soal-12)
  	- [Soal 13](#soal-13)
	- [Soal 14](#soal-14)
 	- [Soal 16](#soal-16)
	
## Soal 1
* Install bind9 pada UML Malang
* Setting /etc/bind/named.conf.local
![1-1](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/1-1.jpg)
* mkdir /etc/bind/jarkom
* copy file db.local menjadi semerua10.pw  ``` cp /etc/bind/db.local /etc/bind/jarkom/semerua10.pw ```
* edit file semerua10.pw
![1-2](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/1-2.jpg)
* service bind9 restart pada UML Malang
* setting pada client gresik nano /etc/resolve.conf masukkan ip malang, dan coba ping
![1-3](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/1-3.jpg)
## Soal 2
* nano /etc/bind/jarkom/semerua10.pw pada UML Malang
![2-1](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/2-1.jpg)
* service bind9 restart pada UML Malang
* lalu cek ping pada UML Client
![2-2](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/2-2.jpg)
## Soal 3
* nano /etc/bind/jarkom/semerua10.pw dan setting seperti dibawah
![3-1](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/3-1.jpg)
* service bind9 restart pada UML Malang
* tes ping penanjakan.semerua10.pw pada UML client
![3-2](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/3-2.jpg)
## Soal 4
* nano /etc/bind/named.conf.local pada UML Malang dan setting seperti dibawah untuk menambah reverse address
![4-1](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/4-1.jpg)
* lalu copy file db.local ```cp /etc/bind/db.local /etc/bind/jarkom/71.151.10.in-addr.arpa``` lalu kita edit seperti dibawah
![4-2](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/4-2.jpg)
* tes pada UML client ```host -t PTR 10.151.73.92``` 
![4-3](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/4-3.jpg)
## Soal 5
* setting pada UML MALANG dan MOJOKERTO pada file ```nano /etc/bind/named.conf.local``` seperti dibawah
![5-1](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/5-1.jpg)
![5-2](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/5-2.jpg)
* service bind9 restart pada UML Mojokerto dan service bind stop pada UML Malang
![5-3](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/4-3.jpg)
* tes ping pada UML Client
![5-4](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/5-4.jpg)
## Soal 6
* Setting pada UML Malang pada file ```nano /etc/bind/jarkom/semerue10.pw```, ```nano /etc/bind/named.conf.options``` dan ```nano /etc/bind/named.conf.local```
![6-1](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/6-1.jpg)
![6-2](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/6-2.jpg)
![6-3](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/6-3.jpg)
* Setting pada UML Mojokerto pada file ```nano /etc/bind/named.conf.local```
![6-4](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/6-4.jpg)
* Cek ping gunung.semeru.a10.pw pada UML client 
![6-5](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/6-5.jpg)
## Soal 7
* Buat subdomain naik.gunung.semerua10.pw dengan men-setting file ```nano /etc/bind/delegasi/gunung/semerua10.pw``` pada UML Mojokerto
![7-1](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/7-1.jpg)
* Cek ping naik.gunung.semerua10.pw pada UML client
![7-2](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/7-2.jpg)
## Soal 8
* Install php dan apache2
* copy file default menjadi semerua10.pw pada directory ``` cd /etc/apache2/sites-available```
![8-1](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/8-1.jpg)
* wget 10.151.36.202/semeru.pw.zip pada directory /var/www/ lalu di unzip dan rename menjadi semerua10.pw
* a2ensite semerua10.pw untuk enable site dan service apache2 restart
* akses website semerua10.pw pada browser
![8-2](https://github.com/rozakcloud/Jarkom_A10_Modul2/blob/main/img/8-2.jpg)
## Soal 9

* Menjalankan perintah a2enmod rewrite untuk mengaktifkan module rewrite.
* Restart apache dengan perintah " service apache2 restart "
* Pindah ke directory /var/www/semerua10.pw dan buat file .htaccess dengan isi file

<img width="368" alt="9" src="https://user-images.githubusercontent.com/57948206/99141513-9dcb1900-267e-11eb-84c2-f87fc68156c0.PNG">

* Pindah ke directory /etc/apache2/sites-available kemudian buka file semerua10.pw dan tambahkan

```
<Directory /var/www/semerua10.pw>
     Options +FollowSymLinks -Multiviews
     AllowOverride All
 </Directory>
 ```
* service apache2 restart
## Soal 10

* Buat directory website dengan perintah  " mkdir /var/www/penanjakan.semerua10.pw "

* Pindah ke direktori /etc/apache2/sites-available dan copy file default ke file penanjakan.semerua10.pw

* Edit file penanjakan.semerua10.pw

<img width="363" alt="10" src="https://user-images.githubusercontent.com/57948206/99141515-9efc4600-267e-11eb-8d9b-699a07a30424.PNG">

* Aktifkan konfigurasi dengan perintah " a2ensite penanjakan.semerua10.pw "

* Download file pendukung dengan wget 10.151.36.202/penanjakan.semerua10.pw.zip di directory /var/www/penanjakan.semerua10.pw

* Extract file .zip

## Soal 11

* tambahkan file /etc/apache2/sites-available/penanjakan.semerua10.pw sesuai dengan gambar :

```
<Directory /var/www/penanjakan.semerua10.pw/public/*>
     Options -Indexes
 </Directory>
 
 ```

<img width="363" alt="11" src="https://user-images.githubusercontent.com/57948206/99141516-9f94dc80-267e-11eb-9907-ea2848188789.PNG">

## Soal 12

* Pindah ke directory /var/www/penanjakan.semerua10.pw dan buat file .htaccess dengan isi file

<img width="362" alt="12a" src="https://user-images.githubusercontent.com/57948206/99141517-a02d7300-267e-11eb-83cf-ed1555d441ff.PNG">

* Pindah ke directory /etc/apache2/sites-available kemudian buka file penanjakan.semerua10.pw dan tambahkan

```
<Directory /var/www/penanjakan.semerua10.pw>
     Options +FollowSymLinks -Multiviews
     AllowOverride All
 </Directory>
 ```
 
<img width="364" alt="12b" src="https://user-images.githubusercontent.com/57948206/99141518-a02d7300-267e-11eb-84cf-f50ec5af58bc.PNG">

## Soal 13

* Edit file konfigurasi yang berada di folder /etc/apache2/sites-available

* Buka file penanjakan.semerua10.pw

* Tambahkan konfirgurasi seperti pada gambar dibawah
```
<Directory /var/www/penanjakan.semerua10.pw/public/javascripts>
     Options -Indexes
 </Directory>
 Alias "/js" "var/www/penanjakan.semerua10.pw/public/javascripts"
 ```

<img width="366" alt="13" src="https://user-images.githubusercontent.com/57948206/99141519-a0c60980-267e-11eb-9637-28c794a88dda.PNG">

* Restart apache dengan perintah service apache2 restart

## Soal 14

* Buat directory naik.gunung.semerua10.pw dengan perintah " mkdir /var/www/naik.gunung.semerua10.pw "

* Salin file dengan perintah " cp /etc/apache2/sites-available/default  /etc/apache2/sites-available naik.gunung.semerua10.pw "

* Buka filenya nano /etc/apache2/sites-available/naik.gunung.semerua10.pw

* Edit <VirtualHost *:80> menjadi <VirtualHost *:8888>

<img width="364" alt="14a" src="https://user-images.githubusercontent.com/57948206/99141520-a15ea000-267e-11eb-8ae2-a8e83868dabb.PNG">

* Buka file ports.conf berada pada directory /etc/apache2

* Tambahkan listen 8888 

* Aktifkan konfirgurasi menggunakan perintah a2ensite

<img width="365" alt="14b" src="https://user-images.githubusercontent.com/57948206/99141521-a15ea000-267e-11eb-9861-57a21e8c5912.PNG">

## Soal 16

* Buka file default di /etc/apache2/sites-available/default

* Kemudian tambahkan " Redirect permanent /http://semerua10.pw/ "

<img width="367" alt="16" src="https://user-images.githubusercontent.com/57948206/99141522-a1f73680-267e-11eb-969a-46bc23bc3ff6.PNG">

* Restart apache dengan perintah service apache2 restart

