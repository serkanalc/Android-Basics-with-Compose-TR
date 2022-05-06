# Alıştırma Problemleri: Kotlin Temelleri

### Konu Başlıkları:


📌  [Başlamadan Önce](https://github.com/serkanalc/Android-Basics-with-Compose-TR/blob/main/Part%2001%20-%20Kotlin'le%20Programlamaya%20Giri%C5%9F/Codelab%2004%20-%20Kotlin'de%20fonksiyonlar%20olu%C5%9Fturun%20ve%20kullan%C4%B1n/Ba%C5%9Flamadan%20%C3%96nce.md) <br>
📌  [Print mesajı](#1) <br>
📌  [Derleme hatasını düzeltin](#2) <br>
📌  [String şablonları](#3) <br>
📌  [String birleştirme](#4) <br>
📌  [Mesaj biçimlendirme](#5) <br>
📌  [Temel matematik işlemlerini uygulayın](#6) <br>
📌  [Varsayılan parametreler](#7) <br>
📌  [Adımsayar](#8) <br>
📌  [İki sayıyı karşılaştır](#9) <br>
📌  [Yinelenen kodu bir fonksiyona taşı](#10) <br>


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

Kod çalışır, ancak iki sayı ekleme mantığı, sonuç değişkeninde bulunur ve bu, kodunuzu yeniden kullanmak için daha az esnek hale getirir. Bunun yerine, kodun yeniden kullanılabilir olması için ekleme işlemini bir add() fonksiyonu çıkarabilirsiniz. Bunu yapmak için kodunuzu aşağıda listelenen kodla güncelleyin. Kodun şimdi ThirdNumber adında yeni bir değer sunduğuna ve bu yeni değişkenin sonucunu firstNumber ile yazdırdığına dikkat edin.

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

// Bu satırın altında add() fonksiyonlarını tanımlayın
```

Programın bu çıktıyı yazdırması için add() fonksiyonunu tanımlayabilir misiniz?

```
10 + 5 = 15
10 + 8 = 18
```
### Aşama 3

Artık iki sayı eklemek için yeniden kullanılabilir bir fonksiyonlarınız var.

subtract() fonksiyonlarını, add() fonksiyonunu uyguladığınız gibi uygulayabilir misiniz?
İpucu: Toplama, çıkarma ve diğer matematik işlemleri arasındaki farkı düşünün. Oradan çözüm kodu üzerinde çalışmaya başlayın.

# <a name="7"></a>Alıştırma 7 - Varsayılan parametreler

Gmail, yeni bir cihazda oturum açma girişiminde bulunulduğunda kullanıcıya bildirim gönderen bir özelliğe sahiptir.

Bu alıştırmada, bu mesaj şablonuyla kullanıcılara bir mesaj görüntüleyen bir program yazacaksınız:

```
Google Hesabı e-posta kimliğiniz için işletim Sisteminde yeni bir oturum açma isteği var.
```
Bir OperatingSystem parametresini ve bir emailId parametresini kabul eden, verilen biçimde bir mesaj oluşturan ve mesajı döndüren bir fonksiyon uygulamanız gerekir.

Örneğin, fonksiyon, OperatingSystem için "Chrome OS" ve e-posta kimliği için "sample@gmail.com" ile çağrıldıysa, şu dizeyi döndürmelidir:

```
Google Hesabınızın sample@gmail.com için Chrome OS'de yeni bir oturum açma isteği var.
```
### Aşama 1

1. Görüntülenen çıktıyı yazdırması için bu programda displayAlertMessage() fonksiyonunu uygulayabilir misiniz?

```
fun main() {
    val operatingSystem = "Chrome OS"
    val emailId = "sample@gmail.com"

    println(displayAlertMessage(operatingSystem, emailId))
}

// DisplayAlertMessage()'ınızı bu satırın altında tanımlayın.
```
2. Programınız bu çıktıyı yazdırıyor mu?

```
Google Hesabınızın sample@gmail.com için Chrome OS'de yeni bir oturum açma isteği var
```

### Adım 2

Mesajı görüntülediniz. Ancak bazı durumlarda, kullanıcının işletim sistemini belirleyemeyeceğinizi keşfedersiniz. Bu gibi durumlarda işletim sistemi adını Bilinmeyen OS olarak belirtmeniz gerekir. fonksiyon her çağrıldığında Bilinmeyen İşletim Sistemi bağımsız değişkenini iletmenize gerek kalmaması için kodu daha da optimize edebilirsiniz.

1. Kodu bu çıktıyı yazdıracak şekilde bu bilgilerle optimize etmenin bir yolunu bulabilir misiniz?

```
user_one@gmail.com Google Hesabınız için Bilinmeyen İşletim Sisteminde yeni bir oturum açma isteği var.

Windows'ta user_two@gmail.com Google Hesabınız için yeni bir oturum açma isteği var.

Mac OS'de user_ Three@gmail.com Google Hesabınız için yeni bir oturum açma isteği var.
```
main() fonksiyon uygulamasını bununla değiştirin:

fun main() {
    val firstUserEmailId = "user_one@gmail.com"

    // Aşağıdaki kod satırı, parametrenizi emailId olarak adlandırdığınızı varsayar.
     // Farklı bir şekilde adlandırdıysanız, adı güncellemekten çekinmeyin.
    println(displayAlertMessage(emailId = firstUserEmailId))
    println()

    val secondUserOperatingSystem = "Windows"
    val secondUserEmailId = "user_two@gmail.com"

    println(displayAlertMessage(secondUserOperatingSystem, secondUserEmailId))
    println()

    val thirdUserOperatingSystem = "Mac OS"
    val thirdUserEmailId = "user_three@gmail.com"

    println(displayAlertMessage(thirdUserOperatingSystem, thirdUserEmailId))
    println()
}

# <a name="8"></a>Alıştırma 8 - Adımsayar

Adımsayar, atılan adım sayısını sayan elektronik bir cihazdır. Günümüzde neredeyse tüm cep telefonları, akıllı saatler ve fitness ekipmanları, içinde yerleşik adım sayarlarla birlikte gelir. Sağlık ve fitness uygulaması, atılan adım sayısını hesaplamak için yerleşik adımsayarları kullanır. Bu fonksiyon, kullanıcının adım sayısına bağlı olarak kullanıcının yaktığı kalori sayısını hesaplar.

1. En iyi uygulamalara dayalı olarak bu programdaki fonksiyonları, fonksiyon parametrelerini ve değişkenleri yeniden adlandırabilir misiniz?

```
fun main() {
    val Steps = 4000
    val caloriesBurned = PEDOMETERstepsTOcalories(Steps);
    println("$Steps adım yürümek $caloriesBurned kalori yaktırır") 
}

fun PEDOMETERstepsTOcalories(NumberOFStepS: Int): Double {
    val CaloriesBURNEDforEachStep = 0.04
    val TotalCALORIESburned = NumberOFStepS * CaloriesBURNEDforEachStep
    return TotalCALORIESburned
}
```
# <a name="9"></a>Alıştırma 9 - İki sayıyı karşılaştır

Modern cep telefonlarında, ekran başında geçirilen süreyi veya her gün telefonunuzda geçirdiğiniz süreyi izleyen yerleşik bir özellik bulunur.

Bu alıştırmada, bugün telefonunuzda geçirdiğiniz süre ile dün geçirdiğiniz süreyi dakika cinsinden karşılaştıran bir fonksiyon uygulayacaksınız. fonksiyon, iki tamsayı parametresini kabul eder ve bir boolean değeri döndürür.

İlk parametre bugün harcadığınız dakika sayısını ve ikinci parametre dün harcadığınız dakika sayısını tutar. Düne kıyasla bugün telefonda daha fazla zaman geçirdiyseniz, fonksiyon gerçek bir değer döndürür. Aksi takdirde, yanlış bir değer döndürür.

Örneğin, fonksiyonu bu adlandırılmış bağımsız değişkenlerle çağırdıysanız:

- timeSpentToday = 300 ve timeSpentYesterday = 250, fonksiyon gerçek bir değer döndürür.
- timeSpentToday = 300 ve timeSpentYesterday = 300, fonksiyon yanlış bir değer döndürür.
- timeSpentToday = 200 ve timeSpentYesterday = 220, fonksiyon yanlış bir değer döndürür.

İpucu: > karşılaştırma operatörü, operatörden önceki değer kendisinden sonraki değerden büyükse gerçek bir değer döndürür. Aksi takdirde, yanlış bir değer döndürür.

# <a name="10"></a>Alıştırma 10 - Yinelenen kodu bir fonksiyona taşı

Bu program, farklı şehirler için hava durumunu görüntüler. Şehir adını, günün yüksek ve düşük sıcaklıklarını ve yağmur ihtimalini içerir.

```
fun main() {
    println("Şehir: Ankara")
    println("Düşük sıcaklık: 27, Yüksek sıcaklık: 31")
    println("Yağmur yağma ihtimali: 82%")
    println()

    println("Şehir: Tokyo")
    println("Düşük sıcaklık: 32, Yüksek sıcaklık: 36")
    println("Yağmur yağma ihtimali: 10%")
    println()
    
    println("Şehir: Cape Town")
    println("Düşük sıcaklık: 59, Yüksek sıcaklık: 64")
    println("Yağmur yağma ihtimali: 2%")
    println()
    
    println("Şehir: Guatemala City")
    println("Düşük sıcaklık: 50, Yüksek sıcaklık: 55")
    println("Yağmur yağma ihtimali: 7%")
    println()
}
```
Her şehir için hava durumunu yazdıran kodda birçok benzerlik var. Örneğin, "Şehir:" ve "Düşük sıcaklık:" gibi birden çok kez tekrarlanan ifadeler vardır. Benzer şekilde tekrarlanan kod, programınızda hata riski oluşturur. Şehirlerden birinde yazım hatası olabilir veya hava durumu ayrıntılarından birini unutabilirsiniz.

1. main() fonksiyonundaki tekrarı azaltmak için tek bir şehir için hava durumu ayrıntılarını yazdıran ve ardından kalan şehirler için aynısını yapan bir fonksiyon oluşturabilir misiniz?
2. Her şehir için oluşturduğunuz fonksiyonu çağırmak ve uygun hava durumu ayrıntılarını argüman olarak iletmek için main() fonksiyonunu güncelleyebilir misiniz?

