# Catatan Minggu 02: Struktur OOP - Class, Object, dan Encapsulation

## Yang saya kerjakan
Pada minggu 2, saya mengerjakan class `Aset.java` dengan menambahkan atribut, konstruktor, getter, dan setter. Saya menggunakan `private` pada setiap atribut agar data tidak bisa diakses langsung dari luar class. Saya juga menambahkan validasi supaya kode dan nama tidak kosong, serta status dan kondisi tidak boleh bernilai null. Setelah selesai, saya menjalankan pengujian dan berhasil melewati 6 test tanpa kegagalan.

## Keputusan desain
Saya menggunakan `private` untuk menerapkan konsep encapsulation. Atribut kode menggunakan `final` karena nilainya tidak boleh diubah setelah objek dibuat. Untuk nilai awal, status diatur menjadi `TERSEDIA` dan kondisi menjadi `BAIK`. Saya menggunakan `trim()` untuk mengecek apakah kode dan nama kosong atau hanya berisi spasi, tetapi nilai aslinya tetap disimpan. Selain itu, saya menggunakan `IllegalArgumentException` untuk menolak input yang tidak sesuai.

## Kendala
Pada awal pengerjaan, saya sempat mengalami kendala `Execution Policy` di PowerShell saat menjalankan pengujian. Setelah itu, saya menggunakan perintah Maven `mvn test -Dgroups=week2` untuk menjalankan pengujian khusus Minggu 2. Hasilnya, pengujian berhasil dengan `BUILD SUCCESS` dan 6 test tanpa kegagalan.

## Penggunaan AI
- Alat yang dipakai: ChatGPT.

- Bagian yang dibantu: Pengerjaan class `Aset.java`, terutama atribut, konstruktor, getter, setter, dan validasi.

- Prompt utama:
1. Bantu lengkapi kode `Aset.java` sesuai ketentuan tugas minggu 2.
2. Jelaskan fungsi kode `Aset.java` dengan bahasa yang mudah dipahami.
3. Apa fungsi perintah Maven untuk menjalankan test minggu 2?

- Yang saya ubah atau tolak: Saya tetap membiarkan bagian `TODO` untuk minggu 3, 4, dan 5 karena belum menjadi bagian dari tugas minggu 2.

- Hal yang saya pahami: Saya jadi lebih memahami cara kerja encapsulation, fungsi `private`, `final`, `getter`, dan `setter`, serta pentingnya validasi agar data yang dimasukkan sesuai ketentuan.
