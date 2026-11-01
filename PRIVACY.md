# Veri kullanımı

Dağıtım dosyalarında geliştiricinin API anahtarları, CV'si, kuralları, sohbet geçmişi, geri bildirimleri veya ses kimliği bulunmaz. Uygulama kendi bilgilerinle başlar.

- **Deepgram:** Tanımayı açtığın kanallardaki ses, metne çevrilmek üzere gönderilir.
- **Groq:** Çevrilecek konuşma ve ilgili yanıt üretiminde kendi CV/kuralların, yakın konuşma bağlamı ve seçilmiş düzeltmeler gönderilir.
- **ElevenLabs:** İngilizce ses üretimi için seslendirilecek metin, ses kimliği ve ses ayarları gönderilir.

Sağlayıcıların kendi veri saklama ve gizlilik koşulları geçerlidir. Programın kendine ait bir geliştirici telemetri sunucusu, hesap backend'i veya otomatik güncelleme servisi yoktur. İnternet olmadan bu modeller çalışmaz.

API anahtarları `%LOCALAPPDATA%\CanliTercuman\credentials.bin` içinde Windows DPAPI korumasıyla saklanır. Bu koruma, aynı Windows hesabındaki bütün yazılımlara karşı bir güvenlik sınırı değildir. CV, kurallar, sohbet ve yanıt örnekleri yerel dosyalardır; paylaşılmamalıdır. Kurulum ve kaldırma kişisel veri klasörünü silmez.

Görüşme ve ses kullanımı konusunda katılımcıların haklarına, hizmet kurallarına ve geçerli gereksinimlere uygun davran. Uygulama görüşmeyi otomatik olarak ses dosyasına kaydetmez; tanınan metinler arayüzde, koç sohbeti ve onaylı örnekler yerel hafızada tutulabilir.
