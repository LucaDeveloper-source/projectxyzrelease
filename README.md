# Project XYZ

> A modern cross-platform application built with Electron and Capacitor.

**Project XYZ** ist eine plattformübergreifende Anwendung, die aus einer gemeinsamen Codebasis für mehrere Plattformen gebaut wird.

### Unterstützte Plattformen

- 🪟 **Windows** — `.exe`
- 🍎 **macOS Intel** — `.dmg` / `.zip`
- 🤖 **Android** — `.apk`
- 📱 **iOS** — unsignierte `.ipa`

---

## 🇩🇪 Deutsch

### Über Project XYZ

Project XYZ ist eine moderne Cross-Platform-Anwendung mit Fokus auf einer einfachen und einheitlichen Nutzung über verschiedene Geräte und Betriebssysteme hinweg.

Das Projekt verwendet **Electron** für Desktop-Anwendungen und **Capacitor** für mobile Plattformen.

### Plattformen & Builds

| Plattform | Format | Architektur |
|---|---|---|
| Windows | `.exe` | x64 |
| macOS | `.dmg` / `.zip` | Intel x64 |
| Android | `.apk` | Android |
| iOS | `.ipa` | iOS / unsigniert |

### Automatische Builds

Die Builds werden über **GitHub Actions** automatisiert.

Bei einem Workflow-Start werden die einzelnen Plattformen unabhängig voneinander gebaut:

```text
Windows
   ↓
ProjectXYZ-Setup-1.0.0.exe
ProjectXYZ-Portable-1.0.0.exe

macOS Intel
   ↓
ProjectXYZ-1.0.0-Intel.dmg
ProjectXYZ-1.0.0-Intel.zip

Android
   ↓
ProjectXYZ.apk

iOS
   ↓
ProjectXYZ-unsigned.ipa
```

### Technologien

- Electron
- Electron Builder
- Capacitor
- Node.js
- Android / Gradle
- Xcode
- GitHub Actions

### Repository-Struktur

```text
projectxyz/
├── .github/
│   └── workflows/
│       └── build.yml
│
├── android/
├── ios/
├── electron/
│   └── main.js
│
├── build/
├── www/
│
├── capacitor.config.json
├── package.json
└── README.md
```

### Entwicklung

Abhängigkeiten installieren:

```bash
npm install
```

Electron-Anwendung lokal starten:

```bash
npm start
```

### Windows bauen

```bash
npm run build:win
```

### macOS bauen

```bash
npm run build:mac
```

### Android bauen

```bash
npx cap sync android
```

Danach kann das Android-Projekt mit Gradle gebaut werden.

### iOS

Das iOS-Build wird über GitHub Actions erstellt.

Der erzeugte IPA-Build ist **unsigniert** und enthält keine Apple-Developer-Signatur.

---

## 🇬🇧 English

### About Project XYZ

Project XYZ is a modern cross-platform application designed to provide a consistent experience across multiple devices and operating systems.

The project uses **Electron** for desktop applications and **Capacitor** for mobile platforms.

### Platforms & Builds

| Platform | Format | Architecture |
|---|---|---|
| Windows | `.exe` | x64 |
| macOS | `.dmg` / `.zip` | Intel x64 |
| Android | `.apk` | Android |
| iOS | `.ipa` | iOS / unsigned |

### Automated Builds

Project XYZ uses **GitHub Actions** to automate the build process.

Each supported platform is built independently:

```text
Windows
   ↓
ProjectXYZ-Setup-1.0.0.exe
ProjectXYZ-Portable-1.0.0.exe

macOS Intel
   ↓
ProjectXYZ-1.0.0-Intel.dmg
ProjectXYZ-1.0.0-Intel.zip

Android
   ↓
ProjectXYZ.apk

iOS
   ↓
ProjectXYZ-unsigned.ipa
```

### Technologies

- Electron
- Electron Builder
- Capacitor
- Node.js
- Android / Gradle
- Xcode
- GitHub Actions

### Repository Structure

```text
projectxyz/
├── .github/
│   └── workflows/
│       └── build.yml
│
├── android/
├── ios/
├── electron/
│   └── main.js
│
├── build/
├── www/
│
├── capacitor.config.json
├── package.json
└── README.md
```

### Development

Install dependencies:

```bash
npm install
```

Start the Electron application locally:

```bash
npm start
```

### Build for Windows

```bash
npm run build:win
```

### Build for macOS

```bash
npm run build:mac
```

### Build for Android

```bash
npx cap sync android
```

The Android project can then be built using Gradle.

### iOS

The iOS build is generated through GitHub Actions.

The resulting IPA is **unsigned** and does not contain an Apple Developer signing identity.

---

## 🔧 GitHub Actions

The repository contains an automated workflow:

```text
.github/workflows/build.yml
```

The workflow builds:

- Windows
- macOS Intel
- Android
- iOS

The generated files are uploaded as **GitHub Actions artifacts** and can also be included in a GitHub Release.

---

## 📦 Releases

Release files are generated automatically by GitHub Actions.

Available artifacts may include:

```text
Windows
├── ProjectXYZ-Setup-*.exe
└── ProjectXYZ-Portable-*.exe

macOS
├── ProjectXYZ-*-Intel.dmg
└── ProjectXYZ-*-Intel.zip

Android
└── ProjectXYZ.apk

iOS
└── ProjectXYZ-unsigned.ipa
```

---

## ⚠️ iOS Signing

The iOS application is intentionally built **without code signing**.

The generated `.ipa` is therefore intended for users who have their own compatible signing/sideloading workflow.

An Apple Developer account and signing process may be required depending on the installation method.

---

## 💻 macOS Intel Compatibility

The macOS desktop build targets **Intel x64**.

It is intended for Intel-based Macs, including older Intel Mac systems.

Actual compatibility also depends on the macOS version installed on the target machine.

---

## 📄 License

This project is currently distributed according to the license and usage terms defined by the project owner.

---

# Project XYZ

**Built with Electron · Capacitor · GitHub Actions**

Made by **Luca**.


