# Flutter Konu Anlatımları
Materyal Kullanımı için basit bir kod.
'''
import 'package:flutter/material.dart'; // Materyal

main() { // Fonksiyon
  runApp( // Çalıştırma Fonksiyonu
    MaterialApp(
      title: "Flutter", // Uygulama başlığı
      home: Material( // Home diyerek Ana Sayfa Belirlenir
        color: Colors.grey,
        child: Text("Merhaba Flutter", textDirection: TextDirection.ltr,),
      ),
    )
  );
}
'''

Text Direction Kullanımı 
'''
import 'package:flutter/material.dart';

main () {
  runApp(
    MaterialApp(
      home: Material(
        color: Colors.grey, // Arka Plan Rengi Gri
        child: Text("Merhaba Flutter", // Köşede yazması gereken yazı
          textDirection: TextDirection.ltr,
          style: TextStyle(color: Colors.purple, fontSize: 20), // Mor text
        ),
      ),
    )
  );
}
'''