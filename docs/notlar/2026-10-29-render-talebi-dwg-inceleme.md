# 29.10.2026 – Emlakçı müşteri: render talebi ve DWG incelemesi

> Depo herkese açık olduğu için müşteri adı, ada/parsel, mahalle ve mimar
> bilgileri bu nota yazılmadı. Asıl dosyalar müşteride ve yerel bilgisayarda.

## Talep

Emlakçı bir müşteri AutoCAD çizim dosyası (`.dwg`) gönderdi, "görsel
hazırlanacak" notu bıraktı ve görüşmede "render" geçti. Beklenen iş: projeden
satış için fotogerçekçi 3D görseller (dış cephe, kuş bakışı, iç mekân) ve
sosyal medya ve ilan materyali.

## Dosyadan çıkanlar

- AutoCAD 2023 ile kaydedilmiş, 1/50 ölçekli mimari uygulama projesi
  (3. revizyon).
- Aynı mal sahibine ait **yan yana iki parsel**, sahil ve yazlık bölgesi:
  - Parsel 1: **3 blok**, her blok bodrum + 3 kat, 12 daire → 36 daire
  - Parsel 2: **2 blok**, aynı kat düzeni → 24 daire
  - Toplam **5 blok, 60 daire**, ağırlıklı küçük daireler (1+1 tarzı,
    ortalama ~41 m² net)
- Bina tipi: kırma çatı ve kiremit kaplama, mantolama ve boya cephe, geniş
  balkonlar, asansör. İki parseldeki blokların taban alanı aynı, cephe
  düzeni farklı.
- Çizim seti eksiksiz: vaziyet, yerleşim, tüm kat planları, çatı, 2 kesit,
  4 cephe, detaylar, kalıp planı.
- Paftadaki "BUNLARDAN 1 ADET ÇEKİLECEK" notu, aynı setin alternatif
  kopyalarından birinin basılacağı anlamına geliyor.

## DWG'yi açma ve PDF alma (ücretsiz yol)

1. AutoCAD Web (`web.autocad.com`, 30 gün deneme) → Upload → dosyayı aç.
2. `PLOT` komutu → çizim stili `monochrome.ctb`, alan **Kapsam (Extents)**
   veya **Pencere (Window)**, kağıt A3 yatay, kağıda sığdır.
3. Dikkat:
   - Alan olarak "Sınırlar (Limits)" seçilirse sayfa boş çıkabilir.
   - Kapatırken **kaydetme**, müşteri dosyası değişmesin.
   - Deneme bitmeden otomatik yenilemeyi kapat (aylık ücret çekilir).
   - Online "DWG → PDF" sitelerine müşteri dosyası yüklenmez.
4. Tüm proje tek A4'e sığdırılınca kalın çizgiler okunmuyor. Çözüm olarak
   çizgiler inceltilip her pafta ayrı sayfa olacak şekilde yüksek
   çözünürlüklü iki PDF üretildi (parsel başına bir tane).

## Render işi için yol haritası

- **İlk iş için öneri:** 3D model ve render taşerona yaptırılır. Müşteri
  ilişkisi, rötuş, ilan ve sosyal medya paketi ZSDD'de kalır. Bu sırada
  Twinmotion veya D5 Render (ücretsiz sürümler) öğrenilir.
- **Ücretsiz araç seti:** DWG TrueView veya AutoCAD Web → SketchUp (deneme)
  ya da Blender → Twinmotion veya D5 → Photopea.
- **Maliyeti düşüren nokta:** Bloklar tek tip olduğu için bir ana model ve
  bir cephe varyantı yeterli. Taşerondan fiyat alırken belirtilmeli.
- **Önerilen görseller:** 5 bloğun kuş bakışı site görseli, sokak seviyesi
  dış cephe, blok girişi yakın plan, 1+1 salon ve mutfak iç mekânı, renkli
  satış planı.
- **Teklifte:** revizyon sınırı, malzeme ve renk kararlarının yazılı alınması,
  "görseller temsilidir" ibaresi, proje kesinleşmeden başlanmaması.

## Müşteriye sorulacaklar

- Kaç görsel, hangi açılar, iç mekân da var mı?
- Cephe, korkuluk ve doğrama renkleri (çizimde yalnızca "dış cephe boyası"
  yazıyor)
- 5 blok tek site olarak mı, iki ayrı proje olarak mı pazarlanacak?
- Parseller arasında yol var mı? Deniz manzarası ve mesafesi?
- Kullanım yeri (ilan, broşür, branda, sosyal medya), teslim tarihi, bütçe
- Mimardan "son revizyon budur" teyidi ve PDF çıktıları

## Sıradaki adımlar

- [ ] Soru listesini emlakçıya gönder
- [ ] Taşeron için render brief'i hazırla, en az 3 teklif al
- [ ] AutoCAD Web denemesinde otomatik yenilemeyi kapat
- [ ] İş bitince buluttaki (AutoCAD Web, Autodesk Viewer) müşteri dosyalarını sil
