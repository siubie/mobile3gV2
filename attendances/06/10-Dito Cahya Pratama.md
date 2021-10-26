# :books: Rangkuman Pertemuan 6

## BAB 1. INSTALASI DAN PENGENALAN FLUTTER

Setelah melakukan jobsheet installasi dan pengenalan flutter, saya dapat memahami tentang:

1. Cara install flutter di linux
2. Pengertian flutter
3. Mengetahui tentang StatelessWidget dan StatefullWidget

### Apa itu Flutter

Flutter adalah sebuah framework open source yang dibuat oleh Google. Google membuat flutter dengan tujuan membangun sebuah framework untuk membuat UI yang modern, native dan reactive yang dapat berjalan di sistem operasi iOS maupun Android. Tidak hanya pada smartphone google juga membuat flutter untuk desktop, web dan embedded device.

Flutter diprogram dengan menggunakan bahasa Dart sebuah bahasa moderen yang dapat
dicompile ke arsitektur processor ARM atau javascript. Flutter menggunakan Skia 2D
rendering engine yang dapat bekerja pada hardware atau software yang berbeda platform.

Dart menggunakan metode compilasi ahead of time (AOT) untuk mengubah kode Dart
menjadi kode native untuk sistem operasi yang digunakan, oleh karena itu aplikasi yang dibangun menggunakan flutter memiliki kecepatan yang hampir sama dengan aplikasi native.

Dart juga menggunakan konsep just-in-time (JIT) sehingga memungkinkan programmer dapat membuat perubahan pada kode program dan langsung melihat hasilnya melalui fitur hot reaload yang dimiliki Flutter.

### Widget dan Element pada flutter

Gaya pengembangan aplikasi menggunakan flutter sedikit berbeda dengan gaya
pengembangan aplikasi pada umumnya, dimana UI pada flutter dibuat menggunakan Widget. Widget adalah sebuah konsep dimana UI dapat dianggap sebagai sebuah balok LEGO, sebuah bentuk baru dapat disusun dari beberapa balok dan masing masing kumpulan balok dapat dikombinasikan dengan kumpulan balok lain sehingga membentuk sebuah bentuk baru yang lebih kompleks. Flutter menggunakan widget ini sebagai balok dasar pembangunan aplikasi.

Widget dapat disusun dan dikombinasikan dalam satu layar, sama halnya dengan xml
pada pemrograman android native, widget dapat disusun dalam bentuk tree dimana satu widget menjadi parent dan widget lain menjadi child. Masing masing widget dapat diberikan konfigurasi sesuai dengan kebutuhan aplikasi.

Flutter memiliki dua jenis widget yaitu StatelessWidget dan StatefullWidget. Stateless widget digunakan ketika value (state /konfigurasi) dari widget tersebut tidak pernah berubah, dan StatefullWidget digunakan ketika value (state / konfigurasi) dari widget dapat berubah. Baik StatelessWidget maupun StatefullWidget sama sama memiliki sebuah method bernama “build” yang memiliki BuildContext untuk mengatur posisi widget didalam widget tree detail mengenai widget dan bagaimana membuatnya akan dibahas pada bab selanjutnya.

## BAB 2. BASIC APLIKASI FLUTTER

Setelah melakukan jobsheet basic aplikasi flutter, saya dapat memahami tentang:

1. Memahami struktur project flutter
2. Memahami fungsi tentang hot reload dan hot restart

### Struktur project flutter

Ketika membuat project flutter secara default berikut adalah struktur folder dan
filenya. Dapat kita lihat strukturnya terdiri dari .dart_tool, .idea, android, ios, lib, test, .gitignore, .metadata, .packages, .flutter_basic.iml, pubspec.lock, pubspec.yaml, README.md.

Berikut adalah penjelasan yang lebih detail tentang struktur files dari flutter.
1. .dart_tools : Konfigurasi untuk dart language
2. .idea : Konfigurasi untuk android studio
3. gitignore : File git yang digunakan untuk mengelola source code. Hal ini akan berguna jika developer sudah bekerja dengan git.
4. metadata : File yang berisi metadata dari project
5. packages : File yang berisi alamat path
6. flutter_basic.iml: File yang berisi detail dari project.
7. pubspec.lock : File yang berisi versi library atau package yang digunakan pada project yang degenerate sesuai dengan file pubspec.yaml.
8. pubspec.yaml : File yang berisi library atau package yang dibutuhkan untuk pengembangan aplikasi.
9. Readme.md : File markdown yang dapat digunakan untuk menjelaskan cara setupaplikasi atau informasi penting yang perlu untuk diketahui oleh developer lain

### Flutter Hot Reload
Pada flutter terdapat fungsi hot reload dan hot restart yang digunakan untuk pengembangan aplikasi dengan flutter. Hote reload mencompile source code yang baru ditambahkan dan dikirimkan ke dart virtual machine diupdate. Setelah selesai update, dart virtual machine akan memperbarui UI sesuai dengan perubahan.

### Flutter Hot Restart
Hot restart akan mencompile ulang aplikasi dan mereset (destroy) state yang ada. Jadi hot restart akan membuild ulang widget tree sesuai dengan code yang telah diperbarui.