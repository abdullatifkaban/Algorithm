# Algoritma Nedir?

## 🎯 Bu Bölümde Ne Öğreneceksin?

- Algoritmanın ne olduğunu ve neden gerekli olduğunu açıklayacaksın.
- Günlük hayattan bir işi sıralı ve açık adımlara dönüştüreceksin.
- İyi bir algoritmanın taşıması gereken özellikleri fark edeceksin.
- Bir problemde girdiyi, çıktıyı ve ara adımları belirleyeceksin.

## 💡 Neden Önemli?

Bilgisayarlar çok hızlıdır ama hiçbir şeyi kendiliğinden bilmez. Ne yapacaklarını
onlara biz söyleriz. İşte bu yüzden işin zor kısmı bilgisayarda değil, insanda:
doğru adımları doğru sırayla düşünmekte. Algoritma, tam da bu düşünme işidir.

Algoritmalar yalnızca bilgisayarlara özgü değildir. Bir yemek tarifi, bir
mobilyanın kurulum kılavuzu, bir bankamatikten para çekme işlemi, telefonundaki
navigasyon: hepsi aslında birer algoritmadır. Bu ders boyunca kod yazmayacağız.
Önce işi adımlara ayırmayı, yani planlamayı öğreneceğiz. Programlama dilleri ise
bu planı bilgisayara yazmanın yollarından sadece biridir.

> [!IMPORTANT]
> Algoritma bir kod değildir. Algoritma, bir işin nasıl yapılacağını anlatan
> plandır. Aynı algoritmayı farklı dillerde yazabilir ya da hiç kod yazmadan
> yalnızca kelimelerle anlatabilirsin.

## ❓ Problem

Bir arkadaşın şehre yeni taşındı ve çevreyi hiç bilmiyor. Sen ise bulunduğun
yerden en yakın eczaneye nasıl gidileceğini çok iyi biliyorsun. Arkadaşın
yanında olamayacaksın; ona yol tarifini yazılı olarak bırakman gerekiyor. Yani
tarifini okuyan kişi sana hiçbir soru soramayacak.

Şimdi düşün: Bu tarifi nasıl yazarsın? Tarif eksik ya da belirsiz olursa
arkadaşının başına ne gelir? Cevabını vermeden önce bir dakika dur ve kendi
tarifini zihninde kur.

## 🤔 Birlikte Düşünelim

Aynı yol için iki farklı tarif yazıldığını düşünelim.

**Tarif A:**

> Biraz ilerle, sonra sağa dön. Eczane oralarda bir yerde.

**Tarif B:**

> Ana kapıdan çık. 200 metre düz yürü. Benzin istasyonunu geçince ilk sokaktan
> sağa dön. Yaklaşık 50 metre sonra eczane solunda kalır.

Sence hangisi daha iyi bir tarif? Neden? Cevabını kendi kelimelerinle bir yere
yazmadan devam etme.

Şimdi birlikte bakalım. Tarif A'da "biraz" ne kadar bir mesafedir? Hangi sağa
dönüş kastediliyor; ilk sokak mı, ikinci mi? "Oralarda bir yerde" ifadesi
eczanenin yerini kesin olarak söylemiyor. Bu tarifi uygulayan kişi büyük
olasılıkla yolunu kaybeder; üstelik yanlış gittiğini de hemen anlayamaz.

Tarif B'de ise her adım ölçülü ve nettir: kaç metre, hangi sokağa, hangi yöne.
Tarifi okuyan kişi, o bölgeyi hiç bilmese bile aynı yolu izleyip aynı yere
varır.

Buradan önemli bir ders çıkar: Bir işi başkasına aktarırken onun, senin
bildiklerini bilmediğini varsaymalısın.

> [!TIP]
> Bir algoritma yazarken kendini, o işi hiç bilmeyen birinin yerine koy. Adımı
> okuyan kişi "acaba ne demek istedi?" diye duruyorsa, o adım yeterince açık
> değildir.

