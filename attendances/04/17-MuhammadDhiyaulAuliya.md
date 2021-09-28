# Rangkuman Pertemuan 4

## B2 : Java - Advnced Widgets Java Edition

### Task :

1. Define color, string, and integer resources
2. Define theme, style, and drawable resources
3. Completing the layout (UI)
4. Create validation method
5. Create method to start CountDownTimer
6. Create method to load color data to List and Hashtable
7. Create method to start game
8. Create method to response user input and calculate score

## Pengertian ListView, Adapter, RecycleView

**ListView**

adalah tampilan beberapa item dalam bentuk list yang dapat di scroll secara vertikal. Setiap item akan otomatis dimasukkan kedalam list menggunakan Adapter yang datanya di ambil dari array/database/json/dsb. ListView sering digunakan dalam aplikasi Android, seperti kontak, email, twitter, dsb.

**Adapter**

adalah jembatan antara dan AdapterView (contohnya ListView) dengan data. Adapter inilah yang menyediakan akses ke item data dan juga bertanggung jawab untuk membuat sebuah View pada setiap item dalam kumpulan data. Selain itu Adapter juga yang mengelola data model. Jadi, dunia ini butuh adapter.

**RecycleView**

Terkadang dalam sebuah aplikasi kita ingin menampilkan sebuah set data yang berjumlah besar (ratusan — atau mungkin sampai jutaan). Nah disini kita tentu perlu sebuah view yang mampu menghandle itu. Adapun sebelum RecyclerView ada namanya ListView. Namun ada beberapa kekurangan yang ada pada ListView. Disini muncullah RecyclerView dengan kemampuan yang lebih baik dari ListView (lebih cepat dan lebih efisien — terutama dalam menangani data berjumlah besar). Adapun contoh penggunaan RecyclerView ada pada GMail.

**RecyclerView** 

adalah versi ListView yang lebih canggih dan fleksibel. Widget ini adalah kontainer untuk menampilkan rangkaian data besar yang bisa digulir secara sangat efisien dengan mempertahankan tampilan dalam jumlah terbatas.
