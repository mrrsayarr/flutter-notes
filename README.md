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

'''
import 'package:flutter/material.dart';

main () {
  runApp(
    MaterialApp(
      home: Material(
        color: Colors.grey, // Arka Plan Rengi Gri
        child: Text("Merhaba Flutter", // Köşede yazması gereken yazı
          textAlign: TextAlign.center, // YAZIYI yatayda ortaya alır
          // center yerine "end" yazılırsa yazı sonda kalır
          textDirection: TextDirection.ltr,
          style: TextStyle(color: Colors.purple, fontSize: 20 // Mor text ve 20 font boyutu
            ,fontWeight: FontWeight.bold // Kalın yazı
            ,fontStyle: FontStyle.italic // İtalik yazı Stili
            ,letterSpacing: 3 // Harfler arasında boşluk bırakır
            ,wordSpacing: 20 // Kelimeler arasında boşluk bırakır
            ,decoration: TextDecoration.underline // Altına çizer
            , background: Paint()..color=Colors.green // Yazı arka planı yeşil olur
            , height: 3 ), // Yazının yüksekliğini belirtir
        ),
      ),
    )
  );
}
'''