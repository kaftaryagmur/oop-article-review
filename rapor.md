# Code Smells and Refactoring: Makale İnceleme Raporu

## Makale Künyesi

**Lacerda, G., Petrillo, F., Pimenta, M. ve Guéhéneuc, Y.-G. (2020).** “Code Smells and Refactoring: A Tertiary Systematic Review of Challenges and Observations.” *Journal of Systems and Software*, 167, 110610. https://doi.org/10.1016/j.jss.2020.110610. Açık ön baskı: https://arxiv.org/abs/2004.10777

## 1. Giriş

Yazılım bakımı hata düzeltmenin yanında yeni gereksinimlere uyum ve işlev ekleme faaliyetlerini kapsar. Lacerda vd., önceki kaynaklara dayanarak bakımın toplam yazılım maliyetindeki payının %50–%80 aralığında bildirildiğini belirtir. Tasarım kararları aşındıkça kod karmaşıklaşır; yetersiz dokümantasyon koşullarında kaynak kod sistem hakkındaki başlıca bilgi kaynağına dönüşür. *Code smell*, doğrudan bir program hatası olmak zorunda olmayan, fakat bakım ve evrimi zorlaştıran yapısal bir belirtidir. *Refactoring* (yeniden yapılandırma) ise yazılımın gözlemlenebilir davranışını koruyarak iç yapısını iyileştirmeyi amaçlayan dönüşümlerdir [1].

Bu kavramlar aynı bakım probleminin farklı yönlerini temsil etmesine karşın araştırma literatürü iki alanı büyük ölçüde ayrı incelemiştir. Seçilen 40 ikincil çalışmanın 25'i smell, 13'ü refactoring temasında sınıflandırılırken yalnız ikisi iki temayı açıkça birlikte ele almıştır [1, Bölüm 3.6]. Lacerda vd. bu parçalı literatürü birleştirmek amacıyla derleme ve sistematik incelemeleri sentezleyen üçüncül sistematik literatür incelemesi yürütmüştür.

## 2. Makalenin Konusu, Amacı ve Araştırma Soruları

Çalışma, iki alandaki ikincil araştırmaların neyi ortaya koyduğunu, hangi konuların belirsiz kaldığını ve alanların yazılım kalitesi üzerinden nasıl ilişkilendirilebileceğini değerlendirir. “Observation” literatürde oluşan uzlaşıyı, “challenge” ise daha fazla araştırılması gereken açık konuyu ifade eder. Beş araştırma sorusu şöyledir:

1. **RQ1:** İkincil çalışmalarda refactoring ile ilgili hangi konular araştırılmıştır?
2. **RQ2:** İkincil çalışmalarda smell ile ilgili hangi konular araştırılmıştır?
3. **RQ3:** Code smell tespiti ve refactoring desteği için hangi araçlardan söz edilmiştir?
4. **RQ4:** Hangi araştırma soruları çalışılmıştır; en çok atıf alan ikincil çalışmalar hangileridir?
5. **RQ5:** Çalışma türleri, kalite ve incelenen birincil çalışma sayıları bakımından yıllık eğilimler nelerdir? [1, Bölüm 3.1]

Sorular konu kapsamından araç desteğine, araştırma söyleminin yapısından alanın yöntemsel gelişimine uzanan bütüncül bir tasarım kurar.

## 3. Araştırma Yöntemi

Çalışma, Kitchenham ve arkadaşlarının yönergelerini izleyen üçüncül bir SLR'dir. Süreç amaç/RQ tanımlama, ilgili literatürü bulma, seçim, kalite değerlendirmesi ve veri çıkarımı adımlarından oluşur. Aramalar ACM Digital Library, IEEE Xplore, ScienceDirect, Wiley, Scopus, AIS eLibrary, Google Scholar ve Springer'da yapılmıştır. Kapsam Opdyke'ın öncü tezinin yılı olan 1992'den 2018'e uzanır [1, Bölüm 3].

Seçim akışı 467 kayıtla başlamış, başlık/özet/anahtar kelime elemesinden sonra 59 çalışma seçilmiştir. Altı tekrar ve yirmi ölçüt dışı çalışma çıkarılınca 33 çalışma kalmış; *snowballing* ile yedi çalışma daha eklenerek nihai örneklem 40'a ulaşmıştır [1, Bölüm 3.6, Şekil 3]. Böylece 467 → 59 → 33 + 7 = 40 akışındaki her sayı farklı işlem aşamasını temsil eder.

