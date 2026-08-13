# Trex Research

# 1. Modern Yazılım Geliştirme Pratikleri

<details>
 <summary><b>Git Nedir? GitHub Nedir?</b></summary>
 <h3>Git Nedir?</h3>
 <ul>
   <li>Git, tamamen kendi bilgisayarınızda çalışan bir versiyon kontrol sistemidir. Bilgisayarınızdaki dosyalarda yaptığınız her değişikliği versiyon versiyon       kaydeder, istediğiniz an istediğiniz versiyona dönmenizi sağlar. Git sadece yazılım projeleri için kullanılmaz, bütün işlerinizde kullanabilirsiniz.</li></ul>
 <br>
 <h3>GitHub Nedir?</h3>
 <ul>
 <li>GitHub, Git kullanarak bilgisayarımızda oluşturduğumuz versiyonları ve dosyaları internet üzerinde yedeklememizi / barındırmamızı sağlayan bir web platformudur. En önemli faydası ekipçe ortak bir proje üzerinde çalışmayı kolaylaştırmasıdır. Ekip üyeleri projelerde yaptıkları değişikleri GitHub'a yükleyebilir, diğer ekip üyelerinin yaptığı değişiklikleri bilgisayarına çekebilir, kimin ne değişiklik yaptığı görülür. Bütün bunlar da ortak bir projede çalışmayı kolaylaştırır.</li>
 </ul>
</details>


<details>
 <summary><b>Temel Git Komutları</b></summary>
 <br>
 
 <ul>
   <li><code>git init</code>: Sıfırdan başlama komutudur. Bilgisayarınızdaki normal bir klasörün içine Git'i kurar ve "artık buradaki            dosyaları takip et" der.</li>
   <br>
   <li><code>git clone</code>: GitHub platformu gibi internet üzerinden erişimin olan bir projeyi, tüm geçmiş versiyonlarıyla birlikte           bilgisiyarınıza indirir.</li>
   <br>
   <li><code>git add</code>: Değişiklik yaptığın dosyaları sepete koyar. Git'e "Birazdan bu dosyaları kaydedeceğim, bunları aklında tut"         demektir.</li>
   <br>
   <li><code>git commit</code>: Sepete eklenen dosyaların o anki durumunun fotoğrafını çeker ve kalıcı bir versiyon olarak kaydeder.git          commit -m yazıp tırnak içinde "şunu değiştirdim" gibi bir açıklama mesajıyla yapılır.</li>
   <br>
   <li><code>git push</code>: Kendi bilgisayarında kaydettiğin yeni versiyonları, internetteki yedeğine fırlatır ve orayı günceller.</li>
   <br>
   <li><code>git pull</code>: Ekip arkadaşlarımız projeye GitHub gibi platformlar üzerinden yeni kodlar yüklediğinde;bu komut, internetteki o    yeni değişiklikleri    senin bilgisayarına çeker ve dosyalarını günceller.</li>
   <br>
   <li><code>git branch</code>: Çalışan sistemi bozmadan denemeler yapmak veya yeni bir özellik kodlamak için açtığın paralel çalışma            alanıdır.Ekip üyelerinin projede yaptığı her değişikliği doğrudan çalışan sistem üzerine eklersek bir çok problem ortaya çıkabilir            branch yöntemi bunun önüne geçiyor.</li>
   <br>
   <li><code>git merge</code>: Bir ekip üyesinin kendi branchında yaptığı değişiklikler bittiğinde ve bu değişikliklerin sorunsuz                çalıştığından emin olduğunda, o yeni değişiklikleri ana projeyle pürüzsüzce birleştirme işlemidir.</li>
 </ul>
</details>

<details>
 <summary><b>Merge Conflict Nedir, Nasıl Çözülür? </b></summary>
 <br>

 <h3>Merge Conflict Nedir</h3>
 <ul>
  <li>Merge conflict, iki farklı kişinin aynı dosyanın aynı satırında farklı değişiklikler yapması sonucu Git'in bu kodları otomatik olarak birleştirememesi ve kararı size   bırakması durumudur.</li>
 </ul>

 <h3>Nasıl Önüne Geçilir</h3>
 <ul>
   <li>Görevleri net bölüşüp aynı dosyalarda eşzamanlı çalışmaktan kaçının.</li>
   <li>Kodlarınızı sık sık ve küçük parçalar halinde commit'leyin.</li> 
   <li>Ana branch'teki güncellemeleri kendi branch'inize düzenli olarak çekin.</li> 
 </ul>

 
 <h3><b> Nasıl Çözülür?</b></h3>
 <ul>
  <li>Çözmek için çakışan dosya kod editöründe açılır, Git'in eklediği uyarı işaretleri (<<<<, ====, >>>) silinip kodun kalacak olan son haline manuel olarak karar verilir   ve ardından dosya git add ve git commit yapılarak kaydedilir.</li>
 </ul>
