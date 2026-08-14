# Trex Research

# 1. Modern Yazılım Geliştirme Pratikleri

<details>
 <summary><b>Git Nedir? GitHub Nedir?</b></summary>

 ---
 
 <h3>Git Nedir?</h3>
 
 -Git, tamamen kendi bilgisayarınızda çalışan bir versiyon kontrol sistemidir. Bilgisayarınızdaki dosyalarda yaptığınız her değişikliği versiyon versiyon kaydeder, istediğiniz an istediğiniz versiyona dönmenizi sağlar. Git sadece yazılım projeleri için kullanılmaz, bütün işlerinizde kullanabilirsiniz.

 ---
 
 <h3>GitHub Nedir?</h3>
 
 -GitHub, Git kullanarak bilgisayarımızda oluşturduğumuz versiyonları ve dosyaları internet üzerinde yedeklememizi / barındırmamızı sağlayan bir web platformudur. En önemli faydası ekipçe ortak bir proje üzerinde çalışmayı kolaylaştırmasıdır. Ekip üyeleri projelerde yaptıkları değişikleri GitHub'a yükleyebilir, diğer ekip üyelerinin yaptığı değişiklikleri bilgisayarına çekebilir, kimin ne değişiklik yaptığı görülür. Bütün bunlar da ortak bir projede çalışmayı kolaylaştırır.
 
</details>


<details>
 <summary><b>Temel Git Komutları</b></summary>

 ---
 
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
 
 <il><b>Esneklik:</b> Kodun bir yerini değiştirdiğimizde diğer yerler patlamaz.</il>
 
 <il><b>Bakım Kolaylığı:</b> Proje çok büyüse bile sınıflar birbirine aşırı bağımlı olmadığı için projeyi yönetmesi çok daha kolay olur. </il>
 
 <il><b>Test Edilebilirlik:</b> Kodlarımızı test ederken gerçek veritabanını bozmamak için içeriye sahte veritabanları enjekte ederek kolayca   test yazabiliriz.</il>
 
</ul>

---

  
 </details>

 # 5.Veritabanı ve ORM

<details>
  <summary>SQL nedir?</summary>

  ---

  -SQL, ilişkisel veritabanı yönetim sistemlerinde verileri depolamak, yönetmek, güncellemek ve sorgulamak için kullandığımız bir programlama            dilidir. Büyük hacimli verileri düzenli tablolar halinde saklamayı, milyonlarca satır arasından saniyeler içinde bilgi çekmeyi sağlar. MySQL, Oracle   ve Microsoft SQL Server gibi pek çok veritabanı sağlayıcısı tarafından ortak bir standart olarak kullanılır.

  -Dilin kökeni 1970'lerin başında IBM laboratuvarlarına dayanır. Edgar F. Codd'un ilişkisel veritabanı teorisinden ilham alan Donald Chamberlin ve      Raymond Boyce, insan diline yakın bir sorgulama sistemi tasarlamıştır. Başlangıçta SEQUEL adıyla geliştirilen dil, marka çakışmaları nedeniyle kısaltılarak SQL adını almıştır. 1979 yılında Oracle tarafından ticari olarak piyasaya sürülmüş, 1986'da ANSI ve 1987'de ISO tarafından resmi standart olarak kabul edilerek günümüzdeki konumuna ulaşmıştır.

 ---

<h3>Temel SQL Sorguları</h3>

<br>

<ul>
 <il><b><code>SELECT</code></b>:
 Veritabanındaki tablolardan veri çekmek, listelemek istediğimizde kullanırız.Bütün tabloyu da çekebiliriz, belli bir koşula uyanları da filtreleyebiliriz.
    </il>
    
     ```SQL 
    
    -- Tablodaki bütün ürünleri listeleriz:
      SELECT * FROM Products;

    -- Sadece fiyatı 1000'den büyük olan ürünlerin isimlerini çekeriz:
    SELECT Name, Price FROM Products WHERE Price > 1000;
     ```
   
  </ul>
 
   <ul>
 <il><b><code>INSERT</code></b>:
 Veritabanına yeni bir kayıt, yeni bir satır eklemek istediğimizde bunu kullanırız.Tablonun istediğimiz sütunlarına yeni değerleri ekleriz.
    </il>
      
     ```SQL 
    
    -- Products tablosuna yeni bir ürün ekleriz:
     INSERT INTO Products (Name, Price) 
      VALUES ('Laptop', 25000);
     ```
   
  </ul>

   <ul>
  <il><b><code>UPDATE</code></b>:
  Veritabanında önceden var olan bir kaydın verisini değiştirmek istediğimizde kullanırız.
    </il>
    
    ```SQL 
    
    -- ID'si 5 olan ürünün fiyatını güncelleriz:
    UPDATE Products 
    SET Price = 22000 
    WHERE Id = 5;
    ```
   
  </ul>

   <ul>
  <il><b><code>DELETE</code></b>:
  Veritabanındaki bir kaydı tamamen ortadan kaldırmak istediğimizde kullanırız.
    </il>
    ,
     
    ```SQL 
    
    -- ID'si 5 olan ürünü veritabanından sileriz:
      DELETE FROM Products 
      WHERE Id = 5;
    ```
   
  </ul>

</details>

<details>
 <summary>İlişkisel ve İlişkisel Olmayan Veri Tabanları Arasındaki Farklar</summary>
 
 ---
 
 -İlişkisel veritabanları, verileri önceden kurallarını belirlediğimiz belirli satır ve sütunlardan oluşan tablolarda saklar; bu tablolara sadece       belirlediğimiz bu kurallara uyan yeni veriler ekleyebiliriz. Yüksek veri tutarlılığı gerektiren sistemler için idealdir. 

 -İlişkisel olmayan veritabanları ise belge veya anahtar-değer gibi esnek yapılar kullanarak şema zorunluluğu sunmaz. Yani istediğimiz her veriyi,       katı bir kurala bağlı kalmadan esnek bir şekilde ekleyebiliriz. Bu yaklaşım, özellikle büyük hacimli verilerin hızla işlenmesi gereken modern web      uygulamaları ve dinamik ürün katalogları gibi alanlarda büyük kolaylık sağlar.

 ---

| Özellik             | İlişkisel (SQL)                        | İlişkisel Olmayan (NoSQL)             |
|:--------------------|:---------------------------------------|:--------------------------------------|
| Veri Yapısı         | Satır ve sütunlu tablolar.             | Belge, key-value veya grafik.         |
| Şema Esnekliği      | Katı ve tanımlı kurallar.              | Esnek ve dinamik şema.                |
| Ölçekleme           | Genellikle dikey (tek sunucu).         | Genellikle yatay (dağıtık).           |
| Veri Tutarlılığı    | Yüksek .                  | Esnek.                |
| Örnek Veritabanları | MySQL, PostgreSQL, Oracle.             | MongoDB, Redis, Cassandra.            |
| İdeal Kullanım      | Finans ve tutarlılık odaklı sistemler. | Büyük veri ve hız odaklı uygulamalar. |

