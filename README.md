
# Курсовая работа 5. Работа с базами данных 

Получает данные о компаниях и вакансиях с сайта hh.ru, спроектированы таблицы в БД PostgreSQL и загружены полученные данные в созданные таблицы.

## Выполненные требования

- Получил данные о 10 работодателях и их вакансиях с сайта [hh.ru](http://hh.ru/). 
Для этого использовал публичный API [hh.ru](http://hh.ru/) и библиотеку `requests`.

- Спроектировал таблицы в БД Postgres для хранения полученных данных о работодателях и их вакансиях. Для работы с БД использовал библиотеку `psycopg2`.
- Реализовал код, который заполняет созданные таблицы в БД Postgres данными о работодателях и их вакансиях.
- Создал класс `DBManager` для работы с данными в БД.

## Класс DBManager

Класс `DBManager`, который подключается к БД Postgres и имеет следующие методы:

- `get_companies_and_vacancies_count()`: получает список всех компаний и количество вакансий у каждой компании.
- `get_all_vacancies()`: получает список всех вакансий с указанием названия компании, названия вакансии и зарплаты и ссылки на вакансию.
- `get_avg_salary()`: получает среднюю зарплату по вакансиям.
- `get_vacancies_with_higher_salary()`: получает список всех вакансий, у которых зарплата выше средней по всем вакансиям.
- `get_vacancies_with_keyword()`: получает список всех вакансий, в названии которых содержатся переданные в метод слова, например “python”.
