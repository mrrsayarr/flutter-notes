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




Margin ve Padding özellikleri
```
import 'package:flutter/material.dart';

main() {
  runApp(MaterialApp(
    home: Material(
      color: Colors.grey[350], // Arka Plan Rengi Gri Tonu
      child: Container(
        margin: EdgeInsets.only(left: 40, top: 60), // Sadece üst ve soldan boşluk bırakır
        // EdgeInsets.all(50)
        // istersek sadece bir kenardan da kısıtlayabiliriz
        // margin container ve dış taraf arasında boşluk bırakır
        // padding ise container içini ilgilendirir
        padding: EdgeInsets.all(22.5),
        color: Colors.greenAccent,
        child: Text(
          "Merhaba Flutter",
          textAlign: TextAlign.start,
          style: TextStyle(color: Colors.white, fontSize: 25),
        ),
      ),
    ),
  ));
}

```



Aligment kullanımı ve koordinat sisteminde gösterimi
```
import 'package:flutter/material.dart';

main() {
  runApp(MaterialApp(
    home: Material(
      color: Colors.grey[350], // Arka Plan Rengi Gri Tonu
      child: Container(
        color: Colors.greenAccent,

        // alignment: Alignment.topCenter, // Yukarı ve orataya sabitler
        alignment: Alignment.center,
        // center yerine (0,0) şeylerde yazılabilir
        child: Text(
          "Merhaba Flutter",
          textAlign: TextAlign.start,
          style: TextStyle(color: Colors.white, fontSize: 25,
            background: Paint()..color=Colors.deepOrange // Yazı Arkaplan rengi
             ),
        ),
      ),
    ),
  ));
}

```


Container özelliklerine devam
```
import 'package:flutter/material.dart';

main() {
  runApp(MaterialApp(
    home: Material(
      color: Colors.grey[350], // Arka Plan Rengi Gri Tonu
      child: Center(
        child: Container(
          // width ve height diyerek genişlik ve yüksekliği ile uğraşabiliriz
          // transform: Matrix4.rotationZ(0.8), yazıyı döndürebiliriz container içinde
          child: Text("Flutter", textDirection: TextDirection.ltr,
            style: TextStyle(fontSize: 30, color: Colors.white)),
        ),
      ),
    ),
  ));
}
```


Dizileri tanımlama ve elemanları gösterme
```
import 'package:flutter/material.dart';

main() {
  // Dizi tanımlama
  List list = []; // Hem double hem de string türünden yazılabilir.
  List<String> sehirler = ["İstanbul", "Ankara"]; // Sadece string türünden veriler girilebilir.
  // list.add("İstanbul"); // indeks 0
  // list.add("Ankara"); // indeks 1
  // YA DA aşağıdaki şekilde belirtilebilir
  list.addAll(["İstanbul", "Ankara", "Amasaya"]);

  runApp(MaterialApp(
    home: Material(
      color: Colors.grey[850], // Arka Plan Rengi Gri Tonu
      child: Center(
        child: Container(
          child: Text(list[0], textDirection: TextDirection.ltr,
            style: TextStyle(fontSize: 30, color: Colors.white),

          ),
        ),
      ),
    ),
  ));
}

```


Row Kullanımı
```
import 'package:flutter/material.dart';

main() {
// Merhaba yanında Flutter yazmak istersek Row veya Column kullanmak gerekir
  runApp(MaterialApp(
    home: Material(
      color: Colors.grey[850],
      child: Center(
        child: Container( // Row veya Column'a arkaplan rengi verilmediği için Container oluşturduk
          color: Colors.orange,
          child: Row(
            mainAxisAlignment: MainAxisAlignment.center,
            children: const <Widget>[
              Text(
                "Merhaba ",
                style: TextStyle(fontSize: 25, color: Colors.white),
              ),
              Text(
                "Flutter ",
                style: TextStyle(fontSize: 25, color: Colors.red),
              ),
              Text(
                "Dart",
                style: TextStyle(fontSize: 25, color: Colors.black87),
              ),
            ],
          ),
        ),
      ),
    ),
  ));
}

```



Column Kullanımı
```
import 'package:flutter/material.dart';

main() {
  runApp(MaterialApp(
    home: Material(
      color: Colors.grey[850],
      child: Center(
        child: Container(
            color: Colors.orange,
            child: Column(
              mainAxisAlignment: MainAxisAlignment.center,
              children: <Widget>[
                Text(
                  "Merhaba ",
                  style: TextStyle(fontSize: 25, color: Colors.blue),
                ),
                Text(
                  "Flutter ",
                  style: TextStyle(fontSize: 25, color: Colors.red),
                ),
                Text(
                  "Dart",
                  style: TextStyle(fontSize: 25, color: Colors.black87),
                ),
              ],
            )),
      ),
    ),
  ));
}
```


Column ve Row 
```
import 'package:flutter/material.dart';

main() {
  runApp(MaterialApp(
    home: Material(
      color: Colors.grey[850],
      child: Center(
        child: Container(
            color: Colors.orange,
            child: Row(
              mainAxisAlignment: MainAxisAlignment.center,
              children: <Widget>[
                Container(
                    color: Colors.lightBlueAccent,
                    margin: EdgeInsets.only(top: 20, bottom: 20, right: 20),
                    child: Column(
                      mainAxisAlignment: MainAxisAlignment.center,
                      children: <Widget>[
                        Container(
                          margin: EdgeInsets.only(right: 10,left: 10) ,
                          child: Text(
                            "Widget 1 ",
                            style: TextStyle(fontSize: 25),
                          ),
                        ),
                        Text(
                          "Widget 2 ",
                          style: TextStyle(fontSize: 25),
                        ),
                        Text(
                          "Widget 3 ",
                          style: TextStyle(fontSize: 25),
                        ),
                      ],
                    )),
                Container(
                    color: Colors.lightBlueAccent,
                    margin: EdgeInsets.only(top: 20, bottom: 20,left: 20),
                    child: Column(
                      mainAxisAlignment: MainAxisAlignment.center,
                      children: <Widget>[
                        Container(
                          margin: EdgeInsets.only(right: 10, left: 10) ,
                          child: Text(
                            "Widget 1",
                            style: TextStyle(fontSize: 25),
                          ),
                        ),
                        Text(
                          "Widget 2",
                          style: TextStyle(fontSize: 25),
                        ),
                        Text(
                          "Widget 3",
                          style: TextStyle(fontSize: 25),
                        ),
                      ],
                    ))
              ],
            )),
      ),
    ),
  ));
}
```


Expanded kullanımı
```
import 'package:flutter/material.dart';

main() {
  runApp(MaterialApp(
      home: Material(
        color: Colors.purple,
        child: Container(
          color: Colors.orange,
          child: Row(
            children: <Widget> [
              Text("Merhaba Flutter", style: TextStyle(fontSize: 30),),
              Icon(Icons.camera),
              Expanded( // bazı durumlarda yazı ekrana sığmazsa hata verir
                  // Hata vermemesi için Expanded kullanılır
                  child: Text("Merhaba Flutter", style: TextStyle(fontSize: 30),),
              )
            ],
          ),
    ),
  )));
}
```


```
s


```
```
s


```
```
s

```
```

s

```
```

s

```
```

s

```
```

s

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