</details>


<details>
 <summary><b>CI/CD nedir?</b></summary>

 <h3>CI Nedir?</h3>
 <ul>
   <li>Kaynak koda yeni bir kod gönderildiğinde sistem projeyi kendi kendine ayağa kaldırarak testleri çalıştırır; böylece eklenen kısmın mevcut sistemi bozup       bozmadığı anında kontrol edilir, kod çakışmaları en aza indirilir ve hatalar erkenden yakalanır.</li>
 </ul>

 <h3>CD Nedir?</h3>
 <ul>
   <li>CI aşamasında başarıyla test edilmiş ve hatasız olduğu onaylanmış bu kodun, kullanıcıların eriştiği canlı sunuculara kesintisiz bir şekilde aktarılması       operasyonudur. Sürekli Teslimat yönteminde kodun canlıya alınması için bir yetkilinin son bir manuel onay vermesi beklenirken, Sürekli Dağıtım                    yönteminde testleri geçen kod hiçbir insan müdahalesi olmadan tamamen otomatik olarak yayına alınır.</li>
 </ul>

 <h3>Azure DevOps, GitHub Actions İle Pipeline Örnekleri</h3>

 <h2>Pipeline Nedir?</h2>
 <ul>
  <il>Pipeline, yukarıda bahsettiğimiz CI ve CD süreçlerinin yol haritasıdır. Sistemin neyi, nasıl ve ne zaman yapacağını adım adım belirlediğimiz talimatlardır.   </il>
 </ul>

### 1. GitHub Actions Pipeline Örneği

GitHub üzerinde `main` dalına kod gönderildiğinde otomatik çalışan yol haritamız:

```yaml
name: GitHub CI Yol Haritasi

# Tetikleyici: Main dalına kod gelince çalış
on:
  push:
    branches: [ "main" ]

jobs:
  test-ve-kurulum:
    runs-on: ubuntu-latest
    steps:
    - name: Kodlari İndir
      uses: actions/checkout@v4
      
    - name: Node.js Ortamini Kur
      uses: actions/setup-node@v4
      with:
        node-version: '18.x'
        
    - name: Paketleri Yukle ve Test Et
      run: |
        npm install
        npm run test
```

### 2. Azure DevOps Pipeline Örneği

Aynı sürecin Microsoft Azure DevOps platformu üzerindeki yol haritası:

```yaml
name: Azure CI Yol Haritasi

# Tetikleyici: Main dalına kod gelince çalış
trigger:
- main

# Çalışacak sanal bilgisayar
pool:
  vmImage: 'ubuntu-latest'

steps:
- task: NodeTool@0
  inputs:
    versionSpec: '18.x'
  displayName: 'Node.js Ortamini Kur'

- script: |
    npm install
    npm run test
  displayName: 'Paketleri Yukle ve Test Et'
```
 
</details>


<details>
 <summary><b>Software Development Life Cycle-Yazılım Geliştirme Yaşam Döngüsü </b></summary>
 
 SDLC, bir yazılımın sadece basit bir fikirden ibaret olduğu ilk günden başlayıp, müşteriye teslim edilmesine ve yıllar sonraki güncellemelerine kadar geçen tüm   süreçtir.

 SDLC Aşamaları:
 
 <ul>
  <li><b>Planlama:</b> Projenin fizibilite çalışmasının yapıldığı, kaynak atamalarının , bütçenin ve risk yönetiminin belirlendiği aşamadır.Kısacası "Biz ne                  yapacağız, bütçemiz ne, bu işe değer mi?" sorularının sorulduğu aşamadır.</li>
  
  <li><b>Analiz:</b>Müşterinin istekleri doğrultusunda projenin gereksinimleri detaylı çıkarılır ve rapora dökülür</li>
  
  <li><b>Tasarım:</b>Belirlenen gereksinimlere göre sistem mimarisi, veritabanı şemaları, API yapıları ve kullanıcı arayüzü tasarımları kodlama başlamadan önce burada        netleştirilir </li>
  
  <li><b>Geliştirme:</b>Tasarlanan sistem mimarisinin koda döküldüğü aşamadır. Frontend ve backend geliştirmeleri bu aşamada yazılır.</li>
  
  <li><b>Test:</b>Yazılan kodun Kalite Güvence süreçlerinden geçirildiği aşamadır. Unit test, entegrasyon testleri ve E2E testleri yapılır. Bug'lar tespit edilip             geliştiriciye düzeltmesi için geri raporlanır. </li>
  
  <li><b>Deployment:</b>Testleri başarıyla geçen derlenmiş kodun, hedef sunuculara aktarılarak son kullanıcının erişimine açılmasıdır. </li>
  
  <li><b>Bakım:</b>Yazılımların geliştirme süreçleri yayınlandıktan sonra bitmiyor;müşterinin yeni istekleri çıkıyor,sistem zaman içinde çeşitli performans                   iyileştirmelerine ihtiyaç duyuyor bu sebeplerden dolayı yazılımın sürekli bakım ihtiyacı oluyor. </li>
  
 </ul>
 