![Elindeki yazılı yol tarifini takip ederek yürüyen bir kişi](../Assets/01-Following-Directions.jpeg)

## 🧭 Çözüm Fikri

Az önce yaptığımız şeyin adı bir algoritma yazmaktı. Şimdi bu kavramı tanımlayalım.

**Algoritma:** Bir problemi çözmek ya da bir işi tamamlamak için izlenen,
sınırlı sayıda ve belirli bir sıraya sahip açık adımlar kümesidir.

Bir algoritma çalışırken hep aynı kalıbı izler: elinde bir başlangıç bilgisi
vardır, adımlar bu bilgiyi işler ve sonunda bir sonuç ortaya çıkar.

```text
Girdi  ->  Algoritma  ->  Çıktı
```

- **Girdi (input):** İşe başlarken elimizde olan bilgi.
- **Çıktı (output):** Adımlar sonunda elde etmek istediğimiz sonuç.

Yol tarifi örneğinde girdi, kişinin başlangıç noktası ve tarifiniz; çıktı ise
kişinin eczaneye ulaşmasıdır.

İyi bir algoritmanın taşıması gereken beş temel özellik şunlardır:

| Özellik | Ne demek? | Kötü örnek |
|---|---|---|
| Açıklık | Her adım tek anlamlı olmalı, iki farklı şekilde anlaşılmamalı. | "Biraz tuz ekle." |
| Belirlilik | Aynı girdiyle her zaman aynı sonuç alınmalı; adımların nasıl yapılacağı belli olmalı. | "Uygun bir sıcaklıkta pişir." |
| Sonluluk | Adımlar bir yerde bitmeli; sonsuza kadar sürmemeli. | "Ta ki hamur istediğin kıvama gelene kadar yoğur." (durma koşulu belirsiz) |
| Girdi | Algoritmanın başlaması için gerekli bilgi tanımlı olmalı. | Malzemeleri hiç saymadan yemek tarifi vermek |
| Çıktı | Sonunda elde edilecek sonuç belli olmalı. | "Bir şeyler yap, ne olursa olsun." |

Bu özelliklerden ikisini biraz açalım.

**Açıklık ve belirlilik karıştırılabilir.** Açıklık, adımın *okuyan için net*
olmasıdır. Belirlilik ise adımın *her seferinde aynı sonucu vermesidir*. "Biraz
tuz ekle" adımı hem açık değildir hem de belirli değildir: bir kişi bir tutam,
başka bir kişi bir kaşık ekleyebilir.

**Sonluluk, pratikte en çok atlanan özelliktir.** Bir algoritma, işi
bitireceği koşulu mutlaka söylemelidir. Aksi hâlde adımlar bir noktada
durmayabilir.

Yaygın bir yanlış inanış, algoritmanın yalnızca matematik veya bilgisayarla
ilgili olduğudur. Oysa az önce gördüğün gibi bir yol tarifi de bir algoritmadır.
Önemli olan, işin adımlara ayrılabilir olmasıdır.

## 🪜 Algoritmanın Adımları

Bir problemle karşılaştığında onu algoritmaya dönüştürmek için şu yolu izleyebilirsin:

1. **Problemi anla.** Senden tam olarak ne isteniyor? Sonuç ne olmalı?
2. **Girdiyi ve çıktıyı belirle.** Elinde başlangıçta ne var, sonunda ne olmalı?
3. **İşi küçük adımlara böl.** Her adım tek bir iş yapsın.
4. **Adımları doğru sıraya koy.** Sıra değişirse sonuç da değişebilir.
5. **Kontrol et.** Her adım açık mı? Eksik ya da gereksiz adım var mı? Özel
   durumlarda (örneğin hiç veri olmaması) ne oluyor?

Bu beş adım, bu dersin geri kalanında sürekli kullanacağın bir yöntemdir. Yeni
bir problem gördüğünde önce bu listeye dön.

## ⏱️ Elle Çalıştıralım