Survey, sistematik haritalama ve SLR'ler DARE temelli dört kalite sorusuyla değerlendirilmiştir. Veri çıkarımı yayın bilgileri, arama/seçim yaklaşımı, RQ'lar, birincil çalışmalar, kalite puanı, konu ve araç alanları üzerinden yapılmış; kümeler *card sorting* ile oluşturulmuştur. Yalnız İngilizce, çevrim içi erişilebilir ve altı sayfadan uzun çalışmaların alınması süreci belirginleştirirken dil ve erişim yanlılığı yaratır.

DARE temelli değerlendirme; incelemenin dahil etme ve dışlama ölçütlerini açıklayıp açıklamadığını, aramanın yeterli olup olmadığını, seçilen çalışmaların kalitesini değerlendirip değerlendirmediğini ve temel çalışmalar hakkında yeterli bilgi sunup sunmadığını sorgular [1, Bölüm 3.4]. Bu yaklaşım, farklı türlerdeki ikincil çalışmaları ortak bir taban üzerinden karşılaştırmaya yardımcı olur. Bununla birlikte kalite puanı, incelenen birincil kanıtın doğru olduğunu tek başına göstermez; daha çok ikincil çalışmanın yöntemini ne ölçüde açık ve sistematik raporladığını gösterir. Dolayısıyla yüksek raporlama kalitesi ile güçlü ampirik kanıt birbirinden ayrılmalıdır.

Arama sonuçlarının veri tabanları arasında farklılaşması da yöntemin yorumlanmasında önemlidir. Yazarlar sekiz kaynağın birleşiminde ortalama arama doğruluğunu %12,63 olarak bildirir; Google Scholar %33,33 ile en yüksek, Springer %5,62 ile en düşük değere sahiptir [1, Bölüm 3.6]. Bu fark, geniş kapsamlı aramanın daha çok aday çalışma üretirken daha fazla ilgisiz kaydın elle elenmesini gerektirdiğini gösterir. Buna karşılık snowballing ile eklenen yedi çalışma, yalnızca anahtar sözcük sorgularına dayanmanın ilgili literatürün bir bölümünü kaçırabileceğini ortaya koyar.

## 4. Bulgular ve Sonuçlar

### 4.1 RQ1 — Refactoring

Refactoring temasındaki 13 çalışma teknikler, fırsat belirleme, kalite etkisi, evrim ve teknik borç gibi başlıklara dağılır. *Extract Method* ve *Extract Class* gibi çıkarma teknikleri sık incelenir. Bununla birlikte akademide en çok incelenen tekniklerle geliştiricilerin pratikte en sık kullandıkları aynı değildir: yeniden adlandırma gibi basit işlemler pratikte yaygın olduğu hâlde fırsat çalışmalarında aynı ilgiyi görmez [1, Bölüm 4.1]. Atıf sıklığı bu nedenle endüstriyel önem yerine geçmez.

### 4.2 RQ2 — Kod ve design smells

*Duplicated Code/Clones*, *Large Class/God Class*, *Feature Envy* ve *Long Method* sık tartışılan kokulardır. Makale özellikle adlandırma sorununu gösterir: *Blob*, *Large Class* ve *God Class* kimi kaynaklarda eş anlamlı, kimilerinde ayrı kavramlardır; *Copy and Paste Programming* de *Duplicated Code* ile eşleştirilebilir [1, Bölüm 4.2]. Bu durum araçların neyi ölçtüğünü ve sonuçların karşılaştırılabilirliğini etkiler.

RQ2 bölümünde 27 S-kodu listelenirken genel tema dağılımı 25 smell çalışması verir. S29 ve S36 refactoring listesinde de yer aldığından bölüm listesi birbirini dışlayan tema sayımı değildir. Dolayısıyla 25 sayısı RQ2 listesinin uzunluğu değil, Şekil 5'teki ana tema sınıflamasıdır.

### 4.3 RQ3 — Diller ve araçlar

On dokuz ikincil çalışma 162'den fazla smell tespit aracı anar. CCFinder ve PMD bu çalışmaların dokuzunda (%47,36), inCode sekizinde (%42,10), DECOR/DETEX ve inFusion yedisinde (%36,84) geçer. Payda tüm 40 değil, araç bildiren 19 çalışmadır. Refactoring tarafında 13 çalışmada 24 farklı araç anılır; JDeodorant en sık anılandır [1, Bölüm 4.3]. Anılma sıklığı bağımsız doğruluk veya kullanılabilirlik ölçümü değildir.

Platform/dil belirten 35 çalışma Java'yı en çok kullanılan teknoloji olarak sunar; Java'yı C++ (%57,14) ve C# (%42,85) izler [1, Bölüm 4.3.1, Şekil 12]. “Java %57,14 — 35 çalışma” yorumu yanlıştır: 35 Java'yı öne çıkaran çalışma sayısı, %57,14 C++ oranıdır. Az sayıda aracın çoklu dil desteklemesi önemli bir boşluktur.

