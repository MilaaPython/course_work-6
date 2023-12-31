# Проект "Сервис рассылок"

## Краткое описание

Проект, в которой зарегестрированный пользователь может осуществлять автоматическую рассылку email заданному списку адресатов. Проект выполнен на Windows.
Создан с использованием Python и Django. В проекте настроена авторизация настроена, кэширование и асинхронное выполнение задач с помощью Schedule. В качестве брокера используется Redis, в качестве базы данных PostgreSQL.

## Инструкция по запуску
1. Создайте файл .env по образцу в файле .env.sample
2. Установите зависимости проекта, указанные в файле pyproject.toml
3. Установите redis (ссылка на пакет: https://github.com/microsoftarchive/redis/releases)
4. Запустите сервер:
   ```bash
   python manage.py runserver
   ```
5. Выполните миграции
6. При необходимости загрузите тестовые данные с помощью фикстуры или же внесите свои собственные данные.
7. Для создания superuser выполните команду csu
    ```bash
   python manage.py csu
   ```
8. Для запуска рассылок необходимо выполнить команду schedule (настройки находятся в файле schedule по пути
   apps/mailings/management/commands)
    ```bash
   python manage.py schedule
   ```
    
## Технологии в проекте (стек)

* Python 3.11
* Django
* PostgreSQL
* Redis
* Schedule
