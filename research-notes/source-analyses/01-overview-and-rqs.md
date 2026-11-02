Lacerda ve arkadaşlarının (2020) **"Code smells and refactoring: A tertiary systematic review of challenges and observations"** başlıklı makalesinin akademik bir makale inceleme raporuna hazırlık amacıyla yapılan detaylı analizi ve yapılandırılmış araştırma notları aşağıda sunulmuştur.

Makaleden doğrudan elde edilen veriler ile yöntemsel/analitik çıkarımlar her başlık altında net biçimde birbirinden ayrılmış ve kaynak pasajlara dayanan iddialar numaralandırılmış atıflarla `[i]` desteklenmiştir.

---

### 1\. Çalışmanın Ele Aldığı Temel Problem Nedir?

* **Doğrudan Makaleden Elde Edilen Bilgi:**
  * **Yazılım Bakım Maliyetleri ve Kod Karmaşıklığı:** Yazılım bakımı, bir yazılım sisteminin toplam maliyetinin %50 ile %80'ini oluşturmaktadır[1]. Yetersiz ve eksik dokümantasyon nedeniyle karmaşık kaynak kodları, sistem hakkındaki tek güvenilir bilgi kaynağı haline gelmektedir[1][2].
  * **Kod Kokularının (Code Smells) Oluşumu ve Olumsuz Etkileri:** Geliştiriciler yeni gereksinimleri karşılamak amacıyla sistemde değişiklik ve iyileştirmeler yaparken koda "code smell" (kod kokusu) dahil ederler[3]. Kod kokuları yazılımın kodlama tasarım ilkelerini ihlal eder (violations of coding design principles), teknik borcu (technical debt) artırır, bakımı ve evrimi olumsuz etkiler, kodun anlaşılabilirliğini düşürür ve yazılım hatalarına (flaws/bugs) zemin hazırlar[3].
  * **Yeniden Yapılandırma (Refactoring) Sürecindeki Sorular:** Yeniden yapılandırma kod kokularını gidermenin temel yoludur; ancak otomatik araç desteği olmadan yanıtlanması zor 4 temel soru bulunmaktadır: (a) Kod veya tasarım seviyesindeki kokular nasıl tespit edilecek?, (b) Hangi yeniden yapılandırma tekniği uygulanmalı?, (c) Uygulama adımları nelerdir?, (d) Bu işlemin sağladığı somut kalite kazançları nelerdir?[3].
  * **Literatürdeki Kopukluk ve Araştırma Boşluğu (Research Gap):** Literatürde kod kokuları ve yeniden yapılandırma konularında ayrı ayrı yürütülmüş çok sayıda ikincil çalışma (secondary study) bulunmasına karşın (25'i kod kokularına, 13'ü yeniden yapılandırmaya odaklanmıştır), bu iki araştırma alanı arasındaki bütüncül ilişkiyi ve literatürdeki boşlukları inceleyen sistematik bir çalışma bulunmamaktadır[8].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Bölüm 1 (Introduction), Şekil 5 (Mind-map of secondary studies)[1].
