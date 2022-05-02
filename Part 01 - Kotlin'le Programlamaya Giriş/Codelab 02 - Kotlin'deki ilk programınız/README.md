# Kotlin'le Programlamaya Giriş

### Konu Başlıkları:

📌  [Kotlin Playground'u açın](#1) <br>
📌  [İlk programınızı çalıştırın](#2) <br>
📌  [Bir Fonksiyonun Parçaları](#3) <br>
📌  [Programınızı değiştirin](#4) <br>
📌  [Kotlin stil rehberi](#5) <br>
📌  [Kodunuzdaki hataları düzeltin](#6) <br>

#


# <a name="1"></a>Kotlin Playground'u açın

Bilgisayarınızdaki bir web tarayıcısında [Kotlin Playground](https://developer.android.com/training/kotlinplayground)'u açın.

Bu resme benzer bir web sayfası görmelisiniz:

<p align="center">
  <img src="https://developer.android.com/codelabs/basic-android-kotlin-compose-first-program/img/73637fd10c41e9f8.png" />
</p>

*Kod düzenleyicide önceden doldurulmuş bazı varsayılan kodlar var. Bu üç kod satırı basit bir program oluşturur:*

```
fun main() {
    println("Hello, world!")
}
```

Daha önce hiç programlama yapmamış olsanız bile, programın ne yaptığını tahmin edebilir misiniz?

Bir sonraki bölüme geçerek tahmininizin doğru olup olmadığını görün!

# <a name="2"></a>İlk programınızı çalıştırın

Programınızı çalıştırmak için Çalıştır düğmesine tıklayın.

Çalıştır düğmesine tıkladığınızda çok şey olur. Kotlin programlama dilindeki kod, insanlar tarafından anlaşılmak içindir, böylece insanlar Kotlin programlarını daha kolay okuyabilir, yazabilir ve işbirliği yapabilir. Ancak, bilgisayarınız bu dili hemen anlamıyor.

Yazdığınız Kotlin kodunu alan, ona satır satır bakan ve onu bilgisayarın anlayabileceği bir şeye çeviren Kotlin derleyicisi adlı bir şeye ihtiyacınız var. Bu işleme kodunuzu derleme denir.

Kodunuz başarıyla derlenirse, programınız çalışır (veya yürütülür). Bilgisayar programınızı çalıştırdığında, talimatlarınızın her birini gerçekleştirir. Daha önce bir yemek tarifi izlediyseniz, tarifteki her adımı gerçekleştirmek, her bir talimatı yerine getirmek olarak kabul edilir.

İşte programınızı çalıştırdığınızda görmeniz gerekenlerin bir ekran görüntüsü.

<p align="center">
  <img src="https://developer.android.com/codelabs/basic-android-kotlin-compose-first-program/img/14bea1122ec05039.png" />
</p>

*Kod düzenleyicinin altında, programınızın çıktısını veya sonucunu gösteren bir bölme görmelisiniz*

```
Hello, world!
```

Güzel! Bu programın amacı `Hello, world!` yazan bir mesajı yazdırmak veya görüntülemektir.

> Uyarı: Bu sonucu görmüyorsanız, önceki bölümdeki üç satırlık kodu kopyalayıp Kotlin Playground'a yapıştırın ve tekrar deneyin.

Bu nasıl çalışıyor? Bir Kotlin programının, kodunuzda Kotlin derleyicisinin başladığı belirli yer olan bir ana işleve sahip olması gerekir. fun main, programın giriş noktası veya başlangıç noktasıdır.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166304842-6e6e1822-814b-4d18-8a8b-8ea53ce6b3ae.png" />
</p>

Şimdi merak ediyor olabilirsiniz, fonksiyon nedir?

# <a name="3"></a>Bir Fonksiyonun Parçaları 

Fonksiyon, belirli bir görevi gerçekleştiren bir programın bir bölümüdür. Programınızda birçok fonksiyona sahip olabilirsiniz veya sadece bir fonksiyona sahip olabilirsiniz.

## Tanımlama ve Fonksiyon çağırma

Kodunuzda önce bir fonksiyon tanımlarsınız. Bu, o görevi gerçekleştirmek için gereken tüm talimatları belirttiğiniz anlamına gelir.

Fonksiyon tanımlandıktan sonra, o işlevi çağırabilirsiniz, böylece bu Fonksiyon içindeki talimatlar gerçekleştirilebilir veya yürütülebilir.

İşte bir benzetme. Çikolatalı kekin nasıl pişirileceğine dair adım adım talimatlar yazıyorsunuz. Bu talimat setinin bir adı olabilir: **çikolatalıKekPişir**. Her kek pişirmek istediğinizde çikolatalıKekPişir talimatlarını uygulayabilirsiniz. 3 kek istiyorsanız, çikolatalıKekPişir talimatlarını 3 kez uygulamanız gerekir. İlk adım, adımları tanımlamak ve ona Fonksiyonu tanımladığı düşünülen bir isim vermektir. Ardından, fonksiyonları çağırmak olarak kabul edilir, yürütülmesini istediğiniz zaman adımlara başvurabilirsiniz.

> Not: "declare a function" alternatif ifadesini duyabilirsiniz. Bildirmek ve tanımlamak kelimeleri birbirinin yerine kullanılabilir ve aynı anlama sahiptir. Bir işlevi tanımlayan tam koda atıfta bulunan "function definition" veya "function declaration" terimlerini de duyabilirsiniz.

### Bir fonksiyon tanımlayın

Bir fonksiyon tanımlamak için gereken temel parçalar şunlardır:

- Fonksiyonun bir ada ihtiyacı vardır, böylece daha sonra arayabilirsiniz.
- Fonksiyon ayrıca, fonksiyon çağrıldığında sağlanması gereken bazı girdiler veya bilgiler gerektirebilir. fonksiyon, amacını gerçekleştirmek için bu girdileri kullanır. Girdi gerektirme isteğe bağlıdır ve bazı fonksiyonlar girdi gerektirmez.
- Fonksiyon‚ ayrıca, görevi gerçekleştirmek için talimatları içeren bir gövdeye sahiptir.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166307405-30402cda-6bbe-4f13-af33-80d4c4fbc656.png" />
</p>

Yukarıdaki diyagramı Kotlin koduna çevirmek için, bir fonksiyon tanımlamak için aşağıdaki syntax veya formatı kullanın. Bu elemanların sırası önemlidir. `Fun` kelimesi önce gelmeli, ardından fonksiyon adı, ardından parantez içindeki girişler, ardından işlev gövdesinin etrafında küme parantezleri gelmelidir.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166307799-a8702e4d-03fd-476d-8913-33958870389a.png" />
</p>

Kotlin Playground'da gördüğünüz ana fonksiyon örneğindeki bir fonksiyonun önemli kısımlarına dikkat edin:

- Fonksiyon tanımı `fun` kelimesiyle başlar.
- O zaman fonksiyonun adı `main` olur.
- Fonksiyona giriş yoktur, bu nedenle parantezler boştur.
- fonksiyon gövdesinde, işlevin açılış ve kapanış küme parantezleri arasında yer alan println("Hello, world!") adında bir kod satırı vardır.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166308222-c7b95206-58c4-4aa6-a67d-e36ce78e3553.png" />
</p>

Fonksiyonun her bir bölümü aşağıda daha ayrıntılı olarak açıklanmıştır.


### İşlev anahtar sözcüğü:

Kotlin'de bir fonksiyon tanımlamak üzere olduğunuzu belirtmek için, yeni bir satırda fun (fonksiyonun kısaltması) özel kelimesini kullanın. Fun tam olarak gösterildiği gibi tümü küçük harflerle yazmalısınız. Kotlin derleyicisi ne demek istediğinizi anlayamayacağından func, function veya bazı alternatif yazımları kullanamazsınız.

Bu özel sözcüklere Kotlin'de anahtar sözcükler denir ve Kotlin'de yeni bir foksiyon oluşturmak gibi belirli bir amaç için ayrılmıştır.

### Fonksiyon adı:

Fonksiyonların, insanların kendilerini tanımlamak için adları olmasına benzer şekilde, birbirlerinden ayırt edilebilmeleri için adları vardır. Fonksiyonun adı fun anahtar sözcüğünden sonra bulunur.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166311376-8afbd686-2196-462a-95ba-34ff943e7f28.png" />
</p>

Fonksiyonun amacına göre fonksiyonunuz için uygun bir ad seçin. İsim genellikle bir fiil veya fiil cümlesidir. fonksiyon adı olarak bir Kotlin anahtar sözcüğünü kullanmaktan kaçınmanız önerilir.

fonksiyon adları,büyük harf kuralına uygun olmalıdır. fonksiyon adının ilk kelimesinin tamamen küçük harf olur, isimde birden fazla kelime varsa kelimeler arasında boşluk bırakılmaz ve diğer kelimeler büyük harfle başlamalıdır.

Örnek fonksiyon isimleri:

- hesaplaİpucu
- gösterHataMesaj
- çekFotoğraf
- 
### Fonksiyon girişleri

fonksiyon adının her zaman parantezler tarafından takip edildiğine dikkat edin. Bu parantezler, foksiyon için girdileri listelediğiniz yerdir.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166313391-2e564860-20c2-4d57-91f8-06cfa7384deb.png" />
</p>

Girdi, bir foksiyonun amacını gerçekleştirmek için ihtiyaç duyduğu bir veri parçasıdır. Bir fonksiyon tanımladığınızda, fonksiyon çağrıldığında belirli girdilerin iletilmesini isteyebilirsiniz. Bir foksiyon için gerekli giriş yoksa parantezler boştur ().

Farklı sayıda girişe sahip bazı işlev örnekleri:

Aşağıdaki şema, `addOne` adlı bir fonksiyonu göstermektedir. Fonksiyonun amacı verilen bir sayıya 1 eklemektir. Verilen sayı olan bir giriş var. Fonksiyon gövdesinin içinde, işleve iletilen sayıya 1 ekleyen kod vardır.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166313826-ce444773-bde2-44fb-9987-4b33c1ef8aea.png" />
</p>

Bu sonraki örnekte `printFullName` adında bir fonksiyon var. Fonksiyon için biri ad, biri de soyadı için olmak üzere iki giriş gereklidir. Fonksiyon gövdesi, kişinin tam adını görüntülemek için çıktıdaki adı ve soyadını yazdırır.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166314083-6d01bd07-6302-4230-a3b4-c7d4b1bf1bee.png" />
</p>

Bu son örnek, foksiyon çağrıldığında herhangi bir girdinin iletilmesini gerektirmeyen bir foksiyonu göstermektedir. `displayHello()` foksiyonunu çağırdığınızda, çıktıya bir Hello mesajı yazdırılır.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166314357-928729ec-40e9-4630-8680-27d1c66f74bc.png" />
</p>

### Fonksiyon gövdesi:

Fonksiyon gövdesi, fonksiyonun amacına ulaşmak için gereken talimatları içerir. fonksiyon gövdesini, açma ve kapama küme parantezleri içinde yer alan kod satırlarını arayarak bulabilirsiniz.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166314837-4fa08900-ca1e-4b0e-bb83-1623b08e48f8.png" />
</p>

### Basit program açıklaması

Codelab'de daha önce gördüğünüz basit programa tekrar bakın.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166307405-30402cda-6bbe-4f13-af33-80d4c4fbc656.png" />
</p>

Program bir fonksiyon içerir: main fonksiyon, Kotlin'deki özel bir işlev adıdır. Kotlin Playground'da kodunuzu yazarken, kodunuz `main()` işlevinin içine yazılmalı veya `main()` işlevinden çağrılmalıdır.

Bu `main()` işlevinin gövdesinde yalnızca bir kod satırı vardır:

```
println("Hello, world!")
```

Bu kod satırı, Hello, world! çıktı bölmesindeki metin. Daha spesifik olarak, bu kod satırında println() işlevi çağrılıyor. println(), Kotlin dilinde önceden tanımlanmış bir fonksiyondur. Bu, Kotlin dilini oluşturan mühendis ekibinin println() foksiyonu için fonksiyon bildirimini zaten yazdığı anlamına gelir. Fonksiyon, yazdırılması gereken mesaj olan bir giriş gerektirir.

println() işlevini çağırdığınızda, mesaj metnini fonksiyon adından sonra parantez içine yerleştirin. Görüntülenecek metnin etrafında "Merhaba, dünya!" gibi tırnak işaretleri kullandığınızdan emin olun.

Program çalıştırıldığında, println() fonksiyonuna iletilen mesaj çıktıya yazdırılır:


```
Hello, world!
```

# Sen de Dene!
Şimdi programdaki orijinal koda tekrar bakın. Çıktının bunun yerine bu mesajı göstermesi için Kotlin Playground'daki kodu değiştirebilir misiniz?

```
Hello, Android!
```

# <a name="4"></a>Programınızı değiştirin

1. Çıktıda görüntülenen mesajı değiştirmek için, programın ikinci satırındaki println() fonksiyon çağrısını değiştirin. println() fonksiyonunda world'u Android ile değiştirin. "Hello, Android!" hala tırnak içinde ve parantez içinde.

```
fun main() {
    println("Hello, Android!")
}
```

2. Programı çalıştır.
3. Çıktı şu mesajı göstermelidir:

```
Hello, Android!
```

İyi iş çıkardın, ilk programınızı değiştirdin!

Şimdi, mesajın iki kez yazdırılması için kodunuzu değiştirebilir misiniz? İstenen çıktıya bakın:

```
Hello, Android!
Hello, Android!
```

### Birden fazla mesaj yazdır

Bir görevi tamamlamak için ihtiyaç duyduğunuz kadar komut satırını bir foksiyonun içine koyabilirsiniz. Ancak, Kotlin'de her satırda yalnızca bir ifade olması gerektiğini unutmayın. Başka bir ifade yazmak istiyorsanız, onu fonksiyonun yeni satırına koyun.

Programınızı birden çok metin satırı yazdıracak şekilde değiştirmek için:

1. İlk println() ifadesini kopyalayın ve altındaki ikinci ifadeyi işlev gövdesine yapıştırın. Her iki println() ifadesi de ana işlevin küme parantezleri içinde yer almalıdır. Şimdi fonksiyon gövdesi içinde iki ifadeniz var.

```
fun main(){    
    println("Hello, Android!")
    println("Hello, Android!")
}
```

2. Programı çalıştır.
3. Programınızı çalıştırdığınızda çıktısı şöyle olmalıdır:


```
Hello, Android!
Hello, Android!
```

Koddaki değişikliklerin çıktıyı nasıl etkilediğini görebilirsiniz.

Kodu, Hello, SENİN_ADIN! yazacak şekilde değiştirin.

# <a name="5"></a>Kotlin stil rehberi

Bu kurs boyunca, bir Android geliştiricisi olarak izleyeceğiniz iyi kodlama uygulamaları hakkında bilgi edineceksiniz. Böyle bir uygulama, Google'ın Kotlin'de yazılan kodlar için Android kodlama standartlarını takip etmektir. Tam kılavuza stil kılavuzu denir ve kodun görsel görünüm ve kodunuzu yazarken izlenecek kurallar açısından nasıl biçimlendirilmesi gerektiğini açıklar. Örneğin, stil kılavuzu boşluk, girinti, adlandırma ve daha fazlasının kullanımına ilişkin öneriler içerir.

Stil kılavuzunu izlemenin amacı, kodunuzun daha kolay okunmasını ve diğer Android geliştiricilerinin kodlarını yazma biçimleriyle daha tutarlı olmasını sağlamaktır. Bu tutarlılık, büyük projelerde birlikte çalışırken önemlidir, böylece projedeki tüm dosyalar boyunca kod stili aynı olur.

Kotlin'de şu ana kadar öğrendiklerinizle ilgili stil kılavuzu tavsiyelerinden bazıları şunlardır:

- Fonksiyon isimleri camel case(deve kılıfı) şeklinde olmalı ve fiil veya fiil tamlaması olmalıdır.
- Her ifade kendi satırında olmalıdır.
- Açılış küme parantezi, işlevin başladığı satırın sonunda görünmelidir.
- Açılan kıvrık parantezden önce bir boşluk olmalıdır.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166318098-3cdba41b-ebb1-4927-be78-18c8c37c440e.png" />
</p>

- İşlev gövdesi 4 boşlukla girintili olmalıdır. Kodunuzu girintilemek için tab karakteri kullanmayın, 4 boşluk yazın.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166318900-9ec7ab8f-4374-4b88-a4d1-0c6e5506a0b9.png" />
</p>

- Kapanış kıvrık parantezi, fonksiyon gövdesindeki son kod satırından sonra kendi satırındadır. Kapanış ayracı, işlevin başındaki fun anahtar sözcüğüyle aynı hizada olmalıdır.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166319024-e7c46fd5-f7e2-4cac-9a60-8790ee9f1978.png" />
</p>

Kotlin'de bilginizi geliştirirken daha fazla Android kodlama kuralı öğreneceksiniz. [Tam stil kılavuzu](https://developer.android.com/kotlin/style-guide) burada, ancak Kotlin'de henüz öğrenmediğiniz diğer konuları kapsadığından endişelenmeyin.

# <a name="6"></a>Kodunuzdaki hataları düzeltin

Bir insan dilini öğrendiğinizde, kelimeleri doğru şekilde kullanmanın ve cümleler kurmanın doğru yolu için sözdizimi ve dilbilgisi kuralları vardır. Benzer şekilde, programlama dilleri için, başarılı bir şekilde derlenen kod anlamına gelen geçerli kodu neyin oluşturduğuna ilişkin belirli kurallar vardır.

Kodlama sürecinin normal bir parçası, hata yapmayı ve yanlışlıkla geçersiz kod yazmayı içerir. Yeni başlayan biri olarak, bu hatalarla karşılaşmak kafa karıştırıcı veya bunaltıcı olabilir. Ama merak etmeyin, bu bekleniyor. Kod, ilk yazıldığında nadiren kusursuz çalışır. Tıpkı bir belge yazmanın birçok taslak gerektirdiği gibi, kod yazmak da beklendiği gibi çalışana kadar birçok yineleme alabilir.

Kod başarıyla derlenemiyorsa bir hata vardır. Örneğin, eksik bir tırnak işareti veya parantez gibi bir yazım hatanız varsa, derleyici kodunuzu anlamaz ve bilgisayarın gerçekleştireceği adımlara çeviremez. Kodunuz beklendiği gibi çalışmıyorsa veya kod düzenleyicinizde bir hata mesajı görüyorsanız, kodunuza geri dönüp düzeltmeniz gerekir. Bu hataları çözme sürecine troubleshooting denir.

1. Aşağıdaki kod parçasını kopyalayıp Kotlin Playground'a yapıştırın ve programı çalıştırın. Ne görüyorsun?

```
fun main() {
    println("Today is sunny!)
}
```
İdeal olarak, Bugün güneşlidir mesajını görmek istersiniz! görüntülenir. Bunun yerine, çıktı bölmesinde hata mesajları içeren ünlem işareti simgeleri görürsünüz.

Hata mesajları "Expecting" kelimesiyle başlar çünkü Kotlin derleyicisi bir şeyi "bekliyor" ancak kodda bulamıyor. Bu durumda derleyici, programınızın ikinci satırındaki kod için bir kapanış tırnak işareti ve bir kapanış parantezi bekler.

println() deyiminde, görüntülenecek mesajın açılış tırnak işaretine sahip olduğuna, ancak kapanış tırnak işaretinin olmadığına dikkat edin. Kodda bir kapatma parantezi olmasına rağmen, derleyici parantezin yazdırılacak metnin bir parçası olduğunu düşünüyor çünkü ondan önce kapatma tırnak işareti yok.

2. Kapanış tırnak işaretini ünlem işaretinden sonra, kapanış parantezinden önce ekleyin.

```
fun main() {
    println("Today is sunny!")
}
```

Main Fonksiyon, metnin tırnak içine alındığı ve parantez içine alındığı bir println() ifadesi olan bir kod satırı içerir: "Today is sunny!".

3. Programı tekrar çalıştırın.
Herhangi bir hata olmamalı ve çıktı bölmesi şu metni göstermelidir:

```
Today is sunny!
```

Hatayı düzeltmek için iyi çalışmalar! Kod yazma ve hataları giderme konusunda daha fazla deneyim kazandığınızda, kodunuzu yazarken büyük harf, yazım, boşluk, semboller ve adlara dikkat etmenin ne kadar önemli olduğunu anlayacaksınız.

Bir sonraki bölümde, öğrendiklerinizi uygulamak için bir dizi alıştırma üzerinde çalışıyorsunuz. Çözümler, codelab'in sonunda sağlanır, ancak yanıtı önce kendi başınıza bulmak için elinizden gelenin en iyisini yapın.
