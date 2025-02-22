## Набор скриптов для работы с TMDB
Все скрипты в данном наборе работают с сервисом TMDB, а также с его результатами.  

### hello_api_TMDB
Скрипт для проверки API-ключа на работоспособность.  
Запрашивает API-ключ и делает запрос к api сервиса.  
Если ключ не рабочий, то выводится соответствующее сообщение об этом.  
Скрипт использует вспомогательные функции для работы из файла tmdb_helpers.

### tmdb_helpers
Вспомогательные функции для запросов к api сервиса.

### search_in_db
Поиск фильма в собственной базе данных пользователя.  
Скрипт запрашивает путь к файлу базы данных.  
Если такой файл существует, производит поиск фильма в нём и выводит в консоль результаты поиска.  
Результат содержит фильмы, которые либо точно, либо частично соответсвуют указанному названию.  
Скрипт использует вспомогательные функции из файла own_db_helpers.  

### own_db_helpers
Вспомогательные функции для работы с собственной базой данных.  

### make_own_db
Создание локальной базы данных на основе фильмов с сервиса.  
Запрашивает API-ключ и скачивает первые 1000 фильмов из базы TMDB.  
Информация о фильмах записывается в файл MyFilmDB.json.  
Скрипт использует вспомогательные функции для работы из файла tmdb_helpers.  

### find similar
Рекомендательная система для фильмов.  
Спрашивет путь к базе данных с фильмами, а также желаемый фильм.  
Выводит в консоль 8 похожих фильмов на указанный пользователем.  
Фильмы ранжируются по рейтингу. Рейтинг высчитывается на основе параметров заданных в скрипте.  