### 4.4 RQ4 — Araştırma sorularının yapısı

Kırk çalışmada 181 RQ, çalışma başına ortalama 4,5 soru vardır. *Description and Classification* 90 soruyla havuzun %49,72'sini ve 30 çalışmayla çalışmaların %75'ini kapsar. Tablo 10'daki çalışma yüzdeleri örtüşebilir; aynı çalışmanın farklı soruları farklı alt türlere girebilir. Bu nedenle yüzdelerin toplamının %100'ü aşması hata değildir. RQ havuzu sütununun paydası ise 181 tekil sorudur. Yalnız dokuz soru (%4,97) ampirik/kanıta dayalı terimlerle ilişkilendirilmiş, CCI ve Design kategorilerinde soru bulunmamıştır [1, Tablo 10].

### 4.5 RQ5 — Zaman ve yöntem eğilimleri

İlk ikincil çalışma 2004'te yayımlanmış, yayınlar 2013 sonrasında artmıştır. Kırk çalışmanın 26'sı SLR (%65), yedisi sistematik haritalama (%17,5), yedisi survey'dir (%17,5). S16 ayrıca *multivocal* niteliktedir; ayrı bir 41. çalışma değildir. Yayınların %75'i dergi, %25'i konferans makalesidir [1, Bölüm 4.5.1]. İkincil yayın sayısındaki artış, birincil kanıtın kendiliğinden güçlü olduğu anlamına gelmez.

### 4.6 Kalite ve QMOOD

Yazarlar içsel kalite niteliklerini QMOOD üzerinden anlaşılabilirlik, işlevsellik, yeniden kullanılabilirlik ve bakım yapılabilirlik gibi dışsal niteliklerle eşleştirir. Şekil 24'te refactoring'in bu niteliklerle smell'lerden daha fazla ilişki gösterdiği ileri sürülür [1, Bölüm 5.2; 6]. Bu sonuç kontrollü deneyden türetilmiş nedensel etki büyüklüğü değildir. Yazarlar kapsamlı/yeterli kanıt bulunmadığını ve bağlama göre refactoring'in yeni kokular doğurabileceğini de söyler. Bu nedenle “refactoring her koşulda kaliteyi daha çok artırır” genellemesi yapılamaz.

### 4.7 Açık araştırma sorunları

Makalenin Tablo 14'te topladığı 13 açık sorun üç ana eksende okunabilir. I1–I6 *code smell* türlerine odaklanır: ortak adlandırma eksikliği, tespit yaklaşımlarının karşılaştırılması, endüstri algısı, geliştirici katılımı, kalite etkilerinin ölçülmesi ve araçların geliştirilmesi. I7–I11 refactoring tarafında geliştirici bilgisini, kalite etkilerini, araç desteğini, dönüşümlerin uzun dönem izlenmesini ve mimari refactoring ile yerel refactoring arasındaki sınırı ele alır. I12 eğitim, I13 ise güvenilir veri kümeleri ve akademik-endüstriyel çalışmalar arasındaki tutarlılık üzerinden iki alanı birlikte kapsar [1, Tablo 14].

Bu sorunlar arasında nedensel bir sıra da kurulabilir. Ortak terminoloji bulunmadığında veri kümelerinin etiketleri ve araç sonuçları karşılaştırılamaz; karşılaştırılabilir tespit bulunmadığında kokuların kalite üzerindeki etkisi güvenilir biçimde ölçülemez; etki ölçülemediğinde uygun refactoring'in seçimi ve yararının izlenmesi zorlaşır. Dolayısıyla I1 yalnızca sözcük seçimine ilişkin bir sorun değil, I2, I5, I6, I8 ve I9'daki kanıt üretimini etkileyen yöntemsel bir başlangıç noktasıdır.

I13 de sonuçların genellenebilirliği açısından belirleyicidir. Ortak ölçütlere göre doğrulanmış veri kümeleri ve büyük ölçekli endüstriyel örnekler olmadan bir aracın farklı dil, ekip ve proje türlerinde benzer sonuç verip vermediği gösterilemez. Bu nedenle araç sayısındaki artış tek başına alanın olgunlaştığını kanıtlamaz; veri kalitesi, tekrar edilebilirlik ve bağlamsal çeşitlilik birlikte değerlendirilmelidir.

## 5. Nesneye Dayalı Programlama ile İlişkisi

### 5.1 Sorumluluk ve kohezyon

*Long Method* ve *Large Class*, bir metot veya sınıfın gereğinden fazla sorumluluk üstlenebildiğini gösterir. Makalenin Tablo 2'de aktardığı tanımlar, bu iki türü Tek Sorumluluk İlkesiyle açıkça ilişkilendirir [1, Tablo 2]. Bir sınıf farklı değişim nedenlerini aynı yapı içinde topladığında kohezyon düşer ve küçük bir gereksinim değişikliği ilgisiz davranışları da etkileyebilir. *Divergent Change* de aynı sınıfın farklı nedenlerle sürekli değiştirilmesi üzerinden benzer bir sorumluluk dağılması sorununa işaret eder.

