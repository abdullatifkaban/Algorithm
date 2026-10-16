# COURSE_PLAN

Bu dosya, "Veri Yapıları ve Algoritmalar" kursunun tasarım kararlarını saklar.
Ders içeriği üretilirken terminoloji, yapı ve pedagojik yaklaşım bu dosyadaki
kararlara göre korunur.

## Kurs Profili

| Alan | Karar |
|---|---|
| Ders adı | Veri Yapıları ve Algoritmalar |
| Eğitim düzeyi | Başlangıç düzeyi (1. sınıf üniversite düzeyine denk, materyal herkese açık) |
| Hedef kitle | Hiç programlama görmemiş, algoritma ve programlamaya yeni başlayan herkes |
| Öğrenci hazırbulunuşluğu | Programlama bilgisi yok; yalnızca temel bilgisayar ve dosya kullanımı varsayılır |
| Ön koşul bilgi | Yok |
| Haftalık süre | 2 saat |
| Toplam süre ve bölümleme | 14 haftalık ders; içerik "Hafta" ifadesi kullanılmadan 12 bölüm sınırı içinde 11 bölüm olarak yapılandırılır |
| Teori/uygulama dengesi | Teorik anlatım ve bol örnek problem; uygulama kodla değil, sözde kod ve akış şeması ile yapılır |
| Ders türü | Algoritma ve problem çözme (programlamaya giriş kavramlarıyla harmanlanmış) |
| Programlama dili | Yok. Hiçbir bölümde gerçek kod kullanılmaz |
| Ana temsil araçları | Türkçe sözde kod ve Mermaid akış şemaları |
| Kapsam sınırı | Programlamaya giriş kavramları (değişken, sabit, veri tipleri, diziler, karar yapıları, döngüler) ve temel algoritmalar (arama, basit sıralama). Yığın, kuyruk, bağlı liste, ağaç, graf, hash tablosu, öbek ve karmaşıklık analizi (Big-O) kapsam dışıdır |
| Değerlendirme bağlamı | Yok. Materyal yalnızca öğrenme materyalidir |
| Beklenen nihai yeterlik | Bir problemi elle çözme, çözüm fikrini algoritmaya dönüştürme, Türkçe sözde kod yazma ve akış şeması çizme |
| Hitap biçimi | "sen" (tüm materyalde tutarlı) |
| Dil politikası | Tüm içerik Türkiye Türkçesi; yalnızca Latin alfabesi. Dosya ve klasör adları İngilizce, içerik Türkçe |
| Yayın bağlamı | GitHub'da herkese açık; bireysel öğrenmeyi destekleyecek şekilde tasarlanır |
| Repo kök klasörü | `Data-Structures-Algorithms` |

## Öğrenme Çıktıları

1. Algoritma kavramını açıklar ve günlük yaşamdan örneklerle ilişkilendirir.
2. Bir problemi anlar; girdileri, çıktıyı ve ara adımları belirleyerek çözümü planlar.
3. Bir çözüm fikrini Türkçe sözde kod ile yazar.
4. Akış şeması sembollerini tanır ve bir algoritmayı Mermaid ile akış şeması olarak çizer.
5. Değişken, sabit ve temel veri tiplerini ayırt eder; bunları problemlerde uygun biçimde kullanır.
6. Atama, aritmetik ve karşılaştırma işlemlerini sözde kod içinde uygular.
7. Karar yapılarını kullanarak farklı durumlara göre farklı işlem yapan çözümler tasarlar.
8. Döngüleri kullanarak tekrar eden işlemleri sözde kod ile ifade eder.
9. Dizileri kullanarak aynı türden çok sayıda veriyi saklar ve işler.
10. Doğrusal arama ve ikili arama algoritmalarını açıklar, uygular ve karşılaştırır.
11. Kabarcık ve seçmeli sıralama algoritmalarını açıklar ve uygular.
12. Bir sözde kodu veya akış şemasını izleme tablosu ile elle çalıştırır; sınır durumlarını sınar ve hataları bulup düzeltir.
13. Bir problemi çözen farklı yaklaşımları karşılaştırır ve çözümünü sadeleştirir.

## İçerik Planı

