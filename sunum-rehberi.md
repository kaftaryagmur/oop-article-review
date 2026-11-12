# Makale incelemesi sunum rehberi

Yaklaşık beş dakikalık anlatım, [inceleme raporunun](rapor.md) yöntemini, sayısal doğrulamasını ve nesneye dayalı tasarım değerlendirmesini izler.

## Anlatım akışı

**0.00–0.40 | Araştırma problemi.** Bir sınıfın büyük olması, sorumluluklarının dağınık olabileceğini düşündürür. Bu belirtiyi hangi ölçütlerle doğrulayabiliriz ve bir dönüşümün bakımı kolaylaştırdığını nasıl ölçebiliriz? Lacerda vd. bu iki sorunun arkasındaki *code smell* ve *refactoring* araştırmalarını birlikte inceliyor. [Rapor, §1–2](rapor.md#1-giriş)

**0.40–1.25 | Yöntem.** Yazarlar doğrudan yazılım projeleri üzerinde yeni bir deney yürütmek yerine önceki derlemeleri ve sistematik haritalamaları inceliyor. İlk aramada 467 kayıt bulunuyor. İlk elemeyi geçen 59 kayıttan altı tekrar ve 20 ölçüt dışı çalışma çıkarılıyor. Kaynakça taramasından gelen yedi ek çalışmayla örneklem 40 ikincil çalışmaya ulaşıyor. [Rapor, §3](rapor.md#3-araştırma-yöntemi)

**1.25–2.20 | Sayısal doğrulama.** Tablo 10 araştırma sorularını sınıflandırıyor. Satırlar 185 ederken toplam 181 olarak verilmiş. Ek veride 181 soru bulunuyor. Fark, *Causality* satırında ortaya çıkıyor. Makalede 14 yazıyor, ek veri 10 gösteriyor. Bu örnek, bir tablonun toplamını ve dayandığı veri dosyasını birlikte kontrol etmenin neden önemli olduğunu gösteriyor. [Rapor, §4.4](rapor.md#44-rq4--araştırma-sorularının-yapısı) · [Yazarların ek verisi](https://doi.org/10.17632/72fvy4r3gj.2)

**2.20–3.40 | OOP örneği.** Varsayımsal bir sipariş sınıfı hem durum geçişlerini hem fiyatlandırmayı yönetiyor. İndirim kuralları bağımsız değişiyorsa hesaplamayı ayrı bir sınıfa taşımak yeni bir indirim kuralının nerede uygulanacağını belirginleştirir. Hesaplama siparişin iç durumuna sık erişiyorsa ayrım bağımlılığı artırabilir. Regresyon testlerinde toplam tutarı, hata davranışını ve sipariş durumunu karşılaştırırım. [Rapor, §5.5](rapor.md#55-sipariş-sınıfında-extract-class-kararı)

**3.40–5.00 | Eleştiri ve öneri.** QMOOD eşleştirmesi, literatürde hangi kalite niteliklerinin hangi dönüşümlerle ilişkilendirildiğini gösteriyor. Bir sınıfa daha sık müdahale edilmesi ve tek bir bakım görevinin daha uzun sürmesi farklı çıktılar. Önerim, aynı sipariş sisteminin iki kopyasında yeni bir indirim kuralı ekleme görevini karşılaştırmak. Dönüşümü bir kopyaya uygular, görevin doğru tamamlanma süresini ve dönüşüm maliyetini ayrı kaydederim. [Rapor, §6.4 ve §8](rapor.md#8-geliştirme-ve-gelecek-çalışma-önerileri)

## Olası sorular

**Üçüncül inceleme neden tercih edilmiş?** Yazarlar, ayrı ayrı gelişen iki literatür alanını derlemeler düzeyinde bir araya getiriyor. Aynı birincil araştırma birkaç derlemede tekrar edebildiği için derleme sayısı bağımsız kanıt sayısını doğrudan vermez. [Rapor, §3 ve §7.2](rapor.md#72-üçüncül-incelemenin-kanıt-sınırları)

**En sık anılan araç en başarılı araç sayılır mı?** Anılma sayısı, aracın incelenen literatürdeki görünürlüğünü ölçer. Başarı karşılaştırması için ortak veri, tespit ölçütleri ve değerlendirme koşulları gerekir. Örneğin DECOR/DETEX 19 çalışmanın sekizinde anılıyor. Bu oran makaledeki Şekil 13 ve ek veriyle doğrulanıyor. [Rapor, §4.3](rapor.md#43-rq3--diller-ve-araçlar)

**QMOOD'dan hangi sonuç çıkarılabilir?** Eşleştirme, incelenen çalışmaların hangi kalite niteliklerini ele aldığını gösterir. Belirli bir projede refactoring’in etkisinin büyüklüğü, yönü ve dönüşüm maliyeti için doğrudan ölçüm gerekir. [Rapor, §4.6 ve §7.4](rapor.md#46-kalite-ve-qmood)

**Örnekte refactoring'in başarılı olduğunu nasıl anlarsın?** İlk ölçüt, test edilen davranışların korunmasıdır. Ardından yeni indirim kuralının doğru tamamlanma süresini, dönüşümün maliyetini ve bağımlılıktaki değişimi değerlendiririm. Tek bir görevden elde edilen bulgunun kapsamı o görev ve kod tabanıyla sınırlıdır. [Rapor, §8](rapor.md#8-geliştirme-ve-gelecek-çalışma-önerileri)
