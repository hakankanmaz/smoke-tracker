# Smoke Tracker · IQOS / Sigara Sayacı

IQOS ya da sigarayı azaltıp bırakma yolculuğu için kişisel takip uygulaması. Her çubuğu tek dokunuşla kaydet, nikotin desteğini, alkolü ve günlük ruh halini yanına ekle, verinle neyin işe yaradığını gör.

## Özellikler

- **Tek dokunuşla kayıt:** "+ IQOS içtim" (ya da "+ Sigara içtim") butonu. Yanlışlıkla bastıysan 5 saniye içinde "Geri al".
- **Bugünün sayısı** ve **son kayıttan beri geçen süre** canlı olarak.
- **Günlük hedef:** Hedefe yaklaşınca sarı, aşınca kırmızı olur.
- **İstatistikler:** Dün, son 7 günün ortalaması, son 14 günün en düşük günü.
- **Son 14 gün grafiği** ve hedef çizgisi.
- **Ortalama ara:** Sigaralar arası ortalama süre, uyanık olduğun saatlere göre hesaplanır. Kalkış ve yatış saatini ayarlardan değiştirebilirsin, varsayılan 06:30–00:00.
- **Saatlere göre dağılım:** Bugün, dün ve son 7 gün için hangi saatlerde içtiğini gösterir. En yoğun saati ve uyku saatlerini işaretler.
- **Tetikleyiciler:** Her kayıttan sonra neden içtiğini listeden seçersin, birden fazla seçebilirsin. Liste ayarlardan düzenlenir, istediğin tetikleyiciyi ekleyip silebilirsin. "Tetikleyiciler" kartı son 7 günde hangi durumların seni sigaraya ittiğini gösterir. Bir kayda dokunarak etiketini sonradan değiştirebilirsin.
- **Canım çekti, içmedim:** Direndiğin her isteği kaydeder ve tetikleyicisini sorar. Bugün kaç isteğe direndiğin üstte görünür.
- **Hedef ara geri sayımı:** İki sigara arası en az kaç dakika olacağını ayarlarsın. Uygulama bir sonraki sigara için en erken saati ve kalan süreyi gösterir. Erken içilen sigaraların arası listede kırmızı görünür. Sayaçlar ve aralar sadece uyanık olduğun saatleri sayar, uyku saatleri dahil edilmez.
- **Paket süresi:** Son 7 günün ortalamasına göre 1 paketin kaç gün gittiğini ve ayda kaç paket içtiğini gösterir. Paketteki sigara sayısı ayarlardan değişir, varsayılan 20.
- **Günü düzenle:** Son 14 gün grafiğinde bir güne dokunup o günün sayısını değiştirebilirsin. Sigaralar kalkış ve yatış saatin arasına eşit dağıtılır. Aynı saate toplu girilmiş bir günü düzeltmek için sayıyı değiştirmeden kaydetmen yeter.
- **Analiz ekranı:** 7, 14 veya 30 günlük dönem için veri paneli.
  - Trend: günlük sayı, 7 günlük ortalama ve %95 güven aralığıyla eğim. Eğim belirginse doğrusal bir tahmin de gösterir.
  - Sigaralar arası süre: histogram, p10/p50/p90 ve haftalık seri. Sadece uyanık süre sayılır.
  - Gün × saat ısı haritası, hafta içi ve hafta sonu karşılaştırması.
  - Tetikleyici profili: sayı, pay, öncesindeki medyan ara ve en sık saat.
  - Rutin metrikleri: günlük sayı, ilk sigara saati, ilk 2 saatteki sigara, 21:00 sonrası, otomatik sigara payı ve medyan ara. Önceki dönemle farkı da gösterir.
  - Saatleri tahmini olan günler (~) saat bazlı metriklere katılmaz.
