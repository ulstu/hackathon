# Хакатон ФИСТ УлГТУ
18.09.2019 - 19.09.2019
Место проведения: УлГТУ, г.Ульяновск, ул. Северный Венец, 32, "Дом интернета" в ККЗ "Тарелка" им. Стениной Т.Л.

## WiFi
SSID: cnit_5GHz, cnit_5GHz
password: treugolnik

## Telegram канал
http://t.me/ithackathonss

## Задания
### Ростелеком Информационные Технологии
1. 'Dropbox' для студентов. Сервис для обмена файлами, статьями, аудио и видео информацией между студентами одного направления, факультета и т.д.
2. Сервис по подбору книг и ресурсов для обучения по выбранной специальности. Ограничение: тематика ИТ. Например, язык программирования, технология. Сервис должен искать в Интернете (например, на сайтах онлайн-обучения курсы под выбранную тематику, а на сайтах онлайн-магазинов книги). При этом должны учитываться отзывы о курсе и преподавателе, рейтинги и другая доступная информация.
3. Сервис проверки знаний - автоматическое составление вопросов в виде теста на основе прочитанной книги. За основу могут браться определённые части книги - аннотации, заключения и т.д.

### Simtech
Задание на хакатон от группы компаний Simtech

#### 1. "Определение местоположения пользователя"

Создать страницу, на которой будет отображаться информация по IP пользователя, страницу личного кабинета с историей посещения и список последних 10 пользователей, кто посетил главную страницу.

Страница "Определение информации":
Пользователь переходит на страницу и ему отображается информация о его местонахождении:
   - страна (название)
   - страна (код страны)
   - город
   - регион

Можно использовать сервис https://dadata.ru/api/detect_address_by_ip/ или другие аналогичные.
Форматированно вывести информацию на главную страницу.

Страница регистрации:
Пользователь может зарегистрироваться. Нужно указать имейл, имя и пароль. Не может быть нескольких пользователей с одинаковым имейлом.

Страница личного кабинета пользователя:
Если он не зарегистрирован в системе, то попасть на эту страницу невозможно. После регистрации каждое его посещение страницы "Определение информации" должно сохранятся в истории. В личном кабинете можно зайти и увидеть эту историю.

Список "Последние 10 человек, которые посетили страницу "Определение информации"":
На странице "Определение информации" должен быть блок, который динамически отображает информацию о последних 10 пользователях, кто посетил страницу, вида "IP->Страна->Регион".
Если пользователь был зарегистрирован, то его нужно отображать как "Имя->IP->Страна->Регион".

#### 2. Реализация простой API системы для управления товарами.

Необходимо реализоваь API систему для управления товарами со следующими параметрами: авторизация в системе, создание товара, отображение товара, обновление товара, удаление товара.

Авторизация:
Входные данные (обязательные поля отмечены символом *):
   - логин*
   - пароль*
Ответ:
   - временный сессионный ключ, который действует 30 минут.
Сообщения об ошибках:
   - не верный логин или пароль

Создание товара:
Входные данные (обязательные поля отмечены символом *):
   - сессионный ключ*
   - название*
   - цена*
   - категория*
   - описание
   - количество*
Ответ:
   - ID товара
   - сообщение об успешном создании
Сообщения об ошибках:
   - не хватает обязательного поля (отобразить что за поле)
   - несоответствие типов (например, в качестве цены передана строка)
   - неавторизованный пользователь

Отображение товара:
Входные данные (обязательные поля отмечены символом *):
   - сессионный ключ*
   - ID товара*
Ответ:
   - ID товара
   - название
   - цена
   - категория
   - описание
   - количество
Сообщения об ошибках:
   - не хватает обязательного поля (отобразить что за поле)
   - несоответствие типов (например, в качестве ID передана строка)
   - неавторизованный пользователь
   - нет такого ID

Обновление товара:
Входные данные (обязательные поля отмечены символом *):
   - сессионный ключ*
   - id товара*
   - название
   - цена
   - категория
   - описание
   - количество
Ответ:
   - ID товара
   - сообщение, что товар успешно обновлён
Сообщения об ошибках:
   - не хватает обязательного поля (отобразить что за поле)
   - несоответствие типов (например, в качестве ID передана строка)
   - неавторизованный пользователь
   - нет такого ID

Удаление товара:
Входные данные (обязательные поля отмечены символом *):
   - сессионный ключ*
   - id товара*
Ответ:
   - id товара
   - сообщение, что товар успешно удалён
