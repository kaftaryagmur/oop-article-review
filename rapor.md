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

Sekiz kaynaktaki 467 kaydın 59'u ilk elemeyi geçmiştir (%12,63). Bu oran ilk elemenin verimini gösterir. *Snowballing* yoluyla eklenen yedi çalışma, kaynakça taramasının sorguyla bulunan kümeyi tamamladığını gösterir [1, Bölüm 3.6; 11].

## 4. Bulgular ve Sonuçlar

### 4.1 RQ1 — Refactoring

Refactoring temasındaki 13 çalışma teknikler, fırsat belirleme, kalite etkisi, evrim ve teknik borç gibi başlıklara dağılır. *Extract Method* ve *Extract Class* gibi çıkarma teknikleri sık incelenir. İncelenen ikincil çalışmaların kapsadığı teknik sayısı 72 tekniğin yalnızca 20–27'si arasında kalır. Üstelik smell ile refactoring arasında bire bir eşleme yoktur: aynı smell için birden fazla dönüşüm birleştirilebilir, aynı dönüşüm farklı smell'lere uygulanabilir ve bağlamdan kopuk bir işlem kaliteyi düşürebilir [1, Bölüm 4.1]. Bu nedenle refactoring fırsatının bulunması, uygun dönüşümün seçildiği veya yararlı sonuç vereceği anlamına gelmez.

Akademide en çok incelenen tekniklerle geliştiricilerin pratikte en sık kullandıkları da aynı değildir. Yeniden adlandırma gibi basit işlemler pratikte yaygın olduğu hâlde fırsat belirleme çalışmalarında aynı ilgiyi görmez. Atıf sıklığı bu nedenle endüstriyel önem yerine geçmez; makalenin RQ1 sonucu, araç otomasyonunun davranışı koruma, dönüşümü uygulama ve artefakt tutarlılığını sürdürme görevlerinde hâlâ sınırlı olduğunu da gösterir [1, Bölüm 4.1.2].

### 4.2 RQ2 — Code smells ve design smells

*Duplicated Code/Clones*, *Large Class/God Class*, *Feature Envy* ve *Long Method* sık tartışılan code smell örnekleridir. Makale özellikle adlandırma sorununu gösterir: *Blob*, *Large Class* ve *God Class* kimi kaynaklarda eş anlamlı, kimilerinde ayrı kavramlardır; *Copy and Paste Programming* de *Duplicated Code* ile eşleştirilebilir [1, Bölüm 4.2]. Bu durum araçların neyi ölçtüğünü ve sonuçların karşılaştırılabilirliğini etkiler.

RQ2'nin girişinde 27 S-kodu listelenirken genel tema dağılımı 25 smell çalışması verir; code smell alt bölümünde ise 28 çalışmanın code smell'lerden söz ettiği belirtilir. Bu sayılar aynı sınıflandırma düzeyine ait değildir. S29 ve S36 refactoring listesinde de yer alır; code smell alt bölümündeki liste ise ana teması başka olan fakat code smell'e değinen çalışmaları da içerir. Dolayısıyla 25, 27 ve 28 sayıları birbiriyle değiştirilemez: ilki Şekil 5'teki ana tema, ikincisi RQ2 kapsam listesi, üçüncüsü code smell anan çalışmaların listesidir [1, Bölüm 3.6; Bölüm 4.2].

Tespit yaklaşımlarında metrik ve kural tabanlı yöntemler öne çıkar; ancak eşik değerlerinde uzlaşma bulunmaması aynı smell için farklı sonuçlar üretebilir. Makalenin burada yaptığı ayrım önemlidir: smell bir kalite sorununun belirtisidir, tek başına kesin hata kararı değildir. RQ2'nin güçlü sonucu belirli bir tespit yönteminin üstünlüğü değil, adlandırma, eşik ve bağlam sorunları nedeniyle yaklaşımların karşılaştırılabilirliğinin zayıf olmasıdır.

