# Değişkenler, Sabitler ve Veri Tipleri

## Giriş: Bilgisayarın Belleği

Bilgisayarlar, verileri hafızalarında saklar. Bu veriler, her birinin kendine has bir "adı" ve "tipi" ile birlikte depolanır. **Değişken**, bilgisayarın verisini saklamak ve daha sonra kullanmak için ayrılan bir konumdur. **Veri tipi**, bu verinin hangi türde bilgiyi taşıyacağını belirler. **Sabit**, değeri değiştirilemeyen bir değişken türüdür.

> [!NOTE]
> Bilgisayar belleği, raflar ve kutulardan oluşan bir depolama gibi düşünülebilir: her kutunun bir etiketi (isim) ve içindeki ürün türü (tip) vardır.

![Bellek analogisi](images/03-Memory-Analogy.jpg)  
> (buraya bellek analogisi görseli uygun olur)

---

## Değişken Nedir? ve Nasıl Kullanılır?

Bir **değişken**, verileri saklamak için kullanılan bir "kavadır". Değişken yaratıldığında (veya tanımlanırken), bilgisayar belli bir bellek bölgesini o veriye ayırır. Daha sonra programın herhangi bir yerinde bu değişkenin ismini çağırarak değeri alabilir ya da değiştirebilirsiniz.

### Değişken Nasıl Tanımlanır?

Genellikle değişken tanımlamak için **isim + tip** şeklinde bir ifade kullanılır.

| Kavram | Açıklama |
|--------|----------|
| **İsim** | Değişkeni tanımlamak için kullandığımız kimlik. İsimlendirme kuralları konusundan daha sonra bahsedilecek. |
| **Tip** | Değişkenin saklayacağı veri türünü belirten etiket (tam sayı, ondalık, metin, mantıksal vb.). |
| **Değer** | Değişkenin atanacağı başlangıç verisi. (İsteğe bağlı; belirtilmezse öntanımlı değer kullanılır.) |

> [!TIP]
> Değişken isimleri anlamlı olmalı: `x` yerine `kullaniciYasi`, `sayi` yerine `toplam` gibi isimler tercih edilmelidir.

![Değişken tanımlama örneği](images/03-Variable-Declaration.jpg)  
> (buraya değişken tanımlamak için örnek kod görseli uygun olur)

### Birkaç Örnek

**Örnek 1: Yaş Değişkeni**

```
Değişken: kullaniciYasi
Tip: Tam Sayı (integer)
Değer: 25
```

**Örnek 2: İsim Değişkeni**

```
Değişken: kullaniciAdi
Tip: Metin (string)
Değer: "Ali"
```

> [!IMPORTANT]
> Değişken adı boşluk veya özel karakter içeremez; alt çizgi (_) kullanılabilir.

---

## Temel Veri Tipleri

Programlama dillerinin çoğu, verileri kategorize etmek için birkaç temel veri tipini standart olarak destekler. Bunlar birbirinden farklı miktarlarda bilgi saklar ve farklı işlemler için kullanılır.

### 1. Tam Sayı (Integer)

- **Açıklama**: Ondalık kısmı olmayan tam sayılar. Pozitif, negatif sıfır veya sıfırdan farklı olabilir.
- **Örnek**: -3, 0, 7, 42
- **Kullanım Alanı**: Sayaclar, listedeki konum indeksleri, bütçeler.
- **Bellek**: Genellikle 4 byte (32 bit) veya 8 byte (64 bit).

### 2. Ondalıklı Sayı (Float / Double)

- **Açıklama**: Ondalıklı (ondalıklıklı) sayılar. Daha hassas matematiksel işlemler için kullanılır.
- **Örnek**: 3.14, -0.5, 2.0, 100.75
- **Kullanım Alanı**: Ölçümler, fiziksel veriler, grafik koordinatları.
- **Bellek**: 4 byte (float) veya 8 byte (double).

> [!TIP]
> Hassasiyet gerektiren işlemlerde double (64 bit) tercih edilmelidir; bellek tasarrufu için float (32 bit) yeterli olabilir.

### 3. Metin (String)

