# I1–I13 Ayrıntılı Analiz Kaydı

Bu dosya ilk ayrıntılı çözümlemeyi korur. Tablo 14'ün doğrudan içeriği ile bu içerikten türetilen açıklamalar aynı kanıt düzeyinde değildir. Doğrulanmış başlıklar ve sınırlar için `../paper-evidence.md` ile `../verification-log.md` esas alınmalıdır. Özellikle `%57 FLOSS` I13'ün tanımı değil, Bölüm 4.5.2'de anılan deney projelerinin oranıdır; I8 için “14 tekniği inceleyen hiçbir çalışma yoktur” biçimindeki mutlak ifade de Tablo 14 tarafından desteklenmez.

Lacerda vd.'nin (2020) **"Code smells and refactoring: A tertiary systematic review of challenges and observations"**[1] başlıklı makalesinin **Section 7 (Open Issues)** ve **Table 14** bölümlerinde tanımlanan **13 açık araştırma problemi (I1–I13)**[2] temel alınarak hazırlanmış yapılandırılmış araştırma notları aşağıda sunulmuştur.

---

### 1\. I1–I13 Açık Araştırma Problemlerinin Detaylı Analizi

Yazarlar, literatürdeki ikincil araştırmalardan elde edilen sentez sonucunda 13 açık araştırma alanı belirlemişlerdir[2]. Her bir problemin ayrıntılı dökümü şu şekildedir:

---

#### **I1: Code Smell Naming (Code Smell Adlandırması ve Terminoloji Sorunu)**

* **Özgün İngilizce Başlık/İfade:** *I1 - Code smell naming*[4] / *problem of code smell nomenclature*[4].
* **Türkçe Açıklaması:** Kod ve design smellsnın adlandırılmasında ve tanımlanmasında belirgin bir terminoloji tutarsızlığı ve parçalanmışlık bulunmaktadır[4].
* **Neden Önemlidir?:** Code smells karmaşık ve gayriresmi tanımlara sahiptir[11]. Resmi bir taksonomik standardın olmaması[23], farklı araştırmacıların aynı koku için farklı isimler (ör. *Copy and Paste Programming* vs. *Duplicated Code* veya *Blob* vs. *God Class/Large Class*) kullanmasına ya da aynı ismi farklı durumlar için tanımlamasına neden olur[21]. Bu durum tespit araçlarının sonuçlarını doğrudan olumsuz etkiler[25][26].
* **Hangi Bulgudan Kaynaklanmaktadır?:** Section 4.2.2[21] ve ikincil çalışmaların [S11, S12, S15, S39, S40] değerlendirilmesinden[4][10].
* **Makalede Önerilen Çözüm / Araştırma Yönü:** Code smell türlerinin adlandırılması ve tanımlarının standartlaştırılması[11]; *Design Patterns* kataloğuna benzer biçimde "diğer adları" (*also known as*) içeren tekil ve bütünleşik bir koku kataloğunun oluşturulması[11][25].
* **İlgili Bölüm, Tablo ve Şekiller:** Section 4.2.2[21], Section 7[10][11], Table 14[4].

---

#### **I2: Approaches to Code Smell Detection (Code Smell Tespit Yaklaşımları)**

* **Özgün İngilizce Başlık/İfade:** *I2 - Approaches to code smell detection*[4] / *which approaches are most effective in smell detection*[4].
* **Türkçe Açıklaması:** Hangi code smell tespit yaklaşımının (metrik tabanlı, kural tabanlı, makine öğrenmesi/arama tabanlı, görselleştirme, geçmiş tabanlı vb.) en etkili olduğunun belirlenmesi gerekliliğidir[4].
* **Neden Önemlidir?:** Mevcut tespit yaklaşımları yüksek yanlış pozitif (*false positive*) oranlarına sahiptir ve sonuçları birbiriyle tutarsızdır[28]. Ayrıca metrik tabanlı yaklaşımlarda eşik değerleri (*thresholds*) standartlaştırılmadığı için farklı tespit yöntemleri tamamen çelişkili sonuçlar üretmektedir[31].
* **Hangi Bulgudan Kaynaklanmaktadır?:** Section 4.2.3[27], Table 8[34] ve 10 ikincil çalışmanın [S2, S13, S15, S18, S19, S20, S30, S31, S32, S33] sentezinden[4].
* **Makalede Önerilen Çözüm / Araştırma Yönü:** Farklı tespit yaklaşımlarının etkililiğinin karşılaştırılması; yaklaşımların kombinasyonlarının (ör. arama tabanlı ve makine öğrenmesi teknikleri) incelenmesi ve henüz tespit yöntemi bulunmayan kokular için yeni yaklaşımların geliştirilmesi[11].
* **İlgili Bölüm, Tablo ve Şekiller:** Section 4.2.3[27], Section 7[11][12], Table 8[34], Table 14[4].

