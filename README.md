# Kodi Handoff Edition 3.0

One APK. Official Kodi with IPTV-handoff superpowers baked in: play a movie
or show from your IPTV app (TiviMate etc.) and it opens in Kodi with the
**correct title**, **auto-downloaded subtitles that are remembered**, and
**resume from where you left off** — none of which stock Kodi does for
streams launched by another app.

Everything is inside this single file: Kodi 21.3, the title-relay, the
resume/subtitle engine, and the OpenSubtitles.com subtitle add-on, all
pre-installed and pre-configured. The only thing you type is your
OpenSubtitles.com login, once.

Works on Fire TV Stick and virtually all Android TV / Google TV boxes
(32-bit ARM build).

---

## Install (about 3 minutes)

1. **Allow sideloading**: Settings → My Fire TV → Developer options → turn on
   **Apps from Unknown Sources** (allow it for the app you install from,
   e.g. Downloader). *(Developer options hidden? Settings → My Fire TV →
   About → click the device name 7 times.)*

2. **Uninstall any existing Kodi first.** This build replaces the official
   Kodi app and is signed differently, so a regular Kodi must be removed or
   the install will fail. *(If you have a Kodi setup you care about, back it
   up first — its data will be gone.)*

3. **Install `Kodi-Handoff-Edition-3.0.apk`**:
   - With the **Downloader** app: host the APK somewhere with a direct link
     and open it in Downloader, or sideload however you prefer.
   - With **adb** from a computer:
     ```
     adb connect <FIRESTICK_IP>:5555
     adb install Kodi-Handoff-Edition-3.0.apk
     ```

4. **Open Kodi once.** On first launch it asks for your **OpenSubtitles.com**
   username and password. Enter them, or press Cancel/Back to skip (you'll
   rarely get subtitles without an account — free signup at
   opensubtitles.com). This is asked only once.

5. **Point your IPTV app at Kodi.** In TiviMate: Settings → Playback →
   Video player → **Custom player** → select **Kodi**. (Other apps: choose
   Kodi as the external player.)

That's it. No add-ons to install, no subtitle service to configure — it's
all inside.

---

## Using it

- **Play** a movie or episode in your IPTV app → it opens in Kodi with the
  right title.
- **Subtitles download automatically** — the best-rated matching subtitle
  is fetched and shown without touching a menu. To pick a different one:
  press Select during playback → speech-bubble icon → Download subtitle.
- Once downloaded for a title, a subtitle is **remembered** and reappears
  automatically next time — no re-download.
- **Resume**: stop or quit anytime. Replaying the same title jumps back to
  where you left off ("Resumed at …" appears briefly).
- **Subtitle out of sync?** Speech-bubble menu → Subtitle delay (positive =
  later); "Set as default for all media" makes it stick.

## Change or add your OpenSubtitles login later

Settings → Add-ons → My add-ons → Subtitle download services →
OpenSubtitles.com → Configure.

## Troubleshooting

- **"Failed to download subtitle (HTTP 406)"** — the free OpenSubtitles.com
  account's 20-downloads-per-day limit is used up; it resets daily at
  23:59 UTC. (Subtitles you already downloaded still work; they're
  remembered and don't count again.)
- **"No subtitles found" on a brand-new movie** — subtitles may simply not
  exist yet that early; make sure your OpenSubtitles.com login is set so all
  available results show.
- **Title/resume magic doesn't happen** — your IPTV app is launching Kodi
  directly; recheck step 5 (it must use Kodi as an external/custom player).

## About this build

- Based on official, unmodified **Kodi 21.3 "Omega"** (GPL) from kodi.tv,
  repackaged with add-ons. Subtitle add-ons and the OpenSubtitles services
  are open source (MIT/GPL). The handoff add-on and relay are original.
- Package id `org.xbmc.kodi`; signed by **ikeamrf** (`ikeamrf@gmail.com`).
  Verify with `apksigner verify --print-certs Kodi-Handoff-Edition-3.0.apk`
  — SHA-256 `91ed1bb02364f1f20e483e6e224af899ea06e3f14626c2c3e35bd92a5f988cb2`.
- Because it's sideloaded, it won't auto-update — new versions are installed
  the same way (they install over this one; same signer).