| Bölüm | Ana Konu | İlgili Çıktılar | Dosya |
|---|---|---|---|
| 1 | Algoritma Nedir? | 1, 2 | Topics/01-Algorithm-Basics.md |
| 2 | Sözde Kod ve Akış Şeması | 3, 4 | Topics/02-Pseudocode-And-Flowchart.md |
| 3 | Değişkenler, Veri Tipleri ve İşlemler | 5, 6 | Topics/03-Variables-Types-Operations.md |
| 4 | Karar Yapıları | 7 | Topics/04-Decision-Structures.md |
| 5 | Döngüler | 8 | Topics/05-Loops.md |
| 6 | Diziler | 9 | Topics/06-Arrays.md |
| 7 | İzleme ve Sınır Durumları | 12 | Topics/07-Tracing-And-Testing.md |
| 8 | Arama Algoritmaları | 10 | Topics/08-Search-Algorithms.md |
| 9 | Sıralama Algoritmaları | 11 | Topics/09-Sorting-Algorithms.md |
| 10 | Problem Çözme Atölyesi | 13 | Topics/10-Problem-Solving-Workshop.md |
| 11 | Genel Tekrar ve Yolun Devamı | tümü | Topics/11-Review-And-Continuation.md |

Bölümler arası bağımlılık: 1-2 temel gösterim; 3 veri ve işlem; 4-5 akış
denetimi; 6 çok verili işlem; 7 sınama becerisi; 8-9 temel algoritmalar;
10 bütünleştirme; 11 kapanış.

## Repo Konvansiyonları

- Kök klasör: `Data-Structures-Algorithms` (İngilizce).
- Bölüm dosyaları `Topics/` klasöründe.
- Dosya adları İngilizce, ASCII, iki haneli sıra numarasıyla başlar, en fazla üç sözcük, sözcükler tire ile ayrılır ve büyük harfle başlar.
- Her bölümün ilk başlığı (H1) Türkçe konu başlığıdır.
- README, bölüm başlığı (H3) altında gruplanmış bağlantı listesinden oluşur.
- Materyalde "Hafta" ifadesi kullanılmaz; bölümler "Bölüm N" biçiminde anılır.
- Hitap biçimi "sen" (bakınız Dil ve Üslup).
- Tarih biçimi: README alt bilgisinde "GG Ay YYYY" (örn. 15 Ekim 2026).

## Terminoloji Kararları

Her kavram için tek Türkçe terim kullanılır; İngilizce karşılık ilk geçişte
parantez içinde verilir ve sonra yalnızca Türkçe terim kullanılır.

| Türkçe terim | İngilizce karşılık |
|---|---|
| algoritma | algorithm |
| sözde kod | pseudocode |
| akış şeması | flowchart |
| izleme tablosu | trace table |
| değişken | variable |
| sabit | constant |
| veri tipi | data type |
| atama | assignment |
| dizi | array |
| indeks | index |
| karar yapısı | decision structure |
| koşul | condition |
| döngü | loop |
| sayılı döngü | counted loop |
| koşullu döngü | conditional loop |
| sayaç | counter |
| birikim değişkeni | accumulator |
| doğrusal arama | linear search |
| ikili arama | binary search |
| kabarcık sıralama | bubble sort |
| seçmeli sıralama | selection sort |
| sınır durumu | edge case |

## Sözde Kod Konvansiyonu

- Anahtar sözcükler Türkçe ve büyük harfle yazılır: `BAŞLA`, `BİTİR`, `OKU`, `YAZ`.
- Atama işlemi `=` ile yapılır: `değişken = değer` (örn. `toplam = 0`).
- Karşılaştırma işlemleri: `==` (eşit), `!=` (eşit değil), `<`, `>`, `<=`, `>=`.
- Atama (`=`) ile eşitlik karşılaştırması (`==`) birbirine karıştırılmamalıdır.
- Mantıksal bağlaçlar: `VE`, `VEYA`, `DEĞİL`.
- Yorumlar `#` ile başlar.
- Karar yapısı:

```pseudocode
EĞER koşul İSE
    ...
DEĞİLSE EĞER başkaKoşul İSE
    ...
DEĞİLSE
    ...
EĞER SONU
```

