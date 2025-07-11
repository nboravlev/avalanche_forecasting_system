# avalache_forecasting_system
Intelligent system for collecting meteorological data, forecasting ski resort avalanche restrictions, and delivering real-time insights via a Telegram bot. Powered by ML, microservices, and containerized architecture.

Структура проета вариант 1

```
/project-root
├── README.md            # Основное описание проекта
├── docker-compose.yml   # Сборка и запуск контейнеров
├── .gitignore
├── /docs                # Дополнительные технические заметки и схемы
│   ├── architecture.md  # Архитектура системы
│   ├── db_schema.md     # Структура базы данных
│   └── diagrams/        # Сюда можно складывать схемы из draw.io
├── /src                 # Исходный код микросервисов
│   ├── bot/
│   ├── parser/
│   └── ml_pipeline/
└── /airflow             # Конфигурация Airflow (если будет)

```

Структура проекта вариант 2
```
/project-root
├── README.md                # Описание проекта и инструкции по запуску
├── docker-compose.yml       # Сборка и оркестрация контейнеров
├── .gitignore
├── requirements.txt         # Основные Python-зависимости (если общий requirements)
├── /docs                    # Дополнительная документация, схемы, архитектура
│   ├── architecture.md
│   ├── db_schema.md
│   └── diagrams/
├── /src                     # Исходный код микросервисов
│   ├── bot/                 # Telegram-бот и AI-агент
│   │   ├── bot.py
│   │   └── requirements.txt
│   ├── parser/              # Парсер сообщений из Telegram
│   │   ├── telegram_listener.py
│   │   └── requirements.txt
│   ├── ml_pipeline/         # Код для подготовки данных и ML-моделей
│   │   ├── train.py
│   │   ├── predict.py
│   │   └── requirements.txt
│   └── common/              # Общие утилиты и библиотеки (например, для работы с БД)
├── /airflow                 # Настройка и DAG-и для Apache Airflow
│   ├── dags/
│   └── docker-compose.yml
├── /database
│   ├── init.sql             # Скрипты для инициализации PostgreSQL
│   └── docker-compose.yml
└── /tests                   # Тесты для микросервисов

```
| Компонент     | Описание                                              |
| ------------- | ----------------------------------------------------- |
| `parser`      | Слушает чаты Telegram, парсит сообщения, пишет в БД   |
| `bot`         | Telegram-бот для получения предсказаний и уведомлений |
| `ml_pipeline` | Подготовка данных, обучение и инференс модели         |
| `database`    | PostgreSQL, хранение метеоданных и событий            |
| `airflow`     | Планировщик задач для автоматизации пайплайнов        |
| `docs`        | Схемы, техническая документация проекта               |


Что планируется

✅ Сбор и парсинг исторических данных из Telegram

✅ Разработка микросервисной архитектуры

✅ Хранение данных в PostgreSQL

✅ Разработка ML-модели для предсказания ограничений

✅ Интеграция модели с Telegram-ботом

✅ Внедрение Airflow для оркестрации процессов

✅ Реализация AI-агента для интеллектуальных ответов (расширение)
