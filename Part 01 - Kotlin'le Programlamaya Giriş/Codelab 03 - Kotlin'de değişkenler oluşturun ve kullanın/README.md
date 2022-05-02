# Kotlin'de değişkenler oluşturun ve kullanın


### Konu Başlıkları:

📌  [Değişkenler ve veri türleri](#1) <br>
📌  [Değişkenleri tanımlayın ve kullanın](#2) <br>
📌  [Bir Fonksiyonun Parçaları](#3) <br>
📌  [Programınızı değiştirin](#4) <br>
📌  [Kotlin stil rehberi](#5) <br>
📌  [Kodunuzdaki hataları düzeltin](#6) <br>

#

# <a name="1"></a>Değişkenler ve veri türleri

Bilgisayar programlamasında, tek bir veri parçası için bir kap olan bir değişken kavramı vardır. Bir değer içeren bir kutu olarak tasavvur edebilirsiniz. Kutu, değişkenin adı olan bir etikete sahiptir. Kutuya adıyla atıfta bulunarak, sahip olduğu değere erişebilirsiniz.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166337582-c3b85a74-0cf5-4aa2-9177-7f94d38a1f37.png" />
</p>

Değeri doğrudan kullanmak varken neden değeri bir kutuda saklayıp kutuya adıyla başvuruda bulunasınız ki? Sorun şu ki, kodunuz tüm talimatlarda değerleri doğrudan kullandığında, programınız yalnızca bu özel durum için çalışacaktır.

İşte değişkenlerin neden yararlı olduğunu anlamayı kolaylaştırabilecek bir benzetme. Aşağıda yeni tanıştığınız birine bir mektup var.

```
Sevgili Lauren,

Bugün ofiste seninle tanışmak harikaydı. Cuma günü seni görmek için sabırsızlanıyorum.

İyi günler!

Bu mektup harika, ama sadece Lauren ile olan özel durumunuz için işe yarıyor.
Ya kendinizi aynı mektubu birçok kez yazarken bulursanız, ancak farklı insanlar için küçük farklılıklar olsa?
Değişebilecek kısımlar için boşluk bırakarak tek harfli bir şablon oluşturmak daha verimli olacaktır.

Sayın ____ ,

Bugün _____'de sizinle tanışmak harikaydı. ____'da görüşmek dileğiyle.

İyi günler!

Ayrıca her boş alana girecek bilgi türünü de belirleyebilirsiniz. Bu, mektup şablonunun beklediğiniz
gibi kullanılmasını sağlar.

Sayın {isim},

Bugün sizinle {konum} adresinde tanışmak harikaydı. {date } tarihinde görüşmek için sabırsızlanıyorum.

İyi günler!

Kavramsal olarak, bir uygulama oluşturmak benzerdir. Uygulamanın diğer kısımları aynı kalırken,
bazı veriler için yer tutucularınız var.

```

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166338031-4be145b6-4cc9-4b87-8fb7-8e887c8e3918.png" />
</p>

Bir haber uygulamasının yukarıdaki çiziminde, "Hoş Geldiniz" metni, "Sizin için en son haberler" başlığı ve "Daha fazla makale görüntüle" düğmesi metni her zaman aynı kalır. Tersine, kullanıcının adı ve her makalenin içeriği değişecektir, bu nedenle bu, her bir bilgiyi tutmak için değişkenleri kullanmak için harika bir fırsat olacaktır.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166338188-7ceb7a11-0234-4f52-9f05-15fac9cb26ec.png" />
</p>

Kodu (veya talimatları) yalnızca Alex adlı bir kullanıcı için veya her zaman aynı başlık ve yayın tarihine sahip bir haber makalesi için çalışacak şekilde haber uygulamanıza yazmak istemezsiniz. Bunun yerine, daha esnek bir uygulama istiyorsunuz, bu nedenle kodunuzu name, makale1Name, makale1Tarihi vb. gibi değişken adlarına başvurarak yazmalısınız. Ardından kodunuz, kullanıcı adının farklı olabileceği ve makale ayrıntılarının farklı olabileceği birçok farklı kullanım durumu için çalışacak kadar genel hale gelir.

### Değişkenlerle örnek uygulama

Değişkenleri nerede kullanabileceğini görmek için bir uygulama örneğine bakalım.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166338363-a824c06e-c528-40d5-bd5f-dd45f0626b34.png" />
</p>

Bir harita uygulamasında, restoran veya işletme gibi her konum için bir ayrıntı ekranı bulabilirsiniz. Google Haritalar uygulamasından alınan yukarıdaki ekran görüntüsü, Googleplex olarak adlandırılan Google'ın şirket merkezinin ayrıntılarını göstermektedir. Uygulamada hangi verilerin değişken olarak saklandığını düşünüyorsunuz?

- Konumun adı
- Konumun yıldız derecelendirmesi
- Konumla ilgili inceleme sayısı
- Kullanıcının bu konumu kaydedip kaydetmediği (veya işaretlediği)
- konumun adresi
- Konum açıklaması

Bu değişkenlerde depolanan verileri değiştirin ve diğer konumların ayrıntılarını da gösterecek kadar esnek bir harita uygulamanız olur.

### Veri tipleri

Uygulamanızın hangi yönlerinin değişken olabileceğine karar verdiğinizde, bu değişkenlerde ne tür verilerin depolanabileceğini belirtmek önemlidir. Kotlin'de bazı ortak temel veri türleri vardır. Aşağıdaki tablo, her satırda farklı bir veri türünü göstermektedir. Her veri türü için, ne tür verileri tutabileceğinin bir açıklaması ve örnek değerler vardır.

| Kotlin veri türleri | Ne tür veriler içerebilir |Örnek değerler |
|:---------------:|---------------| :------------------:|
|String|Text|"Add contact"<br> "Search"<br> "Sign in"|
|Int|Bütün tam sayılar|32<br> 1293490<br> -59281|
|Double|Ondalık sayılar |2.0<br> 501.0292<br> -31723.99999|
|Float|Ondalık sayı (Double'dan daha az kesindir). Numaranın sonunda f veya F vardır.|5.0f<br> -1630.209f<br> 1.2940278F|
|Boolean|doğru ya da yanlış. Yalnızca iki olası değer olduğunda bu veri türünü kullanın. Kotlin'de true ve false anahtar kelimeler olduğuna dikkat edin.|true<br> false|

> Not: Sayısal veri türleri (Int, Double ve Float) için geçerli aralıklar için, Sayılar. Double ve Float arasındaki farkla ilgili ayrıntılar için, iki veri türünü karşılaştıran bu tabloya bakın.

Artık bazı yaygın Kotlin veri türlerinin farkında olduğunuza göre, daha önce gördüğünüz konum ayrıntısı sayfasında tanımlanan değişkenlerin her biri için hangi veri türü uygun olur?

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166339651-2d6cf8a7-3f55-4066-9a9c-179ff3501d18.png" />
</p>

- Konumun adı metindir, bu nedenle veri türü `String` olan bir değişkende saklanabilir.
- Konumun yıldız derecelendirmesi, ondalık bir sayıdır (4,2 yıldız gibi), bu nedenle `Double` olarak saklanabilir.
- Konumun inceleme sayısı bir tam sayıdır, bu nedenle `Int`.
- Kullanıcının bu konumu kaydedip kaydetmediği yalnızca iki olası değere sahiptir (kaydedilmiş veya kaydedilmemiş), bu nedenle doğru ve yanlışın bu durumların her birini temsil edebileceği bir `Boolean` olarak depolanır.
- Konumun adresi metindir, bu nedenle bir `String` olmalıdır.
- Konumun açıklaması da metindir, bu nedenle bir `String` olmalıdır.

Aşağıdaki iki senaryo üzerinde daha pratik yapın. Aşağıdaki uygulamalarda değişkenlerin kullanımını ve veri türlerini tanımlayın.

YouTube uygulaması gibi video izlemeye yönelik bir uygulamada bir video ayrıntıları ekranı vardır. Değişkenler büyük olasılıkla nerede kullanılır? Bu değişkenlerin veri türü nedir?

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166339958-f8b1a3b5-bdb1-4a39-91ab-2051c0700d1d.png" />
</p>

Tek bir doğru cevap yok, ancak bir video izleme uygulamasında, aşağıdaki veri parçaları için değişkenler kullanılabilir:

- Videonun adı (`String`)
- Kanalın adı (`String`)
- Videonun izlenme sayısı (`Int`)
- Videodaki beğeni sayısı (`Int`)
- Videodaki yorum sayısı (`Int`)

Gmail gibi bir e-posta uygulamasında, gelen kutusu ekranı, alınan en son e-posta mesajlarını listeler. Değişkenler büyük olasılıkla nerede kullanılır? Bu değişkenlerin veri türü nedir?

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166340145-9d9c35e5-fb7b-47c7-ad31-cb24d3f7db57.png" />
</p>

Yine, tek bir doğru cevap yok. Bir e-posta uygulamasında, aşağıdaki veri parçaları için değişkenler kullanılabilir:

- Gönderenin adı (`String`)
- E-postanın konusu (`String`)
- E-postanın yıldızlı olup olmadığı (`Boolean`)
- Gelen kutusundaki yeni e-posta sayısı (`Int`)

### Sen de Dene

1. Telefonunuzda en sevdiğiniz uygulamayı açın.
2. Söz konusu ekranda, uygulamada değişkenlerin nerede kullanıldığını düşündüğünüzü belirleyin.
3. Bu değişkenlerin hangi veri türü olduğunu tahmin edin.
4. Yanıtlarınızı uygulamanın ekran görüntüsü, değişkenlerin nerede kullanıldığını düşündüğünüzün bir açıklaması ve #AndroidBasics etiketiyle sosyal medyada paylaşın.

Şimdiye kadar bu codelab'de harika iş çıkardınız! Kodunuzda değişkenlerin ve veri türlerinin nasıl kullanıldığı hakkında daha fazla bilgi edinmek için sonraki bölüme geçin.

# <a name="2"></a>Değişkenleri tanımlayın ve kullanın








