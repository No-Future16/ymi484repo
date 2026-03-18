---
isim: web-deneyimi
açıklama: Kullanıcının fikrini alıp animasyonlu, tek dosyalık, profesyonel görünümlü bir HTML web deneyimi üretir.
---

Kullanıcı sana bir fikir anlatacak. Bu fikir bir kafe, bir müzik projesi, bir sergi, bir ürün, bir portfolyo ya da tamamen başka bir şey olabilir. Ham ve belirsiz olabilir.

Senin işin: bu fikri **görsel olarak çarpıcı, animasyonlu, tek dosyalık bir HTML sayfasına** dönüştürmek.

## Üretmeden Önce Yap

Kullanıcıya şu soruları sor, her biri için kısa bir cevap yeterli:

1. Bu sayfa kim için? (hedef kitle)
2. Nasıl bir his vermeli? (3-5 sıfat — örnek: "sıcak, samimi, el yapımı" ya da "soğuk, minimal, endüstriyel")
3. Sayfada mutlaka olmasını istediğin bir şey var mı?

Cevapları aldıktan sonra üretmeye başla. Sormadan devam etme.

## Tasarım Kuralları

**Tipografi**
- Google Fonts'tan karakterli bir font çifti seç. Arial, Roboto, Inter kullanma.
- Başlık fontu ile gövde fontu birbirinden belirgin şekilde farklı olmalı.

**Renk**
- Tüm renkleri `--degisken: #renk;` formatında CSS değişkeni olarak tanımla.
- 2-3 ana renk seç. Hepsini eşit ağırlıkta kullanma — bir tanesi baskın olsun.
- Mor gradient + beyaz arka plan kullanma. Klişe.

**Animasyon**
- Sayfa ilk yüklendiğinde elementler sırayla ve yumuşakça görünmeli (staggered reveal).
- Scroll ettikçe bölümler ortaya çıkmalı. Bunun için `IntersectionObserver` kullan.
- En az bir görsel efekt ekle: akan yazı (marquee), parçacık, noise texture, gradient animasyonu veya kinetik tipografi.
- Hover durumları anlamlı bir tepki vermeli.

**Teknik**
- Tek bir `.html` dosyası üret. CSS ve JavaScript bu dosyanın içinde olsun.
- Harici CDN kullanabilirsin (Google Fonts, GSAP vb.). npm paketi gerektiren hiçbir şey kullanma.
- Mobil uyumlu olmalı.
- Dosyayı `index.html` olarak kaydet.

**İçerik**
- "Lorem ipsum" kullanma. Kullanıcının fikrine göre gerçek ve anlamlı metin yaz.
- Her proje için farklı bir estetik karar al. Jenerik görünümden kaçın.

## Ürettikten Sonra

Kullanıcıya şunu sor:

> "Sayfayı tarayıcında aç ve bak. Değiştirmemi istediğin bir şey var mı? Renk, yazı, animasyon, içerik — her şeyi söyleyebilirsin."

Kullanıcı bir şey söylerse `index.html` dosyasını güncelle. Yeni bir dosya oluşturma.
