# Gizlilik Politikası · Privacy Policy

**CastCanvas: Live Whiteboard** (iPad, Android) ve **CastCanvas Cam** (iPhone, Android) · Son güncelleme / Last updated: 19 Kasım 2026 / November 19, 2026

[Türkçe](#türkçe) · [English](#english)

---

## Türkçe

**Kısaca:** CastCanvas ve CastCanvas Cam hesap istemez; reklam, takip ya da kendi analiz aracımız yoktur. Tahtalarınız, kayıtlarınız ve ayarlarınız cihazınızda kalır. Görüntü ve ses yalnızca **sizin seçtiğiniz kendi cihazlarınıza** (bilgisayarınızdaki OBS, tabletiniz) yerel ağ üzerinden gider. Bize hiçbir veri gelmez. Tek istisna, Android'deki Google ML Kit kütüphanesinin Google'a gönderdiği teknik tanılama bilgisidir (aşağıda).

### Verileriniz nerede kalır?

- **Tahtalar, PDF'ler, çizimler, sahneler ve ayarlar** yalnızca cihazınızda saklanır.
- **Doğrudan çekim kayıtları** (kamera ve ses) yalnızca tablette, uygulamanın kendi klasöründe saklanır. Fotoğraflar'a ya da Galeri'ye yalnızca siz isterseniz kopyalanır.
- **OBS parolası** iPad'de Anahtar Zinciri'nde, Android'de uygulamanın kendi ayarlarında saklanır.
- **El yazısını formüle çevirme ve arka plan efektleri** (bulanıklaştırma, arka planı değiştirme ya da kaldırma) cihazda yapılır. Görüntünüz bu işlemler için hiçbir yere gönderilmez.

### Yerel ağ

CastCanvas yerel ağı şu işler için kullanır:

- Tahtanızın görüntüsünü **NDI** ile aynı ağdaki **kendi bilgisayarınızda** çalışan OBS'e göndermek.
- OBS'in canlı görüntüsünü ve sesini tablette göstermek; OBS'in sesini kısa videolara eklemek.
- Kaydı ve sahneleri tabletten yönetmek (OBS WebSocket).
- **Telefonunuzu kamera olarak kullanmak:** CastCanvas Cam'in görüntüsünü ve sesini tablete almak.

Bu bağlantılar yalnızca sizin cihazlarınız arasındadır ve yerel ağınızın dışına çıkmaz. Görüntü ve ses yerel ağda şifrelenmeden gider; bu yüzden yalnızca güvendiğiniz ağlarda (ev, okul, kendi etkin noktanız) kullanın.

### Kamera ve mikrofon

- **CastCanvas (tablet):** kamera, OBS'teki bağlanma kare kodunu okutmak ve doğrudan çekimde (OBS'siz) sizi kaydetmek için kullanılır. Mikrofon yalnızca doğrudan çekimde sesinizi kayda eklemek için kullanılır. Görüntü ve ses tablette kalır.
- **CastCanvas Cam (telefon):** kamera, görüntünüzü yerel ağdaki kendi CastCanvas tabletinize göndermek için kullanılır. Mikrofon isteğe bağlıdır; yalnızca tablet telefonun mikrofonunu seçerse ses gönderilir. Görüntü ve ses gerçek zamanlı gider; telefonda kaydedilmez, saklanmaz.
- **Eşleştirme:** tablet telefona ilk bağlanırken telefonun ekranındaki 4 haneli kod sorulur. Kod ağda açık gitmez (HMAC ile doğrulanır). Kod ve bağlanılan cihazların adları yalnızca bu iki cihazda saklanır.
- **Bluetooth:** Bluetooth kulaklığın mikrofonunu seçmek ve adını göstermek için kullanılır. Başka bir Bluetooth cihazı taranmaz.

### Android'de Google ML Kit

Android tablet uygulaması, el yazısı tanıma ve arka plan efektleri için Google'ın **ML Kit** kütüphanesini kullanır. Görüntü işleme cihazda yapılır, görüntünüz gönderilmez. Ancak ML Kit, Google'ın açıkladığı üzere, Google'a şu teknik bilgileri gönderir:
- cihaz modeli ve Android sürümü;
- uygulamanın adı ve sürümü;
- performans ölçüleri ve hata kodları;
- kuruluma özel, kişiyi tanımlamayan bir kimlik.

Google bunları tanılama ve kullanım istatistiği için kullanır ve üçüncü taraflara aktarmaz: [developers.google.com/ml-kit/android-data-disclosure](https://developers.google.com/ml-kit/android-data-disclosure). iPad ve iPhone uygulamalarında böyle bir kütüphane yoktur; efektler Apple'ın cihazdaki Vision çerçevesiyle yapılır.

### Kısa videolar ve OBS sesi

- "OBS sesini kaydet" açıksa (Ayarlar › OBS, varsayılan açık), OBS'in NDI ana çıkışındaki ses (OBS'teki mikrofonunuz) tablette **yalnızca son 2 saat** saklanır. Yalnızca sizin hazırladığınız kısa videoya eklenmek için kullanılır ve hiçbir yere gönderilmez. Daha eski ses kendiliğinden silinir; ayar kapatılınca hepsi silinir.
- Kısa videolar, ders notları ve kayıtlar Fotoğraflar'a ya da Galeri'ye yalnızca siz isterseniz eklenir. Uygulama fotoğraflarınızı okumaz.

