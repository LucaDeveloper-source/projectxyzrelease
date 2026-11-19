# Project XYZ – Windows / Android / iOS

Native Hüllen („Wrapper") um deine Lovable-App https://projectxyzl.lovable.app/
- Windows: Electron -> Installer (.exe) + Portable (.exe)
- Android: Capacitor -> APK (Debug-signiert, direkt installierbar)
- iOS: Capacitor -> **unsignierte** IPA (zum Sideloaden)

Die Apps laden deine Live-Seite. Jede Änderung in Lovable ist sofort in allen Apps sichtbar.

## Bauen (ohne lokale Installation, kostenlos)
1. Neues GitHub-Repository anlegen (am besten **privat**) und den Inhalt dieses Ordners hochladen
   (Ordner `.github` muss mit hoch).
2. Im Repo: Tab **Actions** -> **Build Project XYZ** -> **Run workflow**.
3. Nach ca. 10-15 Min. findest du rechts im Repo unter **Releases** die fertigen Einzeldateien:
   - `ProjectXYZ-Setup-1.0.0.exe` (Windows-Installer)
   - `ProjectXYZ-Portable-1.0.0.exe` (Windows ohne Installation)
   - `ProjectXYZ.apk` (Android)
   - `ProjectXYZ-unsigned.ipa` (iOS, unsigniert)

Das App-Icon (assets/ und build/) wird automatisch fuer alle Plattformen in alle noetigen Groessen umgerechnet.
Das Originalbild ist nur 193x193 px gross - mit einer Version ab 1024x1024 px wird das Icon schaerfer
(Datei `assets/icon-only.png` ersetzen und die Dateien in `build/` und `electron/icon.png` entsprechend).

## Installieren
- **Windows:** .exe starten. SmartScreen warnt bei unsignierten Apps: „Weitere Informationen" -> „Trotzdem ausführen".
- **Android:** APK aufs Handy, „Unbekannte Apps installieren" erlauben, öffnen.
- **iOS:** Die unsignierte IPA mit AltStore oder Sideloadly und deiner Apple-ID aufs iPhone signieren/installieren (bei kostenloser Apple-ID 7 Tage gültig).

## Store-Veröffentlichung
- Google Play: signiertes AAB statt Debug-APK nötig (eigener Keystore, einmalig 25 $).
- Apple TestFlight/App Store: Apple Developer Program (99 $/Jahr) + Signing-Zertifikate.
  Hinweis: Apple lehnt reine Website-Wrapper oft ab (Guideline 4.2).
