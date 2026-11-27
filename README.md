Student Pro — Flutter Web
Веб-приложение Student Pro , собранное из исходников Flutter и размещённое в видео готового статического сайта для GitHub Pages.

🌐 Открытое приложение

О проект
Репозиторий содержит готовую сборку Flutter-приложений:

главная точка входа — index.html;
исполняемый код приложения — main.dart.js;
загрузчик Flutter — flutter_bootstrap.js;
PWA-манифест — manifest.json;
иконки, ресурсы и библиотеки CanvasKit;
сервис-воркер для работы и кеширования приложений.
Версия Тейл:

название пакета: student_pro;
версия приложения: 1.0.0;
Идти: 1.
​ ...
Flutter Web
JavaScript
HTML
WebAssembly / CanvasKit
PWA-манифест
GitHub Pages
Структура проекта
.
├── assets/                   # Ресурсы приложения
├── canvaskit/                # CanvasKit для рендеринга
├── icons/                    # Иконки PWA
├── favicon.png
├── favicon_one.ico
├── flutter.js
├── flutter_bootstrap.js
├── flutter_service_worker.js
├── index.html                # Точка входа
├── main.dart.js              # Скомпилированное приложение
├── manifest.json             # Настройки PWA
└── version.json              # Информация о сборке
Локальный запуск
Для запуска статической сборки нужен локальный HTTP-сервер.

Python
python -m http.server 8080
Затем переход в браузере:

http://localhost:8080
Node.js
npx serve .
Развёртывание на страницах GitHub
Проект определяет относительный базовый путь:

/build_ahpc/
Для обновления публикации:

Возьмите приложение во Flutter:

flutter build web --release
Скопируйте важный каталог build/webв корень ветки main.

Добавьте изменения и отредактируйте их в репозитории:

git добавить . 
git commit -m " Обновить сборку Flutter Web " 
git push origin main
В качестве компонентов GitHub Pages выберите:

Source: Deploy from a branch
Branch: main
Folder: / (root)
ПВА
Приложение установки в качестве Progressive Web App содержит:

автономный режим отображения;
портретную ориентацию;
темы и фоновые приложения;
набор пиктограмм;
сервис-воркер для кеширования файлов.
Разработка исходного приложения
В репозитории находятся только готовая сборка, а не исходные файлы Flutter ( lib/, pubspec.yamlи т. п.).

Для внесения изменений необходимо открыть проект во Flutter с исходным кодом, внести изменения и выполнить заново:

flutter build web --release
Лицензия
Лицензия не указана. Перед использованием проекта или его распространением необходимо уточнить условия содержания у автора.

Автор
ЛиамБелл
