# ?? Barkod Okuyucu PWA

Market ürünlerinin **barkodunu** telefon kamerasýyla okutup,
iki farklý modda fiyat kontrolü yapan PWA.

## Modlar
- ?? **Tekli Sorgu:** Bir barkod okut › ürün adý, marka, kategori, fiyat, stok.
- ??? **Sepet Modu:** Birden fazla ürün okut › çalýþan toplam. Kasada sürpriz yok.

## Kullanýlan Web API'leri
- **`getUserMedia`** — arka kamera eriþimi
- **`BarcodeDetector`** — EAN-13/8, UPC-A/E, Code-128/39, ITF tarama
- **Web Audio API** — baþarýlý/hatalý okuma bip sesi
- **Vibration API** — dokunsal geri bildirim (Android)
- **localStorage** — sepeti sayfa yenilemelerde koruma
- **Service Worker** — uygulama kabuðu önbelleði + offline destek

## `products.json` Yapýsý
```json
{
  "8690504009626": {
    "name": "Tam Yaðlý Süt 1 L",
    "brand": "Sütaþ",
    "category": "Süt & Kahvaltýlýk",
    "price": 42.50,
    "unit": "1 L",
    "stock": 24
  }
}