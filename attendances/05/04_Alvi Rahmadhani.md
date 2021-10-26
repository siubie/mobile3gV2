# Rangkuman Pertemuan 5

## B3 - Multiple Activities

-	Buka “LogActivity.java” di folder folder java.
-	Deklarasikan semua variabel yang mewakili semua widget di activity_main.xml

-	Dalam metode onCreate, tentukan semua variabel widget, yang telah dideklarasikan di poin 1, ke id widget terkait menggunakan template 

-	Masih dalam metode onCreate, atur beberapa properti RecyclerView dengan kode

-	Buat kelas Java baru untuk adaptor Log dengan nama 'LogAdapter.java
Ubah kodenya, seperti di bawah ini:
Di kelas 'LogAdapter', buat beberapa variabel dan konstruktor, seperti di bawah ini:
Kemudian, tambahkan metode Override untuk mendapatkan ukuran daftar, seperti di bawah ini:
-	paket org.aplas.soccermatch;
-	impor android.view.LayoutInflater;
-	impor android.view.View;
-	impor android.view.ViewGroup;
-	impor android.widget.ImageView;
-	impor android.widget.TextView;
-	impor java.util.ArrayList;
-	Di kelas 'LogAdapter', buat beberapa variabel dan konstruktor.
-	Kemudian, menambahkan metode Override untuk mendapatkan ukuran daftar
-	Kemudian, menambahkan metode Override untuk menentukan tata letak setiap baris
-	Kemudian, menambahkan metode Override untuk memuat data untuk setiap elemen baris
-	Kemudian, menambahkan metode statis untuk memulai tampilan baris
	 

## B4 - Multimedia Resources

-	Buka “InvertActivity.java” di folder java.
-	Buat onClickListener untuk ImageView dengan id 'insectPic' dalam metode onCreate. Dia akan membuka SubInvertActivity dengan animasi transisi adegan antara ImageView terkait
-	Buat onClickListener untuk ImageView dengan id 'arachnidPic' dalam metode onCreate. Ini akan membuka SubInvertActivity dengan animasi transisi adegan antara ImageView terkait. Masukkan kode ini ke dalam metode 'onClick
-	Buat onClickListener untuk ImageView dengan id 'molluscPic' dalam metode onCreate. Dia akan membuka SubInvertActivity dengan animasi transisi adegan antara ImageView terkait. Masukkan kode ini ke dalam metode 'onClick
-	Buat onClickListener untuk ImageView dengan id 'crustaceanPic' di onCreate metode. Ini akan membuka SubInvertActivity dengan animasi transisi adegan antara ImageView terkait. Masukkan kode ini ke dalam metode 'onClick
-	Buat onClickListener untuk ImageView dengan id 'mediaButton' dalam metode onCreate Ini akan membuka MediaActivity dengan animasi transisi. Letakkan kode ini di metode 'onClick'


## C1 - Basic Data Storage

-	Buka “ShowDataActivity.java”
-	Buat conditional dalam metode binding ke "setUser" yang jika "nama file" adalah null jadi pemintal kosong dan judulnya juga tidak. Dan jika "nama file" diisi maka pemintaldiisi "nama file" Metode ini digunakan untuk memeriksa file di dalam aplikasi. 
-	Buka “BookData.java” dan buat metode dengan nama “loadFileList” untuk deklarasi nilai pemintal dengan "nama file" yang terletak di “DATA_LOCATION”. Dengan variabel dengan nama "fileList" dengan nilai "ArrayList". Dan file direktori di “DATA_LOCATION
Untuk memeriksa file yang tersedia dan menampilkan semua file di direktori
-	Buka “ShowDataActivity.java” dan buat metode binding untuk onClickListener untuk "btnDelData" dengan memeriksa "spBook" terisi atau tidak. Jika "spBook" kosong jadi tampilkan teks "Tidak ada Data Buku!!". Jika “spBook” sudah terisi begitu juga penghapusan bersyarat berhasil dan penghapusan gagal.
-	Buat metode pengikatan untuk menambahkan data baru dengan onClickListener untuk “btnTambah Data”. Metode ini mengandung maksud untuk langsung ke “InputDataActivity.java
-	Buat metode pengikatan untuk mengedit data dengan onClickListener untuk “btnEditData”. Metode ini berisi maksud dan putExtra untuk mendapatkan nilai sebelumnya dan edit di "InputDataActivity.java"
-	Dapatkan hasil tugas Anda. Jika lulus Anda akan mendapatkan centang hijau


