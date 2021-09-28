# Rangkuman Pertemuan 4
-	Mengerjakan Aplas B2 – Advanced Widget

-	TASK GUIDE (B2X.01)

Menentukan color, string, dan integer resources

Di mulai proyek untuk membuat aplikasi Android game sederhana. Pertama dengan konfigurasi proyek dan konfigurasi sumber daya.

-	TASK GUIDE (B2X.02)

Menentukan theme, style, dan drawable resources

Diharapkan akan memahami style, theme, dan drawable vector image.

-	TASK GUIDE (B2X.03)

Completing the layout (UI)

Diharapkan akan membuat UI untuk proyek Color Game dengan beberapa onClick
atribut.

-	TASK GUIDE (B2X.04)

Create validation method

Diharapkan akan mendeklarasikan fields yang dibutuhkan oleh aplikasi dan mendefinisikan method untuk memeriksa validitas untuk memasuki permainan.

-	TASK GUIDE (B2X.05)

Create method to start CountDownTimer

Diharapkan akan mengerti bagaimana Countdowntimer bekerja.

-	TASK GUIDE (B2X.06)

Create method to load color data to List and Hashtable

Diharapkan akan memahami bagaimana mengakses array dari resource dan memasukkannya ke dalam List dan Hashtable.

-	TASK GUIDE (B2X.07)

Create method to start game

Diharapkan akan mengerti bagaimana memulai timer untuk memulai permainan.
 
-	TASK GUIDE (B2X.08)

Create method to response user input and calculate score

Diharapkan akan mengerti bagaimana menangani timer dan menghitung skor.

-	ListView

Dalam pengembangan Android, setiap kali kami ingin menampilkan daftar vertikal item yang dapat digulir, kami akan menggunakan LisView yang memiliki data yang diisi menggunakan Adaptor.
Adaptor paling sederhana untuk digunakan disebut ArrayAdapter karena adaptor mengonversi objek ArrayList menjadi item View yang dimuat ke dalam container ListView.

-	RecyclerView

RecyclerView adalah ViewGroup yang merender tampilan berbasis adaptor dengan cara yang serupa. Itu seharusnya menjadi penerus ListView dan GridView.
Setiap elemen individu dalam daftar ditentukan oleh objek view holder. Anda menentukan view holder dengan memperluas RecyclerView.ViewHolder.
RecyclerView meminta tampilan tersebut, dan mengikat tampilan ke datanya, dengan memanggil metode di adaptor. Anda menentukan adaptor dengan memperluas RecyclerView.Adapter.
layout manager mengatur elemen individual dalam daftar Anda. Anda dapat menggunakan salah satu pengelola tata letak yang disediakan oleh pustaka RecyclerView, atau Anda dapat menentukan sendiri. layout manager semuanya didasarkan pada kelas abstrak LayoutManager perpustakaan.

-	LayoutManagers

RecyclerView menyediakan pengelola tata letak bawaan ini:
LinearLayoutManager menampilkan item dalam daftar gulir vertikal atau horizontal.
GridLayoutManager menampilkan item dalam kotak.
StaggeredGridLayoutManager menampilkan item dalam kisi terhuyung.

-	Adapter

RecyclerView menyertakan jenis adaptor baru. Ini adalah pendekatan yang mirip dengan yang sudah Anda gunakan, tetapi dengan beberapa kekhasan, seperti ViewHolder yang diperlukan.
Anda perlu mengganti tiga metode:
1.	onCreateViewHolder()
2.	diBindViewHolder()
3.	getItemCount()
