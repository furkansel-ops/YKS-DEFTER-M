# YKS Defterim — yayına alma ve paylaşma

Bu klasördeki dosyaları GitHub Pages'e koyunca uygulama bir adres üzerinden
çalışır: iPhone dahil her cihazda ana ekrana eklenebilir, çevrimdışı açılır,
`file://` yüzünden yaşanan engeller ortadan kalkar.

## Klasörde ne var

    index.html                 uygulamanın kendisi
    manifest.webmanifest       uygulama adı, simge, renk bilgileri
    sw.js                      çevrimdışı çalışma
    icon-192.png               ana ekran simgeleri
    icon-512.png
    icon-maskable-512.png
    apple-touch-icon.png

Hepsi aynı dizinde durur; alt klasör yoktur. GitHub'a yüklerken
dosyaları topluca seçip sürüklemen yeterli.

## 1) GitHub'a koy (bir kez, ~10 dakika)

1. github.com hesabı aç (varsa geç).
2. Sağ üstten **New repository**.
   - Ad: `yks` (istediğin ad olabilir)
   - **Public** seç (Pages ücretsiz sürümde herkese açık depo ister)
   - **Create repository**
3. Açılan sayfada **uploading an existing file** bağlantısına tıkla.
4. Bu klasördeki **bütün dosyaları** seçip sürükleyip bırak (alt klasör yok).
5. Aşağıdan **Commit changes**.
6. Depo sayfasında **Settings → Pages**.
   - Source: **Deploy from a branch**
   - Branch: **main** / klasör: **/ (root)** → **Save**
7. Bir iki dakika sonra aynı sayfada adres çıkar:

       https://KULLANICIADIN.github.io/yks/

Bu adres artık senin uygulaman. Güncelleme yapmak istediğinde yeni
`index.html`'i aynı yere yükleyip **Commit changes** demen yeterli;
telefonlardaki kopyalar kendiliğinden yenilenir.

## 2) Kendi cihazlarında aç

- **Android / bilgisayar:** adresi aç, tarayıcı menüsünden
  "Ana ekrana ekle" / "Uygulamayı yükle".
- **iPhone (Safari):** adresi aç → **Paylaş** → **Ana Ekrana Ekle**.

> **iPhone için önemli:** Safari, ana ekrana eklenmemiş sitelerin verisini
> 7 gün kullanılmazsa siler. Ablan mutlaka ana ekrana eklemeli.

## 3) Verini şu anki tarayıcıdan taşı

Yeni adres, yeni bir depo demek — eski veri kendiliğinden gelmez.

1. Şu an kullandığın dosyada: **Daha → Ayarlar → Yedeği indir** (JSON).
2. Yeni adreste aynı yerden **Yedeği yükle** ile geri al.

PDF dosyaları bu yedeğe girmez (çok büyük olurlar). Onları yeni adreste
tekrar eklemen, ya da Drive'a yükleyip listeden açman gerekir.

## 4) Ablanla ortak kullanım

Ablan da adresi açıp ana ekrana ekler. Aynı veriyi görmeniz için:

1. Sende: **Daha → Ayarlar → Google E-Tablolar eşitlemesi** bölümündeki
   **web uygulaması adresi** ve **gizli anahtarı** ona ver.
2. O da aynı alanlara yazsın, **Ayarları kaydet** desin.
3. Aynı bölümdeki **cihaz adı** alanına ikiniz farklı ad yazın
   ("Telefon", "Ablam" gibi) — çakışmada hangisinin kaldığı böyle anlaşılır.
4. Değişiklik yaptıktan sonra **Şimdi aktar** düğmesine basın.

Plan hücreleri kendiliğinden ve sürekli eşitlenir. Denemeler, konular,
süreler ve PDF listesi "Şimdi aktar" ile taşınır.

### Bilmen gerekenler

- Ablan senin **bütün verini değiştirebilir ve silebilir**; Drive'daki
  "YKS Defterim" klasörüne de yazabilir. Geri alma yalnız kendi cihazında
  çalışır — karşıdan gelen bir silmeyi geri alamazsın.
- Bu yüzden **düzenli JSON yedeği** al. Ayarlar'daki haftalık otomatik
  yedeği açman en kolayı.
- İkiniz de aynı anda değişiklik yaptıysanız uygulama hangisinin kalacağını
  sorar; seçmeden önce iki tarafın saatine bak.

### Ayrı veri isterseniz

Eşitleme adresini paylaşmayın. Aynı uygulamayı kullanır ama her biriniz
kendi defterini tutar.

## 5) YouTube anahtarı üzerine

Uygulamada gömülü bir YouTube anahtarı var; ablanın aramaları da aynı
kotadan gider. İkiniz için fazlasıyla yeter. Yine de:

- Adresi başkalarına yaymayın (depo herkese açık olduğu için anahtar da açıktır).
- Google Cloud'da anahtara **API kısıtlaması** koy: yalnız
  *YouTube Data API v3*. Böylece kaçsa bile başka bir şey için kullanılamaz.
- Anahtarı hiç paylaşmak istemezsen: uygulamada **Daha → Ayarlar →
  Uygulama içi video → Kaynak: Kapalı** seçilebilir; düğmeler YouTube'u açar.

## 6) iPhone'da bilinen iki durum

- **PDF görüntüleyici:** iOS Safari gömülü PDF'i açmayabilir. Açılmazsa
  görüntüleyicideki **Yeni sekmede** düğmesi kullanılmalı.
- **Depo temizliği:** iOS, uzun süre açılmayan uygulamaların verisini
  silebilir. Ana ekrana eklemek ve ara ara açmak bunu önler.
