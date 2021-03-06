## Запуск проекта
### Необходимо
NodeJS версии `v4.1.x`+ и NPM `2.14.x`+
```
 brew install node
```
Установить глобально пакеты `webpack`, `ts-node` и  `typescript`
```
 npm install --global webpack
 npm install --global ts-node
 npm install --global typescript
```

### Старт
Клонируем репозиторий в нужную директорию (ProjectName)
```
git clone https://github.com/awibox/bem-builder-angular.git ProjectName
```
Переходим в директорию проекта
```
cd ProjectName
```
Устанавливаем окружение из package.json
```
npm install
```
Запускаем проект
```
npm start
```
Открыть [http://0.0.0.0:3000](http://0.0.0.0:3000) или [http://localhost:3000](http://localhost:3000) в браузере

###Добавление страниц и модулей
Для коректной работы необходимо установить `gsed`
```
brew install gnu-sed
```
Добавление страницы
```
./add page [Page Name]
```
Добавление модуля
```
./add module [Module Name]
```
Если скрипт не работает:
```
source add
chmod 777 add
```

## Структура проекта

```
bem-builder-angular/
 ├──public/ 
 |   └──index.html                            * индексный html-файл
 ├──source/                                   * папка с исходниками         
 |   ├──app
 │   │   ├──pages                             * страницы 
 │   │   │   ├──home
 │   │   │   │   ├──home.ts                   * компонент сраницы
 │   │   │   │   ├──home.html                 * шаблон страницы
 │   │   │   │   └──home.scss                 * стили страницы
 │   │   │   └──...
 │   │   └──app.ts                            * основной файл приложения
 │   │
 |   ├──build                                 * папка с настойками сборки
 │   │   ├──sass  
 │   │   │   ├──build.scss                    * настройка сборки sass
 │   │   │   └──retina.scss                   * стили для ретина-экранов
 │   │   ├──main.ts                           * настройка сборки main.js
 │   │   └──vendor.ts                         * настройка сборки vendor.js
 │   │
 |   └──modules                               * папка с модулями
 │       ├──player
 │       │   ├──pipes                         * pipes для модуля
 │       │   ├──player.ts                     * описание моудля в typescript
 │       │   ├──player.html                   * шаблон модуля
 │       │   └──player.scss                   * стили модуля
 │       └──...
 │
 ├──add                                       * cкрипт для добавления модулей и страниц
 │
 ├──test/                                     * тесты
 │
 ├──tsconfig.json                             * настройки typescript
 ├──typings.json                              * описание typings
 ├──package.json                              * описание окружения для npm i
 │
 ├──webpack.config.js                         * конфигурация сборки webpack
 └──webpack.test.config.js                    * конфигурация webpack для тестов
```
