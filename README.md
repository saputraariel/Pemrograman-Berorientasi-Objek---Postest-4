# Pemrograman-Berorientasi-Objek---Postest-4

TEMA : Sistem Manajemen ALat2 Musik Tradisional

Mohamad Ariel Saputra D Loi

Sistem Informasi C 2024

2409116087

# Penjelasan Program

## AlatMusik.Java (Abstarct Class)

<img width="743" height="146" alt="image" src="https://github.com/user-attachments/assets/8f77181e-c54a-459e-8cf9-33dc23aa8cf1" />

Bagian awal ini mendefinisikan sebuah class abstract bernama AlatMusik. Class ini bersifat abstract sehingga tidak bisa dibuat objek langsung, tetapi hanya bisa diturunkan pada class lain. Di dalamnya terdapat dua atribut nama dan asal yang digunakan untuk menyimpan informasi dasar tentang alat musik tradisional.

<img width="761" height="123" alt="image" src="https://github.com/user-attachments/assets/1dd4d126-47cc-46de-a41f-23639dc9345b" />

Kode ini adalah constructor dari class AlatMusik. Constructor digunakan untuk memberikan nilai awal pada atribut nama dan asal ketika objek baru dibuat. Kata kunci this dipakai untuk membedakan antara parameter dan atribut di dalam class. Dengan constructor ini, setiap alat musik yang dibuat akan langsung memiliki nama dan asalnya.

<img width="897" height="168" alt="image" src="https://github.com/user-attachments/assets/44581468-b434-4c88-be0b-460af7ce88a0" />

mainkan(). Method abstract tidak memiliki isi, sehingga setiap class turunan wajib membuat implementasi sendiri tentang bagaimana alat musik tersebut dimainkan.Method tampilkanInfo() pertama digunakan untuk menampilkan informasi sederhana berupa nama dan asal alat musik. Method ini sudah memiliki isi supaya bisa langsung dipanggil oleh class turunan tanpa harus di override.

<img width="1074" height="275" alt="image" src="https://github.com/user-attachments/assets/5f9da6e1-8667-41fa-ad97-c2fd6089868a" />

Method tampilkanInfo(boolean detail) adalah bentuk Polymorphism dengan Overloading. Method ini memiliki nama yang sama dengan method sebelumnya, tetapi parameternya berbeda. Jika parameter detail bernilai true, maka informasi ditampilkan lebih lengkap.

## Perawatan.Java (Interface)

<img width="502" height="185" alt="image" src="https://github.com/user-attachments/assets/01ce1b21-cde1-4184-8a6c-509c02396ed5" />

interface hanya berisi deklarasi tanpa isi, setiap class yang menggunakan Perawatan wajib membuat implementasi sendiri untuk method rawat(). Bagian ini juga merupakan contoh penerapan Abstraction, karena hanya menyediakan aturan umum.

## Main.java (Main Class)

<img width="1047" height="579" alt="image" src="https://github.com/user-attachments/assets/b2fb6128-e62d-4e59-84df-07b5688c9c65" />

Class Main berfungsi sebagai titik masuk program dengan method main(). Di dalamnya dibuat objek Gamelan dan Angklung yang bertipe AlatMusik untuk menunjukkan konsep polymorphism. Kedua objek memanggil method tampilkanInfo() dalam dua versi (overloading), lalu method mainkan() (overriding) untuk menampilkan cara memainkan alat musik, serta method rawat() dari interface Perawatan setelah dilakukan casting. Bagian ini memperlihatkan gabungan penggunaan abstraksi, interface, overloading, dan overriding dalam satu eksekusi program.

## Angklung.java

<img width="1019" height="179" alt="image" src="https://github.com/user-attachments/assets/7dd36b42-cd42-49a5-ae79-67519baa1a11" />

Class Angklung juga merupakan turunan dari AlatMusik dan mengimplementasikan Perawatan. Constructor menerima parameter nama dan asal, lalu meneruskannya ke constructor superclass agar atribut langsung terisi saat objek dibuat.

<img width="1477" height="348" alt="image" src="https://github.com/user-attachments/assets/63f24173-2c94-418c-9ee6-0d9e40a82107" />

Method mainkan() merupakan hasil override dari abstract method di AlatMusik.Method rawat() adalah implementasi dari interface Perawatan. Pada angklung, perawatan yang dituliskan adalah dijemur agar bambu tidak lembab.

## Gamelan.java

<img width="884" height="173" alt="image" src="https://github.com/user-attachments/assets/96f22fbc-c247-4e93-b40a-dd4140569842" />

Class Gamelan dibuat sebagai turunan dari AlatMusik sekaligus mengimplementasikan interface Perawatan. Kata kunci extends dipakai untuk mewarisi dari abstract class AlatMusik, sedangkan implements dipakai untuk menggunakan interface Perawatan.

<img width="1100" height="329" alt="image" src="https://github.com/user-attachments/assets/fb7739be-bd53-442c-99d7-34f800d83057" />

Method mainkan() di sini adalah implementasi dari method abstract yang ada di AlatMusik.Karena interface hanya berupa aturan, maka Gamelan harus mendefinisikan sendiri cara perawatan gamelan. Implementasi yang dibuat adalah menyatakan bahwa gamelan dirawat dengan cara disimpan di tempat kering


