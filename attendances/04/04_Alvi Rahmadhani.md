# Rangkuman Pertemuan 4
Jobsheet TASK GUIDE (B2X.01)
Buat Proyek Baru di Android Studio dan pilih “Add No Activity”, lalu Next
Setelah itu   Konfigurasi Proyek
Kemudian Buka colors.xml
Buka strings.xml. Tambahkan beberapa string dan bilangan bulat seperti tabel ini
Masih di strings.xml, tambahkan array string
Buka styles.xml
Buat Aktivitas Kosong baru dengan menu ini
Buka MyActivity.java
Buka AndroidManifest.xml
Ubah isi file “build.gradle (Module: app)” seperti di bawah ini, lalu Sync
Dan yang terakhir pengujian

Jika Pengujiannya centang Hijau semua maka bisa lanjut ke jobsheet berikutnya

Jobsheet TASK GUIDE (B2X.02)
 Buka tugas B2X.01 (proyek ColorGameX) yang sudah lulus tes
Kemudian Salin “ic_resicon.xml” di folder suplemen ke “drawable”
Setelah itu Buat bentuk baru yang dapat digambar. Klik kanan drawable klik New drawable resource
Nama filenya  round_btn, lalu klik ok
Setelah nama file Buka file dan tentukan bentuk di “round_btn.xml” dengan kode yang ada pada josbheet TASK GUIDE (B2X.02) Halaman 2 no 4
Pada tag bentuk, tentukan 4 nilai tag dengan spesifikasi yang ada di Jobsheet TASK GUIDE (B2X.02) Halaman 3 no 5
Kemudian Buka file “styles.xml”. Di bawah tag “AppTheme”, tambahkan gaya baru dengan nama
“ColoredButton” tanpa parent mengacu pada spesifikasi diJobsheet TASK GUIDE(B2X.02) Halaman 3 no 6
Di bawah tag “ColoredButton”, tambahkan gaya baru dengan nama “ProgressBar” dengan induk
"@android:style/Widget.SeekBar" mengacu pada spesifikasi di Jobsheet TASK GUIDE (B2X.02) Halaman 3 no 7
Jika sudah pengujian 
Setelah itu jawab soal di halaman 4 sampai pengujian nya centang hijau semua maka bisa langsung masuk ke jobsheet selanjutnya



Jobsheet TASK GUIDE (B2X.03)
Buka tugas B2X.02 (proyek ColorGameX) yang sudah lulus tes.
Buka file activity_layout.xml, untuk memulai desain UI
Pada editor layout xml, hapus default “ConstraintLayout” dengan semua tag-nya dan
buat "LinearLayout" dengan id "mainLayout" sebagai tata letak utama lihat di
spesifikasi yang ada pada Jobsheet TASK GUIDE (B2X.03) Halaman 2 no 3
Setelah itu Pada tag LinearLayout (mainLayout), tambahkan TextView dengan referensi id “appTitle” di
spesifikasi yang ada pada Jobsheet TASK GUIDE (B2X.03) Halaman 2 no 4

Jika sudah Di bawah TextView appTitle, tambahkan LinearLayout dengan id "accessBox" lihat di
spesifikasi yang ada pada Jobsheet TASK GUIDE (B2X.03) Halaman 3 no 5

Setelah itu Di bawah LinearLayout accessBox, tambahkan LinearLayout dengan id "colorBox" lihat di
spesifikasi yang ada pada Jobsheet TASK GUIDE (B2X.03) Halaman 3 no 6
Setelah itu Di bawah ColorBox LinearLayout, tambahkan RelativeLayout dengan id “buttonBox1” lihat di
spesifikasi yang ada pada Jobsheet TASK GUIDE (B2X.03) Halaman 3 no 7
Setelah itu  Di bawah RelativeLayout buttonBox1, tambahkan Spasi dengan id "spaceBox" lihat di
spesifikasi yang ada pada Jobsheet TASK GUIDE (B2X.03) Halaman 3 no 8
Setelah itu Di bawah Space spaceBox, tambahkan RelativeLayout dengan id "buttonBox2" lihat di
spesifikasi yang ada pada Jobsheet TASK GUIDE (B2X.03) Halaman 3 no 9
Setelah itu Di bawah RelativeLayout buttonBox2, tambahkan LinearLayout dengan id “scoreBox” lihat di
spesifikasi yang ada pada Jobsheet TASK GUIDE (B2X.03) Halaman 3 no 10

Di bawah LinearLayout scoreBox, tambahkan LinearLayout dengan id “progressBox” lihat di
spesifikasi yang ada pada Jobsheet TASK GUIDE (B2X.03) Halaman 4 no 11
Sementara, UI terlihat seperti di Jobsheet TASK GUIDE (B2X.03) Halaman 4 no 12
Buka "MyActivity.java", di bawah metode onCreate, tulis 3 metode baru seperti di Jobsheet TASK GUIDE (B2X.03) Halaman 4 no 13
Kembali ke “activity_layout.xml” LinearLayout “accessBox”. Di LinearLayout
masukkan EditText dengan id "appCode" lihat spesifikasi di Jobsheet TASK GUIDE (B2X.03) Halaman 5 no 14
Di bawah EditText appCode, tambahkan Tombol dengan id "submitBtn" lihat di spesifikasi di Jobsheet TASK GUIDE (B2X.03) Halaman 5 no 15
Pergi ke LinearLayout "colorBox". Di LinearLayout masukkan TextView dengan id
"clrText" lihat spesifikasi di Jobsheet TASK GUIDE (B2X.03) Halaman 5 no 16
Di bawah TextView clrText, tambahkan Spasi dengan id "spaceText1" mengacu pada spesifikasi
Di Jobsheet TASK GUIDE (B2X.03) Halaman 6 no 17
Di bawah Space spaceText1, tambahkan TextView dengan id "appText1" lihat spesifikasi
Di Jobsheet TASK GUIDE (B2X.03) Halaman 6 no 18
Pergi ke RelativeLayout “buttonBox1”. Di RelativeLayout masukkan Tombol dengan id
"color1" lihat spesifikasi di Jobsheet TASK GUIDE (B2X.03) Halaman 6 no 19
Di bawah Button color1, tambahkan Button dengan id “color2” lihat spesifikasi di Jobsheet TASK GUIDE (B2X.03) Halaman 6 no 20
Di bawah Button color2, tambahkan Button dengan id “color3” lihat spesifikasi di Jobsheet TASK GUIDE (B2X.03) Halaman 6 no 21
