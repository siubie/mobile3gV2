# Rangkuman Pertemuan 8
- Instalasi ekstensi Visual Studio Code yaitu WakaTime
- Menambah suhu Fahrenheit pada aplikasi konversi suhu

### Konversi Desain ke StatelaessWidget
Flutter menggunakan Widget sebagai elemen elemen pembangun UI, widget ini adalah kode program yang diterjemahkan 
menjadi tampilan yang dapat dilihat dan diinteraksikan oleh pengguna. Stateless widget bersifat statis / final 
dimana nilai atau konfigurasi telah diinisiasi sejak awal, nilai variabel pada widget ini tidak dapat diubah 
oleh widget ini sendiri tetapi dapat diubah oleh parent widget nya jika parent nya adalah StatefullWidget.

Untuk mempermudah proses konversi dari desain ke stateless widget perlu memperhatikan item-item yang ada pada desain tersebut, apa saja widget yang terlibat dan apa saja widget 
layout yang digunakan. Sekilas dari UI desain konversi suhu bahwa terdapat satu input text, empat text, dan satu buah button. 
Secara lebih dalam perhatikan karakteristik item-item tersebut seperti hint pada input, ukuran text yang berbeda, warna text pada tombol dan ukuran tombol yang memenuhi 
lebar layar. Perhatikan juga bagaimana UI pada desain tersebut disusun dalam cara pandang row  dan column, secara sederhana aplikasi ini terdiri dari satu kolom dan tiga baris 
dimana baris pertama berisi input, baris kedua berisi info suhu dan nilainya, serta baris ketiga berisi sebuah button. Khusus pada baris kedua terbagi menjadi dua buah kolom 
yang memiliki dua buah text.

### Membuat Aplikasi Interaktif
Setelah berhasil membuat layout selanjutnya adalah membuat aplikasi yang mamapu melakukan konversi suhu dari input berupa derajat celcius ke tiga derajat lain yaitu kelvin, 
reamur dan fahrenheit.

#### Konversi Desain ke StatefullWidget
Statefull widget bersifat dinamis, widget ini dapat diperbarui ketika dibutuhkan sesuai dengan action pengguna atau jika ada ada perubahan data. 
Perubahan data pada statefull widget di trigger oleh perubahan state oleh karena itu sebuah StatefullWidget selalu memiliki State. 

#### Membuat State
Dalam Reactive Framework seperti Flutter, kita bisa membuat UI sebagai return value function(state) UI dari sebuah function dimana function tersebut 
dipanggil dengan 1 argumen yaitu adalah state. Jadi, State adalah sebuah data yang bisa berubah dengan / seperti lifecycle didalam aplikasi yang dibuat.

### Membagi Ke Widget Yang Lebih Kecil
Membagi isi dari main.dart menjadi widget yang lebih sederhana sehingga mudah untuk di maintain dan di perbaiki.
