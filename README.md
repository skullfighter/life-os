# Life OS

Habits, meals, weight and to-dos in one app. It never resets, and every month becomes a shareable Wrapped card.
It installs on iPhone, Android, Windows and Mac straight from the browser. There's no app store, no account and no server.

## What's in this folder

| File | What it is |
|---|---|
| `index.html` | The whole app |
| `manifest.webmanifest` | Tells phones and computers the app's name, icon and colours so it can be installed |
| `sw.js` | Lets the app open and work with no internet |
| `icons/` | App icons for every platform |
| `fonts/` | The app's fonts, bundled so nothing loads from other sites |
| `.nojekyll` | A blank file GitHub Pages likes. It's hidden on Mac, which is fine. |

---

## 1. Put it online with GitHub Pages (free, about 10 minutes)

1. Sign in at **github.com** (or create a free account).
2. Click **+** at the top right, then **New repository**. Name it `life-os`, set it to **Public**, and click **Create repository**.
3. On the new page, click **uploading an existing file**. Drag in **everything inside this folder**, including the `icons` and `fonts` folders. Click **Commit changes**.
4. Go to **Settings → Pages**. Under *Build and deployment*, set Source to **Deploy from a branch**, Branch to **main** and **/ (root)**, then click **Save**.
5. Wait 1–2 minutes and refresh. GitHub shows your link, for example `https://YOUR-USERNAME.github.io/life-os/`.

That link is your app. Share it anywhere, including your Instagram bio.

> Anyone with the link can open the app, but each person's data stays on their own device. Nobody can see your ticks, weight or meals, including you when you're on someone else's phone.

## 2. Install it

| Device | How |
|---|---|
| **iPhone / iPad** | Open the link in **Safari**. Tap **Share**, then **Add to Home Screen**, then **Add**. |
| **Android** | Open the link in **Chrome**. Tap **Install app** when it pops up, or open the **⋮** menu and choose **Install app** / **Add to Home screen**. |
| **Windows / Mac (Chrome or Edge)** | Click the **install icon** at the right end of the address bar, or open the browser menu and look for **Install**. |
| **Mac (Safari)** | **File → Add to Dock**. |

Once installed, it opens full screen with its own icon and works offline. On Android and in Chrome, you can also install from **Settings → Install app** inside Life OS.

## 3. Bring your existing data over

Your Claude version and this app store data separately. To move it:

1. In the Claude version, go to **Settings → Download backup**.
2. In the installed app, go to **Settings → Restore from file** and pick that backup.

## 4. Keep your data safe

Data lives only on the device you use it on. The app reminds you monthly to **save a backup file**. Keep those files somewhere safe, such as Google Drive or iCloud. If you get a new phone, install the app again and use **Restore from file**.

## 5. Updating the app later

1. Replace `index.html` (or any file) in your GitHub repository with the new version.
2. Open `sw.js` and change `lifeos-v1` to `lifeos-v2` (then `v3` next time, and so on).
3. Commit. Phones pick up the new version the next time the app is opened. Sometimes it takes a second open.

Nobody's data is touched by an update.

---

## Later: App Store and Play Store

This app is already a proper installable web app (a PWA), so it can be packaged for the stores without rewriting it:

- **PWABuilder** (pwabuilder.com). Paste your GitHub link and it generates a Google Play package and an iOS project.
- **Capacitor**, if you want native features like reminders or home-screen widgets.

Costs and rules to plan for:

- **Apple:** Developer Program membership is $99/year, and building for iOS needs a Mac with Xcode. Apple can reject apps that feel like a wrapped website (guideline 4.2), so add something native first, such as daily reminder notifications or a widget.
- **Google Play:** a one-time $25 fee. New personal developer accounts must run a closed test with at least 12 testers for 14 days before going public.

## Privacy, in one line

Life OS collects nothing. There are no accounts, analytics or trackers, and all data stays on your device unless you export a backup yourself.

Fonts: Unbounded, Manrope and JetBrains Mono, all under the SIL Open Font License (see `fonts/LICENSE.txt`).
