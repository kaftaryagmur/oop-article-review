Lacerda vd.'nin (2020) **"Code smells and refactoring: A tertiary systematic review of challenges and observations"** başlıklı makalesinin araştırma metodolojisine ilişkin ayrıntılı analiz ve yapılandırılmış inceleme notları aşağıda sunulmuştur.

Analizdeki tüm sayısal veriler, yöntemsel adımlar ve kısıtlar doğrudan ilgili makaleden alınmış ve kaynak pasajlara dayanan atıflarla `[i]` desteklenmiştir.

---

### 1\. Tertiary Systematic Literature Review Nedir? Bu Makalede Hangi Tür Çalışmalar İncelenmiştir?

* **Doğrudan Makaleden Elde Edilen Bilgi / Tanım:**
  * Üçüncül Sistematik Literatür İncelemesi (Tertiary Systematic Literature Review - Tertiary SLR), belirli bir araştırma alanındaki mevcut kanıt durumunu (*state of the evidence*) haritalandırmak ve sentezlemek amacıyla birincil çalışmalar (*primary studies*) yerine **ikincil çalışmaları (** **secondary studies** **)** inceleyen bir "incelemelerin incelemesi" (*review of reviews*) yöntemidir[1].
* **İncelenen Çalışma Türleri ve Dağılımı:**
  * Bu makalede, 1992–2018 yılları arasında "code smells" (code smells) ve "refactoring" (yeniden yapılandırma) konularında yayımlanmış **40 ikincil çalışma** sistematik olarak incelenmiştir[2][3].
  * Seçilen ikincil çalışmaların türlerine göre sayısal dağılımı şu şekildedir:
    * **Systematic Literature Reviews (SLR) - Sistematik Literatür İncelemeleri:** 26 çalışma (%65)[4].
    * **Systematic Mappings (SM) - Sistematik Haritalamalar:** 7 çalışma (%17.5)[4].
    * **Surveys - Anket/Derleme Çalışmaları:** 7 çalışma (%17.5)[4].
    * **Multivocal Literature Mapping:** 1 çalışma (S16 kodlu çalışma hem survey hem de multivocal niteliğe sahiptir)[4].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Bölüm 1 (Introduction), Bölüm 3.1, Bölüm 4.5.1, Şekil 16 (Type of secondary studies) [13, 260, Şekil 16].
* **Yorum / Çıkarım / Yöntemsel Açıklama:**
  * Üçüncül incelemeler, bir alanda çok sayıda ikincil çalışma biriktiğinde literatürdeki genel konsensüsleri ve kapsanmayan araştırma boşluklarını tek bir çatı altında toplamak için tercih edilir.

---

### 2\. Literatür Taraması Hangi Veri Tabanlarında ve Hangi Arama Stratejisiyle Yapılmıştır?

* **Doğrudan Makaleden Elde Edilen Bilgi:**
  * **Uygulanan Protokol ve Kılavuz:** İnceleme, Kitchenham ve arkadaşlarının (2007, 2009, 2010b) yazılım mühendisliği için önerdiği SLR yönergelerine uygun olarak kurgulanmıştır[5].
  * **Kullanılan 8 Dijital Kütüphane / Veri Tabanı:**
    1. ACM Digital Library[6]
    2. IEEE Xplore[7]
    3. ScienceDirect[7]
    4. Wiley InterScience[8]
    5. Scopus[9]
    6. AIS eLibrary[10]
    7. Google Scholar[10]
    8. Springer[11]
  * **PICOC Yapılandırması:** Arama stratejisi PICOC (Population, Intervention, Comparison, Outcomes, Context) süreci ile yapılandırılmıştır[6]:
    * *Population (P):* Yazılım mühendisliği, yazılım geliştirme, yazılım bakımı/evrimi ve yazılım kalitesi ile ilgili konferans ve dergiler[13].
    * *Intervention (I):* Sistematik literatür incelemeleri, sistematik haritalamalar, derlemeler (surveys) ve sistematik incelemeler[13].
    * *Comparison (C):* İkincil çalışmaları karakterize etmek amaçlandığından "Uygulanamaz" (*Not applicable*)[6][13].
    * *Outcomes (O):* İkincil çalışmalarda tanımlanan yöntemler, teknikler, pratikler, uygulamalar, problemler, stratejiler ve araçlar[11].
    * *Context (C):* Code smells ve refactoring alanı[11].
  * **Kartopu Yöntemi (Snowballing):** Veri tabanı aramalarında gözden kaçabilecek çalışmaları havuza eklemek amacıyla Wohlin (2014) tarafından önerilen referans tarama (snowballing) tekniği uygulanmıştır[14][15].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Bölüm 3.2 (Identification of relevant literature), Tablo 5 (Digital libraries, criteria considered, and search queries) [69-78, Tablo 5].

