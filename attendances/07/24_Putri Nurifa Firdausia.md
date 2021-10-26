## Pertemuan 7

Pada zoom meeting mereview materi yang ada di modul dan setiap mahasiswa menjelaskan apa yang sudah dipelajari selama satu minggu.
Kemudia dilakukan sesi tanya jawab antara dosen dengan mahasiswa. 
kemudian kita harus mempelajari modul terlebih dahulu sebelum kelas dimulai
kemudian melanjutkan chapter 3 dan mempelajari lebih lanjut tentang flutter. 

## Aplikasi dengan statefull widget

Untuk pembuatan aplikasi ini dimulai dengan membuat 
sebuah desain yang dapat dimulai dengan membuat wireframe atau desain utuh di perangkat 
lunak seperti adobe xd atau sketch dan yang lain

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

## Membuat State

Untuk membuat state tambahkanlah kode program yang menurut anda perlu ditambahkan 
berikut ini contoh kode program pada state dari widget MyApp yang sekarang berubah 
menjadi statefull widget.

```java
class _MyAppState extends State<MyApp> {
 //variabel berubah
 double _inputUser = 0;
 double _kelvin = 0;
 //tambahkan variabel lain yang dibutuhkan
 ```

## Membagi ke Widget yang lebih kecil

Lakukan lah extraksi widget ke file yang berbeda dengan cara Ctrl + . pada widget 
yang ingin anda potong dan pilih menu Extract Widget, berikanlah nama class yang sesuai 
dan pindahkan ke file baru.
Berikut ini nama nama widget dan ekstraksi yang dapat dicontoh :
1. Input : Berisi Widget TextFormField dan controller nya
2. Result : Berisi widget hasil konversi yang memiliki variabel nama dan hasil.
3. Convert : Berisi button dan reference ke function yang digunakan untuk 
melakukan setState()

## Send Parameter ke child

Sebuah widget dapat mengirim paramter ke child widgetnya melalui constructor yang 
dimiliki oleh widget tersebut parameter ini dapat menyesuaikan dengan kebutuhan yang 
dimiliki oleh widget terssebut. Berikut ini contoh pembuatan widget dan constructor dari 
widget yang dibuat.

```java 
Input(etInput: etInput),
class Input extends StatelessWidget {
 const Input({
 Key key,
 @required this.etInput,
 }) : super(key: key);
 final TextEditingController etInput;
 @override
 Widget build(BuildContext context) {
 return TextFormField(
 decoration: InputDecoration(hintText: "Masukkan Suhu Dalam Celcius"),
 inputFormatters: [FilteringTextInputFormatter.digitsOnly],
 controller: etInput,
 keyboardType: TextInputType.number,
 );
 }
}
```

## Send Event ke child

Selain mengirimkan parameter ke child widget parent juga dapat mengirim fungsi turun 
ke child widget dimana fungsi ini akan dipanggil lagi oleh parent widget yang memiliki state. 
Berikut ini contoh kode program untuk menurunkan fungsi ke child widget.

```java
Convert(konvertHandler: _konversiSuhu),
class Convert extends StatelessWidget {
 final Function konvertHandler;
 Convert({Key key, @required this.konvertHandler});
 @override
 Widget build(BuildContext context) {
 return Container(
 width: double.infinity,
 height: 50,
 child: RaisedButton(
 onPressed: konvertHandler,
 color: Colors.blueAccent,
 textColor: Colors.white,
 child: Text("Konversi Suhu"),
 ),
 );
 }
}
```
 
 ## Membuat Event
event perhitungan konversi dan 
update hasil konversi dilakukan saat tombol Konversi ditekan

## Dialog
Dialog widget pada flutter memiliki dua jenis dialog yaitu AlertDialog dan 
SimpleDialog. Contoh penggunaan AlertDialog widget pada source code dan ouputnya 
adalah sebagai berikut:
```java 
class MyApp extends StatelessWidget {
 int _count = 0;
 @override
 Widget build(BuildContext context) {
 return MaterialApp(
 
 home: Scaffold(
 body:MyLayout(),
 ),
 );
 }
}
class MyLayout extends StatelessWidget {
 @override
 Widget build(BuildContext context) {
 return Padding(
 padding: const EdgeInsets.all(8.0),
 child: RaisedButton(
 child: Text('Show alert'),
 onPressed: () {
 showAlertDialog(context);
 },
 ),
 );
 }
}
showAlertDialog(BuildContext context) {
 // set up the button
 Widget okButton = FlatButton(
 child: Text("OK"),
 onPressed: () { },
 );
 // set up the AlertDialog
 AlertDialog alert = AlertDialog(
 title: Text("My title"),
 content: Text("This is my message."),
 actions: [
 okButton,
 ],
 );
 // show the dialog
 showDialog(
 context: context,
 builder: (BuildContext context) {
 return alert;
 },
 );
}
```

## Input dan Selection Widget
Flutter menyediakan widget yang dapat menerima input dari pengguna aplikasi yaitu 
antara lain Checkbox, Date and Time Pickers, Radio Button, Slider, Switch, TextField.
Contoh penggunaan TextField widget pada source code dan ouputnya adalah sebagai beriku

```java 
class MyApp extends StatelessWidget {
 @override
 Widget build(BuildContext context) {
 return MaterialApp(
 
 home: Scaffold(
 appBar: AppBar(
 title: Text("Contoh TextField")
 ),
 body: TextField(
 obscureText: false,
 decoration: InputDecoration(
 border: OutlineInputBorder(),
 labelText: 'Nama',
 ),
 ),
 ),
 );
 }
}
```

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

