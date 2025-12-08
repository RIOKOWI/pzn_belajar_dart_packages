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

## MEMBUAT LIBRARY

- saat membuat kode dart di dart packages, disarankan lakukan di dalam folder src
- dan ketika melakukan import kode dart dari library, jangan import dari folder src, hal ini karena kode di src biasanya digunakan sebagai internal library, dan tidak dijamin akan backward compatible ketika terjadi update library

EXPORT LIBRARY
- setelah membuat kode dart di dalam folder src, kita bisa buat kode dart di lib yang digunakan untuk mengekspos bagian mana yang ingin kita ekspos
- kita bisa menggunakan kata kunci export jika ingin mengekspos semua kode di dalam file dart, atau gunakan export show jika hanya beberapa saj
- jangan lupa untuk menambahkan kata kunci library dan diikuti dengan nama library yang kita buat, walaupun tidak wajib, tapi direkomendasikan menggunakan nya, karena secara default jika kita tidak menambahkan library, secara otomatis nama library nya adalah string kosong.

IMPORT LIBRARY
- setelah membuat library jika kita ingin menggunakannya, kita bisa mencobanya di folder example
- kita bisa melakukan import dengan pola:
package:nama_library/file.dart

contoh di file :
LIBRARY\pzn_belajar_dart_library\lib\src\say_hello.dart
LIBRARY\pzn_belajar_dart_library\lib\src\customer.dart
LIBRARY\pzn_belajar_dart_library\lib\hello.dart
LIBRARY\pzn_belajar_dart_library\example\hello.dart

## UPGRADE PACKAGES
- melakukan upgrade library adalah hal yang sudah biasa
- hal yang perlu kita lakukan ketika upgrade library adalah, menaikkan versi dari packages di file
pubspec.yaml
- jika menggunakan Git, disarankan untuk menambah tag baru untuk versi baru

contoh di file :
lib\src\say_hello.dart