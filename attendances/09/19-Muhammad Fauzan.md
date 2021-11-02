# Rangkuman Pertemuan 9
- Mengerjakan Praktikum Flutter Chapter 4, menambahkan Dropdown Widget.

## List
List adalah collection yang seperti pada bahasa pemrograman yang lain. Pada bahasa pemrograman Dart, array adalah list of object sehingga disebut juga dengan list.

Contoh :
```
//contoh list of integer
var list = [1, 2, 3];

//contoh list of string
var list = [ 'Car', 'Boat', 'Plane', ];
```
List pada Dart menggunakan index 0 sebagai nilai awal dan list.length – 1 adalah index nilai terakhir dari sebuat list.

List pada Dart menggunakan index 0 sebagai nilai awal dan list.length – 1 adalah index nilai terakhir dari sebuat list.

Dart juga menyediakan collection if dan collection for yang digunakan untuk membuat collection dengan kondisi dan repetisi / perulangan. Berikut adalah contoh collection if untuk 
membuat list yang terdiri dari 3 atau 4 item sesuai dengan kondisi.

Contoh Collection if :
```
var nav = [
 'Home',
 'Furniture',
 'Plants',
 if (promoActive) 'Outlet'
];
```
Contoh Collection for untuk memanipulasi list item sebelum ditambahkan 
pada list yang lain :
```
var listOfInts = [1, 2, 3];
var listOfStrings = [
 '#0', for (var i in listOfInts) '#$i'
];
print (listOfStrings[1] == '#1');
```
## Menambahkan Dropdown Widget
Dapat diamati pada source code dropdown items merupakan list yang terdiri dari DropdownMenuItem Widget. Hal ini akan tidak efektif karena code kita akan panjang jika 
terdapat banyak item yang harus dimasukkan ke items. Hal ini dapat ditangani dengan menggunakan fungsi map pada list.
```
DropdownButton<String>
```
String digunakan untuk memberi tipe data value dari Dropdown adalah bertipe String.
```
listItem.map((String value)
```
Digunakan untuk melakukan iterasi untuk setiap item dari listItem sesuai dengan parameter bertipe String.