---

#### **I3: Code Smell and Industry Perception (Code Smells ve Endüstri Algısı)**

* **Özgün İngilizce Başlık/İfade:** *I3 - Code smell and industry perception*[5] / *whether practitioners recognize code smells*[5][12].
* **Türkçe Açıklaması:** Yazılım geliştiricilerin ve endüstri uygulayıcılarının akademik olarak tanımlanan code smell türlerini tanıyıp tanımadıklarının ve bunları kod kalitesi problemlerinin semptomları olarak algılayıp algılamadıklarının değerlendirilmesidir[5][12].
* **Neden Önemlidir?:** Akademik literatürde tanımlanan kokular ile endüstrideki yazılım geliştiricilerin günlük pratikte karşılaştığı problemler ve zihinsel modeller arasında kopukluk bulunmaktadır[5].
* **Hangi Bulgudan Kaynaklanmaktadır?:** Section 4.2.4[40], Section 6[41][42] ve ikincil çalışmaların [S15, S23, S24] değerlendirilmesinden[5].
* **Makalede Önerilen Çözüm / Araştırma Yönü:** Geliştiricilerin code smell türlerine ilişkin algılarını, kokuları nasıl tespit ettiklerini ve gerçek projelerdeki davranışlarını inceleyen ampirik saha araştırmalarının yürütülmesi[5][12].
* **İlgili Bölüm, Tablo ve Şekiller:** Section 4.2.4[40], Section 6[41][42], Section 7[12], Table 14[5].

---

#### **I4: Developers and Code Smell Detection Process (Geliştiriciler ve Code Smell Tespit Süreci)**

* **Özgün İngilizce Başlık/İfade:** *I4 - Developers and code smell detection process*[5] / *evaluating the participation of developers in the code smell detection process*[5][13].
* **Türkçe Açıklaması:** Code smell tespit sürecine geliştiricilerin ne zaman ve nasıl katılması gerektiğinin ve insan faktörünün tespit sürecine entegrasyonunun incelenmesidir[5][13].
* **Neden Önemlidir?:** Tam otomatik araçlar kodun bağlamını ve geliştirici niyetini tam olarak kavrayamaz[43][44]; tamamen manuel (insan algısına dayalı) tespit ise zaman alıcı ve hataya açıktır[45].
* **Hangi Bulgudan Kaynaklanmaktadır?:** Section 4.2.3[45][46], Section 4.3.4[48] ve ikincil çalışmaların [S2, S11] bulgularından[5].
* **Makalede Önerilen Çözüm / Araştırma Yönü:** İnsan uzmanlığını ve geliştiricilerin deneyimlerini/içgörülerini otomatik tespit süreçlerine dahil eden hibrit veya etkileşimli tespit mekanizmalarının geliştirilmesi[5].
* **İlgili Bölüm, Tablo ve Şekiller:** Section 4.2.3[45][46], Section 4.3.4[48], Section 7[12][13], Table 14[5].

---

#### **I5: Code Smell and Impact on Quality Attributes (Code Smells ve Kalite Nitelikleri Üzerindeki Etki)**

