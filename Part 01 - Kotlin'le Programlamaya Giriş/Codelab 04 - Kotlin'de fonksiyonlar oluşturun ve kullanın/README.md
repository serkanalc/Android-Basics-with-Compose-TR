### Konu Başlıkları:


📌  [Başlamadan Önce](https://github.com/serkanalc/Android-Basics-with-Compose-TR/blob/main/Part%2001%20-%20Kotlin'le%20Programlamaya%20Giri%C5%9F/Codelab%2004%20-%20Kotlin'de%20fonksiyonlar%20olu%C5%9Fturun%20ve%20kullan%C4%B1n/Ba%C5%9Flamadan%20%C3%96nce.md) <br>
📌  [Bir fonksiyonu tanımlayın ve çağırın](#1) <br>

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


