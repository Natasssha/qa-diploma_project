## Дипломный проект по курсу «Тестировщик ПО»

#### О проекте:
Дипломный проект представляет собой автоматизацию тестирования комплексного сервиса, взаимодействующего с СУБД и API Банка.
Приложение предлагает купить тур по определённой цене двумя способами:

1. Обычная оплата по дебетовой карте
2. Выдача кредита по данным банковской карты.  

Само приложение не обрабатывает данные по картам, а пересылает их банковским сервисам:

1. Cервису платежей;

2. Кредитному сервису.

## Инструкция по запуску тестов:

### Предварительная подготовка к тестированию:

Установить IntelliJ Idea. Скачать и ознакомиться с документацией можно на официальном сайте https://www.jetbrains.com/ru-ru/idea/.

Установить Docker Desktop. Скачать и ознакомиться с документацией можно на официальном сайте https://www.docker.com/get-started.

Для запуска тестов необходимо:

Скачать проект с удаленного репозитория на свой локальный, с помощью команды git clone https://github.com/Natasssha/qa-diploma_project.git

Открыть проект на установленной заранее IntelliJ Idea

Развернуть контейнеры с помощью команды docker-compose up в терминале.

В соседней вкладке запустить само приложение либо командой:

"java -jar .\artifacts\aqa-shop.jar --spring.datasource.url=jdbc:postgresql://localhost:5432/app" для запуска БД PostgreSQL;

"java -jar .\artifacts\aqa-shop.jar --spring.datasource.url=jdbc:mysql://localhost:3306/app" для запуска БД MySQL 

#### Запустить тесты командой
./gradlew clean test.

Для генерации отчета Allure о выполненных тестах прописываем в терминале команду: 

./gradlew allureServe

Сгенерированный отчет откроется автоматически в браузере используемом по умолчанию.
