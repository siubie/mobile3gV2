# Presensi Pertemuan 6

## Install Flutter Windows
Untuk install Flutter dan menjalankannya, lingkungan development kamu harus memiliki beberapa hal yang memadai seperti:

Sistem operasi: Windows 7 SP1 atau yang terbaru 64-bit, yang berdasarkan x86-64.
Ruang penyimpanan minimal 1.64 GB tidak termasuk ruangan untuk IDE/Tools.
Tools: Flutter bergantung pada tools yang tersedia di lingkungan development Kamu.
– Windows PowerShell 5.0 atau yang lebih baru (ini sudah diinstal sebelumnya dengan Windows 10)

– Git untuk Windows 2.x, dengan Gunakan Git dari opsi Prompt Perintah Windows.

Jika Git untuk Windows sudah terinstal, pastikan Kamu dapat menjalankan perintah git dari command prompt atau PowerShell.

### Download Flutter SDK
Unduh penginstalan berikut untuk mendapatkan rilis stabil terbaru dari Flutter SDK:

https://storage.googleapis.com/flutter_infra_release/releases/stable/windows/flutter_windows_2.2.3-stable.zip

Untuk saluran rilis lainnya, dan versi lama, lihat halaman rilis SDK.

Ekstrak file zip dan tempatkan flutter yang ada di lokasi instalasi yang diinginkan untuk Flutter SDK (misalnya, C:\Users\<your-user-name>\Documents).

Kalau kamu tidak ingin menginstal versi tetap dari paket instalasi, kamu bisa melewati langkah 1 dan 2. Sebagai gantinya, dapatkan kode sumber dari repo Flutter di GitHub, dan ubah cabang atau tag sesuai kebutuhan. Sebagai contoh:

git clone https://github.com/flutter/flutter.git -b stable

Kamu sekarang siap menjalankan perintah Flutter di Flutter Console.

### Update Path

Kalau kamu ingin menjalankan perintah Flutter di konsol Windows biasa, lakukan langkah-langkah ini untuk menambahkan Flutter ke variabel lingkungan PATH:

Dari bilah pencarian start, masukkan ‘env’ dan pilih Edit variabel lingkungan untuk akun kamu.
Di bawah Variabel pengguna, periksa apakah ada entri bernama Path:
– Jika entri ada, tambahkan path lengkap ke flutter\bin menggunakan ; sebagai pemisah dari nilai-nilai yang ada.

– Jika entri tidak ada, buatlah variabel pengguna baru bernama Path dengan path lengkap ke flutter\bin sebagai nilainya.

Kamu harus menutup dan membuka kembali jendela konsol yang ada agar perubahan ini diterapkan.

Catatan:

Pada rilis dev 1.19.0 Flutter, Flutter SDK berisi perintah dart di samping perintah flutter sehingga Kamu dapat lebih mudah menjalankan program baris perintah Dart.

Mengunduh Flutter SDK juga mengunduh versi Dart yang kompatibel, tetapi jika Kamu telah mengunduh Dart SDK secara terpisah, pastikan versi dart Flutter berada di urutan pertama di jalur Kamu, karena kedua versi tersebut mungkin tidak kompatibel.

Perintah berikut memberi tahu Kamu apakah perintah flutter dan dart berasal dari direktori bin yang sama dan karenanya kompatibel.
```
where flutter dart
  C:\path-to-flutter-sdk\bin\flutter
  C:\path-to-flutter-sdk\bin\flutter.bat
  C:\path-to-dart-sdk\bin\dart.exe        :: this should go after `C:\path-to-flutter-sdk\bin\` commands
  C:\path-to-flutter-sdk\bin\dart
  C:\path-to-flutter-sdk\bin\dart.bat
  ```
Seperti yang ditampilkan di atas, perintah Dart dari Flutter SDK tidak datang lebih dulu. Perbarui jalur Kamu untuk menggunakan perintah dari C:\path-to-flutter-sdk\bin\ sebelum perintah dari C:\path-to-dart-sdk\bin\ (dalam kasus ini).

Setelah memulai ulang shell kamu agar perubahan diterapkan, menjalankan perintah where lagi akan menunjukkan bahwa perintah flutter dan dart dari direktori yang sama sekarang didahulukan.
```
where flutter dart
  C:\dev\src\flutter\bin\flutter
  C:\dev\src\flutter\bin\flutter.bat
  C:\dev\src\flutter\bin\dart
  C:\dev\src\flutter\bin\dart.bat
  C:\dev\src\dart-sdk\bin\dart.exe
```
Bagaimanapun jika kamu menggunakan PowerShell, di dalamnya where adalah alias perintah Where-Object, jadi Kamu harus menggunakan where.exe sebagai gantinya.

PS where.exe flutter dart

###Jalankan Flutter Doctor

Dari jendela konsol yang memiliki direktori Flutter di Path. Jalankan perintah berikut untuk melihat apakah ada dependensi platform yang Kamu perlukan untuk menyelesaikan penyiapan:
```
C:\src\flutter>flutter doctor
```
Perintah ini memeriksa lingkungan Kamu dan menampilkan laporan status penginstalan Flutter kamu. Periksa output dengan cermat untuk perangkat lunak lain yang mungkin perlu kamu instal atau tugas lebih lanjut yang harus dilakukan (ditampilkan dalam teks tebal).

