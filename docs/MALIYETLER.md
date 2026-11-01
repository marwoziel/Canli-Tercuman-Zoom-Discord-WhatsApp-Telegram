# Maliyetler: düşük bütçeyle kullanım

Fiyat kontrol tarihi: **1 Kasım 2026**. Tutarlar ABD dolarıdır. Aşağıdaki tutarlar sağlayıcıların sayfalarından alınan birim fiyatlarla yapılan kullanım hesabıdır; abonelik teklifi veya sabit oturum fiyatı değildir.

| Hizmet | Sayfada gösterilen fiyat | Kaynak |
|---|---|---|
| Groq GPT-OSS 120B | 1 milyon girdi tokenı $0,15; çıktı tokenı $0,60 | [Groq modelleri](https://console.groq.com/docs/models) |
| Groq GPT-OSS 20B | 1 milyon girdi tokenı $0,075; çıktı tokenı $0,30 | [Groq modelleri](https://console.groq.com/docs/models) |
| Deepgram Nova-3 Monolingual, Pay as you go | $0,0077 / işlenen ses dakikası | [Deepgram fiyatları](https://deepgram.com/pricing) |
| Deepgram Nova-3 Multilingual, Pay as you go | $0,0092 / işlenen ses dakikası | [Deepgram fiyatları](https://deepgram.com/pricing) |
| ElevenLabs Flash / Turbo API sayfası | $0,04 / 1.000 karakter | [ElevenLabs API fiyatları](https://elevenlabs.io/pricing/api) |

## Örnek oturum hesabı

Varsayımlar: toplam 40 dakika işlenen tek dil ses akışı; tüm çeviri/öneri/otopilot çağrıları toplamında 200.000 girdi ve 20.000 çıktı tokenı; 6.000 karakter seslendirme.

- Tanıma: 40 × $0,0077 = **$0,308**.
- GPT-OSS 120B: 0,2 × $0,15 + 0,02 × $0,60 = **$0,042**.
- Seslendirme: 6 × $0,04 = **$0,24**.
- Bu varsayımlarla toplam kullanım: **$0,59**. Tanımanın tamamı çok dilli tarifeden olursa yaklaşık **$0,65**.

Bu bir ölçülmüş fatura değil, açık varsayımlı hesap örneğidir. Gerçek toplamı uygulama süresinden tek başına çıkarma: iki ses kanalı aynı anda işlendiğinde süreleri toplanır; sessizlik içeren gönderilmiş ses de işlenen süreye dahil olabilir. Groq, Türkçe çeviri, öneri ve otopilot için ayrı çağrılar yapabilir. CV/kuralların uzunluğu, yanıt sayısı, iç muhakeme tokenları ve tekrar denemeler token tüketimini değiştirir.

ElevenLabs hesabının planı, dahil krediler, ek karakter fiyatı ve seçilen ses farklı ücretlendirme getirebilir. Vergiler, döviz kuru, abonelik tabanı, varsa ses klonlama ve sanal ses sürücüsü maliyetleri yukarıdaki örneğe dahil değildir. Ücretsiz kota veya kampanya, sürekli ücretsiz kullanım garantisi değildir. Son fiyat hesabındaki sağlayıcı panelidir.

## Tasarruf

Gerekmeyen mikrofon kanalını kapat, boşta uzun süre açık bırakma. CV'yi ilgili bilgilerle sınırla, kurallarda kısa yanıt iste. Sürekli deneme yapmak yerine ses yönlendirmesini yerel **Ses Testi** ile kontrol et. Hesap panellerinde harcama limiti ve kullanım uyarılarını ayarla.

Tanıtımda uygun ifade: **“Kendi API hesaplarınla, düşük kullanım maliyetiyle çalıştır; örnek maliyet hesabını incele.”** “Sınırsız ücretsiz”, “her toplantı şu kadar” veya “herkesten ucuz” iddiası kullanılmaz.
