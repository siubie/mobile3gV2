## Pertemuan 6

mencoba flutter chapter 3, yaitu belajar mengenai cara pembuatan aplikasi sederhana yang memiliki statefull widget. 
Untuk pembuatan aplikasi Konversi Suhu dimulai dengan membuat sebuah desain yang dapat dimulai dengan membuat wireframe atau desain utuh di perangkat lunak. 
Untuk menyederhanakan proses desain sudah disediakan template sederhana di starter code dengan menggunakan template material design.

Mempelajari untuk mempermudah proses konversi desain ke stateless widget yang sudah di contohkan dan sudah di representasikan menjadi sebuah tree layout pada jobsheet flutter chapter 3.

Mempelajari shortcut pada Visual Studio Code yaitu shortcut CTRL + . yang dapat digunakan untuk membungkus widget yang sudah ada atau untuk membuat widget yang telah dibuat menjadi class baru.

Mempelajari cara agar pada TextField hanya memiliki tampilan input keyboard khusus angka dan memiliki validasi hanya angka.

Mempelajari untuk mengambil data inputan user yang berada di TextField menggunakan TextEditingController. Mengetahui cara membuat function yang dapat dipanggil nantinya.

Mempelajari tentang penggunaan pemisahan widget kedalam class baru dan di pindahkan ke file baru, sehingga pada main.dart tidak terlalu panjang kode baris pemogramannya.

Mempelajari membuat sebuah event untuk mengkonversi suhu, dimana pada event tersebut terdapat rumus untuk mengkonversi suhu. 
Hasil konversi harus diubah menjadi double karena yang diinput oleh user berupa string.

## Stateless Widget
Stateless widget bersifat statis / final dimana nilai atau konfigurasi telah diinisiasi sejak awal, nilai variabel pada widget ini tidak dapat diubah oleh widget ini sendiri 
tetapi dapat diubah oleh parent widget nya jika parent nya adalah StatefullWidget
Struktur dasar stateless widget adalah sebagai berikut:

```java 
class exampleStateless extends StatelessWidget{
 @override
 Widget build(BuildContext context) {
 
 }
}
```


## Statefull Widget

Statefull widget bersifat dinamis, widget ini dapat diperbarui ketika dibutuhkan sesuai 
dengan action pengguna atau jika ada ada perubahan data. Perubahan data pada statefull 
widget di trigger oleh perubahan state oleh karena itu sebuah StatefullWidget selalu memiliki State
Struktur dasar statefull widget adalah sebagai berikut:
```java
class exampleStateless extends StatefulWidget{
 @override
 State<StatefulWidget> createState() {
 }
}
```
