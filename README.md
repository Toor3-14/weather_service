### Задание

Напишите службу REST с одной конечной точкой `/weather`.

Требования:

- При вызове этот сервис должен запросить в базе данных текущую погоду (температуру) в таблице «weather_history». 
- Если на текущую дату в базе данных не найдено ни одной записи, то необходимо считать текущее значение температуры с сервиса «openweathermap.org». 
- После считывания температуры он должен вставить новую запись в «weather_history». 
- В конце концов, он должен вернуть пользователю значение температуры.

Заметки:

- Вы можете использовать любую среду Java для создания веб-службы (например, Spring).
- Вы можете использовать любую базу данных для хранения исторических данных (например, H2 или PostgreSQL).
- Для взаимодействия с базой данных можно использовать интерфейсы JDBC или JPA.
- Для чтения веб-страницы и извлечения значений температуры используйте стандартные классы Java (нет необходимости использовать дополнительную библиотеку).
- Таблица Weather_history состоит из двух столбцов:
     - date DATE 
     - temperature DECIMAL
     


### Инструкция

Собрать проект
```
./gradlew build 
```



Запустить сервис
```
./gradlew bootRun - 
```


Запустить тесты

``` 
 ./gradlew test
```


Запустить докер

```
docker build -t api .

docker run -p 9009:9009 api
```