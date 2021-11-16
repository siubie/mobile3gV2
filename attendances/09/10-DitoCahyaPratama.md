# :books: Rangkuman Pertemuan 9

## BAB 5. Navigasi dan Route

Setelah melakukan jobsheet navigasi dan route, saya dapat memahami tentang:

1. Cara desain aplikasi dengan menggunakan flutter
2. Dapat mengetahui pengertian dan penggunaan navigator
3. Dapat mengetahui pengertian dan penggunaan route
4. Dapat melakukan pengiriman data ke halaman yang dituju
5. Dapat melakukan pembacaan data dari data yang dikirim dari halaman sebelumnya

### Navigator
Navigator: sebuah widget yang mengatur tumpukan (struktur data stack) dari obyek rute.

Widget Navigator bekerja seperti tumpukan layar (stack), ia menggunakan prinsip LIFO (Last-In, First-Out). Ada dua method yang dapat digunakan pada Navigator widget yaitu :

- Navigator.push (): Metode push digunakan untuk menambahkan rute lain ke atas tumpukan screen (stack) saat ini. Halaman baru ditampilkan di atas halaman sebelumnya.
- Navigator.pop (): Metode pop menghapus rute paling atas dari tumpukan. Ini menampilkan halaman sebelumnya kepada pengguna.

### Route
Route: sebuah obyek yang merepresentasikan tampilan, umumnya diimplementasikan oleh class seperti MaterialPageRoute.

Sebuah Route umumnya dimasukkan (push) atau diambil (pop) dari dan ke tumpukan Navigator. Ketika sebuah halaman dilakukan operasi push, maka halaman tersebut akan  diletakkan di atas halaman yang memanggilnya.

Dan jika pop dipanggil (tombol back ditekan) maka aplikasi akan menampilkan halaman sebelumnya. Selain itu Flutter juga mendukung adanya penamaan Route yang didefinisikan di awal.

### Pengiriman data
Untuk melakukan pengiriman data ke halaman berikutnya, cukup menambahkan informasi arguments pada penggunaan Navigator. Perbaharui kode pada bagian Navigator menjadi berikut.

```dart
Navigator.pushNamed(context, '/item', arguments: item);
```

### Pembacaan data
Pembacaan nilai yang dikirimkan pada halaman sebelumnya dapat dilakukan menggunakan ModalRoute. Tambahkan kode berikut pada blok fungsi build dalam halaman ItemPage. Setelah nilai didapatkan, anda dapat menggunakannya seperti penggunaan variabel pada umumnya.

```dart
final Item itemArgs = ModalRoute.of(context).settings.arguments;
```