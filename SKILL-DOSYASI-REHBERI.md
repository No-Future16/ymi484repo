# Skill Dosyası Nedir?

## Bir Benzetmeyle Başlayalım

Bir restorana girdiğini düşün. Garson sana "Ne istersiniz?" diye soruyor. Sen de "Güzel bir şey getir" diyorsun.

Garson ne getirecek? Belki pizza, belki sushi, belki çorba. Senin kafandaki "güzel" ile garsonun kafandaki "güzel" aynı şey olmayabilir.

Ama eğer eline bir **menü** verirsen — malzemeler, pişirme şekli, sunum kuralları yazılı — garson her seferinde senin beklediğin şeyi getirir.

**Skill dosyası, yapay zeka ajanı için o menüdür.**

---

## Neden Gerekli?

Bir yapay zeka ajanına "Bana bir web sayfası yap" dersen, çalışır ve bir şey üretir. Ama:

- Senin istediğin tarzda olmayabilir
- Her seferinde farklı bir şey çıkar
- Kalite tutarsız olur
- Bazı önemli detayları atlar

Skill dosyası bu sorunları çözer. Ajana **kesin kurallar** verir:

| Skill dosyası olmadan | Skill dosyası ile |
|---|---|
| "Bir web sayfası yap" | "Animasyonlu, tek dosyalık, mobil uyumlu bir HTML sayfası yap" |
| Her seferinde farklı sonuç | Tutarlı ve öngörülebilir sonuç |
| Ajan varsayım yapar | Ajan soru sorar, sonra üretir |
| Kalite kontrolü yok | Tasarım kuralları tanımlı |

### Gerçek Dünya Karşılığı

Skill dosyaları yazılım dünyasında yeni bir kavram değil. Aslında zaten bildiğin pek çok şeye benzer:

- **Yemek tarifi** — malzemeleri, sırayı ve sonucu tanımlar
- **Mimari şartname** — bir binanın nasıl yapılacağını belirler
- **API dokümantasyonu** — bir servisin nasıl kullanılacağını anlatır
- **Tasarım sistemi (design system)** — bir ürünün görsel kurallarını tanımlar

Skill dosyası da bunların yapay zeka versiyonu: **tekrarlanabilir, kaliteli sonuç almak için yazılmış bir talimat belgesi.**

---

## Bir Skill Dosyasının Anatomisi

Her skill dosyası şu bölümlerden oluşur. Bunu bir şablon olarak düşün:

```
┌─────────────────────────────────────────┐
│  1. FRONTMATTER (Kimlik Bilgisi)        │
│     - İsim ve kısa açıklama             │
├─────────────────────────────────────────┤
│  2. ROL TANIMI                          │
│     - Ajan kim? Ne yapacak?             │
├─────────────────────────────────────────┤
│  3. ÜRETMEDEN ÖNCE YAP                  │
│     - Kullanıcıya sorulacak sorular     │
├─────────────────────────────────────────┤
│  4. KURALLAR                            │
│     - Tasarım, teknik, içerik kuralları │
├─────────────────────────────────────────┤
│  5. ÇIKTI FORMATI                       │
│     - Ne üretilecek, hangi dosya adıyla │
├─────────────────────────────────────────┤
│  6. ÜRETTIKTEN SONRA                    │
│     - Geri bildirim döngüsü             │
└─────────────────────────────────────────┘
```

Şimdi her bölümü tek tek inceleyelim.

---

### 1. Frontmatter (Kimlik Bilgisi)

```yaml
---
isim: web-deneyimi
açıklama: Kullanıcının fikrini alıp animasyonlu, tek dosyalık bir HTML web deneyimi üretir.
---
```

Bu bölüm dosyanın en üstünde `---` işaretleri arasında yer alır. Skill dosyasının **kimlik kartıdır**. İki şeyi tanımlar:

- **isim:** Skill'in kısa, teknik adı (boşluk yerine tire kullan)
- **açıklama:** Bir cümleyle ne yaptığını anlatır

Bu bilgi sayesinde ajan (veya onu yöneten sistem) bu dosyanın ne işe yaradığını hızlıca anlar.

---

### 2. Rol Tanımı

```markdown
Kullanıcı sana bir fikir anlatacak. Senin işin: bu fikri görsel olarak çarpıcı,
animasyonlu, tek dosyalık bir HTML sayfasına dönüştürmek.
```

Bu bölüm ajana **kim olduğunu** ve **ne yapması gerektiğini** söyler. Bunu bir iş tanımı gibi düşün. Ne kadar net yazarsan, ajan o kadar doğru davranır.

**İpucu:** "Sen bir X uzmanısın" gibi bir giriş, ajanın ürettiği sonucun kalitesini artırır. Çünkü ajan bu rolü benimseyerek o alandaki bilgisini daha etkin kullanır.

---

### 3. Üretmeden Önce Yap

```markdown
Kullanıcıya şu soruları sor:
1. Bu sayfa kim için?
2. Nasıl bir his vermeli?
3. Sayfada mutlaka olmasını istediğin bir şey var mı?
```

**Bu bölüm kritik.** Olmadan da çalışır ama sonuç kötüleşir. Neden?

Çünkü yapay zeka bilmediği şeyleri **varsayar**. Varsayımlar çoğu zaman yanlış olur. Bu bölüm ajanı "önce sor, sonra üret" mantığına zorlar.

**Analoji:** Bir terziye gidip "Bana bir elbise dik" demek ile "Boy 1.75, bel 82, lacivert kumaş, slim fit" demek arasındaki farkı düşün. İkinci durumda terzi tam istediğini diker.

---

### 4. Kurallar

