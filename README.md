# Android Build Engine

Starter Android project untuk mengetes pipeline Jetpack Compose ke GitHub Actions.

## Struktur

```text
android-build-engine/
├── app/
├── gradle/
├── gradlew
├── gradlew.bat
├── settings.gradle.kts
├── build.gradle.kts
└── .github/workflows/build-android.yml
```

## Lokal

Wrapper JAR perlu dibuat/download jika belum ada:

```bash
gradle wrapper --gradle-version 8.9
./gradlew assembleDebug
```

Output:

```text
app/build/outputs/apk/debug/app-debug.apk
```

## GitHub Actions

1. Buat private repository bernama `android-build-engine`.
2. Upload seluruh isi folder ini.
3. Buka tab **Actions**.
4. Pilih **Build Android Compose APK**.
5. Klik **Run workflow**.
6. Pilih `debug` atau `release`.
7. Setelah selesai, download artifact `android-debug-apk` atau `android-release-apk`.

Project ini memakai:

- JDK 17
- Android API 35
- Android Build Tools 35.0.0
- Kotlin 2.0.21
- Jetpack Compose BOM 2024.12.01
- Gradle 8.9
