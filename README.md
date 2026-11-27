# Applify 📱

> Centralized Android Application Distribution Hub & F-Droid Repository by **Saurabh Kundu**.

[![Deploy F-Droid Repo](https://github.com/saurabhkundu1/Applify/actions/workflows/deploy-fdroid-pages.yml/badge.svg)](https://github.com/saurabhkundu1/Applify/actions/workflows/deploy-fdroid-pages.yml)
[![F-Droid Compatible](https://img.shields.io/badge/F--Droid-Compatible-blue?logo=f-droid)](https://saurabhkundu1.github.io/Applify/repo)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📌 About Applify

**Applify** is an open-source, self-hosted distribution repository for Android applications developed by Saurabh Kundu. Powered by **GitHub Pages**, **GitHub Actions**, and **F-Droid Server**, Applify delivers automated, privacy-first software updates directly to your favorite F-Droid client (such as **Droid-ify**, **Neo Store**, **F-Droid**, or **Obtainium**).

### ✨ Key Highlights

- **📱 Native F-Droid Protocol**: Full compatibility with F-Droid v1 & v2 JSON/XML index standards, `fdroidrepo://` deep linking, and QR code scanning.
- **🔄 Automated Release CI/CD**: Automatically triggered upon push and dispatch, updating F-Droid indices and GitHub Pages without human intervention.
- **🛡️ Release Verification**: All APKs are verified for ZIP integrity, single-signature consistency, and package/version metadata before indexing.
- **🔒 Transparent Distribution**: Published APKs are listed with their package metadata, permissions, and direct source repository links.
- **🧭 Permission Transparency**: App cards list Android permissions from the published APK manifest with clear explanations.
- **🔍 Privacy at a Glance**: Each app card clearly outlines local data policies and third-party interactions.

---

## 📦 Hosted Applications

| Application | Package ID | Version | Description | Links |
| :--- | :--- | :--- | :--- | :--- |
| **Secure Pass** | `com.applify.securepass` | `1.5.1` | Offline password manager with AES-256-GCM encryption, biometric unlock, 1-tap quick copy, card strength pills, reuse alerts, filter chips, and vault audit. | [Source](https://github.com/saurabhkundu1/secure-password-manager) |
| **Skycast** | `com.applify.skycast` | `1.0.3` | Modern weather app with responsive adaptive layout, Outdoor Comfort & Activity Insights, Feels-Like & Wind metrics, and Open-Meteo visualization. | [Source](https://github.com/saurabhkundu1/skycast-weather) |
| **ChronoSphere** | `com.applify.chronosphere` | `1.8.1` | World clock with interactive time travel scrubbing (-12h to +12h), Day ☀️ / Night 🌙 city badges, meeting planner, and home-screen widget. | [Source](https://github.com/saurabhkundu1/chronosphere-time-app) |
| **Signal Atlas** | `com.applify.signalatlas` | `1.4.1` | Private cellular signal logger with real-time reception health badge, network technology analytics (% 5G, % 4G), and OpenStreetMap export. | [Source](https://github.com/saurabhkundu1/signal-logger) |
| **Siprise** | `com.applify.watertracker` | `1.5.1` | Daily hydration tracker with daily goal-achieved celebration cards, custom quick-log amounts, gentle reminders, home-screen widget, and TalkBack accessibility. | [Source](https://github.com/saurabhkundu1/siprise-android) |
| **AdLoop** | `com.adloop.app` | `0.1.1` | Vertical video reward ads feed with session campaigns, smart pacing status indicator, reward credits tracking, and interactive pacing dialog. | [Source](https://github.com/saurabhkundu1/adloop-ads) |

---

## 🌐 Repository Information

| Resource | Value / Link |
| :--- | :--- |
| **Web Portal** | [https://saurabhkundu1.github.io/Applify/](https://saurabhkundu1.github.io/Applify/) |
| **F-Droid Repo URL** | `https://saurabhkundu1.github.io/Applify/repo` |
| **F-Droid Deep Link** | [`fdroidrepo://saurabhkundu1.github.io/Applify/repo`](fdroidrepo://saurabhkundu1.github.io/Applify/repo) |
| **SHA-256 Fingerprint** | `18F030BE4407811F4DBC2C7D26A52A5261F1C921AEF9C33F350046AA2AE19077` |

---

## 📲 How to Add to F-Droid / Droid-ify / Neo Store / Obtainium

### Option 1: Add from the Web Portal
1. Visit [https://saurabhkundu1.github.io/Applify/](https://saurabhkundu1.github.io/Applify/) on your Android phone.
2. Tap **Add this repository**.
3. Choose or confirm your F-Droid-compatible client when prompted.

### Option 2: Add Manually
1. Open **Droid-ify** or **F-Droid**.
2. Go to **Settings** > **Repositories** > **+** (Add Repository).
3. Paste: `https://saurabhkundu1.github.io/Applify/repo`
4. Confirm with the repository fingerprint:
   `18F030BE4407811F4DBC2C7D26A52A5261F1C921AEF9C33F350046AA2AE19077`

---

## 📄 License

This repository and its web assets are licensed under the [MIT License](LICENSE). Each hosted application has its own independent license documented in its source repository.
