# RPG Dungeon — Projekt Android Studio

## Jak otworzyć i uruchomić?

### 1. Zainstaluj Android Studio
Pobierz bezpłatnie ze strony: https://developer.android.com/studio

### 2. Otwórz projekt
- Uruchom Android Studio
- Wybierz "Open" → wskaż ten folder (rpg-android)
- Poczekaj aż Gradle zsynchronizuje projekt (~2-5 min przy pierwszym otwarciu)

### 3. Uruchom na telefonie lub emulatorze
Opcja A — Emulator:
- W Android Studio kliknij "Device Manager" → "Create Device"
- Wybierz np. Pixel 6, API 34
- Kliknij zielony trójkąt ▶️ "Run"

Opcja B — Twój telefon:
- Włącz "Opcje deweloperskie" na telefonie (Ustawienia → O telefonie → kliknij 7x "Numer kompilacji")
- Włącz "Debugowanie USB"
- Podłącz telefon kablem USB do komputera
- Kliknij ▶️ "Run" w Android Studio

### 4. Edytowanie gry
Cały kod gry jest w jednym pliku:
  app/src/main/assets/game.html
Otwórz go w dowolnym edytorze tekstowym i edytuj.
Po zapisaniu — kliknij ▶️ Run ponownie.

### 5. Budowanie APK do instalacji (bez Play Store)
Build → Build Bundle(s)/APK(s) → Build APK(s)
Plik znajdziesz w: app/build/outputs/apk/debug/app-debug.apk

### 6. Wrzucenie na Google Play
- Utwórz konto deweloperskie: https://play.google.com/console ($25 jednorazowo)
- Build → Generate Signed Bundle/APK → Android App Bundle (.aab)
- Wgraj plik .aab do Google Play Console
- Wypełnij opis, screenshoty, kategoria "Gry > RPG"
- Opublikuj!

## Zarabianie (AdMob)
1. Utwórz konto: https://admob.google.com
2. Dodaj zależność w app/build.gradle:
   implementation 'com.google.android.gms:play-services-ads:23.0.0'
3. Dodaj w MainActivity.java inicjalizację AdMob
4. Wstaw reklamy w game.html przez JavaScript bridge

## Struktura projektu
  rpg-android/
  ├── app/src/main/
  │   ├── assets/game.html     ← TUTAJ JEST CAŁA GRA
  │   ├── java/.../MainActivity.java  ← wrapper WebView
  │   └── AndroidManifest.xml
  └── CZYTAJ_MNIE.md           ← ten plik