- Sayılı döngü:

```pseudocode
DÖNGÜ sayac = başlangıç'tan bitiş'e ADIM adım
    ...
DÖNGÜ SONU
```

- Koşullu döngü:

```pseudocode
DÖNGÜ koşul İKEN
    ...
DÖNGÜ SONU
```

- Bölüm girintisi dört boşluktur.
- Dizi oluşturma: `dizi = DİZİ(n)`; eleman erişimi `dizi[indeks]`; indeksler 0'dan başlar (geçerli aralık 0..n-1).
- Değişken adları küçük harfle başlar, boşluk içermez ve ne sakladığını anlatır; adlarda Türkçe'ye özgü harfler yerine sade karşılıkları kullanılır (örn. `ogrenciNotu`, `kisaKenar`).
- Her anahtar sözcük, onu öğreten bölümde tanıtılır; bölümlerde yeni anahtar sözcük icat edilmez.

## Dil ve Üslup

- İçerik Türkiye Türkçesiyle ve "sen" hitabıyla yazılır.
- Ton: akademik + açık + samimi + açıklayıcı.
- Gereksiz resmî, çeviri kokan veya bürokratik ifadelerden kaçınılır.
- Her metin üretiminden sonra Türkçe dil incelemesi ve yabancı karakter taraması yapılır.

## Pedagojik Yaklaşım

- Ders türü algoritma ve problem çözme olduğu için akış: problem -> problemi anlama -> elle örnek -> çözüm fikri -> algoritma adımları -> sözde kod -> akış şeması -> izleme tablosuyla elle çalıştırma -> test ve sınır durumları -> bağımsız problem.
- Öğrenci çözümü görmeden önce problemi düşünür ve elle dener.
- Kavramların ardından sözde kod ve onun akış şeması birlikte verilir; Bölüm 3'ten itibaren her ana sözde kodun bir akış şeması bulunur.
- Her bölüm bağımsız çalışmaya elverişlidir; ancak her bölüm bir cümleyle kursun akışı içindeki yerini belirtir.
- Cevaplar soruların altına yazılmaz; açılır `<details>` bloğunda verilir.

## Görsel ve Biçim Konvansiyonları

- Akış şemaları ve süreç gösterimleri Mermaid ile çizilir; ASCII ile şema çizilmez.
- Mermaid düğüm etiketleri çift tırnak içinde ve doğru Türkçe karakterlerle yazılır.
- Akış şeması sembolleri şu Mermaid biçimleriyle çizilir: başlangıç/bitiş oval `([...])`; işlem dikdörtgen `[...]`; giriş/çıkış (`OKU`/`YAZ`) paralel kenar `[/.../]`; karar eşkenar dörtgen `{...}`; döngü altıgen `{{...}}`; akış yönü oklarla.
- Döngüler akış şemasında altıgenle gösterilir. Sayılı döngüde altıgen, sayacın hazırlığını ve döngü aralığını taşır (örn. `{{"i = 0'dan n-1'e kadar"}}`); gövde altıgenden çıkar ve sonunda tekrar altıgene dönen bir okla "tekrar et" anlamı verilir. Koşullu döngüde altıgen, döngü koşulunu taşır (örn. `{{"koşul sağlandığı sürece"}}`).
- Bölüm 3'ten itibaren her ana sözde kod örneğinin bir akış şeması vardır; şema, ilgili sözde kodun hemen ardında ya da 🗺️ Akış Şeması bölümünde aynı sırayla verilir.
- Gerçek dünyadan bir nesne veya sahne kavramı somutlaştırıyorsa, teorik bölümlerde "GÖRSEL ÖNERİSİ" yer tutucusu kullanılabilir.
- Görseller `Assets/` klasöründe tutulur; klasör ilk görsel eklendiğinde oluşturulur.
- GitHub uyarı blokları (NOTE, TIP, IMPORTANT, WARNING, CAUTION) amacına uygun ve ölçülü kullanılır.
- Emoji yalnızca başlıklarda, başlık başına en fazla bir tane kullanılır.

## İçerik Şablonu