</details>


# 2. .NET Ekosistemi 

<details>
 <summary><b> .NET nedir? Tarihçesi, amacı, neden kullanılır? </b></summary>
 <br>
 
 <h3>.NET nedir?</h3>
 <ul>
   <li>.NET,bir dil değildir Microsoft tarafından geliştirilen, açık kaynaklı, platformlar arası ve çok dilli bir yazılım geliştirme platformudur.Masaüstü, web, mobil,        bulut ve oyun geliştirme gibi çok çeşitli alanlarda uygulama yazılmasına olanak tanır.</li>
 </ul>
 <br>
 
 <h3>Neden Kullanılır ve Amacı Nedir?</h3>
 <ul>
   <li>.NET altyapısının temel amacı, yazılımcıların sıfırdan kod yazmak yerine hazır kütüphaneler ve standartlaşmış araçlar kullanarak çok daha hızlı, güvenli ve verimli     bir şekilde projeler üretmesini sağlamaktır. Bu platform, güvenlik ve bellek yönetimi gibi arka plan işlemlerini otomatik olarak hallederek geliştiricinin hızını çok       ciddi oranda arttırır. Ayrıca web, masaüstü veya mobil gibi tamamen farklı alanlar için aynı temel bilgi birikimiyle yazılım geliştirilebilmesine imkan verir.</li>
 </ul>

 <h3>Tarihçesi</h3>
 <ul>
   <li>Tarihsel gelişimine baktığımızda, Microsoft tarafından 2002 yılında sadece Windows işletim sistemine özel kapalı bir ekosistem olarak piyasaya sürülmüştür.             İlerleyen yıllarda yazılım dünyasındaki açık kaynak ve platform bağımsızlığı trendlerine ayak uydurmak için büyük bir evrim geçirmiş,2016 yılında baştan aşağı              yenilenerek tamamen açık kaynaklı hale gelmiş ve Linux ile Apple sistemlerinde de çalışabilir duruma gelmiştir. Günümüzde ise eski sürümlerindeki isim karmaşaları          giderilerek tek ve modern bir çatı altında birleştirilmiş, modern yazılım dünyasının en güçlü standartlarından biri haline gelmiştir.</li>
 </ul>
 
</details>


<details>
 <summary><b>.NET Framework, .NET Core ve .NET 7/8+ farkları</b></summary>
 <br>
 
 <h3>.NET Framework</h3>
 <ul>
   <li>Microsoft tarafından 2002 yılında piyasaya sürülen ve sadece Windows işletim sistemlerinde çalışan kapalı kaynaklı ilk versiyondur.
   Bu yapı tamamen Windows tabanlı donanım ve sunuculara bağımlıydı. Zamanla kod tabanı çok büyüdü ve hantallaştı. Bulut sistemlerinin yaygınlaşması ve farklı işletim         sistemlerine olan ihtiyacın artmasıyla birlikte sadece windows işletim sisteminde çalışıyor olması modern web ihtiyaçlarına yanıt vermekte zorlanmaya başladı.</li>
 </ul>
 <br>
 
 <h3>.NET Core</h3>
 <ul>
   <li>2016 yılında piyasaya sürülen bu sürüm, Microsoft'un kapalı kutu mantığını yıktığı devrim niteliğinde bir adımdır.Framework sürümünün aksine baştan aşağı yeniden       yazılmış, açık kaynak kodlu ve tamamen platform bağımsız bir hale getirilmiştir. Node.js gibi teknolojilerin sunduğu çevikliği ve farklı işletim sistemlerinde çalışma      mantığını benimsemiştir. Artık yazılan bir kod Windows, Linux ve macOS üzerinde sorunsuz çalışabilir hale gelmiştir. Özellikle mikroservis mimarileri ve yüksek             performanslı bulut uygulamaları için optimize edilmiştir.</li>
 </ul>

 <h3> .NET 7/8+ farkları</h3>
 <ul>
   <li>.NET 7 standart destek sürümü olduğu için on sekiz aylık ömrünü tamamlamıştır ancak .NET 8 ve sonrası uzun vadeli destek sunarak özellikle B2B SaaS platformları        gibi kesintisiz çalışması gereken mimariler için güvenilir bir temel oluşturur. .NET 8 ile birlikte gelen gelişmiş performans iyileştirmeleri ve önceden derleme            yetenekleri sayesinde bulut tabanlı uygulamalar çok daha hızlı ayağa kalkar ve daha az sunucu kaynağı tüketir. Ayrıca veritabanı tarafında Entity Framework Core            üzerinden MySQL gibi ilişkisel sistemlerle kurulan bağlantılarda sorgu hızları artırılmış, büyük projelerin arka plan yönetimi çok daha pürüzsüz hale getirilmiştir.</li>
 </ul>
 
