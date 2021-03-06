# :books: Rangkuman Pertemuan 8

## BAB 4. Statefull Widget dan Map

Setelah melakukan jobsheet aplikasi dengan statefull widget, saya dapat memahami tentang:

1. Cara desain aplikasi dengan menggunakan flutter
2. Dapat mengetahui pengertian dan penggunaan list
3. Dapat menambahkan dropdown widget pada aplikasi flutter sebelumnya
4. Dapat mengetahui fungsi dari Map
5. Dapat menambahkan list view widget pada aplikasi flutter sebelumnya

### List

Sebelum masuk pada praktikum akan dijelaskan pengantar tentang List pada Dart. List adalah collection yang seperti pada bahasa pemrograman yang lain. Pada bahasa pemrograman Dart, array adalah list of object sehingga disebut juga dengan list. Berikut ini adalah contoh list pada Dart

``` dart
//contoh list of integer
var list = [1, 2, 3];
//contoh list of string
var list = [ 'Car', 'Boat', 'Plane', ];
```

List pada Dart mengguna index 0 sebagai nilai awal dan list.length – 1 adalah index nilai terakhir dari sebuat list. List pada Dart mengguna index 0 sebagai nilai awal dan list.length – 1 adalah index nilai terakhir dari sebuat list.

```dart
var list = [1, 2, 3];
print(list.length == 3);
print (list[1] == 2);
```

Untuk membuat list pada saat compile time dapat menggunakan const

```dart
var constantList = const [1, 2, 3];
```

Mulai Dart 2.3 dikenalkan spread operator (…) dan null-aware spread operator (…?) yang digunakan insert banyak nilai ke collection. Contohnya pada source code di bawah ini, digunakan untuk memasukkan nilai dari list ke list2.

```dart
var list = [1, 2, 3];
var list2 = [0, ...list];
print(list2.length == 4);
```

Anda juga dapat menggunakan null-aware spread operator untuk menghindari exception ketika list bernilai null.

```dart
var list;
var list2 = [0, ...?list];
print(list2.length == 1);
```

Dart juga menyediakan collection if dan collection for yang digunakan untuk membuat collection dengan kondisi dan repetisi / perulangan. Berikut adalah contoh collection if untuk membuat list yang terdiri dari 3 atau 4 item sesuai dengan kondisi.

```dart
var nav = [
 'Home',
 'Furniture',
 'Plants',
 if (promoActive) 'Outlet'
];
```

Berikut adalah contoh collection for untuk memanipulasi list item sebelum ditambahkan pada list yang lain.

```dart
var listOfInts = [1, 2, 3];
var listOfStrings = [
 '#0', for (var i in listOfInts) '#$i'
];
print (listOfStrings[1] == '#1');
```