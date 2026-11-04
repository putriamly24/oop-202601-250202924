# Catatan Minggu 03: Inheritance

## Yang saya kerjakan
Pada minggu 3, saya membuat tiga class Java, yaitu `Ruang.java`, `Laptop.java`, dan `AlatLab.java` yang merupakan turunan dari class `Aset`. Saya menerapkan konsep inheritance menggunakan extends dan super, menambahkan atribut serta getter sesuai kebutuhan masing-masing class, dan melakukan validasi pada data yang dimasukkan. Saya juga menggunakan `@Override` untuk menentukan jenis aset pada setiap class.

## Keputusan desain
Saya meletakkan atribut yang digunakan bersama, seperti kode, nama, status, dan kondisi, di dalam class `Aset`. Sementara itu, atribut khusus diletakkan pada masing-masing class turunana:
- `Ruang.java`: kapasitas.
- `Laptop.java`: spesifikasi dan nomor investaris.
- `AlatLab.java`: labolatorium dan tingkat risiko.

## Kendala
Kendala yang saya alami adalah memahami penggunann `extends`, `super`, dan `@override` dalam inheritance. Setelah mencoba menerapkan dan menjalankan pengujian menggunakan Maven, seluruh 8 test berhasil.

## Penggunaan AI
- Alat yang dipakai: ChatGPT
- Bagian yang dibantu AI: Memperoleh referensi dan penjelasan terkait penerapan konsep inheritance, penggunaan `extends` dan `super`, serta penerapan validasi pada class turunan.
- Prompt utama: Meminta penjelasan dan arahan terkait penerapan konsep inheritance, penggunaan `extends` dan `super`, serta penerapan validasi pada class turunan.

- Yang saya ubah atau tolak dari saran AI, dan alasannya:  Saya tetap mempertahankan bagian TODO untuk Minggu 4 agar tidak mengerjakan materi di luar tugas minggu ini.
- Satu hal yang saya pahami lebih baik sekarang: Saya lebih memahami bahwa inheritance dapat digunakan untuk mewariskan atribut dan method dari class induk ke class turunan sehingga kode menjadi lebih terstruktur dan tidak perlu ditulis berulang.

## Hasil Pengujian

```
PS D:\code\oop-202601-250202924> mvn -B -ntp test "-Dgroups=week3"
[INFO] Scanning for projects...
[INFO] Loaded 24360 auto-discovered prefixes for remote repository central (prefixes-central.txt)
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Build Order:
[INFO] 
[INFO] Aset-Pinjam (OOP 202601)                                           [pom]
[INFO] Aset-Pinjam Core (minggu 1-11)                                     [jar]
[INFO] Aset-Pinjam API (minggu 12-15)                                     [jar]
[INFO] 
[INFO] --------------------< id.ac.upb:asetpinjam-parent >---------------------
[INFO] Building Aset-Pinjam (OOP 202601) 0.1.0                            [1/3]
[INFO]   from pom.xml
[INFO] --------------------------------[ pom ]---------------------------------
[INFO] 
[INFO] ---------------------< id.ac.upb:asetpinjam-core >----------------------
[INFO] Building Aset-Pinjam Core (minggu 1-11) 0.1.0                      [2/3]
[INFO]   from core\pom.xml
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] Loaded 64 auto-discovered prefixes for remote repository apache.snapshots (prefixes-apache.snapshots.txt)
[INFO] 
[INFO] --- resources:3.3.1:resources (default-resources) @ asetpinjam-core ---
[INFO] Copying 0 resource from src\main\resources to target\classes
[INFO] Copying 1 resource from src\main\resources to target\classes
[INFO] 
[INFO] --- compiler:3.14.1:compile (default-compile) @ asetpinjam-core ---
[INFO] Nothing to compile - all classes are up to date.
[INFO] 
[INFO] --- resources:3.3.1:testResources (default-testResources) @ asetpinjam-core ---
[INFO] skip non existing resourceDirectory D:\code\oop-202601-250202924\core\src\test\resources
[INFO] 
[INFO] --- compiler:3.14.1:testCompile (default-testCompile) @ asetpinjam-core ---
[INFO] Nothing to compile - all classes are up to date.
[INFO] 
[INFO] --- surefire:3.5.6:test (default-test) @ asetpinjam-core ---
[INFO] Using auto detected provider org.apache.maven.surefire.junitplatform.JUnitPlatformProvider
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running id.ac.upb.asetpinjam.Minggu03HierarkiTest
[INFO] Tests run: 8, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.165 s -- in id.ac.upb.asetpinjam.Minggu03HierarkiTest
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 8, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] 
[INFO] ----------------------< id.ac.upb:asetpinjam-api >----------------------
[INFO] Building Aset-Pinjam API (minggu 12-15) 0.1.0                      [3/3]
[INFO]   from api\pom.xml
[INFO] --------------------------------[ jar ]---------------------------------
[WARNING] Could not transfer metadata /.meta/prefixes.txt from/to spring-milestones (https://repo.spring.io/milestone): No such host is known (repo.spring.io)
[INFO] 
[INFO] --- resources:3.3.1:resources (default-resources) @ asetpinjam-api ---
[INFO] Copying 1 resource from src\main\resources to target\classes
[INFO] Copying 0 resource from src\main\resources to target\classes
[INFO] 
[INFO] --- compiler:3.14.1:compile (default-compile) @ asetpinjam-api ---
[INFO] Nothing to compile - all classes are up to date.
[INFO] 
[INFO] --- resources:3.3.1:testResources (default-testResources) @ asetpinjam-api ---
[INFO] skip non existing resourceDirectory D:\code\oop-202601-250202924\api\src\test\resources
[INFO] 
[INFO] --- compiler:3.14.1:testCompile (default-testCompile) @ asetpinjam-api ---
[INFO] Nothing to compile - all classes are up to date.
[INFO] 
[INFO] --- surefire:3.5.6:test (default-test) @ asetpinjam-api ---
[INFO] Using auto detected provider org.apache.maven.surefire.junitplatform.JUnitPlatformProvider
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 0, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Summary for Aset-Pinjam (OOP 202601) 0.1.0:
[INFO] 
[INFO] Aset-Pinjam (OOP 202601) ........................... SUCCESS [  0.006 s]
[INFO] Aset-Pinjam Core (minggu 1-11) ..................... SUCCESS [  4.495 s]
[INFO] Aset-Pinjam API (minggu 12-15) ..................... SUCCESS [  2.443 s]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  10.572 s
[INFO] Finished at: 2026-11-04T13:56:21+07:00
[INFO] ------------------------------------------------------------------------
PS D:\code\oop-202601-250202924>
```
