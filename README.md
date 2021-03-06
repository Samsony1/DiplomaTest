# Дипломный проект профессии «Тестировщик»

 [План Автоматизации](https://github.com/Samsony1/DiplomaTest/blob/main/docs/Plan.md)
 
 [Отчет по итогам Тестирования](https://github.com/Samsony1/DiplomaTest/blob/main/docs/Report.md)
 
 [Отчет по итогам Автоматизации](https://github.com/Samsony1/DiplomaTest/blob/main/docs/Summary.md)
 
 [Allure Report](https://github.com/Samsony1/DiplomaTest/blob/main/docs/Allure.png)

## Инструкция по запуску

1. Запустить контейнеры docker:  

    Для работы с базой данных mysql выполнить команду:  
    <code>docker-compose -f docker-compose-mysql.yml up -d</code>
    После прогона тестов остановить контейнеры:  
    <code>docker-compose -f docker-compose-mysql.yml down</code>

    Для работы с базой данных postgres выполнить команду:  
    <code>docker-compose -f docker-compose-postgres.yml up -d</code>
    После прогона тестов остановить контейнеры:  
    <code>docker-compose -f docker-compose-postgres.yml down</code>

2. Запустить приложение:  

    Для запуска приложения с базой данных mysql выполнить команду:  
    <code>java -Dspring.datasource.url=jdbc:mysql://localhost:3306/app -jar aqa-shop.jar</code>

    Для запуска приложения с базой данных postgres выполнить команду:  
    <code>java -Dspring.datasource.url=jdbc:postgresql://localhost:5432/app -jar aqa-shop.jar</code>

3. Запустить тесты:  

   Для запуска тестов с базой данных mysql выполнить команду:  
   <code>gradlew test -Ddb.url=jdbc:mysql://localhost:3306/app</code>

   Для запуска тестов с базой данных postgres выполнить команду:  
   <code>gradlew test -Ddb.url=jdbc:postgresql://localhost:5432/app</code>

4. Сформировать отчеты командой:  
   <code>gradlew allureReport</code>  

5. Открыть отчеты в браузере командой:  
   <code>gradlew allureServe</code>