*Extract Method*, uzun bir işlemin anlamlı parçalara ayrılmasına; *Extract Class* ise birbiriyle ilişkili alan ve davranışların ayrı bir sınıfta toplanmasına yardımcı olabilir. Bununla birlikte sınıfı bölmek tek başına iyi tasarım üretmez. Yeni sınıflar arasında yoğun veri alışverişi oluşursa kohezyondaki kazanç, artan bağımlılıkla dengelenebilir. Bu nedenle dönüşümün başarısı yalnız sınıf veya metot uzunluğunun azalmasıyla değil, ortaya çıkan sorumluluk sınırlarının kavramsal açıklığıyla değerlendirilmelidir.

### 5.2 Kapsülleme ve bağımlılık

*Feature Envy*, bir metodun kendi sınıfındaki verilerden çok başka bir sınıfın üyeleriyle ilgilenmesi durumudur [1, Tablo 2]. OOP açısından bu belirti, davranışın veriye yakın konumlandırılması ve sınıf sorumluluklarının doğru dağıtılması sorununu gündeme getirir. *Move Method*, davranışı kullandığı verinin sahibi olan sınıfa taşıyarak bu ilişkiyi iyileştirebilir. Ancak metodun birden fazla sınıfın verisine aynı ölçüde ihtiyaç duyması, sorunun yalnızca yanlış konumlandırmadan değil eksik bir alan soyutlamasından kaynaklandığını gösterebilir.

*Message Chains* ve *Inappropriate Intimacy*, sınıflar arasındaki bağımlılığın farklı biçimlerini görünür kılar. Uzun mesaj zincirleri bir nesnenin başka nesnelerin iç yapısını adım adım bilmesini gerektirirken, uygunsuz yakınlık iki sınıfın birbirinin ayrıntılarına aşırı bağımlı olmasına yol açar. Bu yapılar kapsülleme sınırlarını zayıflatabilir ve bir sınıftaki değişikliğin başka sınıflara yayılmasına neden olabilir. *Shotgun Surgery* ise tek bir değişikliğin çok sayıda sınıfa dağılmasıyla bu değişim yayılımının bakım üzerindeki sonucunu gösterir.

### 5.3 Kalıtım ve çok biçimlilik

*Refused Bequest*, bir alt sınıfın üst sınıftan devraldığı veri veya davranışların önemli bölümünü kullanmamasını ifade eder [1, Tablo 2]. Bu durum, kalıtım ilişkisinin gerçek bir “bir türüdür” ilişkisine dayanmadığını veya alt sınıfın yanlış bir hiyerarşide konumlandırıldığını düşündürebilir. *Pull Up Method*, ortak davranışları üst sınıfta birleştirebilir; *Collapse Hierarchy* ise gereksiz ayrımları ortadan kaldırabilir. Ancak bu teknikler yalnız davranışsal uyumluluk ve sınıfların kavramsal rolleri korunuyorsa anlamlıdır.

Yoğun tür denetimine dayanan *Switch Statements* kullanımı da çok biçimliliğin yeterince kullanılmadığı bir tasarıma işaret edebilir. *Replace Conditional with Polymorphism*, türe göre dallanan davranışı alt sınıflara veya ortak bir arayüzü gerçekleştiren nesnelere dağıtabilir. Buna rağmen her koşullu ifade bir design smell değildir. Az sayıda, kararlı ve açık bir koşulu sınıf hiyerarşisine dönüştürmek sistemi gereksiz yere karmaşıklaştırabilir. Refactoring kararı, yalnız kalıbın varlığına değil değişim sıklığına ve davranış çeşitliliğine dayanmalıdır.

### 5.4 Bağlama bağlı refactoring kararı

Makalenin Tablo 8'deki eşleştirmeleri, code smell türleri ile refactoring teknikleri arasında bire bir ilişki olmadığını gösterir. Aynı smell birden fazla dönüşümle ele alınabilir; aynı refactoring farklı smell türlerinde kullanılabilir [1, Tablo 8]. Örneğin her *Large Class* otomatik olarak *Extract Class* gerektirmez. Sınıf büyük olsa da tek ve tutarlı bir sorumluluğu temsil edebilir; tersine, daha küçük bir sınıf birbirinden kopuk sorumluluklar taşıyabilir.

