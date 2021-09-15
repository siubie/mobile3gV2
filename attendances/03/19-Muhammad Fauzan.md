## Rangkuman Pertemuan 3

Mengerjakan Aplas B1

Belajar mengenai activity, widget, dan navigation component.

• Field

Field merupakan tipe data yang didefiniskan, sementara method merupakan operasi. Inheritance (pewarisan) adalah proses dimana satu objek mengakuisisi properti dari obyek lain. Ini mendukung klasifikasi hirarkis. Dengan menggunakan warisan, objek hanya perlu mendefinisikan kualitas-kualitas yang membuatnya unik dalam kelasnya. Hal ini dapat mewarisi atribut umum dari induknya. Sebuah sub - class baru mewarisi semua atribut dari super - class nya.

• Constructor

Constructor adalah method khusus yang akan dieksekusi pada saat pembuatan objek (instance).
Biasanya method ini digunakan untuk inisialisasi atau mempersiapkan data untuk objek.
 
• Constructor dengan Parameter

Constructor biasanya digunakan untuk initialize (menyiapkan) data untuk class.
Untuk melakukan ini, kita harus membuat parameter sebagai inputan untuk constructor.

• Default Constructor (no-arg constructor)

Default Constructor disebut juga no-arg constructor adalah salah satu Constructor yang ada di Java. Berikut adalah syntax umumnya:
<class_name>(){}
Hal yang menarik untuk diperhatikan adalah jika tidak ada konstruktor yang ditentukan dalam kelas Java, maka kompilator Java secara otomatis membuat konstruktor default untuk kelas tersebut.
Bergantung pada jenis objek, konstruktor default memberikan nilai default ke objek. Kekurangan dari menggunakan konstruktor default yang dibuat secara otomatis oleh javac adalah setelah itu programmer tidak dapat mengatur nilai awal untuk atribut objek.

• Method setter dan getter

Setter adalah sebuah aksi saat kita memasukan sebuah nilai/values kedalam suatu variable/object, sedangkan Getter adalah sebuah aksi saat kita mengambil sebuah nilai/values dari suatu variable/object.
Materi Widget
Paket widget pada dasarnya merupakan visualisasi dari elemen user interface (UI) yang digunakan pada layar aplikasi Android di mana kita dapat merancang sendiri sesuai kebutuhan. 
Widget di dalam Android ditampilkan dengan konsep View. Di mana aplikasi Android pada umumnya menggunakan widget sebagai Layout XML. Untuk mengimplementasikan widget, selain file kotlin kita juga membutuhkan tambahan dua file. Berikut ini adalah file-file yang umumnya kita butuhkan apabila kita membuat widget: 
1.	File Kotlin. Berupa file yang mengimplementasikan aksi dari widget. Jika kita mendefinisikan suatu widget beserta posisinya di layar yang didefinisikan dari file XML, kita harus melakukan coding di file kotlin yang dapat mengambil semua nilai atribut dari file layout XML yang didefinisikan. 
2.	File XML. Sebuah file yang mendefinisikan komponen elemen-elemen XML yang digunakan untuk inisialisasi widget serta atribut yang mendukungnya. 
3.	Layout XML. File XML menggambarkan atau penambahan keterangan pada layout widget kita. 
Komponen widget TextView dan Button sudah kita bahas pada modul sebelumnya. Beberapa komponen widget akan kita bahas saat ini. Widget EditText untuk menuliskan teks ke aplikasi dan akan ditangkap oleh aplikasi untuk diolah. Widget Image Button untuk membuat button yang diberi gambar. Widget Image View untuk membuat tampilan gambar. Sedangkan widget RadioButton/ RadioGroup biasanya digunakan bersama-sama. 
Di dalam satu RadioGroup terdapat beberapa RadioButton. Dan di dalam satu RadioGroup user hanya dapat melakukan satu check/pemilihan RadioButton. Dan yang terakhir widget akan kita bahas CheckBox, pilihan yang dapat dipilih lebih dari satu item. 

• Event Handling

Android dapat menangani event dari interaksi dengan pengguna. Saat mempertimbangkan event dalam user interface, pendekatannya adalah menangkap event dari objek View tertentu yang digunakan pengguna untuk berinteraksi. Kelas View menyediakan sarana untuk melakukannya. 
Dalam berbagai kelas View yang akan digunakan untuk menyusun layout, mungkin dapat dilihat beberapa method callback publik yang tampak berguna untuk kejadian UI. Method ini dipanggil oleh framework Android ketika masing-masing tindakan terjadi pada objek itu. Misalnya, jika View (seperti Button) disentuh, method onTouchEvent() akan dipanggil pada objek itu. Kelas View salah satunya berisi sekumpulan interface bertumpuk dengan callback yang mudah didefinisikan. Antarmuka ini, yang disebut event listener, digunakan untuk melakukan interaksi pengguna dengan UI. 