### Paylaşım

Dışa aktardığınız PDF'ler, ders paketleri ve videolar yalnızca sizin seçtiğiniz yere (Dosyalar, AirDrop, paylaşım menüsü vb.) gider.

### Bilgisayar kurulum programları

Windows ve Mac kurulum programları OBS Studio, NDI Runtime ve DistroAV'ı resmi kaynaklarından indirir (GitHub, ndi.video). Bu siteler kendi gizlilik politikalarına tabidir. Kurulum programları sizin hakkınızda hiçbir veri göndermez; yalnızca bilgisayarınızdaki OBS ayarlarını değiştirir.

### Çocuklar

Uygulamalar öğretmenler için tasarlanmıştır ve kimseden kişisel veri toplamaz; buna 13 yaşından küçük çocuklar da dahildir.

### Değişiklikler ve iletişim

Bu politika değişirse bu sayfa güncellenir. Sorularınız için: [github.com/HIDIRsoftware/CastCanvas/issues](https://github.com/HIDIRsoftware/CastCanvas/issues)

---

## English

**In short:** CastCanvas and CastCanvas Cam need no account and contain no ads, tracking or analytics of our own. Your boards, recordings and settings stay on your device. Picture and sound only go to **your own devices that you choose** (OBS on your computer, your tablet) over your local network. No data comes to us. The one exception is the technical diagnostics that the Google ML Kit library sends to Google on Android (see below).

### Where your data stays

- **Boards, PDFs, drawings, scenes and settings** are stored only on your device.
- **Direct recordings** (camera and sound) are stored only on the tablet, in the app's own folder. They are copied to Photos or the Gallery only when you choose.
- **The OBS password** is stored in the Keychain on iPad and in the app's own settings on Android.
- **Handwriting-to-formula and background effects** (blur, replace or remove the background) run on the device. Your picture is never sent anywhere for them.

### Local network

CastCanvas uses the local network to:

- Send your board's picture over **NDI** to OBS on **your own computer** on the same network.
- Show OBS's live picture and sound on the tablet, and add OBS's audio to short videos.
- Control recording and scenes from the tablet (OBS WebSocket).
- **Use your phone as a camera:** receive CastCanvas Cam's picture and sound on the tablet.

These connections are only between your own devices and never leave your local network. Picture and sound travel unencrypted on the local network, so use the apps only on networks you trust (home, school, your own hotspot).

### Camera and microphone

- **CastCanvas (tablet):** the camera is used to scan the connection QR code shown in OBS and to record you in direct recording (without OBS). The microphone is used only to add your voice to direct recordings. Picture and sound stay on the tablet.
- **CastCanvas Cam (phone):** the camera is used to send your picture to your own CastCanvas tablet on the local network. The microphone is optional; sound is sent only if the tablet picks the phone's microphone. Picture and sound are sent in real time and are never recorded or stored on the phone.
- **Pairing:** the first time a tablet connects to a phone, it asks for the 4-digit code shown on the phone. The code never travels in the clear (it's verified with HMAC). The code and the names of paired devices are stored only on those two devices.
- **Bluetooth:** used to pick a Bluetooth headset's microphone and show its name. No other Bluetooth devices are scanned.

### Google ML Kit on Android

The Android tablet app uses Google's **ML Kit** library for handwriting recognition and background effects. The image processing runs on the device and your picture is never sent. However, as Google discloses, ML Kit sends these technical details to Google:
- the device model and Android version;
- the app's name and version;
- performance metrics and error codes;
- a per-installation identifier that does not identify you.

Google uses them for diagnostics and usage statistics and does not transfer them to third parties: [developers.google.com/ml-kit/android-data-disclosure](https://developers.google.com/ml-kit/android-data-disclosure). The iPad and iPhone apps contain no such library; their effects use Apple's on-device Vision framework.

### Short videos and OBS audio

- When "Record OBS audio" is on (Settings › OBS, on by default), the audio from OBS's NDI main output (your microphone in OBS) is kept on the tablet **for the last 2 hours only**. It is used only to add sound to short videos you make and is never sent anywhere. Older audio is deleted automatically, and all of it is deleted when you turn the setting off.
- Short videos, lesson notes and recordings are added to Photos or the Gallery only when you choose. The apps do not read your photos.

### Sharing

PDFs, lesson packages and videos you export go only where you choose (Files, AirDrop, the share menu, etc.).

### Computer setup programs

The Windows and Mac setup programs download OBS Studio, NDI Runtime and DistroAV from their official sources (GitHub, ndi.video). Those sites have their own privacy policies. The setup programs send no data about you; they only change OBS settings on your computer.

### Children

The apps are designed for teachers and collect no personal data from anyone, including children under 13.

### Changes and contact

If this policy changes, this page will be updated. Questions: [github.com/HIDIRsoftware/CastCanvas/issues](https://github.com/HIDIRsoftware/CastCanvas/issues)