Sebagai contoh:

[-] Android toolchain – develop for Android devices

Android SDK at D:\Android\sdk
✗ Android SDK is missing command line tools; download from https://goo.gl/XxQghQ

Try re-installing or updating your Android SDK,
visit https://flutter.dev/setup/#android-setup for detailed instructions.

Bagian berikut menjelaskan cara melakukan tugas ini dan menyelesaikan proses penyiapan. Setelah Kamu menginstal dependensi yang hilang, Kamu dapat menjalankan lagi perintah flutter doctor untuk memverifikasi bahwa Kamu telah mengatur semuanya dengan benar.

### Android Setup

- Download dan install Android Studio.

- Mulai Android Studio, dan buka ‘Panduan Penyiapan Android Studio’. Ini menginstal Android SDK, Android SDK Command-line Tools, dan Android SDK Build-Tools terbaru, yang diperlukan oleh Flutter saat mengembangkan untuk Android.

- Jalankan flutter doctor untuk mengonfirmasi bahwa Flutter telah menemukan instalasi Android Studio Kamu. Jika Flutter tidak dapat menemukannya, jalankan flutter config –android-studio-dir <directory> untuk menyetel direktori tempat Android Studio diinstal.

### Mengatur Perangkat Android

Untuk bersiap menjalankan dan menguji aplikasi Flutter di perangkat Android, Kamu memerlukan perangkat Android yang menjalankan Android 4.1 (API level 16) atau lebih tinggi.

- Aktifkan Developer options dan debugging USB di perangkat Kamu. Instruksi terperinci tersedia di dokumentasi Android.

- Khusus Windows: Instal Driver USB Google.

- Menggunakan kabel USB, colokkan ponsel Kamu ke komputer.Jika diminta pada perangkat Kamu, otorisasi komputer Kamu untuk mengakses perangkat Kamu.

- Jalankan perintah flutter devices di terminal untuk memverifikasi bahwa Flutter mengenali perangkat Android Kamu yang terhubung. Secara default, Flutter menggunakan versi Android SDK tempat alat adb Kamu berada. Jika Kamu ingin Flutter menggunakan penginstalan Android SDK yang berbeda, Kamu harus menyetel variabel lingkungan ANDROID_SDK_ROOT ke direktori penginstalan tersebut.

## BASIC APLIKASI FLUTTER

### Struktur Project Flutter

1.  Struktur folder

Ketika membuat project flutter secara default berikut adalah struktur folder dan 
filenya. Dapat kita lihat strukturnya terdiri dari .dart_tool, .idea, android, ios, lib, test, 
.gitignore, .metadata, .packages, .flutter_basic.iml, pubspec.lock, pubspec.yaml, 
README.md.

Berikut adalah penjelasan yang lebih detail tentang struktur files dari flutter.
- .dart_tools : Konfigurasi untuk dart language
- .idea : Konfigurasi untuk android studio
- gitignore : File git yang digunakan untuk mengelola source code. Hal ini akan 
berguna jika developer sudah bekerja dengan git.
- metadata : File yang berisi metadata dari project
- packages : File yang berisi alamat path
- flutter_basic.iml: File yang berisi detail dari project.
- pubspec.lock : File yang berisi versi library atau package yang digunakan pada 
project yang degenerate sesuai dengan file pubspec.yaml.
- pubspec.yaml : File yang berisi library atau package yang dibutuhkan untuk 
pengembangan aplikasi.
- Readme.md : File markdown yang dapat digunakan untuk menjelaskan cara setup
aplikasi atau informasi penting yang perlu untuk diketahui oleh 
developer lain.

2. Multi os ios dan android

Perhatikan pada folder project flutter terdapat dua folder yaitu folder ios dan folder 
android, dengan menggunakan kedua folder tersebut flutter dapat membuat aplikasi berbasis 
ios dan berbasis android dalam satu project.

3. Folder android

Folder android berisi file file pendukung untuk mengenerate project android dan akan 
dikompilasi menjadi sebuah apk pada folder build. Namun anda jarang atau bahkan tidak 
perlu mengedit yang ada di folder android. Anda akan banyak bekerja di folder lib.

4. Folder ios

Berisi project ios, folder ini sama dengan folder android, sangat jarang dan bahkan 
tidak perlu untuk mengubah apapun pada folder ios. Folder ios dan android dikelola oleh 
flutter sdk yang akan dimerge (disatukan) dengan code yang ada di folder lib untuk membuat 
aplikasi ios dan android.

5.  Folder lib

Folder lib berisi kode program dengan bahasa dart yang berupa widget yang dapat 
dibuat sesuai dengan kebutuhan aplikasi anda.

6. Folder test

Berisi source code dart yang digunakan untuk melakukan test secara otomatis pada 
aplikasi flutter.

7. Pubspec.yaml

Pada file ini berisi konfigurasi konfigurasi project flutter yang dibuat dimana anda 
dapat mendata asset berupa font, gambar dan lain lain. Pada file ini anda juga dapat 
mengkonfigurasi flutter sdk dan konfigurasi yang terkait flutter.

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