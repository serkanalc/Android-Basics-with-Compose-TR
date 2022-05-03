# Kotlin'de değişkenler oluşturun ve kullanın


### Konu Başlıkları:

📌  [Değişkenler ve veri türleri](#1) <br>
📌  [Değişkenleri tanımlayın ve kullanın](#2) <br>
📌  [Değişkenleri güncelleyin](#3) <br>

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