- **Açıklama**: Karakterler koleksiyonu. Kelimeler, cümleler, paragraflar ya da her türlü metin verisi içerebilir. Genellikle çift tırnak (") veya tek tırnak (') ile çevrelidir.
- **Örnek**: "Merhaba", 'Selam', "Ali Velioğlu"
- **Kullanım Alanı**: Kullanıcı girdileri, dosya isimleri, açıklamalar.
- **Bellek**: Değişken uzunluğa göre değişir (genellikle 1 byte per karakter).

> [!NOTE]
> Metin içinde özel karakterler (örn: yeni satır \n, tab \t) escape karakterleriyle eklenebilir.

### 4. Mantıksal (Boolean)

- **Açıklama**: Sadece iki olası değerden birini taşır: **Doğru (true)** veya **Yanlış (false)**. Koşulları kontrol etmek ve kararlar almak için kullanılır.
- **Örnek**: `true`, `false`, `doğru`, `yanlış`
- **Kullanım Alanı**: Koşullar (`if`), döngüler (`while`), on/off anahtarları.
- **Bellek**: Genellikle 1 byte.

> [!CAUTION]
> Bazı dillerde `0` ve `1` de mantıksal olarak kabul edilir; bu karışıklığı önlemek için açıkça `true`/`false` kullanın.

---

## Sabitler (Constants)

Bir **sabit**, değiştirilemez bir değerdir. Değişkenlerin aksine, program çalışırken sabitinin değeri değiştirilemez. Sabitler genellikle programın başlangıcında veya yapılandırma bölümünde tanımlanır.

### Neden Sabitler Kullanılır?

- **Okunabilirlik**: Değerleri isimlerle ifade etmek, kodun anlaşılmasını kolaylaştırır.
- **Güvenlik**: Rastgele değişimlerden kaçınmak için belirli değerleri korur.
- **Bakım**: Tek bir yerden değiştirilmesi, tüm kodu etkilemeden güncellemek mümkün kılar.

| Örnek Sabit | Değer | Açıklama |
|-------------|-------|----------|
| `PI` | 3.14159 | Dairenin çevre ve çap oranı |
| `MAX_KULLANICI` | 100 | Sistemde maksimum kullanıcı sayısı |
| `GREETING` | "Merhaba!" | Sabit bir selamlama mesajı |
| `VAT_ORANI` | 0.18 | %18 KDV oranı |

> [!TIP]
> Sabit isimleri genellikle büyük harfle yazılır (örn: `PI`, `MAX_KULLANICI`) – bu da değişkenlerden ayırt edilmesini sağlar.

![Sabit kullanım örneği](images/03-Constants-Example.jpg)  
> (buraya sabitler kullanımının görsel örneği uygun olur)

---

## Veri Dönüşümleri (Type Casting)

Bazen bir değişkenin tipini değiştirmek isteyebiliriz. Bu işlem **"veri dönüşümü"** veya **"type casting"** olarak adlandırılır.

### Neden Dönüşüm Yapılır?

| Durum | Açıklama |
|-------|----------|
| **Sayıyı metne çevirme** | Hesaplamaları metin olarak göstermek istersek. |
| **Metni sayıya çevirme** | Metin olarak girilen bir sayısal değeri, hesaplamalar için sayıya dönüştürmek istersek. |
| **Tipi uyumsuzluğu** | Farklı tiplere sahip iki değişkenle işlem yapmak istiyoruz. |

### Basit Örnekler

**Örnek: Sayıyı Metne Çevirme**

```
Değişken: sayi (tam sayı)
Değer: 42
Yeni Değişken: metin (metin)
Değer: str(sayi)  # "42" çıktısı
```

**Örnek: Metni Sayıya Çevirme**

```
Değişken: fiyatMetni (metin)
Değer: "100"
Yeni Değişken: fiyat (tam sayı)
Değer: int(fiyatMetni)  # 100 çıktısı
```

> [!WARNING]
> Geçersiz metni sayıya çevirmeyi denerseniz (örn: `"abc"`), hata alabilir; giriş verisini önceden doğrulayın.

![Veri dönüşüm örneği](images/03-Type-Casting.jpg)  
> (buraya veri dönüşüm örnekleri görseli uygun olur)

---

## Değişken Kullanım Kuralları

Değişken isimlendirirken dikkat edilmesi gereken bazı kuralar ve en iyi uygulamalar vardır:

1. **İsimler anlamlı olmalı**: `x` yerine `kullanici_adi`, `sayi` yerine `toplam` gibi isimler tercih edilmelidir.
2. **Büyük/küçük hassasiyet**: İsimler büyük/küçük harf hassasiyetine sahip olabilir (diline göre farklılık gösterir).
3. **İsim başında sayı olmamalı**: `1sayi` geçersiz; `sayi1` geçerli.
4. **Boşluk veya özel karakter kullanılmaz**: Değişken ismi sadece harfler, sayılar ve alt çizgi (_) içerebilir.
5. **Klavye kısayolları veya tanımlı sözlükler**: Bazı dillerde (Python, JavaScript vb.) değişken ismi olarak "if" ya da "for" gibi ayrılmış kelimeler kullanılmaz.

### Hatalı ve Doğru İsimlendirme Örnekleri

| Hatalı İsim | Neden | Doğru İsim | Açıklama |
|-------------|-------|------------|----------|
| `user-name` | Tırnak içermiyor olabilir | `user_name` | Alt çizgi tercih edilmeli |
| `2big` | Sayıyla başlar | `big2` | Sayı alt üfle eklenmeli |
| `if` | Ayrılmış kelime | `kosul` | Ayrılmış kelimeler kullanılmayalı |
| `user age` | Boşluk var | `user_age` | Boşluk yerine alt çizgi |

> [!NOTE]
> Bazı dillerde değişken isimleri case-sensitive (büyük/küçük harf duyarlıdır): `age` ve `Age` farklıdır.

![Değişken isimlendirme kuralları](images/03-Variable-Naming-Rules.jpg)  
> (buraya değişken isimlendirme kurallarının karşılaştırması görseli uygun olur)

---

## Örnek Uygulama: Kullanıcı Bilgisi Toplama

Aşağıdaki örnek, değişkenleri, tipleri ve kullanım kurallarını bir arada gösterir.

### Senaryo: Kullanıcı Girişi ve Bilgileri

1. Kullanıcının adını ve yaşını sor.
2. Yaşı 10 yıl artır.
3. Sonuçları ekrana yaz.

### Kod Parçacığı (Pseudo-code)

```
# Değişkenler tanımlanıyor
Değişken: kullanici_adi (metin)
Değişken: yas (tam_sayı)
Değişken: yeni_yas (tam_sayı)

# Kullanıcıdan veri alınıyor
kullanici_adi = "Ali"
yas = 25

# Yaşı 10 artırıyor
yeni_yas = yas + 10

# Sonuçlar ekrana yazdırılıyor
Yaz: "Kullanıcı: " + kullanici_adi
Yaz: "Yaş: " + yas
Yaz: "Yeni Yaş: " + yeni_yas
```

> [!TIP]
> Bu örnekte `yas` değişkeni bir kez tanımlanır ve ardından değeri değiştirilir; böylece bellekte sadece bir konum kullanılır.

![Kullanıcı bilgisi örneği](images/03-User-Info-Example.jpg)  
> (buraya örnek uygulama görseli uygun olur)

---

## Alıştırmalar

Aşağıdaki alıştırmaları çözün. Her birini kod (pseudo-code veya kendi diline) olarak yazın ve değişken isimlerini anlamlı kıl.

### Alıştırma 1: Üçgenin Alanı

Taban ve yüksekliği veriliyor. Üçgenin alanını (alan = taban × yükseki ÷ 2) hesaplayın ve sonucu ekrana yazdırın.

### Alıştırma 2: Sayıları Topla

Kullanıcıdan iki tam sayı isteyin ve toplamı ekrana yazdırın. Sayının "çift" veya "tek" olduğunu da belirtin.

### Alıştırma 3: Koşul Kontrolü

Kullanıcıdan bir not (0-100 arası) alın. Not 50 ve üzeri ise "Başarılı", altı ise "Başarısız" yazdırın. Mantıksal (boolean) bir değişken kullanarak kontrol yapın.

> [!IMPORTANT]
> Her alıştırma için önce değişkenleri tanımlayın, sonra işlemleri yapın, sonunda sonucu gösterin.

![Alıştırmalar örneği](images/03-Exercises.jpg)  
> (buraya alıştırmaların görsel örneği uygun olur)

---

## Özet

- **Değişken**, bilgisayarın verisini saklamak ve kullanmak için ayrılan bir konumdur.
- **Veri tipi**, değişkenin saklayacağı bilgiyi tanımlar (tam sayı, ondalık, metin, mantıksal).
- **Temel tipler**: Integer (tam sayı), Float/Double (ondalık), String (metin), Boolean (mantıksal).
- **Veri dönüşümü**, bir tipi başka bir türe çevirmektir; `str()`, `int()` gibi fonksiyonlar ile yapılır.
- **Sabitler**, değiştirilemez değerlerdir; programın anlaşılırlığı ve bakımı için kullanılır.
- **Değişken isimlendirme**, anlamlı, tek başına sayı başlatmayan, boşluk veya özel karakter içermeyen kurallara uyarak yapılmalıdır.

> [!NOTE]
> Değişken ve veri tipi kavramları, daha sonraki konularda (diziler, döngüler, fonksiyonlar) sıkça kullanılacaktır.

Sonraki bölümde **Aritmetik ve Mantıksal Operatörler** konusuna geçeceğiz.