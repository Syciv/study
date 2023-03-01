# Лабораторная работа №1 по курсу "Анализ уязвимостей программного обеспечения"
___

## Требования к окружению

1. jdk-17
2. maven2
3. docker compose

## Запуск приложения

1. Для сборки приложения использовать команду:
`mvn clean package -P build`.
Для сборки необходим запущенный докер, так как в нём поднимается тестовая БД, в которой применяются миграции и генерируются jooq-классы.
2. Для запуска приложения и БД в контейнерах:
`docker-compose up`

## Спецификация АПИ
http://localhost:8080/aupo/api/swagger-ui/index.html

## Логи
Записываются в logs.txt