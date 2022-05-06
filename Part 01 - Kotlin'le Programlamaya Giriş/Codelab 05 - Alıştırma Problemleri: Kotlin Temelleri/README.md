# Alıştırma Problemleri: Kotlin Temelleri

### Konu Başlıkları:


📌  [Başlamadan Önce](https://github.com/serkanalc/Android-Basics-with-Compose-TR/blob/main/Part%2001%20-%20Kotlin'le%20Programlamaya%20Giri%C5%9F/Codelab%2004%20-%20Kotlin'de%20fonksiyonlar%20olu%C5%9Fturun%20ve%20kullan%C4%B1n/Ba%C5%9Flamadan%20%C3%96nce.md) <br>
📌  [Bir fonksiyonu tanımlayın ve çağırın](#1) <br>
📌  [Bir fonksiyonu tanımlayın ve çağırın](#2) <br>
📌  [Bir fonksiyonu tanımlayın ve çağırın](#3) <br>
📌  [Bir fonksiyonu tanımlayın ve çağırın](#4) <br>
📌  [Bir fonksiyonu tanımlayın ve çağırın](#5) <br>
📌  [Bir fonksiyonu tanımlayın ve çağırın](#6) <br>
📌  [Bir fonksiyonu tanımlayın ve çağırın](#7) <br>
📌  [Bir fonksiyonu tanımlayın ve çağırın](#8) <br>
📌  [Bir fonksiyonu tanımlayın ve çağırın](#9) <br>
📌  [Bir fonksiyonu tanımlayın ve çağırın](#10) <br>
📌  [Bir fonksiyonu tanımlayın ve çağırın](#11) <br>

#

# <a name="1"></a>Alıştırma 1 - Print mesajı

Bu yolda öğrendiklerinizi arkadaşlarınıza anlatın.

Bu mesajları dört ayrı satıra yazdıran bir main() fonksiyonu yazabilir misiniz?

```
Değer değişmediğinde val anahtar sözcüğünü kullanın.
Değer değişebildiğinde var anahtar sözcüğünü kullanın.
Bir fonksiyon tanımladığınızda, ona iletilebilecek parametreleri tanımlarsınız.
Bir fonksiyonu çağırdığınızda, parametreler için argümanlar iletirsiniz.
```
# <a name="2"></a>Alıştırma 2 - Derleme hatasını düzeltin

Bu program, kullanıcıya bir arkadaştan sohbet mesajı aldıklarını bildiren bir mesaj yazdırır.

```
fun main() { 
    println("Bir arkadaştan yeni sohbet mesajı'}
}
```
1. Bu programdaki derleme hatalarının temel nedenini bulup düzeltebilir misiniz?
2. Kod, dize ve fonksiyon bağımsız değişkeninin açılıp kapanmasını belirtmek için uygun semboller kullanıyor mu?

İpucu: Kodu çalıştırmak ve derleme hatalarını görüntülemek için Kotlin Playground'u kullanabilirsiniz.

Hataları düzelttikten sonra, program hatasız derlenmeli ve şu çıktıyı yazdırmalıdır:

```
Bir arkadaştan yeni sohbet mesajı
```
# <a name="3"></a>Alıştırma 3 - String şablonları

Bu program, kullanıcıları belirli bir ürünle ilgili yaklaşan promosyon satışı hakkında bilgilendirir. Yüzde iskontosu için indirim Yüzdesi değişkenine ve indirimdeki öğe için madde değişkenine dayanan bir string şablonuna sahiptir. Ancak kodda derleme hataları var.

```
fun main() {
    val discountPercentage: Int = 0
    val offer: String = ""
    val item = "Google Chromecast"
    discountPercentage = 20
    offer = "İndirim - $item de $discountPercentage% indirim var ! Acele edin!"
    
    println(offer)
}
```
1. Hataların temel nedenini bulup düzeltebilir misiniz?
2. Kotlin Playground'da kodu çalıştırmadan önce bu programın çıktısını belirleyebilir misiniz?

İpucu: Salt okunur bir değişkene yeniden değer atayabilir misiniz?

Hataları düzelttikten sonra, program hatasız derlenmeli ve şu çıktıyı yazdırmalıdır:

# <a name="4"></a>Alıştırma 4 - String birleştirme

Bu program toplam parti boyutunu görüntüler. Partide yetişkinler ve çocuklar var. NumberOfAdults değişkeni partideki yetişkin sayısını, numberOfKids değişkeni ise çocuk sayısını tutar.

```
fun main() {
    val numberOfAdults = "20"
    val numberOfKids = "30"
    val total = numberOfAdults + numberOfKids
    println("toplam parti boyutu: $total")
}
```
### Aşama 1

- Kotlin Playground'da kodu çalıştırmadan önce bu programın çıktısını belirleyebilir misiniz?

Çıktıyı belirledikten sonra, kodu Kotlin Playground'da çalıştırın ve çıktınızın görüntülenen çıktıyla eşleşip eşleşmediğini kontrol edin.

İpucu: + operatörünü iki dizede kullandığınızda ne olur?

### Adım 2
Kod çalışır ve bazı çıktıları yazdırır, ancak çıktı partiye katılan toplam insan sayısını göstermez.

Sorunu kodda bulabilir ve bu çıktıyı yazdıracak şekilde düzeltebilir misiniz?

# <a name="5"></a>Alıştırma 5 - Mesaj biçimlendirme

Bu program, bir çalışanın bu ay aldığı toplam maaşı gösterir. Toplam maaş, çalışanın her ay aldığı temel maaş değişkeni ve çalışana verilen ek ikramiye olan bonusAmount  değişkeni olmak üzere iki kısma ayrılır.

```
fun main() {
    val baseSalary = 5000
    val bonusAmount = 1000
    val totalSalary = "$baseSalary + $bonusAmount"
    println("Bonusunuz için tebrikler! Toplam $totalSalary(ek bonus) alacaksınız.).")
}
```
1. Kotlin Playground'da çalıştırmadan önce bu kodun çıktısını bulabilir misiniz?
2. Kodu Kotlin Playground'da çalıştırdığınızda beklediğiniz çıktıyı yazdırıyor mu?

# <a name="6"></a>Alıştırma 6 - Temel matematik işlemlerini uygulayın

Bu alıştırmada, temel matematik işlemlerini gerçekleştiren ve çıktıyı yazdıran bir program yazacaksınız.

### Aşama 1

Bu main() fonksiyonu bir derleme hatası içerir:

```
fun main() {
    val firstNumber = 10
    val secondNumber = 5
    
    println("$firstNumber + $secondNumber = $result")
}
```
Programın bu çıktıyı yazdırması için hatayı düzeltebilir misiniz?

```
10 + 5 = 15
```
### Adım 2

Kod çalışır, ancak iki sayı ekleme mantığı, sonuç değişkeninde bulunur ve bu, kodunuzu yeniden kullanmak için daha az esnek hale getirir. Bunun yerine, kodun yeniden kullanılabilir olması için ekleme işlemini bir add() işlevine çıkarabilirsiniz. Bunu yapmak için kodunuzu aşağıda listelenen kodla güncelleyin. Kodun şimdi ThirdNumber adında yeni bir değer sunduğuna ve bu yeni değişkenin sonucunu firstNumber ile yazdırdığına dikkat edin.

```
fun main() {
    val firstNumber = 10
    val secondNumber = 5
    val thirdNumber = 8
    
    val result = add(firstNumber, secondNumber)
    val anotherResult = add(firstNumber, thirdNumber)

    println("$firstNumber + $secondNumber = $result")
    println("$firstNumber + $thirdNumber = $anotherResult")
}

// Bu satırın altında add() işlevini tanımlayın
```

Programın bu çıktıyı yazdırması için add() işlevini tanımlayabilir misiniz?

```
10 + 5 = 15
10 + 8 = 18
```
### Aşama 3

Artık iki sayı eklemek için yeniden kullanılabilir bir işleviniz var.

subtract() işlevini, add() işlevini uyguladığınız gibi uygulayabilir misiniz?
İpucu: Toplama, çıkarma ve diğer matematik işlemleri arasındaki farkı düşünün. Oradan çözüm kodu üzerinde çalışmaya başlayın.

# <a name="7"></a>Alıştırma 7 - Temel matematik işlemlerini uygulayın
