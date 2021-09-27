Absensi Pertemuan 4

Pada Task Guide 1 kita harus membuat project baru dengna nama ColorGameX dengan ketentuan menggunakan bahawa java dan target API Andorid 5.0 (Lolipop)

Kemudian update isi color dengan spesifikasi yang sudah ada di guide 01

kemudian menambahkan app name dengan nilai APLAS COLOR GAME

menambahkan integer dengan beberapa nilai dan nama yang telah ditentukan. 

kemudian menambahkan array dengan nama colorList dan menambahkan array dengan nama charList

kemudian kita tambahkan beberapa item didalam file themes

membuat activity baru dengan nama class MyActivity dan nama Layout activity_Layout

update gradle sesuai dengan yang ada di modul dan jangan lupa syc now

setelah itu running file test 011 dan 012

Pada Tast Guide 2 kita copy file ic_resicon.xml yang ada di dalam folder suplement kedalam folder drawable

kemudian kita buat file baru dengan nama round_btn 

pada file round_btn kita buat sebuah corners untuk menentukan radius dari sebuah button

membuat gradient untuk mengatur komposisi warna dan samaran warna pada button 

membuat size untuk menentukan ukuran besar kecilnya button

menentukan padding untuk mengatur jarak button 

kemudian kita tambahkan ColoredButton pada file themes untuk menentukan width dan height button

dan lakukan running pada file test 021 yang akan melakukan pengecekan pada ColoredButton, ProggressBar, ResIconDrawable, dan RoundBtnDrawable

kemudian pada Task Guide 3 kita sudah mulai masuk untuk mengerjakan desin layout

pada task ini kita sudah mulai mengerjakan layout dan class java untuk melakukan pengaturan proses yang harus berjalan di layout 

pada task 4 mendeklarasikan variable di class MyActivity pada task guide ini kita akan memahami bagaimana cara mendeklarasikan variable

kemudian pada task guide 5 kita membuat method dengan modifier private dan nama initTime 

method tersebut adalah method tanpa parameter

kemudian mendaklarasikan CountDownTimer yang digunakan untuk mengupdate waktu

kemudian membuat method dengan nama initColorList

kemudian kita tetapkan data warna sesuai dengan yang ada di colorList

kemudia kita deklarasikan array dengan nama temp

kemudian kita menetapkan elmen dari charList untuk digunakan sebagi kata kunci dengan menggunakan perulangan for

kemudian kita panggil method initColorList didalam method onCreate

kemudian kita buat method untuk memulai game tersebut

kemudian kita buat method untuk melakukan inputan dan melakukan perhitungan score

**LIST VIEW**
- Dalam pengembangan Android, setiap kali kami ingin menampilkan daftar vertikal item yang dapat digulirkan, kami akan menggunakan LisView yang memiliki data yang diisi menggunakan Adapter
- Adapter paling sederhana untuk digunakan disebut ArrayAdapter karena adaptor mengubah ArrayList objek menjadi Item Tampilan yang dimuat ke dalam wadah ListView.

**RECYCLE VIEW**
- RecyclerView adalah ViewGroup yang membuat tampilan berbasis adaptor dengan cara yang sama. Ini seharusnya menjadi penerus ListView dan GridView. 
- Setiap elemen individu dalam daftar ditentukan oleh objek pemegang tampilan. Anda menentukan pemegang tampilan dengan memperluas 
- RecyclerView meminta tampilan tersebut, dan mengikat tampilan ke data mereka, dengan memanggil metode di adaptor. Anda menentukan adaptor dengan memperluas RecyclerView.Adapter.
- Manajer tata letak mengatur elemen individual dalam daftar Anda. Anda dapat menggunakan salah satu pengelola tata letak yang disediakan oleh pustaka RecyclerView, atau Anda dapat menentukan sendiri. Pengelola tata letak semuanya didasarkan pada kelas abstrak LayoutManager pustaka
