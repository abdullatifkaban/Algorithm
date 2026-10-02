# Algoritma Nedir?

## Giriş: İşlem Yapmanın Felsefesi

Bilgisayarlar, sadece sayılar ve karakterleri işleyebilir. Bir işlem yapabilmek için, “bir şey yap” şeklinde karmaşık talimatlara ihtiyaç duyar. **Algoritma**, bu işlem yapma sürecinin en temel ve önemli yapı taşıdır.

> [!NOTE]
> Algoritma, bir yemek tarifine benzer: malzemeler (girdiler), adımlar (süreç) ve sonuç (çıktı) içerir.

```mermaid
flowchart TD
    A[Başla] --> B{İşlem yap}
    B -->|Evet| C[Sonuç al]
    B -->|Hayır| D[Başka dene]
    C --> E[Bitir]
    D --> B
```

---

## Algoritma Tanımı: Evrensel Bir Kavram

Algoritma, **belirli bir problemi çözmek için belirli bir sıralı adım dizisidir**. Her adım, önceki adımın sonucuna dayalı olarak yapılır ve sonunda kesin bir çıktı verir.

### Algoritmanın Beş Kritik Özelliği

| Özellik | Açıklama | Örnek |
|---------|----------|-------|
| **Giriş** | İşlem başlamadan önce alınan veriler | Diş fırçalama için su, macun |
| **Çıkış** | Algoritmanın sonunda ulaşılan sonuç | Temiz diş |
| **Belirli** | Her adım net ve tek yönlü ifade edilmelidir | “2 dakika fırçala” → “biraz fırçala” değil |
| **Sonlu** | Belli sayıda adım sonlanır, sonsuz döngü yoktur | Diş fırçalama 2 dakikada biter |
| **Etkili** | Her adım temel işlemlerle gerçekleştirilebilir | Her adım temel, uygulanabilir ve kağıt-kalemle bile yürütülebilecek basitlikte olmalıdır |

> [!TIP]
> İyi bir algoritma, her adımını kesin ve ölçülebilir kılar; belirsiz kalmaz.

```mermaid
flowchart LR
    A[Beş Özellik] --> B[Giriş]
    A --> C[Çıkış]
    A --> D[Belirli]
    A --> E[Sonlu]
    A --> F[Etkili]
```

---

## Algoritmanın Hayatımızda Herkese Açık Örnekleri

### 1. Kahve Yapım Algoritması

1. Kahve makinesine su ekleyin.  
2. Kavanozun içine kahve çekirdeği koyun.  
3. Kapağı kapatın.  
4. Brezilya Ayarı’nı seçin.  
5. “Start” tuşuna basın.  
6. Kavanozdan kahveyi çıkarın.  
7. **Eğer** şekerli isteniyorsa **şeker/şekerleme ekleyin**.  

> [!IMPORTANT]
> Her adım sıralı olmalı; örneğin kahveyi makineden almadan önce ekranı çalıştırmamalıyız.

```mermaid
flowchart TD
    A[Su ekle] --> B[Kahve koy]
    B --> C[Kapak kapa]
    C --> D[Start tuşuna bas]
    D --> E[Kahveyi çıkar]
    E --> F{Şekerli isteniyor mu?}
    F -->|Evet| G[Şeker ekle]
    F -->|Hayır| H[İçeriği servis et]
    G --> H
    H --> I[Bitir]
```

### 2. YouTube’da Video Arama Algoritması

1. Tarayıcı açın.  
2. youtube.com adresine girin.  
3. Arama çubuğuna videonun adını yazın.  
4. “Enter” tuşuna basın.  
5. Listelenen videolar arasından istediğinizi seçin.  
6. Video oynatıcıyı başlatın.

```mermaid
flowchart TD
    A[Tarayıcı aç] --> B[YouTube sitesine git]
    B --> C[Arama çubuğuna yazı yaz]
    C --> D[Enter tuşuna bas]
    D --> E[Sonuçları listele]
    E --> F[İstenen videoyu seç]
    F --> G[Video oynatıcıyı başlat]
    G --> H[Bitir]
```

### 3. Diyalog Kutusu Açma Algoritması (Telefon)

1. Telefon uçak modunu kapatın.  
2. Ana sayfaya dönün.  
3. “Telefon” uygulamasını açın.  
4. Aranacak kişiyi girin.  
5. “Ara” butonuna dokunun.  

```mermaid
flowchart TD
    A[Uçak modunu kapat] --> B[Ana sayfaya dön]
    B --> C[Telefon uygulamasını aç]
    C --> D[Kişi numarasını gir]
    D --> E[Ara butonuna dokun]
    E --> F[Arama başlar]
    F --> G[Bitir]
```

---

## Neden Algoritma Çok Önemlidir? Üç Evrensel Soru

