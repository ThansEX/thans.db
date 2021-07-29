## Nedir bu Thans.db ?
Json tabanlı çalışan bir veritabanıdır, sadeliği ve türkçe komutları ile hızlı ve güvenli çalışmaktadır.

## Nasıl json tanımlarım?
```js
/// Önce Tanımlama yapalım
const veriler = require("thans.db");
const db = new veriler("./thans.json");
```

## Peki nasıl kullanabilirim?
```js
/// Veri değerini sabitlemek (set)

db.ayarla("Verimiz", "Thans"); // Verimiz verisini "Thans" olarak sabiledik.

// Veri değerini çekmek
db.cek("Verimiz"); // Çıktı olarak "Thans" çıktısını alacaksınız.
db.bul("Verimiz"); // Çıktı olarak "Thans" çıktısını alacaksınız.

// Veri silme
db.sil("Verimiz"); // Verimiz verisini sildik.

// Veri kontrolü
db.kontrol("Verimiz"); // Eğer ki veri bulunuyor ise "true" çıktısı alırsınız, eğer ki veri bulunmuyorsa "false" çıktısını alırsınız. 

// Veri ekleme - Veri azaltma
db.ekle("Sayı", 5); // Sayı verimize 5 eklendi

db.eksilt("Sayı", 4); // Sayı verimizden 4 eksiltildi

// Verimize değer ekleme
db.degerekle("Kimlik", { Isim: "Thans", Soyisim: "Darwin"}); // Kimlik verisine isim ve soyisim değerlerini ekledik.

// Jsondaki verileri silme 
db.temizle(); // db ile tanımlı olan Json dosyasını tamamen temizledik.
```
