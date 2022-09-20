# FiveDaysWeatherBot

## Описание проекта:
Бот предоставляет возможность узнать прогноз погоды на пять дней в любом городе, используя приложение телеграм.

## Настройка и установка:
1. Запустите IntelliJ IDEA и создайте новый файл, используя GIT (File -> New -> Project from Version Control...).
2. Ссылка для скачивания https://github.com/Nik00102/FiveDaysWeatherBot.git .
3. Скомпилируйте файл FiveDaysWeatherBotApplication.java.
4. Зарегистрируйтесь на сайте погоды https://openweathermap.org/, после регистрации будет доступен ключ API (*apiKey*).
5. Получите токен (*botToken*) и создайте нового бота (*botUserName*) через @BotFather в телеграме коммандой "/newbot".
6. Записать все полученные *apiKey*, *botToken*, *botUserName* в файл application.properties (расположен в папке */src/main/resources/*)
7. Зарегистрируйтесь на сайте Heroku.com и создайте приложение на сайте (Heroku - это облачная платформа, и ее можго использовать для того, чтобы запускать приложение не только на локальной машине, но и удаленно).
8. Конфигурационный файл Procfile (без расширения, важно!) уже есть в директории проекта.
    Содержимое Procfile: **web: java -jar target/FiveDaysWeatherBot-0.0.1-SNAPSHOT.jar**
 9. В папке с проектом в командной строке или bash необходимо выполнить команду: 
 **heroku login**
 10. Инициализировать репозиторий:
**git init** 
11. Создать новый контейнер heroku:
**heroku git:remote -a @имя вашего приложения@**
12. Загрузить проект 
**git push heroku master**
13. Запустить бота
**heroku ps:scale web=1**
14. Остановить бота
**heroku ps:scale web=0**
15. Получить лог
**heroku logs --tail**
