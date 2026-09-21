# Görsel ekleme rehberi

Ürün görselleri `public/img/urunler/<urun-slug>/` klasöründe durur.

## Adlandırma

```
public/img/urunler/nisan-yelpazesi/nisan-yelpazesi-01.webp   ← kapak
public/img/urunler/nisan-yelpazesi/nisan-yelpazesi-02.webp
public/img/urunler/nisan-yelpazesi/nisan-yelpazesi-02-600.webp  ← küçük sürüm (isteğe bağlı)
```

- Numara **iki haneli** ve `-01`'den başlar. `-01` her zaman kapak görselidir.
- Dosya adında Türkçe karakter, boşluk ve büyük harf kullanmayın.
- Yönetim panelinden yüklerseniz bu adlandırma ve küçük sürüm **otomatik** yapılır.

## Ölçüler

| Kullanım | Uzun kenar | Oran | Biçim |
| --- | --- | --- | --- |
| Ürün görseli | 1600 px | 4:5 (dikey) | WebP, kalite ~0.82 |
| Küçük sürüm (`-600`) | 600 px | 4:5 | WebP |
| Kategori kapağı | 1600 px | 4:5 | WebP |
| Paylaşım görseli (`og-varsayilan`) | 1200 × 630 px | 1.91:1 | JPG/WebP |

Panel yüklediğiniz fotoğrafı tarayıcıda küçültüp WebP'ye çevirir, EXIF dönüşünü
düzeltir ve her iki sürümü de commit eder. Elle ekliyorsanız aynı ölçüleri hedefleyin;
ürünün JSON kaydındaki `genislik` / `yukseklik` değerlerini de gerçek ölçüyle güncelleyin
(bu değerler düzen kaymasını — CLS — önler).

## Yer tutucular

Şu an her üründe markanın renklerinde bir **SVG yer tutucu** var
(`<slug>-01.svg`). Gerçek fotoğrafı aynı klasöre koyup ürünün `gorseller`
listesindeki yolu `.webp` olarak güncellediğinizde yer tutucu kendiliğinden devre
dışı kalır. Panelden görsel yüklerseniz bu güncelleme otomatik olur.

## Depo boyutu

GitHub deposu şişmesin diye 1600 px'ten büyük veya 400 KB'ı aşan dosya yüklemeyin.
Fotoğrafları doğrudan telefondan (3-8 MB) commit etmeyin — panel üzerinden yükleyin.