• Event listener

Event listener merupakan antarmuka di kelas View yang berisi method callback tunggal. Method ini akan dipanggil oleh framework Android jika View yang telah didaftarkan dengan listener dipicu oleh interaksi pengguna dengan item dalam UI. 
Yang juga disertakan dalam antarmuka event listener adalah method callback berikut ini: 
1.	Method onClick() dari View.OnClickListener. Ini dipanggil baik saat pengguna menyentuh item (jika dalam mode sentuh), maupun memfokuskan pada item dengan tombol navigasi atau trackball dan menekan tombol "enter" yang sesuai atau menekan trackball. 
2.	Method onLongClick() dari View.OnLongClickListener. Ini dipanggil baik saat pengguna menyentuh dan menahan item (jika dalam mode sentuh), maupun memfokuskan pada item dengan tombol navigasi atau trackball dan menekan serta menahan tombol "enter" yang sesuai atau menekan dan menahan trackball (selama satu detik). 
3.	Method onFocusChange() dari View.OnFocusChangeListener. Ini dipanggil saat pengguna menyusuri ke atau dari item, dengan menggunakan tombol navigasi atau trackball. 
4.	Method onKey() dari View.OnKeyListener. Ini dipanggil saat pengguna memfokuskan pada item dan menekan atau melepas tombol perangkat keras pada perangkat. 
5.	Method onTouch() dari View.OnTouchListener. Ini dipanggil saat pengguna melakukan tindakan yang digolongkan sebagai peristiwa sentuh, termasuk penekanan, pelepasan, atau isyarat perpindahan pada layar (dalam batasan item itu). 
6.	Method onCreateContextMenu() dari View.OnCreateContextMenuListener. Ini dipanggil saat Menu Konteks sedang dibuat (akibat "klik lama" terus-menerus).  

• Materi Navigation Component

Android Navigation Component merupakan sebuah arsitektur baru yang di perkenalan pada Google I/O tahun lalu, arsitektur ini membantu kita dalam penerapan Single Activity, bagi teman teman yang belum tahu secara sederhana single activity merupakan sebuah konsep dimana kita hanya membuat satu buah activity di dalam aplikasi kita, kemudian semua tampilan UI akan di letak kan pada fragment fragment.
Pada case sederhana kita berpindah daru satu fragment ke fragment lain menggunakan fragment transaction, namun dalam case yang lebih komplek kita akan kesulitan dalam menghadle backstack dari fragment fragment tersebuh, sehingga di ciptakan lah Navigation Component yang akan memudahkan kita dalam menanganan ini.
Beberapa keuntungan menggunakan Navigation Component :
•	Hadle backstack lebih mudah
•	Menggunakan Automated Transaction
•	Pengaturan animasi transaksi lebih mudah
•	Pengiriman argument lebih mudah
•	Deeplink jauh lebih mudah diterapkan

• Membuat grafik navigasi

Navigasi terjadi di antara tujuan-tujuan aplikasi dalam hal ini, di mana saja dalam aplikasi yang dapat dinavigasi oleh pengguna. Tujuan tersebut terhubung melalui tindakan.
Grafik navigasi adalah file resource yang berisi semua tujuan dan tindakan Anda. Grafik tersebut mewakili semua jalur navigasi aplikasi yang dibuat.
Saat Anda menambahkan grafik navigasi pertama, Android Studio akan membuat direktori resource navigation di dalam direktori res. Direktori ini berisi file resource grafik navigasi Anda (misalnya nav_graph.xml).

• Materi Navigation Editor

Setelah menambahkan grafik, Android Studio akan membuka grafik tersebut ke dalam Navigation Editor. Di dalam Navigation Editor, dapat mengedit grafik navigasi secara visual atau langsung mengedit XML yang mendasarinya.
- Panel tujuan: Mencantumkan host navigasi Anda dan semua tujuan yang saat ini ada di Editor Grafik.
- Graph Editor: Berisi representasi visual dari grafik navigasi Anda. Anda dapat beralih antara tampilan Desain dan representasi XML yang mendasarinya dalam tampilan Teks.
- Atribut: Menampilkan atribut untuk item yang saat ini dipilih dalam grafik navigasi.
Elemen <navigation> adalah elemen root pada grafik navigasi. Saat menambahkan tujuan dan menghubungkan tindakan ke grafik, Anda dapat melihat elemen <destination> dan <action> yang sesuai di sini sebagai elemen turunan. Jika Anda memiliki grafik bertingkat, elemen tersebut akan muncul sebagai elemen <navigation> turunan.
