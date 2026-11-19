# CastCanvas setup guide

CastCanvas can be used in three ways. Follow the section for the one you use:

- **Streaming and recording with OBS:** the board goes to OBS on your computer; camera and audio are in OBS. See section 2.
- **Direct recording (no OBS):** board, camera and audio are combined and recorded on the tablet. See section 3.
- **Using a phone as the camera:** the CastCanvas Cam app on the phone sends its picture and sound to the tablet. See section 4.

Section 5 lists which permissions the app asks for and why; section 6 covers common problems.

## 1. What you need

<!-- ios -->
- **iPad:** iPadOS 17 or later. Apple Pencil recommended.
<!-- /ios -->
<!-- android -->
- **Android tablet:** Android 10 or later. A tablet with a stylus is recommended.
<!-- /android -->
- **A computer for streaming with OBS:** Windows 10/11 or macOS 12 and later.
- **Network:** the tablet and the computer (or the phone) must be on the same network: 5 GHz Wi-Fi, the computer's mobile hotspot, or a cable.

## 2. Streaming with OBS

### Prepare the computer (once)

1. Open the download page: [github.com/HIDIRsoftware/CastCanvas](https://github.com/HIDIRsoftware/CastCanvas). The link is in the app too, where you can also send it to the computer:
   <!-- ios -->
   **Settings › Connection › Computer setup**.
   <!-- /ios -->
   <!-- android -->
   **Settings › About › Computer setup**.
   <!-- /android -->
2. **Windows:** download `CastCanvas-Setup-Windows.zip`, extract it and run **CastCanvas-Setup.exe**. Answer **Yes** when Windows asks for administrator permission.
3. **Mac:** download `CastCanvas-Setup-Mac.zip` and open the **CastCanvas Setup** app. It asks for your Mac password once while installing NDI.
4. The setup program installs OBS Studio, NDI Runtime and DistroAV, and configures the firewall and OBS. It skips whatever is already installed.

> If Windows says "Windows protected your PC", choose **More info › Run anyway**. If the Mac says the app "can't be verified", go to **System Settings › Privacy & Security › Open Anyway**. The setup files aren't signed with a paid certificate yet, which is why the warning appears.

### Connect the tablet to the computer

- **Wi-Fi:** join the same network as the computer, preferably 5 GHz. On Windows the easiest way is to turn on the computer's **Mobile hotspot** at 5 GHz and join it from the tablet.
- **Cable (lowest and steadiest latency):** plug a USB-C Ethernet adapter with a charging port into the tablet; connect the tablet and the computer to the same router or switch; turn the tablet's Wi-Fi off.
<!-- android -->
- **USB cable (Windows):** connect the tablet to the computer with a data cable and turn on **Settings › Connections › Mobile Hotspot and Tethering › USB tethering** on the tablet.
<!-- /android -->

### Add the board in OBS

1. In OBS: **Sources › + › NDI Source**.
<!-- ios -->
2. **Source name:** **IPAD (Yayin Tahtasi)**.
<!-- /ios -->
<!-- android -->
2. **Source name:** **ANDROID (Yayin Tahtasi)**.
<!-- /android -->
3. **Bandwidth:** Highest. **Latency Mode:** Lowest (unbuffered).
4. Right-click the source › **Transform › Reset Transform**, then drag it into place in the scene. Don't scale it; enter the size of its slot on the tablet under **Settings › Broadcast › Output area**.

### Control recording from the tablet (optional)

1. In OBS open **Tools › WebSocket Server Settings** and enable the server. The setup program does this for you.
2. On the tablet, turn on the remote under **Settings › OBS**; scan the QR code shown in OBS or type the password.
3. Start and stop recording with the record button in the top bar.

<!-- ios -->
> Illustrated steps that show the tablet's current status: **Settings › About › Connecting to OBS**.
<!-- /ios -->
<!-- android -->
> Illustrated steps that show the tablet's current status: **Settings › Connection › Connecting to OBS**.
<!-- /android -->

## 3. Direct recording (no OBS)

<!-- ios -->
1. Open **Settings › Broadcast › Direct recording** and turn on **Direct recording mode**.
<!-- /ios -->
<!-- android -->
1. Open **Settings › Direct recording** and turn on **Direct recording mode**.
<!-- /android -->
2. Choose a **Camera**:
   - the tablet's own front or back camera;
   - a USB camera or capture card (through a USB-C hub). Android asks for USB permission the first time it's plugged in;
   - a phone (CastCanvas Cam, section 4).
3. Choose a **Microphone**: the tablet's microphone, a USB microphone or wireless lavalier receiver, a wired microphone, or Bluetooth earphones. Bluetooth audio lags a little; fix it with **Audio offset**.
4. **Scenes:** use **Edit scene** to place the layers (camera, board, frame image). Set up several scenes and switch between them from the scene menu in the top bar.
5. **View:** the view button in the top bar switches between **Board**, **Corner monitor** and **Scene on screen**. With the scene on screen, the pencil button lets you edit the scene in place.
6. **Recording:** the record button in the top bar. When it stops, use the card that appears or the **Recordings** list to watch it, cut the start and end with **Trim**, share it or save it.
<!-- ios -->
   - Recordings stay on the iPad; **Save to Photos** copies one to Photos.
<!-- /ios -->
<!-- android -->
   - Recordings stay on the tablet; **Save to Gallery** copies one to the **Movies/CastCanvas** folder.
<!-- /android -->

## 4. Use a phone as the camera (CastCanvas Cam)

1. Install the **CastCanvas Cam** app on the phone (Android or iPhone) and open it. Allow the camera; also allow the microphone if you want to use the phone's microphone.
2. Connect the phone and the tablet to **the same Wi-Fi**. If a school or guest network keeps devices apart, join the tablet to **the phone's hotspot**; the tablet finds the phone by itself.
3. On the tablet, pick the phone's name in the **Camera** list of the direct recording settings (section 3, step 1).
4. Enter the **4-digit pairing code** shown on the phone. It's asked only once.
5. To use the phone's microphone, pick the phone under **Microphone**.
6. **Picture quality** and **Fast transfer (UDP)** are in the same place. With fast transfer on, a lost packet doesn't hold up the picture.

> If the phone isn't listed, use **Add phone by address** and type the address shown on the phone (e.g. `192.168.1.23:52700`). More details are in the guide inside CastCanvas Cam on the phone.

## 5. Permissions and why

CastCanvas doesn't need an account and has no ads or tracking. Picture and sound only go where you send them (to OBS, the tablet or a recording).

<!-- ios -->
### iPad

- **Local Network:** to send the board to OBS on the same network over NDI, to receive OBS's live picture and sound, and to find the OBS remote and phone cameras. Without it, OBS can't see the tablet.
- **Camera:** to scan the connection QR code in OBS and to record you in direct recording. The picture is only saved on this iPad.
- **Microphone:** to add your voice to direct recordings. Audio is only saved on this iPad.
- **Add to Photos:** to save a short video, lesson notes or a recording to Photos when you ask. Your photos aren't read.

To change them: iPad **Settings › CastCanvas**.
<!-- /ios -->
<!-- android -->
### Android

The app asks for these when it needs them:

- **Camera:** to record you with the tablet's camera or a USB camera in direct recording, and to scan the QR code in OBS.
- **Microphone:** to add your voice to direct recordings.
- **Nearby devices (Bluetooth connect, Android 12 and later):** to use Bluetooth earphones' microphone and show their name. Not needed if you don't use Bluetooth.
- **USB device:** Android also asks the first time each USB camera or capture card is plugged in.

Granted at install time, never asked:

- **Internet, network and Wi-Fi state:** to send the board to OBS, connect to a phone camera and show the tablet's address. The app doesn't connect to any internet server.
- **Wi-Fi multicast:** so OBS, the tablet and phones can find each other on the network (NDI, Bonjour/mDNS).
- **Change audio settings:** to switch to a Bluetooth earphone's microphone.
- **Keep awake:** so Wi-Fi doesn't drop into power saving and delay the picture while a phone camera is connected.

No file or storage permission is needed: recordings stay in the app's own folder and are copied to the Gallery only when you ask.

To change them: on the tablet, **Settings › Apps › CastCanvas › Permissions**.
<!-- /android -->

## 6. Troubleshooting

- **The tablet doesn't show up in OBS:**
  - Are the tablet and the computer on the same network?
  - On a Mac, is **System Settings › Privacy & Security › Local Network › OBS** on?
  - A school or guest network may keep devices apart; use the computer's hotspot or a cable.
- **The picture stutters:** use 5 GHz Wi-Fi or a cable. Set **Latency Mode** to **Low** in OBS.
- **The phone isn't found:** is CastCanvas Cam open in the foreground on the phone? Same network? Join the tablet to the phone's hotspot or use **Add phone by address**.
- **Audio is ahead of or behind the picture:** **Audio offset** under the microphone in the direct recording settings.
- **Camera or microphone doesn't work:** check the permissions in section 5.
