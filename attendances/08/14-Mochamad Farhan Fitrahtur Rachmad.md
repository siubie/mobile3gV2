# Rangkuman Pertemuan 8

Pada chapter 4 mengerjakan dan mengembangkan projek aplikasi yaitu aplikasi konversi suhu dan menginstal ekstensi untuk visual studio code yaitu Wakatime

## Wakatime

Wakatime ini adalah plugin dari sebuah aplikasi web bernama Wakatime.fungsinya yaitu untuk time-tracking, jadi wakatime ini secara otomatis men-track aktivitas koding kita. terkadang ngerasa udah ngoding ber-jam-jam. tapi berapa sih waktu aktual kita ngoding. nah aplikasi ini membantu kita mengetahuinya. bahkan dia bisa di-konek-kan dengan git untuk mengetahui kita mengerjakan commit apa selama berapa jam

## Dropdown Widget

Dropdown di Flutter membantu pengguna aplikasi memilih item dari item menu drop-down. Widget ini akan menampilkan item yang dipilih pada tombol drop-down dan ikon untuk menunjukkan pengguna memiliki daftar item untuk dipilih.

Contoh Kode :

```
 DropdownButton(
              hint: Text("Select The Gender"),
              value: _valGender,
              items: _listGender.map((value) {
                return DropdownMenuItem(
                  child: Text(value),
                  value: value,
                );
              }).toList(),
              onChanged: (value) {
                setState(() {
                  _valGender = value;  
                });
              },
            ),

```

##  List 

Array adalah salah satu struktur data yang paling umum dan paling populer yang disediakan oleh bahasa pemrograman. namun dart tidak menyediakan array, namun sebaliknya dart memiliki list yang kurang lebih semua sama disediakan oleh array.

List jika pada bahasa pemrograman lain disebut array, jadi dalam pemrograman dart list itu merupakan kumpulan untuk menyimpan lebih dari satu nilai atau banyak nilai dalam variable. Artinya setiap elemen yang di dalam list memiliki posisi tetap, yang dimana saat kita gunakan list tersebut dengan mengakses objek menurut indeks-nya.

Contoh Kode :

```
List lokasi = [
    'Jakarta',
    'Bandung',
    'Bogor',
    'Bekasi',
    'Malang',
    'Surabaya',
    'Jogjakarta',
    'Solo'
];

    ListView(
          children: lokasi.map((nama) {
            return ListTile(
              leading: Icon(Icons.map),
              title: Text(nama),
            );
          }).toList(),
        ),
      ),
```

