# Smoke Tracker · Sigara Sayacı

Sigarayı bırakma yolculuğu için tek dokunuşluk sayaç. İçtiğin her sigarayı kaydet, günde kaç tane içtiğini gör, hedefini yavaş yavaş düşür.

## Özellikler

- **Tek dokunuşla kayıt:** "+ Sigara içtim" butonu. Yanlışlıkla bastıysan 5 saniye içinde "Geri al".
- **Bugünün sayısı** ve **son sigaradan beri geçen süre** canlı olarak.
- **Günlük hedef:** Hedefe yaklaşınca sarı, aşınca kırmızı olur.
- **İstatistikler:** Dün, son 7 günün ortalaması, son 14 günün en düşük günü.
- **Son 14 gün grafiği** ve hedef çizgisi.
- **Unutulan kayıt:** Geçmiş bir saat için kayıt ekleyebilirsin. Yanlış kaydı listeden silebilirsin.
- **Yedekleme:** Verileri JSON olarak indir ve geri yükle.
- **Çevrimdışı çalışır**, telefon ana ekranına uygulama gibi eklenir.

Veriler sadece telefonunda, tarayıcının yerel deposunda tutulur. Hiçbir sunucuya gönderilmez.

## Yayınlama (GitHub Pages)

1. GitHub'da repo → **Settings → Pages**.
2. **Source:** "Deploy from a branch", **Branch:** `main`, klasör `/ (root)` → **Save**.
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
