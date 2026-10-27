# Mesafeci

[mesafeci.com](https://mesafeci.com), Türkiye'de iki yer arasındaki karayolu mesafesini, yaklaşık yol süresini ve yolculuğun toplam maliyetini hesaplayan ücretsiz bir sitedir.

## Neler var?

- **İller ve ilçeler arası mesafe:** Güzergâh, tahmini süre ve yol üzerindeki iller.
- **Yol masrafı:** Benzin, motorin, LPG veya elektrikli araç için yakıt ya da şarj tutarı, otoyol ve köprü geçişleri dahil.
- **Kişi başı maliyet:** Masrafı yolcu sayısına bölerek gösterir.
- **Pompa fiyatları:** İl ve ilçe bazında, her gün güncellenen akaryakıt fiyatları.
- **Gişeler:** Otoyol ve köprü geçiş ücretleri.

## Veriler

- Mesafeler açık harita verisinden (ODbL) hesaplanır.
- Akaryakıt fiyatları her gün, otoyol ve köprü ücretleri resmî tarifeler değiştikçe güncellenir.
- Tutarlar kuruşuna kadar gösterilir, yuvarlanmaz.

## Hesaplama nasıl yapılıyor?

**Mesafe:** Kuş uçuşu değil, gerçek karayolu ağı üzerinden ölçülür. İl ya da ilçe seçildiğinde başlangıç noktası o yerin merkezidir; bu yüzden kendi adresinizden ölçülen mesafeyle arada birkaç kilometre fark olabilir.

**Süre:** Trafiksiz sürüş süresidir. Anlık trafik, yol çalışması ve molalar dahil değildir.

**Yakıt:**

    yakıt tutarı = mesafe (km) × tüketim (L/100 km) ÷ 100 × litre fiyatı

Litre fiyatı, yola çıkılan ilçenin pompa fiyatıdır. Elektrikli araçta litre yerine kWh/100 km tüketim ve TL/kWh şarj ücreti kullanılır.

**Otoyol ve köprü:** KGM tarifesinden, otomobil (1. sınıf) için ve KDV dahil eklenir. Bir güzergâhtaki gişelerin hepsinin tarifesi bilinmiyorsa bilinen tutarlar toplanıp "en az" olarak gösterilir; hiçbiri bilinmiyorsa "?" yazılır. Tahmini rakam eklenmez.

**Örnek (27 Ekim 2026):** İstanbul–Ankara tek yön 442,3 km. Benzinli orta sınıf otomobil (6,0 L/100 km) ve İstanbul pompa fiyatı 76,30 TL/L ile yakıt 2.024,85 TL; otoyol ve köprü 1.274,00 TL.

Otopark, yemek ve mola masrafları hesaba dahil değildir.

## Ne sıklıkla güncelleniyor?

| Veri | Güncelleme |
|---|---|
| Akaryakıt pompa fiyatları | Her gece |
| Elektrik tarifesi ve şarj ücretleri | Ayda iki kez |
| Otoyol ve köprü ücretleri | Tarife değiştiğinde |

## Sık sorulanlar

**Süre neden navigasyondan kısa?** Gösterilen süre trafiksiz ve molasız sürüşü varsayar. Uzun yolda yaklaşık iki saatte bir mola vermek gerekir.

**Hibrit araçta hangi tüketimi yazmalıyım?** Hibritlerde tüketim şehir içiyle otoyolda çok değişir. En doğru sonuç için aracınızın yol bilgisayarındaki ortalamayı yazın.

**Fiyatlar istasyondan neden birkaç kuruş farklı?** Aynı ilçedeki istasyonlar arasında küçük fiyat farkları olabilir. Sitede ilçe listesindeki fiyat kullanılır.

## İletişim

Öneri ve hata bildirimleri için [mesafeci.com](https://mesafeci.com) adresindeki İletişim sayfasını kullanabilirsiniz.