Bu bölüm skill dosyasının **en uzun ve en önemli** kısmıdır. Ajanın uyması gereken tüm standartları tanımlar.

`web-deneyimi.md` dosyasında kurallar dört kategoriye ayrılmış:

**Tipografi kuralları:**
```markdown
- Google Fonts'tan karakterli bir font çifti seç
- Arial, Roboto, Inter kullanma ← yasak listesi
- Başlık ve gövde fontu belirgin şekilde farklı olmalı
```

**Renk kuralları:**
```markdown
- CSS değişkeni kullan ← teknik standart
- 2-3 ana renk, biri baskın ← tasarım kararı
- Mor gradient + beyaz kullanma ← klişe yasağı
```

**Animasyon kuralları:**
```markdown
- Staggered reveal ← spesifik teknik
- IntersectionObserver kullan ← hangi API'yi kullanacağı
- En az bir görsel efekt ← minimum beklenti
```

**Teknik kurallar:**
```markdown
- Tek .html dosyası ← çıktı formatı
- CDN kullanabilir, npm kullanamaz ← sınırlar
- Mobil uyumlu olmalı ← kalite standardı
```

Kuralların nasıl yazıldığına dikkat et:
- **Yapılacaklar** (Google Fonts kullan) ve **yapılmayacaklar** (Arial kullanma) birlikte tanımlanmış
- **Soyut ifadeler yerine somut talimatlar** var ("güzel olsun" yerine "IntersectionObserver kullan")
- **Minimum beklentiler** belirlenmiş ("en az bir görsel efekt")

---

### 5. Çıktı Formatı

```markdown
- Tek bir .html dosyası üret
- Dosyayı index.html olarak kaydet
```

Ajan ne üreteceğini ve nasıl kaydedeceğini bilmeli. Bu bölüm olmadan ajan:
- Birden fazla dosya oluşturabilir
- Yanlış isimle kaydedebilir
- Farklı bir formatta (örneğin React komponenti) üretebilir

---

### 6. Ürettikten Sonra

```markdown
Kullanıcıya sor:
"Sayfayı tarayıcında aç ve bak. Değiştirmemi istediğin bir şey var mı?"
```

Bu bölüm **geri bildirim döngüsünü** başlatır. Ajan üretip bırakmaz — kullanıcıya sorar ve gerekirse düzeltir. Bu, iteratif tasarım sürecinin yapay zeka ile uygulanmasıdır.

---

## İyi Skill Dosyası Yazmanın Altın Kuralları

1. **Somut ol.** "Güzel bir tasarım yap" yerine "2-3 ana renk kullan, biri baskın olsun" yaz.

2. **Yasakları belirt.** Ne yapılmaması gerektiğini söylemek, ne yapılması gerektiğini söylemek kadar önemli.

3. **Soruları tanımla.** Ajanın varsayım yapmasını engelle — önce sormasını iste.

4. **Minimum beklentiyi koy.** "En az bir animasyon", "en az 3 bölüm" gibi alt sınırlar tanımla.

5. **Geri bildirim döngüsü kur.** Ajanın üretip susmamasını, kullanıcıya dönmesini sağla.

6. **Test et ve geliştir.** İlk seferde mükemmel bir skill dosyası yazamazsın. Kullan, eksikleri gör, güncelle.

---

## Skill Dosyası vs. Tek Seferlik Prompt

"Neden her seferinde uzun bir prompt yazmak yerine skill dosyası kullanıyoruz?" diye sorabilirsin. Fark şu:

| | Tek seferlik prompt | Skill dosyası |
|---|---|---|
| **Tekrarlanabilirlik** | Her seferinde yeniden yazarsın | Bir kez yaz, sürekli kullan |
| **Tutarlılık** | Her seferinde farklı sonuç | Aynı standartlarda çıktı |
| **Paylaşılabilirlik** | Kafanda kalır | Dosya olarak paylaşılır |
| **Geliştirilebilirlik** | Kaybolur gider | Versiyonlanır, iyileştirilir |
| **Karmaşıklık** | Uzun promptlar dağılır | Yapılandırılmış, okunabilir |

Skill dosyası bir **bilgi varlığıdır.** Onu yazarak aslında bir süreç tasarlıyorsun — ve bu süreç tekrar tekrar kullanılabilir.

---

## Pratik: `web-deneyimi.md` Dosyasını İncele

Şimdi `skills/web-deneyimi.md` dosyasını aç ve yukarıdaki bölümleri dosyada bul:

- [ ] Frontmatter var mı? İsim ve açıklama yazılı mı?
- [ ] Rol tanımı var mı? Ajan ne yapacağını anlıyor mu?
- [ ] Sorular tanımlı mı? Kaç soru var?
- [ ] Kurallar kategorilere ayrılmış mı?
- [ ] Çıktı formatı belirlenmiş mi?
- [ ] Geri bildirim döngüsü kurulmuş mu?

Ardından `skills/benim-skilim.md` dosyasına bak — bu boş bir iskelet. Her bölümün yerini gör.

---

## Sonraki Adım

Bu kavramları anladıktan sonra `README.md` dosyasındaki alıştırma adımlarını takip edebilirsin. Alıştırmada:

1. Skill dosyasını ajana okutacaksın
2. Ajanla konuşarak bir web sayfası üreteceksin
3. Sonucu iteratif olarak geliştireceksin
4. Her şeyi GitHub'a göndereceksin

Skill dosyası ajanın **pusula**sıdır. Pusulası olmayan ajan yürür ama nereye gittiğini bilemez.

---

*YMI 484 — Üretken Yapay Zeka ve Arayüz Tasarımı*
