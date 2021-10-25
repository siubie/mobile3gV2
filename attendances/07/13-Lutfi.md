3 Rangkuman Pertemuan 7
Menguji coba Praktikum Flutter Chapter 3
Belajar mengenai cara pembuatan aplikasi sederhana yang memiliki statefull widget. k pembuatan aplikasi ini dimulai dengan membuat sebuah desain yang dapat dimulai dengan membuat wireframe atau desain utuh di perangkat lunak seperti adobe xd atau sketch dan yang lain.

Konversi Desain Ke StatelessWidget
Stateless widget adalah widget yang hanya bertugas untuk menampilkan sesuatu secara statis. Tanpa melakukan tracking perubahan data dari waktu ke waktu. Membuat starter code di main.dart sehingga menjadi seperti kode program dibawah ini :

import 'package:flutter/material.dart'; import 'package:flutter/services.dart'; void main() { runApp(MyApp()); } class MyApp extends StatelessWidget { // This widget is the root of your application. @override Widget build(BuildContext context) { return MaterialApp( title: 'Flutter Demo', theme: ThemeData( primarySwatch: Colors.blue, visualDensity: VisualDensity.adaptivePlatformDensity, ), home: Scaffold( appBar: AppBar( title: Text("Konverter Suhu"), ), body: Container(), ), ); } }

Mempelajari untuk mempermudah proses konversi desain ke stateless widget yang sudah di contohkan dan sudah di representasikan menjadi sebuah tree layout pada jobsheet flutter chapter 3. Mempelajari shortcut pada Visual Studio Code yaitu shortcut CTRL + . yang dapat digunakan untuk membungkus widget yang sudah ada atau untuk membuat widget yang telah dibuat menjadi class baru. Mempelajari cara agar pada TextField hanya memiliki tampilan input keyboard khusus angka dan memiliki validasi hanya angka. Mempelajari untuk mengambil data inputan user yang berada di TextField menggunakan TextEditingController. Mengetahui cara membuat function yang dapat dipanggil nantinya. Mempelajari tentang penggunaan pemisahan widget kedalam class baru dan di pindahkan ke file baru, sehingga pada main.dart tidak terlalu panjang kode baris pemogramannya. Mempelajari membuat sebuah event untuk mengkonversi suhu, dimana pada event tersebut terdapat rumus untuk mengkonversi suhu. Hasil konversi harus diubah menjadi double karena yang diinput oleh user berupa string.

Membuat Aplikasi Interaktif
Setelah berhasil membuat layout selanjutnya adalah membuat aplikasi yang mamapu melakukan konversi suhu dari input berupa derajat celcius ke tiga derajat lain yaitu kelvin, reamur dan fahrenheit.

Membuat State
Untuk membuat state tambahkanlah kode program yang menurut anda perlu ditambahkan berikut ini contoh kode program pada state dari widget MyApp yang sekarang berubah menjadi statefull widget.

Mengambil Data Input Suhu
Selain memiliki variabel input tentu saja input ini harus diambil dari TextFormField yang menadi cara user menginputkan angka untuk di konversi.

Membuat Event
event perhitungan konversi dan update hasil konversi dilakukan saat tombol Konversi ditekan.

Membagi ke Widget yang lebih kecil
Lakukan lah extraksi widget ke file yang berbeda dengan cara Ctrl + . pada widget yang ingin anda potong dan pilih menu Extract Widget, berikanlah nama class yang sesuai dan pindahkan ke file baru. Berikut ini nama nama widget dan ekstraksi yang dapat dicontoh :

Input : Berisi Widget TextFormField dan controller nya
Result : Berisi widget hasil konversi yang memiliki variabel nama dan hasil.
Convert : Berisi button dan reference ke function yang digunakan untuk melakukan setState().
Send Parameter ke child
Sebuah widget dapat mengirim paramter ke child widgetnya melalui constructor yang dimiliki oleh widget tersebut parameter ini dapat menyesuaikan dengan kebutuhan yang dimiliki oleh widget terssebut.

Send Event ke child
Selain mengirimkan parameter ke child widget parent juga dapat mengirim fungsi turun ke child widget dimana fungsi ini akan dipanggil lagi oleh parent widget yang memiliki state. Berikut ini contoh kode program untuk menurunkan fungsi ke child widget.
