
<!-- Animated Header Banner -->
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0:0B0F19,25:00E5FF,50:7C4DFF,75:FF2E93,100:00F5D4&height=280&section=header&text=GEN%20BOX&fontSize=72&fontAlignY=38&desc=Next-Gen%20Gamified%20Offline%20Vault%20%26%20Theme%20Ecosystem&descAlignY=58&descSize=20" width="100%" alt="Gen Box Header"/>

  <a href="https://github.com/gencode3939/Gen-Box">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=20&duration=3000&pause=1200&color=00E5FF&center=true&vCenter=true&width=900&lines=%E2%9C%A8+100%25+Offline-First+Gamified+Savings+%26+Vault;%F0%9F%9A%80+Gen+Connect%3A+Air-Gapped+Hardware+Bluetooth+BLE+Sharing;%F0%9F%8E%A8+Theme+Studio%3A+Instant+Dynamic+Material+3+Color+Theming;%F0%9F%8E%AE+Gamified+Economy%3A+Gen+Points%2C+Levels+%26+Unlockable+Skins;%F0%9F%94%92+Zero-Cloud+Privacy%3A+Pure+On-Device+Room+SQLite+Encryption" alt="Gen Box Animated Typing Slogan" />
  </a>
</div>

<p align="center">
  <a href="https://android.com"><img src="https://img.shields.io/badge/Platform-Android%208.0%2B-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Platform" /></a>
  <a href="https://kotlinlang.org"><img src="https://img.shields.io/badge/Kotlin-2.0%2B-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" alt="Language" /></a>
  <a href="https://developer.android.com/jetpack/compose"><img src="https://img.shields.io/badge/UI-Jetpack%20Compose%20M3-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white" alt="UI" /></a>
  <a href="https://developer.android.com/training/data-storage/room"><img src="https://img.shields.io/badge/Storage-Room%20SQLite-009688?style=for-the-badge&logo=sqlite&logoColor=white" alt="Database" /></a>
  <a href="https://bluetooth.com"><img src="https://img.shields.io/badge/Hardware-Bluetooth%20BLE-007FFF?style=for-the-badge&logo=bluetooth&logoColor=white" alt="Bluetooth BLE" /></a>
  <a href="https://github.com/gencode3939/Gen-Box"><img src="https://img.shields.io/badge/License-MIT-F59E0B?style=for-the-badge&logo=open-source-initiative&logoColor=white" alt="License" /></a>
</p>

---

## 🌟 Overview

**Gen Box** is a state-of-the-art, **100% offline-first**, gamified financial goal tracker and digital vault built natively for Android. Designed with an unwavering commitment to user privacy, **Gen Box requires zero accounts, zero cloud servers, and collects zero telemetry.**

By turning routine saving habits into an engaging RPG-style progression system, Gen Box empowers users to achieve their milestones with interactive goal boxes, dynamic AI-powered theme customization, and an air-gapped peer-to-peer Bluetooth sharing protocol (**Gen Connect**).

---

## 🚀 Key Features

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=16&duration=2400&pause=1000&color=7C4DFF&center=true&vCenter=true&width=750&lines=%E2%9A%A1+Air-Gapped+Data+Transfer+%E2%80%A2+Dynamic+Color+Palette;%F0%9F%8E%AE+Gamified+Quest+Tree+%E2%80%A2+Zero-Cloud+Architecture" alt="Features Typing" />
</div>

### 📡 1. Gen Connect (Air-Gapped Bluetooth Transfer)
- **Direct Hardware BLE Discovery:** Scans and connects directly with nearby and paired Android devices via `BluetoothLeScanner` and `BluetoothAdapter` without relying on internet connections.
- **GTP2 Protocol Security:** Custom-designed transmission format featuring a 4-byte Magic Header (`GTP2`), 64-byte SHA-256 integrity verification, and AES-256-GCM encrypted payloads.
- **Ultra-Fast Sharing:** Transfer customized themes and box presets in milliseconds using 512-byte MTU optimization.

