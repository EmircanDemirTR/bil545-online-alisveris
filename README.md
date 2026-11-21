# Online alışverişte satın alma niyeti

BIL545 · Proje 1 · Üsküdar Üniversitesi · 2026–2027 Güz

## Grup

| Grup | Öğrenci | Öğrenci no | İletişim |
|---|---|---|---|
| 7 | Emircan Demir | 264309006 | emircan.demir@st.uskudar.edu.tr |

Grup dağıldıktan sonra hoca mailde sadece Bölüm 2'yi yapmam gerektiğini söyledi. Bölüm 1'i de ben ekledim.

## Soru

Konu 9.5. Tamamlanmış bir oturumun gezinme özeti, satın almayla biten oturumları ayırmaya yeter mi?

## Veri

| | |
|---|---|
| Kaynak | [UCI Online Shoppers Purchasing Intention](https://doi.org/10.24432/C5F88Q) |
| Lisans | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Boyut | 12.330 oturum ve 17 öznitelik |
| Hedef | *Revenue*, oturumda satın alma olup olmadığı |

Bölüm 2'de 12.330 oturumun tamamı ve *PageValues* dışındaki 16 öznitelik kullanılacak.

## Depo yapısı

- *README.md* proje özeti
- [proje1/BIL545_Proje1_EmircanDemir.ipynb](proje1/BIL545_Proje1_EmircanDemir.ipynb) Proje 1 defteri

## Çalıştırma

[Colab'da aç](https://colab.research.google.com/github/EmircanDemirTR/bil545-online-alisveris/blob/main/proje1/BIL545_Proje1_EmircanDemir.ipynb) ve **Çalışma zamanı → Tümünü çalıştır** seçeneğini kullan. CSV bulunmazsa defter UCI'dan indiriyor. Bağlantı açılmazsa defter indirilebilir ve Colab'a yüklenebilir. Yerelde Weka için Java gerekiyor.

## Sonuç özeti

| 5 kat × 5 tekrar | AP (ortalama ± std) |
|---|---:|
| Dummy | 0,1547 ± 0,0002 |
| Lojistik regresyon, ana model | 0,3288 ± 0,0145 |
| Tüm veride ön işleme (yanlış) | 0,3289 ± 0,0146 |
| Sızıntı deneyi, satın almaları yalnız eğitimden kopyalama | 0,3238 ± 0,0136 |
| Sızıntı deneyi, satın almaları tüm veriden kopyalama (yanlış) | 0,3317 ± 0,0148 |

*PageValues* eklenince AP **0,6412 ± 0,0219** oldu. Değerin hangi dönemin işlemlerinden hesaplandığını bilmediğim için ana modele almadım. Weka'da J48'in 10 kat AP'si **0,2723 ± 0,0331**.

## Katkı ve yapay zekâ beyanı

Konuyu ve veriyi ben seçtim. Sunumda eksiklik, sızıntı ve Weka sonuçlarını anlatmayı planlıyorum. Kod, deneylerin çalıştırılması ve yazıların düzenlenmesinde OpenAI Codex'ten yardım aldım.

## Kaynaklar

- [Sakar ve Kastro (2018), UCI veri seti](https://doi.org/10.24432/C5F88Q)
- [Sakar vd. (2019), satın alma niyeti çalışması](https://doi.org/10.1007/s00521-018-3523-0)
- [Kaufman vd. (2012), veri madenciliğinde sızıntı](https://doi.org/10.1145/2382577.2382579)
