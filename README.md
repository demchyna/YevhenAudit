## Опис проекту

Проект написаний мовою програмування Java. Для створення проекту були використані фреймворки Spring Boot, Spring IoC, Spring MVC, Spring Security, Hibernate (ORM), Spring Data JPA, Hibernate Validator, шаблонізатор Thymeleaf. Для збереження даних використовується СКБД PostgreSQL.

В основі розробленого додатку лежить шаблон проектування MVC. Структурно додаток розділено на ряд шарів, а саме: DAO (Data Access Object) – шар доступу до бази даних; Service – сервісний шар роботи з даними; Model – шар представлення даних та їх відображення на таблиці з БД; Controller – шар обробки запитів користувача; View – шар візуального представлення даних клієнту. Такий поділ дозволяє послабити зв’язки між компонентами програми і передбачає горизонтальне масштабування в майбутньому. 

Процедура автентифікації та авторизації користувача реалізована засобами фреймворку Spring Security. Дані про користувачів зберігаються в базі даних. Кожен користувач може мати одну із двох наперед визначених ролей – ADMIN або USER. Роль ADMIN забезпечує монопольний доступ до всіх ресурсів програми. Користувач з роллю USER має доступ тільки до тих ресурсів, які були особисто створені ним. Усі паролі зберігаються в БД у захешованому вигляді. Для хешування паролів використовується стійка до зламування криптографічна функція Bcrypt.

Розроблений веб-додаток розгорнуто на безкоштовній хмарній PaaS-платформі Heroku. Уся процедура розгортання описана тут: [Deploying Spring Boot Applications to Heroku](https://devcenter.heroku.com/articles/deploying-spring-boot-apps-to-heroku).
