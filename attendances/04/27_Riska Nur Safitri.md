Rangkuman Pertemuan 4 :

1. Mengerjakan Tugas B2 - Advanced Widget Java
    - Mengidentifikasi warna, string, dan resource interger
    - Mengidentifikasi tema, style, dan resource drawable
    - Layout UI
    - Validasi method
    - Method start CountDownTimer
    - Method load color data 
    - Method startgame

2. ListView
    - Dalam pengembangan Android, setiap kali kita ingin menampilkan daftar vertikal item yang dapat digulir, kita akan menggunakan LisView yang memiliki data yang diisi menggunakan Adaptor.
    - Adaptor paling sederhana adalah ArrayAdapter karena mengonversi objek ArrayList menjadi item View yang dimuat ke dalam container ListView.

3. Using ArrayAdapter
    ArrayAdapter<String> itemsAdapter =  new ArrayAdapter<String>(this, android.R.layout.simple_list_item_1, items);
    ListView listView = findViewById(R.id.lvItems);
    listView.setAdapter(itemsAdapter);

4. Using Custom ArrayAdapter
    - Menentukan model
    - Membuat tampilan template
    - Menentukan Adaptor -> Warisan ArrayAdapter
    - Memasang Adaptor ke ListView
    - Mengisi Data ke ListView

5. RecylerView
    - RecyclerView adalah ViewGroup yang merender tampilan berbasis adaptor dengan cara yang serupa. Setiap elemen individu dalam daftar ditentukan oleh objek view holder. 

6. LayoutManager
    - LinearLayoutManager : menampilkan item dalam daftar gulir vertikal atau horizontal.
    - GridLayoutManager : menampilkan item dalam kotak.
    - StaggeredGridLayoutManager : menampilkan item dalam kisi terhuyung.

7. Adapter
    - RecyclerView menyertakan jenis adaptor baru.

