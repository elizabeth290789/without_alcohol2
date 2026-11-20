# День за днём 2.0

Автономный Android-трекер дней без алкоголя для Android 9 и новее. В приложении можно отмечать дни употребления, исправлять даты отметок и просматривать историю периодов и достижений.

[Скачать подписанный APK](https://github.com/elizabeth290789/without_alcohol2/raw/refs/heads/main/downloads/day-by-day-2.0.apk) · [Контрольная сумма SHA-256](downloads/SHA256SUMS.txt)

У приложения идентификатор `ru.daybyday.app2`. Его можно установить рядом с «День за днём» (`ru.daybyday.app`). При первом запуске история 2.0 пустая. Отметки, настройки и достижения сохраняются в хранилище нового приложения.

Исходная версия 2.0 взята из [коммита d3b7685](https://github.com/elizabeth290789/without_alcohol/commit/d3b76854da7e3ed038fbbbde3af285466dbd7a37).

## Сборка

Понадобятся JDK 17, Android SDK Platform 35 и Build Tools 35.0.0. Укажите путь к SDK через `ANDROID_HOME` или `local.properties`.

```sh
./gradlew testDebugUnitTest lintDebug assembleRelease
```

Gradle создаёт неподписанный APK в `app/build/outputs/apk/release/app-release-unsigned.apk`. Для следующего выпуска увеличьте `versionCode` и подпишите APK тем же ключом, что использовался для выпуска 2.0. Храните ключ и пароль вне репозитория.
