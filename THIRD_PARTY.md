# Üçüncü taraf bileşenler

Bu uygulama Qt/PySide6/Shiboken6 6.8.3 kütüphanelerini dinamik olarak kullanır. Bu bileşenler The Qt Company Ltd. ve katkıda bulunanların telif haklarını taşır ve LGPLv3 kapsamında kullanılır. Uygulamanın özgün kodları bu kütüphanelerden ayrı bir eserdir ve yayımlanmamıştır.

Lisans metinleri kurulu programdaki `licenses` klasöründedir. Sürüm envanteri `DEPENDENCIES.json` içindedir. Dağıtım deposundaki sürüm varlıklarına `CanliTercuman-ThirdParty-Sources-1.0.0.zip` ayrıca eklenmelidir; bu arşiv yalnızca açık kaynak bağımlılıkların kaynaklarını içerir, uygulamanın özgün kodlarını içermez.

## Kaynak erişimi

- [Qt Base 6.8.3 kaynakları](https://download.qt.io/archive/qt/6.8/6.8.3/submodules/qtbase-everywhere-src-6.8.3.tar.xz)
- [Qt SVG 6.8.3 kaynakları](https://download.qt.io/archive/qt/6.8/6.8.3/submodules/qtsvg-everywhere-src-6.8.3.tar.xz)
- [Qt çevirileri 6.8.3](https://download.qt.io/archive/qt/6.8/6.8.3/submodules/qttranslations-everywhere-src-6.8.3.tar.xz)
- [PySide6 / Shiboken6 6.8.3 kaynakları](https://download.qt.io/official_releases/QtForPython/pyside6/PySide6-6.8.3-src/pyside-setup-everywhere-src-6.8.3.tar.xz)
- [libsndfile 1.2.2](https://github.com/libsndfile/libsndfile/releases/tag/1.2.2), [ses kütüphanesi derleme tarifleri](https://github.com/bastibe/libsndfile-binaries)

Bu kütüphanelerin kaynakları değiştirilmemiştir. Uygulama kaynaklarını elde etmen gerekmeksizin uyumlu kütüphanelerle yeniden birleştirebilirsin. Kütüphane değişikliklerinin hata ayıklaması için gereken tersine mühendislik hakların saklıdır.

## Paylaşılan kütüphaneyi değiştirme

Programı kapat ve kurulum klasörünün yedeğini al. Aynı Windows x64 / Python ABI ile uyumlu kendi derlediğin Qt/PySide6 DLL/PYD dosyalarını `_internal/PySide6`, Shiboken bileşenlerini `_internal/shiboken6` altında değiştirebilirsin. `libsndfile_x64.dll` ses kütüphanesi `_internal/_soundfile_data` altındadır. Uygulama bu kütüphanelerin imza veya hash değerini çalışırken zorunlu kılmaz. Uyumlu bir arayüz koruman gerekir.

Derleme yönergeleri: [Qt Windows](https://doc.qt.io/qt-6.8/windows-building.html), [Qt for Python](https://doc.qt.io/qtforpython-6.8/building_from_source/index.html). Üçüncü taraf lisansların verdiği haklar uygulamanın dağıtım koşullarıyla kısıtlanmaz.

Diğer bağımlılıklar arasında Python, NumPy, requests, PyAudioWPatch, websocket-client, sounddevice, soundfile/libsndfile, pypdf, cffi ve sertifika/veri paketleri bulunur. Her birinin kendi lisans ve telif bildirimi paket içinde korunur. PyInstaller yalnızca paketleme aracıdır ve kendi istisnası kapsamında kullanılmıştır. Microsoft Visual C++ çalışma zamanı bileşenleri ilgili dağıtım koşullarına tabidir.