### 4.3 RQ3 — Diller ve araçlar

Yazarlar sonuç bölümünde 162 farklı tespit aracı, Bölüm 4.3.3'te ise 24 farklı refactoring aracı bildirir [1].

Araç bildiren 19 ikincil çalışmanın dokuzunda CCFinder ve PMD, sekizinde inCode ve DECOR/DETEX, yedisinde inFusion geçer. DECOR/DETEX için Bölüm 4.3.2 yedi kod sıralar. Şekil 13 ve ek veri sekiz çalışmayı doğrular (8/19, yaklaşık %42,1). Refactoring araçları için JDeodorant 13 veri kaydının 10'unda geçer (yaklaşık %76,9). Makalede verilen %71,42 bu paydayla uyuşmaz. Bu sıklıklar araçların araştırmalarda ne kadar yer bulduğunu gösterir [1, Bölüm 4.3; 11].

Platform veya dil bildiren 35 çalışmanın tamamı Java'yı anar. C++ 20 (%57,14), C# 15 (%42,85) çalışmada geçer. Bölüm 4.3.2, iki ikincil çalışmaya dayanarak araçların ortalama üç ila dört smell türünü kapsadığını bildirir. Bu ortalamanın hangi araç kümesi ve hesaplama yöntemiyle elde edildiği açıklanmadığından 162 araca genellenebilirliği belirsizdir [1, Bölüm 4.3; 11].

### 4.4 RQ4 — Araştırma sorularının yapısı

Kırk çalışmada 181 RQ, çalışma başına ortalama 4,5 soru vardır. *Description and Classification* 90 soruyla havuzun %49,72'sini ve 30 çalışmayla çalışmaların %75'ini kapsar. Keşifsel ve temel sıklık soruları birlikte 152 RQ'ya (%83,97) ulaşırken, ilişki ve nedensellik soruları azınlıkta kalır. Yalnız dokuz soru (%4,97) ampirik/kanıta dayalı terimlerle ilişkilendirilmiş, *Causality-Comparative Interaction* ve *Design* kategorilerinde soru bulunmamıştır [1, Bölüm 4.4.1; Tablo 10]. Bu dağılım, literatürün ağırlıkla “ne var ve nasıl sınıflandırılır?” sorularını yanıtladığını; koşula bağlı nedensellik ve etkili çözüm tasarımı konusunda daha sınırlı olduğunu gösterir.

Tablo 10'un çalışma sütununda payda 40'tır ve kategoriler örtüşebilir. Soru sütunundaki satırlar ise 185'e ulaşırken toplam 181 olarak bildirilmiştir. Ek veri 181 soruyu doğrular ve *Causality* kategorisinde tabloda verilen 14 yerine 10 soru gösterir (%5,52). Makaledeki 9/181 oranı soru metinlerinde aranan sözcüklerin eşleşme sıklığını verir [1, Bölüm 4.4.1; 11].

Mens ve Tourwé (S10), Google Scholar verilerinde hem toplam atıfta hem yıllık atıfta ilk sıradadır. S10, S20 ve S26 her iki ilk beş listesinde de yer alır. Bu sıralamalar makalede kullanılan bibliyometrik kesite aittir [1, Bölüm 4.4.2, Tablo 12–13].

### 4.5 RQ5 — Zaman ve yöntem eğilimleri

İlk ikincil çalışma 2004'te yayımlanmış, yayınlar 2013 sonrasında artmıştır. Kırk çalışmanın 26'sı SLR (%65), yedisi sistematik haritalama (%17,5), yedisi survey'dir (%17,5). S16 ayrıca *multivocal* niteliktedir; ayrı bir 41. çalışma değildir. Yayınların %75'i dergi, %25'i konferans makalesidir ve çalışmaların %80'den fazlası dört üzerinden üç ile dört arasında kalite puanı almıştır [1, Bölüm 4.5.1–4.5.3]. Puan, dört DARE sorusuna dayalı raporlama kalitesini gösterir; birincil bulguların doğruluğunu doğrudan kanıtlamaz.

