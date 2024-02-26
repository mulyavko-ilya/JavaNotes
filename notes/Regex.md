---
aliases: регулярные выражения 
tags: Regex
---
Регулярные выражения (их еще называют _regexp_, или _regex_) — это механизм для поиска и замены текста. В строке, файле, нескольких файлах... Их используют разработчики в коде приложения, тестировщики в автотестах, да просто при работе в командной строке!

## Поиск лишних переносов строки внутри абзаца

`(?<=[^\n])\n(?=[^\n])`

Пояснение:

- `(?<=[^\n])` - позитивное ретроспективное условие, которое ищет перенос строки (`\n`), за которым следует любой символ, кроме переноса строки.
- `\n` - символ переноса строки.
- `(?=[^\n])` - позитивное проспективное условие, которое ищет перенос строки (`\n`), перед которым следует любой символ, кроме переноса строки.


https://habr.com/ru/post/545150/