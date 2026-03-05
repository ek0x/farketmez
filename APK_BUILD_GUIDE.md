# Fark Etmez - APK Alma Rehberi

Bu proje Capacitor ile Android APK olarak alınabilir.

## 1) Gerekenler

- Node.js 18+
- Android Studio (SDK + Emulator/Device)
- Java 17 (Android Studio ile gelir)

## 2) Projeyi hazırla

```bash
npm install
npm run build
npx cap add android
npx cap sync android
```

> `android/` klasoru olustuktan sonra tekrar `npx cap add android` calistirmayin.

## 3) Android Studio'da ac

```bash
npx cap open android
```

Android Studio acildiginda:

1. Sol ustten `Build > Build Bundle(s) / APK(s) > Build APK(s)`
2. Islem bitince `locate` ile APK dosyasini ac

Genelde cikis yolu:

`android/app/build/outputs/apk/debug/app-debug.apk`

## 4) Telefona yukle

- USB debugging acik Android telefona baglan
- `app-debug.apk` dosyasini telefona atip kur
- Gerekirse "Unknown sources" izni ver

## 5) Kod degistirdikten sonra

```bash
npm run build
npx cap sync android
```

Sonra Android Studio'dan tekrar APK al.
