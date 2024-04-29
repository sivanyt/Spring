# Spring Course
Functional Requirements:
1. Як користувач, я хочу мати можливість створювати нове опитування, щоб збирати дані від клієнтів.
2. Як користувач, я хочу мати зручний інтерфейс для додавання нових клієнтів до опитування з вказанням їхньої початкової дати участі.
3. Як користувач, я хочу бачити дедлайн для завершення обробки результатів кожного опитування, щоб планувати роботу своєї команди.
4. Як адміністратор системи, я хочу мати можливість автоматично обробляти результати опитувань, щоб швидко отримувати аналіз даних.
5. Як користувач, я хочу бачити список доступних опитувань разом з їхнім призначенням та типом, щоб обрати потрібне для участі.
6. Як аналітик, я хочу мати зручний доступ до даних про кількість планованих опитувань для кожного типу, щоб проводити аналізи та прогнозувати обсяги роботи.
7. Як користувач, я хочу мати можливість визначити цілі та наміри кожного опитування, щоб точно встановити завдання для участників.
8. Як користувач, я хочу мати зручний доступ до інформації про регіони та важливість проведення опитувань у кожному кварталі, щоб краще розуміти контекст досліджень.
9. Як користувач, я хочу бачити статус обробки кожного опитування, щоб знати, чи готові дані для подальшого аналізу.
10. Як користувач, я хочу мати можливість швидко знаходити інформацію про кожне опитування, включаючи його назву, тип та призначення, щоб оперативно працювати з ними.

System Behaviours:
1. Створення опитування:
- Система дозволяє користувачам створювати нові опитування.
- Під час створення опитування, користувач вказує тип, призначення, назву опитування та його початкову та кінцеву дату.
2. Додавання клієнтів до опитування:
- Користувач може додавати клієнтів до кожного створеного опитування.
- При додаванні клієнта, вказується його ім'я та початкова дата участі в опитуванні.
3. Обробка результатів:
- Система автоматично обробляє результати кожного завершеного опитування.
- Після обробки, результати стають доступними для подальшого аналізу.
4. Перегляд даних про опитування:
- Користувач може переглядати список всіх доступних опитувань разом з їхнім призначенням, типом та статусом обробки.
- Для кожного опитування відображаються дані про кількість учасників та дату завершення.
5. Визначення цілей та намірів:
- Користувач може встановлювати цілі та наміри кожного опитування, щоб визначити його основні завдання та спрямування.
6. Перегляд інформації про квартали:
- Система надає користувачам можливість переглядати дані про квартали, в яких проводяться опитування.
- Для кожного кварталу відображається інформація про регіон, важливість та назву опитування.
7. Визначення типу опитування:
- Користувач може переглядати і встановлювати тип кожного опитування, щоб краще класифікувати їх.
8. Перегляд кількості планованих опитувань:
- Користувач має доступ до інформації про кількість планованих опитувань для кожного типу, щоб зрозуміти обсяг роботи.

REST API endpoints:
1. Створення опитування:
- Метод: POST
- URL: /surveys
- Параметри: тип, призначення, назва, початкова та кінцева дата
2. Додавання клієнта до опитування:
- Метод: POST
- URL: /surveys/{survey_id}/clients
- Параметри: ім'я клієнта, початкова дата
3. Встановлення кінцевої дати для опитування:
- Метод: PUT
- URL: /surveys/{survey_id}
- Параметри: кінцева дата
4. Отримання результатів обробки:
- Метод: GET
- URL: /surveys/{survey_id}/results
5. Визначення типу опитування:
- Метод: GET
- URL: /surveys/{survey_id}/type
6. Встановлення цілей та намірів опитування:
- Метод: PUT
- URL: /surveys/{survey_id}
7. Отримання кількості планованих опитувань:
- Метод: GET
- URL: /surveys/{survey_id}/planned_amount
8. Перегляд інформації про квартали:
- Метод: GET
- URL: /quarters/{quarter_id}/surveys
