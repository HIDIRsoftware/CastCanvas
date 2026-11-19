# CastCanvas Cam setup guide

CastCanvas Cam turns your phone's camera (and, if you like, its microphone) into a camera for the **CastCanvas** tablet on the same network. The tablet puts the picture into its scene in direct recording (no OBS) and records it. Nothing is recorded on the phone, and the picture never leaves your network.

## 1. What you need

- **Phone:** Android 8 or later, or an iPhone with iOS 17 or later.
- **Tablet:** an iPad or Android tablet with CastCanvas. The tablet uses **direct recording**.
- **Network:** the phone and the tablet on the same network: the same Wi-Fi (preferably 5 GHz) or the phone's hotspot.

## 2. Connecting (first time)

1. Open CastCanvas Cam. Allow the **Camera**. If you want to use the phone's microphone, allow the **Microphone** too.
2. Connect the phone and the tablet to **the same Wi-Fi**.
   - School, hotel and guest networks keep devices apart. In that case turn on the phone's **hotspot** and join it from the tablet; the tablet finds the phone by itself.
3. Open CastCanvas on the tablet and pick this phone's name in the **Camera** list of the direct recording settings.
4. On the phone, tap **Pair**: the **4-digit pairing code** and the phone's address appear. Enter the code on the tablet.
5. The code is asked only the first time. After that, just open the app on the phone; the tablet connects by itself.

> If the tablet doesn't list the phone, type the address shown on the phone (e.g. `192.168.1.23:52700`) into **Add phone by address** on the tablet.

## 3. Using it

- **Keep it in front:** the picture is only sent while the app is open on screen. Don't lock the phone or switch to another app.
- **Buttons** (appear when you tap, hide after a few seconds):
  - **Flip:** switches between the front and back cameras.
  - **Zoom:** zoom steps such as 0.5×, 1×, 2×.
  - **Settings:** picture, advanced settings, microphone and display.
  - **Dim:** darkens the screen to save battery and heat; the picture keeps going. Tap the screen to wake it.
  - **Pair:** shows the pairing code and address. **New code** replaces the old one; it must be entered again on the tablet.
- **Focus:** tap a spot in the preview; focus and brightness are set there and locked. On the tablet you can also double-tap the camera picture in the scene editor.
- **Settings** (on the phone or the tablet; each sees the other's changes):
  - **Picture:** brightness, focus, lock light and colour, torch.
  - **Advanced settings:** face priority, white balance, manual focus, manual exposure (ISO, shutter), stabilization, rotation lock.
  <!-- android -->
  - **Anti-flicker:** turn it on if the picture flickers under fluorescent or LED lights; 50 Hz in Europe and Turkey, 60 Hz in the Americas.
  <!-- /android -->
  <!-- ios -->
  - **Stabilization:** on iPhone optical stabilization is always on; the setting turns electronic stabilization on or off (it adds a little latency).
  <!-- /ios -->
  - **Microphone:** the phone's microphone, a USB microphone (including wireless lavalier receivers), a wired microphone or a Bluetooth headset. The best sound comes from a lavalier with a USB-C receiver; a Bluetooth headset sounds like a phone call.
  - **Display:** preview on the phone, grid and level.
- **On the tablet:** **Picture quality** (standard, high, highest) and **Fast transfer (UDP)**. With fast transfer on, a lost packet doesn't hold up the picture, so there's less stutter.

## 4. Tips

- Put the phone on a tripod or holder; keep it charging during long lessons.
- The closer the tablet and the phone are to the router, the lower the latency. 5 GHz Wi-Fi is better than 2.4 GHz.
- Turn on **Do Not Disturb** so notifications don't interrupt the lesson.
- If the phone gets hot, the tablet warns you. Use **Dim** and take the phone out of its case.

## 5. Permissions and why

CastCanvas Cam doesn't need an account and has no ads or tracking. Picture and sound only go to the tablet on your local network; nothing is recorded on the phone or sent to the internet.

<!-- android -->
### Android

The app asks for these:

- **Camera (required):** to send your picture to the tablet.
- **Microphone (optional):** to send your voice to the tablet if it picks the phone's microphone. Without it only the picture is sent.
- **Nearby devices (Bluetooth connect, Android 12 and later, optional):** to use a Bluetooth headset's microphone and show its name.

Granted at install time, never asked:

- **Internet and network state:** to send picture and sound to the tablet on your local network and let the tablet find the phone. The app doesn't connect to any internet server.
- **Wi-Fi state and keep awake:** to hold Wi-Fi in low-latency mode while the picture is being sent, so power saving doesn't hold packets back.
- **Change audio settings:** to switch to a Bluetooth headset's microphone.

To change them: on the phone, **Settings › Apps › CastCanvas Cam › Permissions**.
<!-- /android -->
<!-- ios -->
### iPhone

- **Camera (required):** to send your picture to the CastCanvas tablet on the same network.
- **Microphone (optional):** to send your voice to the tablet when it asks for it.
- **Local Network (required):** so the tablet can find this phone and connect to it. Without it the tablet can't see the phone.

To change them: iPhone **Settings › CastCanvas Cam**.
<!-- /ios -->

## 6. Troubleshooting

- **The tablet can't find the phone:**
  - Is CastCanvas Cam open in the foreground on the phone?
  - Are both on the same Wi-Fi? If it's a guest network, join the tablet to the phone's hotspot.
  - Otherwise use **Add phone by address** on the tablet.
<!-- ios -->
  - On the iPhone, is **Settings › CastCanvas Cam › Local Network** on?
<!-- /ios -->
- **The tablet says the phone is on another tablet:** the phone is connected to another tablet. Tap **Take the phone to this tablet**.
- **Wrong code:** tap **Pair** on the phone and enter the code on screen again. After 5 wrong tries in a row, the phone waits 1 minute.
- **The picture stutters or lags:** switch to 5 GHz Wi-Fi, move the tablet and the phone closer to the router, and keep **Fast transfer (UDP)** on. If needed, lower **Picture quality**.
- **No sound:** did you allow the microphone on the phone? Is the phone selected as the microphone on the tablet?
