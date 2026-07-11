# Kodi Handoff Edition 3.0

Play a movie or show from your IPTV app (like TiviMate) and it opens in Kodi
with the **correct title**, **subtitles that download automatically and are
remembered**, and it **resumes from where you left off**. Everything is in one
app — you don't install any add-ons.

Works on **Fire TV Stick** and most **Android TV / Google TV** devices.

**Downloader code: `5040864`**

All versions: https://github.com/chethanjsgit/kodi-handoff-edition/releases

---

## Install — just follow these steps in order

You'll do this once. Take about 5 minutes.

### Step 1 — Get the "Downloader" app

- **Fire TV Stick:** from the Fire TV home screen, search (magnifying glass) for
  **Downloader**, and install the orange app by AFTVnews.
- **Android TV / Google TV:** open the **Google Play Store**, search for
  **Downloader**, and install it.

### Step 2 — Turn on app installing (do this once)

**On Fire TV Stick:**
1. Go to **Settings** (the gear icon) → **My Fire TV** → **Developer options**.
   - Don't see Developer options? Go to **Settings → My Fire TV → About**, then
     click on the **device name** 7 times until it says you're a developer, then
     go back.
2. Turn on **Install unknown apps** (or "Apps from Unknown Sources"), and in the
   list, turn it **ON for Downloader**.

**On Android TV / Google TV:**
1. Go to **Settings → System → About**, scroll to **Android TV OS build**, and
   click it **7 times** until it says "You are now a developer."
2. Go to **Settings → Apps → Security & restrictions → Unknown sources**, and
   turn it **ON for Downloader**.

### Step 3 — Remove any old Kodi first (important)

If you already have Kodi installed, **uninstall it** before continuing, or the
new app won't install. (Settings → Applications → find Kodi → Uninstall.)
If you've never had Kodi, skip this step.

### Step 4 — Download and install with the code

1. Open the **Downloader** app.
2. In the box at the top, type this code: **`5040864`** and press **Go**.
3. Wait for it to download (it's about 65 MB).
4. When it finishes, a screen asks **"Do you want to install this
   application?"** — choose **Install**.
5. After it installs, choose **Done** (not "Open" yet — Downloader will offer to
   delete the downloaded file; you can say **Delete** to save space).

### Step 5 — Open Kodi and sign in to subtitles (once)

1. Open **Kodi** (it may say "Preparing for first run" — wait a moment).
2. It will ask for your **OpenSubtitles.com username**, then **password**.
   Type them in.
   - Don't have an account? It's free — sign up at **opensubtitles.com** first
     (an OpenSubtitles.com account is what lets subtitles download).
   - Want to skip for now? Press **Back** on each prompt. You can add it later.
3. That's the only setup. It won't ask again.

### Step 6 — Tell your IPTV app to use Kodi

In **TiviMate**: Settings → **Playback** → **Video player** → **Custom player**
→ choose **Kodi**.
(Other IPTV apps: wherever you pick an "external" or "custom" player, choose
**Kodi**.)

**Done!** Now play anything in your IPTV app and it opens in Kodi with the title,
subtitles, and resume all handled for you.

---

## How to use it day to day

- **Just play** a movie or episode in your IPTV app — it opens in Kodi.
- **Subtitles come on by themselves** — the best-rated match is downloaded and
  shown automatically. To pick a different one: press the **Select/OK** button
  during playback, click the **speech-bubble icon**, then **Download subtitle**.
- A subtitle you've used for a title is **remembered** — next time it comes back
  automatically, no downloading again.
- **Resume:** stop or leave anytime. Play the same title again and it jumps back
  to where you stopped ("Resumed at …" flashes on screen).
- **Subtitles a little early or late?** During playback: **Select/OK** →
  speech-bubble icon → **Subtitle delay**, and nudge it. Choose "Set as default
  for all media" to keep it.

## If something's not working

- **"Failed to download subtitle (HTTP 406)"** — your free OpenSubtitles.com
  account has used its 20 downloads for the day. It resets every day. Subtitles
  you already have still work and don't count again.
- **"No subtitles found"** on a brand-new movie — subtitles may not exist yet
  that early. Make sure your OpenSubtitles.com login is entered (Step 5).
- **The title/subtitles/resume don't happen** — your IPTV app is opening Kodi
  the wrong way. Recheck Step 6: it must use **Kodi** as the custom/external
  player.
- **Need to change your OpenSubtitles login later** — in Kodi: Settings →
  Add-ons → My add-ons → Subtitle download services → OpenSubtitles.com →
  Configure.

## Getting a newer version later

New versions are posted here: **https://github.com/chethanjsgit/kodi-handoff-edition/releases**
Install a newer one the same way (Downloader code above) — it installs right
over the old one and keeps your settings and history.

---

*Built from official Kodi 21.3 "Omega" (open source) with the handoff features
added. App id `org.xbmc.kodi`, signed by ikeamrf (). Because
it's installed outside the app store, it won't auto-update — get new versions
from the releases link above.*
