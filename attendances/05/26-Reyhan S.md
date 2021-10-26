Catatan
Animasi dan Multimedia

Pengenalan pada animasi:

-	Animasi Bitmap
-	Visibilitas dan Gerakan UI
-	Gerak Berbasis Fisika
-	Menganimasikan perubahan Tata Letak
-	Menganimasikan diantara aktifitas

Bitmap Animation atau animasi bitmap

Saat Anda ingin menganimasikan grafik bitmap seperti ikon atau ilustrasi, Anda harus menggunakan API animasi yang dapat digambar. 
Salah satu cara untuk menganimasikan Drawable adalah memuat serangkaian sumber daya Drawable satu demi satu untuk membuat animasi. Ini adalah animasi tradisional dalam arti dibuat dengan urutan gambar yang berbeda, diputar secara berurutan, seperti gulungan film. Kelas AnimationDrawable adalah dasar untuk animasi Drawable. Ini lebih mudah dilakukan dengan satu file XML yang mencantumkan bingkai yang menyusun animasi. File XML untuk jenis animasi ini berada di direktori res/drawable/ dari proyek Android Anda. Dalam hal ini, instruksinya adalah urutan dan durasi untuk setiap frame animasi.
File XML terdiri dari elemen <animation-list> sebagai simpul akar dan serangkaian simpul <item> anak yang masing-masing menentukan bingkai: sumber daya yang dapat digambar untuk bingkai dan durasi bingkai. Berikut adalah contoh file XML untuk animasi Drawable
Animasi ini berjalan hanya untuk tiga frame. Dengan menyetel atribut android:oneshot dari daftar ke true, itu akan berputar sekali saja lalu berhenti dan tahan pada frame terakhir. Jika disetel salah maka animasi akan berulang. Dengan XML ini disimpan sebagai rocket_thrust.xml di direktori res/drawable/ proyek, XML dapat ditambahkan sebagai gambar latar belakang ke View dan kemudian dipanggil untuk bermain. Berikut adalah contoh Aktivitas, di mana animasi ditambahkan ke ImageView dan kemudian dianimasikan saat layar disentuh.


Animate UI visibility and motion atau visibilitas dan Gerakan UI

Saat Anda perlu mengubah visibilitas atau posisi tampilan dalam tata letak Anda, Anda harus menyertakan animasi halus untuk membantu pengguna memahami bagaimana UI berubah.
Untuk memindahkan, mengungkapkan, atau menyembunyikan tampilan dalam tata letak saat ini, Anda dapat menggunakan sistem animasi properti yang disediakan oleh paket android.animation, tersedia di Android 3.0 (API level 11) dan yang lebih tinggi. API ini memperbarui properti objek Tampilan Anda selama periode waktu tertentu, terus menggambar ulang tampilan saat properti berubah. 

Saat aplikasi Anda digunakan, informasi baru perlu ditampilkan di layar saat informasi lama dihapus. Segera beralih apa yang ditampilkan dapat terlihat menggelegar atau pengguna dapat dengan mudah melewatkan konten baru di layar. Memanfaatkan animasi dapat memperlambat perubahan dan menarik perhatian pengguna dengan gagasan sehingga pembaruan lebih jelas.
Ada tiga animasi umum yang digunakan saat menampilkan atau menyembunyikan tampilan. Anda dapat menggunakan animasi pengungkapan melingkar, animasi crossfade, atau animasi cardflip.

Cara Membuat animasi crossfade

Animasi crossfade (juga dikenal sebagai dissolve) secara bertahap memudarkan satu View atau ViewGroup sementara secara bersamaan memudar di yang lain. Animasi ini berguna untuk situasi di mana Anda ingin mengganti konten atau tampilan di aplikasi Anda. Animasi crossfade yang ditampilkan di sini menggunakan ViewPropertyAnimator, yang tersedia untuk Android 3.1 (API level 12) dan yang lebih tinggi.

Pertama, Anda perlu membuat dua tampilan yang ingin Anda crossfade. Contoh berikut membuat indikator kemajuan dan tampilan teks yang dapat digulir:

-	Siapkan animasi crossfade
Untuk mengatur animasi crossfade:
Buat variabel anggota untuk tampilan yang ingin Anda crossfade. 
Untuk tampilan yang memudar, atur visibilitasnya ke GONE. Ini mencegah tampilan mengambil ruang tata letak dan menghilangkannya dari perhitungan tata letak, mempercepat pemrosesan.
Cache properti sistem config_shortAnimTime dalam variabel anggota. Properti ini mendefinisikan durasi "pendek" standar untuk animasi. 

-	Gerak berbasis fisika atau physics based motion
Bila memungkinkan, animasi Anda harus menerapkan fisika dunia nyata sehingga terlihat alami.
Untuk menyediakan perilaku ini, pustaka Dukungan Android menyertakan API animasi berbasis fisika yang mengandalkan hukum fisika untuk mengontrol bagaimana animasi Anda terjadi.

-	Menganimasikan gerakan menggunakan fisika pegas atau animate movement using spring physic
Gerak berbasis fisika didorong oleh gaya. Gaya pegas adalah salah satu gaya yang memandu interaktivitas dan gerak. Gaya pegas memiliki sifat-sifat sebagai berikut: redaman dan kekakuan. Dalam animasi berbasis pegas, nilai dan kecepatan dihitung berdasarkan gaya pegas yang diterapkan pada setiap frame.

