# API anahtarları ve ses kimliği

Bu uygulamaya geliştiricinin hesabı yüklenmiş değildir. Her kullanıcı aşağıdaki üç sağlayıcıda kendi hesabını kullanır. API kullanım ücretleri bu hesaplardan karşılanır.

| Gerekli bilgi | Hesap / anahtar sayfası | Ne için kullanılır? |
|---|---|---|
| Deepgram API anahtarı | [Deepgram Console](https://console.deepgram.com/) | İngilizce toplantı sesini ve Türkçe mikrofonu metne çevirir. |
| Groq API anahtarı | [Groq API Keys](https://console.groq.com/keys) | Çeviri, CV/kurallara göre yanıt önerisi ve otopilot yanıtı üretir. |
| ElevenLabs API anahtarı | [ElevenLabs API ayarları](https://elevenlabs.io/app/settings/api-keys) | İngilizce metni sese çevirir. |
| ElevenLabs Voice ID | [ElevenLabs hesabı](https://elevenlabs.io/app/voices) | Seslendirmede hangi sesin kullanılacağını belirler. |

## Deepgram

Konsola giriş yap, ilgili projeyi seç, proje ayarlarından API anahtarları bölümünü aç ve yeni anahtar oluştur. Anahtarın konuşma tanıma isteği yapma yetkisi olmalı. Üretilen gizli anahtarı uygulamadaki **Deepgram API anahtarı** alanına gir. [Resmî anahtar oluşturma rehberi](https://developers.deepgram.com/docs/create-additional-api-keys).

## Groq

Groq hesabında API Keys sayfasından bir anahtar oluştur ve uygulamadaki **Groq API anahtarı** alanına gir. Uygulama GPT-OSS modellerini kullanır; hesap/model izinleri ve hız limitleri geçerlidir. [Resmî hızlı başlangıç](https://console.groq.com/docs/quickstart).

## ElevenLabs ve Voice ID

ElevenLabs hesabında kişisel API anahtarı oluştur. Metinden ses üretimi için gereken izni ve yeterli kullanım kotasını sağla; tam gizli anahtarı **ElevenLabs API anahtarı** alanına gir. Anahtarın adı veya kayıt kimliği gizli anahtarın yerine geçmez. [Resmî API anahtarı bilgileri](https://elevenlabs.io/docs/overview/administration/workspaces/api-keys).

Kullanma hakkın bulunan bir ses seç ve o sesin **Voice ID** değerini ayrı alana gir. Kendi sesinle çalışmak istiyorsan önce kendi ElevenLabs hesabında desteklenen bir ses klonu oluşturman gerekir; klonlama seçenekleri plana göre değişebilir. Uygulama otomatik ses klonlamaz. **API anahtarı ile Voice ID farklı bilgilerdir.**

## Uygulamaya girme

İlk açılış sihirbazının **API ve Ses** adımında dört alanı doldur ve **Doğrula** düğmesine bas. Üç servis ve ses başarılı olduğunda Devam açılır; son adımda **Kurulumu bitir ve programı aç** ile kaydedilir. Sonradan **Kurulum / API Kontrolü** ve **Ses Kimliği** düğmelerini kullanabilirsin. Kişisel CV'ni **PDF Yükle**, kurallarını **Kuralları Düzenle** ile ekle.

Anahtarlar Windows kullanıcı hesabına bağlı korumayla yerel saklanır. Anahtarını GitHub'a, Twitter'a, hata bildirimine veya ekran görüntüsüne koyma. Süresi dolan veya kotası biten bir anahtar için sağlayıcı panelini kontrol et. Uygulamanın kurulmuş olması hesap bakiyesi veya API erişimi sağlamaz.
