# Karar Yapıları

## Giriş: Seçim Yapmanın Temeli

Bir program yalnızca komutları yukarıdan aşağıya sırayla çalıştırmakla kalmaz; çoğu zaman veriye veya kullanıcı girdilerine bağlı olarak farklı adımlar seçmek zorunda kalır. **Karar yapıları (koşullu ifadeler)**, bilgisayara akılı seçimler yapma yeteneği kazandıran mekanizmadır. Belirli bir koşul **Doğru (True)** ise bir yol, **Yanlış (False)** ise başka bir yol izlenir.

> \[!NOTE\]
> Karar yapısı bir yol ayrımı (kavşak) gibidir: Hangi yoldan ilerleyeceğinizi o andaki koşul belirler.

```
flowchart TD
    A([Başla]) --> B{Koşul Doğru mu?}
    B -- Evet --> C[İşlem A]
    B -- Hayır --> D[İşlem B]
    C --> E([Bitir])
    D --> E

```

## Karar Yapılarının Önemi ve Avantajları

- **Dinamik Programlama**: Sabit çıktılar yerine duruma ve veriye göre tepki veren esnek yazılımlar oluşturmayı sağlar.
- **Akış Kontrolü**: Hatalı veya istenmeyen verilerin programa zarar vermesini engeller (örneğin sıfıra bölme hatasını önlemek).
- **Mantıksal Ayrıştırma**: Karmaşık iş kurallarını basitleştirerek adım adım kontrol edilebilir hale getirir.

> \[!TIP\]
> Karar yapılarını koda dökmeden önce bir akış şeması üzerinde görselleştirmek, mantıksal açıkları erkenden tespit etmenizi sağlar.

## Karar Yapısının Temel Elemanları

Bir karar yapısı oluştururken mantıksal değerlendirmeler yapmak için **Karşılaştırma Operatörleri** ve **Mantıksal Operatörler** kullanılır.

### 1. Karşılaştırma Operatörleri

İki değeri birbiriyle kıyaslamak için kullanılan operatörlerdir. İşlem sonucunda her zaman **Doğru (True)** veya **Yanlış (False)** döner.

| Operatör | Anlamı | Örnek İfade | Sonuç (`x = 5` için) | 
| ----- | ----- | ----- | ----- | 
| `==` | Eşit mi? | `x == 5` | `True` | 
| `!=` | Eşit değil mi? | `x != 5` | `False` | 
| `>` | Büyük mü? | `x > 3` | `True` | 
| `<` | Küçük mü? | `x < 10` | `True` | 
| `>=` | Büyük veya eşit mi? | `x >= 5` | `True` | 
| `<=` | Küçük veya eşit mi? | `x <= 4` | `False` | 

> \[!WARNING\]
> Tek eşittir (`=`) **değer atama** işlemidir. Çift eşittir (`==`) ise **karşılaştırma** işlemidir. Bu iki sembolü karıştırmak yaygın bir mantık hatasıdır.

### 2. Mantıksal Operatörler

Birden fazla koşulu tek bir kararda birleştirmek için kullanılır.

* **VE (AND / `&&`)**: Bağlanan tüm koşulların **aynı anda Doğru** olmasını gerektirir.

  * Örnek: `kullanici_adi == "admin" AND sifre == "1234"`

* **VEYA (OR / `||`)**: Bağlanan koşullardan **en az birinin Doğru** olması yeterlidir.

  * Örnek: `bakiye >= 100 OR kredi_kartı == True`

* **DEĞİL (NOT / `!`)**: Mantıksal durumun tersini alır. Doğru ise Yanlış, Yanlış ise Doğru yapar.

  * Örnek: `NOT(isLoggedIn)` -> Kullanıcı giriş yapmamışsa.

---

## Karar Yapılarının Temel Türleri

### 1. Tek Yönlü Karar Yapısı (If)

Koşul sağlandığında (`True`) belirli bir işlem yapılır. Koşul sağlanmıyorsa (`False`) hiçbir şey yapmadan akışa devam edilir.

```
flowchart TD
    A([Başla]) --> B{Sayı > 0?}
    B -- Evet --> C[/Ekrana Yaz: Pozitif/]
    B -- Hayır --> D([Bitir])
    C --> D

```

### 2. Çift Yönlü Karar Yapısı (If-Else)

Koşul sağlandığında bir yol, sağlanmadığında ise alternatif bir yol izlenir.

```
flowchart TD
    A([Başla]) --> B{Not >= 50?}
    B -- Evet --> C[/Ekrana Yaz: Başarılı/]
    B -- Hayır --> D[/Ekrana Yaz: Başarısız/]
    C --> E([Bitir])
    D --> E

```

