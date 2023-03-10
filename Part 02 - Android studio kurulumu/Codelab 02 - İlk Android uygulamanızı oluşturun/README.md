#  İlk Android Uygulamanızı Oluşturun

### Konu Başlıkları:

📌  [Şablon kullanarak bir proje yaratın](#1) <br>
📌  [Proje dosyalarını bulun](#2) <br>
📌  [Metini güncelleyin](#3) <br>



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
