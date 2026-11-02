# Özgün Makale Kanıt Özeti

Kaynak: Lacerda vd. (2020). Bölüm, tablo ve şekil numaraları arXiv v1 tam metnine göredir.

## Araştırma tasarımı

- Bölüm 3, Kitchenham vd. yönergelerine dayanan beş adımlı üçüncül SLR sürecini açıklar: amaç/RQ, ilgili literatürü belirleme, seçim ölçütleri, kalite değerlendirmesi ve veri çıkarımı.
- Sekiz kaynak kullanılmıştır: ACM DL, IEEE Xplore, ScienceDirect, Wiley, Scopus, AIS eLibrary, Google Scholar ve Springer (Tablo 5).
- Seçim akışı Bölüm 3.6 ve Şekil 3'te 467 bulunan kayıt, 59 ilk seçim, 6 tekrar + 20 ölçüt dışı kayıt çıkarıldıktan sonra 33 çalışma ve snowballing ile eklenen 7 çalışma sonucu 40 nihai çalışma olarak verilir.
- Kapsam 1992–2018'dir; 1992 Opdyke'ın doktora tezinin tarihidir. Seçilen ilk ikincil çalışma ise 2004'te yayımlanmıştır.
- Seçilen 40 çalışma tema olarak 13 refactoring, 25 smell ve her ikisini birlikte ele alan 2 çalışma biçiminde sınıflanmıştır (Bölüm 3.6/Şekil 5).

## RQ1–RQ5

- **RQ1:** İkincil çalışmalarda hangi refactoring konuları araştırılmıştır? Bölüm 4.1, refactoring temasına ayrılan 13 çalışmayı listeler.
- **RQ2:** İkincil çalışmalarda hangi smell konuları araştırılmıştır? Bölüm 4.2'deki liste 27 S-kodu içerir; bunun tema dağılımındaki 25 ile aynı evren olmadığı unutulmamalıdır. S29 ve S36 iki temada da geçtiğinden bu liste birbirini dışlayan sınıf sayımı değildir.
- **RQ3:** Smell tespiti ve refactoring desteği için hangi araçlardan söz edilmiştir? Bölüm 4.3, 19 çalışmada 162'den fazla farklı smell aracı ve 13 çalışmada 24 refactoring aracı bildirir.
- **RQ4:** Toplam 181 RQ (ortalama 4,5) vardır. Tablo 10'da Description and Classification 90/181 RQ ile en büyük havuz payına sahiptir. CCI ve Design türlerinde RQ yoktur.
- **RQ5:** 40 çalışmanın 26'sı SLR (%65), 7'si SM (%17,5), 7'si survey'dir (%17,5). S16 ayrıca multivocal olarak nitelenmiştir; bu 41. çalışma değildir.

## Dil ve araç yüzdeleri

Bölüm 4.3.1, platform/dil anan 35 çalışmanın Java'yı en çok kullanılan teknoloji olarak sunduğunu belirtir. Ardından gelen C++ ve C# oranları sırasıyla %57,14 ve %42,85'tir. Bu cümledeki oranları Java'ya bağlamak yanlıştır. CCFinder ve PMD, araç bildiren 19 çalışmanın %47,36'sında; inCode %42,10, DECOR/DETEX ve inFusion %36,84 oranında geçer.

## Tablo 10'un doğru okunması

Tablo iki farklı payda verir: `# of studies` sütunundaki yüzdeler 40 çalışma, `# RQs in the pool` sütunundaki yüzdeler 181 RQ üzerindendir. Bir çalışma farklı alt kategorilerde RQ'lara sahip olabileceği için çalışma yüzdeleri birbirini dışlayan parçalar değildir ve toplamlarının %100 olması beklenmez.

## QMOOD yorumu

Bölüm 5.2 ve Şekil 24, yalnızca seçilen ikincil çalışmalarda bulunan içsel nitelikleri QMOOD ilişkileriyle dışsal niteliklere yeniden dağıtır. Yazarların sonucu, bu yeniden gruplamada refactoring'in anlaşılabilirlik, işlevsellik, yeniden kullanılabilirlik ve bakım yapılabilirlik üzerinde smell'lerden daha fazla ilişki/etki gösterdiğidir. Bu, kontrollü deneylerden türetilmiş nedensel ve evrensel bir etki büyüklüğü değildir. Yazarlar kapsamlı ve yeterli kanıt bulunmadığını, bağlama göre refactoring'in yeni smell'lere de yol açabileceğini söyler.

## I1–I13 (Tablo 14)

1. I1 — Code smell naming
2. I2 — Approaches to code smell detection
3. I3 — Code smell and industry perception
4. I4 — Developers and code smell detection process
5. I5 — Code smell and impact on quality attributes
6. I6 — Code smell tools
7. I7 — Developer's refactoring knowledge
8. I8 — Refactoring and impact on quality attributes
9. I9 — Refactoring tools
10. I10 — Refactoring tracking
11. I11 — Architectural refactoring versus contextual refactoring
12. I12 — Teaching code smell and refactoring
13. I13 — Research gaps on code smell and refactoring

I1–I6 smell, I7–I11 refactoring, I12–I13 ise her iki konu altında sınıflandırılır. Tablo 14 kısa gözlemler sunar; ön analizlerdeki uzun “önerilen çözüm” paragraflarının tamamı doğrudan tablo içeriği sayılmamalıdır.
