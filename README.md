# 🇹🇷 Pure CSS Turkish Flag (Türk Bayrağı)

Bu proje, **Türk Bayrağı Kanunu** ve teknik tüzüğüne milimetrik olarak sadık kalınarak, sadece **HTML** ve **CSS** kullanılarak hazırlanmıştır. Görsel herhangi bir resim dosyası (.png, .jpg) içermez; her şey kod ile çizilmiştir.

## 🚀 Proje Hakkında

Bu çalışmanın temel amacı, CSS'in geometrik şekil oluşturma yeteneklerini (CSS Shapes) ve koordinat sistemini (Positioning) pekiştirmektir.

Bayrak ölçüleri, resmi **G (Genişlik)** katsayısına göre hesaplanmıştır:
* **Oran:** 1:1.5
* **Renkler:** CIELAB renk uzayı ve resmi Al rengi.
* **Yıldız:** "CSS Border Hack" yöntemi ile 5 farklı üçgenin birleştirilmesiyle oluşturulmuştur.

## 🛠️ Kullanılan Teknolojiler ve Teknikler

* **HTML5** (Semantik Yapı)
* **CSS3**
    * **Flexbox:** Sayfa ortalama işlemleri için.
    * **Absolute Positioning:** Hilal ve Yıldız'ın tüzüğe uygun koordinatlara yerleştirilmesi için.
    * **CSS Border Triangles:** Yıldızın kollarını oluşturmak için kullanılan "Eski Usul" geometri tekniği.
    * **Transform & Rotate:** Yıldızın açısını Hilal'e tam bakacak şekilde ayarlamak için (-18 deg).
    * **Modern Color Space:** `lab()` renk fonksiyonu kullanımı.

## 📐 Matematiksel Hesaplamalar

Proje, `Height: 500px` (G) baz alınarak hazırlanmıştır:

| Bölüm | Tüzük Oranı | Piksel Karşılığı |
| :--- | :--- | :--- |
| **Genişlik (Boy)** | 1.5 G | 750px |
| **Dış Ay Merkezi** | 0.5 G | 250px |
| **Dış Ay Çapı** | 0.5 G | 250px |
| **İç Ay Çapı** | 0.4 G | 200px |
| **Yıldız Çapı** | 0.25 G | 125px |

## 💻 Koddan Bir Örnek (Yıldız Yapımı)

Yıldız, `clip-path` yerine daha temel bir teknik olan border manipülasyonu ile 5 parçadan oluşturuldu:

```css
.star-point {
    width: 0;
    height: 0;
    border-left: 20px solid transparent;
    border-right: 20px solid transparent;
    border-bottom: 60px solid white;
    transform-origin: 50% 100%;
}