Aşağıdaki iskelet her bölümde uygulanır. Zorunlu bölümler her bölümde bulunur;
isteğe bağlı bölümler yalnızca ilgili içerik gerektirdiğinde açılır ve
doldurulmak için zorlanmaz.

```markdown
# Bölüm Başlığı

## 🎯 Bu Bölümde Ne Öğreneceksin?   [zorunlu]
## 💡 Neden Önemli?   [zorunlu]
## 🔗 Ön Bilgi   [isteğe bağlı: önceki bölümlerden bilgi gerektiğinde]
## ❓ Problem   [zorunlu]
## 🤔 Birlikte Düşünelim   [zorunlu]
## 🧭 Çözüm Fikri   [zorunlu]
## 🪜 Algoritmanın Adımları   [isteğe bağlı: çok adımlı çözümlerde]
## 📝 Sözde Kod   [zorunlu: Bölüm 2 ve sonrası; Bölüm 1'de yok]
## 🗺️ Akış Şeması   [zorunlu: Bölüm 3 ve sonrası; her ana sözde kod için]
## ⏱️ Elle Çalıştıralım   [zorunlu]
## ⚠️ Bir Şeyler Ters Giderse   [isteğe bağlı: anlamlı hata senaryosu varsa]
## ✍️ Kendin Dene   [zorunlu]
## 🎓 Öğrendiklerini Kontrol Et   [zorunlu]
## 🚀 Bağımsız Çalışma   [zorunlu]
## 📖 Daha Fazlasını Öğrenmek   [zorunlu]
## 📌 Kısa Özet   [zorunlu]

---
[Geri: Önceki bölüm başlığı](NN-Onceki-Dosya.md) | [İleri: Sonraki bölüm başlığı](NN-Sonraki-Dosya.md)
```

Bölüm başlığı emoji seti:

| Bölüm | Emoji |
|---|---|
| Bu Bölümde Ne Öğreneceksin? | 🎯 |
| Neden Önemli? | 💡 |
| Ön Bilgi | 🔗 |
| Problem | ❓ |
| Birlikte Düşünelim | 🤔 |
| Çözüm Fikri | 🧭 |
| Algoritmanın Adımları | 🪜 |
| Sözde Kod | 📝 |
| Akış Şeması | 🗺️ |
| Elle Çalıştıralım | ⏱️ |
| Bir Şeyler Ters Giderse | ⚠️ |
| Kendin Dene | ✍️ |
| Öğrendiklerini Kontrol Et | 🎓 |
| Bağımsız Çalışma | 🚀 |
| Daha Fazlasını Öğrenmek | 📖 |
| Kısa Özet | 📌 |

Kurallar:

- Yapay zekâ görsellerinin üslubu: "düz vektör çizim, yumuşak pastel renkler, açık arka plan".
- Görsel yer tutucuları teorik bölümlerde, bir kavramı somutlaştırdığında kullanılır; Mermaid ile çizilebilecek şeyler için konmaz.
- Bölüm başlığı emojileri README emojileriyle çakışmayacak biçimde seçilmiştir; bir emoji hiçbir yerde farklı anlam taşımaz.
- Bölüm sonunda önceki ve sonraki bölüme bağlantı verilir; ilk ve son bölümde eksik yön bağlantısı yazılmaz.
- İzleme tablosu (trace table) Bölüm 7'de öğretilir; ondan önceki bölümlerde elle çalıştırma basit adım izleme biçiminde yapılır.
- Akış şeması sembolleri "Görsel ve Biçim Konvansiyonları" bölümünde tanımlandığı gibi çizilir: oval (başlangıç/bitiş), dikdörtgen (işlem), paralel kenar (giriş/çıkış), eşkenar dörtgen (karar), altıgen (döngü).

## İçerik Durumu

- [x] Kurs profili
- [x] Öğrenme çıktıları
- [x] İçerik planı
- [x] Repo yapısı
- [x] İçerik şablonu
- [x] Bölüm 01
- [x] Bölüm 02
- [x] Bölüm 03
- [x] Bölüm 04
- [x] Bölüm 05
- [x] Bölüm 06
- [x] Bölüm 07
- [x] Bölüm 08
- [x] Bölüm 09
- [x] Bölüm 10
- [x] Bölüm 11