- **Deneyler:** Bir hipotez, metrik, başlangıç günü ve süre tanımlarsın. Uygulama deney dönemini önceki aynı uzunluktaki dönemle karşılaştırır ve Welch t-testiyle farkın anlamlı olup olmadığını söyler. Çalışan deney "Bugün" ekranında görünür.
- **CSV dışa aktarma:** Her kayıt tarih, saat, tür ve tetikleyicilerle iner. Türler: iqos (ya da sigara), direnildi, nrt_*, alkol ve checkin. İçkilerde tür ve birim, günlük kontrolde puanlar ve not ayrı sütunlardadır. Sheets veya Grafana'da kullanılabilir.
- **Geçmiş günler:** "Kayıtlar" kartında ‹ › ile önceki günlere gidip kayıtları silebilir veya etiketleyebilirsin.
- **Çift dokunma koruması:** 1 dakikadan kısa arayla ikinci kayıt eklenirken onay ister.
- **Ürün ayarı:** IQOS ya da sigara seçilir, varsayılan IQOS. Butonlar ve metinler buna göre değişir ("+ IQOS içtim", çubuk, paket). Eski kayıtlar olduğu gibi kalır.
- **Nikotin desteği:** Bant takma ve çıkarma, sakız, pastil ve sprey tek dokunuşla kaydedilir. Bant ne zamandan beri takılı, bugün kaç sakız gibi bilgiler "Bugün" ekranında görünür. Analizde bantlı ve bantsız günlerdeki çubuk sayısı karşılaştırılır.
- **Alkol:** Bira, şarap ve diğer içkiler hızlıca eklenir, geri alınabilir. Birim standart içkidir (10 g alkol), tür başına ayarlanabilir. Haftalık kartta içilen ve alkolsüz akşamlar ile haftalık alkolsüz akşam hedefi (varsayılan 3) görünür. Gece yarısından sonraki içkiler önceki akşama sayılır. İçkiden sonraki 4 saat içinde kaydedilen çubukta "Alkol" tetikleyicisi önceden seçili gelir.
- **Bırakılanlar:** Bıraktığın her şey için temiz gün sayacı ve sıradaki eşik (1 hafta, 2 hafta, 1 ay, 3 ay, 6 ay, 1 yıl). Ot / 7 Ekim 2026 ile hazır gelir, ayarlardan düzenlenir ve yenisi eklenir.
- **Günlük kontrol:** Akşam 30 saniyede ruh hali, sinirlilik, uyku ve enerji (1–5), öksürük (yok/az/çok) ve isteğe bağlı not. 20:00'den sonra yapılmamışsa "Bugün" ekranında hatırlatma çıkar. Analizde dönem ortalamaları ve gün gün çizgileri görünür.
- **Azaltma planı:** Başlangıç hedefi, adım, kaç günde bir azalacağı ve taban girilir. Günlük hedef her gün plana göre kendiliğinden ayarlanır, "Plan: bugün X, Y gün sonra Z" satırı görünür. Bugünkü hedef elle değiştirilirse sadece o gün için geçerli olur.
- **İlişkiler:** Analiz ekranında, seçili döneme göre: içilen ve alkolsüz günlerde çubuk sayısı, içkili akşamın ertesi uyku, çok ve az içilen günlerde sinirlilik, bantlı ve bantsız günlerde sinirlilik. Gün sayısı, ortalamalar ve Welch t-testi sonucu gösterilir, az veriyle kesin konuşulmaz.
- **Para:** Paket fiyatı ve önceki tüketim (varsayılan günde 20) girilince takibe başladığından bu yana ve bu hafta ne kadar tasarruf ettiğin görünür. İçki fiyatlarıyla haftalık alkol harcaması da hesaplanır.
- **Deney metrikleri:** Deneylerde günlük içki, alkolsüz gün payı, nikotin sakızı, sinirlilik ve uyku puanı da ölçülebilir.
- **Unutulan kayıt:** Geçmiş bir saat için kayıt ekleyebilirsin. Yanlış kaydı listeden silebilirsin.
- **Yedekleme:** Bütün veriler ve ayarlar JSON olarak indirilir ve geri yüklenir. Eski sürümlerin yedekleri de sorunsuz yüklenir.
- **Çevrimdışı çalışır**, telefon ana ekranına uygulama gibi eklenir.

Veriler sadece telefonunda, tarayıcının yerel deposunda tutulur. Hiçbir sunucuya gönderilmez.

## Yayınlama (GitHub Pages)

1. GitHub'da repo → **Settings → Pages**.
2. **Source:** "Deploy from a branch", **Branch:** `gh-pages`, klasör `/ (root)` → **Save**. Yeni sürüm yayınlamak için `main`'i `gh-pages` branch'ine push'la.
3. Bir dakika sonra uygulama şu adreste açılır: `https://hakankanmaz.github.io/smoke-tracker/`

## Telefona kurulum

- **iPhone (Safari):** Adresi aç → Paylaş butonu → **Ana Ekrana Ekle**.
- **Android (Chrome):** Adresi aç → ⋮ menü → **Ana ekrana ekle / Uygulamayı yükle**.

Ana ekrandan açtığında tam ekran, normal bir uygulama gibi çalışır.

## Geliştirme

Derleme adımı yok. Yerelde denemek için:

```sh
python3 -m http.server 8000
# http://localhost:8000
```

Uygulama dosyalarını değiştirdiğinde `sw.js` içindeki `VERSION` değerini artır ki telefondaki önbellek yenilensin.
