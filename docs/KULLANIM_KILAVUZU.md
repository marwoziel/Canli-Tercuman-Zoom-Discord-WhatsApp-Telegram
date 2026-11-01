# Kullanım kılavuzu

## 1. Gereksinimler

Windows 10/11, 64 bit işlemci, internet, mikrofon ve tercihen kulaklık gerekir. Yükleyici Python'u ayrıca kurmanı istemez. Deepgram, Groq ve ElevenLabs hesapları sana aittir. Hesapların API erişimi ve kullanım kotası bulunmalıdır.

## 2. Kurulum ve ilk açılış

GitHub Releases içindeki `CanliTercuman-Setup-1.1.1.exe` dosyasını çalıştır. Başlat menüsüne ve masaüstüne Canlı Tercüman kısayolu eklenir. Program yalnızca kendi kullanıcı hesabına kurulur.

Windows yayımlayan kişiyi doğrulayamadığını belirtirse dosyanın resmî depo bağlantısını ve yayımlanan SHA-256 değerini kontrol et. Paket henüz bir kod imzalama sertifikası taşımaz; güvenlik yazılımını devre dışı bırakman gerekmez.

İlk pencerede üç API anahtarını ve ElevenLabs Voice ID değerini gir. Alanlar boş başlar. Sihirbazdaki Doğrula düğmesi servis erişimini test eder. Son adımda kurulumu bitirdiğinde anahtarlar Windows kullanıcı hesabına bağlı biçimde korunur. Sonradan ana ekrandaki **Kurulum / API Kontrolü** ile değiştirebilirsin.

Hesap sayfaları: [Deepgram](https://console.deepgram.com/), [Groq](https://console.groq.com/keys), [ElevenLabs](https://elevenlabs.io/app/settings/api-keys). Kendi sesinle konuşmak istiyorsan hesabındaki kendi klon sesinin Voice ID değerini kullan. Uygulama senin adına ses klonlamaz; herhangi bir geliştiricinin sesi pakete dahil edilmez.

## 3. CV ve kurallar

**PDF Yükle** ile metin içeren CV PDF'ni seç. Taranmış/görüntü PDF için önce metin çıkarma gerekebilir. CV eklemeden de temel çeviri çalışır; otopilot deneyim ve özgeçmiş ayrıntılarını bilmez.

**Kuralları Düzenle** ile kendi üslubunu, yetkilerini ve doğrulanmış bilgilerini ekle. Örnek: “Kısa ve doğal yanıt ver. Bilmediğim konuda kesin söz verme. Deneyim ve sonuç uydurma.” Başkasına ait CV veya hazır kişisel kurallar yüklenmiş değildir.

**Yanıtı Düzelt ve Öğret** benzer sorular için yerel örnek kaydeder. Bu işlem model ağırlıklarını eğitmez. Aynı soru için son kaydettiğin düzeltme kullanılır.

## 4. Türkçe konuşup İngilizce ilet

Görüşme uygulamasının mikrofonunu **CABLE Output** yap. Canlı Tercüman'da fiziksel mikrofonunu ve dinlemek için kulaklığını seç. **Türkçe → İngilizce** düğmesini aç, Türkçe konuş ve cümlenin bitişi için kısa süre bekle. Kaynak metin ile İngilizce çeviri ikinci sekmede görünür; İngilizce ses görüşmeye gider.

Mikrofon çevirisi söylediğin içeriği çevirir; CV'den senin yerine cevap uydurması amaçlanmaz.

## 5. Otopilot

**Otopilot** düğmesini aç. Mikrofon çevirisi kendiliğinden kapanır. Karşı tarafın İngilizce konuşması tamamlandığında program kendi CV ve kurallarına göre kısa İngilizce yanıt üretir ve seçtiğin ElevenLabs sesiyle görüşmeye gönderir. Hazırlanan yanıt ekranda ayrıca görünür. Otopilot açıkken İngilizce test kutusu da sesli yanıt üretebilir.

Otopilotu kapatmak bekleyen otomatik yanıtı ve çalan sesi iptal eder. **F8** yalnızca o anki işi durdurur; düğme açık kalırsa sonraki yeni soruda yeniden yanıt verebilir. Tamamen durdurmak için otopilot düğmesini kapat.

Yapay zekâ yanlış anlayabilir veya yanlış yanıt verebilir. Denetim gerektiğinde manuel moda geç. Kullanma hakkın bulunan sesi kullan; görüşmedeki katılımcıların ve hizmetin kurallarına uygun davran.

## 6. Ses ve bekleme ayarları

**Ses hızı** okuma hızını; **Cümle arası** seslendirmenin duraklamasını; **Soru sonu** İngilizce sorunun bittiğini kabul etmeden önce beklenecek sessizliği ayarlar. Çok parçalı sorular erken bölünüyorsa soru sonu süresini artır; daha hızlı tepki için azalt.

Yerel dinlemeyi kapatmak görüşmeye giden sesi kapatmaz. **Toplantıyı kulaklığa aktar** ayrı toplantı çıkışını kulaklığa dinletir. Aynı ses yolunu döngüye sokmamak için [ses şemasını](SES_YONLENDIRME.md) uygula.

## 7. Kayıtlar ve kaldırma

Kişisel dosyalar `%LOCALAPPDATA%\CanliTercuman` altında, program dosyalarından ayrı tutulur. CV, kurallar, sohbet geçmişi, geri bildirimler ve ses ayarları yereldir; API anahtarları `credentials.bin` içindedir. Bu klasörü paylaşma. DPAPI koruması aynı Windows kullanıcısı altında çalışan her uygulamaya karşı mutlak koruma değildir.

Program klasörü `%LOCALAPPDATA%\Programs\CanliTercuman` altındadır. Windows uygulama listesinden kaldırılabilir. Kaldırma kişisel verileri otomatik silmez; tekrar kullanmayacaksan veri klasörünü kendin silebilirsin. Güncelleme de bu kişisel klasörü değiştirmez.
