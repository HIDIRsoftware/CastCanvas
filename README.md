<p align="center">
  <img src="castcanvas-icon.png" width="128" alt="CastCanvas">
</p>

<h1 align="center">CastCanvas · Kurulum / Setup</h1>

<p align="center">
  <a href="https://github.com/alihdr2/CastCanvas/releases/latest/download/CastCanvas-Setup-Windows.zip"><b>⬇ Windows (.zip)</b></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/alihdr2/CastCanvas/releases/latest/download/CastCanvas-Setup-Mac.zip"><b>⬇ Mac (.zip)</b></a>
</p>

---

## Türkçe

iPad'deki **CastCanvas** tahtasını OBS'te yayına almak için bilgisayarı tek seferde hazırlar:

- **OBS Studio**, **NDI Runtime** ve **DistroAV** (OBS için NDI eklentisi) kurulur. Kurulu olanlar atlanır, eski sürümler güncellenir.
- Programlar resmi kaynaklarından indirilir ve kurulmadan önce doğrulanır (SHA-256 özeti ve dijital imza).
- OBS iPad için ayarlanır: kaydı iPad'den başlatma (WebSocket) ve iPad'de canlı OBS görüntüsü (NDI ana çıkışı).
- **Windows:** güvenlik duvarı izinleri verilir. İsterseniz 5 GHz mobil etkin nokta da açılır.
- **Mac:** gerekli izinler (Yerel Ağ, Kamera, Mikrofon) tek tek gösterilir. Bitişte iPad'in okutacağı kare kod çıkar.

### Nasıl kurulur

| | Windows 10/11 | macOS 12 ve üstü |
|---|---|---|
| 1 | Zip'i indirin. Sağ tık › **Tümünü ayıkla** | Zip'i indirin. Açılınca **CastCanvas Setup** uygulaması çıkar |
| 2 | **CastCanvas-Setup.exe**'ye çift tıklayın | Uygulamayı açın |
| 3 | Windows yönetici izni sorar: **Evet** | NDI kurulurken Mac parolanızı bir kez sorar |

> **"Bilgisayarınız korundu" / "Doğrulanamadı" uyarısı:** kurulum dosyaları henüz ücretli bir sertifikayla imzalanmadığı için çıkar. Dosyalar bu sayfadan indirildiyse güvenlidir.
> - **Windows:** **Ek bilgi** › **Yine de çalıştır**. Tarayıcı uyarırsa **Sakla** deyin.
> - **Mac:** uygulamayı bir kez açmayı deneyin, sonra **Sistem Ayarları › Gizlilik ve Güvenlik** › **Yine de Aç** deyin.

Kurulumdan sonra iPad'de **CastCanvas › Ayarlar › OBS** bölümünü açın ve kurulumun gösterdiği bilgileri girin (Mac'te kare kodu okutun). OBS'te kaynağı ekleyin: **Kaynaklar › + › NDI Source › "IPAD (Yayin Tahtasi)"**.

---

## English

Gets your computer ready to bring the **CastCanvas** board from your iPad into OBS, in one go:

- Installs **OBS Studio**, **NDI Runtime** and **DistroAV** (the NDI plugin for OBS). Programs that are already installed are skipped; old versions are updated.
- Downloads each program from its official source and verifies it before installing (SHA-256 checksum and digital signature).
- Sets up OBS for the iPad: start recording from the iPad (WebSocket) and a live OBS picture on the iPad (NDI main output).
- **Windows:** adds the firewall permissions. Optionally, it turns on a 5 GHz Mobile Hotspot.
- **Mac:** walks you through the permissions OBS needs (Local Network, Camera, Microphone). At the end it shows a QR code for the iPad to scan.

### How to install

| | Windows 10/11 | macOS 12 or later |
|---|---|---|
| 1 | Download the zip. Right-click › **Extract All** | Download the zip. Opening it gives you the **CastCanvas Setup** app |
| 2 | Double-click **CastCanvas-Setup.exe** | Open the app |
| 3 | Windows asks for administrator permission: **Yes** | Your Mac asks for your password once while NDI is installed |

> **"Windows protected your PC" / "cannot be verified" warning:** it appears because the setup files are not yet signed with a paid certificate. Files downloaded from this page are safe.
> - **Windows:** **More info** › **Run anyway**. If your browser warns you, choose **Keep**.
> - **Mac:** try to open the app once, then go to **System Settings › Privacy & Security** › **Open Anyway**.

After setup, open **CastCanvas › Settings › OBS** on the iPad and enter the details the setup shows (on a Mac, scan the QR code). Then add the source in OBS: **Sources › + › NDI Source › "IPAD (Yayin Tahtasi)"**.