* **Özgün İngilizce Başlık/İfade:** *I5 - Code smell and impact on quality attributes*[5] / *explicit connection between smells and quality*[5].
* **Türkçe Açıklaması:** Code smells ile yazılımın dışsal ve içsel kalite nitelikleri (bakım yapılabilirlik, anlaşılabilirlik, test edilebilirlik vb.) arasındaki doğrudan ve ölçülebilir bağlantıların ortaya konulmasıdır[5].
* **Neden Önemlidir?:** Literatürdeki birçok çalışma code smell türlerinin kalite üzerindeki olumsuz etkilerini varsaymakta, ancak bu etkileri doğrudan ve somut ölçümlerle kanıtlamakta eksik kalmaktadır[5].
* **Hangi Bulgudan Kaynaklanmaktadır?:** Section 4.2.4[29][40], Section 5.1[50][51] ve ikincil çalışmaların [S15, S23, S24] değerlendirilmesinden[5].
* **Makalede Önerilen Çözüm / Araştırma Yönü:** Belirli code smell türlerinin bireysel veya bir arada (co-occurrence) ortaya çıktığında kalite standartları (ör. ISO/IEC 25010) üzerindeki somut etkilerini ölçen ampirik araştırmaların yapılması[5].
* **İlgili Bölüm, Tablo ve Şekiller:** Section 4.2.4[29][40], Section 5.1[50][51], Section 7[13], Table 14[5].

---

#### **I6: Code Smell Tools (Code Smell Tespit Araçları)**

* **Özgün İngilizce Başlık/İfade:** *I6 - Code smell tools*[5] / *opportunities to explore smell detection tools*[5].
* **Türkçe Açıklaması:** Code smell tespit araçlarının teknik kısıtlarının giderilmesi ve daha gelişmiş araçların geliştirilmesidir[5].
* **Neden Önemlidir?:** Mevcut code smell tespit araçlarının çoğu eskimiştir veya ölçeklenebilirlik, önceliklendirme, görselleştirme, çoklu dil desteği, düşük doğruluk (precision/recall) gibi ciddi kısıtlara sahiptir[14]. Araçlar ortalama olarak yalnızca 3 ila 4 koku türünü kapsayabilmektedir[55][56] ve %57'den fazlası yalnızca Java odaklıdır[53].
* **Hangi Bulgudan Kaynaklanmaktadır?:** Section 4.3.2[43], Table 8[34] ve 9 ikincil çalışmanın [S2, S4, S9, S13, S15, S18, S19, S39, S40] analizinden[5].
* **Makalede Önerilen Çözüm / Araştırma Yönü:** Çoklu programlama dilini (özellikle JavaScript) destekleyen, ölçeklenebilir, gelişmiş görselleştirme ve filtreleme özelliklerine sahip kapsayıcı araçların geliştirilmesi[14].
* **İlgili Bölüm, Tablo ve Şekiller:** Section 4.3.2[43], Section 7[13][14], Table 8[34], Table 14[5].

---

#### **I7: Developer’s Refactoring Knowledge (Geliştiricinin Refactoring Bilgisi ve Zihinsel Modeli)**

* **Özgün İngilizce Başlık/İfade:** *I7 - Developer’s refactoring knowledge*[6] / *developers’ knowledge about refactoring*[6].
* **Türkçe Açıklaması:** Geliştiricilerin refactoring yaparken kullandıkları zihinsel modellerin, karar verme süreçlerinin ve bilgi düzeylerinin incelenmesidir[6].
* **Neden Önemlidir?:** IDE'ler otomatik refactoring işlevleri sunsa da, geliştiriciler kullanılabilirlik sorunları, güvensizlik veya refactoring sürecine dair bilgi eksikliği nedeniyle bu otomatik işlevleri sıklıkla kullanmamaktadır[14]. Refactoring kararları rasgele veya öznel verilebilmektedir[15][41].
* **Hangi Bulgudan Kaynaklanmaktadır?:** Section 4.3.3[59], Section 4.3.4[48], Section 6[41][42] ve ikincil çalışmaların [S10, S22] sentezinden[6].
* **Makalede Önerilen Çözüm / Araştırma Yönü:** Geliştiricilerin karar alma mekanizmalarının (rasyonel vs. öznel), günlük refactoring alışkanlıklarının ve öğrenme süreçlerinin ampirik olarak değerlendirilmesi[6].
* **İlgili Bölüm, Tablo ve Şekiller:** Section 4.3.3[59], Section 4.3.4[48], Section 6[41][42], Section 7[14][15], Table 14[6].

---

#### **I8: Refactoring and Impact on Quality Attributes (Refactoring ve Kalite Nitelikleri Üzerindeki Etki)**