### 3. Çoklu Karar Yapısı (If - Else If - Else)

Birden fazla olasılığın ve koşulun sırayla kontrol edildiği durumlar için kullanılır. Koşullardan biri sağlandığında ilgili blok çalışır ve yapıdan çıkılır.

```
flowchart TD
    A([Başla]) --> B{Not >= 90?}
    B -- Evet --> C[Harf Notu: A]
    B -- Hayır --> D{Not >= 80?}
    D -- Evet --> E[Harf Notu: B]
    D -- Hayır --> F{Not >= 70?}
    F -- Evet --> G[Harf Notu: C]
    F -- Hayır --> H[Harf Notu: F]
    C --> I([Bitir])
    E --> I
    G --> I
    H --> I

```

### 4. Çoklu Seçim Yapısı (Switch - Case)

Bir değişkenin alabileceği sabit değerlere göre doğrudan ilgili duruma (Case) atlamasını sağlayan temiz ve okunabilir bir karar yapısıdır. Özelikle menü seçimlerinde tercih edilir.

```
# Sahte Kod Örneği (Switch-Case)
SEÇİM (gun_no)
    DURUM 1: YAZDIR "Pazartesi"
    DURUM 2: YAZDIR "Salı"
    DURUM 3: YAZDIR "Çarşamba"
    VARSAYILAN: YAZDIR "Geçersiz Gün"
SON SEÇİM
```

---

## Karar Yapısının Öğrenilmesi İçin Örnek Uygulama

**Senaryo:** Girilen bir sayının pozitif, negatif veya sıfır olduğunu tespit etme.

**Algoritma Adımları:**

1. **Başla**

2. Kullanıcıdan bir sayı al (`Sayı`)

3. **Sayı > 0** ise "Pozitif" yazdır.

4. Değilse ve **Sayı < 0** ise "Negatif" yazdır.

5. Aksi halde (Sayı 0'a eşitse) "Sıfır" yazdır.

6. **Bitir**

```
flowchart TD
    A([Başla]) --> B[/Sayı Al/]
    B --> C{Sayı > 0?}
    C -- Evet --> D[/Yaz: Pozitif/]
    C -- Hayır --> E{Sayı < 0?}
    E -- Evet --> F[/Yaz: Negatif/]
    E -- Hayır --> G[/Yaz: Sıfır/]
    D --> H([Bitir])
    F --> H
    G --> H

```

---

## Alıştırmalar

Aşağıdaki problemleri inceleyerek algoritma adımlarını ve akış şemalarını oluşturun.

### Alıştırma 1: Yaş Grubu Kontrolü

Kullanıcıdan yaş bilgisini alın:

* 18'den küçükse → "Reşit Değil"

* 18–64 yaş arası ise → "Yetişkin"

* 65 ve üzeri ise → "Kıdemli Yetişkin / Emekli" mesajını ekrana yazdırın.

### Alıştırma 2: Sayısal Notu Harf Notuna Çevirme

Kullanıcıdan 0–100 arası bir sınav notu alın:

* 90–100 → A

* 80–89 → B

* 70–79 → C

* 60–69 → D

* 0–59 → F harf notunu ekrana yazdırın.

### Alıştırma 3: Kullanıcı Giriş Kontrolü (VE Operatörü Uygulaması)

Kullanıcıdan `kullanici_adi` ve `sifre` bilgilerini alın.

* Eğer `kullanici_adi == "admin"` **VE** `sifre == "12345"` ise "Giriş Başarılı"

* Aksi halde "Kullanıcı adı veya şifre hatalı!" mesajı verin.

> \[!IMPORTANT\]
> Alıştırmaları çözerken önce kararın tek yönlü mü, çift yönlü mü yoksa çoklu mu olduğunu belirleyin.

---

## Özet

- **Karar Yapıları**, programın dinamik koşullara göre farklı kod bloklarını çalıştırmasını sağlar.

- **Tek Yönlü (If)**: Koşul sağlandığında çalışır.

- **Çift Yönlü (If-Else)**: Koşulun sağlandığı ve sağlanmadığı iki farklı yol sunar.

- **Çoklu Karar (If - Else If - Else)**: Birden fazla sıralı koşulu kontrol eder.

- **Switch-Case**: Belirli sabit değerler üzerinden doğrudan dallanma sağlar.

- Mantıksal operatörler (**AND**, **OR**, **NOT**) karmaşık koşulları tek bir yapıda birleştirmemize imkan tanır.

Sonraki bölümde kararların tekrarlayan işlemlerle birleştiği **Döngüler (Loops)** konusuna geçeceğiz.