</details>


<details>
 <summary><b>Platformlar arası çalışabilir mi? (Windows, Linux, macOS)</b></summary>
 <br>
 Evet, kesinlikle çalışabilir.Yukarıda da belirttiğimiz gibi Modern .NET bütün platformlarda çalışır.Microsoftun .NET Core'u çıkarmasının en temel amacı sadece windows      üzerinde çalışan .NET Frameworkun bu eksikliğini giderip .NET ekosistemini bütün işletim sistemlerinde çalışacak bir yapı haline getirmekti.
</details>


# 3. Backend Geliştirme Temelleri 

<details>
 
 <summary>Backend Nedir?</summary>
 
 ---

 -Backend yazılım sistemlerinde kullanıcının görmediği, sunucu tarafında çalışan ve sistemin bütün mantığını, verilerini ve güvenliğini yöneten kısmıdır.Frontend ise        yazılım sistemlerinde kullanıcıların gördüğü, tıkladığı ve doğrudan etkileşim kurduğu kısımdır.Renkler, yazılar, resimler, butonlar ve menüler frontend kısmında yer        alır.Yazılım sistemlerini bir bina gibi düşünecek olursak,binanın dışarıdan görünen yüzü frontend kısmıdır; su, elektrik ve taşıyıcı kolonları backend kısmıdır             diyebiliriz.
 ***
 </details>


 
<details>
 
 <summary>Web Sunucusu Nedir? API Nedir? API Türleri</summary>

 ---
 
  <h3>Web Sunucusu Nedir?</h3>
  -Web sunucuları internet sitelerine ait dosyaları depolar ve kullanıcıların tarayıcılarından gelen HTTP/HTTPS isteklerini alarak bu dosyaları onlara                        ulaştırır.Kullanıcının tarayıcısı da bu dosyaları görüntüye çevirip kullanıcıya sunar. 

---

  <h3>API Nedir?</h3>
  -API, farklı yazılım sistemlerinin iletişim kurmasını ve veri alışverişi yapmasını sağlayan bir köprüdür diyebiliriz. Örneğin, "Google ile giriş yap" seçeneğiyle bir       uygulamaya girdiğimizde, girdiğimiz uygulama Google’ın veritabanına doğrudan ulaşıp kullanıcının girdiği bilgilerin doğru olup olmadığını kontrol edemez; çünkü şirketler   veritabanlarını dışarıya açmazlar. Fakat API bu sorunu çözer. Kullanıcının girdiği uygulama Google’a API isteği atar ve sonucu alır.Aynı zamanda API'ler, her şeyi          sıfırdan yazmak yerine mevcut servisleri projenize birkaç satır kodla dâhil edebilme imkânı sunar. Örneğin, geliştirdiğimiz projede harita ihtiyacı olduğunda oturup        sıfırdan harita geliştirmek yerine Google Maps'e API ile bağlanıp bu ihtiyacı kolayca giderebiliyoruz.

---

  <h3>API Türleri</h3>
  -Mimari tarzlarına göre ve kullanım kapsamına göre farklı api türleri vardır.

  <h4>Mimari Tarzlarına Göre Api Türleri</h4>
  <b>REST:</b>İnternette gördüğümüz API'lerin çok büyük bir kısmı REST mimarisiyle çalışır.REST mimarisi HTTP protokolünü temel alır.Standart URL'ler üzerinden     istek atılır ve genellikle JSON formatında veri alınır. Stateless bir yapıdadır, yani sunucu her isteği bağımsız olarak değerlendirir.
  <br>
  <b>SOAP:</b>REST'ten daha eski, kuralları daha katı olan bir protokoldür.Genellikle veri güvenliğinin kritik olduğu alanlarda tercih edilir.HTTP üzerinden                  çalışabilir,veri alışverişi için sadece XML formatını kullanır. 
  
  <b>GraphQL:</b>Facebook tarafından REST API'lerin gereksiz veri çekme sorununu çözmek için geliştirilmiş modern bir sorgu dilidir.Örneğin REST mimarisinde /users           yaptığımız zaman user'in bütün bilgilerini getirir fakat GraphQL bize "Bana sadece kullanıcının yaşını getir." deme imkanı sunuyor bu da gereksiz veri çekme sorununu       önlüyor.

  <h4>Kullanım Kapsamına Göre Api Türleri</h4>
  <b>Public Api:</b>Şirketlerin, geliştirdikleri servisleri veya verileri tüm dünyadaki yazılımcıların projelerine kolayca entegre edebilmesi için internet üzerinden         herkese açtığı erişilebilir arayüzlerdir.
  
  <b>İnternal Api:</b>Bir şirketin dış dünyaya tamamen kapalı olarak, sadece kendi bünyesindeki yazılım ekiplerinin kurum içi sistemlerini, veritabanlarını güvenli bir       şekilde birbirine bağlamak için geliştirdiği özel arayüzlerdir.
  
  <b>Partner Api:</b>Herkesin erişemediği, yalnızca belirli sözleşmeler, özel izinler aracılığıyla anlaşmalı olunan firmaların  kullanımına tahsis edilen veri paylaşım       kanallarıdır.

  <b>Composite Api:</b>Tek bir istek atıldığında arka planda birden fazla farklı veri kaynağına veya API'ye aynı anda ulaşıp, gelen dağınık verileri toplayıp derleyerek      kullanıcıya tek bir paket halinde sunan sistemleridir.

  ---
 


 ## REST, SOAP ve GraphQL Karşılaştırması

