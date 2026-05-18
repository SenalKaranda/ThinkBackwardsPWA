# Think Backwards — installers & packages

This repo hosts the downloadable installers for **[Think Backwards](https://www.thinkbackwards.app/)**, a gameshow-inspired offline-first hot-seat trivia game. The web app itself is the primary way to play — this repo is for users who want a native install without going through their browser.

> **The easiest way to install is straight from your browser.** Open [thinkbackwards.app](https://www.thinkbackwards.app/) in Chrome or Edge and click the install button in the address bar. You get the same experience as the native installs below, without downloading anything from this repo.

The native installs here exist for users on browsers that don't support PWA install (Firefox desktop, etc.) or who simply prefer a real installer.

---

## Downloads

Grab the latest installer for your platform from the **[Releases page](../../releases/latest)**.

| Platform | File | Notes |
|---|---|---|
| Windows 10/11 | `Think Backwards_X.Y.Z_x64-setup.exe` | NSIS installer. Recommended. Per-user install, no admin required. |
| Windows 10/11 (MSI) | `Think Backwards_X.Y.Z_x64_en-US.msi` | Alternative for orgs/users that prefer MSI. |
| Android | `app-release-signed.apk` | Sideload. See instructions below. |
| Android (Play Store format) | `app-release-bundle.aab` | For Play Store submission only — end users want the APK. |

> Don't see an iOS option? Apple doesn't allow sideloaded apps. On iOS, open [thinkbackwards.app](https://www.thinkbackwards.app/) in Safari and tap **Share → Add to Home Screen**.

---

## Install instructions

### Windows

1. Download the `.exe` from the latest release.
2. Double-click to run.
3. SmartScreen may show a **"Windows protected your PC"** warning because the installer isn't code-signed. Click **More info → Run anyway**. This is normal for self-distributed apps.
4. The installer drops Think Backwards into your Start Menu. No admin rights needed.

To uninstall: Windows Settings → Apps → Think Backwards → Uninstall.

> The Windows version uses **WebView2**, which ships with Windows 10/11 by default. If you're on a stripped-down Windows install, you may need to install the [WebView2 Runtime](https://developer.microsoft.com/microsoft-edge/webview2/) once.

### Android

1. Download the `.apk` from the latest release on your phone.
2. Tap the file. Android will warn that "this type of file can harm your device" — this is the standard sideload warning. Tap **Settings** (or **More details**) and enable **Allow from this source** for your browser/file manager.
3. Tap **Install**.

To uninstall: long-press the app icon → App info → Uninstall.

---

## Updates

Native installs **don't auto-update.** When a new version is released here, you'll need to download the new installer and re-install.

If you want automatic updates, use the in-browser PWA install instead — it updates silently whenever the web app does.

To check for new releases, watch this repo (top-right **Watch → Custom → Releases**) and GitHub will notify you when a release is published.

---

## About the app

- **Offline-first.** Everything runs in your browser/installer; no account, no servers, no telemetry.
- **Hot-seat multiplayer.** One device, multiple players, pass-and-play.
- **Custom categories.** Download extra category packs from **[ThinkBackwardsCategories](https://github.com/SenalKaranda/ThinkBackwardsCategories)** via the in-app Settings → Categories tab.

---

## Reporting bugs

Please open an [issue](../../issues) on this repo, or email **catdadstudios@gmail.com**.

Include:
- What platform you're on (browser version, OS, install method).
- What you did and what happened.
- A screenshot if relevant.

---

## Source

The app's source lives in a separate private repo. This repo only hosts release binaries built automatically from each tagged release.
