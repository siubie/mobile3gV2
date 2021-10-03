# :books: Rangkuman Pertemuan 5

- Mengerjakan Aplas B3, B4, C1, dan perkenalan Flutter 

### Penjelasan

#### Pengantar animasi
Animasi dapat menambahkan isyarat visual yang memberi tahu pengguna tentang apa yang terjadi di aplikasi Anda. Fitur ini berguna terutama saat status UI berubah, 
misalnya saat konten baru dimuat atau tindakan baru tersedia. Animasi juga berperan memperindah aplikasi Anda, sehingga memberikannya penampilan dan kesan yang lebih berkualitas.
Android menyertakan berbagai API animasi sesuai dengan jenis animasi yang Anda inginkan, 
maka halaman ini akan memberikan ringkasan berbagai cara yang dapat Anda gunakan untuk menambahkan gerakan ke UI Anda.

#### Menganimasikan bitmap
Saat ingin menganimasikan grafik bitmap seperti ikon atau ilustrasi, Anda harus menggunakan API animasi yang dapat digambar. Biasanya, 
animasi tersebut didefinisikan secara statis dengan resource yang dapat digambar, tetapi Anda juga dapat menentukan perilaku animasi saat waktu proses.
Misalnya, menganimasikan tombol putar agar berubah menjadi tombol jeda saat diketuk adalah cara yang baik untuk mengomunikasikan kepada pengguna 
bahwa kedua tindakan tersebut terkait, dan dengan menekan salah satunya akan membuat yang lain terlihat.

#### Menganimasikan gerakan dan visibilitas UI
Jika Anda perlu mengubah visibilitas atau posisi tampilan di tata letak, Anda harus menyertakan animasi halus untuk membantu pengguna memahami perubahan yang akan terjadi pada UI.
Untuk memindahkan, menampilkan, atau menyembunyikan tampilan dalam tata letak saat ini, Anda dapat menggunakan sistem animasi properti yang disediakan oleh paket ```android.animation```,
tersedia di versi Android 3.0 (API level 11) dan versi yang lebih tinggi. API tersebut akan memperbarui properti objek View Anda selama periode waktu tertentu, 
terus-menerus menggambar ulang tampilan saat properti berubah. Misalnya, ketika mengubah properti posisi, tampilan akan bergerak melintasi layar, 
atau saat Anda mengubah properti alfa, tampilan akan menjadi jelas atau memudar.

#### Data Binding
Data Binding adalah support library yang memungkinkan Anda mengikat komponen UI dalam tata letak ke sumber data di aplikasi Anda menggunakan format deklaratif, bukan secara terprogram.
Tata letak sering ditentukan dalam aktivitas dengan kode yang memanggil metode framework UI. Misalnya, kode di bawah ini memanggil ```findViewById()```
untuk menemukan widget ```TextView``` dan mengikatnya ke properti ```userName``` variabel ```viewModel```:

```
    TextView textView = findViewById(R.id.sample_text);
    textView.setText(viewModel.getUserName());
```

Contoh berikut menunjukkan cara menggunakan Library Data Binding untuk menetapkan teks ke widget secara langsung dalam file tata letak. 
Dengan cara ini, Anda tidak perlu lagi memanggil salah satu kode Java yang ditampilkan di atas. Perhatikan penggunaan sintaks ```@{}``` dalam ekspresi penetapan:

```
<TextView
        android:text="@{viewmodel.userName}" />
```

#### Flutter
Flutter adalah sebuah framework open source yang dibuat oleh Google. Google membuat flutter dengan tujuan membangun sebuah framework untuk membuat UI yang modern, native
dan reactive yang dapat berjalan di sistem operasi iOS maupun Android. Tidak hanya pada smartphone google juga membuat flutter untuk desktop, web dan embedded device.

Flutter diprogram dengan menggunakan bahasa Dart sebuah bahasa moderen yang dapat dicompile ke arsitektur processor ARM atau javascript. Flutter menggunakan Skia 2D
rendering engine yang dapat bekerja pada hardware atau software yang berbeda platform. Dart menggunakan metode compilasi ahead of time (AOT) untuk mengubah kode Dart
menjadi kode native untuk sistem operasi yang digunakan, oleh karena itu aplikasi yang dibangun menggunakan flutter memiliki kecepatan yang hampir sama dengan aplikasi native.
Dart juga menggunakan konsep just-in-time (JIT) sehingga memungkinkan programmer dapat membuat perubahan pada kode program dan langsung melihat hasilnya melalui fitur hot
reaload yang dimiliki Flutter.

Flutter menggunakan Dart untuk membuat User Interface, sehingga memudahkan dalam membuat aplikasi karena menggunakan satu bahasa (Dart) dalam pembuatan UI maupun logika
program. Flutter menggunakan pendekatan declarative dimana Flutter membangun UI mengikuti “State” yang dimiliki oleh aplikasi. Ketika state berubah maka UI akan digambar ulang.