* **Özgün İngilizce Başlık/İfade:** *I8 - Refactoring and impact on quality attributes*[6] / *relationships with quality attributes*[6].
* **Türkçe Açıklaması:** Az incelenmiş refactoring tekniklerinin ve geliştiriciler tarafından pratikte en sık kullanılan tekniklerin yazılım kalite nitelikleri üzerindeki etkilerinin araştırılmasıdır[6].
* **Neden Önemlidir?:** Literatürde tanımlı 72 refactoring tekniğinden yalnızca 20 ila 27 adedi kalite açısından incelenmiştir[62][63]. Top-10 code smellnu gidermek için önerilen 14 refactoring tekniğinin kalite üzerindeki somut etkisine dair hiçbir akademik çalışma bulunmamaktadır[61]. Ayrıca refactoring yanlış uygulandığında kaliteyi iyileştirmek yerine düşürebilmektedir[60].
* **Hangi Bulgudan Kaynaklanmaktadır?:** Section 4.1.1[62], Section 4.1.3[60], Section 5.2[61][69] ve ikincil çalışmaların [S4, S5, S7, S22] analizinden[6].
* **Makalede Önerilen Çözüm / Araştırma Yönü:** Az araştırılmış refactoring tekniklerinin bireysel kalite nitelikleri (güvenlik, anlaşılabilirlik, genişletilebilirlik) üzerindeki etkilerinin ISO/IEC 25010 gibi standart kalite modelleri çerçevesinde sistematik olarak ölçülmesi[6].
* **İlgili Bölüm, Tablo ve Şekiller:** Section 4.1.3[60], Section 5.2[61], Section 7[15][16], Table 14[6].

---

#### **I9: Refactoring Tools (Refactoring Araçları ve Otomasyonu)**

