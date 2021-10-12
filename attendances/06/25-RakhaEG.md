perbedaan statefull widget dan stateless widget 
Widget dapat berupa stateful atau stateless. Jika widget dapat berubah—ketika pengguna berinteraksi dengannya, misalnya—itu stateful.

Widget stateless tidak pernah berubah. Icon, IconButton, dan Text adalah contoh widget stateless. Subkelas widget stateless StatelessWidget.

Widget stateful bersifat dinamis: misalnya dapat mengubah tampilannya sebagai respons terhadap peristiwa yang dipicu oleh interaksi pengguna atau saat menerima data. Kotak centang, Radio, Slider, InkWell, Form, dan TextField adalah contoh widget stateful. Subkelas widget stateful StatefulWidget.

Status widget disimpan dalam objek State, memisahkan status widget dari tampilannya. Status terdiri dari nilai-nilai yang dapat berubah, seperti nilai slider saat ini atau apakah kotak centang dicentang. Saat status widget berubah, objek status memanggil setState(), memberi tahu kerangka kerja untuk menggambar ulang widget

createState() untuk membuat objek State. Framework memanggil createState() saat ingin membangun widget.
Memanggil setState memberi tahu kerangka kerja bahwa keadaan internal objek ini telah berubah dengan cara yang mungkin berdampak pada antarmuka pengguna di 
