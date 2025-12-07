## PENGENALAN DART PACKAGES

- Ekosistem dart menggunakan packages untuk melakukan manajemen software yang bisa di sharing. seperti library atau tool.
- saat kita membuat project d Dart, sebenarnya secara tidak langsung kita membuat packages
- packages bisa dalam bentuk aplikasi atau libary (yang digunakan pada aplikasi)

KEUNTUNGAN MENGGUNAKAN DART PACKAGES
- dengan menggunakan packages, kita akan mengikuti cara management kode Dart
- dengan packages juga kita bisa melakukan dependency management secara otomatis tanpa harus download library yang kita butuhkan secara manual

## MEMBUAT PROJECT LIBRARY 

perintah :
dart create--template=package-simple pzn_belajar_dart_library

## STRUKTUR DIRECTORY PACKAGES

- salah satu keuntungan menggunakan packages adalah, struktur directory yang standard untuk project di Dart
- secara minimal, saat kita membuat dart packages, hanya butuh file pubspec.yaml dan folder lib
- pubspec.yaml digunakan untuk konfigurasi dart packages nya, sedangkan folder lib untuk menyimpan kode program dart kita
- Namun saat kita membuat project menggunakan perintah dart create, struktur direktorinya lebih kompleks