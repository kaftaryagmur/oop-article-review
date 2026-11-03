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

*Long Method* ve *Large Class* tek sorumluluğun aşınmasına, *Divergent Change* düşük kohezyona, *Feature Envy* davranışın yanlış sınıfta konumlanmasına işaret eder. *Message Chains* ve *Inappropriate Intimacy* yüksek bağımlılığı görünür kılar. Bunlar makaledeki tanımlardan hareketle yapılan OOP yorumlarıdır; her koku otomatik olarak hata değildir [1, Tablo 2].

*Extract Class* sorumlulukları ayırabilir, *Move Method* davranışı uygun nesneye taşıyabilir, *Replace Conditional with Polymorphism* tür denetimli koşulları çok biçimlilikle değiştirebilir. Ancak koku ile tek bir zorunlu çözüm arasında bire bir eşleme yoktur. Aynı koku farklı dönüşümler gerektirebilir; aynı refactoring farklı kokulara uygulanabilir [1, Tablo 8]. İyi tasarım, aracın önerisini mekanik uygulamak yerine davranış koruma ve kalite ödünleşimlerini değerlendirmeyi gerektirir.

## 6. Alanın Gelişimi ve Temel Kaynaklar

Alanın teknik temeli Opdyke'ın 1992 tarihli doktora tezine uzanır; tez davranışı koruyan nesne yönelimli dönüşümleri ve önkoşulları ayrıntılandırmıştır [2]. Brown vd.'nin 1998 tarihli *AntiPatterns* kitabı tekrar eden kötü çözümleri kataloglaştırmış; *Blob* ve *Spaghetti Code* gibi sorunları görünür kılmıştır [3]. Fowler vd.'nin 1999 kitabı smell ve refactoring kataloglarını günlük geliştirici pratiğine taşıyarak ortak söz varlığını biçimlendirmiştir [4].

Mens ve Tourwé'nin 2004 araştırması, alanı tanım, süreç, araç ve araştırma sorunları bakımından özetleyen erken ve etkili bir derlemedir [5]. Lacerda vd. tarafından en çok atıf alan ikincil çalışma olarak raporlanır; ancak atıf sayısı 2019 sonundaki sorguya bağlıdır. Bansiya ve Davis'in QMOOD modeli de nesne yönelimli tasarım özellikleriyle üst düzey kalite nitelikleri arasında ilişki kurarak kalite sentezine dayanak sağlar [6]. Tarihsel çizgi böylece dönüşüm kuramından pratik kataloglara, ardından ikincil ve üçüncül kanıt sentezine uzanır.

## 7. Eleştirel Değerlendirme

Makalenin gücü, parçalı iki alanı aynı kanıt haritasında birleştirmesidir. Sekiz kaynak, açık seçim akışı, kalite değerlendirmesi ve çoğaltma paketi izlenebilirliği artırır. RQ'lar yalnız teknik/araçları değil ikincil araştırmaların soru yapılarını da inceler; bulgular uygulayıcı, araştırmacı ve eğitici açısından tartışılır.

Üçüncül inceleme ise ikincil çalışmaların kapsamı ve raporlama kalitesiyle sınırlıdır. Aynı birincil çalışma birden fazla derlemeye girmiş olabilir; kanıt bağımsızlığı zayıflayabilir. İngilizce, çevrim içi ve altı sayfadan uzun çalışma koşulları yanlılık yaratır. *Card sorting* kategorileri yorumlayıcıdır. Ayrıca dil yüzdeleri ile RQ2'deki örtüşen listeler kolay yanlış okunmaktadır.

Arama kapsamının sekiz veri tabanına yayılması kapsayıcılığı güçlendirir; buna karşılık sorguların veri tabanlarına göre uyarlanması sonuç kümelerinin tam olarak eşdeğer olmadığı anlamına gelir. Yazarların bildirdiği ortalama arama doğruluğu %12,63'tür ve veri tabanları arasında belirgin fark vardır [1, Bölüm 3.6]. Snowballing yedi ek çalışma sağlayarak duyarlılığı artırmış olsa da yalnız seçilen çalışmaların kaynakçalarına dayanması, başlangıç kümesinin sınırlarını bütünüyle ortadan kaldırmaz.

QMOOD sentezi ortak görünüm sağlasa da etki büyüklüklerini, çalışma kalitesini ve bağlamsal değişkenleri nicel meta-analizde birleştirmez. “Refactoring kaliteyi smell'lerden daha fazla etkiler” yazarların sentez sonucudur; her projede net olumlu sonuç kanıtı değildir.

Tablo 14'te I1–I6 smell, I7–I11 refactoring, I12–I13 iki alanla ilgilidir. I1 (adlandırma), I5/I8 (kalite), I9 (araç), I13 (veri kümeleri ve akademi-endüstri tutarlılığı) eleştirel tartışma için güçlüdür. Bu kısa gözlemlerden türetilen ayrıntılı çözümler doğrudan makale ifadesi sayılmamalıdır; örneğin Feature Envy ile kapsülleme arasındaki ilişki makul bir OOP yorumudur, fakat Tablo 14'ün doğrudan bulgusu değildir.

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
