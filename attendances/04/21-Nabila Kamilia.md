Tugas B2 Advanced Widgets

Mendefinisikan warna, string dan resource integer
Mendefinisikan tema, style dan resource drawable
Menyelesaikan layout (UI)
Membuat validasi method 
Membuat method start CountDownTimer
Membuat method untuk load color data untuk List dan Hashtable
Membuat method to start game
Membuat method to response user input dan perhitungan skor

Untuk menjalankannya diperlukan AVD Mananager, device definition phone diharapkan diatas Pixel 2 dikarenakan ketika saya run projeknya terjadi error dan tidak dapat menampilkan hasilnya.
Jadi saya ubah menjadi Pixel 4 XL.

ListView
Dalam pengembangan Android, setiap kali kami ingin menampilkan daftar vertikal
item yang dapat digulir, kami akan menggunakan LisView yang memiliki data yang diisi menggunakan Adaptor. 
Adaptor paling sederhana untuk digunakan disebut ArrayAdapter karena adaptor mengonversi objek ArrayList menjadi item View yang dimuat ke dalam container ListView.

RecyclerView
RecyclerView adalah ViewGroup yang merender tampilan berbasis adaptor dengan cara yang serupa. Itu seharusnya menjadi penerus ListView dan GridView.
Setiap elemen individu dalam daftar ditentukan oleh objek view holder. Anda menentukan view holder dengan memperluas RecyclerView.ViewHolder. 
RecyclerView meminta tampilan tersebut, dan mengikat tampilan ke datanya, dengan memanggil metode di adaptor. Anda menentukan adaptor dengan memperluas RecyclerView.Adapter.
layout manager mengatur elemen individual dalam daftar Anda. Anda dapat menggunakan salah satu pengelola tata letak yang disediakan oleh pustaka RecyclerView, atau Anda dapat menentukan sendiri. 
layout manager semuanya didasarkan pada kelas abstrak LayoutManager perpustakaan.

Adapter
RecyclerView menyertakan jenis adaptor baru. Ini adalah pendekatan yang mirip dengan yang sudah Anda gunakan, tetapi dengan beberapa kekhasan, seperti ViewHolder yang diperlukan.
Anda perlu mengganti tiga metode :
1. onCreateViewHolder()
2. onBindViewHolder()
3. getItemCount()