Şimdi bir algoritmayı elle çalıştıralım. Elimizde, iki kartta yazan sayılardan
büyük olanı bulan bir algoritma olsun.

```text
1. İki kartı da oku.
2. Birinci karttaki sayıyı aklında tut.
3. İkinci karttaki sayıya bak.
4. İkinci sayı, aklında tuttuğun sayıdan büyükse aklındakini ikinci sayı yap.
5. Aklındaki sayıyı sonuç olarak yaz ve dur.
```

Bu algoritmayı (7 ve 3) sayılarıyla adım adım izleyelim:

| Adım | Ne oluyor? | Aklındaki sayı |
|---|---|---|
| 2 | Birinci kart 7 olduğu için aklında 7 var. | 7 |
| 3 | İkinci kart 3. | 7 |
| 4 | 3, 7'den büyük değil; bir şey değişmiyor. | 7 |
| 5 | Sonuç yazılır. | 7 |

Şimdi aynı algoritmayı (4 ve 9) ile çalıştıralım:

| Adım | Ne oluyor? | Aklındaki sayı |
|---|---|---|
| 2 | Birinci kart 4 olduğu için aklında 4 var. | 4 |
| 3 | İkinci kart 9. | 4 |
| 4 | 9, 4'ten büyük; aklındaki sayı 9 olur. | 9 |
| 5 | Sonuç yazılır. | 9 |

Elle çalıştırma sayesinde algoritmanın iki farklı durumda da doğru sonucu
verdiğini gördük.

Şimdi 4. adımı bilinçli olarak çıkaralım. O zaman algoritma her seferinde
birinci karttaki sayıyı yazar; (4 ve 9) örneğinde sonuç yanlışlıkla 4 olur. Tek
bir adımın eksikliği, algoritmayı tamamen bozabilir. Bu yüzden bir algoritmayı
yazdıktan sonra mutlaka örneklerle elle çalıştırmalısın.

## ⚠️ Bir Şeyler Ters Giderse

**Belirti:** Algoritma senin verdiğin örnekte doğru çalışıyor, ama başka bir
örnekte yanlış sonuç veriyor.

**Olası neden:** Adımlardan biri belirsiz ya da eksik yazılmıştır.

**Ne yapmalısın?** Algoritmayı farklı bir girdiyle yeniden elle çalıştır. Sonuç
beklediğinden farklı çıktığı adımı bul. Çoğu zaman sorun, "eşitlik durumu"
(iki sayı eşitse ne olacak?) gibi düşünmediğin bir durumda saklıdır. O durumu
da açıkça yazacak şekilde adımı düzelt.

## ✍️ Kendin Dene

**1.** Sabah evden çıkıp işe ya da okula gitme işini, en az altı adımlık bir
algoritmaya dönüştür. Her adım açık olmalı.

**2.** Aşağıdaki adımlardan hangisi "açıklık" özelliğini ihlal eder? Neden?

```text
1. Fırını 180 derecede ısıt.
2. Hamuru biraz yoğur.
3. Kek kalıbını yağla.
```

**3.** Şu problem için girdiyi ve çıktıyı belirle: "Bir metindeki sesli harfleri
saymak."

<details>
<summary>İpucu</summary>

1. Adımları yazarken "nasıl" sorusunu sor: "Nasıl gidiyorum? Hangi araçla?
Ne kadar sürüyor?"
2. "Biraz" gibi ölçüsüz kelimeleri ara.
3. Girdi, işe başlarken elinde olan şeydir; çıktı ise sonunda elde ettiğindir.

</details>

<details>
<summary>Çözümleri göster</summary>

1. Örnek bir cevap: (a) Kalk, (b) yüzünü yıka, (c) giyin, (d) kahvaltı yap,
(e) çantana gerekli malzemeleri koy, (f) evden çık, (g) durağa yürü, (h) uygun
otobüse bin. Her adım tek bir iş yapar ve nettir.