### 🎨 2. Reactive Dynamic Theming Engine
- **Instant Palette Morphing:** Seamlessly apply custom AI-extracted themes across the entire app with animated Material 3 `ColorScheme` transitions.
- **Preset & Custom Controls:** Quick-access theme chips (Calm Blue, Warm Coral, Night Glass, Mint Focus, Neutral Paper) with full override support for generated palettes.
- **Dark/Light & AMOLED Optimization:** Tailored contrast levels for both vibrant day-mode visibility and energy-efficient AMOLED black environments.

### 🎮 3. Gamification & Progression System
- **Gen Points (GP) Economy:** Earn points for financial discipline (+15 GP per deposit, +25 GP per new goal, +150 GP milestone jackpots).
- **Interactive Quests & Trophies:** Unlock achievements, level up your vault profile, and track savings streaks.
- **Reward Marketplace:** Redeem accumulated GP for custom 3D box models, neon glow shaders, and sound effects.

### 🌌 4. Quiet Galaxy & Gen Voice Assistant
- **Quiet Galaxy:** An interactive, meditative visual galaxy designed to foster mindfulness and stress-free financial planning.
- **Gen Voice Assistant:** Offline voice processing for rapid balance checks, deposit logging, and goal progress briefings.
- **Goal Orchestra:** Orchestrate multiple concurrent savings targets with automated milestone pacing.

### 🔒 5. Privacy-First Architecture
- **Zero-Cloud Guarantee:** All records, transactions, and audit logs are stored locally in an ACID-compliant Room SQLite database.
- **Privacy Shield:** Quickly conceal financial numbers (`••••••`) in public spaces with a single tap.
- **Audit & Export:** Full JSON backup and restore capabilities with automated validation.

---

## 🏛️ System Architecture

```mermaid
graph TD
    UI[📱 Jetpack Compose UI] -->|StateFlow / M3 Events| VM[🧠 MainViewModel]
    VM -->|Data Operations| PREF[⚙️ UserPreferencesRepository]
    VM -->|CRUD & Persistence| GOAL[📦 GoalRepository]
    GOAL -->|ACID Transactions| DB[(🗄️ Room SQLite Database)]
    VM -->|Hardware LE Scan| BLE[📡 GenConnect BLE Controller]
    VM -->|Dynamic Theme Flow| THEME[🎨 Palette & Theme Engine]
    VM -->|Reward Engine| QUEST[🎮 Gamification Engine]
```

### Technology Stack

| Layer | Technologies | Purpose |
| :--- | :--- | :--- |
| **User Interface** | Jetpack Compose, Material Design 3 | Modern, declarative, fully reactive UI with smooth morphing transitions |
| **Architecture** | MVVM, Clean Architecture, Kotlin Coroutines & Flow | Unidirectional data flow, modular scalability, and robust state management |
| **Local Storage** | Room SQLite, DataStore Preferences | Zero-latency, structured, 100% on-device data persistence |
| **Hardware BLE** | Android Bluetooth Low Energy Framework | Direct device-to-device air-gapped theme transfer |
| **Cryptography** | AES-256-GCM, SHA-256 Digest | Complete integrity verification and cryptographic payload protection |

---

## 🛠️ Build & Installation

### Prerequisites
- **Android OS:** Android 8.0 (API Level 26) or newer (Android 14+ recommended)
- **IDE:** Android Studio Koala / Ladybug or newer
- **JDK:** Java 17+

### Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/gencode3939/Gen-Box.git
cd Gen-Box

# 2. Build Debug APK
./gradlew assembleDebug

# 3. Install on connected device or emulator
./gradlew installDebug
```

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for full details.

<!-- Animated Footer Wave -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0:0B0F19,25:00E5FF,50:7C4DFF,75:FF2E93,100:00F5D4&height=140&section=footer" alt="Gen Box Animated Footer" width="100%" />
</p>

<p align="center">
  <sub>Crafted with ❤️ by <a href="https://github.com/gencode3939"><b>@gencode3939</b></a> • Open Source & Privacy-First</sub>
</p>
