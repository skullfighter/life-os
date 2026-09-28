# Life OS

Habits, meals, weight and to-dos in one app. It never resets, and every month becomes a shareable Wrapped card.
It installs on iPhone, Android, Windows and Mac straight from the browser. There's no app store, no account and no server.

## What's in this folder

| File | What it is |
|---|---|
| `index.html` | The whole app |
| `manifest.webmanifest` | Tells phones and computers the app's name, icon and colours so it can be installed |
| `sw.js` | Lets the app open and work with no internet |
| `config.js` | Your settings. Put your GoatCounter code here to count installs (see below) |
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

## 4. Count how many people use it (optional, free)

The app can count **anonymous** numbers for you with GoatCounter, a free, cookie-free counter that doesn't need a consent banner.

1. Go to **goatcounter.com** and sign up. Pick a code, for example `lifeos-vikas`. Your dashboard will be at `lifeos-vikas.goatcounter.com`.
2. In your GitHub repository, open `config.js`, click the **pencil** (Edit), and put your code between the quotes:
   `window.LIFEOS_ANALYTICS = 'lifeos-vikas';`
3. Click **Commit changes**. Counting starts within a minute or two.

What you'll see in the GoatCounter dashboard:

| Name | What it counts |
|---|---|
| `/life-os/` (page views) | Every time someone opens the app or the link |
| `new-visitor` | Each device that opens the link for the first time in a browser |
| `install` | Each device that opens Life OS as an installed app for the first time. This is your **download count** |
| `daily-active` | Installed apps opened that day (one per device per day) |
| `tried-sample` | People who tapped "Try it with sample data" |
| `started` | People who set up their own Life OS |

Keep in mind:
- Counts are per **device**, not per person. Someone with a phone and a laptop counts twice.
- Ad blockers and some privacy browsers block counters, so real numbers are a bit higher.
- On iPhone, the install is counted the first time the app is opened from the Home Screen.
- Only these event names are sent, never anyone's habits, meals, weight or name.

## 5. Keep your data safe

Data lives only on the device you use it on. The app reminds you monthly to **save a backup file**. Keep those files somewhere safe, such as Google Drive or iCloud. If you get a new phone, install the app again and use **Restore from file**.

## 6. Updating the app later

1. Replace `index.html` (or any file) in your GitHub repository with the new version.
2. Open `sw.js` and raise the number in `VERSION` by one (for example `lifeos-v3` → `lifeos-v4`).
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

There are no accounts, and all data stays on your device unless you export a backup yourself. If you switch on counting in `config.js`, the app sends anonymous event names (visit, install, daily open) to GoatCounter. It never sends anything anyone enters.

Fonts: Unbounded, Manrope and JetBrains Mono, all under the SIL Open Font License (see `fonts/LICENSE.txt`).
