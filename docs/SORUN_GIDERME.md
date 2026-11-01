# Sorun giderme

| Belirti | Kontrol |
|---|---|
| Program ilk açılışta ayar istiyor | Üç API anahtarını ve kullanma hakkın bulunan ElevenLabs Voice ID değerini gir. |
| API anahtarı başka bilgisayarda açılmıyor | Yerel koruma Windows hesabına bağlıdır; yeni bilgisayarda kendi ayarlarını tekrar gir. |
| Karşı tarafa ses gitmiyor | VB-Cable kurulu mu? Görüşmenin mikrofonu CABLE Output mu? ElevenLabs anahtarı, ses erişimi ve kota geçerli mi? |
| Sen sesi duymuyorsun | Dinleme açık mı? Fiziksel kulaklık seçili mi? Ses Testi çalışıyor mu? |
| Otopilot sessiz | Otopilot açık mı? İngilizce toplantı kaynağı doğru mu? Soru tamamlandı mı? API hatası var mı? |
| Yanıt kesiliyor / gecikiyor | Ağ ve kotaları kontrol et; soru sonu beklemesini konuşmanın ritmine göre ayarla. |
| Kendi sesine yeniden yanıt veriyor | Ses yolları geri besleniyor olabilir. Otopilotu kapat, F8'e bas ve ses yönlendirme rehberine dön. |
| CV yüklenmiyor | Metin çıkarılabilen PDF kullan. Görüntü PDF için önce OCR gerekebilir. |
| WhatsApp/Telegram cihaz seçtirmiyor | Masaüstü sürümü veya destekleyen web sürümünde Windows/tarayıcı ses ayarını kontrol et. |
| Güncellemede dosya kullanılıyor | Önce çalışan Canlı Tercüman penceresini kapat; kurulum dosyasını tekrar aç. |

Hata bildirirken API anahtarı, CV, konuşma geçmişi veya kişisel veri klasörünü ekleme. Sürüm, Windows sürümü, seçilen cihaz türleri ve anahtarsız hata metni yeterlidir. Her hizmetin API durumunu ve kullanım kotasını kendi panelinden kontrol et.

## Kulaklığa ses geliyor ama program duymuyor

1. Ana ekranda **Kulaklığa gelen sesi dinle** düğmesine bas. Seçilen kulaklığın WASAPI Loopback kaynağı eşleştirilir.
2. Tarayıcı/toplantı uygulamasının ses çıkışı da aynı kulaklık olmalı. Ses çalarken **Kaynak sesi: ALGILANIYOR** satırını kontrol et.
3. Elle seçim için **Toplantı sesi** listesinden kulaklığının **[Loopback]** kaynağını seç. CABLE In 16ch ancak toplantı uygulamasının çıkışını özellikle bu sanal kanala yönlendirdiğinde ses taşır.
4. Aynı kulaklık yakalanırken yerel İngilizce seslendirme süresince kendini tekrar algılamamak için geçici bastırma uygulanır. Kesintisiz ayrı kanal kullanmak istersen ses yönlendirme kılavuzunu izle.
