Konsep Utama

Cara termudah untuk memulai Pyramid adalah menggunakannya sebagai microframework, di mana seluruh aplikasi Anda berada dalam satu berkas Python (.py). Ini memiliki kerumitan awal yang rendah namun tetap memberi Anda kemampuan untuk berkembang menjadi aplikasi yang lebih besar nanti.

Komponen Kunci dalam Contoh

Tutorial ini menggunakan satu berkas app.py yang menunjukkan empat konsep inti:

View (Baris 6-8: hello_world)
Ini adalah fungsi yang menerima request (permintaan) dari browser dan mengembalikan Response (respons), dalam hal ini adalah HTML sederhana.

Titik Masuk (Baris 11: if __name__ == '__main__':)
Ini adalah standar Python yang memberi tahu skrip untuk menjalankan kode di dalamnya hanya ketika berkas tersebut dieksekusi secara langsung (bukan saat diimpor).

Konfigurasi (Baris 12-14: with Configurator() ...)
Ini adalah inti dari Pyramid. Configurator digunakan untuk menghubungkan berbagai bagian aplikasi. Dalam contoh ini, ia melakukan dua hal:

config.add_route('hello', '/'): Mendaftarkan sebuah route bernama hello untuk URL / (halaman utama).

config.add_view(hello_world, route_name='hello'): Menghubungkan route hello ke fungsi view hello_world.

Server WSGI (Baris 15-17: serve(app, ...) dari waitress)
Setelah aplikasi (app) dikonfigurasi, server WSGI (dalam hal ini waitress) diperlukan untuk menjalankan aplikasi tersebut dan menanggapi permintaan HTTP dari browser.

Tujuan Utama

Tujuan dari langkah ini adalah untuk menjalankan aplikasi web Pyramid yang fungsional dengan cara sesederhana mungkin, sebagai dasar untuk tutorial selanjutnya.