Ek veride açık kaynak (FLOSS) 25, endüstriyel 15 ve örnek proje 4 kez işaretlenmiştir. Bir derleme birden fazla tür bildirebildiği için %57, 44 kategori kaydının 25'ine karşılık gelir. Şekil 20 için ise yazarlar, birincil çalışma sayısını belirtmeyen bazı derlemelerde kaynakça uzunluğunu vekil ölçüt olarak kullanır. Yıllık karşılaştırma bu nedenle farklı ölçüm türlerini bir araya getirir. Bildirilen 4.573, derlemelerin kaynakça kayıtları toplamıdır [1, Bölüm 4.5.2–4.5.3; 11].

### 4.6 Kalite ve QMOOD

Yazarlar Şekil 24'te QMOOD'dan yararlanarak içsel metrikleri daha üst düzey kalite nitelikleriyle eşleştirir. Aynı metrik birden çok niteliğe bağlanabilir. Bölüm 5.2 kalite etkisine odaklanan yedi smell derlemesi ile bir refactoring derlemesi belirlediğinden iki tarafın kanıt kapsamı da farklıdır. Bu eşleme ilişkilerin kapsamını görselleştirir. Karşılaştırmalı etki büyüklüğü için ortak ölçüm, etki yönü ve karşılaştırılabilir örneklemler gerekir. Yazarlar ayrıca inceledikleri smell örneklerine yönelik 14 refactoring seçeneği için kendi sentezlerinde kalite etkisine ilişkin bağlantılı çalışma bulamadıklarını bildirir [1, Bölüm 5.2, Şekil 23–24; 6].

### 4.7 Açık araştırma sorunları

Makalenin Tablo 14'te topladığı 13 açık sorun üç ana eksende okunabilir. I1–I6 *code smell* türlerine odaklanır. I1 ortak adlandırma sorununu, I2 tespit yaklaşımlarının etkinliğini, I3 uygulayıcıların smell algısını ve I4 geliştiricilerin tespit sürecine katılımını ele alır. I5 smell ile kalite nitelikleri arasında açık bağ kurulamamasına, I6 ise ölçeklenebilirlik, önceliklendirme, görselleştirme, çoklu smell ve dil desteği ile doğruluk sorunları taşıyan araçlara yönelir [1, Bölüm 7; Tablo 14].

I7–I11 refactoring alanındadır. I7 geliştiricinin bilgisini ve karar modelini; I8 az incelenmiş veya pratikte sık kullanılan dönüşümlerin kalite etkisini; I9 araçların geliştirilmesini; I10 dönüşümlerin yazılım evrimi boyunca izlenmesini; I11 ise metot, sınıf, paket ve mimari düzeyler arasındaki sınırı inceler. I12 sınıf ortamında etkili öğretim ve araçları, I13 güvenilir veri kümelerini, büyük ölçekli akademik ve endüstriyel projeleri ve iki bağlam arasındaki veri tutarsızlıklarını kapsar. I12 ve I13 her iki konuya ortak sınıflandırılmıştır [1, Tablo 14].

Bu sorunlar arasında nedensel bir sıra da kurulabilir. Ortak terminoloji bulunmadığında veri kümelerinin etiketleri ve araç sonuçları karşılaştırılamaz; karşılaştırılabilir tespit bulunmadığında smell'lerin kalite üzerindeki etkisi güvenilir biçimde ölçülemez; etki ölçülemediğinde uygun refactoring'in seçimi ve yararının izlenmesi zorlaşır. Dolayısıyla I1 yalnızca sözcük seçimine ilişkin bir sorun değil, I2, I5, I6, I8 ve I9'daki kanıt üretimini etkileyen yöntemsel bir başlangıç noktasıdır. Bu nedensel bağ, Tablo 14'te hazır bir sonuç olarak verilmez; tablodaki sorunlardan bu raporda türetilen eleştirel yorumdur.

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

