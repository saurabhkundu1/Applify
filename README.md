# Applify 📱

> Centralized Android Application Distribution Hub & F-Droid Store by **Saurabh Kundu**.

[![Deploy F-Droid Repo](https://github.com/saurabhkundu1/Applify/actions/workflows/deploy-fdroid-pages.yml/badge.svg)](https://github.com/saurabhkundu1/Applify/actions/workflows/deploy-fdroid-pages.yml)
[![F-Droid Compatible](https://img.shields.io/badge/F--Droid-Compatible-blue?logo=f-droid)](https://saurabhkundu1.github.io/Applify/repo)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📌 About Applify

**Applify** is an open-source, self-hosted distribution repository for all Android applications developed by Saurabh Kundu. Built on top of **GitHub Pages**, **GitHub Actions**, and **F-Droid Server**, Applify delivers automated, privacy-first software updates directly to your favorite F-Droid client (such as **Droid-ify**, **Neo Store**, **F-Droid**, or **Obtainium**).

### ✨ Key Highlights

- **📱 Native F-Droid Protocol**: Full compatibility with F-Droid v1 & v2 JSON/XML index standards, `fdroidrepo://` deep linking, and QR code scanning.
- **🔄 Automated Release CI/CD**: Automatically triggered via `repository_dispatch` when a new release is published in source app repositories, updating F-Droid indices and GitHub Pages without human intervention.
- **🛡️ Rigorous Security & Verification**: Every incoming APK is verified for valid zip structure, V1/V2/V3 signatures (`apksigner`), and application badging (`aapt`) before index registration.
- **🔒 Privacy First**: 100% open-source applications distributed directly without third-party tracking, ads, or proprietary SDKs.

---

## 📦 Hosted Applications

| Application | Package ID | Version | Description | Links |
| :--- | :--- | :--- | :--- | :--- |
| **Secure Pass** | `com.applify.securepass` | `1.0.1` | Offline, high-security password manager with AES-256-GCM encryption and biometrics. | [Source](https://github.com/saurabhkundu1/secure-password-manager) \| [APK Download](https://saurabhkundu1.github.io/Applify/repo/com.applify.securepass_2.apk) |
| **Skycast** | `com.applify.skycast` | `1.0.0` | Modern weather application with interactive graphs and Open-Meteo visualization. | [Source](https://github.com/saurabhkundu1/skycast-weather) \| [APK Download](https://saurabhkundu1.github.io/Applify/repo/com.applify.skycast_1.apk) |

---

## 🌐 Repository Information

| Resource | Value / Link |
| :--- | :--- |
| **Web Portal** | [https://saurabhkundu1.github.io/Applify/](https://saurabhkundu1.github.io/Applify/) |
| **F-Droid Repo URL** | `https://saurabhkundu1.github.io/Applify/repo` |
| **F-Droid Deep Link** | [`fdroidrepo://saurabhkundu1.github.io/Applify/repo`](fdroidrepo://saurabhkundu1.github.io/Applify/repo) |
| **SHA-256 Fingerprint** | `DE 62 E0 D3 86 DB 9B 6F C6 16 AD F6 57 3F 45 8A AC 8D 04 F8 73 00 7C 73 B8 58 5F BE F0 96 02 55` |

---

## 📲 How to Add to F-Droid / Droid-ify / Neo Store / Obtainium

### Option 1: One-Tap Setup
1. Visit [https://saurabhkundu1.github.io/Applify/](https://saurabhkundu1.github.io/Applify/) on your Android phone.
2. Tap **Add to F-Droid / Droid-ify**.
3. Confirm adding the repository when prompted by your client app.

### Option 2: QR Code Scan
1. Open Droid-ify, Neo Store, or F-Droid on your device.
2. Go to **Settings ➔ Repositories**.
3. Tap the **QR Code** button and scan the QR code on the [Applify Web Portal](https://saurabhkundu1.github.io/Applify/).

### Option 3: Manual Addition
1. Open your F-Droid client app.
2. Navigate to **Settings ➔ Repositories**.
3. Tap **Add (+)**.
4. Enter the repository URL:
   ```
   https://saurabhkundu1.github.io/Applify/repo
   ```
5. Save and refresh repositories.

---

## ⚙️ Automated Integration Workflow

When a source app repository (e.g. `saurabhkundu1/skycast-weather`) creates a new release, it dispatches a webhook event to Applify:

```json
{
  "event_type": "new_release",
  "client_payload": {
    "source_repo": "saurabhkundu1/skycast-weather",
    "package_name": "com.applify.skycast",
    "version": "1.0.0",
    "version_code": "1",
    "tag": "Skycast-1.0.0",
    "asset_name": "skycast-1.0.0.apk"
  }
}
```

The receiving GitHub Actions workflow (`deploy-fdroid-pages.yml`) executes the following steps:
1. Validates payload fields and enforces repository/package whitelists.
2. Downloads the published release asset from GitHub Releases.
3. Verifies zip integrity (`zip -T`), signature (`apksigner`), and badging (`aapt`).
4. Moves the verified APK into `repo/`.
5. Executes `fdroid update` to regenerate signed F-Droid v1/v2 index JSON/XML files.
6. Synchronizes root and `repo/` index files.
7. Commits updated artifacts and deploys the site to GitHub Pages.

---

## 📂 Repository Layout

```
Applify/
├── .github/
│   └── workflows/
│       └── deploy-fdroid-pages.yml # Main deployment and release-dispatch handler
├── metadata/
│   ├── com.applify.securepass.yml  # Metadata definition for Secure Pass
│   └── com.applify.skycast.yml     # Metadata definition for Skycast
├── repo/
│   ├── config.yml                  # F-Droid server configuration
│   ├── index-v1.json               # F-Droid v1 JSON index
│   ├── index-v2.json               # F-Droid v2 JSON index
│   ├── entry.json                  # F-Droid v2 entry header
│   ├── index.xml                   # F-Droid XML fallback index
│   ├── com.applify.securepass_2.apk# Published Secure Pass APK
│   └── com.applify.skycast_1.apk   # Published Skycast APK
├── index.html                      # Web catalogue & landing page
├── README.md                       # Project documentation
└── .nojekyll                       # GitHub Pages Jekyll bypass
```

---

## 👤 Author

**Saurabh Kundu**  
- GitHub: [@saurabhkundu1](https://github.com/saurabhkundu1)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