Bu nedenle code smell, kesin hata kararı değil tasarımın yeniden incelenmesini sağlayan bir belirtidir. Refactoring de kendi başına amaç değil, davranışı koruyarak tasarımın anlaşılabilirliğini ve değiştirilebilirliğini geliştirmeye yarayan bir araçtır. OOP ilkeleri bu kararda mekanik eşikler sunmak yerine sorumluluk, kapsülleme, bağımlılık, kalıtım ve çok biçimlilik açısından değerlendirme ölçütleri sağlar. Araç önerisi başlangıç noktası olabilir; nihai karar sistem bağlamını ve kalite ödünleşimlerini bilen geliştirici tarafından verilmelidir.

## 6. Alanın Gelişimi ve Temel Kaynaklar

### 6.1 Davranışı koruyan dönüşümlerin teknik temeli

Alanın teknik başlangıç noktalarından biri Opdyke'ın 1992 tarihli doktora tezidir. Opdyke, nesne yönelimli çerçevelerin yeniden düzenlenmesini programın gözlemlenebilir davranışını koruyan dönüşümler üzerinden ele almış ve bu dönüşümlerin güvenli biçimde uygulanabilmesi için önkoşullar tanımlamıştır [2]. Böylece refactoring, yalnızca kodun daha düzenli görünmesini sağlayan sezgisel bir temizlik işlemi değil, uygulanabilirliği denetlenmesi gereken küçük dönüşümlerin bileşimi olarak kavramsallaştırılmıştır. Tezde ilkel dönüşümlerin daha yüksek düzeyli yeniden yapılandırmaları oluşturacak biçimde birleştirilmesi, sonraki araç desteği çalışmalarına da teknik bir zemin sağlamıştır. Bu yaklaşımın nesneye dayalı programlama açısından önemi, sınıf hiyerarşisi, örnek değişken, metot ve kalıtım ilişkilerindeki değişikliklerin işlevsel davranıştan bağımsız değerlendirilemeyeceğini göstermesidir.

### 6.2 Sorun ve çözüm kataloglarının oluşması

Brown vd.'nin 1998 tarihli *AntiPatterns* kitabı, tekrar eden fakat olumsuz sonuç üreten çözümleri yazılım geliştirme, yazılım mimarisi ve proje yönetimi başlıkları altında kataloglaştırmıştır [3]. Bu kapsam, antipattern kavramının yalnızca kaynak kod düzeyindeki code smell'lerle özdeş olmadığını gösterir. *Blob* ve *Spaghetti Code* gibi örnekler, tasarım kararlarının sorumluluk dağılımı, bağımlılık ve değiştirilebilirlik üzerindeki etkisini görünür kılmıştır. Kitabın tarihsel katkısı, sorunu adlandırmakla kalmayıp bağlamı, ortaya çıkan olumsuz sonuçları ve yeniden yapılandırılmış çözümü birlikte sunmasıdır.

Fowler vd.'nin 1999 tarihli çalışması ise refactoring bilgisini geliştiricinin günlük pratiğine taşıyan ortak bir söz varlığı oluşturmuştur [4]. Refactoring, programın dış davranışını değiştirmeden iç yapısını küçük ve denetlenebilir adımlarla iyileştirme tekniği olarak sunulmuş; code smell'ler bu adımları gerektirebilecek tasarım sorunlarının belirtileri şeklinde ele alınmıştır. Katalog yapısı, bir code smell'i otomatik olarak hata saymak yerine hangi bağlamda hangi dönüşümün düşünülebileceğini tartışmaya açar. Bu nedenle Fowler vd.'nin katkısı yalnızca terim üretmek değil, teşhis ile müdahale arasında tekrarlanabilir bir uygulama dili kurmaktır.

### 6.3 Ölçme ve araştırma alanının sistemleşmesi

Bansiya ve Davis'in 2002 tarihli QMOOD modeli, nesne yönelimli tasarım özellikleri ile yeniden kullanılabilirlik, esneklik, anlaşılabilirlik, işlevsellik, genişletilebilirlik ve etkililik gibi üst düzey kalite nitelikleri arasında nicel ilişkiler kurmuştur [6]. Model, refactoring tarihinin doğrudan bir kataloğu değildir; buna karşılık, yapısal değişikliklerin kalite üzerindeki etkisini ölçme arayışının önemli bir örneğidir. Lacerda vd.'nin refactoring etkilerini QMOOD nitelikleri üzerinden yeniden gruplaması da bu ölçme geleneğine dayanır. Ancak bu yeniden gruplama, farklı bağlamlarda yürütülmüş araştırmaların sonuçlarını ortak başlıklar altında birleştirir; tek başına nedensel etki kanıtı oluşturmaz.

