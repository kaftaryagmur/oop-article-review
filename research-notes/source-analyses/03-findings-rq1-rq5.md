Lacerda ve arkadaşlarının (2020) **"Code smells and refactoring: A tertiary systematic review of challenges and observations"** başlıklı makalesinde sunulan araştırma bulguları, yazarların belirlediği **5 Araştırma Sorusu (RQ1–RQ5)** çerçevesinde yapılandırılmış araştırma notları olarak aşağıda analiz edilmiştir[1].

---

### 1\. RQ1: Refactoring Konuları ve Teknikleri

1. **Özgün İngilizce İfade:**
  * *"RQ1: What refactoring-related topics have been investigated in secondary studies?"*[2][4]
2. **Sorunun Amacı (Türkçe):**
  * İkincil çalışmalarda yeniden yapılandırma (*refactoring*) ile ilgili hangi konuların araştırıldığını ve hangi alanların eksik kaldığını belirleyerek yeni ikincil çalışma ihtiyaçlarını tespit etmek[4][5].
3. **Kullanılan Veri veya Analiz Yaklaşımı:**
  * Doğrudan refactoring konusuna odaklanan 13 ikincil çalışma [S3, S5, S6, S7, S10, S14, S17, S21, S22, S25, S27, S29, S36] ve hem kod kokuları (*code smells*) hem de refactoring konusunu birlikte ele alan 2 çalışma [S4, S13] analiz edilmiş[6][7]; konular *Card Sorting* (Kart Sıralama) tekniğiyle temalara ayrılmıştır[8].
4. **Elde Edilen Temel Bulgular ve Sayısal Sonuçlar:**
  * **En Çok İncelenen Konular:** Refactoring fırsatlarının belirlenmesi (*refactoring opportunities*) 32 çalışmada, refactoring tekniklerinin uygulanması (*application of refactoring techniques*) 14 çalışmada, destek araçları (*support tools*) 10 çalışmada ele alınmıştır [130, Şekil 6].
  * **En Çok İncelenen Refactoring Teknikleri:** Çıkarma teknikleri (*Extraction techniques*) en ön sıradadır[9]. *Extract (method, variable...)* 9 çalışma [101, Şekil 7]; *Pull Up (field...)* 8 çalışma, *Rename (method, variable...)* 8 çalışma, *Remove (parameter...)* 8 çalışma, *Replace (conditional...)* 8 çalışma, *Push Down (field...)* 7 çalışma, *Move (field, method...)* 7 çalışma, *Inline (method...)* 6 çalışma tarafından incelenmiştir [101, Şekil 7].
  * **Fırsat Tespiti Yaklaşımları:** En yaygın yöntemler kalite metriği odaklı (*quality metrics-oriented*), ön-koşul odaklı (*pre-condition-oriented*) ve kümeleme odaklı (*clustering-oriented*) yaklaşımlardır[10][11].
  * **Kaliteye Etkisi:** Refactoring her zaman tüm kalite yönlerini iyileştirmez[12]. Örneğin *Extract Class*, birleşimi (*cohesion*) artırabilirken karmaşıklık (*complexity*) ve bağımlılığı (*coupling*) olumsuz etkileyebilir[13].
  * **Teknik Borç:** Refactoring, teknik borcun (*technical debt*) olumsuz etkilerini azaltmada temel stratejidir[14][15].
5. **Dayandığı Tablo, Şekil ve Bölüm Numaraları:**
  * Bölüm 4.1 (Section 4.1.1–4.1.4), Tablo 8, Şekil 5, Şekil 6, Şekil 7[6].
6. **Yazarların Ulaştığı Sonuç:**
  * Akademik araştırmalar ile endüstriyel uygulama arasında boşluk (*gap*) bulunmaktadır[17]. Akademisyenler *Extract Class* ve *Extract Method* gibi karmaşık dönüşümlere odaklanırken, geliştiricilerin günlük işte en çok başvurduğu *Rename Method, Inline Temp, Add Parameter* gibi pratik işlemler akademide ihmal edilmiştir[17].
7. **Bulguların Sınırları ve Belirsizlikleri:**
  * Kod kokusu ile refactoring arasındaki ilişki birebir (*one-to-one*) değildir[17][20].
  * Literatürde tanımlı 72 refactoring tekniğinden yalnızca 20 ila 27 adedi ikincil çalışmalarda detaylandırılmıştır[11][21].
  * Refactoring otomasyonunda kodun dış davranışının korunduğunu (*behavior preservation*) garanti etmek son derece zordur[22][23].

