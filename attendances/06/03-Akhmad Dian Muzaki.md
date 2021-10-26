# Rangkuman Materi Pertemuan 05
Minggu Ke-05 Mata Kuliah Mobile
--

            Nama           : Akhmad Dian Muzaki
            NIM            : 1941720205
            No.Absen       : 03
            Dosen Pengampu : Putra Prima Arhandi, S.T., M.Kom.

Contents

# Rangkuman Chapter 1 | 2 | 3
## Chap 1: Pengenalan Flutter
---
### Tujuan Pembelajaran
1. Mahasiswa mampu menginstall flutter pada device masing-masing
2. mahasiswa memahami flutter dan widget
3. mahasiswa mampu menyelesaikan tugas praktikum
---
### Flutter:
Flutter adalah sebuah framework open source yang dibuat oleh Google. Google membuat
flutter dengan tujuan membangun sebuah framework untuk membuat UI yang modern, native 
dan reactive yang dapat berjalan di sistem operasi iOS maupun Android. Tidak hanya pada 
smartphone google juga membuat flutter untuk desktop, web dan embedded device.
Flutter diprogram dengan menggunakan bahasa Dart sebuah bahasa moderen yang dapat 
dicompile ke arsitektur processor ARM atau javascript. Flutter menggunakan Skia 2D 
rendering engine yang dapat bekerja pada hardware atau software yang berbeda platform.
Dart menggunakan metode compilasi ahead of time (AOT) untuk mengubah kode Dart 
menjadi kode native untuk sistem operasi yang digunakan, oleh karena itu aplikasi yang 
dibangun menggunakan flutter memiliki kecepatan yang hampir sama dengan aplikasi native. 
Dart juga menggunakan konsep just-in-time (JIT) sehingga memungkinkan programmer dapat 
membuat perubahan pada kode program dan langsung melihat hasilnya melalui fitur hot 
reaload yang dimiliki Flutter.
Flutter menggunakan Dart untuk membuat User Interface, sehingga memudahkan dalam 
membuat aplikasi karena menggunakan satu bahasa (Dart) dalam pembuatan UI maupun logika 
program. Flutter menggunakan pendekatan declarative dimana Flutter membangun UI 
mengikuti “State” yang dimiliki oleh aplikasi. Ketika state berubah maka UI akan digambar 
ulang .

### Widget dan Elemen Pada FLutter:
Widget adalah sebuah konsep dimana UI dapat dianggap sebagai sebuah balok LEGO, sebuah 
bentuk baru dapat disusun dari beberapa balok dan masing masing kumpulan balok dapat 
dikombinasikan dengan kumpulan balok lain sehingga membentuk sebuah bentuk baru yang 
lebih kompleks. Flutter menggunakan widget ini sebagai balok dasar pembangunan aplikasi.
Widget dapat disusun dan dikombinasikan dalam satu layar, sama halnya dengan xml 
pada pemrograman android native, widget dapat disusun dalam bentuk tree dimana satu widget 
menjadi parent dan widget lain menjadi child. Masing masing widget dapat diberikan 
konfigurasi sesuai dengan kebutuhan aplikasi.
Flutter memiliki dua jenis widget yaitu StatelessWidget dan StatefullWidget. Stateless 
widget digunakan ketika value (state /konfigurasi) dari widget tersebut tidak pernah berubah, 
dan StatefullWidget digunakan ketika value (state / konfigurasi) dari widget dapat berubah.
Baik StatelessWidget maupun StatefullWidget sama sama memiliki sebuah method bernama 
“build” yang memiliki BuildContext untuk mengatur posisi widget didalam widget tree.