| Özellik | REST | SOAP | GraphQL |
| :--- | :--- | :--- | :--- |
| **Tür / Mimari** | Mimari Tasarım Stili | Katı Kurallı Protokol | Sorgu Dili |
| **Veri Formatı** | Genellikle JSON | Sadece XML | JSON |
| **Veri Çekme Esnekliği** | Sabit uç noktalar; istek atılan yerdeki tüm veri gelir. | Sabit yapılı XML zarfları ile katı veri alışverişi. | İhtiyaca göre nokta atışı veri seçimi; sadece istenen alanlar gelir. |
| **Güvenlik Standardı** | Standart HTTP güvenliği | Gelişmiş yerleşik güvenlik standartları . | Standart HTTP güvenliği |
| **Avantajları** | Hafif, hızlı, esnek ve öğrenmesi/uygulaması oldukça kolaydır. | Çok güvenlidir, hata yönetimi gelişmiştir, kurumsal standartları tamdır. | Gereksiz veri yükünü ortadan kaldırır. |
| **Dezavantajları** | Büyük veri yapılarında gereksiz fazla veri taşıyabilir. | XML yapısı ağır, kodlaması zahmetlidir; günümüzde modern web projelerinde pek tercih edilmez. | Önbellekleme mekanizması REST'e göre daha karmaşıktır. |
| **Kullanım Alanı** | Web, mobil uygulamalar ve genel mikroservisler | Bankacılık, finans ve yüksek güvenlikli kurumsal sistemler | Modern web uygulamaları ve esneklik gerektiren projeler |

---

</details>


<details>
 
 <summary>HTTP Nedir? HTTP Metodları Nelerdir</summary>
 <br>

 ***
 
 <h3>HTTP Nedir?</h3>
 -HTTP,web tarayıcılarının,yani istemcilerin,ile web sunucuları arasında verilerin nasıl taşınacağını ve iletileceğini belirleyen temel kurallardır.En basit tanımıyla        HTTP, web sitelerinin sayfalarını, görsellerini, videolarını vs. web sunucusundan bilgisayarımıza veya telefonumuza getiren iletişim dilidir.
 
 ***
 
 <h3>Nasıl Çalışır?</h3>
 <b>İstek:</b>Tarayıcınıza bir adres yazıp Enter tuşuna bastığınızda, tarayıcınız internet üzerinden ilgili web sitesinin sunucusuna bir HTTP İsteği gönderir.    ("Bana     ana sayfa verilerini gönder" der.)
 
 <b>Yanıt:</b> Sunucu bu isteği alır, işler ve tarayıcınıza bir HTTP yanıtı döner. Bu yanıtın içinde web sitesinin kodları ve durum kodlar bulunur.Daha sonrasında           tarayıcı bu kodları çalıştırarak websitesini gösterir.
 ***   
 <h3>HTTP Metodları</h3>
 -Sunucuya bir istek atarken ne yapmak istediğimizi belirten komutlar kullanırız. En yaygın olanları şunlardır:

 <b>GET:</b>Sunucudan veri istemek için kullanılır.
 
 <b>POST:</b>Sunucuya yeni veri göndermek ve kaydettirmek için kullanılır.
 
 <b>PUT:</b>Sunucudaki mevcut bir veriyi güncellemek için kullanılır.

 <b>DELETE:</b>Sunucudaki bir veriyi silmek için kullanılır.

 ---
 
 <h3>HTTP Metodları Kod Örneği</h3>
 -Yukarıda belirttiğimiz HTPP metodlarının sunucu ve istemci tarafında örnek kullanımlarını yapacağız:
 

 <h2>SUNUCU HTTP METHODLARI KOD ÖRNEĞİ</h2>

 ```csharp
using Microsoft.AspNetCore.Mvc;

[Route("api/[controller]")]
[ApiController]
public class NotlarController : ControllerBase
{
    // Sanal bir veritabanı yerine hafızada tutulan liste oluşturduk
    private static List<string> notlar = new List<string> { "Alışveriş yapılacak", "Kod yazılacak" };

    // 1. GET: Sunucuya httpget isteği gelince bütün notları geri döndürecek
    [HttpGet]
    public List<string> GetNotlar()
    {
        return notlar;
    }

    // 2. POST: Sunucuya htpp post isteği ve eklenecek bilgi geldiğinde ,yeni not listeye eklenecek
    [HttpPost]
    public void NotEkle([FromBody] string yeniNot)
    {
        notlar.Add(yeniNot);
    }

    // 3. PUT: Sunucuya htppPut ,id ve yeni not geldiğinde o id'deki not güncellenecek
    [HttpPut("{id}")]
    public void NotGuncelle(int id, [FromBody] string guncelNot)
    {
        notlar[id] = guncelNot;
    }

    // 4. DELETE: Sunucuya httpDelete ve id numarası geldiğinde o id'deki not silinecek
    [HttpDelete("{id}")]
    public void NotSil(int id)
    {
        notlar.RemoveAt(id);
    }
}
```