---

### 2\. RQ2: Kod ve Tasarım Kokusu Konuları ve Yöntemleri

1. **Özgün İngilizce İfade:**
  * *"RQ2: What smells-related topics have been investigated in secondary studies?"*[3][4]
2. **Sorunun Amacı (Türkçe):**
  * İkincil çalışmalarda kod kokuları (*code smells*) ve tasarım kokuları (*design smells*) ile ilgili araştırılan konuları, tespit yöntemlerini ve eksik kalan alanları belirlemek[4][5].
3. **Kullanılan Veri veya Analiz Yaklaşımı:**
  * Kokulara odaklanan 25 ikincil çalışma [S1, S2, S8, S9, S11, S12, S15, S16, S18, S19, S20, S23, S24, S26, S28, S29, S30, S31, S32, S33, S34, S35, S36, S37, S38, S39, S40] ve her iki alanı kapsayan 2 ikincil çalışma [S4, S13] analiz edilmiştir[6][24].
4. **Elde Edilen Temel Bulgular ve Sayısal Sonuçlar:**
  * **Tasarım Kokuları (14 Çalışma):** En çok bahsedilen top-5 tasarım kokusu: *Blob* (8 çalışma), *Swiss Army Knife* (6 çalışma), *Functional Decomposition* (5 çalışma), *Spaghetti Code* (5 çalışma), *Lava Flow* (2 çalışma) [153, Şekil 8].
  * **Kod Kokuları (28 Çalışma):** En çok bahsedilen top-10 kod kokusu: *Duplicated Code/Clones* (25 çalışma — 7'si doğrudan klon odaklıdır), *Large Class/God Class* (18 çalışma), *Feature Envy* (18 çalışma), *Long Method* (16 çalışma), *Long Parameter List* (15 çalışma), *Data Clumps* (14 çalışma), *Refused Bequest* (14 çalışma), *Divergent Change* (13 çalışma), *Shotgun Surgery* (13 çalışma), *Lazy Class* (11 çalışma) [157, 158, Şekil 9].
  * **Teknik Borç:** *God Class/Large Class* teknik borç bağlamında en çok araştırılan kokudur; bu kokuya sahip sınıfların hatalara (*defects*) 13 kat daha yatkın ve değişime (*change-prone*) 7 kat daha meyilli olduğu bildirilmiştir[25].
  * **Tespit Yaklaşımları:** Metrik tabanlı (*metrics-based*) yaklaşım 28 çalışmada, kural/strateji tabanlı (*detection strategies/rules*) yaklaşım 26 çalışmada, insan algısı (*human perception*) 14 çalışmada, görselleştirme (*visualization*) 10 çalışmada, olasılıksal/arama tabanlı (*probabilistic/search-based*) yaklaşım 5 çalışmada ele alınmıştır [166, 170, 172, Şekil 11].
  * **Birlikte Görülme (** **Co-occurrence** **):** *God Class/Large Class, Long Method, Feature Envy* ve *Duplicated Code/Clones* sıklıkla birlikte ortaya çıkmaktadır [162, Şekil 10].
5. **Dayandığı Tablo, Şekil ve Bölüm Numaraları:**
  * Bölüm 4.2 (Section 4.2.1–4.2.4), Tablo 8, Şekil 8, Şekil 9, Şekil 10, Şekil 11[16].
6. **Yazarların Ulaştığı Sonuç:**
  * Literatürde ciddi bir adlandırma ve tanım karmaşası (*nomenclature problem*) bulunmaktadır[29]. Farklı araştırmacılar aynı problem için farklı isimler kullanmakta veya aynı isme farklı anlamlar yüklemektedir[29][30].
  * Tasarım Düzenleri (*Design Patterns*) kataloğu mantığında tekil bir koku kataloğu standartlaştırılmalıdır[32].
7. **Bulguların Sınırları ve Belirsizlikleri:**
  * *Alternative Classes with Different Interfaces, Incomplete Class Library, Primitive Obsession, Inappropriate Intimacy* ve *Comments* kokularının araştırmacılar tarafından neden ihmal edildiği literatürde açıklanmamıştır[33][34].
  * Tespit araçlarının kullandığı eşik değerlerinde (*thresholds*) standart bulunmadığından farklı tespit araçları aynı kod tabanı için son derece çelişkili sonuçlar üretmektedir[35].

---

### 3\. RQ3: Kod Kokusu Tespiti ve Refactoring Destek Araçları

1. **Özgün İngilizce İfade:**
  * *"RQ3: Which tools have been mentioned for code-smell detection and refactoring support?"*[3]
2. **Sorunun Amacı (Türkçe):**
  * Kod kokusu tespiti ve refactoring desteği sağlanan yazılım araçlarını, desteklenen programlama dillerini ve araçların metodolojik özelliklerini incelemek[5][39].
3. **Kullanılan Veri veya Analiz Yaklaşımı:**
  * Koku tespiti araçlarından bahseden 19 ikincil çalışma [S1, S2, S9, S12, S13, S17, S18, S19, S20, S26, S27, S30, S31, S33, S34, S35, S38, S39, S40] ve refactoring araçlarından bahseden 13 ikincil çalışma [S1, S2, S4, S9, S12, S13, S14, S17, S18, S29, S34, S39, S40] analiz edilmiştir[40][41].
4. **Elde Edilen Temel Bulgular ve Sayısal Sonuçlar:**
  * **Programlama Dilleri:** Araç araştırmalarının %57.14'ünde (35 çalışma) Java hedeflenmiştir [190, Şekil 12]. C++ (%42.85 - 20 çalışma) ve C# (15 çalışma) takip eden dillerdir [190, Şekil 12].
  * **Koku Tespit Araçları (162+ Farklı Araç):** En çok bahsedilen top-5 koku tespit aracı: *CCFinder* (%47.36 — 9 çalışma) ve *PMD* (%47.36 — 9 çalışma), *inCode* (%42.10 — 8 çalışma) ve *DECOR/DETEX* (%42.10 — 8 çalışma), *inFusion* (%36.84 — 7 çalışma) [193, Şekil 13].
  * **Refactoring Araçları (24 Farklı Araç):** En çok bahsedilen top-5 refactoring aracı: *JDeodorant* (%71.42 — 10 çalışma), *TrueRefactor* (%21.42 — 3 çalışma), *Eclipse Refactoring* (%14.28 — 2 çalışma), *IntelliJ IDEA Refactoring* (%14.28 — 2 çalışma), *Wrangler* (%7.14 — 1 çalışma) [209, Şekil 14].
  * **Doğruluk Oranı Raporlaması:** Koku tespit araçlarının yalnızca yaklaşık %30'u doğruluk (*accuracy / precision and recall*) verilerini açıkça paylaşmaktadır[42].
  * **Kapsam:** Araçlar ortalama olarak yalnızca 3 ila 4 koku türünü tespit edebilmektedir[43][44]. Fowler'ın 22 kokusunun tamamını kapsadığını belirten tek araç ticari bir araç olan *inFusion*'dur[43].
5. **Dayandığı Tablo, Şekil ve Bölüm Numaraları:**
  * Bölüm 4.3 (Section 4.3.1–4.3.4), Tablo 8, Tablo 9, Şekil 12, Şekil 13, Şekil 14[16].
6. **Yazarların Ulaştığı Sonuç:**
  * Akademik araçlar ezici çoğunlukla Java odaklıdır; endüstrinin lider dillerinden JavaScript ihmal edilmiştir[40].
  * Koku tespitini doğrudan otomatik refactoring önerisine ve dönüştürme uygulamasına bağlayan olgun araç sayısı oldukça azdır (*JDeodorant* bu konudaki ana istisnadır)[41].
7. **Bulguların Sınırları ve Belirsizlikleri:**
  * Araç sonuçlarını nesnel biçimde karşılaştıracak standart mihenk taşı (*standard benchmark systems*) veri setleri bulunmamaktadır[52][53].
  * Araçların çoğu olgunluktan yoksundur, kullanılabilirlik (*usability*) ve görselleştirme filtreleri yetersizdir[49][54].

---

### 4\. RQ4: İkincil Çalışmaların Araştırma Soruları ve Atıf Analizi

1. **Özgün İngilizce İfade:**
  * *"RQ4: Which RQs have been studied on code smells and refactoring? What are the highest cited secondary studies?"*[3]
2. **Sorunun Amacı (Türkçe):**
  * İkincil çalışmalarda tanımlanan araştırma sorularının (RQ) yapısını ve türlerini Easterbrook taksonomisine göre analiz etmek ve en yüksek atıf alan ikincil araştırmaları belirlemek[55][56].
3. **Kullanılan Veri veya Analiz Yaklaşımı:**
  * 40 ikincil çalışmada açıkça tanımlanmış toplam 181 Araştırma Sorusu (RQ), Easterbrook et al. (2008) taksonomisine göre kategorize edilmiştir [235, 236, Tablo 10]. Atıf verileri Google Scholar üzerinden toplanmıştır[57][58].
4. **Elde Edilen Temel Bulgular ve Sayısal Sonuçlar:**
  * **Toplam RQ Sayısı:** 40 çalışmada 181 RQ (ortalama 4.5 RQ/çalışma)[59]. S40 çalışması 13 RQ ile en kapsamlı çalışmadır[59]. S28 ve S30 çalışmalarında yalnızca 1 RQ bulunurken, bazı çalışmalarda (örn. S4, S18) soru cümleleri açıkça yapılandırılmamıştır[59][60].
  * **Easterbrook Taksonomisi Dağılımı:**
    * *Description and Classification (DC) [Betimsel ve Sınıflandırma]:* 90 RQ (%49.72 — 30 çalışmada [%75]) [239, Tablo 10].
    * *Frequency Distribution (FD) [Sıklık Dağılımı]:* 19 RQ (%10.49 — 11 çalışmada [%27.5]) [240, Tablo 10].
    * *Existence (E) [Varlık/Var Olma]:* 16 RQ (%8.83 — 13 çalışmada [%32.5]) [238, Tablo 10].
    * *Descriptive-Process (DP) [Betimsel Süreç]:* 16 RQ (%8.83 — 10 çalışmada [%25]) [241, Tablo 10].
    * *Causality (C) [Nedensellik]:* 14 RQ (%7.73 — 9 çalışmada [%22.5]) [242, Tablo 10].
    * *Relationship (R) [İlişki/Korelasyon]:* 13 RQ (%7.18 — 12 çalışmada [%30]) [241, Tablo 10].
    * *Description-Comparative (DCO) [Betimsel Karşılaştırma]:* 11 RQ (%6.07 — 7 çalışmada [%17.5]) [240, Tablo 10].
    * *Causality-Comparative (CC) [Nedensel Karşılaştırma]:* 6 RQ (%3.31 — 5 çalışmada [%12.5]) [243, Tablo 10].
    * *Causality-Comparative Interaction (CCI)* ve *Design (D)* kategorilerinde **0 RQ (%0.0)** tespit edilmiştir [244, Tablo 10].
    * Toplam Keşifsel ve Temel Oran (*Exploratory &amp; Base-Rate*) soruları: 152 RQ (%83.97)[61].
  * **Atıf Analizi (Toplam 2.568 Atıf, Ortalama 64.2, Medyan = 9)**[62]**:**
    * *En Çok Atıf Alan Çalışmalar (Toplam Google Scholar Atıfı):* Mens &amp; Tourwé (2004) [S10]: 1301 atıf; Koschke (2007) [S30]: 277 atıf; Rattan et al. (2013) [S20]: 216 atıf; Li et al. (2015) [S26]: 208 atıf; Zhang et al. (2011) [S11]: 113 atıf [257, Tablo 12].
    * *En Çok Atıf Alan Çalışmalar (Yıllık Ortalama Atıf):* Mens &amp; Tourwé (2004) [S10]: 86.72 atıf/yıl; Li et al. (2015) [S26]: 52.00 atıf/yıl; Laguna &amp; Crespo (2013) [S14]: 42.50 atıf/yıl; Rattan et al. (2013) [S20]: 36.00 atıf/yıl; Alves et al. (2016) [S23]: 27.00 atıf/yıl [258, Tablo 13].
5. **Dayandığı Tablo, Şekil ve Bölüm Numaraları:**
  * Bölüm 4.4 (Section 4.4.1–4.4.2), Tablo 10, Tablo 11, Tablo 12, Tablo 13[56].
6. **Yazarların Ulaştığı Sonuç:**
  * İkincil çalışmalarda en çok ilgi gören ve atıf toplayan ana temalar **Kod Klonları (** **Code Clones** **)** ve **Teknik Borçtur (** **Technical Debt** **)**[67][68].
7. **Bulguların Sınırları ve Belirsizlikleri:**
  * Literatürdeki soruların %83'ten fazlası yüzeysel durum tespiti yapan betimsel soruları kapsamaktadır[61]. Farklı koşullar altındaki nedensel etkileşimleri (*Causality-Comparative Interaction*) ve etkili tasarım çözümlerini (*Design*) sorgulayan gelişmiş RQ'lar ikincil çalışmalarda yer almamaktadır[69][70].

---

### 5\. RQ5: Yayın Eğilimleri, Kalite Değerlendirmesi ve Birincil Çalışmalar

1. **Özgün İngilizce İfade:**
  * *"RQ5: What are the annual trends of types, quality, and the number of primary studies reviewed by the secondary studies?"*[3]
2. **Sorunun Amacı (Türkçe):**
  * İkincil çalışmaların yıllara göre yayın dağılımlarını, türlerini, DARE kalite değerlendirme puanlarını, inceledikleri birincil çalışma sayılarını ve deneylerde kullandıkları proje türlerini incelemek[55].
3. **Kullanılan Veri veya Analiz Yaklaşımı:**
  * Seçilen 40 ikincil çalışmanın yayın mecraları (dergi/konferans), Kitchenham/DARE standartlarına dayalı 4 kalite sorusu üzerinden alınan puanlar (0–4 arası) ve inceledikleri birincil araştırma verileri sentezlenmiştir[71].
4. **Elde Edilen Temel Bulgular ve Sayısal Sonuçlar:**
  * **Yıllık Eğilim:** İlk ikincil çalışma 2004 yılında yayımlanmıştır [264, Şekil 15]. İkincil çalışma yayınları 2013 yılından sonra hızlı bir artış göstermiştir (son 3 yılda basılanlar tüm çalışmaların yarısından fazlasını oluşturur) [264, 283, Şekil 15].
  * **İkincil Çalışma Türleri:** Sistematik Literatür İncelemeleri (SLR) 26 çalışma (%65), Sistematik Haritalamalar (SM) 7 çalışma (%17.5), Anketler/Derlemeler (Survey) 7 çalışma (%17.5), Çok Sesli Haritalama (Multivocal Literature Mapping) 1 çalışma (%2.5) [265, Şekil 16]. Yayınların %75'i dergilerde (*journals*), %25'i konferanslarda basılmıştır[74].
  * **Kalite Puanı (** **Quality Score** **):** 0 ile 4 arasında değişen DARE puanlama ölçeğinde seçilen 40 ikincil çalışmanın tamamı 2 ile 4 arası puan almıştır [281, Şekil 21]. Çalışmaların **%80'inden fazlası 3 ile 4 puan arasında** yüksek kaliteye sahiptir[75].
  * **Birincil Çalışma Sayıları:** İkincil çalışmalar toplam 4.573 referansı incelemiştir (ortalama 114.32 referans/çalışma, medyan = 99)[72]. Birincil verileri tarama süresi ortalama 15.2 yıldır[76].
  * **Deney Veri Setleri ve Projeler:** Ampirik doğrulamalarda kullanılan projelerin **%57'si Açık Kaynaklı (FLOSS)**, **%34'ü Endüstriyel**, **%9'u Akademik/Oyuncak (** **Toy** **)** projelerdir [271, Şekil 18]. En çok incelenen açık kaynak projeleri: *Apache, Eclipse, jHotDraw, ArgoUML* ve *GanttProject*'tir [272, Şekil 19].
5. **Dayandığı Tablo, Şekil ve Bölüm Numaraları:**
  * Bölüm 4.5 (Section 4.5.1–4.5.3), Şekil 15, Şekil 16, Şekil 17, Şekil 18, Şekil 19, Şekil 20, Şekil 21[62].
6. **Yazarların Ulaştığı Sonuç:**
  * Yazılım mühendisliği disiplininde SLR metodolojisi olgunlaşmakta ve metodolojik kalite yükselmektedir[71][75]. Ancak ampirik araştırmalar aşırı derecede açık kaynak kodlu (FLOSS) projelere bağımlıdır[79][80].
7. **Bulguların Sınırları ve Belirsizlikleri:**
  * Endüstriyel projelerde yapılan doğrulamalar kısıtlıdır[78][80].
  * Deneylerde endüstri uzmanlarının (*field experts*) katılımıyla yapılan doğrulama ve değerlendirmeler oldukça eksiktir[75][81].
  * Araç ve yöntem performanslarını sınayacak standart mihenk taşı (*benchmark*) proje grupları bulunmamaktadır[82][83].

---

### Makalenin Bütününden Çıkan Sekiz Temel Bulgu

#### 1. Disiplinler Arası Ayrışma

**Temel Bulgu (Observation):** Kod kokuları ile refactoring literatürde çoğunlukla birbirinden izole araştırılmaktadır. **Sayısal Kanıt / Veri:** 40 çalışmanın 25'i kokuya, 13'ü refactoring'e odaklanmış; her ikisini birlikte ele alan çalışma sayısı yalnız 2'dir. **Kaynak Referansı:** Section 3.6, Şekil 5[6][84]

#### 2. Köprü Unsur ve Kalite

**Temel Bulgu (Observation):** Kod kokuları ile refactoring'i bağlayan temel unsur Yazılım Kalitesi ve Teknik Borçtur. QMOOD analizi refactoring'in kaliteye etkisinin kokulardan daha baskın olduğunu gösterir. **Sayısal Kanıt / Veri:** Refactoring uygulamaları 10 farklı kalite niteliğini doğrudan etkilemektedir. **Kaynak Referansı:** Section 5, Şekil 22, Şekil 24[85]

#### 3. Refactoring Teknikleri

**Temel Bulgu (Observation):** Akademik araştırmalar karmaşık dönüşümlere odaklanırken pratikte en sık kullanılan basit refactoring'ler akademide ihmal edilmektedir. **Sayısal Kanıt / Veri:** *Extract Class/Method* en çok incelenen teknikken, tanımlı 72 teknikten sadece 20-27 adedi ikincil çalışmalarda yer bulmuştur. **Kaynak Referansı:** Section 4.1.1, Şekil 7[9]

#### 4. Baskın Kod Kokuları

**Temel Bulgu (Observation):** Tasarım seviyesinde en çok *Blob*, kod seviyesinde ise *Duplicated Code/Clones* ve *Large Class/God Class* incelenmiştir. **Sayısal Kanıt / Veri:** *Duplicated Code* 25 çalışmada, *God Class* 18 çalışmada bahsedilmiştir. *God Class* kusurlara 13 kat daha yatkındır. **Kaynak Referansı:** Section 4.2.1, Section 4.2.2, Şekil 8, Şekil 9[25]

#### 5. Adlandırma &amp; Standart Eksikliği

**Temel Bulgu (Observation):** Terminolojide ciddi tutarsızlıklar (*nomenclature problem*) ve eşik değeri standart yoksunluğu vardır. **Sayısal Kanıt / Veri:** Farklı araçların koku tespit sonuçları arasındaki tutarlılık oranı düşüktür; standart katalog eksiktir. **Kaynak Referansı:** Section 4.2.2, Section 4.2.3[29]

#### 6. Yazılım Araçları ve Diller

**Temel Bulgu (Observation):** Araçlarda baskın bir Java hakimiyeti vardır. Koku tespiti ile otomatik refactoring'i birleştiren araç sayısı çok azdır. **Sayısal Kanıt / Veri:** Çalışmaların %57.14'ü Java odaklıdır. En çok atıf alan tespit aracı *CCFinder* (%47.36), refactoring aracı *JDeodorant*'tır (%71.42). **Kaynak Referansı:** Section 4.3.1–4.3.3, Şekil 12, Şekil 13, Şekil 14[41]

#### 7. Araştırma Sorusu Yapısı

**Temel Bulgu (Observation):** İkincil çalışmalardaki araştırma soruları ezici çoğunlukla betimseldir; karmaşık nedensellik soruları eksiktir. **Sayısal Kanıt / Veri:** 181 RQ'nun %83.97'si keşifsel ve betimseldir. *Causality-Comparative Interaction* ve *Design* türünde 0 soru bulunmaktadır. **Kaynak Referansı:** Section 4.4.1, Tablo 10[61]

#### 8. Veri Seti ve Deney Projeleri

**Temel Bulgu (Observation):** Deneylerde ve doğrulamalarda kullanılan projeler ağırlıklı olarak açık kaynaklı projelerdir; endüstriyel doğrulama azdır. **Sayısal Kanıt / Veri:** Projelerin %57'si FLOSS (Açık Kaynak), %34'ü Endüstriyel, %9'u Akademik/Oyuncak projedir. **Kaynak Referansı:** Section 4.5.2, Şekil 18, Şekil 19[79][91]



