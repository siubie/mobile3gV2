Form widget sendiri berfungsi untuk mempermudah dalam proses pembuatan dan memberi keamanan lebih pada aplikasi flutter seperti validasi, dan aksi lainnya yang umum terdapat pada sebuah form.

TextFormField Widget
TextFormField berfungsi sebagai input field, biasanya digunakan untuk input nama lengkap, searching, email, password dan input lainnya. Untuk contoh kode penggunaannya seperti dibawah ini

TextFormField();

Label dan Placeholder pada TextFormField
Untuk menambahkan label, placeholder atau icon pada TextField, kita dapat menggunakan properti decoration. contohnya seperti ini

TextFormField(
  decoration: new InputDecoration(
      hintText: "Masukan Nama Lengkap Anda",
      labelText: "Nama Lengkap",
      icon: Icon(Icons.people)),
),


masih pada properti decoration, kita juga dapat menambah border, contohnya seperti ini

TextFormField(
  decoration: new InputDecoration(
    hintText: "masukan nama lengkap anda",
    labelText: "Nama Lengkap",
    icon: Icon(Icons.people),
    border: OutlineInputBorder(
        borderRadius: new BorderRadius.circular(5.0)),
  ),
)


keyboardType
Kita juga dapat merubah tampilan tipe keyboard saat textFormField aktif, caranya dengan menggunakan properti keyboardType. Contoh

keyboardType: TextInputType.phone,


BidangTeks di Flutter adalah widget textfield yang paling umum digunakan yang memungkinkan pengguna mengumpulkan masukan dari keyboard ke dalam aplikasi. 
Kita dapat menggunakan widget TextField dalam membuat formulir, mengirim pesan, membuat pengalaman pencarian, dan banyak lagi.

TextField(
  decoration: const InputDecoration(
    border: OutlineInputBorder(),
    hintText: 'Enter a search term'
  ),
);
