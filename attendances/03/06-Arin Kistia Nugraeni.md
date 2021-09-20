Rangkuman Pertemuan 2

Mengerjakan Aplas B1

* Membuat class Temperature, untuk mengkonversi satuan temperature.
* Membuat class Distance, untuk mengkonversi satuan jarak.
* Membuat class Weight, untuk mengkonversi satuan berat.
* Menambahkan fields dan method pada class MainActivity.
* Menambahkan methods untuk activity dan menetapkan setiap elemen dari activity.
* Menambahkan string-array resource dan membuat method RadioGroup diubah menjadi Spinner.
* Menambahkan sebuah method untuk layout konversi.
* Menambahkan methods catch element action.
* Menambahkan fungsi untuk upload gamnbar dan membuat event listener ketika formula checkbox tercentang.

Rangkuman Materi

## Activity

Activity adalah komponen yang mewakili satu window, satu tingkatan dari tampilan. Biasanya mengisi layar tapi dapat disematkan di layar activity lainnya atau muncul sebagai floating window Java class yang biasanya satu activity dalam satu file. Activity mewakili sebuah activity seperti mengirim email atau mendapatkan petunjuk arah. Activity juga menangani interaksi kepada pengguna, seperti klik tombol, input teks, atau verifikasi login. Dapat pula memulai activity lain di aplikasi yang sama atau yang lain. Activity memiliki siklus dibuat, dimulai, dijalankan, dihentikan sementara, dilajutkan, dihentikan, dan dihancurkan.

* Activity terikat longgar untuk membuat aplikasi.
* User biasanya melihat 'main activity' sebagai activity pertama.
* Activities dapat diatur dalam parent-child relationship dalam Android manifest untuk membantu navigasi.
* Activity biasanya memiliki UI layout.
* Layout biasanya didefinisikan alam satu atau lebih file XML.
* Layout activity mengembang sebagai bagian dari pembuatan.

### Implement new activities

* Mendefinisikan layout dalam XML.
* Mendefinisikan Activity Java class.
* Menghubungkan Activity dengan layout.
* Mendeklarasikan Activity dalam Android manifest.

## Intent

Intent adalah deskripsi dari sebuah operasi untuk dijalankan, merupakan sebuah objek yang digunakan untuk request sebuah aksi dari komponen aplikasi lain via sistem Android.

## Navigation

### Temporal atau Back Navigation

* Disediakan oleh tombol kembali device
* Dikontrol oleh back-stack sistem Android

### Ancestral atau Up Navigation

* Disediakan oleh bar action aplikasi
* Dikontrol dengan mendefinisikan parent-child relationship antara activity dalam Android manifest.