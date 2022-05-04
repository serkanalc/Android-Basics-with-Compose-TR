# Kotlin'de değişkenler oluşturun ve kullanın


### Konu Başlıkları:


📌  [Başlamadan Önce](https://github.com/serkanalc/Android-Basics-with-Compose-TR/blob/main/Part%2001%20-%20Kotlin'le%20Programlamaya%20Giri%C5%9F/Codelab%2003%20-%20Kotlin'de%20de%C4%9Fi%C5%9Fkenler%20olu%C5%9Fturun%20ve%20kullan%C4%B1n/Ba%C5%9Flamadan%20%C3%96nce.md) <br>
📌  [Değişkenler ve veri türleri](#1) <br>
📌  [Değişkenleri tanımlayın ve kullanın](#2) <br>
📌  [Değişkenleri güncelleyin](#3) <br>
📌  [Diğer veri türlerini keşfedin](#4) <br>
📌  [Kodlama kuralları](#5) <br>
📌  [Kodunuzda yorum yapma](#6) <br>



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

### Tanımlamaya karşı değişken kullanımı

Değişkeni kullanmadan önce kodunuzda bir değişken tanımlamanız gerekir. Bu, işlevleri çağırmadan önce tanımlama hakkında son kod laboratuvarında öğrendiklerinize benzer.

Bir değişken tanımladığınızda, onu benzersiz bir şekilde tanımlamak için bir ad atarsınız. Ayrıca veri türünü belirterek ne tür verileri tutabileceğine de karar verebilirsiniz. Son olarak, değişkende saklanacak bir başlangı değeri sağlayabilirsiniz, ancak bu isteğe bağlıdır.

> Not: "declare a variable" alternatif ifadesini duyabilirsiniz. Declare ve tanımlamak kelimeleri birbirinin yerine kullanılabilir ve aynı anlama sahiptir. Bir değişkeni tanımlayan koda atıfta bulunan "variable definition" veya "variable declaration" terimini de duyabilirsiniz.

Bir değişken tanımladıktan sonra, o değişkeni programınızda kullanabilirsiniz. Bir değişken kullanmak için kodunuzdaki değişken adını yazın; bu, Kotlin derleyicisine kodun o noktasında değişkenin değerini kullanmak istediğinizi söyler.

Örneğin, bir kullanıcının gelen kutusundaki okunmamış mesajların sayısı için bir değişken tanımlayın. Değişken isim sayısına sahip olabilir. Kullanıcının gelen kutusundaki okunmamış 2 iletiyi temsil eden, değişkenin içinde 2 sayısı gibi bir değeri saklayın. (Değişkende saklamak için farklı bir sayı seçebilirsiniz, ancak bu örnek için 2 sayısını kullanın.)

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166447119-efa5dec9-6e2c-4c3c-9a24-97f1fc5848d0.png" />
</p>

Kodunuzun okunmamış mesaj sayısına erişmesi gerektiğinde, kodunuza count yazın. Komutlarınızı yürütürken, Kotlin derleyicisi kodunuzdaki değişken adını görür ve onun yerine değişken değerini kullanır.

Teknik olarak, bu süreci tanımlamak için daha spesifik kelime kelimeleri vardır:

İfade, değeri olan küçük bir kod birimidir. Bir ifade değişkenlerden, işlev çağrılarından ve daha fazlasından oluşabilir. Aşağıdaki durumda, ifade bir değişkenden oluşur: İfadenin değeri 2'dir.


<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166447410-4f520c03-293c-49a2-b150-38fc162e38ec.png" />
</p>

Evaluate, bir ifadenin değerini belirlemek anlamına gelir. Bu durumda ifade 2 olarak değerlendirilir. Derleyici koddaki ifadeleri değerlendirir ve programdaki talimatları yürütürken bu değerleri kullanır.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166447604-aaa52e03-f441-463d-bbbf-65fb4e8a28d5.png" />
</p>

Bu davranışı Kotlin Playground'da gözlemlemek için sonraki bölümdeki programı çalıştırın.

### Örnek

1. [Kotlin Playground](https://developer.android.com/training/kotlinplayground)'u bir web tarayıcısında açın.
2. Kotlin Playground'daki mevcut kodu aşağıdaki program ile değiştirin.

Bu program, başlangıç değeri 2 olan count adında bir değişken oluşturur ve bunu, count değişkeninin değerini çıktıya yazdırarak kullanır. Henüz kod sözdiziminin tüm yönlerini anlamadıysanız endişelenmeyin. İlerleyen bölümlerde daha detaylı anlatılacaktır.

```
fun main() {
    val count: Int = 2
    println(count)
}
```
3. Programı çalıştırın ve çıktı şöyle olmalıdır:

```
2
```

### Değişken declaration(bildirimi)

Çalıştırdığınız programda, ikinci kod satırı şöyle diyor:

```
val count: Int = 2
```
Bu ifade, 2 sayısını tutan count adında bir tamsayı değişkeni oluşturur.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166447119-efa5dec9-6e2c-4c3c-9a24-97f1fc5848d0.png" />
</p>

Kotlin'de bir değişken bildirmek için sözdizimini (veya biçimini) okumaya alışmak biraz zaman alabilir. Aşağıdaki şema, değişkenle ilgili her ayrıntının nerede olması gerektiği ile boşlukların ve sembollerin konumlarını gösterir.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166448832-d8c8eae7-b04c-476e-b42b-814458e018c2.png" />
</p>

Count değişkeni örneği bağlamında, değişken bildiriminin val kelimesiyle başladığını görebilirsiniz. Değişkenin adı count'tur. Veri türü Int ve başlangıç değeri 2'dir.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166448955-2c29bc04-306b-46a2-9308-113e48106399.png" />
</p>

Değişken bildiriminin her bir bölümü aşağıda daha ayrıntılı olarak açıklanmıştır.

### Yeni değişken tanımlamak için anahtar kelime

Yeni bir değişken tanımlamak için Kotlin'in val (value - değer anlamına gelen) anahtar sözcüğüyle başlayın. O zaman Kotlin derleyicisi bu ifadede bir değişken bildirimi olduğunu bilir.

### Değişken ismi

Bir fonksiyonu adlandırdığınız gibi, bir değişkeni de adlandırırsınız. Değişken bildiriminde, değişken adı val anahtar sözcüğünü takip eder.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166449310-bc575b2f-580c-4a28-b1ae-6ede668206e3.png" />
</p>

İstediğiniz herhangi bir değişken adını seçebilirsiniz, ancak en iyi uygulama, değişken adı olarak Kotlin anahtar kelimelerini kullanmaktan kaçının.

Kodunuzun daha kolay okunabilmesi için, değişkenin tuttuğu verileri açıklayan bir ad seçmek en iyisidir.

Değişken adları, fonksiyon adlarıyla öğrendiğiniz gibi, camel case(deve kılıfı) kuralına uymalıdır. Değişken adının ilk kelimesinin tamamı küçük harftir. İsimde birden fazla kelime varsa kelimeler arasında boşluk bırakılmaz ve diğer kelimeler büyük harfle başlamalıdır.

Örnek değişken isimleri:

- numberOfEmails
- cityName
- bookPublicationDate

Daha önce gösterilen kod örneği için, count değişkenin adıdır.

```
val count: Int = 2
```
### Değişken data type (veri türü)

Değişken adından sonra iki nokta üst üste, boşluk ve ardından değişkenin veri türünü eklersiniz. Daha önce belirtildiği gibi, String, Int, Double, Float ve Boolean, temel Kotlin veri türlerinden bazılarıdır. Bu kursun ilerleyen bölümlerinde daha fazla veri türü öğreneceksiniz. Veri türlerini tam olarak gösterildiği gibi yazmayı ve her birine büyük harfle başlamayı unutmayın.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166449808-8a308315-5007-4e5c-be38-427bc3051a55.png" />
</p>

Count değişkeni örneği için Int, değişkenin veri türüdür.

```
val count: Int = 2
```

### Atama operatörü

Değişken bildiriminde, eşittir simgesi (=) veri türünü takip eder. Eşittir işareti sembolüne atama operatörü denir. Atama operatörü, değişkene bir değer atar. Başka bir deyişle, eşittir işaretinin sağ tarafındaki değer, eşittir işaretinin sol tarafındaki değişkende saklanır.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166450145-4dfcd7cf-8ab5-4342-b6b1-807fe4bf7b4b.png" />
</p>

### Değişken başlangıç değeri

Değişken değeri, değişkende depolanan gerçek verilerdir.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166450338-d7618a9c-1fc7-474c-9983-9789a7964a02.png" />
</p>

Sayı değişkeni örneğinde, 2 sayısı değişkenin başlangıç değeridir.

```
val count: Int = 2
```

Şu ifadeyi de duyabilirsiniz: "the count variable is initialized to 2." Bu, değişken bildirildiğinde değişkende depolanan ilk değerin 2 olduğu anlamına gelir.

İlk değer, değişken için bildirilen veri türüne bağlı olarak farklı olacaktır.

Codelab'de daha önce tanıyabileceğiniz aşağıdaki tabloya bakın. Üçüncü sütun, karşılık gelen her türden bir değişkende saklanabilecek örnek değerleri gösterir. Bu değerler, fixed veya constant değerler olduklarından (değer sürekli aynıdır) değişmez olarak adlandırılır. Örnek olarak, 32 tamsayısı her zaman 32 değerine sahip olacaktır. Buna karşılık, bir değişken, değeri değişebileceği için değişmez değildir. Türlerine göre şu değişmez değerlerden söz edildiğini duyabilirsiniz: dize değişmezi, tamsayı değişmezi, boolean değişmezi, vb.

| Kotlin veri türleri | Ne tür veriler içerebilir |Örnek değerler |
|:---------------:|---------------| :------------------:|
|String|Text|"Add contact"<br> "Search"<br> "Sign in"|
|Int|Bütün tam sayılar|32<br> 1293490<br> -59281|
|Double|Ondalık sayılar |2.0<br> 501.0292<br> -31723.99999|
|Float|Ondalık sayı (Double'dan daha az kesindir). Numaranın sonunda f veya F vardır.|5.0f<br> -1630.209f<br> 1.2940278F|
|Boolean|doğru ya da yanlış. Yalnızca iki olası değer olduğunda bu veri türünü kullanın. Kotlin'de true ve false anahtar kelimeler olduğuna dikkat edin.|true<br> false|

Değişkenin veri türüne göre uygun ve geçerli bir değer sağlamak önemlidir. Örneğin, Kotlin derleyicisi size bir hata vereceğinden, "Merhaba" gibi bir dize değişmezini Int türünde bir değişken içinde depolayamazsınız.

### Değişken kullanımı

Kotlin Playground'da çalıştırdığınız orijinal program aşağıdadır. Şimdiye kadar, ikinci kod satırının, sayısı 2 değerinde yeni bir tamsayı değişkeni oluşturduğunu öğrendiniz.

```
fun main() {
    val count: Int = 2
    println(count)
}
```
Şimdi üçüncü kod satırına bakın. Sayı değişkenini çıktıya yazdırıyorsunuz:

```
println(count)
```

Kelime sayısının etrafında tırnak işareti olmadığına dikkat edin. Bu bir değişken adıdır, bir string değişmezi değildir. (Kelime bir dize değişmezi olsaydı tırnak içinde bulurdunuz.) Programı çalıştırdığınızda, Kotlin derleyicisi println() komutu için parantez içindeki ifadeyi sayar ve bu ifadeyi değerlendirir. İfade 2 olarak değerlendirildiğinden, girdi olarak 2 ile println() yöntemi çağrılır.

Dolayısıyla programın çıktısı:

```
2
```

Çıktıdaki sayı tek başına çok kullanışlı değildir. 2'nin neyi temsil ettiğini açıklamak için çıktıda daha ayrıntılı bir mesajın basılması daha yararlı olacaktır.

### String şablonu

Çıktıda görüntülenecek daha yararlı bir mesaj:

```
2 okunmamış mesajınız var.
```

Programın daha yararlı bir mesaj vermesi için aşağıdaki adımları izleyin.

1. Kotlin Playground'daki programınızı aşağıdaki kodla güncelleyin. println() çağrısı için, count değişkeni adını içeren bir dize değişmezi iletin. Metni tırnak içine almayı unutmayın. Bunun size beklediğiniz sonuçları vermeyeceğini unutmayın. Sorunu daha sonraki bir adımda çözeceksiniz.

```
fun main() {
    val count: Int = 2
    println("Okunmamış mesajlarınız var.")
}
```
2. Programı çalıştırın ve çıktı şunları göstermelidir:

```
Okunmamış mesajlarınız var.
```

Bu cümle anlamsız! İletide değişken adının değil, ccount değişkeninin değerinin görüntülenmesini istiyorsunuz.

3. Programınızı düzeltmek için, count değişkeninin önüne bir dolar işareti simgesi ekleyin: "$count okunmamış iletileriniz var." Bu bir string şablonudur çünkü bu durumda $count olan bir şablon ifadesi içerir. Bir şablon ifadesi, bir değer olarak değerlendirilen ve daha sonra dizeye eklenen bir ifadedir. Bu durumda, şablon ifadesi $count 2 olarak değerlendirilir ve 2, ifadenin bulunduğu dizeye eklenir.

```
fun main() {
    val count: Int = 2
    println("Okunmamış $count mesajlarınız var.")
}
```

4. Programı çalıştırdığınızda, çıktı istenen hedefle eşleşir:

```
okunmamış 2 mesajınız var.
```

Bu cümle kullanıcı için çok daha anlamlı!

5. Şimdi, count değişkeninin başlangıç değerini farklı bir tamsayı değişmeziyle değiştirin. Örneğin, 10 sayısını seçebilirsiniz. Kodun geri kalanını programda değiştirmeden bırakın.

```
fun main() {
    val count: Int = 10
    println("Okunmamış $count mesajlarınız var.")
}
```

6. Programı çalıştır. Çıktının buna göre değiştiğine ve programınızdaki println() ifadesini değiştirmenize bile gerek olmadığına dikkat edin.

```
Okunmamış 10 mesajlarınız var.
```

Bir string şablonunun ne kadar yararlı olabileceğini görebilirsiniz. String şablonunu kodunuza yalnızca bir kez yazdınız ("$count okunmamış mesajınız var."). Count değişkeninin başlangıç değerini değiştirirseniz, println() ifadesi çalışmaya devam eder. Kodunuz artık daha esnek!

Bu noktayı daha da vurgulamak için aşağıdaki iki programı karşılaştırın. Aşağıdaki ilk program, okunmamış mesajların tam sayısı doğrudan dizede olan bir dize değişmezi kullanır. Bu program yalnızca kullanıcınızın okunmamış 10 mesajı olduğunda çalışır.

```
fun main() {
    println("Okunmamış 10 mesajlarınız var.")
}
```
Aşağıdaki ikinci programda bir değişken ve bir string şablonu kullanarak kodunuz daha fazla senaryoya uyarlanabilir. Bu ikinci program daha esnektir!

```
fun main() {
    val count: Int = 10
    println("Okunmamış $count mesajlarınız var.")
}
```

### Tür çıkarımı

Değişkenleri bildirirken daha az kod yazmanıza izin veren bir ipucu.

Type inference (Tür çıkarımı), Kotlin derleyicisinin, tür açıkça kodda yazılmadan, bir değişkenin hangi veri türünün olması gerektiğini çıkarabildiği (veya belirleyebildiği) zamandır. Bu, değişken için bir başlangıç değeri sağlarsanız, değişken bildiriminde veri türünü atlayabileceğiniz anlamına gelir. Kotlin derleyicisi, ilk değerin veri türüne bakar ve değişkenin bu türden verileri tutmasını istediğinizi varsayar.

Aşağıda, tür çıkarımı kullanan bir değişken bildiriminin sözdizimi verilmiştir:

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166457713-e9aca941-f575-49c0-a62c-a3a9fded65be.png" />
</p>

Sayım örneğine dönersek, program başlangıçta şu kod satırını içeriyordu:

```
val count: Int = 2
```

Ancak bu kod satırı aşağıdaki gibi de yazılabilir. İki nokta üst üste simgesinin (:) ve Int veri türünün atlandığına dikkat edin. Güncellenen sözdiziminde yazılacak daha az sözcük vardır ve sayım adı verilen ve 2 değerinde bir Int değişkeni oluşturmanın aynı sonucunu elde eder. 

```
val count = 2
```
Kotlin derleyicisi, sayı değişkenine 2 (tamsayı) depolamak istediğinizi bilir, böylece sayım değişkeninin Int türünde olduğu sonucunu çıkarabilir. Uygun, değil mi? Bu, Kotlin kodunu yazmanın nasıl daha kısa olduğuna dair bir örnek!

Bu örnekte yalnızca Int türünde bir değişken ele alınsa da, tür çıkarımı kavramı Kotlin'deki tüm veri türleri için geçerlidir.

### Tam sayılarla temel matematik işlemleri

2 değerine sahip bir Int değişkeni ile "2" değerine sahip bir String değişkeni arasındaki fark nedir? Her ikisi de çıktıya yazdırıldığında, aynı görünürler.

Tamsayılarını bir Int (String yerine) olarak saklamanın avantajı, toplama, çıkarma, bölme ve çarpma gibi Int değişkenleriyle matematik işlemleri yapabilmenizdir (diğer [operatörlere](https://kotlinlang.org/docs/keyword-reference.html#operators-and-special-symbols) bakın). Örneğin, toplamlarını almak için iki tamsayı değişkeni birlikte eklenebilir. Tam sayıların Dizeler olarak saklanmasının makul olduğu durumlar kesinlikle vardır, ancak bu bölümün amacı, Int değişkenleriyle neler yapabileceğinizi size göstermektir.

1. Kotlin Playground'a dönün ve kod düzenleyicideki tüm kodu kaldırın.
2. Bir gelen kutusundaki okunmamış e-postaların sayısı için bir tamsayı değişkeni tanımladığınız yeni bir program oluşturun ve bunu 5 gibi bir değere tanımlayın. İsterseniz farklı bir sayı seçebilirsiniz. Gelen kutusundaki okunan e-posta sayısı için ikinci bir tamsayı değişkeni tanımlayın. 100 gibi bir değere tanımlayın. İsterseniz farklı bir sayı seçebilirsiniz. Ardından, iki tam sayıyı bir araya getirerek gelen kutusundaki toplam mesaj sayısını yazdırın.

```
fun main() {
    val unreadCount = 5
    val readCount = 100
    println("Gelen kutunuzda toplam ${unreadCount + readCount} iletiniz var.")
}
```
3. Programı çalıştırın ve gelen kutusundaki toplam mesaj sayısını göstermelidir:

```
Gelen kutunuzda toplam 105 iletiniz var.
```

Bir string şablonu için, tek bir değişken adından önce $ sembolünü koyabileceğinizi öğrendiniz. Ancak, daha karmaşık bir ifadeniz varsa, ifadeyi küme parantezlerinden önce $ sembolüyle küme parantezleri içine almalısınız: `${unreadCount + readCount}`. Kaşlı ayraçlar içindeki unreadCount + readCount ifadesi 105 olarak değerlendirilir. Ardından, dize değişmezine 105 değeri eklenir.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166459321-28c86c3a-d7f3-49a9-b30d-51364e20de6b.png" />
</p>

> Uyarı: Şablon ifadesinin etrafındaki küme parantezlerini unutursanız, beklenmedik sonuçlar alırsınız. Println() ifadesini println("Gelen kutunuzda $unreadCount + readCount toplam iletiniz var.") olarak değiştirerek ve çıktıyı gözlemleyerek Kotlin Playground'da bunu test edebilirsiniz.

4. Bu konuyu daha fazla araştırmak için, farklı adlara ve farklı başlangıç değerlerine sahip değişkenler oluşturun ve mesajları çıktıya yazdırmak için şablon ifadeleri kullanın.


Örneğin, bunu yazdırmak için programınızı değiştirin:

```
100 fotoğraf
10 fotoğraf silindi
90 fotoğraf kaldı
```

İşte programınızı yazmanın bir yolu, ancak onu yazmanın başka doğru yolları da var!

```
fun main() {
    val numberOfPhotos = 100
    val photosDeleted = 10
    println("$numberOfPhotos fotoğraf")
    println("$photosDeleted fotoğraf silindi")
    println("${numberOfPhotos - photosDeleted} fotoğraf kaldı")
}
```

# <a name="3"></a>Değişkenleri güncelleyin

Bir uygulama çalışırken, bir değişkenin değerinin güncellenmesi gerekebilir. Örneğin, bir alışveriş uygulamasında, kullanıcı alışveriş sepetine ürün ekledikçe alışveriş sepeti toplamı artar.

Alışveriş kullanım durumunu basit bir programa dönüştürelim. Mantık Kotlin'de değil, insan diliyle yazılmıştır. Buna sözde kod adı verilir, çünkü kodun nasıl yazılacağının kilit noktalarını açıklar, ancak kodun tüm ayrıntılarını içermez.

> Not: Sözde kod, derlenebilen çalışan kod anlamına gelmez, bu nedenle sözde kod olarak adlandırılır.

Bir programın main fonksiyonunda:

- 0 değerinde başlayan bir `cartTotal` tamsayı değişkeni oluşturun.
- Kullanıcı, alışveriş sepetine maliyeti 20 ABD doları olan bir kazak ekler.
- cartTotal değişkenini, alışveriş sepetlerindeki ürünlerin mevcut maliyeti olan 20 olarak güncelleyin.
- cartTotal değişkeni olan sepetlerindeki öğelerin toplam maliyetini çıktıya yazdırın.

Kodu daha da basitleştirmek için, kullanıcı alışveriş sepetine ürün eklediğinde kodu yazmanız gerekmez. (Bir programın kullanıcı girdisine nasıl yanıt verebileceğini henüz öğrenmediniz. Bu daha sonraki bir ünitede gelecektir.) Bu nedenle, cartTotal değişkenini oluşturduğunuz, güncellediğiniz ve yazdırdığınız kısımlara odaklanın.

1. Kotlin Playground'daki mevcut kodu aşağıdaki programla değiştirin. Programın 2. satırında cartTotal değişkenini 0 değerine tanımlarsınız. Bir başlangıç değeri sağladığınız için, tür çıkarımı nedeniyle Int veri türünü belirtmenize gerek yoktur. Programın 3. satırında, cartTotal değişkenini atama operatörü (=) ile 20'ye güncellemeye çalışıyorsunuz. Programın 4. satırında, bir string şablonu kullanarak cartTotal değişkenini yazdırıyorsunuz.

```
fun main() {
    val cartTotal = 0
    cartTotal = 20
    println("Total: $cartTotal")
}
```
2. Programı çalıştırın ve bir derleme hatası alacaksınız.
3. Hatanın, val'in yeniden atanamayacağını söylediğine dikkat edin. Hata, cartTotal değişkeninin değerini 20 olarak değiştirmeye çalışan programın üçüncü satırındadır. val cartTotal, bir başlangıç değeri (0) atandıktan sonra başka bir değere (20) yeniden atanamaz.

```
Val cannot be reassigned (Val yeniden atanamaz)
```
Bir değişkenin değerini güncellemeniz gerekiyorsa, değişkeni val yerine Kotlin var anahtar kelimesiyle bildirin.

- val anahtar sözcüğü - Değişken değerinin değişmeyeceğini düşündüğünüzde kullanın.
- var anahtar sözcüğü - Değişken değerinin değişebileceğini düşündüğünüzde kullanın.

Val ile değişken salt okunurdur, yani değişkenin değerini yalnızca okuyabilir veya ona erişebilirsiniz. Değer ayarlandıktan sonra değerini düzenleyemez veya değiştiremezsiniz. var ile değişken değişkendir, yani değer değiştirilebilir veya değiştirilebilir. Değer mutasyona uğratılabilir.

Farkı hatırlamak için val'i sabit bir değer ve var'ı değişken olarak düşünün. Kotlin'de, mümkün olduğunda var anahtar sözcüğü yerine val anahtar sözcüğünün kullanılması önerilir.

4. Programın 2. satırındaki cartTotal değişken bildirimini val yerine var kullanacak şekilde güncelleyin. Kodun nasıl görünmesi gerektiği:

```
fun main() {
    var cartTotal = 0
    cartTotal = 20
    println("Total: $cartTotal")
}
```
5. Değişkeni güncelleyen programın 3. satırındaki kodun sözdizimine dikkat edin.

```
cartTotal = 20
```
Mevcut değişkene (cartTotal) yeni bir değer (20) atamak için atama operatörünü (=) kullanın. Değişken zaten tanımlı olduğundan var anahtar sözcüğünü tekrar kullanmanız gerekmez.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166594065-077986b1-9ffe-4a5b-b44f-0fe8e1ffcc48.png" />
</p>

Kutu benzetmesini kullanarak, cartTotal etiketli kutuda saklanan 20 değerini hayal edin.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166595018-d6499150-95bd-46e5-8ad1-f1f99dfcff4d.png" />
</p>

Daha önceki bir kod satırında zaten bildirilmiş olan bir değişkeni güncellemek için genel syntax için bir diyagram burada. İfadeyi güncellemek istediğiniz değişkenin adıyla başlatın. Bir boşluk, eşittir işareti ve ardından başka bir boşluk ekleyin. Ardından değişken için güncellenen değeri yazın.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166596349-6c9c0c03-0709-462c-8401-a6159128b8c8.png" />
</p>

6. Programınızı çalıştırın ve kod başarıyla derlenmelidir. Bu çıktıyı yazdırmalıdır:

```
Total: 20
```

7. Program çalışırken değişken değerinin nasıl değiştiğini görmek için, değişken başlangıçta tanımlandıktan sonra cartTotal değişkenini çıktıya yazdırın. Aşağıdaki kod değişikliklerine bakın. 3. satırda yeni bir println() ifadesi var. Ayrıca kodun 4. satırına boş bir satır eklenmiş. Boş satırların derleyicinin kodu nasıl anladığı üzerinde herhangi bir etkisi yoktur. İlgili kod bloklarını ayırarak kodunuzu okumayı kolaylaştıracak boş bir satır ekleyin.

```
fun main() {
    var cartTotal = 0
    println("Total: $cartTotal")

    cartTotal = 20
    println("Total: $cartTotal")
}
```

8. Programı tekrar çalıştırın ve çıktı şöyle olmalıdır:

```
Total: 0
Total: 20
```
Başlangıçta alışveriş sepeti toplamının 0 olduğunu görebilirsiniz. Ardından 20'ye güncellenir. Bir değişkeni başarıyla güncellediniz! Bu, cartTotal'ı salt okunur bir değişkenden (val ile) değişebilir bir değişkene (var ile) değiştirdiğiniz için mümkün oldu.

Değerin değişmesini bekliyorsanız, bir değişkeni bildirmek için yalnızca `var` kullanmanız gerektiğini unutmayın. Aksi takdirde, bir değişkeni bildirmek için varsayılan olarak `val` kullanmalısınız. Bu uygulama, kodunuzu daha güvenli hale getirir. val kullanmak, siz beklemiyorsanız değişkenlerin programınızda güncellenmemesini sağlar. Bir değere bir değer atandığında, her zaman o değerde kalır.

> Not: Diğer programlama dillerine aşina iseniz, bir val bildirmek, salt okunur bir değişken olduğu için sabit bir değer bildirmek gibidir. Bu codelab için daha gelişmiş olan Kotlin'de sabitleri bildirirken izlenecek ek kurallar vardır, ancak bunları stil kılavuzunun [Constants](https://developer.android.com/kotlin/style-guide#constant_names) bölümünde bulabilirsiniz.

### Artırma ve eksiltme operatörleri


Artık bir değişkenin değerini güncellemek için değişken olarak bildirilmesi gerektiğini biliyorsunuz. Bu bilgiyi, tanıdık gelmesi gereken aşağıdaki e-posta mesajı örneğine uygulayın.

1. Kotlin Playground'daki kodu bu programla değiştirin:

```
fun main() {
    val count: Int = 10
    println("Okunmamış $count mesajınız var.")
}
```
2. Programı çalıştır. Şunları yazdırmalıdır:

```
Okunmamış 10 mesajınız var
```
3. Sayı değişkenini değişken bir değer yapmak için val anahtar sözcüğünü var anahtar sözcüğüyle değiştirin. Programı çalıştırdığınızda çıktıda herhangi bir değişiklik olmamalıdır.

```
fun main() {
    val count: Int = 10
    println("Okunmamış $count mesajınız var.")
}
```
4. Ancak, şimdi sayımı farklı bir değere güncelleyebilirsiniz. Örneğin, kullanıcının gelen kutusuna yeni bir e-posta geldiğinde, sayısını 1'e kadar artırabilirsiniz (Bir e-postanın gelmesi için kod yazmanıza gerek yoktur. İnternetten veri almak çok daha ileri bir konudur.) Şimdilik, bu kod satırıyla 1 artan sayı değişkenine odaklanın:

```
count = count + 1
```

Eşittir işaretinin sağındaki ifade count + 1'dir ve 11 olarak değerlendirilir. Bunun nedeni, şu anki count değerinin 10 (programın 2. satırında) ve 10 + 1'in 11'e eşit olmasıdır. Ardından atama operatörü ile. Sayı değişkeninde 11 değeri atanır veya saklanır.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166605102-5ba2c28d-fc5d-4081-b3cb-ea55afb0e64b.png" />
</p>


Bu kod satırını programınıza main() fonksiyonunun en altına ekleyin. Kodunuz aşağıdaki gibi görünmelidir:

```
fun main() {
    var count = 10
    println("Okunmamış $count mesajınız var.")
    count = count + 1
}
```

Programı şimdi çalıştırırsanız, çıktı öncekiyle aynıdır çünkü güncelledikten sonra count değişkenini kullanmak için herhangi bir kod eklememişsinizdir.

5. Değişken güncellendikten sonra okunmamış mesajların sayısını yazdıran başka bir print ifadesi ekleyin.

```
fun main() {
    var count = 10
    println("Okunmamış $count mesajınız var.")
    count = count + 1
    println("Okunmamış $count mesajınız var.")
}
```

6. Programı çalıştır. İkinci mesaj, güncellenen 11 mesaj sayısını göstermelidir.

```
Okunmamış 10 mesajınız var.
Okunmamış 11 mesajınız var.
```

7. Kısaca, bir değişkeni 1 artırmak istiyorsanız, iki artı sembolünden oluşan artırma operatörünü (++) kullanabilirsiniz. Bu sembolleri bir değişken adından hemen sonra kullanarak, derleyiciye değişkenin mevcut değerine 1 eklemek istediğinizi söylersiniz ve ardından yeni değeri değişkende saklarsınız. Aşağıdaki iki kod satırı eşdeğerdir, ancak ++ artış operatörünü kullanmak daha az yazmayı gerektirir.

```
count = count + 1
```
```
count++
```
Kodunuzda bu değişikliği yapın ve ardından programınızı çalıştırın. Değişken adı ile artırma operatörü arasında boşluk olmamalıdır.

```
fun main() {
    var count = 10
    println("Okunmamış $count mesajınız var.")
    count++
    println("Okunmamış $count mesajınız var.")
}
```
8. Programı çalıştır. Çıktı aynı, ancak şimdi yeni bir operatör öğrendiniz!

```
Okunmamış 10 mesajınız var.
Okunmamış 11 mesajınız var.
```
Şimdi, sayma değişkeni adından sonra azaltma operatörünü (--) kullanmak için programınızın 4. satırını değiştirin. Azaltma operatörü iki eksi sembolünden oluşur. Azaltma operatörünü değişken adından sonra yerleştirerek derleyiciye değişkenin değerini 1 azaltmak ve yeni değeri değişkene kaydetmek istediğinizi söylersiniz.

```
fun main() {
    var count = 10
    println("Okunmamış $count mesajınız var.")
    count--
    println("Okunmamış $count mesajınız var.")
}
```

10. Programı çalıştır. Bu çıktıyı yazdırmalıdır:

```
Okunmamış 10 mesajınız var.
Okunmamış 9 mesajınız var.
```
Bu bölümde, artırma operatörünü (++) ve azaltma operatörünü (--) kullanarak değiştirilebilir bir değişkeni nasıl güncelleyeceğinizi öğrendiniz. Daha spesifik olarak, say++, say + 1 ile aynıdır ve say--, say - 1 ile aynıdır.

# <a name="4"></a>Diğer veri türlerini keşfedin

Codelab'de daha önce, bazı yaygın temel veri türleriyle tanıştınız: `String`, `Int`, `Double` ve `Boolean`. Int veri türünü az önce kullandınız, şimdi diğer veri türlerini keşfedeceksiniz.

| Kotlin veri türleri | Ne tür veriler içerebilir |
|:---------------:|---------------| 
|String|Text|
|Int|Bütün tam sayılar|
|Double|Ondalık sayılar |
|Boolean|doğru ya da yanlış. Yalnızca iki olası değer olduğunda bu veri türünü kullanın. Kotlin'de true ve false anahtar kelimeler olduğuna dikkat edin.|

Çıktının ne olduğunu görmek için bu programları Kotlin Playground'da deneyin.

### Double

Ondalık değere sahip bir değişkene ihtiyacınız olduğunda, Double değişkeni kullanın. Geçerli aralığı hakkında bilgi edinmek için [bu tabloya](https://kotlinlang.org/docs/basic-types.html#floating-point-types) bakın ve örneğin saklayabileceği ondalık basamaklara bakın.

> Not: Double veri türünün adı, tek duyarlıklı Float veri türüne kıyasla çift duyarlıklı veri türünden gelir. Kesinlik, tutabilecekleri ondalık basamak sayısıdır. Bu nedenle, bir Double değişkeni daha kesin bir değer depolayabilir. Merak ediyorsanız, [bu tablo](https://kotlinlang.org/docs/basic-types.html#floating-point-types) Double ve Float türleri arasındaki belirli farklılıklar hakkında daha fazla ayrıntı gösterir. Codelab'ın bu bölümü, ondalık sayılarla çalışmak için Double kullanımına odaklanır.

Bir varış noktasına gittiğinizi ve yol boyunca mola vermeniz gerektiği için seyahatinizin üç ayrı bölüme ayrıldığını hayal edin. Bu program, hedefinize ulaşmak için kalan toplam mesafeyi görüntüler.

1. Bu kodu Kotlin Playground'a girin. Her kod satırında neler olduğunu anlayabiliyor musunuz?

```
fun main() {
    val trip1: Double = 3.20
    val trip2: Double = 4.10
    val trip3: Double = 1.72
    val totalTripLength: Double = 0.0
    println("$totalTripLength km yolunuz kaldı")
}
```

Gezinin her bir bölümünün mesafesini temsil etmek için trip1, trip2 ve trip3 adlı üç değişken bildirilir. Ondalık değerleri sakladıkları için hepsi Double değişkenleridir. Değerleri program boyunca değişmediğinden, her bir değişkeni bildirmek için val kullanın. Program ayrıca, şu anda 0.0 olarak tanımlanmış olan totalTripLength adlı dördüncü bir değişken oluşturur. Programın son satırı, totalTripLength değerine sahip bir mesaj yazdırır.

2. Kodu, totalTripLength değişkeni üç açma uzunluğunun toplamı olacak şekilde düzeltin.

```
val totalTripLength: Double = trip1 + trip2 + trip3
```

Eşittir işaretinin sağındaki ifade 9,02 olarak değerlendirilir çünkü 3,20 + 4,10 + 1,72, 9,02'ye eşittir. 9.02 değeri totalTripLength değişkeninde saklanır.

Tüm programınız aşağıdaki kod gibi görünmelidir:

```
fun main() {
    val trip1: Double = 3.20
    val trip2: Double = 4.10
    val trip3: Double = 1.72
    val totalTripLength: Double = trip1 + trip2 + trip3
    println("$totalTripLength km yolunuz kaldı")
}
```

3. Programı çalıştır. Bunu yazdırmalı:

```
9.02 km yolunuz kaldı
```

4. Tür çıkarımı nedeniyle değişken bildirimlerinden gereksiz Double veri türünü kaldırmak için kodunuzu düzeltin. Kotlin derleyicisi, başlangıç değerleri olarak sağlanan ondalık sayılara dayalı olarak bu değişkenlerin Double veri türleri olduğu sonucunu çıkarabilir.

```
fun main() {
    val trip1 = 3.20
    val trip2 = 4.10
    val trip3 = 1.72
    val totalTripLength: Double = trip1 + trip2 + trip3
    println("$totalTripLength km yolunuz kaldı")
}
```
5. Kodunuzun hala derlendiğinden emin olmak için kodunuzu yeniden çalıştırın. Çıktı aynı olmalı, ancak şimdi kodunuz daha basit!

### String

Metin depolayabilen bir değişkene ihtiyacınız olduğunda, bir String değişkeni kullanın. "Merhaba Kotlin" gibi String değişmez değerlerinin etrafında tırnak işaretleri kullanmayı unutmayın, oysa Int ve Double değişmez değerlerinin çevresinde tırnak işaretleri yoktur.

1. Bu programı kopyalayıp Kotlin Playground'a yapıştırın.

```
fun main() {
    val nextMeeting = "Bir sonraki görüşme:"
    val date = "1 Ocak"
    val reminder = nextMeeting + date
    println(reminder)
}
```

Bildirilen iki String değişkeni olduğuna dikkat edin, bir nextMeeting değişkeni ve bir tarih değişkeni. Ardından, nextMeeting değişkeni artı tarih değişkenine eşit olarak ayarlanan, reminder adlı üçüncü bir String değişkeni bildirilir.

`+` sembolü ile birleştirme adı verilen iki diziyi birbirine ekleyebilirsiniz. İki ip birbiri ardına birleştirilir. nextMeeting + date ifadesinin sonucu, aşağıdaki şemada gösterildiği gibi "Bir sonraki görüşme: 1 Ocak" olur.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166725777-6b0bbcdb-ec9a-416b-b170-9ca1f9bdd0e3.png" />
</p>

"Sonraki toplantı: 1 Ocak" değeri daha sonra programın 4. satırındaki atama operatörü kullanılarak reminder değişkenine kaydedilir.

2. Programınızı çalıştırın. Bunu yazdırmalı:

```
Bir sonraki görüşme:1 Ocak
```
İki dizeyi birbirine bağladığınızda, dizeler arasına fazladan boşluk eklenmez. Ortaya çıkan dizede iki nokta üst üste işaretinden sonra bir boşluk istiyorsanız, boşluğu bir dizeye veya diğerine eklemeniz gerekir.

3. nextMeeting değişkeninizi, kapanış tırnak işaretinden önce dizenin sonunda fazladan boşluk olacak şekilde güncelleyin. (Alternatif olarak, tarih değişkeninin başına fazladan bir boşluk ekleyebilirdiniz). Programınız aşağıdaki gibi görünmelidir:

```
fun main() {
    val nextMeeting = "Bir sonraki görüşme: "
    val date = "1 Ocak"
    val reminder = nextMeeting + date
    println(reminder)
}
```
4. Programınızı tekrar çalıştırın ve şimdi çıktı mesajında iki nokta üst üste işaretinden sonra bir boşluk olmalıdır.

```
Bir sonraki görüşme: 1 Ocak
```
5. Hatırlatıcı değişkeninde depolanan ifadeye başka bir metin parçası ekleyecek veya birleştirecek şekilde kodu değiştirin.

Reminder dizesinin sonuna "iş yerinde" dizesini eklemek için + sembolünü kullanın.

6. Programı çalıştır.
Bu çıktıyı yazdırmalıdır:

```
Bir sonraki görüşme: 1 Ocak iş yerinde
```
Aşağıdaki kod, davranışı uygulayabileceğiniz bir yolu gösterir.

```
fun main() {
    val nextMeeting = "Bir sonraki görüşme: "
    val date = "1 Ocak"
    val reminder = nextMeeting + date + " iş yerinde"
    println(reminder)
}
```
nextMeeting ve date çevresinde tırnak işareti bulunmadığına dikkat edin, çünkü bunlar var olan dize değişkenlerinin adlarıdır (ilgili değerleri, etraflarında tırnak bulunan metinlerdir). Tersine, "iş yerinde" değişmezi daha önce herhangi bir değişkende tanımlanmamıştır, bu nedenle derleyicinin bunun diğer dizelerle birleştirilmesi gereken bir dize olduğunu bilmesi için bu metnin etrafında tırnak kullanın.

Teknik olarak, ayrı değişkenler kullanmak yerine tam metinli tek bir String değişkeni bildirerek aynı çıktıyı elde edebilirsiniz. Ancak, bu alıştırmanın amacı, String değişkenlerini nasıl bildirebileceğinizi ve değiştirebileceğinizi, özellikle de ayrı stringleri nasıl birleştireceğinizi göstermektir.

7. Dizeler içeren kodu okurken kaçış dizileriyle karşılaşabilirsiniz. Kaçış dizileri, önünde ters eğik çizgi olarak da adlandırılan ters eğik çizgi simgesi (\) bulunan karakterlerdir.

Bir örnek, aşağıdaki örnekte olduğu gibi bir dize değişmezi içinde \$ görmektir. Bu kodu kopyalayıp Kotlin Playground'a yapıştırın.

```
fun main() {
    println("Ödenmesi gereken tutar: \$5")
}
```
Dize içindeki ifadenin değerini almak için bir ifadenin önüne dolar işareti simgesini ($) koymayı daha önce öğrenmiştiniz. Peki ya dizginizde $ sembolünü kullanmak isterseniz? Ardından, dizenizde $ sembolünden önce \$ olarak \ sembolünü eklemeniz gerekir.

8. Çıktıyı görmek için programı çalıştırın. Şunları göstermelidir:

```
Ödenmesi gereken tutar: $5
```

"Ödenmesi gereken tutar: \$5", bir kaçış dizisi olan \$ içeren bir dize değişmez değeridir. Bir şablon ifadesi içermediği için bir dize şablonu değildir.

Kotlin'de desteklenen diğer kaçış dizileri için, kaçış dizileriyle ilgili [dokümantasyon](https://kotlinlang.org/docs/basic-types.html#characters) sayfasına bakın. Örneğin, dizenizde bir tırnak işareti istiyorsanız, \" deki gibi tırnak işaretinden önce \ sembolünü kullanın.

9. Bu kodu Kotlin Playground'a kopyalayın.

```
fun main() {
    println("She said, \"Hello\"")
}
```
Çıktı:

```
She said, "Hello"
```

Artık dizileri birleştirmeyi ve ayrıca diziler içindeki dizilerden kaçmayı öğrendiniz. Bu codelab'in kapsadığı son veri türüne geçin.

### Boolean

Boolean veri türü, değişkeniniz true veya false ile temsil edilen yalnızca iki olası değere sahip olduğunda kullanışlıdır.

Örnek olarak, bir cihazın uçak modunun açık mı yoksa kapalı mı olduğunu veya bir uygulamanın bildirimlerinin etkin mi yoksa devre dışı mı olduğunu gösteren bir değişken verilebilir.

1. Bu kodu Kotlin Playground'a girin. Bu programın 2. satırında, noticeEnabled adında bir Boolean değişkeni bildirir ve onu true olarak başlatırsınız. Teknik olarak, bildirimde : Boolean'ı atlayabilirsiniz, böylece isterseniz kaldırabilirsiniz. Programın 3. satırında noticeEnabled değişkeninin değerini yazdırıyorsunuz.

```
fun main() {
    val notificationsEnabled: Boolean = true
    println(notificationsEnabled)
}
```
Programı çalıştırın ve şunu yazdırmalıdır:

```
true
```
2. Programın 2. satırında Boolean'ın başlangıç değerini false olarak değiştirin.

```
fun main() {
    val notificationsEnabled: Boolean = false
    println(notificationsEnabled)
}
```
Programı çalıştırın ve şunu yazdırmalıdır:

```
false
```
3. Diğer veri türleri, Dizeler ile birleştirilebilir. Örneğin, Booleanları Dizelerle birleştirebilirsiniz. "Bildirimler etkinleştirildi mi?" dizesinin sonuna noticeEnabled boolean değişkeninin değerini birleştirmek (veya eklemek) için + simgesini kullanın.

```
fun main() {
    val notificationsEnabled: Boolean = false
    println("Bildirimler etkinleştirildi mi? " + notificationsEnabled)
}
```
Birleştirmenin sonucunu görmek için programı çalıştırın. Program şu çıktıyı yazdırmalıdır:

```
Bildirimler etkinleştirildi mi? false
```
Boolean değişkenini doğru veya yanlış bir değere ayarlamanın mümkün olduğunu görebilirsiniz. Bir Boolean değişkeni gerçek bir değere sahip olduğunda, bazı talimat setlerini yürüttüğünüz daha ilginç senaryoları kodlamanıza olanak tanır. Veya Boolean değeri yanlış bir değere sahipse bu talimatları atlarsınız. Gelecekteki bir codelab'de Booleanlar hakkında daha fazla bilgi edineceksiniz.


# <a name="5"></a>Kodlama kuralları

Önceki codelab'de, Android kodunu Google'ın önerdiği ve diğer profesyonel geliştiricilerin izlediği, tutarlı bir şekilde yazmak için Kotlin stil kılavuzuyla tanıştınız.

Öğrendiğiniz yeni konulara dayalı olarak izlemeniz için birkaç biçimlendirme ve kodlama kuralı daha:

- Değişken isimleri büyük harfle ve küçük harfle başlamalıdır.
- Değişken bildiriminde, veri türünü belirttiğinizde iki nokta üst üste işaretinden sonra bir boşluk olmalıdır.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166840249-23799c44-9de0-4499-94e8-ae5434f4d365.png" />
</p>

- Atama (=), toplama (+), çıkarma (-), çarpma (*), bölme (/) operatörleri ve daha fazlası gibi bir operatörden önce ve sonra bir boşluk olmalıdır.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166840359-e1e5d67b-6cc2-44cd-bc4a-64081758167d.png" />
</p>

Daha karmaşık programlar yazarken, satır başına önerilen 100 karakter sınırı vardır. Bu, bir programdaki tüm kodu, kodu okurken yatay olarak kaydırmanıza gerek kalmadan bilgisayar ekranınızda kolayca okuyabilmenizi sağlar.

# <a name="6"></a>Kodunuzda yorum yapma

Kodlama yaparken izlenecek başka bir iyi uygulama, kodun ne yapmak istediğini açıklayan yorumlar eklemektir. Yorumlar, kodunuzu okuyan kişilerin onu daha kolay takip etmesine yardımcı olabilir. İki eğik çizgi simgesi //, satırın geri kalanında kendisinden sonra gelen metnin yorum olarak kabul edildiğini, dolayısıyla kod olarak yorumlanmadığını belirtir. İki eğik çizgi sembolünden sonra boşluk eklemek yaygın bir uygulamadır.

```
// Bu bir yorumdur.
```

Bir yorum, bir kod satırının ortasından da başlayabilir. Bu örnekte, yükseklik = 1 normal bir kodlama ifadesidir. // veya Başlamak için yüksekliğin 1 olduğunu varsayın, sonraki her şey bir yorum olarak yorumlanır ve kodun bir parçası olarak kabul edilmez.

```
yükseklik = 1 // Başlamak için yüksekliğin 1 olduğunu varsayın.
```

Kodu bir satırda 100 karakteri aşan uzun bir yorumla daha ayrıntılı açıklamak istiyorsanız, çok satırlı bir yorum kullanın. Çok satırlı yorumu eğik çizgi (/) ve yıldız işareti (*) ile /* olarak başlatın. Yorumun her yeni satırının başına bir yıldız işareti ekleyin. Ardından son olarak yorumu bir yıldız işareti ve eğik çizgi sembolü */ ile sonlandırın.

```
/*
  * Bu çok uzun bir yorum
  * birden fazla satır kullanın.
  */
```

Bu program, neler olduğunu açıklayan tek satırlı ve çok satırlı yorumlar içerir:

```
/**
  * Bu program mesaj sayısını görüntüler
  * kullanıcının gelen kutusundaki.
  */
fun main() {
    // Okunmamış mesajların sayısı için bir değişken oluşturun.
    var count = 10
    println("sizin $count okunmamış mesajınız var.")

    // Mesaj sayısını 1 azaltın.
    count--
    println("sizin $count okunmamış mesajınız var.")
}
```

Daha önce belirtildiği gibi, ilgili ifadeleri birlikte gruplandırmak ve kodun okunmasını kolaylaştırmak için kodunuza boş satırlar ekleyebilirsiniz.

1. Kullandığınız önceki bir kod parçacığına bazı yorumlar ekleyin.
2. Yorumların çıktıyı etkilememesi gerektiğinden, davranışın değişmediğinden emin olmak için programı çalıştırın.

