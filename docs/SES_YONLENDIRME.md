# Ses yönlendirme

Temel zincir:

```text
Fiziksel mikrofon → Türkçe tanıma → İngilizce ses → CABLE Input
                                                    ↓
Görüşme uygulamasında mikrofon: CABLE Output → Karşı taraf

Karşı tarafın sesi → Seçilen Windows çıkışı → Toplantı sesi tanıma
```

## Bir defalık sürücü kurulumu

[VB-Audio'nun resmî sayfasından](https://vb-audio.com/Cable/) VB-Cable'ı indir. Üreticinin yönergesine göre sürücüyü yönetici olarak kur ve gerektiğinde yeniden başlat. Uygulama yükleyicisi bu sürücüyü paketlemez veya lisansını devralmaz.

**CABLE Input** sesin gönderildiği çıkıştır; **CABLE Output** görüşme uygulamasının seçeceği mikrofon girişidir. Adların benzer olması normaldir.

## Görüşme uygulamaları

| Uygulama | Mikrofon / giriş | Hoparlör / çıkış |
|---|---|---|
| Zoom masaüstü | CABLE Output | Fiziksel kulaklık veya ayrı toplantı çıkışı |
| Discord masaüstü | CABLE Output | Fiziksel kulaklık veya ayrı toplantı çıkışı |
| WhatsApp masaüstü / destekleyen web sürümü | Seçilebiliyorsa CABLE Output | Fiziksel kulaklık veya ayrı toplantı çıkışı |
| Telegram masaüstü / destekleyen web sürümü | Seçilebiliyorsa CABLE Output | Fiziksel kulaklık veya ayrı toplantı çıkışı |

Menü isimleri sürüme göre değişir. Uygulama cihaz seçtirmiyorsa Windows'un uygulama bazlı ses ayarını veya tarayıcının mikrofon seçimini kullan. Bu tablo yapılandırma rehberidir; her hizmetin bütün sürümlerinde canlı test yapıldığı anlamına gelmez.

## Aynı çıkış ve ayrı çıkış

En basit düzende toplantı sesi ile yerel İngilizce ses aynı kulaklıkta duyulur. Program kendi sesini tekrar tanımamak için seslendirme sırasında tanımayı geçici bastırır; bu esnada yeni söz kaçabilir.

Kesintisiz dinleme için toplantı sesini **giden CABLE Input'tan farklı** bir çıkışa yönlendir ve Canlı Tercüman'da aynı toplantı kaynağını seç. Yerel dinlemeyi fiziksel kulaklığa ver. Aynı yolun kendi kendisine geri beslenmediğini ses testiyle doğrula. Tek standart kabloyla bütün yönleri aynı anda ayırabildiğini varsayma; ek sanal çıkış donanımı/yazılımı gerekebilir.

Önce **Ses Testi**, ardından kısa bir Türkçe cümleyle görüşme uygulamasının mikrofon göstergesini kontrol et. İki Canlı Tercüman kopyasını aynı anda açma. Sorun varsa F8 ile durdurup otopilotu kapat.
