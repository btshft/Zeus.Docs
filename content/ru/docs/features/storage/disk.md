---
title: Дисковое хранилище
type: docs
bookToC: false
---

# Дисковое хранилище

Персистентное дисковое хранилище реализовано с помощью библиотеки [Microsoft.FASTER](https://github.com/microsoft/FASTER). Для подключения хранилища необходимо изменить `appsettings.json`, схема представлена ниже. Скобками обозначены поля необязательные к заполнению.

```html
  "Alerting": {
    "Subscriptions": {
      "Store": {
        "Faster": {
          # Путь к папке с хранилищем
          [ "Directory": <path> | default: "./storage" ],

          # Название хранилища
          [ "Name": <string> | default: "zeus" ]
        }
      }
    }
  }
```

### Пример

Пример блока, добавлющего интеграцию с дисковым хранилищем представлен ниже.

```json
{
  "Alerting": {
    "Subscriptions": {
      "Store": {
        "Faster": {
          "Directory": "./database"
        }
      }
    }
  }
}
```