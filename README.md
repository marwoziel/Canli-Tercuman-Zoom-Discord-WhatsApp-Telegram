# Canlı Tercüman — Zoom, Discord, WhatsApp, Telegram

**Türkçe konuş. İngilizce duyulsun. İstersen yanıtı otopilota bırak.**

Windows için iki yönlü canlı konuşma asistanı. Türkçe söylediklerini İngilizce seslendirir; İngilizce konuşmaları Türkçeye çevirir ve yanıt önerir. Otopilot açıkken kendi CV ve kurallarına göre İngilizce yanıtı otomatik seslendirir.

[**Windows kurulumunu indir**](https://github.com/marwoziel/Canli-Tercuman-Zoom-Discord-WhatsApp-Telegram/releases/latest/download/CanliTercuman-Setup-1.0.0.exe) · [Sürümler](https://github.com/marwoziel/Canli-Tercuman-Zoom-Discord-WhatsApp-Telegram/releases)

## Kurulum

1. Bu deponun **Releases** bölümünden `CanliTercuman-Setup-1.0.0.exe` dosyasını indir.
2. Kurulum dosyasını çalıştır. Python veya terminal gerekmez; kullanıcı hesabına kurulur.
3. İlk açılışta **kendi** Deepgram, Groq, ElevenLabs API anahtarlarını ve ElevenLabs Voice ID değerini gir.
4. Karşı tarafa ses göndermek için [resmî VB-Cable sürücüsünü](https://vb-audio.com/Cable/) kur; gerekiyorsa Windows'u yeniden başlat.
5. Görüşme uygulamasının mikrofonunu **CABLE Output**, Canlı Tercüman'daki dinleme cihazını fiziksel kulaklığın olarak seç.

**Tek tık kurulum uygulama içindir.** API hesapları, ses kimliği ve ses sürücüsünün ilk kurulumu ayrıca gerekir. VB-Cable sürücüsü pakete gömülü değildir ve uygulama tarafından sessizce kurulmaz.

![İlk açılış — alanlar boş başlar](assets/ilk-acilis.png)

**Yeni başlayanlar:** [Sanal mikrofon dahil baştan sona kurulum](docs/BASTAN_SONA_KURULUM.md) · [API anahtarı alma bağlantıları](docs/API_ANAHTARLARI.md)

## İki mod

| Düğme | Ne yapar? |
|---|---|
| **Türkçe → İngilizce: AÇIK** | Sen Türkçe konuşursun; İngilizce çeviri seçtiğin sesle karşı tarafa gider. |
| **Otopilot: AÇIK** | İngilizce konuşma bittiğinde kendi CV ve kurallarına göre İngilizce yanıt hazırlanıp sesli gönderilir. |
| **F8** | Çalan sesi ve bekleyen yanıtı iptal eder. Otopilot açıksa sonraki yeni konuşmada tekrar devreye girer. |

İki mod aynı anda açılmaz. Otopilot her uygulama açılışında kapalıdır.

## Düşük kullanım maliyetiyle kendi hesabından çalıştır

API maliyetini kontrol et: kendi hesaplarını kullan, gereksiz açık mikrofonu kapat, yanıtları kısa tut. Açık varsayımlı örnek bir oturum yaklaşık **0,59 ABD doları kullanım bedeli** hesaplar; bu bir tarife veya garanti değildir. Plan ücretleri, vergiler, ses kredileri ve yeniden denemeler değişebilir. [Fiyat kaynakları ve örnek hesap](docs/MALIYETLER.md).

## Kişiselleştirme ve gizlilik

CV, kurallar, konuşma hafızası ve ses kimliği boş başlar; geliştiriciye ait örnek kişisel veri içermez. Kendi CV'ni **PDF Yükle**, tercihlerini **Kuralları Düzenle** üzerinden ekle. Ses için **Ses Kimliği**, hesaplar için **API Ayarları** düğmesini kullan.

API anahtarları Windows DPAPI ile bu kullanıcı hesabına bağlı olarak yerel saklanır. Konuşma sesi Deepgram'a, ilgili metin/CV/kurallar Groq'a, seslendirilecek metin ElevenLabs'e gönderilir. Bu çevrimdışı bir uygulama değildir. [Veri kullanımı](PRIVACY.md).

## Belgeler

- [Adım adım kullanım](docs/KULLANIM_KILAVUZU.md)
- [Zoom / Discord / WhatsApp / Telegram ses ayarı](docs/SES_YONLENDIRME.md)
- [Maliyet ve tasarruf](docs/MALIYETLER.md)
- [Sorun giderme](docs/SORUN_GIDERME.md)
- [Sürüm notları](CHANGELOG.md)

## GitHub ve fork

Bu depo **kurulum ve dokümantasyon deposudur**. Uygulamanın ham kaynak kodları yayımlanmaz. Depoyu forklayarak belgeleri, çevirileri ve dağıtım sayfasını geliştirebilirsin; uygulama kodunun geliştirilebilir bir fork'u burada bulunmaz. [Dağıtım koşulları](LICENSE.md).

Zoom, Discord, WhatsApp ve Telegram ile bağlantı, Windows ses cihazı yönlendirmesi üzerinden kurulur; bu servislerin resmî eklentisi değildir. Cihaz seçimi uygulama sürümüne göre değişebilir. Tam seslendirme gecikmesi ağ ve API yanıt süresine bağlıdır; canlı çıktı hatasızlık garantisi taşımaz.
