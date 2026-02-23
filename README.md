# motivation_app_data

Данные для приложения [motivation_app](https://github.com/AndreyFrigoris/motivation_app): цитаты в формате JSON. Приложение при старте загружает файлы отсюда и кэширует их локально.

## Структура

В папке **`data/`** лежат JSON-файлы:

| Файл | Описание |
|------|----------|
| `quotes_main.json` | Основные цитаты (EN) |
| `quotes_main_ru.json` | Основные цитаты (RU) |
| `quotes_stoic.json` | Стоические цитаты (EN) |
| `quotes_stoic_ru.json` | Стоические цитаты (RU) |
| `quotes_noty.json` | Цитаты для уведомлений (EN) |
| `quotes_noty_ru.json` | Цитаты для уведомлений (RU) |

Каждый файл — массив объектов с полями:

- `text` — текст цитаты  
- `author` — автор или источник  
- `imageUrl` — путь к фоновому изображению (например `assets/images/bg_01.jpg`)

## Как приложение использует данные

Приложение запрашивает файлы по адресу:

`https://raw.githubusercontent.com/AndreyFrigoris/motivation_app_data/master/data/<имя_файла>`

При каждом запуске кэш обновляется из этого репозитория; при отсутствии сети используются данные, встроенные в приложение (assets).

## Лицензия

Контент распространяется под лицензией **CC0 1.0 Universal** (Public Domain). Подробности — в файле [LICENSE](LICENSE).