<h2>İSTEMCİ HTTP METHODLARI KOD ÖRNEĞİ</h2>

```csharp

// 1. GET: Sunucuya istek atıp mevcut notları çekerek kullanıcıya (konsola) bastırır
fetch('http://localhost:5000/api/notlar')
  .then(cevap => cevap.json())
  .then(notlarListesi => console.log("Sunucudan gelen notlar:", notlarListesi));

// 2. POST: Sunucuya yeni bir not gönderip listeye eklemesini sağlar
fetch('http://localhost:5000/api/notlar', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify("Yarın spor yapılacak")
})
.then(() => console.log("Not başarıyla eklendi!"));

// 3. PUT: Sunucudaki 0 numaralı notu yeni metinle değiştirip günceller
fetch('http://localhost:5000/api/notlar/0', {
    method: 'PUT',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify("Alışveriş listesi güncellendi")
})
.then(() => console.log("Not güncellendi!"));

// 4. DELETE: Sunucuya 1 numaralı notun silinmesi için istek atar
fetch('http://localhost:5000/api/notlar/1', {
    method: 'DELETE'
})
.then(() => console.log("Not silindi!"));
```

 </details>


 <details>
  <summary>RESTful</summary>

  ---
  -REST bir mimari kural bütünüdür; RESTful ise o kuralların sahada eksiksiz bir şekilde uygulanmış halidir. Yani eğer yazdığımız bir API, REST          mimarisinin kurallarına harfiyen uyuyorsa, artık o projeye "RESTful API" diyoruz.REST işin teorisi ve kurallarıdır, RESTful ise o başarıyla hayata     geçirdiğinde sistemin kazandığı uygunluk unvanıdır.

  ---
  
 </details>


 <details>
  <summary>JSON Veri Formatı ve Kullanım Amacı</summary>

  ---

  <h3>JSON NEDİR?</h3>
  -JSON, sunucu ile istemci arasında veri alışverişini en sade ve dilden bağımsız şekilde gerçekleştiren modern bir iletişim standardıdır ,              JSON'dan önce verileri taşımak için etiket mantığına dayanan ağır XML formatı kullanılıyordu; her veri parçası için sürekli açılış ve kapanış          etiketleri yazmak zorunda kalmak dosyaları gereksiz yere şişirip ağ trafiğini yavaşlatıyordu. Anahtar-değer prensibine dayanan yapısıyla bu            karmaşaya son veren JSON, sunucu ile istemci arasında hafif bir kargo paketi gibi çalışarak hem geliştiricilerin anında okuyabileceği sade bir dil     sundu hem de bilgisayarların mikro saniyeler içinde işleyebileceği  bir format haline geldi.

  ---



  # JSON ve XML Karşılaştırma Örneği

<table>
  <tr>
    <th width="50%">JSON </th>
    <th width="50%">XML </th>
  </tr>
  <tr>
    <td>
<pre><code class="language-json">{
  "ad": "Hamza",
  "yas": 22,
  "ogrenciMi": true,
  "sehir": "Kocaeli"
}</code></pre>
    </td>
    <td>
<pre><code class="language-xml">&lt;Kullanici&gt;
  &lt;Ad&gt;Hamza&lt;/Ad&gt;
  &lt;Yas&gt;22&lt;/Yas&gt;
  &lt;OgrenciMi&gt;true&lt;/OgrenciMi&gt;
  &lt;Sehir&gt;Kocaeli&lt;/Sehir&gt;
&lt;/Kullanici&gt;</code></pre>
    </td>
  </tr>
</table>

---

Görüldüğü üzere JSON,  XML'e kıyasla sade ve anahtar-değer yapısıyla daha sade bir çözüm sunuyor.

