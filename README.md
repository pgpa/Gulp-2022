# Gulp-2022
Сборка Gulp-2022

 Структура:
  src - исходники;
  gulp  - вспомогательные файлы;
      config - настройки;
      tasks - таски;
  dist - результат (создается автоматически);

Экспорт по FTP:
	- Заполняем файл ftp.js
	- Устанавливаем папку (в которую на сервере выгрузить файлы)
 	   в path.js (ftp: 'test')
    Запуск 
	npm run deplou

    Автоматическкая передача по FTP:
	в файле gulpfile.js 
	function watcher() {
	...
	gulp.watch(path.watch.html, html) // 'html' меняем на 'gulp.series(html, ftp)'
	... // аналогично и в др...
	}

Перенос сборки в новый проэкт.

     Забираем:
             2 папки :
           	gulp
	src
            2 файла
	gulpfile.js
	package.json
	
      Заменяем:
	"browser-sync": "^2.27.7" на
	"browser-sync": "latest" - для всех, кроме:

	"webp-converter": "^2.2.3" меняем на
	"webp-converter": "2.2.3"
    
        Установка:
	
          1.  Установка с нуля:
	Проверяем верси:
		node -v
		npm -v  
		gulp -v

	если не устанавливали,то устанавливаем:
	    Node - https://nodejs.org/ - качаем версию LTS
             	   (далее команды в папке  нового проэкта:)
	    npm i gulp-cli -g - установка Gulp глобально
               если устанавливали то:

          2.  Установка не с нуля :) :
	npm i - инициализация среды	

        Запуск в режиме разработчика
	npm run dev
       Создание .zip
	npm run zip

Создание нового проэкта:
	1. смотрим п.1 выше
	2.  npm i gulp -D      - установка Gulp локально
		и т.д. и т.п.


Сборка Gulp.
    Версии:
	node -v          v16.13.2	
	npm -v           8.1.2
	gulp -v	CLI version: 2.3.0
		Local version: 4.0.2

"devDependencies": {
    "browser-sync": "^2.27.7",
    "del": "^6.0.0",
    "fs": "^0.0.1-security",
    "gulp": "^4.0.2",
    "gulp-autoprefixer": "^8.0.0",
    "gulp-clean-css": "^4.3.0",
    "gulp-file-include": "^2.3.0",
    "gulp-fonter": "^0.3.0",
    "gulp-ftp": "^1.1.0",
    "gulp-group-css-media-queries": "^1.2.2",
    "gulp-if": "^3.0.0",
    "gulp-imagemin": "^8.0.0",
    "gulp-newer": "^1.4.0",
    "gulp-notify": "^4.0.0",
    "gulp-plumber": "^1.2.1",
    "gulp-rename": "^2.0.0",
    "gulp-replace": "^1.1.3",
    "gulp-sass": "^5.0.0",
    "gulp-svg-sprite": "^1.5.0",
    "gulp-ttf2woff2": "^4.0.1",
    "gulp-util": "^3.0.8",
    "gulp-version-number": "^0.2.4",
    "gulp-webp": "^4.0.1",
    "gulp-webp-html-nosvg": "^1.0.1",
    "gulp-webpcss": "^1.1.1",
    "gulp-zip": "^5.1.0",
    "sass": "^1.45.1",
    "swiper": "^7.3.4",
    "vinyl-ftp": "^0.6.1",
    "webp-converter": "^2.2.3",
    "webpack": "^5.65.0",
    "webpack-stream": "^7.0.0"
  }
