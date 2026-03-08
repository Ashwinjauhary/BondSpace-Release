# BondSpace Mobile — Release Folder

This folder contains the **BondSpace Android APK** and the **landing page** for distributing the app.

## 📱 Install the App

1. Download `BondSpace.apk`
2. On your Android phone, enable **Install from Unknown Sources**  
   *(Settings → Security → Unknown Sources)*
3. Open the APK and install

> **You only need to install once!** The app updates itself automatically.

---

## 🔄 How Auto-Updates Work

BondSpace uses a custom **OTA (Over-The-Air)** update system:

```
Developer pushes code to GitHub
         ↓
GitHub Actions builds the new web bundle + APK
         ↓
Bundle is published to GitHub Releases
         ↓
On your next app launch, BondSpace silently downloads
the new bundle in the background and reloads itself
         ↓
You always have the latest version — no reinstall needed!
```

---

## 🌐 Landing Page

Open `landing/index.html` in any browser to see the full app showcase page.

---

## 🛠️ For Developers

To build a new APK locally:

```bash
# 1. Clone the repo
git clone https://github.com/Ashwinjauhary/bondspace.git
cd bondspace/frontend

# 2. Install dependencies
npm install --legacy-peer-deps

# 3. Build static export + sync to Android
npm run cap:sync

# 4. Build debug APK
npm run cap:build-apk

# 5. Find your APK at:
# android/app/build/outputs/apk/debug/app-debug.apk
```

Or just push to `main` — GitHub Actions does it all automatically!

---

Made with ❤️ — BondSpace, *a private digital universe for two.*