---

### 3\. Arama İfadeleri (Search Strings) Nelerdir?

* **Doğrudan Makaleden Elde Edilen Bilgi:**
  * **Temel Arama Terimleri:** Yazarların araştırma soruları ve makale anahtar kelimelerinden çıkardığı temel terimler şunlardır: `survey, systematic mapping, systematic literature review, smell, refactoring, tool, technique, method, practice, application, problem, software`[16][17].
  * **Veri Tabanlarına Özel Arama Sorguları (Search Queries per Database):**
    * **ACM Digital Library:** `acmdlTitle:(smell refactoring) AND recordAbstract:(survey ‘‘systematic literature’’ ‘‘systematic literature review’’ ‘‘systematic review’’ review ‘‘systematic mapping’’ ‘‘systematic study’’ ‘‘mapping study’’) AND (tool ∗ technique ∗ method ∗ practice ∗ problem ∗)`[6].
    * **IEEE Xplore:** `((‘‘Document Title’’:smell OR refactoring) AND (‘‘Abstract’’:systematic literature OR systematic mapping OR mapping study OR systematic review OR survey) AND (‘‘Publication Title’’:software engineering OR software quality OR software maintenance OR software evolution))`[7].
    * **ScienceDirect:** `(1) smell OR refactoring (2) survey OR ‘‘systematic literature’’ OR ‘‘systematic literature review’’ OR ‘‘systematic review’’ OR review OR ‘‘systematic mapping’’ OR ‘‘systematic study’’ OR ‘‘mapping study’’` (Title, abstract, keywords)[7][8].
    * **Wiley InterScience:** `survey OR 'systematic literature' OR 'systematic review' OR review OR 'systematic mapping' OR 'systematic study' OR study OR mapping’’ in Abstract and ‘‘refactoring OR smell’’ in Abstract AND software AND (technique ∗ OR tool ∗ OR method ∗ OR practice ∗ OR application OR problem)`[8].
    * **Scopus:** `(TITLE(survey OR ‘‘systematic literature’’ OR ‘‘systematic literature review’’ OR ‘‘systematic review’’ OR review OR ‘‘systematic mapping’’ OR ‘‘systematic study’’ OR ‘‘mapping study’’) AND TITLE-ABS(refactoring OR smell)) AND ALL(tool ∗ OR technique ∗ OR method ∗ OR practice ∗ OR problem ∗ AND software) AND ((PUBYEAR &gt; 1992) AND (PUBYEAR &lt; 2019)) AND (LIMIT-TO(SUBJAREA, ‘‘COMP’’)) AND (LIMIT-TO(DOCTYPE, ‘‘cp’’) OR LIMIT-TO(DOCTYPE, ‘‘ar’’)) AND (LIMIT-TO(LANGUAGE, ‘‘English’’))`[9].
    * **AIS eLibrary:** `(survey OR 'systematic literature' OR 'systematic review' OR review OR 'systematic mapping' AND software) AND abstract:(refactoring OR smell) AND (software AND (technique ∗ OR tool ∗ OR method ∗ OR practice ∗ OR application OR problem ∗))`[10].
    * **Google Scholar:** `1992–2018 allintitle:(smell OR refactoring) AND (‘‘systematic literature’’ OR ‘‘systematic mapping’’ OR ‘‘systematic study’’ OR ‘‘literature review’’ OR survey)`[10].
    * **Springer:** `(systematic literature OR mapping study OR systematic mapping OR literature review) AND (smell OR refactor ∗) AND (tool ∗ OR technique ∗ OR method ∗ OR practice ∗ OR problem ∗)`[11].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Bölüm 3.2, Tablo 5 [71-78, Tablo 5].

---

### 4\. Dahil Etme ve Dışlama Kriterleri (Inclusion/Exclusion Criteria) Nelerdir?