---

 </details>

 # 4. ASP.NET 

 <details>
  <summary>ASP.NET ve ASP.NET Core Nedir?</summary>

  ---

  <h3>ASP.NET ve ASP.NET Core Nedir?</h3>
  -ASP.NET, .NET ekosisteminin web projeleri geliştirmek için sunduğu hazır araçları, kütüphaneleri ve yapıları barındıran web   framework'üdür; yani .NET'in web dünyasına açılan alt kümesidir. Tıpkı ikinci konu başlığımız olan .NET ekosistemindeki        geleneksel .NET Framework yapısında olduğu gibi, ilk nesil klasik ASP.NET de temelde sadece Windows işletim sistemine ve IIS   sunucusuna bağımlı olarak çalışırken, onun modern ve güçlü evrimi olan ASP.NET Core bu sınırları tamamen ortadan kaldırarak    Windows, Linux ve macOS üzerinde çalışabilen, çok daha yüksek performanslı ve açık kaynaklı yeni nesil bir yaklaşım sunar.

  ---

 </details>


  <details>
  <summary>MVC Nedir, Ne İçin Kullanılır? </summary>

  ---

  <h3>MVC Nedir?</h3>
  -MVC (Model-View-Controller), bir yazılım projesini üç ayrı temel katmana ayırarak geliştirmeyi sağlayan popüler bir tasarım    kalıbıdır. Bu mimari yaklaşımın temel amacı; uygulamanın verilerini, iş mantığını ve kullanıcı arayüzünü birbirinden kesin     çizgilerle ayırarak kodun çok daha düzenli, sürdürülebilir ve test edilebilir olmasını sağlamaktır.
  
 ---
 
  MVC üç temel katmandan oluşur:

<ul>
  <li><b>1. Model Katmanı:</b> Veritabanı ile doğrudan haberleşen, uygulamanın verilerini barındıran, işleyen ve kurallarına göre doğrulayan temel       veri katmanıdır.</li>
  <li><b>2. View Katmanı:</b> Kullanıcının ekranda karşılaştığı; HTML, CSS ve JavaScript teknolojileriyle tasarlanan görsel arayüz katmanıdır. Sadece    verinin son kullanıcıya sunulmasından sorumludur.</li>
  <li><b>3. Controller Katmanı:</b> Kullanıcıdan gelen tüm istekleri ilk karşılayan, Model ile View arasında akış ve veri transferini sağlayan yönetim   katmanıdır.</li>
</ul>
  
  ---

 ### MVC Akış Şeması

```text
    Kullanıcı (Browser)
         │ 
         │ 1. İstek Gönderir (Sayfa/Veri İsteği)
         ▼
    [ Controller Katmanı ] ────── 2. Veri Talebi ─────► [ Model Katmanı ]
         │                                                      │
         │                                                      │ 3. Veritabanından
         │ ◄───── 4. İşlenen Veri Dönüşü ───────────────────────┘    Veri Çekilir
         ▼
    [ View Katmanı ]
         │ 
         │ 5. HTML/CSS ile Arayüz Oluşturulur
         ▼
    Kullanıcıya Sonuç Gösterilir
  ```

 ---

 </details>


  <details>
  <summary>Middleware nedir, Nasıl çalışır?</summary>,

  ---

  <h3>Nedir?</h3>
  -Middleware, web uygulamalarına dışarıdan gelen isteğin, uygulamanın ana kodlarına ulaşmadan önce geçtiği ilk kontrol, gerekli kontrollerin    yapıldığı güvenlik katmanıdır.

  ---

  <h3>Nasıl Çalışır?</h3>
  <ul>
    <il>1.Kullanıcı arayüzünde bir işlem yapar,örneğin bir butona tıklar,ve tarayıcı sunucuya bir HTTP İsteği gönderir.</il>
    <il>2.Sunucuya gelen bu istek,sunucuya girmeden en dış katmanındaki middleware pipeline'a girer.</il>
    <il>3.İstek middleware süzgeçlerinden geçer, gerekli kontroller yapılır.</il>
    <il>4.Süzgeçlerden onay alan istek,sunucuya ulaşır ve işlenip kullanıcıya geri döner.Eğer onay almazsa, sunucuya ulaşamadan  geri             çevrilir.</il>
  </ul>

  ---

  <h3>Startup.cs ya da Program.cs İçindeki Middleware Sıralaması</h3>
  
  -Yukarıda HTTP isteklerinin middleware süzgeçlerinden geçtiğini belirtmiştik.İşte bu süzgeçlerin belirli bir sıralaması vardır; bu sıralama            uygulamanın güvenliği, performansı ve doğru çalışması açısından hayati önem taşır.ASP.NET Core uygulamalarında Startup.cs veya Program.cs              dosyalarında bu sıralamaya dikkat edilmelidir. Middleware'ler pipeline mantığıyla çalışır. Gelen bir HTTP isteği bu katmanlardan sırayla geçer,        son noktada işlenir ve yanıt önerken tam tersi sırayla geri çıkar. Doğru sıralama yapılmazsa yetkilendirme açıkları, performans kayıpları veya         işlevsel hatalar ortaya çıkabilir.

  <br>
  
  <b>Önerilen Sıralama</b>

  ---
  
  <br>
     
 | Sıra | Middleware | Açıklama | Neden Bu Sırada Olmalı? |