Сообщения об ошибках:
   - не хватает обязательного поля (отобразить что за поле)
   - несоответствие типов (например, в качестве ID передана строка)
   - неавторизованный пользователь
   - нет такого ID

Доп. задачи:
- добавить логирование всех запросов (в файлик или в базу с возможностью отобразить)
- сделать массовое отображение товаров (передаём список ID, возвращается несколько товаров)
- сделать массовое создание (передаём несколько блоков с информацией о товарах)
- сделать массовое редактирование (передаём несколько блоков с информацией о товарах)
- сделать массовое удаление (передаём несколько ID товаров)
- сделать поиск (например, отображать товары, у которых одинаковая категория или по диапазону цен)
- написать документацию с примерами

### TrueMachine

#### 1. Карта чрезвычайних ситуаций и преступлений
В США подобную систему активно используют горожане, с помощью нее через мобильное приложение на карте отмечаются красные точки, нажав на которые ты можешь узнать, что произошло: кража, пожар, выстрелы, человеку плохо. И люди могут оставлять комментарии (чат) и вести прямую трансляцию из этой точки из приложения. Тогда у всех жителей есть мгновенный источник получения информации из проблемной зоны: на основе этого можно принимать решения - проезжать или проходить мимо этих точек, например если это была перестрелка, то лучше проехать мимо и не соваться в проблемную зону; а если пожар или плохо человеку, то люди поблизости могут помочь, чтобы предовратить тяжелые последствия, не дожидаясь службу. Эти точки в систему добавляются через службу 911 автоматически. К сожалению, в России подобного решения нет.
Поэтому наш кейс предлагает разработать похожую систему. Но так как сделать интеграцию с системой 112 - это не быстро в рамках одного хакатона, поэтому TrueMachine предоставит запрос, который будет возвращать json с проблемными точками - с типом проишествия, координаты и степень опасности (чтобы окрашивать точки в разные цвета). В первой версии (то что на хакатоне) - нужно будет сделать веб и мобайл версию, в которой будут выводиться эти точки, нажав на которые можно будет просомтреть комментарии и оставить свой комментарий. В будущем эту систему можно будет предлагать городу, добавлять возможность вести прямые трансляции и многое другое.

#### 2. Система сбора ошибок
Есть множество ошибок при разработке, которые нужно отслеживать в режиме реального времени - если произошел свой в системе - разработчики должны получить уведомление об этом (на почту, телегу, слак и тд). Сейчас существует множество систем, но их основной минус - они платные и порой нагруженные. Например, для простых проектов достаточно функицонала уведомлений о сбое, информации об ошибке - объект exception’а, и стенд (стейджинг или боевой сервер).
В рамках кейса предлагается разработать сервис сбора ошибок, работающий через  HTTP протокол. При выбросе исключения в коде, на сервер отправляетсяз запрос, а уже сервер рассылает уведомления разработчикам.

#### 3. Менеджер паролей
В 2019 множество сервисов, в которых вход организован по email и паролю. Есть проблема запоминания этих паролей, а использовать один и тот же пароль на всех сервисах - небезопасно. Поэтому требуется решение, которое будет хранить пароли пользователя в различных сервисах. Вход в приложение осуществляется по биометрии или по пинкоду. Приложение должно соответсвовать требованиям безопасности, и хранить на сервере сами пароли нельзя.

#### 4. Задача со звездочкой*
Проверка наличия свободных столиков в кафе, ресторанах и кальяных.
Часто в пятницу после работы компания друзей решает отдохнуть в кафе или кальяной. Но такая компания не одна, и любимые заведения могут быть заняты или просто нет мест на то кол-во персон, коорое требуется. Не у каждого заведения есть свой API для проверки доступности, а если есть, то интегрировать каждое кафе - не целесообразно и затратно. Но зато у каждого заведения есть администратор и номер телефона. Поэтому в рамках кейса нужен робот, который прозванивает все желаемые кафе и уточняет у администраторов - есть ли на данный момент N мест в кафе. На выходе робот выдает список кафе, в которых есть свободные места на N персон. Тогда компании остается лишь позвонить одному кафе, чтобы забронировать места на ближайшее время, вместо совершения нескольких звонков.

### Команда RoboLife ФИСТ УлГТУ
#### 1. Разработать робота на омниколесах с манипулятором, управляемым с использованием сенсора Kinect
#### 2. Разработать мобильного робота, управляемого через телефон через Bluetooth
