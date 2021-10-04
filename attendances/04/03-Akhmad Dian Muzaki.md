# Rangkuman Materi Activities and Intents dan JAVA DataBinding

Minggu Ke-04 Mata Kuliah Mobile
--

            Nama           : Akhmad Dian Muzaki
            NIM            : 1941720205
            No.Absen       : 03
            Dosen Pengampu : Putra Prima Arhandi, S.T., M.Kom.

Contents

# 1.	Widget 
    Widget adalah komponen utama untuk membangun UI di Android Widget mewarisi dari kelas View
# 2.	UI Hirarchy 
    UI Hirarchy Antarmuka pengguna (UI) untuk aplikasi Android dibangun sebagai hierarki tata letak dan widget.perlu mendefinisikan id dalam XML untuk memanipulasi Widget menggunakan Java atau Kotlin
# 3.	Set/Get Value of Widget 
    Set/Get Value of WidgetTergantung pada widget contoh: a. EditText: Text dll b. ImageView: ImageResource dll c. RadioButton: Text, Checked d. CheckBox: Text, Checked
# 4.	Navigation Component 
    Navigation Component Navigasi antara layar dan aplikasi yang berbeda adalah bagian inti dari pengalaman pengguna. Prinsip-prinsip berikut menetapkan dasar untuk pengalaman pengguna yang konsisten dan intuitif di seluruh aplikasi Komponen Navigasi dirancang untuk menerapkan prinsip-prinsip ini secara default, memastikan bahwa pengguna dapat menerapkan heuristik dan pola yang sama dalam navigasi saat mereka berpindah antar aplikasi
# 5.	Destination 
    Destination Setiap aplikasi yang telah dibuat memiliki tujuan awal yang tetap.Ini adalah layar pertama yang dilihat pengguna saat mereka meluncurkan aplikasi Anda dari peluncur.Tujuan ini juga merupakan layar terakhir yang dilihat pengguna ketika mereka kembali ke peluncur setelah menekan tombol Kembali.
# 6.	Navigaton Graph Tujuan
    Navigaton Graph Tujuan adalah area konten yang berbeda di aplikasi Anda Tindakan adalah koneksi logis antara tujuan Anda yang mewakili jalur yang dapat diambil pengguna
# 7.	Navigation Editor: 
        •	Panel tujuan: Mencantumkan host navigasi Anda dan semua tujuan yang saat ini ada di Editor Grafik.
        •	Editor Grafik: Berisi representasi visual dari grafik navigasi Anda. Anda dapat beralih antara tampilan Desain dan representasi XML yang mendasarinya dalam tampilan Teks.
        •	Atribut: Menampilkan atribut untuk item yang saat ini dipilih dalam grafik navigasi.

# 8.	Menambahkan Navhost 
    Menambahkan Navhost ke Activity Salah satu bagian inti dari komponen Navigasi adalah host navigasi. Host navigasi adalah wadah kosong tempat tujuan ditukar masuk dan keluar saat pengguna menavigasi melalui aplikasi yang telah dibuat. Host navigasi harus berasal dari NavHost