* **Doğrudan Makaleden Elde Edilen Bilgi:**
  * **Dışlama Kriterleri (Exclusion Criteria):**
    1. Yazılım mühendisliği alanı (geliştirme, kalite, bakım ve evrim) ile ilgili olmayan makaleler[18].
    2. İngilizce dilinde yazılmamış çalışmalar[18].
    3. Bilişim alanındaki akademik olmayan etkinliklerde sunulan metinler (ör. *Agile Conference, Agiles Conf*)[18][19].
    4. Öğretici materyaller (*tutorials*), pozisyon bildirileri (*position papers*), yüksek lisans ve doktora tezleri (*theses and dissertations*)[19].
  * **Dahil Etme Kriterleri (Inclusion Criteria):**
    1. Code smells ve refactoring konularındaki ikincil çalışmalar (Systematic Literature Reviews, Systematic Mappings, Surveys)[19].
    2. Code smell tespiti için araçların, yöntemlerin, pratiklerin kullanımını, geliştirilmesini veya değerlendirilmesini açıklayan makaleler[19].
    3. Refactoring araçlarının, yöntemlerinin ve tekniklerinin kullanımını, geliştirilmesini veya değerlendirilmesini açıklayan makaleler[19].
    4. **1992–2018** yılları arasında yayımlanmış araştırmalar (1992, Opdyke'ın refactoring konulu ilk doktora tezinin yayın yılıdır)[14][19].
    5. Sadece tam akademik makaleler (**6 sayfadan uzun / full papers**)[14].
    6. Çevrim içi olarak indirilebilir ve erişilebilir durumda olması[14].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Bölüm 3.3 (Selection criteria)[14].

---

### 5\. İlk Bulunan, Eleme Aşamalarından Geçen ve Nihai Olarak Seçilen Çalışma Sayıları Nelerdir?

* **Doğrudan Makaleden Elde Edilen Bilgi:**
  * **İlk Bulunan Toplam Çalışma Sayısı:** 8 veri tabanından toplam **467** ikincil çalışma tespit edilmiştir[15][20].
    * *Veri tabanlarına göre ilk sonuç dağılımı:* ACM: 30, IEEE: 65, Scopus: 58, ScienceDirect: 130, Springer: 89, Google Scholar: 33, AIS: 40, Wiley: 22 [89, Şekil 3].
  * **1\. Eleme Aşaması (Başlık, Özet ve Anahtar Kelime Filtrelemesi):** Kriterlere göre yapılan ön seçim sonucu sayı **59** çalışmaya düşürülmüştür [86, 87, Şekil 3].
  * **2\. Eleme Aşaması (Mükerrer Çıkarma ve Tam Metin Analizi):** 59 çalışmadan 26'sı (6 mükerrer/duplicate + seçim kriterlerine uymayan 20 çalışma) elenmiş ve geriye **33** seçilmiş çalışma kalmıştır [87, Şekil 3].
  * **Kartopu / Snowballing Yöntemi İle Eklenenler:** Seçilen 33 çalışmanın referanslarındaki toplam **7.141 referans** gözden geçirilmiş, 184 çalışma detaylı incelenmiş ve kriterlere uyan **7** yeni çalışma havuza eklenmiştir[21][22].
  * **Nihai Seçilen Çalışma Sayısı:** İncelemeye toplam **40 ikincil çalışma** dahil edilmiştir [88, Şekil 3].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Bölüm 3.6 (Execution), Şekil 3 (Steps of execution research and number of selected studies) [86-89, Şekil 3].

---

### 6\. Quality Assessment Nasıl Uygulanmıştır?

* **Doğrudan Makaleden Elde Edilen Bilgi:**
  * **Metodolojik Model:** York Üniversitesi *Centre for Reviews and Dissemination (CRD) Database of Abstracts of Reviews of Effects (DARE)* kriterleri ve Kitchenham et al. tarafından üçüncül SLR'lar için önerilen kalite değerlendirme modeli kullanılmıştır[14][23].
  * **4 Kalite Değerlendirme Sorusu:**
    1. İncelemenin dahil etme ve dışlama kriterleri açıklanmış ve uygun mudur? (*Are the reviews inclusion and exclusion criteria described and appropriate?*)[23].
    2. Literatür taramasının ilgili tüm çalışmaları kapsama olasılığı yüksek midir? (*Is the literature search likely to have covered all relevant studies?*)[23][24].
    3. İncelemeyi yapanlar dahil edilen çalışmaların kalitesini/geçerliliğini değerlendirmiş midir? (*Did the reviewers assess the quality/validity of the included studies?*)[24].
    4. Birincil veriler/çalışmalar yeterince tanımlanmış mıdır? (*Were the primary data/studies adequately described?*)[24].
  * **Puanlama Yöntemi ve Ölçek:** Her aday çalışma için 4 sorunun her birine **{0, 0.5, 1}** değerlerinden biri verilmiş ve toplanmıştır; toplam kalite puanı **0 ile 4** arasında ölçeklenmiştir[24][25].
  * **Kalite Değerlendirme Sonuçları:**
    * Seçilen 40 çalışmanın tamamı **2 ile 4** arasında puan almıştır [276, Şekil 21].
    * Çalışmaların **%80'inden fazlası 3 ile 4** arasında yüksek kalite puanına sahiptir[25][26]. Surveys (anketler/derlemeler) resmi bir SLR protokolü izlemediği için nispeten daha düşük puan almıştır[25].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Bölüm 3.4 (Quality assessment), Bölüm 4.5.3, Şekil 21 (Total quality score per year) [81-83, 275-277, Şekil 21].

---

### 7\. Data Extraction ve Synthesis Süreçleri Nasıl Gerçekleştirilmiştir?

* **Doğrudan Makaleden Elde Edilen Bilgi:**
  * **Veri Çıkarma (Data Extraction) Yapısı:** Veri extraction süreci yapılandırılmış bir **Google Forms** formu üzerinden yürütülmüştür[24].
  * **Toplanan Veri Kalemleri:**
    * *Makale künyesi:* Başlık, yazarlar, kurum, ülke, yayın yılı, araştırmanın başlangıç/bitiş yılı, yayın yeri, özet, anahtar kelimeler, yayın türü (dergi/konferans)[27].
    * *Araştırma yöntemi türü ve katkılar:* (Survey, Systematic Mapping, SLR)[27].
    * *Kullanılan veri tabanları ve Araştırma Soruları (RQs)*[27].
    * *İncelenen birincil makale sayısı*[27].
    * *Smells ve refactoring kategorizasyonları*[27][28].
    * *Araştırma yaklaşımları:* (Vaka çalışmaları, anketler, deneysel ve ampirik araştırmalar)[28].
    * *Proje ve veri seti türleri:* (FLOSS, ticari/endüstriyel, akademik/toy), kod depoları ve programlama dilleri[28].
    * *Bağlam:* İncelenen refactoring teknikleri, en çok atıf alan araçlar ve açıklanan kod/design smells[28].
  * **Kullanılan Yardımcı Araçlar:** Makalelerin kataloglanması ve yapılandırılmasında **Mendeley** kullanılmıştır[28]. Elde edilen veriler açık erişimli bir *replication package* olarak paylaşılmıştır[29].
  * **Sentez ve Sınıflandırma Yöntemi (Card Sorting):** Makalelerden elde edilen konu ve temaları gruplandırmak amacıyla **Card Sorting** (Kart Sıralama / Barrett and Edwards, 1995) yöntemi uygulanmıştır[30].
  * **Tematik Dağılım:** Sentez sonucunda ikincil çalışmalar 3 ana temaya ayrılmıştır [91, Şekil 5]:
    1. *Refactoring odaklı çalışmalar:* 13 çalışma [91, 98, Şekil 5].
    2. *Smells (kod/design smells) odaklı çalışmalar:* 25 çalışma [91, 150, Şekil 5].
    3. *Her iki konuyu birden ele alan çalışmalar:* 2 çalışma [91, Şekil 5].
  * **İlave Sentez Modelleri:** RQ4 kapsamındaki sorular Easterbrook et al. (2008) taksonomisine göre sınıflandırılmış [231, Tablo 10]; kokular ve refactoring'in kaliteye etkisi ise **QMOOD modeli** çerçevesinde haritalandırılmıştır [304, Şekil 23, Şekil 24].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Bölüm 3.5, Bölüm 3.6, Bölüm 4 (Şekil 5, Tablo 10), Bölüm 5 (Şekil 23, Şekil 24) [83-86, 91-94, 231, 304, Şekil 5, Şekil 23, Şekil 24, Tablo 10].

---

### 8\. Araştırmanın Kapsadığı Yayın Yılları Nelerdir?

* **Doğrudan Makaleden Elde Edilen Bilgi:**
  * **Taranan Yayın Yılları:** Makale **1992 – 2018** yılları arasında yayımlanmış çalışmaları kapsamaktadır[15][19].
  * **Başlangıç Yılı Gerekçesi:** Refactoring alanındaki ilk ayrıntılı yazılı çalışma kabul edilen William Opdyke'ın 1992 tarihli doktora tezidir[14].
  * **Elde Edilen İkincil Çalışmaların Yayın Dağılımı:** Taramada ulaşılan **en eski ikincil çalışma 2004 yılına** aittir (Mens ve Tourwé, 2004)[32]. 2004–2012 yılları arasında kısıtlı sayıda ikincil yayın bulunurken, **2013 yılından itibaren** yayın sayısında hızlı bir artış gerçekleşmiştir[32].
  * **Kapsanan Birincil Araştırmaların Zaman Aralığı:** Seçilen 40 ikincil çalışmanın kendi bünyelerinde taradığı birincil araştırmaların ortalama kapsama süresi **15.2 yıldır**[33]. (En kısa zaman aralığı S8 ile 7 yıl: 2007–2014; en geniş zaman aralığı S40 ile 27 yıl: 1990–2017)[33].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Bölüm 3.3, Bölüm 3.6, Bölüm 4.5.1, Bölüm 4.5.3, Şekil 15 (Distribution of publications per year) [80, 89, 90, 259, 271, Şekil 15].

---

### 9\. Yazarların Belirttiği Threats to Validity Nelerdir?

* **Doğrudan Makaleden Elde Edilen Bilgi:** Yazarlar makalenin geçerlilik tehditlerini (*Threats to Validity*) 6 ana noktada toplamış ve aldıkları önlemleri açıklamışlardır[34]:
  1. **Arama Dizesi Tehdidi (Search String / Construct Validity):** Tanımlanan arama dizesinin ilgili tüm ikincil çalışmaları kapsayamama riski.
    * *Alınan Önlem:* Temel terimlerin çeşitli eş anlamlıları dizeye eklenmiş ve arama dizesini optimize etmek için pilot aramalar yürütülmüştür[34].
  2. **Veri Tabanı Seçimi ve Kapsam Tehdidi (Database Selection / External Validity):** İncelemenin 8 veri tabanı ile sınırlı kalması nedeniyle diğer veri tabanlarındaki yayınların kaçırılma riski.
    * *Alınan Önlem:* Kartopu (snowballing) yöntemi uygulanarak seçilen makalelerin referans listeleri taranmış ve ilave çalışmalar havuza dahil edilmiştir[35][36].
  3. **Dil Kısıtlaması (Language Bias):** Yalnızca İngilizce dilindeki makalelerin incelemeye alınması.
    * *Gerekçe/Açıklama:* Yazılım mühendisliği alanındaki temel bilimsel yayın mecralarının İngilizce yayın kabul etmesi nedeniyle bu kısıtlamanın kabul edilebilir olduğu belirtilmiştir[36][37].
  4. **Öznel Veri Çıkarma ve Sınıflandırma Tehdidi (Subjectivity in Classification &amp; Data Extraction):** Veri çıkarma ve kategorizasyon adımlarının araştırmacıların öznel yorumlarına açık olması.
    * *Alınan Önlem:* Taraf tutmayı (bias) önlemek için standart prosedürler ve yapılandırılmış veri çıkarma formları izlenmiştir[37].
  5. **Veri Ayrıntı Düzeyi Tehdidi (Granularity of Secondary Studies):** İncelenen ikincil çalışmaların kendi raporlama eksikliklerinin veya ayrıntı düzeylerinin çıkarılan sonuçları etkileme riski[37][38].
  6. **Güvenilirlik ve Tekrarlanabilirlik (Reliability Validity):** Çalışmanın başkaları tarafından tekrarlanabilirliği.
    * *Alınan Önlem:* Araştırma protokolü ve arama dizeleri ayrıntılı açıklanmış, ayrıca bir *replication package* sunularak tekrarlanabilirlik garanti edilmiştir[29][38].
* **Dayandığı Bölüm / Tablo / Şekil:**
  * Bölüm 3.5, Bölüm 8 (Threats to validity)[29].
