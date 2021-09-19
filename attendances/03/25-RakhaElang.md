Widget
- Widget adalalah kompenen utama dalam aplikasi android
- Widget dan layouts berkerja secara hirarki
- View adalah widget di android studio
- View group membawahi widget-widget atau subclaass seperti button 
- Setiap Widget memiliki atribute id , tata letak , ukuran , padding 
	- Id widget adalah tanda pengenal setiap widget dan harus berbeda
	- tatak letak adalah pengaturan untuk tata letak seperti math parent atau wrapt parent
		- Match Parent adalah tata letak berdasarkan parent atau atasan
		- Wrap parent adalah tata letak berdasarkan konten isi atau objek 
	- Ukuran lebar dan tinggi widget 
	- Padding batasan konten dengan border yang dimiliki widget
- Macam-macam layout yang disediakan android studio
	- Linear Layout
		- Layaout mengatur posisi secara horizal atau vertical 
	- Relative Layout
		- Layout mengatus posisi secara terhubung antara widget satu dengan lainnya
		- Saling berhubungna
	- Web View
		- Tampilan sepert Web view
	- List View
		- Tampilan mengatur secara kolom
	- Grid View
		- Tampilan mengatur secara kolom dan barus
- Array Adapter
	- Mengambil beberapa jenis data dan membuat tampiln 
	- ArrayAdapter
		- ArrayAdapater cocok untuk data berupa array 
	- Simple Cursosr Adapter
		- SimpelCursorAdapter cocok data yang berasal dari kursor
- Button
	- Objek yang akan melakukan sesesatu berdaarkan sentuhan
	- onClick
		- Untuk penggunana klik makan menggunakan method. Untuk syarat adalah nama method harus sama seperti atribut onClick pada button , harus publick , dan mempunyai parameter View 
		- Menggunakan setOnClickListener 
			- Lakukan di method onCreate lalu membuat variable button dan memanggil method setOnClickListtener
- CheckBox
	- Objek untuk pilihan suatu opsi di aplikasi android
	- Peristiwa onClick 
		- Menggunakan method yang namanya seperti atribut onClick setiap checkbox dan menggunakan parameter view.Menggunakan isChecked sebagai algoritma apa yang terjadi jika user mencetang checkbox 
- Radio Button 
	- Objek untuk pilihan untuk memilih satu opsi saja 
	- Pengelompokakan radio menggunakan radio group
	- Peristiwa onClick
		- Menggunakan method yang namanya seperti atribut onClick setiap checkbox dan menggunakan parameter view.Menggunakan isChecked sebagai algoritma apa yang terjadi jika user memilih radioButton 
- Spinner 
	- Objek cara cepat untuk memilih salah satu dari sekumpulan nilai.Menyentuh spinner akan menampilkan menu drop-down bersama semua nilai lain yang tersedia
	- Untuk array untuk ditampilak di spinner dapat dibuat di string.xml secara array
	- Lalu di class java membuat variable spinner lalu mendefiniskan arrayAdapter
	- ArrayAdapter menggunakan memanggil createFormResource
	- Parameternya adalah konten , sumberArray , dan layout untuk menampilkan 
	- lalu memanggil parameter setDrop
	- spinner memanggil param setAdapater dan param arrayAdapter
	- 
Navigation Compenent
- Navigasi adalah interaksi yang memungkinkan pengguna melihat-lihat, masuk, dan keluar dari berbagai konten dalam aplikasi
- Komponen navigasi terdiri dari 
	- Grafik
		- XML yang mengadung infromasi tentang navigasi
	- navHost
		- tujuan navigasi 
	- navController
		- Objek yang  mengelola navigasi dalam bentuk navHost
- Principle Navigation 
	- Navigasi dalam android menggunakna algoritma seperti stack jadi 
	- Tujuan awal aplikasi dalam data sebelumnya selalu berada di bagian bawah stack
	- Operasi yang mengubah data sebelumnya selalu beroperasi di bagian atas stack, baik dengan mengirim tujuan baru ke bagian atas stack atau memunculkan tujuan paling atas dari stack. Menavigasi ke tujuan akan mengirim tujuan tersebut ke stack paling atas.
	- Saat aplikasi pertama kali diluncurkan, tugas baru akan dibuat untuk pengguna, dan aplikasi akan menampilkan tujuan awalnya. Ini menjadi tujuan dasar data sebelumnya dan merupakan dasar untuk status navigasi aplikasi Anda. Bagian atas stack adalah layar saat ini, dan tujuan sebelumnya dalam stack menunjukkan histori halaman yang pernah
