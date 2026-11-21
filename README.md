# Online alışverişte satın alma niyeti

BIL545 · Proje 1 · Üsküdar Üniversitesi · 2026–2027 Güz

## Grup 7

Emircan Demir · 264309006 · emircan.demir@st.uskudar.edu.tr

Grup dağıldıktan sonra hoca mailde sadece Bölüm 2'yi yapmam gerektiğini söyledi. Bölüm 1'i de ben ekledim.

## Veri ve çalıştırma

Konu 9.5. Satın almayla biten oturumları, gezinme bilgileriyle ayırmayı denedim. Veri setinde 12.330 oturum ve 17 öznitelik var. Hedef *Revenue*. [UCI veri seti](https://doi.org/10.24432/C5F88Q) · [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

[Defter](proje1/BIL545_Proje1_EmircanDemir.ipynb) · [Colab'da aç](https://colab.research.google.com/github/EmircanDemirTR/bil545-online-alisveris/blob/main/proje1/BIL545_Proje1_EmircanDemir.ipynb)

Colab'da **Çalışma zamanı → Tümünü çalıştır** yeterli. Defter, CSV'yi bulamazsa UCI'dan indiriyor. Bağlantı özel depo nedeniyle açılmazsa defteri indirip Colab'a yükleyebilirsiniz. Yerelde Weka için Java gerekiyor.

## Bölüm 1 sonucu

5 katlı çapraz doğrulamayı 5 kez tekrarladım. Bu deneyde Dummy **0,1564 ± 0,0002**, lojistik regresyon **0,2998 ± 0,0183** AP verdi. *PageValues* eklenince AP **0,6374 ± 0,0212** oldu. Değerin ne zaman hesaplandığını bilmediğim için ana modele almadım. Weka'da J48, 10 katlı kontrolde **0,2430 ± 0,0283** AP verdi.

## Katkı ve yapay zekâ beyanı

Konuyu ve veriyi ben seçtim. Sunumda eksiklik, sızıntı ve Weka sonuçlarını anlatmayı planlıyorum. Kod, deneylerin çalıştırılması ve yazıların düzenlenmesinde OpenAI Codex'ten yardım aldım. Kaynaklar defterin sonunda.