Mens ve Tourwé'nin 2004 tarihli araştırması, refactoring alanındaki çalışmaları desteklenen etkinlikler, kullanılan teknikler, dönüştürülen yazılım artefaktları, araç desteği ve yazılım sürecine etkiler bakımından sistemleştirmiştir [5]. Bu çalışma, alanın tek tek dönüşüm kataloglarından araştırma soruları, biçimsel güvenceler ve araç tasarımı çevresinde örgütlenen bir inceleme alanına geçtiğini gösterir.

### 6.4 Ampirik kanıtların çeşitlenmesi

Khomh vd., dört açık kaynak sisteminin 54 sürümünde 13 antipattern'i incelemiştir. Sürüm geçmişine dayalı bu gözlemsel çalışmanın inceleme birimi sınıftır. Yazarlar, antipattern içeren sınıfların bir değişiklikte ya da hata düzeltmesinde yer alma olasılığının daha yüksek olduğunu ve sınıf büyüklüğünün bu ilişkiyi tek başına açıklamadığını bildirmiştir. Eclipse için kullanılan kayıtlar daha geniş kapsamlı sorun düzeltmelerini içerir [7, Bölüm 7].

Sjøberg vd. ise altı profesyonel geliştiricinin işlevsel olarak eşdeğer dört Java sisteminde yürüttüğü bakım görevlerini incelemiştir. Ölçüm, değiştirilen 298 Java dosyasında geliştiricilerin harcadığı süredir. Dosya büyüklüğü ve değişiklik sayısı hesaba katıldığında, incelenen 12 code smell türünden hiçbiri daha yüksek süreyle istatistiksel olarak anlamlı ilişki göstermemiştir. *Refused Bequest* için daha düşük süreyle bir ilişki raporlanmıştır [8, Bölüm 3–4].

Bu iki bulgu farklı bakım sorularını yanıtlar. Sürüm geçmişi bir sınıfa ne sıklıkla müdahale edildiğini, görev çalışması ise belirli bir müdahalenin geliştiriciye ne kadar zaman aldığını açıklar. Anlamlı bir süre artışının saptanmaması, olası etkinin büyüklüğünü bu örneklem dışında belirlemek için yetersizdir. Her iki çalışma da bir refactoring müdahalesinin bakım çabasını ne ölçüde değiştirdiği sorusunu açık bırakır [7; 8].

Al Dallal'ın 2015 tarihli sistematik derlemesi, refactoring fırsatlarını belirleyen 47 birincil çalışmayı incelemiş; *Extract Class* ve *Move Method* işlemlerinin öne çıktığını, değerlendirmelerin çoğunlukla akademik araştırmacılar tarafından açık kaynak ve görece küçük veri kümeleri üzerinde yapıldığını göstermiştir [9]. Sharma ve Spinellis ise 445 birincil çalışmayı sentezleyerek smell tanımlarındaki çeşitliliği, beş temel tespit yaklaşımını ve mevcut araçların yanlış pozitifler ile sınırlı smell kapsamı sorunlarını belirlemiştir [10]. Böylece tarihsel çizgi, 1990'lardaki güvenli dönüşüm ve katalog oluşturma çabasından, 2000'lerde alanın sistemleştirilmesine; oradan da büyük literatür kümelerinde kanıtın kapsamını ve sınırlarını sorgulayan ikincil araştırmalara ilerlemiştir. Lacerda vd.'nin üçüncül incelemesi bu çizginin son halkasında, sonuçları tek bir kesin hükme indirgemek yerine hangi konularda uzlaşma veya belirsizlik bulunduğunu haritalandırmaktadır [1].

## 7. Eleştirel Değerlendirme

### 7.1 Yöntemsel güçlü yönler

