# Rangkuman Pertemuan 8

## Menguji coba Praktikum Flutter Chapter 4
Pada pertemuan ini menguji coba chapter ke 4 yaitu konversi suhu. Belajar mengenai cara pembuatan aplikasi sederhana yang memiliki statefull widget. k pembuatan aplikasi ini dimulai dengan membuat 
sebuah desain yang dapat dimulai dengan membuat wireframe atau desain utuh di perangkat 
lunak seperti adobe xd atau sketch dan yang lain.

## Instalasi ekstensi Wakatime di VS code
WakaTime punya fungsi untuk tracking waktu yang kita habiskan untuk coding.
di WakaTime, semuanya otomatis dilakukan mulai dari kita mengetik sampai dengan berakhirnya tulisan dan melakukan penyimpanan ke storage.
Tak hanya durasi aktivitas yang dilacak, tapi juga editor yang digunakan, berkas apa yang digunakan, dan bahasa pemrograman/tool yang dipakai. Perlu diketahui, setiap integrasi dengan editor apapun, dibutuhkan data berupa API KEY. API KEY ini didapatkan pada menu setting sesaat setelah selesai mendaftar di website resminya.

## List
List adalah collection yang seperti pada bahasa pemrograman yang lain. Pada bahasa pemrograman Dart, 
array adalah list of object sehingga disebut juga dengan list. Berikut ini adalah contoh list 
pada Dart yaitu :

```
var list = [5, 6, 7];
var list2 = [4, ...list];
print(list2.length == 4);
```
Anda juga dapat menggunakan null-aware spread operator untuk menghindari exception 
ketika list bernilai null.
```
var list;
var list2 = [0, ...?list];
print(list2.length == 1);
```
Dart juga menyediakan collection if dan collection for yang digunakan untuk membuat 
collection dengan kondisi dan repetisi / perulangan. Berikut adalah contoh collection if untuk 
membuat list yang terdiri dari 3 atau 4 item sesuai dengan kondisi.