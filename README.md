Восстановление буквы «ё» в русских текстах
===
[![NPM version](https://img.shields.io/npm/v/eyo.svg?style=flat)](https://www.npmjs.com/package/eyo)
[![NPM downloads](https://img.shields.io/npm/dm/eyo.svg?style=flat)](https://www.npmjs.com/package/eyo)
[![Build Status](https://img.shields.io/travis/hcodes/eyo.svg?style=flat)](https://travis-ci.org/hcodes/eyo)
[![Build Status](https://img.shields.io/appveyor/ci/hcodes/eyo/master.svg?style=flat)](https://ci.appveyor.com/project/hcodes/eyo)
[![Coverage Status](https://img.shields.io/coveralls/hcodes/eyo.svg?style=flat)](https://coveralls.io/r/hcodes/eyo)

[![Dependency Status](https://img.shields.io/david/hcodes/eyo.svg?style=flat)](https://david-dm.org/hcodes/eyo) [![devDependency Status](https://img.shields.io/david/dev/hcodes/eyo.svg?style=flat)](https://david-dm.org/hcodes/eyo#info=devDependencies)

Частичное портирование [php-yoficator](https://code.google.com/p/php-yoficator/).

## Особенности
+ восстановление буквы «ё» в русских текстах, вместо написанной «е»;
+ замена «е» на «ё» только в бесспорных случаях;
+ исправление в словах нескольких букв «е», «ё»;
+ корректная обработка сокращений («мед. училище», но не «мёд. училище»);
+ аббревиатуры не обрабатываются.

## Установка
`npm install eyo -g`

## Командная строка
`eyo file.txt > file.out.txt` — замена «е» на «ё» в файле.<br/>
`eyo http://example.com/index.html > file.out.txt` — замена «е» на «ё» на странице сайта.

`cat file1.txt file2.txt file3.txt | eyo`

`eyo -l file.txt` — вывод слов для файла, где необходима замена.<br/>
`eyo -l https://example.com/index.html` — вывод слов для страницы сайта, где необходима замена.

## Node.js
`npm install eyo`

```
var eyo = require('eyo');
console.log(eyo.restore('Лед')); // Лёд
```

## Ссылки
+ [http://ru.wikipedia.org/wiki/Ёфикатор](https://ru.wikipedia.org/wiki/%D0%81%D1%84%D0%B8%D0%BA%D0%B0%D1%82%D0%BE%D1%80)

## [Лицензия](./LICENSE.md)
MIT License
