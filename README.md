# Student Pro — Flutter Web

Готовая статическая сборка веб-приложения **Student Pro**, созданная с помощью Flutter и размещённая для публикации через GitHub Pages.

**[Открыть приложение](https://leambell.github.io/build_ahpc/)**

## О проекте

Репозиторий содержит готовую сборку Flutter-приложения:

- главная точка входа — `index.html`;
- скомпилированный код приложения — `main.dart.js`;
- загрузчик Flutter — `flutter_bootstrap.js`;
- PWA-манифест — `manifest.json`;
- значки и ресурсы приложения;
- библиотеки CanvasKit для рендеринга;
- сервисный работник для автономной работы и кеширования файлов.

### Информация о сборке

- Название пакета: `student_pro`
- Версия приложения: `1.0.0`
- Номер сборки: `1`

## Технологии

- Flutter Web
- Dart
- JavaScript
- HTML
- WebAssembly / CanvasKit
- Progressive Web App (PWA)
- GitHub Pages

## Структура проекта

```text
.
├── assets/                    # Ресурсы приложения
├── canvaskit/                 # CanvasKit для рендеринга
├── icons/                     # Значки PWA
├── favicon.png
├── favicon_one.ico
├── flutter.js
├── flutter_bootstrap.js
├── flutter_service_worker.js
├── index.html                 # Точка входа
├── main.dart.js               # Скомпилированное приложение
├── manifest.json              # Настройки PWA
└── version.json               # Информация о сборке
```

## Локальный запуск

Для запуска статической сборки нужен локальный HTTP-сервер.

### Python

```bash
python -m http.server 8080
```

Затем откройте в браузере:

```text
http://localhost:8080
```

### Node.js

```bash
npx serve .
```

## Развёртывание на GitHub Pages

Проект настроен для публикации с относительным базовым путём:

```text
/build_ahpc/
```

Для обновления опубликованной сборки:

1. Соберите приложение в исходном проекте Flutter:

   ```bash
   flutter build web --release
   ```

2. Скопируйте содержимое каталога `build/web` в корень ветки `main`.

3. Зафиксируйте и отправьте изменения:

   ```bash
   git add .
   git commit -m "Update Flutter Web build"
   git push origin main
   ```

4. В настройках GitHub Pages выберите:

   - **Source:** `Deploy from a branch`
   - **Branch:** `main`
   - **Folder:** `/ (root)`

## Progressive Web App

Приложение может работать как Progressive Web App:

- поддерживается автономный режим;
- используется портретная ориентация;
- настроены тема и фоновый цвет;
- добавлены значки для установки;
- сервисный работник кеширует файлы для повторного использования.

## Исходный код

В этом репозитории находится только готовая сборка Flutter Web. Исходные файлы приложения, например `lib/` и `pubspec.yaml`, отсутствуют.

Для внесения изменений потребуется исходный код приложения. После получения исходников изменения можно собирать так:

```bash
flutter pub get
flutter run -d chrome
flutter build web --release
```

## Лицензия

Лицензия не указана. Перед использованием, изменением или распространением проекта необходимо уточнить условия лицензирования.

## Автор

Лиам Белл