Makalenin başlıca katkısı, code smell tespitiyle refactoring araştırmalarını ortak bir çerçevede incelemesidir. Tablo 8, bir tasarım belirtisinden yola çıkarak literatürde hangi tespit yöntemlerinin ve hangi dönüşüm seçeneklerinin tartışıldığını izlemeye olanak verir. Açık seçim akışı ve ek veri paketi, bu eşleştirmelerin dayandığı derlemeleri kontrol etmeyi kolaylaştırır [1, Bölüm 3 ve Tablo 8; 11].

### 7.2 Üçüncül incelemenin kanıt sınırları

Üçüncül incelemenin yorum gücü, dayandığı derlemelerin raporlama kalitesi ve kapsamıyla sınırlıdır. Birincil çalışmaların derlemeler arasındaki örtüşmesi ölçülmeden, bir bulgunun farklı derlemelerde yer alması kaç bağımsız araştırmanın onu desteklediğini göstermez. Deney bağlamı, örneklem veya ölçüm ayrıntıları derlemelerde eksikse bu belirsizlik üçüncül senteze de taşınır.

Arama kapsamı veri tabanına göre değişir. Örneğin ScienceDirect araması iki dergiyle sınırlıdır [1, Tablo 5]. Bölüm 3 ve 8, bağımsız tarama ve kodlamanın nasıl yürütüldüğünü ve değerlendiriciler arasındaki uyuşmazlıkların nasıl giderildiğini açıkça belirtmez. Bu ayrıntılar, özellikle konu sınıflandırmalarının yeniden üretilebilirliğini değerlendirmeyi güçleştirir.

### 7.3 Genellenebilirlik

Java'nın araç geliştirme ve deneylerde baskın olması, sonuçların dinamik diller, işlevsel programlama dilleri veya farklı çalışma zamanı özelliklerine sahip platformlara doğrudan aktarılmasını sınırlar. Bir code smell tespit kuralının kullandığı metrik ve eşik değerleri dilin tür sistemi, deyimleri ve proje mimarisiyle değişebilir. Bu nedenle Java üzerinde yüksek başarı gösteren bir yaklaşımın JavaScript, Python veya C++ projelerinde aynı doğrulukla çalışacağı varsayılamaz.

Açık kaynak projeler tekrarlanabilirlik ve veri erişimi açısından değerlidir; ancak kapalı kaynaklı endüstriyel sistemlerin ekip yapısı, süreçleri, yaşları ve değişiklik baskıları farklı olabilir. Küçük akademik veya örnek projelerde ölçülen refactoring etkileri de uzun ömürlü ve çok ekipli sistemlerin bakım maliyetini temsil etmeyebilir. I13'te önerilen güvenilir veri kümeleri bu nedenle yalnız daha fazla proje toplamakla sınırlı kalmamalı; farklı dil, büyüklük, alan ve geliştirme bağlamlarını dengeli biçimde içermelidir.

### 7.4 Kanıt ile yorumun ayrılması

QMOOD eşleştirmesi hangi kalite niteliklerinin hangi dönüşümlerle ilişkilendirildiğini gösterir. Belirli bir *Extract Class* müdahalesinin bakım maliyetini değiştirip değiştirmediğini değerlendirmek için ise ölçülen çıktının tanımlanması gerekir. §6.4'teki iki araştırma bu ayrımı somutlaştırır. Bir sınıfın daha sık değişmesi ile belirli bir bakım görevinin daha uzun sürmesi farklı sonuçlardır. Birindeki ilişkiyi diğerine taşımak için iki çıktıyı da gözleyen bir çalışma gerekir [1, Bölüm 5.2; 7; 8].

Bu sınır, Tablo 14'teki I5 ve I8'in birlikte okunmasıyla belirginleşir. Önce bir code smell'in hangi kalite sorunuyla hangi bağlamda ilişkili olduğu incelenir. Ardından seçilen dönüşümün aynı sonuç üzerindeki etkisi uygun bir karşılaştırmayla sınanır. §8'deki araştırma önerisi bu ikinci soruyu bakım süresi üzerinden somutlaştırır.

