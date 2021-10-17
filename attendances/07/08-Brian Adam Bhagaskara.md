# Presensi Pertemuan 7
## Cara Menampilkan Gambar di Flutter

### Gambar dari Assets lokal
Gambar dari asset lokal yaitu file gambar yang ditambahkan kedalam folder aplikasi yang nantinya digunakan untuk menampilkan gambar tanpa koneksi internet. Tahapan menampilkan gambar lokal yaitu :

1. buat folder baru assets/images
posisi folder sejajar dengan pubspec.yaml. Untuk penamaan folder bisa apa aja namun sebaiknya gunakan nama yang umum pada istilah pemrograman. Hal tersebut berguna untuk membantu orang lain apabila bekerja sebagai tim.

2. Masukan gambar ke dalam folder tersebut.

3. Registrasikan image / gambar yang tadi kita masukan dengan cara edit file pubspec.yaml

```
flutter:   
  assets:     
    - assets/images/paddy-field.jpg
```

Jika memiliki beberapa gambar yang ingin di import maka kita dapat menggunakan cara yang lebih sederhana yaitu hanya menggunakan nama direktori saja.

```
flutter:   
  assets:     
    - assets/images/
```

4. Tampilkan asset image dengan Image.asset Widget

```
Image.asset('assets/images/paddy-field.jpg');
```

Contoh lengkapnya seperti kode dibawah ini
```
import 'package:flutter/material.dart';

void main() => runApp(BelajarImage());

class BelajarImage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text("belajarFlutter.com"),
        ),
        body: Image.asset('assets/images/paddy-field.jpg'),
      )
    );
  }
}
```

Format gambar yang support yaitu : JPEG, WebP, GIF, animated WebP/GIF, PNG, BMP, and WBMP. Penggunaan local image biasanya untuk gambar yang bersifat statis seperti logo aplikasi, background asset. Semakin banyak gambar yang di import maka semakin besar pula ukuran aplikasinya nanti

### Gambar dari Internet

Menampilkan gambar dari internet lebih mudah dari local asset karena tidak perlu mengatur folder seperti local image. Cukup dengan menggunakan Image.network dan masukan url nya maka sudah selesai.

```
Image.network('https://cdn.pixabay.com/photo/2019/11/10/17/36/indonesia-4616370_1280.jpg');
```

Meskipun lebih mudah menggunakan network namun menampilkan gambar memiliki tantangan tersendiri yaitu :

1. Setiap load image akan membutuhkan kuota / koneksi internet
2. Apabila internet terputus maka gambar akan blank dan error

Untuk mengurangi permintaan download image secara berulang pada gambar yang sudah pernah di load maka gunakan cache. Cache berguna untuk menyimpan gambar yang sudah di load secara temporary atau sementara.

## Cara menggunakan cache Network Image

1. install package cached_network_image dengan cara tambahkan di pubspec.yaml

```
dependencies:
  cached_network_image: ^2.2.0+1
 ```

2. import package

```
import 'package:cached_network_image/cached_network_image.dart';
```

3. tambahkan CachedNetworkImage pada Image widget kurang lebih seperti ini

```
child: Image(
    image: CachedNetworkImageProvider("https://cdn.pixabay.com/photo/2019/11/10/17/36/indonesia-4616370_1280.jpg")
)
```

Agar layout tidak menjadi berantakan sebaikanya tambahkan placeholder dan tampilan error saat terjadi kesalahan seperti koneksi bermasalah atau url yang salah dengan cara seperti ini

```
CachedNetworkImage(
  imageUrl: "https://cdn.pixabay.com/photo/2019/11/10/17/36/indonesia-4616370_1280.jpg",
  placeholder: (context, url) => CircularProgressIndicator(),
  errorWidget: (context, url, error) => Text("Koneksi Error"),
),
```

Dengan menggunakan kode diatas maka saat image belum ter-load maka akan muncul progress bar. Dan apabila terjadi error akan menampilkan text “Koneksi Error”. Baik progress bar maupun errorWidget kita dapat mengganti dengan image, icon atau widget lainnya.

