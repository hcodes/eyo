Восстановление буквы «ё» в русских текстах
===
[![NPM version](https://img.shields.io/npm/v/eyo.svg?style=flat)](https://www.npmjs.com/package/eyo)
[![NPM downloads](https://img.shields.io/npm/dm/eyo.svg?style=flat)](https://www.npmjs.com/package/eyo)
[![Build Status](https://img.shields.io/travis/hcodes/eyo.svg?style=flat)](https://travis-ci.org/hcodes/eyo)
[![Build Status](https://img.shields.io/appveyor/ci/hcodes/eyo/master.svg?style=flat)](https://ci.appveyor.com/project/hcodes/eyo)
[![Coverage Status](https://img.shields.io/coveralls/hcodes/eyo.svg?style=flat)](https://coveralls.io/r/hcodes/eyo)
[![Dependency Status](https://img.shields.io/david/hcodes/eyo.svg?style=flat)](https://david-dm.org/hcodes/eyo)

<img src="https://raw.githubusercontent.com/hcodes/eyo/master/images/logo.png" align="right" alt="eyo" width="200" height="200" />

## Особенности
+ проверка и восстановление буквы «ё» в русских текстах, вместо написанной «е»;
+ замена «е» на «ё» только в бесспорных случаях;
+ исправление в словах нескольких букв «е», «ё»;
+ корректная обработка сокращений («мед. училище», но не «мёд. училище»);
+ аббревиатуры не обрабатываются.

![eyo](https://raw.githubusercontent.com/hcodes/eyo/master/images/screenshot.png)


## Установка
`npm install eyo -g`

## Командная строка
```
Usage: eyo [options] <file-or-url...>
    Restoring the letter «ё» (yo) in russian texts.

Options:
    -h, --help       Output usage information
    -V, --version    Output the version number
    -l, --lint       Search of safe and unsafe replacements
    -s, --sort       Sort results
        --no-colors  Clean output without colors
```

### Примеры использования
`eyo file.txt > file.out.txt` — безопасная замена «е» на «ё» в файле.<br/>
`eyo https://example.com/index.html > file.out.html` — безопасная замена «е» на «ё» на странице сайта.

`cat file1.txt file2.txt file3.txt | eyo`

`eyo --lint file1.txt file2.txt` — вывод слов для файлов, где необходима или возможна замена.<br/>
`eyo --lint http://habrahabr.ru` — вывод слов для страницы сайта, где необходима или возможна замена.

## Node.js

Используйте отдельный пакет [`eyo-kernel`](https://www.npmjs.com/package/eyo-kernel) без зависимостей.

`npm install eyo-kernel`

```js
var eyo = require('eyo-kernel');
console.log(eyo.restore('Лед')); // Лёд
```

## Ссылки
+ [Ёфикация в браузере](https://hcodes.github.io/eyo-browser/)
+ [eyo-kernel](https://www.npmjs.com/package/eyo-kernel) — отдельный пакет для ёфикации без зависимостей
+ [https://ru.wikipedia.org/wiki/Ёфикатор](https://ru.wikipedia.org/wiki/%D0%81%D1%84%D0%B8%D0%BA%D0%B0%D1%82%D0%BE%D1%80)
+ [Про букву ё](http://www.gramota.ru/class/istiny/istiny_7_jo/)
+ [Поиск опечаток в тексте](https://github.com/hcodes/yaspeller)

## [Лицензия](./LICENSE)
MIT License