---
 
</details>
 
<details>
 <summary>ORM nedir? Entity Framework Core nedir? </summary>

 ---

 <h3>ORM Nedir?</h3>
 -Normalde veritabanında bir tablo oluşturmak veya veri eklemek için uzun uzun SQL komutları yazmamız gerekir ve ufak bir yazım hatası her şeyi bozar.  ORM tam burada devreye girip aradaki tercüman gibi çalışır; SQL kodlarıyla uğraşmak yerine kendi programlama dilimizle (C#, Java vb.) sanki normal     nesnelerle çalışıyormuş gibi işlemler yaparız. Örneğin veritabanına yeni bir veri kaydetmek için karmaşık SQL cümleleri yazmak yerine, ORM'in bize     sunduğu basit metodları kullanırız. Bu sayede hem kodumuz çok daha temiz ve okunur olur hem de SQL hatalarıyla vakit kaybetmeyiz.

 ---

 ## SQL vs ORM Örneği
 Aşağıda sql ve orm farkını daha iyi anlayabileceğimiz bir örnek görüyoruz:

| İşlem                 | Kod Örneği                                                         | Mantık                                                                     |
|:----------------------|:-----------------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| Tablo Oluşturma (SQL) | CREATE TABLE Users (Id INT PRIMARY KEY, Name NVARCHAR(50));                        | Veritabanı diliyle doğrudan şema tanımlanır.                               |
| Tablo Oluşturma (ORM) | public class User { public int Id { get; set; } public string Name { get; set; } } | Programlama dilinde class tanımlanır, ORM bunu tabloya dönüştürür. |

---

<h3>Entity Framework Core Nedir?</h3>
-Entity Framework, yukarıda bahsettiğimiz ORM yaklaşımının Microsoft tarafından .NET dünyası için geliştirilmiş en güçlü ve popüler uygulamasıdır. Temel olarak nesne tabanlı kodlarınız ile veritabanı arasındaki iletişimi yöneten bu framework, geliştiricileri ham SQL sorguları yazma yükünden kurtararak iş mantığına odaklanmalarını sağlar. Onu diğer ORM araçlarından ayıran en önemli özelliklerin başında, veritabanı ile C# arasında kusursuz bir uyum sağlayan LINQ entegrasyonu gelir; bu sayede veritabanı sorgularını sanki uygulama içindeki basit bir listeyi sorguluyormuşsunuz gibi rahatlıkla yazabilirsiniz. Bunun yanı sıra, "Migration" adı verilen sistemle veritabanı şemanızda yaptığınız kod tabanlı değişiklikleri otomatik olarak veritabanına yansıtabilir ve "Change Tracking" özelliği sayesinde üzerinde işlem yaptığınız verilerin sadece değişen kısımlarını tek bir komutla kaydedebilirsiniz. Kısacası Entity Framework, veritabanı yönetimini otomatize eden, kodunuzu hem daha okunabilir hem de daha güvenli hale getiren, esnek ve gelişmiş bir yazılım katmanıdır.

---

</details>


<details>
 <summary> DbContext Nedir, Nasıl Kullanılır? </summary>

 ---

 <h3>Nedir?</h3>
 -DbContext, Entity Framework çatısı altında veritabanı ile uygulama arasındaki tüm trafiği yöneten tek yetkili merkezdir. Uygulamanın veritabanına      bağlanması, tabloları tanıması ve veri üzerinde yapacağın tüm değişiklikleri veritabanına bildirmesi tamamen bu sınıfın    sorumluluğundadır.

 ---

 <h3>Nasıl Kullanılır?</h3>

 ## 1 . Veri Ekleme
```Csharp
var yeniUrun = new Product { Name = "Laptop", Price = 25000 };
db.Products.Add(yeniUrun); //yeni ürünü database'e db sınıfının Add komutu ile ekledik 
db.SaveChanges(); //yaptığımız bu değişikliği db sınıfının SaveChanges komutu ile veritabanına kayıt ettik.
```

## 2.Veri Silme

```Csharp
var urun = db.Products.Find(5); / id 'si 5 olan ürünü bulduk
db.Products.Remove(urun); // db sınıfının Remove komutu ürünü veritabanından sildik.
db.SaveChanges(); // db sınıfının SaveChanges komutu ile yaptığımız bu değişikliği kaydettik.
```

---

</details>


<details>
 <summary>LINQ nedir? En Çok Kullanılan LINQ İfadeleri</summary>

 ---

 <h3>LINQ Nedir?</h3>
 
 -LINQ (Language Integrated Query), .NET ekosisteminde verilerle çalışmayı standart hale getiren ve programlama dilinin içine doğrudan         sorgulama yeteneği ekleyen güçlü bir mimaridir.Klasik yöntemlerde verilerle çalışırken farklı diller kullanmak zorunda kalırız. LINQ ise bu   karmaşayı ortadan kaldırır. Tür bağımsız olarak; ister bir SQL veritabanından, ister bir bellekteki listeden, ister bir XML dosyasından veri  çekiyor olalım, hep aynı C# sözdizimini kullanmamızı sağlar.

 ---

 <h3>En Çok Kullanılan LINQ İfadeleri</h3>

 <ul>
   <li><code>Where()</code>: Belirli bir koşula uyan verileri seçmek için kullanılır.</li>
   <li><code>Select()</code>: Verilen bir listedeki nesnelerin sadece belirli özelliklerini seçmek veya dönüştürmek için kullanılır</li>
   <li><code>OrderBy()</code>: Verileri belirli bir özelliğe göre küçükten büyüğe  veya büyükten küçüğe sıralar.</li>
   <li><code>FirstOrDefault()</code>: Şarta uyan ilk elemanı getirir, eğer bulamazsa varsayılan boş değeri döndürür.</li>
   <li><code>ToList()</code>: Yazılan LINQ sorgusunu hemen çalıştırır ve sonuçları bir C# listesine  çevirir.</li>
   <li><code>Count()</code>: Koşula uyan veya listedeki toplam eleman sayısını verir.</li>
 </ul>

 ---

<h3>LINQ Örnekleri ve Karşılık Gelen SQL Açıklamaları </h3>

| İşlem                  | LINQ                            | SQL               |
|:-------------------------------------------|:-------------------------------------------------|:-------------------------------------------|
| Tüm Ürünleri Çekmek                        | db.Products.ToList();                            | SELECT * FROM Products;                    |
| Fiyatı 1000'den Büyük Olanları Filtrelemek | db.Products.Where(p => p.Price > 1000).ToList(); | SELECT * FROM Products WHERE Price > 1000; |
| Ürünleri Fiyata Göre Sıralamak             | db.Products.OrderBy(p => p.Price).ToList();      | SELECT * FROM Products ORDER BY Price;     |
| Sadece Ürün İsimlerini Almak               | db.Products.Select(p => p.Name).ToList();        | SELECT Name FROM Products;                 |
| ID'si 5 Olan Tek Bir Kaydı Bulmak          | db.Products.FirstOrDefault(p => p.Id == 5);      | SELECT TOP 1 * FROM Products WHERE Id = 5; |

---
LINQ kullanırken yazdığımız C# metotları,Entity Framework aracılığıyla yukarıdaki tabloda örnek verdiğimiz gibi veritabanının konuşabildiği saf SQL diline çevrilir. Bu sayede hem sorgu hatalarından kaçınırız hem de kodumuz çok daha okunabilir ve yönetilebilir hale gelir.

---

</details>

<details>
<summary>Code-First ve Database-First Yaklaşımı Nedir?</summary>

---

-Entity Framework Core kullanırken veritabanı ile uygulama kodumuzu nasıl senkronize edeceğimize karar veren iki ana yaklaşım vardır.


<h3>1. Code-First Yaklaşım</h3>
-Veritabanında hiçbir tablo oluşturmadan işe başlarız. Önce C# tarafında sınıflarını ve aralarındaki ilişkiyi yazarız. Entity Framework, yazdığımız bu kodlara bakarak veritabanındaki tabloları senin yerine otomatik olarak oluşturur.

---

<h3>2. Database-First Yaklaşım</h3>
-Önce veritabanını tasarlarız. Ardından Entity Framework'e "Git bu veritabanını oku ve veritabanına karşılık gelen C# sınıflarını otomatik üret" denir.Sistem, veritabanındaki tablolara bakarak bizim için C# sınıflarını otomatik olarak kod dosyası şeklinde oluşturur.

---

<h3>Code-First vs Database-First Karşılaştırması</h3>

| Özellik | Code-First| Database-First  |
|:---|:---|:---|
| **Temel Olayı** | Önce C# kodunu yazarız, veritabanı ona bakarak **otomatik oluşur**. | Önce veritabanı hazırdır, kodu ona bakarak **otomatik üretir**. |
| **Süreç Akışı** | C# Sınıfları -> Migration -> Veritabanı | Veritabanı -> Scaffolding -> C# Sınıfları |
| **Avantajları** | Kod üstünden tam kontrol, hızlı geliştirme, tip güvenliği. | Hazır veritabanına cuk diye oturur, SQL tarafı sağlam başlar. |
| **Dezavantajları** | Karmaşık özel DB ayarlarında bazen manuel müdahale ister. | DB şeması değiştiğinde sınıfları baştan taratmak gerekebilir, kod üstünde esneklik azdır. |
| **Hangi Yaklaşımı Seçmeliyiz? ** | Sıfırdan bir proje kuruyorsak, bütün kontrolü koda vermek istiyorsak **kesinlikle Code-First seçmeliyiz.** | Elimizde zaten yılların kurumsal, hazır veritabanı varsa veya dışarıdan hazır DB verildiyse **Database-First seçmeliyiz.** |

---

</details>

# 6.Güvenlik ve Performans

<details>
 <summary>Authentication vs Authorization Nedir? </summary>
 
---

-Bu iki kavram yazılım güvenliğinde sık karıştırılır.Authentication (Kimlik Doğrulama) ve Authorization (Yetkilendirme), temel olarak farklı güvenlik adımlarını temsil eder.

 ---

 <h3>Authentication Nedir?</h3>
 -Kimlik doğrulama (Authentication), sisteme erişmek isteyen bir kişinin iddia ettiği kişi olup olmadığını kanıtlama sürecidir. Günlük hayattan bir örnek vermek   gerekirse, bir binaya girerken güvenliğe kimliğinizi göstermeniz kimlik doğrulama işlemidir. Dijital dünyada ise kullanıcı adı ve şifre girmek, parmak izi        okutmak veya telefona gelen SMS kodunu yazmak bu sürece karşılık gelir. Sistem, girilen bilgilerin veritabanındaki kayıtlarla eşleşip eşleşmediğini kontrol       ederek kullanıcının gerçekliğinden emin olur ve "Sen gerçekten iddia ettiğin kişisin" onayını verir.
 
---

 <h3>Authorization Nedir?</h3>
 -Yetkilendirme (Authorization) ise kimliği başarıyla doğrulanmış bir kullanıcının sistem içerisinde hangi alanlara erişebileceğini, hangi dosyaları okuyup        değiştirebileceğini veya hangi işlemleri yapabileceğini belirleyen süreçtir. Konser alanına biletinizi gösterip girdikten sonra sadece normal izleyici alanında   mı duracağınıza, yoksa sahne arkası veya VIP bölüme geçip geçemeyeceğinize karar verilmesi yetkilendirmedir. Yazılım dünyasında da bir kullanıcının sisteme üye   olarak giriş yaptıktan sonra kendi profilini düzenleyebilmesi ancak sistem yöneticilerine özel admin paneline girememesi tamamen yetkilendirme mekanizmasının     bir sonucudur.

 ---
 
 ### Özetle kimlik doğrulama sizin kapıdan içeri girmenizi sağlarken, yetkilendirme içeride hangi odalara girebileceğinizi belirler.

 --- 

 <h3>Authentication vs Authorization</h3>

| Özellik | Authentication |Authorization |
| :--- | :--- | :--- |
| **Temel Tanım** | Kullanıcının kim olduğunu kanıtlama ve doğrulama sürecidir. | Doğrulanmış kullanıcının hangi kaynaklara erişebileceğini belirleme sürecidir. |
| **Cevapladığı Soru** | "Sen kimsin?" | "Neye erişim iznin var?"  |
| **İşlem Sırası** | Her zaman **önce** gerçekleşir. | Kimlik doğrulama gerçekleştikten **sonra** çalışır. |
| **Günlük Hayat Örneği** | Havalimanı dış hatlar terminaline girerken bilet ve pasaport kontrolünden geçmek. | Uçağa bindiğinizde ekonomi sınıfından kalkıp first class koltuğa oturmaya çalışırken hostesin biletinizi kontrol etmesi. |
| **Yazılım Örneği** | Bir Netflix hesabına kullanıcı adı ve şifrenizi girerek giriş yapmanız. | Giriş yaptıktan sonra çocuk hesabının sadece çizgi filmleri görebilmesi, yetişkin filmlerini açamaması. |

---
 
</details>


<details>
 <summary>JWT (JSON Web Token) Nedir, Nasıl Çalışır?</summary>

 ---

 <h3>JWT Nedir?</h3>
 
 -JWT (JSON Web Token), istemci ile sunucu arasında sunucuya yük bindirmeden kimlik doğrulamayı sağlayan, kriptografik imzalı standart bir veri yapısıdır.        Sunucu her kullanıcı için veritabanında oturum tutmak yerine, kullanıcı bilgilerini gizli bir anahtarla imzalayıp istemciye verir; sonraki isteklerde sunucu     veritabanına bakmadan sadece bu imzayı kontrol ederek işlemin geçerliliğini onaylar. Günlük hayattan örnek vermek gerekirse JWT, tıpkı bir otelde bileğinize     takılan akıllı otel bilekliğine benzer. Girişte kimliğinizi bir kez gösterip bileğinize bu mühürlü bilekliği taktırırsınız; tatil boyunca odanıza veya           yemekhaneye girerken tekrar tekrar kimlik göstermez, sadece bilekliğinizi okutarak geçersiniz. Yazılımsal olarak da; bir siteye giriş yaptığınızda sunucu        tarayıcınıza bu token'ı verir. Siz sayfalar arası gezinirken veya sepete ürün eklerken, tarayıcınız arka planda bu token'ı sunucuya göstererek sürekli yeniden   şifre girmenizi engeller.

 ---

 <h3>JWT Yapısı</h3>

 -Bir JWT, nokta (.) karakteriyle birbirine bağlanan üç ana bölümden oluşur:

 1.Header: JWT şifrelemesinde kullanılabilecek çeşitli şifreleme ve algoritma yöntemleri bulunur. Token'ın hangi algoritma (örneğin HS256 veya RS256) ile         imzalandığı ve türü bu kısımda açıkça belirtilir; böylece sunucu, token'ı doğrulayacağı zaman onu nasıl çözmesi gerektiğini ilk olarak bu başlığa bakarak        anlar.
 
 2.Payload: Kullanıcının ID'si, adı veya yetkileri gibi verilerin tutulduğu alandır. Şifrelenmez, sadece okunabilir formatta kodlanır; bu yüzden asla şifre       gibi hassas bilgiler konulmaz.
 
3. Signature:Header ve Payload verileri seçilen algoritmayla harmanlanır, sunucudaki gizli anahtar ile işlenerek ortaya benzersiz bir imza çıkar.Hackertokendaki herhangi bir veriyi değiştirmeye çalışırsa imza bozulur; sunucu kendi gizli anahtarıyla kontrol ettiğinde uyuşmazlığı anlar ve isteği reddeder.
  
 </ul>

 ---

 ### Örnek Bir JWT ve Çözülmüş Hali

| Bölüm | Token İçindeki Hali | Çözülmüş Hali  |
| :--- | :--- | :--- |
| **1. Header** | `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9` | `{"alg": "HS256", "typ": "JWT"}` |
| **2. Payload** | `eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkFoZXRzIFlpbG1heiIsImlhdCI6MTcxMDAwMDAwMH0` | `{"sub": "1234567890", "name": "Ahmet Yılmaz", "iat": 1710000000}` |
| **3. Signature** | `SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c` | Header ve Payload'ın gizli anahtarla imzalanmış hali |

---

<h3>Nasıl Çalışır</h3>

1. Login Talebi: İstemci, kullanıcı adı ve şifre gibi kimlik bilgilerini güvenli bir POST isteğiyle sunucuya iletir.
  
2. Token Üretimi: Sunucu gelen bilgileri veritabanından doğrular. Bilgiler doğruysa; kullanıcının ID'si ve yetkilerini içeren bir payload hazırlar,bunu          kendine ait gizli bir anahtarla imzalayarak bir JWT üretir ve istemciye geri döner.
  
3. Token'ın Saklanması: İstemci, sunucudan gelen bu token'ı tarayıcı tarafında uygun bir alanda saklar;genellikle LocalStorage, SessionStorage veya    en        güvenlisi olan HttpOnly Cookie tercih edilir. 
  
4. Korumalı İstekler: İstemci, veri istemek için sunucuya tekrar istek atacağı zaman, HTTP isteğinin başına token'ı ekler.

5. Kriptografik Doğrulama:Sunucu gelen isteği karşıladığında veritabanını hiç sorgulamaz; sadece kendi gizli anahtarını kullanarak token'ın imzasını ve          süresini matematiksel olarak kontrol eder. İmza orijinal çıkarsa işlemin onayını verir, aksi halde isteği anında reddeder.
 

 ---

 <h3>Avantajları</h3>
 
  
 -Sunucuda oturum tutma zorunluluğunu ortadan kaldırır, bu sayede sunucu yükü azalır.
  
 -Sunucu, her istekte veritabanını sorgulamak yerine sadece matematiksel imza kontrolü yapar.
  
 -Node.js, Python, Java veya farklı mobil/web teknolojileri arasında sorunsuz şekilde çalışır.
  
 -Boyutu küçüktür; HTTP başlıklarında çok hızlı bir şekilde taşınabilir.
 
 -Bir kez üretilen token, gizli anahtarı bilen tüm alt servisler tarafından ortak bir şekilde doğrulanıp kullanılabilir.
  
 

  ---

</details>
<details>
<summary>OAuth, OAuth2.0, OpenIddict, OpenID Nedir?</summary>

---

<h3>OAuth Nedir?</h3>
-OAuth, bir uygulamanın şifrenizi paylaşmanıza gerek kalmadan, başka bir servis üzerindeki verilerinize güvenli bir şekilde erişmesini sağlayan yetkilendirme standardıdır. Örneğin, Spotify'a "Google ile bağlan" dediğinizde şifrenizi Spotify görmez, ancak OAuth sayesinde Google, Spotify'a temel verilerinize erişmesi için güvenli ve sınırlı bir token verir.


<h3>OAuth2.0</h3>
-OAuth 2.0, ilk versiyonun eksiklerini kapatarak günümüzün modern web, mobil ve API dünyasına uyarlanmış, günümüzde tüm sosyal medya girişlerinin ve güvenli veri paylaşım protokollerinin temelini oluşturan endüstri standardıdır.


<h3>OpenID Nedir?</h3>
-OpenID , OAuth 2.0 protokolünün hemen üzerine inşa edilmiş ayrı bir katmandır.OpenID "Sisteme giriş yapan bu kullanıcı kim?" sorusunu yanıtlar ve kullanıcının kimliğini kanıtlar.


<h3>OpenIddict Nedir?</h3>
-OAuth 2.0 ve OpenID Connect protokolleri uyulması gereken birer protokoldür. Bu kuralları sıfırdan .NET'te kodlamak ve sunucu altyapısını kurmak büyük bir zahmettir. OpenIddict, bu protokolleri tek tek yazmakla uğraşmamak için .NET projelerine kurduğumuz hazır çerçevedir.

---

<h3>Örnek Senaryo</h3>

-Bir e-ticaret sitesine ilk kez kayıt olduğumuzu ve "Google ile Giriş Yap" butonunu kullandığımızı hayal edelim:

1.AŞAMA-Kimlik Doğrulama (OpenID Connect):Butona tıkladığımızda site bizi Google'a yönlendirir. Google'da oturum açtığımızda Google, "Bu kişi gerçekten Ahmet, e-postası ahmet@gmail.com" diyerek kimliğimizi doğrular ve bir kimlik belgesi üretir.Eğer bu kimlik belgesi olmasaydı, e-ticaret sitesi sürekli Google'a dönüp "Bu kişi gerçekten kim?" diye sormak zorunda kalırdı. Bu belge, bu soruyu tek seferde ve güvenli bir şekilde kapatır.

2.AŞAMA-Yetkilendirme (OAuth 2.0): Ardından Google bize, "Bu e-ticaret sitesi temel profil bilgilerine erişmek istiyor, izin veriyor musun?" diye sorar. "İzin ver" dediğimizde, Google şifremizi siteye asla vermez; bunun yerine sitenin verilerimize sınırlı bir şekilde erişmesini sağlayan bir erişim tokeni verir.

-OpenIddict: Biz bu sistemi .NET üzerinde geliştirirken OAuth ve OpenID kurallarını sıfırdan kodlamakla uğraşmayız; projemize OpenIddict kütüphanesini kurarak tüm bu token ve güvenlik altyapısını hazır olarak yönetiriz.

---

</details>



<details>
 <summary>Performans Artımı İçin Ne Yapılabilir? </summary>

---

 -Günümüzün dijital ekosisteminde yazılım projelerinin başarısı, yalnızca doğru çalışan özellikler sunmakla sınırlı değildir; kusursuz bir kullanıcı deneyiminin   en temel yapı taşı performans ve hızdır. Kullanıcıların milisaniyeler içinde yanıt alamadığı, yavaş yüklenen ekranlarla karşılaştığı anlarda sabrı hızla         tükenmekte ve rakip alternatiflere yönelmesi an meselesi olmaktadır.Sadece son kullanıcı tarafında değil, arka plandaki bulut maliyetleri, sunucu kaynak         tüketimi ve sistemin yüksek trafik altındaki kararlılığı açısından da performans optimizasyonu artık lüks değil, olmazsa olmaz kritik bir mühendislik            disiplinidir. .NET projelerinde bu hıza ulaşmak ve kaynakları en verimli şekilde yönetmek için doğru mimari kararları almamız gerekir.

---

<h3>Performans Artırımı İçin Önerilen Teknikler</h3>

### `AsNoTracking` :
-Entity Framework Core, varsayılan olarak veritabanından bir veri çektiğimiz an arkada görünmez bir dedektif (Change Tracker) görevlendirir. Bu dedektif, "Acaba bu veriyi kod içinde değiştirdin mi?" diye sürekli o nesneyi izler; çünkü hedefi SaveChanges çağrıldığında değişiklikleri veritabanına otomatik yansıtmaktır.Ancak amacımız sadece veriyi okumak, ekrana basmak veya listelemekse, o dedektifin peşinde gezmesi fazladan CPU ve RAM harcayan tam anlamıyla bir kaynak israfıdır. Sorgularımıza `AsNoTracking()` ekleyerek EF Core'a "Bu veriyi çek ama arkasına dedektif dikme, sadece okuyup geçeceğim" komutunu verir; böylece bellek yükünü azaltıp performansı anında yukarı çekeriz.

### `IAsyncEnumerable` :
-Milyonlarca satırlık devasa veri setleriyle çalışırken `ToListAsync()` patlatıp tüm veriyi tek seferde RAM'e yığmaya kalkarsak sunucu `OutOfMemoryException` yiyip çökebilir. `IAsyncEnumerable<T> `sayesinde veritabanından verileri musluktan damlar gibi parça parça 
 asenkron bir şekilde çekeriz. Böylece RAM şişmez, veriler geldikçe anlık olarak işleyip tüketiriz.

### `Caching` :
-Sürekli değişmeyen veya hesaplanması ağır olan, aynı zamanda sık sık ihtiyaç duyduğumuz verileri her seferinde veritabanına sorup sistemi yormak yerine, ilk seferinde çekip RAM'de saklar, sonraki isteklerde doğrudan RAM'den okuruz; böylece RAM'i gereksiz yere şişirmeden hız kazanırız.

### `Redis` :
-Uygulama iç caching tek sunucu için harikadır; ancak sistem büyüyüp birden fazla sunucuya geçtiğimizde her sunucu kendi önbelleğini tutmaya başlar ve veri tutarsızlığı çıkar. Redis tam burada devreye girer; bu önbellek verilerini ortak ve merkezi bir havuzda tutan, tamamen RAM üzerinde çalıştığı için bize inanılmaz bir hız sunan harika bir cache ve veri sunucusudur.

### `Profiling` :
-Kodun nerede yavaşladığını tahmin etmek yerine veriye dayalı olarak nokta atışı tespit etme sürecidir. Hangi metodun ne kadar CPU harcadığını, hangi sorgunun sistemi kilitlediğini MiniProfiler veya BenchmarkDotNet gibi araçlarla milisaniyesine kadar ölçer, problemi tam yerinden çözeriz.

---
 
</details>



<details>
<summary>OWASP TOP 10</summary>
 
 ---
 
-OWASP (Open Web Application Security Project), web güvenliğini geliştirmeye odaklanmış uluslararası ve bağımsız bir siber güvenlik topluluğudur. Yazılımlarda en sık rastlanan zafiyetleri ve saldırı tiplerini analiz ederek geliştiriciler için bir rehber sunar. Bu kapsamda periyodik olarak yayımladıkları OWASP Top 10 listesi, web uygulamalarındaki en kritik 10 güvenlik riskini ortaya koyan ve sektörde temel kabul edilen en bilinen çalışmadır.

---

<h3>En Yaygın Güvenlik Açıkları ve Tanımları</h3>

* **SQL Injection (SQLi):** Kullanıcıdan alınan girdilerin filtrelenmeden doğrudan SQL sorgusuna eklenmesi sonucu, saldırganın veritabanında yetkisiz sorgu çalıştırması veya verileri çalmasıdır.
* **Cross-Site Scripting (XSS):** Web sayfasına kötü amaçlı JavaScript kodları enjekte edilmesi ve bu sayfayı açan diğer kullanıcıların oturum bilgilerinin ele geçirilmesidir.
* **Cross-Site Request Forgery: Giriş yapmış bir kullanıcının tarayıcısı üzerinden, kullanıcının haberi olmadan yetkisiz istekler  gönderilmesidir.
* **Broken Authentication :** Zayıf şifre politikaları veya oturum yönetimi hataları yüzünden kullanıcı hesaplarının saldırganlarca kolayca ele geçirilmesidir.

---

<h3>OWASP Top 10 Güvenlik Açıkları</h3>

| # | Güvenlik Açığı | Açıklama | Tipik Risk / Örnek |
| :--- | :--- | :--- | :--- |
| **01** | **Broken Access Control** | Kullanıcının yetkisi dışındaki sayfalara, verilere veya işlemlere erişebilmesidir. | URL'deki `user_id=5` değerini `6` yaparak başkasının profilini/faturasını görüntüleme. |
| **02** | **Cryptographic Failures**  | Hassas verilerin  şifrelenmeden veya zayıf algoritmalarla aktarılmasıdır. | Kullanıcı şifrelerinin veritabanında düz metin saklanması veya HTTPS kullanılmaması. |
| **03** | **Injection**  | Güvenilmeyen kullanıcı girdilerinin doğrudan veritabanı veya komut satırı sorgularına dahil edilmesidir. | Giriş formuna `' OR 1=1 --` yazılarak şifresiz admin girişi yapılması. |
| **04** | **Insecure Design**  | Güvenlik risklerinin kodlama aşamasında değil, mimari ve iş mantığı tasarımında göz ardı edilmesidir. | Şifre sıfırlama için tek bir tahmin edilebilir güvenlik sorusu kullanılması. |
| **05** | **Security Misconfiguration**  | Sunucu veya framework üzerindeki varsayılan ayarların, açık portların veya hata sayfalarının güvensiz bırakılmasıdır. | Canlı ortamda 'debug mode' açık unutulup hata anında veritabanı yollarının ekranda görünmesi. |
| **06** | **Vulnerable & Outdated Components**  | Projede bilinen güvenlik açığı (CVE) bulunan eski kütüphane veya paketlerin kullanılmasıdır. | Güvenlik yaması almamış eski bir NuGet/npm paketinin saldırganlarca istismar edilmesi. |
| **07** | **Identification & Authentication Failures**  | Giriş sistemlerinin, oturum yönetiminin ve şifre politikalarının zayıf uygulanmasıdır. | Giriş ekranında deneme sınırı  olmaması nedeniyle şifrenin kaba kuvvetle kırılması. |
| **08** | **Software & Data Integrity Failures**  | Kod, eklenti veya veri güncellemelerinin kaynağının ve bütünlüğünün doğrulanmadan yüklenmesidir. | Doğrulanmamış bir CDN'den zararlı JavaScript çekilmesi. |
| **09** | **Security Logging & Monitoring Failures** | Güvenlik olaylarının  kaydedilmemesi ve saldırıların geç fark edilmesidir. | Bir sisteme sızıldığında log tutulmadığı için saldırının aylar sonra fark edilmesi. |
| **10** | **Server-Side Request Forgery ** | Saldırganın, sunucuya dışarıdan beklenmeyen veya iç ağdaki  adreslere istek attırmasıdır. | Bir web sitesinin "URL'den resim yükle" özelliğini kullanarak sunucunun iç IP adreslerinin taranması. |

---

<h3>ASP.NET Core ile Alınabilecek Önlemler</h3>

-Bu güvenlik açıklarını ASP.NET Core tarafında engellemek için kullanılan temel yöntemler şunlardır:

---

<h4>1. Model Validation</h3> 

-Gelen verinin tip, uzunluk ve format kurallarına uygunluğunu denetler; hatalı veriyi doğrudan reddeder.

```csharp
public class RegisterDto
{
    [Required(ErrorMessage = "Kullanıcı adı zorunludur.")]
    [StringLength(50, MinimumLength = 3)]
    public string Username { get; set; } = string.Empty;

    [Required]
    [EmailAddress(ErrorMessage = "Geçerli bir e-posta giriniz.")]
    public string Email { get; set; } = string.Empty;
}
```
---

<h4>2.Input Sanitization</h3>

-Kullanıcının gönderdiği HTML içeriklerdeki zararlı JavaScript etiketlerini temizler.

```csharp
// Paket: Ganss.Xss.HtmlSanitizer
var sanitizer = new HtmlSanitizer();

// Zararlı script silinir, sadece güvenli metin kalır
string cleanHtml = sanitizer.Sanitize(rawInputHtml);
```
---

<h4>3.SQL Injection Koruması</h3>

-LINQ sorguları veriyi otomatik parametreleştirir, ham SQL birleştirmesinden doğan riskleri önler.

```Csharp
// GÜVENLİ: Otomatik parametrik sorgu
var user = await _context.Users
    .FirstOrDefaultAsync(u => u.Email == inputEmail);
```
---

<h4>4.CSRF Koruması</h3>

-Kullanıcının oturumu üzerinden üçüncü parti sitelerden sahte istek atılmasını engeller.

```Csharp
[HttpPost]
[ValidateAntiForgeryToken]
public IActionResult UpdatePassword(ChangePasswordDto dto)
{
    // İşlem başarılı
    return Ok();
}
````
---

<h4>5.Kimlik & Oturum Güvenliği</h3>

-Çerezleri JavaScript erişimine kapatır ve hatalı girişlerde hesabı kilitler.

```Csharp
builder.Services.ConfigureApplicationCookie(options =>
{
    options.Cookie.HttpOnly = true;              // JS erişimini kapatır (XSS önlemi)
    options.Cookie.SecurePolicy = CookieSecurePolicy.Always; // Yalnızca HTTPS
    options.Lockout.MaxFailedAccessAttempts = 5; // 5 hatalı denemede kilitle
});
```
---

</details>


# 7.Logging ve Hata Yönetimi 

<details>
 <summary>Neden Loglama Yapılır? Log Seviyesi Nedir?</summary>

 ---
 
-Loglama, bir sistemin çalışma anında gerçekleştirdiği olayları, durum değişikliklerini, hataları ve kullanıcı etkileşimlerini zaman         damgasıyla birlikte kayıt altına alma işlemidir.

---


<h3>Neden Loglama Yapılır?</h3>

-Canlı ortamda kod debug edilemez. Hatanın ne zaman, nerede ve neden çıktığını anlamak için loglara bakılır.
 
-Sistemin nerede yavaşladığını, hangi sorguların geciktiğini ve kaynak tüketimini izlemek için tutulur.

-Hangi kullanıcının ne zaman, hangi veriye eriştiğini veya yetkisiz denemeleri belgelemek için saklanır.

-Kullanıcıların sistemde nasıl ilerlediğini ve iş süreçlerinin aksamadan işleyip işlemediğini görmek için kullanılır.
 
---

<h3>Log Seviyesi Nedir?</h3>

-Her olayın önemi aynı değildir; log seviyesi, mesajları önem derecesine göre etiketleyerek hem diskin gereksiz yere dolmasını önler hem de  geliştiricinin sadece kritik hatalara hızlıca odaklanmasını sağlar.

<h4>Log Seviyeleri</h4>

| Seviye | Öncelik | Ne Zaman Kullanılır? | Örnek |
| :--- | :--- | :--- | :--- |
| **TRACE** | En Düşük | Kod akışının en ince ayrıntılarıdır. | `Fonksiyona parametre: [x=5] ile girildi.` |
| **DEBUG** | Düşük | Geliştirme/test aşamasında değişken değerlerini ve iç durumu izlemek için. | `Kullanıcı ID: 42 cache'de bulunamadı.` |
| **INFO** | Orta | Sistemin normal ve beklenen işleyişine dair genel durum bildirimleri. | `Kullanıcı başarıyla giriş yaptı.` |
| **WARN** | Yüksek | Sistem çalışıyor ama potansiyel tehlike veya beklenmedik durum var. | `Bellek kullanımı %85 sınırına ulaştı.` |
| **ERROR** | Çok Yüksek | Bir işlem başarısız oldu veya hata verdi ama sistem genel olarak ayakta. | `Ödeme servisi yanıt vermedi, işlem iptal.` |
| **FATAL** | En Yüksek | Sistemin tamamen çökmesine neden olan kritik felaket durumu. | `Veritabanı bağlantısı koptu, uygulama durduruldu.` |

---

</details>

<details>
 <summary>ASP.NET Core'da Logging Altyapısı </summary>

-ASP.NET Core, harici bir kütüphaneye gerek kalmadan çalışan güçlü bir yerleşik loglama altyapısına sahiptir.

<h3>Temel Çalışma Mantığı</h3>

* **`ILogger<T>`:** Koddaki olayları loglamak için Dependency Injection  ile sınıflara çağrılan ana arayüzdür.

* **Structured Logging :** Logları string birleştirmek (`$""`) yerine parametrik `{Parametre}` şablonuyla yazar. Böylece loglar JSON nesnesi olarak tutulur ve aramalarda kolayca filtrelenir.
  
* **`appsettings.json`:** Kod derlenmeden hangi seviyedeki logların tutulacağı ayarlanır.

```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning",
      "Microsoft.EntityFrameworkCore.Database.Command": "Information"
    }
  }
}
```
</details>

<details>
 <summary>Global Exception Handling Nedir? Nasıl Yapılır? </summary>

---

<h3>Global Exception Handling Nedir?</h3>

-Projedeki her controller veya servis metodunun içine tek tek `try-catch` blokları yazmak hem kod kalabalığı yaratır hem de gözden kaçan bir hata anında uygulamanın dış dünyaya kontrolsüz, güvensiz teknik hata sayfaları fırlatmasına neden olur. Global Exception Handling, uygulamanın en dış katmanına merkezi bir güvenlik ağı kurma yaklaşımıdır. Sistemde nerede ve ne zaman bir hata fırlatılırsa fırlatılsın, bu merkezi ağ hatayı havada yakalar, uygulamanın çökmesini engeller ve kullanıcıya standart, temiz bir hata yanıtı döner. Böylece iş mantığı içeren kodlar gereksiz hata bloklarından arınır ve hata yönetimi tek bir standart üzerinden yürütülür.

---

-ASP.NET Core tarafında bu mimariyi hayata geçirirken iki temel bileşenden yararlanırız: 

<h3>1. UseExceptionHandler</h3>

-ASP.NET Core'un hazır middleware bileşenidir ve Global Exception Handling'in  yakalama görevini üstlenir. HTTP istek hattında meydana gelen ve yakalanmamış tüm exceptionsları otomatik olarak yakalar. Görevi, hatanın kullanıcıya doğrudan yansımasını önlemek, HTTP durum kodunu  ayarlamak ve kullanıcıya sistemin iç yapısını  ifşa etmeyen güvenli, sade bir JSON formatında yanıt üretmektir.

<h3>2. ILogger</h3>

-ASP.NET Core'un hazır loglama arayüzüdür ve Global Exception Handling sürecinde hatanın arka plandaki kaydını tutma görevini üstlenir. 
`UseExceptionHandler` hatayı yakaladığında, kullanıcıya gösterilmeyen kritik teknik detaylar  `ILogger` aracılığıyla `ERROR` veya `CRITICAL` seviyesinde log dosyalarına veya merkezi log sunucularına yazılır. Bu sayede yazılımcı, kullanıcıya hiçbir teknik detay hissettirmeden sistemde neyin, nerede patladığını eksiksiz şekilde analiz edebilir.

---

Aşağıdaki kod örneğinde, hem `UseExceptionHandler` ile hatayı merkezi olarak yakalayıp kullanıcıya temiz yanıt dönmeyi hem de `ILogger` ile hatanın tüm detaylarını arka plana kaydetmeyi tek bir noktada sağladık.

```csharp
using Microsoft.AspNetCore.Diagnostics;

var builder = WebApplication.CreateBuilder(args);
builder.Services.AddControllers();

var app = builder.Build();

// GLOBAL EXCEPTION HANDLER (Merkezi Yakalama ve Loglama)
app.UseExceptionHandler(errorApp =>
{
    errorApp.Run(async context =>
    {
        context.Response.StatusCode = StatusCodes.Status500InternalServerError;
        context.Response.ContentType = "application/json";

        var exceptionFeature = context.Features.Get<IExceptionHandlerPathFeature>();
        var logger = context.RequestServices.GetRequiredService<ILogger<Program>>();

        if (exceptionFeature != null)
        {
            var exception = exceptionFeature.Error;
            var path = exceptionFeature.Path;

            // 1. ILogger: Hatanın tüm teknik detayını arka planda logla
            logger.LogError(exception, "Kritik Sistem Hatası! Yol: {Path} | Mesaj: {Message}", path, exception.Message);

            // 2. UseExceptionHandler: Kullanıcıya kod detayı vermeden güvenli mesaj dön
            var response = new
            {
                Status = 500,
                Message = "Sunucu tarafında beklenmeyen bir hata oluştu. Lütfen daha sonra tekrar deneyiniz."
            };

            await context.Response.WriteAsJsonAsync(response);
        }
    });
});

app.MapControllers();
app.Run();
```

---

</details>


#  8. Yazılım Geliştirme Prensipleri

<details>
 <summary>SOLID prensipleri</summary>

---

-SOLID; yazılım mimarisini daha esnek, anlaşılır, test edilebilir ve değişime açık tutmak amacıyla Robert C. Martin tarafından derlenen beş  temel nesne yönelimli tasarım ilkesidir.

---

1. Single Responsibility Principle — Tek Sorumluluk Prensibi

-Bir sınıfın değişmek için yalnızca tek bir nedeni ve odaklandığı tek bir sorumluluğu olmalıdır. Bir sınıfa hem veri tabanı işlemini hem de e-posta gönderimini yüklemek hata riskini artırır.

**Örnek :**
  * ❌ *Hatalı:* `UserService` sınıfının hem kullanıcıyı kaydetmesi hem de hoş geldin e-postası göndermesi.
  * ✅ *Doğru:* `UserRepository` sınıfının sadece kayıt işine, `EmailService` sınıfının sadece bildirim işine bakması; `UserService`'in bu    iki servisi koordine etmesi.

---

 2. Open/Closed Principle  — Açık / Kapalı Prensibi

-Yazılım varlıkları yeni özellikler eklenmesine açık, ancak var olan çalışan kaynak kodunun değiştirilmesine kapalı olmalıdır.

 **Örnek**
 
  * ❌ *Hatalı:* Yeni bir ödeme yöntemi geldiğinde `PaymentService` içindeki `if-else` bloklarını açıp değiştirmek.
  * ✅ *Doğru:* Bir `PaymentMethod` arayüzü tanımlayıp; `CreditCardPayment`, `PayPalPayment` ve `CryptoPayment` sınıflarını bu arayüzden türeterek sisteme dokunmadan yeni yöntemler eklemek.

---

3. Liskov Substitution Principle — Liskov İkame Prensibi

-Alt sınıflar, miras aldıkları üst sınıfların yerine geçebilmeli ve programın beklenen davranışını bozmamalıdır.

**Örnek**
  * ❌ *Hatalı:* `Bird` sınıfına `fly()` metodu koyup, uçamayan `Ostrich` (Devekuşu) sınıfında bu metottan hata fırlatmak.
  * ✅ *Doğru:* `Bird` üst sınıfını genel bırakıp, yalnızca uçabilen kuşlar için `FlyingBird` arayüzü/sınıfı tanımlamak.

---

4. Interface Segregation Principle — Arayüz Ayrımı Prensibi

-Sınıflar, kullanmadıkları ve ihtiyaç duymadıkları metotları barındıran hantal arayüzleri uygulamaya zorlanmamalıdır.

**Örnek :**
  * ❌ *Hatalı:* `SmartDevice` arayüzüne `print()`, `scan()`, `fax()` koyup, sadece çıktı alan basit bir yazıcıyı tarayıcı ve faks metotlarını boş bırakmaya zorlamak.
  * ✅ *Doğru:* Arayüzü `Printer`, `Scanner` ve `Fax` olarak bölmek; yazıcının sadece `Printer` arayüzünü uygulamasını sağlamak.

---

5. Dependency Inversion Principle  — Bağımlılıkların Tersi Prensibi

-Yüksek seviyeli modüller alt seviyeli somut modüllere değil; her iki katman da soyutlamalara bağımlı olmalıdır.

 **Örnek Senaryo:**
  * ❌ *Hatalı:* `OrderService` sınıfının içinde `new MySQLDatabase()` yazarak doğrudan MySQL'e göbekten bağlanması.
  * ✅ *Doğru:* Bir `Database` arayüzü tanımlayıp, `OrderService`'e bu arayüzü dışarıdan dependency Injection ile vermek; böylece             istenildiğinde Mongo veya PostgreSQL'e kod değiştirmeden geçebilmek.

---

</details>



<details>
 <summary>Design Patterns</summary>

 ---

 <h3>Nedir?</h3>
 
 -Design Patterns (Tasarım Kalıpları),yazılım geliştirirken sıkça karşılaşılan mimari sorunlara yıllar içinde bulunmuş, kendini kanıtlamış ve standartlaşmış çözüm taslaklarıdır. Hazır bir kütüphane veya kod bloğu değil; kodun daha esnek, okunabilir ve yönetilebilir olmasını sağlayan mantıksal rehberlerdir. Proje büyüdükçe kodun dağılmasını önler ve ekip içinde ortak bir mühendislik dili oluşturur.

---

### 1. Singleton Pattern (Tekillik Kalıbı)

-Bir sınıfın uygulama yaşam döngüsü boyunca yalnızca tek bir örneğinin oluşturulmasını garanti eder ve bu örneğe global bir erişim noktası sağlar. Sistem kaynaklarının gereksiz yere birden fazla kez tüketilmesini önler.

**Örnek**
  * ❌ *Hatalı:* Uygulama içinde veritabanı bağlantısı veya loglama ihtiyacı olan her servisin kendi içinde `new DatabaseConnection()` diyerek yüzlerce ayrı bağlantı açması ve sistemi kilitlemesi.
  * ✅ *Doğru:* `DatabaseConnection` sınıfının kurucusunu (constructor) `private` yapıp, yalnızca `getInstance()` metodu üzerinden tek bir ortak bağlantı havuzunu tüm uygulamaya kullandırmak.

---

## 2. Repository Pattern (Depo / Veri Erişim Kalıbı)

* **Kategori:** Yapısal / Mimari (Structural / Architectural)
* **Açıklama:** Veri tabanı veya harici veri kaynaklarına erişim mantığını, iş mantığından (Business Logic) tamamen soyutlayan kalıptır. Kodun veri kaynağının türünden (SQL, NoSQL, REST API vb.) bağımsız çalışmasını sağlar.
* **Örnek Senaryo:**
  * ❌ *Hatalı:* `UserService` veya Controller katmanında doğrudan SQL sorguları yazıp (`SELECT * FROM users`), veritabanı ORM'ine veya tablolarına doğrudan bağlanmak.
  * ✅ *Doğru:* Bir `IUserRepository` arayüzü tanımlayıp `getById()`, `save()`, `delete()` gibi metotlar üzerinden veri işlemlerini yönetmek; böylece veritabanı teknolojisi değiştiğinde iş mantığına dokunmamak ve mock nesnelerle kolayca birim testi yazabilmek.

---

## 3. Factory Pattern (Fabrika Kalıbı)

* **Kategori:** Yaratımsal (Creational)
* **Açıklama:** Nesne oluşturma mantığını istemciden (client) gizleyerek, hangi nesnenin üretileceğini çalışma anındaki parametrelere veya koşullara göre belirleyen bir fabrika metoduna devretme yöntemidir.
* **Örnek Senaryo:**
  * ❌ *Hatalı:* Sipariş onaylandığında `if (type === "SMS") new SmsNotification(); else if (type === "Email") new EmailNotification();` şeklinde `new` anahtar kelimesiyle somut sınıfları doğrudan kodun içine gömmek.
  * ✅ *Doğru:* Bir `NotificationFactory` sınıfı oluşturup `createNotification(type)` metodu çağırmak; istemcinin arka plandaki nesne yaratım detaylarını bilmeden yalnızca ortak `INotification` arayüzünü kullanmasını sağlamak.

---
 
</details>
