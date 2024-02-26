---
tags: SQL
---
## Что такое данные, информация, база данных? Что «под капотом» БД?
[Данные и информация](https://eopearhiiv.edu.ee/e-kursused/eucip/arendus_vk/211___.html)

>[!Info]+ Информация
>**Информация** - факты, события, вещи, процессы, идеи, понятия или иные касающиеся объектов знания, которые имеет особое значение в определенном контексте.
>
>В организации необходимую информацию в основном сохраняют в документах (в цифровой форме или на бумажном носителе), а данные, главным образом, в базах данных.
>
>Информация может быть определена как сообщение, которое выступает в виде документа или коммуникации в аудиовизуальной форме. Как и у каждого сообщения, так и у информации имеются отправитель и получатель. Задача информации - влиять на суждение и поведение получателя. В отличие от данных у информации имеются смысл, значимость и назначение. Данные становятся информацией, если их создатель добавляет к ним смысл. Важно отметить, что ИТ помогает превращать данные в информацию, а также добавлять им смысловую ценность. Тем не менее, ИТ не помогает в создании контекста (категории, калькуляции, формы) - все это создают люди.

>[!Info]+ Данные
>Называют формализованный способ представления информации в понятной для человека и / или машины форме (отформатированной специальным образом), которую можно использовать для общения, трактовки, сохранения или обработки.
>
>Данные являются детальными, объективными фактами событий. Все организации нуждаются в данных, и большинство сфер деятельности основано на них (данных). Эффективное управление данными - это одно из важнейших критериев успеха, в противоположность этому, большой объем данных, безусловно, еще не является критерием успеха.
>
>Нет возможности автоматически вывести правильные решения на основе большого набора данных объективно по двум причинам.
>
>Во-первых, слишком большой объем данных делает данные трудными для идентификации и для осмысления их значения. Во-вторых (это также главная причина), у данных по своей сути нет значения. Данные характеризуют или описывают только произошедшее, они не включают ни оценок, ни вдохновения. Для организации данные все же очень значимы, поскольку на их основе создают информацию.

**База данных — это набор данных, хранящиеся в структурированном виде.**

**Система управления базами данных СУБД** — это совокупность языковых и
программных средств, которая осуществляет доступ к данным, позволяет их создавать, менять и удалять, обеспечивает безопасность данных.
[[БД img.png|БД и СУБД]]
Семь из десяти самых популярных СУБД — реляционные (связанные, relation/связь)
Это Oracle, MySQL, Microsoft SQL Server, PostgreSQL, IBM Db2, Microsoft Access, SQLite.

Есть также: MongoDB – документ- ориентированная СУБД; Redis - хранилище по типу «ключ-значение»; Elasticsearch - поисковой движок

[[Типы баз данных]], [[Структура данных в БД]], [[Представление VIEW и временные таблицы]]
## Что такое SQL?
Язык программирования структурированных запросов **Structured Query Language**, SQL.
[[Пояснение SQL.png|Принцип клиент серверных отношений SQL]]
![[Основные операторы SQL и пример реляционной БД.png]]
Revoke - отзывает разрешения
Deny - запрещает
Grant - дает разшение
## Какие бывают связи таблиц SQL?

| Тип связи | Пример |
| ---- | ---- |
| Многие ко многим<br>**@ManyToMany** | Каждому работнику соответствует одна и более должностей.<br>Каждой должности соответствует один и более работников. |
| Один ко многим<br>**@OneToMany** | Вариант: **связь ОБЯЗАТЕЛЬНА**: телефон принадлежит только одному пользователю, а пользователю могут принадлежать один и более телефонов<br>Вариант: **связь НЕ обязательна**: на Земле живут все люди. Каждый человек живет на Земле. Но платена может существовать без людей |
| Один к одному<br>**@OneToOne** | Вариант: **связь обязательна**: у загранпаспорта обязательно должен быть один владелец. В этом случае это обязательная связь<br>Вариант: **связь не обязательна**: наличие загранпаспорта необязательна - его может и не быть у гражданина. Это необязательная связь |


<!-- ![[Связи таблиц в SQL.png]] -->
## Операции SQL по группам

| Оператор                         | Пояснение                                                      |
| -------------------------------- | -------------------------------------------------------------- |
| DDL Data Definition Language     | Создание структуры БД и ее объектов                            |
| DML Data Manipulation Language   | Взаимодействие с данными: вставка, удаление, изменение, чтение |
| TCL Transaction Control Language | Управление транзакциями                                        |
| DCL Data Control Language        | Управление правами доступа к данным и структурам БД                                                               |
[[Операции SQL по группам]]
## Выборка
Базовый синтаксис SQL запроса
- [[Исключение дубликатов, DISTINCT]]
Условный оператор [[Условный оператор WHERE|WHERE]]
- [[Операторы IS NULL BETWEEN IN]]
- [[Оператор LIKE]]
Сортировка группировка [[Оператор ORDER BY]], [[Оператор GROUP BY|GROUP BY]]
- [[Агрегатные функции]]
- [[Оператор HAVING]]
Многотабличные запросы, операция [[Многотабличные запросы операция JOIN|JOIN]]
- [[INNER JOIN]], [[OUTER JOIN]]
Ограничение выборки, [[Оператор LIMIT]]
- [[Подзапросы]] [[Что лучше подзапросы или JOIN]]
	- [[Подзапросы с одной строкой и одним столбцом]]
	- [[Подзапросы с несколькими строками и одним столбцом]]
- [[Оператор EXISTS]]

[[Объединение запросов, оператор UNION]]
- [[Запрос из 2х таблиц]]

## Манипуляции с данными
- [[Оператор MERGE ]]
- [[Сравнение TRUNCATE и DELETE]]
### Форматы данных
[[TIMESTAMP]]

## Ограничения и ключи
[[Ограничения, constraints]]
[[Ключи БД]]

## Производительность, ресурсы системы
[[SQL оценка производительности]]
- [[Транзакции принцип ACID]]
- [[Нормализация денормализация]]
- [[Шардирование базы данных]]

[[SQL инъекции]]