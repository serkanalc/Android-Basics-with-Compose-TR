### Konu Başlıkları:


📌  [Başlamadan Önce](https://github.com/serkanalc/Android-Basics-with-Compose-TR/blob/main/Part%2001%20-%20Kotlin'le%20Programlamaya%20Giri%C5%9F/Codelab%2004%20-%20Kotlin'de%20fonksiyonlar%20olu%C5%9Fturun%20ve%20kullan%C4%B1n/Ba%C5%9Flamadan%20%C3%96nce.md) <br>
📌  [Bir fonksiyonu tanımlayın ve çağırın](#1) <br>
📌  [Bir fonksiyondan bir değer döndürün](#2) <br>
📌  [BirthdayGreeting() fonksiyonuna bir parametre ekleyin](#3) <br>
📌  [Birden çok parametreli fonksiyonlar](#4) <br>



#

# <a name="1"></a>Bir fonksiyonu tanımlayın ve çağırın

fonksiyonları derinlemesine keşfetmeden önce, bazı temel terminolojiyi gözden geçirelim.

- Bir fonksiyonui bildirmek (veya tanımlamak) için `fun` anahtar sözcüğünü kullanır ve bir görevi yürütmek için gereken talimatları içeren kaşlı ayraçlar içinde kodu içerir.

- Bir fonksiyonu çağırmak, o fonksiyonda bulunan tüm kodun yürütülmesine neden olur.

Şimdiye kadar, tüm kodunuzu main() fonksiyonuna yazdınız. main() fonksiyonu aslında kodunuzun hiçbir yerinde çağrılmaz; Kotlin derleyicisi bunu bir başlangıç noktası olarak kullanır. main() fonksiyonu yalnızca, println() fonksiyonuna yapılan çağrılar gibi yürütmek istediğiniz diğer kodları dahil etmek için tasarlanmıştır.

println() fonksiyonu, Kotlin dilinin bir parçasıdır. Ancak, kendi fonksiyonlarınızı tanımlayabilirsiniz. Bu, bir kereden fazla aramanız gerektiğinde kodunuzun yeniden kullanılmasına izin verir. Aşağıdaki programı örnek alın.


```
fun main() {
    println("Doğum günün kutlu olsun, Rover!")
    println("Şimdi 5 yaşındasın!")
}
```
main() fonksiyonu iki println() ifadesinden oluşur; biri Rover'a mutlu yıllar dilemek, diğeri ise Rover'ın yaşını belirtmek.

Kotlin, tüm kodunuzu main() fonksiyonuna koymanıza izin verirken, her zaman istemeyebilirsiniz. Örneğin, programınızın bir Yeni Yıl selamını da içermesini istiyorsanız, ana fonksiyonun bu çağrıları println()'ye de dahil etmesi gerekir. Ya da belki Rover'ı birkaç kez selamlamak istersiniz. Kodu kopyalayıp yapıştırabilir veya doğum günü tebrik için ayrı bir fonksiyon oluşturabilirsiniz. İkincisini yapacaksan. Belirli görevler için ayrı fonksiyonlar oluşturmanın birçok faydası vardır.

- Yeniden kullanılabilir kod: Birden fazla kez kullanmanız gereken kodu kopyalayıp yapıştırmak yerine, gerektiğinde bir fonksiyonu çağırabilirsiniz.

- Okunabilirlik: fonksiyonların yalnızca belirli bir görevi yerine getirmesini sağlamak, diğer geliştiricilerin ve ekip arkadaşlarının yanı sıra gelecekteki benliğinizin bir kod parçasının tam olarak ne yaptığını bilmesine yardımcı olur.


Birfonksiyonu tanımlamanın syntaxı aşağıda gösterilmiştir.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/166845102-970d3db8-a926-4195-91c6-7126bd0093e0.png" />
</p>

Bir fonksiyon tanımı, fun anahtar sözcüğüyle başlar, ardından fonksiyonun adı, bir dizi açma ve kapama parantezleri ve bir dizi açma ve kapama kaşlı ayraçları gelir. Kıvrımlı parantezler içinde, fonksiyon çağrıldığında çalışacak olan kod bulunur.

İki println() ifadesini main() foksiyonundan çıkarmak için yeni bir fonksiyon yaratacaksınız.

1. Tarayıcınızda Kotlin Playground'u açın ve içeriği aşağıdaki kodla değiştirin.

```
fun main() {
    println("Doğum günün kutlu olsun, Rover!")
    println("Şimdi 5 yaşındasın!")
}
```
2. main() fonksiyonundan sonra `birthdayGreeting()` adlı yeni bir fonksiyon tanımlayın. Bu fonksiyon, main() fonksiyonuyla aynı sözdizimi ile bildirilir.

```
fun main() {
    println("Doğum günün kutlu olsun, Rover!")
    println("Şimdi 5 yaşındasın!")
}

fun birthdayGreeting() {
    
}
```

3. main() öğesindeki iki println() ifadesini birthdayGreeting() fonksiyonunun küme parantezlerine taşıyın.

```
fun main() {
   
}

fun birthdayGreeting() {
    println("Doğum günün kutlu olsun, Rover!")
    println("Şimdi 5 yaşındasın!")
}
```

4. main() fonksiyonunda, birthdayGreeting() fonksiyonunu çağırın. Bitmiş kodunuz aşağıdaki gibi görünmelidir.

```
fun main() {
   birthdayGreeting()
}

fun birthdayGreeting() {
    println("Doğum günün kutlu olsun, Rover!")
    println("Şimdi 5 yaşındasın!")
}
```

5. Kodunuzu çalıştırın. Aşağıdaki çıktıyı görmelisiniz.

```
Doğum günün kutlu olsun, Rover!
Şimdi 5 yaşındasın!
    
```
# <a name="2"></a>Bir fonksiyondan bir değer döndürün

Daha karmaşık uygulamalarda, fonksiyonlar metin yazdırmaktan daha fazlasını yapar.

Kotlin fonksiyonları, kodunuzda başka bir yerde kullanabileceğiniz bir değişkende saklanan, *return value (dönüş değeri)* adı verilen verileri de oluşturabilir.

Bir fonksiyon tanımlarken, döndürmesini istediğiniz değerin veri tipini belirleyebilirsiniz. Dönüş türü, parantezlerden sonra iki nokta üst üste (:) ve iki nokta üst üste işaretinden sonra bir türün adı (Int, String, vb.) konularak belirtilir. Dönüş türünden sonra ve açılış küme parantezinden önce tek bir boşluk yerleştirilir. Fonksiyon gövdesi içinde, tüm ifadelerden sonra, fonksiyonun döndürmesini istediğiniz değeri belirtmek için bir return ifadesi kullanırsınız. Bir return ifadesi, return anahtar sözcüğünü ve ardından bir değişken gibi, fonksiyonun çıktı olarak döndürmesini istediğiniz değerden oluşur.

Döndürme türü olan bir fonksiyonu bildirmek için kullanılan sözdizimi aşağıda gösterilmiştir.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/167029363-096bd84f-c1f2-4188-86b0-209c9cd2c25f.png" />
</p>

### Unit türü

Varsayılan olarak, bir iade türü belirtmezseniz, varsayılan iade türü Unit'dir. Unit, fonksiyonun bir değer döndürmediği anlamına gelir. Unit, diğer dillerdeki `void` dönüş türlerine eşdeğerdir (Java ve C'de void; Swift'de Void/empty Tuple (); Python'da Yok, vb.). Bir değer döndürmeyen herhangi bir fonksiyon, örtük olarak Unit döndürür. Unit iade etmek için kodunuzu değiştirerek bunu gözlemleyebilirsiniz.

1. birthdayGreeting() fonksiyon bildiriminde, kapanış parantezinden sonra iki nokta üst üste ekleyin ve dönüş türünü Unit olarak belirtin.

```
fun birthdayGreeting(): Unit {
    println("Doğum günün kutlu olsun, Rover!")
    println("Şimdi 5 yaşındasın!")
}
```
2. Kodu çalıştırın ve her şeyin hala çalıştığını gözlemleyin.

```
Doğum günün kutlu olsun, Rover!
Şimdi 5 yaşındasın!
```

Kotlin'de Birim dönüş türünü belirtmek isteğe bağlıdır. Hiçbir şey döndürmeyen veya Unit döndürmeyen fonksiyonlar için bir return ifadesine ihtiyacınız yoktur.

> Not: Daha sonraki bir codelab'de lambdas adlı bir Kotlin özelliği hakkında bilgi edindiğinizde Unit türünü tekrar göreceksiniz.

### BirthdayGreeting() öğesinden bir String döndürün

Bir fonksiyonun nasıl değer döndürebileceğini göstermek için, yalnızca sonucu yazdırmak yerine birthdayGreeting() fonksiyonunu bir string'e döndürecek şekilde değiştireceksiniz.

1. Unit dönüş türünü String ile değiştirin.

```
fun birthdayGreeting(): Stirng {
    println("Doğum günün kutlu olsun, Rover!")
    println("Şimdi 5 yaşındasın!")
}
```
2. Kodunuzu çalıştırın. Aşağıdaki hatayı alacaksınız. Bir fonksiyon için (örneğin, String) bir dönüş türü bildirirseniz, bu fonksiyonun bir dönüş ifadesi içermesi gerekir. Bir fonksiyondan iki değil yalnızca bir string döndürebilirsiniz, bu nedenle önce her biri için bir değişken oluşturacaksınız: birthdayGreeting ve ageGreeting.

```
A 'return' expression required in a function with a block body ('{...}')
```
3. val anahtar sözcüğünü kullanarak println() deyimlerini iki değişkenle değiştirin. birthdayGreeting() öğesinden println() çağrılarını kaldırdığınız için, birthdayGreeting() öğesinin çağrılması hiçbir şey yazdırmaz.

```
fun birthdayGreeting(): String {
    val nameGreeting = "Doğum günün kutlu olsun, Rover!"
    val ageGreeting = "Şimdi 5 yaşındasın!"
}
```
4. Daha önceki bir kod laboratuvarında öğrendiğiniz string biçimlendirme syntax'ını kullanarak, her iki selamlamadan oluşan fonksiyondan bir string döndürmek için bir return ifadesi ekleyin.

Selamları ayrı bir satırda biçimlendirmek için ayrıca \n kaçış karakterini kullanmanız gerekir. Bu tıpkı önceki bir kod laboratuvarında öğrendiğiniz \$ ve \" kaçış karakterleri gibidir. \n karakteri yeni satırla değiştirilir, böylece iki selamlamanın her biri ayrı bir satırda olur.

```
fun birthdayGreeting(): String {
    val nameGreeting = "Doğum günün kutlu olsun, Rover!"
    val ageGreeting = "Şimdi 5 yaşındasın!"
    return "$nameGreeting\n$ageGreeting"
}
```

5. main() içinde, birthdayGreeting() bir değer döndürdüğünden, sonucu bir string değişkeninde saklayabilirsiniz. DoğumgünüGreeting() çağrısının sonucunu saklamak için val kullanarak bir karşılama değişkeni bildirin.

```
fun main() {
    val greeting = birthdayGreeting()
}
```
6. main() içinde, selamlama stringine yazdırmak için println() öğesini çağırın. main() fonksiyonu şimdi aşağıdaki gibi görünmelidir.

```
fun main() {
    val greeting = birthdayGreeting()
    println(greeting)
}
```

7. Kodunuzu çalıştırın ve sonucun öncekiyle aynı olduğunu gözlemleyin. Bir değer döndürmek, sonucu bir değişkende saklamanıza izin verir, ancak println() fonksiyonunun içinde birthdayGreeting() fonksiyonunu çağırırsanız ne olacağını düşünüyorsunuz?

```
Doğum günün kutlu olsun, Rover!
Şimdi 5 yaşındasın!
```

8. Değişkeni kaldırın ve birthdayGreeting() fonksiyonunu çağırmanın sonucunu println() fonksiyonuna iletin:

```
fun main() {
    println(birthdayGreeting())
}
```

9. Kodunuzu çalıştırın ve çıktıyı izleyin. birthdayGreeting()'i çağırmanın dönüş değeri doğrudan println()'e iletilir.

```
Doğum günün kutlu olsun, Rover!
Şimdi 5 yaşındasın!
```

# <a name="3"></a>BirthdayGreeting() fonksiyonuna bir parametre ekleyin

Gördüğünüz gibi, println()'i çağırdığınızda, parantez içine bir string ekleyebilir veya fonksiyona bir değer iletebilirsiniz. Aynısını birthdayGreeting() fonksiyonunuzla da yapabilirsiniz. Ancak, ilk önce birthdayGreeting() öğesine bir parametre eklemeniz gerekir.

Bir parametre, bir değişkenin adını ve fonksiyon içinde erişilecek veri olarak bir fonksiyona iletebileceğiniz bir veri tipini belirtir. Parametreler, fonksiyon adından sonra parantez içinde belirtilir.

<p align="center">
  <img src="https://user-images.githubusercontent.com/70329389/167032535-a49b4fe7-140c-40ee-bf51-f35cb11599d3.png" />
</p>

Her parametre, iki nokta üst üste ve boşlukla ayrılmış bir değişken adı ve veri türünden oluşur. Birden çok parametre virgülle ayrılır.

Şu anda birthdayGreeting() fonksiyonu yalnızca Rover'ı selamlamak için kullanılabilir. birthdayGreeting() fonksiyonuna bir parametre eklersiniz, böylece fonksiyona ilettiğiniz herhangi bir adı selamlayabilirsiniz.

1. birthdayGreeting() fonksiyonunun parantezleri içinde, sözdizimi adını kullanarak String türünde bir ad parametresi ekleyin.

```
fun birthdayGreeting(name: String): String {
    val nameGreeting = "Doğum günün kutlu olsun, Rover!"
    val ageGreeting = "Şimdi 5 yaşındasın!"
    return "$nameGreeting\n$ageGreeting"
}
```

Önceki adımda tanımlanan parametre, val anahtar sözcüğü ile bildirilen bir değişken gibi çalışır. Değeri, birthdayGreeting() fonksiyonunda herhangi bir yerde kullanılabilir. Daha önceki bir codelab'de, bir değişkenin değerini bir stringe nasıl ekleyebileceğinizi öğrenmiştiniz.

nameGreeting dizesindeki Rover'ı $ sembolü ve ardından name parametresi ile değiştirin.

```
fun birthdayGreeting(name: String): String {
    val nameGreeting = "Doğum günün kutlu olsun, $name!"
    val ageGreeting = "Şimdi 5 yaşındasın!"
    return "$nameGreeting\n$ageGreeting"
}
```

3. Kodunuzu çalıştırın ve hatayı gözlemleyin. Artık name parametresini bildirdiğinize göre, birthdayGreeting()'i aradığınızda bir String girmeniz gerekiyor. Parametre alan bir fonksiyonu çağırdığınızda, fonksiyona bir argüman iletirsiniz. Argüman, "Rover" gibi ilettiğiniz değerdir.

```
No value passed for parameter 'name'
```
4. "Rover"ı main() içindeki birthdayGreeting() çağrısına iletin.

```
fun main() {
    println(birthdayGreeting("Rover"))
}
```

5. Kodunuzu çalıştırın ve çıktıyı izleyin. Rover adı, ad parametresinden gelir.

```
Doğum günün kutlu olsun, Rover!
```
6. birthdayGreeting() bir parametre aldığından, onu Rover dışında bir adla çağırabilirsiniz. "Rex" bağımsız değişkenini ileterek, println() çağrısının içine birthdayGreeting() öğesine başka bir çağrı ekleyin.

```
println(birthdayGreeting("Rover"))
println(birthdayGreeting("Rex"))

```

7. Kodu tekrar çalıştırın ve çıktının birthdayGreeting()'e iletilen bağımsız değişkene göre farklılık gösterdiğini gözlemleyin.


> Not: Genellikle birbirinin yerine kullanıldıklarını bulsanız da, parametre ve argüman aynı şey değildir. Bir fonksiyon tanımladığınızda, ona iletilebilecek parametreleri tanımlarsınız. Bir fonksiyonu çağırdığınızda, parametreler için argümanlar iletirsiniz. Parametreler, ad değişkeni gibi fonksiyon tarafından erişilebilen değişkenlerdir; bağımsız değişkenler ise "Rover" dizesi gibi ilettiğiniz gerçek değerlerdir.

> Uyarı: Bir fonksiyonuun bir parametreye iletilen değeri değiştirebildiği Java gibi bazı dillerin aksine, Kotlin'deki parametreler değişmezdir. İşlev gövdesi içinden bir parametrenin değerini yeniden atayamazsınız.

# <a name="4"></a>Birden çok parametreli fonksiyonlar