---
## Chap 2: Basic Aplikasi Flutter
### Struktur Project flutter
#### Struktur Folder
Ketika membuat project flutter secara default berikut adalah struktur folder dan 
filenya. Dapat kita lihat strukturnya terdiri dari .dart_tool, .idea, android, ios, lib, test, 
.gitignore, .metadata, .packages, .flutter_basic.iml, pubspec.lock, pubspec.yaml, 
README.md. Berikut adalah penjelasan yang lebih detail tentang struktur files dari flutter:
1. .dart_tools : Konfigurasi untuk dart language
2. .idea : Konfigurasi untuk android studio
3. gitignore : File git yang digunakan untuk mengelola source code. Hal ini akan 
    berguna jika developer sudah bekerja dengan git.
4. metadata : File yang berisi metadata dari project
5. packages : File yang berisi alamat path
6. flutter_basic.iml: File yang berisi detail dari project.
7. pubspec.lock : File yang berisi versi library atau package yang digunakan pada 
project yang degenerate sesuai dengan file pubspec.yaml.
8. pubspec.yaml : File yang berisi library atau package yang dibutuhkan untuk 
pengembangan aplikasi.
9. Readme.md : File markdown yang dapat digunakan untuk menjelaskan cara setup
aplikasi atau informasi penting yang perlu untuk diketahui oleh 
developer lain.
#### Multi OS IOS dan ANDROID
Readme.md : File markdown yang dapat digunakan untuk menjelaskan cara setup
aplikasi atau informasi penting yang perlu untuk diketahui oleh 
developer lain.
#### Folder Android
Folder android berisi file file pendukung untuk mengenerate project android dan akan 
dikompilasi menjadi sebuah apk pada folder build. Namun anda jarang atau bahkan tidak 
perlu mengedit yang ada di folder android. Anda akan banyak bekerja di folder lib.
#### Folder IOS
Berisi project ios, folder ini sama dengan folder android, sangat jarang dan bahkan 
tidak perlu untuk mengubah apapun pada folder ios. Folder ios dan android dikelola oleh 
flutter sdk yang akan dimerge (disatukan) dengan code yang ada di folder lib untuk membuat 
aplikasi ios dan android.
#### Folder Lib
Folder lib berisi kode program dengan bahasa dart yang berupa widget yang dapat 
dibuat sesuai dengan kebutuhan aplikasi anda.
#### Folder Test
Berisi source code dart yang digunakan untuk melakukan test secara otomatis pada 
aplikasi flutter.
#### Pubspec.yaml
Pada file ini berisi konfigurasi konfigurasi project flutter yang dibuat dimana anda 
dapat mendata asset berupa font, gambar dan lain lain. Pada file ini anda juga dapat 
mengkonfigurasi flutter sdk dan konfigurasi yang terkait flutter.

---
### Flutter Hot Reload
Pada flutter terdapat fungsi hot reload dan hot restart yang digunakan untuk 
pengembangan aplikasi dengan flutter. Hote reload mencompile source code yang baru 
ditambahkan dan dikirimkan ke dart virtual machine diupdate. Setelah selesai update, dart 
virtual machine akan memperbarui UI sesuai dengan perubahan. Keunggulan hot reload 
adalah waktu prosenya cepat disbanding hot restart. Akan tetapi hot reload mempertahan
state yang ada sehingga jika menggunakan state maka nilai dari widget tidak akan berubah.
### Flutter Hot Restart
Hot restart akan mencompile ulang aplikasi dan mereset (destroy) state yang ada. Jadi 
hot restart akan membuild ulang widget tree sesuai dengan code yang telah diperbarui. 
### Bedah Hello Word Project
#### Import Statement
Seperti halnya kode program pada umumnya dart dapat menggunakan statement 
import untuk mengimport package, library, atau file lain yang digunakan pada file yang 
dieksekusi. (import 'package:flutter/material.dart';)
#### Main Function
Main function pada flutter dibuat dengan menggunakan kode program berikut ini 
dimana semua proses aplikasi dimulai dari mengeksekusi fungsi main.
(void main() {
 runApp(MyApp());
})
Perhatikan pada fungsi main ini yang di eksekusi adalah class MyApp dimana class 
MyApp harus mengextend salah satu StatlessWidget atau StatefullWidget, ingat bahwa 
flutter membangun UI menggunakan widget.
#### Stateles Widget
Flutter menggunakan Widget sebagai elemen elemen pembangun UI, widget ini adalah 
kode program yang diterjemahkan menjadi tampilan yang dapat dilihat dan diinteraksikan 
oleh pengguna. Stateless widget bersifat statis / final dimana nilai atau konfigurasi telah 
diinisiasi sejak awal, nilai variabel pada widget ini tidak dapat diubah oleh widget ini sendiri 
tetapi dapat diubah oleh parent widget nya jika parent nya adalah StatefullWidget. Struktur 
dasar stateless widget adalah sebagai berikut:
(class exampleStateless extends StatelessWidget{
 @override
 Widget build(BuildContext context) {
 
 }
})
#### Statefull Widget
Statefull widget bersifat dinamis, widget ini dapat diperbarui ketika dibutuhkan sesuai 
dengan action pengguna atau jika ada ada perubahan data. Perubahan data pada statefull 
widget di trigger oleh perubahan state oleh karena itu sebuah StatefullWidget selalu memiliki 
State. 

