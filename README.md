# YMI 484 — Alıştırma 1: Animatif Web Deneyimi

Hoş geldin. Bu alıştırmada **sıfır kod yazacaksın.**

Sonunda: gerçek bir web sayfası üretmiş, onu GitHub'a göndermiş olacaksın. Bunu bir yapay zeka ajanıyla konuşarak yapacaksın.

---

## Bu Repoda Ne Var?

```
ymi484repo/
├── README.md                  ← şu an okuduğun dosya
├── skills/
│   ├── web-deneyimi.md        ← hazır skill dosyası — ajanın okuyacağı talimatlar
│   └── benim-skilim.md        ← boş iskelet — skill dosyası nasıl yazılır görmek için
└── ornek/
    └── index.html             ← örnek bir çıktı (ilham için bak)
```

Alıştırmanın sonunda klasörüne şu dosyalar eklenmiş olacak:

```
├── index.html                 ← senin ürettiğin web sayfası
└── REFLECTION.md              ← kısa bir değerlendirme
```

---

## Skill Dosyası Nedir?

`skills/web-deneyimi.md` dosyasını aç ve oku.

Bu dosya bir **skill dosyasıdır** — yapay zeka ajanına ne yapacağını, nasıl davranacağını, neyi üretmesi gerektiğini anlatan yapılandırılmış bir talimat belgesi. Ajan bu dosyayı okuyarak ne yapması gerektiğini anlıyor.

Skill dosyaları sayesinde aynı kalitede sonucu her seferinde, herkese tekrar edebilirsin.

`skills/benim-skilim.md` dosyasına da bak — bu boş bir iskelet. Bir skill dosyasının hangi bölümlerden oluştuğunu görmek için oraya bakabilirsin. Bu alıştırmada onu doldurmak zorunda değilsin.

---

## Başlamadan Önce

### 1. Bu repoyu bilgisayarına indir

Terminali aç. Masaüstüne gitmek için:

```
cd Desktop
```

Repoyu indir:

```
git clone https://github.com/No-Future16/ymi484repo.git
```

Klasörün içine gir:

```
cd ymi484repo
```

> **Terminal nerede?**
> Mac: Spotlight'ta (⌘ + Space) "Terminal" yaz.
> Windows: Başlat menüsünde "Git Bash" yaz.

> **Git kurulu değilse:** [git-scm.com](https://git-scm.com) adresinden indir.

### 2. Klasörü Antigravity'de aç

Antigravity masaüstünde açık olmalı. Klasörü aç:

- Antigravity'de **File → Open Folder** (ya da **Klasör Aç**) seçeneğine tıkla
- Az önce indirdiğin `ymi484repo` klasörünü seç

Klasör Antigravity'de açıldığında, sol panelde `skills/`, `ornek/` ve diğer dosyaları göreceksin.

---

## Adım 1: Örnek Çıktıya Bak

Sol panelde `ornek/index.html` dosyasına çift tıkla. Dosya Gezgini'nden veya Finder'dan bulup tarayıcıda da açabilirsin.

Bu, skill dosyası kullanılarak üretilmiş bir örnek. Seninkinin böyle görünmesi gerekmiyor — bu sadece "ne tür bir çıktı çıkabileceğini" görmek için.

---

## Adım 2: Ajanla Konuş

Antigravity'de sohbet alanını aç. Ajana Türkçe yazacaksın.

İlk mesajın şu kalıptan birini takip etmeli:

---

**Kalıp A — Sadece fikri söyle:**
> `skills/web-deneyimi.md dosyasını oku. Ben [fikrin] için bir web sayfası yapmak istiyorum.`

Örnek:
> `skills/web-deneyimi.md dosyasını oku. Ben bir kafe için web sayfası yapmak istiyorum, sıcak ve samimi bir his vermeli.`

---

**Kalıp B — Daha serbest:**
> `skills/web-deneyimi.md dosyasını oku ve bana ne sormak istediğini sor.`

Ajan sana birkaç soru soracak. Cevapla, ardından üretmeye başlayacak.

---

Ajan çalışırken sol panelde `index.html` dosyasının oluştuğunu göreceksin.

---

## Adım 3: Çıktını İncele

`index.html` dosyasını tarayıcıda aç:

- Sol panelde `index.html` dosyasına sağ tıkla → **Reveal in Finder / Explorer**
- Açılan klasörde dosyaya çift tıkla

Sayfa tarayıcıda açılacak. İncele.

---

## Adım 4: Refine Et

Bir şeyleri değiştirmek istiyorsan ajana Türkçe söyle:

> `Renkleri daha koyu yap.`

> `Başlık yazı tipi çok ince kalıyor, daha kalın olsun.`

> `Animasyonlar çok hızlı, yavaşlat.`

> `İçeriği biraz değiştir — kafe adı "Demir" olsun.`

Ajan `index.html` dosyasını güncelleyecek. Tarayıcıyı yenile, değişimleri gör. İstediğin kadar tekrarla.

---

## Adım 5: REFLECTION.md Dosyasını Oluştur

`ymi484repo` klasöründe yeni bir dosya oluştur, adı `REFLECTION.md` olsun. İçine şunu yaz:

```
# Değerlendirme

## Ne yapmak istedin?


## Ajana ne söyledin, ne aldın? Sürpriz olan bir şey var mıydı?


## Kaç kez "bunu değiştir" dedin ve neden?


## Skill dosyası işe yaradı mı? Değiştirmek istediğin bir şey var mıydı?

```

Uzun yazmak zorunda değilsin. Birkaç cümle yeterli.

---

## Adım 6: Kendi GitHub Repo'na Gönder

### Önce GitHub'da yeni bir repo oluştur

1. [github.com](https://github.com) adresine git, giriş yap
2. Sağ üstteki **+** → **New repository**
3. İsim: `ymi484-odev1`
4. **Public** seçili olsun
5. **Create repository**

### Terminalde sırasıyla çalıştır

`ymi484repo` klasöründeyken:

```
git add .
```

```
git commit -m "Alıştırma 1 teslim"
```

```
git remote set-url origin https://github.com/[KULLANICI_ADIN]/ymi484-odev1.git
```

> Köşeli parantezi kendi GitHub kullanıcı adınla değiştir.

```
git push -u origin main
```

### Kontrol et

`https://github.com/[KULLANICI_ADIN]/ymi484-odev1` adresine git.

`index.html` ve `REFLECTION.md` dosyaları orada görünüyorsa teslim tamamdır. ✓

---

## Teslim Edilecekler

| Dosya | Ne? |
|---|---|
| `index.html` | Ürettiğin web sayfası |
| `REFLECTION.md` | Kısa değerlendirme |

---

## Takıldığında

1. Hata mesajını oku
2. Hata mesajını ajana yapıştır: `Bu hatayı aldım, ne yapmalıyım?`
3. Hâlâ çözülmediyse sor

---

*YMI 484 — Üretken Yapay Zeka ve Arayüz Tasarımı*
