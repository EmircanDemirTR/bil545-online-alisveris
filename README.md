# Online alışverişte satın alma niyeti

> BIL545 · Veri Madenciliğinde İleri Konular · 2026–2027 Güz · Üsküdar Üniversitesi

## Grup

| Üye | Öğrenci no |
|---|---|
| Emircan Demir | 264309006 |

- **Grup ve iletişim sorumlusu** Emircan Demir (tek kişi)
- **Konu** 9.5 · Online alışverişte satın alma niyeti
- **Proje 1 kapsamı** Öğretim üyesiyle görüşüldüğü üzere Bölüm 1 ve Bölüm 2. Bu sürümde Bölüm 1 tamamlandı.

## Soru

Tamamlanmış oturumların gezinme özetleri ve ziyaret bilgileri, mağaza ekibinin dönüşüm analizi için satın almayla biten oturumları ayırmasına ne kadar yardımcı olur?

## Veri

| | |
|---|---|
| Veri kümesi | Online Shoppers Purchasing Intention Dataset |
| Kaynak | [Sakar ve Kastro (2018), UCI](https://doi.org/10.24432/C5F88Q) |
| Lisans | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Ham boyut | 12.330 oturum × 18 sütun (17 öznitelik ve hedef) |
| Hedef | `Revenue`, oturumun satın almayla bitip bitmediği |

Defter `online_shoppers_intention.csv` dosyasını çalışma klasöründe veya bir seviyede yukarıda arar. Dosya bulunmazsa UCI arşivini indirip CSV'yi bellekten okur. İstersen CSV'yi UCI sayfasından indirip Colab'ın **Dosyalar** panelinden yükleyebilirsin.

## Depo yapısı

```text
.
├── README.md
└── proje1/
    └── BIL545_Proje1_EmircanDemir.ipynb
```

## Çalıştırma

1. [Defteri GitHub'dan aç](proje1/BIL545_Proje1_EmircanDemir.ipynb) veya [Colab'da aç](https://colab.research.google.com/github/EmircanDemirTR/bil545-online-alisveris/blob/main/proje1/BIL545_Proje1_EmircanDemir.ipynb). Depo özel olduğu için Colab'da GitHub erişimini etkinleştirmen veya `.ipynb` dosyasını indirip Colab'a yüklemen gerekebilir.
2. Colab'da **Çalışma zamanı → Tümünü çalıştır**. İlk hücre kullanılan Python ve kütüphane sürümlerini yazar. Weka hücresi Maven Central'dan iki JAR dosyası indirir.
3. Yerel çalıştırmada Jupyter ve PATH üzerinde Java gerekir. Kaydedilen çıktılar Python 3.12.10, NumPy 2.5.3, pandas 3.0.6, scikit-learn 1.9.1, Matplotlib 3.11.2 ve Weka 3.8.6 ile üretildi.

## Sonuç özeti

### Proje 1 · Bölüm 1

| 5 × 5 katmanlı çapraz doğrulama | AP (ortalama ± std) |
|---|---:|
| Çoğunluk sınıfı, Dummy | 0,1564 ± 0,0002 |
| Kat içinde ön işleme, lojistik regresyon | 0,2998 ± 0,0183 |
| Tüm veride ön işleme, lojistik regresyon (yanlış kurulum) | 0,2998 ± 0,0185 |
| `PageValues` dahil, lojistik regresyon (sızıntı riski deneyi) | 0,6374 ± 0,0212 |

- Ham veride %15,47 satın alma ve sıfır doğrulanmış eksik hücre var. Eksiklik göstergesi, ayrı bir MAR benzetiminde AP'yi ortalama 0,0004 artırdı.
- `TrafficType` için geçerli üç kodlama yöntemi yakın AP verdi. Doğrulama etiketlerini gören hedef kodlama AP'yi kat dışı hedef kodlamaya göre 0,0018 artırdı.
- `PageValues` hesabında hangi dönemin işlemlerinin kullanıldığı doğrulanamadığından ana skor bu sütun çıkarılarak hesaplandı. Lojistik regresyon 0,5 eşiğinde satın almaların ortalama %3,3'ünü yakaladı.
- Weka'nın 10 kat kontrolünde ZeroR **0,1564 ± 0,0003**, J48 **0,2430 ± 0,0283** AP verdi. J48, 1.908 satın almanın 150'sini saptadı. ZeroR hiçbirini saptayamadı.

## Katkı beyanı

| Üye | Çalışma kapsamı | Planlanan sunum konusu |
|---|---|---|
| Emircan Demir | Konu ve veri seçimi, tek kişilik proje kapsamında Bölüm 1.1–1.7 | Eksiklik deneyi, sızıntı ve Python–Weka sonuçları |

## Yapay zekâ beyanı

OpenAI Codex, yönergenin incelenmesi, deneylerin tasarlanıp uygulanması, çalıştırma kontrolleri ve sonuç yorumlarının ilk taslağı için kullanıldı.

## Kaynaklar

- [UCI Online Shoppers Purchasing Intention veri kümesi](https://doi.org/10.24432/C5F88Q)
- [Sakar vd. (2019), gerçek zamanlı satın alma niyeti çalışması](https://doi.org/10.1007/s00521-018-3523-0)
- [Kaufman vd. (2012), veri madenciliğinde sızıntı](https://doi.org/10.1145/2382577.2382579)
- [University of Waikato, Weka komut satırı örnekleri](https://waikato.github.io/weka-wiki/primer/)
