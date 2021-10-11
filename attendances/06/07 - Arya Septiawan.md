# Rangkuman Pertemuan 6

## Menginstall Flutter

- Menguji coba flutter bab 1  mengubah tampilan project hello world 
- Mencoba mengerjakan flutter bab 2 yaitu membuat struktur aplikasi flutter

Flutter adalah SDK untuk pengembangan aplikasi Mobile yang dikembangkan oleh Google. Sama seperti React Native, Framework ini dapat digunakan untuk membuat atau mengembangkan Aplikasi Mobile yang dapat berjalan pada Device iOS dan Android. Hal yang menarik pada Framework ini adalah semua kodenya di Compile dalam kode Native nya (Android NDK, LLVM, AOT-compiled) tanpa ada Intrepeter pada prosesnya sehingga proses Compile-nya menjadi lebih cepat.

## Aplikasi :

1. Visual Studio Code (VS Code )

2. Flutter SDK (Tutorial Instalasi: https://flutter.dev/docs/get-started/install )

3. Emulator SDK Android (sebenarnya membutuhkan Android Studio untuk emulator, namun kita bisa menggunakan HP kita secara langsung)

## Cek Validasi Flutter VS Code :

1. Kita jalankan Command Line pada VS Code dengan pilih View->Command Pallete.

2. Ketik "doctor", dan pilih Flutter: Run Flutter Doctor.

3. Lihat Output, jika tidak ada notifikasi atau pesan peringatan, kita dapat lanjutkan ke tahap selanjutnya.

## Pengaturan Environment Variables di Windows

1. Silahkan setting pengaturan Environment Variables, edit Path nya agar dapat dibaca oleh system. Ikuti langkah-langkah yang penulis buat.
2. Cari dan pilih system pada properties, environment variables.
Disini silahkan  klik Path pilih edit.
3. Selanjutnya masukkan alamat flutternya yang terdapat di localdisk C, src, flutter, bin.
4. Lakukan hal yang sama seperti langkah diatas, masukkan dart-sdk nya dalam Path.
Pengaturan Device untuk Debugging
5. Langkah ini lakukan untuk setting didalam ponsel hp Anda.Ikuti langkah-langkah serikut :
6. Silahkan cari pengaturan Tentang Ponsel.
7. Disini silahkan anda klik 7 kali pada Nomor Bentukan.
8. Selanjutnya silahkan Anda cari pengaturan tambahan, pilih Opsi Pengembang.
9. Masukkan kode Capthca klik gunakan.
10. Aktifkan Opsi Pengembangnya.
11. Lalu scroll kebagian bawah,disitu terdapat debugging USB silahkan Anda aktifkan.
12. Selanjutnya, Anda buat folder di localdisk D atau dimana saja, kemudian klik kanan didalam folder tersebut untuk mulai membuat project nya, pilih gitbush here. Jika selesai, pastikan bahwa ponsel Android Anda telah disambungkan ke komputer laptop dengan menggunakan kabel USB. Ketikkan perintah dibawah ini :
flutter

$ flutter doctor

13. Jika ada notif seperti itu, Silahkan anda ketikkan perintah seperti dibawah ini :
$ flutter doctor --android-licenses

$ flutter create project1

Ini adalah proses Anda membuat suatu folder project menggunakan git bash. tunggu hingga proses selesai.

## Membuat Project Flutter :

1. Kita jalankan Command Line pada VS Code dengan pilih View->Command Pallete. Ketik "Flutter" dan pilih Flutter: New Project.

2. Masukan nama project aplikasi kita buat. Untuk tutorialnya, saya memberi nama my_app. Pastikan sesuai format aturan penamaan berlaku (tidak menggunakan huruf besar, karakter spesial)
3. Pilih direktori untuk proyek Flutter kita ingin buat. Dan, klik "Select a folder to create the project in"
4. Tunggu beberapa saat sampai Flutter terinstal. Pastikan koneksi internet tersambung.
5. Jika sudah, Flutter pun siap digunakan untuk membangun proyek aplikasi kita.

## Menjalankan Project Flutter :

1. Siapkan HP atau emulator android kita untuk menjalankan proyek Flutter kita. Pastikan status bar kita ada perangkat/device yang terkoneksi. Sebelumnya, saya sarankan menginstall untuk Vysor . Vysor berguna sebagai streaming gawai di laptop. Dengan Vysor, kita dapat mengatur gawai kita dengan laptop tanpa perlu mengawasi gawai kita.
2. Pada Terminal, jalankan flutter run
3. Tunggu sampai aplikasi kita terinstall langsung dengan HP kita.
4. Lalu, buka Vysor dan klik View.
5. Proyek Flutter sudah terinstall di gawai kita dan siap kita gunakan untuk mengembangkan aplikasi kita.

# Apa itu Dart ?

Bahasa pemrograman Dart merupakan bahasa pemrograman General-Purpose yang dirancang oleh Lars Bak dan Kasper Lund.
Dart digunakan untuk mengembangkan berbagai macam platform termasuk di dalamnya adalah web, aplikasi mobile, server, dan perangkat yang mengarah pada teknologi Internet of Things.