### Soru 1: “Bu İşlemi Kimse Yapmıyorsa Ne Yaparım?”

Algoritma, karşılaştığınız bir problemin **adım adım çözüm yolunu** oluşturur. Örneğin, “bir metnin içinde belirli bir kelimenin var olup olmadığını” nasıl bulursunuz?

#### Adım Adım Çözüm:
1. Metni oku.  
2. Kelimeyi baştan itibaren kontrol et.  
3. Eşleşirse, sonuç “var”.  
4. Hiç eşleşmezse, sonuç “yok”.

### Soru 2: “Bilgisayarı Etkin Kullanmak İçin Ne Gerekir?”

Bilgisayarlar sadece “ilk = 5, sonra = 3” gibi basit komutları işletir. **Algoritma**, bu basit komutları bir araya toplayıp karmaşık işlerde kullanmamızı sağlar.

> [!WARNING]
> Algoritmadan çok fazla adım çıkarmak, programı gereksiz yavaşlatır ve hata olasılığını artırır.

```mermaid
flowchart TD
    A[Başla] --> B[Metni oku]
    B --> C[Kelimeyi tara]
    C --> D{Eşleşti mi?}
    D -->|Evet| E[Sonuç: var]
    D -->|Hayır| F[Sonuç: yok]
    E --> Z[Bitir]
    F --> Z
```

### Soru 3: “Farklı Şekillerde Aynı İşleti Yapabilir miyim?”

Evet! Aynı problem, farklı algoritmalarla çözülebilir. Örneğin, 100 sayı içinde en büyük sayıyı bulmak için:

- **Yöntem A**: Her sayıyı tek tek karşılaştır. (100 elemanda 100 karşılaştırma yapmak gibi)
- **Yöntem B**: Sayıları sırala, ilk elemanı al. (100 elemanda ~700 karşılaştırma yapmak gibi, sıralama maliyetiyle)
- **Yöntem C**: Sadece bir değişken tut, gezerken en büyüğü yakala. (100 elemanda 100 karşılaştırma yapmak gibi, ama sadece bir değişkenle)

Her yöntem farklıdır ama hepsi doğru sonucu verir.

> [!CAUTION]
> Yanlış algoritma seçimi, büyük veri kümelerinde performans sorunlarına yol açabilir (örnek: O(n²) yerine O(n log n) kullanılmalı).

---

## Algoritma Geliştirme Süreci

### Aşama 1: Problemi Tanımla

Öncelikle **tam olarak ne istendiğini** belirlemelisiniz:
- “Kullanıcı girişinde bir şifre kontrolü yap” yeterli mi?
- “Şifreyi bir kere kullanma sayısı kadar tut” gerekir mi?

> [!NOTE]
> Problemi net bir tanım koymak, gereksiz adımları önler.

```mermaid
flowchart TD
    A[Problemi belirle] --> B[Giriş-Çıkış tanımlı mı?]
    B -->|Hayır| C[Giriş ve çıkışları netleştir]
    C --> D[Adımları sırala]
    D --> E[Her adımı netleştir]
    E --> F[Çözümü test et]
    F --> G[Bitir]
```

### Aşama 2: Giriş ve Çıkışları Belirle

- **Giriş**: Algoritmaya ne kadar veri gerekir?
- **Çıkış**: Ne tür bir sonuç istersiniz?

| Sorunun Örneği | Giriş | Çıkış |
|----------------|-------|-------|
| Ortalama hesaplama | 3 sayı | Bu sayıların ortalaması |
| Sayı çift mi? | 1 tam sayı | “Evet” veya “Hayır” |
| Kitap arama | Kitap adı, yazar | Kitabın konumu |

> [!TIP]
> Girdi ve çıktıyı net tanımlamak, algoritmanın test edilmesini kolaylaştırır.

### Aşama 3: İçerdeki Mantığı Çöz

Bu aşamada, **çözüm için sıralanmamış adımlarla** başa çıkabilirsiniz. Genellikle “eğer…ise, o zaman…değilse…” yapıları kullanılır.

> [!IMPORTANT]
> Mantık adımlarını karıştırmadan önce tüm olası senaryoları yazın.

```mermaid
flowchart TD
    A[Koşul 1] -->|Evet| B[İşlem 1]
    A -->|Hayır| C[Koşul 2]
    C -->|Evet| D[İşlem 2]
    C -->|Hayır| E[İşlem 3]
    B --> Z[Bitir]
    D --> Z
    E --> Z
```

### Aşama 4: Sıralı Algoritma Oluştur

Algoritmanız bir satırda yazılmaz. Her adım **açık ve sıralı** olmalıdır.

#### Örnek: Sayının Çift Olup Olmadığını Kontrol Etme

```
Başla.
Sayı = 7
Eğer Sayı % 2 = 0 ise
    Yaz: "Çift sayıdır"
Değilse
    Yaz: "Tek sayıdır"
Bitir.
```

