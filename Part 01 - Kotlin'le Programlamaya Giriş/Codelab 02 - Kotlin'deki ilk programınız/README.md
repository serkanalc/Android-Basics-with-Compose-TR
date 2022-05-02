# Kotlin'le Programlamaya Giriş

### Konu Başlıkları:

📌  [Kotlin Playground'u açın](#1) <br>
📌  [İlk programınızı çalıştırın](#2) <br>
📌  [Bir Fonksiyonun Parçaları](#3) <br>
📌  [Compose ile Android Temelleri'ne hoş geldiniz!](#4) <br>

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










