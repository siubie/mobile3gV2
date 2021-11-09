
Struktur Project Flutte

Ketika membuat project flutter secara default berikut adalah struktur folder dan 
filenya. Dapat kita lihat strukturnya terdiri dari .dart_tool, .idea, android, ios, lib, test, 
.gitignore, .metadata, .packages, .flutter_basic.iml, pubspec.lock, pubspec.yaml, 
README.md.

Penjelasan tentang struktur files dari flutter :
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


Untuk struktur folder

Multi os ios dan android
Perhatikan pada folder project flutter terdapat dua folder yaitu folder ios dan folder 
android, dengan menggunakan kedua folder tersebut flutter dapat membuat aplikasi berbasis 
ios dan berbasis android dalam satu project.

Folder android
Folder android berisi file file pendukung untuk mengenerate project android dan akan 
dikompilasi menjadi sebuah apk pada folder build. Namun anda jarang atau bahkan tidak 
perlu mengedit yang ada di folder android. Anda akan banyak bekerja di folder lib.

Folder ios
Berisi project ios, folder ini sama dengan folder android, sangat jarang dan bahkan 
tidak perlu untuk mengubah apapun pada folder ios. Folder ios dan android dikelola oleh 
flutter sdk yang akan dimerge (disatukan) dengan code yang ada di folder lib untuk membuat 
aplikasi ios dan android.

Folder lib
Folder lib berisi kode program dengan bahasa dart yang berupa widget yang dapat 
dibuat sesuai dengan kebutuhan aplikasi anda.

Folder test
Berisi source code dart yang digunakan untuk melakukan test secara otomatis pada 
aplikasi flutter.

Pubspec.yaml
Pada file ini berisi konfigurasi konfigurasi project flutter yang dibuat dimana anda 
dapat mendata asset berupa font, gambar dan lain lain. Pada file ini anda juga dapat 
mengkonfigurasi flutter sdk dan konfigurasi yang terkait flutter.
