# Flutter Konu Anlatımları
Materyal Kullanımı için basit bir kod.
```
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
```

Text Direction Kullanımı 
```
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
```


Bazı Style çalışmaları, yazı ortalama ...
```
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
```


Yazı ortalama
```
import 'package:flutter/material.dart';

main () {
  runApp(
    MaterialApp(
      home: Material(
        color: Colors.grey, // Arka Plan Rengi Gri
        child: Center(
          child: Text("Flutter yazısı merkezde" // Yazı ORTALANMIS oldu
            , style: TextStyle(color: Colors.white
            , fontSize: 25),),
        ),
      ),
    )
  );
}
```



Değişkenler
```
import 'package:flutter/material.dart';

main () {
  String ad= " Flutter Porgramlama "; // String değişken türü
  int tamsayi = 19; // Tam sayi değişken türü
  int tamsayi2 = 1;

  runApp(
    MaterialApp(
      home: Material(
        color: Colors.grey, // Arka Plan Rengi Gri
        child: Center(
          child: Text(ad + (tamsayi + tamsayi2).toString() // tam sayılar ve string çağrılmış oldu
            // Ayrıca int olan bir ifadeyi stringe dönüştürdük yoksa hata alırız
            // Toplama yapmaz çünkü ikisi de string türünde yapması için
            // iki sayi parantez içinde toplanıp stringe dönüşümü yapılmalıdır
            , style: TextStyle(color: Colors.white
            , fontSize: 25),),
        ),
      ),
    )
  );
}

```



"double" değişkeni, "string" türündeki değişkeni "int" değişkene çevirme
```
import 'dart:convert'; // Otomatik olarak toString() kullanıldığında gelecektir
import 'package:flutter/material.dart';

main () {
  String ad= " Flutter Porgramlama "; // String değişken türü
  int tamsayi = 19; // Tam sayi değişken türü
  double sayi=7.3; // Double sayi değişkeni ondalık türü için kullanılır
  // float değişkeni dart dilinde mevcut değildir

  String no="10";

  runApp(
    MaterialApp(
      home: Material(
        color: Colors.grey, // Arka Plan Rengi Gri
        child: Center( // Merkez konumunda şu an
          child: Text( //(tamsayi + sayi).toString()
            (tamsayi + int.parse(no)).toString() // String bir ifadeyi int türüne dönüştürme
            , style: TextStyle(color: Colors.white, fontSize: 25),),
        ),
      ),
    )
  );
}

```





```
```




```
```



```
```



```
```

```
```




```
```



```
```



```
```