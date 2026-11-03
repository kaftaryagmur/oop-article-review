# Kod Kokuları ve Refactoring Makale İncelemesi

Bu depo, Nesneye Dayalı Programlama Dilleri dersi kapsamında kod kokuları (*code smells*) ve yeniden yapılandırma (*refactoring*) arasındaki ilişkiyi inceleyen akademik raporu içerir.

İncelemenin merkezinde Lacerda ve arkadaşlarının 2020 yılında yayımlanan “Code Smells and Refactoring: A Tertiary Systematic Review of Challenges and Observations” başlıklı çalışması bulunmaktadır. Makale, kod kokuları ve refactoring alanındaki 40 ikincil araştırmayı bir araya getiren üçüncül bir sistematik literatür incelemesidir.

## Ana makale

Guilherme Lacerda, Fabio Petrillo, Marcelo Pimenta ve Yann-Gaël Guéhéneuc. “Code Smells and Refactoring: A Tertiary Systematic Review of Challenges and Observations.” *Journal of Systems and Software*, 167, 110610, 2020.

- DOI: https://doi.org/10.1016/j.jss.2020.110610
- Açık ön baskı: https://arxiv.org/abs/2004.10777

## İnceleme kapsamı

Rapor aşağıdaki konuları ele almaktadır:

- Makalenin amacı, araştırma soruları ve üçüncül inceleme yöntemi
- Kod kokuları ve refactoring üzerine araştırma eğilimleri
- Koku tespit ve refactoring araçları
- Programlama dili ve araç dağılımlarının değerlendirilmesi
- Tablo 10'daki araştırma sorusu sınıflandırması
- QMOOD modeli üzerinden yazılım kalitesi ilişkisi
- I1–I13 açık araştırma sorunları
- Kod kokuları ve refactoring'in nesneye dayalı programlama ilkeleriyle ilişkisi
- Alanın Opdyke, Brown, Fowler, Mens ve Tourwé gibi temel çalışmalar üzerinden tarihsel gelişimi
- Makalenin yöntemsel güçlü yönleri, sınırlılıkları ve gelecekteki araştırma olanakları

## Depo yapısı

```text
oop-article-review/
├── README.md
├── rapor.md
├── PROJECT_CONTEXT.md
├── references/
│   └── references.md
├── research-notes/
│   ├── README.md
│   ├── paper-evidence.md
│   ├── verification-log.md
│   └── source-analyses/
├── figures/
└── final/
```

`rapor.md`, akademik incelemenin ana metnidir. `references/` kullanılan kaynakların doğrulanmış künyelerini içerir. `research-notes/` altında özgün makaleden çıkarılan kanıtlar, iddia doğrulamaları ve kaynak analizleri yer alır. `figures/` raporda kullanılabilecek görseller, `final/` ise son teslim çıktıları için ayrılmıştır.

## Akademik yaklaşım

Araştırma notlarındaki sayısal ve yorumlayıcı iddialar özgün makalenin ilgili bölüm, tablo ve şekilleriyle karşılaştırılmıştır. Makalenin doğrudan bulguları ile raporun eleştirel yorumları ayrı tutulmuş; özellikle çalışma sayıları, araç ve programlama dili yüzdeleri, Tablo 10 ve QMOOD yorumunda bağlam ve payda farklılıkları gözetilmiştir.

Rapor, kod kokularını yalnızca kaynak koddaki sorun işaretleri olarak değil; sınıf sorumluluğu, kohezyon, bağımlılık, kapsülleme, kalıtım ve çok biçimlilik gibi nesneye dayalı tasarım kavramlarıyla ilişkili bakım belirtileri olarak değerlendirmektedir. Refactoring ise otomatik ve her durumda yararlı bir işlem olarak değil, davranış koruma ve kalite ödünleşimleri çerçevesinde ele alınmaktadır.
