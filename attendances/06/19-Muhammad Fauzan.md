## Rangkuman Pertemuan 6
- Mengerjakan Praktikum Flutter Chapter 1 dan 2.

### Struktur Flutter

#### Struktur Folder
Ketika membuat project flutter secara default berikut adalah struktur folder dan filenya. Dapat kita lihat 
strukturnya terdiri dari .dart_tool, .idea, android, ios, lib, test, .gitignore, .metadata, .packages, .flutter_basic.iml, pubspec.lock, pubspec.yaml, 
README.md.

#### Flutter Hot Reload
Pada flutter terdapat fungsi hot reload dan hot restart yang digunakan untuk pengembangan aplikasi dengan flutter. 
Hote reload mencompile source code yang baru ditambahkan dan dikirimkan ke dart virtual machine diupdate. 
Setelah selesai update, dart virtual machine akan memperbarui UI sesuai dengan perubahan. Keunggulan hot reload 
adalah waktu prosenya cepat disbanding hot restart. Akan tetapi hot reload mempertahan state yang ada sehingga jika 
menggunakan state maka nilai dari widget tidak akan berubah.

#### Flutter Hot Restart
Hot restart akan mencompile ulang aplikasi dan mereset (destroy) state yang ada. Jadi hot restart akan membuild ulang widget 
tree sesuai dengan code yang telah diperbarui.

#### Stateless Widget
Flutter menggunakan Widget sebagai elemen elemen pembangun UI, widget ini adalah kode program yang diterjemahkan 
menjadi tampilan yang dapat dilihat dan diinteraksikan oleh pengguna. Stateless widget bersifat statis / final 
dimana nilai atau konfigurasi telah diinisiasi sejak awal, nilai variabel pada widget ini tidak dapat diubah 
oleh widget ini sendiri tetapi dapat diubah oleh parent widget nya jika parent nya adalah StatefullWidget. 

Contoh :
```
class MyApp extends StatelessWidget {

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Belajar Flutter',
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        appBar: AppBar(
          centerTitle: true,
          title: Text('Stateless Widget'),
        ),
        body: Center(
          child: Text('Muhammad Fauzan', style: TextStyle(fontSize: 30)),
        ),
      )
    );
  }
}
```

#### Statefull Widget
Statefull widget bersifat dinamis, widget ini dapat diperbarui ketika dibutuhkan sesuai dengan action pengguna 
atau jika ada ada perubahan data. Perubahan data pada statefull widget di trigger oleh perubahan state 
oleh karena itu sebuah StatefullWidget selalu memiliki State. 

Contoh :
```
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