> [!TIP]
> Modulo operatörü (`%`) ile tek/çift kontrolü hızlı ve güvenilir bir yoldur.

```mermaid
flowchart TD
    A[Başla] --> B[Sayı = 7]
    B --> C{Sayı mod 2 = 0?}
    C -->|Evet| D[Yaz: Çift sayıdır]
    C -->|Hayır| E[Yaz: Tek sayıdır]
    D --> F[Bitir]
    E --> F
```

---

## Algoritma Türleri

### 1. İşlevsel (Functional) Algoritmalar

Bir işin “nasıl yapılır” sorusuna odaklanır.  
**Örnek**: “Bir dizinin ortalamasını nasıl alırım?”

### 2. Karar Aracı (Decision-Based) Algoritmalar

Koşullara göre farklı sonuçlar verir.  
**Örnek**: “Hangi yolculuk ücreti daha uygun?”

> [!NOTE]
> Karar algoritmaları, genellikle elmas (rombüs) şeklinde gösterilir.

```mermaid
flowchart TD
    A[Start] --> B{Koşul?}
    B -->|Evet| C[İşlem A]
    B -->|Hayır| D[İşlem B]
    C --> E[End]
    D --> E
```

### 3. Tekrarlı (Iterative) Algoritmalar

Bir işlem belli kez veya koşul sağlandıkça tekrarlanır.  
**Örnek**: “Listedeki tüm öğrencilerin notlarını topla”

---

## Algoritma Çiziminde İpuçları

- **Belli adımlar kesinlikle izlenecek** bir şey olmalı.
- **“Ya da”, “ve”, “eğer” gibi kelimeler yerine “ise”, “diğer taktirde” gibi net ifadeler kullanın.
- Mümkünse **örneklem** ekleyin: “Örneğin, 24 yazdırın, sonra 18’i çıkarın.”

> [!TIP]
> Akış şeması çizerken her kutucuğa kısa ve anlamlı ifadeler yazın; okunabilirliği artar.

---

## Sık Karşılaşılan Hatalar ve Çözüm Yolları

| Hata | Neden | Çözüm |
|------|--------|--------|
| **Adım eksikliği** | Bir parça unutulmuş | Tüm adımlar bir kontrol listesinde |
| **Adım çelişkisi** | “Aynı anda iki iş yap” | Akış şeması çizerek kontrol et |
| **Adım kuvvetliliği** | “Biraz fazla” gibi belirsizlikler | Net sayılar veya ölçü birimleri |
| **Sonsuz döngü** | “Eğer koşul ise, ekle” ama hiç bitme şartı yok | Mutlaka bir “bitir” veya “dur” adımı |

> [!WARNING]
> Sonsuz döngü, programın donmasına ve kaynak tüketimine yol açar; her zaman bir çıkış koşulu olmalıdır.

---

## Alıştırmalar

Aşağıdaki alıştırmaları kendi başınıza çözün. Çözümünüzü **doğrudan yaz** ve ardından bir akış şeması çizin.

### Alıştırma 1: Kahvaltı Alarmı

Akşam yemek sonrası erken kalkmak için size kalan sürenin bir algoritması yazın. Giriş: kalan saat, dakika. Çıkış: “Alarm kaç’ta çalsın?”

### Alıştırma 2: Kitap Sayfası Sayma

Bir kitapta kaç sayfa olduğunu öğrenmek için izlemeniz gereken adımları sırasıyla yazın. Her sayfayı saymanız gerekiyor mu? Bir başlık ile neyi ararsınız?

### Alıştırma 3: E-posta Şifresi Güncelleme

E-posta hesabınıza giriş yapıp şifrenizi değiştirmek için adım adım bir yol haritası çıkarın. Aşağıdaki noktaları içermeli:
- Şifreniz nerede saklanır?  
- Hangi siteye giriş yapmalısınız?  
- Şifreyi ne zaman güncellemelisiniz?

> [!IMPORTANT]
> Şifre değiştirme sürecinde mevcut oturumlar dikkate alınmalı; kullanıcıya uygun bir zaman seçin.

---

## Özet

- **Algoritma**, problemi çözmek için sıralı bir talimattır.
- **5 temel özellik**: giriş, çıkış, belirli, sonlu, etkili.
- Günlük hayat tüm alışkanlıklarından daha karmaşık algoritmalar gerektirir.
- Doğru bir algoritma, hatasız sonuç verir; yanlış bir algoritma, hatanızı bile kendine öğretir.

> [!NOTE]
> Algoritma kavramını pekiştirmek için günlük yaşam üzerinden örnekler üretmeye devam edin.

Sonraki bölümde **“Akış Şemaları”** nasıl çizeriz, onu öğreneceğiz.