# Rangkuman Pertemuan 4

1.	Pertama menguji coba membuat projek konfigurasi dan resource konfigurasi dengan membuat projek baru di android studio dan membuat konfigurasi serta resource konfigurasi projek sesuai dengan buku panduan. Menambahakan warna dan elemen dengan tipe data variable string array. Kemudian membuat aktivatas pada menu baru serta file android manifest berformat xml. Setelah semua selesai dilakukan pengujian dengan cara menyalin ElementTest.java, ResourceTest.java, ViewTest.java, TestB2AdvancedWidgetsX011.java dan TestB2AdvancedWidgetsX011.java” file ke folder "org.aplas.colorgamex (test)" kemudian mengeksekusi untuk melihat hasilnya

2.	Tahap kedua Mendefinisikan tema,style dan resource drawable dengan cara menyalin file ic_resicion berformat xml ke dalam folder drawable. Kemudain membuat resource file drawable baru dan mengisi kode sesuai spesifikasi panduan Setelah semua selesai dilakukan pengujian dengan cara menyalin ElementTest.java, ResourceTest.java, ViewTest.java, TestB2AdvancedWidgetsX021.java dan TestB2AdvancedWidgetsX021.java” file ke folder "org.aplas.colorgamex (test)" kemudian mengeksekusi untuk melihat hasilnya.


3.	Pada tahap ketiga ini membuat layout (UI) pada warna game dengan cara membuka file
activity_layout yang berformat xml untuk mendesain UI. Kemudian membuka file java MyActivity pada method mengisi 3 method baru sesuai dengan buku panduan selanjutnya Setelah semua selesai dilakukan pengujian dengan cara menyalin TestB2AdvancedWidgetsX031.java dan TestB2AdvancedWidgetsX031.java” file ke folder "org.aplas.colorgamex (test)" kemudian mengeksekusi untuk melihat hasilnya.

4.	Pada tahap keempat ini melakukan pemrograman java pada file myactivity dan Membuat validasi method. Kemudian mendeklarasikan tipe data pada view resource serta membuat validasi dengan mengkomparasi tipe data string dari text password Setelah semua selesai dilakukan pengujian dengan cara menyalin file TestB2AdvancedWidgetsX041.java dan TestB2AdvancedWidgetsX041.java” file ke folder "org.aplas.colorgamex (test)" kemudian mengeksekusi untuk melihat hasilnya.

5.	Tahap kelima Membuat method start CountDownTimer dengan cara menambahkan  fields baru di kelas MyActivity :
public class MyActivity extends AppCompatActivity {



Context context;

RecyclerView recyclerView;

RecyclerView.Adapter recyclerViewAdapter;

RecyclerView.LayoutManager recylerViewLayoutManager;

String[] subjects = { "apel","jeruk"}



setContentView(R.layout.activity_main);



context = getApplicationContext();

recyclerView = findViewById(R.id.recyclerView);

recylerViewLayoutManager = new LinearLayoutManager(context);

recyclerView.setLayoutManager(recylerViewLayoutManager);

recyclerViewAdapter = new AdapterRecyclerView(context, subjects);

recyclerView.setAdapter(recyclerViewAdapter);

}

}

Kemudian membuat method baru dengan nama initTime dan parameter blank fungsinya untuk mendefinisikan countdown field dengan CountdownTimer Kemudian setelah semua selesai dilakukan pengujian dengan cara menyalin file TestB2AdvancedWidgetsX051.java dan TestB2AdvancedWidgetsX051.java” file ke folder "org.aplas.colorgamex (test)" kemudian mengeksekusi untuk melihat hasilnya dan menjalankan aplikasinya Jika telah berhasil  tidak ada perubahan di UI.

6.	Pada tahap keenam ini Membuat method untuk load color data ke List & Hashtable dan menambahkan beberapa method void dan blank parameter serta mendeklarasikan tipe data string setelah semua selesai dilakukan pengujian dengan cara menyalin file TestB2AdvancedWidgetsX061.java dan TestB2AdvancedWidgetsX061.java” file ke folder "org.aplas.colorgamex (test)" dan mengeksekusi file tersebut.

