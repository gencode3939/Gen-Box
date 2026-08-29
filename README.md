
# 📦 Gen Box — Smart, Offline-First Savings & Piggy Bank Manager

<p align="center">
  <img src="https://cdn.phototourl.com/free/2026-08-29-9d13e2c6-60f9-432d-873d-3fff2650715c.jpg" width="140" height="140" alt="Gen Box App Icon" style="border-radius: 28px;" />
</p>

<p align="center">
  <a href="https://android.com"><img src="https://img.shields.io/badge/Platform-Android-3DDC84?style=flat&logo=android&logoColor=white" alt="Platform" /></a>
  <a href="https://kotlinlang.org"><img src="https://img.shields.io/badge/Language-Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white" alt="Language" /></a>
  <a href="https://developer.android.com/jetpack/compose"><img src="https://img.shields.io/badge/UI-Jetpack%20Compose-4285F4?style=flat&logo=jetpackcompose&logoColor=white" alt="UI" /></a>
  <a href="https://developer.android.com/topic/architecture"><img src="https://img.shields.io/badge/Architecture-MVVM%20%2B%20Clean-FF6F00?style=flat" alt="Architecture" /></a>
  <a href="https://developer.android.com/training/data-storage/room"><img src="https://img.shields.io/badge/Storage-Room%20(Offline--First)-009688?style=flat&logo=sqlite&logoColor=white" alt="Database" /></a>
  <a href="https://m3.material.io"><img src="https://img.shields.io/badge/Design-Material%20Design%203-6750A4?style=flat" alt="Design" /></a>
</p>

**Gen Box** is a modern, privacy-respecting, offline-first personal savings goals tracker and smart virtual piggy bank application built with **Jetpack Compose**, **Kotlin Coroutines**, and **Android Room Database**.

---

## ✨ Key Features

### 🎯 Purpose-Driven Savings Boxes (Virtual Piggy Banks)
- Create individual savings boxes tailored for vacations, emergency funds, tech gadgets, investments, or custom milestones.
- **Custom Color Picker**: Choose from 12 Material palettes or specify custom 6-digit **HEX color codes** (`#RRGGBB`) with real-time preview.
- **Icon Selector**: Assign expressive icons matching your savings objective.
- **Dynamic Cadence & Pacing**: Calculate recommended daily, weekly, or monthly contribution targets based on your set deadline.

### 🔒 100% Privacy & Offline-First Security
- **Zero Cloud Leak**: All data is stored locally in an encrypted Room SQLite database on your device. No third-party analytics, tracking, or remote servers.
- **Privacy Mask Mode**: One-tap toggle to mask balances and amounts (`••••••`) in public spaces or screenshots.
- **Security Hardened**: Built-in protection against XSS/HTML injection, parameterized SQL queries, and sanitized exports preventing CSV formula injection (CWE-1236).
- **Security Audit Log**: Review local logs for critical state changes and transactions.

### 🌐 Bilingual & Multi-Currency Architecture
- **Instant Language Switching**: Full runtime localization in **English (🇺🇸)** and **Turkish (🇹🇷)** with no app restart required.
- **Multi-Currency Support**: Native handling for **Turkish Lira (₺)**, **US Dollar ($)**, **Euro (€)**, and **British Pound (£)**.

### 📊 Analytics & Smart Insights
- **Savings Velocity & History**: Interactive 6-month net savings bar charts and monthly contribution breakdowns.
- **Goal Distribution**: Visual balance allocation charts across all active boxes.
- **Smart Rule-Based Insights**: Personalized suggestions, pace warnings, and milestone highlights.

### 🎨 Micro-Interactions & Fluid Motion
- **Confetti Celebration**: Particle physics burst when a goal achieves 100% completion.
- **Spring Physics**: Tactile bounce feedback on buttons, cards, and interactive chips.
- **Animated Value Counters**: Smooth numerical ticker transitions when depositing or withdrawing funds.
- **Accessibility & Reduce Motion**: Full support for users who prefer reduced animations.

### 💾 Backup & Data Portability
- **JSON Backup & Restore**: Export full encrypted JSON snapshots with flexible merge or replace import modes.
- **CSV Spreadsheet Export**: Export transaction sheets compatible with Excel, Google Sheets, or Numbers.
- **Clipboard Sharing**: Direct copy-to-clipboard and system share sheet integrations.

---

## 🏗️ Architecture & Tech Stack

Gen Box follows Google's recommended Android architecture practices:

```
app/
 ├── core/
 │    ├── database/       # Room DB, DAOs, Entity Models & Converters
 │    ├── localization/   # Dynamic bilingual string dictionary & language manager
 │    ├── model/          # Domain models (Goal, Transaction, Currency, AuditEvent)
 │    ├── repository/     # Repository pattern, business logic, sanitizers, export/import
 │    └── utils/          # Pacing calculators, currency formatters, security sanitizers
 ├── ui/
 │    ├── components/     # Reusable Compose widgets (AmountField, SpringClick, Ticker, Confetti)
 │    ├── dialogs/        # Deposit/Withdraw, Goal Form, Color Picker, Backup & Audit sheets
 │    ├── screens/        # Dashboard, Goals List, Goal Detail, Analytics, Settings, Onboarding
 │    ├── theme/          # Material 3 typography, dynamic color schemes, shapes
 │    ├── MainActivity.kt # Single-activity edge-to-edge entry point
 │    └── MainViewModel.kt# Unified StateFlow state management
```

### 🛠️ Technologies Used
- **Kotlin 2.0+**
- **Jetpack Compose** (Material 3, Animations, Icons Extended)
- **AndroidX Lifecycle & ViewModel** (`StateFlow`, `collectAsStateWithLifecycle`)
- **Room Database** (KSP symbol processing, SQLite)
- **DataStore Preferences** (Persistent user configuration)
- **Coroutines & Flow** (Asynchronous reactive pipelines)


## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 💡 Acknowledgements

Designed with simplicity, privacy, and user delight in mind. Built with Jetpack Compose & Material 3.