Mens ve Tourwé'nin 2004 tarihli araştırması, refactoring alanındaki çalışmaları desteklenen etkinlikler, kullanılan teknikler, dönüştürülen yazılım artefaktları, araç desteği ve yazılım sürecine etkiler bakımından sistemleştirmiştir [5]. Bu çalışma, alanın tek tek dönüşüm kataloglarından araştırma soruları, biçimsel güvenceler ve araç tasarımı çevresinde örgütlenen bir inceleme alanına geçtiğini gösterir. Lacerda vd. bu yayını kendi tarama tarihlerindeki atıf verilerine göre en çok atıf alan ikincil çalışma olarak raporlamıştır [1]. Bu niteleme kalıcı bir sıralama değil, 2019 sonunda alınmış bibliyometrik bir kesittir.

### 6.4 Ampirik kanıtların çeşitlenmesi

2010'lu yıllardaki çalışmalar, smell ile bakım kalitesi arasındaki ilişkinin bağlama göre değiştiğini ortaya koymuştur. Khomh vd., dört açık kaynak sisteminin 54 sürümünde 13 antipattern'i incelemiş; antipattern içeren sınıfların hemen hemen tüm sürümlerde değişime ve hata düzeltmeye daha yatkın olduğunu, bu farkın yalnızca sınıf büyüklüğüyle açıklanamadığını bildirmiştir [7]. Buna karşılık Sjøberg vd.'nin profesyonel geliştiricilerle yürüttüğü kontrollü çalışmada incelenen 12 code smell'in hiçbiri, dosya büyüklüğü ve değişiklik sayısı denetlendiğinde daha yüksek bakım çabasıyla anlamlı biçimde ilişkilendirilmemiştir [8]. Bu iki sonuç çelişki olarak görünse de aynı bağımlı değişkeni ve aynı araştırma tasarımını kullanmaz: ilki sürüm geçmişindeki değişim ve hata eğilimini, ikincisi belirli bakım görevlerinde harcanan süreyi ölçer.

Al Dallal'ın 2015 tarihli sistematik derlemesi, refactoring fırsatlarını belirleyen 47 birincil çalışmayı incelemiş; *Extract Class* ve *Move Method* işlemlerinin öne çıktığını, değerlendirmelerin çoğunlukla akademik araştırmacılar tarafından açık kaynak ve görece küçük veri kümeleri üzerinde yapıldığını göstermiştir [9]. Sharma ve Spinellis ise 445 birincil çalışmayı sentezleyerek smell tanımlarındaki çeşitliliği, beş temel tespit yaklaşımını ve mevcut araçların yanlış pozitifler ile sınırlı smell kapsamı sorunlarını belirlemiştir [10]. Böylece tarihsel çizgi, 1990'lardaki güvenli dönüşüm ve katalog oluşturma çabasından, 2000'lerde alanın sistemleştirilmesine; oradan da büyük literatür kümelerinde kanıtın kapsamını ve sınırlarını sorgulayan ikincil araştırmalara ilerlemiştir. Lacerda vd.'nin üçüncül incelemesi bu çizginin son halkasında, sonuçları tek bir kesin hükme indirgemek yerine hangi konularda uzlaşma veya belirsizlik bulunduğunu haritalandırmaktadır [1].

## 7. Eleştirel Değerlendirme

### 7.1 Yöntemsel güçlü yönler

Makalenin gücü, parçalı iki alanı aynı kanıt haritasında birleştirmesidir. Sekiz kaynak, açık seçim akışı, kalite değerlendirmesi ve çoğaltma paketi izlenebilirliği artırır. RQ'lar yalnız teknik/araçları değil ikincil araştırmaların soru yapılarını da inceler; bulgular uygulayıcı, araştırmacı ve eğitici açısından tartışılır.

Araştırma sorularının konu, araç, soru yapısı ve yıllık eğilimler biçiminde ayrılması, çalışmanın yalnızca kaynak sayan bir bibliyografik özet olmasını engeller. Tablo 8'de code smell türlerinin tespit yaklaşımları, araçlar ve olası refactoring teknikleriyle birlikte gösterilmesi de parçalı bilgileri aynı bağlamda okumayı kolaylaştırır. Ayrıca yazarların gözlem ile açık sorun arasında ayrım yapması, literatürde sık tekrarlanan iddiaların kesin kanıt olarak sunulması riskini azaltan önemli bir yöntemsel tercihtir.

### 7.2 Üçüncül incelemenin kanıt sınırları

Üçüncül inceleme ise ikincil çalışmaların kapsamı ve raporlama kalitesiyle sınırlıdır. Aynı birincil çalışma birden fazla derlemeye girmiş olabilir; kanıt bağımsızlığı zayıflayabilir. İngilizce, çevrim içi ve altı sayfadan uzun çalışma koşulları yanlılık yaratır. *Card sorting* kategorileri yorumlayıcıdır. Ayrıca dil yüzdeleri ile RQ2'deki örtüşen listeler kolay yanlış okunmaktadır.