- Pemulaian Navigasi
	- atur build.gradle
	- Setiap tindakan di selalu berhubungan jika diatur menggunakan navigasi
	- grpah navigasi berupa file resource yang berisi tujuan dan tindakan aplikasi android
	- saat membuat graphic maka android stu akan membuat direktori resource navigation di dalam direktori res. Direktori ini berisi file resource grafik navigasi Anda (misalnya nav_graph.xml).
	- untuk menambahkan navghost dapat berupa xml 
	- untuk menambahkan tujuan 
- Anatomi tujuan 
	- Type 
		- tujuan diimpelentasi sebagai fragmen . activity , atau class 
	- Label 
		- nama tujuan yang dapat dibaca oleh pengguna 
	- ID
		- kata unique yang harus berbeda 
	- Drop Down Class
		- menampilkan nama class yang dikaitkan dengan tujuan 
- Menavigasikan ket tujuan 
	- Menvagasikan tujuan dapat menggunakan navController 
	- Mendefinikan navHostFragment 
	- Lalu menggunakan param berupa fragmet
- Membuat tujuan 
	- Dialog Fragment 
	- menggunakan activity
		- Untuk menambahkan tujuan Activity, tentukan Activity tujuan dengan nama class-nya yang sepenuhnya memenuhi syarat:
- Mendesain navigasi
	- Toolbar
		- menampilkan atau menyembunyikan item menu tindakan berdasarkan jumlah ruang yang tersedia.
	- RecyclerView.LayoutManager
		- mengubah jumlah span untuk memanfaatkan ukuran jendela secara optimal
- Mendesain graph navigation 
	- grafik navigasi untuk mengelola navigasi aplikasi
- Graph 
	- <include>
		- includemenggunakan grafik dari modul project lain atau project library
- Opening tujuan 
	- dapat dilakukan menggunakan navController
	- menavigais menggunakna ID
		- menggunakan navigate(ID) mengambil ID resource dari tindakan atau tujuan
	- Option navigation 
		- Navigasi menghasilkan class nav action yang sesuai, yang berisi konfigurasi yang ditentukan untuk tindakan seperti tujuan argmen default , option navigasi
- data sebelumnya ang berisi tujuan yang telah Anda kunjungi.  ditempatkan pada tumpukan saat pengguna membuka aplikasi setiap panggilan ke metode navigate() akan menempatkan tujuan lainnya di atas tumpukan.up and back akan memanggil metode   navController.navigateUpdan navController.nageasd, secara berurutan, untuk menghapus (atau pop) tujuan teratas dari tumpukan.
- navigasi bersyarat
	- contoh login 
		- aplikasi harus menavigasi ke login_fragment, tempat pengguna dapat memasukkan nama pengguna dan sandi untuk autentikasi. 
		- jika disetujui, pengguna akan dikirim kembali ke layar profile_fragment. Jika ditolak, pengguna akan diberi tahu bahwa kredensial mereka tidak valid menggunakan snackbar
		- jika pengguna menavigasi kembali ke layar profil tanpa login, mereka akan diarahkan ke layar main_fragment.
		- MainFragment berisi tombol yang dapat diklik pengguna untuk melihat profilnya.
		- Jika ingin melihat layar profil, pengguna harus melakukan autentikasi terlebih dahulu. 
		- Interaksi ini dibuat menggunakan dua fragmen terpisah, tetapi bergantung pada status pengguna bersama. 
		- Informasi status ini tidak menjadi tanggung jawab kedua fragmen tersebut dan lebih sesuai disimpan dalam UserViewModel bersama.
		-  ViewModel ini dibagikan di antara fragmen dengan menggabungkannya ke aktivitas, yang menerapkan ViewModelStoreOwner. Dalam contoh berikut, requireActivity() dicocokkan ke MainActivity karena MainActivity menghosting ProfileFragment:
		- dapat menggunakan NavController.getPreviousBackStackEntry() untuk mengambil NavBackStackEntry pada tujuan sebelumnya, yang mengenkapsulasi status khusus NavController untuk tujuan tersebut. 
		- LoginFragment menggunakan SavedStateHandle dari NavBackStackEntry sebelumnya untuk menetapkan nilai awal yang menunjukkan apakah pengguna berhasil login. 
		- Ini adalah status yang ingin kami kembalikan jika pengguna segera menekan tombol kembali sistem android studio yang  
		- Menetapkan status ini menggunakan SavedStateHandle akan memastikan bahwa status tetap ada selama proses penghentian.
    Desination
        konten yang berbeda setiap app android studio
    Actions
        Koneksi yang menghubungkan setiap destination aplikasi
    Destination Panel
        Ragam naviagasi
    Graph Editor
        Menvisualisasi navigation graph 
    Attributes
        Attributs item yang dipilih 
    Add Navhost Into Activity
        Nagigation Host
        Navigation host adalah empty container 
        saling bergantian sebagai navigate di aplikasi