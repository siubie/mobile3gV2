# Rangkuman Pertemuan 7

##  bab 3 - Aplikasi dengan Stateful Widget

## Stateful widget

Stateful widget merupakan suatu widget yang sifatnya dinamis atau dapat berubah-ubah, kebalikan dari stateless widget.

Apa saja yang dapat berubah pada stateful widget?

Stateful widget dapat mengubah atau mengupdate tampilan, menambah widget laiinya, mengubah nilai variabel, icon, warna dan masih banyak lagi.

Kapan stateful widget dapat melakukan perubahan??

Stateful widget dapat mengubah dirinya kapanpun dibutuhkan berdasarkan action dari pengguna atau bahkan ketika terjadi perubahan data dari sisi database.

Masih menggunakan contoh yang sama seperti pada stateless hanya saja kita dapat mengubah nilai yang ada pada body sesuka kita berdasarkan action dari pengguna.

contoh kode :

```
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatefulWidget {
  @override
  _MyAppState createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  int _angka = 1;

  void _increment(){
    setState(() {
      _angka += 1;
    });
  }
 
 @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Belajar Flutter',
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        floatingActionButton: FloatingActionButton(
          child: Icon(Icons.add),
          onPressed: ()=>_increment(),
        ),
        appBar: AppBar(
          centerTitle: true,
          title: Text('Stateful Widget'),
        ),
        body: Center(
          child: Text('Angka : $_angka', style: TextStyle(fontSize: 30)),
        ),
      )
    );
  }
}
```

## Send Parameter ke Child

Sebuah widget dapat mengirim paramter ke child widgetnya melalui constructor yang
dimiliki oleh widget tersebut parameter ini dapat menyesuaikan dengan kebutuhan yang
dimiliki oleh widget tersebut

contoh kode :

```
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

## Send Event Handler Ke Child

Widget parent juga dapat mengirim fungsi turu
```
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

contoh kode :

```
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