-	Menganimasikan perubahan tata letak atau animate layout changes
Di Android 4.4 (API level 19) dan yang lebih tinggi, Anda dapat menggunakan kerangka kerja transisi untuk membuat animasi saat Anda menukar tata letak dalam aktivitas atau fragmen saat ini. Anda dapat menggunakan ini untuk menukar seluruh UI atau untuk memindahkan/mengganti hanya beberapa tampilan.
Misalnya, saat pengguna mengetuk item untuk melihat informasi selengkapnya, Anda dapat mengganti tata letak dengan detail item, menerapkan transisi.

-	Menganimasikan perubahan tata letak menggunakan transisi atau animate layout changes using a transition.
Kerangka transisi Android memungkinkan Anda untuk menganimasikan semua jenis gerakan di UI hanya dengan menyediakan tata letak awal dan tata letak akhir. 
Kerangka transisi mencakup fitur-fitur berikut:
Animasi tingkat grup: Menerapkan satu atau beberapa efek animasi ke semua tampilan dalam hierarki tampilan.
Animasi bawaan: Gunakan animasi yang telah ditentukan sebelumnya untuk efek umum seperti fade out atau gerakan.
Dukungan file sumber daya: Memuat hierarki tampilan dan animasi bawaan dari file sumber daya tata letak.
Callback siklus hidup: Menerima panggilan balik yang memberikan kontrol atas proses animasi dan perubahan hierarki.

-	Animasikan di antara aktivitas atau animate between activities
Di Android 5.0 (API level 21) dan yang lebih tinggi, Anda juga dapat membuat animasi yang bertransisi di antara aktivitas Anda.
Anda dapat menerapkan animasi sederhana seperti menggeser aktivitas baru dari samping atau memudarkannya, tetapi Anda juga dapat membuat animasi yang bertransisi antara tampilan bersama di setiap aktivitas. Misalnya, ketika pengguna mengetuk item untuk melihat informasi lebih lanjut, Anda dapat beralih ke aktivitas baru dengan

-	Animasikan di antara aktivitas

Transisi aktivitas dalam aplikasi desain material menyediakan koneksi visual antara status yang berbeda melalui gerakan dan transformasi antara elemen umum. Anda dapat menentukan animasi kustom untuk transisi masuk dan keluar dan untuk transisi elemen bersama di antara aktivitas.
Transisi masuk menentukan bagaimana tampilan dalam suatu aktivitas memasuki adegan. Misalnya, dalam transisi meledak masuk, pandangan memasuki adegan dari luar dan terbang ke tengah layar.
Transisi keluar menentukan bagaimana tampilan dalam aktivitas keluar dari adegan. Misalnya, dalam transisi keluar meledak, tampilan keluar dari adegan menjauh dari pusat.
Transisi elemen bersama menentukan bagaimana pandangan yang dibagikan antara dua aktivitas bertransisi di antara aktivitas ini. Misalnya, jika dua aktivitas memiliki gambar yang sama dalam posisi dan ukuran yang berbeda, transisi elemen bersama changeImageTransform diterjemahkan





Multimedia

Kerangka kerja multimedia Android mencakup dukungan untuk memutar berbagai jenis media umum, sehingga Anda dapat dengan mudah mengintegrasikan audio, video, dan gambar ke dalam aplikasi Anda.
Dokumen ini menunjukkan kepada Anda cara menggunakan MediaPlayer untuk menulis aplikasi pemutar media yang berinteraksi dengan pengguna dan sistem untuk mendapatkan kinerja yang baik dan pengalaman pengguna yang menyenangkan. Atau, Anda mungkin ingin menggunakan ExoPlayer, yang merupakan pustaka sumber terbuka yang dapat disesuaikan yang mendukung fitur berkinerja tinggi yang tidak tersedia di MediaPlayer

Kelas berikut digunakan untuk memutar suara dan video dalam kerangka kerja Android:
MediaPlayer Kelas ini adalah API utama untuk memutar suara dan video.
AudioManager Kelas ini mengelola sumber audio dan output audio pada perangkat.

Deklarasi manifes atau manifest declarations

Kelas berikut digunakan untuk memutar suara dan video dalam kerangka kerja Android:
Izin Internet - Jika Anda menggunakan MediaPlayer untuk mengalirkan konten berbasis jaringan, aplikasi Anda harus meminta akses jaringan.

Menggunakan mediaplayer atau using mediaplayer

Salah satu komponen terpenting dari kerangka kerja media adalah kelas MediaPlayer. Objek kelas ini dapat mengambil, mendekode, dan memutar audio dan video dengan pengaturan minimal. Ini mendukung beberapa sumber media yang berbeda seperti:
Sumber daya lokal
URI internal, seperti yang mungkin Anda peroleh dari Content Resolver
URL eksternal (aliran)
Untuk daftar format media yang didukung Android, lihat halaman Format Media yang Didukung.
Berikut adalah contoh cara memutar audio yang tersedia sebagai sumber mentah lokal (disimpan di direktori res/raw/ aplikasi Anda).








