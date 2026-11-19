# CastCanvas Cam kurulum rehberi

CastCanvas Cam, telefonunuzun kamerasını (ve isterseniz mikrofonunu) aynı ağdaki **CastCanvas** tabletine kamera olarak verir. Tablet bu görüntüyü doğrudan çekimde (OBS'siz) sahnesine koyar ve kaydeder. Telefonda kayıt yapılmaz, görüntü internete çıkmaz.

## 1. Gerekenler

- **Telefon:** Android 8 ya da üstü, veya iOS 17 ya da üstü bir iPhone.
- **Tablet:** CastCanvas yüklü bir iPad ya da Android tablet. Tablette **doğrudan çekim** kullanılır.
- **Ağ:** telefon ve tablet aynı ağda: aynı Wi-Fi (tercihen 5 GHz) ya da telefonun etkin noktası.

## 2. Bağlanma (ilk sefer)

1. CastCanvas Cam'i açın. **Kamera** iznini verin. Telefonun mikrofonunu da kullanacaksanız **Mikrofon** iznini de verin.
2. Telefonu ve tableti **aynı Wi-Fi'a** bağlayın.
   - Okul, otel ya da misafir ağları cihazları birbirinden ayırır. O zaman telefonda **etkin noktayı** açıp tableti ona bağlayın; tablet telefonu kendiliğinden bulur.
3. Tablette CastCanvas'ı açın, doğrudan çekim ayarlarında **Kamera** listesinden bu telefonun adını seçin.
4. Telefonda **Eşleştir**'e dokunun: **4 haneli eşleştirme kodu** ve telefonun adresi görünür. Kodu tablete girin.
5. Kod yalnızca ilk seferde sorulur. Sonra telefonda uygulamayı açmanız yeter; tablet kendiliğinden bağlanır.

> Tablet telefonu listede göstermezse tabletteki **Telefonu adresle ekle**'ye telefon ekranındaki adresi (ör. `192.168.1.23:52700`) yazın.

## 3. Kullanım

- **Önde tutun:** görüntü yalnızca uygulama ekranda açıkken gider. Telefonu kilitlemeyin, başka uygulamaya geçmeyin.
- **Düğmeler** (dokununca görünür, birkaç saniye sonra gizlenir):
  - **Çevir:** ön ve arka kamera arasında geçer.
  - **Yakınlık:** yakınlaştırma (0,5×, 1×, 2× gibi).
  - **Ayarlar:** görüntü, gelişmiş ayarlar, mikrofon ve görünüm.
  - **Karart:** ekranı karartır, pil ve ısınma azalır; görüntü gitmeye devam eder. Açmak için ekrana dokunun.
  - **Eşleştir:** eşleştirme kodunu ve adresi gösterir. **Yeni kod** eskisini geçersiz kılar; tablette yeniden girilir.
- **Odak:** önizlemede bir yere dokunun; odak ve parlaklık oraya göre ayarlanıp kilitlenir. Tablette de sahne düzenleyicide kamera görüntüsüne çift dokunarak odaklanabilirsiniz.
- **Ayarlar** (telefonda ya da tablette, ikisi de birbirini görür):
  - **Görüntü:** parlaklık, odak, ışık ve renk kilidi, fener.
  - **Gelişmiş ayarlar:** yüze öncelik, beyaz dengesi, elle odak, elle pozlama (ISO, enstantane), görüntü sabitleme, yön kilidi.
  <!-- android -->
  - **Titreme önleme:** floresan ya da LED ışıkta görüntü titriyorsa açın; Türkiye'de 50 Hz.
  <!-- /android -->
  <!-- ios -->
  - **Sabitleme:** iPhone'da optik sabitleme her zaman açıktır; ayardan elektronik sabitleme açılıp kapanır (biraz gecikme ekler).
  <!-- /ios -->
  - **Mikrofon:** telefonun mikrofonu, USB mikrofon (kablosuz yaka mikrofonu alıcısı dahil), kablolu mikrofon ya da Bluetooth kulaklık. En iyi ses USB-C alıcılı yaka mikrofonundan gelir; Bluetooth kulaklık telefon görüşmesi kalitesindedir.
  - **Görünüm:** telefonda önizleme, ızgara ve terazi.
- **Tablette:** **Görüntü kalitesi** (standart, yüksek, en yüksek) ve **Hızlı aktarım (UDP)**. Hızlı aktarım açıkken kaybolan bir paket görüntüyü bekletmez, takılma azalır.

## 4. İpuçları

- Telefonu bir tripoda ya da tutucuya takın; uzun derslerde şarja takılı kalsın.
- Tablet ve telefon modeme ne kadar yakınsa gecikme o kadar az olur. 5 GHz Wi-Fi, 2,4 GHz'den daha iyidir.
- Ders sırasında bildirim gelmesin diye **Rahatsız Etmeyin**'i açın.
- Telefon ısınırsa tablet uyarır. **Karart**'ı kullanın, telefonu kılıfından çıkarın.

## 5. İzinler ve nedenleri

CastCanvas Cam hesap açtırmaz, reklam ve takip içermez. Görüntü ve ses yalnızca yerel ağdaki tablete gider; telefonda kaydedilmez, internete çıkmaz.

<!-- android -->
### Android

Uygulama bunları sorar:

- **Kamera (zorunlu):** görüntünüzü tablete göndermek için.
- **Mikrofon (isteğe bağlı):** tablet telefonun mikrofonunu seçerse sesinizi tablete göndermek için. Vermezseniz yalnızca görüntü gider.
- **Yakındaki cihazlar (Bluetooth bağlantısı, Android 12 ve üstü, isteğe bağlı):** Bluetooth kulaklığın mikrofonunu kullanmak ve adını göstermek için.

Kurulumda verilen, ayrıca sorulmayan izinler:

- **İnternet ve ağ durumu:** görüntüyü ve sesi yerel ağdaki tablete göndermek, tabletin telefonu ağda bulması için. Uygulama internette bir sunucuya bağlanmaz.
- **Wi-Fi durumu ve uyanık tutma:** görüntü giderken Wi-Fi'ı düşük gecikme kipinde tutmak için (güç tasarrufu paketleri bekletmesin).
- **Ses ayarlarını değiştirme:** Bluetooth kulaklığın mikrofonuna geçmek için.

Değiştirmek için: telefonda **Ayarlar › Uygulamalar › CastCanvas Cam › İzinler**.
<!-- /android -->
<!-- ios -->
### iPhone

- **Kamera (zorunlu):** görüntünüzü aynı ağdaki CastCanvas tabletine göndermek için.
- **Mikrofon (isteğe bağlı):** tablet isterse sesinizi tablete göndermek için.
- **Yerel Ağ (zorunlu):** tabletin bu telefonu bulup bağlanabilmesi için. Kapalıysa tablet telefonu göremez.

Değiştirmek için: iPhone **Ayarlar › CastCanvas Cam**.
<!-- /ios -->

## 6. Sorun giderme

- **Tablet telefonu bulamıyor:**
  - Telefonda CastCanvas Cam önde açık mı?
  - İkisi aynı Wi-Fi'da mı? Misafir ağıysa tableti telefonun etkin noktasına bağlayın.
  - Olmazsa tablette **Telefonu adresle ekle**.
<!-- ios -->
  - iPhone'da **Ayarlar › CastCanvas Cam › Yerel Ağ** açık mı?
<!-- /ios -->
- **Tablet "telefon başka tablette" diyor:** telefon başka bir tablete bağlı. Tablette **Telefonu bu tablete al**'a dokunun.
- **Kod yanlış:** telefonda **Eşleştir**'e dokunup ekrandaki kodu yeniden girin. Art arda 5 yanlış denemeden sonra telefon 1 dakika bekletir.
- **Görüntü takılıyor ya da gecikiyor:** 5 GHz Wi-Fi'a geçin, tableti ve telefonu modeme yaklaştırın, tablette **Hızlı aktarım (UDP)** açık olsun. Gerekirse **Görüntü kalitesi**'ni düşürün.
- **Ses gelmiyor:** telefonda mikrofon izni verildi mi? Tablette mikrofon olarak telefon seçili mi?