Aynı birincil araştırmanın farklı ikincil çalışmalarda tekrar edilmesi, belirli bir bulgunun literatürde olduğundan daha baskın görünmesine yol açabilir. Üçüncül inceleme bu tekrarları ayrı deneysel doğrulamalar gibi değerlendirmemelidir. Benzer şekilde ikincil çalışmalarda deney bağlamı, örneklem büyüklüğü veya ölçüm yöntemi eksik raporlanmışsa bu eksiklik üçüncül senteze de taşınır. Bu nedenle çalışma, doğrudan bir meta-analizden çok araştırma alanının kapsamını ve eğilimlerini gösteren bir kanıt haritası olarak daha güçlüdür.

Arama kapsamının sekiz veri tabanına yayılması kapsayıcılığı güçlendirir; buna karşılık sorguların veri tabanlarına göre uyarlanması sonuç kümelerinin tam olarak eşdeğer olmadığı anlamına gelir. Yazarların bildirdiği ortalama arama doğruluğu %12,63'tür ve veri tabanları arasında belirgin fark vardır [1, Bölüm 3.6]. Snowballing yedi ek çalışma sağlayarak duyarlılığı artırmış olsa da yalnız seçilen çalışmaların kaynakçalarına dayanması, başlangıç kümesinin sınırlarını bütünüyle ortadan kaldırmaz.

### 7.3 Genellenebilirlik

Java'nın araç geliştirme ve deneylerde baskın olması, sonuçların dinamik diller, işlevsel programlama dilleri veya farklı çalışma zamanı özelliklerine sahip platformlara doğrudan aktarılmasını sınırlar. Bir code smell tespit kuralının kullandığı metrik ve eşik değerleri dilin tür sistemi, deyimleri ve proje mimarisiyle değişebilir. Bu nedenle Java üzerinde yüksek başarı gösteren bir yaklaşımın JavaScript, Python veya C++ projelerinde aynı doğrulukla çalışacağı varsayılamaz.

Açık kaynak projeler tekrarlanabilirlik ve veri erişimi açısından değerlidir; ancak kapalı kaynaklı endüstriyel sistemlerin ekip yapısı, süreçleri, yaşları ve değişiklik baskıları farklı olabilir. Küçük akademik veya örnek projelerde ölçülen refactoring etkileri de uzun ömürlü ve çok ekipli sistemlerin bakım maliyetini temsil etmeyebilir. I13'te önerilen güvenilir veri kümeleri bu nedenle yalnız daha fazla proje toplamakla sınırlı kalmamalı; farklı dil, büyüklük, alan ve geliştirme bağlamlarını dengeli biçimde içermelidir.

### 7.4 Kanıt ile yorumun ayrılması

QMOOD sentezi ortak görünüm sağlasa da etki büyüklüklerini, çalışma kalitesini ve bağlamsal değişkenleri nicel meta-analizde birleştirmez. “Refactoring kaliteyi smell'lerden daha fazla etkiler” yazarların sentez sonucudur; her projede net olumlu sonuç kanıtı değildir.

Benzer biçimde bir aracın çok sayıda ikincil çalışmada anılması, o aracın daha doğru, güncel veya kullanışlı olduğunu göstermez. Literatürde 162'den fazla tespit aracının bulunması da sonuçların birbiriyle tutarlı olduğu anlamına gelmez. Code smell tespit edilmesi kesin bir yazılım hatasının varlığını kanıtlamadığı gibi, önerilen refactoring'in uygulanması da bütün kalite niteliklerini aynı anda iyileştirmeyebilir. Bu ayrımlar, frekans bulgularıyla etkinlik bulgularının ve ilişkiyle nedenselliğin karıştırılmaması açısından önemlidir.

Tablo 14'te I1–I6 smell, I7–I11 refactoring, I12–I13 iki alanla ilgilidir. I1 (adlandırma), I5/I8 (kalite), I9 (araç), I13 (veri kümeleri ve akademi-endüstri tutarlılığı) eleştirel tartışma için güçlüdür. Bu kısa gözlemlerden türetilen ayrıntılı çözümler doğrudan makale ifadesi sayılmamalıdır; örneğin Feature Envy ile kapsülleme arasındaki ilişki makul bir OOP yorumudur, fakat Tablo 14'ün doğrudan bulgusu değildir.

Sonuç olarak makalenin en güçlü yönü geniş ve izlenebilir bir araştırma haritası sunmasıdır. En önemli sınırlılığı ise farklı yöntem, örneklem ve kalite ölçütlerine dayanan ikincil çalışmaları ortak bir anlatı içinde birleştirmesidir. Bulgular bu nedenle kesin neden-sonuç hükümleri olarak değil, alandaki eğilimleri, uzlaşıları ve doğrulanmayı bekleyen araştırma sorunlarını gösteren bir sentez olarak okunmalıdır.

