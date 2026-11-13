# Eskiz Defteri

Tablet için eskiz defteri. Kalemler, suluboya, pastel, aydınger katmanları ve yapay zekâ ile render içerir. Chrome'da "Ana ekrana ekle" ile uygulama gibi kurulur, internet olmadan da açılır.

Adres (Pages açıldıktan sonra): **https://mfbarsiv.github.io/eskiz-defteri/**

## GitHub'a yükleme

1. GitHub'da **New repository** ile `eskiz-defteri` adında, **Public** bir depo aç.
2. Depoda **Add file → Upload files** de. Zip'in içindeki her şeyi sürükle:
   - `index.html`
   - `manifest.webmanifest`
   - `sw.js`
   - `README.md`
   - `icons` klasörü
   Klasör yapısı aynen kalmalı. **Commit changes**'e bas.
3. **Settings → Pages** bölümüne git:
   - Source: **Deploy from a branch**
   - Branch: **main**
   - Klasör: **/ (root)**
   Sonra **Save**.
4. 1–2 dakika içinde adres çalışır.

## Tablete kurma

1. Tablette **Chrome** ile adresi aç.
2. Sağ üstteki **⋮** menüsünden **Ana ekrana ekle** (ya da **Uygulamayı yükle**) de.
3. Ana ekrandaki **Eskiz Defteri** simgesinden aç. Tam ekran açılır.

## Render için

1. Render sekmesinde **Ayarlar**'a gir.
2. Gemini ya da OpenAI anahtarını gir. Anahtar yalnız bu tablette, bu uygulamanın içinde saklanır.
3. Render için internet gerekir. Çizim internetsiz de çalışır.

## Çizimler nerede duruyor

- Çizimler tablette, uygulamanın kendi deposunda kendiliğinden kaydedilir.
- Tüm sayfalar **Defter**'de durur: sol üstteki *Eskiz Defteri* yazısına dokun.
- **Kaydet** düğmesi açık sayfayı PNG ya da JPG olarak İndirilenler'e kaydeder. **Paylaş** ile Drive'a, Fotoğraflar'a ya da WhatsApp'a gönderebilirsin.
- **Yedek al** (Defter'de) bütün sayfaları, katmanları ve renderları tek bir `.json` dosyasına koyar. Bu dosyayı ara ara Drive'a at.
  - Chrome verisini silersen ya da tablet değişirse, **Yedekten yükle** ile hepsi geri gelir.

## Yeni (v2)

- **Görsel ekle** (üstte, resim + artı simgesi): ekran görüntüsünü ya da resmi seç. Sürükleyerek taşı, iki parmakla büyüt/döndür, **Tamam** de. Görsel sayfanın en altına ayrı katman olarak girer; üstüne çizersin. Panel'den gizleyebilir ya da silebilirsin.
- **Düz çizgi**: kalemi bir noktadan diğerine çek, bir an bekle; çizgi düzleşir ama eskiz hissini korur. Alttaki **Düz** düğmesi bekleme olmadan çizgi çeker. Yanındaki dalga kaydırıcısı **eskiz hissini** ayarlar (0 = cetvel gibi). Ayarlar Panel → Düz çizgi'de.
- **Kâğıt boyutu**: Panel → Kâğıt boyutu (A4, A3, A2, Kare, Geniş; yatay/dikey). Mevcut sayfayı büyütürsen çizimin ortada kalır. Yeni sayfa açarken de boyut sorulur.

## Güncelleme

Yeni bir `index.html` gelince depoda eski dosyanın üstüne yükle. Uygulama, internet varken bir sonraki açılışta yeni sürümü alır. Gerekirse uygulamayı bir kez kapatıp aç.

Yalnız `index.html` değişti ama tablet hâlâ eskisini gösteriyorsa, `sw.js` içindeki `eskiz-defteri-v1` adını `v2` yap ve onu da yükle.