* **Özgün İngilizce Başlık/İfade:** *I9 - Refactoring tools*[7] / *propose/improve refactoring tools*[7].
* **Türkçe Açıklaması:** Refactoring destek araçlarının geliştirilmesi, iyileştirilmesi ve code smell tespiti ile otomatik refactoring uygulamasının birleştirilmesidir[7].
* **Neden Önemlidir?:** Literatürde tanımlanan refactoring araçlarının sayısı oldukça azdır (13 ikincil çalışmada yalnızca 24 araç tespit edilmiştir)[71]. En önemlisi, tespit edilen kokuya göre refactoring uygulamasını tamamen otomatikleştiren entegre araç sayısı yok denecek kadar azdır (Table 8'de `*` ile işaretlenmiştir)[34][72]. Araçlar refactoring sırasında oluşan hataları bildirmede yetersizdir[48].
* **Hangi Bulgudan Kaynaklanmaktadır?:** Section 4.3.3[71][73], Section 4.3.4[48], Table 8 (\* sembolü)[34][72] ve ikincil çalışmaların [S2, S9, S17, S18, S39, S40] sonuçlarından[7].
* **Makalede Önerilen Çözüm / Araştırma Yönü:** Geliştiricinin ihtiyacına göre özelleştirilebilen, code smell tespiti ile refactoring önerisi ve uygulamasını doğrudan bağlayan, refactoring etkilerini öngören güvenilir araçların geliştirilmesi[7].
* **İlgili Bölüm, Tablo ve Şekiller:** Section 4.3.3[71][73], Section 4.3.4[48], Section 7[17], Table 8[34], Table 14[7].

---

#### **I10: Refactoring Tracking (Refactoring İzleme ve Etki Takibi)**

* **Özgün İngilizce Başlık/İfade:** *I10 - Refactoring tracking*[7] / *monitoring the effects of refactoring*[7].
* **Türkçe Açıklaması:** Yapılan refactoring işlemlerinin ve bunların yazılım evrimi üzerindeki uzun vadeli etkilerinin takip edilmesi ve izlenmesidir[7].
* **Neden Önemlidir?:** Refactoring işlemlerinin maliyetleri somut ve anlık iken, kazançları soyut ve uzun vadelidir[77]. Refactoring uygulamasının uzun vadeli etkilerini ve teknik borç üzerindeki değişimini izleyen mekanizmaların eksikliği kararları zorlaştırmaktadır[75].
* **Hangi Bulgudan Kaynaklanmaktadır?:** Section 4.1.4[75][77], Section 6[76] ve ikincil çalışmaların [S21, S23] bulgularından[7].
* **Makalede Önerilen Çözüm / Araştırma Yönü:** Yazılım evrimi boyunca refactoring dönüşümlerini ve bunların kalite/maliyet üzerindeki uzun vadeli sonuçlarını izleyen takip sistemlerinin ve araştırmalarının kurgulanması[7][18].
* **İlgili Bölüm, Tablo ve Şekiller:** Section 4.1.4[75][77], Section 6[76], Section 7[18], Table 14[7].

---

#### **I11: Architectural Refactoring versus Contextual Refactoring (Mimari Refactoring ile Bağlamsal Refactoring Karşılaştırması)**

* **Özgün İngilizce Başlık/İfade:** *I11 - Architectural refactoring versus contextual refactoring*[7] / *frontier about architectural and contextual refactoring*[7].
* **Türkçe Açıklaması:** Mimari seviyedeki (makro/paket düzeyi) refactoring ile bağlamsal/yerel seviyedeki (mikro/sınıf/metot düzeyi) refactoring arasındaki sınırların ve kaliteye etkilerinin araştırılmasıdır[7].
* **Neden Önemlidir?:** Mimari refactoring yüksek riskli, tahmin edilmesi ve önceliklendirilmesi zor bir süreçtir[78]. Alt seviye kod dönüşümleri ile sistem geneline yayılan mimari dönüşümlerin kalite kazançları arasındaki sınırlar belirsizdir[18][78].
* **Hangi Bulgudan Kaynaklanmaktadır?:** Section 2.2.1[79][80], Section 4.1.4[78] ve ikincil çalışmaların [S21, S23, S26, S27] değerlendirilmesinden[7].
* **Makalede Önerilen Çözüm / Araştırma Yönü:** Paket, sınıf ve metot düzeyindeki dönüşüm sınırlarının (frontiers) belirlenmesi ve mimari refactoring'in kalite üzerindeki somut faydalarının araştırılması[7][18].
* **İlgili Bölüm, Tablo ve Şekiller:** Section 2.2.1[79][80], Section 4.1.4[78], Section 7[18], Table 14[7].

---

#### **I12: Teaching Code Smell and Refactoring (Code Smells ve Refactoring Öğretimi)**

* **Özgün İngilizce Başlık/İfade:** *I12 - Teaching code smell and refactoring*[8] / *best practices and tools for learning and training*[8].
* **Türkçe Açıklaması:** Code smells ve refactoring konularının yazılım mühendisliği eğitim müfredatlarına entegrasyonu ve sınıf içi öğretim yöntemlerinin geliştirilmesidir[8].
* **Neden Önemlidir?:** Öğrencilerin ve yeni yazılım geliştiricilerin kod kalitesi, temiz kod ilkeleri ve refactoring bilinci kazanması endüstrideki kalite açıklarını kapatmak için şarttır[82][83]. Klasik teorik anlatımlar bu becerileri kazandırmada yetersiz kalmaktadır[81][84].
* **Hangi Bulgudan Kaynaklanmaktadır?:** Section 6 (Instructors)[81] ve Table 14[8].
* **Makalede Önerilen Çözüm / Araştırma Yönü:** Sınıf ortamlarında gerçek dünya projeleri, etkileşimli eğitsel araçlar, ciddi oyunlar (*serious games*) ve pratik uygulamaya dayalı *Coding Dojo* etkinliklerinin kullanımı üzerine araştırmalar yapılması[8].
* **İlgili Bölüm, Tablo ve Şekiller:** Section 6[81], Section 7[19], Table 14[8].

---

#### **I13: Research Gaps on Code Smell and Refactoring (Code Smell ve Refactoring Araştırmalarındaki Boşluklar ve Veri Seti Eksiklikleri)**

* **Özgün İngilizce Başlık/İfade:** *I13 - Research gaps on code smell and refactoring*[8] / *reliable datasets, large-scale projects, data inconsistencies*[8].
* **Türkçe Açıklaması:** Araştırmalarda güvenilir veri setlerinin eksikliği, açık kaynak kodlu projelere aşırı bağımlılık ve veri tutarsızlıkları gibi metodolojik boşlukların giderilmesidir[8].
* **Neden Önemlidir?:** Deneylerde kullanılan projelerin %57'si açık kaynak kodlu (FLOSS) projelerdir[86][88]. Sektör uzmanlarınca doğrulanmış ortak mihenk taşı (*benchmark*) veri setleri bulunmamaktadır[87][89]. Bu durum araştırma sonuçlarının genellenebilirliğini ve güvenilirliğini tehdit eder[87][90].
* **Hangi Bulgudan Kaynaklanmaktadır?:** Section 4.5.1[91][92], Section 4.5.2[86][87] ve 12 ikincil çalışmanın [S5, S15, S17, S20, S21, S23, S24, S26, S27, S34, S37, S40] analizinden[8].
* **Makalede Önerilen Çözüm / Araştırma Yönü:** Karşılaştırılabilir ve güvenilir mihenk taşı veri setlerinin (PROMISE benzeri) oluşturulması; geniş ölçekli endüstriyel ve akademik projelerin bir arada kullanıldığı araştırmaların yürütülmesi[8].
* **İlgili Bölüm, Tablo ve Şekiller:** Section 4.5.2[86][87], Section 7[19][20], Table 14[8].

---

### 2\. Problemlerin Tematik Sınıflandırılması

13 açık araştırma problemi (I1–I13) içeriksel odaklarına göre 7 ana tematik grupta toplanmıştır[4]:

1. **Terminoloji ve Standartlar:** `I1` (Code smell adlandırması ve tanım tutarsızlığı)[4].
2. **Code Smell Tespiti ve Algı:** `I2` (Tespit yaklaşımları), `I3` (Endüstri algısı), `I4` (Geliştirici katılımı)[4][5].
3. **Yazılım Kalitesi, Mimari ve İzleme:** `I5` (Kokuların kaliteye etkisi), `I8` (Refactoring'in kaliteye etkisi), `I10` (Refactoring takibi), `I11` (Mimari vs. bağlamsal refactoring)[5].
4. **Araç Desteği ve Otomasyon:** `I6` (Code smell tespit araçları), `I9` (Refactoring araçları ve otomasyon)[5][7].
5. **Geliştirici Davranışı ve İnsan Faktörü:** `I7` (Geliştiricilerin refactoring bilgisi ve zihinsel modelleri)[6].
6. **Eğitim ve Müfredat:** `I12` (Code smell ve refactoring öğretimi)[8].
7. **Araştırma Metodolojisi ve Veri Setleri:** `I13` (Metodolojik boşluklar, veri seti tutarsızlıkları, mihenk taşı eksikliği)[8].

---

### 3\. Doğrudan Nesneye Dayalı Programlama (OOP) İlkeleriyle İlişkili Problemler

Belirlenen açık problemlerden bazıları dogrudan Nesneye Dayalı Programlama (Object-Oriented Programming - OOP) ilkeleriyle (Soyutlama, Kapsülleme, Kalıtım, Çok Biçimlilik, Yüksek Birleşim / Düşük Bağımlılık ve Tek Sorumluluk İlkesi - SRP) ilişkilidir[66]:

* **I1 ve I2 (Terminoloji ve Code Smell Tespiti):** En yaygın koku türleri (*Blob/God Class, Feature Envy, Refused Bequest, Divergent Change, Shotgun Surgery*) doğrudan OOP ilkelerinin ihlalidir[94]. Örneğin *God Class* Tek Sorumluluk İlkesini (SRP) ve Birleşimi (*Cohesion*) ihlal ederken; *Feature Envy* Kapsüllemeyi (*Encapsulation*) ve sınıflar arası bağımlılığı (*Coupling*) olumsuz etkiler[67].
* **I8 (Refactoring ve Kalite Etkisi):** *Extract Class, Extract Subclass, Move Method, Replace Conditional with Polymorphism* gibi refactoring teknikleri doğrudan OOP yapılarının (sınıf, metot, kalıtım hiyerarşisi, arayüz) yeniden düzenlenmesini sağlar[66]. Bu dönüşümlerin içsel OOP kalitesine (birleşim, bağımlılık, kalıtım derinliği) etkileri bu problemin merkezindedir[66].
* **I11 (Mimari vs. Bağlamsal Refactoring):** OOP'de bağlamsal refactoring sınıf ve metot düzeyindeki nesne sorumluluklarını düzenlerken; mimari refactoring paket ve alt sistemler arasındaki bağımlılık tersine çevirme (*dependency inversion*) ve modülerlik sınırlarını belirler[78].

---

### 4\. Makalede Doğrudan Belirtilen Çözümler ile Analitik Çıkarımların Ayrılması

* **Makalede Doğrudan Belirtilen Çözüm / Yönelimler:**
  * Code smells için "Design Patterns" kataloğuna benzer tekil bir standart taksonomi ve katalog oluşturulması[11][25].
  * Tespit araçlarının çoklu dil desteğine (özellikle JavaScript) kavuşturulması ve code smell tespiti ile otomatik refactoring uygulamasının tek araçta birleştirilmesi[14].
  * Açık kaynak kodlu Java projelerine bağımlılığı azaltmak için endüstriyel projeleri de içeren ortak mihenk taşı (*benchmark*) veri setlerinin kurulması[19].
  * Sınıflarda *Coding Dojo* gibi pratik yöntemlerin kullanılması[19][82].
* **Analitik Çıkarımlar / Yorumlar:**
  * Literatürdeki temel ikilem, refactoring'in doğası gereği kaliteyi artırma amacı taşımasına rağmen, pratikte bir kalite niteliğini iyileştirirken diğerine zarar verebilmesidir (ör. birleşimi artırmak için sınıfı bölmenin bağımlılığı yükseltmesi)[60][66].
  * Otomasyon kısıtlarının temel nedeni, kodun dışsal davranışının korunduğunu (*behavior preservation*) statik analizle %100 garanti etmenin teknik zorluğudur[100][101].

---

### 5\. Akademik İnceleme Raporunda Eleştirel Tartışmaya En Uygun 4 Temel Problem

Akademik bir makale inceleme raporunda metodolojik derinlik, teorik çelişki ve endüstriyel etki bakımından eleştirel olarak tartışılmaya en uygun **4 problem** seçilmiş ve gerekçeleri aşağıda açıklanmıştır:

1. **I1 (Code Smell Naming / Terminology Standardization):**
  * *Neden Eleştirel Tartışmaya Uygundur?:* Bilimsel bir disiplinde standart bir terminolojinin olmaması, araştırmaların birbiriyle karşılaştırılmasını ve sentezlenmesini olanaksız kılar[22][23]. Aynı kavrama farklı isimler verilmesi literatürde bilgi kirliliğine ve araçlar arasında çelişkili sonuçlara yol açmaktadır[21][31].
2. **I5 ve I8 (Quality Impact Paradox / Kalite Etkisi İkilemi):**
  * *Neden Eleştirel Tartışmaya Uygundur?:* Refactoring yapılmasının ana gerekçesi kaliteyi artırmaktır[102][103]. Ancak makale, refactoring'in her zaman tüm kalite kriterlerini iyileştirmediğini, hatta bazen kaliteyi düşürdüğünü ve 14 temel refactoring tekniğinin kaliteye etkisinin hiç araştırılmadığını göstermektedir[60][61]. Bu durum refactoring araştırmalarındaki temel bir teorik boşluğu temsil eder.
3. **I9 (Refactoring Tools &amp; Automation Gap / Araç Otomasyonu Kopukluğu):**
  * *Neden Eleştirel Tartışmaya Uygundur?:* Literatürde yüzlerce code smell tespit aracı varken, code smell tespit edildiğinde buna uygun refactoring dönüşümünü otomatikleştiren araç sayısı yok denecek kadar azdır (Table 8)[34][72]. Tespit ile uygulama arasındaki bu kopukluk akademinin endüstriye pratik araç sunmadaki yetersizliğini gösterir.
4. **I13 (Research Gaps, Lack of Benchmarks &amp; FLOSS Bias / Metodolojik Yanlılık):**
  * *Neden Eleştirel Tartışmaya Uygundur?:* Makaledeki en çarpıcı metodolojik bulgu, ikincil araştırmaların %57'sinin açık kaynak kodlu (FLOSS) projeler ve ezici çoğunlukla Java dili üzerine inşa edilmiş olmasıdır[57][86]. Standart mihenk taşlarının olmaması ve endüstriyel doğrulamaların yetersizliği, akademik bulguların dışsal geçerliliğini (*external validity*) ciddi biçimde sorgulanabilir kılmaktadır[87][90].
