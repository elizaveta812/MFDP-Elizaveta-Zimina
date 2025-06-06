# Heart Monitoring Telegram Bot

## Описание

Этот проект представляет собой телеграм-бота, который отправляет алерты в случае опасности сердечного приступа и предоставляет информацию о состоянии сердца. Бот предназначен для родственников людей с проблемами сердца, чтобы они могли следить за состоянием пожилых людей на расстоянии.


## Структура проекта

bot/

├── logs/                     # Папка для логов

│   ├── my_bot.log

├── Dockerfile                # Dockerfile для бота

├── bot.py                   # Запуск бота

├── model.py                  # Модель данных

├── config.py                  # Загрузка токена

├── handlers.py                  # Определение состояний

└── **init**.py

database/

├── database.py               # Модуль для работы с базой данных

└── **init**.py



tests/

├── test_main.py              # Тесты для ключевых функций бота

└── **init**.py



workers/

├── Dockerfile.worker         # Dockerfile для воркеров

├── worker.py                 # Логика воркеров

└── **init**.py

docker-compose.yml              # Конфигурация для Docker Compose

README.md                       # Документация проекта

requirements.txt               # Зависимости проекта

.gitignore                      # Файл для игнорирования файлов в Git

.env.template                   # Шаблон для переменных окружения



## Установка

1. Клонируйте репозиторий:
   ```
   bash
   git clone https://github.com/elizaveta812/MFDP-Elizaveta-Zimina.git
   cd heart-monitoring-bot
   ```
   

3. Установите зависимости:
   ```
   bash
   pip install -r requirements.txt
   ```
   

5. Настройте переменные окружения:
   - Скопируйте файл `.env.template` в `.env` и заполните необходимые значения.

6. Запустите приложение с помощью Docker Compose:
   ```
   bash
   docker-compose up --build
   ```
   

## Использование

- После запуска бота, найдите его в Telegram по имени пользователя и начните взаимодействие.
- Бот будет отправлять алерты в случае обнаружения опасных состояний сердца.
- Вы можете использовать команды для получения информации о состоянии сердца.

## Тестирование

Для запуска тестов выполните следующую команду:
```
bash
pytest tests/
```


## Логирование

Логи приложения сохраняются в папке `app/logs`. Убедитесь, что у вашего приложения есть права на запись в эту папку.

## Масштабируемость

Сервис может быть масштабирован путем увеличения количества воркеров. Для этого измените конфигурацию в `docker-compose.yml`.

