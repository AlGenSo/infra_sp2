**Проект: запуск docker-compose**
---
---
### Описание
##### Идея проекта
Проект YaMDb собирает отзывы пользователей на произведения.
Здесь нельзя посмотреть фильм или послушать музыку.
Произведения делятся на категории, такие как «Книги», «Фильмы», «Музыка».
##### Задача проекта
Отправить проект «работодателю» «вместе с компьютером» — в контейнере.
Результаты тестовых заданий для Python-разработчиков часто просят отправлять в контейнерах. Это делается для того, чтобы человеку, который будет проверять ваше тестовое, не пришлось настраивать окружение на своём компьютере.

---
### Технологии:
- Django 
- Django REST Framework
- Django Filter
- PyJWT
- Docker
- PostgreSQL
- Nginx
- Gunicorn
---
### Запуск проекта
##### Для тестирования запросов можно использовать
[Postman](https://www.postman.com/downloads/)
##### Запуск проекта
* _Клонировать репозиторий: `git clone` git@github.com:AlGenSo/infra_sp2.git_
* _Перейти в него в командной строке: `cd infra_sp2`_
* _Перейти в папку infra: `cd infra`_
* _Создать файл .env, с параметрами:_
   ```
   DB_ENGINE=django.db.backends.postgresql
   DB_NAME=postgres
   POSTGRES_USER=postgres
   POSTGRES_PASSWORD=postgres
   DB_HOST=db
   DB_PORT=5432
   ```
* _Собрать образ при помощи docker-compose: `$ docker-compose up -d --build`_
* _Выполнить по почереди следующие команды:_

  _Замечание: При использовании ОС Win 11 Home, некоторые команды не проходят без префикса winpty (например, при создании суперюзера)_

   ```
   docker-compose exec web python manage.py migrate # Выполнить миграции
   docker-compose exec web python manage.py createsuperuser # Создать суперюзера
   docker-compose exec web python manage.py collectstatic --no-input # Собрать статику
   ```
* _После запуска проекта, будет доступна документация http://localhost/redoc/_
---
---

### Команда разработчиков проекта api_yamdb:
[X] Кондаков Тимофей
[X] Сенгилейцев Никита
[X] Солодовников Александр (по совместительству тимлид)
---

### Разработчик проекта **Запуск docker-compose**:
##### Солодовников Александр
---