---

### Build in Widget
Pada framework flutter terdapat banyak widget. Widget yang telah disediakan dapat 
digunakan mengembangkan aplikasi yang mobile, desktop dan web yang memiliki tampilan 
menarik. Secara lebih detail widget yang tersedia di flutter dapat dicek pada 
https://flutter.dev/docs/development/ui/widgets. Berikut adalah beberapa contoh widget yang 
sering digunakan pada pembuatan aplikasi dengan flutter. 
1. Text Widget
2. Image Widget
3. Material Design and Ios CUpertino
4. Button
5. Scaffold
6. Dialog
7. Input dan Selection Widget
8. Date and Times Pickers

---
### Build In Layout Widget
#### Container
Container merupakan single child objek yang artinya hanya 
dapat memiliki satu buah child widget, akan tetapi dalam sebuat container kita dapat 
menempatkan row, column, text dan container lain. Container memiliki beberapa property 
yaitu:
1. property child
2. property alignment
3. property color
4. property height and width
5. property margin
6. property padding
7. property transform
8. property decoration

#### Row and Column
Column widget digunakan untuk mangatur tata letak widget secara vertikal. Sedangkan row 
digunakan untuk mengatur tata letak widget secara horizontal.
#### Stack
Stack Widget digunakan untuk menumpuk beberapa widget pada beberapa lapisan.
#### ListView
ListView widget digunanakan untuk menampilkan data dalam bentuk list dan jika datanya 
melebihi dari render box maka halaman tersebut dapat di scroll.
#### GridView
Gridview digunakan untuk menata tata letak widget pada list 2 dimensi. GridView juga
secara otomatis menyediakan scrolling ketika konten melebihi render box.