## 8. Geliştirme ve Gelecek Çalışma Önerileri

Ortak adlandırma ve tanım sözlüğü, aynı olgunun farklı etiketlenmesini azaltmalı; veri kümeleri uzmanlarca doğrulanmış örnekler içermelidir. Smell tespiti, refactoring önerisi, davranış koruma denetimi ve uzun dönem kalite izlemesi aynı araç zincirinde ilişkilendirilebilir. Otomasyon geliştirici kararını kaldırmak yerine gerekçe, güven düzeyi ve kalite ödünleşimlerini görünür kılmalıdır.

Java ve açık kaynak ağırlığının ötesine geçen, çok dilli ve endüstriyel bağlamlı çalışmalar gereklidir. Bunlar yalnız önce/sonra metrik farkını değil hata eğilimi, değişiklik maliyeti, anlaşılabilirlik, geliştirici zamanı ve uzun dönem etkileri izlemelidir. Eğitimde gerçekçi kod tabanlarında smell tanıma, test destekli refactoring ve kod incelemesi birleştirilebilir; fakat belirli öğretim yönteminin üstünlüğü ayrıca sınanmalıdır.

## 9. Genel Sonuç

Lacerda vd., *code smells* ile refactoring'i yazılım kalitesi çevresinde birleştiren kapsamlı bir üçüncül inceleme sunar. Kalıcı katkısı, neyin bilindiği ile neyin güvenilir biçimde bilinmediğini ayırmasıdır. Smell adlandırması tutarsız, araç desteği parçalı, kalite kanıtları heterojen ve akademi-endüstri bağı sınırlıdır. Çalışma aynı zamanda sınıf sorumluluğu, kohezyon, bağımlılık, kalıtım ve çok biçimlilik kavramlarını bakım problemiyle ilişkilendiren güçlü bir OOP çerçevesidir.

Bu raporda RQ2 çalışma sayısı, dil yüzdeleri, Tablo 10 ve QMOOD yorumu özgün metin üzerinden sınırlandırılmıştır. Refactoring, kokunun varlığına verilen otomatik ve her zaman yararlı tepki değil; bağlam, davranış koruma ve kalite ödünleşimleriyle değerlendirilmesi gereken tasarım kararıdır.

## Kaynakça

[1] Lacerda, G., Petrillo, F., Pimenta, M., & Guéhéneuc, Y.-G. (2020). Code smells and refactoring: A tertiary systematic review of challenges and observations. *Journal of Systems and Software, 167*, 110610. https://doi.org/10.1016/j.jss.2020.110610

[2] Opdyke, W. F. (1992). *Refactoring object-oriented frameworks* (Doctoral dissertation). University of Illinois at Urbana-Champaign.

[3] Brown, W. H., Malveau, R. C., McCormick, H. W., & Mowbray, T. J. (1998). *AntiPatterns: Refactoring software, architectures, and projects in crisis*. John Wiley & Sons.

[4] Fowler, M., Beck, K., Brant, J., Opdyke, W., & Roberts, D. (1999). *Refactoring: Improving the design of existing code*. Addison-Wesley.

[5] Mens, T., & Tourwé, T. (2004). A survey of software refactoring. *IEEE Transactions on Software Engineering, 30*(2), 126–139. https://doi.org/10.1109/TSE.2004.1265817

[6] Bansiya, J., & Davis, C. G. (2002). A hierarchical model for object-oriented design quality assessment. *IEEE Transactions on Software Engineering, 28*(1), 4–17. https://doi.org/10.1109/32.979986

[7] Khomh, F., Di Penta, M., Guéhéneuc, Y.-G., & Antoniol, G. (2012). An exploratory study of the impact of antipatterns on class change- and fault-proneness. *Empirical Software Engineering, 17*, 243–275. https://doi.org/10.1007/s10664-011-9171-y

[8] Sjøberg, D. I. K., Yamashita, A., Anda, B. C. D., Mockus, A., & Dybå, T. (2013). Quantifying the effect of code smells on maintenance effort. *IEEE Transactions on Software Engineering, 39*(8), 1144–1156. https://doi.org/10.1109/TSE.2012.89

[9] Al Dallal, J. (2015). Identifying refactoring opportunities in object-oriented code: A systematic literature review. *Information and Software Technology, 58*, 231–249. https://doi.org/10.1016/j.infsof.2014.08.002

[10] Sharma, T., & Spinellis, D. (2018). A survey on software smells. *Journal of Systems and Software, 138*, 158–173. https://doi.org/10.1016/j.jss.2017.12.034