2. İkinci adım ("Hamuru biraz yoğur") açıklık kuralını ihlal eder. "Biraz"
kelimesi ölçüsüzdür; ne kadar yoğurulacağı belirsizdir. "Hamuru 5 dakika yoğur"
gibi ölçülü bir ifade açık olur.

3. Girdi: metin. Çıktı: metindeki sesli harf sayısı (bir sayı). Ara adımlar
metnin harflerini tek tek inceleyip sesli olanları saymaktır.

</details>

## 🎓 Öğrendiklerini Kontrol Et

**1.** Algoritmayı kendi cümlelerinle tanımla.

**2.** Algoritmanın "sonluluk" özelliği ne anlama gelir? Sonlanmayan bir örnek
düşünebilir misin?

**3.** Bir yemek tarifindeki "tuzu damak tadına göre ayarla" ifadesi hangi
özelliği zorlar? Bunu nasıl düzeltirsin?

**4.** Girdi ile çıktı arasındaki farkı, kendi seçtiğin bir örnekle açıkla.

<details>
<summary>Cevapları göster</summary>

1. Algoritma; bir problemi çözmek için izlenen, açık, belirli ve sonlu
adımlardan oluşan bir plandır. Adımlar bir girdiyi işleyip bir çıktı üretir.

2. Sonluluk, adımların bir noktada bitmesi gerektiğidir. "Kilo 70'in altına
düşene kadar koş" gibi durma koşulu belirsiz bir yönerge sonsuza kadar
sürebilir; bu yüzden sonluluk özelliğini ihlal eder.

3. Açıklık ve belirlilik özelliklerini zorlar; çünkü "damak tadına göre"
kişiden kişiye değişir. "Yarım çay kaşığı tuz ekle" gibi ölçülü bir ifade
düzeltir.

4. Örneğin bir hesap makinesi için girdi, girilen iki sayıdır; çıktı ise
bunların toplamıdır. Girdi, işin başında elimizde olandır; çıktı, işlem
sonucunda elde ettiğimizdir.

</details>

## 🚀 Bağımsız Çalışma

Günlük hayatında sık yaptığın bir işi seç (örneğin çamaşır yıkama, markette
ödeme sırası seçme veya bir oyunun adım sırası). Bu işi bir algoritmaya
dönüştür. Sonra bilinçli bir deney yap: adımlardan birini çıkar ya da sırasını
değiştir. Ne olacağını önce tahmin et, sonra tahminini gözden geçir. Hangi
adımın gerçekten gerekli olduğunu bu şekilde fark edebilirsin.

## 📖 Daha Fazlasını Öğrenmek

- "Algoritma" sözcüğü, 9. yüzyılda yaşamış matematikçi El-Harezmî'nin
  (al-Khwarizmi) adından gelir. Birçok dilde algoritma karşılığı bu isimden
  türemiştir.
- Türkçe Vikipedi'nin "Algoritma" maddesi, kavramın tanımına ve tarihine kısa
  bir bakış sunar.
- Çevrendeki kılavuzları (mobilya kurulumu, yemek tarifi) birer algoritma
  gözüyle okumayı dene; hangi adımların açık ya da belirsiz olduğunu ara.

## 📌 Kısa Özet

- Algoritma, bir problemi çözen; açık, belirli ve sonlu adımlardan oluşan bir
  plandır.
- Her algoritmanın bir girdisi ve bir çıktısı vardır: girdi, algoritma, çıktı.
- İyi bir algoritmanın özellikleri: açıklık, belirlilik, sonluluk, girdi ve
  çıktı.
- Algoritma bir kod değildir; kod, algoritmayı yazmanın araçlarından biridir.
- Bir problemi algoritmaya dönüştürmenin yolu: anla, girdiyi ve çıktıyı belirle,
  adımlara böl, sırala, kontrol et.
- Bir sonraki bölümde, yazdığın adımları sözde kod ve akış şemasıyla
  göstermeyi öğreneceksin.

---
[İleri: Sözde Kod ve Akış Şeması](02-Pseudocode-And-Flowchart.md)