---
## Chap 3: Aplikasi dengan Statefull Widget
### Desain Aplikasi
Untuk pembuatan aplikasi ini dimulai dengan membuat 
sebuah desain yang dapat dimulai dengan membuat wireframe atau desain utuh di perangkat 
lunak seperti adobe xd atau sketch dan yang lain. Untuk menyederhanakan proses desain 
anda sudah disediakan template sederhana di starter code dengan menggunakan template 
material design. Berikut ini desain mockup aplikasi yang dibuat.
### Konversi Desain ke Stateless Widget
Untuk mempermudah proses konversi dari desain ke stateless widget perhatikanlah 
item item yang ada pada desain tersebut, apa saja widget yang terlibat dan apa saja widget 
layout yang digunakan
### Membuat Aplikasi Interaktif
Setelah berhasil membuat layout selanjutnya adalah membuat aplikasi yang mamapu 
melakukan konversi suhu dari input berupa derajat celcius ke tiga derajat lain yaitu kelvin, 
reamur dan fahrenheit.
#### Convert ke StatefullWidget
Setelah berhasil membuat layout selanjutnya adalah membuat aplikasi yang mamapu 
melakukan konversi suhu dari input berupa derajat celcius ke tiga derajat lain yaitu kelvin, 
reamur dan fahrenheit.
#### Membuat State
Untuk membuat state perhatikan beberapa best practice berikut ini mengenai elemen
mana dari UI yang akan dimasukkan kedalam state.
1. Apakah ada elemen pada UI yang berubah ?
2. Apakah yang menyebabkan elemen tersebut berubah ? 
Jika diperhatikan dari UI yang disediakan maka elemen yang dapat berubah adalah input 
dari user, dan output dari proses konversi suhu. Sedangkan yang menjadi trigger perubahan 
adalah ketika tombol konversi ditekan. Pada pengembangan aplikasi menggunakan flutter 
elemen yang berubah ini akan dimasukkan kedalam state dan elemen yang mentrigger 
perubahan akan disebut event. Untuk membuat state tambahkanlah kode program yang menurut anda perlu ditambahkan 
berikut ini contoh kode program pada state dari widget MyApp yang sekarang berubah 
menjadi statefull widget.
#### Mengambil Data Input Suhu
Selain memiliki variabel input tentu saja input ini harus diambil dari TextFormField yang 
menadi cara user menginputkan angka untuk di konversi, carilah cara menambahkan 
controller terhadap TextFormField ini. 
#### Membuat Event
Langkah selanjutnya adalah membuat event dimana event perhitungan konversi dan 
update hasil konversi dilakukan saat tombol Konversi ditekan. Untuk menyambungkan 
proses klik button ke perubahan state ada beberapa langkah yang harus anda lakukan. 
1. Buat Fungsi di dalam state MyAppState
2. Panggil Fungsi ini ketika tombol konversi di tekan
3. Tambahkan Set State di fungsi tersebut dan ubah lah state dari variabel yang anda 
gunakan sebagai dasar perhitungan konversi.
4. Tambahkan kode program untuk melakukan konversi suhu dan set state variabel yang 
anda gunakan untuk kelvin, reamur dan fahrenheit. 
#### Menampilkan Output Result
Untuk menampilkan output anda hanya perlu menyambungkan variabel yang berubah 
pada state ke widget Text yang menampilkan hasil.

---
### Membagi ke Widget Yang Lebih Kecil
Lakukan lah extraksi widget ke file yang berbeda dengan cara Ctrl + . pada widget 
yang ingin anda potong dan pilih menu Extract Widget, berikanlah nama class yang sesuai 
dan pindahkan ke file baru.
Berikut ini nama nama widget dan ekstraksi yang dapat dicontoh :
1. Input : Berisi Widget TextFormField dan controller nya
2. Result : Berisi widget hasil konversi yang memiliki variabel nama dan hasil.
3. Convert : Berisi button dan reference ke function yang digunakan untuk 
melakukan setState().
#### Send Parameter ke Child
Sebuah widget dapat mengirim paramter ke child widgetnya melalui constructor yang 
dimiliki oleh widget tersebut parameter ini dapat menyesuaikan dengan kebutuhan yang 
dimiliki oleh widget terssebut. Berikut ini contoh pembuatan widget dan constructor dari 
widget yang dibuat.
#### Send Evvent Handler ke Child
Selain mengirimkan parameter ke child widget parent juga dapat mengirim fungsi turun 
ke child widget dimana fungsi ini akan dipanggil lagi oleh parent widget yang memiliki state. 
Berikut ini contoh kode program untuk menurunkan fungsi ke child widget.

---
# Link Tugas:
## Chapter 1
https://github.com/muzakidian/polinema_mobile_flutter_hello

## Chapter 2
https://github.com/muzakidian/flutter-basic

## Chapter 3
https://github.com/muzakidian/konversi-suhu-flutter.git