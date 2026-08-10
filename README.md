# Trex Research

# 1. Modern Yazılım Geliştirme Pratikleri

<details>
 <summary><b>Git Nedir? GitHub Nedir?</b></summary>
 <br>
  <h3>Git Nedir?</h3>
 <ul>
   <li>Git, tamamen kendi bilgisayarınızda çalışan bir versiyon kontrol sistemidir. Bilgisayarınızdaki dosyalarda yaptığınız her değişikliği versiyon versiyon       kaydeder, istediğiniz an istediğiniz versiyona dönmenizi sağlar. Git sadece yazılım projeleri için kullanılmaz, bütün işlerinizde kullanabilirsiniz.</li>
 </ul>
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
   <li> ** git init: ** Sıfırdan başlama komutudur. Bilgisayarınızdaki normal bir klasörün içine Git'i kurar ve "artık buradaki dosyaları takip et" der.</li>
   
   <li>git clone: GitHub platformu gibi internet üzerinden erişimin olan bir projeyi, tüm geçmiş versiyonlarıyla birlikte bilgisiyarınıza indirir.</li>
   
   <li>git add: Değişiklik yaptığın dosyaları sepete koyar. Git'e "Birazdan bu dosyaları kaydedeceğim, bunları aklında tut" demektir.</li>
   
   <li>git commit: Sepete eklenen dosyaların o anki durumunun fotoğrafını çeker ve kalıcı bir versiyon olarak kaydeder.git commit -m yazıp tırnak içinde "şunu değiştirdim"     gibi bir açıklama mesajıyla yapılır.</li>
   
   <li>git push: Kendi bilgisayarında kaydettiğin yeni versiyonları, internetteki yedeğine fırlatır ve orayı günceller.</li
   
   <li>git pull: Ekip arkadaşlarımız projeye GitHub gibi platformlar üzerinden yeni kodlar yüklediğinde;bu komut, internetteki o yeni değişiklikleri senin bilgisayarına       çeker ve dosyalarını günceller.</li>
   
   <li>git branch: Çalışan sistemi bozmadan denemeler yapmak veya yeni bir özellik kodlamak için açtığın paralel çalışma alanıdır.Ekip üyelerinin projede yaptığı her          değişikliği doğrudan çalışan sistem üzerine eklersek bir çok problem ortaya çıkabilir branch yöntemi bunun önüne geçiyor.</li>
   
   <li>git merge: Bir ekip üyesinin kendi branchında yaptığı değişiklikler bittiğinde ve bu değişikliklerin sorunsuz çalıştığından emin olduğunda, o yeni değişiklikleri       ana projeyle pürüzsüzce birleştirme işlemidir.</li>
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
