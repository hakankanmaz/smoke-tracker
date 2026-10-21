# Smoke Tracker · Sigara Sayacı

Sigarayı bırakma yolculuğu için tek dokunuşluk sayaç. İçtiğin her sigarayı kaydet, günde kaç tane içtiğini gör, hedefini yavaş yavaş düşür.

## Özellikler

- **Tek dokunuşla kayıt:** "+ Sigara içtim" butonu. Yanlışlıkla bastıysan 5 saniye içinde "Geri al".
- **Bugünün sayısı** ve **son sigaradan beri geçen süre** canlı olarak.
- **Günlük hedef:** Hedefe yaklaşınca sarı, aşınca kırmızı olur.
- **İstatistikler:** Dün, son 7 günün ortalaması, son 14 günün en düşük günü.
- **Son 14 gün grafiği** ve hedef çizgisi.
- **Ortalama ara:** Sigaralar arası ortalama süre, uyanık olduğun saatlere göre hesaplanır. Kalkış ve yatış saatini ayarlardan değiştirebilirsin, varsayılan 06:30–00:00.
- **Saatlere göre dağılım:** Bugün, dün ve son 7 gün için hangi saatlerde içtiğini gösterir. En yoğun saati ve uyku saatlerini işaretler.
- **Tetikleyiciler:** Her kayıttan sonra neden içtiğini listeden seçersin, birden fazla seçebilirsin. Liste ayarlardan düzenlenir, istediğin tetikleyiciyi ekleyip silebilirsin. "Tetikleyiciler" kartı son 7 günde hangi durumların seni sigaraya ittiğini gösterir. Bir kayda dokunarak etiketini sonradan değiştirebilirsin.
- **Canım çekti, içmedim:** Direndiğin her isteği kaydeder ve tetikleyicisini sorar. Bugün kaç isteğe direndiğin üstte görünür.
- **Hedef ara geri sayımı:** İki sigara arası en az kaç dakika olacağını ayarlarsın. Uygulama bir sonraki sigara için en erken saati ve kalan süreyi gösterir. Erken içilen sigaraların arası listede kırmızı görünür.
- **Paket süresi:** Son 7 günün ortalamasına göre 1 paketin kaç gün gittiğini ve ayda kaç paket içtiğini gösterir. Paketteki sigara sayısı ayarlardan değişir, varsayılan 20.
- **Günü düzenle:** Son 14 gün grafiğinde bir güne dokunup o günün sayısını değiştirebilirsin. Sigaralar kalkış ve yatış saatin arasına eşit dağıtılır. Aynı saate toplu girilmiş bir günü düzeltmek için sayıyı değiştirmeden kaydetmen yeter.
- **Unutulan kayıt:** Geçmiş bir saat için kayıt ekleyebilirsin. Yanlış kaydı listeden silebilirsin.
- **Yedekleme:** Verileri JSON olarak indir ve geri yükle.
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
