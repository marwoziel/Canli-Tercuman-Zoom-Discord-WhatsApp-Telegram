# Baştan sona kurulum: sanal mikrofon dahil

## 1 — Canlı Tercüman'ı kur

GitHub Releases bölümünden **CanliTercuman-Setup-1.0.0.exe** indir ve çalıştır. Windows 10/11 x64 içindir. Python veya terminal gerektirmez. Başlat menüsü ve masaüstü kısayolu oluşur.

## 2 — Sanal mikrofon: VB-Cable

1. [VB-Audio'nun resmî VB-Cable sayfasını](https://vb-audio.com/Cable/) aç.
2. Windows sürücü paketini indir ve ZIP'in içindeki tüm dosyaları bir klasöre çıkar.
3. Paket içindeki Windows 64 bit kurulum programını üreticinin yönergesine göre **yönetici olarak** çalıştır ve sürücüyü kur.
4. Üreticinin istediği yeniden başlatmayı tamamla.
5. Windows ses aygıtlarında **CABLE Input** çıkışı ve **CABLE Output** girişi görünmeli.

VB-Cable üçüncü taraf bir sanal ses sürücüsüdür. Bu uygulamanın kurulum dosyasına gömülmez; sürücü kurulumu ve olası yeniden başlatma ayrı bir defalık adımdır. İndirme için resmî sayfayı kullan. [Üreticinin kurulum bilgisi](https://vb-audio.com/Cable/).

## 3 — Kendi API hesaplarını hazırla

[API anahtarı alma rehberindeki](API_ANAHTARLARI.md) bağlantılardan Deepgram, Groq ve ElevenLabs anahtarlarını al. ElevenLabs'te kullanma hakkın bulunan sesin Voice ID değerini de hazırla. Bunları uygulamanın ilk açılış penceresine gir.

## 4 — Görüşmenin mikrofonunu ayarla

Zoom, Discord veya cihaz seçimini destekleyen WhatsApp/Telegram masaüstü/web sürümünde **mikrofon / ses girişi = CABLE Output** seç. Bu, İngilizce sesin karşı tarafa gideceği sanal mikrofondur.

Görüşmenin hoparlörünü **CABLE Input** yapma: bu uygulamanın giden konuşma yoludur. Fiziksel kulaklığını veya ayrı toplantı çıkışını seç. [Uygulama bazlı ses yönlendirme tablosu](SES_YONLENDIRME.md).

## 5 — Canlı Tercüman'da ayarla

- **Toplantı sesi:** Karşı tarafı duyduğun Windows çıkışını seç.
- **Benim Türkçe mikrofonum:** Kendi fiziksel mikrofonunu seç.
- **Senin İngilizce sesini dinle:** Kendi kulaklığını seç ve **Ses Testi** ile kontrol et.
- **PDF Yükle / Kuralları Düzenle:** Kendi bilgilerini ekle; dağıtım boş başlar.

## 6 — Önce kısa test yap

**Türkçe → İngilizce** düğmesini aç ve kısa bir Türkçe cümle söyle. İngilizce çeviri görünüp görüşmenin mikrofon göstergesi hareket etmeli. Ardından **Otopilot** düğmesini açıp kısa bir İngilizce soru ile dene: yanıt, kendi CV/kurallarına göre otomatik İngilizce hazırlanır ve seslendirilir. Otopilot açıkken İngilizce test kutusu da sesli yanıt üretir; gerçek bir görüşmede bunu bilerek kullan.

İki mod birbirini kapatır. **F8** çalan/bekleyen yanıtı keser. Otopilotu tamamen devreden çıkarmak için düğmesini kapat.

## 7 — Yankı ve kesintisiz dinleme

Toplantı sesi ile yerel seslendirme aynı çıkıştaysa uygulama kendi sesini tekrar tanımamak için tanımayı kısa süre bastırır; bu sırada yeni söz kaçabilir. Kesintisiz dinleme için giden CABLE Input'tan ayrı bir toplantı çıkışı ve doğru kulaklık yönlendirmesi gerekir. Bütün ses yollarını tek sanal kabloya bağlamak yeterli değildir.

Ayrıntılar: [kullanım kılavuzu](KULLANIM_KILAVUZU.md), [sorun giderme](SORUN_GIDERME.md), [maliyetler](MALIYETLER.md). Program çevrimdışı çalışmaz; sağlayıcı kotaları ve gerçek ses cihazları ayrıca gerekir.
