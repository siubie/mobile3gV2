# :books: Rangkuman Pertemuan 4

## Aplas B2 - Advanced Widgets

Setelah melakukan praktikum B2 - Advanced Widgets, saya dapat memahami tentang:

1. Mengetahui tentang mengkonfigurasi resource dan project.
2. Mengetahui tentang style, theme, dan drawable vector image.
3. Membuat UI untuk proyek Color Game dengan beberapa attribute onClick.
4. Mendeklarasikan fields yang dibutuhkan aplikasi dan menentukan method untuk check validity to enter the game.
5. Mengetahui cara kerja Countdowntimer.
6. Mengetahui bagaimana cara mengakses array dari resource dan memasukkannya ke dalam List dan Hashtable.
7. Memahami bagaimana cara memulai timer untuk memulai permainan.
8. Memahami bagaimana cara menangani timer dan menghitung skor.

### Pengertian ListView, Adapter, RecycleView

#### ListView
ListView adalah tampilan beberapa item dalam bentuk list yang dapat di scroll secara vertikal. Setiap item akan otomatis dimasukkan kedalam list menggunakan Adapter yang datanya di ambil dari array/database/json/dsb. ListView sering digunakan dalam aplikasi Android, seperti kontak, email, twitter, dsb.

#### Adapter
Adapter adalah jembatan antara dan AdapterView (contohnya ListView) dengan data. Adapter inilah yang menyediakan akses ke item data dan juga bertanggung jawab untuk membuat sebuah View pada setiap item dalam kumpulan data. Selain itu Adapter juga yang mengelola data model. Jadi, dunia ini butuh adapter.

#### RecycleView
Terkadang dalam sebuah aplikasi kita ingin menampilkan sebuah set data yang berjumlah besar (ratusan — atau mungkin sampai jutaan). Nah disini kita tentu perlu sebuah view yang mampu menghandle itu. Adapun sebelum RecyclerView ada namanya ListView. Namun ada beberapa kekurangan yang ada pada ListView. Disini muncullah RecyclerView dengan kemampuan yang lebih baik dari ListView (lebih cepat dan lebih efisien — terutama dalam menangani data berjumlah besar). Adapun contoh penggunaan RecyclerView ada pada GMail.

RecyclerView adalah versi ListView yang lebih canggih dan fleksibel. Widget ini adalah kontainer untuk menampilkan rangkaian data besar yang bisa digulir secara sangat efisien dengan mempertahankan tampilan dalam jumlah terbatas.


### Cara kerja adapter
Adapter akan memanggil method getView() lalu mengembalikan sebuah view pada setiap item dengan menggunakan adapter view. Method getView() ini lah yang mengatur format layout dan kesesuaian data pada item dengan adapter view. Jika getView() mengambalikan View baru untuk setiap waktu ketika dipanggil, ini akan berpengaruh pada performa aplikasi. Jika kita membuat View baru sebagai solusinya, sebenarnya ini terlalu berlebihan karena ketika view baru telah dibuat, maka view yang lama masih akan tersimpan. Untuk itulah android memiliki fitur yang dinamakan dengan recycles yang berfungsi untuk mendaur ulang view ini. 