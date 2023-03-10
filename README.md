# Лабораторная работа №1 по курсу "Анализ уязвимостей программного обеспечения"
___

## Требования к окружению

1. jdk-17
2. maven2
3. docker compose

## Запуск приложения

1. Для сборки приложения использовать команду:
```
mvn clean package -P build
```
Для сборки необходим запущенный докер, так как в нём поднимается тестовая БД, в которой применяются миграции и генерируются jooq-классы.

2. Для запуска приложения и БД в контейнерах:
```
docker-compose up
```

## Спецификация АПИ
http://localhost:8080/aupo/api/swagger-ui/index.html после запуска приложения

## Логи
Записываются в logs.txt

## Загрузка csv-файлов
### Формат:
Разделитель - точка с запятой, без строки с заголовками.  
Порядок:  
Для сущности ученик:
id сущности, Фамилия, Имя, Отчество, id класса

Пример:

| 1   | Иванов  | Иван   | Иванович   | 1   |
|-----|---------|--------|------------|-----|
| 2   | Антонов | Антон  | Иванович   | 1   |
| 4   | Буянов  | Никита | Васильевич | 1   |

Для сущности класс:  
id сущности, id параллели, id учителя, id учебного года

Пример (?):

| 1   | 2   | 3   | 1   |
|-----|-----|-----|-----|
| 2   | 4   | 2   | 3   |
| 4   | 1   | 3   | 2   |