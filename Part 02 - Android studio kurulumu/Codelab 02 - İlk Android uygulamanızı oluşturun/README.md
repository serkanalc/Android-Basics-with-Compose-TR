#  İlk Android Uygulamanızı Oluşturun

### Konu Başlıkları:



📌  [Başlamadan Önce](https://github.com/serkanalc/Android-Basics-with-Compose-TR/blob/main/Part%2002%20-%20Android%20studio%20kurulumu/Codelab%2002%20-%20İlk%20Android%20uygulamanızı%20oluşturun/Başlamadan%20Önce.md) <br>
📌  [Şablon kullanarak bir proje yaratın](#1) <br>
📌  [Proje dosyalarını bulun](#2) <br>
📌  [Metini güncelleyin](#3) <br>
📌  [Arka plan rengini değiştirin](#4) <br>
📌  [Dolgu ekleyin](#5) <br>
📌  [Çözüm kodunu gözden geçirin](#6) <br>





# <a name="1"></a>Şablon kullanarak bir proje yaratın


Bu codelab’de Android Studio’nun size sağladığı Empty Compose Activity proje şablonunu kullanarak bir Android uygulaması yaratacaksınız.

Android Studio’da bir proje yaratmak için:

1.  Android Studio’yu başlatmak için Android Studio imgesine iki kez tıklayın
    
2.  **Welcome to Android Studio** diyaloğunda **New Project**’e tıklayın. **New Project** sayfası Android Studio tarafından size sağlanan bir şablon listesi sunacak. Android Studio’da, proje şablonu belirli uygulamaların blueprintini sağlayan bir Android projesidir. Şablonlar projeniz için Android Studio’nun projenizi kurması için gerekli olan temeli ve gerekli dosyaları yaratır. Seçtiğiniz şablona göre daha hızlı ilerlemeniz için başlangıç kodunu temin eder.
    
3.  **Phone and Tablet** tab’ının seçili olduğundan emin olun.
    
4.  **Empty Compose Activity** şablonuna, projenizin şablonu olarak seçmek için tıklayın. **Empty Compose Activity şablonu**, Compose uygulaması yaratmak için kullanabileceğiniz basit bir proje yaratmak için kullanabileceğiniz şablondur. Tek bir ekranı vardır ve “**Hello Android**” yazısını gösterir.
    
5.  **Next**’e tılayın. **New Project** diyaloğu açılacaktır. Burada projenizi yapılandırmak için alanlar vardır.
    
6.  Projenizi aşağıdaki gibi yapılandırın:
    

**Name** alanı projenizin ismi için kullanılır, bu codelab için “Greeting Card” yazın.

**Package name** alanını olduğu gibi bırakın. Bu sayede dosya yapısında dosyalarınız düzenli bir şekilde duracaktır. Bu yüzden dosyanızın ismi com.example.greetingcard olacaktır.

**Save location** alanını olduğu gibi bırakın. Bu alan projeniz ile ilgili bütün dosyaların nerede kayıtlı kaldığını içerir. Dosyalarınızın nerede olduğunu not edin ki dosyalarınızı kolayca bulabilin.

**Language** alanında **Kotlin** seçili olacaktır. Bu alan projeniz için hangi programlama dilini kullanmak istediğinizi belirler. Compose sadece Kotlin ile uyumlu olduğu için bu alanda değişiklik yapamazsınız.

**Minimum SDK** alanındaki menüden **API 21: Android 5.0 (Lollipop)**’u seçin. [Minimum SDK](https://developer.android.com/guide/topics/manifest/uses-sdk-element), uygulamanızın çalışabileceği minimum Android versiyonunu belirtir.

**Use legacy android.support libraries** onay kutucuğu onaylanmamış işaretlenmemiş bir şekilde olacaktır.

7.  **Finish**’e basın. Bu biraz vakit alacaktır -bir kahve için harika bir zaman! Android Studio kurulurken, Android Studio’nun hala projenizi kurduğuna dair bir ilerleme çubuğu ve bir mesaj belirecektir. Bunun gibi gözükebilir:
    

Proje kurulumunuzun yaratıldığını size bildiren bir mesaj belirecektir.

8.  **What’s New** pane’i Android Studio’nun yeni özellikleri içeren güncellemeler gözükecektir. Bu sayfayı şimdilik kapatın.
    
9.  Android Studio’nun sağ üst köşesindeki **Split**’e tıklayın, bu hem kodlamayı hem de dizaynı görüntülemenize yardımcı olacaktır. Ayrıca **Code**’a tıklayarak sadece kodlamayı veya **Design**’a tıklayarak sadece dizaynı görüntüleyebilirsiniz.
    

**Split**’e tıkladıktan sonra üç alan görmelisiniz:

-   **Project** görüntüsü (1) projenizin dosyalarını ve klasörlerini gösterir
    
-   **Code** görüntüsü (2) kodlamayı düzenleyebileceğiniz kısımdır
    
-   **Design** görüntüsü (3) uygulamanızın önizlenimini yapabileceğiniz kısımdır
    

**Design** görüntüsünde, şu metini göreceğiniz boş bir pencere göreceksiniz:

10.  **Build & Refresh**’e tıklayın. Bu yapılanma biraz vakit alabilir ama bittiğinde önizlenim “**Hello Android!**” yazısını içeren bir metin kutusu çıkacaktır. Empty Compose aktivitesi bu uygulamayı yaratmanız için gerekli tüm kodları içerir.


# <a name="2"></a>Proje dosyalarını bulun


Bu bölümde dosya yapılandırmasıyla ilgili daha bilgi sahibi olarak Android Studio’yu keşfetmeye devam edeceksiniz.

1.  Android Studio’da, **Project** sekmesine bir bakın. **Project** şeriti projenizin dosyalarını ve klasörlerini size gösterir. Projenizi kurarken paket isminiz **com.example.greetingcard** idi. Sizin de görebileceğiniz üzere paket tam olarak burada Project sekmesindedir. Paket aslında kodlamanızın bulunduğu klasördür. Android Studio projenizi, paketlerden oluşan yönlendirici bir yapıda düzenler.
    
2.  Eğer gerekliyse, **Project** sekmesinde aşağı açılan menüden **Android**’i seçin.
    

  

Bu kullandığınız dosyaların standart görünümü ve organizasyonudur. Projeniz için kod yazdığınız zaman kullanışlıdır çünkü uygulamanızda üzerinde çalıştığınız dosyalara kolay erişmenize yardımcı olur. Fakat dosyalarınıza dosya tarayıcısıyla bakarsanız, Finder veya Windows Explorer gibi, dosya düzeni farklı bir şekilde olacaktır.

3.  Aşağı açılan menüden **Project Source Files**’ı seçin. Artık dosyalarınızı herhangi bir dosya tarayıcısında olduğu gibi aratabilirsiniz.
    
4.  Önceki görüntüye geri gelmek için tekrar **Android**’i seçin. Bu kurs için Android görüntüsünü kullandınız. Eğer dosya yapınız farklı gözükürse, hala Android görüntüsünde olduğunuzdan emin olmak için kontrol edin.
    


# <a name="3"></a>Metini güncelleyin


Android Studio’yu iyice tanıdığınıza göre kutlama kartınızı yapmanın vakti geldi!

  

`MainActivity.kt` dosyasında **Code** görüntüsüne bakın. Fark edeceksinizdir ki burada otomatik olarak yaratılan fonksiyonlar olacaktır, spesifik olarak `onCreate()` ve `setContent()` fonksiyonları.

  

> Not: Unutmayın ki fonksiyon, bir programın belirli bir görevi yerine getiren bir segmenttir.


```kotlin
class MainActivity : ComponentActivity() {
   override fun onCreate(savedInstanceState: Bundle?) {
       super.onCreate(savedInstanceState)
       setContent {
           GreetingCardTheme {
               // A surface container using the 'background' color from the theme
               Surface(
                   modifier = Modifier.fillMaxSize(),
                   color = MaterialTheme.colors.background
               ) {
                   Greeting("Android")
               }
           }
       }
   }
}
```

`onCreate()` fonksiyonu bu uygulamanın başlangıç noktasıdır ve diğer fonksiyonları bir kullanıcı arayüzü yaratmak için çağırır. Kotlin programlarında `main()` fonksiyonu, kodunuzdaki Kotlin derleyicisinin başladığı spesifik bir yerdir. Android programlarında, `onCreate()` fonksiyonu bu rolü yerine getirir.

`onCreate()` fonkisyonunun içindeki `setContent()` fonskiyonu, composable fonksiyonlar aracılığıyla sizin düzeninizi tanımlamak için kullanılır. `@Composable` annotationıyla işaretletnen tüm fonksiyonlar `setContent()` fonksiyonuyla veya diğer Composable fonksiyonlarla çağırılabilir. Annotation, Kotlin derleyicisine bu fonksiyonun Jetpack Compose tarafından UI'n yaratılması için kullanıldığını söyler.

> Not: Derleyici yazdığınız Kotlin kodunu alır,koda satır satır bakar, ve bilgisayarın anlayabileceği bir hale çevirir. Bu sürece kod derlemesi denir.

Şimdi, `Greeting()` fonksiyonuna bakın. `Greeting()` fonksiyonu bir Composable fonksiyondur, dikkat ederseniz ki üzerinde `@Composable` annotationı olacaktır. Composable fonksiyonlar bazı inputları alır ve ekranda gözükeni yaratır.

```kotlin
@Composable
fun Greeting(name: String) {
   Text(text = "Hello $name!")
}
```
Fonksiyonları daha önce öğrendiniz (eğer hatırlamak isterseniz, Create kısmını ziyaret edin ve Kotlin codlab'inde fonksiyonları kullanın), ama composable fonksiyonların birkaç farklılığı vardır.
- `@Composable` fonksiyonların ismi büyük harfle başlar.
- Fonksiyondan önce `@Composable` annotationını koyarsınız.
- `@Composable` fonksiyonlar return edemez.

```kotlin
@Composable
fun Greeting(name: String) {
   Text(text = "Hello $name!")
}
```

Şu an `Greeting()` bir ismi alır ve o kişiye `Hello` yazısını gösterir.
1. `Greeting()` fonksiyonunu kendinizi tanıtmak için güncelleyin.

```kotlin
@Composable
fun Greeting(name: String) {
   Text(text = "Hi, my name is $name!")
}
```

2.Dizayn pane'inin sol üst köşesindeki 🔁 butonuna basarak **DefaultPreview**'u tekrar build edin:

Harika! Metini değiştirdiniz, ama sizi Android olarak tanıtıyor, ki büyük ihtimalle isminiz bu değil. Şimdi, kişiselleştirin ki sizi isminizle tanıtsın!

`DefaultPreview()` fonksiyonu tüm uygulamayı yeniden build etmeden uygulamanızın nasıl gözüktüğünü görmenize yardımcı olan harika bir özelliktir. Preview fonksiyonu olmak için `@Preview` annotationını yazmanız gerekir.

Görebileceğiniz üzere, `@Preview` annotationı `showBackground` parametresinde yer alır. Eğer `showBackground` **true** olarak kurulduysa, uygulama önizleniminize bir arkaplan ekleyecektir.

Android Studio editör için açık bir tema kullandığı için, `showBackground`=true ve `showBackground`=false arasındaki farkı görmenizbiraz zor olabilir. Bununla birlikte, koyu temayla açık tema arasındaki fark bu şekildedir. True olarak kurulan fotoğrafta arka plandaki beyazlığa dikkat edin.

3. `DefaultPreview()`'u kendi isminizle güncelleyin. Sonra yeniden buildleyin ve kişiselleştirilmiş greeting card'ınıza bir göz atın!

```kotlin
@Preview(showBackground = true)
@Composable
fun DefaultPreview() {
   GreetingCardTheme {
       Greeting("Meghan")
   }
}
```
# <a name="4"></a>Arka plan rengini değiştirin

Artık tanıtım metininiz var, ama şimdilik biraz sıkıcı duruyor! Bu bölümde, arka plan rengini değiştirmeyi öğreneceksiniz. 

Tanıtımınız için farklı bir arka plan rengi kurmak için metninizi bir `Surface` ile çevrelemeniz gerekiyor. `Surface`, arayüzün arka plan rengini veya border'ını değiştirebileceğiniz bir bölümünü temsil eden bir container'dır. 
1. Metini `Surface` ile çevrelemek için, metinin satırını highlightlayın, basın (Windows için `Alt+Enter` veya Mac için `Option+Enter`) sonra **Surround with widget**'ı seçin. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/127443136/224383553-cc8d828c-0ec8-433f-8a41-1a91b6f02d14.png" />
</p>

2. **Surround with Container**'ı seçin.

<p align="center">
  <img src="https://user-images.githubusercontent.com/127443136/224383687-b0b9ee4f-4d4f-4e0e-bf47-82f52c74d167.png" />
</p>

Default container size `Box`'ı verecektir, ama siz bunu başka bir container tipiyle değiştirebilirsiniz.

<p align="center">
  <img src="https://user-images.githubusercontent.com/127443136/224384395-30c26b5d-90d3-4d72-b526-cc26f049f726.png" />
</p>

3. `Box`'ı silin ve yerine `Surface()` yazın.

```kotlin
@Composable
fun Greeting(name: String) {
   Surface() {
       Text(text = "Hi, my name is $name!")
   }
}
```

4. `Surface` container'ı `color` parametresine sahiptir, `Color`'a kurun.

```kotlin
@Composable
fun Greeting(name: String) {
   Surface(color = Color) {
       Text(text = "Hi, my name is $name!")
   }
}
```

5. Color yazdığınızda kırmızı ve altı çizili olduğunu görebilirsiniz. Bunu çözmek için dosyanın yukarısına çıkınız ve import yazısının yanındaki üç noktaya tıklayınız.

<p align="center">
  <img src="https://user-images.githubusercontent.com/127443136/224386028-58927a3f-8029-4901-b411-1d453532deca.png" />
</p>

6. Bu ifadeyi import listesinin sonuna ekleyiniz.

```kotlin
import androidx.compose.ui.graphics.Color
```

Tüm import listesi bu şekilde gözükecektir:

```kotlin
import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.layout.fillMaxSize
import androidx.compose.material.MaterialTheme
import androidx.compose.material.Surface
import androidx.compose.material.Text
import androidx.compose.runtime.Composable
import androidx.compose.ui.Modifier
import androidx.compose.ui.tooling.preview.Preview
import com.example.myapplication.ui.theme.GreetingCard
import androidx.compose.ui.graphics.Color
```

7. Kodunuzda, import listesini alfabe sırasına göre tutmak işinizi kolaylaştıracaktır. Bunu yapmak için yukarıdaki araç çubuğundan **Help**'e basın, oraya **Optimize Imports** yazın ve **Optimize Imports**'a tıklayın. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/127443136/224387288-055f3c06-32f3-439b-8f92-48bbebaace5e.png" />
</p>

Şimdi tüm liste bu şekilde gözükecektir:

```kotlin
import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.layout.fillMaxSize
import androidx.compose.material.MaterialTheme
import androidx.compose.material.Surface
import androidx.compose.material.Text
import androidx.compose.runtime.Composable
import androidx.compose.ui.Modifier
import androidx.compose.ui.graphics.Color
import androidx.compose.ui.tooling.preview.Preview
import com.example.myapplication.ui.theme.GreetingCard
```

8. Dikkat ederseniz Surface parantezinin içine yazdığınız Color kırmızı renkte ve altı çizili olmaktan altı kırmızı renkle çizili hale gelmiş olacaktır. Bunu düzeltmek için sonuna nokta koyun. Açılan listede farklı renk seçeneklerinin olduğunu göreceksiniz. 
Bu Android Studio'daki harika eklentilerden biri, akıllı ve yapabildiğinde size yardım eder. Bu durumda belirli bir renk seçmek istediğinizi biliyor ve size farklı seçenekler sunuyor.

<p align="center">
  <img src="https://user-images.githubusercontent.com/127443136/224388745-5bf634f6-2533-4ca6-9732-d60d54a69f6c.png" />
</p>

9. Surface için bir renk belirleyin. Bu codelab magenta'yı kullanıyor, ama siz favorinizi seçebilirsiniz!

```kotlin
@Composable
fun Greeting(name: String) {
   Surface(color = Color.Magenta) {
       Text(text = "Hi, my name is $name!")
   }
}
```

10. **Build&Refresh**'e basın. Metininiz seçtiğiniz renkle kaplanmış bir halde olacaktır!

<p align="center">
  <img src="https://user-images.githubusercontent.com/127443136/224389251-2461ecf5-925f-4bb7-bb03-458e91752cff.png" />
</p>

# <a name="5"></a>Dolgu ekleyin

Artık metininizin bir arka plan rengi var, şimdi metininizin etrafına biraz alan (dolgu) ekleyeceksiniz.

`Modifier` çoğaltmak veya bir composable'ı dekore etmek için kullanılır. Kullanabileceğiniz bir Modifier de `padding`'dir ve bu modifier bir parçanın etrafına (bu durumda metininizin etrafına) alan ekler. Bu `Modifier.padding()` fonksiyonunu kullanarak elde edilir.

1. Bu importları, import komut bölümüne ekleyin.

Yeni importları alfabetik olarak sıralamak için **Optimize Imports**'u kullandığınızdan emin olun. 

```kotlin
import androidx.compose.ui.unit.dp
import androidx.compose.foundation.layout.padding
```

2. Metininizin etrafına `24.dp` boyutunda dolgu modifier'i ekleyin, **Build&Refresh**'e tıklayın.

> Not: Bir sonraki pathway'de density-independent pixels hakkında daha çok şey öğreneceksiniz.
```kotlin
@Composable
fun Greeting(name: String) {
   Surface(color = Color.Magenta) {
       Text(text = "Hi, my name is $name!", modifier = Modifier.padding(24.dp))
   }
}
```

![e197f5dc2a5830e7_856](https://user-images.githubusercontent.com/127443136/224491234-0eae9ee9-6f6c-4257-ba12-b8775413b37f.png)

Tebrikler Compose içinde ilk Android uygulamanızı yarattınız! Bu büyük bir başarı. Farklı renkler ve metinlerle oynamak için kendinize biraz zaman ayırın, kendinize ait yapın!

# <a name="6"></a>Çözüm kodunu gözden geçirin

```kotlin
import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.layout.padding
import androidx.compose.material.MaterialTheme
import androidx.compose.material.Surface
import androidx.compose.material.Text
import androidx.compose.runtime.Composable
import androidx.compose.ui.Modifier
import androidx.compose.ui.graphics.Color
import androidx.compose.ui.tooling.preview.Preview
import androidx.compose.ui.unit.dp
import com.example.myapplication.ui.theme.GreetingCardTheme
class MainActivity : ComponentActivity() {
   override fun onCreate(savedInstanceState: Bundle?) {
       super.onCreate(savedInstanceState)
       setContent {
           GreetingCardTheme {
               // A surface container that uses the 'background' color from the theme
               Surface(color = MaterialTheme.colors.background) {
                   Greeting("Android")
               }
           }
       }
   }
}
@Composable
fun Greeting(name: String) {
   Surface(color = Color.Magenta) {
       Text(text = "Hi, my name is $name!", modifier = Modifier.padding(24.dp))
   }
}
@Preview(showBackground = true)
@Composable
fun DefaultPreview() {
   GreetingCardTheme {
       Greeting("Meghan")
   }
}
```
