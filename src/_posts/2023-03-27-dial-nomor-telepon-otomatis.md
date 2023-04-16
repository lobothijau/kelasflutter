---
title: Trik Dial Nomor Otomatis di Flutter
subtitle: Bila aplikasi Flutter menampilkan nomor telepon, pastikan user bisa mengakses nomor telepon tersebut dengan lebih mudah.
categories:
- Official Package
author: bagus
image: "/images/posts/old-phone.jpg"
image_hero: "/images/posts/old-phone.jpg"
image_credit:
  url: https://unsplash.com/photos/8gWEAAXJjtI
  label: Quino Al on Unsplash
---

Untuk membuat aplikasi Flutter dapat memanggil aplikasi Dialer dan menuliskan nomor teleponnya secara otomatis, pertama tambahkan *package* `url_launcher` dengan perintah `flutter pub add url_launcher`. 

Sekarang konten *dependencies* di `pubspec.yaml` akan menjadi:

```yaml
dependencies:
  flutter:
    sdk: flutter
  cupertino_icons: ^1.0.2
  url_launcher: ^6.1.10
```

Selanjutnya *import package* tersebut di halaman yang akan dipakai:

```dart
import 'package:url_launcher/url_launcher.dart';
```

Trik dari mengakses *phone call dialer* adalah dengan memanggil method `launchUrl`. Method ini menerima sebuah *object* dengan tipe `Uri` yang di-*parse* dari sebuah string. String yang dipakai mirip seperti penggunaan di web yaitu menggunakan teks, `tel:<nomor_telepon>`.

```dart
GestureDetector(
  onTap: () async {
    Uri phoneno = Uri.parse('tel:+628121462571');
    if (await launchUrl(phoneno)) {
      //dialer berhasil diakses
    } else {
      //dailer gagal diakses
    }
  },
  child: const Text(
    "+6281214632571",
  ),
),
```

<img src="/images/posts/CleanShot%202023-03-27%20at%2021.57.27%402x.png" height="600px"/>