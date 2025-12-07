## PENGENALAN DART PACKAGES

- Ekosistem dart menggunakan packages untuk melakukan manajemen software yang bisa di sharing. seperti library atau tool.
- saat kita membuat project d Dart, sebenarnya secara tidak langsung kita membuat packages
- packages bisa dalam bentuk aplikasi atau libary (yang digunakan pada aplikasi)

KEUNTUNGAN MENGGUNAKAN DART PACKAGES
- dengan menggunakan packages, kita akan mengikuti cara management kode Dart
- dengan packages juga kita bisa melakukan dependency management secara otomatis tanpa harus download library yang kita butuhkan secara manual

## MEMBUAT PROJECT LIBRARY 

contoh di file :
LIBRARY\pzn_belajar_dart_library

perintah :
dart create--template=package-simple pzn_belajar_dart_library

## STRUKTUR DIRECTORY PACKAGES

- salah satu keuntungan menggunakan packages adalah, struktur directory yang standard untuk project di Dart
- secara minimal, saat kita membuat dart packages, hanya butuh file pubspec.yaml dan folder lib
- pubspec.yaml digunakan untuk konfigurasi dart packages nya, sedangkan folder lib untuk menyimpan kode program dart kita
- Namun saat kita membuat project menggunakan perintah dart create, struktur direktorinya lebih kompleks

DIRECTORY SRC
- salah satu best practice di dart packages adalah, tidak mengekspos kode dart kecuali memang dibutuhkan
- dan salah satu best practic yang dilakukan di dart packages, biasanya kode program dart akan di tempatkan di folder src di dalam folder lib
- semua kode program dart di dalam src, secara default tidak di ekspos ke luar
- ketika kita butuh mengekspos keluar (artinya bisa diakses oleh project lain), maka biasanya dilakukan secara eksplisit di kode dart di dalam folder lib

INITINYA :
- kalo code internal (tidak perlu di ekspos ke luar) simpan di src 
- kalo code external (perlu di ekspos ke luar) simpan di lib 

contoh di file :
LIBRARY\pzn_belajar_dart_library\lib\src\pzn_belajar_dart_library_base.dart

## PUBSPEC

- saat kita membuat dart packages, hal yang paling utama adalah file pubspec.yaml
- pubspec.yaml merupakan konfigurasi dari dart packages
- di dalam pubspec, kita perlu tentukan nama dart packages yang kita buat, termasuk dependency yang kita butuhkan di dart package tersebut

contoh di file :
pubspec.yaml
LIBRARY\pzn_belajar_dart_library\pubspec.yaml