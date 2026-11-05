# Catatan Minggu 3 Inheritance

## Yang saya kerjakan
Pada minggu ketiga ini saya mengerjakan class yaitu RuangJava,LaptopJava,dan AlatLab.Java,melengkapi field setiap class,konstruktor dengan pemanggilan super(),getter,serta method getJenis() untuk membedakan jenis aset.
## Keputusan desain
Saya meletakkan atribut yang bersifat umum pada class  induk Aset yaitu kode,nama,status dan kondisi.Atribut tersebut bisa untuk semua jenis aset.
Atribut yang mempunyai fungsi khusus saya letakkan pada setiap subclass :
- `Ruang.Java` : atribut kapasitas 
- `Laptop.Java` : atribut spesifikasi dan nomor inventaris untuk membedakan informasi setiap laptop
- `AlatLab.Java` : atribut laboratorium dan tingkat risiko karena membutuhkan informasi khusus mengenai tempat dan tingkat risiko. 
Inheritance kurang cocok digunakan untuk sesuatu yang hanya menjadi komponen dari sebuah projek,contoh : riwayat peminjaman aset lebih cocok menggunakan komposisi karena riwayat tersebut bagian dari aset bukan jenis turunan dari aset 

## Kendala
- Kendala yang saya alami di minggu 3 yaitu penerapan  terkait dengan penggunaan extend,super().Sempat bingung menentukan atribut mana yang di class induk aset dan atribut mana yang dibuat sendiri oleh class turunan.Untuk mengatasinya saya memeriksa kode pada setiap class.

## Penggunaan AI
- Alat yang dipaka:ChatGPT 
- Bagian yang dibantu AI: Membantu melengkapi dan memeriksa class ruang,laptop,dan AlatLab.Membantu memeriksa bagian yang eror. 
- Prompt utama: 
- Membantu melengkapi TODO pada class RUang,Laptop,dan Alatlab.
- Menjelaskan  cara menggunakan inheritance dan pemanggilan super() pada class turunan Java.
- Membantu periksa error pada pengujian.
- Yang saya ubah atau tolak dari saran AI, dan alasannya: Saya menyesuaikan kode yang diberikan AI dengan aturan tugas dan hasil pengujian.
- Satu hal yang saya pahami lebih baik sekarang: Saya memahami bahwa  inheritance digunakan ketika pada suatu class memiliki hubungan dengan class lain.Class turunan bisa gunakan atribut dan method dari class induk melalui extend,penggunaan super() untuk memanggil konstruktor class.

## Hasil Uji

```
PS D:\OOP\oop-202601-250202923> mvn -B -ntp test "-Dgroups=week3"
[INFO] Scanning for projects...
[INFO] Loaded 24375 auto-discovered prefixes for remote repository central (prefixes-central.txt)
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
[INFO] skip non existing resourceDirectory D:\OOP\oop-202601-250202923\core\src\test\resources
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
[INFO] Tests run: 8, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.182 s -- in id.ac.upb.asetpinjam.Minggu03HierarkiTest
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
[INFO] 
[INFO] --- resources:3.3.1:resources (default-resources) @ asetpinjam-api ---
[INFO] Copying 1 resource from src\main\resources to target\classes
[INFO] Copying 0 resource from src\main\resources to target\classes
[INFO] 
[INFO] --- compiler:3.14.1:compile (default-compile) @ asetpinjam-api ---
[INFO] Nothing to compile - all classes are up to date.
[INFO] 
[INFO] --- resources:3.3.1:testResources (default-testResources) @ asetpinjam-api ---
[INFO] skip non existing resourceDirectory D:\OOP\oop-202601-250202923\api\src\test\resources
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
[INFO] Aset-Pinjam Core (minggu 1-11) ..................... SUCCESS [  4.166 s]
[INFO] Aset-Pinjam API (minggu 12-15) ..................... SUCCESS [  1.994 s]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  7.045 s
[INFO] Finished at: 2026-11-05T21:58:29+07:00
[INFO] ------------------------------------------------------------------------

```