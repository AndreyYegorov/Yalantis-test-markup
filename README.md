# Стартовый шаблон для Front-End разработки

Данный шаблон создан для удобства разработки статических страниц фронтенд проектов.

## Используемые технологии для сборки проекта

- `nodejs и npm` - язык nodejs и его пакетный менеджер
- `gulp` - сборщик проекта
- `sass` - препроцессор css
- `pug` - шаблонизатор html

## Начало работы

``` sh
$ npm install
$ npm start
```

## Общая структура проекта

- `src/` - папка рабочего проекта. Все работы с проектом должны проводиться здесь
- `build/` - папка финальной версии верстки
- `design/` - папка для файлов макетов дизайна
- `.gitignore` - файл git для записи игнорируемых каталогов
- `gulpfile.js` - файл заданий gulp
- `package.json` - файл npm-менеджера

## Структура каталога `src/`

### Папка `components/`
 
В этой папке находятся все компоненты проекта. Каждый компоненты находится в папке соответствующей его имени, например `nav/`, `nav-aside/`, `article/`, `form/`. Внутри папки компонента размещаются файлы с расширениями `.pug`, `.scss`, `.js`, имена файлов соотвествуют названию компонента.

### Папка `css/`
 
В этой папке находятся все стили и шрифты проекта.

- папка `common/` содержит в себе общие стили проекта `normalize.scss`, `base.scss`, `fonts.scss`, `layout.scss`, `variables.scss` и т.д
- в папке `fonts/` располагаются все шрифты проекта
- в папке `plugins/` находятся все стили подключенных плагинов с расширением `.css`
- файл `style.scss` подключает в себя все стили проекта: общие стили проекта, стили компонентов, но стили плагинов не подключаются в этот файл, они подключаются в `head-тэг` html-файлов
- скомпилированный файл `style.css` стилей проекта (кроме стилей плагинов). Подключается в `head-тэг` html-файлов

### Папка `img/`

Содержит в себе все изображения проекта.

### Папка `media/`

Содержит в себе все видео и аудио файлы проекта.

### Папка `js/`

В папке находятся все скрипты проекта.

- папка `libs/` содержит в себе сторонние библиотеки `jquery.js`, `jquery-ui.js`, `modernizr.js` и т.д. Подключаются в `head-тэг` html-файлов
- в папке `plugins/` располагаются сторонние плагины для проекта. Подключаются в `head-тэг` html-файлов
- файл `common.js` содержит скрипты общие для всего проекта. Подключается в `head-тэг` html-файлов
- файл `components.js` содержит скрипты компонентов проекта, объединённые в этот один файл. Подключается в `head-тэг` html-файлов

### Папка `metadata/`

Содержит в себе метаданные html-файлов в виде файлов с расширением `.pug`, например `head.pug`.

### Папка `views/`

В этой папке находятся все шаблоны-страницы проекта, файлы с расширением `.pug`, например `index.pug`, `inner.pug`. Эти файлы подключают все зависимые файлы с расширением `.pug`, а именно файлы метаданных и файлы компонентов.

### HTML-файлы в корне проекта

Скомпилированные html-страницы проекта. Открывать эти файлы в браузере.

## Создание build-версии

Это команда позволяет создать build-версию проекта, содержащюю в себе min-файлы `.js` и `.css`.

``` sh
$ npm run build
```