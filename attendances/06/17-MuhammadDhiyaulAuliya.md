# Rangkuman Pertemuan 6

## Apa itu Flutter ?

Flutter adalah sebuah framework open source yang dibuat oleh Google. Google membuat
flutter dengan tujuan membangun sebuah framework untuk membuat UI yang modern, native 
dan reactive yang dapat berjalan di sistem operasi iOS maupun Android. Tidak hanya pada 
smartphone google juga membuat flutter untuk desktop, web dan embedded device.

Flutter diprogram dengan menggunakan bahasa Dart sebuah bahasa moderen yang dapat 
dicompile ke arsitektur processor ARM atau javascript. Flutter menggunakan Skia 2D 
rendering engine yang dapat bekerja pada hardware atau software yang berbeda platform.

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

Flutter juga memudahkan programmer karena dari satu kode program dapat dikompilasi 
ke kode native ARM, menggunakan GPU dan mengakses fitur spesifik dari smartphone baik 
yang mengunakan sistem operasi iOS ataupun yang menggunakan sistem operasi Android. Jadi 
dengan satu kali membuat program dapat membuat 2 aplikasi yang sama untuk sistem operasi 
yang berbeda (iOS atau Android).

## Widget dan Element pada Flutter

Gaya pengembangan aplikasi menggunakan flutter sedikit berbeda dengan gaya 
pengembangan aplikasi pada umumnya, dimana UI pada flutter dibuat menggunakan Widget. 
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
“build” yang memiliki BuildContext untuk mengatur posisi widget didalam widget tree detail 
mengenai widget dan bagaimana membuatnya akan dibahas pada bab selanjutnya.

# Praktikum

1. Praktikum Installasi Flutter
2. Praktikum Hello World
3. Praktikum 2 Membuat Git Repository dan Publish Ke Github
