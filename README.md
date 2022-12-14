### Описание:
Модуль API - Социальная сеть для публикации личных дневников.
### Технологии:
- Python 3.7
- Django 2.2.19
- Django Rest Framework 3.12.4
### Запуск проекта в dev-режиме:

Клонировать репозиторий и перейти в него в командной строке:

```
https://github.com/HoneyKnight/REST_API_Yatube
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
py -3.7 -m venv venv
```

```
source venv/scripts/activate
```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект

```
python3 manage.py runserver
```

### Примеры запросов

Метод запроса GET:

```
api/v1/posts/
```

Пример тела ответа:

```
    {
        "id": 0,
        "author": "string",
        "text": "string",
        "pub_date": "2019-08-24T14:15:22Z",
        "image": "string or null",
        "group": "integer or null"
    }
```

Функционал эндпоинта:
```
Выдаёт список всех постов 
```

Метод запроса POST:

```
api/v1/posts/{post_id}/comments/
```

Пример тела запроса:

```
    {
    "text": "string"
    }
```

Пример тела ответа:

```
    {
        "id": 0,
        "author": "string",
        "text": "string",
        "created": "2019-08-24T14:15:22Z",
        "post": 0
    }
```

Функционал эндпоинта:

```
Создаёт новый комментарий к выбранной публикации
```
