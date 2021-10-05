Catatan
Kelas  RecyclerView  adalah  versi  ListView  yang  lebih  canggih  dan  fleksibel. Widget  ini  adalah  kontainer  untuk  menampilkan  rangkaian  data  besar  yang  bisa digulir  secara  sangat  efisien  dengan  mempertahankan  tampilan  dalam  jumlah terbatas. Gunakan  widget  RecyclerView  bila  Anda  perlu  menampilkan  banyak  data yang  bisa  digulir,  atau  kumpulan  data  dengan  elemen  yang  berubah  pada  waktu proses berdasarkan aksi pengguna atau kejadian jaringan.

RecyclerView adalah ViewGroup yang merender tampilan berbasis adaptor dengan cara yang serupa. Seharusnya menjadi penerus ListView dan GridView.
Setiap elemen individu dalam daftar ditentukan oleh objek view holder. Menentukan view holder dengan memperluas RecyclerView.ViewHolder.
RecyclerView meminta tampilan tersebut, dan mengikat tampilan ke datanya, dengan memanggil metode di adaptor. 
Manajer tata letak mengatur elemen individual dalam daftar. Dapat menggunakan salah satu pengelola tata letak yang disediakan oleh pustaka RecyclerView, atau  dapat menentukan sendiri. Manajer tata letak semuanya didasarkan pada kelas abstrak LayoutManager perpustakaan.

RecyclerView ilustrasi
-	LayoutManager
-	Adapter
-	Dataset

RecyclerView menyertakan jenis adaptor baru. Ini adalah pendekatan yang mirip dengan yang sudah digunakan, tetapi dengan beberapa kekhasan, seperti ViewHolder yang diperlukan.
Sehingga perlu mengganti tiga metode:
-	onCreateViewHolder()
-	diBindViewHolder()
-	getItemCount()

Untuk menampilkan data dalam RecycleView, memperlukan bagian berikut:
-	Data Tidak penting dari mana asal data. Anda bisa membuat data secara lokal, seperti  yang  Anda  lakukan  dalam  latihan,  mendapatkannya  dari  database perangkat seperti yang akan Anda lakukan dalam praktik nanti, ataumenariknya dari awan.
-	RecyclerView. Daftar gulir yang berisi item daftar.
-	Instance  RecyclerView  sebagaimana  didefinisikan  dalam  file  layout  aktivitas Anda akan bertindak sebagai kontainer tampilan.
-	Layout  untuk  satu  item  data.  Semua  item  daftar  tampak  sama,  sehingga  Anda bisa menggunakan layout yang sama
-	Untuk semuanya. Layout item harus dibuat secara terpisah dari layout aktivitas, sehingga satu per satu tampilan item bisa dibuat dan diisi data.
-	Pengelola  layout  Pengelola  layout  menangani  penyusunan  (layout)  komponen antarmuka  pengguna  dalam  suatu  tampilan.  Semua  grup  tampilan  memiliki pengelola  layout.  Untuk  LinearLayout,  sistem  Android  menangani  layout  untuk Anda.  RecyclerView  memerlukan  
-	Pengelola layout  eksplisit  untuk  mengelola susunan   item   daftar   yang   terdapat   di   dalamnya.   Layout   ini   bisa   vertikal, horizontal, atau berupa petak.Pengelola   layout   adalah   instance   dari   Recyclerview.LayoutManager   untuk menyusun layout item dalam RecyclerView 
-	Adapter.  Adapter  menghubungkan  data  Anda  dengan  RecyclerView.  Adapter menyiapkan  data  dan  cara  menampilkan  data  dalam  view  holder.  Bila  data berubah,  adapter  akan  memperbarui  materi  tampilan  item  daftar  terkait  dalam RecyclerView.  Adapter  juga  merupakan  ekstensidari  RecyclerView.Adapter. Adapter menggunakan ViewHolder untuk menampung tampilan yang menyusun setiap  item  dalam  RecyclerView,  dan  mengikat  data  untuk  ditampilkan  dalam tampilan yang menampilkannya.
-	View  holder.  View  holder  memperluas  kelas  ViewHolder. View  holder  berisi tampilan  informasi  untuk  menampilkansatu  item  dari  layout  item.  View  holder digunakan oleh adapter untuk menyediakan data, yang merupakan ekstensi dari RecyclerView.ViewHolder

Data
Semua data yang bisa ditampilan akan ditampilkan dalam RecyclerView
-	Teks
-	Gambar
-	Ikon
Data bisa berasal dari sumber mana pun
-	Dibuat oleh aplikasi. Misalnya, kita acak untuk permainan
-	Dari database local. Misalnya, daftar kontak
-	Dari storage awam atau internet. Misalnya judul berita

Recycler View
-	Suatu grup tampilaln untuk container yang bisa digulir
-	Ideal untuk daftar item serupa yang Panjang
-	Hanya  menggunakan  tampilan  dalam  jumlah  terbatas  yang  digunakan  kembali saat  tampilan  tersebut  tidak  tampak  di  layar.  Hal  ini  menghemat  memori  dan mempercepat  pembaruan  item  daftar  saat  pengguna  menggulir  data,  karena tidak perlu membuat tampilan baru untuk setiap item yang muncul.
-	Secara umum, RecyclerView menyimpan sebanyak mungkin tampilan item yang muat di layar, plus sedikit tambahan pada setiap akhir daftar untuk memastikan pengguliran berjalan cepat dan lancar.

