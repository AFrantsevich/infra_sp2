### Описание проекта:
Данный проект предназначен для отработки навыков использования приложения Docker.

### Технологии:
Postman
Python 3.7.9
Django 2.2.16

### Шаблон для .env:
- DB_ENGINE=django.db.backends.postgresql # указываем, что работаем с postgresql
- DB_NAME=postgres # имя базы данных
- POSTGRES_USER=postgres # логин для подключения к базе данных
- POSTGRES_PASSWORD=postgres # пароль для подключения к БД (установите свой)
- DB_HOST=db # название сервиса (контейнера)
- DB_PORT=5432 # порт для подключения к БД 
- SECRET_KEY='' # Django settings key

### Сборка и запуск контейнеров:
- docker-compose -d --build
- docker-compose exec web python manage.py migrate
- docker-compose exec web python manage.py createsuperuser
- docker-compose exec web python manage.py collectstatic --no-input
