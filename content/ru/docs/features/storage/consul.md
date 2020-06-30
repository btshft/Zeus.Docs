---
title: Хранилище Consul
type: docs
bookToC: false
---

# Хранилище Consul

Хранилище Consul поддерживается начиная с версии [API 1.6.1](https://github.com/hashicorp/consul/tree/v1.6.1/api). 
Подключение хранилища осуществляется путем изменения `appsettings.json`, схема представлена ниже. Скобками обозначены необязательные для заполнения поля

```html
  "Alerting": {
    "Subscriptions": {
      "Store": {
        "Consul": {
          # Адрес Consul-сервера для подключения
          "Address": <url>,

          # Токен для авторизации
          [ "Token": <string> | default : null ],

          # Время ожидания при запросе
          [ "WaitTime": <duration> | default: null ],
           
          # Название ДЦ
          [ "Datacenter" <string> | default: null ]
        }
      }
    }
  }
```

### Пример

Пример блока, добавлющего интеграцию с Consul представлен ниже.

```json
{
  "Alerting": {
    "Subscriptions": {
      "Store": {
        "Consul": {
          "Address": "http://127.0.0.1:8500"
        }
      }
    }
  }
}
```