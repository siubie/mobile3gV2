Rangkuman Pertemuan 7 :

# Mengerjakan Praktikum 2 Aplikasi Flutter 

1. Struktur folder
    - .dart_tools : Konfigurasi untuk dart language
    - .idea : Konfigurasi untuk android studio
    - gitignore : File git yang digunakan untuk mengelola source code. Hal ini akan berguna jika developer sudah bekerja dengan git.
    - metadata : File yang berisi metadata dari project
    - packages : File yang berisi alamat path
    - flutter_basic.iml: File yang berisi detail dari project.
    - pubspec.lock : File yang berisi versi library atau package yang digunakan pada project yang degenerate sesuai dengan file pubspec.yaml.
    - pubspec.yaml : File yang berisi library atau package yang dibutuhkan untuk pengembangan aplikasi.
    - Readme.md : File markdown yang dapat digunakan untuk menjelaskan cara setup aplikasi atau informasi penting yang perlu untuk diketahui oleh developer lain. 
2.  Import Statement
    - Digunakan untuk mengimport package, library, atau file lain yang digunakan pada file yang dieksekusi.
    ```java
    import 'package:flutter/material.dart';

3.  Main function
    - Semua proses aplikasi dimulai dari mengeksekusi fungsi main.
    ```java
    void main() {
        runApp(MyApp());
    }

4. Stateless Widget
    - Stateless widget bersifat statis / final dimana nilai atau konfigurasi telah diinisiasi sejak awal, nilai variabel pada widget ini tidak dapat diubah oleh widget ini sendiri tetapi dapat diubah oleh parent widget nya jika parent nya adalah StatefullWidget.
    ```java
    class exampleStateless extends StatelessWidget{
        @override
        Widget build(BuildContext context) {
        }
    }

5. Statefull Widget
    - Statefull widget bersifat dinamis, widget ini dapat diperbarui ketika dibutuhkan sesuai dengan action pengguna atau jika ada ada perubahan data. Perubahan data pada statefull widget di trigger oleh perubahan state oleh karena itu sebuah StatefullWidget selalu memiliki State.
    ```java
    class exampleStateless extends StatefulWidget{
        @override
        State<StatefulWidget> createState() {
        }
    }

# Mengerjakan Praktikum 3 Aplikasi Dengan Stateful Widget

1. Mengerjakan Konversi Desain Ke StatelessWidget
    ```java
    import 'package:flutter/material.dart';
    import 'package:flutter/services.dart';
    void main() {
        runApp(MyApp());
    }
    
    class MyApp extends StatelessWidget {
        @override
        Widget build(BuildContext context) {
            return MaterialApp(
                title: 'Flutter Demo',
                theme: ThemeData(
                    primarySwatch: Colors.blue,
                    visualDensity: VisualDensity.adaptivePlatformDensity,
                ),
                home: Scaffold(
                    appBar: AppBar(
                    title: Text("Konverter Suhu"),
                    ),
                    body: Container(),
                ),
            );
        }
    }

2. Memodifikasi pada TextFormField agar memiliki hint dengan text “Masukkan Suhu Dalam Celcius”

3. Memodifikasi pada TextFormField agar memiliki validasi hanya angka.

4. Memodifikasi pada TextFormField agar memiliki tampilan input keyboard khusus angka. 