* **Yorum / Çıkarım / Analiz Notu:**
  * Çalışma, problemi yalnızca bireysel kod temizleme teknikleri seviyesinde değil; yüksek bakım maliyetleri, yazılım kalitesindeki bozulma ve akademideki araştırmaların parçalı yapısı (kokular ile refactoring'in birbirinden izole incelenmesi) boyutlarıyla çok yönlü yöntemsel ve teknik bir sorun olarak ele almaktadır.

---

### 2\. Çalışmanın Temel Amacı Nedir?

* **Doğrudan Makaleden Elde Edilen Bilgi:**
  * **Bütüncül Üçüncül İnceleme (Tertiary Systematic Literature Review):** Çalışmanın temel amacı, 1992–2018 yılları arasında yayımlanmış 40 ikincil çalışmayı (surveys, systematic literature reviews - SLR, systematic mappings - SM) inceleyerek kod kokuları (code smells) ve yeniden yapılandırma (refactoring) alanındaki mevcut kanıtları haritalandırmaktır[8].
  * **Bilinenler ve Bilinmeyenler Sentezi:** Literatürdeki kesinleşmiş konsensüsleri (*observations / what we know*) ve henüz çözülememiş açık sorunları (*challenges / open issues / what we do not know*) sistematik biçimde sentezlemektir[8][14].
  * **Kalite İlişkisi ve Gelecek Araştırmalara Rehberlik:** İki alan arasındaki ilişkiyi yazılım kalite nitelikleri (understandability, maintainability, testability, complexity, functionality, reusability) çerçevesinde ortaya koymak ve gelecekteki çalışmalara yön verecek 13 açık araştırma konusunu (open issues) tanımlamaktır[12].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Özet (Abstract), Bölüm 1 (Introduction), Bölüm 3.1 (Goal and Research Questions)[8].
* **Yorum / Çıkarım / Analiz Notu:**
  * Makale doğrudan kaynak kodları inceleyen birincil bir deneysel araştırma yapmak yerine, mevcut tüm derleme ve haritalama araştırmalarını üst seviyede analiz eden yöntemsel bir meta-inceleme (tertiary review) amacı taşımaktadır.

---

### 3\. Yazarların Açıkça Tanımladığı Araştırma Soruları (Research Questions)

* **Doğrudan Makaleden Elde Edilen Bilgi:** Makalede açıkça tanımlanmış 5 araştırma sorusu (RQ1–RQ5) bulunmaktadır[10]:
  * **RQ1: What refactoring-related topics have been investigated in secondary studies?**
    * *Türkçe Açıklaması:* İkincil çalışmalarda yeniden yapılandırma (refactoring) ile ilgili hangi konuların araştırıldığını ve hangi konuların kapsanmadığını belirleyerek yeni ikincil çalışma ihtiyaçlarını ortaya çıkarmak[10].
  * **RQ2: What smells-related topics have been investigated in secondary studies?**
    * *Türkçe Açıklaması:* İkincil çalışmalarda kod ve tasarım kokuları (smells) ile ilgili ele alınan ve ihmal edilen konuları tespit etmek[13].
  * **RQ3: Which tools have been mentioned for code smell detection and refactoring support?**
    * *Türkçe Açıklaması:* Kod kokusu tespiti (smell detection) ve yeniden yapılandırma desteği (refactoring support) için literatürde adı geçen araçları incelemek[13][19].
  * **RQ4: Which RQs have been studied on code smells and refactoring? What are the highest cited secondary studies?**
    * *Türkçe Açıklaması:* İkincil çalışmalarda ne tür araştırma sorularının (RQ kategorileri) sorulduğunu analiz etmek ve en çok atıf alan ikincil araştırmaları belirlemek[13].
  * **RQ5: What are the annual trends of types, quality, and the number of primary studies reviewed by the secondary studies?**
    * *Türkçe Açıklaması:* İkincil çalışmaların incelediği birincil araştırmaların yıllık eğilimlerini, türlerini, metodolojik kalitelerini ve inceledikleri birincil çalışma sayılarını değerlendirerek alanın genel tablosunu çıkarmak[13][20].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Bölüm 1 (Introduction), Bölüm 3.1 (Goal and Research Questions)[10].
* **Yorum / Çıkarım / Analiz Notu:**
  * Araştırma soruları sistematik bir biçimde konu kapsamını (RQ1, RQ2), araç desteğini (RQ3), akademideki etkiyi ve soru yapılarını (RQ4) ve yöntemsel olgunluk eğilimlerini (RQ5) ölçecek şekilde kurgulanmıştır.

---

### 4\. Yazarlar “Code Smell” ve “Refactoring” Kavramlarını Nasıl Ele Alıyor?

* **Doğrudan Makaleden Elde Edilen Bilgi:**
  * **Code Smell (Kod Kokusu) Kavramı:**
    * Kod seviyesindeki problemler "code smell" (Fowler et al., 1999), tasarım seviyesindeki semptomlar ise "design smell" (Brown et al., 1998) olarak adlandırılır[21].
    * Kod kokusu bir yazılım hatasından (bug) farklıdır; uygulama çökmesine doğrudan neden olmaz, ancak kodun anlaşılabilirliğini ve bakımını zorlaştırır, teknik borcu artırır ve gelecekte hata oluşma ihtimalini yükseltir[4].
    * Literatürde adlandırma tutarsızlığı (nomenclature problem) vardır; farklı yazarlar aynı koku için farklı isimler (örn. *Copy and Paste Programming* vs. *Duplicated Code*) veya aynı isim için farklı tanımlar kullanmaktadır[23].
  * **Refactoring (Yeniden Yapılandırma) Kavramı:**
    * Yazılımın dıştan gözlemlenebilir davranışını değiştirmeden (behavior-preserving) koddaki dahili kalite niteliklerini iyileştirme ve kokuları giderme sürecidir (Opdyke 1992, Mens &amp; Tourwé 2004, Fowler &amp; Beck 2019)[3][26].
    * İki ana seviyede gerçekleşir: Küçük değişiklikler için düşük seviyeli (primitive refactorings - örn. *Rename, Extract Method*) ve mimari/makro dönüşümler için yüksek seviyeli (composite refactorings - örn. *Replace Conditional with Polymorphism*)[27][28]. Dönüşümün davranışı bozmadığını doğrulamak için ön-koşullar (preconditions) ve son-koşullar (postconditions) kontrol edilir[28][29].
  * **İki Kavram Arasındaki İlişki:**
    * İki kavram **"aynı paranın iki yüzü" (two faces of a same coin)** olarak tanımlanır[12].
    * Bu iki kavramı birbirine bağlayan temel odak noktası **Yazılım Kalitesi (Software Quality)** ve **Teknik Borçtur (Technical Debt)** [283, 287, 288, Şekil 22].
    * Aralarındaki ilişki birebir (*one-to-one*) değildir; bir koku birden fazla refactoring tekniğiyle giderilebileceği gibi, tek bir refactoring birden fazla kokunun çözümünde uygulanabilir[30].
    * QMOOD modeliyle yapılan analizde, refactoring uygulamalarının dışsal kalite nitelikleri (understandability, maintainability, functionality, reusability) üzerindeki etkisinin kod kokularının kendisinden daha baskın olduğu tespit edilmiştir [18, 310, 311, Şekil 24].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Bölüm 2 (Background - Section 2.1 &amp; 2.2), Bölüm 5 (The relationship between code smells and refactoring - Section 5.1 &amp; 5.2), Şekil 22, Şekil 24[21].
* **Yorum / Çıkarım / Analiz Notu:**
  * Yazarlar her iki kavramı bağımsız teknik konular olarak değil, yazılım kalitesini koruma ve teknik borcu yönetme sürecinin birbirini tamamlayan iki dinamik bileşeni olarak ele almaktadır.

---

### 5\. Bu Çalışmanın Önceki Literatürden Ayrılan Yönü ve Yapılma Gerekçesi Nedir?

* **Doğrudan Makaleden Elde Edilen Bilgi:**
  * **Literatürdeki Boşluk ve Yapılma Gerekçesi:**
    * Kod kokuları ve refactoring alanında yayımlanmış çok sayıda ikincil çalışma bulunmasına rağmen, bu araştırmalar konuları izole bir biçimde incelemiştir[9].
    * İncelenen 40 ikincil çalışmanın **25'i yalnızca kod kokularına**, **13'ü yalnızca yeniden yapılandırmaya** odaklanmış; **her iki konuyu birden ele alan çalışma sayısı sadece 2'de kalmıştır** [93, Şekil 5].
    * İki disiplin arasındaki etkileşimi, ortak araç desteklerini ve kalite üzerindeki birleşik etkilerini derleyen bütüncül bir üçüncül incelemeye (tertiary SLR) ihtiyaç duyulmuştur[8].
  * **Önceki Literatürden Ayrılan Yönleri:**
    * **İlk Geniş Çaplı Üçüncül SLR:** 8 bilimsel veri tabanı kullanılarak 1992–2018 yılları arasındaki 40 ikincil çalışmayı sistematik bir protokol çerçevesinde analiz eden ilk kapsamlı üçüncül araştırmalardan biridir [3, 71, 89, Şekil 3].
    * **Top-10 Kod Kokusu Çapraz Eşleştirme Matrisi (Table 8):** Literatürde en çok incelenen 10 kod kokusunu; tespit yöntemleri, tespit araçları, önerilen refactoring teknikleri ve refactoring araçları ile doğrudan çapraz matrise tabi tutmuştur [17, Tablo 8].
    * **QMOOD Modeli ile Kalite Sentezi:** İçsel nitelikleri (cohesion, coupling, size vb.) dışsal kalite boyutlarıyla QMOOD modeli üzerinden eşleştirerek refactoring'in ve kokuların kalite üzerindeki somut etkilerini görselleştirmiştir [18, 309, 310, Şekil 23, Şekil 24].
    * **13 Açık Araştırma Konusu (Open Issues):** Mevcut literatürün özetlenmesinin ötesine geçerek gelecekteki araştırmalar için 13 açık konu (I1-I13) tanımlamıştır [5, 18, Tablo 14].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Özet (Abstract), Bölüm 1 (Introduction), Bölüm 3.6 (Execution), Bölüm 4 (Table 8), Bölüm 5 (Section 5.1 &amp; 5.2), Bölüm 7 (Table 14), Şekil 3, Şekil 5, Şekil 23, Şekil 24 [3, 5, 14, 15, 17, 18, 71, 89, 93, 309, 310, Tablo 8, Tablo 14].
* **Yorum / Çıkarım / Analiz Notu:**
  * Çalışma, birincil araştırmaları tek tek özetlemek yerine ikincil araştırmaların metodolojik durumunu, kapsam boşluklarını ve çelişkili bulgularını üst seviyede değerlendiren haritalandırıcı bir rehber niteliğindedir.

---

### 6\. Makalenin Yazarlar Tarafından Belirtilen Temel Katkıları Nelerdir?

* **Doğrudan Makaleden Elde Edilen Bilgi:** Yazarlar makalede sağladıkları temel katkıları 4 ana maddede özetlemektedir[14][16]:
  1. **En Sık İncelenen 10 Kod Kokusu İçin Çapraz Matris (Table 8):** En çok bahsedilen 10 kod kokusu (*Duplicated Code/Clones, Large Class/God Class, Feature Envy, Long Method, Long Parameter List, Divergent Change, Data Clumps, Refused Bequest, Shotgun Surgery, Lazy Class*); tespit yaklaşımları, tespit araçları, önerilen refactoring teknikleri ve refactoring araçları ile bir arada haritalandırılmıştır [17, Tablo 8].
  2. **Kalite Etkisi ve QMOOD Modeli İlişkisi (Figure 23 &amp; Figure 24):** İlk 10 kod kokusunun refactoring teknikleri ve kalite nitelikleriyle ilişkisi kurulmuş; QMOOD modeliyle içsel nitelikler dışsal kaliteyle bağdaştırılarak yeniden yapılandırmanın kaliteye etkisinin kod kokularından daha fazla olduğu gösterilmiştir [18, 309, 310, Şekil 23, Şekil 24].
  3. **Paydaş Perspektifleri ve Uygulama Önerileri (Section 6):** Yazılım uygulayıcıları (*practitioners*), akademisyen/eğitmenler (*instructors*) ve araştırmacılar (*researchers*) için ayrı ayrı metodolojik ve pratik öneriler (örn. müfredatta *Coding Dojo* kullanımı, endüstri-akademi iş birliği) sunulmuştur [18, Bölüm 6, 313, 318, 323, 324].
  4. **13 Açık Araştırma Konusu (Section 7 &amp; Table 14):** İleride yapılacak çalışmalara yön vermek üzere kod kokusu adlandırma standartlarından (I1), çoklu dil destekleyen araç eksikliğine (I6, I9) ve kalite izleme sistemlerine (I10) kadar 13 açık konu (I1–I13) tanımlanmıştır [5, 18, Tablo 14].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Bölüm 1 (Introduction), Bölüm 4 (Table 8), Bölüm 5 (Figure 23 &amp; Figure 24), Bölüm 6 (Implications), Bölüm 7 (Open Issues - Table 14) [5, 17, 18, 309, 310, 313, 318, 323, 324, Tablo 8, Tablo 14].
* **Yorum / Çıkarım / Analiz Notu:**
  * Çalışmanın katkıları sadece akademik bir sentez sunmakla kalmayıp; araç geliştiricileri, endüstri uygulayıcıları ve yazılım eğitmenleri için eyleme dönüştürülebilir (*actionable*) somut kılavuzlar sunmaktadır.