# CastCanvas kurulum rehberi

CastCanvas üç şekilde kullanılır. Hangisini kullanacaksanız o bölümü izleyin:

- **OBS ile yayın ve kayıt:** tahta bilgisayardaki OBS'e gider; kamera ve ses OBS'tedir. Bkz. bölüm 2.
- **Doğrudan çekim (OBS'siz):** tahta, kamera ve ses tablette birleşir, kayıt tablette yapılır. Bkz. bölüm 3.
- **Telefonu kamera yapmak:** telefondaki CastCanvas Cam uygulaması görüntüyü ve sesi tablete gönderir. Bkz. bölüm 4.

Uygulamanın hangi izni neden istediği bölüm 5'te, sık karşılaşılan sorunlar bölüm 6'da.

## 1. Gerekenler

<!-- ios -->
- **iPad:** iPadOS 17 ya da üstü. Apple Pencil önerilir.
<!-- /ios -->
<!-- android -->
- **Android tablet:** Android 10 ya da üstü. Kalemli bir tablet önerilir.
<!-- /android -->
- **OBS ile yayın için bilgisayar:** Windows 10/11 ya da macOS 12 ve üstü.
- **Ağ:** tablet ile bilgisayar (ya da telefon) aynı ağda olmalı. 5 GHz Wi-Fi, bilgisayarın mobil etkin noktası ya da kablo.

## 2. OBS ile yayın

### Bilgisayarı hazırlayın (bir kez)

1. İndirme sayfasını açın: [github.com/HIDIRsoftware/CastCanvas](https://github.com/HIDIRsoftware/CastCanvas). Bağlantı uygulamada da var; oradan bilgisayara da gönderebilirsiniz:
   <!-- ios -->
   **Ayarlar › Bağlantı › Bilgisayar kurulumu**.
   <!-- /ios -->
   <!-- android -->
   **Ayarlar › Hakkında › Bilgisayar kurulumu**.
   <!-- /android -->
2. **Windows:** `CastCanvas-Setup-Windows.zip`'i indirin, ayıklayın, **CastCanvas-Setup.exe**'yi çalıştırın. Yönetici izni sorulunca **Evet**.
3. **Mac:** `CastCanvas-Setup-Mac.zip`'i indirin, **CastCanvas Setup** uygulamasını açın. NDI kurulurken Mac parolası bir kez sorulur.
4. Kurulum programı OBS Studio, NDI Runtime ve DistroAV'ı kurar, güvenlik duvarını ve OBS'i ayarlar. Kurulu olanları atlar.

> Windows "bilgisayarınız korundu" derse **Ek bilgi › Yine de çalıştır**. Mac "doğrulanamadı" derse **Sistem Ayarları › Gizlilik ve Güvenlik › Yine de Aç**. Kurulum dosyaları henüz ücretli bir sertifikayla imzalı olmadığı için bu uyarı çıkar.

### Tableti bilgisayara bağlayın

- **Wi-Fi:** tableti bilgisayarla aynı ağa bağlayın, tercihen 5 GHz. Windows'ta bilgisayarın **Mobil etkin nokta**'sını 5 GHz'de açıp tableti ona bağlamak en kolayıdır.
- **Kablo (en düşük ve en kararlı gecikme):** tablete şarj girişli bir USB-C Ethernet adaptörü takın; tablet ve bilgisayar aynı modemde ya da switch'te olsun; tabletin Wi-Fi'ını kapatın.
<!-- android -->
- **USB kablo (Windows):** tableti veri kablosuyla bilgisayara takın, tablette **Ayarlar › Bağlantılar › Mobil Erişim Noktası ve Bağlantı Paylaşımı › USB bağlantı paylaşımı**'nı açın.
<!-- /android -->

### OBS'te tahtayı ekleyin

1. OBS'te **Kaynaklar › + › NDI Source**.
<!-- ios -->
2. **Source name:** **IPAD (Yayin Tahtasi)**.
<!-- /ios -->
<!-- android -->
2. **Source name:** **ANDROID (Yayin Tahtasi)**.
<!-- /android -->
3. **Bandwidth:** Highest. **Latency Mode:** Lowest (unbuffered).
4. Kaynağa sağ tık › **Dönüştür › Dönüştürmeyi Sıfırla**, sonra sahnedeki yerine sürükleyin. Büyütüp küçültmeyin; boşluğun ölçüsünü tablette **Ayarlar › Yayın › Yayın alanı**'na girin.

### Kaydı tabletten yönetin (isteğe bağlı)

1. OBS'te **Araçlar › WebSocket Sunucu Ayarları**'nı açın, sunucuyu etkinleştirin. Kurulum programı bunu kendisi yapar.
2. Tablette **Ayarlar › OBS**'te kumandayı açın; OBS'teki kare kodu okutun ya da parolayı yazın.
3. Üst çubuktaki kayıt düğmesiyle kaydı başlatıp durdurun.

<!-- ios -->
> Resimli ve tabletin o anki durumunu gösteren adımlar: **Ayarlar › Hakkında › OBS'e bağlanma rehberi**.
<!-- /ios -->
<!-- android -->
> Resimli ve tabletin o anki durumunu gösteren adımlar: **Ayarlar › Bağlantı › OBS'e bağlanma rehberi**.
<!-- /android -->

## 3. Doğrudan çekim (OBS'siz)

<!-- ios -->
1. **Ayarlar › Yayın › Doğrudan çekim**'i açın ve **Doğrudan çekim modu**'nu açın.
<!-- /ios -->
<!-- android -->
1. **Ayarlar › Doğrudan çekim**'i açın ve **Doğrudan çekim modu**'nu açın.
<!-- /android -->
2. **Kamera** seçin:
   - tabletin kendi ön ya da arka kamerası;
   - USB kamera ya da capture kart (USB-C hub ile). Android ilk takışta USB izni sorar;
   - telefon (CastCanvas Cam, bölüm 4).
3. **Mikrofon** seçin: tabletin mikrofonu, USB mikrofon ya da kablosuz yaka mikrofonu alıcısı, kablolu mikrofon ya da Bluetooth kulaklık. Bluetooth kulaklıkta ses biraz gecikir; **Ses kaydırma** ile düzeltin.
4. **Sahneler:** **Sahneyi düzenle** ile katmanları (kamera, tahta, çerçeve resmi) yerleştirin. Birden çok sahne kurup üst çubuktaki sahne menüsünden geçin.
5. **Görünüm:** üst çubuktaki görünüm düğmesi **Tahta**, **Köşede monitör** ve **Sahne ekranda** arasında geçer. Sahne ekrandayken kalem simgesiyle sahneyi yerinde düzenleyebilirsiniz.
6. **Kayıt:** üst çubuktaki kayıt düğmesi. Kayıt bitince çıkan kartta ya da **Kayıtlar** listesinde: izleyin, **Kırp** ile başını ve sonunu kesin, paylaşın ya da kaydedin.
<!-- ios -->
   - Kayıtlar iPad'de kalır; **Fotoğraflar'a kaydet** ile Fotoğraflar'a geçer.
<!-- /ios -->
<!-- android -->
   - Kayıtlar tablette kalır; **Galeriye kaydet** ile Galeri'de **Movies/CastCanvas** klasörüne geçer.
<!-- /android -->

## 4. Telefonu kamera yapın (CastCanvas Cam)

1. Telefona **CastCanvas Cam** uygulamasını kurun (Android ya da iPhone) ve açın. Kamera iznini verin; telefon mikrofonunu da kullanacaksanız mikrofon iznini de.
2. Telefonu ve tableti **aynı Wi-Fi'a** bağlayın. Okul ya da misafir ağı cihazları birbirinden ayırıyorsa tableti **telefonun etkin noktasına** bağlayın; tablet telefonu kendiliğinden bulur.
3. Tablette doğrudan çekim ayarlarının **Kamera** listesinde telefonun adını seçin (bölüm 3, 1. adım).
4. Telefon ekranındaki **4 haneli eşleştirme kodunu** tablete girin. Kod bir kez sorulur.
5. Telefonun mikrofonunu kullanmak için **Mikrofon**'da telefonu seçin.
6. **Görüntü kalitesi** ve **Hızlı aktarım (UDP)** ayarları aynı yerde. Hızlı aktarım açıkken kaybolan bir paket görüntüyü bekletmez.

> Telefon listede çıkmazsa **Telefonu adresle ekle** ile telefon ekranındaki adresi (ör. `192.168.1.23:52700`) yazın. Ayrıntılar telefondaki CastCanvas Cam'in kendi rehberinde.

## 5. İzinler ve nedenleri

CastCanvas hesap açtırmaz, reklam ve takip içermez. Görüntü ve ses yalnızca sizin seçtiğiniz yere (OBS'e, tablete ya da kayda) gider.

<!-- ios -->
### iPad

- **Yerel Ağ:** tahtayı NDI ile aynı ağdaki OBS'e göndermek, OBS'in canlı görüntüsünü ve sesini almak, OBS kumandası ve telefon kamerasını bulmak için. Kapalıysa OBS tableti göremez.
- **Kamera:** OBS'teki bağlanma kare kodunu okutmak ve doğrudan çekimde sizi kaydetmek için. Görüntü yalnızca bu iPad'e kaydedilir.
- **Mikrofon:** doğrudan çekimde sesinizi kayda eklemek için. Ses yalnızca bu iPad'e kaydedilir.
- **Fotoğraflar'a ekleme:** kısa videoyu, ders notunu ya da kaydı siz isteyince Fotoğraflar'a kaydetmek için. Fotoğraflarınız okunmaz.

Değiştirmek için: iPad **Ayarlar › CastCanvas**.
<!-- /ios -->
<!-- android -->
### Android

Uygulama bunları kullanırken sorar:

- **Kamera:** doğrudan çekimde tabletin kamerası ya da USB kamera ile sizi kaydetmek ve OBS'teki kare kodu okutmak için.
- **Mikrofon:** doğrudan çekimde sesinizi kayda eklemek için.
- **Yakındaki cihazlar (Bluetooth bağlantısı, Android 12 ve üstü):** Bluetooth kulaklığın mikrofonunu seçmek ve adını göstermek için. Bluetooth kullanmıyorsanız vermeniz gerekmez.
- **USB aygıtı:** her USB kamera ya da capture kart ilk takılınca Android ayrıca sorar.

Kurulumda verilen, ayrıca sorulmayan izinler:

- **İnternet, ağ ve Wi-Fi durumu:** tahtayı OBS'e göndermek, telefon kamerasına bağlanmak ve tabletin adresini göstermek için. Uygulama internette bir sunucuya bağlanmaz.
- **Wi-Fi çoklu yayın:** OBS'in ve telefonların ağda birbirini bulması (NDI, Bonjour/mDNS) için.
- **Ses ayarlarını değiştirme:** Bluetooth kulaklığın mikrofonuna geçmek için.
- **Uyanık tutma:** telefon kamerası bağlıyken Wi-Fi'ın güç tasarrufuna geçip görüntüyü geciktirmemesi için.

Dosya ve depolama izni istenmez: kayıtlar uygulamanın kendi klasöründe durur, Galeri'ye yalnızca siz isteyince kopyalanır.

Değiştirmek için: tablette **Ayarlar › Uygulamalar › CastCanvas › İzinler**.
<!-- /android -->

## 6. Sorun giderme

- **Tablet OBS'te görünmüyor:**
  - Tablet ile bilgisayar aynı ağda mı?
  - Mac'te **Sistem Ayarları › Gizlilik ve Güvenlik › Yerel Ağ › OBS** açık mı?
  - Okul ya da misafir ağı cihazları ayırıyor olabilir; bilgisayarın etkin noktasını ya da kabloyu kullanın.
- **Görüntü takılıyor:** 5 GHz Wi-Fi ya da kablo kullanın. OBS'te **Latency Mode**'u **Low**'a alın.
- **Telefon bulunamıyor:** telefonda CastCanvas Cam önde açık mı? Aynı ağda mı? Tableti telefonun etkin noktasına bağlayın ya da **Telefonu adresle ekle**'yi kullanın.
- **Ses görüntüden geride ya da önde:** doğrudan çekim ayarlarında mikrofonun altındaki **Ses kaydırma**.
- **Kamera ya da mikrofon çalışmıyor:** bölüm 5'teki izinleri kontrol edin.