Contoh kode lengkapnya seperti dibawah ini :

```
import 'package:flutter/material.dart';
import 'package:cached_network_image/cached_network_image.dart';
void main() {
  runApp(MaterialApp(
    title: "BelajarFlutter.com",
    home: BelajarGambarNetwork(),
  ));
}
class BelajarGambarNetwork extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("Belajar Flutter"),
      ),
      body: Center(
        child: CachedNetworkImage(
          imageUrl:
              "https://cdn.pixabay.com/photo/2019/11/10/17/36/indonesia-4616370_1280.jpg",
          placeholder: (context, url) => CircularProgressIndicator(),
          errorWidget: (context, url, error) => Text("Koneksi Error"),
        ),
      ),
    );
  }
  ```

 ## Mengatur ukuran tinggi dan lebar gambar
 
 Untuk mengatur tinggi dan lebar gambar, kita dapat menggunakan properti height untuk tinggi dan width untuk lebar. penggunaanya seperti dibawah ini

 ```
 body: Image.asset(
  'assets/images/paddy-field.jpg',
  height: 100,
  width: 200,
),
 ```

## Manipulasi Warna Gambar

Pada widget Image, kita juga dapat memanipulasi warna gambar dengan properti colorBlendMode penggunaan properti ini biasanya digabungkan dengan properti color. Contoh kodenya dan hasil tampilannya seperti ini

 ```
body: Column(children: <Widget>[
  Image.asset('assets/images/paddy-field.jpg'), // tanpa BlendMode
  Image.asset('assets/images/paddy-field.jpg', // dengan BlendMode
      color: Colors.grey,
      colorBlendMode: BlendMode.hue),
]),
 ```

Image Widget : Properti Lainnya

Beberapa fungsi yang bisa dijalankan dari penggunaan Image BoxFit ini diantaranya yaitu

- contain :	Untuk membuat gambar agar memuat memenuhi sesuai dengan ukuran Box

- cover	: Untuk membuat gambar memenuhi keseluruhan dari box / layar aplikasi baik itu untuk ukuran ketinggian dan juga lebarnya. Apabila gambar memiliki ukuran lebar lebih besar maka gambar akan menjadi ditarik memanjang keatas dan ke samping dengan ukuran yang sama besar memenuhi tinggi aplikasi.

- fill :	Fungsi ini sama seperti cover yaitu untuk memenuhi gambar ke bagian tinggi dan lebar aplikasi namun perbedaanya disini adalah penggunaan fill akan merubah presisi gambar yang artinya gambar bisa saja memanjang atau melebar untuk memenuhi layar aplikasinya.

- fitHeight :	Jika pada fungsi fill keseluruhan tinggi dan lebar gambar yang akan memenuhi layar, penggunaan fitHeight berguna untuk memenuhi layar hanya pada tinggi gambar saja

- fitWidth :	Untuk yang ini gambar akan memenuhi layar pada lebar gambarnya saja.

```
body: Image.asset(
  'assets/images/paddy-field.jpg',
  height: 500,
  fit: BoxFit.fill
),
```

## Membuat Gambar menjadi bulat

Untuk memanipulasi bentuk gambar, kita membutuhkan widget lain selain Image widget. Banyak sekali trik yang dapat kita gunakan, tapi disini kita hanya akan mencoba dua metode untuk memanipulasi bentuk gambar mejadi lingkaran yaitu dengan widget ClipOval dan widget  BoxDecoration

1. BoxDecoration pada Flutter

```
body: Container(
  height: 300,
  width: 300,
  decoration: BoxDecoration(
      image: DecorationImage(
          image: AssetImage('assets/images/paddy-field.jpg'),
          fit: BoxFit.cover
      ),
      shape: BoxShape.circle
  )
),
```

2. ClipOval widget

```
body: ClipOval(
  child: Image(
      width: 300,
      height: 300,
      image: AssetImage('assets/images/paddy-field.jpg'),
      fit: BoxFit.cover),
),
```