| :--- | :--- | :--- | :--- |
| **1** | **Hata Yönetimi (Exception Handling)** | `UseExceptionHandler`<br>`UseDeveloperExceptionPage` | Pipeline'nın devamında çıkabilecek tüm hataları en dıştan yakalayıp kullanıcıya doğru formatta iletebilmek için. |
| **2** | **HTTPS Yönlendirme** | `UseHttpsRedirection` | İstekleri gereksiz işlemlere sokmadan, en erken aşamada güvenli protokole (HTTPS) çekmek için. |
| **3** | **Statik Dosyalar** | `UseStaticFiles` | Resim, CSS, JS gibi statik kaynaklara yetki veya yönlendirme işlemi yapmadan hızlıca yanıt dönerek performans sağlamak için. |
| **4** | **Routing (Yönlendirme)** | `UseRouting` | İsteğin hangi hedefe gideceğini belirlemek için. |
| **5** | **CORS Politikaları** | `UseCors` | Hedef belirlendikten sonra, farklı domainlerden gelen isteklere izin verilip verilmediğini güvenlikten hemen önce denetlemek için. |
| **6** | **Authentication (Kimlik Doğrulama)** | `UseAuthentication` | Authorization kontrolü yapabilmek için, önce sisteme gelen kullanıcının "kim olduğunu" doğrulamak gerektiği için. |
| **7** | **Authorization (Yetkilendirme)** | `UseAuthorization` | Kimliği artık bilinen kullanıcının, ulaşmak istediği hedefe "erişim izni" olup olmadığını son aşamada kontrol etmek için. |
| **8** | **Session / Özel Katmanlar** | `UseSession` vb. | Kullanıcı oturum verilerini  hedefe ulaşmadan hemen önce hazırlamak için. |
| **9** | **Endpoints (Uç Noktalar)** | `MapControllers()` vb. | Tüm güvenlik ve yönlendirme süzgeçlerinden başarıyla geçen isteğin, artık asıl işleneceği son durak olduğu için. |
   
---

 </details>


 <details>
  <summary>Dependency Injection Nedir, Neden Kullanmalıyız? </summary>

  ---
  
  <h3>Nedir?</h3>
  -Dependency Injection, bir nesnenin çalışmak için ihtiyaç duyduğu diğer nesneleri kendi içinde oluşturması yerine,bu nesnelerin dışarıdan bir          mekanizma tarafından verilmesidir.Aşağıdaki kod örnekleri üzerinden dependy injeciton'u daha iyi anlayalabiliriz.

  ---

  ## Dependency Injection'un Olmadığı Örnek

  ---

  ```Csharp
public class Araba 
{
    // Araba gidiyor ve kendi benzinli motorunu kendisi üretiyor.
    // Yarın elektrikli motora geçmek istersek arabanın kodunu çöpe atıp baştan yazmamız gerekir.
    private BenzinliMotor _motor = new BenzinliMotor(); 

    public void Git() 
    {
        _motor.Calistir();
    }
}
```

 ---


 ## Dependency İnjection Örneği

 ```Charp

// 1. Önce ortak bir motor kuralı tanımlıyoruz 
public interface IMotor 
{
    void Calistir();
}

// 2. Benzinli Motor bu kurala uyuyor
public class BenzinliMotor : IMotor 
{
    public void Calistir() { Console.WriteLine("Benzinli motor çalıştı."); }
}

// 3. Elektrikli Motor da bu kurala uyuyor
public class ElektrikliMotor : IMotor 
{
    public void Calistir() { Console.WriteLine("Elektrikli motor sessizce çalıştı."); }
}

// 4. Asıl Araba Sınıfı
public class Araba 
{
    private readonly IMotor _motor;

    // Araba üretilirken (Constructor) dışarıdan motoru ona veriyoruz,bu işlem injection oluyor.
    public Araba(IMotor motor) 
    {
        _motor = motor; 
    }

    public void Git() 
    {
        _motor.Calistir(); // Elinde hangi motor varsa onu çalıştırır
    }
}

```

---

<h3>Neden Kullanmalıyız?</h3>

<ul>
 
 <il><b>Esneklik:</b>Kodun bir yerini değiştirdiğimizde diğer yerler patlamaz.</il>
 
 <il><b>Bakım Kolaylığı:</b>Proje çok büyüse bile sınıflar birbirine aşırı bağımlı olmadığı için projeyi yönetmesi çok daha kolay olur. </il>
 
 <il><b>Test Edilebilirlik:</b>Kodlarımızı test ederken gerçek veritabanını bozmamak için içeriye sahte veritabanları enjekte ederek kolayca   test yazabiliriz.</il>
 
</ul>

---

  
 </details>
 
