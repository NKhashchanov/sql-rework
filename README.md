## Домашнее задание по теме "Введение в SQL. Установка ПО"
База данных: *world-db*
### Основная часть:

- создать новое соединение в *DBeaver* 
- подключить облачную базу данных *world-db* (реквизиты те же, что и у *dvd-rental* из инструкции, 
только название базы данных *world-db*)
- в качестве результата прислать **2** скриншота: диаграмму ER и результат запроса ```select * from country;```

### Дополнительная часть:

Выполнить основную часть используя контейнер Docker.
Для этого нужно использовать датасет  
*ghusta/postgres-world-db*  
database : *world-db*  
user : *world*  
password : *world123*  



## Домашнее задание по теме "Работа с базами данных"
База данных: *dvd-rental*
### Основная часть:

- перечислить все таблицы и первичные ключи в базе данных. Форма решения в виде таблицы:  
 | Название таблицы | Первичный ключ |  
- вывести всех **неактивных** покупателей  
- вывести все фильмы, **выпущенные** в 2006 году  
- вывести 10 последних **платежей** за прокат фильмов. 
Самостоятельно прочитать про limit и offset в postgresql (например тут - 
http://www.postgresqltutorial.com/postgresql-limit/)

### Дополнительная часть:

- вывести первичные ключи через запрос
- найти ошибку в данных по неактивным покупателям
- кратко описать, чем *film_actor_pkey* отличается от *actor_pkey* 



## Домашнее задание по теме "Основы SQL"
База данных: *dvd-rental*
### Основная часть:

- выведите магазины, имеющие больше **300-от** покупателей  
- выведите у каждого покупателя **город** в котором он живет

### Дополнительная часть:

- выведите **ФИО сотрудников** и **города** магазинов, имеющих больше **300-от** покупателей  
- выведите **количество актеров**, снимавшихся в фильмах, которые сдаются в аренду за **2,99**



## Домашнее задание по теме "Углубление в SQL"
База данных: если подключение к облачной базе, то создаете новые таблицы в формате: *таблица_фамилия*, если 
подключение к контейнеру или локальному серверу, то создаете новую схему и в ней создаете таблицы.  
### Основная часть:

Спроектируйте базу данных для следующих сущностей:  
- язык (в смысле английский, французский и тп)  
- народность (в смысле славяне, англосаксы и тп)  
- страны (в смысле Россия, Германия и тп)

Правила следующие:
- на одном языке может говорить несколько народностей
- одна народность может входить в несколько стран
- каждая страна может состоять из нескольких народностей

Суть задания - научиться проектировать архитектуру и работать с **ограничениями**.
Таким образом должно получиться **5 таблиц**. Три таблицы-справочника и две таблицы со связями.

Пришлите скрипты **создания таблиц** и **скрипты по добавлению** в каждую таблицу по **5** строк с данными

### Дополнительная часть:

- показать, как назначать внешние ключи краткой записью при создании таблицы и как можно присвоить 
внешние ключи для столбцов существующей таблицы
- масштабировать получившуюся базу данных используя следующие типы данных: *timestamp*, *boolean* и *text[]* 