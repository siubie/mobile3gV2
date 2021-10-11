# :books: Rangkuman Pertemuan 5

## Aplas B3 - Multiple Activities

Setelah melakukan praktikum B3 - Multiple Activities, saya dapat memahami tentang:

1. Membuat aplikasi Android yang berisi beberapa kegiatan yang bertemakan Pertandingan Sepak Bola.
2. Dapat merancang tata letak Utama sebagai tata letak pertama yang berisi
CardView, ListView, ImageButton, TextView, EditText, dan Button.
3. Dapat mendesain tata letak Play sebagai tata letak kedua yang berisi CardView, ImageButton, ImageView, TextView, Fragment Container, dan Tombol.
4. Dapat mendesain layout Log sebagai layout ketiga yang berisi TextView, RecyclerView, dan Button.
5. Dapat mendesain layout list, layout dialog, layout match log, dan layout fragmen footer.
6. Dapat memprogram untuk MainActivity. Tugas ini akan memperkenalkan bagaimana
untuk menangani ListView, buka pemilih gambar, tampilkan dialog, dan buka
intent lain.
7. Dapat memprogram untuk PlayActivity. yang saya dapatkan yaitu:
    - cara mengumpulkan variabel lewat Intent,
    - cara menggunakan Timer dengan Handler,
    - cara menggunakan Menu Popup, dan
    - cara membuat dan mengakses Fragment.
8. Dapat memprogram untuk LogActivity. yang saya dapatkan yaitu:
    - cara mengumpulkan variabel lewat Intent,
    - cara menggunakan RecyclerView,
    - cara menggunakan adaptor Tampilan, dan
    - cara memuat array sebagai tambahan Intent.


## Aplas B4 - Multimedia Resources

Setelah melakukan praktikum B4 - Multimedia Resources, saya dapat memahami tentang:

1. Dapat membuat aplikasi Android yang berisi beberapa kegiatan yang bertajuk Animal Tour. Pertama dengan proyek konfigurasi dan konfigurasi sumber daya.
2. Dapat merancang tata letak Utama sebagai tata letak pertama yang berisi RecyclerView dengan animasi yang dapat digambar.
3. Dapat merancang tata letak Media sebagai tata letak kedua yang berisi Pemutar Video, Pemutar YouTube, dan ViewFlipper.
4. Dapat mendesain tata letak Invert sebagai tata letak ketiga yang berisi GridLayout untuk menampilkan gambar grid.
5. Dapat mendesain tata letak SubInvert sebagai tata letak keempat yang berisi detail hewan invertebrata.
6. Dapat menulis kode untuk MainActivity yang menampilkan data di RecyclerView dan membuat mereka dapat beralih secara dinamis.
7. Dapat menulis kode untuk MediaActivity yang berisi Video Pemutar, Pemutar YouTube, dan ViewFlipper. Saya juga belajar bagaimana menggunakan gesture.
8. Dapat menulis kode untuk InvertActivity yang berisi
GridLayout untuk gambar hewan Invertebrata. Saya juga bisa menulis kode untuk SubInvertActivity.

## Aplas C1 - Basic Data Storage

Setelah melakukan praktikum C1 - Basic Data Storage, saya dapat memahami tentang:

1. Dapat membuat aplikasi Android yang berisi beberapa kegiatan yang berjudul MyLibrary. Pertama dengan proyek konfigurasi dan konfigurasi sumber daya.
2. Dapat merancang tata letak Utama sebagai tata letak pertama.
3. Dapat mendesain layout Input Data.
4. Dapat mendesain Show Data Layout.
5. Dapat membuat share preferences untuk data pengguna dan data buku.
6. Dapat membuat data input dan menampilkan data dengan data binding.
7. Dapat dapat membuat model data binding.
8. Dapat membuat tombol untuk memilih warna untuk latar belakang.
9. Dapat membuat untuk mengecek data pada halaman “Input Data Activity”.
10. Dapat membuat efek di beberapa konten di halaman “ShowDataActivity”.

### Physics Based Motion
Library DynamicAnimation relatif kecil tetapi kuat. Ini berisi beberapa kelas termasuk FlingAnimation dan SpringAnimation, yang memungkinkan untuk membuat animasi berbasis Physics yang mulus pada suatu aplikasi.

### Animate Layout changes
Framework transisi Android memungkinkan Anda menganimasikan semua jenis gerakan di UI cukup dengan memberikan tata letak awal dan tata letak akhir. Anda dapat memilih jenis animasi apa yang Anda inginkan (seperti memudarkan tampilan masuk/keluar atau mengubah ukuran tampilan) dan framework transisi mencari cara menganimasikan dari tata letak awal hingga tata letak akhir.

### Pengertian MVVM
MVVM adalah sebuah pola arsitektur yang memisahkan antara user interface logic dari business logic. Tujuan penggunaan MVVM sendiri adalah menjaga kode UI agar tetap sederhana dan tanpa mengandung app logic agar mudah untuk dikelola.

#### Model
Model adalah representasi dari data dan business logic dari aplikasi. Salah satu dari strategi implementasi model adalah membuat model dapat terbuka melalui observables agar terpisah antara ViewModel atau observer/ consumer.

#### ViewModel
ViewModel berinteraksi dengan model dan juga menyiapkan observables yang akan diobservasi oleh View. ViewModel dapat menyediakan hooks untuk view dan mem-pass events kepada model.
Salah satu implementasi strategi dari ViewModel adalah untuk memisahkannya dengan View. Contohnya ViewModel tidak seharusnya mengetahui View berinteraksi dengan siapa.

#### View
Tugas dari view pada MVVM adalah untuk observe sebuah ViewModel observable untuk mendapatkan data yang akan mengupdate UI/ tampilan.

#### LiveData
LiveData adalah sebuah observable data holder yang memungkinkan components dalam sebuah aplikasi dapat observe/ mengamati objek LiveData ketika terjadi perubahan. Dengan begini LiveData object producer dengan LiveData object consumer akan terpisah.

### Flutter
Flutter adalah platform yang digunakan para developer untuk membuat aplikasi multiplatform hanya dengan satu basis coding (codebase). Artinya, aplikasi yang dihasilkan dapat dipakai di berbagai platform, baik mobile Android, iOS, web, maupun desktop. 

Flutter memiliki dua komponen penting, yaitu, Software Development Kit (SDK) dan juga framework user interface. 

- Software Development Kit (SDK) merupakan sekumpulan tools yang berfungsi untuk membuat aplikasi supaya bisa dijalankan di berbagai platform. 

- Framework UI merupakan komponen UI, seperti teks, tombol, navigasi, dan lainnya, yang dapat Anda kustomisasi sesuai kebutuhan. 

Flutter juga merupakan platform yang gratis dan open source. Jika Anda ingin menggunakan Flutter, Anda perlu mempelajari bahasa pemrograman Dart. Berbeda dengan framework front-end pada umumnya yang menggunakan JavaScript sebagai bahasa pemrogramannya.

#### Kelebihan Framework Flutter dan Mengapa Anda Harus Menggunakannya?
1. Pengembangan Aplikasi Lebih Mudah dan Cepat 
2. Custom User Interface yang Menarik
3. Performa seperti Aplikasi Native 
4. Biaya Pengembangan Lebih Hemat 

#### Kekurangan Framework Flutter 
1. Library Pihak Ketiga yang Belum Banyak 
2. Aplikasi yang Dihasilkan Berukuran Besar 
3. Perlu Belajar Bahasa Pemrograman Baru