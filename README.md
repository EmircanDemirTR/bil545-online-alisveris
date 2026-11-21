# Online alışverişte satın alma niyeti

BIL545 · Veri Madenciliğinde İleri Konular · 2026–2027 Güz · Üsküdar Üniversitesi

## Grup ve kapsam

**Grup 7** · Emircan Demir · 264309006

**İletişim sorumlusu** Emircan Demir · emircan.demir@st.uskudar.edu.tr

Grup dağıldıktan sonra öğretim üyesi e-postada bireysel olarak Bölüm 2'den sorumlu olduğumu belirtti. Bölüm 1'i de kendi isteğimle hazırladım.

## Veri ve çalıştırma

Konu 9.5. Tamamlanmış alışveriş oturumlarının gezinme ve ziyaret bilgileri, satın almayla biten oturumları ayırmaya ne kadar yardımcı olur?

[UCI Online Shoppers Purchasing Intention](https://doi.org/10.24432/C5F88Q) · [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) · 12.330 oturum, 17 öznitelik. `Revenue` oturumun satın almayla bitip bitmediğini gösterir.

[Defter](proje1/BIL545_Proje1_EmircanDemir.ipynb) · [Colab'da aç](https://colab.research.google.com/github/EmircanDemirTR/bil545-online-alisveris/blob/main/proje1/BIL545_Proje1_EmircanDemir.ipynb)

Colab'da **Çalışma zamanı → Tümünü çalıştır**. Defter CSV'yi çalışma klasöründe bulamazsa UCI'dan indirir. Özel depo Colab'da açılmazsa defter GitHub'dan indirilip Colab'a yüklenebilir. Yerelde Weka için Java gerekir.

## Bölüm 1 sonucu

5 × 5 katmanlı çapraz doğrulamada Dummy **0,1564 ± 0,0002**, lojistik regresyon **0,2998 ± 0,0183** AP verdi. `PageValues` eklendiğinde AP **0,6374 ± 0,0212** oldu. Hesap penceresi doğrulanamadığı için bu sütun ana modelde kullanılmadı. Weka'nın 10 katlı kontrolünde J48 **0,2430 ± 0,0283** AP verdi.

## Katkı ve yapay zekâ beyanı

Konu ve UCI veri setini seçtim, kapsamı öğretim üyesiyle netleştirdim ve Bölüm 1'i gönüllü olarak hazırladım. Sunumda eksiklik, sızıntı ve Weka sonuçlarını anlatmayı planlıyorum. OpenAI Codex kodun hazırlanması ve düzenlenmesi, deneylerin çalıştırılması, çıktı kontrolü ve yorum taslağı için kullanıldı. Kaynaklar defterin sonunda yer alıyor.
