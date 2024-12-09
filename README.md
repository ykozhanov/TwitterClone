# Twitter Clone
Исполнитель: **Юрий Кожанов**

-------------------------------------------------------------------------------------

## Описание проекта
Корпоративный аналог Твиттера с базовыми возможностями:
- Пользователь может добавить новый твит. 
- Пользователь может удалить свой твит. 
- Пользователь может зафоловить другого пользователя. 
- Пользователь может отписаться от другого пользователя. 
- Пользователь может отмечать твит как понравившийся. 
- Пользователь может убрать отметку «Нравится». 
- Пользователь может получить ленту из твитов, отсортированных в порядке убывания по популярности от пользователей, 
которых он фоловит. 
- Твит может содержать картинку. 

Приложение запускается через Docker Compose и не теряет данные между перезапусками.

Также доступна Swagger документация для API приложения.

## Содержание
- [Установка](#установка-и-запуск)
- [Использование](#использование)
- [Тестирование](#тестирование)
- [Используемые инструменты](#используемые-инструменты)
- [Контакты](#контакты)


## Установка и запуск
### Шаг 1: Предварительная настройка
Перед использованием приложения убедитесь, что на Вашем устройстве (Linux-based OS) установлены:
- **Docker 27.2.0**
- **docker-compose 2.29.2**

### Шаг 2: Клонируйте репозиторий
Клонируйте gitlab репозиторий на Ваше устройство:
```bash
git clone https://gitlab.skillbox.ru/iurii_kozhanov/python_advanced_diploma.git
```

### Шаг 3: Docker-Compose
- Перейдите в директорию с репозиторием:
```bash
cd python python_advanced_diploma
```
- Создайте `.env` файл с переменными. Для примера используйте `env.example` из репозитория.
- Для запуска выполните в терминале: 
```bash 
docker-compose up
```


## Использование
- В интернет-браузере откройте http://localhost/, чтобы открыть главную страницу.
- В интернет-браузере откройте http://localhost:8000/docs, чтобы получить доступ к Swagger документации API проекта.

## Тестирование
### Шаг 1: Предварительная настройка
- Для запуска тестов необходимо убедиться, что в `.env` указан URL для тестовой базы данных.
- Перед тестированием приложения убедитесь, что на Вашем устройстве (Linux-based OS) установлен **python 3.12.5**.

### Шаг 2: Запуск тестовой базы данных
```bash
docker-compose -f test-docker-compose.yml up
```

### Шаг 3: Подготовка виртуального окружения
- Создайте виртуальное окружение, выполнив команду: 
```bash
python -m venv venv
```
- Перейдите в директорию с тестами, выполнив в терминале команду: 
```bash
cd tests
```
- Установите необходимые зависимости через команду: 
```bash
pip install -r requirements_test.txt
```

### Шаг 4. Запуск тестов
Запустите выполнение тестов, выполнив в терминале: 
```bash
pytest
```


## Используемые инструменты
- [Python](https://www.python.org/) как основной язык программирования;
- [FastAPI](https://fastapi.tiangolo.com/) как backend сервиса;
- [Nginx](https://nginx.org/en/) как веб-сервер;
- [Postresql](https://www.postgresql.org/) как база данных;
- [SQLAlchemy 2.0](https://www.sqlalchemy.org/) как ORM инструмент;
- [Alembic](https://alembic.sqlalchemy.org/en/latest/) как инструмент миграций базы данных;
- [Pytest](https://docs.pytest.org/en/stable/) как инструмент тестирования.


## Контакты
По вопросам проекта и другим вопросам связанным с используемыми в проекте инструментам 
можно писать на почту `ykozhanov97@gmail.com`
