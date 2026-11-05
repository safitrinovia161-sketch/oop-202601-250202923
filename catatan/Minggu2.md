# Catatan Minggu 2: Struktur OOP: Class, Object, Encapsulation

## Yang saya kerjakan
Saya melengkapi bagian TODO pada Aset.java membuat atribut kode,nama,status dan kodisi menjadi private agar tidak bisa diakses secara langsung dari luar kelas dan membuat konstruktor,getter,setter dan menambahkan vakidasi pada data.

## Keputusan desain
Saya menggunakan atribut private supaya data di class Aset aman tidak bisa diubah dari luar class.Saya menggunakan getter untuk mengambil nilai atribut dan setter mengubah nilai atribut.Saya mengatur nilai awal status menjadi TERSEDIA dan kondisi menjadi BAIK.


## Kendala
-  Ketika menjalankan program ,output yang muncul diterminal tidak sesuai dengan yang saya harapkan dan Ketika diuji di ps1 terjadi error saya mengatasinnya dengan mvn -f core/pom.xml -Dtest=Minggu02AsetTest test

## Penggunaan AI
- Alat yang dipaka:ChatGPT 
- Bagian yang dibantu AI: Menjelaskan tugas minggu ke2,melengkapi TODO dan memahami penyebab eror pada saat menjalankan pengujian 
- Prompt utama: Jelaskan tugas minggu ke dua dan lengkapi kode pada bagian TODO sesuai dengan intruksi minggu ke dua.
- Yang saya ubah atau tolak dari saran AI, dan alasannya: Saya menyesuaikan kode agar bagian yang dikerjakan hanya minggu ke dua dan tetap mempertahankan method minggu ke 3,4,5. 
- Satu hal yang saya pahami lebih baik sekarang: Yang saya pahami konsep enkapsulasi,fungsi dari atribut private ,konstruktor,getter,dan setter.