## 8. Geliştirme ve Gelecek Çalışma Önerileri

Ortak adlandırma ve tanım sözlüğü, aynı olgunun farklı etiketlenmesini azaltmalı; veri kümeleri uzmanlarca doğrulanmış örnekler içermelidir. Smell tespiti, refactoring önerisi, davranış koruma denetimi ve uzun dönem kalite izlemesi aynı araç zincirinde ilişkilendirilebilir. Otomasyon geliştirici kararını kaldırmak yerine gerekçe, güven düzeyi ve kalite ödünleşimlerini görünür kılmalıdır.

Java ve açık kaynak ağırlığının ötesine geçen, çok dilli ve endüstriyel bağlamlı çalışmalar gereklidir. Bunlar yalnız önce/sonra metrik farkını değil hata eğilimi, değişiklik maliyeti, anlaşılabilirlik, geliştirici zamanı ve uzun dönem etkileri izlemelidir. Eğitimde gerçekçi kod tabanlarında smell tanıma, test destekli refactoring ve kod incelemesi birleştirilebilir; fakat belirli öğretim yönteminin üstünlüğü ayrıca sınanmalıdır.

Bu ölçüm farkından hareketle *Large Class* için *Extract Class* uygulamasının sonraki bakım görevlerini kısaltıp kısaltmadığı sınanabilir. Aynı kod tabanının iki eşdeğer kopyası kullanılabilir ve dönüşüm bir kopyaya uygulanabilir. Geliştiriciler iki koşula dengeli dağıtılarak aynı gereksinim ve kabul ölçütleriyle çalışır. Ana sonuç, görevi doğru tamamlamak için harcanan süredir. Dönüşüm maliyeti ayrıca kaydedilir. Kohezyon ve sınıflar arası bağımlılık, olası tasarım ödünleşimlerini incelemek için ayrı ölçülür.

Dönüşüm öncesinde ve sonrasında aynı regresyon testleri çalıştırılarak testlerin kapsadığı davranışlar denetlenir. Birkaç benzer görevle tekrarlanan karşılaştırma, sonucun tek göreve özgü olup olmadığını değerlendirmeye yardımcı olur. Sürüm geçmişindeki değişim veya hata düzeltme sıklığı ise daha uzun süreli bir izleme çalışmasının ayrı çıktısı olarak ele alınabilir.

## 9. Genel Sonuç

Lacerda vd.'nin üçüncül incelemesi, code smell adlandırmasının, tespit yöntemlerinin ve refactoring seçeneklerinin literatürde nasıl ele alındığını ortaya koyar. İncelemenin OOP açısından değeri, bir tasarım belirtisini sınıf sorumluluğu, kohezyon ve bağımlılık üzerinden tartışmaya açmasıdır. Kalite sentezinin kapsamı, hangi dönüşümün belirli bir bakım görevinde ne ölçüde yarar sağlayacağını belirlemek için sınırlıdır [1, Tablo 8 ve Bölüm 5.2].

Bu raporun uygulamaya dönük değerlendirmesine göre refactoring kararı, çözülmek istenen tasarım sorunu ve iyileştirilmesi beklenen bakım çıktısıyla birlikte tanımlanmalıdır. Örneğin *Extract Class* sonrasında sorumluluk dağılımındaki değişim tasarım metrikleriyle, davranışın korunması regresyon testleriyle, bakım kazancı ise görev süresi ve dönüşüm maliyetiyle ayrı ayrı değerlendirilebilir.

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

[11] Lacerda, G., Petrillo, F., Pimenta, M., & Guéhéneuc, Y.-G. (2020). *Online repository for tertiary systematic review about code smells and refactoring* (Sürüm 2) [Veri seti]. Mendeley Data. https://doi.org/10.17632/72fvy4r3gj.2
