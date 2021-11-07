## Absensi Pertemuan 9

## NAVIGASI DAN RUTE 

Mengerjakan modul flutter bab 5, yaitu mempelajari pembangunan aplikasi bergerak multi halaman. 
untuk aplikasinya sendiri yaitu daftar barang belanja. Desain aplikasi menampilkan sebuah ListView widget yang datanya bersumber dari List. 
Ketika item ditekan, data akan dikirimkan ke halaman berikutnya

## Navigator 
widget yang mengatur tumpukan (struktur data stack) dari obyek rute

## Route 
obyek yang merepresentasikan tampilan, umumnya diimplementasikan oleh class seperti MaterialPageRoute

## Mendefinisikan Route
Definisi penamaan route harus bersifat unique. Halaman HomePage didefinisikan sebagai /. 
Dan halaman ItemPage didefinisikan sebagai /item. Untuk mendefinisikan halaman awal, dapat menggunakan named argument initialRoute.

## Berpindah Halaman 
dibutuhkan proses pemodelan data, dibutuhkan dua informasi yaitu nama dan harga.
dengan nama item.dart dan letakkan pada folder models. Pada halaman HomePage terdapat ListView widget
Untuk menampilkan ListView pada praktikum ini digunakan itemBuilder.
Untuk menunjukkan batas data satu dan berikutnya digunakan juga widget Card.
Untuk menambahkan aksi pada ListView dapat digunakan widget InkWell atau GestureDetector. 
GestureDetector bersifat umum dan bisa juga digunakan untuk gesture lain selain sentuhan

## Pengiriman Data
Menambahkan informasi arguments pada penggunaan Navigator

```java 
Navigator.pushNamed(context, '/item', arguments: item);
```

## Pembacaan Data
Pembacaan nilai yang dikirimkan pada halaman sebelumnya dapat dilakukan menggunakan ModalRoute.

```java 
final Item itemArgs = ModalRoute.of(context).settings.arguments;
```
